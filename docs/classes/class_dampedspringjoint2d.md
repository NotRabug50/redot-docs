github\_url  
hide

# DampedSpringJoint2D

**Inherits:** `Joint2D<class_Joint2D>` **&lt;** `Node2D<class_Node2D>`
**&lt;** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A physics joint that connects two 2D physics bodies with a spring-like
force.

classref-introduction-group

## Description

A physics joint that connects two 2D physics bodies with a spring-like
force. This resembles a spring that always wants to stretch to a given
length.

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **damping** = `1.0`
`🔗<class_DampedSpringJoint2D_property_damping>`

classref-property-setget

-   `void (No return value.)` **set\_damping**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_damping**()

The spring joint's damping ratio. A value between `0` and `1`. When the
two bodies move into different directions the system tries to align them
to the spring axis again. A high
`damping<class_DampedSpringJoint2D_property_damping>` value forces the
attached bodies to align faster.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **length** = `50.0`
`🔗<class_DampedSpringJoint2D_property_length>`

classref-property-setget

-   `void (No return value.)` **set\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_length**()

The spring joint's maximum length. The two attached bodies cannot
stretch it past this value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **rest\_length** = `0.0`
`🔗<class_DampedSpringJoint2D_property_rest_length>`

classref-property-setget

-   `void (No return value.)` **set\_rest\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_rest\_length**()

When the bodies attached to the spring joint move they stretch or squash
it. The joint always tries to resize towards this length.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **stiffness** = `20.0`
`🔗<class_DampedSpringJoint2D_property_stiffness>`

classref-property-setget

-   `void (No return value.)` **set\_stiffness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_stiffness**()

The higher the value, the less the bodies attached to the joint will
deform it. The joint applies an opposing force to the bodies, the
product of the stiffness multiplied by the size difference from its
resting length.
