# Upgrading from Godot 4.0 to Godot 4.1

For most games and apps made with 4.0, it should be relatively safe to
migrate to 4.1. This page intends to cover everything you need to pay
attention to when migrating your project.

## Breaking changes

If you are migrating from 4.0 to 4.1, the breaking changes listed here
might affect you. Changes are grouped by areas/systems.

Warning

The GDExtension API completely breaks compatibility in 4.1, so it's not
included in the table below. See the
`updating_your_gdextension_for_godot_4_1` section for more information.

This article indicates whether each breaking change affects GDScript and
whether the C# breaking change is *binary compatible* or *source
compatible*:

-   **Binary compatible** - Existing binaries will load and execute
    successfully without recompilation, and the run-time behavior won't
    change.
-   **Source compatible** - Source code will compile successfully
    without changes when upgrading Godot.

### Core

<table>
<thead>
<tr>
<th>Change</th>
<th>GDScript Compatible</th>
<th>C# Binary Compatible</th>
<th>C# Source Compatible</th>
<th>Introduced</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Basis</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>looking_at</code> adds a new
<code>use_model_front</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-76082`_</td>
</tr>
<tr>
<td><strong>Object</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>get_meta_list</code> changes return type from
<code>PackedStringArray</code> to <code>Array[StringName]</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-76418`_</td>
</tr>
<tr>
<td><strong>Transform3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>looking_at</code> adds a new
<code>use_model_front</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-76082`_</td>
</tr>
<tr>
<td><strong>UndoRedo</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>create_action</code> adds a new
<code>backward_undo_ops</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-76688`_</td>
</tr>
<tr>
<td><strong>WorkerThreadPool</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>wait_for_task_completion</code> changes return type
from <code>void</code> to <code>Error</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>✔️| `G</td>
<td>H-77143`_</td>
</tr>
</tbody>
</table>

### Animation

<table>
<thead>
<tr>
<th>Change</th>
<th>GDScript Compatible</th>
<th>C# Binary Compatible</th>
<th>C# Source Compatible</th>
<th>Introduced</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>AnimationNode</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>_process</code> adds a new <code>test_only</code>
parameter</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/75759">GH-75759</a></td>
</tr>
<tr>
<td>Method <code>blend_input</code> adds a new <code>test_only</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-75759`_</td>
</tr>
<tr>
<td>Method <code>blend_node</code> adds a new <code>test_only</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-75759`_</td>
</tr>
<tr>
<td><strong>AnimationNodeStateMachinePlayback</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>get_travel_path</code> changes return type from
<code>PackedStringArray</code> to <code>Array[StringName]</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-76418`_</td>
</tr>
</tbody>
</table>

### 2D nodes

<table>
<thead>
<tr>
<th>Change</th>
<th>GDScript Compatible</th>
<th>C# Binary Compatible</th>
<th>C# Source Compatible</th>
<th>Introduced</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>PathFollow2D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>lookahead</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/72842">GH-72842</a></td>
</tr>
</tbody>
</table>

### 3D nodes

<table>
<thead>
<tr>
<th>Change</th>
<th>GDScript Compatible</th>
<th>C# Binary Compatible</th>
<th>C# Source Compatible</th>
<th>Introduced</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Geometry3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>segment_intersects_convex</code> changes
<code>planes</code> parameter type from untyped <code>Array</code> to
<code>Array[Plane]</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |❌</td>
<td><div class="line-block">                 `GH</div></td>
<td>-76418`_</td>
</tr>
<tr>
<td><strong>MeshInstance3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>create_multiple_convex_collisions</code> adds a new
<code>settings</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-72152`_</td>
</tr>
<tr>
<td><strong>Node3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>look_at</code> adds a new <code>use_model_front</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-76082`_</td>
</tr>
<tr>
<td>Method <code>look_at_from_position</code> adds a new
<code>use_model_front</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-76082`_</td>
</tr>
</tbody>
</table>

### GUI nodes

