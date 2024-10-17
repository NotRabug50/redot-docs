github\_url  
hide

# EditorSettings

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Object that holds the project-independent editor settings.

classref-introduction-group

## Description

Object that holds the project-independent editor settings. These
settings are generally visible in the **Editor &gt; Editor Settings**
menu.

Property names use slash delimiters to distinguish sections. Setting
values can be of any `Variant<class_Variant>` type. It's recommended to
use `snake_case` for editor settings to be consistent with the Godot
editor itself.

Accessing the settings can be done using the following methods, such as:

gdscript

var settings = EditorInterface.get\_editor\_settings() \#
<span class="title-ref">settings.set("some/property", 10)</span> also
works as this class overrides <span class="title-ref">\_set()</span>
internally. settings.set\_setting("some/property", 10) \#
<span class="title-ref">settings.get("some/property")</span> also works
as this class overrides <span class="title-ref">\_get()</span>
internally. settings.get\_setting("some/property") var
list\_of\_settings = settings.get\_property\_list()

csharp

EditorSettings settings = EditorInterface.Singleton.GetEditorSettings();
// <span class="title-ref">settings.set("some/property", value)</span>
also works as this class overrides
<span class="title-ref">\_set()</span> internally.
settings.SetSetting("some/property", Value); //
<span class="title-ref">settings.get("some/property", value)</span> also
works as this class overrides <span class="title-ref">\_get()</span>
internally. settings.GetSetting("some/property");
Godot.Collections.Array&lt;Godot.Collections.Dictionary&gt;
listOfSettings = settings.GetPropertyList();

\*\*Note:\*\* This class shouldn't be instantiated directly. Instead,
access the singleton using
`EditorInterface.get_editor_settings<class_EditorInterface_method_get_editor_settings>`.

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**settings\_changed**()
`🔗<class_EditorSettings_signal_settings_changed>`

Emitted after any editor setting has changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NOTIFICATION\_EDITOR\_SETTINGS\_CHANGED** = `10000`
`🔗<class_EditorSettings_constant_NOTIFICATION_EDITOR_SETTINGS_CHANGED>`

Emitted after any editor setting has changed. It's used by various
editor plugins to update their visuals on theme changes or logic on
configuration changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **asset\_library/use\_threads**
`🔗<class_EditorSettings_property_asset_library/use_threads>`

If `true`, the Asset Library uses multiple threads for its HTTP
requests. This prevents the Asset Library from blocking the main thread
for every loaded asset.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **debugger/auto\_switch\_to\_remote\_scene\_tree**
`🔗<class_EditorSettings_property_debugger/auto_switch_to_remote_scene_tree>`

If `true`, automatically switches to the **Remote** scene tree when
running the project from the editor. If `false`, stays on the **Local**
scene tree when running the project from the editor.

\*\*Warning:\*\* Enabling this setting can cause stuttering when running
a project with a large amount of nodes (typically a few thousands of
nodes or more), even if the editor window isn't focused. This is due to
the remote scene tree being updated every second regardless of whether
the editor is focused.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **debugger/profile\_native\_calls**
`🔗<class_EditorSettings_property_debugger/profile_native_calls>`

If `true`, enables collection of profiling data from non-GDScript Godot
functions, such as engine class methods. Enabling this slows execution
while profiling further.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **debugger/profiler\_frame\_history\_size**
`🔗<class_EditorSettings_property_debugger/profiler_frame_history_size>`

The size of the profiler's frame history. The default value (3600)
allows seeing up to 60 seconds of profiling if the project renders at a
constant 60 FPS. Higher values allow viewing longer periods of profiling
in the graphs, especially when the project is running at high
framerates.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **debugger/profiler\_frame\_max\_functions**
`🔗<class_EditorSettings_property_debugger/profiler_frame_max_functions>`

The maximum number of script functions that can be displayed per frame
in the profiler. If there are more script functions called in a given
profiler frame, these functions will be discarded from the profiling
results entirely.

\*\*Note:\*\* This setting is only read when the profiler is first
started, so changing it during profiling will have no effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **debugger/profiler\_target\_fps**
`🔗<class_EditorSettings_property_debugger/profiler_target_fps>`

The target frame rate shown in the visual profiler graph, in frames per
second.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **debugger/remote\_inspect\_refresh\_interval**
`🔗<class_EditorSettings_property_debugger/remote_inspect_refresh_interval>`

The refresh interval for the remote inspector's properties (in seconds).
Lower values are more reactive, but may cause stuttering while the
project is running from the editor and the **Remote** scene tree is
selected in the Scene tree dock.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **debugger/remote\_scene\_tree\_refresh\_interval**
`🔗<class_EditorSettings_property_debugger/remote_scene_tree_refresh_interval>`

The refresh interval for the remote scene tree (in seconds). Lower
values are more reactive, but may cause stuttering while the project is
running from the editor and the **Remote** scene tree is selected in the
Scene tree dock.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **docks/filesystem/always\_show\_folders**
`🔗<class_EditorSettings_property_docks/filesystem/always_show_folders>`

If `true`, displays folders in the FileSystem dock's bottom pane when
split mode is enabled. If `false`, only files will be displayed in the
bottom pane. Split mode can be toggled by pressing the icon next to the
`res://` folder path.

\*\*Note:\*\* This setting has no effect when split mode is disabled
(which is the default).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **docks/filesystem/other\_file\_extensions**
`🔗<class_EditorSettings_property_docks/filesystem/other_file_extensions>`

A comma separated list of unsupported file extensions to show in the
FileSystem dock, e.g. `"ico,icns"`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **docks/filesystem/textfile\_extensions**
`🔗<class_EditorSettings_property_docks/filesystem/textfile_extensions>`

A comma separated list of file extensions to consider as editable text
files in the FileSystem dock (by double-clicking on the files), e.g.
`"txt,md,cfg,ini,log,json,yml,yaml,toml,xml"`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **docks/filesystem/thumbnail\_size**
`🔗<class_EditorSettings_property_docks/filesystem/thumbnail_size>`

The thumbnail size to use in the FileSystem dock (in pixels). See also
`filesystem/file_dialog/thumbnail_size<class_EditorSettings_property_filesystem/file_dialog/thumbnail_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **docks/property\_editor/auto\_refresh\_interval**
`🔗<class_EditorSettings_property_docks/property_editor/auto_refresh_interval>`

The refresh interval to use for the Inspector dock's properties. The
effect of this setting is mainly noticeable when adjusting gizmos in the
2D/3D editor and looking at the inspector at the same time. Lower values
make the inspector refresh more often, but take up more CPU time.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **docks/property\_editor/subresource\_hue\_tint**
`🔗<class_EditorSettings_property_docks/property_editor/subresource_hue_tint>`

The tint intensity to use for the subresources background in the
Inspector dock. The tint is used to distinguish between different
subresources in the inspector. Higher values result in a more noticeable
background color difference.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**docks/scene\_tree/ask\_before\_deleting\_related\_animation\_tracks**
`🔗<class_EditorSettings_property_docks/scene_tree/ask_before_deleting_related_animation_tracks>`

If `true`, when a node is deleted with animation tracks referencing it,
a confirmation dialog appears before the tracks are deleted. The dialog
will appear even when using the "Delete (No Confirm)" shortcut.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**docks/scene\_tree/ask\_before\_revoking\_unique\_name**
`🔗<class_EditorSettings_property_docks/scene_tree/ask_before_revoking_unique_name>`

If `true`, displays a confirmation dialog before left-clicking the
"percent" icon next to a node name in the Scene tree dock. When clicked,
this icon revokes the node's scene-unique name, which can impact the
behavior of scripts that rely on this scene-unique name due to
identifiers not being found anymore.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **docks/scene\_tree/auto\_expand\_to\_selected**
`🔗<class_EditorSettings_property_docks/scene_tree/auto_expand_to_selected>`

If `true`, the scene tree dock will automatically unfold nodes when a
node that has folded parents is selected.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **docks/scene\_tree/center\_node\_on\_reparent**
`🔗<class_EditorSettings_property_docks/scene_tree/center_node_on_reparent>`

If `true`, new node created when reparenting node(s) will be positioned
at the average position of the selected node(s).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**docks/scene\_tree/start\_create\_dialog\_fully\_expanded**
`🔗<class_EditorSettings_property_docks/scene_tree/start_create_dialog_fully_expanded>`

If `true`, the Create dialog (Create New Node/Create New Resource) will
start with all its sections expanded. Otherwise, sections will be
collapsed until the user starts searching (which will automatically
expand sections as needed).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/2d/bone\_color1**
`🔗<class_EditorSettings_property_editors/2d/bone_color1>`

The "start" stop of the color gradient to use for bones in the 2D
skeleton editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/2d/bone\_color2**
`🔗<class_EditorSettings_property_editors/2d/bone_color2>`

The "end" stop of the color gradient to use for bones in the 2D skeleton
editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/2d/bone\_ik\_color**
`🔗<class_EditorSettings_property_editors/2d/bone_ik_color>`

The color to use for inverse kinematics-enabled bones in the 2D skeleton
editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/2d/bone\_outline\_color**
`🔗<class_EditorSettings_property_editors/2d/bone_outline_color>`

The outline color to use for non-selected bones in the 2D skeleton
editor. See also
`editors/2d/bone_selected_color<class_EditorSettings_property_editors/2d/bone_selected_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/2d/bone\_outline\_size**
`🔗<class_EditorSettings_property_editors/2d/bone_outline_size>`

The outline size in the 2D skeleton editor (in pixels). See also
`editors/2d/bone_width<class_EditorSettings_property_editors/2d/bone_width>`.

\*\*Note:\*\* Changes to this value only apply after modifying a
`Bone2D<class_Bone2D>` node in any way, or closing and reopening the
scene.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/2d/bone\_selected\_color**
`🔗<class_EditorSettings_property_editors/2d/bone_selected_color>`

The color to use for selected bones in the 2D skeleton editor. See also
`editors/2d/bone_outline_color<class_EditorSettings_property_editors/2d/bone_outline_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/2d/bone\_width**
`🔗<class_EditorSettings_property_editors/2d/bone_width>`

The bone width in the 2D skeleton editor (in pixels). See also
`editors/2d/bone_outline_size<class_EditorSettings_property_editors/2d/bone_outline_size>`.

\*\*Note:\*\* Changes to this value only apply after modifying a
`Bone2D<class_Bone2D>` node in any way, or closing and reopening the
scene.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/2d/grid\_color**
`🔗<class_EditorSettings_property_editors/2d/grid_color>`

The grid color to use in the 2D editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/2d/guides\_color**
`🔗<class_EditorSettings_property_editors/2d/guides_color>`

The guides color to use in the 2D editor. Guides can be created by
dragging the mouse cursor from the rulers.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/2d/smart\_snapping\_line\_color**
`🔗<class_EditorSettings_property_editors/2d/smart_snapping_line_color>`

The color to use when drawing smart snapping lines in the 2D editor. The
smart snapping lines will automatically display when moving 2D nodes if
smart snapping is enabled in the Snapping Options menu at the top of the
2D editor viewport.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/2d/use\_integer\_zoom\_by\_default**
`🔗<class_EditorSettings_property_editors/2d/use_integer_zoom_by_default>`

If `true`, the 2D editor will snap to integer zoom values when not
holding the `Alt` key. If `false`, this behavior is swapped.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/2d/viewport\_border\_color**
`🔗<class_EditorSettings_property_editors/2d/viewport_border_color>`

The color of the viewport border in the 2D editor. This border
represents the viewport's size at the base resolution defined in the
Project Settings. Objects placed outside this border will not be visible
unless a `Camera2D<class_Camera2D>` node is used, or unless the window
is resized and the stretch mode is set to `disabled`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/2d/zoom\_speed\_factor**
`🔗<class_EditorSettings_property_editors/2d/zoom_speed_factor>`

The factor to use when zooming in or out in the 2D editor. For example,
`1.1` will zoom in by 10% with every step. If set to `2.0`, zooming will
only cycle through powers of two.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/3d/default\_fov**
`🔗<class_EditorSettings_property_editors/3d/default_fov>`

The default camera vertical field of view to use in the 3D editor (in
degrees). The camera field of view can be adjusted on a per-scene basis
using the **View** menu at the top of the 3D editor. If a scene had its
camera field of view adjusted using the **View** menu, this setting is
ignored in the scene in question. This setting is also ignored while a
`Camera3D<class_Camera3D>` node is being previewed in the editor.

\*\*Note:\*\* The editor camera always uses the **Keep Height** aspect
mode.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/3d/default\_z\_far**
`🔗<class_EditorSettings_property_editors/3d/default_z_far>`

The default camera far clip distance to use in the 3D editor (in
degrees). Higher values make it possible to view objects placed further
away from the camera, at the cost of lower precision in the depth buffer
(which can result in visible Z-fighting in the distance). The camera far
clip distance can be adjusted on a per-scene basis using the **View**
menu at the top of the 3D editor. If a scene had its camera far clip
distance adjusted using the **View** menu, this setting is ignored in
the scene in question. This setting is also ignored while a
`Camera3D<class_Camera3D>` node is being previewed in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/3d/default\_z\_near**
`🔗<class_EditorSettings_property_editors/3d/default_z_near>`

The default camera near clip distance to use in the 3D editor (in
degrees). Lower values make it possible to view objects placed closer to
the camera, at the cost of lower precision in the depth buffer (which
can result in visible Z-fighting in the distance). The camera near clip
distance can be adjusted on a per-scene basis using the **View** menu at
the top of the 3D editor. If a scene had its camera near clip distance
adjusted using the **View** menu, this setting is ignored in the scene
in question. This setting is also ignored while a
`Camera3D<class_Camera3D>` node is being previewed in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/freelook/freelook\_activation\_modifier**
`🔗<class_EditorSettings_property_editors/3d/freelook/freelook_activation_modifier>`

The modifier key to use to enable freelook in the 3D editor (on top of
pressing the right mouse button).

\*\*Note:\*\* Regardless of this setting, the freelook toggle keyboard
shortcut (`Shift + F` by default) is always available.

\*\*Note:\*\* On certain window managers on Linux, the `Alt` key will be
intercepted by the window manager when clicking a mouse button at the
same time. This means Godot will not see the modifier key as being
pressed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/3d/freelook/freelook\_base\_speed**
`🔗<class_EditorSettings_property_editors/3d/freelook/freelook_base_speed>`

The base 3D freelook speed in units per second. This can be adjusted by
using the mouse wheel while in freelook mode, or by holding down the
"fast" or "slow" modifier keys (`Shift` and `Alt` by default,
respectively).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/3d/freelook/freelook\_inertia**
`🔗<class_EditorSettings_property_editors/3d/freelook/freelook_inertia>`

The inertia of the 3D freelook camera. Higher values make the camera
start and stop slower, which looks smoother but adds latency.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/freelook/freelook\_navigation\_scheme**
`🔗<class_EditorSettings_property_editors/3d/freelook/freelook_navigation_scheme>`

The navigation scheme to use when freelook is enabled in the 3D editor.
Some of the navigation schemes below may be more convenient when
designing specific levels in the 3D editor.

-   **Default:** The "Freelook Forward", "Freelook Backward", "Freelook
    Up" and "Freelook Down" keys will move relative to the camera,
    taking its pitch angle into account for the movement.
-   **Partially Axis-Locked:** The "Freelook Forward" and "Freelook
    Backward" keys will move relative to the camera, taking its pitch
    angle into account for the movement. The "Freelook Up" and "Freelook
    Down" keys will move in an "absolute" manner, *not* taking the
    camera's pitch angle into account for the movement.
-   **Fully Axis-Locked:** The "Freelook Forward", "Freelook Backward",
    "Freelook Up" and "Freelook Down" keys will move in an "absolute"
    manner, *not* taking the camera's pitch angle into account for the
    movement.

See also
`editors/3d/navigation/navigation_scheme<class_EditorSettings_property_editors/3d/navigation/navigation_scheme>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/3d/freelook/freelook\_sensitivity**
`🔗<class_EditorSettings_property_editors/3d/freelook/freelook_sensitivity>`

