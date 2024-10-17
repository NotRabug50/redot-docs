github\_url  
hide

# Gradient

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A color transition.

classref-introduction-group

## Description

This resource describes a color transition by defining a set of colored
points and how to interpolate between them.

See also `Curve<class_Curve>` which supports more complex easing
methods, but does not support colors.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **InterpolationMode**: `🔗<enum_Gradient_InterpolationMode>`

classref-enumeration-constant

`InterpolationMode<enum_Gradient_InterpolationMode>`
**GRADIENT\_INTERPOLATE\_LINEAR** = `0`

Linear interpolation.

classref-enumeration-constant

`InterpolationMode<enum_Gradient_InterpolationMode>`
**GRADIENT\_INTERPOLATE\_CONSTANT** = `1`

Constant interpolation, color changes abruptly at each point and stays
uniform between. This might cause visible aliasing when used for a
gradient texture in some cases.

classref-enumeration-constant

`InterpolationMode<enum_Gradient_InterpolationMode>`
**GRADIENT\_INTERPOLATE\_CUBIC** = `2`

Cubic interpolation.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ColorSpace**: `🔗<enum_Gradient_ColorSpace>`

classref-enumeration-constant

`ColorSpace<enum_Gradient_ColorSpace>` **GRADIENT\_COLOR\_SPACE\_SRGB**
= `0`

sRGB color space.

classref-enumeration-constant

`ColorSpace<enum_Gradient_ColorSpace>`
**GRADIENT\_COLOR\_SPACE\_LINEAR\_SRGB** = `1`

Linear sRGB color space.

classref-enumeration-constant

`ColorSpace<enum_Gradient_ColorSpace>` **GRADIENT\_COLOR\_SPACE\_OKLAB**
= `2`

[Oklab](https://bottosson.github.io/posts/oklab/) color space. This
color space provides a smooth and uniform-looking transition between
colors.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`PackedColorArray<class_PackedColorArray>` **colors** =
`PackedColorArray(0, 0, 0, 1, 1, 1, 1, 1)`
`🔗<class_Gradient_property_colors>`

classref-property-setget

-   `void (No return value.)` **set\_colors**(value:
    `PackedColorArray<class_PackedColorArray>`)
-   `PackedColorArray<class_PackedColorArray>` **get\_colors**()

Gradient's colors as a `PackedColorArray<class_PackedColorArray>`.

\*\*Note:\*\* Setting this property updates all colors at once. To
update any color individually use
`set_color<class_Gradient_method_set_color>`.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedColorArray<class_PackedColorArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ColorSpace<enum_Gradient_ColorSpace>` **interpolation\_color\_space** =
`0` `🔗<class_Gradient_property_interpolation_color_space>`

classref-property-setget

-   `void (No return value.)`
    **set\_interpolation\_color\_space**(value:
    `ColorSpace<enum_Gradient_ColorSpace>`)
-   `ColorSpace<enum_Gradient_ColorSpace>`
    **get\_interpolation\_color\_space**()

The color space used to interpolate between points of the gradient. It
does not affect the returned colors, which will always be in sRGB space.
See `ColorSpace<enum_Gradient_ColorSpace>` for available modes.

\*\*Note:\*\* This setting has no effect when
`interpolation_mode<class_Gradient_property_interpolation_mode>` is set
to
`GRADIENT_INTERPOLATE_CONSTANT<class_Gradient_constant_GRADIENT_INTERPOLATE_CONSTANT>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`InterpolationMode<enum_Gradient_InterpolationMode>`
**interpolation\_mode** = `0`
`🔗<class_Gradient_property_interpolation_mode>`

classref-property-setget

-   `void (No return value.)` **set\_interpolation\_mode**(value:
    `InterpolationMode<enum_Gradient_InterpolationMode>`)
-   `InterpolationMode<enum_Gradient_InterpolationMode>`
    **get\_interpolation\_mode**()

The algorithm used to interpolate between points of the gradient. See
`InterpolationMode<enum_Gradient_InterpolationMode>` for available
modes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedFloat32Array<class_PackedFloat32Array>` **offsets** =
`PackedFloat32Array(0, 1)` `🔗<class_Gradient_property_offsets>`

classref-property-setget

-   `void (No return value.)` **set\_offsets**(value:
    `PackedFloat32Array<class_PackedFloat32Array>`)
-   `PackedFloat32Array<class_PackedFloat32Array>` **get\_offsets**()

Gradient's offsets as a `PackedFloat32Array<class_PackedFloat32Array>`.

\*\*Note:\*\* Setting this property updates all offsets at once. To
update any offset individually use
`set_offset<class_Gradient_method_set_offset>`.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedFloat32Array<class_PackedFloat32Array>` for more details.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_point**(offset: `float<class_float>`,
color: `Color<class_Color>`) `🔗<class_Gradient_method_add_point>`

Adds the specified color to the gradient, with the specified offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_color**(point: `int<class_int>`)
`🔗<class_Gradient_method_get_color>`

Returns the color of the gradient color at index `point`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_offset**(point: `int<class_int>`)
`🔗<class_Gradient_method_get_offset>`

Returns the offset of the gradient color at index `point`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_point\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Gradient_method_get_point_count>`

Returns the number of colors in the gradient.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_point**(point: `int<class_int>`)
`🔗<class_Gradient_method_remove_point>`

Removes the color at index `point`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reverse**()
`🔗<class_Gradient_method_reverse>`

Reverses/mirrors the gradient.

\*\*Note:\*\* This method mirrors all points around the middle of the
gradient, which may produce unexpected results when
`interpolation_mode<class_Gradient_property_interpolation_mode>` is set
to
`GRADIENT_INTERPOLATE_CONSTANT<class_Gradient_constant_GRADIENT_INTERPOLATE_CONSTANT>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **sample**(offset: `float<class_float>`)
`🔗<class_Gradient_method_sample>`

Returns the interpolated color specified by `offset`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_color**(point: `int<class_int>`, color:
`Color<class_Color>`) `🔗<class_Gradient_method_set_color>`

Sets the color of the gradient color at index `point`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_offset**(point: `int<class_int>`,
offset: `float<class_float>`) `🔗<class_Gradient_method_set_offset>`

Sets the offset for the gradient color at index `point`.
