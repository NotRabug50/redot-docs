github\_url  
hide

# EditorPlugin

**Inherits:** `Node<class_Node>` **&lt;** `Object<class_Object>`

Used by the editor to extend its functionality.

classref-introduction-group

## Description

Plugins are used by the editor to extend functionality. The most common
types of plugins are those which edit a given node or resource type,
import plugins and export plugins. See also
`EditorScript<class_EditorScript>` to add functions to the editor.

\*\*Note:\*\* Some names in this class contain "left" or "right" (e.g.
`DOCK_SLOT_LEFT_UL<class_EditorPlugin_constant_DOCK_SLOT_LEFT_UL>`).
These APIs assume left-to-right layout, and would be backwards when
using right-to-left layout. These names are kept for compatibility
reasons.

classref-introduction-group

## Tutorials

-   `Editor plugins documentation index <../tutorials/plugins/editor/index>`

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

**main\_screen\_changed**(screen\_name: `String<class_String>`)
`🔗<class_EditorPlugin_signal_main_screen_changed>`

Emitted when user changes the workspace (**2D**, **3D**, **Script**,
**AssetLib**). Also works with custom screens defined by plugins.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**project\_settings\_changed**()
`🔗<class_EditorPlugin_signal_project_settings_changed>`

**Deprecated:** Use
`ProjectSettings.settings_changed<class_ProjectSettings_signal_settings_changed>`
instead.

Emitted when any project setting has changed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**resource\_saved**(resource: `Resource<class_Resource>`)
`🔗<class_EditorPlugin_signal_resource_saved>`

Emitted when the given `resource` was saved on disc. See also
`scene_saved<class_EditorPlugin_signal_scene_saved>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**scene\_changed**(scene\_root: `Node<class_Node>`)
`🔗<class_EditorPlugin_signal_scene_changed>`

Emitted when the scene is changed in the editor. The argument will
return the root node of the scene that has just become active. If this
scene is new and empty, the argument will be `null`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**scene\_closed**(filepath: `String<class_String>`)
`🔗<class_EditorPlugin_signal_scene_closed>`

Emitted when user closes a scene. The argument is a file path to the
closed scene.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**scene\_saved**(filepath: `String<class_String>`)
`🔗<class_EditorPlugin_signal_scene_saved>`

Emitted when a scene was saved on disc. The argument is a file path to
the saved scene. See also
`resource_saved<class_EditorPlugin_signal_resource_saved>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **CustomControlContainer**:
`🔗<enum_EditorPlugin_CustomControlContainer>`

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_TOOLBAR** = `0`

Main editor toolbar, next to play buttons.

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_SPATIAL\_EDITOR\_MENU** = `1`

The toolbar that appears when 3D editor is active.

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_SPATIAL\_EDITOR\_SIDE\_LEFT** = `2`

Left sidebar of the 3D editor.

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_SPATIAL\_EDITOR\_SIDE\_RIGHT** = `3`

Right sidebar of the 3D editor.

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_SPATIAL\_EDITOR\_BOTTOM** = `4`

Bottom panel of the 3D editor.

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_CANVAS\_EDITOR\_MENU** = `5`

The toolbar that appears when 2D editor is active.

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_CANVAS\_EDITOR\_SIDE\_LEFT** = `6`

Left sidebar of the 2D editor.

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_CANVAS\_EDITOR\_SIDE\_RIGHT** = `7`

Right sidebar of the 2D editor.

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_CANVAS\_EDITOR\_BOTTOM** = `8`

Bottom panel of the 2D editor.

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_INSPECTOR\_BOTTOM** = `9`

Bottom section of the inspector.

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_PROJECT\_SETTING\_TAB\_LEFT** = `10`

Tab of Project Settings dialog, to the left of other tabs.

classref-enumeration-constant

`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`
**CONTAINER\_PROJECT\_SETTING\_TAB\_RIGHT** = `11`

Tab of Project Settings dialog, to the right of other tabs.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DockSlot**: `🔗<enum_EditorPlugin_DockSlot>`

classref-enumeration-constant

`DockSlot<enum_EditorPlugin_DockSlot>` **DOCK\_SLOT\_LEFT\_UL** = `0`

Dock slot, left side, upper-left (empty in default layout).

classref-enumeration-constant

`DockSlot<enum_EditorPlugin_DockSlot>` **DOCK\_SLOT\_LEFT\_BL** = `1`

Dock slot, left side, bottom-left (empty in default layout).

classref-enumeration-constant

`DockSlot<enum_EditorPlugin_DockSlot>` **DOCK\_SLOT\_LEFT\_UR** = `2`

Dock slot, left side, upper-right (in default layout includes Scene and
Import docks).

classref-enumeration-constant

`DockSlot<enum_EditorPlugin_DockSlot>` **DOCK\_SLOT\_LEFT\_BR** = `3`

Dock slot, left side, bottom-right (in default layout includes
FileSystem dock).

classref-enumeration-constant

`DockSlot<enum_EditorPlugin_DockSlot>` **DOCK\_SLOT\_RIGHT\_UL** = `4`

Dock slot, right side, upper-left (in default layout includes Inspector,
Node, and History docks).

classref-enumeration-constant

`DockSlot<enum_EditorPlugin_DockSlot>` **DOCK\_SLOT\_RIGHT\_BL** = `5`

Dock slot, right side, bottom-left (empty in default layout).

