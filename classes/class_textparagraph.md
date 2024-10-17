github\_url  
hide

# TextParagraph

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Holds a paragraph of text.

classref-introduction-group

## Description

Abstraction over `TextServer<class_TextServer>` for handling a single
paragraph of text.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
**alignment** = `0` `🔗<class_TextParagraph_property_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_alignment**(value:
    `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`)
-   `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
    **get\_alignment**()

Paragraph horizontal alignment.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`LineBreakFlag<enum_TextServer_LineBreakFlag>`\]
**break\_flags** = `3` `🔗<class_TextParagraph_property_break_flags>`

classref-property-setget

-   `void (No return value.)` **set\_break\_flags**(value:
    `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`LineBreakFlag<enum_TextServer_LineBreakFlag>`\])
-   `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`LineBreakFlag<enum_TextServer_LineBreakFlag>`\]
    **get\_break\_flags**()

Line breaking rules. For more info see `TextServer<class_TextServer>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **custom\_punctuation** = `""`
`🔗<class_TextParagraph_property_custom_punctuation>`

classref-property-setget

-   `void (No return value.)` **set\_custom\_punctuation**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_custom\_punctuation**()

Custom punctuation character list, used for word breaking. If set to
empty string, server defaults are used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Direction<enum_TextServer_Direction>` **direction** = `0`
`🔗<class_TextParagraph_property_direction>`

classref-property-setget

-   `void (No return value.)` **set\_direction**(value:
    `Direction<enum_TextServer_Direction>`)
-   `Direction<enum_TextServer_Direction>` **get\_direction**()

Text writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ellipsis\_char** = `"…"`
`🔗<class_TextParagraph_property_ellipsis_char>`

classref-property-setget

-   `void (No return value.)` **set\_ellipsis\_char**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_ellipsis\_char**()

Ellipsis character used for text clipping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
**justification\_flags** = `163`
`🔗<class_TextParagraph_property_justification_flags>`

classref-property-setget

