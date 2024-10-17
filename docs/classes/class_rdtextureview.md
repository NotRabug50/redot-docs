github\_url  
hide

# RDTextureView

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Texture view (used by `RenderingDevice<class_RenderingDevice>`).

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`DataFormat<enum_RenderingDevice_DataFormat>` **format\_override** =
`218` `🔗<class_RDTextureView_property_format_override>`

classref-property-setget

-   `void (No return value.)` **set\_format\_override**(value:
    `DataFormat<enum_RenderingDevice_DataFormat>`)
-   `DataFormat<enum_RenderingDevice_DataFormat>`
    **get\_format\_override**()

Optional override for the data format to return sampled values in. The
default value of
`RenderingDevice.DATA_FORMAT_MAX<class_RenderingDevice_constant_DATA_FORMAT_MAX>`
does not override the format.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>` **swizzle\_a** =
`6` `🔗<class_RDTextureView_property_swizzle_a>`

classref-property-setget

-   `void (No return value.)` **set\_swizzle\_a**(value:
    `TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`)
-   `TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
    **get\_swizzle\_a**()

The channel to sample when sampling the alpha channel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>` **swizzle\_b** =
`5` `🔗<class_RDTextureView_property_swizzle_b>`

classref-property-setget

-   `void (No return value.)` **set\_swizzle\_b**(value:
    `TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`)
-   `TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
    **get\_swizzle\_b**()

The channel to sample when sampling the blue color channel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>` **swizzle\_g** =
`4` `🔗<class_RDTextureView_property_swizzle_g>`

classref-property-setget

-   `void (No return value.)` **set\_swizzle\_g**(value:
    `TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`)
-   `TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
    **get\_swizzle\_g**()

The channel to sample when sampling the green color channel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureSwizzle<enum_RenderingDevice_TextureSwizzle>` **swizzle\_r** =
`3` `🔗<class_RDTextureView_property_swizzle_r>`

classref-property-setget

-   `void (No return value.)` **set\_swizzle\_r**(value:
    `TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`)
-   `TextureSwizzle<enum_RenderingDevice_TextureSwizzle>`
    **get\_swizzle\_r**()

The channel to sample when sampling the red color channel.
