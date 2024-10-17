github\_url  
hide

# VisualShaderNodeIs

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A boolean comparison operator to be used within the visual shader graph.

classref-introduction-group

## Description

Returns the boolean result of the comparison between `INF` or `NaN` and
a scalar parameter.

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

enum **Function**: `🔗<enum_VisualShaderNodeIs_Function>`

classref-enumeration-constant

`Function<enum_VisualShaderNodeIs_Function>` **FUNC\_IS\_INF** = `0`

Comparison with `INF` (Infinity).

classref-enumeration-constant

`Function<enum_VisualShaderNodeIs_Function>` **FUNC\_IS\_NAN** = `1`

Comparison with `NaN` (Not a Number; indicates invalid numeric results,
such as division by zero).

classref-enumeration-constant

`Function<enum_VisualShaderNodeIs_Function>` **FUNC\_MAX** = `2`

Represents the size of the `Function<enum_VisualShaderNodeIs_Function>`
enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Function<enum_VisualShaderNodeIs_Function>` **function** = `0`
`🔗<class_VisualShaderNodeIs_property_function>`

classref-property-setget

-   `void (No return value.)` **set\_function**(value:
    `Function<enum_VisualShaderNodeIs_Function>`)
-   `Function<enum_VisualShaderNodeIs_Function>` **get\_function**()

The comparison function. See
`Function<enum_VisualShaderNodeIs_Function>` for options.
