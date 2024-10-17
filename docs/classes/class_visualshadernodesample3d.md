github\_url  
hide

# VisualShaderNodeSample3D

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`VisualShaderNodeTexture2DArray<class_VisualShaderNodeTexture2DArray>`,
`VisualShaderNodeTexture3D<class_VisualShaderNodeTexture3D>`

A base node for nodes which samples 3D textures in the visual shader
graph.

classref-introduction-group

## Description

A virtual class, use the descendants instead.

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

## Enumerations

classref-enumeration

enum **Source**: `🔗<enum_VisualShaderNodeSample3D_Source>`

classref-enumeration-constant

`Source<enum_VisualShaderNodeSample3D_Source>` **SOURCE\_TEXTURE** = `0`

Creates internal uniform and provides a way to assign it within node.

classref-enumeration-constant

`Source<enum_VisualShaderNodeSample3D_Source>` **SOURCE\_PORT** = `1`

Use the uniform texture from sampler port.

classref-enumeration-constant

`Source<enum_VisualShaderNodeSample3D_Source>` **SOURCE\_MAX** = `2`

Represents the size of the
`Source<enum_VisualShaderNodeSample3D_Source>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Source<enum_VisualShaderNodeSample3D_Source>` **source** = `0`
`🔗<class_VisualShaderNodeSample3D_property_source>`

classref-property-setget

-   `void (No return value.)` **set\_source**(value:
    `Source<enum_VisualShaderNodeSample3D_Source>`)
-   `Source<enum_VisualShaderNodeSample3D_Source>` **get\_source**()

An input source type.
