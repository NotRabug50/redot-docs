github\_url  
hide

# VisualShaderNodeTransformVecMult

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Multiplies a `Transform3D<class_Transform3D>` and a
`Vector3<class_Vector3>` within the visual shader graph.

classref-introduction-group

## Description

A multiplication operation on a transform (4×4 matrix) and a vector,
with support for different multiplication operators.

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

enum **Operator**: `🔗<enum_VisualShaderNodeTransformVecMult_Operator>`

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformVecMult_Operator>` **OP\_AxB** =
`0`

Multiplies transform `a` by the vector `b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformVecMult_Operator>` **OP\_BxA** =
`1`

Multiplies vector `b` by the transform `a`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformVecMult_Operator>`
**OP\_3x3\_AxB** = `2`

Multiplies transform `a` by the vector `b`, skipping the last row and
column of the transform.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformVecMult_Operator>`
**OP\_3x3\_BxA** = `3`

Multiplies vector `b` by the transform `a`, skipping the last row and
column of the transform.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformVecMult_Operator>` **OP\_MAX** =
`4`

Represents the size of the
`Operator<enum_VisualShaderNodeTransformVecMult_Operator>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Operator<enum_VisualShaderNodeTransformVecMult_Operator>` **operator**
= `0` `🔗<class_VisualShaderNodeTransformVecMult_property_operator>`

classref-property-setget

-   `void (No return value.)` **set\_operator**(value:
    `Operator<enum_VisualShaderNodeTransformVecMult_Operator>`)
-   `Operator<enum_VisualShaderNodeTransformVecMult_Operator>`
    **get\_operator**()

The multiplication type to be performed. See
`Operator<enum_VisualShaderNodeTransformVecMult_Operator>` for options.
