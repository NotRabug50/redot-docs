github\_url  
hide

# TreeItem

**Inherits:** `Object<class_Object>`

An internal control for a single item inside `Tree<class_Tree>`.

classref-introduction-group

## Description

A single item of a `Tree<class_Tree>` control. It can contain other
**TreeItem**s as children, which allows it to create a hierarchy. It can
also contain text and buttons. **TreeItem** is not a `Node<class_Node>`,
it is internal to the `Tree<class_Tree>`.

To create a **TreeItem**, use
`Tree.create_item<class_Tree_method_create_item>` or
`create_child<class_TreeItem_method_create_child>`. To remove a
**TreeItem**, use `Object.free<class_Object_method_free>`.

\*\*Note:\*\* The ID values used for buttons are 32-bit, unlike
`int<class_int>` which is always 64-bit. They go from `-2147483648` to
`2147483647`.

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

enum **TreeCellMode**: `🔗<enum_TreeItem_TreeCellMode>`

classref-enumeration-constant

`TreeCellMode<enum_TreeItem_TreeCellMode>` **CELL\_MODE\_STRING** = `0`

Cell shows a string label, optionally with an icon. When editable, the
text can be edited using a `LineEdit<class_LineEdit>`, or a
`TextEdit<class_TextEdit>` popup if
`set_edit_multiline<class_TreeItem_method_set_edit_multiline>` is used.

classref-enumeration-constant

`TreeCellMode<enum_TreeItem_TreeCellMode>` **CELL\_MODE\_CHECK** = `1`

Cell shows a checkbox, optionally with text and an icon. The checkbox
can be pressed, released, or indeterminate (via
`set_indeterminate<class_TreeItem_method_set_indeterminate>`). The
checkbox can't be clicked unless the cell is editable.

classref-enumeration-constant

`TreeCellMode<enum_TreeItem_TreeCellMode>` **CELL\_MODE\_RANGE** = `2`

Cell shows a numeric range. When editable, it can be edited using a
range slider. Use `set_range<class_TreeItem_method_set_range>` to set
the value and `set_range_config<class_TreeItem_method_set_range_config>`
to configure the range.

This cell can also be used in a text dropdown mode when you assign a
text with `set_text<class_TreeItem_method_set_text>`. Separate options
with a comma, e.g. `"Option1,Option2,Option3"`.

classref-enumeration-constant

`TreeCellMode<enum_TreeItem_TreeCellMode>` **CELL\_MODE\_ICON** = `3`

Cell shows an icon. It can't be edited nor display text. The icon is
always centered within the cell.

classref-enumeration-constant

`TreeCellMode<enum_TreeItem_TreeCellMode>` **CELL\_MODE\_CUSTOM** = `4`

Cell shows as a clickable button. It will display an arrow similar to
`OptionButton<class_OptionButton>`, but doesn't feature a dropdown (for
that you can use
`CELL_MODE_RANGE<class_TreeItem_constant_CELL_MODE_RANGE>`). Clicking
the button emits the `Tree.item_edited<class_Tree_signal_item_edited>`
signal. The button is flat by default, you can use
`set_custom_as_button<class_TreeItem_method_set_custom_as_button>` to
display it with a `StyleBox<class_StyleBox>`.

