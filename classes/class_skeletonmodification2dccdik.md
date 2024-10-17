github\_url  
hide

# SkeletonModification2DCCDIK

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `SkeletonModification2D<class_SkeletonModification2D>`
**&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A modification that uses CCDIK to manipulate a series of bones to reach
a target in 2D.

classref-introduction-group

## Description

This `SkeletonModification2D<class_SkeletonModification2D>` uses an
algorithm called Cyclic Coordinate Descent Inverse Kinematics, or CCDIK,
to manipulate a chain of bones in a `Skeleton2D<class_Skeleton2D>` so it
reaches a defined target.

CCDIK works by rotating a set of bones, typically called a "bone chain",
on a single axis. Each bone is rotated to face the target from the tip
(by default), which over a chain of bones allow it to rotate properly to
reach the target. Because the bones only rotate on a single axis, CCDIK
*can* look more robotic than other IK solvers.

\*\*Note:\*\* The CCDIK modifier has `ccdik_joints`, which are the data
objects that hold the data for each joint in the CCDIK chain. This is
different from a bone! CCDIK joints hold the data needed for each bone
in the bone chain used by CCDIK.

CCDIK also fully supports angle constraints, allowing for more control
over how a solution is met.

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

`int<class_int>` **ccdik\_data\_chain\_length** = `0`
`🔗<class_SkeletonModification2DCCDIK_property_ccdik_data_chain_length>`

classref-property-setget

-   `void (No return value.)` **set\_ccdik\_data\_chain\_length**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_ccdik\_data\_chain\_length**()

The number of CCDIK joints in the CCDIK modification.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **target\_nodepath** = `NodePath("")`
`🔗<class_SkeletonModification2DCCDIK_property_target_nodepath>`

classref-property-setget

-   `void (No return value.)` **set\_target\_node**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_target\_node**()

The NodePath to the node that is the target for the CCDIK modification.
This node is what the CCDIK chain will attempt to rotate the bone chain
to.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **tip\_nodepath** = `NodePath("")`
`🔗<class_SkeletonModification2DCCDIK_property_tip_nodepath>`

classref-property-setget

-   `void (No return value.)` **set\_tip\_node**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_tip\_node**()

The end position of the CCDIK chain. Typically, this should be a child
of a `Bone2D<class_Bone2D>` node attached to the final
`Bone2D<class_Bone2D>` in the CCDIK chain.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`NodePath<class_NodePath>`
**get\_ccdik\_joint\_bone2d\_node**(joint\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DCCDIK_method_get_ccdik_joint_bone2d_node>`

Returns the `Bone2D<class_Bone2D>` node assigned to the CCDIK joint at
`joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_ccdik\_joint\_bone\_index**(joint\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DCCDIK_method_get_ccdik_joint_bone_index>`

Returns the index of the `Bone2D<class_Bone2D>` node assigned to the
CCDIK joint at `joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**get\_ccdik\_joint\_constraint\_angle\_invert**(joint\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DCCDIK_method_get_ccdik_joint_constraint_angle_invert>`

Returns whether the CCDIK joint at `joint_idx` uses an inverted joint
constraint. See
`set_ccdik_joint_constraint_angle_invert<class_SkeletonModification2DCCDIK_method_set_ccdik_joint_constraint_angle_invert>`
for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>`
**get\_ccdik\_joint\_constraint\_angle\_max**(joint\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DCCDIK_method_get_ccdik_joint_constraint_angle_max>`

Returns the maximum angle constraint for the joint at `joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>`
**get\_ccdik\_joint\_constraint\_angle\_min**(joint\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DCCDIK_method_get_ccdik_joint_constraint_angle_min>`

Returns the minimum angle constraint for the joint at `joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_ccdik\_joint\_enable\_constraint**(joint\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DCCDIK_method_get_ccdik_joint_enable_constraint>`

Returns whether angle constraints on the CCDIK joint at `joint_idx` are
enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**get\_ccdik\_joint\_rotate\_from\_joint**(joint\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DCCDIK_method_get_ccdik_joint_rotate_from_joint>`

Returns whether the joint at `joint_idx` is set to rotate from the
joint, `true`, or to rotate from the tip, `false`. The default is to
rotate from the tip.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_ccdik\_joint\_bone2d\_node**(joint\_idx: `int<class_int>`,
bone2d\_nodepath: `NodePath<class_NodePath>`)
`🔗<class_SkeletonModification2DCCDIK_method_set_ccdik_joint_bone2d_node>`

Sets the `Bone2D<class_Bone2D>` node assigned to the CCDIK joint at
`joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_ccdik\_joint\_bone\_index**(joint\_idx:
`int<class_int>`, bone\_idx: `int<class_int>`)
`🔗<class_SkeletonModification2DCCDIK_method_set_ccdik_joint_bone_index>`

Sets the bone index, `bone_idx`, of the CCDIK joint at `joint_idx`. When
possible, this will also update the `bone2d_node` of the CCDIK joint
based on data provided by the linked skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_ccdik\_joint\_constraint\_angle\_invert**(joint\_idx:
`int<class_int>`, invert: `bool<class_bool>`)
`🔗<class_SkeletonModification2DCCDIK_method_set_ccdik_joint_constraint_angle_invert>`

Sets whether the CCDIK joint at `joint_idx` uses an inverted joint
constraint.

An inverted joint constraint only constraints the CCDIK joint to the
angles *outside of* the inputted minimum and maximum angles. For this
reason, it is referred to as an inverted joint constraint, as it
constraints the joint to the outside of the inputted values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_ccdik\_joint\_constraint\_angle\_max**(joint\_idx:
`int<class_int>`, angle\_max: `float<class_float>`)
`🔗<class_SkeletonModification2DCCDIK_method_set_ccdik_joint_constraint_angle_max>`

Sets the maximum angle constraint for the joint at `joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_ccdik\_joint\_constraint\_angle\_min**(joint\_idx:
`int<class_int>`, angle\_min: `float<class_float>`)
`🔗<class_SkeletonModification2DCCDIK_method_set_ccdik_joint_constraint_angle_min>`

Sets the minimum angle constraint for the joint at `joint_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_ccdik\_joint\_enable\_constraint**(joint\_idx: `int<class_int>`,
enable\_constraint: `bool<class_bool>`)
`🔗<class_SkeletonModification2DCCDIK_method_set_ccdik_joint_enable_constraint>`

Determines whether angle constraints on the CCDIK joint at `joint_idx`
are enabled. When `true`, constraints will be enabled and taken into
account when solving.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_ccdik\_joint\_rotate\_from\_joint**(joint\_idx: `int<class_int>`,
rotate\_from\_joint: `bool<class_bool>`)
`🔗<class_SkeletonModification2DCCDIK_method_set_ccdik_joint_rotate_from_joint>`

Sets whether the joint at `joint_idx` is set to rotate from the joint,
`true`, or to rotate from the tip, `false`.
