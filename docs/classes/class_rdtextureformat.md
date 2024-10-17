github\_url  
hide

# RDTextureFormat

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Texture format (used by `RenderingDevice<class_RenderingDevice>`).

classref-introduction-group

## Description

This object is used by `RenderingDevice<class_RenderingDevice>`.

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

## Property Descriptions

classref-property

`int<class_int>` **array\_layers** = `1`
`🔗<class_RDTextureFormat_property_array_layers>`

classref-property-setget

-   `void (No return value.)` **set\_array\_layers**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_array\_layers**()

The number of layers in the texture. Only relevant for 2D texture
arrays.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **depth** = `1`
`🔗<class_RDTextureFormat_property_depth>`

classref-property-setget

-   `void (No return value.)` **set\_depth**(value: `int<class_int>`)
-   `int<class_int>` **get\_depth**()

The texture's depth (in pixels). This is always `1` for 2D textures.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DataFormat<enum_RenderingDevice_DataFormat>` **format** = `8`
`🔗<class_RDTextureFormat_property_format>`

classref-property-setget

-   `void (No return value.)` **set\_format**(value:
    `DataFormat<enum_RenderingDevice_DataFormat>`)
-   `DataFormat<enum_RenderingDevice_DataFormat>` **get\_format**()

The texture's pixel data format.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **height** = `1`
`🔗<class_RDTextureFormat_property_height>`

classref-property-setget

-   `void (No return value.)` **set\_height**(value: `int<class_int>`)
-   `int<class_int>` **get\_height**()

The texture's height (in pixels).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **mipmaps** = `1`
`🔗<class_RDTextureFormat_property_mipmaps>`

classref-property-setget

-   `void (No return value.)` **set\_mipmaps**(value: `int<class_int>`)
-   `int<class_int>` **get\_mipmaps**()

The number of mipmaps available in the texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureSamples<enum_RenderingDevice_TextureSamples>` **samples** = `0`
`🔗<class_RDTextureFormat_property_samples>`

classref-property-setget

-   `void (No return value.)` **set\_samples**(value:
    `TextureSamples<enum_RenderingDevice_TextureSamples>`)
-   `TextureSamples<enum_RenderingDevice_TextureSamples>`
    **get\_samples**()

The number of samples used when sampling the texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureType<enum_RenderingDevice_TextureType>` **texture\_type** = `1`
`🔗<class_RDTextureFormat_property_texture_type>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_type**(value:
    `TextureType<enum_RenderingDevice_TextureType>`)
-   `TextureType<enum_RenderingDevice_TextureType>`
    **get\_texture\_type**()

The texture type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`\]
**usage\_bits** = `0` `🔗<class_RDTextureFormat_property_usage_bits>`

classref-property-setget

-   `void (No return value.)` **set\_usage\_bits**(value:
    `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`\])
-   `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`TextureUsageBits<enum_RenderingDevice_TextureUsageBits>`\]
    **get\_usage\_bits**()

The texture's usage bits, which determine what can be done using the
texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **width** = `1`
`🔗<class_RDTextureFormat_property_width>`

classref-property-setget

-   `void (No return value.)` **set\_width**(value: `int<class_int>`)
-   `int<class_int>` **get\_width**()

The texture's width (in pixels).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_shareable\_format**(format:
`DataFormat<enum_RenderingDevice_DataFormat>`)
`🔗<class_RDTextureFormat_method_add_shareable_format>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_shareable\_format**(format:
`DataFormat<enum_RenderingDevice_DataFormat>`)
`🔗<class_RDTextureFormat_method_remove_shareable_format>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
