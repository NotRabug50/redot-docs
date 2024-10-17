github\_url  
hide

# VisualShaderNodeMultiplyAdd

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Performs a fused multiply-add operation within the visual shader graph.

classref-introduction-group

## Description

Uses three operands to compute `(a * b + c)` expression.

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

enum **OpType**: `🔗<enum_VisualShaderNodeMultiplyAdd_OpType>`

classref-enumeration-constant

`OpType<enum_VisualShaderNodeMultiplyAdd_OpType>` **OP\_TYPE\_SCALAR** =
`0`

A floating-point scalar type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeMultiplyAdd_OpType>`
**OP\_TYPE\_VECTOR\_2D** = `1`

A 2D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeMultiplyAdd_OpType>`
**OP\_TYPE\_VECTOR\_3D** = `2`

A 3D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeMultiplyAdd_OpType>`
**OP\_TYPE\_VECTOR\_4D** = `3`

A 4D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeMultiplyAdd_OpType>` **OP\_TYPE\_MAX** =
`4`

Represents the size of the
`OpType<enum_VisualShaderNodeMultiplyAdd_OpType>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`OpType<enum_VisualShaderNodeMultiplyAdd_OpType>` **op\_type** = `0`
`🔗<class_VisualShaderNodeMultiplyAdd_property_op_type>`

classref-property-setget

-   `void (No return value.)` **set\_op\_type**(value:
    `OpType<enum_VisualShaderNodeMultiplyAdd_OpType>`)
-   `OpType<enum_VisualShaderNodeMultiplyAdd_OpType>`
    **get\_op\_type**()

A type of operands and returned value.