The mouse sensitivity to use while freelook mode is active in the 3D
editor. See also
`editors/3d/navigation_feel/orbit_sensitivity<class_EditorSettings_property_editors/3d/navigation_feel/orbit_sensitivity>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/3d/freelook/freelook\_speed\_zoom\_link**
`🔗<class_EditorSettings_property_editors/3d/freelook/freelook_speed_zoom_link>`

If `true`, freelook speed is linked to the zoom value used in the camera
orbit mode in the 3D editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/3d/grid\_division\_level\_bias**
`🔗<class_EditorSettings_property_editors/3d/grid_division_level_bias>`

The grid division bias to use in the 3D editor. Negative values will
cause small grid divisions to appear earlier, whereas positive values
will cause small grid divisions to appear later.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/grid\_division\_level\_max**
`🔗<class_EditorSettings_property_editors/3d/grid_division_level_max>`

The largest grid division to use in the 3D editor. Together with
`editors/3d/primary_grid_steps<class_EditorSettings_property_editors/3d/primary_grid_steps>`,
this determines how large the grid divisions can be. The grid divisions
will not be able to get larger than
`primary_grid_steps ^ grid_division_level_max` units. By default, when
`editors/3d/primary_grid_steps<class_EditorSettings_property_editors/3d/primary_grid_steps>`
is `8`, this means grid divisions cannot get larger than `64` units each
(so primary grid lines are `512` units apart), no matter how far away
the camera is from the grid.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/grid\_division\_level\_min**
`🔗<class_EditorSettings_property_editors/3d/grid_division_level_min>`

The smallest grid division to use in the 3D editor. Together with
`editors/3d/primary_grid_steps<class_EditorSettings_property_editors/3d/primary_grid_steps>`,
this determines how small the grid divisions can be. The grid divisions
will not be able to get smaller than
`primary_grid_steps ^ grid_division_level_min` units. By default, this
means grid divisions cannot get smaller than 1 unit each, no matter how
close the camera is from the grid.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/grid\_size**
`🔗<class_EditorSettings_property_editors/3d/grid_size>`

The grid size in units. Higher values prevent the grid from appearing
"cut off" at certain angles, but make the grid more demanding to render.
Depending on the camera's position, the grid may not be fully visible
since a shader is used to fade it progressively.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/3d/grid\_xy\_plane**
`🔗<class_EditorSettings_property_editors/3d/grid_xy_plane>`

If `true`, renders the grid on the XY plane in perspective view. This
can be useful for 3D side-scrolling games.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/3d/grid\_xz\_plane**
`🔗<class_EditorSettings_property_editors/3d/grid_xz_plane>`

If `true`, renders the grid on the XZ plane in perspective view.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/3d/grid\_yz\_plane**
`🔗<class_EditorSettings_property_editors/3d/grid_yz_plane>`

If `true`, renders the grid on the YZ plane in perspective view. This
can be useful for 3D side-scrolling games.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/3d/manipulator\_gizmo\_opacity**
`🔗<class_EditorSettings_property_editors/3d/manipulator_gizmo_opacity>`

Opacity of the default gizmo for moving, rotating, and scaling 3D nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/manipulator\_gizmo\_size**
`🔗<class_EditorSettings_property_editors/3d/manipulator_gizmo_size>`

Size of the default gizmo for moving, rotating, and scaling 3D nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/3d/navigation/emulate\_3\_button\_mouse**
`🔗<class_EditorSettings_property_editors/3d/navigation/emulate_3_button_mouse>`

If `true`, enables 3-button mouse emulation mode. This is useful on
laptops when using a trackpad.

When 3-button mouse emulation mode is enabled, the pan, zoom and orbit
modifiers can always be used in the 3D editor viewport, even when not
holding down any mouse button.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/3d/navigation/emulate\_numpad**
`🔗<class_EditorSettings_property_editors/3d/navigation/emulate_numpad>`

If `true`, allows using the top row `0`-`9` keys to function as their
equivalent numpad keys for 3D editor navigation. This should be enabled
on keyboards that have no numeric keypad available.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/3d/navigation/invert\_x\_axis**
`🔗<class_EditorSettings_property_editors/3d/navigation/invert_x_axis>`

If `true`, invert the horizontal mouse axis when panning or orbiting in
the 3D editor. This setting does *not* apply to freelook mode.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/3d/navigation/invert\_y\_axis**
`🔗<class_EditorSettings_property_editors/3d/navigation/invert_y_axis>`

If `true`, invert the vertical mouse axis when panning, orbiting, or
using freelook mode in the 3D editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/navigation/navigation\_scheme**
`🔗<class_EditorSettings_property_editors/3d/navigation/navigation_scheme>`

The navigation scheme preset to use in the 3D editor. Changing this
setting will affect the mouse button and modifier controls used to
navigate the 3D editor viewport.

All schemes can use `Mouse wheel` to zoom.

-   **Godot:** `Middle mouse button` to orbit.
    `Shift + Middle mouse button` to pan.
    `Ctrl + Shift + Middle mouse button` to zoom.
-   **Maya:** `Alt + Left mouse button` to orbit. `Middle mouse button`
    to pan, `Shift + Middle mouse button` to pan 10 times faster.
    `Alt + Right mouse button` to zoom.
-   **Modo:** `Alt + Left mouse button` to orbit.
    `Alt + Shift + Left mouse button` to pan.
    `Ctrl + Alt + Left mouse button` to zoom.

See also
`editors/3d/navigation/orbit_mouse_button<class_EditorSettings_property_editors/3d/navigation/orbit_mouse_button>`,
`editors/3d/navigation/pan_mouse_button<class_EditorSettings_property_editors/3d/navigation/pan_mouse_button>`,
`editors/3d/navigation/zoom_mouse_button<class_EditorSettings_property_editors/3d/navigation/zoom_mouse_button>`,
and
`editors/3d/freelook/freelook_navigation_scheme<class_EditorSettings_property_editors/3d/freelook/freelook_navigation_scheme>`.

\*\*Note:\*\* On certain window managers on Linux, the `Alt` key will be
intercepted by the window manager when clicking a mouse button at the
same time. This means Godot will not see the modifier key as being
pressed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/navigation/orbit\_mouse\_button**
`🔗<class_EditorSettings_property_editors/3d/navigation/orbit_mouse_button>`

The mouse button that needs to be held down to orbit in the 3D editor
viewport.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/navigation/pan\_mouse\_button**
`🔗<class_EditorSettings_property_editors/3d/navigation/pan_mouse_button>`

The mouse button that needs to be held down to pan in the 3D editor
viewport.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**editors/3d/navigation/show\_viewport\_navigation\_gizmo**
`🔗<class_EditorSettings_property_editors/3d/navigation/show_viewport_navigation_gizmo>`

If `true`, shows gizmos for moving and rotating the camera in the bottom
corners of the 3D editor's viewport. Useful for devices that use touch
screen.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**editors/3d/navigation/show\_viewport\_rotation\_gizmo**
`🔗<class_EditorSettings_property_editors/3d/navigation/show_viewport_rotation_gizmo>`

If `true`, shows a small orientation gizmo in the top-right corner of
the 3D editor's viewports.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/3d/navigation/warped\_mouse\_panning**
`🔗<class_EditorSettings_property_editors/3d/navigation/warped_mouse_panning>`

If `true`, warps the mouse around the 3D viewport while panning in the
3D editor. This makes it possible to pan over a large area without
having to exit panning and adjust the mouse cursor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/navigation/zoom\_mouse\_button**
`🔗<class_EditorSettings_property_editors/3d/navigation/zoom_mouse_button>`

The mouse button that needs to be held down to zoom in the 3D editor
viewport.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/navigation/zoom\_style**
`🔗<class_EditorSettings_property_editors/3d/navigation/zoom_style>`

The mouse cursor movement direction to use when zooming by moving the
mouse. This does not affect zooming with the mouse wheel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/3d/navigation\_feel/orbit\_inertia**
`🔗<class_EditorSettings_property_editors/3d/navigation_feel/orbit_inertia>`

The inertia to use when orbiting in the 3D editor. Higher values make
the camera start and stop slower, which looks smoother but adds latency.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/3d/navigation\_feel/orbit\_sensitivity**
`🔗<class_EditorSettings_property_editors/3d/navigation_feel/orbit_sensitivity>`

The mouse sensitivity to use when orbiting in the 3D editor. See also
`editors/3d/freelook/freelook_sensitivity<class_EditorSettings_property_editors/3d/freelook/freelook_sensitivity>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>`
**editors/3d/navigation\_feel/translation\_inertia**
`🔗<class_EditorSettings_property_editors/3d/navigation_feel/translation_inertia>`

The inertia to use when panning in the 3D editor. Higher values make the
camera start and stop slower, which looks smoother but adds latency.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/3d/navigation\_feel/zoom\_inertia**
`🔗<class_EditorSettings_property_editors/3d/navigation_feel/zoom_inertia>`

The inertia to use when zooming in the 3D editor. Higher values make the
camera start and stop slower, which looks smoother but adds latency.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d/primary\_grid\_color**
`🔗<class_EditorSettings_property_editors/3d/primary_grid_color>`

The color to use for the primary 3D grid. The color's alpha channel
affects the grid's opacity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d/primary\_grid\_steps**
`🔗<class_EditorSettings_property_editors/3d/primary_grid_steps>`

If set above 0, where a primary grid line should be drawn. By default,
primary lines are configured to be more visible than secondary lines.
This helps with measurements in the 3D editor. See also
`editors/3d/primary_grid_color<class_EditorSettings_property_editors/3d/primary_grid_color>`
and
`editors/3d/secondary_grid_color<class_EditorSettings_property_editors/3d/secondary_grid_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d/secondary\_grid\_color**
`🔗<class_EditorSettings_property_editors/3d/secondary_grid_color>`

The color to use for the secondary 3D grid. This is generally a less
visible color than
`editors/3d/primary_grid_color<class_EditorSettings_property_editors/3d/primary_grid_color>`.
The color's alpha channel affects the grid's opacity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d/selection\_box\_color**
`🔗<class_EditorSettings_property_editors/3d/selection_box_color>`

The color to use for the selection box that surrounds selected nodes in
the 3D editor viewport. The color's alpha channel influences the
selection box's opacity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/aabb**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/aabb>`

The color to use for the AABB gizmo that displays the
`GeometryInstance3D<class_GeometryInstance3D>`'s custom
`AABB<class_AABB>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/camera**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/camera>`

The 3D editor gizmo color for `Camera3D<class_Camera3D>`s.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/csg**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/csg>`

The 3D editor gizmo color for CSG nodes (such as
`CSGShape3D<class_CSGShape3D>` or `CSGBox3D<class_CSGBox3D>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/decal**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/decal>`

The 3D editor gizmo color for `Decal<class_Decal>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/fog\_volume**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/fog_volume>`

The 3D editor gizmo color for `FogVolume<class_FogVolume>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/instantiated**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/instantiated>`

The color override to use for 3D editor gizmos if the
`Node3D<class_Node3D>` in question is part of an instantiated scene file
(from the perspective of the current scene).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/joint**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/joint>`

The 3D editor gizmo color for `Joint3D<class_Joint3D>`s and
`PhysicalBone3D<class_PhysicalBone3D>`s.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/joint\_body\_a**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/joint_body_a>`

Color for representing `Joint3D.node_a<class_Joint3D_property_node_a>`
for some `Joint3D<class_Joint3D>` types.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/joint\_body\_b**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/joint_body_b>`

Color for representing `Joint3D.node_b<class_Joint3D_property_node_b>`
for some `Joint3D<class_Joint3D>` types.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/3d\_gizmos/gizmo\_colors/lightmap\_lines**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/lightmap_lines>`

Color of lines displayed in baked `LightmapGI<class_LightmapGI>` node's
grid.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/3d\_gizmos/gizmo\_colors/lightprobe\_lines**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/lightprobe_lines>`

The 3D editor gizmo color used for `LightmapProbe<class_LightmapProbe>`
nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/occluder**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/occluder>`

The 3D editor gizmo color used for
`OccluderInstance3D<class_OccluderInstance3D>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/3d\_gizmos/gizmo\_colors/particle\_attractor**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/particle_attractor>`

The 3D editor gizmo color used for
`GPUParticlesAttractor3D<class_GPUParticlesAttractor3D>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/3d\_gizmos/gizmo\_colors/particle\_collision**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/particle_collision>`

The 3D editor gizmo color used for
`GPUParticlesCollision3D<class_GPUParticlesCollision3D>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/particles**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/particles>`

The 3D editor gizmo color used for
`CPUParticles3D<class_CPUParticles3D>` and
`GPUParticles3D<class_GPUParticles3D>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/path\_tilt**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/path_tilt>`

The 3D editor gizmo color used for `Path3D<class_Path3D>` tilt circles,
which indicate the direction the `Curve3D<class_Curve3D>` is tilted
towards.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/3d\_gizmos/gizmo\_colors/reflection\_probe**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/reflection_probe>`

The 3D editor gizmo color used for
`ReflectionProbe<class_ReflectionProbe>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/selected\_bone**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/selected_bone>`

The 3D editor gizmo color used for the currently selected
`Skeleton3D<class_Skeleton3D>` bone.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/skeleton**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/skeleton>`

The 3D editor gizmo color used for `Skeleton3D<class_Skeleton3D>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/3d\_gizmos/gizmo\_colors/stream\_player\_3d**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/stream_player_3d>`

The 3D editor gizmo color used for
`AudioStreamPlayer3D<class_AudioStreamPlayer3D>`'s emission angle.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/3d\_gizmos/gizmo\_colors/visibility\_notifier**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/visibility_notifier>`

The 3D editor gizmo color used for
`VisibleOnScreenNotifier3D<class_VisibleOnScreenNotifier3D>` and
`VisibleOnScreenEnabler3D<class_VisibleOnScreenEnabler3D>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/3d\_gizmos/gizmo\_colors/voxel\_gi**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_colors/voxel_gi>`

The 3D editor gizmo color used for `VoxelGI<class_VoxelGI>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>`
**editors/3d\_gizmos/gizmo\_settings/bone\_axis\_length**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_settings/bone_axis_length>`

The length of `Skeleton3D<class_Skeleton3D>` bone gizmos in the 3D
editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/3d\_gizmos/gizmo\_settings/bone\_shape**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_settings/bone_shape>`

