github\_url  
hide

# VisualShaderNodeRemap

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A visual shader node for remap function.

classref-introduction-group

## Description

Remap will transform the input range into output range, e.g. you can
change a `0..1` value to `-2..2` etc. See
`@GlobalScope.remap<class_@GlobalScope_method_remap>` for more details.

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

enum **OpType**: `🔗<enum_VisualShaderNodeRemap_OpType>`

classref-enumeration-constant

`OpType<enum_VisualShaderNodeRemap_OpType>` **OP\_TYPE\_SCALAR** = `0`

A floating-point scalar type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeRemap_OpType>` **OP\_TYPE\_VECTOR\_2D** =
`1`

A 2D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeRemap_OpType>`
**OP\_TYPE\_VECTOR\_2D\_SCALAR** = `2`

The `value` port uses a 2D vector type, while the `input min`,
`input max`, `output min`, and `output max` ports use a floating-point
scalar type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeRemap_OpType>` **OP\_TYPE\_VECTOR\_3D** =
`3`

A 3D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeRemap_OpType>`
**OP\_TYPE\_VECTOR\_3D\_SCALAR** = `4`

The `value` port uses a 3D vector type, while the `input min`,
`input max`, `output min`, and `output max` ports use a floating-point
scalar type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeRemap_OpType>` **OP\_TYPE\_VECTOR\_4D** =
`5`

A 4D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeRemap_OpType>`
**OP\_TYPE\_VECTOR\_4D\_SCALAR** = `6`

The `value` port uses a 4D vector type, while the `input min`,
`input max`, `output min`, and `output max` ports use a floating-point
scalar type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeRemap_OpType>` **OP\_TYPE\_MAX** = `7`

Represents the size of the `OpType<enum_VisualShaderNodeRemap_OpType>`
enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`OpType<enum_VisualShaderNodeRemap_OpType>` **op\_type** = `0`
`🔗<class_VisualShaderNodeRemap_property_op_type>`

classref-property-setget

-   `void (No return value.)` **set\_op\_type**(value:
    `OpType<enum_VisualShaderNodeRemap_OpType>`)
-   `OpType<enum_VisualShaderNodeRemap_OpType>` **get\_op\_type**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!
