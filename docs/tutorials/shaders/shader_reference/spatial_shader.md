# Spatial shaders

Spatial shaders are used for shading 3D objects. They are the most
complex type of shader Godot offers. Spatial shaders are highly
configurable with different render modes and different rendering options
(e.g. Subsurface Scattering, Transmission, Ambient Occlusion, Rim
lighting etc). Users can optionally write vertex, fragment, and light
processor functions to affect how objects are drawn.

## Render modes

For visual examples of these render modes, see
`Standard Material 3D and ORM Material 3D<doc_standard_material_3d>`.

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 76%" />
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
<td><strong>depth_draw_opaque</strong></td>
<td>Only draw depth for opaque geometry (not transparent).</td>
</tr>
<tr>
<td><strong>depth_draw_always</strong></td>
<td>Always draw depth (opaque and transparent).</td>
</tr>
<tr>
<td><strong>depth_draw_never</strong></td>
<td>Never draw depth.</td>
</tr>
<tr>
<td><strong>depth_prepass_alpha</strong></td>
<td>Do opaque depth pre-pass for transparent geometry.</td>
</tr>
<tr>
<td><strong>depth_test_disabled</strong></td>
<td>Disable depth testing.</td>
</tr>
<tr>
<td><strong>sss_mode_skin</strong></td>
<td>Subsurface Scattering mode for skin.</td>
</tr>
<tr>
<td><strong>cull_back</strong></td>
<td>Cull back-faces (default).</td>
</tr>
<tr>
<td><strong>cull_front</strong></td>
<td>Cull front-faces.</td>
</tr>
<tr>
<td><strong>cull_disabled</strong></td>
<td>Culling disabled (double sided).</td>
</tr>
<tr>
<td><strong>unshaded</strong></td>
<td>Result is just albedo. No lighting/shading happens in material.</td>
</tr>
<tr>
<td><strong>wireframe</strong></td>
<td>Geometry draws using lines.</td>
</tr>
<tr>
<td><strong>diffuse_burley</strong></td>
<td>Burley (Disney PBS) for diffuse (default).</td>
</tr>
<tr>
<td><strong>diffuse_lambert</strong></td>
<td>Lambert shading for diffuse.</td>
</tr>
<tr>
<td><strong>diffuse_lambert_wrap</strong></td>
<td>Lambert wrapping (roughness dependent) for diffuse.</td>
</tr>
<tr>
<td><strong>diffuse_toon</strong></td>
<td>Toon shading for diffuse.</td>
</tr>
<tr>
<td><strong>specular_schlick_ggx</strong></td>
<td>Schlick-GGX for specular (default).</td>
</tr>
<tr>
<td><strong>specular_toon</strong></td>
<td>Toon for specular.</td>
</tr>
<tr>
<td><strong>specular_disabled</strong></td>
<td>Disable specular.</td>
</tr>
<tr>
<td><strong>skip_vertex_transform</strong></td>
<td><code>VERTEX</code>/<code>NORMAL</code>/etc. need to be transformed
manually in the <code>vertex()</code> function.</td>
</tr>
<tr>
<td><strong>world_vertex_coords</strong></td>
<td><code>VERTEX</code>/<code>NORMAL</code>/etc. are modified in world
space instead of model space.</td>
</tr>
<tr>
<td><strong>ensure_correct_normals</strong></td>
<td>Use when non-uniform scale is applied to mesh.</td>
</tr>
<tr>
<td><strong>shadows_disabled</strong></td>
<td>Disable computing shadows in shader.</td>
</tr>
<tr>
<td><strong>ambient_light_disabled</strong></td>
<td>Disable contribution from ambient light and radiance map.</td>
</tr>
<tr>
<td><strong>shadow_to_opacity</strong></td>
<td>Lighting modifies the alpha so shadowed areas are opaque and
non-shadowed areas are transparent. Useful for overlaying shadows onto a
camera feed in AR.</td>
</tr>
<tr>
<td><strong>vertex_lighting</strong></td>
<td>Use vertex-based lighting.</td>
</tr>
<tr>
<td><strong>particle_trails</strong></td>
<td>Enables the trails when used on particles geometry.</td>
</tr>
<tr>
<td><strong>alpha_to_coverage</strong></td>
<td>Alpha antialiasing mode, see <a
href="https://github.com/godotengine/godot/pull/40364">here</a> for
more.</td>
</tr>
<tr>
<td><strong>alpha_to_coverage_and_one</strong></td>
<td>Alpha antialiasing mode, see <a
href="https://github.com/godotengine/godot/pull/40364">here</a> for
more.</td>
</tr>
<tr>
<td><strong>fog_disabled</strong></td>
<td>Disable receiving depth-based or volumetric fog. Useful for
blend_add materials like particles.</td>
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

