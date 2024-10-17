# Sky shaders

Sky shaders are a special type of shader used for drawing sky
backgrounds and for updating radiance cubemaps which are used for
image-based lighting (IBL). Sky shaders only have one processing
function, the `sky()` function.

There are three places the sky shader is used.

-   First the sky shader is used to draw the sky when you have selected
    to use a Sky as the background in your scene.
-   Second, the sky shader is used to update the radiance cubemap when
    using the Sky for ambient color or reflections.
-   Third, the sky shader is used to draw the lower res subpasses which
    can be used in the high-res background or cubemap pass.

In total, this means the sky shader can run up to six times per frame,
however, in practice it will be much less than that because the radiance
cubemap does not need to be updated every frame, and not all subpasses
will be used. You can change the behavior of the shader based on where
it is called by checking the `AT_*_PASS` booleans. For example:

    shader_type sky;

    void sky() {
        if (AT_CUBEMAP_PASS) {
            // Sets the radiance cubemap to a nice shade of blue instead of doing
            // expensive sky calculations
            COLOR = vec3(0.2, 0.6, 1.0);
        } else {
            // Do expensive sky calculations for background sky only
            COLOR = get_sky_color(EYEDIR);
        }
    }

When using the sky shader to draw a background, the shader will be
called for all non-occluded fragments on the screen. However, for the
background's subpasses, the shader will be called for every pixel of the
subpass.

When using the sky shader to update the radiance cubemap, the sky shader
will be called for every pixel in the cubemap. On the other hand, the
shader will only be called when the radiance cubemap needs to be
updated. The radiance cubemap needs to be updated when any of the shader
parameters are updated. For example, if `TIME` is used in the shader,
then the radiance cubemap will update every frame. The following list of
changes force an update of the radiance cubemap:

-   `TIME` is used.
-   `POSITION` is used and the camera position changes.
-   If any `LIGHTX_*` properties are used and any
    `DirectionalLight3D <class_DirectionalLight3D>` changes.
-   If any uniform is changed in the shader.
-   If the screen is resized and either of the subpasses are used.

Try to avoid updating the radiance cubemap needlessly. If you do need to
update the radiance cubemap each frame, make sure your
`Sky process mode <class_Sky_property_process_mode>` is set to
`PROCESS_MODE_REALTIME <class_Sky_constant_PROCESS_MODE_REALTIME>`.

Note that the `process mode <class_Sky_property_process_mode>` only
affects the rendering of the radiance cubemap. The visible sky is always
rendered by calling the fragment shader for every pixel. With complex
fragment shaders, this can result in a high rendering overhead. If the
sky is static (the conditions listed above are met) or changes slowly,
running the full fragment shader every frame is not needed. This can be
avoided by rendering the full sky into the radiance cubemap, and reading
from this cubemap when rendering the visible sky. With a completely
static sky, this means that it needs to be rendered only once.

The following code renders the full sky into the radiance cubemap and
reads from that cubemap for displaying the visible sky:

    shader_type sky;

    void sky() {
        if (AT_CUBEMAP_PASS) {
            vec3 dir = EYEDIR;

            vec4 col = vec4(0.0);

            // Complex color calculation

            COLOR = col.xyz;
            ALPHA = 1.0;
        } else {
            COLOR = texture(RADIANCE, EYEDIR).rgb;
        }
    }

This way, the complex calculations happen only in the cubemap pass,
which can be optimized by setting the sky's
`process mode <class_Sky_property_process_mode>` and the
`radiance size <class_Sky_property_radiance_size>` to get the desired
balance between performance and visual fidelity.

## Render modes

Subpasses allow you to do more expensive calculations at a lower
resolution to speed up your shaders. For example the following code
renders clouds at a lower resolution than the rest of the sky:

    shader_type sky;
    render_mode use_half_res_pass;

    void sky() {
        if (AT_HALF_RES_PASS) {
            // Run cloud calculation for 1/4 of the pixels
            vec4 color = generate_clouds(EYEDIR);
            COLOR = color.rgb;
            ALPHA = color.a;
        } else {
            // At full resolution pass, blend sky and clouds together
            vec3 color = generate_sky(EYEDIR);
            COLOR = color + HALF_RES_COLOR.rgb * HALF_RES_COLOR.a;
        }
    }

<table>
<colgroup>
<col style="width: 27%" />
<col style="width: 72%" />
</colgroup>
<thead>
<tr>
<th>Render mode</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>use_half_res_pass</strong></td>
<td>Allows the shader to write to and access the half resolution
pass.</td>
</tr>
<tr>
<td><strong>use_quarter_res_pass</strong></td>
<td>Allows the shader to write to and access the quarter resolution
pass.</td>
</tr>
<tr>
<td><strong>disable_fog</strong></td>
<td>If used, fog will not affect the sky.</td>
</tr>
</tbody>
</table>

## Built-ins

Values marked as `in` are read-only. Values marked as `out` can
optionally be written to and will not necessarily contain sensible
values. Samplers cannot be written to so they are not marked.

