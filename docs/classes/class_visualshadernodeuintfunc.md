github\_url  
hide

# VisualShaderNodeUIntFunc

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

An unsigned scalar integer function to be used within the visual shader
graph.

classref-introduction-group

## Description

Accept an unsigned integer scalar (`x`) to the input port and transform
it according to
`function<class_VisualShaderNodeUIntFunc_property_function>`.

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

enum **Function**: `🔗<enum_VisualShaderNodeUIntFunc_Function>`

classref-enumeration-constant

`Function<enum_VisualShaderNodeUIntFunc_Function>` **FUNC\_NEGATE** =
`0`

Negates the `x` using `-(x)`.

classref-enumeration-constant

`Function<enum_VisualShaderNodeUIntFunc_Function>`
**FUNC\_BITWISE\_NOT** = `1`

Returns the result of bitwise `NOT` operation on the integer. Translates
to `~a` in the Godot Shader Language.

classref-enumeration-constant

`Function<enum_VisualShaderNodeUIntFunc_Function>` **FUNC\_MAX** = `2`

Represents the size of the
`Function<enum_VisualShaderNodeUIntFunc_Function>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Function<enum_VisualShaderNodeUIntFunc_Function>` **function** = `0`
`🔗<class_VisualShaderNodeUIntFunc_property_function>`

classref-property-setget

-   `void (No return value.)` **set\_function**(value:
    `Function<enum_VisualShaderNodeUIntFunc_Function>`)
-   `Function<enum_VisualShaderNodeUIntFunc_Function>`
    **get\_function**()

A function to be applied to the scalar. See
`Function<enum_VisualShaderNodeUIntFunc_Function>` for options.