This mode also supports custom drawing using
`set_custom_draw_callback<class_TreeItem_method_set_custom_draw_callback>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **collapsed** `🔗<class_TreeItem_property_collapsed>`

classref-property-setget

-   `void (No return value.)` **set\_collapsed**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_collapsed**()

If `true`, the TreeItem is collapsed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **custom\_minimum\_height**
`🔗<class_TreeItem_property_custom_minimum_height>`

classref-property-setget

-   `void (No return value.)` **set\_custom\_minimum\_height**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_custom\_minimum\_height**()

The custom minimum height.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disable\_folding**
`🔗<class_TreeItem_property_disable_folding>`

classref-property-setget

-   `void (No return value.)` **set\_disable\_folding**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_folding\_disabled**()

If `true`, folding is disabled for this TreeItem.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **visible** `🔗<class_TreeItem_property_visible>`

classref-property-setget

-   `void (No return value.)` **set\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_visible**()

If `true`, the **TreeItem** is visible (default).

Note that if a **TreeItem** is set to not be visible, none of its
children will be visible either.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_button**(column: `int<class_int>`,
button: `Texture2D<class_Texture2D>`, id: `int<class_int>` = -1,
disabled: `bool<class_bool>` = false, tooltip\_text:
`String<class_String>` = "") `🔗<class_TreeItem_method_add_button>`

Adds a button with `Texture2D<class_Texture2D>` `button` to the end of
the cell at column `column`. The `id` is used to identify the button in
the according `Tree.button_clicked<class_Tree_signal_button_clicked>`
signal and can be different from the buttons index. If not specified,
the next available index is used, which may be retrieved by calling
`get_button_count<class_TreeItem_method_get_button_count>` immediately
before this method. Optionally, the button can be `disabled` and have a
`tooltip_text`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_child**(child:
`TreeItem<class_TreeItem>`) `🔗<class_TreeItem_method_add_child>`

Adds a previously unparented **TreeItem** as a direct child of this one.
The `child` item must not be a part of any `Tree<class_Tree>` or
parented to any **TreeItem**. See also
`remove_child<class_TreeItem_method_remove_child>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **call\_recursive**(method:
`StringName<class_StringName>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_TreeItem_method_call_recursive>`

Calls the `method` on the actual TreeItem and its children recursively.
Pass parameters as a comma separated list.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_custom\_bg\_color**(column:
`int<class_int>`) `🔗<class_TreeItem_method_clear_custom_bg_color>`

Resets the background color for the given column to default.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_custom\_color**(column:
`int<class_int>`) `🔗<class_TreeItem_method_clear_custom_color>`

Resets the color for the given column to default.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **create\_child**(index: `int<class_int>` =
-1) `🔗<class_TreeItem_method_create_child>`

Creates an item and adds it as a child.

The new item will be inserted as position `index` (the default value
`-1` means the last position), or it will be the last child if `index`
is higher than the child count.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **deselect**(column: `int<class_int>`)
`🔗<class_TreeItem_method_deselect>`

Deselects the given column.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase\_button**(column: `int<class_int>`,
button\_index: `int<class_int>`)
`🔗<class_TreeItem_method_erase_button>`

Removes the button at index `button_index` in column `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AutoTranslateMode<enum_Node_AutoTranslateMode>`
**get\_auto\_translate\_mode**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_auto_translate_mode>`

Returns the column's auto translate mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AutowrapMode<enum_TextServer_AutowrapMode>`
**get\_autowrap\_mode**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_autowrap_mode>`

Returns the text autowrap mode in the given `column`. By default it is
`TextServer.AUTOWRAP_OFF<class_TextServer_constant_AUTOWRAP_OFF>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_button**(column: `int<class_int>`,
button\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_button>`

Returns the `Texture2D<class_Texture2D>` of the button at index
`button_index` in column `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_button\_by\_id**(column: `int<class_int>`, id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_button_by_id>`

Returns the button index if there is a button with ID `id` in column
`column`, otherwise returns -1.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_button\_color**(column: `int<class_int>`,
id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_button_color>`

Returns the color of the button with ID `id` in column `column`. If the
specified button does not exist, returns
`Color.BLACK<class_Color_constant_BLACK>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_button\_count**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_button_count>`

Returns the number of buttons in column `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_button\_id**(column: `int<class_int>`,
button\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_button_id>`

Returns the ID for the button at index `button_index` in column
`column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_button\_tooltip\_text**(column:
`int<class_int>`, button\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_button_tooltip_text>`

Returns the tooltip text for the button at index `button_index` in
column `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeCellMode<enum_TreeItem_TreeCellMode>` **get\_cell\_mode**(column:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_cell_mode>`

Returns the column's cell mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_child**(index: `int<class_int>`)
`🔗<class_TreeItem_method_get_child>`

Returns a child item by its `index` (see
`get_child_count<class_TreeItem_method_get_child_count>`). This method
is often used for iterating all children of an item.

Negative indices access the children from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_child\_count**()
`🔗<class_TreeItem_method_get_child_count>`

Returns the number of child items.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`TreeItem<class_TreeItem>`\] **get\_children**()
`🔗<class_TreeItem_method_get_children>`

Returns an array of references to the item's children.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_custom\_bg\_color**(column:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_custom_bg_color>`

Returns the custom background color of column `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_custom\_color**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_custom_color>`

Returns the custom color of column `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Callable<class_Callable>` **get\_custom\_draw\_callback**(column:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_custom_draw_callback>`

Returns the custom callback of column `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Font<class_Font>` **get\_custom\_font**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_custom_font>`

Returns custom font used to draw text in the column `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_custom\_font\_size**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_custom_font_size>`

Returns custom font size used to draw text in the column `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_expand\_right**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_expand_right>`

Returns `true` if `expand_right` is set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_first\_child**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_first_child>`

Returns the TreeItem's first child.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_icon**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_icon>`

Returns the given column's icon `Texture2D<class_Texture2D>`. Error if
no icon is set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_icon\_max\_width**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_icon_max_width>`

Returns the maximum allowed width of the icon in the given `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_icon\_modulate**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_icon_modulate>`

Returns the `Color<class_Color>` modulating the column's icon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_icon\_overlay**(column:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_icon_overlay>`

Returns the given column's icon overlay `Texture2D<class_Texture2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_icon\_region**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_icon_region>`

Returns the icon `Texture2D<class_Texture2D>` region as
`Rect2<class_Rect2>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_index**() `🔗<class_TreeItem_method_get_index>`

Returns the node's order in the tree. For example, if called on the
first child item the position is `0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_language**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_language>`

Returns item's text language code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_metadata**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_metadata>`

Returns the metadata value that was set for the given column using
`set_metadata<class_TreeItem_method_set_metadata>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_next**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_next>`

Returns the next sibling TreeItem in the tree or a null object if there
is none.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_next\_in\_tree**(wrap:
`bool<class_bool>` = false) `🔗<class_TreeItem_method_get_next_in_tree>`

Returns the next TreeItem in the tree (in the context of a depth-first
search) or a `null` object if there is none.

If `wrap` is enabled, the method will wrap around to the first element
in the tree when called on the last element, otherwise it returns
`null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_next\_visible**(wrap:
`bool<class_bool>` = false) `🔗<class_TreeItem_method_get_next_visible>`

Returns the next visible TreeItem in the tree (in the context of a
depth-first search) or a `null` object if there is none.

If `wrap` is enabled, the method will wrap around to the first visible
element in the tree when called on the last visible element, otherwise
it returns `null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_parent**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_parent>`

Returns the parent TreeItem or a null object if there is none.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_prev**()
`🔗<class_TreeItem_method_get_prev>`

Returns the previous sibling TreeItem in the tree or a null object if
there is none.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_prev\_in\_tree**(wrap:
`bool<class_bool>` = false) `🔗<class_TreeItem_method_get_prev_in_tree>`

Returns the previous TreeItem in the tree (in the context of a
depth-first search) or a `null` object if there is none.

If `wrap` is enabled, the method will wrap around to the last element in
the tree when called on the first visible element, otherwise it returns
`null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TreeItem<class_TreeItem>` **get\_prev\_visible**(wrap:
`bool<class_bool>` = false) `🔗<class_TreeItem_method_get_prev_visible>`

Returns the previous visible sibling TreeItem in the tree (in the
context of a depth-first search) or a `null` object if there is none.

If `wrap` is enabled, the method will wrap around to the last visible
element in the tree when called on the first visible element, otherwise
it returns `null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_range**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_range>`

Returns the value of a
`CELL_MODE_RANGE<class_TreeItem_constant_CELL_MODE_RANGE>` column.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_range\_config**(column:
`int<class_int>`) `🔗<class_TreeItem_method_get_range_config>`

Returns a dictionary containing the range parameters for a given column.
The keys are "min", "max", "step", and "expr".

classref-item-separator

------------------------------------------------------------------------

classref-method

`StructuredTextParser<enum_TextServer_StructuredTextParser>`
**get\_structured\_text\_bidi\_override**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_structured_text_bidi_override>`

Returns the BiDi algorithm override set for this cell.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`
**get\_structured\_text\_bidi\_override\_options**(column:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_structured_text_bidi_override_options>`

Returns the additional BiDi options set for this cell.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_suffix**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_suffix>`

Gets the suffix string shown after the column value.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_text**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_text>`

Returns the given column's text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
**get\_text\_alignment**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_text_alignment>`

Returns the given column's text alignment.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TextDirection<enum_Control_TextDirection>`
**get\_text\_direction**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_text_direction>`

Returns item's text base writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-method

`OverrunBehavior<enum_TextServer_OverrunBehavior>`
**get\_text\_overrun\_behavior**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_text_overrun_behavior>`

Returns the clipping behavior when the text exceeds the item's bounding
rectangle in the given `column`. By default it is
`TextServer.OVERRUN_TRIM_ELLIPSIS<class_TextServer_constant_OVERRUN_TRIM_ELLIPSIS>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_tooltip\_text**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_tooltip_text>`

Returns the given column's tooltip text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tree<class_Tree>` **get\_tree**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_get_tree>`

Returns the `Tree<class_Tree>` that owns this TreeItem.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_any\_collapsed**(only\_visible:
`bool<class_bool>` = false) `🔗<class_TreeItem_method_is_any_collapsed>`

Returns `true` if this **TreeItem**, or any of its descendants, is
collapsed.

If `only_visible` is `true` it ignores non-visible **TreeItem**s.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_button\_disabled**(column: `int<class_int>`,
button\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_is_button_disabled>`

Returns `true` if the button at index `button_index` for the given
`column` is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_checked**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_is_checked>`

Returns `true` if the given `column` is checked.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_custom\_set\_as\_button**(column:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_is_custom_set_as_button>`

Returns `true` if the cell was made into a button with
`set_custom_as_button<class_TreeItem_method_set_custom_as_button>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_edit\_multiline**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_is_edit_multiline>`

Returns `true` if the given `column` is multiline editable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_editable**(column: `int<class_int>`)
`🔗<class_TreeItem_method_is_editable>`

Returns `true` if the given `column` is editable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_indeterminate**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_is_indeterminate>`

Returns `true` if the given `column` is indeterminate.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_selectable**(column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_is_selectable>`

Returns `true` if the given `column` is selectable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_selected**(column: `int<class_int>`)
`🔗<class_TreeItem_method_is_selected>`

Returns `true` if the given `column` is selected.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_visible\_in\_tree**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TreeItem_method_is_visible_in_tree>`

Returns `true` if `visible<class_TreeItem_property_visible>` is `true`
and all its ancestors are also visible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_after**(item:
`TreeItem<class_TreeItem>`) `🔗<class_TreeItem_method_move_after>`

Moves this TreeItem right after the given `item`.

\*\*Note:\*\* You can't move to the root or move the root.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_before**(item:
`TreeItem<class_TreeItem>`) `🔗<class_TreeItem_method_move_before>`

Moves this TreeItem right before the given `item`.

\*\*Note:\*\* You can't move to the root or move the root.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **propagate\_check**(column: `int<class_int>`,
emit\_signal: `bool<class_bool>` = true)
`🔗<class_TreeItem_method_propagate_check>`

Propagates this item's checked status to its children and parents for
the given `column`. It is possible to process the items affected by this
method call by connecting to
`Tree.check_propagated_to_item<class_Tree_signal_check_propagated_to_item>`.
The order that the items affected will be processed is as follows: the
item invoking this method, children of that item, and finally parents of
that item. If `emit_signal` is `false`, then
`Tree.check_propagated_to_item<class_Tree_signal_check_propagated_to_item>`
will not be emitted.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_child**(child:
`TreeItem<class_TreeItem>`) `🔗<class_TreeItem_method_remove_child>`

Removes the given child **TreeItem** and all its children from the
`Tree<class_Tree>`. Note that it doesn't free the item from memory, so
it can be reused later (see
`add_child<class_TreeItem_method_add_child>`). To completely remove a
**TreeItem** use `Object.free<class_Object_method_free>`.

\*\*Note:\*\* If you want to move a child from one `Tree<class_Tree>` to
another, then instead of removing and adding it manually you can use
`move_before<class_TreeItem_method_move_before>` or
`move_after<class_TreeItem_method_move_after>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **select**(column: `int<class_int>`)
`🔗<class_TreeItem_method_select>`

Selects the given `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_auto\_translate\_mode**(column:
`int<class_int>`, mode:
`AutoTranslateMode<enum_Node_AutoTranslateMode>`)
`🔗<class_TreeItem_method_set_auto_translate_mode>`

Sets the given column's auto translate mode to `mode`.

All columns use
`Node.AUTO_TRANSLATE_MODE_INHERIT<class_Node_constant_AUTO_TRANSLATE_MODE_INHERIT>`
by default, which uses the same auto translate mode as the
`Tree<class_Tree>` itself.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_autowrap\_mode**(column:
`int<class_int>`, autowrap\_mode:
`AutowrapMode<enum_TextServer_AutowrapMode>`)
`🔗<class_TreeItem_method_set_autowrap_mode>`

Sets the autowrap mode in the given `column`. If set to something other
than `TextServer.AUTOWRAP_OFF<class_TextServer_constant_AUTOWRAP_OFF>`,
the text gets wrapped inside the cell's bounding rectangle.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_button**(column: `int<class_int>`,
button\_index: `int<class_int>`, button: `Texture2D<class_Texture2D>`)
`🔗<class_TreeItem_method_set_button>`

Sets the given column's button `Texture2D<class_Texture2D>` at index
`button_index` to `button`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_button\_color**(column:
`int<class_int>`, button\_index: `int<class_int>`, color:
`Color<class_Color>`) `🔗<class_TreeItem_method_set_button_color>`

Sets the given column's button color at index `button_index` to `color`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_button\_disabled**(column:
`int<class_int>`, button\_index: `int<class_int>`, disabled:
`bool<class_bool>`) `🔗<class_TreeItem_method_set_button_disabled>`

If `true`, disables the button at index `button_index` in the given
`column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_button\_tooltip\_text**(column:
`int<class_int>`, button\_index: `int<class_int>`, tooltip:
`String<class_String>`)
`🔗<class_TreeItem_method_set_button_tooltip_text>`

Sets the tooltip text for the button at index `button_index` in the
given `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_cell\_mode**(column: `int<class_int>`,
mode: `TreeCellMode<enum_TreeItem_TreeCellMode>`)
`🔗<class_TreeItem_method_set_cell_mode>`

Sets the given column's cell mode to `mode`. This determines how the
cell is displayed and edited. See
`TreeCellMode<enum_TreeItem_TreeCellMode>` constants for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_checked**(column: `int<class_int>`,
checked: `bool<class_bool>`) `🔗<class_TreeItem_method_set_checked>`

If `checked` is `true`, the given `column` is checked. Clears column's
indeterminate status.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_collapsed\_recursive**(enable:
`bool<class_bool>`) `🔗<class_TreeItem_method_set_collapsed_recursive>`

Collapses or uncollapses this **TreeItem** and all the descendants of
this item.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_custom\_as\_button**(column:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_TreeItem_method_set_custom_as_button>`

Makes a cell with
`CELL_MODE_CUSTOM<class_TreeItem_constant_CELL_MODE_CUSTOM>` display as
a non-flat button with a `StyleBox<class_StyleBox>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_custom\_bg\_color**(column:
`int<class_int>`, color: `Color<class_Color>`, just\_outline:
`bool<class_bool>` = false)
`🔗<class_TreeItem_method_set_custom_bg_color>`

Sets the given column's custom background color and whether to just use
it as an outline.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_custom\_color**(column:
`int<class_int>`, color: `Color<class_Color>`)
`🔗<class_TreeItem_method_set_custom_color>`

Sets the given column's custom color.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_custom\_draw**(column:
`int<class_int>`, object: `Object<class_Object>`, callback:
`StringName<class_StringName>`)
`🔗<class_TreeItem_method_set_custom_draw>`

**Deprecated:** Use
`set_custom_draw_callback<class_TreeItem_method_set_custom_draw_callback>`
instead.

Sets the given column's custom draw callback to the `callback` method on
`object`.

The method named `callback` should accept two arguments: the
**TreeItem** that is drawn and its position and size as a
`Rect2<class_Rect2>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_custom\_draw\_callback**(column:
`int<class_int>`, callback: `Callable<class_Callable>`)
`🔗<class_TreeItem_method_set_custom_draw_callback>`

Sets the given column's custom draw callback. Use an empty
`Callable<class_Callable>` (`Callable()`) to clear the custom callback.
The cell has to be in
`CELL_MODE_CUSTOM<class_TreeItem_constant_CELL_MODE_CUSTOM>` to use this
feature.

The `callback` should accept two arguments: the **TreeItem** that is
drawn and its position and size as a `Rect2<class_Rect2>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_custom\_font**(column:
`int<class_int>`, font: `Font<class_Font>`)
`🔗<class_TreeItem_method_set_custom_font>`

Sets custom font used to draw text in the given `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_custom\_font\_size**(column:
`int<class_int>`, font\_size: `int<class_int>`)
`🔗<class_TreeItem_method_set_custom_font_size>`

Sets custom font size used to draw text in the given `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_edit\_multiline**(column:
`int<class_int>`, multiline: `bool<class_bool>`)
`🔗<class_TreeItem_method_set_edit_multiline>`

If `multiline` is `true`, the given `column` is multiline editable.

\*\*Note:\*\* This option only affects the type of control
(`LineEdit<class_LineEdit>` or `TextEdit<class_TextEdit>`) that appears
when editing the column. You can set multiline values with
`set_text<class_TreeItem_method_set_text>` even if the column is not
multiline editable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_editable**(column: `int<class_int>`,
enabled: `bool<class_bool>`) `🔗<class_TreeItem_method_set_editable>`

If `enabled` is `true`, the given `column` is editable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_expand\_right**(column:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_TreeItem_method_set_expand_right>`

If `enable` is `true`, the given `column` is expanded to the right.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_icon**(column: `int<class_int>`,
texture: `Texture2D<class_Texture2D>`)
`🔗<class_TreeItem_method_set_icon>`

Sets the given cell's icon `Texture2D<class_Texture2D>`. If the cell is
in `CELL_MODE_ICON<class_TreeItem_constant_CELL_MODE_ICON>` mode, the
icon is displayed in the center of the cell. Otherwise, the icon is
displayed before the cell's text.
`CELL_MODE_RANGE<class_TreeItem_constant_CELL_MODE_RANGE>` does not
display an icon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_icon\_max\_width**(column:
`int<class_int>`, width: `int<class_int>`)
`🔗<class_TreeItem_method_set_icon_max_width>`

Sets the maximum allowed width of the icon in the given `column`. This
limit is applied on top of the default size of the icon and on top of
`Tree.icon_max_width<class_Tree_theme_constant_icon_max_width>`. The
height is adjusted according to the icon's ratio.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_icon\_modulate**(column:
`int<class_int>`, modulate: `Color<class_Color>`)
`🔗<class_TreeItem_method_set_icon_modulate>`

Modulates the given column's icon with `modulate`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_icon\_overlay**(column:
`int<class_int>`, texture: `Texture2D<class_Texture2D>`)
`🔗<class_TreeItem_method_set_icon_overlay>`

Sets the given cell's icon overlay `Texture2D<class_Texture2D>`. The
cell has to be in
`CELL_MODE_ICON<class_TreeItem_constant_CELL_MODE_ICON>` mode, and icon
has to be set. Overlay is drawn on top of icon, in the bottom left
corner.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_icon\_region**(column:
`int<class_int>`, region: `Rect2<class_Rect2>`)
`🔗<class_TreeItem_method_set_icon_region>`

Sets the given column's icon's texture region.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_indeterminate**(column:
`int<class_int>`, indeterminate: `bool<class_bool>`)
`🔗<class_TreeItem_method_set_indeterminate>`

If `indeterminate` is `true`, the given `column` is marked
indeterminate.

\*\*Note:\*\* If set `true` from `false`, then column is cleared of
checked status.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_language**(column: `int<class_int>`,
language: `String<class_String>`)
`🔗<class_TreeItem_method_set_language>`

Sets language code of item's text used for line-breaking and text
shaping algorithms, if left empty current locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_metadata**(column: `int<class_int>`,
meta: `Variant<class_Variant>`) `🔗<class_TreeItem_method_set_metadata>`

Sets the metadata value for the given column, which can be retrieved
later using `get_metadata<class_TreeItem_method_get_metadata>`. This can
be used, for example, to store a reference to the original data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_range**(column: `int<class_int>`,
value: `float<class_float>`) `🔗<class_TreeItem_method_set_range>`

Sets the value of a
`CELL_MODE_RANGE<class_TreeItem_constant_CELL_MODE_RANGE>` column.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_range\_config**(column:
`int<class_int>`, min: `float<class_float>`, max: `float<class_float>`,
step: `float<class_float>`, expr: `bool<class_bool>` = false)
`🔗<class_TreeItem_method_set_range_config>`

Sets the range of accepted values for a column. The column must be in
the `CELL_MODE_RANGE<class_TreeItem_constant_CELL_MODE_RANGE>` mode.

If `expr` is `true`, the edit mode slider will use an exponential scale
as with `Range.exp_edit<class_Range_property_exp_edit>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_selectable**(column: `int<class_int>`,
selectable: `bool<class_bool>`)
`🔗<class_TreeItem_method_set_selectable>`

If `selectable` is `true`, the given `column` is selectable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_structured\_text\_bidi\_override**(column: `int<class_int>`,
parser: `StructuredTextParser<enum_TextServer_StructuredTextParser>`)
`🔗<class_TreeItem_method_set_structured_text_bidi_override>`

Set BiDi algorithm override for the structured text. Has effect for
cells that display text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_structured\_text\_bidi\_override\_options**(column:
`int<class_int>`, args: `Array<class_Array>`)
`🔗<class_TreeItem_method_set_structured_text_bidi_override_options>`

Set additional options for BiDi override. Has effect for cells that
display text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_suffix**(column: `int<class_int>`,
text: `String<class_String>`) `🔗<class_TreeItem_method_set_suffix>`

Sets a string to be shown after a column's value (for example, a unit
abbreviation).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_text**(column: `int<class_int>`, text:
`String<class_String>`) `🔗<class_TreeItem_method_set_text>`

Sets the given column's text value.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_text\_alignment**(column:
`int<class_int>`, text\_alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`)
`🔗<class_TreeItem_method_set_text_alignment>`

Sets the given column's text alignment. See
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` for
possible values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_text\_direction**(column:
`int<class_int>`, direction:
`TextDirection<enum_Control_TextDirection>`)
`🔗<class_TreeItem_method_set_text_direction>`

Sets item's text base writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_text\_overrun\_behavior**(column:
`int<class_int>`, overrun\_behavior:
`OverrunBehavior<enum_TextServer_OverrunBehavior>`)
`🔗<class_TreeItem_method_set_text_overrun_behavior>`

Sets the clipping behavior when the text exceeds the item's bounding
rectangle in the given `column`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tooltip\_text**(column:
`int<class_int>`, tooltip: `String<class_String>`)
`🔗<class_TreeItem_method_set_tooltip_text>`

Sets the given column's tooltip text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **uncollapse\_tree**()
`🔗<class_TreeItem_method_uncollapse_tree>`

Uncollapses all **TreeItem**s necessary to reveal this **TreeItem**,
i.e. all ancestor **TreeItem**s.
