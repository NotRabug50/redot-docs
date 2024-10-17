github\_url  
hide

# PopupMenu

**Inherits:** `Popup<class_Popup>` **&lt;** `Window<class_Window>`
**&lt;** `Viewport<class_Viewport>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A modal window used to display a list of options.

classref-introduction-group

## Description

**PopupMenu** is a modal window used to display a list of options.
Useful for toolbars and context menus.

The size of a **PopupMenu** can be limited by using
`Window.max_size<class_Window_property_max_size>`. If the height of the
list of items is larger than the maximum height of the **PopupMenu**, a
`ScrollContainer<class_ScrollContainer>` within the popup will allow the
user to scroll the contents. If no maximum size is set, or if it is set
to `0`, the **PopupMenu** height will be limited by its parent rect.

All `set_*` methods allow negative item indices, i.e. `-1` to access the
last item, `-2` to select the second-to-last item, and so on.

\*\*Incremental search:\*\* Like `ItemList<class_ItemList>` and
`Tree<class_Tree>`, **PopupMenu** supports searching within the list
while the control is focused. Press a key that matches the first letter
of an item's name to select the first item starting with the given
letter. After that point, there are two ways to perform incremental
search: 1) Press the same key again before the timeout duration to
select the next item starting with the same letter. 2) Press letter keys
that match the rest of the word before the timeout duration to match to
select the item in question directly. Both of these actions will be
reset to the beginning of the list if the timeout duration has passed
since the last keystroke was registered. You can adjust the timeout
duration by changing
`ProjectSettings.gui/timers/incremental_search_max_interval_msec<class_ProjectSettings_property_gui/timers/incremental_search_max_interval_msec>`.

\*\*Note:\*\* The ID values used for items are limited to 32 bits, not
full 64 bits of `int<class_int>`. This has a range of `-2^32` to
`2^32 - 1`, i.e. `-2147483648` to `2147483647`.

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

## Theme Properties

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**id\_focused**(id: `int<class_int>`)
`🔗<class_PopupMenu_signal_id_focused>`

Emitted when the user navigated to an item of some `id` using the
`ProjectSettings.input/ui_up<class_ProjectSettings_property_input/ui_up>`
or
`ProjectSettings.input/ui_down<class_ProjectSettings_property_input/ui_down>`
input action.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**id\_pressed**(id: `int<class_int>`)
`🔗<class_PopupMenu_signal_id_pressed>`

Emitted when an item of some `id` is pressed or its accelerator is
activated.

\*\*Note:\*\* If `id` is negative (either explicitly or due to
overflow), this will return the corresponding index instead.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**index\_pressed**(index: `int<class_int>`)
`🔗<class_PopupMenu_signal_index_pressed>`

Emitted when an item of some `index` is pressed or its accelerator is
activated.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**menu\_changed**() `🔗<class_PopupMenu_signal_menu_changed>`

Emitted when any item is added, modified or removed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **allow\_search** = `true`
`🔗<class_PopupMenu_property_allow_search>`

classref-property-setget

-   `void (No return value.)` **set\_allow\_search**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_allow\_search**()

If `true`, allows navigating **PopupMenu** with letter keys.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **hide\_on\_checkable\_item\_selection** = `true`
`🔗<class_PopupMenu_property_hide_on_checkable_item_selection>`

classref-property-setget

-   `void (No return value.)`
    **set\_hide\_on\_checkable\_item\_selection**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_hide\_on\_checkable\_item\_selection**()

If `true`, hides the **PopupMenu** when a checkbox or radio button is
selected.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **hide\_on\_item\_selection** = `true`
`🔗<class_PopupMenu_property_hide_on_item_selection>`

classref-property-setget

-   `void (No return value.)` **set\_hide\_on\_item\_selection**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_hide\_on\_item\_selection**()

If `true`, hides the **PopupMenu** when an item is selected.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **hide\_on\_state\_item\_selection** = `false`
`🔗<class_PopupMenu_property_hide_on_state_item_selection>`

classref-property-setget

-   `void (No return value.)`
    **set\_hide\_on\_state\_item\_selection**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_hide\_on\_state\_item\_selection**()

If `true`, hides the **PopupMenu** when a state item is selected.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **item\_count** = `0`
`🔗<class_PopupMenu_property_item_count>`

classref-property-setget

-   `void (No return value.)` **set\_item\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_item\_count**()

The number of items currently in the list.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **prefer\_native\_menu** = `false`
`🔗<class_PopupMenu_property_prefer_native_menu>`

classref-property-setget

-   `void (No return value.)` **set\_prefer\_native\_menu**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_prefer\_native\_menu**()

If `true`, `MenuBar<class_MenuBar>` will use native menu when supported.

\*\*Note:\*\* If **PopupMenu** is linked to
`StatusIndicator<class_StatusIndicator>`, `MenuBar<class_MenuBar>`, or
another **PopupMenu** item it can use native menu regardless of this
property, use `is_native_menu<class_PopupMenu_method_is_native_menu>` to
check it.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **submenu\_popup\_delay** = `0.3`
`🔗<class_PopupMenu_property_submenu_popup_delay>`

classref-property-setget

-   `void (No return value.)` **set\_submenu\_popup\_delay**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_submenu\_popup\_delay**()

Sets the delay time in seconds for the submenu item to popup on mouse
hovering. If the popup menu is added as a child of another (acting as a
submenu), it will inherit the delay time of the parent menu item.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SystemMenus<enum_NativeMenu_SystemMenus>` **system\_menu\_id** = `0`
`🔗<class_PopupMenu_property_system_menu_id>`

