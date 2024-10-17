# Particle shaders

Particle shaders are a special type of shader that runs before the
object is drawn. They are used for calculating material properties such
as color, position, and rotation. They are drawn with any regular
material for CanvasItem or Spatial, depending on whether they are 2D or
3D.

Particle shaders are unique because they are not used to draw the object
itself; they are used to calculate particle properties, which are then
used by a `CanvasItem<doc_canvas_item_shader>` or
`Spatial<doc_spatial_shader>` shader. They contain two processor
functions: `start()` and `process()`.

Unlike other shader types, particle shaders keep the data that was
output the previous frame. Therefore, particle shaders can be used for
complex effects that take place over multiple frames.

Note

Particle shaders are only available with GPU-based particle nodes
(`class_GPUParticles2D` and `class_GPUParticles3D`).

CPU-based particle nodes (`class_CPUParticles2D` and
`class_CPUParticles3D`) are *rendered* on the GPU (which means they can
use custom CanvasItem or Spatial shaders), but their motion is
*simulated* on the CPU.

## Render modes

<table style="width:99%;">
<colgroup>
<col style="width: 37%" />
<col style="width: 61%" />
</colgroup>
<thead>
<tr>
<th>Render mode</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>keep_data</strong></td>
<td>Do not clear previous data on restart.</td>
</tr>
<tr>
<td><strong>disable_force</strong></td>
<td>Disable attractor force.</td>
</tr>
<tr>
<td><strong>disable_velocity</strong></td>
<td>Ignore <code>VELOCITY</code> value.</td>
</tr>
<tr>
<td><strong>collision_use_scale</strong></td>
<td>Scale the particle's size for collisions.</td>
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

## Start and Process built-ins

These properties can be accessed from both the `start()` and `process()`
functions.

<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 78%" />
</colgroup>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>in float <strong>LIFETIME</strong></td>
<td>Particle lifetime.</td>
</tr>
<tr>
<td>in float <strong>DELTA</strong></td>
<td>Delta process time.</td>
</tr>
<tr>
<td>in uint <strong>NUMBER</strong></td>
<td>Unique number since emission start.</td>
</tr>
<tr>
<td>in uint <strong>INDEX</strong></td>
<td>Particle index (from total particles).</td>
</tr>
<tr>
<td>in mat4 <strong>EMISSION_TRANSFORM</strong></td>
<td>Emitter transform (used for non-local systems).</td>
</tr>
<tr>
<td>in uint <strong>RANDOM_SEED</strong></td>
<td>Random seed used as base for random.</td>
</tr>
<tr>
<td>inout bool <strong>ACTIVE</strong></td>
<td><code>true</code> when the particle is active, can be set
<code>false</code>.</td>
</tr>
<tr>
<td>inout vec4 <strong>COLOR</strong></td>
<td>Particle color, can be written to and accessed in mesh's vertex
function.</td>
</tr>
<tr>
<td>inout vec3 <strong>VELOCITY</strong></td>
<td>Particle velocity, can be modified.</td>
</tr>
<tr>
<td>inout mat4 <strong>TRANSFORM</strong></td>
<td>Particle transform.</td>
</tr>
<tr>
<td>inout vec4 <strong>CUSTOM</strong></td>
<td>Custom particle data. Accessible from shader of mesh as
<code>INSTANCE_CUSTOM</code>.</td>
</tr>
<tr>
<td>inout float <strong>MASS</strong></td>
<td>Particle mass, intended to be used with attractors. Equals
<code>1.0</code> by default.</td>
</tr>
<tr>
<td>in vec4 <strong>USERDATAX</strong></td>
<td>Vector that enables the integration of supplementary user-defined
data into the particle process shader. <code>USERDATAX</code> are six
built-ins identified by number, <code>X</code> can be numbers between 1
and 6, for example <code>USERDATA3</code>.</td>
</tr>
<tr>
<td>in uint <strong>FLAG_EMIT_POSITION</strong></td>
<td>A flag for using on the last argument of
<code>emit_subparticle()</code> function to assign a position to a new
particle's transform.</td>
</tr>
<tr>
<td>in uint <strong>FLAG_EMIT_ROT_SCALE</strong></td>
<td>A flag for using on the last argument of
<code>emit_subparticle()</code> function to assign the rotation and
scale to a new particle's transform.</td>
</tr>
<tr>
<td>in uint <strong>FLAG_EMIT_VELOCITY</strong></td>
<td>A flag for using on the last argument of
<code>emit_subparticle()</code> function to assign a velocity to a new
particle.</td>
</tr>
<tr>
<td>in uint <strong>FLAG_EMIT_COLOR</strong></td>
<td>A flag for using on the last argument of
<code>emit_subparticle()</code> function to assign a color to a new
particle.</td>
</tr>
<tr>
<td>in uint <strong>FLAG_EMIT_CUSTOM</strong></td>
<td>A flag for using on the last argument of
<code>emit_subparticle()</code> function to assign a custom data vector
to a new particle.</td>
</tr>
<tr>
<td>in vec3 <strong>EMITTER_VELOCITY</strong></td>
<td>Velocity of the <code class="interpreted-text"
role="ref">Particles2D&lt;class_GPUParticles2D&gt;</code> (<code
class="interpreted-text"
role="ref">3D&lt;class_GPUParticles3D&gt;</code>) node.</td>
</tr>
<tr>
<td>in float <strong>INTERPOLATE_TO_END</strong></td>
<td>Value of <code class="interpreted-text"
role="ref">interp_to_end&lt;class_GPUParticles2D_property_interp_to_end&gt;</code>
(<code class="interpreted-text"
role="ref">3D&lt;class_GPUParticles3D_property_interp_to_end&gt;</code>)
property of Particles node.</td>
</tr>
<tr>
<td>in uint <strong>AMOUNT_RATIO</strong></td>
<td>Value of <code class="interpreted-text"
role="ref">amount_ratio&lt;class_GPUParticles2D_property_amount_ratio&gt;</code>
(<code class="interpreted-text"
role="ref">3D&lt;class_GPUParticles3D_property_amount_ratio&gt;</code>)
property of Particles node.</td>
</tr>
</tbody>
</table>

