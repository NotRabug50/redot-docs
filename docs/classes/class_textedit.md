github\_url  
hide

# TextEdit

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `CodeEdit<class_CodeEdit>`

A multiline text editor.

classref-introduction-group

## Description

A multiline text editor. It also has limited facilities for editing
code, such as syntax highlighting support. For more advanced facilities
for editing code, see `CodeEdit<class_CodeEdit>`.

\*\*Note:\*\* Most viewport, caret, and edit methods contain a
`caret_index` argument for
`caret_multiple<class_TextEdit_property_caret_multiple>` support. The
argument should be one of the following: `-1` for all carets, `0` for
the main caret, or greater than `0` for secondary carets in the order
they were created.

\*\*Note:\*\* When holding down `Alt`, the vertical scroll wheel will
scroll 5 times as fast as it would normally do. This also works in the
Godot script editor.

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**caret\_changed**() `🔗<class_TextEdit_signal_caret_changed>`

Emitted when any caret changes position.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**gutter\_added**() `🔗<class_TextEdit_signal_gutter_added>`

Emitted when a gutter is added.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**gutter\_clicked**(line: `int<class_int>`, gutter: `int<class_int>`)
`🔗<class_TextEdit_signal_gutter_clicked>`

Emitted when a gutter is clicked.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**gutter\_removed**() `🔗<class_TextEdit_signal_gutter_removed>`

Emitted when a gutter is removed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**lines\_edited\_from**(from\_line: `int<class_int>`, to\_line:
`int<class_int>`) `🔗<class_TextEdit_signal_lines_edited_from>`

Emitted immediately when the text changes.

When text is added `from_line` will be less than `to_line`. On a remove
`to_line` will be less than `from_line`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**text\_changed**() `🔗<class_TextEdit_signal_text_changed>`

Emitted when the text changes.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**text\_set**() `🔗<class_TextEdit_signal_text_set>`

Emitted when `clear<class_TextEdit_method_clear>` is called or
`text<class_TextEdit_property_text>` is set.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **MenuItems**: `🔗<enum_TextEdit_MenuItems>`

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_CUT** = `0`

Cuts (copies and clears) the selected text.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_COPY** = `1`

Copies the selected text.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_PASTE** = `2`

Pastes the clipboard text over the selected text (or at the cursor's
position).

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_CLEAR** = `3`

Erases the whole **TextEdit** text.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_SELECT\_ALL** = `4`

Selects the whole **TextEdit** text.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_UNDO** = `5`

Undoes the previous action.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_REDO** = `6`

Redoes the previous action.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_SUBMENU\_TEXT\_DIR** = `7`

ID of "Text Writing Direction" submenu.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_DIR\_INHERITED** = `8`

Sets text direction to inherited.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_DIR\_AUTO** = `9`

Sets text direction to automatic.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_DIR\_LTR** = `10`

Sets text direction to left-to-right.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_DIR\_RTL** = `11`

Sets text direction to right-to-left.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_DISPLAY\_UCC** = `12`

Toggles control character display.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_SUBMENU\_INSERT\_UCC** =
`13`

ID of "Insert Control Character" submenu.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_LRM** = `14`

Inserts left-to-right mark (LRM) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_RLM** = `15`

Inserts right-to-left mark (RLM) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_LRE** = `16`

Inserts start of left-to-right embedding (LRE) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_RLE** = `17`

Inserts start of right-to-left embedding (RLE) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_LRO** = `18`

Inserts start of left-to-right override (LRO) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_RLO** = `19`

Inserts start of right-to-left override (RLO) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_PDF** = `20`

Inserts pop direction formatting (PDF) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_ALM** = `21`

Inserts Arabic letter mark (ALM) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_LRI** = `22`

Inserts left-to-right isolate (LRI) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_RLI** = `23`

Inserts right-to-left isolate (RLI) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_FSI** = `24`

Inserts first strong isolate (FSI) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_PDI** = `25`

Inserts pop direction isolate (PDI) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_ZWJ** = `26`

Inserts zero width joiner (ZWJ) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_ZWNJ** = `27`

Inserts zero width non-joiner (ZWNJ) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_WJ** = `28`

Inserts word joiner (WJ) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_INSERT\_SHY** = `29`

Inserts soft hyphen (SHY) character.

classref-enumeration-constant

`MenuItems<enum_TextEdit_MenuItems>` **MENU\_MAX** = `30`

Represents the size of the `MenuItems<enum_TextEdit_MenuItems>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EditAction**: `🔗<enum_TextEdit_EditAction>`

classref-enumeration-constant

`EditAction<enum_TextEdit_EditAction>` **ACTION\_NONE** = `0`

No current action.

classref-enumeration-constant

`EditAction<enum_TextEdit_EditAction>` **ACTION\_TYPING** = `1`

A typing action.

classref-enumeration-constant

`EditAction<enum_TextEdit_EditAction>` **ACTION\_BACKSPACE** = `2`

A backwards delete action.

classref-enumeration-constant

`EditAction<enum_TextEdit_EditAction>` **ACTION\_DELETE** = `3`

A forward delete action.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SearchFlags**: `🔗<enum_TextEdit_SearchFlags>`

classref-enumeration-constant

`SearchFlags<enum_TextEdit_SearchFlags>` **SEARCH\_MATCH\_CASE** = `1`

Match case when searching.

classref-enumeration-constant

`SearchFlags<enum_TextEdit_SearchFlags>` **SEARCH\_WHOLE\_WORDS** = `2`

Match whole words when searching.

classref-enumeration-constant

`SearchFlags<enum_TextEdit_SearchFlags>` **SEARCH\_BACKWARDS** = `4`

Search from end to beginning.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CaretType**: `🔗<enum_TextEdit_CaretType>`

classref-enumeration-constant

`CaretType<enum_TextEdit_CaretType>` **CARET\_TYPE\_LINE** = `0`

Vertical line caret.

classref-enumeration-constant

`CaretType<enum_TextEdit_CaretType>` **CARET\_TYPE\_BLOCK** = `1`

Block caret.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SelectionMode**: `🔗<enum_TextEdit_SelectionMode>`

classref-enumeration-constant

`SelectionMode<enum_TextEdit_SelectionMode>` **SELECTION\_MODE\_NONE** =
`0`

Not selecting.

classref-enumeration-constant

`SelectionMode<enum_TextEdit_SelectionMode>` **SELECTION\_MODE\_SHIFT**
= `1`

Select as if `shift` is pressed.

classref-enumeration-constant

`SelectionMode<enum_TextEdit_SelectionMode>`
**SELECTION\_MODE\_POINTER** = `2`

Select single characters as if the user single clicked.

classref-enumeration-constant

`SelectionMode<enum_TextEdit_SelectionMode>` **SELECTION\_MODE\_WORD** =
`3`

Select whole words as if the user double clicked.

classref-enumeration-constant

`SelectionMode<enum_TextEdit_SelectionMode>` **SELECTION\_MODE\_LINE** =
`4`

Select whole lines as if the user triple clicked.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LineWrappingMode**: `🔗<enum_TextEdit_LineWrappingMode>`

classref-enumeration-constant

`LineWrappingMode<enum_TextEdit_LineWrappingMode>`
**LINE\_WRAPPING\_NONE** = `0`

Line wrapping is disabled.

classref-enumeration-constant

`LineWrappingMode<enum_TextEdit_LineWrappingMode>`
**LINE\_WRAPPING\_BOUNDARY** = `1`

Line wrapping occurs at the control boundary, beyond what would normally
be visible.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **GutterType**: `🔗<enum_TextEdit_GutterType>`

classref-enumeration-constant

`GutterType<enum_TextEdit_GutterType>` **GUTTER\_TYPE\_STRING** = `0`

When a gutter is set to string using
`set_gutter_type<class_TextEdit_method_set_gutter_type>`, it is used to
contain text set via the
`set_line_gutter_text<class_TextEdit_method_set_line_gutter_text>`
method.

classref-enumeration-constant

`GutterType<enum_TextEdit_GutterType>` **GUTTER\_TYPE\_ICON** = `1`

When a gutter is set to icon using
`set_gutter_type<class_TextEdit_method_set_gutter_type>`, it is used to
contain an icon set via the
`set_line_gutter_icon<class_TextEdit_method_set_line_gutter_icon>`
method.

classref-enumeration-constant

`GutterType<enum_TextEdit_GutterType>` **GUTTER\_TYPE\_CUSTOM** = `2`

When a gutter is set to custom using
`set_gutter_type<class_TextEdit_method_set_gutter_type>`, it is used to
contain custom visuals controlled by a callback method set via the
`set_gutter_custom_draw<class_TextEdit_method_set_gutter_custom_draw>`
method.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`AutowrapMode<enum_TextServer_AutowrapMode>` **autowrap\_mode** = `3`
`🔗<class_TextEdit_property_autowrap_mode>`

classref-property-setget

-   `void (No return value.)` **set\_autowrap\_mode**(value:
    `AutowrapMode<enum_TextServer_AutowrapMode>`)
-   `AutowrapMode<enum_TextServer_AutowrapMode>`
    **get\_autowrap\_mode**()

If `wrap_mode<class_TextEdit_property_wrap_mode>` is set to
`LINE_WRAPPING_BOUNDARY<class_TextEdit_constant_LINE_WRAPPING_BOUNDARY>`,
sets text wrapping mode. To see how each mode behaves, see
`AutowrapMode<enum_TextServer_AutowrapMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **caret\_blink** = `false`
`🔗<class_TextEdit_property_caret_blink>`

