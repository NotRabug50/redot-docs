github\_url  
hide

# VisualShaderNodeStep

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Calculates a Step function within the visual shader graph.

classref-introduction-group

## Description

Translates to `step(edge, x)` in the shader language.

Returns `0.0` if `x` is smaller than `edge` and `1.0` otherwise.

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

enum **OpType**: `🔗<enum_VisualShaderNodeStep_OpType>`

classref-enumeration-constant

`OpType<enum_VisualShaderNodeStep_OpType>` **OP\_TYPE\_SCALAR** = `0`

A floating-point scalar type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeStep_OpType>` **OP\_TYPE\_VECTOR\_2D** =
`1`

A 2D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeStep_OpType>`
**OP\_TYPE\_VECTOR\_2D\_SCALAR** = `2`

The `x` port uses a 2D vector type, while the `edge` port uses a
floating-point scalar type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeStep_OpType>` **OP\_TYPE\_VECTOR\_3D** =
`3`

A 3D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeStep_OpType>`
**OP\_TYPE\_VECTOR\_3D\_SCALAR** = `4`

The `x` port uses a 3D vector type, while the `edge` port uses a
floating-point scalar type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeStep_OpType>` **OP\_TYPE\_VECTOR\_4D** =
`5`

A 4D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeStep_OpType>`
**OP\_TYPE\_VECTOR\_4D\_SCALAR** = `6`

The `a` and `b` ports use a 4D vector type. The `weight` port uses a
scalar type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeStep_OpType>` **OP\_TYPE\_MAX** = `7`

Represents the size of the `OpType<enum_VisualShaderNodeStep_OpType>`
enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`OpType<enum_VisualShaderNodeStep_OpType>` **op\_type** = `0`
`🔗<class_VisualShaderNodeStep_property_op_type>`

classref-property-setget

-   `void (No return value.)` **set\_op\_type**(value:
    `OpType<enum_VisualShaderNodeStep_OpType>`)
-   `OpType<enum_VisualShaderNodeStep_OpType>` **get\_op\_type**()

A type of operands and returned value.