classref-property-setget

-   `void (No return value.)` **set\_system\_menu**(value:
    `SystemMenus<enum_NativeMenu_SystemMenus>`)
-   `SystemMenus<enum_NativeMenu_SystemMenus>` **get\_system\_menu**()

If set to one of the values of
`SystemMenus<enum_NativeMenu_SystemMenus>`, this **PopupMenu** is bound
to the special system menu. Only one **PopupMenu** can be bound to each
special menu at a time.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **activate\_item\_by\_event**(event:
`InputEvent<class_InputEvent>`, for\_global\_only: `bool<class_bool>` =
false) `🔗<class_PopupMenu_method_activate_item_by_event>`

Checks the provided `event` against the **PopupMenu**'s shortcuts and
accelerators, and activates the first item with matching events. If
`for_global_only` is `true`, only shortcuts and accelerators with
`global` set to `true` will be called.

Returns `true` if an item was successfully activated.

\*\*Note:\*\* Certain `Control<class_Control>`s, such as
`MenuButton<class_MenuButton>`, will call this method automatically.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_check\_item**(label:
`String<class_String>`, id: `int<class_int>` = -1, accel:
`Key<enum_@GlobalScope_Key>` = 0)
`🔗<class_PopupMenu_method_add_check_item>`

Adds a new checkable item with text `label`.

