github\_url  
hide

# CubemapArray

**Inherits:** `ImageTextureLayered<class_ImageTextureLayered>` **&lt;**
`TextureLayered<class_TextureLayered>` **&lt;** `Texture<class_Texture>`
**&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

An array of `Cubemap<class_Cubemap>`s, stored together and with a single
reference.

classref-introduction-group

## Description

**CubemapArray**s are made of an array of `Cubemap<class_Cubemap>`s.
Like `Cubemap<class_Cubemap>`s, they are made of multiple textures, the
amount of which must be divisible by 6 (one for each face of the cube).

The primary benefit of **CubemapArray**s is that they can be accessed in
shader code using a single texture reference. In other words, you can
pass multiple `Cubemap<class_Cubemap>`s into a shader using a single
**CubemapArray**. `Cubemap<class_Cubemap>`s are allocated in adjacent
cache regions on the GPU, which makes **CubemapArray**s the most
efficient way to store multiple `Cubemap<class_Cubemap>`s.

\*\*Note:\*\* Godot uses **CubemapArray**s internally for many effects,
including the `Sky<class_Sky>` if you set
`ProjectSettings.rendering/reflections/sky_reflections/texture_array_reflections<class_ProjectSettings_property_rendering/reflections/sky_reflections/texture_array_reflections>`
to `true`. To create such a texture file yourself, reimport your image
files using the import presets of the File System dock.

\*\*Note:\*\* **CubemapArray** is not supported in the OpenGL 3
rendering backend.

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
`🔗<class_CubemapArray_method_create_placeholder>`

Creates a placeholder version of this resource
(`PlaceholderCubemapArray<class_PlaceholderCubemapArray>`).