## Global built-ins

Global built-ins are available everywhere, including in custom
functions.

There are 4 `LIGHTX` lights, accessed as `LIGHT0`, `LIGHT1`, `LIGHT2`,
and `LIGHT3`.

<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 78%" />
</colgroup>
<thead>
<tr>
<th>Built-in</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>in float <strong>TIME</strong></td>
<td>Global time since the engine has started, in seconds. It repeats
after every <code>3,600</code> seconds (which can be changed with the
<code class="interpreted-text"
role="ref">rollover&lt;class_ProjectSettings_property_rendering/limits/time/time_rollover_secs&gt;</code>
setting). It's not affected by <code class="interpreted-text"
role="ref">time_scale&lt;class_Engine_property_time_scale&gt;</code> or
pausing. If you need a <code>TIME</code> variable that can be scaled or
paused, add your own <code class="interpreted-text"
role="ref">global shader uniform&lt;doc_shading_language_global_uniforms&gt;</code>
and update it each frame.</td>
</tr>
<tr>
<td>in vec3 <strong>POSITION</strong></td>
<td>Camera position, in world space.</td>
</tr>
<tr>
<td>samplerCube <strong>RADIANCE</strong></td>
<td>Radiance cubemap. Can only be read from during background pass.
Check <code>!AT_CUBEMAP_PASS</code> before using.</td>
</tr>
<tr>
<td>in bool <strong>AT_HALF_RES_PASS</strong></td>
<td><code>true</code> when rendering to half resolution pass.</td>
</tr>
<tr>
<td>in bool <strong>AT_QUARTER_RES_PASS</strong></td>
<td><code>true</code> when rendering to quarter resolution pass.</td>
</tr>
<tr>
<td>in bool <strong>AT_CUBEMAP_PASS</strong></td>
<td><code>true</code> when rendering to radiance cubemap.</td>
</tr>
<tr>
<td>in bool <strong>LIGHTX_ENABLED</strong></td>
<td><code>true</code> if <code>LIGHTX</code> is visible and in the
scene. If <code>false</code>, other light properties may be
garbage.</td>
</tr>
<tr>
<td>in float <strong>LIGHTX_ENERGY</strong></td>
<td>Energy multiplier for <code>LIGHTX</code>.</td>
</tr>
<tr>
<td>in vec3 <strong>LIGHTX_DIRECTION</strong></td>
<td>Direction that <code>LIGHTX</code> is facing.</td>
</tr>
<tr>
<td>in vec3 <strong>LIGHTX_COLOR</strong></td>
<td>Color of <code>LIGHTX</code>.</td>
</tr>
<tr>
<td>in float <strong>LIGHTX_SIZE</strong></td>
<td>Angular diameter of <code>LIGHTX</code> in the sky. Expressed in
radians. For reference, the sun from earth is about .0087 radians (0.5
degrees).</td>
</tr>
<tr>
<td>in float <strong>PI</strong></td>
<td>A <code>PI</code> constant (<code>3.141592</code>). A ratio of a
circle's circumference to its diameter and amount of radians in half
turn.</td>
</tr>
<tr>
<td>in float <strong>TAU</strong></td>
<td>A <code>TAU</code> constant (<code>6.283185</code>). An equivalent
of <code>PI * 2</code> and amount of radians in full turn.</td>
</tr>
<tr>
<td>in float <strong>E</strong></td>
<td>An <code>E</code> constant (<code>2.718281</code>). Euler's number
and a base of the natural logarithm.</td>
</tr>
</tbody>
</table>

## Sky built-ins

<table>
<colgroup>
<col style="width: 24%" />
<col style="width: 75%" />
</colgroup>
<thead>
<tr>
<th>Built-in</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>in vec3 <strong>EYEDIR</strong></td>
<td>Normalized direction of current pixel. Use this as your basic
direction for procedural effects.</td>
</tr>
<tr>
<td>in vec2 <strong>SCREEN_UV</strong></td>
<td>Screen UV coordinate for current pixel. Used to map a texture to the
full screen.</td>
</tr>
<tr>
<td>in vec2 <strong>SKY_COORDS</strong></td>
<td>Sphere UV. Used to map a panorama texture to the sky.</td>
</tr>
<tr>
<td>in vec4 <strong>HALF_RES_COLOR</strong></td>
<td>Color value of corresponding pixel from half resolution pass. Uses
linear filter.</td>
</tr>
<tr>
<td>in vec4 <strong>QUARTER_RES_COLOR</strong></td>
<td>Color value of corresponding pixel from quarter resolution pass.
Uses linear filter.</td>
</tr>
<tr>
<td>out vec3 <strong>COLOR</strong></td>
<td>Output color.</td>
</tr>
<tr>
<td>out float <strong>ALPHA</strong></td>
<td>Output alpha value, can only be used in subpasses.</td>
</tr>
<tr>
<td>out vec4 <strong>FOG</strong></td>
<td></td>
</tr>
</tbody>
</table>
