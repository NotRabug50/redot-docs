github\_url  
hide

# VisualShaderNodeIntFunc

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A scalar integer function to be used within the visual shader graph.

classref-introduction-group

## Description

Accept an integer scalar (`x`) to the input port and transform it
according to
`function<class_VisualShaderNodeIntFunc_property_function>`.

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

enum **Function**: `🔗<enum_VisualShaderNodeIntFunc_Function>`

classref-enumeration-constant

`Function<enum_VisualShaderNodeIntFunc_Function>` **FUNC\_ABS** = `0`

Returns the absolute value of the parameter. Translates to `abs(x)` in
the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeIntFunc_Function>` **FUNC\_NEGATE** = `1`

Negates the `x` using `-(x)`.

classref-enumeration-constant

`Function<enum_VisualShaderNodeIntFunc_Function>` **FUNC\_SIGN** = `2`

Extracts the sign of the parameter. Translates to `sign(x)` in the Godot
Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeIntFunc_Function>` **FUNC\_BITWISE\_NOT**
= `3`

Returns the result of bitwise `NOT` operation on the integer. Translates
to `~a` in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeIntFunc_Function>` **FUNC\_MAX** = `4`

Represents the size of the
`Function<enum_VisualShaderNodeIntFunc_Function>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Function<enum_VisualShaderNodeIntFunc_Function>` **function** = `2`
`🔗<class_VisualShaderNodeIntFunc_property_function>`

classref-property-setget

-   `void (No return value.)` **set\_function**(value:
    `Function<enum_VisualShaderNodeIntFunc_Function>`)
-   `Function<enum_VisualShaderNodeIntFunc_Function>`
    **get\_function**()

A function to be applied to the scalar. See
`Function<enum_VisualShaderNodeIntFunc_Function>` for options.
