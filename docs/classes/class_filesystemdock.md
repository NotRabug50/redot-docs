github\_url  
hide

# FileSystemDock

**Inherits:** `VBoxContainer<class_VBoxContainer>` **&lt;**
`BoxContainer<class_BoxContainer>` **&lt;** `Container<class_Container>`
**&lt;** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Godot editor's dock for managing files in the project.

classref-introduction-group

## Description

This class is available only in `EditorPlugin<class_EditorPlugin>`s and
can't be instantiated. You can access it using
`EditorInterface.get_file_system_dock<class_EditorInterface_method_get_file_system_dock>`.

While **FileSystemDock** doesn't expose any methods for file
manipulation, it can listen for various file-related signals.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**display\_mode\_changed**()
`🔗<class_FileSystemDock_signal_display_mode_changed>`

Emitted when the user switches file display mode or split mode.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**file\_removed**(file: `String<class_String>`)
`🔗<class_FileSystemDock_signal_file_removed>`

Emitted when the given `file` was removed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**files\_moved**(old\_file: `String<class_String>`, new\_file:
`String<class_String>`) `🔗<class_FileSystemDock_signal_files_moved>`

Emitted when a file is moved from `old_file` path to `new_file` path.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**folder\_color\_changed**()
`🔗<class_FileSystemDock_signal_folder_color_changed>`

Emitted when folders change color.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**folder\_moved**(old\_folder: `String<class_String>`, new\_folder:
`String<class_String>`) `🔗<class_FileSystemDock_signal_folder_moved>`

Emitted when a folder is moved from `old_folder` path to `new_folder`
path.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**folder\_removed**(folder: `String<class_String>`)
`🔗<class_FileSystemDock_signal_folder_removed>`

Emitted when the given `folder` was removed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**inherit**(file: `String<class_String>`)
`🔗<class_FileSystemDock_signal_inherit>`

Emitted when a new scene is created that inherits the scene at `file`
path.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**instantiate**(files: `PackedStringArray<class_PackedStringArray>`)
`🔗<class_FileSystemDock_signal_instantiate>`

Emitted when the given scenes are being instantiated in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**resource\_removed**(resource: `Resource<class_Resource>`)
`🔗<class_FileSystemDock_signal_resource_removed>`

Emitted when an external `resource` had its file removed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_resource\_tooltip\_plugin**(plugin:
`EditorResourceTooltipPlugin<class_EditorResourceTooltipPlugin>`)
`🔗<class_FileSystemDock_method_add_resource_tooltip_plugin>`

Registers a new
`EditorResourceTooltipPlugin<class_EditorResourceTooltipPlugin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **navigate\_to\_path**(path:
`String<class_String>`)
`🔗<class_FileSystemDock_method_navigate_to_path>`

Sets the given `path` as currently selected, ensuring that the selected
file/directory is visible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_resource\_tooltip\_plugin**(plugin:
`EditorResourceTooltipPlugin<class_EditorResourceTooltipPlugin>`)
`🔗<class_FileSystemDock_method_remove_resource_tooltip_plugin>`

Removes an
`EditorResourceTooltipPlugin<class_EditorResourceTooltipPlugin>`. Fails
if the plugin wasn't previously added.
