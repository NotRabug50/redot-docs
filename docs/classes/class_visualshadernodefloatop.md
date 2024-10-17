github\_url  
hide

# VisualShaderNodeFloatOp

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A floating-point scalar operator to be used within the visual shader
graph.

classref-introduction-group

## Description

Applies `operator<class_VisualShaderNodeFloatOp_property_operator>` to
two floating-point inputs: `a` and `b`.

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

enum **Operator**: `🔗<enum_VisualShaderNodeFloatOp_Operator>`

classref-enumeration-constant

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **OP\_ADD** = `0`

Sums two numbers using `a + b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **OP\_SUB** = `1`

Subtracts two numbers using `a - b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **OP\_MUL** = `2`

Multiplies two numbers using `a * b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **OP\_DIV** = `3`

Divides two numbers using `a / b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **OP\_MOD** = `4`

Calculates the remainder of two numbers. Translates to `mod(a, b)` in
the Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **OP\_POW** = `5`

Raises the `a` to the power of `b`. Translates to `pow(a, b)` in the
Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **OP\_MAX** = `6`

Returns the greater of two numbers. Translates to `max(a, b)` in the
Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **OP\_MIN** = `7`

Returns the lesser of two numbers. Translates to `min(a, b)` in the
Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **OP\_ATAN2** = `8`

Returns the arc-tangent of the parameters. Translates to `atan(a, b)` in
the Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **OP\_STEP** = `9`

Generates a step function by comparing `b`(x) to `a`(edge). Returns 0.0
if `x` is smaller than `edge` and otherwise 1.0. Translates to
`step(a, b)` in the Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **OP\_ENUM\_SIZE** =
`10`

Represents the size of the
`Operator<enum_VisualShaderNodeFloatOp_Operator>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Operator<enum_VisualShaderNodeFloatOp_Operator>` **operator** = `0`
`🔗<class_VisualShaderNodeFloatOp_property_operator>`

classref-property-setget

-   `void (No return value.)` **set\_operator**(value:
    `Operator<enum_VisualShaderNodeFloatOp_Operator>`)
-   `Operator<enum_VisualShaderNodeFloatOp_Operator>`
    **get\_operator**()

An operator to be applied to the inputs. See
`Operator<enum_VisualShaderNodeFloatOp_Operator>` for options.
