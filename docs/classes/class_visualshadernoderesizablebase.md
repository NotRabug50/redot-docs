github\_url  
hide

# VisualShaderNodeResizableBase

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`VisualShaderNodeCurveTexture<class_VisualShaderNodeCurveTexture>`,
`VisualShaderNodeCurveXYZTexture<class_VisualShaderNodeCurveXYZTexture>`,
`VisualShaderNodeFrame<class_VisualShaderNodeFrame>`,
`VisualShaderNodeGroupBase<class_VisualShaderNodeGroupBase>`

Base class for resizable nodes in a visual shader graph.

classref-introduction-group

## Description

Resizable nodes have a handle that allows the user to adjust their size
as needed.

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

`Vector2<class_Vector2>` **size** = `Vector2(0, 0)`
`🔗<class_VisualShaderNodeResizableBase_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_size**()

The size of the node in the visual shader graph.