classref-property-setget

-   `void (No return value.)` **set\_caret\_blink\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_caret\_blink\_enabled**()

If `true`, makes the caret blink.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **caret\_blink\_interval** = `0.65`
`🔗<class_TextEdit_property_caret_blink_interval>`

classref-property-setget

-   `void (No return value.)` **set\_caret\_blink\_interval**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_caret\_blink\_interval**()

The interval at which the caret blinks (in seconds).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **caret\_draw\_when\_editable\_disabled** = `false`
`🔗<class_TextEdit_property_caret_draw_when_editable_disabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_draw\_caret\_when\_editable\_disabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>`
    **is\_drawing\_caret\_when\_editable\_disabled**()

If `true`, caret will be visible when
`editable<class_TextEdit_property_editable>` is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **caret\_mid\_grapheme** = `false`
`🔗<class_TextEdit_property_caret_mid_grapheme>`

classref-property-setget

-   `void (No return value.)`
    **set\_caret\_mid\_grapheme\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_caret\_mid\_grapheme\_enabled**()

Allow moving caret, selecting and removing the individual composite
character components.

\*\*Note:\*\* `Backspace` is always removing individual composite
character components.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **caret\_move\_on\_right\_click** = `true`
`🔗<class_TextEdit_property_caret_move_on_right_click>`

classref-property-setget

-   `void (No return value.)`
    **set\_move\_caret\_on\_right\_click\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_move\_caret\_on\_right\_click\_enabled**()

If `true`, a right-click moves the caret at the mouse position before
displaying the context menu.

If `false`, the context menu ignores mouse location.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **caret\_multiple** = `true`
`🔗<class_TextEdit_property_caret_multiple>`

classref-property-setget

-   `void (No return value.)` **set\_multiple\_carets\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_multiple\_carets\_enabled**()

Sets if multiple carets are allowed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CaretType<enum_TextEdit_CaretType>` **caret\_type** = `0`
`🔗<class_TextEdit_property_caret_type>`

classref-property-setget

-   `void (No return value.)` **set\_caret\_type**(value:
    `CaretType<enum_TextEdit_CaretType>`)
-   `CaretType<enum_TextEdit_CaretType>` **get\_caret\_type**()

Set the type of caret to draw.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **context\_menu\_enabled** = `true`
`🔗<class_TextEdit_property_context_menu_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_context\_menu\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_context\_menu\_enabled**()

If `true`, a right-click displays the context menu.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **custom\_word\_separators** = `""`
`🔗<class_TextEdit_property_custom_word_separators>`

classref-property-setget

-   `void (No return value.)` **set\_custom\_word\_separators**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_custom\_word\_separators**()

The characters to consider as word delimiters if
`use_custom_word_separators<class_TextEdit_property_use_custom_word_separators>`
is `true`. The characters should be defined without separation, for
example `#_!`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **deselect\_on\_focus\_loss\_enabled** = `true`
`🔗<class_TextEdit_property_deselect_on_focus_loss_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_deselect\_on\_focus\_loss\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_deselect\_on\_focus\_loss\_enabled**()

If `true`, the selected text will be deselected when focus is lost.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **drag\_and\_drop\_selection\_enabled** = `true`
`🔗<class_TextEdit_property_drag_and_drop_selection_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_drag\_and\_drop\_selection\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_drag\_and\_drop\_selection\_enabled**()

If `true`, allow drag and drop of selected text. Text can still be
dropped from other sources.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **draw\_control\_chars** = `false`
`🔗<class_TextEdit_property_draw_control_chars>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_control\_chars**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_draw\_control\_chars**()

If `true`, control characters are displayed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **draw\_spaces** = `false`
`🔗<class_TextEdit_property_draw_spaces>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_spaces**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_drawing\_spaces**()

If `true`, the "space" character will have a visible representation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **draw\_tabs** = `false`
`🔗<class_TextEdit_property_draw_tabs>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_tabs**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_drawing\_tabs**()

If `true`, the "tab" character will have a visible representation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editable** = `true`
`🔗<class_TextEdit_property_editable>`

classref-property-setget

-   `void (No return value.)` **set\_editable**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_editable**()

If `false`, existing text cannot be modified and new text cannot be
added.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **empty\_selection\_clipboard\_enabled** = `true`
`🔗<class_TextEdit_property_empty_selection_clipboard_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_empty\_selection\_clipboard\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_empty\_selection\_clipboard\_enabled**()

If `true`, copying or cutting without a selection is performed on all
lines with a caret. Otherwise, copy and cut require a selection.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **highlight\_all\_occurrences** = `false`
`🔗<class_TextEdit_property_highlight_all_occurrences>`

classref-property-setget

-   `void (No return value.)`
    **set\_highlight\_all\_occurrences**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_highlight\_all\_occurrences\_enabled**()

If `true`, all occurrences of the selected text will be highlighted.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **highlight\_current\_line** = `false`
`🔗<class_TextEdit_property_highlight_current_line>`

classref-property-setget

-   `void (No return value.)` **set\_highlight\_current\_line**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_highlight\_current\_line\_enabled**()

If `true`, the line containing the cursor is highlighted.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **indent\_wrapped\_lines** = `false`
`🔗<class_TextEdit_property_indent_wrapped_lines>`

classref-property-setget

-   `void (No return value.)` **set\_indent\_wrapped\_lines**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_indent\_wrapped\_lines**()

If `true`, all wrapped lines are indented to the same amount as the
unwrapped line.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **language** = `""`
`🔗<class_TextEdit_property_language>`

classref-property-setget

-   `void (No return value.)` **set\_language**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_language**()

Language code used for line-breaking and text shaping algorithms, if
left empty current locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **middle\_mouse\_paste\_enabled** = `true`
`🔗<class_TextEdit_property_middle_mouse_paste_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_middle\_mouse\_paste\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_middle\_mouse\_paste\_enabled**()

If `false`, using middle mouse button to paste clipboard will be
disabled.

\*\*Note:\*\* This method is only implemented on Linux.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **minimap\_draw** = `false`
`🔗<class_TextEdit_property_minimap_draw>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_minimap**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_drawing\_minimap**()

If `true`, a minimap is shown, providing an outline of your source code.
The minimap uses a fixed-width text size.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **minimap\_width** = `80`
`🔗<class_TextEdit_property_minimap_width>`

classref-property-setget

-   `void (No return value.)` **set\_minimap\_width**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_minimap\_width**()

The width, in pixels, of the minimap.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **placeholder\_text** = `""`
`🔗<class_TextEdit_property_placeholder_text>`

classref-property-setget

-   `void (No return value.)` **set\_placeholder**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_placeholder**()

Text shown when the **TextEdit** is empty. It is **not** the
**TextEdit**'s default value (see `text<class_TextEdit_property_text>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **scroll\_fit\_content\_height** = `false`
`🔗<class_TextEdit_property_scroll_fit_content_height>`

classref-property-setget

-   `void (No return value.)`
    **set\_fit\_content\_height\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_fit\_content\_height\_enabled**()

If `true`, **TextEdit** will disable vertical scroll and fit minimum
height to the number of visible lines. When both this property and
`scroll_fit_content_width<class_TextEdit_property_scroll_fit_content_width>`
are `true`, no scrollbars will be displayed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **scroll\_fit\_content\_width** = `false`
`🔗<class_TextEdit_property_scroll_fit_content_width>`

classref-property-setget

-   `void (No return value.)`
    **set\_fit\_content\_width\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_fit\_content\_width\_enabled**()

