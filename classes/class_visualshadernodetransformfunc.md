github\_url  
hide

# VisualShaderNodeTransformFunc

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Computes a `Transform3D<class_Transform3D>` function within the visual
shader graph.

classref-introduction-group

## Description

Computes an inverse or transpose function on the provided
`Transform3D<class_Transform3D>`.

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

enum **Function**: `🔗<enum_VisualShaderNodeTransformFunc_Function>`

classref-enumeration-constant

`Function<enum_VisualShaderNodeTransformFunc_Function>`
**FUNC\_INVERSE** = `0`

Perform the inverse operation on the `Transform3D<class_Transform3D>`
matrix.

classref-enumeration-constant

`Function<enum_VisualShaderNodeTransformFunc_Function>`
**FUNC\_TRANSPOSE** = `1`

Perform the transpose operation on the `Transform3D<class_Transform3D>`
matrix.

classref-enumeration-constant

`Function<enum_VisualShaderNodeTransformFunc_Function>` **FUNC\_MAX** =
`2`

Represents the size of the
`Function<enum_VisualShaderNodeTransformFunc_Function>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Function<enum_VisualShaderNodeTransformFunc_Function>` **function** =
`0` `🔗<class_VisualShaderNodeTransformFunc_property_function>`

classref-property-setget

-   `void (No return value.)` **set\_function**(value:
    `Function<enum_VisualShaderNodeTransformFunc_Function>`)
-   `Function<enum_VisualShaderNodeTransformFunc_Function>`
    **get\_function**()

The function to be computed. See
`Function<enum_VisualShaderNodeTransformFunc_Function>` for options.
