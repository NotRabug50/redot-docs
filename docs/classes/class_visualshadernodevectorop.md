github\_url  
hide

# VisualShaderNodeVectorOp

**Inherits:**
`VisualShaderNodeVectorBase<class_VisualShaderNodeVectorBase>` **&lt;**
`VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A vector operator to be used within the visual shader graph.

classref-introduction-group

## Description

A visual shader node for use of vector operators. Operates on vector `a`
and vector `b`.

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

enum **Operator**: `🔗<enum_VisualShaderNodeVectorOp_Operator>`

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_ADD** = `0`

Adds two vectors.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_SUB** = `1`

Subtracts a vector from a vector.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_MUL** = `2`

Multiplies two vectors.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_DIV** = `3`

Divides vector by vector.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_MOD** = `4`

Returns the remainder of the two vectors.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_POW** = `5`

Returns the value of the first parameter raised to the power of the
second, for each component of the vectors.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_MAX** = `6`

Returns the greater of two values, for each component of the vectors.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_MIN** = `7`

Returns the lesser of two values, for each component of the vectors.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_CROSS** = `8`

Calculates the cross product of two vectors.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_ATAN2** = `9`

Returns the arc-tangent of the parameters.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_REFLECT** =
`10`

Returns the vector that points in the direction of reflection. `a` is
incident vector and `b` is the normal vector.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_STEP** = `11`

Vector step operator. Returns `0.0` if `a` is smaller than `b` and `1.0`
otherwise.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **OP\_ENUM\_SIZE** =
`12`

Represents the size of the
`Operator<enum_VisualShaderNodeVectorOp_Operator>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Operator<enum_VisualShaderNodeVectorOp_Operator>` **operator** = `0`
`🔗<class_VisualShaderNodeVectorOp_property_operator>`

classref-property-setget

-   `void (No return value.)` **set\_operator**(value:
    `Operator<enum_VisualShaderNodeVectorOp_Operator>`)
-   `Operator<enum_VisualShaderNodeVectorOp_Operator>`
    **get\_operator**()

The operator to be used. See
`Operator<enum_VisualShaderNodeVectorOp_Operator>` for options.
