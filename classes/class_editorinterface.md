github\_url  
hide

# EditorInterface

**Inherits:** `Object<class_Object>`

Godot editor's interface.

classref-introduction-group

## Description

**EditorInterface** gives you control over Godot editor's window. It
allows customizing the window, saving and (re-)loading scenes, rendering
mesh previews, inspecting and editing resources and objects, and
provides access to `EditorSettings<class_EditorSettings>`,
`EditorFileSystem<class_EditorFileSystem>`,
`EditorResourcePreview<class_EditorResourcePreview>`,
`ScriptEditor<class_ScriptEditor>`, the editor viewport, and information
about scenes.

\*\*Note:\*\* This class shouldn't be instantiated directly. Instead,
access the singleton directly by its name.

gdscript

var editor\_settings = EditorInterface.get\_editor\_settings()

csharp

// In C# you can access it via the static Singleton property.
EditorSettings settings = EditorInterface.Singleton.GetEditorSettings();

classref-reftable-group

## Properties

<table>
<tbody>
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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

## Property Descriptions

classref-property

`bool<class_bool>` **distraction\_free\_mode**
`🔗<class_EditorInterface_property_distraction_free_mode>`

classref-property-setget

-   `void (No return value.)` **set\_distraction\_free\_mode**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_distraction\_free\_mode\_enabled**()

If `true`, enables distraction-free mode which hides side docks to
increase the space available for the main view.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **movie\_maker\_enabled**
`🔗<class_EditorInterface_property_movie_maker_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_movie\_maker\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_movie\_maker\_enabled**()

If `true`, the Movie Maker mode is enabled in the editor. See
`MovieWriter<class_MovieWriter>` for more information.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **edit\_node**(node: `Node<class_Node>`)
`🔗<class_EditorInterface_method_edit_node>`

Edits the given `Node<class_Node>`. The node will be also selected if
it's inside the scene tree.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **edit\_resource**(resource:
`Resource<class_Resource>`)
`🔗<class_EditorInterface_method_edit_resource>`

Edits the given `Resource<class_Resource>`. If the resource is a
`Script<class_Script>` you can also edit it with
`edit_script<class_EditorInterface_method_edit_script>` to specify the
line and column position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **edit\_script**(script:
`Script<class_Script>`, line: `int<class_int>` = -1, column:
`int<class_int>` = 0, grab\_focus: `bool<class_bool>` = true)
`🔗<class_EditorInterface_method_edit_script>`

Edits the given `Script<class_Script>`. The line and column on which to
open the script can also be specified. The script will be open with the
user-configured editor for the script's language which may be an
external editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Control<class_Control>` **get\_base\_control**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_base_control>`

Returns the main container of Godot editor's window. For example, you
can use it to retrieve the size of the container and place your controls
accordingly.

\*\*Warning:\*\* Removing and freeing this node will render the editor
useless and may cause a crash.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorCommandPalette<class_EditorCommandPalette>`
**get\_command\_palette**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_command_palette>`

Returns the editor's `EditorCommandPalette<class_EditorCommandPalette>`
instance.

\*\*Warning:\*\* Removing and freeing this node will render a part of
the editor useless and may cause a crash.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_current\_directory**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_current_directory>`

Returns the current directory being viewed in the
`FileSystemDock<class_FileSystemDock>`. If a file is selected, its base
directory will be returned using
`String.get_base_dir<class_String_method_get_base_dir>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_current\_feature\_profile**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_current_feature_profile>`

Returns the name of the currently activated feature profile. If the
default profile is currently active, an empty string is returned
instead.

In order to get a reference to the
`EditorFeatureProfile<class_EditorFeatureProfile>`, you must load the
feature profile using
`EditorFeatureProfile.load_from_file<class_EditorFeatureProfile_method_load_from_file>`.

\*\*Note:\*\* Feature profiles created via the user interface are loaded
from the `feature_profiles` directory, as a file with the `.profile`
extension. The editor configuration folder can be found by using
`EditorPaths.get_config_dir<class_EditorPaths_method_get_config_dir>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_current\_path**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_current_path>`

Returns the current path being viewed in the
`FileSystemDock<class_FileSystemDock>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **get\_edited\_scene\_root**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_edited_scene_root>`

Returns the edited (current) scene's root `Node<class_Node>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`VBoxContainer<class_VBoxContainer>` **get\_editor\_main\_screen**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_editor_main_screen>`

Returns the editor control responsible for main screen plugins and
tools. Use it with plugins that implement
`EditorPlugin._has_main_screen<class_EditorPlugin_private_method__has_main_screen>`.

