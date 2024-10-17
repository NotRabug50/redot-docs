# CanvasItem shaders

CanvasItem shaders are used to draw all 2D elements in Godot. These
include all nodes that inherit from CanvasItems, and all GUI elements.

CanvasItem shaders contain fewer built-in variables and functionality
than `Spatial shaders<doc_spatial_shader>`, but they maintain the same
basic structure with vertex, fragment, and light processor functions.

## Render modes

<table>
<colgroup>
<col style="width: 32%" />
<col style="width: 67%" />
</colgroup>
<thead>
<tr>
<th>Render mode</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>blend_mix</strong></td>
<td>Mix blend mode (alpha is transparency), default.</td>
</tr>
<tr>
<td><strong>blend_add</strong></td>
<td>Additive blend mode.</td>
</tr>
<tr>
<td><strong>blend_sub</strong></td>
<td>Subtractive blend mode.</td>
</tr>
<tr>
<td><strong>blend_mul</strong></td>
<td>Multiplicative blend mode.</td>
</tr>
<tr>
<td><strong>blend_premul_alpha</strong></td>
<td>Pre-multiplied alpha blend mode.</td>
</tr>
<tr>
<td><strong>blend_disabled</strong></td>
<td>Disable blending, values (including alpha) are written as-is.</td>
</tr>
<tr>
<td><strong>unshaded</strong></td>
<td>Result is just albedo. No lighting/shading happens in material.</td>
</tr>
<tr>
<td><strong>light_only</strong></td>
<td>Only draw on light pass.</td>
</tr>
<tr>
<td><strong>skip_vertex_transform</strong></td>
<td><code>VERTEX</code> needs to be transformed manually in the
<code>vertex()</code> function.</td>
</tr>
<tr>
<td><strong>world_vertex_coords</strong></td>
<td><code>VERTEX</code> is modified in world coordinates instead of
local.</td>
</tr>
</tbody>
</table>

## Built-ins

Values marked as `in` are read-only. Values marked as `out` can
optionally be written to and will not necessarily contain sensible
values. Values marked as `inout` provide a sensible default value, and
can optionally be written to. Samplers cannot be written to so they are
not marked.

## Global built-ins

Global built-ins are available everywhere, including custom functions.

<table>
<colgroup>
<col style="width: 18%" />
<col style="width: 81%" />
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

## Vertex built-ins

