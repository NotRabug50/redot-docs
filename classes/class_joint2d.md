github\_url  
hide

# Joint2D

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `DampedSpringJoint2D<class_DampedSpringJoint2D>`,
`GrooveJoint2D<class_GrooveJoint2D>`, `PinJoint2D<class_PinJoint2D>`

Abstract base class for all 2D physics joints.

classref-introduction-group

## Description

Abstract base class for all joints in 2D physics. 2D joints bind
together two physics bodies (`node_a<class_Joint2D_property_node_a>` and
`node_b<class_Joint2D_property_node_b>`) and apply a constraint.

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

classref-reftable-group

## Methods

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

`float<class_float>` **bias** = `0.0` `🔗<class_Joint2D_property_bias>`

classref-property-setget

-   `void (No return value.)` **set\_bias**(value: `float<class_float>`)
-   `float<class_float>` **get\_bias**()

When `node_a<class_Joint2D_property_node_a>` and
`node_b<class_Joint2D_property_node_b>` move in different directions the
`bias<class_Joint2D_property_bias>` controls how fast the joint pulls
them back to their original position. The lower the
`bias<class_Joint2D_property_bias>` the more the two bodies can pull on
the joint.

When set to `0`, the default value from
`ProjectSettings.physics/2d/solver/default_constraint_bias<class_ProjectSettings_property_physics/2d/solver/default_constraint_bias>`
is used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disable\_collision** = `true`
`🔗<class_Joint2D_property_disable_collision>`

classref-property-setget

-   `void (No return value.)`
    **set\_exclude\_nodes\_from\_collision**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_exclude\_nodes\_from\_collision**()

If `true`, the two bodies bound together do not collide with each other.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **node\_a** = `NodePath("")`
`🔗<class_Joint2D_property_node_a>`

classref-property-setget

-   `void (No return value.)` **set\_node\_a**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_node\_a**()

Path to the first body (A) attached to the joint. The node must inherit
`PhysicsBody2D<class_PhysicsBody2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **node\_b** = `NodePath("")`
`🔗<class_Joint2D_property_node_b>`

classref-property-setget

-   `void (No return value.)` **set\_node\_b**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_node\_b**()

Path to the second body (B) attached to the joint. The node must inherit
`PhysicsBody2D<class_PhysicsBody2D>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`RID<class_RID>` **get\_rid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Joint2D_method_get_rid>`

Returns the joint's internal `RID<class_RID>` from the
`PhysicsServer2D<class_PhysicsServer2D>`.
