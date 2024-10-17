github\_url  
hide

# VisualShaderNodeSwitch

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A selector function for use within the visual shader graph.

classref-introduction-group

## Description

Returns an associated value of the
`op_type<class_VisualShaderNodeSwitch_property_op_type>` type if the
provided boolean value is `true` or `false`.

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

enum **OpType**: `🔗<enum_VisualShaderNodeSwitch_OpType>`

classref-enumeration-constant

`OpType<enum_VisualShaderNodeSwitch_OpType>` **OP\_TYPE\_FLOAT** = `0`

A floating-point scalar.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeSwitch_OpType>` **OP\_TYPE\_INT** = `1`

An integer scalar.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeSwitch_OpType>` **OP\_TYPE\_UINT** = `2`

An unsigned integer scalar.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeSwitch_OpType>` **OP\_TYPE\_VECTOR\_2D** =
`3`

A 2D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeSwitch_OpType>` **OP\_TYPE\_VECTOR\_3D** =
`4`

A 3D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeSwitch_OpType>` **OP\_TYPE\_VECTOR\_4D** =
`5`

A 4D vector type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeSwitch_OpType>` **OP\_TYPE\_BOOLEAN** = `6`

A boolean type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeSwitch_OpType>` **OP\_TYPE\_TRANSFORM** =
`7`

A transform type.

classref-enumeration-constant

`OpType<enum_VisualShaderNodeSwitch_OpType>` **OP\_TYPE\_MAX** = `8`

Represents the size of the `OpType<enum_VisualShaderNodeSwitch_OpType>`
enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`OpType<enum_VisualShaderNodeSwitch_OpType>` **op\_type** = `0`
`🔗<class_VisualShaderNodeSwitch_property_op_type>`

classref-property-setget

-   `void (No return value.)` **set\_op\_type**(value:
    `OpType<enum_VisualShaderNodeSwitch_OpType>`)
-   `OpType<enum_VisualShaderNodeSwitch_OpType>` **get\_op\_type**()

A type of operands and returned value.
