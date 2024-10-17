github\_url  
hide

# Label

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A control for displaying plain text.

classref-introduction-group

## Description

A control for displaying plain text. It gives you control over the
horizontal and vertical alignment and can wrap the text inside the
node's bounding rectangle. It doesn't support bold, italics, or other
rich text formatting. For that, use `RichTextLabel<class_RichTextLabel>`
instead.

classref-introduction-group

## Tutorials

-   [2D Dodge The Creeps
    Demo](https://godotengine.org/asset-library/asset/2712)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`AutowrapMode<enum_TextServer_AutowrapMode>` **autowrap\_mode** = `0`
`🔗<class_Label_property_autowrap_mode>`

classref-property-setget

-   `void (No return value.)` **set\_autowrap\_mode**(value:
    `AutowrapMode<enum_TextServer_AutowrapMode>`)
-   `AutowrapMode<enum_TextServer_AutowrapMode>`
    **get\_autowrap\_mode**()

If set to something other than
`TextServer.AUTOWRAP_OFF<class_TextServer_constant_AUTOWRAP_OFF>`, the
text gets wrapped inside the node's bounding rectangle. If you resize
the node, it will change its height automatically to show all the text.
To see how each mode behaves, see
`AutowrapMode<enum_TextServer_AutowrapMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **clip\_text** = `false`
`🔗<class_Label_property_clip_text>`

classref-property-setget

-   `void (No return value.)` **set\_clip\_text**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_clipping\_text**()

If `true`, the Label only shows the text that fits inside its bounding
rectangle and will clip text horizontally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ellipsis\_char** = `"…"`
`🔗<class_Label_property_ellipsis_char>`

classref-property-setget

-   `void (No return value.)` **set\_ellipsis\_char**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_ellipsis\_char**()

Ellipsis character used for text clipping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
**horizontal\_alignment** = `0`
`🔗<class_Label_property_horizontal_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_horizontal\_alignment**(value:
    `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`)
-   `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
    **get\_horizontal\_alignment**()

Controls the text's horizontal alignment. Supports left, center, right,
and fill, or justify. Set it to one of the
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
**justification\_flags** = `163`
`🔗<class_Label_property_justification_flags>`

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

`LabelSettings<class_LabelSettings>` **label\_settings**
`🔗<class_Label_property_label_settings>`

classref-property-setget

-   `void (No return value.)` **set\_label\_settings**(value:
    `LabelSettings<class_LabelSettings>`)
-   `LabelSettings<class_LabelSettings>` **get\_label\_settings**()

A `LabelSettings<class_LabelSettings>` resource that can be shared
between multiple **Label** nodes. Takes priority over theme properties.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **language** = `""`
`🔗<class_Label_property_language>`

classref-property-setget

-   `void (No return value.)` **set\_language**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_language**()

Language code used for line-breaking and text shaping algorithms, if
left empty current locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **lines\_skipped** = `0`
`🔗<class_Label_property_lines_skipped>`

classref-property-setget

-   `void (No return value.)` **set\_lines\_skipped**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_lines\_skipped**()

The number of the lines ignored and not displayed from the start of the
`text<class_Label_property_text>` value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_lines\_visible** = `-1`
`🔗<class_Label_property_max_lines_visible>`

classref-property-setget

-   `void (No return value.)` **set\_max\_lines\_visible**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_lines\_visible**()

Limits the lines of text the node shows on screen.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StructuredTextParser<enum_TextServer_StructuredTextParser>`
**structured\_text\_bidi\_override** = `0`
`🔗<class_Label_property_structured_text_bidi_override>`

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
`[]` `🔗<class_Label_property_structured_text_bidi_override_options>`

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

`PackedFloat32Array<class_PackedFloat32Array>` **tab\_stops** =
`PackedFloat32Array()` `🔗<class_Label_property_tab_stops>`

classref-property-setget

-   `void (No return value.)` **set\_tab\_stops**(value:
    `PackedFloat32Array<class_PackedFloat32Array>`)
-   `PackedFloat32Array<class_PackedFloat32Array>` **get\_tab\_stops**()

Aligns text to the given tab-stops.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedFloat32Array<class_PackedFloat32Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **text** = `""` `🔗<class_Label_property_text>`

classref-property-setget

-   `void (No return value.)` **set\_text**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_text**()

The text to display on screen.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextDirection<enum_Control_TextDirection>` **text\_direction** = `0`
`🔗<class_Label_property_text_direction>`

classref-property-setget

-   `void (No return value.)` **set\_text\_direction**(value:
    `TextDirection<enum_Control_TextDirection>`)
-   `TextDirection<enum_Control_TextDirection>`
    **get\_text\_direction**()

Base text writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`OverrunBehavior<enum_TextServer_OverrunBehavior>`
**text\_overrun\_behavior** = `0`
`🔗<class_Label_property_text_overrun_behavior>`

classref-property-setget

-   `void (No return value.)` **set\_text\_overrun\_behavior**(value:
    `OverrunBehavior<enum_TextServer_OverrunBehavior>`)
-   `OverrunBehavior<enum_TextServer_OverrunBehavior>`
    **get\_text\_overrun\_behavior**()

Sets the clipping behavior when the text exceeds the node's bounding
rectangle. See `OverrunBehavior<enum_TextServer_OverrunBehavior>` for a
description of all modes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **uppercase** = `false`
`🔗<class_Label_property_uppercase>`

classref-property-setget

-   `void (No return value.)` **set\_uppercase**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_uppercase**()

If `true`, all the text displays as UPPERCASE.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VerticalAlignment<enum_@GlobalScope_VerticalAlignment>`
**vertical\_alignment** = `0`
`🔗<class_Label_property_vertical_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_vertical\_alignment**(value:
    `VerticalAlignment<enum_@GlobalScope_VerticalAlignment>`)
-   `VerticalAlignment<enum_@GlobalScope_VerticalAlignment>`
    **get\_vertical\_alignment**()

Controls the text's vertical alignment. Supports top, center, bottom,
and fill. Set it to one of the
`VerticalAlignment<enum_@GlobalScope_VerticalAlignment>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **visible\_characters** = `-1`
`🔗<class_Label_property_visible_characters>`

classref-property-setget

-   `void (No return value.)` **set\_visible\_characters**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_visible\_characters**()

The number of characters to display. If set to `-1`, all characters are
displayed. This can be useful when animating the text appearing in a
dialog box.

\*\*Note:\*\* Setting this property updates
`visible_ratio<class_Label_property_visible_ratio>` accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VisibleCharactersBehavior<enum_TextServer_VisibleCharactersBehavior>`
**visible\_characters\_behavior** = `0`
`🔗<class_Label_property_visible_characters_behavior>`

classref-property-setget

-   `void (No return value.)`
    **set\_visible\_characters\_behavior**(value:
    `VisibleCharactersBehavior<enum_TextServer_VisibleCharactersBehavior>`)
-   `VisibleCharactersBehavior<enum_TextServer_VisibleCharactersBehavior>`
    **get\_visible\_characters\_behavior**()

Sets the clipping behavior when
`visible_characters<class_Label_property_visible_characters>` or
`visible_ratio<class_Label_property_visible_ratio>` is set. See
`VisibleCharactersBehavior<enum_TextServer_VisibleCharactersBehavior>`
for more info.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **visible\_ratio** = `1.0`
`🔗<class_Label_property_visible_ratio>`

classref-property-setget

-   `void (No return value.)` **set\_visible\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_visible\_ratio**()

The fraction of characters to display, relative to the total number of
characters (see
`get_total_character_count<class_Label_method_get_total_character_count>`).
If set to `1.0`, all characters are displayed. If set to `0.5`, only
half of the characters will be displayed. This can be useful when
animating the text appearing in a dialog box.

\*\*Note:\*\* Setting this property updates
`visible_characters<class_Label_property_visible_characters>`
accordingly.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Rect2<class_Rect2>` **get\_character\_bounds**(pos: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Label_method_get_character_bounds>`

Returns the bounding rectangle of the character at position `pos` in the
label's local coordinate system. If the character is a non-visual
character or `pos` is outside the valid range, an empty
`Rect2<class_Rect2>` is returned. If the character is a part of a
composite grapheme, the bounding rectangle of the whole grapheme is
returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_line\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Label_method_get_line_count>`

Returns the number of lines of text the Label has.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_line\_height**(line: `int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Label_method_get_line_height>`

Returns the height of the line `line`.

If `line` is set to `-1`, returns the biggest line height.

If there are no lines, returns font size in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_total\_character\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Label_method_get_total_character_count>`

Returns the total number of printable characters in the text (excluding
spaces and newlines).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_visible\_line\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Label_method_get_visible_line_count>`

Returns the number of lines shown. Useful if the **Label**'s height
cannot currently display all lines.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **font\_color** = `Color(1, 1, 1, 1)`
`🔗<class_Label_theme_color_font_color>`

Default text `Color<class_Color>` of the **Label**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_outline\_color** = `Color(0, 0, 0, 1)`
`🔗<class_Label_theme_color_font_outline_color>`

The color of text outline.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_shadow\_color** = `Color(0, 0, 0, 0)`
`🔗<class_Label_theme_color_font_shadow_color>`

`Color<class_Color>` of the text's shadow effect.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **line\_spacing** = `3`
`🔗<class_Label_theme_constant_line_spacing>`

Vertical space between lines in multiline **Label**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **outline\_size** = `0`
`🔗<class_Label_theme_constant_outline_size>`

Text outline size.

\*\*Note:\*\* If using a font with
`FontFile.multichannel_signed_distance_field<class_FontFile_property_multichannel_signed_distance_field>`
enabled, its
`FontFile.msdf_pixel_range<class_FontFile_property_msdf_pixel_range>`
must be set to at least *twice* the value of
`outline_size<class_Label_theme_constant_outline_size>` for outline
rendering to look correct. Otherwise, the outline may appear to be cut
off earlier than intended.

\*\*Note:\*\* Using a value that is larger than half the font size is
not recommended, as the font outline may fail to be fully closed in this
case.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **shadow\_offset\_x** = `1`
`🔗<class_Label_theme_constant_shadow_offset_x>`

The horizontal offset of the text's shadow.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **shadow\_offset\_y** = `1`
`🔗<class_Label_theme_constant_shadow_offset_y>`

The vertical offset of the text's shadow.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **shadow\_outline\_size** = `1`
`🔗<class_Label_theme_constant_shadow_outline_size>`

The size of the shadow outline.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **font** `🔗<class_Label_theme_font_font>`

`Font<class_Font>` used for the **Label**'s text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **font\_size**
`🔗<class_Label_theme_font_size_font_size>`

Font size of the **Label**'s text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **normal**
`🔗<class_Label_theme_style_normal>`

Background `StyleBox<class_StyleBox>` for the **Label**.
