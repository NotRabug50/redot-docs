github\_url  
hide

# PlaceholderCubemap

**Inherits:**
`PlaceholderTextureLayered<class_PlaceholderTextureLayered>` **&lt;**
`TextureLayered<class_TextureLayered>` **&lt;** `Texture<class_Texture>`
**&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A `Cubemap<class_Cubemap>` without image data.

classref-introduction-group

## Description

This class replaces a `Cubemap<class_Cubemap>` or a
`Cubemap<class_Cubemap>`-derived class in 2 conditions:

-   In dedicated server mode, where the image data shouldn't affect game
    logic. This allows reducing the exported PCK's size significantly.
-   When the `Cubemap<class_Cubemap>`-derived class is missing, for
    example when using a different engine version.

\*\*Note:\*\* This class is not intended for rendering or for use in
shaders. Operations like calculating UV are not guaranteed to work.
