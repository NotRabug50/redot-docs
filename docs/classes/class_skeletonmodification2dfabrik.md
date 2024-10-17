github\_url  
hide

# SkeletonModification2DFABRIK

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `SkeletonModification2D<class_SkeletonModification2D>`
**&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A modification that uses FABRIK to manipulate a series of
`Bone2D<class_Bone2D>` nodes to reach a target.

classref-introduction-group

## Description

This `SkeletonModification2D<class_SkeletonModification2D>` uses an
algorithm called Forward And Backward Reaching Inverse Kinematics, or
FABRIK, to rotate a bone chain so that it reaches a target.

FABRIK works by knowing the positions and lengths of a series of bones,
typically called a "bone chain". It first starts by running a forward
pass, which places the final bone at the target's position. Then all
other bones are moved towards the tip bone, so they stay at the defined
bone length away. Then a backwards pass is performed, where the
root/first bone in the FABRIK chain is placed back at the origin. Then
all other bones are moved so they stay at the defined bone length away.
This positions the bone chain so that it reaches the target when
possible, but all of the bones stay the correct length away from each
other.

Because of how FABRIK works, it often gives more natural results than
those seen in
`SkeletonModification2DCCDIK<class_SkeletonModification2DCCDIK>`. FABRIK
also supports angle constraints, which are fully taken into account when
solving.

\*\*Note:\*\* The FABRIK modifier has `fabrik_joints`, which are the
data objects that hold the data for each joint in the FABRIK chain. This
is different from `Bone2D<class_Bone2D>` nodes! FABRIK joints hold the
data needed for each `Bone2D<class_Bone2D>` in the bone chain used by
FABRIK.

To help control how the FABRIK joints move, a magnet vector can be
passed, which can nudge the bones in a certain direction prior to
solving, giving a level of control over the final result.

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

`int<class_int>` **fabrik\_data\_chain\_length** = `0`
`🔗<class_SkeletonModification2DFABRIK_property_fabrik_data_chain_length>`

classref-property-setget

-   `void (No return value.)`
    **set\_fabrik\_data\_chain\_length**(value: `int<class_int>`)
-   `int<class_int>` **get\_fabrik\_data\_chain\_length**()

The number of FABRIK joints in the FABRIK modification.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **target\_nodepath** = `NodePath("")`
`🔗<class_SkeletonModification2DFABRIK_property_target_nodepath>`

classref-property-setget

-   `void (No return value.)` **set\_target\_node**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_target\_node**()

The NodePath to the node that is the target for the FABRIK modification.
This node is what the FABRIK chain will attempt to rotate the bone chain
to.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`NodePath<class_NodePath>`
**get\_fabrik\_joint\_bone2d\_node**(joint\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DFABRIK_method_get_fabrik_joint_bone2d_node>`

Returns the `Bone2D<class_Bone2D>` node assigned to the FABRIK joint at
`joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_fabrik\_joint\_bone\_index**(joint\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DFABRIK_method_get_fabrik_joint_bone_index>`

Returns the index of the `Bone2D<class_Bone2D>` node assigned to the
FABRIK joint at `joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**get\_fabrik\_joint\_magnet\_position**(joint\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DFABRIK_method_get_fabrik_joint_magnet_position>`

Returns the magnet position vector for the joint at `joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**get\_fabrik\_joint\_use\_target\_rotation**(joint\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DFABRIK_method_get_fabrik_joint_use_target_rotation>`

Returns whether the joint is using the target's rotation rather than
allowing FABRIK to rotate the joint. This option only applies to the
tip/final joint in the chain.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_fabrik\_joint\_bone2d\_node**(joint\_idx: `int<class_int>`,
bone2d\_nodepath: `NodePath<class_NodePath>`)
`🔗<class_SkeletonModification2DFABRIK_method_set_fabrik_joint_bone2d_node>`

Sets the `Bone2D<class_Bone2D>` node assigned to the FABRIK joint at
`joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_fabrik\_joint\_bone\_index**(joint\_idx: `int<class_int>`,
bone\_idx: `int<class_int>`)
`🔗<class_SkeletonModification2DFABRIK_method_set_fabrik_joint_bone_index>`

Sets the bone index, `bone_idx`, of the FABRIK joint at `joint_idx`.
When possible, this will also update the `bone2d_node` of the FABRIK
joint based on data provided by the linked skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_fabrik\_joint\_magnet\_position**(joint\_idx: `int<class_int>`,
magnet\_position: `Vector2<class_Vector2>`)
`🔗<class_SkeletonModification2DFABRIK_method_set_fabrik_joint_magnet_position>`

Sets the magnet position vector for the joint at `joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_fabrik\_joint\_use\_target\_rotation**(joint\_idx:
`int<class_int>`, use\_target\_rotation: `bool<class_bool>`)
`🔗<class_SkeletonModification2DFABRIK_method_set_fabrik_joint_use_target_rotation>`

Sets whether the joint at `joint_idx` will use the target node's
rotation rather than letting FABRIK rotate the node.

\*\*Note:\*\* This option only works for the tip/final joint in the
chain. For all other nodes, this option will be ignored.
