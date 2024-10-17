github\_url  
hide

# CurveTexture

**Inherits:** `Texture2D<class_Texture2D>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A 1D texture where pixel brightness corresponds to points on a curve.

classref-introduction-group

## Description

A 1D texture where pixel brightness corresponds to points on a
`Curve<class_Curve>` resource, either in grayscale or in red. This
visual representation simplifies the task of saving curves as image
files.

If you need to store up to 3 curves within a single texture, use
`CurveXYZTexture<class_CurveXYZTexture>` instead. See also
`GradientTexture1D<class_GradientTexture1D>` and
`GradientTexture2D<class_GradientTexture2D>`.

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **TextureMode**: `🔗<enum_CurveTexture_TextureMode>`

classref-enumeration-constant

`TextureMode<enum_CurveTexture_TextureMode>` **TEXTURE\_MODE\_RGB** =
`0`

Store the curve equally across the red, green and blue channels. This
uses more video memory, but is more compatible with shaders that only
read the green and blue values.

classref-enumeration-constant

`TextureMode<enum_CurveTexture_TextureMode>` **TEXTURE\_MODE\_RED** =
`1`

Store the curve only in the red channel. This saves video memory, but
some custom shaders may not be able to work with this.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Curve<class_Curve>` **curve** `🔗<class_CurveTexture_property_curve>`

classref-property-setget

-   `void (No return value.)` **set\_curve**(value:
    `Curve<class_Curve>`)
-   `Curve<class_Curve>` **get\_curve**()

The `Curve<class_Curve>` that is rendered onto the texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureMode<enum_CurveTexture_TextureMode>` **texture\_mode** = `0`
`🔗<class_CurveTexture_property_texture_mode>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_mode**(value:
    `TextureMode<enum_CurveTexture_TextureMode>`)
-   `TextureMode<enum_CurveTexture_TextureMode>`
    **get\_texture\_mode**()

The format the texture should be generated with. When passing a
CurveTexture as an input to a `Shader<class_Shader>`, this may need to
be adjusted.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **width** = `256`
`🔗<class_CurveTexture_property_width>`

classref-property-setget

-   `void (No return value.)` **set\_width**(value: `int<class_int>`)
-   `int<class_int>` **get\_width**()

The width of the texture (in pixels). Higher values make it possible to
represent high-frequency data better (such as sudden direction changes),
at the cost of increased generation time and memory usage.
