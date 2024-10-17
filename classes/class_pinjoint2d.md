github\_url  
hide

# PinJoint2D

**Inherits:** `Joint2D<class_Joint2D>` **&lt;** `Node2D<class_Node2D>`
**&lt;** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A physics joint that attaches two 2D physics bodies at a single point,
allowing them to freely rotate.

classref-introduction-group

## Description

A physics joint that attaches two 2D physics bodies at a single point,
allowing them to freely rotate. For example, a
`RigidBody2D<class_RigidBody2D>` can be attached to a
`StaticBody2D<class_StaticBody2D>` to create a pendulum or a seesaw.

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

`bool<class_bool>` **angular\_limit\_enabled** = `false`
`🔗<class_PinJoint2D_property_angular_limit_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_limit\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_angular\_limit\_enabled**()

If `true`, the pin maximum and minimum rotation, defined by
`angular_limit_lower<class_PinJoint2D_property_angular_limit_lower>` and
`angular_limit_upper<class_PinJoint2D_property_angular_limit_upper>` are
applied.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_lower** = `0.0`
`🔗<class_PinJoint2D_property_angular_limit_lower>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_limit\_lower**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_angular\_limit\_lower**()

The minimum rotation. Only active if
`angular_limit_enabled<class_PinJoint2D_property_angular_limit_enabled>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_upper** = `0.0`
`🔗<class_PinJoint2D_property_angular_limit_upper>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_limit\_upper**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_angular\_limit\_upper**()

The maximum rotation. Only active if
`angular_limit_enabled<class_PinJoint2D_property_angular_limit_enabled>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **motor\_enabled** = `false`
`🔗<class_PinJoint2D_property_motor_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_motor\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_motor\_enabled**()

When activated, a motor turns the pin.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **motor\_target\_velocity** = `0.0`
`🔗<class_PinJoint2D_property_motor_target_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_motor\_target\_velocity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_motor\_target\_velocity**()

Target speed for the motor. In radians per second.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **softness** = `0.0`
`🔗<class_PinJoint2D_property_softness>`

classref-property-setget

-   `void (No return value.)` **set\_softness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_softness**()

The higher this value, the more the bond to the pinned partner can flex.
