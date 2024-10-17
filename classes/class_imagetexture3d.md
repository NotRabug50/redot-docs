github\_url  
hide

# ImageTexture3D

**Inherits:** `Texture3D<class_Texture3D>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Texture with 3 dimensions.

classref-introduction-group

## Description

**ImageTexture3D** is a 3-dimensional `ImageTexture<class_ImageTexture>`
that has a width, height, and depth. See also
`ImageTextureLayered<class_ImageTextureLayered>`.

3D textures are typically used to store density maps for
`FogMaterial<class_FogMaterial>`, color correction LUTs for
`Environment<class_Environment>`, vector fields for
`GPUParticlesAttractorVectorField3D<class_GPUParticlesAttractorVectorField3D>`
and collision maps for
`GPUParticlesCollisionSDF3D<class_GPUParticlesCollisionSDF3D>`. 3D
textures can also be used in custom shaders.

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

`Error<enum_@GlobalScope_Error>` **create**(format:
`Format<enum_Image_Format>`, width: `int<class_int>`, height:
`int<class_int>`, depth: `int<class_int>`, use\_mipmaps:
`bool<class_bool>`, data: `Array<class_Array>`\[`Image<class_Image>`\])
`🔗<class_ImageTexture3D_method_create>`

Creates the **ImageTexture3D** with specified `width`, `height`, and
`depth`. See `Format<enum_Image_Format>` for `format` options. If
`use_mipmaps` is `true`, then generate mipmaps for the
**ImageTexture3D**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update**(data:
`Array<class_Array>`\[`Image<class_Image>`\])
`🔗<class_ImageTexture3D_method_update>`

Replaces the texture's existing data with the layers specified in
`data`. The size of `data` must match the parameters that were used for
`create<class_ImageTexture3D_method_create>`. In other words, the
texture cannot be resized or have its format changed by calling
`update<class_ImageTexture3D_method_update>`.
