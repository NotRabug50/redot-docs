github\_url  
hide

# VisualShaderNodeVectorBase

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`VisualShaderNodeFaceForward<class_VisualShaderNodeFaceForward>`,
`VisualShaderNodeVectorCompose<class_VisualShaderNodeVectorCompose>`,
`VisualShaderNodeVectorDecompose<class_VisualShaderNodeVectorDecompose>`,
`VisualShaderNodeVectorDistance<class_VisualShaderNodeVectorDistance>`,
`VisualShaderNodeVectorFunc<class_VisualShaderNodeVectorFunc>`,
`VisualShaderNodeVectorLen<class_VisualShaderNodeVectorLen>`,
`VisualShaderNodeVectorOp<class_VisualShaderNodeVectorOp>`,
`VisualShaderNodeVectorRefract<class_VisualShaderNodeVectorRefract>`

A base type for the nodes that perform vector operations within the
visual shader graph.

classref-introduction-group

## Description

This is an abstract class. See the derived types for descriptions of the
possible operations.

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

enum **OpType**: `🔗<enum_VisualShaderNodeVectorBase_OpType>`

classref-enumeration-constant

`OpType<enum_VisualShaderNodeVectorBase_OpType>`
**OP\_TYPE\_VECTOR\_2D** = `0`

A 2D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeVectorBase_OpType>`
**OP\_TYPE\_VECTOR\_3D** = `1`

A 3D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeVectorBase_OpType>`
**OP\_TYPE\_VECTOR\_4D** = `2`

A 4D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeVectorBase_OpType>` **OP\_TYPE\_MAX** = `3`

Represents the size of the
`OpType<enum_VisualShaderNodeVectorBase_OpType>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`OpType<enum_VisualShaderNodeVectorBase_OpType>` **op\_type** = `1`
`🔗<class_VisualShaderNodeVectorBase_property_op_type>`

classref-property-setget

-   `void (No return value.)` **set\_op\_type**(value:
    `OpType<enum_VisualShaderNodeVectorBase_OpType>`)
-   `OpType<enum_VisualShaderNodeVectorBase_OpType>` **get\_op\_type**()

A vector type that this operation is performed on.
