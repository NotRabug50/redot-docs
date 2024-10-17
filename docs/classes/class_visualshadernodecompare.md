github\_url  
hide

# VisualShaderNodeCompare

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A comparison function for common types within the visual shader graph.

classref-introduction-group

## Description

Compares `a` and `b` of
`type<class_VisualShaderNodeCompare_property_type>` by
`function<class_VisualShaderNodeCompare_property_function>`. Returns a
boolean scalar. Translates to `if` instruction in shader code.

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ComparisonType**:
`🔗<enum_VisualShaderNodeCompare_ComparisonType>`

classref-enumeration-constant

`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>`
**CTYPE\_SCALAR** = `0`

A floating-point scalar.

classref-enumeration-constant

`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>`
**CTYPE\_SCALAR\_INT** = `1`

An integer scalar.

classref-enumeration-constant

`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>`
**CTYPE\_SCALAR\_UINT** = `2`

An unsigned integer scalar.

classref-enumeration-constant

`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>`
**CTYPE\_VECTOR\_2D** = `3`

A 2D vector type.

classref-enumeration-constant

`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>`
**CTYPE\_VECTOR\_3D** = `4`

A 3D vector type.

classref-enumeration-constant

`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>`
**CTYPE\_VECTOR\_4D** = `5`

A 4D vector type.

classref-enumeration-constant

`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>`
**CTYPE\_BOOLEAN** = `6`

A boolean type.

classref-enumeration-constant

`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>`
**CTYPE\_TRANSFORM** = `7`

A transform (`mat4`) type.

classref-enumeration-constant

`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>`
**CTYPE\_MAX** = `8`

Represents the size of the
`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Function**: `🔗<enum_VisualShaderNodeCompare_Function>`

classref-enumeration-constant

`Function<enum_VisualShaderNodeCompare_Function>` **FUNC\_EQUAL** = `0`

Comparison for equality (`a == b`).

classref-enumeration-constant

`Function<enum_VisualShaderNodeCompare_Function>` **FUNC\_NOT\_EQUAL** =
`1`

Comparison for inequality (`a != b`).

classref-enumeration-constant

`Function<enum_VisualShaderNodeCompare_Function>`
**FUNC\_GREATER\_THAN** = `2`

Comparison for greater than (`a > b`). Cannot be used if
`type<class_VisualShaderNodeCompare_property_type>` set to
`CTYPE_BOOLEAN<class_VisualShaderNodeCompare_constant_CTYPE_BOOLEAN>` or
`CTYPE_TRANSFORM<class_VisualShaderNodeCompare_constant_CTYPE_TRANSFORM>`.

classref-enumeration-constant

`Function<enum_VisualShaderNodeCompare_Function>`
**FUNC\_GREATER\_THAN\_EQUAL** = `3`

Comparison for greater than or equal (`a >= b`). Cannot be used if
`type<class_VisualShaderNodeCompare_property_type>` set to
`CTYPE_BOOLEAN<class_VisualShaderNodeCompare_constant_CTYPE_BOOLEAN>` or
`CTYPE_TRANSFORM<class_VisualShaderNodeCompare_constant_CTYPE_TRANSFORM>`.

classref-enumeration-constant

`Function<enum_VisualShaderNodeCompare_Function>` **FUNC\_LESS\_THAN** =
`4`

Comparison for less than (`a < b`). Cannot be used if
`type<class_VisualShaderNodeCompare_property_type>` set to
`CTYPE_BOOLEAN<class_VisualShaderNodeCompare_constant_CTYPE_BOOLEAN>` or
`CTYPE_TRANSFORM<class_VisualShaderNodeCompare_constant_CTYPE_TRANSFORM>`.

classref-enumeration-constant

`Function<enum_VisualShaderNodeCompare_Function>`
**FUNC\_LESS\_THAN\_EQUAL** = `5`

Comparison for less than or equal (`a <= b`). Cannot be used if
`type<class_VisualShaderNodeCompare_property_type>` set to
`CTYPE_BOOLEAN<class_VisualShaderNodeCompare_constant_CTYPE_BOOLEAN>` or
`CTYPE_TRANSFORM<class_VisualShaderNodeCompare_constant_CTYPE_TRANSFORM>`.

classref-enumeration-constant

`Function<enum_VisualShaderNodeCompare_Function>` **FUNC\_MAX** = `6`

Represents the size of the
`Function<enum_VisualShaderNodeCompare_Function>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Condition**: `🔗<enum_VisualShaderNodeCompare_Condition>`

classref-enumeration-constant

`Condition<enum_VisualShaderNodeCompare_Condition>` **COND\_ALL** = `0`

The result will be true if all of component in vector satisfy the
comparison condition.

classref-enumeration-constant

`Condition<enum_VisualShaderNodeCompare_Condition>` **COND\_ANY** = `1`

The result will be true if any of component in vector satisfy the
comparison condition.

classref-enumeration-constant

`Condition<enum_VisualShaderNodeCompare_Condition>` **COND\_MAX** = `2`

Represents the size of the
`Condition<enum_VisualShaderNodeCompare_Condition>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Condition<enum_VisualShaderNodeCompare_Condition>` **condition** = `0`
`🔗<class_VisualShaderNodeCompare_property_condition>`

classref-property-setget

-   `void (No return value.)` **set\_condition**(value:
    `Condition<enum_VisualShaderNodeCompare_Condition>`)
-   `Condition<enum_VisualShaderNodeCompare_Condition>`
    **get\_condition**()

Extra condition which is applied if
`type<class_VisualShaderNodeCompare_property_type>` is set to
`CTYPE_VECTOR_3D<class_VisualShaderNodeCompare_constant_CTYPE_VECTOR_3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Function<enum_VisualShaderNodeCompare_Function>` **function** = `0`
`🔗<class_VisualShaderNodeCompare_property_function>`

classref-property-setget

-   `void (No return value.)` **set\_function**(value:
    `Function<enum_VisualShaderNodeCompare_Function>`)
-   `Function<enum_VisualShaderNodeCompare_Function>`
    **get\_function**()

A comparison function. See
`Function<enum_VisualShaderNodeCompare_Function>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>` **type** =
`0` `🔗<class_VisualShaderNodeCompare_property_type>`

classref-property-setget

-   `void (No return value.)` **set\_comparison\_type**(value:
    `ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>`)
-   `ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>`
    **get\_comparison\_type**()

The type to be used in the comparison. See
`ComparisonType<enum_VisualShaderNodeCompare_ComparisonType>` for
options.
