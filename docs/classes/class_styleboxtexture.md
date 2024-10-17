github\_url  
hide

# StyleBoxTexture

**Inherits:** `StyleBox<class_StyleBox>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A texture-based nine-patch `StyleBox<class_StyleBox>`.

classref-introduction-group

## Description

A texture-based nine-patch `StyleBox<class_StyleBox>`, in a way similar
to `NinePatchRect<class_NinePatchRect>`. This stylebox performs a 3×3
scaling of a texture, where only the center cell is fully stretched.
This makes it possible to design bordered styles regardless of the
stylebox's size.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **AxisStretchMode**: `🔗<enum_StyleBoxTexture_AxisStretchMode>`

classref-enumeration-constant

`AxisStretchMode<enum_StyleBoxTexture_AxisStretchMode>`
**AXIS\_STRETCH\_MODE\_STRETCH** = `0`

Stretch the stylebox's texture. This results in visible distortion
unless the texture size matches the stylebox's size perfectly.

classref-enumeration-constant

`AxisStretchMode<enum_StyleBoxTexture_AxisStretchMode>`
**AXIS\_STRETCH\_MODE\_TILE** = `1`

Repeats the stylebox's texture to match the stylebox's size according to
the nine-patch system.

classref-enumeration-constant

`AxisStretchMode<enum_StyleBoxTexture_AxisStretchMode>`
**AXIS\_STRETCH\_MODE\_TILE\_FIT** = `2`

Repeats the stylebox's texture to match the stylebox's size according to
the nine-patch system. Unlike
`AXIS_STRETCH_MODE_TILE<class_StyleBoxTexture_constant_AXIS_STRETCH_MODE_TILE>`,
the texture may be slightly stretched to make the nine-patch texture
tile seamlessly.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`AxisStretchMode<enum_StyleBoxTexture_AxisStretchMode>`
**axis\_stretch\_horizontal** = `0`
`🔗<class_StyleBoxTexture_property_axis_stretch_horizontal>`

classref-property-setget

-   `void (No return value.)` **set\_h\_axis\_stretch\_mode**(value:
    `AxisStretchMode<enum_StyleBoxTexture_AxisStretchMode>`)
-   `AxisStretchMode<enum_StyleBoxTexture_AxisStretchMode>`
    **get\_h\_axis\_stretch\_mode**()

Controls how the stylebox's texture will be stretched or tiled
horizontally. See
`AxisStretchMode<enum_StyleBoxTexture_AxisStretchMode>` for possible
values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AxisStretchMode<enum_StyleBoxTexture_AxisStretchMode>`
**axis\_stretch\_vertical** = `0`
`🔗<class_StyleBoxTexture_property_axis_stretch_vertical>`

classref-property-setget

-   `void (No return value.)` **set\_v\_axis\_stretch\_mode**(value:
    `AxisStretchMode<enum_StyleBoxTexture_AxisStretchMode>`)
-   `AxisStretchMode<enum_StyleBoxTexture_AxisStretchMode>`
    **get\_v\_axis\_stretch\_mode**()

Controls how the stylebox's texture will be stretched or tiled
vertically. See `AxisStretchMode<enum_StyleBoxTexture_AxisStretchMode>`
for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **draw\_center** = `true`
`🔗<class_StyleBoxTexture_property_draw_center>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_center**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_draw\_center\_enabled**()

If `true`, the nine-patch texture's center tile will be drawn.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **expand\_margin\_bottom** = `0.0`
`🔗<class_StyleBoxTexture_property_expand_margin_bottom>`

classref-property-setget

-   `void (No return value.)` **set\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Expands the bottom margin of this style box when drawing, causing it to
be drawn larger than requested.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **expand\_margin\_left** = `0.0`
`🔗<class_StyleBoxTexture_property_expand_margin_left>`

classref-property-setget

-   `void (No return value.)` **set\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Expands the left margin of this style box when drawing, causing it to be
drawn larger than requested.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **expand\_margin\_right** = `0.0`
`🔗<class_StyleBoxTexture_property_expand_margin_right>`

classref-property-setget

-   `void (No return value.)` **set\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Expands the right margin of this style box when drawing, causing it to
be drawn larger than requested.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **expand\_margin\_top** = `0.0`
`🔗<class_StyleBoxTexture_property_expand_margin_top>`

classref-property-setget

-   `void (No return value.)` **set\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_expand\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Expands the top margin of this style box when drawing, causing it to be
drawn larger than requested.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **modulate\_color** = `Color(1, 1, 1, 1)`
`🔗<class_StyleBoxTexture_property_modulate_color>`

classref-property-setget

-   `void (No return value.)` **set\_modulate**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_modulate**()

Modulates the color of the texture when this style box is drawn.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Rect2<class_Rect2>` **region\_rect** = `Rect2(0, 0, 0, 0)`
`🔗<class_StyleBoxTexture_property_region_rect>`