classref-enumeration-constant

`DockSlot<enum_EditorPlugin_DockSlot>` **DOCK\_SLOT\_RIGHT\_UR** = `6`

Dock slot, right side, upper-right (empty in default layout).

classref-enumeration-constant

`DockSlot<enum_EditorPlugin_DockSlot>` **DOCK\_SLOT\_RIGHT\_BR** = `7`

Dock slot, right side, bottom-right (empty in default layout).

classref-enumeration-constant

`DockSlot<enum_EditorPlugin_DockSlot>` **DOCK\_SLOT\_MAX** = `8`

Represents the size of the `DockSlot<enum_EditorPlugin_DockSlot>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AfterGUIInput**: `🔗<enum_EditorPlugin_AfterGUIInput>`

classref-enumeration-constant

`AfterGUIInput<enum_EditorPlugin_AfterGUIInput>`
**AFTER\_GUI\_INPUT\_PASS** = `0`

Forwards the `InputEvent<class_InputEvent>` to other EditorPlugins.

classref-enumeration-constant

`AfterGUIInput<enum_EditorPlugin_AfterGUIInput>`
**AFTER\_GUI\_INPUT\_STOP** = `1`

Prevents the `InputEvent<class_InputEvent>` from reaching other Editor
classes.

classref-enumeration-constant

`AfterGUIInput<enum_EditorPlugin_AfterGUIInput>`
**AFTER\_GUI\_INPUT\_CUSTOM** = `2`

Pass the `InputEvent<class_InputEvent>` to other editor plugins except
the main `Node3D<class_Node3D>` one. This can be used to prevent node
selection changes and work with sub-gizmos instead.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_apply\_changes**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__apply_changes>`

This method is called when the editor is about to save the project,
switch to another tab, etc. It asks the plugin to apply any pending
state changes to ensure consistency.

This is used, for example, in shader editors to let the plugin know that
it must apply the shader code being written by the user to the object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_build**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__build>`

This method is called when the editor is about to run the project. The
plugin can then perform required operations before the project runs.

This method must return a boolean. If this method returns `false`, the
project will not run. The run is aborted immediately, so this also
prevents all other plugins'
`_build<class_EditorPlugin_private_method__build>` methods from running.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_clear**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__clear>`

Clear all the state and reset the object being edited to zero. This
ensures your plugin does not keep editing a currently existing node, or
a node from the wrong scene.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_disable\_plugin**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__disable_plugin>`

Called by the engine when the user disables the **EditorPlugin** in the
Plugin tab of the project settings window.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_edit**(object: `Object<class_Object>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__edit>`

This function is used for plugins that edit specific object types (nodes
or resources). It requests the editor to edit the given object.

`object` can be `null` if the plugin was editing an object, but there is
no longer any selected object handled by this plugin. It can be used to
cleanup editing state.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_enable\_plugin**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__enable_plugin>`