\*\*Note:\*\* This node is a `VBoxContainer<class_VBoxContainer>`, which
means that if you add a `Control<class_Control>` child to it, you need
to set the child's
`Control.size_flags_vertical<class_Control_property_size_flags_vertical>`
to `Control.SIZE_EXPAND_FILL<class_Control_constant_SIZE_EXPAND_FILL>`
to make it use the full available space.

\*\*Warning:\*\* Removing and freeing this node will render a part of
the editor useless and may cause a crash.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorPaths<class_EditorPaths>` **get\_editor\_paths**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_editor_paths>`

Returns the `EditorPaths<class_EditorPaths>` singleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_editor\_scale**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_editor_scale>`

Returns the actual scale of the editor UI (`1.0` being 100% scale). This
can be used to adjust position and dimensions of the UI added by
plugins.

\*\*Note:\*\* This value is set via the `interface/editor/display_scale`
and `interface/editor/custom_display_scale` editor settings. Editor must
be restarted for changes to be properly applied.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorSettings<class_EditorSettings>` **get\_editor\_settings**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_editor_settings>`

Returns the editor's `EditorSettings<class_EditorSettings>` instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Theme<class_Theme>` **get\_editor\_theme**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_editor_theme>`

Returns the editor's `Theme<class_Theme>`.

\*\*Note:\*\* When creating custom editor UI, prefer accessing theme
items directly from your GUI nodes using the `get_theme_*` methods.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorUndoRedoManager<class_EditorUndoRedoManager>`
**get\_editor\_undo\_redo**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_editor_undo_redo>`

Returns the editor's
`EditorUndoRedoManager<class_EditorUndoRedoManager>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`SubViewport<class_SubViewport>` **get\_editor\_viewport\_2d**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_editor_viewport_2d>`

Returns the 2D editor `SubViewport<class_SubViewport>`. It does not have
a camera. Instead, the view transforms are done directly and can be
accessed with
`Viewport.global_canvas_transform<class_Viewport_property_global_canvas_transform>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`SubViewport<class_SubViewport>` **get\_editor\_viewport\_3d**(idx:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_editor_viewport_3d>`

Returns the specified 3D editor `SubViewport<class_SubViewport>`, from
`0` to `3`. The viewport can be used to access the active editor cameras
with `Viewport.get_camera_3d<class_Viewport_method_get_camera_3d>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`FileSystemDock<class_FileSystemDock>` **get\_file\_system\_dock**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_file_system_dock>`

Returns the editor's `FileSystemDock<class_FileSystemDock>` instance.

\*\*Warning:\*\* Removing and freeing this node will render a part of
the editor useless and may cause a crash.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorInspector<class_EditorInspector>` **get\_inspector**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_inspector>`

Returns the editor's `EditorInspector<class_EditorInspector>` instance.

\*\*Warning:\*\* Removing and freeing this node will render a part of
the editor useless and may cause a crash.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_open\_scenes**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_open_scenes>`

Returns an `Array<class_Array>` with the file paths of the currently
opened scenes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_playing\_scene**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_playing_scene>`

Returns the name of the scene that is being played. If no scene is
currently being played, returns an empty string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorFileSystem<class_EditorFileSystem>`
**get\_resource\_filesystem**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_resource_filesystem>`

Returns the editor's `EditorFileSystem<class_EditorFileSystem>`
instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorResourcePreview<class_EditorResourcePreview>`
**get\_resource\_previewer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_resource_previewer>`

Returns the editor's
`EditorResourcePreview<class_EditorResourcePreview>` instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ScriptEditor<class_ScriptEditor>` **get\_script\_editor**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_script_editor>`

Returns the editor's `ScriptEditor<class_ScriptEditor>` instance.

\*\*Warning:\*\* Removing and freeing this node will render a part of
the editor useless and may cause a crash.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_selected\_paths**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_selected_paths>`

Returns an array containing the paths of the currently selected files
(and directories) in the `FileSystemDock<class_FileSystemDock>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorSelection<class_EditorSelection>` **get\_selection**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_get_selection>`

Returns the editor's `EditorSelection<class_EditorSelection>` instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **inspect\_object**(object:
`Object<class_Object>`, for\_property: `String<class_String>` = "",
inspector\_only: `bool<class_bool>` = false)
`🔗<class_EditorInterface_method_inspect_object>`

Shows the given property on the given `object` in the editor's Inspector
dock. If `inspector_only` is `true`, plugins will not attempt to edit
`object`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_multi\_window\_enabled**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_is_multi_window_enabled>`

Returns `true` if multiple window support is enabled in the editor.
Multiple window support is enabled if *all* of these statements are
true:

-   `EditorSettings.interface/multi_window/enable<class_EditorSettings_property_interface/multi_window/enable>`
    is `true`.
-   `EditorSettings.interface/editor/single_window_mode<class_EditorSettings_property_interface/editor/single_window_mode>`
    is `false`.
-   `Viewport.gui_embed_subwindows<class_Viewport_property_gui_embed_subwindows>`
    is `false`. This is forced to `true` on platforms that don't support
    multiple windows such as Web, or when the `--single-window`
    `command line argument <../tutorials/editor/command_line_tutorial>`
    is used.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_playing\_scene**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_is_playing_scene>`

Returns `true` if a scene is currently being played, `false` otherwise.
Paused scenes are considered as being played.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_plugin\_enabled**(plugin:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorInterface_method_is_plugin_enabled>`

Returns `true` if the specified `plugin` is enabled. The plugin name is
the same as its directory name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Texture2D<class_Texture2D>`\]
**make\_mesh\_previews**(meshes:
`Array<class_Array>`\[`Mesh<class_Mesh>`\], preview\_size:
`int<class_int>`) `🔗<class_EditorInterface_method_make_mesh_previews>`

Returns mesh previews rendered at the given size as an
`Array<class_Array>` of `Texture2D<class_Texture2D>`s.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **mark\_scene\_as\_unsaved**()
`🔗<class_EditorInterface_method_mark_scene_as_unsaved>`

Marks the current scene tab as unsaved.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **open\_scene\_from\_path**(scene\_filepath:
`String<class_String>`)
`🔗<class_EditorInterface_method_open_scene_from_path>`

Opens the scene at the given path.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play\_current\_scene**()
`🔗<class_EditorInterface_method_play_current_scene>`

Plays the currently active scene.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play\_custom\_scene**(scene\_filepath:
`String<class_String>`)
`🔗<class_EditorInterface_method_play_custom_scene>`

Plays the scene specified by its filepath.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play\_main\_scene**()
`🔗<class_EditorInterface_method_play_main_scene>`

Plays the main scene.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_dialog**(dialog:
`Window<class_Window>`, rect: `Rect2i<class_Rect2i>` = Rect2i(0, 0, 0,
0)) `🔗<class_EditorInterface_method_popup_dialog>`

Pops up the `dialog` in the editor UI with
`Window.popup_exclusive<class_Window_method_popup_exclusive>`. The
dialog must have no current parent, otherwise the method fails.

See also
`Window.set_unparent_when_invisible<class_Window_method_set_unparent_when_invisible>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_dialog\_centered**(dialog:
`Window<class_Window>`, minsize: `Vector2i<class_Vector2i>` =
Vector2i(0, 0)) `🔗<class_EditorInterface_method_popup_dialog_centered>`

Pops up the `dialog` in the editor UI with
`Window.popup_exclusive_centered<class_Window_method_popup_exclusive_centered>`.
The dialog must have no current parent, otherwise the method fails.

See also
`Window.set_unparent_when_invisible<class_Window_method_set_unparent_when_invisible>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_dialog\_centered\_clamped**(dialog:
`Window<class_Window>`, minsize: `Vector2i<class_Vector2i>` =
Vector2i(0, 0), fallback\_ratio: `float<class_float>` = 0.75)
`🔗<class_EditorInterface_method_popup_dialog_centered_clamped>`

Pops up the `dialog` in the editor UI with
`Window.popup_exclusive_centered_clamped<class_Window_method_popup_exclusive_centered_clamped>`.
The dialog must have no current parent, otherwise the method fails.

See also
`Window.set_unparent_when_invisible<class_Window_method_set_unparent_when_invisible>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_dialog\_centered\_ratio**(dialog:
`Window<class_Window>`, ratio: `float<class_float>` = 0.8)
`🔗<class_EditorInterface_method_popup_dialog_centered_ratio>`

Pops up the `dialog` in the editor UI with
`Window.popup_exclusive_centered_ratio<class_Window_method_popup_exclusive_centered_ratio>`.
The dialog must have no current parent, otherwise the method fails.

See also
`Window.set_unparent_when_invisible<class_Window_method_set_unparent_when_invisible>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_node\_selector**(callback:
`Callable<class_Callable>`, valid\_types:
`Array<class_Array>`\[`StringName<class_StringName>`\] = \[\],
current\_value: `Node<class_Node>` = null)
`🔗<class_EditorInterface_method_popup_node_selector>`

Pops up an editor dialog for selecting a `Node<class_Node>` from the
edited scene. The `callback` must take a single argument of type
`NodePath<class_NodePath>`. It is called on the selected
`NodePath<class_NodePath>` or the empty path `^""` if the dialog is
canceled. If `valid_types` is provided, the dialog will only show Nodes
that match one of the listed Node types. If `current_value` is provided,
the Node will be automatically selected in the tree, if it exists.

\*\*Example:\*\* Display the node selection dialog as soon as this node
is added to the tree for the first time:

    func _ready():
        if Engine.is_editor_hint():
            EditorInterface.popup_node_selector(_on_node_selected, ["Button"])

    func _on_node_selected(node_path):
        if node_path.is_empty():
            print("node selection canceled")
        else:
            print("selected ", node_path)

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_property\_selector**(object:
`Object<class_Object>`, callback: `Callable<class_Callable>`,
type\_filter: `PackedInt32Array<class_PackedInt32Array>` =
PackedInt32Array(), current\_value: `String<class_String>` = "")
`🔗<class_EditorInterface_method_popup_property_selector>`

Pops up an editor dialog for selecting properties from `object`. The
`callback` must take a single argument of type
`NodePath<class_NodePath>`. It is called on the selected property path
(see
`NodePath.get_as_property_path<class_NodePath_method_get_as_property_path>`)
or the empty path `^""` if the dialog is canceled. If `type_filter` is
provided, the dialog will only show properties that match one of the
listed `Variant.Type<enum_@GlobalScope_Variant.Type>` values. If
`current_value` is provided, the property will be selected automatically
in the property list, if it exists.

    func _ready():
        if Engine.is_editor_hint():
            EditorInterface.popup_property_selector(this, _on_property_selected, [TYPE_INT])

    func _on_property_selected(property_path):
        if property_path.is_empty():
            print("property selection canceled")
        else:
            print("selected ", property_path)

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_quick\_open**(callback:
`Callable<class_Callable>`, base\_types:
`Array<class_Array>`\[`StringName<class_StringName>`\] = \[\])
`🔗<class_EditorInterface_method_popup_quick_open>`

Pops up an editor dialog for quick selecting a resource file. The
`callback` must take a single argument of type `String<class_String>`
which will contain the path of the selected resource or be empty if the
dialog is canceled. If `base_types` is provided, the dialog will only
show resources that match these types. Only types deriving from
`Resource<class_Resource>` are supported.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reload\_scene\_from\_path**(scene\_filepath:
`String<class_String>`)
`🔗<class_EditorInterface_method_reload_scene_from_path>`

Reloads the scene at the given path.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **restart\_editor**(save: `bool<class_bool>` =
true) `🔗<class_EditorInterface_method_restart_editor>`

Restarts the editor. This closes the editor and then opens the same
project. If `save` is `true`, the project will be saved before
restarting.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **save\_all\_scenes**()
`🔗<class_EditorInterface_method_save_all_scenes>`

Saves all opened scenes in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **save\_scene**()
`🔗<class_EditorInterface_method_save_scene>`

Saves the currently active scene. Returns either
`@GlobalScope.OK<class_@GlobalScope_constant_OK>` or
`@GlobalScope.ERR_CANT_CREATE<class_@GlobalScope_constant_ERR_CANT_CREATE>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **save\_scene\_as**(path:
`String<class_String>`, with\_preview: `bool<class_bool>` = true)
`🔗<class_EditorInterface_method_save_scene_as>`

Saves the currently active scene as a file at `path`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **select\_file**(file: `String<class_String>`)
`🔗<class_EditorInterface_method_select_file>`

Selects the file, with the path provided by `file`, in the FileSystem
dock.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_current\_feature\_profile**(profile\_name:
`String<class_String>`)
`🔗<class_EditorInterface_method_set_current_feature_profile>`

Selects and activates the specified feature profile with the given
`profile_name`. Set `profile_name` to an empty string to reset to the
default feature profile.

A feature profile can be created programmatically using the
`EditorFeatureProfile<class_EditorFeatureProfile>` class.

\*\*Note:\*\* The feature profile that gets activated must be located in
the `feature_profiles` directory, as a file with the `.profile`
extension. If a profile could not be found, an error occurs. The editor
configuration folder can be found by using
`EditorPaths.get_config_dir<class_EditorPaths_method_get_config_dir>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_main\_screen\_editor**(name:
`String<class_String>`)
`🔗<class_EditorInterface_method_set_main_screen_editor>`

Sets the editor's current main screen to the one specified in `name`.
`name` must match the title of the tab in question exactly (e.g. `2D`,
`3D`, `Script`, or `AssetLib` for default tabs).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_plugin\_enabled**(plugin:
`String<class_String>`, enabled: `bool<class_bool>`)
`🔗<class_EditorInterface_method_set_plugin_enabled>`

Sets the enabled status of a plugin. The plugin name is the same as its
directory name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop\_playing\_scene**()
`🔗<class_EditorInterface_method_stop_playing_scene>`

Stops the scene that is currently playing.