-   `void (No return value.)` **set\_justification\_flags**(value:
    `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\])
-   `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
    **get\_justification\_flags**()

Line fill alignment rules. See
`JustificationFlag<enum_TextServer_JustificationFlag>` for more
information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_lines\_visible** = `-1`
`🔗<class_TextParagraph_property_max_lines_visible>`

classref-property-setget

-   `void (No return value.)` **set\_max\_lines\_visible**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_lines\_visible**()

Limits the lines of text shown.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Orientation<enum_TextServer_Orientation>` **orientation** = `0`
`🔗<class_TextParagraph_property_orientation>`

classref-property-setget

-   `void (No return value.)` **set\_orientation**(value:
    `Orientation<enum_TextServer_Orientation>`)
-   `Orientation<enum_TextServer_Orientation>` **get\_orientation**()

Text orientation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **preserve\_control** = `false`
`🔗<class_TextParagraph_property_preserve_control>`

classref-property-setget

-   `void (No return value.)` **set\_preserve\_control**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_preserve\_control**()

If set to `true` text will display control characters.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **preserve\_invalid** = `true`
`🔗<class_TextParagraph_property_preserve_invalid>`

classref-property-setget

-   `void (No return value.)` **set\_preserve\_invalid**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_preserve\_invalid**()

If set to `true` text will display invalid characters.

classref-item-separator

------------------------------------------------------------------------

classref-property

`OverrunBehavior<enum_TextServer_OverrunBehavior>`
**text\_overrun\_behavior** = `0`
`🔗<class_TextParagraph_property_text_overrun_behavior>`

classref-property-setget

-   `void (No return value.)` **set\_text\_overrun\_behavior**(value:
    `OverrunBehavior<enum_TextServer_OverrunBehavior>`)
-   `OverrunBehavior<enum_TextServer_OverrunBehavior>`
    **get\_text\_overrun\_behavior**()

Sets the clipping behavior when the text exceeds the paragraph's set
width. See `OverrunBehavior<enum_TextServer_OverrunBehavior>` for a
description of all modes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **width** = `-1.0`
`🔗<class_TextParagraph_property_width>`

classref-property-setget

-   `void (No return value.)` **set\_width**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_width**()

Paragraph width.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **add\_object**(key: `Variant<class_Variant>`, size:
`Vector2<class_Vector2>`, inline\_align:
`InlineAlignment<enum_@GlobalScope_InlineAlignment>` = 5, length:
`int<class_int>` = 1, baseline: `float<class_float>` = 0.0)
`🔗<class_TextParagraph_method_add_object>`

Adds inline object to the text buffer, `key` must be unique. In the
text, object is represented as `length` object replacement characters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **add\_string**(text: `String<class_String>`, font:
`Font<class_Font>`, font\_size: `int<class_int>`, language:
`String<class_String>` = "", meta: `Variant<class_Variant>` = null)
`🔗<class_TextParagraph_method_add_string>`

Adds text span and font to draw it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_TextParagraph_method_clear>`

Clears text paragraph (removes text and inline objects).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_dropcap**()
`🔗<class_TextParagraph_method_clear_dropcap>`

Removes dropcap.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw**(canvas: `RID<class_RID>`, pos:
`Vector2<class_Vector2>`, color: `Color<class_Color>` = Color(1, 1, 1,
1), dc\_color: `Color<class_Color>` = Color(1, 1, 1, 1))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_draw>`

Draw all lines of the text and drop cap into a canvas item at a given
position, with `color`. `pos` specifies the top left corner of the
bounding box.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_dropcap**(canvas: `RID<class_RID>`,
pos: `Vector2<class_Vector2>`, color: `Color<class_Color>` = Color(1, 1,
1, 1))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_draw_dropcap>`

Draw drop cap into a canvas item at a given position, with `color`.
`pos` specifies the top left corner of the bounding box.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_dropcap\_outline**(canvas:
`RID<class_RID>`, pos: `Vector2<class_Vector2>`, outline\_size:
`int<class_int>` = 1, color: `Color<class_Color>` = Color(1, 1, 1, 1))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_draw_dropcap_outline>`

Draw drop cap outline into a canvas item at a given position, with
`color`. `pos` specifies the top left corner of the bounding box.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_line**(canvas: `RID<class_RID>`, pos:
`Vector2<class_Vector2>`, line: `int<class_int>`, color:
`Color<class_Color>` = Color(1, 1, 1, 1))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_draw_line>`

Draw single line of text into a canvas item at a given position, with
`color`. `pos` specifies the top left corner of the bounding box.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_line\_outline**(canvas:
`RID<class_RID>`, pos: `Vector2<class_Vector2>`, line: `int<class_int>`,
outline\_size: `int<class_int>` = 1, color: `Color<class_Color>` =
Color(1, 1, 1, 1))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_draw_line_outline>`

Draw outline of the single line of text into a canvas item at a given
position, with `color`. `pos` specifies the top left corner of the
bounding box.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_outline**(canvas: `RID<class_RID>`,
pos: `Vector2<class_Vector2>`, outline\_size: `int<class_int>` = 1,
color: `Color<class_Color>` = Color(1, 1, 1, 1), dc\_color:
`Color<class_Color>` = Color(1, 1, 1, 1))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_draw_outline>`

Draw outlines of all lines of the text and drop cap into a canvas item
at a given position, with `color`. `pos` specifies the top left corner
of the bounding box.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_dropcap\_lines**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_dropcap_lines>`

Returns number of lines used by dropcap.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_dropcap\_rid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_dropcap_rid>`

Returns drop cap text buffer RID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_dropcap\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_dropcap_size>`

Returns drop cap bounding box size.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_line\_ascent**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_line_ascent>`

Returns the text line ascent (number of pixels above the baseline for
horizontal layout or to the left of baseline for vertical).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_line\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_line_count>`

Returns number of lines in the paragraph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_line\_descent**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_line_descent>`

Returns the text line descent (number of pixels below the baseline for
horizontal layout or to the right of baseline for vertical).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_line\_object\_rect**(line: `int<class_int>`,
key: `Variant<class_Variant>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_line_object_rect>`

Returns bounding rectangle of the inline object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_line\_objects**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_line_objects>`

Returns array of inline objects in the line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_line\_range**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_line_range>`

Returns character range of the line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_line\_rid**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_line_rid>`

Returns TextServer line buffer RID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_line\_size**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_line_size>`

Returns size of the bounding box of the line of text. Returned size is
rounded up.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_line\_underline\_position**(line:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_line_underline_position>`

Returns pixel offset of the underline below the baseline.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_line\_underline\_thickness**(line:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_line_underline_thickness>`

Returns thickness of the underline.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_line\_width**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_line_width>`

Returns width (for horizontal layout) or height (for vertical) of the
line of text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_non\_wrapped\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_non_wrapped_size>`

Returns the size of the bounding box of the paragraph, without line
breaks.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_rid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_rid>`

Returns TextServer full string buffer RID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_get_size>`

Returns the size of the bounding box of the paragraph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **hit\_test**(coords: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextParagraph_method_hit_test>`

Returns caret character offset at the specified coordinates. This
function always returns a valid position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **resize\_object**(key: `Variant<class_Variant>`,
size: `Vector2<class_Vector2>`, inline\_align:
`InlineAlignment<enum_@GlobalScope_InlineAlignment>` = 5, baseline:
`float<class_float>` = 0.0)
`🔗<class_TextParagraph_method_resize_object>`

Sets new size and alignment of embedded object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bidi\_override**(override:
`Array<class_Array>`) `🔗<class_TextParagraph_method_set_bidi_override>`

Overrides BiDi for the structured text.

Override ranges should cover full source text without overlaps. BiDi
algorithm will be used on each range separately.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **set\_dropcap**(text: `String<class_String>`, font:
`Font<class_Font>`, font\_size: `int<class_int>`, dropcap\_margins:
`Rect2<class_Rect2>` = Rect2(0, 0, 0, 0), language:
`String<class_String>` = "")
`🔗<class_TextParagraph_method_set_dropcap>`

Sets drop cap, overrides previously set drop cap. Drop cap (dropped
capital) is a decorative element at the beginning of a paragraph that is
larger than the rest of the text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **tab\_align**(tab\_stops:
`PackedFloat32Array<class_PackedFloat32Array>`)
`🔗<class_TextParagraph_method_tab_align>`

Aligns paragraph to the given tab-stops.