Vertex data (`VERTEX`, `NORMAL`, `TANGENT`, `BITANGENT`) are presented
in model space (also called local space). If not written to, these
values will not be modified and be passed through as they came.

They can optionally be presented in world space by using the
`world_vertex_coords` render mode.

Users can disable the built-in modelview transform (projection will
still happen later) and do it manually with the following code:

    shader_type spatial;
    render_mode skip_vertex_transform;

    void vertex() {
        VERTEX = (MODELVIEW_MATRIX * vec4(VERTEX, 1.0)).xyz;
        NORMAL = normalize((MODELVIEW_MATRIX * vec4(NORMAL, 0.0)).xyz);
        BINORMAL = normalize((MODELVIEW_MATRIX * vec4(BINORMAL, 0.0)).xyz);
        TANGENT = normalize((MODELVIEW_MATRIX * vec4(TANGENT, 0.0)).xyz);
    }

Other built-ins, such as `UV`, `UV2`, and `COLOR`, are also passed
through to the `fragment()` function if not modified.

Users can override the modelview and projection transforms using the
`POSITION` built-in. If `POSITION` is written to anywhere in the shader,
it will always be used, so the user becomes responsible for ensuring
that it always has an acceptable value. When `POSITION` is used, the
value from `VERTEX` is ignored and projection does not happen. However,
the value passed to the fragment shader still comes from `VERTEX`.

For instancing, the `INSTANCE_CUSTOM` variable contains the instance
custom data. When using particles, this information is usually:

-   **x**: Rotation angle in radians.
-   **y**: Phase during lifetime (`0.0` to `1.0`).
-   **z**: Animation frame.