If `true`, **TextEdit** will disable horizontal scroll and fit minimum
width to the widest line in the text. When both this property and
`scroll_fit_content_height<class_TextEdit_property_scroll_fit_content_height>`
are `true`, no scrollbars will be displayed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **scroll\_horizontal** = `0`
`🔗<class_TextEdit_property_scroll_horizontal>`

classref-property-setget

-   `void (No return value.)` **set\_h\_scroll**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_h\_scroll**()

If there is a horizontal scrollbar, this determines the current
horizontal scroll value in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **scroll\_past\_end\_of\_file** = `false`
`🔗<class_TextEdit_property_scroll_past_end_of_file>`

classref-property-setget

-   `void (No return value.)`
    **set\_scroll\_past\_end\_of\_file\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_scroll\_past\_end\_of\_file\_enabled**()

Allow scrolling past the last line into "virtual" space.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **scroll\_smooth** = `false`
`🔗<class_TextEdit_property_scroll_smooth>`

classref-property-setget

-   `void (No return value.)` **set\_smooth\_scroll\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_smooth\_scroll\_enabled**()

Scroll smoothly over the text rather than jumping to the next location.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **scroll\_v\_scroll\_speed** = `80.0`
`🔗<class_TextEdit_property_scroll_v_scroll_speed>`

classref-property-setget

-   `void (No return value.)` **set\_v\_scroll\_speed**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_v\_scroll\_speed**()

Sets the scroll speed with the minimap or when
`scroll_smooth<class_TextEdit_property_scroll_smooth>` is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **scroll\_vertical** = `0.0`
`🔗<class_TextEdit_property_scroll_vertical>`

classref-property-setget

-   `void (No return value.)` **set\_v\_scroll**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_v\_scroll**()

If there is a vertical scrollbar, this determines the current vertical
scroll value in line numbers, starting at 0 for the top line.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **selecting\_enabled** = `true`
`🔗<class_TextEdit_property_selecting_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_selecting\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_selecting\_enabled**()

If `true`, text can be selected.

If `false`, text can not be selected by the user or by the
`select<class_TextEdit_method_select>` or
`select_all<class_TextEdit_method_select_all>` methods.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shortcut\_keys\_enabled** = `true`
`🔗<class_TextEdit_property_shortcut_keys_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_shortcut\_keys\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_shortcut\_keys\_enabled**()

If `true`, shortcut keys for context menu items are enabled, even if the
context menu is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StructuredTextParser<enum_TextServer_StructuredTextParser>`
**structured\_text\_bidi\_override** = `0`
`🔗<class_TextEdit_property_structured_text_bidi_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_structured\_text\_bidi\_override**(value:
    `StructuredTextParser<enum_TextServer_StructuredTextParser>`)
-   `StructuredTextParser<enum_TextServer_StructuredTextParser>`
    **get\_structured\_text\_bidi\_override**()

Set BiDi algorithm override for the structured text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>` **structured\_text\_bidi\_override\_options** =
`[]` `🔗<class_TextEdit_property_structured_text_bidi_override_options>`

classref-property-setget

-   `void (No return value.)`
    **set\_structured\_text\_bidi\_override\_options**(value:
    `Array<class_Array>`)
-   `Array<class_Array>`
    **get\_structured\_text\_bidi\_override\_options**()

Set additional options for BiDi override.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SyntaxHighlighter<class_SyntaxHighlighter>` **syntax\_highlighter**
`🔗<class_TextEdit_property_syntax_highlighter>`

classref-property-setget

-   `void (No return value.)` **set\_syntax\_highlighter**(value:
    `SyntaxHighlighter<class_SyntaxHighlighter>`)
-   `SyntaxHighlighter<class_SyntaxHighlighter>`
    **get\_syntax\_highlighter**()

The syntax highlighter to use.

\*\*Note:\*\* A `SyntaxHighlighter<class_SyntaxHighlighter>` instance
should not be used across multiple **TextEdit** nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **text** = `""`
`🔗<class_TextEdit_property_text>`

classref-property-setget

-   `void (No return value.)` **set\_text**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_text**()

String value of the **TextEdit**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextDirection<enum_Control_TextDirection>` **text\_direction** = `0`
`🔗<class_TextEdit_property_text_direction>`

classref-property-setget

-   `void (No return value.)` **set\_text\_direction**(value:
    `TextDirection<enum_Control_TextDirection>`)
-   `TextDirection<enum_Control_TextDirection>`
    **get\_text\_direction**()

Base text writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_custom\_word\_separators** = `false`
`🔗<class_TextEdit_property_use_custom_word_separators>`

classref-property-setget

-   `void (No return value.)`
    **set\_use\_custom\_word\_separators**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_custom\_word\_separators\_enabled**()

If `false`, using `Ctrl + Left` or `Ctrl + Right` (`Cmd + Left` or
`Cmd + Right` on macOS) bindings will use the behavior of
`use_default_word_separators<class_TextEdit_property_use_default_word_separators>`.
If `true`, it will also stop the caret if a character within
`custom_word_separators<class_TextEdit_property_custom_word_separators>`
is detected. Useful for subword moving. This behavior also will be
applied to the behavior of text selection.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_default\_word\_separators** = `true`
`🔗<class_TextEdit_property_use_default_word_separators>`

classref-property-setget

-   `void (No return value.)`
    **set\_use\_default\_word\_separators**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_default\_word\_separators\_enabled**()

If `false`, using `Ctrl + Left` or `Ctrl + Right` (`Cmd + Left` or
`Cmd + Right` on macOS) bindings will stop moving caret only if a space
or punctuation is detected. If `true`, it will also stop the caret if a
character is part of `` !"#$%&'()*+,-./:;<=>?@[\]^`{|}~ ``, the Unicode
General Punctuation table, or the Unicode CJK Punctuation table. Useful
for subword moving. This behavior also will be applied to the behavior
of text selection.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **virtual\_keyboard\_enabled** = `true`
`🔗<class_TextEdit_property_virtual_keyboard_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_virtual\_keyboard\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_virtual\_keyboard\_enabled**()

If `true`, the native virtual keyboard is shown when focused on
platforms that support it.

classref-item-separator

------------------------------------------------------------------------

classref-property

`LineWrappingMode<enum_TextEdit_LineWrappingMode>` **wrap\_mode** = `0`
`🔗<class_TextEdit_property_wrap_mode>`

classref-property-setget

-   `void (No return value.)` **set\_line\_wrapping\_mode**(value:
    `LineWrappingMode<enum_TextEdit_LineWrappingMode>`)
-   `LineWrappingMode<enum_TextEdit_LineWrappingMode>`
    **get\_line\_wrapping\_mode**()

Sets the line wrapping mode to use.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_backspace**(caret\_index:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextEdit_private_method__backspace>`

