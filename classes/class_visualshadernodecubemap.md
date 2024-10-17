github\_url  
hide

# VisualShaderNodeCubemap

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A `Cubemap<class_Cubemap>` sampling node to be used within the visual
shader graph.

classref-introduction-group

## Description

Translated to `texture(cubemap, vec3)` in the shader language. Returns a
color vector and alpha channel as scalar.

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Source**: `🔗<enum_VisualShaderNodeCubemap_Source>`

classref-enumeration-constant

`Source<enum_VisualShaderNodeCubemap_Source>` **SOURCE\_TEXTURE** = `0`

Use the `Cubemap<class_Cubemap>` set via
`cube_map<class_VisualShaderNodeCubemap_property_cube_map>`. If this is
set to `source<class_VisualShaderNodeCubemap_property_source>`, the
`samplerCube` port is ignored.

classref-enumeration-constant

`Source<enum_VisualShaderNodeCubemap_Source>` **SOURCE\_PORT** = `1`

Use the `Cubemap<class_Cubemap>` sampler reference passed via the
`samplerCube` port. If this is set to
`source<class_VisualShaderNodeCubemap_property_source>`, the
`cube_map<class_VisualShaderNodeCubemap_property_cube_map>` texture is
ignored.

classref-enumeration-constant

`Source<enum_VisualShaderNodeCubemap_Source>` **SOURCE\_MAX** = `2`

Represents the size of the `Source<enum_VisualShaderNodeCubemap_Source>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureType**: `🔗<enum_VisualShaderNodeCubemap_TextureType>`

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeCubemap_TextureType>` **TYPE\_DATA** =
`0`

No hints are added to the uniform declaration.

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeCubemap_TextureType>` **TYPE\_COLOR**
= `1`

Adds `source_color` as hint to the uniform declaration for proper sRGB
to linear conversion.

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeCubemap_TextureType>`
**TYPE\_NORMAL\_MAP** = `2`

Adds `hint_normal` as hint to the uniform declaration, which internally
converts the texture for proper usage as normal map.

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeCubemap_TextureType>` **TYPE\_MAX** =
`3`

Represents the size of the
`TextureType<enum_VisualShaderNodeCubemap_TextureType>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`TextureLayered<class_TextureLayered>` **cube\_map**
`🔗<class_VisualShaderNodeCubemap_property_cube_map>`

classref-property-setget

-   `void (No return value.)` **set\_cube\_map**(value:
    `TextureLayered<class_TextureLayered>`)
-   `TextureLayered<class_TextureLayered>` **get\_cube\_map**()

The `Cubemap<class_Cubemap>` texture to sample when using
`SOURCE_TEXTURE<class_VisualShaderNodeCubemap_constant_SOURCE_TEXTURE>`
as `source<class_VisualShaderNodeCubemap_property_source>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Source<enum_VisualShaderNodeCubemap_Source>` **source** = `0`
`🔗<class_VisualShaderNodeCubemap_property_source>`

classref-property-setget

-   `void (No return value.)` **set\_source**(value:
    `Source<enum_VisualShaderNodeCubemap_Source>`)
-   `Source<enum_VisualShaderNodeCubemap_Source>` **get\_source**()

Defines which source should be used for the sampling. See
`Source<enum_VisualShaderNodeCubemap_Source>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureType<enum_VisualShaderNodeCubemap_TextureType>`
**texture\_type** = `0`
`🔗<class_VisualShaderNodeCubemap_property_texture_type>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_type**(value:
    `TextureType<enum_VisualShaderNodeCubemap_TextureType>`)
-   `TextureType<enum_VisualShaderNodeCubemap_TextureType>`
    **get\_texture\_type**()

Defines the type of data provided by the source texture. See
`TextureType<enum_VisualShaderNodeCubemap_TextureType>` for options.