classref-property-setget

-   `void (No return value.)` **set\_region\_rect**(value:
    `Rect2<class_Rect2>`)
-   `Rect2<class_Rect2>` **get\_region\_rect**()

Species a sub-region of the texture to use.

This is equivalent to first wrapping the texture in an
`AtlasTexture<class_AtlasTexture>` with the same region.

If empty (`Rect2(0, 0, 0, 0)`), the whole texture will be used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture**
`🔗<class_StyleBoxTexture_property_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**()

The texture to use when drawing this style box.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **texture\_margin\_bottom** = `0.0`
`🔗<class_StyleBoxTexture_property_texture_margin_bottom>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_texture\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Increases the bottom margin of the 3×3 texture box.

A higher value means more of the source texture is considered to be part
of the bottom border of the 3×3 box.

This is also the value used as fallback for
`StyleBox.content_margin_bottom<class_StyleBox_property_content_margin_bottom>`
if it is negative.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **texture\_margin\_left** = `0.0`
`🔗<class_StyleBoxTexture_property_texture_margin_left>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_texture\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Increases the left margin of the 3×3 texture box.

A higher value means more of the source texture is considered to be part
of the left border of the 3×3 box.

This is also the value used as fallback for
`StyleBox.content_margin_left<class_StyleBox_property_content_margin_left>`
if it is negative.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **texture\_margin\_right** = `0.0`
`🔗<class_StyleBoxTexture_property_texture_margin_right>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_texture\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Increases the right margin of the 3×3 texture box.

A higher value means more of the source texture is considered to be part
of the right border of the 3×3 box.

This is also the value used as fallback for
`StyleBox.content_margin_right<class_StyleBox_property_content_margin_right>`
if it is negative.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **texture\_margin\_top** = `0.0`
`🔗<class_StyleBoxTexture_property_texture_margin_top>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
-   `float<class_float>` **get\_texture\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Increases the top margin of the 3×3 texture box.

A higher value means more of the source texture is considered to be part
of the top border of the 3×3 box.

This is also the value used as fallback for
`StyleBox.content_margin_top<class_StyleBox_property_content_margin_top>`
if it is negative.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_expand\_margin**(margin:
`Side<enum_@GlobalScope_Side>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBoxTexture_method_get_expand_margin>`

Returns the expand margin size of the specified
`Side<enum_@GlobalScope_Side>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_texture\_margin**(margin:
`Side<enum_@GlobalScope_Side>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBoxTexture_method_get_texture_margin>`

Returns the margin size of the specified `Side<enum_@GlobalScope_Side>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_expand\_margin**(margin:
`Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
`🔗<class_StyleBoxTexture_method_set_expand_margin>`

Sets the expand margin to `size` pixels for the specified
`Side<enum_@GlobalScope_Side>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_expand\_margin\_all**(size:
`float<class_float>`)
`🔗<class_StyleBoxTexture_method_set_expand_margin_all>`

Sets the expand margin to `size` pixels for all sides.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_texture\_margin**(margin:
`Side<enum_@GlobalScope_Side>`, size: `float<class_float>`)
`🔗<class_StyleBoxTexture_method_set_texture_margin>`

Sets the margin to `size` pixels for the specified
`Side<enum_@GlobalScope_Side>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_texture\_margin\_all**(size:
`float<class_float>`)
`🔗<class_StyleBoxTexture_method_set_texture_margin_all>`

Sets the margin to `size` pixels for all sides.