Called by the engine when the user enables the **EditorPlugin** in the
Plugin tab of the project settings window.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_forward\_3d\_draw\_over\_viewport**(viewport\_control:
`Control<class_Control>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__forward_3d_draw_over_viewport>`

Called by the engine when the 3D editor's viewport is updated. Use the
`overlay` `Control<class_Control>` for drawing. You can update the
viewport manually by calling
`update_overlays<class_EditorPlugin_method_update_overlays>`.

gdscript

func \_forward\_3d\_draw\_over\_viewport(overlay):  
\# Draw a circle at cursor position.
overlay.draw\_circle(overlay.get\_local\_mouse\_position(), 64,
Color.WHITE)

func \_forward\_3d\_gui\_input(camera, event):  
if event is InputEventMouseMotion:  
\# Redraw viewport when cursor is moved. update\_overlays() return
EditorPlugin.AFTER\_GUI\_INPUT\_STOP

return EditorPlugin.AFTER\_GUI\_INPUT\_PASS

csharp

public override void \_Forward3DDrawOverViewport(Control
viewportControl) { // Draw a circle at cursor position.
viewportControl.DrawCircle(viewportControl.GetLocalMousePosition(), 64,
Colors.White); }

public override EditorPlugin.AfterGuiInput \_Forward3DGuiInput(Camera3D
viewportCamera, InputEvent @event) { if (@event is
InputEventMouseMotion) { // Redraw viewport when cursor is moved.
UpdateOverlays(); return EditorPlugin.AfterGuiInput.Stop; } return
EditorPlugin.AfterGuiInput.Pass; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_forward\_3d\_force\_draw\_over\_viewport**(viewport\_control:
`Control<class_Control>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__forward_3d_force_draw_over_viewport>`

This method is the same as
`_forward_3d_draw_over_viewport<class_EditorPlugin_private_method__forward_3d_draw_over_viewport>`,
except it draws on top of everything. Useful when you need an extra
layer that shows over anything else.

You need to enable calling of this method by using
`set_force_draw_over_forwarding_enabled<class_EditorPlugin_method_set_force_draw_over_forwarding_enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_forward\_3d\_gui\_input**(viewport\_camera:
`Camera3D<class_Camera3D>`, event: `InputEvent<class_InputEvent>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__forward_3d_gui_input>`

Called when there is a root node in the current edited scene,
`_handles<class_EditorPlugin_private_method__handles>` is implemented,
and an `InputEvent<class_InputEvent>` happens in the 3D viewport. The
return value decides whether the `InputEvent<class_InputEvent>` is
consumed or forwarded to other **EditorPlugin**s. See
`AfterGUIInput<enum_EditorPlugin_AfterGUIInput>` for options.

gdscript

\# Prevents the InputEvent from reaching other Editor classes. func
\_forward\_3d\_gui\_input(camera, event): return
EditorPlugin.AFTER\_GUI\_INPUT\_STOP

csharp

// Prevents the InputEvent from reaching other Editor classes. public
override EditorPlugin.AfterGuiInput \_Forward3DGuiInput(Camera3D camera,
InputEvent @event) { return EditorPlugin.AfterGuiInput.Stop; }

This method must return
`AFTER_GUI_INPUT_PASS<class_EditorPlugin_constant_AFTER_GUI_INPUT_PASS>`
in order to forward the `InputEvent<class_InputEvent>` to other Editor
classes.

gdscript

\# Consumes InputEventMouseMotion and forwards other InputEvent types.
func \_forward\_3d\_gui\_input(camera, event): return
EditorPlugin.AFTER\_GUI\_INPUT\_STOP if event is InputEventMouseMotion
else EditorPlugin.AFTER\_GUI\_INPUT\_PASS

csharp

// Consumes InputEventMouseMotion and forwards other InputEvent types.
public override EditorPlugin.AfterGuiInput \_Forward3DGuiInput(Camera3D
camera, InputEvent @event) { return @event is InputEventMouseMotion ?
EditorPlugin.AfterGuiInput.Stop : EditorPlugin.AfterGuiInput.Pass; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_forward\_canvas\_draw\_over\_viewport**(viewport\_control:
`Control<class_Control>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__forward_canvas_draw_over_viewport>`

Called by the engine when the 2D editor's viewport is updated. Use the
`overlay` `Control<class_Control>` for drawing. You can update the
viewport manually by calling
`update_overlays<class_EditorPlugin_method_update_overlays>`.

gdscript

func \_forward\_canvas\_draw\_over\_viewport(overlay):  
\# Draw a circle at cursor position.
overlay.draw\_circle(overlay.get\_local\_mouse\_position(), 64,
Color.WHITE)

func \_forward\_canvas\_gui\_input(event):  
if event is InputEventMouseMotion:  
\# Redraw viewport when cursor is moved. update\_overlays() return true

return false

csharp

public override void \_ForwardCanvasDrawOverViewport(Control
viewportControl) { // Draw a circle at cursor position.
viewportControl.DrawCircle(viewportControl.GetLocalMousePosition(), 64,
Colors.White); }

public override bool \_ForwardCanvasGuiInput(InputEvent @event) { if
(@event is InputEventMouseMotion) { // Redraw viewport when cursor is
moved. UpdateOverlays(); return true; } return false; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_forward\_canvas\_force\_draw\_over\_viewport**(viewport\_control:
`Control<class_Control>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__forward_canvas_force_draw_over_viewport>`

This method is the same as
`_forward_canvas_draw_over_viewport<class_EditorPlugin_private_method__forward_canvas_draw_over_viewport>`,
except it draws on top of everything. Useful when you need an extra
layer that shows over anything else.

You need to enable calling of this method by using
`set_force_draw_over_forwarding_enabled<class_EditorPlugin_method_set_force_draw_over_forwarding_enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_forward\_canvas\_gui\_input**(event:
`InputEvent<class_InputEvent>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__forward_canvas_gui_input>`

Called when there is a root node in the current edited scene,
`_handles<class_EditorPlugin_private_method__handles>` is implemented,
and an `InputEvent<class_InputEvent>` happens in the 2D viewport. If
this method returns `true`, `event` is intercepted by this
**EditorPlugin**, otherwise `event` is forwarded to other Editor
classes.

gdscript

\# Prevents the InputEvent from reaching other Editor classes. func
\_forward\_canvas\_gui\_input(event): return true

csharp

// Prevents the InputEvent from reaching other Editor classes. public
override bool ForwardCanvasGuiInput(InputEvent @event) { return true; }

This method must return `false` in order to forward the
`InputEvent<class_InputEvent>` to other Editor classes.

gdscript

\# Consumes InputEventMouseMotion and forwards other InputEvent types.
func \_forward\_canvas\_gui\_input(event): if (event is
InputEventMouseMotion): return true return false

csharp

// Consumes InputEventMouseMotion and forwards other InputEvent types.
public override bool \_ForwardCanvasGuiInput(InputEvent @event) { if
(@event is InputEventMouseMotion) { return true; } return false; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **\_get\_breakpoints**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPlugin_private_method__get_breakpoints>`

This is for editors that edit script-based objects. You can return a
list of breakpoints in the format (`script:line`), for example:
`res://path_to_script.gd:25`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **\_get\_plugin\_icon**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPlugin_private_method__get_plugin_icon>`

Override this method in your plugin to return a
`Texture2D<class_Texture2D>` in order to give it an icon.

For main screen plugins, this appears at the top of the screen, to the
right of the "2D", "3D", "Script", and "AssetLib" buttons.

Ideally, the plugin icon should be white with a transparent background
and 16×16 pixels in size.

gdscript

func \_get\_plugin\_icon():  
\# You can use a custom icon: return
preload("<res://addons/my_plugin/my_plugin_icon.svg>") \# Or use a
built-in icon: return
EditorInterface.get\_editor\_theme().get\_icon("Node", "EditorIcons")

csharp

public override Texture2D \_GetPluginIcon() { // You can use a custom
icon: return
ResourceLoader.Load&lt;Texture2D&gt;("<res://addons/my_plugin/my_plugin_icon.svg>");
// Or use a built-in icon: return
EditorInterface.Singleton.GetEditorTheme().GetIcon("Node",
"EditorIcons"); }

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_plugin\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPlugin_private_method__get_plugin_name>`

Override this method in your plugin to provide the name of the plugin
when displayed in the Godot editor.

For main screen plugins, this appears at the top of the screen, to the
right of the "2D", "3D", "Script", and "AssetLib" buttons.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **\_get\_state**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPlugin_private_method__get_state>`

Override this method to provide a state data you want to be saved, like
view position, grid settings, folding, etc. This is used when saving the
scene (so state is kept when opening it again) and for switching tabs
(so state can be restored when the tab returns). This data is
automatically saved for each scene in an `editstate` file in the editor
metadata folder. If you want to store global (scene-independent) editor
data for your plugin, you can use
`_get_window_layout<class_EditorPlugin_private_method__get_window_layout>`
instead.

Use `_set_state<class_EditorPlugin_private_method__set_state>` to
restore your saved state.

\*\*Note:\*\* This method should not be used to save important settings
that should persist with the project.

\*\*Note:\*\* You must implement
`_get_plugin_name<class_EditorPlugin_private_method__get_plugin_name>`
for the state to be stored and restored correctly.

    func _get_state():
        var state = {"zoom": zoom, "preferred_color": my_color}
        return state

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_unsaved\_status**(for\_scene:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPlugin_private_method__get_unsaved_status>`

Override this method to provide a custom message that lists unsaved
changes. The editor will call this method when exiting or when closing a
scene, and display the returned string in a confirmation dialog. Return
empty string if the plugin has no unsaved changes.

When closing a scene, `for_scene` is the path to the scene being closed.
You can use it to handle built-in resources in that scene.

If the user confirms saving,
`_save_external_data<class_EditorPlugin_private_method__save_external_data>`
will be called, before closing the editor.

    func _get_unsaved_status(for_scene):
        if not unsaved:
            return ""

        if for_scene.is_empty():
            return "Save changes in MyCustomPlugin before closing?"
        else:
            return "Scene %s has changes from MyCustomPlugin. Save before closing?" % for_scene.get_file()

    func _save_external_data():
        unsaved = false

If the plugin has no scene-specific changes, you can ignore the calls
when closing scenes:

    func _get_unsaved_status(for_scene):
        if not for_scene.is_empty():
            return ""

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_get\_window\_layout**(configuration:
`ConfigFile<class_ConfigFile>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__get_window_layout>`

Override this method to provide the GUI layout of the plugin or any
other data you want to be stored. This is used to save the project's
editor layout when
`queue_save_layout<class_EditorPlugin_method_queue_save_layout>` is
called or the editor layout was changed (for example changing the
position of a dock). The data is stored in the `editor_layout.cfg` file
in the editor metadata directory.

Use
`_set_window_layout<class_EditorPlugin_private_method__set_window_layout>`
to restore your saved layout.

    func _get_window_layout(configuration):
        configuration.set_value("MyPlugin", "window_position", $Window.position)
        configuration.set_value("MyPlugin", "icon_color", $Icon.modulate)

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_handles**(object: `Object<class_Object>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPlugin_private_method__handles>`

Implement this function if your plugin edits a specific type of object
(Resource or Node). If you return `true`, then you will get the
functions `_edit<class_EditorPlugin_private_method__edit>` and
`_make_visible<class_EditorPlugin_private_method__make_visible>` called
when the editor requests them. If you have declared the methods
`_forward_canvas_gui_input<class_EditorPlugin_private_method__forward_canvas_gui_input>`
and
`_forward_3d_gui_input<class_EditorPlugin_private_method__forward_3d_gui_input>`
these will be called too.

\*\*Note:\*\* Each plugin should handle only one type of objects at a
time. If a plugin handles more types of objects and they are edited at
the same time, it will result in errors.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_has\_main\_screen**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPlugin_private_method__has_main_screen>`

Returns `true` if this is a main screen editor plugin (it goes in the
workspace selector together with **2D**, **3D**, **Script** and
**AssetLib**).

When the plugin's workspace is selected, other main screen plugins will
be hidden, but your plugin will not appear automatically. It needs to be
added as a child of
`EditorInterface.get_editor_main_screen<class_EditorInterface_method_get_editor_main_screen>`
and made visible inside
`_make_visible<class_EditorPlugin_private_method__make_visible>`.

Use
`_get_plugin_name<class_EditorPlugin_private_method__get_plugin_name>`
and
`_get_plugin_icon<class_EditorPlugin_private_method__get_plugin_icon>`
to customize the plugin button's appearance.

    var plugin_control

    func _enter_tree():
        plugin_control = preload("my_plugin_control.tscn").instantiate()
        EditorInterface.get_editor_main_screen().add_child(plugin_control)
        plugin_control.hide()

    func _has_main_screen():
        return true

    func _make_visible(visible):
        plugin_control.visible = visible

    func _get_plugin_name():
        return "My Super Cool Plugin 3000"

    func _get_plugin_icon():
        return EditorInterface.get_editor_theme().get_icon("Node", "EditorIcons")

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_make\_visible**(visible:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__make_visible>`

This function will be called when the editor is requested to become
visible. It is used for plugins that edit a specific object type.

Remember that you have to manage the visibility of all your editor
controls manually.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_save\_external\_data**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__save_external_data>`

This method is called after the editor saves the project or when it's
closed. It asks the plugin to save edited external scenes/resources.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_set\_state**(state:
`Dictionary<class_Dictionary>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__set_state>`

Restore the state saved by
`_get_state<class_EditorPlugin_private_method__get_state>`. This method
is called when the current scene tab is changed in the editor.

\*\*Note:\*\* Your plugin must implement
`_get_plugin_name<class_EditorPlugin_private_method__get_plugin_name>`,
otherwise it will not be recognized and this method will not be called.

    func _set_state(data):
        zoom = data.get("zoom", 1.0)
        preferred_color = data.get("my_color", Color.WHITE)

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_set\_window\_layout**(configuration:
`ConfigFile<class_ConfigFile>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorPlugin_private_method__set_window_layout>`

Restore the plugin GUI layout and data saved by
`_get_window_layout<class_EditorPlugin_private_method__get_window_layout>`.
This method is called for every plugin on editor startup. Use the
provided `configuration` file to read your saved data.

    func _set_window_layout(configuration):
        $Window.position = configuration.get_value("MyPlugin", "window_position", Vector2())
        $Icon.modulate = configuration.get_value("MyPlugin", "icon_color", Color.WHITE)

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_autoload\_singleton**(name:
`String<class_String>`, path: `String<class_String>`)
`🔗<class_EditorPlugin_method_add_autoload_singleton>`

Adds a script at `path` to the Autoload list as `name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_context\_menu\_plugin**(slot:
`ContextMenuSlot<enum_EditorContextMenuPlugin_ContextMenuSlot>`, plugin:
`EditorContextMenuPlugin<class_EditorContextMenuPlugin>`)
`🔗<class_EditorPlugin_method_add_context_menu_plugin>`

Adds a plugin to the context menu. `slot` is the context menu where the
plugin will be added.

See `ContextMenuSlot<enum_EditorContextMenuPlugin_ContextMenuSlot>` for
available context menus. A plugin instance can belong only to a single
context menu slot.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Button<class_Button>` **add\_control\_to\_bottom\_panel**(control:
`Control<class_Control>`, title: `String<class_String>`, shortcut:
`Shortcut<class_Shortcut>` = null)
`🔗<class_EditorPlugin_method_add_control_to_bottom_panel>`

Adds a control to the bottom panel (together with Output, Debug,
Animation, etc). Returns a reference to the button added. It's up to you
to hide/show the button when needed. When your plugin is deactivated,
make sure to remove your custom control with
`remove_control_from_bottom_panel<class_EditorPlugin_method_remove_control_from_bottom_panel>`
and free it with `Node.queue_free<class_Node_method_queue_free>`.

Optionally, you can specify a shortcut parameter. When pressed, this
shortcut will toggle the bottom panel's visibility. See the default
editor bottom panel shortcuts in the Editor Settings for inspiration.
Per convention, they all use `Alt` modifier.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_control\_to\_container**(container:
`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`,
control: `Control<class_Control>`)
`🔗<class_EditorPlugin_method_add_control_to_container>`

Adds a custom control to a container (see
`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`).
There are many locations where custom controls can be added in the
editor UI.

Please remember that you have to manage the visibility of your custom
controls yourself (and likely hide it after adding it).

When your plugin is deactivated, make sure to remove your custom control
with
`remove_control_from_container<class_EditorPlugin_method_remove_control_from_container>`
and free it with `Node.queue_free<class_Node_method_queue_free>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_control\_to\_dock**(slot:
`DockSlot<enum_EditorPlugin_DockSlot>`, control:
`Control<class_Control>`, shortcut: `Shortcut<class_Shortcut>` = null)
`🔗<class_EditorPlugin_method_add_control_to_dock>`

Adds the control to a specific dock slot (see
`DockSlot<enum_EditorPlugin_DockSlot>` for options).

If the dock is repositioned and as long as the plugin is active, the
editor will save the dock position on further sessions.

When your plugin is deactivated, make sure to remove your custom control
with
`remove_control_from_docks<class_EditorPlugin_method_remove_control_from_docks>`
and free it with `Node.queue_free<class_Node_method_queue_free>`.

Optionally, you can specify a shortcut parameter. When pressed, this
shortcut will toggle the dock's visibility once it's moved to the bottom
panel (this shortcut does not affect the dock otherwise). See the
default editor bottom panel shortcuts in the Editor Settings for
inspiration. Per convention, they all use `Alt` modifier.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_custom\_type**(type:
`String<class_String>`, base: `String<class_String>`, script:
`Script<class_Script>`, icon: `Texture2D<class_Texture2D>`)
`🔗<class_EditorPlugin_method_add_custom_type>`

Adds a custom type, which will appear in the list of nodes or resources.

When a given node or resource is selected, the base type will be
instantiated (e.g. "Node3D", "Control", "Resource"), then the script
will be loaded and set to this object.

\*\*Note:\*\* The base type is the base engine class which this type's
class hierarchy inherits, not any custom type parent classes.

You can use the virtual method
`_handles<class_EditorPlugin_private_method__handles>` to check if your
custom object is being edited by checking the script or using the `is`
keyword.

During run-time, this will be a simple object with a script so this
function does not need to be called then.

\*\*Note:\*\* Custom types added this way are not true classes. They are
just a helper to create a node with specific script.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_debugger\_plugin**(script:
`EditorDebuggerPlugin<class_EditorDebuggerPlugin>`)
`🔗<class_EditorPlugin_method_add_debugger_plugin>`

Adds a `Script<class_Script>` as debugger plugin to the Debugger. The
script must extend `EditorDebuggerPlugin<class_EditorDebuggerPlugin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_export\_platform**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`)
`🔗<class_EditorPlugin_method_add_export_platform>`

Registers a new `EditorExportPlatform<class_EditorExportPlatform>`.
Export platforms provides functionality of exporting to the specific
platform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_export\_plugin**(plugin:
`EditorExportPlugin<class_EditorExportPlugin>`)
`🔗<class_EditorPlugin_method_add_export_plugin>`

Registers a new `EditorExportPlugin<class_EditorExportPlugin>`. Export
plugins are used to perform tasks when the project is being exported.

See
`add_inspector_plugin<class_EditorPlugin_method_add_inspector_plugin>`
for an example of how to register a plugin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_import\_plugin**(importer:
`EditorImportPlugin<class_EditorImportPlugin>`, first\_priority:
`bool<class_bool>` = false)
`🔗<class_EditorPlugin_method_add_import_plugin>`

Registers a new `EditorImportPlugin<class_EditorImportPlugin>`. Import
plugins are used to import custom and unsupported assets as a custom
`Resource<class_Resource>` type.

If `first_priority` is `true`, the new import plugin is inserted first
in the list and takes precedence over pre-existing plugins.

\*\*Note:\*\* If you want to import custom 3D asset formats use
`add_scene_format_importer_plugin<class_EditorPlugin_method_add_scene_format_importer_plugin>`
instead.

See
`add_inspector_plugin<class_EditorPlugin_method_add_inspector_plugin>`
for an example of how to register a plugin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_inspector\_plugin**(plugin:
`EditorInspectorPlugin<class_EditorInspectorPlugin>`)
`🔗<class_EditorPlugin_method_add_inspector_plugin>`

Registers a new `EditorInspectorPlugin<class_EditorInspectorPlugin>`.
Inspector plugins are used to extend
`EditorInspector<class_EditorInspector>` and provide custom
configuration tools for your object's properties.

\*\*Note:\*\* Always use
`remove_inspector_plugin<class_EditorPlugin_method_remove_inspector_plugin>`
to remove the registered
`EditorInspectorPlugin<class_EditorInspectorPlugin>` when your
**EditorPlugin** is disabled to prevent leaks and an unexpected
behavior.

gdscript

const MyInspectorPlugin =
preload("<res://addons/your_addon/path/to/your/script.gd>") var
inspector\_plugin = MyInspectorPlugin.new()

func \_enter\_tree():  
add\_inspector\_plugin(inspector\_plugin)

func \_exit\_tree():  
remove\_inspector\_plugin(inspector\_plugin)

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_node\_3d\_gizmo\_plugin**(plugin:
`EditorNode3DGizmoPlugin<class_EditorNode3DGizmoPlugin>`)
`🔗<class_EditorPlugin_method_add_node_3d_gizmo_plugin>`

Registers a new
`EditorNode3DGizmoPlugin<class_EditorNode3DGizmoPlugin>`. Gizmo plugins
are used to add custom gizmos to the 3D preview viewport for a
`Node3D<class_Node3D>`.

See
`add_inspector_plugin<class_EditorPlugin_method_add_inspector_plugin>`
for an example of how to register a plugin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_resource\_conversion\_plugin**(plugin:
`EditorResourceConversionPlugin<class_EditorResourceConversionPlugin>`)
`🔗<class_EditorPlugin_method_add_resource_conversion_plugin>`

Registers a new
`EditorResourceConversionPlugin<class_EditorResourceConversionPlugin>`.
Resource conversion plugins are used to add custom resource converters
to the editor inspector.

See
`EditorResourceConversionPlugin<class_EditorResourceConversionPlugin>`
for an example of how to create a resource conversion plugin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**add\_scene\_format\_importer\_plugin**(scene\_format\_importer:
`EditorSceneFormatImporter<class_EditorSceneFormatImporter>`,
first\_priority: `bool<class_bool>` = false)
`🔗<class_EditorPlugin_method_add_scene_format_importer_plugin>`

Registers a new
`EditorSceneFormatImporter<class_EditorSceneFormatImporter>`. Scene
importers are used to import custom 3D asset formats as scenes.

If `first_priority` is `true`, the new import plugin is inserted first
in the list and takes precedence over pre-existing plugins.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**add\_scene\_post\_import\_plugin**(scene\_import\_plugin:
`EditorScenePostImportPlugin<class_EditorScenePostImportPlugin>`,
first\_priority: `bool<class_bool>` = false)
`🔗<class_EditorPlugin_method_add_scene_post_import_plugin>`

Add a `EditorScenePostImportPlugin<class_EditorScenePostImportPlugin>`.
These plugins allow customizing the import process of 3D assets by
adding new options to the import dialogs.

If `first_priority` is `true`, the new import plugin is inserted first
in the list and takes precedence over pre-existing plugins.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_tool\_menu\_item**(name:
`String<class_String>`, callable: `Callable<class_Callable>`)
`🔗<class_EditorPlugin_method_add_tool_menu_item>`

Adds a custom menu item to **Project &gt; Tools** named `name`. When
clicked, the provided `callable` will be called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_tool\_submenu\_item**(name:
`String<class_String>`, submenu: `PopupMenu<class_PopupMenu>`)
`🔗<class_EditorPlugin_method_add_tool_submenu_item>`

Adds a custom `PopupMenu<class_PopupMenu>` submenu under **Project &gt;
Tools &gt;** `name`. Use
`remove_tool_menu_item<class_EditorPlugin_method_remove_tool_menu_item>`
on plugin clean up to remove the menu.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_translation\_parser\_plugin**(parser:
`EditorTranslationParserPlugin<class_EditorTranslationParserPlugin>`)
`🔗<class_EditorPlugin_method_add_translation_parser_plugin>`

Registers a custom translation parser plugin for extracting translatable
strings from custom files.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**add\_undo\_redo\_inspector\_hook\_callback**(callable:
`Callable<class_Callable>`)
`🔗<class_EditorPlugin_method_add_undo_redo_inspector_hook_callback>`

Hooks a callback into the undo/redo action creation when a property is
modified in the inspector. This allows, for example, to save other
properties that may be lost when a given property is modified.

The callback should have 4 arguments: `Object<class_Object>`
`undo_redo`, `Object<class_Object>` `modified_object`,
`String<class_String>` `property` and `Variant<class_Variant>`
`new_value`. They are, respectively, the `UndoRedo<class_UndoRedo>`
object used by the inspector, the currently modified object, the name of
the modified property and the new value the property is about to take.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorInterface<class_EditorInterface>` **get\_editor\_interface**()
`🔗<class_EditorPlugin_method_get_editor_interface>`

**Deprecated:** `EditorInterface<class_EditorInterface>` is a global
singleton and can be accessed directly by its name.

Returns the `EditorInterface<class_EditorInterface>` singleton instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PopupMenu<class_PopupMenu>` **get\_export\_as\_menu**()
`🔗<class_EditorPlugin_method_get_export_as_menu>`

Returns the `PopupMenu<class_PopupMenu>` under **Scene &gt; Export
As...**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_plugin\_version**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPlugin_method_get_plugin_version>`

Provide the version of the plugin declared in the `plugin.cfg` config
file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ScriptCreateDialog<class_ScriptCreateDialog>`
**get\_script\_create\_dialog**()
`🔗<class_EditorPlugin_method_get_script_create_dialog>`

Gets the Editor's dialog used for making scripts.

\*\*Note:\*\* Users can configure it before use.

\*\*Warning:\*\* Removing and freeing this node will render a part of
the editor useless and may cause a crash.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorUndoRedoManager<class_EditorUndoRedoManager>`
**get\_undo\_redo**() `🔗<class_EditorPlugin_method_get_undo_redo>`

Gets the undo/redo object. Most actions in the editor can be undoable,
so use this object to make sure this happens when it's worth it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **hide\_bottom\_panel**()
`🔗<class_EditorPlugin_method_hide_bottom_panel>`

Minimizes the bottom panel.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **make\_bottom\_panel\_item\_visible**(item:
`Control<class_Control>`)
`🔗<class_EditorPlugin_method_make_bottom_panel_item_visible>`

Makes a specific item in the bottom panel visible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **queue\_save\_layout**()
`🔗<class_EditorPlugin_method_queue_save_layout>`

Queue save the project's editor layout.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_autoload\_singleton**(name:
`String<class_String>`)
`🔗<class_EditorPlugin_method_remove_autoload_singleton>`

Removes an Autoload `name` from the list.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_context\_menu\_plugin**(plugin:
`EditorContextMenuPlugin<class_EditorContextMenuPlugin>`)
`🔗<class_EditorPlugin_method_remove_context_menu_plugin>`

Removes the specified context menu plugin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_control\_from\_bottom\_panel**(control:
`Control<class_Control>`)
`🔗<class_EditorPlugin_method_remove_control_from_bottom_panel>`

Removes the control from the bottom panel. You have to manually
`Node.queue_free<class_Node_method_queue_free>` the control.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_control\_from\_container**(container:
`CustomControlContainer<enum_EditorPlugin_CustomControlContainer>`,
control: `Control<class_Control>`)
`🔗<class_EditorPlugin_method_remove_control_from_container>`

Removes the control from the specified container. You have to manually
`Node.queue_free<class_Node_method_queue_free>` the control.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_control\_from\_docks**(control:
`Control<class_Control>`)
`🔗<class_EditorPlugin_method_remove_control_from_docks>`

Removes the control from the dock. You have to manually
`Node.queue_free<class_Node_method_queue_free>` the control.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_custom\_type**(type:
`String<class_String>`)
`🔗<class_EditorPlugin_method_remove_custom_type>`

Removes a custom type added by
`add_custom_type<class_EditorPlugin_method_add_custom_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_debugger\_plugin**(script:
`EditorDebuggerPlugin<class_EditorDebuggerPlugin>`)
`🔗<class_EditorPlugin_method_remove_debugger_plugin>`

Removes the debugger plugin with given script from the Debugger.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_export\_platform**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`)
`🔗<class_EditorPlugin_method_remove_export_platform>`

Removes an export platform registered by
`add_export_platform<class_EditorPlugin_method_add_export_platform>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_export\_plugin**(plugin:
`EditorExportPlugin<class_EditorExportPlugin>`)
`🔗<class_EditorPlugin_method_remove_export_plugin>`

Removes an export plugin registered by
`add_export_plugin<class_EditorPlugin_method_add_export_plugin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_import\_plugin**(importer:
`EditorImportPlugin<class_EditorImportPlugin>`)
`🔗<class_EditorPlugin_method_remove_import_plugin>`

Removes an import plugin registered by
`add_import_plugin<class_EditorPlugin_method_add_import_plugin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_inspector\_plugin**(plugin:
`EditorInspectorPlugin<class_EditorInspectorPlugin>`)
`🔗<class_EditorPlugin_method_remove_inspector_plugin>`

Removes an inspector plugin registered by
`add_inspector_plugin<class_EditorPlugin_method_add_inspector_plugin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_node\_3d\_gizmo\_plugin**(plugin:
`EditorNode3DGizmoPlugin<class_EditorNode3DGizmoPlugin>`)
`🔗<class_EditorPlugin_method_remove_node_3d_gizmo_plugin>`

Removes a gizmo plugin registered by
`add_node_3d_gizmo_plugin<class_EditorPlugin_method_add_node_3d_gizmo_plugin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_resource\_conversion\_plugin**(plugin:
`EditorResourceConversionPlugin<class_EditorResourceConversionPlugin>`)
`🔗<class_EditorPlugin_method_remove_resource_conversion_plugin>`

Removes a resource conversion plugin registered by
`add_resource_conversion_plugin<class_EditorPlugin_method_add_resource_conversion_plugin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_scene\_format\_importer\_plugin**(scene\_format\_importer:
`EditorSceneFormatImporter<class_EditorSceneFormatImporter>`)
`🔗<class_EditorPlugin_method_remove_scene_format_importer_plugin>`

Removes a scene format importer registered by
`add_scene_format_importer_plugin<class_EditorPlugin_method_add_scene_format_importer_plugin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_scene\_post\_import\_plugin**(scene\_import\_plugin:
`EditorScenePostImportPlugin<class_EditorScenePostImportPlugin>`)
`🔗<class_EditorPlugin_method_remove_scene_post_import_plugin>`

Remove the
`EditorScenePostImportPlugin<class_EditorScenePostImportPlugin>`, added
with
`add_scene_post_import_plugin<class_EditorPlugin_method_add_scene_post_import_plugin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_tool\_menu\_item**(name:
`String<class_String>`)
`🔗<class_EditorPlugin_method_remove_tool_menu_item>`

Removes a menu `name` from **Project &gt; Tools**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_translation\_parser\_plugin**(parser:
`EditorTranslationParserPlugin<class_EditorTranslationParserPlugin>`)
`🔗<class_EditorPlugin_method_remove_translation_parser_plugin>`

Removes a custom translation parser plugin registered by
`add_translation_parser_plugin<class_EditorPlugin_method_add_translation_parser_plugin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_undo\_redo\_inspector\_hook\_callback**(callable:
`Callable<class_Callable>`)
`🔗<class_EditorPlugin_method_remove_undo_redo_inspector_hook_callback>`

Removes a callback previously added by
`add_undo_redo_inspector_hook_callback<class_EditorPlugin_method_add_undo_redo_inspector_hook_callback>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_dock\_tab\_icon**(control:
`Control<class_Control>`, icon: `Texture2D<class_Texture2D>`)
`🔗<class_EditorPlugin_method_set_dock_tab_icon>`

Sets the tab icon for the given control in a dock slot. Setting to
`null` removes the icon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_force\_draw\_over\_forwarding\_enabled**()
`🔗<class_EditorPlugin_method_set_force_draw_over_forwarding_enabled>`

Enables calling of
`_forward_canvas_force_draw_over_viewport<class_EditorPlugin_private_method__forward_canvas_force_draw_over_viewport>`
for the 2D editor and
`_forward_3d_force_draw_over_viewport<class_EditorPlugin_private_method__forward_3d_force_draw_over_viewport>`
for the 3D editor when their viewports are updated. You need to call
this method only once and it will work permanently for this plugin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_input\_event\_forwarding\_always\_enabled**()
`🔗<class_EditorPlugin_method_set_input_event_forwarding_always_enabled>`

Use this method if you always want to receive inputs from 3D view screen
inside
`_forward_3d_gui_input<class_EditorPlugin_private_method__forward_3d_gui_input>`.
It might be especially usable if your plugin will want to use raycast in
the scene.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **update\_overlays**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPlugin_method_update_overlays>`

Updates the overlays of the 2D and 3D editor viewport. Causes methods
`_forward_canvas_draw_over_viewport<class_EditorPlugin_private_method__forward_canvas_draw_over_viewport>`,
`_forward_canvas_force_draw_over_viewport<class_EditorPlugin_private_method__forward_canvas_force_draw_over_viewport>`,
`_forward_3d_draw_over_viewport<class_EditorPlugin_private_method__forward_3d_draw_over_viewport>`
and
`_forward_3d_force_draw_over_viewport<class_EditorPlugin_private_method__forward_3d_force_draw_over_viewport>`
to be called.
