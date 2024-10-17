github\_url  
hide

# VisualShaderNodeTexture

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Performs a 2D texture lookup within the visual shader graph.

classref-introduction-group

## Description

Performs a lookup operation on the provided texture, with support for
multiple texture sources to choose from.

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

enum **Source**: `🔗<enum_VisualShaderNodeTexture_Source>`

classref-enumeration-constant

`Source<enum_VisualShaderNodeTexture_Source>` **SOURCE\_TEXTURE** = `0`

Use the texture given as an argument for this function.

classref-enumeration-constant

`Source<enum_VisualShaderNodeTexture_Source>` **SOURCE\_SCREEN** = `1`

Use the current viewport's texture as the source.

classref-enumeration-constant

`Source<enum_VisualShaderNodeTexture_Source>` **SOURCE\_2D\_TEXTURE** =
`2`

Use the texture from this shader's texture built-in (e.g. a texture of a
`Sprite2D<class_Sprite2D>`).

classref-enumeration-constant

`Source<enum_VisualShaderNodeTexture_Source>` **SOURCE\_2D\_NORMAL** =
`3`

Use the texture from this shader's normal map built-in.

classref-enumeration-constant

`Source<enum_VisualShaderNodeTexture_Source>` **SOURCE\_DEPTH** = `4`

Use the depth texture captured during the depth prepass. Only available
when the depth prepass is used (i.e. in spatial shaders and in the
forward\_plus or gl\_compatibility renderers).

classref-enumeration-constant

`Source<enum_VisualShaderNodeTexture_Source>` **SOURCE\_PORT** = `5`

Use the texture provided in the input port for this function.

classref-enumeration-constant

`Source<enum_VisualShaderNodeTexture_Source>` **SOURCE\_3D\_NORMAL** =
`6`

Use the normal buffer captured during the depth prepass. Only available
when the normal-roughness buffer is available (i.e. in spatial shaders
and in the forward\_plus renderer).

classref-enumeration-constant

`Source<enum_VisualShaderNodeTexture_Source>` **SOURCE\_ROUGHNESS** =
`7`

Use the roughness buffer captured during the depth prepass. Only
available when the normal-roughness buffer is available (i.e. in spatial
shaders and in the forward\_plus renderer).

classref-enumeration-constant

`Source<enum_VisualShaderNodeTexture_Source>` **SOURCE\_MAX** = `8`

Represents the size of the `Source<enum_VisualShaderNodeTexture_Source>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureType**: `🔗<enum_VisualShaderNodeTexture_TextureType>`

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeTexture_TextureType>` **TYPE\_DATA** =
`0`

No hints are added to the uniform declaration.

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeTexture_TextureType>` **TYPE\_COLOR**
= `1`

Adds `source_color` as hint to the uniform declaration for proper sRGB
to linear conversion.

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeTexture_TextureType>`
**TYPE\_NORMAL\_MAP** = `2`

Adds `hint_normal` as hint to the uniform declaration, which internally
converts the texture for proper usage as normal map.

classref-enumeration-constant

`TextureType<enum_VisualShaderNodeTexture_TextureType>` **TYPE\_MAX** =
`3`

Represents the size of the
`TextureType<enum_VisualShaderNodeTexture_TextureType>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Source<enum_VisualShaderNodeTexture_Source>` **source** = `0`
`🔗<class_VisualShaderNodeTexture_property_source>`

classref-property-setget

-   `void (No return value.)` **set\_source**(value:
    `Source<enum_VisualShaderNodeTexture_Source>`)
-   `Source<enum_VisualShaderNodeTexture_Source>` **get\_source**()

Determines the source for the lookup. See
`Source<enum_VisualShaderNodeTexture_Source>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture**
`🔗<class_VisualShaderNodeTexture_property_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**()

The source texture, if needed for the selected
`source<class_VisualShaderNodeTexture_property_source>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureType<enum_VisualShaderNodeTexture_TextureType>`
**texture\_type** = `0`
`🔗<class_VisualShaderNodeTexture_property_texture_type>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_type**(value:
    `TextureType<enum_VisualShaderNodeTexture_TextureType>`)
-   `TextureType<enum_VisualShaderNodeTexture_TextureType>`
    **get\_texture\_type**()

Specifies the type of the texture if
`source<class_VisualShaderNodeTexture_property_source>` is set to
`SOURCE_TEXTURE<class_VisualShaderNodeTexture_constant_SOURCE_TEXTURE>`.
See `TextureType<enum_VisualShaderNodeTexture_TextureType>` for options.