Override this method to define what happens when the user presses the
backspace key.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_copy**(caret\_index: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextEdit_private_method__copy>`

Override this method to define what happens when the user performs a
copy operation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_cut**(caret\_index: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextEdit_private_method__cut>`

Override this method to define what happens when the user performs a cut
operation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_handle\_unicode\_input**(unicode\_char:
`int<class_int>`, caret\_index: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextEdit_private_method__handle_unicode_input>`

Override this method to define what happens when the user types in the
provided key `unicode_char`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_paste**(caret\_index: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextEdit_private_method__paste>`

Override this method to define what happens when the user performs a
paste operation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_paste\_primary\_clipboard**(caret\_index:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextEdit_private_method__paste_primary_clipboard>`

Override this method to define what happens when the user performs a
paste operation with middle mouse button.

\*\*Note:\*\* This method is only implemented on Linux.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **add\_caret**(line: `int<class_int>`, column:
`int<class_int>`) `🔗<class_TextEdit_method_add_caret>`

Adds a new caret at the given location. Returns the index of the new
caret, or `-1` if the location is invalid.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_caret\_at\_carets**(below:
`bool<class_bool>`) `🔗<class_TextEdit_method_add_caret_at_carets>`

Adds an additional caret above or below every caret. If `below` is
`true` the new caret will be added below and above otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_gutter**(at: `int<class_int>` = -1)
`🔗<class_TextEdit_method_add_gutter>`

Register a new gutter to this **TextEdit**. Use `at` to have a specific
gutter order. A value of `-1` appends the gutter to the right.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_selection\_for\_next\_occurrence**()
`🔗<class_TextEdit_method_add_selection_for_next_occurrence>`

Adds a selection and a caret for the next occurrence of the current
selection. If there is no active selection, selects word under caret.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **adjust\_carets\_after\_edit**(caret:
`int<class_int>`, from\_line: `int<class_int>`, from\_col:
`int<class_int>`, to\_line: `int<class_int>`, to\_col: `int<class_int>`)
`🔗<class_TextEdit_method_adjust_carets_after_edit>`

**Deprecated:** No longer necessary since methods now adjust carets
themselves.

This method does nothing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **adjust\_viewport\_to\_caret**(caret\_index:
`int<class_int>` = 0)
`🔗<class_TextEdit_method_adjust_viewport_to_caret>`

Adjust the viewport so the caret is visible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_ime**()
`🔗<class_TextEdit_method_apply_ime>`

Applies text from the [Input Method
Editor](https://en.wikipedia.org/wiki/Input_method) (IME) to each caret
and closes the IME if it is open.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **backspace**(caret\_index: `int<class_int>` =
-1) `🔗<class_TextEdit_method_backspace>`

Called when the user presses the backspace key. Can be overridden with
`_backspace<class_TextEdit_private_method__backspace>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **begin\_complex\_operation**()
`🔗<class_TextEdit_method_begin_complex_operation>`

Starts a multipart edit. All edits will be treated as one action until
`end_complex_operation<class_TextEdit_method_end_complex_operation>` is
called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **begin\_multicaret\_edit**()
`🔗<class_TextEdit_method_begin_multicaret_edit>`

Starts an edit for multiple carets. The edit must be ended with
`end_multicaret_edit<class_TextEdit_method_end_multicaret_edit>`.
Multicaret edits can be used to edit text at multiple carets and delay
merging the carets until the end, so the caret indexes aren't affected
immediately.
`begin_multicaret_edit<class_TextEdit_method_begin_multicaret_edit>` and
`end_multicaret_edit<class_TextEdit_method_end_multicaret_edit>` can be
nested, and the merge will happen at the last
`end_multicaret_edit<class_TextEdit_method_end_multicaret_edit>`.

Example usage:

    begin_complex_operation()
    begin_multicaret_edit()
    for i in range(get_caret_count()):
        if multicaret_edit_ignore_caret(i):
            continue
        # Logic here.
    end_multicaret_edit()
    end_complex_operation()

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **cancel\_ime**()
`🔗<class_TextEdit_method_cancel_ime>`

Closes the [Input Method
Editor](https://en.wikipedia.org/wiki/Input_method) (IME) if it is open.
Any text in the IME will be lost.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **center\_viewport\_to\_caret**(caret\_index:
`int<class_int>` = 0)
`🔗<class_TextEdit_method_center_viewport_to_caret>`

Centers the viewport on the line the editing caret is at. This also
resets the
`scroll_horizontal<class_TextEdit_property_scroll_horizontal>` value to
`0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**() `🔗<class_TextEdit_method_clear>`

Performs a full reset of **TextEdit**, including undo history.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_undo\_history**()
`🔗<class_TextEdit_method_clear_undo_history>`

Clears the undo history.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **collapse\_carets**(from\_line:
`int<class_int>`, from\_column: `int<class_int>`, to\_line:
`int<class_int>`, to\_column: `int<class_int>`, inclusive:
`bool<class_bool>` = false) `🔗<class_TextEdit_method_collapse_carets>`

Collapse all carets in the given range to the `from_line` and
`from_column` position.

`inclusive` applies to both ends.

If `is_in_mulitcaret_edit<class_TextEdit_method_is_in_mulitcaret_edit>`
is `true`, carets that are collapsed will be `true` for
`multicaret_edit_ignore_caret<class_TextEdit_method_multicaret_edit_ignore_caret>`.

`merge_overlapping_carets<class_TextEdit_method_merge_overlapping_carets>`
will be called if any carets were collapsed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **copy**(caret\_index: `int<class_int>` = -1)
`🔗<class_TextEdit_method_copy>`

Copies the current text selection. Can be overridden with
`_copy<class_TextEdit_private_method__copy>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **cut**(caret\_index: `int<class_int>` = -1)
`🔗<class_TextEdit_method_cut>`

Cut's the current selection. Can be overridden with
`_cut<class_TextEdit_private_method__cut>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **delete\_selection**(caret\_index:
`int<class_int>` = -1) `🔗<class_TextEdit_method_delete_selection>`

Deletes the selected text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **deselect**(caret\_index: `int<class_int>` =
-1) `🔗<class_TextEdit_method_deselect>`

Deselects the current selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **end\_action**()
`🔗<class_TextEdit_method_end_action>`

Marks the end of steps in the current action started with
`start_action<class_TextEdit_method_start_action>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **end\_complex\_operation**()
`🔗<class_TextEdit_method_end_complex_operation>`

Ends a multipart edit, started with
`begin_complex_operation<class_TextEdit_method_begin_complex_operation>`.
If called outside a complex operation, the current operation is pushed
onto the undo/redo stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **end\_multicaret\_edit**()
`🔗<class_TextEdit_method_end_multicaret_edit>`

Ends an edit for multiple carets, that was started with
`begin_multicaret_edit<class_TextEdit_method_begin_multicaret_edit>`. If
this was the last
`end_multicaret_edit<class_TextEdit_method_end_multicaret_edit>` and
`merge_overlapping_carets<class_TextEdit_method_merge_overlapping_carets>`
was called, carets will be merged.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_caret\_column**(caret\_index: `int<class_int>` =
0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_caret_column>`

Returns the column the editing caret is at.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_caret\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_caret_count>`

Returns the number of carets in this **TextEdit**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_caret\_draw\_pos**(caret\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_caret_draw_pos>`

Returns the caret pixel draw position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**get\_caret\_index\_edit\_order**()
`🔗<class_TextEdit_method_get_caret_index_edit_order>`

**Deprecated:** Carets no longer need to be edited in any specific
order. If the carets need to be sorted, use
`get_sorted_carets<class_TextEdit_method_get_sorted_carets>` instead.

Returns a list of caret indexes in their edit order, this done from
bottom to top. Edit order refers to the way actions such as
`insert_text_at_caret<class_TextEdit_method_insert_text_at_caret>` are
applied.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_caret\_line**(caret\_index: `int<class_int>` =
0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_caret_line>`

Returns the line the editing caret is on.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_caret\_wrap\_index**(caret\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_caret_wrap_index>`

Returns the wrap index the editing caret is on.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_first\_non\_whitespace\_column**(line:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_first_non_whitespace_column>`

Returns the first column containing a non-whitespace character.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_first\_visible\_line**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_first_visible_line>`

Returns the first visible line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_gutter\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_gutter_count>`

Returns the number of gutters registered.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_gutter\_name**(gutter: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_gutter_name>`

Returns the name of the gutter at the given index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`GutterType<enum_TextEdit_GutterType>` **get\_gutter\_type**(gutter:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_gutter_type>`

Returns the type of the gutter at the given index. Gutters can contain
icons, text, or custom visuals. See
`GutterType<enum_TextEdit_GutterType>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_gutter\_width**(gutter: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_gutter_width>`

Returns the width of the gutter at the given index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`HScrollBar<class_HScrollBar>` **get\_h\_scroll\_bar**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_h_scroll_bar>`

Returns the `HScrollBar<class_HScrollBar>` used by **TextEdit**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_indent\_level**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_indent_level>`

Returns the number of spaces and `tab * tab_size` before the first char.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_last\_full\_visible\_line**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_last_full_visible_line>`

Returns the last visible line. Use
`get_last_full_visible_line_wrap_index<class_TextEdit_method_get_last_full_visible_line_wrap_index>`
for the wrap index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_last\_full\_visible\_line\_wrap\_index**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_last_full_visible_line_wrap_index>`

Returns the last visible wrap index of the last visible line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_last\_unhidden\_line**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_last_unhidden_line>`

Returns the last unhidden line in the entire **TextEdit**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_line**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line>`

Returns the text of a specific line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_line\_background\_color**(line:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_background_color>`

Returns the current background color of the line. `Color(0, 0, 0, 0)` is
returned if no color is set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_line\_column\_at\_pos**(position:
`Vector2i<class_Vector2i>`, allow\_out\_of\_bounds: `bool<class_bool>` =
true)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_column_at_pos>`

Returns the line and column at the given position. In the returned
vector, `x` is the column, `y` is the line. If `allow_out_of_bounds` is
`false` and the position is not over the text, both vector values will
be set to `-1`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_line\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_count>`

Returns the number of lines in the text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_line\_gutter\_icon**(line:
`int<class_int>`, gutter: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_gutter_icon>`

Returns the icon currently in `gutter` at `line`. This only works when
the gutter type is
`GUTTER_TYPE_ICON<class_TextEdit_constant_GUTTER_TYPE_ICON>` (see
`set_gutter_type<class_TextEdit_method_set_gutter_type>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_line\_gutter\_item\_color**(line:
`int<class_int>`, gutter: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_gutter_item_color>`

Returns the color currently in `gutter` at `line`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_line\_gutter\_metadata**(line:
`int<class_int>`, gutter: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_gutter_metadata>`

Returns the metadata currently in `gutter` at `line`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_line\_gutter\_text**(line:
`int<class_int>`, gutter: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_gutter_text>`

Returns the text currently in `gutter` at `line`. This only works when
the gutter type is
`GUTTER_TYPE_STRING<class_TextEdit_constant_GUTTER_TYPE_STRING>` (see
`set_gutter_type<class_TextEdit_method_set_gutter_type>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_line\_height**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_height>`

Returns the maximum value of the line height among all lines.

\*\*Note:\*\* The return value is influenced by
`line_spacing<class_TextEdit_theme_constant_line_spacing>` and
`font_size<class_TextEdit_theme_font_size_font_size>`. And it will not
be less than `1`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector2i<class_Vector2i>`\]
**get\_line\_ranges\_from\_carets**(only\_selections: `bool<class_bool>`
= false, merge\_adjacent: `bool<class_bool>` = true)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_ranges_from_carets>`

Returns an `Array<class_Array>` of line ranges where `x` is the first
line and `y` is the last line. All lines within these ranges will have a
caret on them or be part of a selection. Each line will only be part of
one line range, even if it has multiple carets on it.

If a selection's end column
(`get_selection_to_column<class_TextEdit_method_get_selection_to_column>`)
is at column `0`, that line will not be included. If a selection begins
on the line after another selection ends and `merge_adjacent` is `true`,
or they begin and end on the same line, one line range will include both
selections.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_line\_width**(line: `int<class_int>`,
wrap\_index: `int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_width>`

Returns the width in pixels of the `wrap_index` on `line`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_line\_wrap\_count**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_wrap_count>`

Returns the number of times the given line is wrapped.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_line\_wrap\_index\_at\_column**(line:
`int<class_int>`, column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_wrap_index_at_column>`

Returns the wrap index of the given line column.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_line\_wrapped\_text**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_line_wrapped_text>`

Returns an array of `String<class_String>`s representing each wrapped
index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_local\_mouse\_pos**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_local_mouse_pos>`

Returns the local mouse position adjusted for the text direction.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PopupMenu<class_PopupMenu>` **get\_menu**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_menu>`

Returns the `PopupMenu<class_PopupMenu>` of this **TextEdit**. By
default, this menu is displayed when right-clicking on the **TextEdit**.

You can add custom menu items or remove standard ones. Make sure your
IDs don't conflict with the standard ones (see
`MenuItems<enum_TextEdit_MenuItems>`). For example:

gdscript

func \_ready():  
var menu = get\_menu() \# Remove all items after "Redo".
menu.item\_count = menu.get\_item\_index(MENU\_REDO) + 1 \# Add custom
items. menu.add\_separator() menu.add\_item("Insert Date",
MENU\_MAX + 1) \# Connect callback.
menu.id\_pressed.connect(\_on\_item\_pressed)

func \_on\_item\_pressed(id):  
if id == MENU\_MAX + 1:  
insert\_text\_at\_caret(Time.get\_date\_string\_from\_system())

csharp

public override void \_Ready() { var menu = GetMenu(); // Remove all
items after "Redo". menu.ItemCount =
menu.GetItemIndex(TextEdit.MenuItems.Redo) + 1; // Add custom items.
menu.AddSeparator(); menu.AddItem("Insert Date",
TextEdit.MenuItems.Max + 1); // Add event handler. menu.IdPressed +=
OnItemPressed; }

public void OnItemPressed(int id) { if (id ==
TextEdit.MenuItems.Max + 1) {
InsertTextAtCaret(Time.GetDateStringFromSystem()); } }

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to hide it or any of its children, use
their `Window.visible<class_Window_property_visible>` property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_minimap\_line\_at\_pos**(position:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_minimap_line_at_pos>`

Returns the equivalent minimap line at `position`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_minimap\_visible\_lines**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_minimap_visible_lines>`

Returns the number of lines that may be drawn on the minimap.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>`
**get\_next\_visible\_line\_index\_offset\_from**(line:
`int<class_int>`, wrap\_index: `int<class_int>`, visible\_amount:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_next_visible_line_index_offset_from>`

Similar to
`get_next_visible_line_offset_from<class_TextEdit_method_get_next_visible_line_offset_from>`,
but takes into account the line wrap indexes. In the returned vector,
`x` is the line, `y` is the wrap index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_next\_visible\_line\_offset\_from**(line:
`int<class_int>`, visible\_amount: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_next_visible_line_offset_from>`

Returns the count to the next visible line from `line` to
`line + visible_amount`. Can also count backwards. For example if a
**TextEdit** has 5 lines with lines 2 and 3 hidden, calling this with
`line = 1, visible_amount = 1` would return 3.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_pos\_at\_line\_column**(line:
`int<class_int>`, column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_pos_at_line_column>`

Returns the local position for the given `line` and `column`. If `x` or
`y` of the returned vector equal `-1`, the position is outside of the
viewable area of the control.

\*\*Note:\*\* The Y position corresponds to the bottom side of the line.
Use
`get_rect_at_line_column<class_TextEdit_method_get_rect_at_line_column>`
to get the top side position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2i<class_Rect2i>` **get\_rect\_at\_line\_column**(line:
`int<class_int>`, column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_rect_at_line_column>`

Returns the local position and size for the grapheme at the given `line`
and `column`. If `x` or `y` position of the returned rect equal `-1`,
the position is outside of the viewable area of the control.

\*\*Note:\*\* The Y position of the returned rect corresponds to the top
side of the line, unlike
`get_pos_at_line_column<class_TextEdit_method_get_pos_at_line_column>`
which returns the bottom side.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_saved\_version**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_saved_version>`

Returns the last tagged saved version from
`tag_saved_version<class_TextEdit_method_tag_saved_version>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_scroll\_pos\_for\_line**(line:
`int<class_int>`, wrap\_index: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_scroll_pos_for_line>`

Returns the scroll position for `wrap_index` of `line`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_selected\_text**(caret\_index:
`int<class_int>` = -1) `🔗<class_TextEdit_method_get_selected_text>`

Returns the text inside the selection of a caret, or all the carets if
`caret_index` is its default value `-1`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selection\_at\_line\_column**(line:
`int<class_int>`, column: `int<class_int>`, include\_edges:
`bool<class_bool>` = true, only\_selections: `bool<class_bool>` = true)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_selection_at_line_column>`

Returns the caret index of the selection at the given `line` and
`column`, or `-1` if there is none.

If `include_edges` is `false`, the position must be inside the selection
and not at either end. If `only_selections` is `false`, carets without a
selection will also be considered.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selection\_column**(caret\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_selection_column>`

**Deprecated:** Use
`get_selection_origin_column<class_TextEdit_method_get_selection_origin_column>`
instead.

Returns the original start column of the selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selection\_from\_column**(caret\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_selection_from_column>`

Returns the selection begin column. Returns the caret column if there is
no selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selection\_from\_line**(caret\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_selection_from_line>`

Returns the selection begin line. Returns the caret line if there is no
selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selection\_line**(caret\_index: `int<class_int>`
= 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_selection_line>`

**Deprecated:** Use
`get_selection_origin_line<class_TextEdit_method_get_selection_origin_line>`
instead.

Returns the original start line of the selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`SelectionMode<enum_TextEdit_SelectionMode>` **get\_selection\_mode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_selection_mode>`

Returns the current selection mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selection\_origin\_column**(caret\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_selection_origin_column>`

Returns the origin column of the selection. This is the opposite end
from the caret.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selection\_origin\_line**(caret\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_selection_origin_line>`

Returns the origin line of the selection. This is the opposite end from
the caret.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selection\_to\_column**(caret\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_selection_to_column>`

Returns the selection end column. Returns the caret column if there is
no selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selection\_to\_line**(caret\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_selection_to_line>`

Returns the selection end line. Returns the caret line if there is no
selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**get\_sorted\_carets**(include\_ignored\_carets: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_sorted_carets>`

Returns the carets sorted by selection beginning from lowest line and
column to highest (from top to bottom of text).

If `include_ignored_carets` is `false`, carets from
`multicaret_edit_ignore_caret<class_TextEdit_method_multicaret_edit_ignore_caret>`
will be ignored.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_tab\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_tab_size>`

Returns the **TextEdit**'s' tab size.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_total\_gutter\_width**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_total_gutter_width>`

Returns the total width of all gutters and internal padding.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_total\_visible\_line\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_total_visible_line_count>`

Returns the number of lines that may be drawn.

classref-item-separator

------------------------------------------------------------------------

classref-method

`VScrollBar<class_VScrollBar>` **get\_v\_scroll\_bar**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_v_scroll_bar>`

Returns the `VScrollBar<class_VScrollBar>` of the **TextEdit**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_version**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_version>`

Returns the current version of the **TextEdit**. The version is a count
of recorded operations by the undo/redo history.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_visible\_line\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_visible_line_count>`

Returns the number of visible lines, including wrapped text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_visible\_line\_count\_in\_range**(from\_line:
`int<class_int>`, to\_line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_visible_line_count_in_range>`

Returns the total number of visible + wrapped lines between the two
lines.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_word\_at\_pos**(position:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_word_at_pos>`

Returns the word at `position`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_word\_under\_caret**(caret\_index:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_get_word_under_caret>`

Returns a `String<class_String>` text with the word under the caret's
location.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_ime\_text**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_has_ime_text>`

Returns `true` if the user has text in the [Input Method
Editor](https://en.wikipedia.org/wiki/Input_method) (IME).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_redo**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_has_redo>`

Returns `true` if a "redo" action is available.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_selection**(caret\_index: `int<class_int>` =
-1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_has_selection>`

Returns `true` if the user has selected text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_undo**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_has_undo>`

Returns `true` if an "undo" action is available.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **insert\_line\_at**(line: `int<class_int>`,
text: `String<class_String>`) `🔗<class_TextEdit_method_insert_line_at>`

Inserts a new line with `text` at `line`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **insert\_text**(text: `String<class_String>`,
line: `int<class_int>`, column: `int<class_int>`,
before\_selection\_begin: `bool<class_bool>` = true,
before\_selection\_end: `bool<class_bool>` = false)
`🔗<class_TextEdit_method_insert_text>`

Inserts the `text` at `line` and `column`.

If `before_selection_begin` is `true`, carets and selections that begin
at `line` and `column` will moved to the end of the inserted text, along
with all carets after it.

If `before_selection_end` is `true`, selections that end at `line` and
`column` will be extended to the end of the inserted text. These
parameters can be used to insert text inside of or outside of
selections.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **insert\_text\_at\_caret**(text:
`String<class_String>`, caret\_index: `int<class_int>` = -1)
`🔗<class_TextEdit_method_insert_text_at_caret>`

Insert the specified text at the caret position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_caret\_after\_selection\_origin**(caret\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_caret_after_selection_origin>`

Returns `true` if the caret of the selection is after the selection
origin. This can be used to determine the direction of the selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_caret\_visible**(caret\_index: `int<class_int>`
= 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_caret_visible>`

Returns `true` if the caret is visible on the screen.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_dragging\_cursor**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_dragging_cursor>`

Returns `true` if the user is dragging their mouse for scrolling,
selecting, or text dragging.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_gutter\_clickable**(gutter: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_gutter_clickable>`

Returns whether the gutter is clickable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_gutter\_drawn**(gutter: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_gutter_drawn>`

Returns whether the gutter is currently drawn.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_gutter\_overwritable**(gutter:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_gutter_overwritable>`

Returns whether the gutter is overwritable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_in\_mulitcaret\_edit**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_in_mulitcaret_edit>`

Returns `true` if a
`begin_multicaret_edit<class_TextEdit_method_begin_multicaret_edit>` has
been called and
`end_multicaret_edit<class_TextEdit_method_end_multicaret_edit>` has not
yet been called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_line\_gutter\_clickable**(line:
`int<class_int>`, gutter: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_line_gutter_clickable>`

Returns whether the gutter on the given line is clickable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_line\_wrapped**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_line_wrapped>`

Returns if the given line is wrapped.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_menu\_visible**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_menu_visible>`

Returns whether the menu is visible. Use this instead of
`get_menu().visible` to improve performance (so the creation of the menu
is avoided).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_mouse\_over\_selection**(edges:
`bool<class_bool>`, caret\_index: `int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_mouse_over_selection>`

Returns whether the mouse is over selection. If `edges` is `true`, the
edges are considered part of the selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_overtype\_mode\_enabled**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_is_overtype_mode_enabled>`

Returns whether the user is in overtype mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **menu\_option**(option: `int<class_int>`)
`🔗<class_TextEdit_method_menu_option>`

Executes a given action as defined in the
`MenuItems<enum_TextEdit_MenuItems>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **merge\_gutters**(from\_line:
`int<class_int>`, to\_line: `int<class_int>`)
`🔗<class_TextEdit_method_merge_gutters>`

Merge the gutters from `from_line` into `to_line`. Only overwritable
gutters will be copied.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **merge\_overlapping\_carets**()
`🔗<class_TextEdit_method_merge_overlapping_carets>`

Merges any overlapping carets. Will favor the newest caret, or the caret
with a selection.

If `is_in_mulitcaret_edit<class_TextEdit_method_is_in_mulitcaret_edit>`
is `true`, the merge will be queued to happen at the end of the
multicaret edit. See
`begin_multicaret_edit<class_TextEdit_method_begin_multicaret_edit>` and
`end_multicaret_edit<class_TextEdit_method_end_multicaret_edit>`.

\*\*Note:\*\* This is not called when a caret changes position but after
certain actions, so it is possible to get into a state where carets
overlap.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **multicaret\_edit\_ignore\_caret**(caret\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_multicaret_edit_ignore_caret>`

Returns `true` if the given `caret_index` should be ignored as part of a
multicaret edit. See
`begin_multicaret_edit<class_TextEdit_method_begin_multicaret_edit>` and
`end_multicaret_edit<class_TextEdit_method_end_multicaret_edit>`. Carets
that should be ignored are ones that were part of removed text and will
likely be merged at the end of the edit, or carets that were added
during the edit.

It is recommended to `continue` within a loop iterating on multiple
carets if a caret should be ignored.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **paste**(caret\_index: `int<class_int>` = -1)
`🔗<class_TextEdit_method_paste>`

Paste at the current location. Can be overridden with
`_paste<class_TextEdit_private_method__paste>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **paste\_primary\_clipboard**(caret\_index:
`int<class_int>` = -1)
`🔗<class_TextEdit_method_paste_primary_clipboard>`

Pastes the primary clipboard.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **redo**() `🔗<class_TextEdit_method_redo>`

Perform redo operation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_caret**(caret: `int<class_int>`)
`🔗<class_TextEdit_method_remove_caret>`

Removes the given caret index.

\*\*Note:\*\* This can result in adjustment of all other caret indices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_gutter**(gutter: `int<class_int>`)
`🔗<class_TextEdit_method_remove_gutter>`

Removes the gutter from this **TextEdit**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_line\_at**(line: `int<class_int>`,
move\_carets\_down: `bool<class_bool>` = true)
`🔗<class_TextEdit_method_remove_line_at>`

Removes the line of text at `line`. Carets on this line will attempt to
match their previous visual x position.

If `move_carets_down` is `true` carets will move to the next line down,
otherwise carets will move up.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_secondary\_carets**()
`🔗<class_TextEdit_method_remove_secondary_carets>`

Removes all additional carets.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_text**(from\_line: `int<class_int>`,
from\_column: `int<class_int>`, to\_line: `int<class_int>`, to\_column:
`int<class_int>`) `🔗<class_TextEdit_method_remove_text>`

Removes text between the given positions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **search**(text: `String<class_String>`,
flags: `int<class_int>`, from\_line: `int<class_int>`, from\_column:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextEdit_method_search>`

Perform a search inside the text. Search flags can be specified in the
`SearchFlags<enum_TextEdit_SearchFlags>` enum.

In the returned vector, `x` is the column, `y` is the line. If no
results are found, both are equal to `-1`.

gdscript

var result = search("print", SEARCH\_WHOLE\_WORDS, 0, 0) if result.x !=
-1: \# Result found. var line\_number = result.y var column\_number =
result.x

csharp

Vector2I result = Search("print", (uint)TextEdit.SearchFlags.WholeWords,
0, 0); if (result.X != -1) { // Result found. int lineNumber = result.Y;
int columnNumber = result.X; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **select**(origin\_line: `int<class_int>`,
origin\_column: `int<class_int>`, caret\_line: `int<class_int>`,
caret\_column: `int<class_int>`, caret\_index: `int<class_int>` = 0)
`🔗<class_TextEdit_method_select>`

Selects text from `origin_line` and `origin_column` to `caret_line` and
`caret_column` for the given `caret_index`. This moves the selection
origin and the caret. If the positions are the same, the selection will
be deselected.

If `selecting_enabled<class_TextEdit_property_selecting_enabled>` is
`false`, no selection will occur.

\*\*Note:\*\* If supporting multiple carets this will not check for any
overlap. See
`merge_overlapping_carets<class_TextEdit_method_merge_overlapping_carets>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **select\_all**()
`🔗<class_TextEdit_method_select_all>`

Select all the text.

If `selecting_enabled<class_TextEdit_property_selecting_enabled>` is
`false`, no selection will occur.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **select\_word\_under\_caret**(caret\_index:
`int<class_int>` = -1)
`🔗<class_TextEdit_method_select_word_under_caret>`

Selects the word under the caret.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_caret\_column**(column:
`int<class_int>`, adjust\_viewport: `bool<class_bool>` = true,
caret\_index: `int<class_int>` = 0)
`🔗<class_TextEdit_method_set_caret_column>`

Moves the caret to the specified `column` index.

If `adjust_viewport` is `true`, the viewport will center at the caret
position after the move occurs.

\*\*Note:\*\* If supporting multiple carets this will not check for any
overlap. See
`merge_overlapping_carets<class_TextEdit_method_merge_overlapping_carets>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_caret\_line**(line: `int<class_int>`,
adjust\_viewport: `bool<class_bool>` = true, can\_be\_hidden:
`bool<class_bool>` = true, wrap\_index: `int<class_int>` = 0,
caret\_index: `int<class_int>` = 0)
`🔗<class_TextEdit_method_set_caret_line>`

Moves the caret to the specified `line` index. The caret column will be
moved to the same visual position it was at the last time
`set_caret_column<class_TextEdit_method_set_caret_column>` was called,
or clamped to the end of the line.

If `adjust_viewport` is `true`, the viewport will center at the caret
position after the move occurs.

If `can_be_hidden` is `true`, the specified `line` can be hidden.

If `wrap_index` is `-1`, the caret column will be clamped to the
`line`'s length. If `wrap_index` is greater than `-1`, the column will
be moved to attempt to match the visual x position on the line's
`wrap_index` to the position from the last time
`set_caret_column<class_TextEdit_method_set_caret_column>` was called.

\*\*Note:\*\* If supporting multiple carets this will not check for any
overlap. See
`merge_overlapping_carets<class_TextEdit_method_merge_overlapping_carets>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_gutter\_clickable**(gutter:
`int<class_int>`, clickable: `bool<class_bool>`)
`🔗<class_TextEdit_method_set_gutter_clickable>`

Sets the gutter as clickable. This will change the mouse cursor to a
pointing hand when hovering over the gutter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_gutter\_custom\_draw**(column:
`int<class_int>`, draw\_callback: `Callable<class_Callable>`)
`🔗<class_TextEdit_method_set_gutter_custom_draw>`

Set a custom draw method for the gutter. The callback method must take
the following args: `line: int, gutter: int, Area: Rect2`. This only
works when the gutter type is
`GUTTER_TYPE_CUSTOM<class_TextEdit_constant_GUTTER_TYPE_CUSTOM>` (see
`set_gutter_type<class_TextEdit_method_set_gutter_type>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_gutter\_draw**(gutter:
`int<class_int>`, draw: `bool<class_bool>`)
`🔗<class_TextEdit_method_set_gutter_draw>`

Sets whether the gutter should be drawn.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_gutter\_name**(gutter:
`int<class_int>`, name: `String<class_String>`)
`🔗<class_TextEdit_method_set_gutter_name>`

Sets the name of the gutter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_gutter\_overwritable**(gutter:
`int<class_int>`, overwritable: `bool<class_bool>`)
`🔗<class_TextEdit_method_set_gutter_overwritable>`

Sets the gutter to overwritable. See
`merge_gutters<class_TextEdit_method_merge_gutters>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_gutter\_type**(gutter:
`int<class_int>`, type: `GutterType<enum_TextEdit_GutterType>`)
`🔗<class_TextEdit_method_set_gutter_type>`

Sets the type of gutter. Gutters can contain icons, text, or custom
visuals. See `GutterType<enum_TextEdit_GutterType>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_gutter\_width**(gutter:
`int<class_int>`, width: `int<class_int>`)
`🔗<class_TextEdit_method_set_gutter_width>`

Set the width of the gutter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line**(line: `int<class_int>`,
new\_text: `String<class_String>`) `🔗<class_TextEdit_method_set_line>`

Sets the text for a specific `line`.

Carets on the line will attempt to keep their visual x position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_as\_center\_visible**(line:
`int<class_int>`, wrap\_index: `int<class_int>` = 0)
`🔗<class_TextEdit_method_set_line_as_center_visible>`

Positions the `wrap_index` of `line` at the center of the viewport.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_as\_first\_visible**(line:
`int<class_int>`, wrap\_index: `int<class_int>` = 0)
`🔗<class_TextEdit_method_set_line_as_first_visible>`

Positions the `wrap_index` of `line` at the top of the viewport.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_as\_last\_visible**(line:
`int<class_int>`, wrap\_index: `int<class_int>` = 0)
`🔗<class_TextEdit_method_set_line_as_last_visible>`

Positions the `wrap_index` of `line` at the bottom of the viewport.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_background\_color**(line:
`int<class_int>`, color: `Color<class_Color>`)
`🔗<class_TextEdit_method_set_line_background_color>`

Sets the current background color of the line. Set to
`Color(0, 0, 0, 0)` for no color.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_gutter\_clickable**(line:
`int<class_int>`, gutter: `int<class_int>`, clickable:
`bool<class_bool>`)
`🔗<class_TextEdit_method_set_line_gutter_clickable>`

If `clickable` is `true`, makes the `gutter` on `line` clickable. See
`gutter_clicked<class_TextEdit_signal_gutter_clicked>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_gutter\_icon**(line:
`int<class_int>`, gutter: `int<class_int>`, icon:
`Texture2D<class_Texture2D>`)
`🔗<class_TextEdit_method_set_line_gutter_icon>`

Sets the icon for `gutter` on `line` to `icon`. This only works when the
gutter type is
`GUTTER_TYPE_ICON<class_TextEdit_constant_GUTTER_TYPE_ICON>` (see
`set_gutter_type<class_TextEdit_method_set_gutter_type>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_gutter\_item\_color**(line:
`int<class_int>`, gutter: `int<class_int>`, color: `Color<class_Color>`)
`🔗<class_TextEdit_method_set_line_gutter_item_color>`

Sets the color for `gutter` on `line` to `color`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_gutter\_metadata**(line:
`int<class_int>`, gutter: `int<class_int>`, metadata:
`Variant<class_Variant>`)
`🔗<class_TextEdit_method_set_line_gutter_metadata>`

Sets the metadata for `gutter` on `line` to `metadata`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_gutter\_text**(line:
`int<class_int>`, gutter: `int<class_int>`, text:
`String<class_String>`) `🔗<class_TextEdit_method_set_line_gutter_text>`

Sets the text for `gutter` on `line` to `text`. This only works when the
gutter type is
`GUTTER_TYPE_STRING<class_TextEdit_constant_GUTTER_TYPE_STRING>` (see
`set_gutter_type<class_TextEdit_method_set_gutter_type>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_overtype\_mode\_enabled**(enabled:
`bool<class_bool>`)
`🔗<class_TextEdit_method_set_overtype_mode_enabled>`

If `true`, sets the user into overtype mode. When the user types in this
mode, it will override existing text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_search\_flags**(flags:
`int<class_int>`) `🔗<class_TextEdit_method_set_search_flags>`

Sets the search `flags`. This is used with
`set_search_text<class_TextEdit_method_set_search_text>` to highlight
occurrences of the searched text. Search flags can be specified from the
`SearchFlags<enum_TextEdit_SearchFlags>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_search\_text**(search\_text:
`String<class_String>`) `🔗<class_TextEdit_method_set_search_text>`

Sets the search text. See
`set_search_flags<class_TextEdit_method_set_search_flags>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_selection\_mode**(mode:
`SelectionMode<enum_TextEdit_SelectionMode>`)
`🔗<class_TextEdit_method_set_selection_mode>`

Sets the current selection mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_selection\_origin\_column**(column:
`int<class_int>`, caret\_index: `int<class_int>` = 0)
`🔗<class_TextEdit_method_set_selection_origin_column>`

Sets the selection origin column to the `column` for the given
`caret_index`. If the selection origin is moved to the caret position,
the selection will deselect.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_selection\_origin\_line**(line:
`int<class_int>`, can\_be\_hidden: `bool<class_bool>` = true,
wrap\_index: `int<class_int>` = -1, caret\_index: `int<class_int>` = 0)
`🔗<class_TextEdit_method_set_selection_origin_line>`

Sets the selection origin line to the `line` for the given
`caret_index`. If the selection origin is moved to the caret position,
the selection will deselect.

If `can_be_hidden` is `false`, The line will be set to the nearest
unhidden line below or above.

If `wrap_index` is `-1`, the selection origin column will be clamped to
the `line`'s length. If `wrap_index` is greater than `-1`, the column
will be moved to attempt to match the visual x position on the line's
`wrap_index` to the position from the last time
`set_selection_origin_column<class_TextEdit_method_set_selection_origin_column>`
or `select<class_TextEdit_method_select>` was called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tab\_size**(size: `int<class_int>`)
`🔗<class_TextEdit_method_set_tab_size>`

Sets the tab size for the **TextEdit** to use.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tooltip\_request\_func**(callback:
`Callable<class_Callable>`)
`🔗<class_TextEdit_method_set_tooltip_request_func>`

Provide custom tooltip text. The callback method must take the following
args: `hovered_word: String`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **skip\_selection\_for\_next\_occurrence**()
`🔗<class_TextEdit_method_skip_selection_for_next_occurrence>`

Moves a selection and a caret for the next occurrence of the current
selection. If there is no active selection, moves to the next occurrence
of the word under caret.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **start\_action**(action:
`EditAction<enum_TextEdit_EditAction>`)
`🔗<class_TextEdit_method_start_action>`

Starts an action, will end the current action if `action` is different.

An action will also end after a call to
`end_action<class_TextEdit_method_end_action>`, after
`ProjectSettings.gui/timers/text_edit_idle_detect_sec<class_ProjectSettings_property_gui/timers/text_edit_idle_detect_sec>`
is triggered or a new undoable step outside the
`start_action<class_TextEdit_method_start_action>` and
`end_action<class_TextEdit_method_end_action>` calls.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **swap\_lines**(from\_line: `int<class_int>`,
to\_line: `int<class_int>`) `🔗<class_TextEdit_method_swap_lines>`

Swaps the two lines. Carets will be swapped with the lines.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **tag\_saved\_version**()
`🔗<class_TextEdit_method_tag_saved_version>`

Tag the current version as saved.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **undo**() `🔗<class_TextEdit_method_undo>`

Perform undo operation.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **background\_color** = `Color(0, 0, 0, 0)`
`🔗<class_TextEdit_theme_color_background_color>`

Sets the background `Color<class_Color>` of this **TextEdit**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **caret\_background\_color** = `Color(0, 0, 0, 1)`
`🔗<class_TextEdit_theme_color_caret_background_color>`

`Color<class_Color>` of the text behind the caret when using a block
caret.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **caret\_color** = `Color(0.875, 0.875, 0.875, 1)`
`🔗<class_TextEdit_theme_color_caret_color>`

`Color<class_Color>` of the caret. This can be set to a fully
transparent color to hide the caret entirely.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **current\_line\_color** =
`Color(0.25, 0.25, 0.26, 0.8)`
`🔗<class_TextEdit_theme_color_current_line_color>`

Background `Color<class_Color>` of the line containing the caret.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_color** = `Color(0.875, 0.875, 0.875, 1)`
`🔗<class_TextEdit_theme_color_font_color>`

Sets the font `Color<class_Color>`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_outline\_color** = `Color(0, 0, 0, 1)`
`🔗<class_TextEdit_theme_color_font_outline_color>`

The tint of text outline of the **TextEdit**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_placeholder\_color** =
`Color(0.875, 0.875, 0.875, 0.6)`
`🔗<class_TextEdit_theme_color_font_placeholder_color>`

Font color for
`placeholder_text<class_TextEdit_property_placeholder_text>`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_readonly\_color** =
`Color(0.875, 0.875, 0.875, 0.5)`
`🔗<class_TextEdit_theme_color_font_readonly_color>`

Sets the font `Color<class_Color>` when
`editable<class_TextEdit_property_editable>` is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_selected\_color** = `Color(0, 0, 0, 0)`
`🔗<class_TextEdit_theme_color_font_selected_color>`

Sets the `Color<class_Color>` of the selected text. If equal to
`Color(0, 0, 0, 0)`, it will be ignored.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **search\_result\_border\_color** =
`Color(0.3, 0.3, 0.3, 0.4)`
`🔗<class_TextEdit_theme_color_search_result_border_color>`

`Color<class_Color>` of the border around text that matches the search
query.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **search\_result\_color** =
`Color(0.3, 0.3, 0.3, 1)`
`🔗<class_TextEdit_theme_color_search_result_color>`

`Color<class_Color>` behind the text that matches the search query.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **selection\_color** = `Color(0.5, 0.5, 0.5, 1)`
`🔗<class_TextEdit_theme_color_selection_color>`

Sets the highlight `Color<class_Color>` of text selections.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **word\_highlighted\_color** =
`Color(0.5, 0.5, 0.5, 0.25)`
`🔗<class_TextEdit_theme_color_word_highlighted_color>`

Sets the highlight `Color<class_Color>` of multiple occurrences.
`highlight_all_occurrences<class_TextEdit_property_highlight_all_occurrences>`
has to be enabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **caret\_width** = `1`
`🔗<class_TextEdit_theme_constant_caret_width>`

The caret's width in pixels. Greater values can be used to improve
accessibility by ensuring the caret is easily visible, or to ensure
consistency with a large font size. If set to `0` or lower, the caret
width is automatically set to 1 pixel and multiplied by the display
scaling factor.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **line\_spacing** = `4`
`🔗<class_TextEdit_theme_constant_line_spacing>`

Sets the spacing between the lines.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **outline\_size** = `0`
`🔗<class_TextEdit_theme_constant_outline_size>`

The size of the text outline.

\*\*Note:\*\* If using a font with
`FontFile.multichannel_signed_distance_field<class_FontFile_property_multichannel_signed_distance_field>`
enabled, its
`FontFile.msdf_pixel_range<class_FontFile_property_msdf_pixel_range>`
must be set to at least *twice* the value of
`outline_size<class_TextEdit_theme_constant_outline_size>` for outline
rendering to look correct. Otherwise, the outline may appear to be cut
off earlier than intended.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **font** `🔗<class_TextEdit_theme_font_font>`

Sets the default `Font<class_Font>`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **font\_size**
`🔗<class_TextEdit_theme_font_size_font_size>`

Sets default font size.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **space**
`🔗<class_TextEdit_theme_icon_space>`

Sets a custom `Texture2D<class_Texture2D>` for space text characters.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **tab** `🔗<class_TextEdit_theme_icon_tab>`

Sets a custom `Texture2D<class_Texture2D>` for tab text characters.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **focus**
`🔗<class_TextEdit_theme_style_focus>`

Sets the `StyleBox<class_StyleBox>` when in focus. The
`focus<class_TextEdit_theme_style_focus>` `StyleBox<class_StyleBox>` is
displayed *over* the base `StyleBox<class_StyleBox>`, so a partially
transparent `StyleBox<class_StyleBox>` should be used to ensure the base
`StyleBox<class_StyleBox>` remains visible. A `StyleBox<class_StyleBox>`
that represents an outline or an underline works well for this purpose.
To disable the focus visual effect, assign a
`StyleBoxEmpty<class_StyleBoxEmpty>` resource. Note that disabling the
focus visual effect will harm keyboard/controller navigation usability,
so this is not recommended for accessibility reasons.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **normal**
`🔗<class_TextEdit_theme_style_normal>`

Sets the `StyleBox<class_StyleBox>` of this **TextEdit**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **read\_only**
`🔗<class_TextEdit_theme_style_read_only>`

Sets the `StyleBox<class_StyleBox>` of this **TextEdit** when
`editable<class_TextEdit_property_editable>` is disabled.