An `id` can optionally be provided, as well as an accelerator (`accel`).
If no `id` is provided, one will be created from the index. If no
`accel` is provided, then the default value of 0 (corresponding to
`@GlobalScope.KEY_NONE<class_@GlobalScope_constant_KEY_NONE>`) will be
assigned to the item (which means it won't have any accelerator). See
`get_item_accelerator<class_PopupMenu_method_get_item_accelerator>` for
more info on accelerators.

\*\*Note:\*\* Checkable items just display a checkmark, but don't have
any built-in checking behavior and must be checked/unchecked manually.
See `set_item_checked<class_PopupMenu_method_set_item_checked>` for more
info on how to control it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_check\_shortcut**(shortcut:
`Shortcut<class_Shortcut>`, id: `int<class_int>` = -1, global:
`bool<class_bool>` = false)
`🔗<class_PopupMenu_method_add_check_shortcut>`

Adds a new checkable item and assigns the specified
`Shortcut<class_Shortcut>` to it. Sets the label of the checkbox to the
`Shortcut<class_Shortcut>`'s name.

An `id` can optionally be provided. If no `id` is provided, one will be
created from the index.

\*\*Note:\*\* Checkable items just display a checkmark, but don't have
any built-in checking behavior and must be checked/unchecked manually.
See `set_item_checked<class_PopupMenu_method_set_item_checked>` for more
info on how to control it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_icon\_check\_item**(texture:
`Texture2D<class_Texture2D>`, label: `String<class_String>`, id:
`int<class_int>` = -1, accel: `Key<enum_@GlobalScope_Key>` = 0)
`🔗<class_PopupMenu_method_add_icon_check_item>`

Adds a new checkable item with text `label` and icon `texture`.

An `id` can optionally be provided, as well as an accelerator (`accel`).
If no `id` is provided, one will be created from the index. If no
`accel` is provided, then the default value of 0 (corresponding to
`@GlobalScope.KEY_NONE<class_@GlobalScope_constant_KEY_NONE>`) will be
assigned to the item (which means it won't have any accelerator). See
`get_item_accelerator<class_PopupMenu_method_get_item_accelerator>` for
more info on accelerators.

\*\*Note:\*\* Checkable items just display a checkmark, but don't have
any built-in checking behavior and must be checked/unchecked manually.
See `set_item_checked<class_PopupMenu_method_set_item_checked>` for more
info on how to control it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_icon\_check\_shortcut**(texture:
`Texture2D<class_Texture2D>`, shortcut: `Shortcut<class_Shortcut>`, id:
`int<class_int>` = -1, global: `bool<class_bool>` = false)
`🔗<class_PopupMenu_method_add_icon_check_shortcut>`

Adds a new checkable item and assigns the specified
`Shortcut<class_Shortcut>` and icon `texture` to it. Sets the label of
the checkbox to the `Shortcut<class_Shortcut>`'s name.

An `id` can optionally be provided. If no `id` is provided, one will be
created from the index.

\*\*Note:\*\* Checkable items just display a checkmark, but don't have
any built-in checking behavior and must be checked/unchecked manually.
See `set_item_checked<class_PopupMenu_method_set_item_checked>` for more
info on how to control it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_icon\_item**(texture:
`Texture2D<class_Texture2D>`, label: `String<class_String>`, id:
`int<class_int>` = -1, accel: `Key<enum_@GlobalScope_Key>` = 0)
`🔗<class_PopupMenu_method_add_icon_item>`

Adds a new item with text `label` and icon `texture`.

An `id` can optionally be provided, as well as an accelerator (`accel`).
If no `id` is provided, one will be created from the index. If no
`accel` is provided, then the default value of 0 (corresponding to
`@GlobalScope.KEY_NONE<class_@GlobalScope_constant_KEY_NONE>`) will be
assigned to the item (which means it won't have any accelerator). See
`get_item_accelerator<class_PopupMenu_method_get_item_accelerator>` for
more info on accelerators.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_icon\_radio\_check\_item**(texture:
`Texture2D<class_Texture2D>`, label: `String<class_String>`, id:
`int<class_int>` = -1, accel: `Key<enum_@GlobalScope_Key>` = 0)
`🔗<class_PopupMenu_method_add_icon_radio_check_item>`

Same as
`add_icon_check_item<class_PopupMenu_method_add_icon_check_item>`, but
uses a radio check button.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_icon\_radio\_check\_shortcut**(texture:
`Texture2D<class_Texture2D>`, shortcut: `Shortcut<class_Shortcut>`, id:
`int<class_int>` = -1, global: `bool<class_bool>` = false)
`🔗<class_PopupMenu_method_add_icon_radio_check_shortcut>`

Same as
`add_icon_check_shortcut<class_PopupMenu_method_add_icon_check_shortcut>`,
but uses a radio check button.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_icon\_shortcut**(texture:
`Texture2D<class_Texture2D>`, shortcut: `Shortcut<class_Shortcut>`, id:
`int<class_int>` = -1, global: `bool<class_bool>` = false, allow\_echo:
`bool<class_bool>` = false)
`🔗<class_PopupMenu_method_add_icon_shortcut>`

Adds a new item and assigns the specified `Shortcut<class_Shortcut>` and
icon `texture` to it. Sets the label of the checkbox to the
`Shortcut<class_Shortcut>`'s name.

An `id` can optionally be provided. If no `id` is provided, one will be
created from the index.

If `allow_echo` is `true`, the shortcut can be activated with echo
events.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_item**(label: `String<class_String>`,
id: `int<class_int>` = -1, accel: `Key<enum_@GlobalScope_Key>` = 0)
`🔗<class_PopupMenu_method_add_item>`

Adds a new item with text `label`.

An `id` can optionally be provided, as well as an accelerator (`accel`).
If no `id` is provided, one will be created from the index. If no
`accel` is provided, then the default value of 0 (corresponding to
`@GlobalScope.KEY_NONE<class_@GlobalScope_constant_KEY_NONE>`) will be
assigned to the item (which means it won't have any accelerator). See
`get_item_accelerator<class_PopupMenu_method_get_item_accelerator>` for
more info on accelerators.

\*\*Note:\*\* The provided `id` is used only in
`id_pressed<class_PopupMenu_signal_id_pressed>` and
`id_focused<class_PopupMenu_signal_id_focused>` signals. It's not
related to the `index` arguments in e.g.
`set_item_checked<class_PopupMenu_method_set_item_checked>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_multistate\_item**(label:
`String<class_String>`, max\_states: `int<class_int>`, default\_state:
`int<class_int>` = 0, id: `int<class_int>` = -1, accel:
`Key<enum_@GlobalScope_Key>` = 0)
`🔗<class_PopupMenu_method_add_multistate_item>`

Adds a new multistate item with text `label`.

Contrarily to normal binary items, multistate items can have more than
two states, as defined by `max_states`. The default value is defined by
`default_state`.

An `id` can optionally be provided, as well as an accelerator (`accel`).
If no `id` is provided, one will be created from the index. If no
`accel` is provided, then the default value of 0 (corresponding to
`@GlobalScope.KEY_NONE<class_@GlobalScope_constant_KEY_NONE>`) will be
assigned to the item (which means it won't have any accelerator). See
`get_item_accelerator<class_PopupMenu_method_get_item_accelerator>` for
more info on accelerators.

\*\*Note:\*\* Multistate items don't update their state automatically
and must be done manually. See
`toggle_item_multistate<class_PopupMenu_method_toggle_item_multistate>`,
`set_item_multistate<class_PopupMenu_method_set_item_multistate>` and
`get_item_multistate<class_PopupMenu_method_get_item_multistate>` for
more info on how to control it.

Example usage:

    func _ready():
        add_multistate_item("Item", 3, 0)

        index_pressed.connect(func(index: int):
                toggle_item_multistate(index)
                match get_item_multistate(index):
                    0:
                        print("First state")
                    1:
                        print("Second state")
                    2:
                        print("Third state")
            )

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_radio\_check\_item**(label:
`String<class_String>`, id: `int<class_int>` = -1, accel:
`Key<enum_@GlobalScope_Key>` = 0)
`🔗<class_PopupMenu_method_add_radio_check_item>`

Adds a new radio check button with text `label`.

An `id` can optionally be provided, as well as an accelerator (`accel`).
If no `id` is provided, one will be created from the index. If no
`accel` is provided, then the default value of 0 (corresponding to
`@GlobalScope.KEY_NONE<class_@GlobalScope_constant_KEY_NONE>`) will be
assigned to the item (which means it won't have any accelerator). See
`get_item_accelerator<class_PopupMenu_method_get_item_accelerator>` for
more info on accelerators.

\*\*Note:\*\* Checkable items just display a checkmark, but don't have
any built-in checking behavior and must be checked/unchecked manually.
See `set_item_checked<class_PopupMenu_method_set_item_checked>` for more
info on how to control it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_radio\_check\_shortcut**(shortcut:
`Shortcut<class_Shortcut>`, id: `int<class_int>` = -1, global:
`bool<class_bool>` = false)
`🔗<class_PopupMenu_method_add_radio_check_shortcut>`

Adds a new radio check button and assigns a `Shortcut<class_Shortcut>`
to it. Sets the label of the checkbox to the
`Shortcut<class_Shortcut>`'s name.

An `id` can optionally be provided. If no `id` is provided, one will be
created from the index.

\*\*Note:\*\* Checkable items just display a checkmark, but don't have
any built-in checking behavior and must be checked/unchecked manually.
See `set_item_checked<class_PopupMenu_method_set_item_checked>` for more
info on how to control it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_separator**(label:
`String<class_String>` = "", id: `int<class_int>` = -1)
`🔗<class_PopupMenu_method_add_separator>`

Adds a separator between items. Separators also occupy an index, which
you can set by using the `id` parameter.

A `label` can optionally be provided, which will appear at the center of
the separator.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_shortcut**(shortcut:
`Shortcut<class_Shortcut>`, id: `int<class_int>` = -1, global:
`bool<class_bool>` = false, allow\_echo: `bool<class_bool>` = false)
`🔗<class_PopupMenu_method_add_shortcut>`

Adds a `Shortcut<class_Shortcut>`.

An `id` can optionally be provided. If no `id` is provided, one will be
created from the index.

If `allow_echo` is `true`, the shortcut can be activated with echo
events.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_submenu\_item**(label:
`String<class_String>`, submenu: `String<class_String>`, id:
`int<class_int>` = -1) `🔗<class_PopupMenu_method_add_submenu_item>`

**Deprecated:** Prefer using
`add_submenu_node_item<class_PopupMenu_method_add_submenu_node_item>`
instead.

Adds an item that will act as a submenu of the parent **PopupMenu** node
when clicked. The `submenu` argument must be the name of an existing
**PopupMenu** that has been added as a child to this node. This submenu
will be shown when the item is clicked, hovered for long enough, or
activated using the `ui_select` or `ui_right` input actions.

An `id` can optionally be provided. If no `id` is provided, one will be
created from the index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_submenu\_node\_item**(label:
`String<class_String>`, submenu: `PopupMenu<class_PopupMenu>`, id:
`int<class_int>` = -1)
`🔗<class_PopupMenu_method_add_submenu_node_item>`

Adds an item that will act as a submenu of the parent **PopupMenu** node
when clicked. This submenu will be shown when the item is clicked,
hovered for long enough, or activated using the `ui_select` or
`ui_right` input actions.

`submenu` must be either child of this **PopupMenu** or has no parent
node (in which case it will be automatically added as a child). If the
`submenu` popup has another parent, this method will fail.

An `id` can optionally be provided. If no `id` is provided, one will be
created from the index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**(free\_submenus: `bool<class_bool>` =
false) `🔗<class_PopupMenu_method_clear>`

Removes all items from the **PopupMenu**. If `free_submenus` is `true`,
the submenu nodes are automatically freed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_focused\_item**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_focused_item>`

Returns the index of the currently focused item. Returns `-1` if no item
is focused.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Key<enum_@GlobalScope_Key>` **get\_item\_accelerator**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_accelerator>`

Returns the accelerator of the item at the given `index`. An accelerator
is a keyboard shortcut that can be pressed to trigger the menu button
even if it's not currently open. The return value is an integer which is
generally a combination of
`KeyModifierMask<enum_@GlobalScope_KeyModifierMask>`s and
`Key<enum_@GlobalScope_Key>`s using bitwise OR such as
`KEY_MASK_CTRL | KEY_A` (`Ctrl + A`). If no accelerator is defined for
the specified `index`,
`get_item_accelerator<class_PopupMenu_method_get_item_accelerator>`
returns `0` (corresponding to
`@GlobalScope.KEY_NONE<class_@GlobalScope_constant_KEY_NONE>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_item\_icon**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_icon>`

Returns the icon of the item at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_item\_icon\_max\_width**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_icon_max_width>`

Returns the maximum allowed width of the icon for the item at the given
`index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_item\_icon\_modulate**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_icon_modulate>`

Returns a `Color<class_Color>` modulating the item's icon at the given
`index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_item\_id**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_id>`

Returns the ID of the item at the given `index`. `id` can be manually
assigned, while index can not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_item\_indent**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_indent>`

Returns the horizontal offset of the item at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_item\_index**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_index>`

Returns the index of the item containing the specified `id`. Index is
automatically assigned to each item by the engine and can not be set
manually.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_item\_language**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_language>`

Returns item's text language code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_item\_metadata**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_metadata>`

Returns the metadata of the specified item, which might be of any type.
You can set it with
`set_item_metadata<class_PopupMenu_method_set_item_metadata>`, which
provides a simple way of assigning context data to items.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_item\_multistate**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_multistate>`

Returns the state of the item at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_item\_multistate\_max**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_multistate_max>`

Returns the max states of the item at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Shortcut<class_Shortcut>` **get\_item\_shortcut**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_shortcut>`

Returns the `Shortcut<class_Shortcut>` associated with the item at the
given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_item\_submenu**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_submenu>`

**Deprecated:** Prefer using
`get_item_submenu_node<class_PopupMenu_method_get_item_submenu_node>`
instead.

Returns the submenu name of the item at the given `index`. See
`add_submenu_item<class_PopupMenu_method_add_submenu_item>` for more
info on how to add a submenu.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PopupMenu<class_PopupMenu>` **get\_item\_submenu\_node**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_submenu_node>`

Returns the submenu of the item at the given `index`, or `null` if no
submenu was added. See
`add_submenu_node_item<class_PopupMenu_method_add_submenu_node_item>`
for more info on how to add a submenu.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_item\_text**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_text>`

Returns the text of the item at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TextDirection<enum_Control_TextDirection>`
**get\_item\_text\_direction**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_text_direction>`

Returns item's text base writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_item\_tooltip**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_get_item_tooltip>`

Returns the tooltip associated with the item at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_item\_checkable**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_is_item_checkable>`

Returns `true` if the item at the given `index` is checkable in some
way, i.e. if it has a checkbox or radio button.

\*\*Note:\*\* Checkable items just display a checkmark or radio button,
but don't have any built-in checking behavior and must be
checked/unchecked manually.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_item\_checked**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_is_item_checked>`

Returns `true` if the item at the given `index` is checked.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_item\_disabled**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_is_item_disabled>`

Returns `true` if the item at the given `index` is disabled. When it is
disabled it can't be selected, or its action invoked.

See `set_item_disabled<class_PopupMenu_method_set_item_disabled>` for
more info on how to disable an item.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_item\_radio\_checkable**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_is_item_radio_checkable>`

Returns `true` if the item at the given `index` has radio button-style
checkability.

\*\*Note:\*\* This is purely cosmetic; you must add the logic for
checking/unchecking items in radio groups.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_item\_separator**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_is_item_separator>`

Returns `true` if the item is a separator. If it is, it will be
displayed as a line. See
`add_separator<class_PopupMenu_method_add_separator>` for more info on
how to add a separator.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_item\_shortcut\_disabled**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_is_item_shortcut_disabled>`

Returns `true` if the specified item's shortcut is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_native\_menu**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_is_native_menu>`

Returns `true` if the system native menu is supported and currently used
by this **PopupMenu**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_system\_menu**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PopupMenu_method_is_system_menu>`

Returns `true` if the menu is bound to the special system menu.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_item**(index: `int<class_int>`)
`🔗<class_PopupMenu_method_remove_item>`

Removes the item at the given `index` from the menu.

\*\*Note:\*\* The indices of items after the removed item will be
shifted by one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **scroll\_to\_item**(index: `int<class_int>`)
`🔗<class_PopupMenu_method_scroll_to_item>`

Moves the scroll view to make the item at the given `index` visible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_focused\_item**(index:
`int<class_int>`) `🔗<class_PopupMenu_method_set_focused_item>`

Sets the currently focused item as the given `index`.

Passing `-1` as the index makes so that no item is focused.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_accelerator**(index:
`int<class_int>`, accel: `Key<enum_@GlobalScope_Key>`)
`🔗<class_PopupMenu_method_set_item_accelerator>`

Sets the accelerator of the item at the given `index`. An accelerator is
a keyboard shortcut that can be pressed to trigger the menu button even
if it's not currently open. `accel` is generally a combination of
`KeyModifierMask<enum_@GlobalScope_KeyModifierMask>`s and
`Key<enum_@GlobalScope_Key>`s using bitwise OR such as
`KEY_MASK_CTRL | KEY_A` (`Ctrl + A`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_as\_checkable**(index:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_PopupMenu_method_set_item_as_checkable>`

Sets whether the item at the given `index` has a checkbox. If `false`,
sets the type of the item to plain text.

\*\*Note:\*\* Checkable items just display a checkmark, but don't have
any built-in checking behavior and must be checked/unchecked manually.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_as\_radio\_checkable**(index:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_PopupMenu_method_set_item_as_radio_checkable>`

Sets the type of the item at the given `index` to radio button. If
`false`, sets the type of the item to plain text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_as\_separator**(index:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_PopupMenu_method_set_item_as_separator>`

Mark the item at the given `index` as a separator, which means that it
would be displayed as a line. If `false`, sets the type of the item to
plain text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_checked**(index:
`int<class_int>`, checked: `bool<class_bool>`)
`🔗<class_PopupMenu_method_set_item_checked>`

Sets the checkstate status of the item at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_disabled**(index:
`int<class_int>`, disabled: `bool<class_bool>`)
`🔗<class_PopupMenu_method_set_item_disabled>`

Enables/disables the item at the given `index`. When it is disabled, it
can't be selected and its action can't be invoked.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_icon**(index: `int<class_int>`,
icon: `Texture2D<class_Texture2D>`)
`🔗<class_PopupMenu_method_set_item_icon>`

Replaces the `Texture2D<class_Texture2D>` icon of the item at the given
`index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_icon\_max\_width**(index:
`int<class_int>`, width: `int<class_int>`)
`🔗<class_PopupMenu_method_set_item_icon_max_width>`

Sets the maximum allowed width of the icon for the item at the given
`index`. This limit is applied on top of the default size of the icon
and on top of
`icon_max_width<class_PopupMenu_theme_constant_icon_max_width>`. The
height is adjusted according to the icon's ratio.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_icon\_modulate**(index:
`int<class_int>`, modulate: `Color<class_Color>`)
`🔗<class_PopupMenu_method_set_item_icon_modulate>`

Sets a modulating `Color<class_Color>` of the item's icon at the given
`index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_id**(index: `int<class_int>`, id:
`int<class_int>`) `🔗<class_PopupMenu_method_set_item_id>`

Sets the `id` of the item at the given `index`.

The `id` is used in `id_pressed<class_PopupMenu_signal_id_pressed>` and
`id_focused<class_PopupMenu_signal_id_focused>` signals.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_indent**(index: `int<class_int>`,
indent: `int<class_int>`) `🔗<class_PopupMenu_method_set_item_indent>`

Sets the horizontal offset of the item at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_language**(index:
`int<class_int>`, language: `String<class_String>`)
`🔗<class_PopupMenu_method_set_item_language>`

Sets language code of item's text used for line-breaking and text
shaping algorithms, if left empty current locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_metadata**(index:
`int<class_int>`, metadata: `Variant<class_Variant>`)
`🔗<class_PopupMenu_method_set_item_metadata>`

Sets the metadata of an item, which may be of any type. You can later
get it with
`get_item_metadata<class_PopupMenu_method_get_item_metadata>`, which
provides a simple way of assigning context data to items.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_multistate**(index:
`int<class_int>`, state: `int<class_int>`)
`🔗<class_PopupMenu_method_set_item_multistate>`

Sets the state of a multistate item. See
`add_multistate_item<class_PopupMenu_method_add_multistate_item>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_multistate\_max**(index:
`int<class_int>`, max\_states: `int<class_int>`)
`🔗<class_PopupMenu_method_set_item_multistate_max>`

Sets the max states of a multistate item. See
`add_multistate_item<class_PopupMenu_method_add_multistate_item>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_shortcut**(index:
`int<class_int>`, shortcut: `Shortcut<class_Shortcut>`, global:
`bool<class_bool>` = false)
`🔗<class_PopupMenu_method_set_item_shortcut>`

Sets a `Shortcut<class_Shortcut>` for the item at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_shortcut\_disabled**(index:
`int<class_int>`, disabled: `bool<class_bool>`)
`🔗<class_PopupMenu_method_set_item_shortcut_disabled>`

Disables the `Shortcut<class_Shortcut>` of the item at the given
`index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_submenu**(index:
`int<class_int>`, submenu: `String<class_String>`)
`🔗<class_PopupMenu_method_set_item_submenu>`

**Deprecated:** Prefer using
`set_item_submenu_node<class_PopupMenu_method_set_item_submenu_node>`
instead.

Sets the submenu of the item at the given `index`. The submenu is the
name of a child **PopupMenu** node that would be shown when the item is
clicked.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_submenu\_node**(index:
`int<class_int>`, submenu: `PopupMenu<class_PopupMenu>`)
`🔗<class_PopupMenu_method_set_item_submenu_node>`

Sets the submenu of the item at the given `index`. The submenu is a
**PopupMenu** node that would be shown when the item is clicked. It must
either be a child of this **PopupMenu** or has no parent (in which case
it will be automatically added as a child). If the `submenu` popup has
another parent, this method will fail.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_text**(index: `int<class_int>`,
text: `String<class_String>`) `🔗<class_PopupMenu_method_set_item_text>`

Sets the text of the item at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_text\_direction**(index:
`int<class_int>`, direction:
`TextDirection<enum_Control_TextDirection>`)
`🔗<class_PopupMenu_method_set_item_text_direction>`

Sets item's text base writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_tooltip**(index:
`int<class_int>`, tooltip: `String<class_String>`)
`🔗<class_PopupMenu_method_set_item_tooltip>`

Sets the `String<class_String>` tooltip of the item at the given
`index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **toggle\_item\_checked**(index:
`int<class_int>`) `🔗<class_PopupMenu_method_toggle_item_checked>`

Toggles the check state of the item at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **toggle\_item\_multistate**(index:
`int<class_int>`) `🔗<class_PopupMenu_method_toggle_item_multistate>`

Cycle to the next state of a multistate item. See
`add_multistate_item<class_PopupMenu_method_add_multistate_item>` for
details.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **font\_accelerator\_color** =
`Color(0.7, 0.7, 0.7, 0.8)`
`🔗<class_PopupMenu_theme_color_font_accelerator_color>`

The text `Color<class_Color>` used for shortcuts and accelerators that
show next to the menu item name when defined. See
`get_item_accelerator<class_PopupMenu_method_get_item_accelerator>` for
more info on accelerators.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_color** = `Color(0.875, 0.875, 0.875, 1)`
`🔗<class_PopupMenu_theme_color_font_color>`

The default text `Color<class_Color>` for menu items' names.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_disabled\_color** =
`Color(0.4, 0.4, 0.4, 0.8)`
`🔗<class_PopupMenu_theme_color_font_disabled_color>`

`Color<class_Color>` used for disabled menu items' text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_hover\_color** =
`Color(0.875, 0.875, 0.875, 1)`
`🔗<class_PopupMenu_theme_color_font_hover_color>`

`Color<class_Color>` used for the hovered text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_outline\_color** = `Color(0, 0, 0, 1)`
`🔗<class_PopupMenu_theme_color_font_outline_color>`

The tint of text outline of the menu item.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_separator\_color** =
`Color(0.875, 0.875, 0.875, 1)`
`🔗<class_PopupMenu_theme_color_font_separator_color>`

`Color<class_Color>` used for labeled separators' text. See
`add_separator<class_PopupMenu_method_add_separator>`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_separator\_outline\_color** =
`Color(0, 0, 0, 1)`
`🔗<class_PopupMenu_theme_color_font_separator_outline_color>`

The tint of text outline of the labeled separator.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **h\_separation** = `4`
`🔗<class_PopupMenu_theme_constant_h_separation>`

The horizontal space between the item's elements.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **icon\_max\_width** = `0`
`🔗<class_PopupMenu_theme_constant_icon_max_width>`

The maximum allowed width of the item's icon. This limit is applied on
top of the default size of the icon, but before the value set with
`set_item_icon_max_width<class_PopupMenu_method_set_item_icon_max_width>`.
The height is adjusted according to the icon's ratio.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **indent** = `10`
`🔗<class_PopupMenu_theme_constant_indent>`

Width of the single indentation level.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **item\_end\_padding** = `2`
`🔗<class_PopupMenu_theme_constant_item_end_padding>`

Horizontal padding to the right of the items (or left, in RTL layout).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **item\_start\_padding** = `2`
`🔗<class_PopupMenu_theme_constant_item_start_padding>`

Horizontal padding to the left of the items (or right, in RTL layout).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **outline\_size** = `0`
`🔗<class_PopupMenu_theme_constant_outline_size>`

The size of the item text outline.

\*\*Note:\*\* If using a font with
`FontFile.multichannel_signed_distance_field<class_FontFile_property_multichannel_signed_distance_field>`
enabled, its
`FontFile.msdf_pixel_range<class_FontFile_property_msdf_pixel_range>`
must be set to at least *twice* the value of
`outline_size<class_PopupMenu_theme_constant_outline_size>` for outline
rendering to look correct. Otherwise, the outline may appear to be cut
off earlier than intended.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **separator\_outline\_size** = `0`
`🔗<class_PopupMenu_theme_constant_separator_outline_size>`

The size of the labeled separator text outline.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **v\_separation** = `4`
`🔗<class_PopupMenu_theme_constant_v_separation>`

The vertical space between each menu item.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **font** `🔗<class_PopupMenu_theme_font_font>`

`Font<class_Font>` used for the menu items.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **font\_separator**
`🔗<class_PopupMenu_theme_font_font_separator>`

`Font<class_Font>` used for the labeled separator.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **font\_separator\_size**
`🔗<class_PopupMenu_theme_font_size_font_separator_size>`

Font size of the labeled separator.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **font\_size**
`🔗<class_PopupMenu_theme_font_size_font_size>`

Font size of the menu items.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **checked**
`🔗<class_PopupMenu_theme_icon_checked>`

`Texture2D<class_Texture2D>` icon for the checked checkbox items.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **checked\_disabled**
`🔗<class_PopupMenu_theme_icon_checked_disabled>`

`Texture2D<class_Texture2D>` icon for the checked checkbox items when
they are disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **radio\_checked**
`🔗<class_PopupMenu_theme_icon_radio_checked>`

`Texture2D<class_Texture2D>` icon for the checked radio button items.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **radio\_checked\_disabled**
`🔗<class_PopupMenu_theme_icon_radio_checked_disabled>`

`Texture2D<class_Texture2D>` icon for the checked radio button items
when they are disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **radio\_unchecked**
`🔗<class_PopupMenu_theme_icon_radio_unchecked>`

`Texture2D<class_Texture2D>` icon for the unchecked radio button items.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **radio\_unchecked\_disabled**
`🔗<class_PopupMenu_theme_icon_radio_unchecked_disabled>`

`Texture2D<class_Texture2D>` icon for the unchecked radio button items
when they are disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **submenu**
`🔗<class_PopupMenu_theme_icon_submenu>`

`Texture2D<class_Texture2D>` icon for the submenu arrow (for
left-to-right layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **submenu\_mirrored**
`🔗<class_PopupMenu_theme_icon_submenu_mirrored>`

`Texture2D<class_Texture2D>` icon for the submenu arrow (for
right-to-left layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **unchecked**
`🔗<class_PopupMenu_theme_icon_unchecked>`

`Texture2D<class_Texture2D>` icon for the unchecked checkbox items.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **unchecked\_disabled**
`🔗<class_PopupMenu_theme_icon_unchecked_disabled>`

`Texture2D<class_Texture2D>` icon for the unchecked checkbox items when
they are disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **hover**
`🔗<class_PopupMenu_theme_style_hover>`

`StyleBox<class_StyleBox>` displayed when the **PopupMenu** item is
hovered.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **labeled\_separator\_left**
`🔗<class_PopupMenu_theme_style_labeled_separator_left>`

`StyleBox<class_StyleBox>` for the left side of labeled separator. See
`add_separator<class_PopupMenu_method_add_separator>`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **labeled\_separator\_right**
`🔗<class_PopupMenu_theme_style_labeled_separator_right>`

`StyleBox<class_StyleBox>` for the right side of labeled separator. See
`add_separator<class_PopupMenu_method_add_separator>`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **panel**
`🔗<class_PopupMenu_theme_style_panel>`

`StyleBox<class_StyleBox>` for the background panel.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **separator**
`🔗<class_PopupMenu_theme_style_separator>`

`StyleBox<class_StyleBox>` used for the separators. See
`add_separator<class_PopupMenu_method_add_separator>`.