Note

In order to use the `COLOR` variable in a StandardMaterial3D, set
`vertex_color_use_as_albedo` to `true`. In a ShaderMaterial, access it
with the `COLOR` variable.

## Start built-ins

<table>
<colgroup>
<col style="width: 15%" />
<col style="width: 84%" />
</colgroup>
<thead>
<tr>
<th>Built-in</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>in bool <strong>RESTART_POSITION</strong></td>
<td><code>true</code> if particle is restarted, or emitted without a
custom position (i.e. this particle was created by
<code>emit_subparticle()</code> without the
<code>FLAG_EMIT_POSITION</code> flag).</td>
</tr>
<tr>
<td>in bool <strong>RESTART_ROT_SCALE</strong></td>
<td><code>true</code> if particle is restarted, or emitted without a
custom rotation or scale (i.e. this particle was created by
<code>emit_subparticle()</code> without the
<code>FLAG_EMIT_ROT_SCALE</code> flag).</td>
</tr>
<tr>
<td>in bool <strong>RESTART_VELOCITY</strong></td>
<td><code>true</code> if particle is restarted, or emitted without a
custom velocity (i.e. this particle was created by
<code>emit_subparticle()</code> without the
<code>FLAG_EMIT_VELOCITY</code> flag).</td>
</tr>
<tr>
<td>in bool <strong>RESTART_COLOR</strong></td>
<td><code>true</code> if particle is restarted, or emitted without a
custom color (i.e. this particle was created by
<code>emit_subparticle()</code> without the <code>FLAG_EMIT_COLOR</code>
flag).</td>
</tr>
<tr>
<td>in bool <strong>RESTART_CUSTOM</strong></td>
<td><code>true</code> if particle is restarted, or emitted without a
custom property (i.e. this particle was created by
<code>emit_subparticle()</code> without the
<code>FLAG_EMIT_CUSTOM</code> flag).</td>
</tr>
</tbody>
</table>

## Process built-ins

<table>
<colgroup>
<col style="width: 26%" />
<col style="width: 73%" />
</colgroup>
<thead>
<tr>
<th>Built-in</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>in bool <strong>RESTART</strong></td>
<td><code>true</code> if the current process frame is first for the
particle.</td>
</tr>
<tr>
<td>in bool <strong>COLLIDED</strong></td>
<td><code>true</code> when the particle has collided with a particle
collider.</td>
</tr>
<tr>
<td>in vec3 <strong>COLLISION_NORMAL</strong></td>
<td>A normal of the last collision. If there is no collision detected it
is equal to <code>(0.0, 0.0, 0.0)</code>.</td>
</tr>
<tr>
<td>in float <strong>COLLISION_DEPTH</strong></td>
<td>A length of normal of the last collision. If there is no collision
detected it is equal to <code>0.0</code>.</td>
</tr>
<tr>
<td>in vec3 <strong>ATTRACTOR_FORCE</strong></td>
<td>A combined force of the attractors at the moment on that
particle.</td>
</tr>
</tbody>
</table>

## Process functions

`emit_subparticle()` is currently the only custom function supported by
particles shaders. It allows users to add a new particle with specified
parameters from a sub-emitter. The newly created particle will only use
the properties that match the `flags` parameter. For example, the
following code will emit a particle with a specified position, velocity,
and color, but unspecified rotation, scale, and custom value:

    mat4 custom_transform = mat4(1.0);
    custom_transform[3].xyz = vec3(10.5, 0.0, 4.0);
    emit_subparticle(custom_transform, vec3(1.0, 0.5, 1.0), vec4(1.0, 0.0, 0.0, 1.0), vec4(1.0), FLAG_EMIT_POSITION | FLAG_EMIT_VELOCITY | FLAG_EMIT_COLOR);

<table>
<colgroup>
<col style="width: 70%" />
<col style="width: 29%" />
</colgroup>
<thead>
<tr>
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td>bool <strong>emit_subparticle</strong> (mat4 xform, vec3 velocity,
vec4 color, vec4 custom, uint flags)</td>
<td>Emits a particle from a sub-emitter.</td>
</tr>
</tbody>
</table>
