github\_url  
hide

# VisualShaderNodeFloatFunc

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A scalar floating-point function to be used within the visual shader
graph.

classref-introduction-group

## Description

Accept a floating-point scalar (`x`) to the input port and transform it
according to
`function<class_VisualShaderNodeFloatFunc_property_function>`.

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

enum **Function**: `🔗<enum_VisualShaderNodeFloatFunc_Function>`

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_SIN** = `0`

Returns the sine of the parameter. Translates to `sin(x)` in the Godot
Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_COS** = `1`

Returns the cosine of the parameter. Translates to `cos(x)` in the Godot
Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_TAN** = `2`

Returns the tangent of the parameter. Translates to `tan(x)` in the
Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_ASIN** = `3`

Returns the arc-sine of the parameter. Translates to `asin(x)` in the
Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_ACOS** = `4`

Returns the arc-cosine of the parameter. Translates to `acos(x)` in the
Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_ATAN** = `5`

Returns the arc-tangent of the parameter. Translates to `atan(x)` in the
Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_SINH** = `6`

Returns the hyperbolic sine of the parameter. Translates to `sinh(x)` in
the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_COSH** = `7`

Returns the hyperbolic cosine of the parameter. Translates to `cosh(x)`
in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_TANH** = `8`

Returns the hyperbolic tangent of the parameter. Translates to `tanh(x)`
in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_LOG** = `9`

Returns the natural logarithm of the parameter. Translates to `log(x)`
in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_EXP** = `10`

Returns the natural exponentiation of the parameter. Translates to
`exp(x)` in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_SQRT** =
`11`

Returns the square root of the parameter. Translates to `sqrt(x)` in the
Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_ABS** = `12`

Returns the absolute value of the parameter. Translates to `abs(x)` in
the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_SIGN** =
`13`

Extracts the sign of the parameter. Translates to `sign(x)` in the Godot
Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_FLOOR** =
`14`

Finds the nearest integer less than or equal to the parameter.
Translates to `floor(x)` in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_ROUND** =
`15`

Finds the nearest integer to the parameter. Translates to `round(x)` in
the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_CEIL** =
`16`

Finds the nearest integer that is greater than or equal to the
parameter. Translates to `ceil(x)` in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_FRACT** =
`17`

Computes the fractional part of the argument. Translates to `fract(x)`
in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_SATURATE** =
`18`

Clamps the value between `0.0` and `1.0` using `min(max(x, 0.0), 1.0)`.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_NEGATE** =
`19`

Negates the `x` using `-(x)`.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_ACOSH** =
`20`

Returns the arc-hyperbolic-cosine of the parameter. Translates to
`acosh(x)` in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_ASINH** =
`21`

Returns the arc-hyperbolic-sine of the parameter. Translates to
`asinh(x)` in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_ATANH** =
`22`

Returns the arc-hyperbolic-tangent of the parameter. Translates to
`atanh(x)` in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_DEGREES** =
`23`

Convert a quantity in radians to degrees. Translates to `degrees(x)` in
the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_EXP2** =
`24`

Returns 2 raised by the power of the parameter. Translates to `exp2(x)`
in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>`
**FUNC\_INVERSE\_SQRT** = `25`

Returns the inverse of the square root of the parameter. Translates to
`inversesqrt(x)` in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_LOG2** =
`26`

Returns the base 2 logarithm of the parameter. Translates to `log2(x)`
in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_RADIANS** =
`27`

Convert a quantity in degrees to radians. Translates to `radians(x)` in
the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_RECIPROCAL**
= `28`

Finds reciprocal value of dividing 1 by `x` (i.e. `1 / x`).

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_ROUNDEVEN**
= `29`

Finds the nearest even integer to the parameter. Translates to
`roundEven(x)` in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_TRUNC** =
`30`

Returns a value equal to the nearest integer to `x` whose absolute value
is not larger than the absolute value of `x`. Translates to `trunc(x)`
in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_ONEMINUS** =
`31`

Subtracts scalar `x` from 1 (i.e. `1 - x`).

classref-enumeration-constant

`Function<enum_VisualShaderNodeFloatFunc_Function>` **FUNC\_MAX** = `32`

Represents the size of the
`Function<enum_VisualShaderNodeFloatFunc_Function>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Function<enum_VisualShaderNodeFloatFunc_Function>` **function** = `13`
`🔗<class_VisualShaderNodeFloatFunc_property_function>`

classref-property-setget

-   `void (No return value.)` **set\_function**(value:
    `Function<enum_VisualShaderNodeFloatFunc_Function>`)
-   `Function<enum_VisualShaderNodeFloatFunc_Function>`
    **get\_function**()

A function to be applied to the scalar. See
`Function<enum_VisualShaderNodeFloatFunc_Function>` for options.
