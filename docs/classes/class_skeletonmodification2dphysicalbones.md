github\_url  
hide

# SkeletonModification2DPhysicalBones

**Experimental:** Physical bones may be changed in the future to perform
the position update of `Bone2D<class_Bone2D>` on their own, without
needing this resource.

**Inherits:** `SkeletonModification2D<class_SkeletonModification2D>`
**&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A modification that applies the transforms of
`PhysicalBone2D<class_PhysicalBone2D>` nodes to `Bone2D<class_Bone2D>`
nodes.

classref-introduction-group

## Description

This modification takes the transforms of
`PhysicalBone2D<class_PhysicalBone2D>` nodes and applies them to
`Bone2D<class_Bone2D>` nodes. This allows the `Bone2D<class_Bone2D>`
nodes to react to physics thanks to the linked
`PhysicalBone2D<class_PhysicalBone2D>` nodes.

classref-reftable-group

## Properties

<table>
<tbody>
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

`int<class_int>` **physical\_bone\_chain\_length** = `0`
`🔗<class_SkeletonModification2DPhysicalBones_property_physical_bone_chain_length>`

classref-property-setget

-   `void (No return value.)`
    **set\_physical\_bone\_chain\_length**(value: `int<class_int>`)
-   `int<class_int>` **get\_physical\_bone\_chain\_length**()

The number of `PhysicalBone2D<class_PhysicalBone2D>` nodes linked in
this modification.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **fetch\_physical\_bones**()
`🔗<class_SkeletonModification2DPhysicalBones_method_fetch_physical_bones>`

Empties the list of `PhysicalBone2D<class_PhysicalBone2D>` nodes and
populates it with all `PhysicalBone2D<class_PhysicalBone2D>` nodes that
are children of the `Skeleton2D<class_Skeleton2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **get\_physical\_bone\_node**(joint\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DPhysicalBones_method_get_physical_bone_node>`

Returns the `PhysicalBone2D<class_PhysicalBone2D>` node at `joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_physical\_bone\_node**(joint\_idx:
`int<class_int>`, physicalbone2d\_node: `NodePath<class_NodePath>`)
`🔗<class_SkeletonModification2DPhysicalBones_method_set_physical_bone_node>`

Sets the `PhysicalBone2D<class_PhysicalBone2D>` node at `joint_idx`.

\*\*Note:\*\* This is just the index used for this modification, not the
bone index used in the `Skeleton2D<class_Skeleton2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **start\_simulation**(bones:
`Array<class_Array>`\[`StringName<class_StringName>`\] = \[\])
`🔗<class_SkeletonModification2DPhysicalBones_method_start_simulation>`

Tell the `PhysicalBone2D<class_PhysicalBone2D>` nodes to start
simulating and interacting with the physics world.

Optionally, an array of bone names can be passed to this function, and
that will cause only `PhysicalBone2D<class_PhysicalBone2D>` nodes with
those names to start simulating.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop\_simulation**(bones:
`Array<class_Array>`\[`StringName<class_StringName>`\] = \[\])
`🔗<class_SkeletonModification2DPhysicalBones_method_stop_simulation>`

Tell the `PhysicalBone2D<class_PhysicalBone2D>` nodes to stop simulating
and interacting with the physics world.

Optionally, an array of bone names can be passed to this function, and
that will cause only `PhysicalBone2D<class_PhysicalBone2D>` nodes with
those names to stop simulating.
