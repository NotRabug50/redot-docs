# Upgrading from Godot 4.1 to Godot 4.2

For most games and apps made with 4.1 it should be relatively safe to
migrate to 4.2. This page intends to cover everything you need to pay
attention to when migrating your project.

## Breaking changes

If you are migrating from 4.1 to 4.2, the breaking changes listed here
might affect you. Changes are grouped by areas/systems.

Warning

The `class_Mesh` resource format has changed in 4.2 to allow for [vertex
and attribute
compression](https://github.com/godotengine/godot/pull/81138). This
allows for improved rendering performance, especially on platforms
constrained by memory bandwidth such as mobile.

It is still possible to load the Godot 4.0-4.1 Mesh formats, but it is
**not** possible to load the Godot 4.2 Mesh format in prior Godot
versions. When opening a Godot project made with a version prior to 4.2,
you may be presented with an upgrade dialog that offers two options:

-   **Restart & Upgrade:** Upgrades the mesh format for all meshes in
    the project and saves the result to disk. Once chosen, this option
    prevents downgrading the project to a Godot version prior to 4.2.
    Set up a version control system and push your changes *before*
    choosing this option!
-   **Upgrade Only:** Upgrades the mesh format in-memory without writing
    it to disk. This allows downgrading the project to a Godot version
    older than 4.2 if you need to do so in the future. The downside is
    that loading the project will be slower every time as the mesh
    format needs to be upgraded every time the project is loaded. These
    increased loading times will also affect the exported project. The
    number and complexity of Mesh resources determines how much loading
    times are affected.

If this dialog doesn't appear, use **Project &gt; Tools &gt; Upgrade
Mesh Surfaces…** at the top of the editor.

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
<td><strong>Node</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Constant <code>NOTIFICATION_NODE_RECACHE_REQUESTED</code>
removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| `</td>
<td>GH-84419`_</td>
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
<td><strong>AnimationPlayer</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>_post_process_key_value</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>add_animation_library</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>advance</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Signal <code>animation_finished</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-80813`_</td>
</tr>
<tr>
<td>Signal <code>animation_started</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-80813`_</td>
</tr>
<tr>
<td>Signal <code>animation_libraries_updated</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Signal <code>animation_list_changed</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Property <code>audio_max_polyphony</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Signal <code>caches_cleared</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>clear_caches</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>find_animation</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>find_animation_library</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>get_animation</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>get_animation_library</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>get_animation_library_list</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>get_animation_list</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>has_animation</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>has_animation_library</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Property <code>method_call_mode</code> renamed to
<code>callback_mode_method</code> and moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Property <code>playback_active</code> renamed to <code>active</code>
and moved to base class <code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Property <code>playback_process_mode</code> renamed to
<code>callback_mode_process</code> and moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>remove_animation_library</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>rename_animation_library</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Property <code>reset_on_save</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Property <code>root_node</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>set_reset_on_save_enabled</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>seek</code> adds a new <code>update_only</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td><strong>AnimationTree</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>_post_process_key_value</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Property <code>active</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>advance</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Signal <code>animation_finished</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-80813`_</td>
</tr>
<tr>
<td>Signal <code>animation_started</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-80813`_</td>
</tr>
<tr>
<td>Property <code>audio_max_polyphony</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>get_root_motion_position</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>get_root_motion_position_accumulator</code> moved to
base class <code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>get_root_motion_rotation</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>get_root_motion_rotation_accumulator</code> moved to
base class <code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>get_root_motion_scale</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Method <code>get_root_motion_scale_accumulator</code> moved to base
class <code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Property <code>process_callback</code> renamed to
<code>callback_mode_process</code> and moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Property <code>root_motion_track</code> moved to base class
<code>AnimationMixer</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-80813`_</td>
</tr>
<tr>
<td>Property <code>tree_root</code> changes type from
<code>AnimationNode</code> to <code>AnimationRootNode</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-80813`_</td>
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
<td><strong>PopupMenu</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>add_icon_shortcut</code> adds a new
<code>allow_echo</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-36493`_</td>
</tr>
<tr>
<td>Method <code>add_shortcut</code> adds a new <code>allow_echo</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-36493`_</td>
</tr>
<tr>
<td>Method <code>clear</code> adds a new <code>free_submenus</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-79965`_</td>
</tr>
<tr>
<td><strong>RichTextLabel</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>add_image</code> adds new <code>key</code>,
<code>pad</code>, <code>tooltip</code>, and <code>size_in_percent</code>
optional parameters</td>
<td><blockquote>
<p><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code></p>
</blockquote></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility. A compatibility method was added.)</code>
|</td>
<td>✔️| `G</td>
<td>H-80410`_</td>
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
<td><strong>ImporterMesh</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>add_surface</code> changes <code>flags</code> parameter
type from <code>uint32</code> to <code>uint64</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-81138`_</td>
</tr>
<tr>
<td>Method <code>get_surface_format</code> changes return type from
<code>uint32</code> to <code>uint64</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-81138`_</td>
</tr>
<tr>
<td><strong>MeshDataTool</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>commit_to_surface</code> adds a new
<code>compression_flags</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-81138`_</td>
</tr>
<tr>
<td>Method <code>get_format</code> changes return type from
<code>uint32</code> to <code>uint64</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-81138`_</td>
</tr>
<tr>
<td><strong>RenderingDevice</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Enum field <code>BarrierMask.BARRIER_MASK_RASTER</code> changes
value from <code>1</code> to <code>9</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79911`_</td>
</tr>
<tr>
<td>Enum field <code>BarrierMask.BARRIER_MASK_ALL_BARRIERS</code>
changes value from <code>7</code> to <code>32767</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79911`_</td>
</tr>
<tr>
<td>Enum field <code>BarrierMask.BARRIER_MASK_NO_BARRIER</code> changes
value from <code>8</code> to <code>32768</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79911`_</td>
</tr>
<tr>
<td>Method <code>shader_create_from_bytecode</code> adds a new
<code>placeholder_rid</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-79606`_</td>
</tr>
<tr>
<td>Method <code>shader_get_vertex_input_attribute_ask</code> changes
return type from <code>uint32</code> to <code>uint64</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-81138`_</td>
</tr>
<tr>
<td><strong>SurfaceTool</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>commit</code> changes <code>flags</code> parameter type
from <code>uint32</code> to <code>uint64</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-81138`_</td>
</tr>
</tbody>
</table>

### Text

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
<td><strong>Font</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>set_fallbacks</code> replaced with
<code>fallbacks</code> property</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-78266`_</td>
</tr>
<tr>
<td>Method <code>get_fallbacks</code> replaced with
<code>fallbacks</code> property</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-78266`_</td>
</tr>
<tr>
<td>Method <code>find_variation</code> adds new
<code>spacing_top</code>, <code>spacing_bottom</code>,
<code>spacing_space</code>, and <code>spacing_glyph</code> optional
parameters</td>
<td><blockquote>
<p><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code></p>
</blockquote></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility. A compatibility method was added.)</code>
|</td>
<td>✔️| `G</td>
<td>H-80954`_</td>
</tr>
</tbody>
</table>

### GraphEdit

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
<td><strong>GraphEdit</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>arrange_nodes_button_hidden</code> renamed to
<code>show_arrange_button</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility. A compatibility method was added.)</code>
|</td>
<td>✔️ with compat| `G</td>
<td>H-81582`_</td>
</tr>
<tr>
<td>Method <code>get_zoom_hbox</code> renamed to
<code>get_menu_hbox</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility. A compatibility method was added.)</code>
|</td>
<td>✔️ with compat| `G</td>
<td>H-79308`_</td>
</tr>
<tr>
<td>Property <code>snap_distance</code> renamed to
<code>snapping_distance</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility. A compatibility method was added.)</code>
|</td>
<td>✔️ with compat| `G</td>
<td>H-79308`_</td>
</tr>
<tr>
<td>Property <code>use_snap</code> renamed to
<code>snapping_enabled</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility. A compatibility method was added.)</code>
|</td>
<td>✔️ with compat| `G</td>
<td>H-79308`_</td>
</tr>
<tr>
<td><strong>GraphNode</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>comment</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79307">GH-79307</a></td>
</tr>
<tr>
<td>Signal <code>close_request</code> renamed to
<code>delete_request</code> and moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility. A compatibility method was added.)</code>
|</td>
<td>✔️ with compat| `G</td>
<td>H-79311`_</td>
</tr>
<tr>
<td>Property <code>draggable</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79311`_</td>
</tr>
<tr>
<td>Property <code>draggable</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79311`_</td>
</tr>
<tr>
<td>Signal <code>dragged</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-79311`_</td>
</tr>
<tr>
<td>Method <code>get_connection_input_color</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Method <code>get_connection_input_count</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Method <code>get_connection_input_height</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Method <code>get_connection_input_position</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Method <code>get_connection_input_slot</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Method <code>get_connection_input_type</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Method <code>get_connection_output_color</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Method <code>get_connection_output_count</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Method <code>get_connection_output_height</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Method <code>get_connection_output_position</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Method <code>get_connection_output_slot</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Method <code>get_connection_output_type</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Property <code>language</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Signal <code>node_deselected</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79311`_</td>
</tr>
<tr>
<td>Signal <code>node_selected</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79311`_</td>
</tr>
<tr>
<td>Property <code>overlay</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Property <code>position_offset</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79311`_</td>
</tr>
<tr>
<td>Signal <code>position_offset_changed</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79311`_</td>
</tr>
<tr>
<td>Signal <code>raise_request</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79311`_</td>
</tr>
<tr>
<td>Property <code>resizable</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79311`_</td>
</tr>
<tr>
<td>Signal <code>resize_request</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-79311`_</td>
</tr>
<tr>
<td>Property <code>selectable</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79311`_</td>
</tr>
<tr>
<td>Property <code>selected</code> moved to base class
<code>GraphElement</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️| |✔</td>
<td>️| `GH</td>
<td>-79311`_</td>
</tr>
<tr>
<td>Property <code>show_close</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
<tr>
<td>Property <code>text_direction</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/79311">GH-79311</a></td>
</tr>
</tbody>
</table>

### TileMap

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
<td><strong>TileMap</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>cell_quadrant_size</code> renamed to
<code>rendering_quadrant_size</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility. A compatibility method was added.)</code>
|</td>
<td>✔️ with compat| `G</td>
<td>H-81070`_</td>
</tr>
</tbody>
</table>

### XR

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
<td><strong>XRInterface</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>environment_blend_mode</code> added</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-81561`_</td>
</tr>
</tbody>
</table>

Note

This change breaks compatibility in C# because the new property
conflicts with the name of an existing enum and the C# bindings
generator gives priority to properties, so the enum type was renamed
from `EnvironmentBlendMode` to `EnvironmentBlendModeEnum`.
