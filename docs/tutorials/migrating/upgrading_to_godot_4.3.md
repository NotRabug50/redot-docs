# Upgrading from Godot 4.2 to Godot 4.3

For most games and apps made with 4.2 it should be relatively safe to
migrate to 4.3. This page intends to cover everything you need to pay
attention to when migrating your project.

## Breaking changes

If you are migrating from 4.2 to 4.3, the breaking changes listed here
might affect you. Changes are grouped by areas/systems.

This article indicates whether each breaking change affects GDScript and
whether the C# breaking change is *binary compatible* or *source
compatible*:

-   **Binary compatible** - Existing binaries will load and execute
    successfully without recompilation, and the run-time behavior won't
    change.
-   **Source compatible** - Source code will compile successfully
    without changes when upgrading Godot.

### GDExtension

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
<td><strong>GDExtension</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>close_library</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/88418">GH-88418</a></td>
</tr>
<tr>
<td>Method <code>initialize_library</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/88418">GH-88418</a></td>
</tr>
<tr>
<td>Method <code>open_library</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/88418">GH-88418</a></td>
</tr>
</tbody>
</table>

Since it was basically impossible to use these methods in any useful
way, these methods have been removed. Use
`GDExtensionManager::load_extension` and
`GDExtensionManager::unload_extension` instead to correctly load and
unload a GDExtension.

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
<td><strong>Animation</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>position_track_interpolate</code> adds a new
<code>backward</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-86629`_</td>
</tr>
<tr>
<td>Method <code>rotation_track_interpolate</code> adds a new
<code>backward</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-86629`_</td>
</tr>
<tr>
<td>Method <code>scale_track_interpolate</code> adds a new
<code>backward</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-86629`_</td>
</tr>
<tr>
<td>Method <code>blend_shape_track_interpolate</code> adds a new
<code>backward</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-86629`_</td>
</tr>
<tr>
<td>Method <code>value_track_interpolate</code> adds a new
<code>backward</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-86629`_</td>
</tr>
<tr>
<td>Method <code>track_find_key</code> adds a new <code>limit</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-86661`_</td>
</tr>
<tr>
<td>Method <code>track_find_key</code> adds a new <code>backward</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-92861`_</td>
</tr>
<tr>
<td><strong>AnimationMixer</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>_post_process_key_value</code> changes
<code>object</code> parameter type from <code>Object</code> to
<code>uint64</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-86687`_</td>
</tr>
<tr>
<td><strong>Skeleton3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>add_bone</code> changes return type from
<code>void</code> to <code>int32</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>✔️| `G</td>
<td>H-88791`_</td>
</tr>
<tr>
<td>Signal <code>bone_pose_changed</code> replaced by
<code>skeleton_updated</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/90575">GH-90575</a></td>
</tr>
<tr>
<td><strong>BoneAttachment3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>on_bone_pose_update</code> replaced by
<code>on_skeleton_update</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-90575`_</td>
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
<td><strong>AcceptDialog</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>register_text_enter</code> changes parameter
<code>line_edit</code> type from <code>Control</code> to
<code>LineEdit</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-89419`_</td>
</tr>
<tr>
<td>Method <code>remove_button</code> changes parameter
<code>button</code> type from <code>Control</code> to
<code>Button</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-89419`_</td>
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
<td><strong>PhysicsShapeQueryParameters3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>motion</code> changes type from <code>Vector2</code>
to <code>Vector3</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/85393">GH-85393</a></td>
</tr>
</tbody>
</table>

Note

In C#, the enum `PhysicsServer3D.G6DofJointAxisFlag` breaks
compatibility because of the way the bindings generator detects the enum
prefix. New members were added in
[GH-89851](https://github.com/godotengine/godot/pull/89851) to the enum
that caused the enum members to be renamed.

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
<td><strong>RenderingDevice</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Enum field <code>FinalAction.FINAL_ACTION_CONTINUE</code> changes
value from <code>2</code> to <code>0</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-84976`_</td>
</tr>
<tr>
<td>Enum field <code>InitialAction.INITIAL_ACTION_CLEAR</code> changes
value from <code>0</code> to <code>1</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-84976`_</td>
</tr>
<tr>
<td>Enum field
<code>InitialAction.INITIAL_ACTION_CLEAR_REGION_CONTINUE</code> changes
value from <code>2</code> to <code>1</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-84976`_</td>
</tr>
<tr>
<td>Enum field <code>InitialAction.INITIAL_ACTION_CONTINUE</code>
changes value from <code>5</code> to <code>0</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-84976`_</td>
</tr>
<tr>
<td>Enum field <code>InitialAction.INITIAL_ACTION_DROP</code> changes
value from <code>4</code> to <code>2</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-84976`_</td>
</tr>
<tr>
<td>Enum field <code>InitialAction.INITIAL_ACTION_KEEP</code> changes
value from <code>3</code> to <code>0</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-84976`_</td>
</tr>
<tr>
<td>Method <code>buffer_clear</code> removes <code>post_barrier</code>
parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-84976`_</td>
</tr>
<tr>
<td>Method <code>buffer_update</code> removes <code>post_barrier</code>
parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-84976`_</td>
</tr>
<tr>
<td>Method <code>compute_list_begin</code> removes
<code>allow_draw_overlap</code> parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-84976`_</td>
</tr>
<tr>
<td>Method <code>compute_list_end</code> removes
<code>post_barrier</code> parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-84976`_</td>
</tr>
<tr>
<td>Method <code>draw_list_begin</code> removes
<code>storage_textures</code> parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-84976`_</td>
</tr>
<tr>
<td>Method <code>draw_list_end</code> removes <code>post_barrier</code>
parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-84976`_</td>
</tr>
<tr>
<td>Method <code>texture_clear</code> removes <code>post_barrier</code>
parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-84976`_</td>
</tr>
<tr>
<td>Method <code>texture_copy</code> removes <code>post_barrier</code>
parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-84976`_</td>
</tr>
<tr>
<td>Method <code>texture_resolve_multisample</code> removes
<code>post_barrier</code> parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-84976`_</td>
</tr>
<tr>
<td>Method <code>texture_update</code> removes <code>post_barrier</code>
parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️ with compat| `GH</td>
<td>-84976`_</td>
</tr>
<tr>
<td><strong>RenderingServer</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>environment_set_fog</code> adds a new
<code>fog_mode</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-84792`_</td>
</tr>
<tr>
<td><strong>RenderSceneBuffersRD</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>get_color_layer</code> adds a new <code>msaa</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-80214`_</td>
</tr>
<tr>
<td>Method <code>get_depth_layer</code> adds a new <code>msaa</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-80214`_</td>
</tr>
<tr>
<td>Method <code>get_velocity_layer</code> adds a new <code>msaa</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-80214`_</td>
</tr>
<tr>
<td>Method <code>get_color_texture</code> adds a new <code>msaa</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-80214`_</td>
</tr>
<tr>
<td>Method <code>get_depth_texture</code> adds a new <code>msaa</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-80214`_</td>
</tr>
<tr>
<td>Method <code>get_velocity_texture</code> adds a new
<code>msaa</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-80214`_</td>
</tr>
</tbody>
</table>

Note

While the values of the enum fields in `RenderingDevice.InitialAction`
and `RenderingDevice.FinalAction` changed, the only method that consumed
them (`draw_list_begin`) added a compatibility method which supports the
old values. So in practice it doesn't break compatibility.

Note

In C#, the enum `RenderingDevice.DriverResource` breaks compatibility
because of the way the bindings generator detects the enum prefix. New
members were added in
[GH-83452](https://github.com/godotengine/godot/pull/83452) to the enum
that caused the enum members to be renamed.

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
<td>Method <code>find_variation</code> adds a new
<code>baseline_offset</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-87668`_</td>
</tr>
<tr>
<td><strong>RichTextLabel</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>push_meta</code> adds a new <code>underline_mode</code>
optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-89024`_</td>
</tr>
<tr>
<td><strong>TextServer</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>shaped_text_get_word_breaks</code> adds a new optional
<code>skip_grapheme_flags</code> parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-90732`_</td>
</tr>
<tr>
<td><strong>TextServerExtension</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>_shaped_text_get_word_breaks</code> adds a new
<code>skip_grapheme_flags</code> parameter</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/90732">GH-90732</a></td>
</tr>
</tbody>
</table>

