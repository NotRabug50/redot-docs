github\_url  
hide

# VisualShaderNodeExpression

**Inherits:**
`VisualShaderNodeGroupBase<class_VisualShaderNodeGroupBase>` **&lt;**
`VisualShaderNodeResizableBase<class_VisualShaderNodeResizableBase>`
**&lt;** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`VisualShaderNodeGlobalExpression<class_VisualShaderNodeGlobalExpression>`

A custom visual shader graph expression written in Godot Shading
Language.

classref-introduction-group

## Description

Custom Godot Shading Language expression, with a custom number of input
and output ports.

The provided code is directly injected into the graph's matching shader
function (`vertex`, `fragment`, or `light`), so it cannot be used to
declare functions, varyings, uniforms, or global constants. See
`VisualShaderNodeGlobalExpression<class_VisualShaderNodeGlobalExpression>`
for such global definitions.

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

`String<class_String>` **expression** = `""`
`🔗<class_VisualShaderNodeExpression_property_expression>`

classref-property-setget

-   `void (No return value.)` **set\_expression**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_expression**()

An expression in Godot Shading Language, which will be injected at the
start of the graph's matching shader function (`vertex`, `fragment`, or
`light`), and thus cannot be used to declare functions, varyings,
uniforms, or global constants.