This allows you to easily adjust the shader to a particle system using
default particles material. When writing a custom particle shader, this
value can be used as desired.

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
<td>in vec2 <strong>VIEWPORT_SIZE</strong></td>
<td>Size of viewport (in pixels).</td>
</tr>
<tr>
<td>in mat4 <strong>VIEW_MATRIX</strong></td>
<td>World space to view space transform.</td>
</tr>
<tr>
<td>in mat4 <strong>INV_VIEW_MATRIX</strong></td>
<td>View space to world space transform.</td>
</tr>
<tr>
<td>in mat4 <strong>MAIN_CAM_INV_VIEW_MATRIX</strong></td>
<td>View space to world space transform of camera used to draw the
current viewport.</td>
</tr>
<tr>
<td>in mat4 <strong>INV_PROJECTION_MATRIX</strong></td>
<td>Clip space to view space transform.</td>
</tr>
<tr>
<td>in vec3 <strong>NODE_POSITION_WORLD</strong></td>
<td>Node position, in world space.</td>
</tr>
<tr>
<td>in vec3 <strong>NODE_POSITION_VIEW</strong></td>
<td>Node position, in view space.</td>
</tr>
<tr>
<td>in vec3 <strong>CAMERA_POSITION_WORLD</strong></td>
<td>Camera position, in world space.</td>
</tr>
<tr>
<td>in vec3 <strong>CAMERA_DIRECTION_WORLD</strong></td>
<td>Camera direction, in world space.</td>
</tr>
<tr>
<td>in uint <strong>CAMERA_VISIBLE_LAYERS</strong></td>
<td>Cull layers of the camera rendering the current pass.</td>
</tr>
<tr>
<td>in bool <strong>OUTPUT_IS_SRGB</strong></td>
<td><code>true</code> when output is in sRGB color space (this is
<code>true</code> in the Compatibility renderer, <code>false</code> in
Forward+ and Forward Mobile).</td>
</tr>
<tr>
<td>in int <strong>INSTANCE_ID</strong></td>
<td>Instance ID for instancing.</td>
</tr>
<tr>
<td>in vec4 <strong>INSTANCE_CUSTOM</strong></td>
<td>Instance custom data (for particles, mostly).</td>
</tr>
<tr>
<td>in int <strong>VIEW_INDEX</strong></td>
<td>The view that we are rendering. <code>VIEW_MONO_LEFT</code>
(<code>0</code>) for Mono (not multiview) or left eye,
<code>VIEW_RIGHT</code> (<code>1</code>) for right eye.</td>
</tr>
<tr>
<td>in int <strong>VIEW_MONO_LEFT</strong></td>
<td>Constant for Mono or left eye, always <code>0</code>.</td>
</tr>
<tr>
<td>in int <strong>VIEW_RIGHT</strong></td>
<td>Constant for right eye, always <code>1</code>.</td>
</tr>
<tr>
<td>in vec3 <strong>EYE_OFFSET</strong></td>
<td>Position offset for the eye being rendered. Only applicable for
multiview rendering.</td>
</tr>
<tr>
<td>inout vec3 <strong>VERTEX</strong></td>
<td>Vertex position in model space.</td>
</tr>
<tr>
<td>in int <strong>VERTEX_ID</strong></td>
<td>The index of the current vertex in the vertex buffer.</td>
</tr>
<tr>
<td>inout vec3 <strong>NORMAL</strong></td>
<td>Normal in model space.</td>
</tr>
<tr>
<td>inout vec3 <strong>TANGENT</strong></td>
<td>Tangent in model space.</td>
</tr>
<tr>
<td>inout vec3 <strong>BINORMAL</strong></td>
<td>Binormal in model space.</td>
</tr>
<tr>
<td>out vec4 <strong>POSITION</strong></td>
<td>If written to, overrides final vertex position.</td>
</tr>
<tr>
<td>inout vec2 <strong>UV</strong></td>
<td>UV main channel.</td>
</tr>
<tr>
<td>inout vec2 <strong>UV2</strong></td>
<td>UV secondary channel.</td>
</tr>
<tr>
<td>inout vec4 <strong>COLOR</strong></td>
<td>Color from vertices.</td>
</tr>
<tr>
<td>out float <strong>ROUGHNESS</strong></td>
<td>Roughness for vertex lighting.</td>
</tr>
<tr>
<td>inout float <strong>POINT_SIZE</strong></td>
<td>Point size for point rendering.</td>
</tr>
<tr>
<td>inout mat4 <strong>MODELVIEW_MATRIX</strong></td>
<td>Model/local space to view space transform (use if possible).</td>
</tr>
<tr>
<td>inout mat3 <strong>MODELVIEW_NORMAL_MATRIX</strong></td>
<td></td>
</tr>
<tr>
<td>in mat4 <strong>MODEL_MATRIX</strong></td>
<td>Model/local space to world space transform.</td>
</tr>
<tr>
<td>in mat3 <strong>MODEL_NORMAL_MATRIX</strong></td>
<td></td>
</tr>
<tr>
<td>inout mat4 <strong>PROJECTION_MATRIX</strong></td>
<td>View space to clip space transform.</td>
</tr>
<tr>
<td>in uvec4 <strong>BONE_INDICES</strong></td>
<td></td>
</tr>
<tr>
<td>in vec4 <strong>BONE_WEIGHTS</strong></td>
<td></td>
</tr>
<tr>
<td>in vec4 <strong>CUSTOM0</strong></td>
<td>Custom value from vertex primitive. When using extra UVs,
<code>xy</code> is UV3 and <code>zw</code> is UV4.</td>
</tr>
<tr>
<td>in vec4 <strong>CUSTOM1</strong></td>
<td>Custom value from vertex primitive. When using extra UVs,
<code>xy</code> is UV5 and <code>zw</code> is UV6.</td>
</tr>
<tr>
<td>in vec4 <strong>CUSTOM2</strong></td>
<td>Custom value from vertex primitive. When using extra UVs,
<code>xy</code> is UV7 and <code>zw</code> is UV8.</td>
</tr>
<tr>
<td>in vec4 <strong>CUSTOM3</strong></td>
<td>Custom value from vertex primitive.</td>
</tr>
</tbody>
</table>

