github\_url  
hide

# CollisionShape3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A node that provides a `Shape3D<class_Shape3D>` to a
`CollisionObject3D<class_CollisionObject3D>` parent.

classref-introduction-group

## Description

A node that provides a `Shape3D<class_Shape3D>` to a
`CollisionObject3D<class_CollisionObject3D>` parent and allows to edit
it. This can give a detection shape to an `Area3D<class_Area3D>` or turn
a `PhysicsBody3D<class_PhysicsBody3D>` into a solid object.

\*\*Warning:\*\* A non-uniformly scaled **CollisionShape3D** will likely
not behave as expected. Make sure to keep its scale the same on all axes
and adjust its `shape<class_CollisionShape3D_property_shape>` resource
instead.

classref-introduction-group

## Tutorials

-   `Physics introduction <../tutorials/physics/physics_introduction>`
-   [3D Kinematic Character
    Demo](https://godotengine.org/asset-library/asset/2739)
-   [3D Platformer
    Demo](https://godotengine.org/asset-library/asset/2748)
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)

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

classref-reftable-group

## Methods

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

`bool<class_bool>` **disabled** = `false`
`🔗<class_CollisionShape3D_property_disabled>`

classref-property-setget

-   `void (No return value.)` **set\_disabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_disabled**()

A disabled collision shape has no effect in the world.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Shape3D<class_Shape3D>` **shape**
`🔗<class_CollisionShape3D_property_shape>`

classref-property-setget

-   `void (No return value.)` **set\_shape**(value:
    `Shape3D<class_Shape3D>`)
-   `Shape3D<class_Shape3D>` **get\_shape**()

The actual shape owned by this collision shape.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **make\_convex\_from\_siblings**()
`🔗<class_CollisionShape3D_method_make_convex_from_siblings>`

Sets the collision shape's shape to the addition of all its convexed
`MeshInstance3D<class_MeshInstance3D>` siblings geometry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **resource\_changed**(resource:
`Resource<class_Resource>`)
`🔗<class_CollisionShape3D_method_resource_changed>`

**Deprecated:** Use `Resource.changed<class_Resource_signal_changed>`
instead.

This method does nothing.
