# Fog shaders

Fog shaders are used to define how fog is added (or subtracted) from a
scene in a given area. Fog shaders are always used together with
`FogVolumes <class_FogVolume>` and volumetric fog. Fog shaders only have
one processing function, the `fog()` function.

The resolution of the fog shaders depends on the resolution of the
volumetric fog froxel grid. Accordingly, the level of detail that a fog
shader can add depends on how close the `FogVolume <class_FogVolume>` is
to the camera.

Fog shaders are a special form of compute shader that is called once for
every froxel that is touched by an axis aligned bounding box of the
associated `FogVolume <class_FogVolume>`. This means that froxels that
just barely touch a given `FogVolume <class_FogVolume>` will still be
used.

## Built-ins

Values marked as `in` are read-only. Values marked as `out` can
optionally be written to and will not necessarily contain sensible
values. Samplers cannot be written to so they are not marked.

## Global built-ins

Global built-ins are available everywhere, including in custom
functions.

<table>
<colgroup>
<col style="width: 27%" />
<col style="width: 72%" />
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

## Fog built-ins

All of the output values of fog volumes overlap one another. This allows
`FogVolumes <class_FogVolume>` to be rendered efficiently as they can
all be drawn at once.

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
<td>in vec3 <strong>WORLD_POSITION</strong></td>
<td>Position of current froxel cell in world space.</td>
</tr>
<tr>
<td>in vec3 <strong>OBJECT_POSITION</strong></td>
<td>Position of the center of the current <code class="interpreted-text"
role="ref">FogVolume &lt;class_FogVolume&gt;</code> in world space.</td>
</tr>
<tr>
<td>in vec3 <strong>UVW</strong></td>
<td>3-dimensional UV, used to map a 3D texture to the current <code
class="interpreted-text"
role="ref">FogVolume &lt;class_FogVolume&gt;</code>.</td>
</tr>
<tr>
<td>in vec3 <strong>SIZE</strong></td>
<td>Size of the current <code class="interpreted-text"
role="ref">FogVolume &lt;class_FogVolume&gt;</code> when its <code
class="interpreted-text"
role="ref">shape&lt;class_FogVolume_property_shape&gt;</code> has a
size.</td>
</tr>
<tr>
<td>in vec3 <strong>SDF</strong></td>
<td>Signed distance field to the surface of the <code
class="interpreted-text"
role="ref">FogVolume &lt;class_FogVolume&gt;</code>. Negative if inside
volume, positive otherwise.</td>
</tr>
<tr>
<td>out vec3 <strong>ALBEDO</strong></td>
<td>Output base color value, interacts with light to produce final
color. Only written to fog volume if used.</td>
</tr>
<tr>
<td>out float <strong>DENSITY</strong></td>
<td>Output density value. Can be negative to allow subtracting one
volume from another. Density must be used for fog shader to write
anything at all.</td>
</tr>
<tr>
<td>out vec3 <strong>EMISSION</strong></td>
<td>Output emission color value, added to color during light pass to
produce final color. Only written to fog volume if used.</td>
</tr>
</tbody>
</table>
