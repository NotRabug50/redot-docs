github\_url  
hide

# VisualShaderNodeVectorFunc

**Inherits:**
`VisualShaderNodeVectorBase<class_VisualShaderNodeVectorBase>` **&lt;**
`VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A vector function to be used within the visual shader graph.

classref-introduction-group

## Description

A visual shader node able to perform different functions using vectors.

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

enum **Function**: `🔗<enum_VisualShaderNodeVectorFunc_Function>`

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_NORMALIZE**
= `0`

Normalizes the vector so that it has a length of `1` but points in the
same direction.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_SATURATE**
= `1`

Clamps the value between `0.0` and `1.0`.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_NEGATE** =
`2`

Returns the opposite value of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>`
**FUNC\_RECIPROCAL** = `3`

Returns `1/vector`.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_ABS** = `4`

Returns the absolute value of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_ACOS** =
`5`

Returns the arc-cosine of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_ACOSH** =
`6`

Returns the inverse hyperbolic cosine of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_ASIN** =
`7`

Returns the arc-sine of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_ASINH** =
`8`

Returns the inverse hyperbolic sine of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_ATAN** =
`9`

Returns the arc-tangent of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_ATANH** =
`10`

Returns the inverse hyperbolic tangent of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_CEIL** =
`11`

Finds the nearest integer that is greater than or equal to the
parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_COS** =
`12`

Returns the cosine of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_COSH** =
`13`

Returns the hyperbolic cosine of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_DEGREES** =
`14`

Converts a quantity in radians to degrees.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_EXP** =
`15`

Base-e Exponential.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_EXP2** =
`16`

Base-2 Exponential.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_FLOOR** =
`17`

Finds the nearest integer less than or equal to the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_FRACT** =
`18`

Computes the fractional part of the argument.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>`
**FUNC\_INVERSE\_SQRT** = `19`

Returns the inverse of the square root of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_LOG** =
`20`

Natural logarithm.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_LOG2** =
`21`

Base-2 logarithm.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_RADIANS** =
`22`

Converts a quantity in degrees to radians.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_ROUND** =
`23`

Finds the nearest integer to the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_ROUNDEVEN**
= `24`

Finds the nearest even integer to the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_SIGN** =
`25`

Extracts the sign of the parameter, i.e. returns `-1` if the parameter
is negative, `1` if it's positive and `0` otherwise.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_SIN** =
`26`

Returns the sine of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_SINH** =
`27`

Returns the hyperbolic sine of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_SQRT** =
`28`

Returns the square root of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_TAN** =
`29`

Returns the tangent of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_TANH** =
`30`

Returns the hyperbolic tangent of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_TRUNC** =
`31`

Returns a value equal to the nearest integer to the parameter whose
absolute value is not larger than the absolute value of the parameter.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_ONEMINUS**
= `32`

Returns `1.0 - vector`.

classref-enumeration-constant

`Function<enum_VisualShaderNodeVectorFunc_Function>` **FUNC\_MAX** =
`33`

Represents the size of the
`Function<enum_VisualShaderNodeVectorFunc_Function>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Function<enum_VisualShaderNodeVectorFunc_Function>` **function** = `0`
`🔗<class_VisualShaderNodeVectorFunc_property_function>`

classref-property-setget

-   `void (No return value.)` **set\_function**(value:
    `Function<enum_VisualShaderNodeVectorFunc_Function>`)
-   `Function<enum_VisualShaderNodeVectorFunc_Function>`
    **get\_function**()

The function to be performed. See
`Function<enum_VisualShaderNodeVectorFunc_Function>` for options.
