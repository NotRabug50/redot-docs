github\_url  
hide

# ImageTextureLayered

**Inherits:** `TextureLayered<class_TextureLayered>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `Cubemap<class_Cubemap>`,
`CubemapArray<class_CubemapArray>`,
`Texture2DArray<class_Texture2DArray>`

Base class for texture types which contain the data of multiple
`ImageTexture<class_ImageTexture>`s. Each image is of the same size and
format.

classref-introduction-group

## Description

Base class for `Texture2DArray<class_Texture2DArray>`,
`Cubemap<class_Cubemap>` and `CubemapArray<class_CubemapArray>`. Cannot
be used directly, but contains all the functions necessary for accessing
the derived resource types. See also `Texture3D<class_Texture3D>`.

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

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **create\_from\_images**(images:
`Array<class_Array>`\[`Image<class_Image>`\])
`🔗<class_ImageTextureLayered_method_create_from_images>`

Creates an **ImageTextureLayered** from an array of
`Image<class_Image>`s. See `Image.create<class_Image_method_create>` for
the expected data format. The first image decides the width, height,
image format and mipmapping setting. The other images *must* have the
same width, height, image format and mipmapping setting.

Each `Image<class_Image>` represents one `layer`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update\_layer**(image: `Image<class_Image>`,
layer: `int<class_int>`)
`🔗<class_ImageTextureLayered_method_update_layer>`

Replaces the existing `Image<class_Image>` data at the given `layer`
with this new image.

The given `Image<class_Image>` must have the same width, height, image
format, and mipmapping flag as the rest of the referenced images.

If the image format is unsupported, it will be decompressed and
converted to a similar and supported `Format<enum_Image_Format>`.

The update is immediate: it's synchronized with drawing.
