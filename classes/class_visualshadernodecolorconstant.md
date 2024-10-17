github\_url  
hide

# VisualShaderNodeColorConstant

**Inherits:** `VisualShaderNodeConstant<class_VisualShaderNodeConstant>`
**&lt;** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A `Color<class_Color>` constant to be used within the visual shader
graph.

classref-introduction-group

## Description

Has two output ports representing RGB and alpha channels of
`Color<class_Color>`.

Translated to `vec3 rgb` and `float alpha` in the shader language.

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

## Property Descriptions

classref-property

`Color<class_Color>` **constant** = `Color(1, 1, 1, 1)`
`🔗<class_VisualShaderNodeColorConstant_property_constant>`

classref-property-setget

-   `void (No return value.)` **set\_constant**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_constant**()

A `Color<class_Color>` constant which represents a state of this node.