### Audio

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
<td><strong>AudioStreamPlaybackPolyphonic</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>play_stream</code> adds new <code>playback_type</code>,
and <code>bus</code> optional parameters</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-91382`_</td>
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
<td><strong>AStar2D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>get_id_path</code> adds new
<code>allow_partial_path</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-88047`_</td>
</tr>
<tr>
<td>Method <code>get_point_path</code> adds new
<code>allow_partial_path</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-88047`_</td>
</tr>
<tr>
<td><strong>AStar3D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>get_id_path</code> adds new
<code>allow_partial_path</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-88047`_</td>
</tr>
<tr>
<td>Method <code>get_point_path</code> adds new
<code>allow_partial_path</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-88047`_</td>
</tr>
<tr>
<td><strong>AStarGrid2D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>get_id_path</code> adds new
<code>allow_partial_path</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-88047`_</td>
</tr>
<tr>
<td>Method <code>get_point_path</code> adds new
<code>allow_partial_path</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-88047`_</td>
</tr>
<tr>
<td><strong>NavigationRegion2D</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Property <code>avoidance_layers</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/90747">GH-90747</a></td>
</tr>
<tr>
<td>Property <code>constrain_avoidance</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/90747">GH-90747</a></td>
</tr>
<tr>
<td>Method <code>get_avoidance_layer_value</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/90747">GH-90747</a></td>
</tr>
<tr>
<td>Method <code>set_avoidance_layer_value</code> removed</td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/90747">GH-90747</a></td>
</tr>
</tbody>
</table>

Note

The constrain avoidance feature in `NavigationRegion2D` was experimental
and has been discontinued with no replacement.

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
<td><strong>TileData</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>get_navigation_polygon</code> adds new
<code>flip_h</code>, <code>flip_v</code>, and <code>transpose</code>
optional parameters</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-84660`_</td>
</tr>
<tr>
<td>Method <code>get_occluder</code> adds new <code>flip_h</code>,
<code>flip_v</code>, and <code>transpose</code> optional parameters</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-84660`_</td>
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
<td><strong>WebXRInterface</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>get_input_source_tracker</code> changes return type
from <code>XRPositionalTracker</code> to
<code>XRControllerTracker</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>✔️| `G</td>
<td>H-90645`_</td>
</tr>
<tr>
<td><strong>XRServer</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>get_tracker</code> changes return type from
<code>XRPositionalTracker</code> to <code>XRTracker</code></td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>❌| |</td>
<td>❌| `</td>
<td>GH-90645`_</td>
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
<td><strong>EditorInspectorPlugin</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>add_property_editor</code> adds a new
<code>label</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-92322`_</td>
</tr>
<tr>
<td><strong>EditorPlugin</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Method <code>add_control_to_bottom_panel</code> adds a new
<code>shortcut</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-88081`_</td>
</tr>
<tr>
<td>Method <code>add_control_to_dock</code> adds a new
<code>shortcut</code> optional parameter</td>
<td><code class="interpreted-text"
role="abbr">✔️ (This API does not break compatibility.)</code> |</td>
<td>✔️ with compat| |✔</td>
<td>️| `GH</td>
<td>-88081`_</td>
</tr>
<tr>
<td><strong>EditorSceneFormatImporterFBX</strong></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr>
<td>Type renamed to <code>EditorSceneFormatImporterFBX2GLTF</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><code class="interpreted-text"
role="abbr">❌ (This API breaks compatibility.)</code></td>
<td><a
href="https://github.com/godotengine/godot/pull/81746">GH-81746</a></td>
</tr>
</tbody>
</table>

## Behavior changes

In 4.3 some behavior changes have been introduced, which might require
you to adjust your project.

### Core

Note

Binary serialization was modified to fix some issues with the
serialization of scripted Objects and typed Arrays
([GH-78219](https://github.com/godotengine/godot/pull/78219)). This
breaks compat with script encoding/decoding.

Note

`PackedByteArray` is now able to use a more compact base64 encoding for
storage. But the trade-off is that it breaks compatibility, meaning that
older versions of Godot may not be able to open resources saved by 4.3
([GH-89186](https://github.com/godotengine/godot/pull/89186)).

To maximize compatibility, this new storage format will only be enabled
for resources and scenes that contain large PackedByteArrays for now.
Support for this new format will also be added in patch updates for
older versions of Godot. Once all supported Godot versions are able to
read the new format, we will gradually retire the compatibility measures
and have all resources and scenes use the new storage format.

Note

In C#, the `Transform3D.InterpolateWith` implementation was fixed to use
the right order of operations, applying the rotation before the scale
([GH-89843](https://github.com/godotengine/godot/pull/89843)).

Note

In C#, the `Aabb.GetSupport` implementation was fixed to properly return
the support vector
([GH-88919](https://github.com/godotengine/godot/pull/88919)).

Note

In C#, the Variant types' `ToString` implementation now defaults to
using the `InvariantCulture`
([GH-89547](https://github.com/godotengine/godot/pull/89547)) which
means `Vector2(1.2, 3.4)` is formatted using `.` as the decimal
separator independently of the language of the operating system that the
program is running on.

### Animation

Note

`AnimationMixer` replaced its Capture mode with a new Capture feature
that works much better than the old one, this replaces the existing
cache ([GH-86715](https://github.com/godotengine/godot/pull/86715)).

Note

`AnimationNode` has a reworked process for retrieving the semantic time
info. This ensures that time-related behavior works as expected, but
changes the blending behavior. Implementors of the `_process` virtual
method should also note that this method is now deprecated and will be
replaced by a new one in the future
([GH-87171](https://github.com/godotengine/godot/pull/87171)).

More information about the changes to Animation can be found in the
[Migrating Animations from Godot 4.0 to
4.3](https://godotengine.org/article/migrating-animations-from-godot-4-0-to-4-3)
article.

### GUI nodes

Note

The default font outline color was changed from white to black
([GH-54641](https://github.com/godotengine/godot/pull/54641)).

Note

The `auto_translate` property is deprecated in favor of the
`auto_translate_mode` property which is now in `Node`
([GH-87530](https://github.com/godotengine/godot/pull/87530)). The
default value for `auto_translate_mode` is `AUTO_TRANSLATE_INHERIT`,
which means nodes inherit the `auto_translate_mode` value from their
parent. This means, existing nodes with the `auto_translate` property
set to `true` may no longer be translated if they are children of a node
with the `auto_translate` property set to `false`.

### Multiplayer

Note

The `SceneMultiplayer` caching protocol was changed to send the received
ID instead of the Node path when sending a node removal confirmation
packet ([GH-90027](https://github.com/godotengine/godot/pull/90027)).

This is a breaking change for the high-level multiplayer protocol making
it incompatible with previous Godot versions. Upgrade both your server
and client versions to Godot 4.3 to handle this change gracefully.

Note that high-level multiplayer facilities are only ever meant to be
compatible with server and client using the same Godot version. It is
recommended to implement some kind of version checking.

### Rendering

Note

Decals now convert the modulate color from an sRGB color to a linear
color, like all other inputs, to ensure proper blending
([GH-89849](https://github.com/godotengine/godot/pull/89849)). Existing
projects that were using the decal's modulate property will notice a
change in their visuals.

Note

The reverse Z depth buffer technique is now implemented. This may break
compatibility for some shaders. Read the [Introducing Reverse Z (AKA I'm
sorry for breaking your
shader)](https://godotengine.org/article/introducing-reverse-z/) article
for more information and guidance on how to fix common scenarios.

### TileMap

Note

`TileMap` layers were moved to individual nodes
([GH-87379](https://github.com/godotengine/godot/pull/87379) and
[GH-89179](https://github.com/godotengine/godot/pull/89179)).

### Android

Note

Android permissions are no longer requested automatically because it
goes against the recommended best practices
([GH-87080](https://github.com/godotengine/godot/pull/87080)). Use the
`request_permission` method in `OS` and the
`on_request_permissions_result` signal on `MainLoop` to request
permissions and wait for the user response.