The shape of `Skeleton3D<class_Skeleton3D>` bone gizmos in the 3D
editor. **Wire** is a thin line, while **Octahedron** is a set of lines
that represent a thicker hollow line pointing in a specific direction
(similar to most 3D animation software).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>`
**editors/3d\_gizmos/gizmo\_settings/path3d\_tilt\_disk\_size**
`🔗<class_EditorSettings_property_editors/3d_gizmos/gizmo_settings/path3d_tilt_disk_size>`

Size of the disk gizmo displayed when editing `Path3D<class_Path3D>`'s
tilt handles.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/animation/autorename\_animation\_tracks**
`🔗<class_EditorSettings_property_editors/animation/autorename_animation_tracks>`

If `true`, automatically updates animation tracks' target paths when
renaming or reparenting nodes in the Scene tree dock.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/animation/confirm\_insert\_track**
`🔗<class_EditorSettings_property_editors/animation/confirm_insert_track>`

If `true`, display a confirmation dialog when adding a new track to an
animation by pressing the "key" icon next to a property. Holding Shift
will bypass the dialog.

If `false`, the behavior is reversed, i.e. the dialog only appears when
Shift is held.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/animation/default\_create\_bezier\_tracks**
`🔗<class_EditorSettings_property_editors/animation/default_create_bezier_tracks>`

If `true`, create a Bezier track instead of a standard track when
pressing the "key" icon next to a property. Bezier tracks provide more
control over animation curves, but are more difficult to adjust quickly.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/animation/default\_create\_reset\_tracks**
`🔗<class_EditorSettings_property_editors/animation/default_create_reset_tracks>`

If `true`, create a `RESET` track when creating a new animation track.
This track can be used to restore the animation to a "default" state.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/animation/onion\_layers\_future\_color**
`🔗<class_EditorSettings_property_editors/animation/onion_layers_future_color>`

The modulate color to use for "future" frames displayed in the animation
editor's onion skinning feature.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/animation/onion\_layers\_past\_color**
`🔗<class_EditorSettings_property_editors/animation/onion_layers_past_color>`

The modulate color to use for "past" frames displayed in the animation
editor's onion skinning feature.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/bone\_mapper/handle\_colors/error**
`🔗<class_EditorSettings_property_editors/bone_mapper/handle_colors/error>`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/bone\_mapper/handle\_colors/missing**
`🔗<class_EditorSettings_property_editors/bone_mapper/handle_colors/missing>`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/bone\_mapper/handle\_colors/set**
`🔗<class_EditorSettings_property_editors/bone_mapper/handle_colors/set>`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/bone\_mapper/handle\_colors/unset**
`🔗<class_EditorSettings_property_editors/bone_mapper/handle_colors/unset>`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/grid\_map/editor\_side**
`🔗<class_EditorSettings_property_editors/grid_map/editor_side>`

Specifies the side of 3D editor's viewport where GridMap's mesh palette
will appear.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/grid\_map/palette\_min\_width**
`🔗<class_EditorSettings_property_editors/grid_map/palette_min_width>`

Minimum width of GridMap's mesh palette side panel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/grid\_map/pick\_distance**
`🔗<class_EditorSettings_property_editors/grid_map/pick_distance>`

The maximum distance at which tiles can be placed on a GridMap, relative
to the camera position (in 3D units).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/grid\_map/preview\_size**
`🔗<class_EditorSettings_property_editors/grid_map/preview_size>`

Texture size of mesh previews generated for GridMap's MeshLibrary.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/panning/2d\_editor\_pan\_speed**
`🔗<class_EditorSettings_property_editors/panning/2d_editor_pan_speed>`

The panning speed when using the mouse wheel or touchscreen events in
the 2D editor. This setting does not apply to panning by holding down
the middle or right mouse buttons.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/panning/2d\_editor\_panning\_scheme**
`🔗<class_EditorSettings_property_editors/panning/2d_editor_panning_scheme>`

Controls whether the mouse wheel scroll zooms or pans in the 2D editor.
See also
`editors/panning/sub_editors_panning_scheme<class_EditorSettings_property_editors/panning/sub_editors_panning_scheme>`
and
`editors/panning/animation_editors_panning_scheme<class_EditorSettings_property_editors/panning/animation_editors_panning_scheme>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/panning/animation\_editors\_panning\_scheme**
`🔗<class_EditorSettings_property_editors/panning/animation_editors_panning_scheme>`

