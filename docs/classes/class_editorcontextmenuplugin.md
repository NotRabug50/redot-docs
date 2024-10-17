github\_url  
hide

# EditorContextMenuPlugin

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Plugin for adding custom context menus in the editor.

classref-introduction-group

## Description

**EditorContextMenuPlugin** allows for the addition of custom options in
the editor's context menu.

Currently, context menus are supported for three commonly used areas:
the file system, scene tree, and editor script list panel.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ContextMenuSlot**:
`🔗<enum_EditorContextMenuPlugin_ContextMenuSlot>`

classref-enumeration-constant

`ContextMenuSlot<enum_EditorContextMenuPlugin_ContextMenuSlot>`
**CONTEXT\_SLOT\_SCENE\_TREE** = `0`

Context menu of Scene dock.
`_popup_menu<class_EditorContextMenuPlugin_private_method__popup_menu>`
will be called with a list of paths to currently selected nodes, while
option callback will receive the list of currently selected nodes.

classref-enumeration-constant

`ContextMenuSlot<enum_EditorContextMenuPlugin_ContextMenuSlot>`
**CONTEXT\_SLOT\_FILESYSTEM** = `1`

Context menu of FileSystem dock.
`_popup_menu<class_EditorContextMenuPlugin_private_method__popup_menu>`
and option callback will be called with list of paths of the currently
selected files.

classref-enumeration-constant

`ContextMenuSlot<enum_EditorContextMenuPlugin_ContextMenuSlot>`
**CONTEXT\_SLOT\_FILESYSTEM\_CREATE** = `3`

The "Create..." submenu of FileSystem dock's context menu.
`_popup_menu<class_EditorContextMenuPlugin_private_method__popup_menu>`
and option callback will be called with list of paths of the currently
selected files.

classref-enumeration-constant

`ContextMenuSlot<enum_EditorContextMenuPlugin_ContextMenuSlot>`
**CONTEXT\_SLOT\_SCRIPT\_EDITOR** = `2`

Context menu of Scene dock.
`_popup_menu<class_EditorContextMenuPlugin_private_method__popup_menu>`
will be called with the path to the currently edited script, while
option callback will receive reference to that script.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_popup\_menu**(paths:
`PackedStringArray<class_PackedStringArray>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorContextMenuPlugin_private_method__popup_menu>`

Called when creating a context menu, custom options can be added by
using the
`add_context_menu_item<class_EditorContextMenuPlugin_method_add_context_menu_item>`
or
`add_context_menu_item_from_shortcut<class_EditorContextMenuPlugin_method_add_context_menu_item_from_shortcut>`
functions. `paths` contains currently selected paths (depending on
menu), which can be used to conditionally add options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_context\_menu\_item**(name:
`String<class_String>`, callback: `Callable<class_Callable>`, icon:
`Texture2D<class_Texture2D>` = null)
`🔗<class_EditorContextMenuPlugin_method_add_context_menu_item>`

Add custom option to the context menu of the plugin's specified slot.
When the option is activated, `callback` will be called. Callback should
take single `Array<class_Array>` argument; array contents depend on
context menu slot.

    func _popup_menu(paths):
        add_context_menu_item("File Custom options", handle, ICON)

If you want to assign shortcut to the menu item, use
`add_context_menu_item_from_shortcut<class_EditorContextMenuPlugin_method_add_context_menu_item_from_shortcut>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**add\_context\_menu\_item\_from\_shortcut**(name:
`String<class_String>`, shortcut: `Shortcut<class_Shortcut>`, icon:
`Texture2D<class_Texture2D>` = null)
`🔗<class_EditorContextMenuPlugin_method_add_context_menu_item_from_shortcut>`

Add custom option to the context menu of the plugin's specified slot.
The option will have the `shortcut` assigned and reuse its callback. The
shortcut has to be registered beforehand with
`add_menu_shortcut<class_EditorContextMenuPlugin_method_add_menu_shortcut>`.

    func _init():
        add_menu_shortcut(SHORTCUT, handle)

    func _popup_menu(paths):
        add_context_menu_item_from_shortcut("File Custom options", SHORTCUT, ICON)

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_context\_submenu\_item**(name:
`String<class_String>`, menu: `PopupMenu<class_PopupMenu>`, icon:
`Texture2D<class_Texture2D>` = null)
`🔗<class_EditorContextMenuPlugin_method_add_context_submenu_item>`

Add a submenu to the context menu of the plugin's specified slot. The
submenu is not automatically handled, you need to connect to its signals
yourself. Also the submenu is freed on every popup, so provide a new
`PopupMenu<class_PopupMenu>` every time.

    func _popup_menu(paths):
        var popup_menu = PopupMenu.new()
        popup_menu.add_item("Blue")
        popup_menu.add_item("White")
        popup_menu.id_pressed.connect(_on_color_submenu_option)

        add_context_menu_item("Set Node Color", popup_menu)

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_menu\_shortcut**(shortcut:
`Shortcut<class_Shortcut>`, callback: `Callable<class_Callable>`)
`🔗<class_EditorContextMenuPlugin_method_add_menu_shortcut>`

Registers a shortcut associated with the plugin's context menu. This
method should be called once (e.g. in plugin's
`Object._init<class_Object_private_method__init>`). `callback` will be
called when user presses the specified `shortcut` while the menu's
context is in effect (e.g. FileSystem dock is focused). Callback should
take single `Array<class_Array>` argument; array contents depend on
context menu slot.

    func _init():
        add_menu_shortcut(SHORTCUT, handle)
