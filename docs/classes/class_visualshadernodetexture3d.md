github\_url  
hide

# VisualShaderNodeTexture3D

**Inherits:** `VisualShaderNodeSample3D<class_VisualShaderNodeSample3D>`
**&lt;** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Performs a 3D texture lookup within the visual shader graph.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Texture3D<class_Texture3D>` **texture**
`🔗<class_VisualShaderNodeTexture3D_property_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(value:
    `Texture3D<class_Texture3D>`)
-   `Texture3D<class_Texture3D>` **get\_texture**()

A source texture. Used if
`VisualShaderNodeSample3D.source<class_VisualShaderNodeSample3D_property_source>`
is set to
`VisualShaderNodeSample3D.SOURCE_TEXTURE<class_VisualShaderNodeSample3D_constant_SOURCE_TEXTURE>`.
