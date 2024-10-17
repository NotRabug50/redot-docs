github\_url  
hide

# NinePatchRect

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A control that displays a texture by keeping its corners intact, but
tiling its edges and center.

classref-introduction-group

## Description

Also known as 9-slice panels, **NinePatchRect** produces clean panels of
any size based on a small texture. To do so, it splits the texture in a
3×3 grid. When you scale the node, it tiles the texture's edges
horizontally or vertically, tiles the center on both axes, and leaves
the corners unchanged.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**texture\_changed**() `🔗<class_NinePatchRect_signal_texture_changed>`

Emitted when the node's texture changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **AxisStretchMode**: `🔗<enum_NinePatchRect_AxisStretchMode>`

classref-enumeration-constant

`AxisStretchMode<enum_NinePatchRect_AxisStretchMode>`
**AXIS\_STRETCH\_MODE\_STRETCH** = `0`

Stretches the center texture across the NinePatchRect. This may cause
the texture to be distorted.

classref-enumeration-constant

`AxisStretchMode<enum_NinePatchRect_AxisStretchMode>`
**AXIS\_STRETCH\_MODE\_TILE** = `1`

Repeats the center texture across the NinePatchRect. This won't cause
any visible distortion. The texture must be seamless for this to work
without displaying artifacts between edges.

classref-enumeration-constant

`AxisStretchMode<enum_NinePatchRect_AxisStretchMode>`
**AXIS\_STRETCH\_MODE\_TILE\_FIT** = `2`

Repeats the center texture across the NinePatchRect, but will also
stretch the texture to make sure each tile is visible in full. This may
cause the texture to be distorted, but less than
`AXIS_STRETCH_MODE_STRETCH<class_NinePatchRect_constant_AXIS_STRETCH_MODE_STRETCH>`.
The texture must be seamless for this to work without displaying
artifacts between edges.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`AxisStretchMode<enum_NinePatchRect_AxisStretchMode>`
**axis\_stretch\_horizontal** = `0`
`🔗<class_NinePatchRect_property_axis_stretch_horizontal>`

classref-property-setget

-   `void (No return value.)` **set\_h\_axis\_stretch\_mode**(value:
    `AxisStretchMode<enum_NinePatchRect_AxisStretchMode>`)
-   `AxisStretchMode<enum_NinePatchRect_AxisStretchMode>`
    **get\_h\_axis\_stretch\_mode**()

The stretch mode to use for horizontal stretching/tiling. See
`AxisStretchMode<enum_NinePatchRect_AxisStretchMode>` for possible
values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AxisStretchMode<enum_NinePatchRect_AxisStretchMode>`
**axis\_stretch\_vertical** = `0`
`🔗<class_NinePatchRect_property_axis_stretch_vertical>`

classref-property-setget

-   `void (No return value.)` **set\_v\_axis\_stretch\_mode**(value:
    `AxisStretchMode<enum_NinePatchRect_AxisStretchMode>`)
-   `AxisStretchMode<enum_NinePatchRect_AxisStretchMode>`
    **get\_v\_axis\_stretch\_mode**()

The stretch mode to use for vertical stretching/tiling. See
`AxisStretchMode<enum_NinePatchRect_AxisStretchMode>` for possible
values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **draw\_center** = `true`
`🔗<class_NinePatchRect_property_draw_center>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_center**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_draw\_center\_enabled**()

If `true`, draw the panel's center. Else, only draw the 9-slice's
borders.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **patch\_margin\_bottom** = `0`
`🔗<class_NinePatchRect_property_patch_margin_bottom>`

classref-property-setget

-   `void (No return value.)` **set\_patch\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, value: `int<class_int>`)
-   `int<class_int>` **get\_patch\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The height of the 9-slice's bottom row. A margin of 16 means the
9-slice's bottom corners and side will have a height of 16 pixels. You
can set all 4 margin values individually to create panels with
non-uniform borders.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **patch\_margin\_left** = `0`
`🔗<class_NinePatchRect_property_patch_margin_left>`

classref-property-setget

-   `void (No return value.)` **set\_patch\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, value: `int<class_int>`)
-   `int<class_int>` **get\_patch\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The width of the 9-slice's left column. A margin of 16 means the
9-slice's left corners and side will have a width of 16 pixels. You can
set all 4 margin values individually to create panels with non-uniform
borders.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **patch\_margin\_right** = `0`
`🔗<class_NinePatchRect_property_patch_margin_right>`

classref-property-setget

-   `void (No return value.)` **set\_patch\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, value: `int<class_int>`)
-   `int<class_int>` **get\_patch\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The width of the 9-slice's right column. A margin of 16 means the
9-slice's right corners and side will have a width of 16 pixels. You can
set all 4 margin values individually to create panels with non-uniform
borders.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **patch\_margin\_top** = `0`
`🔗<class_NinePatchRect_property_patch_margin_top>`

classref-property-setget

-   `void (No return value.)` **set\_patch\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, value: `int<class_int>`)
-   `int<class_int>` **get\_patch\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The height of the 9-slice's top row. A margin of 16 means the 9-slice's
top corners and side will have a height of 16 pixels. You can set all 4
margin values individually to create panels with non-uniform borders.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Rect2<class_Rect2>` **region\_rect** = `Rect2(0, 0, 0, 0)`
`🔗<class_NinePatchRect_property_region_rect>`

classref-property-setget

-   `void (No return value.)` **set\_region\_rect**(value:
    `Rect2<class_Rect2>`)
-   `Rect2<class_Rect2>` **get\_region\_rect**()

Rectangular region of the texture to sample from. If you're working with
an atlas, use this property to define the area the 9-slice should use.
All other properties are relative to this one. If the rect is empty,
NinePatchRect will use the whole texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture**
`🔗<class_NinePatchRect_property_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**()

The node's texture resource.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_patch\_margin**(margin:
`Side<enum_@GlobalScope_Side>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NinePatchRect_method_get_patch_margin>`

Returns the size of the margin on the specified
`Side<enum_@GlobalScope_Side>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_patch\_margin**(margin:
`Side<enum_@GlobalScope_Side>`, value: `int<class_int>`)
`🔗<class_NinePatchRect_method_set_patch_margin>`

Sets the size of the margin on the specified
`Side<enum_@GlobalScope_Side>` to `value` pixels.