Note

`MODELVIEW_MATRIX` combines both the `MODEL_MATRIX` and `VIEW_MATRIX`
and is better suited when floating point issues may arise. For example,
if the object is very far away from the world origin, you may run into
floating point issues when using the separated `MODEL_MATRIX` and
`VIEW_MATRIX`.

Note

`INV_VIEW_MATRIX` is the matrix used for rendering the object in that
pass, unlike `MAIN_CAM_INV_VIEW_MATRIX`, which is the matrix of the
camera in the scene. In the shadow pass, `INV_VIEW_MATRIX`'s view is
based on the camera that is located at the position of the light.

## Fragment built-ins

The default use of a Godot fragment processor function is to set up the
material properties of your object and to let the built-in renderer
handle the final shading. However, you are not required to use all these
properties, and if you don't write to them, Godot will optimize away the
corresponding functionality.

<table>
<colgroup>
<col style="width: 29%" />
<col style="width: 70%" />
</colgroup>
<thead>
<tr>
<th>Built-in</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>in vec2 <strong>VIEWPORT_SIZE</strong></td>
<td>Size of viewport (in pixels).</td>
</tr>
<tr>
<td>in vec4 <strong>FRAGCOORD</strong></td>
<td>Coordinate of pixel center in screen space. <code>xy</code>
specifies position in window, <code>z</code> specifies fragment depth if
<code>DEPTH</code> is not used. Origin is lower-left.</td>
</tr>
<tr>
<td>in bool <strong>FRONT_FACING</strong></td>
<td><code>true</code> if current face is front facing.</td>
</tr>
<tr>
<td>in vec3 <strong>VIEW</strong></td>
<td>Normalized vector from fragment position to camera (in view space).
This is the same for both perspective and orthogonal cameras.</td>
</tr>
<tr>
<td>in vec2 <strong>UV</strong></td>
<td>UV that comes from the <code>vertex()</code> function.</td>
</tr>
<tr>
<td>in vec2 <strong>UV2</strong></td>
<td>UV2 that comes from the <code>vertex()</code> function.</td>
</tr>
<tr>
<td>in vec4 <strong>COLOR</strong></td>
<td>COLOR that comes from the <code>vertex()</code> function.</td>
</tr>
<tr>
<td>in vec2 <strong>POINT_COORD</strong></td>
<td>Point coordinate for drawing points with
<code>POINT_SIZE</code>.</td>
</tr>
<tr>
<td>in bool <strong>OUTPUT_IS_SRGB</strong></td>
<td><code>true</code> when output is in sRGB color space (this is
<code>true</code> in the Compatibility renderer, <code>false</code> in
Forward+ and Forward Mobile).</td>
</tr>
<tr>
<td>in mat4 <strong>MODEL_MATRIX</strong></td>
<td>Model/local space to world space transform.</td>
</tr>
<tr>
<td>in mat3 <strong>MODEL_NORMAL_MATRIX</strong></td>
<td></td>
</tr>
<tr>
<td>in mat4 <strong>VIEW_MATRIX</strong></td>
<td>World space to view space transform.</td>
</tr>
<tr>
<td>in mat4 <strong>INV_VIEW_MATRIX</strong></td>
<td>View space to world space transform.</td>
</tr>
<tr>
<td>in mat4 <strong>PROJECTION_MATRIX</strong></td>
<td>View space to clip space transform.</td>
</tr>
<tr>
<td>in mat4 <strong>INV_PROJECTION_MATRIX</strong></td>
<td>Clip space to view space transform.</td>
</tr>
<tr>
<td>in vec3 <strong>NODE_POSITION_WORLD</strong></td>
<td>Node position, in world space.</td>
</tr>
<tr>
<td>in vec3 <strong>NODE_POSITION_VIEW</strong></td>
<td>Node position, in view space.</td>
</tr>
<tr>
<td>in vec3 <strong>CAMERA_POSITION_WORLD</strong></td>
<td>Camera position, in world space.</td>
</tr>
<tr>
<td>in vec3 <strong>CAMERA_DIRECTION_WORLD</strong></td>
<td>Camera direction, in world space.</td>
</tr>
<tr>
<td>in uint <strong>CAMERA_VISIBLE_LAYERS</strong></td>
<td>Cull layers of the camera rendering the current pass.</td>
</tr>
<tr>
<td>in vec3 <strong>VERTEX</strong></td>
<td>Vertex position that comes from the <code>vertex()</code> function
(default, in view space).</td>
</tr>
<tr>
<td>inout vec3 <strong>LIGHT_VERTEX</strong></td>
<td>A writable version of <code>VERTEX</code> that can be used to alter
light and shadows. Writing to this will not change the position of the
fragment.</td>
</tr>
<tr>
<td>in int <strong>VIEW_INDEX</strong></td>
<td>The view that we are rendering. <code>VIEW_MONO_LEFT</code>
(<code>0</code>) for Mono (not multiview) or left eye,
<code>VIEW_RIGHT</code> (<code>1</code>) for right eye.</td>
</tr>
<tr>
<td>in int <strong>VIEW_MONO_LEFT</strong></td>
<td>Constant for Mono or left eye, always <code>0</code>.</td>
</tr>
<tr>
<td>in int <strong>VIEW_RIGHT</strong></td>
<td>Constant for right eye, always <code>1</code>.</td>
</tr>
<tr>
<td>in vec3 <strong>EYE_OFFSET</strong></td>
<td>Position offset for the eye being rendered. Only applicable for
multiview rendering.</td>
</tr>
<tr>
<td>sampler2D <strong>SCREEN_TEXTURE</strong></td>
<td>Removed in Godot 4. Use a <code>sampler2D</code> with
<code>hint_screen_texture</code> instead.</td>
</tr>
<tr>
<td>in vec2 <strong>SCREEN_UV</strong></td>
<td>Screen UV coordinate for current pixel.</td>
</tr>
<tr>
<td>sampler2D <strong>DEPTH_TEXTURE</strong></td>
<td>Removed in Godot 4. Use a <code>sampler2D</code> with
<code>hint_depth_texture</code> instead.</td>
</tr>
<tr>
<td>out float <strong>DEPTH</strong></td>
<td>Custom depth value (range of <code>[0.0, 1.0]</code>). If
<code>DEPTH</code> is being written to in any shader branch, then you
are responsible for setting the <code>DEPTH</code> for
<strong>all</strong> other branches. Otherwise, the graphics API will
leave them uninitialized.</td>
</tr>
<tr>
<td>inout vec3 <strong>NORMAL</strong></td>
<td>Normal that comes from the <code>vertex()</code> function (default,
in view space).</td>
</tr>
<tr>
<td>inout vec3 <strong>TANGENT</strong></td>
<td>Tangent that comes from the <code>vertex()</code> function (default,
in view space).</td>
</tr>
<tr>
<td>inout vec3 <strong>BINORMAL</strong></td>
<td>Binormal that comes from the <code>vertex()</code> function
(default, in view space).</td>
</tr>
<tr>
<td>out vec3 <strong>NORMAL_MAP</strong></td>
<td>Set normal here if reading normal from a texture instead of
<code>NORMAL</code>.</td>
</tr>
<tr>
<td>out float <strong>NORMAL_MAP_DEPTH</strong></td>
<td>Depth from <code>NORMAL_MAP</code>. Defaults to
<code>1.0</code>.</td>
</tr>
<tr>
<td>out vec3 <strong>ALBEDO</strong></td>
<td>Albedo (default white). Base color.</td>
</tr>
<tr>
<td>out float <strong>ALPHA</strong></td>
<td>Alpha (range of <code>[0.0, 1.0]</code>). If read from or written
to, the material will go to the transparent pipeline.</td>
</tr>
<tr>
<td>out float <strong>ALPHA_SCISSOR_THRESHOLD</strong></td>
<td>If written to, values below a certain amount of alpha are
discarded.</td>
</tr>
<tr>
<td>out float <strong>ALPHA_HASH_SCALE</strong></td>
<td></td>
</tr>
<tr>
<td>out float <strong>ALPHA_ANTIALIASING_EDGE</strong></td>
<td></td>
</tr>
<tr>
<td>out vec2 <strong>ALPHA_TEXTURE_COORDINATE</strong></td>
<td></td>
</tr>
<tr>
<td>out float <strong>METALLIC</strong></td>
<td>Metallic (range of <code>[0.0, 1.0]</code>).</td>
</tr>
<tr>
<td>out float <strong>SPECULAR</strong></td>
<td>Specular. Defaults to <code>0.5</code>, best not to modify unless
you want to change IOR.</td>
</tr>
<tr>
<td>out float <strong>ROUGHNESS</strong></td>
<td>Roughness (range of <code>[0.0, 1.0]</code>).</td>
</tr>
<tr>
<td>out float <strong>RIM</strong></td>
<td>Rim (range of <code>[0.0, 1.0]</code>). If used, Godot calculates
rim lighting.</td>
</tr>
<tr>
<td>out float <strong>RIM_TINT</strong></td>
<td>Rim Tint, range of <code>0.0</code> (white) to <code>1.0</code>
(albedo). If used, Godot calculates rim lighting.</td>
</tr>
<tr>
<td>out float <strong>CLEARCOAT</strong></td>
<td>Small added specular blob. If used, Godot calculates Clearcoat.</td>
</tr>
<tr>
<td>out float <strong>CLEARCOAT_GLOSS</strong></td>
<td>Gloss of Clearcoat. If used, Godot calculates Clearcoat.</td>
</tr>
<tr>
<td>out float <strong>ANISOTROPY</strong></td>
<td>For distorting the specular blob according to tangent space.</td>
</tr>
<tr>
<td>out vec2 <strong>ANISOTROPY_FLOW</strong></td>
<td>Distortion direction, use with flowmaps.</td>
</tr>
<tr>
<td>out float <strong>SSS_STRENGTH</strong></td>
<td>Strength of Subsurface Scattering. If used, Subsurface Scattering
will be applied to object.</td>
</tr>
<tr>
<td>out vec4 <strong>SSS_TRANSMITTANCE_COLOR</strong></td>
<td></td>
</tr>
<tr>
<td>out float <strong>SSS_TRANSMITTANCE_DEPTH</strong></td>
<td></td>
</tr>
<tr>
<td>out float <strong>SSS_TRANSMITTANCE_BOOST</strong></td>
<td></td>
</tr>
<tr>
<td>inout vec3 <strong>BACKLIGHT</strong></td>
<td></td>
</tr>
<tr>
<td>out float <strong>AO</strong></td>
<td>Strength of Ambient Occlusion. For use with pre-baked AO.</td>
</tr>
<tr>
<td>out float <strong>AO_LIGHT_AFFECT</strong></td>
<td>How much AO affects lights (range of <code>[0.0, 1.0]</code>,
default <code>0.0</code>).</td>
</tr>
<tr>
<td>out vec3 <strong>EMISSION</strong></td>
<td>Emission color (can go over <code>(1.0, 1.0, 1.0)</code> for
HDR).</td>
</tr>
<tr>
<td>out vec4 <strong>FOG</strong></td>
<td>If written to, blends final pixel color with <code>FOG.rgb</code>
based on <code>FOG.a</code>.</td>
</tr>
<tr>
<td>out vec4 <strong>RADIANCE</strong></td>
<td>If written to, blends environment map radiance with
<code>RADIANCE.rgb</code> based on <code>RADIANCE.a</code>.</td>
</tr>
<tr>
<td>out vec4 <strong>IRRADIANCE</strong></td>
<td>If written to, blends environment map irradiance with
<code>IRRADIANCE.rgb</code> based on <code>IRRADIANCE.a</code>.</td>
</tr>
</tbody>
</table>

