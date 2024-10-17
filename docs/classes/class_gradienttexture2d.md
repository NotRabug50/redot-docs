github\_url  
hide

# GradientTexture2D

**Inherits:** `Texture2D<class_Texture2D>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A 2D texture that creates a pattern with colors obtained from a
`Gradient<class_Gradient>`.

classref-introduction-group

## Description

A 2D texture that obtains colors from a `Gradient<class_Gradient>` to
fill the texture data. This texture is able to transform a color
transition into different patterns such as a linear or a radial
gradient. The gradient is sampled individually for each pixel so it does
not necessarily represent an exact copy of the gradient(see
`width<class_GradientTexture2D_property_width>` and
`height<class_GradientTexture2D_property_height>`). See also
`GradientTexture1D<class_GradientTexture1D>`,
`CurveTexture<class_CurveTexture>` and
`CurveXYZTexture<class_CurveXYZTexture>`.

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Fill**: `🔗<enum_GradientTexture2D_Fill>`

classref-enumeration-constant

`Fill<enum_GradientTexture2D_Fill>` **FILL\_LINEAR** = `0`

The colors are linearly interpolated in a straight line.

classref-enumeration-constant

`Fill<enum_GradientTexture2D_Fill>` **FILL\_RADIAL** = `1`

The colors are linearly interpolated in a circular pattern.

classref-enumeration-constant

`Fill<enum_GradientTexture2D_Fill>` **FILL\_SQUARE** = `2`

The colors are linearly interpolated in a square pattern.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Repeat**: `🔗<enum_GradientTexture2D_Repeat>`

classref-enumeration-constant

`Repeat<enum_GradientTexture2D_Repeat>` **REPEAT\_NONE** = `0`

The gradient fill is restricted to the range defined by
`fill_from<class_GradientTexture2D_property_fill_from>` to
`fill_to<class_GradientTexture2D_property_fill_to>` offsets.

classref-enumeration-constant

`Repeat<enum_GradientTexture2D_Repeat>` **REPEAT** = `1`

The texture is filled starting from
`fill_from<class_GradientTexture2D_property_fill_from>` to
`fill_to<class_GradientTexture2D_property_fill_to>` offsets, repeating
the same pattern in both directions.

classref-enumeration-constant

`Repeat<enum_GradientTexture2D_Repeat>` **REPEAT\_MIRROR** = `2`

The texture is filled starting from
`fill_from<class_GradientTexture2D_property_fill_from>` to
`fill_to<class_GradientTexture2D_property_fill_to>` offsets, mirroring
the pattern in both directions.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Fill<enum_GradientTexture2D_Fill>` **fill** = `0`
`🔗<class_GradientTexture2D_property_fill>`

classref-property-setget

-   `void (No return value.)` **set\_fill**(value:
    `Fill<enum_GradientTexture2D_Fill>`)
-   `Fill<enum_GradientTexture2D_Fill>` **get\_fill**()

The gradient fill type, one of the `Fill<enum_GradientTexture2D_Fill>`
values. The texture is filled by interpolating colors starting from
`fill_from<class_GradientTexture2D_property_fill_from>` to
`fill_to<class_GradientTexture2D_property_fill_to>` offsets.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **fill\_from** = `Vector2(0, 0)`
`🔗<class_GradientTexture2D_property_fill_from>`

classref-property-setget

-   `void (No return value.)` **set\_fill\_from**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_fill\_from**()

The initial offset used to fill the texture specified in UV coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **fill\_to** = `Vector2(1, 0)`
`🔗<class_GradientTexture2D_property_fill_to>`

classref-property-setget

-   `void (No return value.)` **set\_fill\_to**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_fill\_to**()

The final offset used to fill the texture specified in UV coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Gradient<class_Gradient>` **gradient**
`🔗<class_GradientTexture2D_property_gradient>`

classref-property-setget

-   `void (No return value.)` **set\_gradient**(value:
    `Gradient<class_Gradient>`)
-   `Gradient<class_Gradient>` **get\_gradient**()

The `Gradient<class_Gradient>` used to fill the texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **height** = `64`
`🔗<class_GradientTexture2D_property_height>`

classref-property-setget

-   `void (No return value.)` **set\_height**(value: `int<class_int>`)
-   `int<class_int>` **get\_height**()

The number of vertical color samples that will be obtained from the
`Gradient<class_Gradient>`, which also represents the texture's height.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Repeat<enum_GradientTexture2D_Repeat>` **repeat** = `0`
`🔗<class_GradientTexture2D_property_repeat>`

classref-property-setget

-   `void (No return value.)` **set\_repeat**(value:
    `Repeat<enum_GradientTexture2D_Repeat>`)
-   `Repeat<enum_GradientTexture2D_Repeat>` **get\_repeat**()

The gradient repeat type, one of the
`Repeat<enum_GradientTexture2D_Repeat>` values. The texture is filled
starting from `fill_from<class_GradientTexture2D_property_fill_from>` to
`fill_to<class_GradientTexture2D_property_fill_to>` offsets by default,
but the gradient fill can be repeated to cover the entire texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_hdr** = `false`
`🔗<class_GradientTexture2D_property_use_hdr>`

classref-property-setget

-   `void (No return value.)` **set\_use\_hdr**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_hdr**()

If `true`, the generated texture will support high dynamic range
(`Image.FORMAT_RGBAF<class_Image_constant_FORMAT_RGBAF>` format). This
allows for glow effects to work if
`Environment.glow_enabled<class_Environment_property_glow_enabled>` is
`true`. If `false`, the generated texture will use low dynamic range;
overbright colors will be clamped
(`Image.FORMAT_RGBA8<class_Image_constant_FORMAT_RGBA8>` format).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **width** = `64`
`🔗<class_GradientTexture2D_property_width>`

classref-property-setget

-   `void (No return value.)` **set\_width**(value: `int<class_int>`)
-   `int<class_int>` **get\_width**()

The number of horizontal color samples that will be obtained from the
`Gradient<class_Gradient>`, which also represents the texture's width.
