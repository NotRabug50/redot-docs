github\_url  
hide

# PhysicalBone2D

**Inherits:** `RigidBody2D<class_RigidBody2D>` **&lt;**
`PhysicsBody2D<class_PhysicsBody2D>` **&lt;**
`CollisionObject2D<class_CollisionObject2D>` **&lt;**
`Node2D<class_Node2D>` **&lt;** `CanvasItem<class_CanvasItem>` **&lt;**
`Node<class_Node>` **&lt;** `Object<class_Object>`

A `RigidBody2D<class_RigidBody2D>`-derived node used to make
`Bone2D<class_Bone2D>`s in a `Skeleton2D<class_Skeleton2D>` react to
physics.

classref-introduction-group

## Description

The **PhysicalBone2D** node is a `RigidBody2D<class_RigidBody2D>`-based
node that can be used to make `Bone2D<class_Bone2D>`s in a
`Skeleton2D<class_Skeleton2D>` react to physics.

\*\*Note:\*\* To make the `Bone2D<class_Bone2D>`s visually follow the
**PhysicalBone2D** node, use a
`SkeletonModification2DPhysicalBones<class_SkeletonModification2DPhysicalBones>`
modification on the `Skeleton2D<class_Skeleton2D>` parent.

\*\*Note:\*\* The **PhysicalBone2D** node does not automatically create
a `Joint2D<class_Joint2D>` node to keep **PhysicalBone2D** nodes
together. They must be created manually. For most cases, you want to use
a `PinJoint2D<class_PinJoint2D>` node. The **PhysicalBone2D** node will
automatically configure the `Joint2D<class_Joint2D>` node once it's been
added as a child node.

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

`bool<class_bool>` **auto\_configure\_joint** = `true`
`🔗<class_PhysicalBone2D_property_auto_configure_joint>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_configure\_joint**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_auto\_configure\_joint**()

If `true`, the **PhysicalBone2D** will automatically configure the first
`Joint2D<class_Joint2D>` child node. The automatic configuration is
limited to setting up the node properties and positioning the
`Joint2D<class_Joint2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **bone2d\_index** = `-1`
`🔗<class_PhysicalBone2D_property_bone2d_index>`

classref-property-setget

-   `void (No return value.)` **set\_bone2d\_index**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_bone2d\_index**()

The index of the `Bone2D<class_Bone2D>` that this **PhysicalBone2D**
should simulate.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **bone2d\_nodepath** = `NodePath("")`
`🔗<class_PhysicalBone2D_property_bone2d_nodepath>`

classref-property-setget

-   `void (No return value.)` **set\_bone2d\_nodepath**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_bone2d\_nodepath**()

The `NodePath<class_NodePath>` to the `Bone2D<class_Bone2D>` that this
**PhysicalBone2D** should simulate.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **follow\_bone\_when\_simulating** = `false`
`🔗<class_PhysicalBone2D_property_follow_bone_when_simulating>`

classref-property-setget

-   `void (No return value.)`
    **set\_follow\_bone\_when\_simulating**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_follow\_bone\_when\_simulating**()

If `true`, the **PhysicalBone2D** will keep the transform of the bone it
is bound to when simulating physics.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **simulate\_physics** = `false`
`🔗<class_PhysicalBone2D_property_simulate_physics>`

classref-property-setget

-   `void (No return value.)` **set\_simulate\_physics**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_simulate\_physics**()

If `true`, the **PhysicalBone2D** will start simulating using physics.
If `false`, the **PhysicalBone2D** will follow the transform of the
`Bone2D<class_Bone2D>` node.

\*\*Note:\*\* To have the `Bone2D<class_Bone2D>`s visually follow the
**PhysicalBone2D**, use a
`SkeletonModification2DPhysicalBones<class_SkeletonModification2DPhysicalBones>`
modification on the `Skeleton2D<class_Skeleton2D>` node with the
`Bone2D<class_Bone2D>` nodes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Joint2D<class_Joint2D>` **get\_joint**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicalBone2D_method_get_joint>`

Returns the first `Joint2D<class_Joint2D>` child node, if one exists.
This is mainly a helper function to make it easier to get the
`Joint2D<class_Joint2D>` that the **PhysicalBone2D** is autoconfiguring.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_simulating\_physics**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicalBone2D_method_is_simulating_physics>`

Returns a boolean that indicates whether the **PhysicalBone2D** is
running and simulating using the Godot 2D physics engine. When `true`,
the PhysicalBone2D node is using physics.
