github\_url  
hide

# PhysicalBoneSimulator3D

**Inherits:** `SkeletonModifier3D<class_SkeletonModifier3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Node that can be the parent of `PhysicalBone3D<class_PhysicalBone3D>`
and can apply the simulation results to `Skeleton3D<class_Skeleton3D>`.

classref-introduction-group

## Description

Node that can be the parent of `PhysicalBone3D<class_PhysicalBone3D>`
and can apply the simulation results to `Skeleton3D<class_Skeleton3D>`.

classref-reftable-group

## Methods

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **is\_simulating\_physics**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicalBoneSimulator3D_method_is_simulating_physics>`

Returns a boolean that indicates whether the **PhysicalBoneSimulator3D**
is running and simulating.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**physical\_bones\_add\_collision\_exception**(exception:
`RID<class_RID>`)
`🔗<class_PhysicalBoneSimulator3D_method_physical_bones_add_collision_exception>`

Adds a collision exception to the physical bone.

Works just like the `RigidBody3D<class_RigidBody3D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**physical\_bones\_remove\_collision\_exception**(exception:
`RID<class_RID>`)
`🔗<class_PhysicalBoneSimulator3D_method_physical_bones_remove_collision_exception>`

Removes a collision exception to the physical bone.

Works just like the `RigidBody3D<class_RigidBody3D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **physical\_bones\_start\_simulation**(bones:
`Array<class_Array>`\[`StringName<class_StringName>`\] = \[\])
`🔗<class_PhysicalBoneSimulator3D_method_physical_bones_start_simulation>`

Tells the `PhysicalBone3D<class_PhysicalBone3D>` nodes in the Skeleton
to start simulating and reacting to the physics world.

Optionally, a list of bone names can be passed-in, allowing only the
passed-in bones to be simulated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **physical\_bones\_stop\_simulation**()
`🔗<class_PhysicalBoneSimulator3D_method_physical_bones_stop_simulation>`

Tells the `PhysicalBone3D<class_PhysicalBone3D>` nodes in the Skeleton
to stop simulating.
