github\_url  
hide

# Texture2DArray

**Inherits:** `ImageTextureLayered<class_ImageTextureLayered>` **&lt;**
`TextureLayered<class_TextureLayered>` **&lt;** `Texture<class_Texture>`
**&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A single texture resource which consists of multiple, separate images.
Each image has the same dimensions and number of mipmap levels.

classref-introduction-group

## Description

A Texture2DArray is different from a Texture3D: The Texture2DArray does
not support trilinear interpolation between the `Image<class_Image>`s,
i.e. no blending. See also `Cubemap<class_Cubemap>` and
`CubemapArray<class_CubemapArray>`, which are texture arrays with
specialized cubemap functions.

A Texture2DArray is also different from an
`AtlasTexture<class_AtlasTexture>`: In a Texture2DArray, all images are
treated separately. In an atlas, the regions (i.e. the single images)
can be of different sizes. Furthermore, you usually need to add a
padding around the regions, to prevent accidental UV mapping to more
than one region. The same goes for mipmapping: Mipmap chains are handled
separately for each layer. In an atlas, the slicing has to be done
manually in the fragment shader.

To create such a texture file yourself, reimport your image files using
the Godot Editor import presets.

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Resource<class_Resource>` **create\_placeholder**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Texture2DArray_method_create_placeholder>`

Creates a placeholder version of this resource
(`PlaceholderTexture2DArray<class_PlaceholderTexture2DArray>`).
