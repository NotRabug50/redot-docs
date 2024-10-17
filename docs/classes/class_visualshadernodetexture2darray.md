github\_url  
hide

# VisualShaderNodeTexture2DArray

**Inherits:** `VisualShaderNodeSample3D<class_VisualShaderNodeSample3D>`
**&lt;** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A 2D texture uniform array to be used within the visual shader graph.

classref-introduction-group

## Description

Translated to `uniform sampler2DArray` in the shader language.

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`TextureLayered<class_TextureLayered>` **texture\_array**
`🔗<class_VisualShaderNodeTexture2DArray_property_texture_array>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_array**(value:
    `TextureLayered<class_TextureLayered>`)
-   `TextureLayered<class_TextureLayered>` **get\_texture\_array**()

A source texture array. Used if
`VisualShaderNodeSample3D.source<class_VisualShaderNodeSample3D_property_source>`
is set to
`VisualShaderNodeSample3D.SOURCE_TEXTURE<class_VisualShaderNodeSample3D_constant_SOURCE_TEXTURE>`.
