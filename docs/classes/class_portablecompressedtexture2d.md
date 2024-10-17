github\_url  
hide

# PortableCompressedTexture2D

**Inherits:** `Texture2D<class_Texture2D>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Provides a compressed texture for disk and/or VRAM in a way that is
portable.

classref-introduction-group

## Description

This class allows storing compressed textures as self contained (not
imported) resources.

For 2D usage (compressed on disk, uncompressed on VRAM), the lossy and
lossless modes are recommended. For 3D usage (compressed on VRAM) it
depends on the target platform.

If you intend to only use desktop, S3TC or BPTC are recommended. For
only mobile, ETC2 is recommended.

For portable, self contained 3D textures that work on both desktop and
mobile, Basis Universal is recommended (although it has a small quality
cost and longer compression time as a tradeoff).

This resource is intended to be created from code.

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **CompressionMode**:
`🔗<enum_PortableCompressedTexture2D_CompressionMode>`

classref-enumeration-constant

`CompressionMode<enum_PortableCompressedTexture2D_CompressionMode>`
**COMPRESSION\_MODE\_LOSSLESS** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CompressionMode<enum_PortableCompressedTexture2D_CompressionMode>`
**COMPRESSION\_MODE\_LOSSY** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CompressionMode<enum_PortableCompressedTexture2D_CompressionMode>`
**COMPRESSION\_MODE\_BASIS\_UNIVERSAL** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CompressionMode<enum_PortableCompressedTexture2D_CompressionMode>`
**COMPRESSION\_MODE\_S3TC** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CompressionMode<enum_PortableCompressedTexture2D_CompressionMode>`
**COMPRESSION\_MODE\_ETC2** = `4`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CompressionMode<enum_PortableCompressedTexture2D_CompressionMode>`
**COMPRESSION\_MODE\_BPTC** = `5`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **keep\_compressed\_buffer** = `false`
`🔗<class_PortableCompressedTexture2D_property_keep_compressed_buffer>`

classref-property-setget

-   `void (No return value.)` **set\_keep\_compressed\_buffer**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_keeping\_compressed\_buffer**()

When running on the editor, this class will keep the source compressed
data in memory. Otherwise, the source compressed data is lost after
loading and the resource can't be re saved.

This flag allows to keep the compressed data in memory if you intend it
to persist after loading.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **size\_override** = `Vector2(0, 0)`
`🔗<class_PortableCompressedTexture2D_property_size_override>`

classref-property-setget

-   `void (No return value.)` **set\_size\_override**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_size\_override**()

Allow overriding the texture size (for 2D only).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **create\_from\_image**(image:
`Image<class_Image>`, compression\_mode:
`CompressionMode<enum_PortableCompressedTexture2D_CompressionMode>`,
normal\_map: `bool<class_bool>` = false, lossy\_quality:
`float<class_float>` = 0.8)
`🔗<class_PortableCompressedTexture2D_method_create_from_image>`

Initializes the compressed texture from a base image. The compression
mode must be provided.

`normal_map` is recommended to ensure optimum quality if this image will
be used as a normal map.

If lossy compression is requested, the quality setting can optionally be
provided. This maps to Lossy WebP compression quality.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CompressionMode<enum_PortableCompressedTexture2D_CompressionMode>`
**get\_compression\_mode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PortableCompressedTexture2D_method_get_compression_mode>`

Return the compression mode used (valid after initialized).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Format<enum_Image_Format>` **get\_format**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PortableCompressedTexture2D_method_get_format>`

Return the image format used (valid after initialized).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_keeping\_all\_compressed\_buffers**()
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_PortableCompressedTexture2D_method_is_keeping_all_compressed_buffers>`

Return whether the flag is overridden for all textures of this type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_keep\_all\_compressed\_buffers**(keep:
`bool<class_bool>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_PortableCompressedTexture2D_method_set_keep_all_compressed_buffers>`

Overrides the flag globally for all textures of this type. This is used
primarily by the editor.
