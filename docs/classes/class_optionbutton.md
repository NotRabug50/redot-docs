github\_url  
hide

# OptionButton

**Inherits:** `Button<class_Button>` **&lt;**
`BaseButton<class_BaseButton>` **&lt;** `Control<class_Control>`
**&lt;** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A button that brings up a dropdown with selectable options when pressed.

classref-introduction-group

## Description

**OptionButton** is a type of button that brings up a dropdown with
selectable items when pressed. The item selected becomes the "current"
item and is displayed as the button text.

See also `BaseButton<class_BaseButton>` which contains common properties
and methods associated with this node.

\*\*Note:\*\* The ID values used for items are limited to 32 bits, not
full 64 bits of `int<class_int>`. This has a range of `-2^32` to
`2^32 - 1`, i.e. `-2147483648` to `2147483647`.

\*\*Note:\*\* The `Button.text<class_Button_property_text>` and
`Button.icon<class_Button_property_icon>` properties are set
automatically based on the selected item. They shouldn't be changed
manually.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**item\_focused**(index: `int<class_int>`)
`🔗<class_OptionButton_signal_item_focused>`

Emitted when the user navigates to an item using the
`ProjectSettings.input/ui_up<class_ProjectSettings_property_input/ui_up>`
or
`ProjectSettings.input/ui_down<class_ProjectSettings_property_input/ui_down>`
input actions. The index of the item selected is passed as argument.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**item\_selected**(index: `int<class_int>`)
`🔗<class_OptionButton_signal_item_selected>`

Emitted when the current item has been changed by the user. The index of
the item selected is passed as argument.

`allow_reselect<class_OptionButton_property_allow_reselect>` must be
enabled to reselect an item.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **allow\_reselect** = `false`
`🔗<class_OptionButton_property_allow_reselect>`

classref-property-setget

-   `void (No return value.)` **set\_allow\_reselect**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_allow\_reselect**()

If `true`, the currently selected item can be selected again.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **fit\_to\_longest\_item** = `true`
`🔗<class_OptionButton_property_fit_to_longest_item>`

classref-property-setget

-   `void (No return value.)` **set\_fit\_to\_longest\_item**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_fit\_to\_longest\_item**()

If `true`, minimum size will be determined by the longest item's text,
instead of the currently selected one's.

\*\*Note:\*\* For performance reasons, the minimum size doesn't update
immediately when adding, removing or modifying items.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **item\_count** = `0`
`🔗<class_OptionButton_property_item_count>`

classref-property-setget

-   `void (No return value.)` **set\_item\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_item\_count**()

The number of items to select from.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **selected** = `-1`
`🔗<class_OptionButton_property_selected>`

classref-property-setget

-   `int<class_int>` **get\_selected**()

The index of the currently selected item, or `-1` if no item is
selected.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_icon\_item**(texture:
`Texture2D<class_Texture2D>`, label: `String<class_String>`, id:
`int<class_int>` = -1) `🔗<class_OptionButton_method_add_icon_item>`

Adds an item, with a `texture` icon, text `label` and (optionally) `id`.
If no `id` is passed, the item index will be used as the item's ID. New
items are appended at the end.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_item**(label: `String<class_String>`,
id: `int<class_int>` = -1) `🔗<class_OptionButton_method_add_item>`

Adds an item, with text `label` and (optionally) `id`. If no `id` is
passed, the item index will be used as the item's ID. New items are
appended at the end.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_separator**(text:
`String<class_String>` = "")
`🔗<class_OptionButton_method_add_separator>`

Adds a separator to the list of items. Separators help to group items,
and can optionally be given a `text` header. A separator also gets an
index assigned, and is appended at the end of the item list.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_OptionButton_method_clear>`

Clears all the items in the **OptionButton**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_item\_icon**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_get_item_icon>`

Returns the icon of the item at index `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_item\_id**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_get_item_id>`

Returns the ID of the item at index `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_item\_index**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_get_item_index>`

Returns the index of the item with the given `id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_item\_metadata**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_get_item_metadata>`