Note

Shaders going through the transparent pipeline when `ALPHA` is written
to may exhibit transparency sorting issues. Read the
`transparency sorting section in the 3D rendering limitations page <doc_3d_rendering_limitations_transparency_sorting>`
for more information and ways to avoid issues.

## Light built-ins

Writing light processor functions is completely optional. You can skip
the `light()` function by using the `unshaded` render mode. If no light
function is written, Godot will use the material properties written to
in the `fragment()` function to calculate the lighting for you (subject
to the render mode).

The `light()` function is called for every light in every pixel. It is
called within a loop for each light type.

Below is an example of a custom `light()` function using a Lambertian
lighting model:

    void light() {
        DIFFUSE_LIGHT += clamp(dot(NORMAL, LIGHT), 0.0, 1.0) * ATTENUATION * LIGHT_COLOR;
    }

If you want the lights to add together, add the light contribution to
`DIFFUSE_LIGHT` using `+=`, rather than overwriting it.

Warning

The `light()` function won't be run if the `vertex_lighting` render mode
is enabled, or if
`Rendering > Quality > Shading > Force Vertex Shading<class_ProjectSettings_property_rendering/shading/overrides/force_vertex_shading>`
is enabled in the Project Settings. (It's enabled by default on mobile
platforms.)

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 66%" />
</colgroup>
<thead>
<tr>
<th>Built-in</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>in vec2 <strong>VIEWPORT_SIZE</strong></td>
<td>Size of viewport (in pixels).</td>
</tr>
<tr>
<td>in vec4 <strong>FRAGCOORD</strong></td>
<td>Coordinate of pixel center in screen space. <code>xy</code>
specifies position in window, <code>z</code> specifies fragment depth if
<code>DEPTH</code> is not used. Origin is lower-left.</td>
</tr>
<tr>
<td>in mat4 <strong>MODEL_MATRIX</strong></td>
<td>Model/local space to world space transform.</td>
</tr>
<tr>
<td>in mat4 <strong>INV_VIEW_MATRIX</strong></td>
<td>View space to world space transform.</td>
</tr>
<tr>
<td>in mat4 <strong>VIEW_MATRIX</strong></td>
<td>World space to view space transform.</td>
</tr>
<tr>
<td>in mat4 <strong>PROJECTION_MATRIX</strong></td>
<td>View space to clip space transform.</td>
</tr>
<tr>
<td>in mat4 <strong>INV_PROJECTION_MATRIX</strong></td>
<td>Clip space to view space transform.</td>
</tr>
<tr>
<td>in vec3 <strong>NORMAL</strong></td>
<td>Normal vector, in view space.</td>
</tr>
<tr>
<td>in vec2 <strong>UV</strong></td>
<td>UV that comes from the <code>vertex()</code> function.</td>
</tr>
<tr>
<td>in vec2 <strong>UV2</strong></td>
<td>UV2 that comes from the <code>vertex()</code> function.</td>
</tr>
<tr>
<td>in vec3 <strong>VIEW</strong></td>
<td>View vector, in view space.</td>
</tr>
<tr>
<td>in vec3 <strong>LIGHT</strong></td>
<td>Light vector, in view space.</td>
</tr>
<tr>
<td>in vec3 <strong>LIGHT_COLOR</strong></td>
<td><code class="interpreted-text"
role="ref">Light color&lt;class_Light3D_property_light_color&gt;</code>
multiplied by <code class="interpreted-text"
role="ref">light energy&lt;class_Light3D_property_light_energy&gt;</code>
multiplied by <code>PI</code>. The <code>PI</code> multiplication is
present because physically-based lighting models include a division by
<code>PI</code>.</td>
</tr>
<tr>
<td>in float <strong>SPECULAR_AMOUNT</strong></td>
<td>For <code class="interpreted-text"
role="ref">class_OmniLight3D</code> and <code class="interpreted-text"
role="ref">class_SpotLight3D</code>, <code>2.0</code> multiplied by
<code class="interpreted-text"
role="ref">light_specular&lt;class_Light3D_property_light_specular&gt;</code>.
For <code class="interpreted-text"
role="ref">class_DirectionalLight3D</code>, <code>1.0</code>.</td>
</tr>
<tr>
<td>in bool <strong>LIGHT_IS_DIRECTIONAL</strong></td>
<td><code>true</code> if this pass is a <code class="interpreted-text"
role="ref">class_DirectionalLight3D</code>.</td>
</tr>
<tr>
<td>in float <strong>ATTENUATION</strong></td>
<td>Attenuation based on distance or shadow.</td>
</tr>
<tr>
<td>in vec3 <strong>ALBEDO</strong></td>
<td>Base albedo.</td>
</tr>
<tr>
<td>in vec3 <strong>BACKLIGHT</strong></td>
<td></td>
</tr>
<tr>
<td>in float <strong>METALLIC</strong></td>
<td>Metallic.</td>
</tr>
<tr>
<td>in float <strong>ROUGHNESS</strong></td>
<td>Roughness.</td>
</tr>
<tr>
<td>in bool <strong>OUTPUT_IS_SRGB</strong></td>
<td><code>true</code> when output is in sRGB color space. This is
<code>true</code> in the Compatibility renderer, <code>false</code> in
Forward+ and Forward Mobile.</td>
</tr>
<tr>
<td>out vec3 <strong>DIFFUSE_LIGHT</strong></td>
<td>Diffuse light result.</td>
</tr>
<tr>
<td>out vec3 <strong>SPECULAR_LIGHT</strong></td>
<td>Specular light result.</td>
</tr>
<tr>
<td>out float <strong>ALPHA</strong></td>
<td>Alpha (range of <code>[0.0, 1.0]</code>). If written to, the
material will go to the transparent pipeline.</td>
</tr>
</tbody>
</table>

Note

Shaders going through the transparent pipeline when `ALPHA` is written
to may exhibit transparency sorting issues. Read the
`transparency sorting section in the 3D rendering limitations page <doc_3d_rendering_limitations_transparency_sorting>`
for more information and ways to avoid issues.

Transparent materials also cannot cast shadows or appear in
`hint_screen_texture` and `hint_depth_texture` uniforms. This in turn
prevents those materials from appearing in screen-space reflections or
refraction. `SDFGI <doc_using_sdfgi>` sharp reflections are not visible
on transparent materials (only rough reflections are visible on
transparent materials).
