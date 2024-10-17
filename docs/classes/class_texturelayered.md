github\_url  
hide

# TextureLayered

**Inherits:** `Texture<class_Texture>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`CompressedTextureLayered<class_CompressedTextureLayered>`,
`ImageTextureLayered<class_ImageTextureLayered>`,
`PlaceholderTextureLayered<class_PlaceholderTextureLayered>`,
`TextureLayeredRD<class_TextureLayeredRD>`

Base class for texture types which contain the data of multiple
`Image<class_Image>`s. Each image is of the same size and format.

classref-introduction-group

## Description

Base class for `ImageTextureLayered<class_ImageTextureLayered>` and
`CompressedTextureLayered<class_CompressedTextureLayered>`. Cannot be
used directly, but contains all the functions necessary for accessing
the derived resource types. See also `Texture3D<class_Texture3D>`.

Data is set on a per-layer basis. For
`Texture2DArray<class_Texture2DArray>`s, the layer specifies the array
layer.

All images need to have the same width, height and number of mipmap
levels.

A **TextureLayered** can be loaded with
`ResourceLoader.load<class_ResourceLoader_method_load>`.

Internally, Godot maps these files to their respective counterparts in
the target rendering driver (Vulkan, OpenGL3).

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **LayeredType**: `🔗<enum_TextureLayered_LayeredType>`

classref-enumeration-constant

`LayeredType<enum_TextureLayered_LayeredType>`
**LAYERED\_TYPE\_2D\_ARRAY** = `0`

Texture is a generic `Texture2DArray<class_Texture2DArray>`.

classref-enumeration-constant

`LayeredType<enum_TextureLayered_LayeredType>`
**LAYERED\_TYPE\_CUBEMAP** = `1`

Texture is a `Cubemap<class_Cubemap>`, with each side in its own layer
(6 in total).

classref-enumeration-constant

`LayeredType<enum_TextureLayered_LayeredType>`
**LAYERED\_TYPE\_CUBEMAP\_ARRAY** = `2`

Texture is a `CubemapArray<class_CubemapArray>`, with each cubemap being
made of 6 layers.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Format<enum_Image_Format>` **\_get\_format**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_private_method__get_format>`

Called when the **TextureLayered**'s format is queried.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_height**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_private_method__get_height>`

Called when the **TextureLayered**'s height is queried.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **\_get\_layer\_data**(layer\_index:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_private_method__get_layer_data>`

Called when the data for a layer in the **TextureLayered** is queried.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_layered\_type**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_private_method__get_layered_type>`

Called when the layers' type in the **TextureLayered** is queried.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_layers**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_private_method__get_layers>`

Called when the number of layers in the **TextureLayered** is queried.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_width**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_private_method__get_width>`

Called when the **TextureLayered**'s width queried.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_has\_mipmaps**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_private_method__has_mipmaps>`

Called when the presence of mipmaps in the **TextureLayered** is
queried.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Format<enum_Image_Format>` **get\_format**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_method_get_format>`

Returns the current format being used by this texture. See
`Format<enum_Image_Format>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_height**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_method_get_height>`

Returns the height of the texture in pixels. Height is typically
represented by the Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **get\_layer\_data**(layer: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_method_get_layer_data>`

Returns an `Image<class_Image>` resource with the data from specified
`layer`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`LayeredType<enum_TextureLayered_LayeredType>` **get\_layered\_type**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_method_get_layered_type>`

Returns the **TextureLayered**'s type. The type determines how the data
is accessed, with cubemaps having special types.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_layers**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_method_get_layers>`

Returns the number of referenced `Image<class_Image>`s.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_width**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_method_get_width>`

Returns the width of the texture in pixels. Width is typically
represented by the X axis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_mipmaps**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextureLayered_method_has_mipmaps>`

Returns `true` if the layers have generated mipmaps.
