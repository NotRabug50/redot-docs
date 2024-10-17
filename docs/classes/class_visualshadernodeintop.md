github\_url  
hide

# VisualShaderNodeIntOp

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

An integer scalar operator to be used within the visual shader graph.

classref-introduction-group

## Description

Applies `operator<class_VisualShaderNodeIntOp_property_operator>` to two
integer inputs: `a` and `b`.

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

enum **Operator**: `🔗<enum_VisualShaderNodeIntOp_Operator>`

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>` **OP\_ADD** = `0`

Sums two numbers using `a + b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>` **OP\_SUB** = `1`

Subtracts two numbers using `a - b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>` **OP\_MUL** = `2`

Multiplies two numbers using `a * b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>` **OP\_DIV** = `3`

Divides two numbers using `a / b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>` **OP\_MOD** = `4`

Calculates the remainder of two numbers using `a % b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>` **OP\_MAX** = `5`

Returns the greater of two numbers. Translates to `max(a, b)` in the
Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>` **OP\_MIN** = `6`

Returns the lesser of two numbers. Translates to `max(a, b)` in the
Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>` **OP\_BITWISE\_AND** =
`7`

Returns the result of bitwise `AND` operation on the integer. Translates
to `a & b` in the Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>` **OP\_BITWISE\_OR** =
`8`

Returns the result of bitwise `OR` operation for two integers.
Translates to `a | b` in the Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>` **OP\_BITWISE\_XOR** =
`9`

Returns the result of bitwise `XOR` operation for two integers.
Translates to `a ^ b` in the Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>`
**OP\_BITWISE\_LEFT\_SHIFT** = `10`

Returns the result of bitwise left shift operation on the integer.
Translates to `a << b` in the Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>`
**OP\_BITWISE\_RIGHT\_SHIFT** = `11`

Returns the result of bitwise right shift operation on the integer.
Translates to `a >> b` in the Godot Shader Language.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeIntOp_Operator>` **OP\_ENUM\_SIZE** =
`12`

Represents the size of the
`Operator<enum_VisualShaderNodeIntOp_Operator>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Operator<enum_VisualShaderNodeIntOp_Operator>` **operator** = `0`
`🔗<class_VisualShaderNodeIntOp_property_operator>`

classref-property-setget

-   `void (No return value.)` **set\_operator**(value:
    `Operator<enum_VisualShaderNodeIntOp_Operator>`)
-   `Operator<enum_VisualShaderNodeIntOp_Operator>` **get\_operator**()

An operator to be applied to the inputs. See
`Operator<enum_VisualShaderNodeIntOp_Operator>` for options.