<table>
<thead>
<tr>
<th>Change</th>
<th>GDScript Compatible</th>
<th>C# Binary Compatible</th>
<th>C# Source Compatible</th>
<th>Introduced</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>CodeEdit</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>add_code_completion_option</code> adds a new
<code>location</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-75746`_</td>
</tr>
<tr>
<td><strong>RichTextLabel</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>push_list</code> adds a new <code>bullet</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-75017`_</td>
</tr>
<tr>
<td>Method <code>push_paragraph</code> adds a new
<code>justification_flags</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-75250`_</td>
</tr>
<tr>
<td>Method <code>push_paragraph</code> adds a new <code>tab_stops</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-76401`_</td>
</tr>
<tr>
<td><strong>Tree</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>edit_selected</code> adds a new <code>force_edit</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-76794`_</td>
</tr>
</tbody>
</table>

### Physics

<table>
<thead>
<tr>
<th>Change</th>
<th>GDScript Compatible</th>
<th>C# Binary Compatible</th>
<th>C# Source Compatible</th>
<th>Introduced</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>Area2D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>priority</code> changes type from <code>float</code>
to <code>int</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/72749">GH-72749</a></td>
</tr>
<tr>
<td><strong>Area3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>priority</code> changes type from <code>float</code>
to <code>int</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/72749">GH-72749</a></td>
</tr>
<tr>
<td><strong>PhysicsDirectSpaceState2D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>collide_shape</code> changes return type from
<code>Array[PackedVector2Array]</code> to
<code>Array[Vector2]</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/75260">GH-75260</a></td>
</tr>
<tr>
<td><strong>PhysicsDirectSpaceState3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>collide_shape</code> changes return type from
<code>Array[PackedVector3Array]</code> to
<code>Array[Vector3]</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/75260">GH-75260</a></td>
</tr>
</tbody>
</table>

### Rendering

<table>
<thead>
<tr>
<th>Change</th>
<th>GDScript Compatible</th>
<th>C# Binary Compatible</th>
<th>C# Source Compatible</th>
<th>Introduced</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>RDShaderFile</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>get_version_list</code> changes return type from
<code>PackedStringArray</code> to <code>Array[StringName]</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-76418`_</td>
</tr>
<tr>
<td><strong>RenderingDevice</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>draw_list_begin</code> changes
<code>storage_textures</code> parameter type from untyped
<code>Array</code> to <code>Array[RID]</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |❌</td>
<td><div class="line-block">                 `GH</div></td>
<td>-76418`_</td>
</tr>
<tr>
<td><strong>RenderingServer</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>global_shader_parameter_get_list</code> changes return
type from <code>PackedStringArray</code> to
<code>Array[StringName]</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-76418`_</td>
</tr>
<tr>
<td><strong>SurfaceTool</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>add_triangle_fan</code> changes <code>tangents</code>
parameter type from untyped <code>Array</code> to
<code>Array[Plane]</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |❌</td>
<td><div class="line-block">                 `GH</div></td>
<td>-76418`_</td>
</tr>
</tbody>
</table>

### Navigation

<table>
<thead>
<tr>
<th>Change</th>
<th>GDScript Compatible</th>
<th>C# Binary Compatible</th>
<th>C# Source Compatible</th>
<th>Introduced</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>NavigationAgent2D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>set_velocity</code> replaced with <code>velocity</code>
property</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-69988`_</td>
</tr>
<tr>
<td>Property <code>time_horizon</code> split into
<code>time_horizon_agents</code> and
<code>time_horizon_obstacles</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td><strong>NavigationAgent3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>agent_height_offset</code> renamed to
<code>path_height_offset</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td>Property <code>ignore_y</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td>Method <code>set_velocity</code> replaced with <code>velocity</code>
property</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-69988`_</td>
</tr>
<tr>
<td>Property <code>time_horizon</code> split into
<code>time_horizon_agents</code> and
<code>time_horizon_obstacles</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td><strong>NavigationObstacle2D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>estimate_radius</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td>Method <code>get_rid</code> renamed to
<code>get_agent_rid</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td><strong>NavigationObstacle3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>estimate_radius</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td>Method <code>get_rid</code> renamed to
<code>get_agent_rid</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td><strong>NavigationServer2D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>agent_set_callback</code> renamed to
<code>agent_set_avoidance_callback</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td>Method <code>agent_set_target_velocity</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td>Method <code>agent_set_time_horizon</code> split into
<code>agent_set_time_horizon_agents</code> and
<code>agent_set_time_horizon_obstacles</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td><strong>NavigationServer3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>agent_set_callback</code> renamed to
<code>agent_set_avoidance_callback</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td>Method <code>agent_set_target_velocity</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
<tr>
<td>Method <code>agent_set_time_horizon</code> split into
<code>agent_set_time_horizon_agents</code> and
<code>agent_set_time_horizon_obstacles</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/69988">GH-69988</a></td>
</tr>
</tbody>
</table>

### Networking

<table>
<thead>
<tr>
<th>Change</th>
<th>GDScript Compatible</th>
<th>C# Binary Compatible</th>
<th>C# Source Compatible</th>
<th>Introduced</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>WebRTCPeerConnectionExtension</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>_create_data_channel</code> changes return type from
<code>Object</code> to <code>WebRTCDataChannel</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>✔️| `G</td>
<td>H-78237`_</td>
</tr>
</tbody>
</table>

### Editor plugins

<table>
<thead>
<tr>
<th>Change</th>
<th>GDScript Compatible</th>
<th>C# Binary Compatible</th>
<th>C# Source Compatible</th>
<th>Introduced</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>AnimationTrackEditPlugin</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Type <code>AnimationTrackEditPlugin</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/76413">GH-76413</a></td>
</tr>
<tr>
<td><strong>EditorInterface</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Type <code>EditorInterface</code> changes inheritance from
<code>Node</code> to <code>Object</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-76176`_</td>
</tr>
<tr>
<td>Method <code>set_movie_maker_enabled</code> replaced with
<code>movie_maker_enabled</code> property</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-76176`_</td>
</tr>
<tr>
<td>Method <code>is_movie_maker_enabled</code> replaced with
<code>movie_maker_enabled</code> property</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-76176`_</td>
</tr>
<tr>
<td><strong>EditorResourcePreviewGenerator</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>_generate</code> adds a new <code>metadata</code>
parameter</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/64628">GH-64628</a></td>
</tr>
<tr>
<td>Method <code>_generate_from_path</code> adds a new
<code>metadata</code> parameter</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/64628">GH-64628</a></td>
</tr>
<tr>
<td><strong>EditorUndoRedoManager</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>create_action</code> adds a new
<code>backward_undo_ops</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-76688`_</td>
</tr>
</tbody>
</table>

## Behavior changes

In 4.1 some behavior changes have been introduced, which might require
you to adjust your project.

<table>
<thead>
<tr>
<th>Change</th>
<th>Introduced</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>SubViewportContainer</strong></td>
<td></td>
</tr>
<tr>
<td>When input events should reach SubViewports and their children,
<code>SubViewportContainer.mouse_filter</code> now needs to be
<code>MOUSE_FILTER_STOP</code> or <code>MOUSE_FILTER_PASS</code>. See <a
href="https://github.com/godotengine/godot/issues/79271">GH-79271</a>
for details.</td>
<td><a
href="https://github.com/godotengine/godot/pull/57894">GH-57894</a></td>
</tr>
<tr>
<td>Multiple layered <code>SubViewportContainer</code> nodes, that
should all receive mouse input events, now need to be replaced by
<code>Area2D</code> nodes. See <a
href="https://github.com/godotengine/godot/issues/79128">GH-79128</a>
for details.</td>
<td><a
href="https://github.com/godotengine/godot/pull/57894">GH-57894</a></td>
</tr>
<tr>
<td><strong>Viewport</strong></td>
<td></td>
</tr>
<tr>
<td><code>Viewport</code> nodes, that have Physics Picking enabled, now
automatically set InputEvents as handled. See <a
href="https://github.com/godotengine/godot/issues/79897">GH-79897</a>
for workarounds.</td>
<td><a
href="https://github.com/godotengine/godot/pull/77595">GH-77595</a></td>
</tr>
</tbody>
</table>

## Updating your GDExtension for 4.1

GDExtension is still in beta. Until it's marked as stable, compatibility
may break when upgrading to a new minor version of Godot.

In order to fix a serious bug, in Godot 4.1 we had to break binary
compatibility in a big way and source compatibility in a small way.

This means that GDExtensions made for Godot 4.0 will need to be
recompiled for Godot 4.1 (using the `4.1` branch of godot-cpp), with a
small change to their source code.

In Godot 4.0, your "entry\_symbol" function looks something like this:

    GDExtensionBool GDE_EXPORT example_library_init(const GDExtensionInterface *p_interface, const GDExtensionClassLibraryPtr p_library, GDExtensionInitialization *r_initialization) {
        godot::GDExtensionBinding::InitObject init_obj(p_interface, p_library, r_initialization);

        init_obj.register_initializer(initialize_example_module);
        init_obj.register_terminator(uninitialize_example_module);
        init_obj.set_minimum_library_initialization_level(MODULE_INITIALIZATION_LEVEL_SCENE);

        return init_obj.init();
    }

However, for Godot 4.1, it should look like:

    GDExtensionBool GDE_EXPORT example_library_init(GDExtensionInterfaceGetProcAddress p_get_proc_address, const GDExtensionClassLibraryPtr p_library, GDExtensionInitialization *r_initialization) {
        godot::GDExtensionBinding::InitObject init_obj(p_get_proc_address, p_library, r_initialization);

        init_obj.register_initializer(initialize_example_module);
        init_obj.register_terminator(uninitialize_example_module);
        init_obj.set_minimum_library_initialization_level(MODULE_INITIALIZATION_LEVEL_SCENE);

        return init_obj.init();
    }

There are two small changes:

1.  The first argument changes from
    `const GDExtensionInterface *p_interface` to
    `GDExtensionInterfaceGetProcAddress p_get_proc_address`
2.  The constructor for the <span class="title-ref">init\_obj</span>
    variable now receives `p_get_proc_address` as its first parameter

You also need to add an extra `compatibility_minimum` line to your
`.gdextension` file, so that it looks something like:

    [configuration]

    entry_symbol = "example_library_init"
    compatibility_minimum = 4.1

This lets Godot know that your GDExtension has been updated and is safe
to load in Godot 4.1.
