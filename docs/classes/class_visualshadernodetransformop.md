github\_url  
hide

# VisualShaderNodeTransformOp

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A `Transform3D<class_Transform3D>` operator to be used within the visual
shader graph.

classref-introduction-group

## Description

Applies `operator<class_VisualShaderNodeTransformOp_property_operator>`
to two transform (4×4 matrices) inputs.

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

enum **Operator**: `🔗<enum_VisualShaderNodeTransformOp_Operator>`

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformOp_Operator>` **OP\_AxB** = `0`

Multiplies transform `a` by the transform `b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformOp_Operator>` **OP\_BxA** = `1`

Multiplies transform `b` by the transform `a`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformOp_Operator>` **OP\_AxB\_COMP**
= `2`

Performs a component-wise multiplication of transform `a` by the
transform `b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformOp_Operator>` **OP\_BxA\_COMP**
= `3`

Performs a component-wise multiplication of transform `b` by the
transform `a`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformOp_Operator>` **OP\_ADD** = `4`

Adds two transforms.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformOp_Operator>`
**OP\_A\_MINUS\_B** = `5`

Subtracts the transform `a` from the transform `b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformOp_Operator>`
**OP\_B\_MINUS\_A** = `6`

Subtracts the transform `b` from the transform `a`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformOp_Operator>` **OP\_A\_DIV\_B**
= `7`

Divides the transform `a` by the transform `b`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformOp_Operator>` **OP\_B\_DIV\_A**
= `8`

Divides the transform `b` by the transform `a`.

classref-enumeration-constant

`Operator<enum_VisualShaderNodeTransformOp_Operator>` **OP\_MAX** = `9`

Represents the size of the
`Operator<enum_VisualShaderNodeTransformOp_Operator>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Operator<enum_VisualShaderNodeTransformOp_Operator>` **operator** = `0`
`🔗<class_VisualShaderNodeTransformOp_property_operator>`

classref-property-setget

-   `void (No return value.)` **set\_operator**(value:
    `Operator<enum_VisualShaderNodeTransformOp_Operator>`)
-   `Operator<enum_VisualShaderNodeTransformOp_Operator>`
    **get\_operator**()

The type of the operation to be performed on the transforms. See
`Operator<enum_VisualShaderNodeTransformOp_Operator>` for options.
