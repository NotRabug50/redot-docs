github\_url  
hide

# Joint3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

**Inherited By:** `ConeTwistJoint3D<class_ConeTwistJoint3D>`,
`Generic6DOFJoint3D<class_Generic6DOFJoint3D>`,
`HingeJoint3D<class_HingeJoint3D>`, `PinJoint3D<class_PinJoint3D>`,
`SliderJoint3D<class_SliderJoint3D>`

Abstract base class for all 3D physics joints.

classref-introduction-group

## Description

Abstract base class for all joints in 3D physics. 3D joints bind
together two physics bodies (`node_a<class_Joint3D_property_node_a>` and
`node_b<class_Joint3D_property_node_b>`) and apply a constraint. If only
one body is defined, it is attached to a fixed
`StaticBody3D<class_StaticBody3D>` without collision shapes.

classref-introduction-group

## Tutorials

-   [3D Truck Town
    Demo](https://godotengine.org/asset-library/asset/2752)

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

`bool<class_bool>` **exclude\_nodes\_from\_collision** = `true`
`🔗<class_Joint3D_property_exclude_nodes_from_collision>`

classref-property-setget

-   `void (No return value.)`
    **set\_exclude\_nodes\_from\_collision**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_exclude\_nodes\_from\_collision**()

If `true`, the two bodies bound together do not collide with each other.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **node\_a** = `NodePath("")`
`🔗<class_Joint3D_property_node_a>`

classref-property-setget

-   `void (No return value.)` **set\_node\_a**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_node\_a**()

Path to the first node (A) attached to the joint. The node must inherit
`PhysicsBody3D<class_PhysicsBody3D>`.

If left empty and `node_b<class_Joint3D_property_node_b>` is set, the
body is attached to a fixed `StaticBody3D<class_StaticBody3D>` without
collision shapes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **node\_b** = `NodePath("")`
`🔗<class_Joint3D_property_node_b>`

classref-property-setget

-   `void (No return value.)` **set\_node\_b**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_node\_b**()

Path to the second node (B) attached to the joint. The node must inherit
`PhysicsBody3D<class_PhysicsBody3D>`.

If left empty and `node_a<class_Joint3D_property_node_a>` is set, the
body is attached to a fixed `StaticBody3D<class_StaticBody3D>` without
collision shapes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **solver\_priority** = `1`
`🔗<class_Joint3D_property_solver_priority>`

classref-property-setget

-   `void (No return value.)` **set\_solver\_priority**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_solver\_priority**()

The priority used to define which solver is executed first for multiple
joints. The lower the value, the higher the priority.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`RID<class_RID>` **get\_rid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Joint3D_method_get_rid>`

Returns the joint's internal `RID<class_RID>` from the
`PhysicsServer3D<class_PhysicsServer3D>`.
