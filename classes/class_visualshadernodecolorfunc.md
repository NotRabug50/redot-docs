github\_url  
hide

# VisualShaderNodeColorFunc

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A `Color<class_Color>` function to be used within the visual shader
graph.

classref-introduction-group

## Description

Accept a `Color<class_Color>` to the input port and transform it
according to
`function<class_VisualShaderNodeColorFunc_property_function>`.

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

enum **Function**: `🔗<enum_VisualShaderNodeColorFunc_Function>`

classref-enumeration-constant

`Function<enum_VisualShaderNodeColorFunc_Function>` **FUNC\_GRAYSCALE**
= `0`

Converts the color to grayscale using the following formula:

    vec3 c = input;
    float max1 = max(c.r, c.g);
    float max2 = max(max1, c.b);
    float max3 = max(max1, max2);
    return vec3(max3, max3, max3);

classref-enumeration-constant

`Function<enum_VisualShaderNodeColorFunc_Function>` **FUNC\_HSV2RGB** =
`1`

Converts HSV vector to RGB equivalent.

classref-enumeration-constant

`Function<enum_VisualShaderNodeColorFunc_Function>` **FUNC\_RGB2HSV** =
`2`

Converts RGB vector to HSV equivalent.

classref-enumeration-constant

`Function<enum_VisualShaderNodeColorFunc_Function>` **FUNC\_SEPIA** =
`3`

Applies sepia tone effect using the following formula:

    vec3 c = input;
    float r = (c.r * 0.393) + (c.g * 0.769) + (c.b * 0.189);
    float g = (c.r * 0.349) + (c.g * 0.686) + (c.b * 0.168);
    float b = (c.r * 0.272) + (c.g * 0.534) + (c.b * 0.131);
    return vec3(r, g, b);

classref-enumeration-constant

`Function<enum_VisualShaderNodeColorFunc_Function>` **FUNC\_MAX** = `4`

Represents the size of the
`Function<enum_VisualShaderNodeColorFunc_Function>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Function<enum_VisualShaderNodeColorFunc_Function>` **function** = `0`
`🔗<class_VisualShaderNodeColorFunc_property_function>`

classref-property-setget

-   `void (No return value.)` **set\_function**(value:
    `Function<enum_VisualShaderNodeColorFunc_Function>`)
-   `Function<enum_VisualShaderNodeColorFunc_Function>`
    **get\_function**()

A function to be applied to the input color. See
`Function<enum_VisualShaderNodeColorFunc_Function>` for options.