Vertex data (`VERTEX`) is presented in local space (pixel coordinates,
relative to the Node2D's origin). If not written to, these values will
not be modified and be passed through as they came.

The user can disable the built-in model to world transform (world to
screen and projection will still happen later) and do it manually with
the following code:

    shader_type canvas_item;
    render_mode skip_vertex_transform;

    void vertex() {

        VERTEX = (MODEL_MATRIX * vec4(VERTEX, 0.0, 1.0)).xy;
    }

Other built-ins, such as `UV` and `COLOR`, are also passed through to
the `fragment()` function if not modified.

For instancing, the `INSTANCE_CUSTOM` variable contains the instance
custom data. When using particles, this information is usually:

-   **x**: Rotation angle in radians.
-   **y**: Phase during lifetime (`0.0` to `1.0`).
-   **z**: Animation frame.

<table>
<colgroup>
<col style="width: 38%" />
<col style="width: 61%" />
</colgroup>
<thead>
<tr>
<th>Built-in</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>in mat4 <strong>MODEL_MATRIX</strong></td>
<td>Local space to world space transform. World space is the coordinates
you normally use in the editor.</td>
</tr>
<tr>
<td>in mat4 <strong>CANVAS_MATRIX</strong></td>
<td>World space to canvas space transform. In canvas space the origin is
the upper-left corner of the screen and coordinates ranging from
<code>(0.0, 0.0)</code> to viewport size.</td>
</tr>
<tr>
<td>in mat4 <strong>SCREEN_MATRIX</strong></td>
<td>Canvas space to clip space. In clip space coordinates ranging from
<code>(-1.0, -1.0)</code> to <code>(1.0, 1.0).</code></td>
</tr>
<tr>
<td>in int <strong>INSTANCE_ID</strong></td>
<td>Instance ID for instancing.</td>
</tr>
<tr>
<td>in vec4 <strong>INSTANCE_CUSTOM</strong></td>
<td>Instance custom data.</td>
</tr>
<tr>
<td>in bool <strong>AT_LIGHT_PASS</strong></td>
<td>Always <code>false</code>.</td>
</tr>
<tr>
<td>in vec2 <strong>TEXTURE_PIXEL_SIZE</strong></td>
<td>Normalized pixel size of default 2D texture. For a Sprite2D with a
texture of size 64x32px, <strong>TEXTURE_PIXEL_SIZE</strong> =
<code>vec2(1/64, 1/32)</code></td>
</tr>
<tr>
<td>inout vec2 <strong>VERTEX</strong></td>
<td>Vertex position, in local space.</td>
</tr>
<tr>
<td>in int <strong>VERTEX_ID</strong></td>
<td>The index of the current vertex in the vertex buffer.</td>
</tr>
<tr>
<td>inout vec2 <strong>UV</strong></td>
<td>Normalized texture coordinates. Range from <code>0.0</code> to
<code>1.0</code>.</td>
</tr>
<tr>
<td>inout vec4 <strong>COLOR</strong></td>
<td>Color from vertex primitive.</td>
</tr>
<tr>
<td>inout float <strong>POINT_SIZE</strong></td>
<td>Point size for point drawing.</td>
</tr>
<tr>
<td>in vec4 <strong>CUSTOM0</strong></td>
<td>Custom value from vertex primitive.</td>
</tr>
<tr>
<td>in vec4 <strong>CUSTOM1</strong></td>
<td>Custom value from vertex primitive.</td>
</tr>
</tbody>
</table>

## Fragment built-ins

Certain Nodes (for example, `Sprite2Ds <class_Sprite2D>`) display a
texture by default. However, when a custom `fragment()` function is
attached to these nodes, the texture lookup needs to be done manually.
Godot provides the texture color in the `COLOR` built-in variable
multiplied by the node's color. To read the texture color by itself, you
can use:

    COLOR = texture(TEXTURE, UV);

Similarly, if a normal map is used in the
`CanvasTexture <class_CanvasTexture>`, Godot uses it by default and
assigns its value to the built-in `NORMAL` variable. If you are using a
normal map meant for use in 3D, it will appear inverted. In order to use
it in your shader, you must assign it to the `NORMAL_MAP` property.
Godot will handle converting it for use in 2D and overwriting `NORMAL`.

    NORMAL_MAP = texture(NORMAL_TEXTURE, UV).rgb;

<table>
<colgroup>
<col style="width: 41%" />
<col style="width: 58%" />
</colgroup>
<thead>
<tr>
<th>Built-in</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>in vec4 <strong>FRAGCOORD</strong></td>
<td>Coordinate of pixel center. In screen space. <code>xy</code>
specifies position in viewport. Upper-left of the viewport is the
origin, <code>(0.0, 0.0)</code>.</td>
</tr>
<tr>
<td>in vec2 <strong>SCREEN_PIXEL_SIZE</strong></td>
<td>Size of individual pixels. Equal to inverse of resolution.</td>
</tr>
<tr>
<td>in vec2 <strong>POINT_COORD</strong></td>
<td>Coordinate for drawing points.</td>
</tr>
<tr>
<td>sampler2D <strong>TEXTURE</strong></td>
<td>Default 2D texture.</td>
</tr>
<tr>
<td>in vec2 <strong>TEXTURE_PIXEL_SIZE</strong></td>
<td>Normalized pixel size of default 2D texture. For a Sprite2D with a
texture of size 64x32px, <strong>TEXTURE_PIXEL_SIZE</strong> =
<code>vec2(1/64, 1/32)</code></td>
</tr>
<tr>
<td>in bool <strong>AT_LIGHT_PASS</strong></td>
<td>Always <code>false</code>.</td>
</tr>
<tr>
<td>sampler2D <strong>SPECULAR_SHININESS_TEXTURE</strong></td>
<td>Specular shininess texture of this object.</td>
</tr>
<tr>
<td>in vec4 <strong>SPECULAR_SHININESS</strong></td>
<td>Specular shininess color, as sampled from the texture.</td>
</tr>
<tr>
<td>in vec2 <strong>UV</strong></td>
<td>UV from the <code>vertex()</code> function.</td>
</tr>
<tr>
<td>in vec2 <strong>SCREEN_UV</strong></td>
<td>Screen UV coordinate for current pixel.</td>
</tr>
<tr>
<td>sampler2D <strong>SCREEN_TEXTURE</strong></td>
<td>Removed in Godot 4. Use a <code>sampler2D</code> with
<code>hint_screen_texture</code> instead.</td>
</tr>
<tr>
<td>inout vec3 <strong>NORMAL</strong></td>
<td>Normal read from <code>NORMAL_TEXTURE</code>. Writable.</td>
</tr>
<tr>
<td>sampler2D <strong>NORMAL_TEXTURE</strong></td>
<td>Default 2D normal texture.</td>
</tr>
<tr>
<td>out vec3 <strong>NORMAL_MAP</strong></td>
<td>Configures normal maps meant for 3D for use in 2D. If used,
overrides <code>NORMAL</code>.</td>
</tr>
<tr>
<td>out float <strong>NORMAL_MAP_DEPTH</strong></td>
<td>Normal map depth for scaling.</td>
</tr>
<tr>
<td>inout vec2 <strong>VERTEX</strong></td>
<td>Pixel position in screen space.</td>
</tr>
<tr>
<td>inout vec2 <strong>SHADOW_VERTEX</strong></td>
<td>Same as <code>VERTEX</code> but can be written to alter
shadows.</td>
</tr>
<tr>
<td>inout vec3 <strong>LIGHT_VERTEX</strong></td>
<td>Same as <code>VERTEX</code> but can be written to alter lighting. Z
component represents height.</td>
</tr>
<tr>
<td>inout vec4 <strong>COLOR</strong></td>
<td>Color from the <code>vertex()</code> function multiplied by the
<code>TEXTURE</code> color. Also output color value.</td>
</tr>
</tbody>
</table>

## Light built-ins

Light processor functions work differently in Godot 4.x than they did in
Godot 3.x. In Godot 4.x all lighting is done during the regular draw
pass. In other words, Godot no longer draws the object again for each
light.

Use the `unshaded` render mode if you do not want the `light()` function
to run. Use the `light_only` render mode if you only want to see the
impact of lighting on an object; this can be useful when you only want
the object visible where it is covered by light.

If you define a `light()` function it will replace the built in light
function, even if your light function is empty.

Below is an example of a light shader that takes a CanvasItem's normal
map into account:

    void light() {
      float cNdotL = max(0.0, dot(NORMAL, LIGHT_DIRECTION));
      LIGHT = vec4(LIGHT_COLOR.rgb * COLOR.rgb * LIGHT_ENERGY * cNdotL, LIGHT_COLOR.a);
    }

<table>
<colgroup>
<col style="width: 30%" />
<col style="width: 69%" />
</colgroup>
<thead>
<tr>
<th>Built-in</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>in vec4 <strong>FRAGCOORD</strong></td>
<td>Coordinate of pixel center. In screen space. <code>xy</code>
specifies position in viewport. Upper-left of the viewport is the
origin, <code>(0.0, 0.0)</code>.</td>
</tr>
<tr>
<td>in vec3 <strong>NORMAL</strong></td>
<td>Input normal.</td>
</tr>
<tr>
<td>in vec4 <strong>COLOR</strong></td>
<td>Input color. This is the output of the <code>fragment()</code>
function.</td>
</tr>
<tr>
<td>in vec2 <strong>UV</strong></td>
<td>UV from the <code>vertex()</code> function, equivalent to the UV in
the <code>fragment()</code> function.</td>
</tr>
<tr>
<td>sampler2D <strong>TEXTURE</strong></td>
<td>Current texture in use for CanvasItem.</td>
</tr>
<tr>
<td>in vec2 <strong>TEXTURE_PIXEL_SIZE</strong></td>
<td>Normalized pixel size of <code>TEXTURE</code>. For a Sprite2D with a
<code>TEXTURE</code> of size <code>64x32</code> pixels,
<strong>TEXTURE_PIXEL_SIZE</strong> = <code>vec2(1/64, 1/32)</code></td>
</tr>
<tr>
<td>in vec2 <strong>SCREEN_UV</strong></td>
<td>Screen UV coordinate for current pixel.</td>
</tr>
<tr>
<td>in vec2 <strong>POINT_COORD</strong></td>
<td>UV for Point Sprite.</td>
</tr>
<tr>
<td>in vec4 <strong>LIGHT_COLOR</strong></td>
<td><code class="interpreted-text"
role="ref">Color&lt;class_Light2D_property_color&gt;</code> of the <code
class="interpreted-text" role="ref">class_Light2D</code>. If the light
is a <code class="interpreted-text"
role="ref">class_PointLight2D</code>, multiplied by the light's <code
class="interpreted-text"
role="ref">texture&lt;class_PointLight2D_property_texture&gt;</code>.</td>
</tr>
<tr>
<td>in float <strong>LIGHT_ENERGY</strong></td>
<td><code class="interpreted-text"
role="ref">Energy multiplier&lt;class_Light2D_property_energy&gt;</code>
of the <code class="interpreted-text"
role="ref">class_Light2D</code>.</td>
</tr>
<tr>
<td>in vec3 <strong>LIGHT_POSITION</strong></td>
<td>Position of the <code class="interpreted-text"
role="ref">class_Light2D</code> in screen space. If using a <code
class="interpreted-text" role="ref">class_DirectionalLight2D</code> this
is always <code>(0.0, 0.0, 0.0)</code>.</td>
</tr>
<tr>
<td>in vec3 <strong>LIGHT_DIRECTION</strong></td>
<td>Direction of the <code class="interpreted-text"
role="ref">class_Light2D</code> in screen space.</td>
</tr>
<tr>
<td>in bool <strong>LIGHT_IS_DIRECTIONAL</strong></td>
<td><code>true</code> if this pass is a <code class="interpreted-text"
role="ref">class_DirectionalLight2D</code>.</td>
</tr>
<tr>
<td>in vec3 <strong>LIGHT_VERTEX</strong></td>
<td>Pixel position, in screen space as modified in the
<code>fragment()</code> function.</td>
</tr>
<tr>
<td>inout vec4 <strong>LIGHT</strong></td>
<td>Output color for this <code class="interpreted-text"
role="ref">class_Light2D</code>.</td>
</tr>
<tr>
<td>in vec4 <strong>SPECULAR_SHININESS</strong></td>
<td>Specular shininess, as set in the object's texture.</td>
</tr>
<tr>
<td>out vec4 <strong>SHADOW_MODULATE</strong></td>
<td>Multiply shadows cast at this point by this color.</td>
</tr>
</tbody>
</table>

## SDF functions

There are a few additional functions implemented to sample an
automatically generated Signed Distance Field texture. These functions
available for the `fragment()` and `light()` functions of CanvasItem
shaders.

The signed distance field is generated from `class_LightOccluder2D`
nodes present in the scene with the **SDF Collision** property enabled
(which is the default). See the
`2D lights and shadows <doc_2d_lights_and_shadows_setting_up_shadows>`
documentation for more information.

<table>
<colgroup>
<col style="width: 52%" />
<col style="width: 47%" />
</colgroup>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>float <strong>texture_sdf</strong> (vec2 sdf_pos)</td>
<td>Performs an SDF texture lookup.</td>
</tr>
<tr>
<td>vec2 <strong>texture_sdf_normal</strong> (vec2 sdf_pos)</td>
<td>Calculates a normal from the SDF texture.</td>
</tr>
<tr>
<td>vec2 <strong>sdf_to_screen_uv</strong> (vec2 sdf_pos)</td>
<td>Converts an SDF to screen UV.</td>
</tr>
<tr>
<td>vec2 <strong>screen_uv_to_sdf</strong> (vec2 uv)</td>
<td>Converts screen UV to an SDF.</td>
</tr>
</tbody>
</table>
