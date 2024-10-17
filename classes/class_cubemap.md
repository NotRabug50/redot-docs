github\_url  
hide

# Cubemap

**Inherits:** `ImageTextureLayered<class_ImageTextureLayered>` **&lt;**
`TextureLayered<class_TextureLayered>` **&lt;** `Texture<class_Texture>`
**&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Six square textures representing the faces of a cube. Commonly used as a
skybox.

classref-introduction-group

## Description

A cubemap is made of 6 textures organized in layers. They are typically
used for faking reflections in 3D rendering (see
`ReflectionProbe<class_ReflectionProbe>`). It can be used to make an
object look as if it's reflecting its surroundings. This usually
delivers much better performance than other reflection methods.

This resource is typically used as a uniform in custom shaders. Few core
Godot methods make use of **Cubemap** resources.

To create such a texture file yourself, reimport your image files using
the Godot Editor import presets.

\*\*Note:\*\* Godot doesn't support using cubemaps in a
`PanoramaSkyMaterial<class_PanoramaSkyMaterial>`. You can use [this
tool](https://danilw.github.io/GLSL-howto/cubemap_to_panorama_js/cubemap_to_panorama.html)
to convert a cubemap to an equirectangular sky map.

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
`🔗<class_Cubemap_method_create_placeholder>`

Creates a placeholder version of this resource
(`PlaceholderCubemap<class_PlaceholderCubemap>`).