Retrieves the metadata of an item. Metadata may be any type and can be
used to store extra information about an item, such as an external
string ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_item\_text**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_get_item_text>`

Returns the text of the item at index `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_item\_tooltip**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_get_item_tooltip>`

Returns the tooltip of the item at index `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PopupMenu<class_PopupMenu>` **get\_popup**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_get_popup>`

Returns the `PopupMenu<class_PopupMenu>` contained in this button.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to hide it or any of its children, use
their `Window.visible<class_Window_property_visible>` property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selectable\_item**(from\_last:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_get_selectable_item>`

Returns the index of the first item which is not disabled, or marked as
a separator. If `from_last` is `true`, the items will be searched in
reverse order.

Returns `-1` if no item is found.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selected\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_get_selected_id>`

Returns the ID of the selected item, or `-1` if no item is selected.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_selected\_metadata**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_get_selected_metadata>`

Gets the metadata of the selected item. Metadata for items can be set
using `set_item_metadata<class_OptionButton_method_set_item_metadata>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_selectable\_items**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_has_selectable_items>`

Returns `true` if this button contains at least one item which is not
disabled, or marked as a separator.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_item\_disabled**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_is_item_disabled>`

Returns `true` if the item at index `idx` is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_item\_separator**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OptionButton_method_is_item_separator>`

Returns `true` if the item at index `idx` is marked as a separator.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_item**(idx: `int<class_int>`)
`🔗<class_OptionButton_method_remove_item>`

Removes the item at index `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **select**(idx: `int<class_int>`)
`🔗<class_OptionButton_method_select>`

Selects an item by index and makes it the current item. This will work
even if the item is disabled.

Passing `-1` as the index deselects any currently selected item.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_disable\_shortcuts**(disabled:
`bool<class_bool>`)
`🔗<class_OptionButton_method_set_disable_shortcuts>`

If `true`, shortcuts are disabled and cannot be used to trigger the
button.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_disabled**(idx: `int<class_int>`,
disabled: `bool<class_bool>`)
`🔗<class_OptionButton_method_set_item_disabled>`

Sets whether the item at index `idx` is disabled.

Disabled items are drawn differently in the dropdown and are not
selectable by the user. If the current selected item is set as disabled,
it will remain selected.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_icon**(idx: `int<class_int>`,
texture: `Texture2D<class_Texture2D>`)
`🔗<class_OptionButton_method_set_item_icon>`

Sets the icon of the item at index `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_id**(idx: `int<class_int>`, id:
`int<class_int>`) `🔗<class_OptionButton_method_set_item_id>`

Sets the ID of the item at index `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_metadata**(idx: `int<class_int>`,
metadata: `Variant<class_Variant>`)
`🔗<class_OptionButton_method_set_item_metadata>`

Sets the metadata of an item. Metadata may be of any type and can be
used to store extra information about an item, such as an external
string ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_text**(idx: `int<class_int>`,
text: `String<class_String>`)
`🔗<class_OptionButton_method_set_item_text>`

Sets the text of the item at index `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_item\_tooltip**(idx: `int<class_int>`,
tooltip: `String<class_String>`)
`🔗<class_OptionButton_method_set_item_tooltip>`

Sets the tooltip of the item at index `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **show\_popup**()
`🔗<class_OptionButton_method_show_popup>`

Adjusts popup position and sizing for the **OptionButton**, then shows
the `PopupMenu<class_PopupMenu>`. Prefer this over using
`get_popup().popup()`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`int<class_int>` **arrow\_margin** = `4`
`🔗<class_OptionButton_theme_constant_arrow_margin>`

The horizontal space between the arrow icon and the right edge of the
button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **modulate\_arrow** = `0`
`🔗<class_OptionButton_theme_constant_modulate_arrow>`

If different than `0`, the arrow icon will be modulated to the font
color.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **arrow**
`🔗<class_OptionButton_theme_icon_arrow>`

The arrow icon to be drawn on the right end of the button.