Controls whether the mouse wheel scroll zooms or pans in the animation
track and Bezier editors. See also
`editors/panning/2d_editor_panning_scheme<class_EditorSettings_property_editors/panning/2d_editor_panning_scheme>`
and
`editors/panning/sub_editors_panning_scheme<class_EditorSettings_property_editors/panning/sub_editors_panning_scheme>`
(which controls the animation blend tree editor's pan behavior).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/panning/simple\_panning**
`🔗<class_EditorSettings_property_editors/panning/simple_panning>`

If `true`, allows panning by holding down `Space` in the 2D editor
viewport (in addition to panning with the middle or right mouse
buttons). If `false`, the left mouse button must be held down while
holding down `Space` to pan in the 2D editor viewport.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/panning/sub\_editors\_panning\_scheme**
`🔗<class_EditorSettings_property_editors/panning/sub_editors_panning_scheme>`

Controls whether the mouse wheel scroll zooms or pans in subeditors. The
list of affected subeditors is: animation blend tree editor,
`Polygon2D<class_Polygon2D>` editor, tileset editor, texture region
editor and visual shader editor. See also
`editors/panning/2d_editor_panning_scheme<class_EditorSettings_property_editors/panning/2d_editor_panning_scheme>`
and
`editors/panning/animation_editors_panning_scheme<class_EditorSettings_property_editors/panning/animation_editors_panning_scheme>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/panning/warped\_mouse\_panning**
`🔗<class_EditorSettings_property_editors/panning/warped_mouse_panning>`

If `true`, warps the mouse around the 2D viewport while panning in the
2D editor. This makes it possible to pan over a large area without
having to exit panning and adjust the mouse cursor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/polygon\_editor/auto\_bake\_delay**
`🔗<class_EditorSettings_property_editors/polygon_editor/auto_bake_delay>`

The delay in seconds until more complex and performance costly polygon
editors commit their outlines, e.g. the 2D navigation polygon editor
rebakes the navigation mesh polygons. A negative value stops the auto
bake.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/polygon\_editor/point\_grab\_radius**
`🔗<class_EditorSettings_property_editors/polygon_editor/point_grab_radius>`

The radius in which points can be selected in the
`Polygon2D<class_Polygon2D>` and
`CollisionPolygon2D<class_CollisionPolygon2D>` editors (in pixels).
Higher values make it easier to select points quickly, but can make it
more difficult to select the expected point when several points are
located close to each other.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/polygon\_editor/show\_previous\_outline**
`🔗<class_EditorSettings_property_editors/polygon_editor/show_previous_outline>`

If `true`, displays the polygon's previous shape in the 2D polygon
editors with an opaque gray outline. This outline is displayed while
dragging a point until the left mouse button is released.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**editors/shader\_editor/behavior/files/restore\_shaders\_on\_load**
`🔗<class_EditorSettings_property_editors/shader_editor/behavior/files/restore_shaders_on_load>`

If `true`, reopens shader files that were open in the shader editor when
the project was last closed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/tiles\_editor/display\_grid**
`🔗<class_EditorSettings_property_editors/tiles_editor/display_grid>`

If `true`, displays a grid while the TileMap editor is active. See also
`editors/tiles_editor/grid_color<class_EditorSettings_property_editors/tiles_editor/grid_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **editors/tiles\_editor/grid\_color**
`🔗<class_EditorSettings_property_editors/tiles_editor/grid_color>`

The color to use for the TileMap editor's grid.

\*\*Note:\*\* Only effective if
`editors/tiles_editor/display_grid<class_EditorSettings_property_editors/tiles_editor/display_grid>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editors/tiles\_editor/highlight\_selected\_layer**
`🔗<class_EditorSettings_property_editors/tiles_editor/highlight_selected_layer>`

Highlight the currently selected TileMapLayer by dimming the other ones
in the scene.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/category\_colors/color\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/category_colors/color_color>`

The color of a graph node's header when it belongs to the "Color"
category.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/category\_colors/conditional\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/category_colors/conditional_color>`

The color of a graph node's header when it belongs to the "Conditional"
category.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/category\_colors/input\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/category_colors/input_color>`

The color of a graph node's header when it belongs to the "Input"
category.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/category\_colors/output\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/category_colors/output_color>`

The color of a graph node's header when it belongs to the "Output"
category.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/category\_colors/particle\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/category_colors/particle_color>`

The color of a graph node's header when it belongs to the "Particle"
category.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/category\_colors/scalar\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/category_colors/scalar_color>`

The color of a graph node's header when it belongs to the "Scalar"
category.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/category\_colors/special\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/category_colors/special_color>`

The color of a graph node's header when it belongs to the "Special"
category.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/category\_colors/textures\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/category_colors/textures_color>`

The color of a graph node's header when it belongs to the "Textures"
category.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/category\_colors/transform\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/category_colors/transform_color>`

The color of a graph node's header when it belongs to the "Transform"
category.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/category\_colors/utility\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/category_colors/utility_color>`

The color of a graph node's header when it belongs to the "Utility"
category.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/category\_colors/vector\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/category_colors/vector_color>`

The color of a graph node's header when it belongs to the "Vector"
category.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **editors/visual\_editors/color\_theme**
`🔗<class_EditorSettings_property_editors/visual_editors/color_theme>`

The color theme to use in the visual shader editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/connection\_colors/boolean\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/connection_colors/boolean_color>`

The color of a port/connection of boolean type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/connection\_colors/sampler\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/connection_colors/sampler_color>`

The color of a port/connection of sampler type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/connection\_colors/scalar\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/connection_colors/scalar_color>`

The color of a port/connection of scalar type (float, int, unsigned
int).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/connection\_colors/transform\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/connection_colors/transform_color>`

The color of a port/connection of transform type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/connection\_colors/vector2\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/connection_colors/vector2_color>`

The color of a port/connection of Vector2 type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/connection\_colors/vector3\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/connection_colors/vector3_color>`

The color of a port/connection of Vector3 type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**editors/visual\_editors/connection\_colors/vector4\_color**
`🔗<class_EditorSettings_property_editors/visual_editors/connection_colors/vector4_color>`

The color of a port/connection of Vector4 type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **editors/visual\_editors/grid\_pattern**
`🔗<class_EditorSettings_property_editors/visual_editors/grid_pattern>`

The pattern used for the background grid.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/visual\_editors/lines\_curvature**
`🔗<class_EditorSettings_property_editors/visual_editors/lines_curvature>`

The curvature to use for connection lines in the visual shader editor.
Higher values will make connection lines appear more curved, with values
above `0.5` resulting in more "angular" turns in the middle of
connection lines.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **editors/visual\_editors/minimap\_opacity**
`🔗<class_EditorSettings_property_editors/visual_editors/minimap_opacity>`

The opacity of the minimap displayed in the bottom-right corner of the
visual shader editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>`
**editors/visual\_editors/visual\_shader/port\_preview\_size**
`🔗<class_EditorSettings_property_editors/visual_editors/visual_shader/port_preview_size>`

The size to use for port previews in the visual shader uniforms (toggled
by clicking the "eye" icon next to an output). The value is defined in
pixels at 100% zoom, and will scale with zoom automatically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **export/ssh/scp**
`🔗<class_EditorSettings_property_export/ssh/scp>`

Path to the SCP (secure copy) executable (used for remote deploy to
desktop platforms). If left empty, the editor will attempt to run `scp`
from `PATH`.

\*\*Note:\*\* SCP is not the same as SFTP. Specifying the SFTP
executable here will not work.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **export/ssh/ssh**
`🔗<class_EditorSettings_property_export/ssh/ssh>`

Path to the SSH executable (used for remote deploy to desktop
platforms). If left empty, the editor will attempt to run `ssh` from
`PATH`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>`
**filesystem/directories/autoscan\_project\_path**
`🔗<class_EditorSettings_property_filesystem/directories/autoscan_project_path>`

The folder where projects should be scanned for (recursively), in a way
similar to the project manager's **Scan** button. This can be set to the
same value as
`filesystem/directories/default_project_path<class_EditorSettings_property_filesystem/directories/default_project_path>`
for convenience.

\*\*Note:\*\* Setting this path to a folder with very large amounts of
files/folders can slow down the project manager startup significantly.
To keep the project manager quick to start up, it is recommended to set
this value to a folder as "specific" as possible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **filesystem/directories/default\_project\_path**
`🔗<class_EditorSettings_property_filesystem/directories/default_project_path>`

The folder where new projects should be created by default when clicking
the project manager's **New Project** button. This can be set to the
same value as
`filesystem/directories/autoscan_project_path<class_EditorSettings_property_filesystem/directories/autoscan_project_path>`
for convenience.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>`
**filesystem/external\_programs/3d\_model\_editor**
`🔗<class_EditorSettings_property_filesystem/external_programs/3d_model_editor>`

The program that opens 3D model scene files when clicking "Open in
External Program" option in Filesystem Dock. If not specified, the file
will be opened in the system's default program.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **filesystem/external\_programs/audio\_editor**
`🔗<class_EditorSettings_property_filesystem/external_programs/audio_editor>`

The program that opens audio files when clicking "Open in External
Program" option in Filesystem Dock. If not specified, the file will be
opened in the system's default program.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>`
**filesystem/external\_programs/raster\_image\_editor**
`🔗<class_EditorSettings_property_filesystem/external_programs/raster_image_editor>`

The program that opens raster image files when clicking "Open in
External Program" option in Filesystem Dock. If not specified, the file
will be opened in the system's default program.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>`
**filesystem/external\_programs/terminal\_emulator**
`🔗<class_EditorSettings_property_filesystem/external_programs/terminal_emulator>`

The terminal emulator program to use when using **Open in Terminal**
context menu action in the FileSystem dock. You can enter an absolute
path to a program binary, or a path to a program that is present in the
`PATH` environment variable.

If left empty, Godot will use the default terminal emulator for the
system:

-   **Windows:** PowerShell
-   **macOS:** Terminal.app
-   **Linux:** The first terminal found on the system in this order:
    gnome-terminal, konsole, xfce4-terminal, lxterminal, kitty,
    alacritty, urxvt, xterm.

To use Command Prompt (cmd) instead of PowerShell on Windows, enter
`cmd` in this field and the correct flags will automatically be used.

On macOS, make sure to point to the actual program binary located within
the `Programs/MacOS` folder of the .app bundle, rather than the .app
bundle directory.

If specifying a custom terminal emulator, you may need to override
`filesystem/external_programs/terminal_emulator_flags<class_EditorSettings_property_filesystem/external_programs/terminal_emulator_flags>`
so it opens in the correct folder.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>`
**filesystem/external\_programs/terminal\_emulator\_flags**
`🔗<class_EditorSettings_property_filesystem/external_programs/terminal_emulator_flags>`

The command-line arguments to pass to the terminal emulator that is run
when using **Open in Terminal** context menu action in the FileSystem
dock. See also
`filesystem/external_programs/terminal_emulator<class_EditorSettings_property_filesystem/external_programs/terminal_emulator>`.

If left empty, the default flags are `{directory}`, which is replaced by
the absolute path to the directory that is being opened in the terminal.

\*\*Note:\*\* If the terminal emulator is set to PowerShell, cmd, or
Konsole, Godot will automatically prepend arguments to this list, as
these terminals require nonstandard arguments to open in the correct
folder.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>`
**filesystem/external\_programs/vector\_image\_editor**
`🔗<class_EditorSettings_property_filesystem/external_programs/vector_image_editor>`

The program that opens vector image files when clicking "Open in
External Program" option in Filesystem Dock. If not specified, the file
will be opened in the system's default program.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **filesystem/file\_dialog/display\_mode**
`🔗<class_EditorSettings_property_filesystem/file_dialog/display_mode>`

The display mode to use in the editor's file dialogs.

-   **Thumbnails** takes more space, but displays dynamic resource
    thumbnails, making resources easier to preview without having to
    open them.
-   **List** is more compact but doesn't display dynamic resource
    thumbnails. Instead, it displays static icons based on the file
    extension.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **filesystem/file\_dialog/show\_hidden\_files**
`🔗<class_EditorSettings_property_filesystem/file_dialog/show_hidden_files>`

If `true`, display hidden files in the editor's file dialogs. Files that
have names starting with `.` are considered hidden (e.g.
`.hidden_file`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **filesystem/file\_dialog/thumbnail\_size**
`🔗<class_EditorSettings_property_filesystem/file_dialog/thumbnail_size>`

The thumbnail size to use in the editor's file dialogs (in pixels). See
also
`docks/filesystem/thumbnail_size<class_EditorSettings_property_docks/filesystem/thumbnail_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **filesystem/file\_server/password**
`🔗<class_EditorSettings_property_filesystem/file_server/password>`

Password used for file server when exporting project with remote file
system.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **filesystem/file\_server/port**
`🔗<class_EditorSettings_property_filesystem/file_server/port>`

Port used for file server when exporting project with remote file
system.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **filesystem/import/blender/blender\_path**
`🔗<class_EditorSettings_property_filesystem/import/blender/blender_path>`

The path to the directory containing the Blender executable used for
converting the Blender 3D scene files `.blend` to glTF 2.0 format during
import. Blender 3.0 or later is required.

To enable this feature for your specific project, use
`ProjectSettings.filesystem/import/blender/enabled<class_ProjectSettings_property_filesystem/import/blender/enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **filesystem/import/blender/rpc\_port**
`🔗<class_EditorSettings_property_filesystem/import/blender/rpc_port>`

The port number used for Remote Procedure Call (RPC) communication with
Godot's created process of the blender executable.

Setting this to 0 effectively disables communication with Godot and the
blender process, making performance slower.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **filesystem/import/blender/rpc\_server\_uptime**
`🔗<class_EditorSettings_property_filesystem/import/blender/rpc_server_uptime>`

The maximum idle uptime (in seconds) of the Blender process.

This prevents Godot from having to create a new process for each import
within the given seconds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **filesystem/import/fbx/fbx2gltf\_path**
`🔗<class_EditorSettings_property_filesystem/import/fbx/fbx2gltf_path>`

The path to the FBX2glTF executable used for converting Autodesk FBX 3D
scene files `.fbx` to glTF 2.0 format during import.

To enable this feature for your specific project, use
`ProjectSettings.filesystem/import/fbx2gltf/enabled<class_ProjectSettings_property_filesystem/import/fbx2gltf/enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **filesystem/on\_save/compress\_binary\_resources**
`🔗<class_EditorSettings_property_filesystem/on_save/compress_binary_resources>`

If `true`, uses lossless compression for binary resources.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**filesystem/on\_save/safe\_save\_on\_backup\_then\_rename**
`🔗<class_EditorSettings_property_filesystem/on_save/safe_save_on_backup_then_rename>`

If `true`, when saving a file, the editor will rename the old file to a
different name, save a new file, then only remove the old file once the
new file has been saved. This makes loss of data less likely to happen
if the editor or operating system exits unexpectedly while saving (e.g.
due to a crash or power outage).

\*\*Note:\*\* On Windows, this feature can interact negatively with
certain antivirus programs. In this case, you may have to set this to
`false` to prevent file locking issues.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>`
**filesystem/quick\_open\_dialog/default\_display\_mode**
`🔗<class_EditorSettings_property_filesystem/quick_open_dialog/default_display_mode>`

If set to `Adaptive`, the dialog opens in list view or grid view
depending on the requested type. If set to `Last Used`, the display mode
will always open the way you last used it.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **filesystem/quick\_open\_dialog/include\_addons**
`🔗<class_EditorSettings_property_filesystem/quick_open_dialog/include_addons>`

If `true`, results will include files located in the `addons` folder.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **filesystem/tools/oidn/oidn\_denoise\_path**
`🔗<class_EditorSettings_property_filesystem/tools/oidn/oidn_denoise_path>`

The path to the directory containing the Open Image Denoise (OIDN)
executable, used optionally for denoising lightmaps. It can be
downloaded from
[openimagedenoise.org](https://www.openimagedenoise.org/downloads.html).

To enable this feature for your specific project, use
`ProjectSettings.rendering/lightmapping/denoising/denoiser<class_ProjectSettings_property_rendering/lightmapping/denoising/denoiser>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **input/buffering/agile\_event\_flushing**
`🔗<class_EditorSettings_property_input/buffering/agile_event_flushing>`

If `true`, input events will be flushed just before every idle and
physics frame.

If `false`, these events will be flushed only once per process frame,
between iterations of the engine.

Enabling this setting can greatly improve input responsiveness,
especially in devices that struggle to run at the project's intended
frame rate.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **input/buffering/use\_accumulated\_input**
`🔗<class_EditorSettings_property_input/buffering/use_accumulated_input>`

If `true`, similar input events sent by the operating system are
accumulated. When input accumulation is enabled, all input events
generated during a frame will be merged and emitted when the frame is
done rendering. Therefore, this limits the number of input method calls
per second to the rendering FPS.

Input accumulation can be disabled to get slightly more precise/reactive
input at the cost of increased CPU usage.

\*\*Note:\*\* Input accumulation is *enabled* by default.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>`
**interface/editor/accept\_dialog\_cancel\_ok\_buttons**
`🔗<class_EditorSettings_property_interface/editor/accept_dialog_cancel_ok_buttons>`

How to position the Cancel and OK buttons in the editor's
`AcceptDialog<class_AcceptDialog>`s. Different platforms have different
standard behaviors for this, which can be overridden using this setting.
This is useful if you use Godot both on Windows and macOS/Linux and your
Godot muscle memory is stronger than your OS specific one.

-   **Auto** follows the platform convention: Cancel first on macOS and
    Linux, OK first on Windows.
-   **Cancel First** forces the ordering Cancel/OK.
-   **OK First** forces the ordering OK/Cancel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/automatically\_open\_screenshots**
`🔗<class_EditorSettings_property_interface/editor/automatically_open_screenshots>`

If `true`, automatically opens screenshots with the default program
associated to `.png` files after a screenshot is taken using the
**Editor &gt; Take Screenshot** action.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **interface/editor/code\_font**
`🔗<class_EditorSettings_property_interface/editor/code_font>`

The font to use for the script editor. Must be a resource of a
`Font<class_Font>` type such as a `.ttf` or `.otf` font file.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/code\_font\_contextual\_ligatures**
`🔗<class_EditorSettings_property_interface/editor/code_font_contextual_ligatures>`

The font ligatures to enable for the currently configured code font. Not
all fonts include support for ligatures.

\*\*Note:\*\* The default editor code font ([JetBrains
Mono](https://www.jetbrains.com/lp/mono/)) has contextual ligatures in
its font file.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>`
**interface/editor/code\_font\_custom\_opentype\_features**
`🔗<class_EditorSettings_property_interface/editor/code_font_custom_opentype_features>`

List of custom OpenType features to use, if supported by the currently
configured code font. Not all fonts include support for custom OpenType
features. The string should follow the OpenType specification.

\*\*Note:\*\* The default editor code font ([JetBrains
Mono](https://www.jetbrains.com/lp/mono/)) has custom OpenType features
in its font file, but there is no documented list yet.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>`
**interface/editor/code\_font\_custom\_variations**
`🔗<class_EditorSettings_property_interface/editor/code_font_custom_variations>`

List of alternative characters to use, if supported by the currently
configured code font. Not all fonts include support for custom
variations. The string should follow the OpenType specification.

\*\*Note:\*\* The default editor code font ([JetBrains
Mono](https://www.jetbrains.com/lp/mono/)) has alternate characters in
its font file, but there is no documented list yet.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/code\_font\_size**
`🔗<class_EditorSettings_property_interface/editor/code_font_size>`

The size of the font in the script editor. This setting does not impact
the font size of the Output panel (see
`run/output/font_size<class_EditorSettings_property_run/output/font_size>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **interface/editor/custom\_display\_scale**
`🔗<class_EditorSettings_property_interface/editor/custom_display_scale>`

The custom editor scale factor to use. This can be used for displays
with very high DPI where a scale factor of 200% is not sufficient.

\*\*Note:\*\* Only effective if
`interface/editor/display_scale<class_EditorSettings_property_interface/editor/display_scale>`
is set to **Custom**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/display\_scale**
`🔗<class_EditorSettings_property_interface/editor/display_scale>`

The display scale factor to use for the editor interface. Higher values
are more suited to hiDPI/Retina displays.

If set to **Auto**, the editor scale is automatically determined based
on the screen resolution and reported display DPI. This heuristic is not
always ideal, which means you can get better results by setting the
editor scale manually.

If set to **Custom**, the scaling value in
`interface/editor/custom_display_scale<class_EditorSettings_property_interface/editor/custom_display_scale>`
will be used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/dock\_tab\_style**
`🔗<class_EditorSettings_property_interface/editor/dock_tab_style>`

Tab style of editor docks.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **interface/editor/editor\_language**
`🔗<class_EditorSettings_property_interface/editor/editor_language>`

The language to use for the editor interface.

Translations are provided by the community. If you spot a mistake,
`contribute to editor translations on Weblate! <../contributing/documentation/editor_and_docs_localization>`

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/editor\_screen**
`🔗<class_EditorSettings_property_interface/editor/editor_screen>`

The preferred monitor to display the editor. If **Auto**, the editor
will remember the last screen it was displayed on across restarts.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/expand\_to\_title**
`🔗<class_EditorSettings_property_interface/editor/expand_to_title>`

Expanding main editor window content to the title, if supported by
`DisplayServer<class_DisplayServer>`. See
`DisplayServer.WINDOW_FLAG_EXTEND_TO_TITLE<class_DisplayServer_constant_WINDOW_FLAG_EXTEND_TO_TITLE>`.

Specific to the macOS platform.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/font\_allow\_msdf**
`🔗<class_EditorSettings_property_interface/editor/font_allow_msdf>`

If set to `true`, MSDF font rendering will be used for the visual shader
graph editor. You may need to set this to `false` when using a custom
main font, as some fonts will look broken due to the use of
self-intersecting outlines in their font data. Downloading the font from
the font maker's official website as opposed to a service like Google
Fonts can help resolve this issue.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/font\_antialiasing**
`🔗<class_EditorSettings_property_interface/editor/font_antialiasing>`

FreeType's font anti-aliasing mode used to render the editor fonts. Most
fonts are not designed to look good with anti-aliasing disabled, so it's
recommended to leave this enabled unless you're using a pixel art font.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/font\_disable\_embedded\_bitmaps**
`🔗<class_EditorSettings_property_interface/editor/font_disable_embedded_bitmaps>`

If set to `true`, embedded font bitmap loading is disabled (bitmap-only
and color fonts ignore this property).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/font\_hinting**
`🔗<class_EditorSettings_property_interface/editor/font_hinting>`

The font hinting mode to use for the editor fonts. FreeType supports the
following font hinting modes:

-   **None:** Don't use font hinting when rasterizing the font. This
    results in a smooth font, but it can look blurry.
-   **Light:** Use hinting on the X axis only. This is a compromise
    between font sharpness and smoothness.
-   **Normal:** Use hinting on both X and Y axes. This results in a
    sharp font, but it doesn't look very smooth.

If set to **Auto**, the font hinting mode will be set to match the
current operating system in use. This means the **Light** hinting mode
will be used on Windows and Linux, and the **None** hinting mode will be
used on macOS.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/font\_subpixel\_positioning**
`🔗<class_EditorSettings_property_interface/editor/font_subpixel_positioning>`

The subpixel positioning mode to use when rendering editor font glyphs.
This affects both the main and code fonts. **Disabled** is the fastest
to render and uses the least memory. **Auto** only uses subpixel
positioning for small font sizes (where the benefit is the most
noticeable). **One Half of a Pixel** and **One Quarter of a Pixel**
force the same subpixel positioning mode for all editor fonts,
regardless of their size (with **One Quarter of a Pixel** being the
highest-quality option).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/editor/import\_resources\_when\_unfocused**
`🔗<class_EditorSettings_property_interface/editor/import_resources_when_unfocused>`

If `true`, (re)imports resources even if the editor window is unfocused
or minimized. If `false`, resources are only (re)imported when the
editor window is focused. This can be set to `true` to speed up
iteration by starting the import process earlier when saving files in
the project folder. This also allows getting visual feedback on changes
without having to click the editor window, which is useful with
multi-monitor setups. The downside of setting this to `true` is that it
increases idle CPU usage and may steal CPU time from other applications
when importing resources.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/keep\_screen\_on**
`🔗<class_EditorSettings_property_interface/editor/keep_screen_on>`

If `true`, keeps the screen on (even in case of inactivity), so the
screensaver does not take over. Works on desktop and mobile platforms.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/localize\_settings**
`🔗<class_EditorSettings_property_interface/editor/localize_settings>`

If `true`, setting names in the editor are localized when possible.

\*\*Note:\*\* This setting affects most
`EditorInspector<class_EditorInspector>`s in the editor UI, primarily
Project Settings and Editor Settings. To control names displayed in the
Inspector dock, use
`interface/inspector/default_property_name_style<class_EditorSettings_property_interface/inspector/default_property_name_style>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/low\_processor\_mode\_sleep\_usec**
`🔗<class_EditorSettings_property_interface/editor/low_processor_mode_sleep_usec>`

The amount of sleeping between frames when the low-processor usage mode
is enabled (in microseconds). Higher values will result in lower CPU/GPU
usage, which can improve battery life on laptops. However, higher values
will result in a less responsive editor. The default value is set to
allow for maximum smoothness on monitors up to 144 Hz. See also
`interface/editor/unfocused_low_processor_mode_sleep_usec<class_EditorSettings_property_interface/editor/unfocused_low_processor_mode_sleep_usec>`.

\*\*Note:\*\* This setting is ignored if
`interface/editor/update_continuously<class_EditorSettings_property_interface/editor/update_continuously>`
is `true`, as enabling that setting disables low-processor mode.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **interface/editor/main\_font**
`🔗<class_EditorSettings_property_interface/editor/main_font>`

The font to use for the editor interface. Must be a resource of a
`Font<class_Font>` type such as a `.ttf` or `.otf` font file.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **interface/editor/main\_font\_bold**
`🔗<class_EditorSettings_property_interface/editor/main_font_bold>`

The font to use for bold text in the editor interface. Must be a
resource of a `Font<class_Font>` type such as a `.ttf` or `.otf` font
file.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/main\_font\_size**
`🔗<class_EditorSettings_property_interface/editor/main_font_size>`

The size of the font in the editor interface.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/editor/mouse\_extra\_buttons\_navigate\_history**
`🔗<class_EditorSettings_property_interface/editor/mouse_extra_buttons_navigate_history>`

If `true`, the mouse's additional side buttons will be usable to
navigate in the script editor's file history. Set this to `false` if
you're using the side buttons for other purposes (such as a push-to-talk
button in a VoIP program).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/project\_manager\_screen**
`🔗<class_EditorSettings_property_interface/editor/project_manager_screen>`

The preferred monitor to display the project manager.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/save\_each\_scene\_on\_quit**
`🔗<class_EditorSettings_property_interface/editor/save_each_scene_on_quit>`

If `false`, the editor will save all scenes when confirming the **Save**
action when quitting the editor or quitting to the project list. If
`true`, the editor will ask to save each scene individually.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/save\_on\_focus\_loss**
`🔗<class_EditorSettings_property_interface/editor/save_on_focus_loss>`

If `true`, scenes and scripts are saved when the editor loses focus.
Depending on the work flow, this behavior can be less intrusive than
`text_editor/behavior/files/autosave_interval_secs<class_EditorSettings_property_text_editor/behavior/files/autosave_interval_secs>`
or remembering to save manually.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/separate\_distraction\_mode**
`🔗<class_EditorSettings_property_interface/editor/separate_distraction_mode>`

If `true`, the editor's Script tab will have a separate distraction mode
setting from the 2D/3D/AssetLib tabs. If `false`, the distraction-free
mode toggle is shared between all tabs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>`
**interface/editor/show\_internal\_errors\_in\_toast\_notifications**
`🔗<class_EditorSettings_property_interface/editor/show_internal_errors_in_toast_notifications>`

If enabled, displays internal engine errors in toast notifications
(toggleable by clicking the "bell" icon at the bottom of the editor). No
matter the value of this setting, non-internal engine errors will always
be visible in toast notifications.

The default **Auto** value will only enable this if the editor was
compiled with the `dev_build=yes` SCons option (the default is
`dev_build=no`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/show\_update\_spinner**
`🔗<class_EditorSettings_property_interface/editor/show_update_spinner>`

If enabled, displays an icon in the top-right corner of the editor that
spins when the editor redraws a frame. This can be used to diagnose
situations where the engine is constantly redrawing, which should be
avoided as this increases CPU and GPU utilization for no good reason. To
further troubleshoot these situations, start the editor with the
`--debug-canvas-item-redraw`
`command line argument <../tutorials/editor/command_line_tutorial>`.

Consider enabling this if you are developing editor plugins to ensure
they only make the editor redraw when required.

The default **Auto** value will only enable this if the editor was
compiled with the `dev_build=yes` SCons option (the default is
`dev_build=no`).

\*\*Note:\*\* If
`interface/editor/update_continuously<class_EditorSettings_property_interface/editor/update_continuously>`
is `true`, the spinner icon displays in red.

\*\*Note:\*\* If the editor was started with the
`--debug-canvas-item-redraw`
`command line argument <../tutorials/editor/command_line_tutorial>`, the
update spinner will *never* display regardless of this setting's value.
This is to avoid confusion with what would cause redrawing in real world
scenarios.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/single\_window\_mode**
`🔗<class_EditorSettings_property_interface/editor/single_window_mode>`

If `true`, embed modal windows such as docks inside the main editor
window. When single-window mode is enabled, tooltips will also be
embedded inside the main editor window, which means they can't be
displayed outside of the editor window. Single-window mode can be faster
as it does not need to create a separate window for every popup and
tooltip, which can be a slow operation depending on the operating system
and rendering method in use.

This is equivalent to
`ProjectSettings.display/window/subwindows/embed_subwindows<class_ProjectSettings_property_display/window/subwindows/embed_subwindows>`
in the running project, except the setting's value is inverted.

\*\*Note:\*\* To query whether the editor can use multiple windows in an
editor plugin, use
`EditorInterface.is_multi_window_enabled<class_EditorInterface_method_is_multi_window_enabled>`
instead of querying the value of this editor setting.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/ui\_layout\_direction**
`🔗<class_EditorSettings_property_interface/editor/ui_layout_direction>`

Editor UI default layout direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>`
**interface/editor/unfocused\_low\_processor\_mode\_sleep\_usec**
`🔗<class_EditorSettings_property_interface/editor/unfocused_low_processor_mode_sleep_usec>`

When the editor window is unfocused, the amount of sleeping between
frames when the low-processor usage mode is enabled (in microseconds).
Higher values will result in lower CPU/GPU usage, which can improve
battery life on laptops (in addition to improving the running project's
performance if the editor has to redraw continuously). However, higher
values will result in a less responsive editor. The default value is set
to limit the editor to 20 FPS when the editor window is unfocused. See
also
`interface/editor/low_processor_mode_sleep_usec<class_EditorSettings_property_interface/editor/low_processor_mode_sleep_usec>`.

\*\*Note:\*\* This setting is ignored if
`interface/editor/update_continuously<class_EditorSettings_property_interface/editor/update_continuously>`
is `true`, as enabling that setting disables low-processor mode.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/update\_continuously**
`🔗<class_EditorSettings_property_interface/editor/update_continuously>`

If `true`, redraws the editor every frame even if nothing has changed on
screen. When this setting is enabled, the update spinner displays in red
(see
`interface/editor/show_update_spinner<class_EditorSettings_property_interface/editor/show_update_spinner>`).

\*\*Warning:\*\* This greatly increases CPU and GPU utilization, leading
to increased power usage. This should only be enabled for
troubleshooting purposes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/use\_embedded\_menu**
`🔗<class_EditorSettings_property_interface/editor/use_embedded_menu>`

If `true`, editor main menu is using embedded `MenuBar<class_MenuBar>`
instead of system global menu.

Specific to the macOS platform.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/editor/use\_native\_file\_dialogs**
`🔗<class_EditorSettings_property_interface/editor/use_native_file_dialogs>`

If `true`, editor UI uses OS native file/directory selection dialogs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/editor/vsync\_mode**
`🔗<class_EditorSettings_property_interface/editor/vsync_mode>`

Sets the V-Sync mode for the editor. Does not affect the project when
run from the editor (this is controlled by
`ProjectSettings.display/window/vsync/vsync_mode<class_ProjectSettings_property_display/window/vsync/vsync_mode>`).

Depending on the platform and used renderer, the engine will fall back
to **Enabled** if the desired mode is not supported.

\*\*Note:\*\* V-Sync modes other than **Enabled** are only supported in
the Forward+ and Mobile rendering methods, not Compatibility.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/editors/derive\_script\_globals\_by\_name**
`🔗<class_EditorSettings_property_interface/editors/derive_script_globals_by_name>`

If `true`, when extending a script, the global class name of the script
is inserted in the script creation dialog, if it exists. If `false`, the
script's file path is always inserted.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/editors/show\_scene\_tree\_root\_selection**
`🔗<class_EditorSettings_property_interface/editors/show_scene_tree_root_selection>`

If `true`, the Scene dock will display buttons to quickly add a root
node to a newly created scene.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/inspector/auto\_unfold\_foreign\_scenes**
`🔗<class_EditorSettings_property_interface/inspector/auto_unfold_foreign_scenes>`

If `true`, automatically expands property groups in the Inspector dock
when opening a scene that hasn't been opened previously. If `false`, all
groups remain collapsed by default.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/inspector/default\_color\_picker\_mode**
`🔗<class_EditorSettings_property_interface/inspector/default_color_picker_mode>`

The default color picker mode to use when opening
`ColorPicker<class_ColorPicker>`s in the editor. This mode can be
temporarily adjusted on the color picker itself.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/inspector/default\_color\_picker\_shape**
`🔗<class_EditorSettings_property_interface/inspector/default_color_picker_shape>`

The default color picker shape to use when opening
`ColorPicker<class_ColorPicker>`s in the editor. This shape can be
temporarily adjusted on the color picker itself.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **interface/inspector/default\_float\_step**
`🔗<class_EditorSettings_property_interface/inspector/default_float_step>`

The floating-point precision to use for properties that don't define an
explicit precision step. Lower values allow entering more precise
values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/inspector/default\_property\_name\_style**
`🔗<class_EditorSettings_property_interface/inspector/default_property_name_style>`

The default property name style to display in the Inspector dock. This
style can be temporarily adjusted in the Inspector dock's menu.

-   **Raw:** Displays properties in `snake_case`.
-   **Capitalized:** Displays properties capitalized.
-   **Localized:** Displays the localized string for the current editor
    language if a translation is available for the given property. If no
    translation is available, falls back to **Capitalized**.

\*\*Note:\*\* To display translated setting names in Project Settings
and Editor Settings, use
`interface/editor/localize_settings<class_EditorSettings_property_interface/editor/localize_settings>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/inspector/delimitate\_all\_container\_and\_resources**
`🔗<class_EditorSettings_property_interface/inspector/delimitate_all_container_and_resources>`

If `true`, add a margin around Array, Dictionary, and Resource Editors
that are not already colored.

\*\*Note:\*\* If
`interface/inspector/nested_color_mode<class_EditorSettings_property_interface/inspector/nested_color_mode>`
is set to **Containers & Resources** this parameter will have no effect
since those editors will already be colored.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/inspector/disable\_folding**
`🔗<class_EditorSettings_property_interface/inspector/disable_folding>`

If `true`, forces all property groups to be expanded in the Inspector
dock and prevents collapsing them.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **interface/inspector/float\_drag\_speed**
`🔗<class_EditorSettings_property_interface/inspector/float_drag_speed>`

Base speed for increasing/decreasing float values by dragging them in
the inspector.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/inspector/horizontal\_vector2\_editing**
`🔗<class_EditorSettings_property_interface/inspector/horizontal_vector2_editing>`

If `true`, `Vector2<class_Vector2>` and `Vector2i<class_Vector2i>`
properties are shown on a single line in the inspector instead of two
lines. This is overall more compact, but it can be harder to view and
edit large values without expanding the inspector horizontally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/inspector/horizontal\_vector\_types\_editing**
`🔗<class_EditorSettings_property_interface/inspector/horizontal_vector_types_editing>`

If `true`, `Vector3<class_Vector3>`, `Vector3i<class_Vector3i>`,
`Vector4<class_Vector4>`, `Vector4i<class_Vector4i>`,
`Rect2<class_Rect2>`, `Rect2i<class_Rect2i>`, `Plane<class_Plane>`, and
`Quaternion<class_Quaternion>` properties are shown on a single line in
the inspector instead of multiple lines. This is overall more compact,
but it can be harder to view and edit large values without expanding the
inspector horizontally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>`
**interface/inspector/max\_array\_dictionary\_items\_per\_page**
`🔗<class_EditorSettings_property_interface/inspector/max_array_dictionary_items_per_page>`

The number of `Array<class_Array>` or `Dictionary<class_Dictionary>`
items to display on each "page" in the inspector. Higher values allow
viewing more values per page, but take more time to load. This increased
load time is noticeable when selecting nodes that have array or
dictionary properties in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/inspector/nested\_color\_mode**
`🔗<class_EditorSettings_property_interface/inspector/nested_color_mode>`

Control which property editors are colored when they are opened.

-   **Containers & Resources:** Color all Array, Dictionary, and
    Resource Editors.
-   **Resources:** Color all Resource Editors.
-   **External Resources:** Color Resource Editors that edits an
    external resource.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/inspector/open\_resources\_in\_current\_inspector**
`🔗<class_EditorSettings_property_interface/inspector/open_resources_in_current_inspector>`

If `true`, subresources can be edited in the current inspector view. If
the resource type is defined in
`interface/inspector/resources_to_open_in_new_inspector<class_EditorSettings_property_interface/inspector/resources_to_open_in_new_inspector>`
or if this setting is `false`, attempting to edit a subresource always
opens a new inspector view.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedStringArray<class_PackedStringArray>`
**interface/inspector/resources\_to\_open\_in\_new\_inspector**
`🔗<class_EditorSettings_property_interface/inspector/resources_to_open_in_new_inspector>`

List of resources that should always be opened in a new inspector view,
even if
`interface/inspector/open_resources_in_current_inspector<class_EditorSettings_property_interface/inspector/open_resources_in_current_inspector>`
is `true`.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/inspector/show\_low\_level\_opentype\_features**
`🔗<class_EditorSettings_property_interface/inspector/show_low_level_opentype_features>`

If `true`, display OpenType features marked as `hidden` by the font file
in the `Font<class_Font>` editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/multi\_window/enable**
`🔗<class_EditorSettings_property_interface/multi_window/enable>`

If `true`, multiple window support in editor is enabled. The following
panels can become dedicated windows (i.e. made floating): Docks, Script
editor, and Shader editor.

\*\*Note:\*\* When
`interface/editor/single_window_mode<class_EditorSettings_property_interface/editor/single_window_mode>`
is `true`, the multi window support is always disabled.

\*\*Note:\*\* To query whether the editor can use multiple windows in an
editor plugin, use
`EditorInterface.is_multi_window_enabled<class_EditorInterface_method_is_multi_window_enabled>`
instead of querying the value of this editor setting.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/multi\_window/maximize\_window**
`🔗<class_EditorSettings_property_interface/multi_window/maximize_window>`

If `true`, when panels are made floating they will be maximized.

If `false`, when panels are made floating their position and size will
match the ones when they are attached (excluding window border) to the
editor window.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/multi\_window/restore\_windows\_on\_load**
`🔗<class_EditorSettings_property_interface/multi_window/restore_windows_on_load>`

If `true`, the floating panel position, size, and screen will be saved
on editor exit. On next launch the panels that were floating will be
made floating in the saved positions, sizes and screens, if possible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/scene\_tabs/display\_close\_button**
`🔗<class_EditorSettings_property_interface/scene_tabs/display_close_button>`

Controls when the Close (X) button is displayed on scene tabs at the top
of the editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/scene\_tabs/maximum\_width**
`🔗<class_EditorSettings_property_interface/scene_tabs/maximum_width>`

The maximum width of each scene tab at the top editor (in pixels).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/scene\_tabs/restore\_scenes\_on\_load**
`🔗<class_EditorSettings_property_interface/scene_tabs/restore_scenes_on_load>`

If `true`, when a project is loaded, restores scenes that were opened on
the last editor session.

\*\*Note:\*\* With many opened scenes, the editor may take longer to
become usable. If starting the editor quickly is necessary, consider
setting this to `false`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/scene\_tabs/show\_script\_button**
`🔗<class_EditorSettings_property_interface/scene_tabs/show_script_button>`

If `true`, show a button next to each scene tab that opens the scene's
"dominant" script when clicked. The "dominant" script is the one that is
at the highest level in the scene's hierarchy.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/scene\_tabs/show\_thumbnail\_on\_hover**
`🔗<class_EditorSettings_property_interface/scene_tabs/show_thumbnail_on_hover>`

If `true`, display an automatically-generated thumbnail when hovering
scene tabs with the mouse. Scene thumbnails are generated when saving
the scene.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **interface/theme/accent\_color**
`🔗<class_EditorSettings_property_interface/theme/accent_color>`

The color to use for "highlighted" user interface elements in the editor
(pressed and hovered items).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/theme/additional\_spacing**
`🔗<class_EditorSettings_property_interface/theme/additional_spacing>`

The extra spacing to add to various GUI elements in the editor (in
pixels). Increasing this value is useful to improve usability on touch
screens, at the cost of reducing the amount of usable screen real
estate.

See also
`interface/theme/spacing_preset<class_EditorSettings_property_interface/theme/spacing_preset>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **interface/theme/base\_color**
`🔗<class_EditorSettings_property_interface/theme/base_color>`

The base color to use for user interface elements in the editor.
Secondary colors (such as darker/lighter variants) are derived from this
color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/theme/base\_spacing**
`🔗<class_EditorSettings_property_interface/theme/base_spacing>`

The base spacing used by various GUI elements in the editor (in pixels).
See also
`interface/theme/spacing_preset<class_EditorSettings_property_interface/theme/spacing_preset>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/theme/border\_size**
`🔗<class_EditorSettings_property_interface/theme/border_size>`

The border size to use for interface elements (in pixels).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **interface/theme/contrast**
`🔗<class_EditorSettings_property_interface/theme/contrast>`

The contrast factor to use when deriving the editor theme's base color
(see
`interface/theme/base_color<class_EditorSettings_property_interface/theme/base_color>`).
When using a positive values, the derived colors will be *darker* than
the base color. This contrast factor can be set to a negative value,
which will make the derived colors *brighter* than the base color.
Negative contrast rates often look better for light themes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/theme/corner\_radius**
`🔗<class_EditorSettings_property_interface/theme/corner_radius>`

The corner radius to use for interface elements (in pixels). `0` is
square.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **interface/theme/custom\_theme**
`🔗<class_EditorSettings_property_interface/theme/custom_theme>`

The custom theme resource to use for the editor. Must be a Godot theme
resource in `.tres` or `.res` format.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/theme/draw\_extra\_borders**
`🔗<class_EditorSettings_property_interface/theme/draw_extra_borders>`

If `true`, draws additional borders around interactive UI elements in
the editor. This is automatically enabled when using the **Black
(OLED)** theme preset, as this theme preset uses a fully black
background.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/theme/follow\_system\_theme**
`🔗<class_EditorSettings_property_interface/theme/follow_system_theme>`

If `true`, the editor theme preset will attempt to automatically match
the system theme.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **interface/theme/icon\_and\_font\_color**
`🔗<class_EditorSettings_property_interface/theme/icon_and_font_color>`

The icon and font color scheme to use in the editor.

-   **Auto** determines the color scheme to use automatically based on
    `interface/theme/base_color<class_EditorSettings_property_interface/theme/base_color>`.
-   **Dark** makes fonts and icons dark (suitable for light themes).
    Icon colors are automatically converted by the editor following the
    set of rules defined in [this
    file](https://github.com/godotengine/godot/blob/master/editor/themes/editor_theme_manager.cpp).
-   **Light** makes fonts and icons light (suitable for dark themes).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **interface/theme/icon\_saturation**
`🔗<class_EditorSettings_property_interface/theme/icon_saturation>`

The saturation to use for editor icons. Higher values result in more
vibrant colors.

\*\*Note:\*\* The default editor icon saturation was increased by 30% in
Godot 4.0 and later. To get Godot 3.x's icon saturation back, set
`interface/theme/icon_saturation<class_EditorSettings_property_interface/theme/icon_saturation>`
to `0.77`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **interface/theme/preset**
`🔗<class_EditorSettings_property_interface/theme/preset>`

The editor theme preset to use.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **interface/theme/relationship\_line\_opacity**
`🔗<class_EditorSettings_property_interface/theme/relationship_line_opacity>`

The opacity to use when drawing relationship lines in the editor's
`Tree<class_Tree>`-based GUIs (such as the Scene tree dock).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **interface/theme/spacing\_preset**
`🔗<class_EditorSettings_property_interface/theme/spacing_preset>`

The editor theme spacing preset to use. See also
`interface/theme/base_spacing<class_EditorSettings_property_interface/theme/base_spacing>`
and
`interface/theme/additional_spacing<class_EditorSettings_property_interface/theme/additional_spacing>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface/theme/use\_system\_accent\_color**
`🔗<class_EditorSettings_property_interface/theme/use_system_accent_color>`

If `true`, set accent color based on system settings.

\*\*Note:\*\* This setting is only effective on Windows and MacOS.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/touchscreen/enable\_long\_press\_as\_right\_click**
`🔗<class_EditorSettings_property_interface/touchscreen/enable_long_press_as_right_click>`

If `true`, long press on touchscreen is treated as right click.

\*\*Note:\*\* Defaults to `true` on touchscreen devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/touchscreen/enable\_pan\_and\_scale\_gestures**
`🔗<class_EditorSettings_property_interface/touchscreen/enable_pan_and_scale_gestures>`

If `true`, enable two finger pan and scale gestures on touchscreen
devices.

\*\*Note:\*\* Defaults to `true` on touchscreen devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**interface/touchscreen/increase\_scrollbar\_touch\_area**
`🔗<class_EditorSettings_property_interface/touchscreen/increase_scrollbar_touch_area>`

If `true`, increases the scrollbar touch area to improve usability on
touchscreen devices.

\*\*Note:\*\* Defaults to `true` on touchscreen devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **interface/touchscreen/scale\_gizmo\_handles**
`🔗<class_EditorSettings_property_interface/touchscreen/scale_gizmo_handles>`

Specify the multiplier to apply to the scale for the editor gizmo
handles to improve usability on touchscreen devices.

\*\*Note:\*\* Defaults to `1` on non-touchscreen devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **network/connection/engine\_version\_update\_mode**
`🔗<class_EditorSettings_property_network/connection/engine_version_update_mode>`

Specifies how the engine should check for updates.

-   **Disable Update Checks** will block the engine from checking
    updates (see also
    `network/connection/network_mode<class_EditorSettings_property_network/connection/network_mode>`).
-   **Check Newest Preview** (default for preview versions) will check
    for the newest available development snapshot.
-   **Check Newest Stable** (default for stable versions) will check for
    the newest available stable version.
-   **Check Newest Patch** will check for the latest available stable
    version, but only within the same minor version. E.g. if your
    version is `4.3.stable`, you will be notified about `4.3.1.stable`,
    but not `4.4.stable`.

All update modes will ignore builds with different major versions (e.g.
Godot 4 -&gt; Godot 5).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **network/connection/network\_mode**
`🔗<class_EditorSettings_property_network/connection/network_mode>`

Determines whether online features are enabled in the editor, such as
the Asset Library or update checks. Disabling these online features
helps alleviate privacy concerns by preventing the editor from making
HTTP requests to the Godot website or third-party platforms hosting
assets from the Asset Library.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **network/debug/remote\_host**
`🔗<class_EditorSettings_property_network/debug/remote_host>`

The address to listen to when starting the remote debugger. This can be
set to `0.0.0.0` to allow external clients to connect to the remote
debugger (instead of restricting the remote debugger to connections from
`localhost`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **network/debug/remote\_port**
`🔗<class_EditorSettings_property_network/debug/remote_port>`

The port to listen to when starting the remote debugger. Godot will try
to use port numbers above the configured number if the configured number
is already taken by another application.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **network/http\_proxy/host**
`🔗<class_EditorSettings_property_network/http_proxy/host>`

The host to use to contact the HTTP and HTTPS proxy in the editor (for
the asset library and export template downloads). See also
`network/http_proxy/port<class_EditorSettings_property_network/http_proxy/port>`.

\*\*Note:\*\* Godot currently doesn't automatically use system proxy
settings, so you have to enter them manually here if needed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **network/http\_proxy/port**
`🔗<class_EditorSettings_property_network/http_proxy/port>`

The port number to use to contact the HTTP and HTTPS proxy in the editor
(for the asset library and export template downloads). See also
`network/http_proxy/host<class_EditorSettings_property_network/http_proxy/host>`.

\*\*Note:\*\* Godot currently doesn't automatically use system proxy
settings, so you have to enter them manually here if needed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **network/tls/editor\_tls\_certificates**
`🔗<class_EditorSettings_property_network/tls/editor_tls_certificates>`

The TLS certificate bundle to use for HTTP requests made within the
editor (e.g. from the AssetLib tab). If left empty, the [included
Mozilla certificate
bundle](https://github.com/godotengine/godot/blob/master/thirdparty/certs/ca-certificates.crt)
will be used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **project\_manager/default\_renderer**
`🔗<class_EditorSettings_property_project_manager/default_renderer>`

The renderer type that will be checked off by default when creating a
new project. Accepted strings are "forward\_plus", "mobile" or
"gl\_compatibility".

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **project\_manager/directory\_naming\_convention**
`🔗<class_EditorSettings_property_project_manager/directory_naming_convention>`

Directory naming convention for the project manager. Options are "No
convention" (project name is directory name), "kebab-case" (default),
"snake\_case", "camelCase", "PascalCase", or "Title Case".

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **project\_manager/sorting\_order**
`🔗<class_EditorSettings_property_project_manager/sorting_order>`

The sorting order to use in the project manager. When changing the
sorting order in the project manager, this setting is set permanently in
the editor settings.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **run/auto\_save/save\_before\_running**
`🔗<class_EditorSettings_property_run/auto_save/save_before_running>`

If `true`, saves all scenes and scripts automatically before running the
project. Setting this to `false` prevents the editor from saving if
there are no changes which can speed up the project startup slightly,
but it makes it possible to run a project that has unsaved changes.
(Unsaved changes will not be visible in the running project.)

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **run/bottom\_panel/action\_on\_play**
`🔗<class_EditorSettings_property_run/bottom_panel/action_on_play>`

The action to execute on the bottom panel when running the project.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **run/bottom\_panel/action\_on\_stop**
`🔗<class_EditorSettings_property_run/bottom_panel/action_on_stop>`

The action to execute on the bottom panel when stopping the project.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **run/output/always\_clear\_output\_on\_play**
`🔗<class_EditorSettings_property_run/output/always_clear_output_on_play>`

If `true`, the editor will clear the Output panel when running the
project.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **run/output/font\_size**
`🔗<class_EditorSettings_property_run/output/font_size>`

The size of the font in the **Output** panel at the bottom of the
editor. This setting does not impact the font size of the script editor
(see
`interface/editor/code_font_size<class_EditorSettings_property_interface/editor/code_font_size>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **run/output/max\_lines**
`🔗<class_EditorSettings_property_run/output/max_lines>`

Maximum number of lines to show at any one time in the Output panel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **run/platforms/linuxbsd/prefer\_wayland**
`🔗<class_EditorSettings_property_run/platforms/linuxbsd/prefer_wayland>`

If `true`, on Linux/BSD, the editor will check for Wayland first instead
of X11 (if available).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **run/window\_placement/android\_window**
`🔗<class_EditorSettings_property_run/window_placement/android_window>`

Specifies how the Play window is launched relative to the Android
editor.

-   **Auto (based on screen size)** (default) will automatically choose
    how to launch the Play window based on the device and screen
    metrics. Defaults to **Same as Editor** on phones and **Side-by-side
    with Editor** on tablets.
-   **Same as Editor** will launch the Play window in the same window as
    the Editor.
-   **Side-by-side with Editor** will launch the Play window
    side-by-side with the Editor window.
-   **Launch in PiP mode** will launch the Play window directly in
    picture-in-picture (PiP) mode if PiP mode is supported and enabled.
    When maximized, the Play window will occupy the same window as the
    Editor.

\*\*Note:\*\* Only available in the Android editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **run/window\_placement/play\_window\_pip\_mode**
`🔗<class_EditorSettings_property_run/window_placement/play_window_pip_mode>`

Specifies the picture-in-picture (PiP) mode for the Play window.

-   **Disabled:** PiP is disabled for the Play window.
-   **Enabled:** If the device supports it, PiP is always enabled for
    the Play window. The Play window will contain a button to enter PiP
    mode.
-   **Enabled when Play window is same as Editor** (default for Android
    editor): If the device supports it, PiP is enabled when the Play
    window is the same as the Editor. The Play window will contain a
    button to enter PiP mode.

\*\*Note:\*\* Only available in the Android editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **run/window\_placement/rect**
`🔗<class_EditorSettings_property_run/window_placement/rect>`

The window mode to use to display the project when starting the project
from the editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>`
**run/window\_placement/rect\_custom\_position**
`🔗<class_EditorSettings_property_run/window_placement/rect_custom_position>`

The custom position to use when starting the project from the editor (in
pixels from the top-left corner). Only effective if
`run/window_placement/rect<class_EditorSettings_property_run/window_placement/rect>`
is set to **Custom Position**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **run/window\_placement/screen**
`🔗<class_EditorSettings_property_run/window_placement/screen>`

The monitor to display the project on when starting the project from the
editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/appearance/caret/caret\_blink**
`🔗<class_EditorSettings_property_text_editor/appearance/caret/caret_blink>`

If `true`, makes the caret blink according to
`text_editor/appearance/caret/caret_blink_interval<class_EditorSettings_property_text_editor/appearance/caret/caret_blink_interval>`.
Disabling this setting can improve battery life on laptops if you spend
long amounts of time in the script editor, since it will reduce the
frequency at which the editor needs to be redrawn.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>`
**text\_editor/appearance/caret/caret\_blink\_interval**
`🔗<class_EditorSettings_property_text_editor/appearance/caret/caret_blink_interval>`

The interval at which the caret will blink (in seconds). See also
`text_editor/appearance/caret/caret_blink<class_EditorSettings_property_text_editor/appearance/caret/caret_blink>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/appearance/caret/highlight\_all\_occurrences**
`🔗<class_EditorSettings_property_text_editor/appearance/caret/highlight_all_occurrences>`

If `true`, highlights all occurrences of the currently selected text in
the script editor. See also
`text_editor/theme/highlighting/word_highlighted_color<class_EditorSettings_property_text_editor/theme/highlighting/word_highlighted_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/appearance/caret/highlight\_current\_line**
`🔗<class_EditorSettings_property_text_editor/appearance/caret/highlight_current_line>`

If `true`, colors the background of the line the caret is currently on
with
`text_editor/theme/highlighting/current_line_color<class_EditorSettings_property_text_editor/theme/highlighting/current_line_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/appearance/caret/type**
`🔗<class_EditorSettings_property_text_editor/appearance/caret/type>`

The shape of the caret to use in the script editor. **Line** displays a
vertical line to the left of the current character, whereas **Block**
displays an outline over the current character.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>`
**text\_editor/appearance/guidelines/line\_length\_guideline\_hard\_column**
`🔗<class_EditorSettings_property_text_editor/appearance/guidelines/line_length_guideline_hard_column>`

The column at which to display a subtle line as a line length guideline
for scripts. This should generally be greater than
`text_editor/appearance/guidelines/line_length_guideline_soft_column<class_EditorSettings_property_text_editor/appearance/guidelines/line_length_guideline_soft_column>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>`
**text\_editor/appearance/guidelines/line\_length\_guideline\_soft\_column**
`🔗<class_EditorSettings_property_text_editor/appearance/guidelines/line_length_guideline_soft_column>`

The column at which to display a *very* subtle line as a line length
guideline for scripts. This should generally be lower than
`text_editor/appearance/guidelines/line_length_guideline_hard_column<class_EditorSettings_property_text_editor/appearance/guidelines/line_length_guideline_hard_column>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/appearance/guidelines/show\_line\_length\_guidelines**
`🔗<class_EditorSettings_property_text_editor/appearance/guidelines/show_line_length_guidelines>`

If `true`, displays line length guidelines to help you keep line lengths
in check. See also
`text_editor/appearance/guidelines/line_length_guideline_soft_column<class_EditorSettings_property_text_editor/appearance/guidelines/line_length_guideline_soft_column>`
and
`text_editor/appearance/guidelines/line_length_guideline_hard_column<class_EditorSettings_property_text_editor/appearance/guidelines/line_length_guideline_hard_column>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/appearance/gutters/highlight\_type\_safe\_lines**
`🔗<class_EditorSettings_property_text_editor/appearance/gutters/highlight_type_safe_lines>`

If `true`, highlights type-safe lines by displaying their line number
color with
`text_editor/theme/highlighting/safe_line_number_color<class_EditorSettings_property_text_editor/theme/highlighting/safe_line_number_color>`
instead of
`text_editor/theme/highlighting/line_number_color<class_EditorSettings_property_text_editor/theme/highlighting/line_number_color>`.
Type-safe lines are lines of code where the type of all variables is
known at compile-time. These type-safe lines may run faster thanks to
typed instructions.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/appearance/gutters/line\_numbers\_zero\_padded**
`🔗<class_EditorSettings_property_text_editor/appearance/gutters/line_numbers_zero_padded>`

If `true`, displays line numbers with zero padding (e.g. `007` instead
of `7`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/appearance/gutters/show\_info\_gutter**
`🔗<class_EditorSettings_property_text_editor/appearance/gutters/show_info_gutter>`

If `true`, displays a gutter at the left containing icons for methods
with signal connections and for overridden methods.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/appearance/gutters/show\_line\_numbers**
`🔗<class_EditorSettings_property_text_editor/appearance/gutters/show_line_numbers>`

If `true`, displays line numbers in a gutter at the left.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/appearance/lines/autowrap\_mode**
`🔗<class_EditorSettings_property_text_editor/appearance/lines/autowrap_mode>`

If
`text_editor/appearance/lines/word_wrap<class_EditorSettings_property_text_editor/appearance/lines/word_wrap>`
is set to `1`, sets text wrapping mode. To see how each mode behaves,
see `AutowrapMode<enum_TextServer_AutowrapMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/appearance/lines/code\_folding**
`🔗<class_EditorSettings_property_text_editor/appearance/lines/code_folding>`

If `true`, displays the folding arrows next to indented code sections
and allows code folding. If `false`, hides the folding arrows next to
indented code sections and disallows code folding.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/appearance/lines/word\_wrap**
`🔗<class_EditorSettings_property_text_editor/appearance/lines/word_wrap>`

If `true`, wraps long lines over multiple lines to avoid horizontal
scrolling. This is a display-only feature; it does not actually insert
line breaks in your scripts.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/appearance/minimap/minimap\_width**
`🔗<class_EditorSettings_property_text_editor/appearance/minimap/minimap_width>`

The width of the minimap in the script editor (in pixels).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/appearance/minimap/show\_minimap**
`🔗<class_EditorSettings_property_text_editor/appearance/minimap/show_minimap>`

If `true`, draws an overview of the script near the scroll bar. The
minimap can be left-clicked to scroll directly to a location in an
"absolute" manner.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/appearance/whitespace/draw\_spaces**
`🔗<class_EditorSettings_property_text_editor/appearance/whitespace/draw_spaces>`

If `true`, draws space characters as centered points.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/appearance/whitespace/draw\_tabs**
`🔗<class_EditorSettings_property_text_editor/appearance/whitespace/draw_tabs>`

If `true`, draws tab characters as chevrons.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/appearance/whitespace/line\_spacing**
`🔗<class_EditorSettings_property_text_editor/appearance/whitespace/line_spacing>`

The space to add between lines (in pixels). Greater line spacing can
help improve readability at the cost of displaying fewer lines on
screen.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/files/auto\_reload\_and\_parse\_scripts\_on\_save**
`🔗<class_EditorSettings_property_text_editor/behavior/files/auto_reload_and_parse_scripts_on_save>`

If `true`, tool scripts will be automatically soft-reloaded after they
are saved.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/files/auto\_reload\_scripts\_on\_external\_change**
`🔗<class_EditorSettings_property_text_editor/behavior/files/auto_reload_scripts_on_external_change>`

If `true`, automatically reloads scripts in the editor when they have
been modified and saved by external editors.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>`
**text\_editor/behavior/files/autosave\_interval\_secs**
`🔗<class_EditorSettings_property_text_editor/behavior/files/autosave_interval_secs>`

If set to a value greater than `0`, automatically saves the current
script following the specified interval (in seconds). This can be used
to prevent data loss if the editor crashes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/files/convert\_indent\_on\_save**
`🔗<class_EditorSettings_property_text_editor/behavior/files/convert_indent_on_save>`

If `true`, converts indentation to match the script editor's indentation
settings when saving a script. See also
`text_editor/behavior/indent/type<class_EditorSettings_property_text_editor/behavior/indent/type>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/files/open\_dominant\_script\_on\_scene\_change**
`🔗<class_EditorSettings_property_text_editor/behavior/files/open_dominant_script_on_scene_change>`

If `true`, opening a scene automatically opens the script attached to
the root node, or the topmost node if the root has no script.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/files/restore\_scripts\_on\_load**
`🔗<class_EditorSettings_property_text_editor/behavior/files/restore_scripts_on_load>`

If `true`, reopens scripts that were opened in the last session when the
editor is reopened on a given project.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/files/trim\_final\_newlines\_on\_save**
`🔗<class_EditorSettings_property_text_editor/behavior/files/trim_final_newlines_on_save>`

If `true`, trims all empty newlines after the final newline when saving
a script. Final newlines refer to the empty newlines found at the end of
files. Since these serve no practical purpose, they can and should be
removed to make version control diffs less noisy.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/files/trim\_trailing\_whitespace\_on\_save**
`🔗<class_EditorSettings_property_text_editor/behavior/files/trim_trailing_whitespace_on_save>`

If `true`, trims trailing whitespace when saving a script. Trailing
whitespace refers to tab and space characters placed at the end of
lines. Since these serve no practical purpose, they can and should be
removed to make version control diffs less noisy.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/general/empty\_selection\_clipboard**
`🔗<class_EditorSettings_property_text_editor/behavior/general/empty_selection_clipboard>`

If `true`, copying or cutting without a selection is performed on all
lines with a caret. Otherwise, copy and cut require a selection.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/behavior/indent/auto\_indent**
`🔗<class_EditorSettings_property_text_editor/behavior/indent/auto_indent>`

If `true`, automatically indents code when pressing the `Enter` key
based on blocks above the new line.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/indent/indent\_wrapped\_lines**
`🔗<class_EditorSettings_property_text_editor/behavior/indent/indent_wrapped_lines>`

If `true`, all wrapped lines are indented to the same amount as the
unwrapped line.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/behavior/indent/size**
`🔗<class_EditorSettings_property_text_editor/behavior/indent/size>`

When using tab indentation, determines the length of each tab. When
using space indentation, determines how many spaces are inserted when
pressing `Tab` and when automatic indentation is performed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/behavior/indent/type**
`🔗<class_EditorSettings_property_text_editor/behavior/indent/type>`

The indentation style to use (tabs or spaces).

\*\*Note:\*\* The
`GDScript style guide <../tutorials/scripting/gdscript/gdscript_styleguide>`
recommends using tabs for indentation. It is advised to change this
setting only if you need to work on a project that currently uses spaces
for indentation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>`
**text\_editor/behavior/navigation/custom\_word\_separators**
`🔗<class_EditorSettings_property_text_editor/behavior/navigation/custom_word_separators>`

The characters to consider as word delimiters if
`text_editor/behavior/navigation/use_custom_word_separators<class_EditorSettings_property_text_editor/behavior/navigation/use_custom_word_separators>`
is `true`. This is in addition to default characters if
`text_editor/behavior/navigation/use_default_word_separators<class_EditorSettings_property_text_editor/behavior/navigation/use_default_word_separators>`
is `true`. The characters should be defined without separation, for
example `_♥=`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/navigation/drag\_and\_drop\_selection**
`🔗<class_EditorSettings_property_text_editor/behavior/navigation/drag_and_drop_selection>`

If `true`, allows drag-and-dropping text in the script editor to move
text. Disable this if you find yourself accidentally drag-and-dropping
text in the script editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/navigation/move\_caret\_on\_right\_click**
`🔗<class_EditorSettings_property_text_editor/behavior/navigation/move_caret_on_right_click>`

If `true`, the caret will be moved when right-clicking somewhere in the
script editor (like when left-clicking or middle-clicking). If `false`,
the caret will only be moved when left-clicking or middle-clicking
somewhere.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/navigation/open\_script\_when\_connecting\_signal\_to\_existing\_method**
`🔗<class_EditorSettings_property_text_editor/behavior/navigation/open_script_when_connecting_signal_to_existing_method>`

If `true`, opens the script editor when connecting a signal to an
existing script method from the Node dock.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/navigation/scroll\_past\_end\_of\_file**
`🔗<class_EditorSettings_property_text_editor/behavior/navigation/scroll_past_end_of_file>`

If `true`, allows scrolling past the end of the file.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/navigation/smooth\_scrolling**
`🔗<class_EditorSettings_property_text_editor/behavior/navigation/smooth_scrolling>`

If `true`, enables a smooth scrolling animation when using the mouse
wheel to scroll. See
`text_editor/behavior/navigation/v_scroll_speed<class_EditorSettings_property_text_editor/behavior/navigation/v_scroll_speed>`
for the speed of this animation.

\*\*Note:\*\*
`text_editor/behavior/navigation/smooth_scrolling<class_EditorSettings_property_text_editor/behavior/navigation/smooth_scrolling>`
currently behaves poorly in projects where
`ProjectSettings.physics/common/physics_ticks_per_second<class_ProjectSettings_property_physics/common/physics_ticks_per_second>`
has been increased significantly from its default value (`60`). In this
case, it is recommended to disable this setting.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/navigation/stay\_in\_script\_editor\_on\_node\_selected**
`🔗<class_EditorSettings_property_text_editor/behavior/navigation/stay_in_script_editor_on_node_selected>`

If `true`, prevents automatically switching between the Script and 2D/3D
screens when selecting a node in the Scene tree dock.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/navigation/use\_custom\_word\_separators**
`🔗<class_EditorSettings_property_text_editor/behavior/navigation/use_custom_word_separators>`

If `true`, uses the characters in
`text_editor/behavior/navigation/custom_word_separators<class_EditorSettings_property_text_editor/behavior/navigation/custom_word_separators>`
as word separators for word navigation and operations. This is in
addition to the default characters if
`text_editor/behavior/navigation/use_default_word_separators<class_EditorSettings_property_text_editor/behavior/navigation/use_default_word_separators>`
is also enabled. Word navigation and operations include double-clicking
on a word or holding `Ctrl` (`Cmd` on macOS) while pressing `left`,
`right`, `backspace`, or `delete`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/behavior/navigation/use\_default\_word\_separators**
`🔗<class_EditorSettings_property_text_editor/behavior/navigation/use_default_word_separators>`

If `true`, uses the characters in
`` `!"#$%&'()*+,-./:;<=>?@[\]^`{|}~ ``, the Unicode General Punctuation
table, and the Unicode CJK Punctuation table as word separators for word
navigation and operations. If `false`, a subset of these characters are
used and does not include the characters `<>$~^=+|`. This is in addition
to custom characters if
`text_editor/behavior/navigation/use_custom_word_separators<class_EditorSettings_property_text_editor/behavior/navigation/use_custom_word_separators>`
is also enabled. These characters are used to determine where a word
stops. Word navigation and operations include double-clicking on a word
or holding `Ctrl` (`Cmd` on macOS) while pressing `left`, `right`,
`backspace`, or `delete`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/behavior/navigation/v\_scroll\_speed**
`🔗<class_EditorSettings_property_text_editor/behavior/navigation/v_scroll_speed>`

The speed of scrolling in lines per second when
`text_editor/behavior/navigation/smooth_scrolling<class_EditorSettings_property_text_editor/behavior/navigation/smooth_scrolling>`
is `true`. Higher values make the script scroll by faster when using the
mouse wheel.

\*\*Note:\*\* You can hold down `Alt` while using the mouse wheel to
temporarily scroll 5 times faster.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/completion/add\_node\_path\_literals**
`🔗<class_EditorSettings_property_text_editor/completion/add_node_path_literals>`

If `true`, uses `NodePath<class_NodePath>` instead of
`String<class_String>` when appropriate for code autocompletion or for
drag and dropping object properties into the script editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/completion/add\_string\_name\_literals**
`🔗<class_EditorSettings_property_text_editor/completion/add_string_name_literals>`

If `true`, uses `StringName<class_StringName>` instead of
`String<class_String>` when appropriate for code autocompletion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/completion/add\_type\_hints**
`🔗<class_EditorSettings_property_text_editor/completion/add_type_hints>`

If `true`, adds
`GDScript static typing <../tutorials/scripting/gdscript/static_typing>`
hints such as `-> void` and `: int` when using code autocompletion or
when creating onready variables by drag and dropping nodes into the
script editor while pressing the `Ctrl` key. If `true`, newly created
scripts will also automatically have type hints added to their method
parameters and return types.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/completion/auto\_brace\_complete**
`🔗<class_EditorSettings_property_text_editor/completion/auto_brace_complete>`

If `true`, automatically completes braces when making use of code
completion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **text\_editor/completion/code\_complete\_delay**
`🔗<class_EditorSettings_property_text_editor/completion/code_complete_delay>`

The delay in seconds after which autocompletion suggestions should be
displayed when the user stops typing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/completion/code\_complete\_enabled**
`🔗<class_EditorSettings_property_text_editor/completion/code_complete_enabled>`

If `true`, code completion will be triggered automatically after
`text_editor/completion/code_complete_delay<class_EditorSettings_property_text_editor/completion/code_complete_delay>`.
Even if `false`, code completion can be triggered manually with the
`ui_text_completion_query` action (by default `Ctrl + Space` or
`Cmd + Space` on macOS).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/completion/colorize\_suggestions**
`🔗<class_EditorSettings_property_text_editor/completion/colorize_suggestions>`

If `true` enables the coloring for some items in the autocompletion
suggestions, like vector components.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/completion/complete\_file\_paths**
`🔗<class_EditorSettings_property_text_editor/completion/complete_file_paths>`

If `true`, provides autocompletion suggestions for file paths in methods
such as `load()` and `preload()`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **text\_editor/completion/idle\_parse\_delay**
`🔗<class_EditorSettings_property_text_editor/completion/idle_parse_delay>`

The delay in seconds after which the script editor should check for
errors when the user stops typing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/completion/put\_callhint\_tooltip\_below\_current\_line**
`🔗<class_EditorSettings_property_text_editor/completion/put_callhint_tooltip_below_current_line>`

If `true`, the code completion tooltip will appear below the current
line unless there is no space on screen below the current line. If
`false`, the code completion tooltip will appear above the current line.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/completion/use\_single\_quotes**
`🔗<class_EditorSettings_property_text_editor/completion/use_single_quotes>`

If `true`, performs string autocompletion with single quotes. If
`false`, performs string autocompletion with double quotes (which
matches the
`GDScript style guide <../tutorials/scripting/gdscript/gdscript_styleguide>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **text\_editor/external/exec\_flags**
`🔗<class_EditorSettings_property_text_editor/external/exec_flags>`

The command-line arguments to pass to the external text editor that is
run when
`text_editor/external/use_external_editor<class_EditorSettings_property_text_editor/external/use_external_editor>`
is `true`. See also
`text_editor/external/exec_path<class_EditorSettings_property_text_editor/external/exec_path>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **text\_editor/external/exec\_path**
`🔗<class_EditorSettings_property_text_editor/external/exec_path>`

The path to the text editor executable used to edit text files if
`text_editor/external/use_external_editor<class_EditorSettings_property_text_editor/external/use_external_editor>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/external/use\_external\_editor**
`🔗<class_EditorSettings_property_text_editor/external/use_external_editor>`

If `true`, uses an external editor instead of the built-in Script
Editor. See also
`text_editor/external/exec_path<class_EditorSettings_property_text_editor/external/exec_path>`
and
`text_editor/external/exec_flags<class_EditorSettings_property_text_editor/external/exec_flags>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/help/class\_reference\_examples**
`🔗<class_EditorSettings_property_text_editor/help/class_reference_examples>`

Controls which multi-line code blocks should be displayed in the editor
help. This setting does not affect single-line code literals in the
editor help.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/help/help\_font\_size**
`🔗<class_EditorSettings_property_text_editor/help/help_font_size>`

The font size to use for the editor help (built-in class reference).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/help/help\_source\_font\_size**
`🔗<class_EditorSettings_property_text_editor/help/help_source_font_size>`

The font size to use for code samples in the editor help (built-in class
reference).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/help/help\_title\_font\_size**
`🔗<class_EditorSettings_property_text_editor/help/help_title_font_size>`

The font size to use for headings in the editor help (built-in class
reference).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/help/show\_help\_index**
`🔗<class_EditorSettings_property_text_editor/help/show_help_index>`

If `true`, displays a table of contents at the left of the editor help
(at the location where the members overview would appear when editing a
script).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/help/sort\_functions\_alphabetically**
`🔗<class_EditorSettings_property_text_editor/help/sort_functions_alphabetically>`

If `true`, the script's method list in the Script Editor is sorted
alphabetically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/script\_list/group\_help\_pages**
`🔗<class_EditorSettings_property_text_editor/script_list/group_help_pages>`

If `true`, class reference pages are grouped together at the bottom of
the Script Editor's script list.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/script\_list/list\_script\_names\_as**
`🔗<class_EditorSettings_property_text_editor/script_list/list_script_names_as>`

Specifies how script paths should be displayed in Script Editor's script
list. If using the "Name" option and some scripts share the same file
name, more parts of their paths are revealed to avoid conflicts.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/script\_list/script\_temperature\_enabled**
`🔗<class_EditorSettings_property_text_editor/script_list/script_temperature_enabled>`

If `true`, the names of recently opened scripts in the Script Editor are
highlighted with the accent color, with its intensity based on how
recently they were opened.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>`
**text\_editor/script\_list/script\_temperature\_history\_size**
`🔗<class_EditorSettings_property_text_editor/script_list/script_temperature_history_size>`

How many script names can be highlighted at most, if
`text_editor/script_list/script_temperature_enabled<class_EditorSettings_property_text_editor/script_list/script_temperature_enabled>`
is `true`. Scripts older than this value use the default font color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **text\_editor/script\_list/show\_members\_overview**
`🔗<class_EditorSettings_property_text_editor/script_list/show_members_overview>`

If `true`, displays an overview of the current script's member variables
and functions at the left of the script editor. See also
`text_editor/script_list/sort_members_outline_alphabetically<class_EditorSettings_property_text_editor/script_list/sort_members_outline_alphabetically>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>`
**text\_editor/script\_list/sort\_members\_outline\_alphabetically**
`🔗<class_EditorSettings_property_text_editor/script_list/sort_members_outline_alphabetically>`

If `true`, sorts the members outline (located at the left of the script
editor) using alphabetical order. If `false`, sorts the members outline
depending on the order in which members are found in the script.

\*\*Note:\*\* Only effective if
`text_editor/script_list/show_members_overview<class_EditorSettings_property_text_editor/script_list/show_members_overview>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/script\_list/sort\_scripts\_by**
`🔗<class_EditorSettings_property_text_editor/script_list/sort_scripts_by>`

Specifies sorting used for Script Editor's open script list.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **text\_editor/theme/color\_theme**
`🔗<class_EditorSettings_property_text_editor/theme/color_theme>`

The syntax theme to use in the script editor.

You can save your own syntax theme from your current settings by using
**File &gt; Theme &gt; Save As...** at the top of the script editor. The
syntax theme will then be available locally in the list of color themes.

You can find additional syntax themes to install in the
[godot-syntax-themes](https://github.com/godotengine/godot-syntax-themes)
repository.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/background\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/background_color>`

The script editor's background color. If set to a translucent color, the
editor theme's base color will be visible behind.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/base\_type\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/base_type_color>`

The script editor's base type color (used for types like
`Vector2<class_Vector2>`, `Vector3<class_Vector3>`,
`Color<class_Color>`, ...).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **text\_editor/theme/highlighting/bookmark\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/bookmark_color>`

The script editor's bookmark icon color (displayed in the gutter).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/brace\_mismatch\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/brace_mismatch_color>`

The script editor's brace mismatch color. Used when the caret is
currently on a mismatched brace, parenthesis or bracket character.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/breakpoint\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/breakpoint_color>`

The script editor's breakpoint icon color (displayed in the gutter).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/caret\_background\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/caret_background_color>`

The script editor's caret background color.

\*\*Note:\*\* This setting has no effect as it's currently unused.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **text\_editor/theme/highlighting/caret\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/caret_color>`

The script editor's caret color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/code\_folding\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/code_folding_color>`

The script editor's color for the code folding icon (displayed in the
gutter).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **text\_editor/theme/highlighting/comment\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/comment_color>`

The script editor's comment color.

\*\*Note:\*\* In GDScript, unlike Python, multiline strings are not
considered to be comments, and will use the string highlighting color
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/completion\_background\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/completion_background_color>`

The script editor's autocompletion box background color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/completion\_existing\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/completion_existing_color>`

The script editor's autocompletion box background color to highlight
existing characters in the completion results. This should be a
translucent color so that
`text_editor/theme/highlighting/completion_selected_color<class_EditorSettings_property_text_editor/theme/highlighting/completion_selected_color>`
can be seen behind.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/completion\_font\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/completion_font_color>`

The script editor's autocompletion box text color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/completion\_scroll\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/completion_scroll_color>`

The script editor's autocompletion box scroll bar color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/completion\_scroll\_hovered\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/completion_scroll_hovered_color>`

The script editor's autocompletion box scroll bar color when hovered or
pressed with the mouse.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/completion\_selected\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/completion_selected_color>`

The script editor's autocompletion box background color for the
currently selected line.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/control\_flow\_keyword\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/control_flow_keyword_color>`

The script editor's control flow keyword color (used for keywords like
`if`, `for`, `return`, ...).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/current\_line\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/current_line_color>`

The script editor's background color for the line the caret is currently
on. This should be set to a translucent color so that it can display on
top of other line color modifiers such as
`text_editor/theme/highlighting/mark_color<class_EditorSettings_property_text_editor/theme/highlighting/mark_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/doc\_comment\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/doc_comment_color>`

The script editor's documentation comment color. In GDScript, this is
used for comments starting with `##`. In C#, this is used for comments
starting with `///` or `/**`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/engine\_type\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/engine_type_color>`

The script editor's engine type color (`Vector2<class_Vector2>`,
`Vector3<class_Vector3>`, `Color<class_Color>`, ...).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/executing\_line\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/executing_line_color>`

The script editor's color for the debugger's executing line icon
(displayed in the gutter).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/folded\_code\_region\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/folded_code_region_color>`

The script editor's background line highlighting color for folded code
region.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **text\_editor/theme/highlighting/function\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/function_color>`

The script editor's function call color.

\*\*Note:\*\* When using the GDScript syntax highlighter, this is
replaced by the function definition color configured in the syntax theme
for function definitions (e.g. `func _ready():`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **text\_editor/theme/highlighting/keyword\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/keyword_color>`

The script editor's non-control flow keyword color (used for keywords
like `var`, `func`, `extends`, ...).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/line\_length\_guideline\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/line_length_guideline_color>`

The script editor's color for the line length guideline. The "hard" line
length guideline will be drawn with this color, whereas the "soft" line
length guideline will be drawn with half of its opacity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/line\_number\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/line_number_color>`

The script editor's color for line numbers. See also
`text_editor/theme/highlighting/safe_line_number_color<class_EditorSettings_property_text_editor/theme/highlighting/safe_line_number_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **text\_editor/theme/highlighting/mark\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/mark_color>`

The script editor's background color for lines with errors. This should
be set to a translucent color so that it can display on top of other
line color modifiers such as
`text_editor/theme/highlighting/current_line_color<class_EditorSettings_property_text_editor/theme/highlighting/current_line_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/member\_variable\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/member_variable_color>`

The script editor's color for member variables on objects (e.g.
`self.some_property`).

\*\*Note:\*\* This color is not used for local variable declaration and
access.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **text\_editor/theme/highlighting/number\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/number_color>`

The script editor's color for numbers (integer and floating-point).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/safe\_line\_number\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/safe_line_number_color>`

The script editor's color for type-safe line numbers. See also
`text_editor/theme/highlighting/line_number_color<class_EditorSettings_property_text_editor/theme/highlighting/line_number_color>`.

\*\*Note:\*\* Only displayed if
`text_editor/appearance/gutters/highlight_type_safe_lines<class_EditorSettings_property_text_editor/appearance/gutters/highlight_type_safe_lines>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/search\_result\_border\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/search_result_border_color>`

The script editor's color for the border of search results. This border
helps bring further attention to the search result. Set this color's
opacity to 0 to disable the border.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/search\_result\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/search_result_color>`

The script editor's background color for search results.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/selection\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/selection_color>`

The script editor's background color for the currently selected text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **text\_editor/theme/highlighting/string\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/string_color>`

The script editor's color for strings (single-line and multi-line).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **text\_editor/theme/highlighting/symbol\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/symbol_color>`

The script editor's color for operators (`( ) [ ] { } + - * /`, ...).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **text\_editor/theme/highlighting/text\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/text_color>`

The script editor's color for text not highlighted by any syntax
highlighting rule.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/text\_selected\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/text_selected_color>`

The script editor's background color for text. This should be set to a
translucent color so that it can display on top of other line color
modifiers such as
`text_editor/theme/highlighting/current_line_color<class_EditorSettings_property_text_editor/theme/highlighting/current_line_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/user\_type\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/user_type_color>`

The script editor's color for user-defined types (using `class_name`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>`
**text\_editor/theme/highlighting/word\_highlighted\_color**
`🔗<class_EditorSettings_property_text_editor/theme/highlighting/word_highlighted_color>`

The script editor's color for words highlighted by selecting them. Only
visible if
`text_editor/appearance/caret/highlight_all_occurrences<class_EditorSettings_property_text_editor/appearance/caret/highlight_all_occurrences>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **text\_editor/theme/line\_spacing**
`🔗<class_EditorSettings_property_text_editor/theme/line_spacing>`

The vertical line separation used in text editors, in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **version\_control/ssh\_private\_key\_path**
`🔗<class_EditorSettings_property_version_control/ssh_private_key_path>`

Path to private SSH key file for the editor's Version Control
integration credentials.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **version\_control/ssh\_public\_key\_path**
`🔗<class_EditorSettings_property_version_control/ssh_public_key_path>`

Path to public SSH key file for the editor's Version Control integration
credentials.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **version\_control/username**
`🔗<class_EditorSettings_property_version_control/username>`

Default username for editor's Version Control integration.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_property\_info**(info:
`Dictionary<class_Dictionary>`)
`🔗<class_EditorSettings_method_add_property_info>`

Adds a custom property info to a property. The dictionary must contain:

-   `name`: `String<class_String>` (the name of the property)
-   `type`: `int<class_int>` (see
    `Variant.Type<enum_@GlobalScope_Variant.Type>`)
-   optionally `hint`: `int<class_int>` (see
    `PropertyHint<enum_@GlobalScope_PropertyHint>`) and `hint_string`:
    `String<class_String>`

gdscript

var settings = EditorInterface.get\_editor\_settings()
settings.set("category/property\_name", 0)

var property\_info = {  
"name": "category/property\_name", "type": TYPE\_INT, "hint":
PROPERTY\_HINT\_ENUM, "hint\_string": "one,two,three"

}

settings.add\_property\_info(property\_info)

csharp

var settings = GetEditorInterface().GetEditorSettings();
settings.Set("category/property\_name", 0);

var propertyInfo = new Godot.Collections.Dictionary { {"name",
"category/propertyName"}, {"type", Variant.Type.Int}, {"hint",
PropertyHint.Enum}, {"hint\_string", "one,two,three"} };

settings.AddPropertyInfo(propertyInfo);

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**check\_changed\_settings\_in\_group**(setting\_prefix:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSettings_method_check_changed_settings_in_group>`

Checks if any settings with the prefix `setting_prefix` exist in the set
of changed settings. See also
`get_changed_settings<class_EditorSettings_method_get_changed_settings>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase**(property: `String<class_String>`)
`🔗<class_EditorSettings_method_erase>`

Erases the setting whose name is specified by `property`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_changed\_settings**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSettings_method_get_changed_settings>`

Gets an array of the settings which have been changed since the last
save. Note that internally `changed_settings` is cleared after a
successful save, so generally the most appropriate place to use this
method is when processing
`NOTIFICATION_EDITOR_SETTINGS_CHANGED<class_EditorSettings_constant_NOTIFICATION_EDITOR_SETTINGS_CHANGED>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_favorites**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSettings_method_get_favorites>`

Returns the list of favorite files and directories for this project.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_project\_metadata**(section:
`String<class_String>`, key: `String<class_String>`, default:
`Variant<class_Variant>` = null)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSettings_method_get_project_metadata>`

Returns project-specific metadata for the `section` and `key` specified.
If the metadata doesn't exist, `default` will be returned instead. See
also
`set_project_metadata<class_EditorSettings_method_set_project_metadata>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_recent\_dirs**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSettings_method_get_recent_dirs>`

Returns the list of recently visited folders in the file dialog for this
project.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_setting**(name: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSettings_method_get_setting>`

Returns the value of the setting specified by `name`. This is equivalent
to using `Object.get<class_Object_method_get>` on the EditorSettings
instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_setting**(name: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSettings_method_has_setting>`

Returns `true` if the setting specified by `name` exists, `false`
otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **mark\_setting\_changed**(setting:
`String<class_String>`)
`🔗<class_EditorSettings_method_mark_setting_changed>`

Marks the passed editor setting as being changed, see
`get_changed_settings<class_EditorSettings_method_get_changed_settings>`.
Only settings which exist (see
`has_setting<class_EditorSettings_method_has_setting>`) will be
accepted.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_builtin\_action\_override**(name:
`String<class_String>`, actions\_list:
`Array<class_Array>`\[`InputEvent<class_InputEvent>`\])
`🔗<class_EditorSettings_method_set_builtin_action_override>`

Overrides the built-in editor action `name` with the input actions
defined in `actions_list`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_favorites**(dirs:
`PackedStringArray<class_PackedStringArray>`)
`🔗<class_EditorSettings_method_set_favorites>`

Sets the list of favorite files and directories for this project.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_initial\_value**(name:
`StringName<class_StringName>`, value: `Variant<class_Variant>`,
update\_current: `bool<class_bool>`)
`🔗<class_EditorSettings_method_set_initial_value>`

Sets the initial value of the setting specified by `name` to `value`.
This is used to provide a value for the Revert button in the Editor
Settings. If `update_current` is true, the current value of the setting
will be set to `value` as well.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_project\_metadata**(section:
`String<class_String>`, key: `String<class_String>`, data:
`Variant<class_Variant>`)
`🔗<class_EditorSettings_method_set_project_metadata>`

Sets project-specific metadata with the `section`, `key` and `data`
specified. This metadata is stored outside the project folder and
therefore won't be checked into version control. See also
`get_project_metadata<class_EditorSettings_method_get_project_metadata>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_recent\_dirs**(dirs:
`PackedStringArray<class_PackedStringArray>`)
`🔗<class_EditorSettings_method_set_recent_dirs>`

Sets the list of recently visited folders in the file dialog for this
project.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_setting**(name: `String<class_String>`,
value: `Variant<class_Variant>`)
`🔗<class_EditorSettings_method_set_setting>`

Sets the `value` of the setting specified by `name`. This is equivalent
to using `Object.set<class_Object_method_set>` on the EditorSettings
instance.
