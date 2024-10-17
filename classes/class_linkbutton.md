github\_url  
hide

# LinkButton

**Inherits:** `BaseButton<class_BaseButton>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

A button that represents a link.

classref-introduction-group

## Description

A button that represents a link. This type of button is primarily used
for interactions that cause a context change (like linking to a web
page).

See also `BaseButton<class_BaseButton>` which contains common properties
and methods associated with this node.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **UnderlineMode**: `🔗<enum_LinkButton_UnderlineMode>`

classref-enumeration-constant

`UnderlineMode<enum_LinkButton_UnderlineMode>`
**UNDERLINE\_MODE\_ALWAYS** = `0`

The LinkButton will always show an underline at the bottom of its text.

classref-enumeration-constant

`UnderlineMode<enum_LinkButton_UnderlineMode>`
**UNDERLINE\_MODE\_ON\_HOVER** = `1`

The LinkButton will show an underline at the bottom of its text when the
mouse cursor is over it.

classref-enumeration-constant

`UnderlineMode<enum_LinkButton_UnderlineMode>`
**UNDERLINE\_MODE\_NEVER** = `2`

The LinkButton will never show an underline at the bottom of its text.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **language** = `""`
`🔗<class_LinkButton_property_language>`

classref-property-setget

-   `void (No return value.)` **set\_language**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_language**()

Language code used for line-breaking and text shaping algorithms, if
left empty current locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StructuredTextParser<enum_TextServer_StructuredTextParser>`
**structured\_text\_bidi\_override** = `0`
`🔗<class_LinkButton_property_structured_text_bidi_override>`

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
`[]`
`🔗<class_LinkButton_property_structured_text_bidi_override_options>`

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

`String<class_String>` **text** = `""`
`🔗<class_LinkButton_property_text>`

classref-property-setget

-   `void (No return value.)` **set\_text**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_text**()

The button's text that will be displayed inside the button's area.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextDirection<enum_Control_TextDirection>` **text\_direction** = `0`
`🔗<class_LinkButton_property_text_direction>`

classref-property-setget

-   `void (No return value.)` **set\_text\_direction**(value:
    `TextDirection<enum_Control_TextDirection>`)
-   `TextDirection<enum_Control_TextDirection>`
    **get\_text\_direction**()

Base text writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`UnderlineMode<enum_LinkButton_UnderlineMode>` **underline** = `0`
`🔗<class_LinkButton_property_underline>`

classref-property-setget

-   `void (No return value.)` **set\_underline\_mode**(value:
    `UnderlineMode<enum_LinkButton_UnderlineMode>`)
-   `UnderlineMode<enum_LinkButton_UnderlineMode>`
    **get\_underline\_mode**()

The underline mode to use for the text. See
`UnderlineMode<enum_LinkButton_UnderlineMode>` for the available modes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **uri** = `""`
`🔗<class_LinkButton_property_uri>`

classref-property-setget

-   `void (No return value.)` **set\_uri**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_uri**()

The [URI](https://en.wikipedia.org/wiki/Uniform_Resource_Identifier) for
this **LinkButton**. If set to a valid URI, pressing the button opens
the URI using the operating system's default program for the protocol
(via `OS.shell_open<class_OS_method_shell_open>`). HTTP and HTTPS URLs
open the default web browser.

gdscript

uri = "<https://godotengine.org>" \# Opens the URL in the default web
browser. uri = "C:SomeFolder" \# Opens the file explorer at the given
path. uri = "C:SomeImage.png" \# Opens the given image in the default
viewing app.

csharp

Uri = "<https://godotengine.org>"; // Opens the URL in the default web
browser. Uri = "C:SomeFolder"; // Opens the file explorer at the given
path. Uri = "C:SomeImage.png"; // Opens the given image in the default
viewing app.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **font\_color** = `Color(0.875, 0.875, 0.875, 1)`
`🔗<class_LinkButton_theme_color_font_color>`

Default text `Color<class_Color>` of the **LinkButton**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_disabled\_color** = `Color(0, 0, 0, 1)`
`🔗<class_LinkButton_theme_color_font_disabled_color>`

Text `Color<class_Color>` used when the **LinkButton** is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_focus\_color** =
`Color(0.95, 0.95, 0.95, 1)`
`🔗<class_LinkButton_theme_color_font_focus_color>`

Text `Color<class_Color>` used when the **LinkButton** is focused. Only
replaces the normal text color of the button. Disabled, hovered, and
pressed states take precedence over this color.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_hover\_color** =
`Color(0.95, 0.95, 0.95, 1)`
`🔗<class_LinkButton_theme_color_font_hover_color>`

Text `Color<class_Color>` used when the **LinkButton** is being hovered.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_hover\_pressed\_color** =
`Color(0, 0, 0, 1)`
`🔗<class_LinkButton_theme_color_font_hover_pressed_color>`

Text `Color<class_Color>` used when the **LinkButton** is being hovered
and pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_outline\_color** = `Color(0, 0, 0, 1)`
`🔗<class_LinkButton_theme_color_font_outline_color>`

The tint of text outline of the **LinkButton**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_pressed\_color** = `Color(1, 1, 1, 1)`
`🔗<class_LinkButton_theme_color_font_pressed_color>`

Text `Color<class_Color>` used when the **LinkButton** is being pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **outline\_size** = `0`
`🔗<class_LinkButton_theme_constant_outline_size>`

The size of the text outline.

\*\*Note:\*\* If using a font with
`FontFile.multichannel_signed_distance_field<class_FontFile_property_multichannel_signed_distance_field>`
enabled, its
`FontFile.msdf_pixel_range<class_FontFile_property_msdf_pixel_range>`
must be set to at least *twice* the value of
`outline_size<class_LinkButton_theme_constant_outline_size>` for outline
rendering to look correct. Otherwise, the outline may appear to be cut
off earlier than intended.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **underline\_spacing** = `2`
`🔗<class_LinkButton_theme_constant_underline_spacing>`

The vertical space between the baseline of text and the underline.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **font** `🔗<class_LinkButton_theme_font_font>`

`Font<class_Font>` of the **LinkButton**'s text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **font\_size**
`🔗<class_LinkButton_theme_font_size_font_size>`

Font size of the **LinkButton**'s text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **focus**
`🔗<class_LinkButton_theme_style_focus>`

`StyleBox<class_StyleBox>` used when the **LinkButton** is focused. The
`focus<class_LinkButton_theme_style_focus>` `StyleBox<class_StyleBox>`
is displayed *over* the base `StyleBox<class_StyleBox>`, so a partially
transparent `StyleBox<class_StyleBox>` should be used to ensure the base
`StyleBox<class_StyleBox>` remains visible. A `StyleBox<class_StyleBox>`
that represents an outline or an underline works well for this purpose.
To disable the focus visual effect, assign a
`StyleBoxEmpty<class_StyleBoxEmpty>` resource. Note that disabling the
focus visual effect will harm keyboard/controller navigation usability,
so this is not recommended for accessibility reasons.
