github\_url  
hide

# GrooveJoint2D

**Inherits:** `Joint2D<class_Joint2D>` **&lt;** `Node2D<class_Node2D>`
**&lt;** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A physics joint that restricts the movement of two 2D physics bodies to
a fixed axis.

classref-introduction-group

## Description

A physics joint that restricts the movement of two 2D physics bodies to
a fixed axis. For example, a `StaticBody2D<class_StaticBody2D>`
representing a piston base can be attached to a
`RigidBody2D<class_RigidBody2D>` representing the piston head, moving up
and down.

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **initial\_offset** = `25.0`
`🔗<class_GrooveJoint2D_property_initial_offset>`

classref-property-setget

-   `void (No return value.)` **set\_initial\_offset**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_initial\_offset**()

The body B's initial anchor position defined by the joint's origin and a
local offset
`initial_offset<class_GrooveJoint2D_property_initial_offset>` along the
joint's Y axis (along the groove).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **length** = `50.0`
`🔗<class_GrooveJoint2D_property_length>`

classref-property-setget

-   `void (No return value.)` **set\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_length**()

The groove's length. The groove is from the joint's origin towards
`length<class_GrooveJoint2D_property_length>` along the joint's local Y
axis.
