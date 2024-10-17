github\_url  
hide

# ProgressBar

**Inherits:** `Range<class_Range>` **&lt;** `Control<class_Control>`
**&lt;** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A control used for visual representation of a percentage.

classref-introduction-group

## Description

A control used for visual representation of a percentage. Shows fill
percentage from right to left.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **FillMode**: `🔗<enum_ProgressBar_FillMode>`

classref-enumeration-constant

`FillMode<enum_ProgressBar_FillMode>` **FILL\_BEGIN\_TO\_END** = `0`

The progress bar fills from begin to end horizontally, according to the
language direction. If
`Control.is_layout_rtl<class_Control_method_is_layout_rtl>` returns
`false`, it fills from left to right, and if it returns `true`, it fills
from right to left.

classref-enumeration-constant

`FillMode<enum_ProgressBar_FillMode>` **FILL\_END\_TO\_BEGIN** = `1`

The progress bar fills from end to begin horizontally, according to the
language direction. If
`Control.is_layout_rtl<class_Control_method_is_layout_rtl>` returns
`false`, it fills from right to left, and if it returns `true`, it fills
from left to right.

classref-enumeration-constant

`FillMode<enum_ProgressBar_FillMode>` **FILL\_TOP\_TO\_BOTTOM** = `2`

The progress fills from top to bottom.

classref-enumeration-constant

`FillMode<enum_ProgressBar_FillMode>` **FILL\_BOTTOM\_TO\_TOP** = `3`

The progress fills from bottom to top.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **editor\_preview\_indeterminate**
`🔗<class_ProgressBar_property_editor_preview_indeterminate>`

classref-property-setget

-   `void (No return value.)`
    **set\_editor\_preview\_indeterminate**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_editor\_preview\_indeterminate\_enabled**()

If `false`, the
`indeterminate<class_ProgressBar_property_indeterminate>` animation will
be paused in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **fill\_mode** = `0`
`🔗<class_ProgressBar_property_fill_mode>`

classref-property-setget

-   `void (No return value.)` **set\_fill\_mode**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_fill\_mode**()

The fill direction. See `FillMode<enum_ProgressBar_FillMode>` for
possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **indeterminate** = `false`
`🔗<class_ProgressBar_property_indeterminate>`

classref-property-setget

-   `void (No return value.)` **set\_indeterminate**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_indeterminate**()

When set to `true`, the progress bar indicates that something is
happening with an animation, but does not show the fill percentage or
value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_percentage** = `true`
`🔗<class_ProgressBar_property_show_percentage>`

classref-property-setget

-   `void (No return value.)` **set\_show\_percentage**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_percentage\_shown**()

If `true`, the fill percentage is displayed on the bar.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **font\_color** = `Color(0.95, 0.95, 0.95, 1)`
`🔗<class_ProgressBar_theme_color_font_color>`

The color of the text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_outline\_color** = `Color(0, 0, 0, 1)`
`🔗<class_ProgressBar_theme_color_font_outline_color>`

The tint of text outline of the **ProgressBar**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **outline\_size** = `0`
`🔗<class_ProgressBar_theme_constant_outline_size>`

The size of the text outline.

\*\*Note:\*\* If using a font with
`FontFile.multichannel_signed_distance_field<class_FontFile_property_multichannel_signed_distance_field>`
enabled, its
`FontFile.msdf_pixel_range<class_FontFile_property_msdf_pixel_range>`
must be set to at least *twice* the value of
`outline_size<class_ProgressBar_theme_constant_outline_size>` for
outline rendering to look correct. Otherwise, the outline may appear to
be cut off earlier than intended.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **font** `🔗<class_ProgressBar_theme_font_font>`

Font used to draw the fill percentage if
`show_percentage<class_ProgressBar_property_show_percentage>` is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **font\_size**
`🔗<class_ProgressBar_theme_font_size_font_size>`

Font size used to draw the fill percentage if
`show_percentage<class_ProgressBar_property_show_percentage>` is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **background**
`🔗<class_ProgressBar_theme_style_background>`

The style of the background.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **fill**
`🔗<class_ProgressBar_theme_style_fill>`

The style of the progress (i.e. the part that fills the bar).
