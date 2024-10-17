github\_url  
hide

# SkeletonModification2DTwoBoneIK

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `SkeletonModification2D<class_SkeletonModification2D>`
**&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A modification that rotates two bones using the law of cosines to reach
the target.

classref-introduction-group

## Description

This `SkeletonModification2D<class_SkeletonModification2D>` uses an
algorithm typically called TwoBoneIK. This algorithm works by leveraging
the law of cosines and the lengths of the bones to figure out what
rotation the bones currently have, and what rotation they need to make a
complete triangle, where the first bone, the second bone, and the target
form the three vertices of the triangle. Because the algorithm works by
making a triangle, it can only operate on two bones.

TwoBoneIK is great for arms, legs, and really any joints that can be
represented by just two bones that bend to reach a target. This solver
is more lightweight than
`SkeletonModification2DFABRIK<class_SkeletonModification2DFABRIK>`, but
gives similar, natural looking results.

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

`bool<class_bool>` **flip\_bend\_direction** = `false`
`🔗<class_SkeletonModification2DTwoBoneIK_property_flip_bend_direction>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_bend\_direction**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_flip\_bend\_direction**()

If `true`, the bones in the modification will blend outward as opposed
to inwards when contracting. If `false`, the bones will bend inwards
when contracting.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **target\_maximum\_distance** = `0.0`
`🔗<class_SkeletonModification2DTwoBoneIK_property_target_maximum_distance>`

classref-property-setget

-   `void (No return value.)` **set\_target\_maximum\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_target\_maximum\_distance**()

The maximum distance the target can be at. If the target is farther than
this distance, the modification will solve as if it's at this maximum
distance. When set to `0`, the modification will solve without distance
constraints.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **target\_minimum\_distance** = `0.0`
`🔗<class_SkeletonModification2DTwoBoneIK_property_target_minimum_distance>`

classref-property-setget

-   `void (No return value.)` **set\_target\_minimum\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_target\_minimum\_distance**()

The minimum distance the target can be at. If the target is closer than
this distance, the modification will solve as if it's at this minimum
distance. When set to `0`, the modification will solve without distance
constraints.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **target\_nodepath** = `NodePath("")`
`🔗<class_SkeletonModification2DTwoBoneIK_property_target_nodepath>`

classref-property-setget

-   `void (No return value.)` **set\_target\_node**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_target\_node**()

The NodePath to the node that is the target for the TwoBoneIK
modification. This node is what the modification will use when bending
the `Bone2D<class_Bone2D>` nodes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`NodePath<class_NodePath>` **get\_joint\_one\_bone2d\_node**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DTwoBoneIK_method_get_joint_one_bone2d_node>`

Returns the `Bone2D<class_Bone2D>` node that is being used as the first
bone in the TwoBoneIK modification.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_joint\_one\_bone\_idx**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DTwoBoneIK_method_get_joint_one_bone_idx>`

Returns the index of the `Bone2D<class_Bone2D>` node that is being used
as the first bone in the TwoBoneIK modification.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **get\_joint\_two\_bone2d\_node**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DTwoBoneIK_method_get_joint_two_bone2d_node>`

Returns the `Bone2D<class_Bone2D>` node that is being used as the second
bone in the TwoBoneIK modification.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_joint\_two\_bone\_idx**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DTwoBoneIK_method_get_joint_two_bone_idx>`

Returns the index of the `Bone2D<class_Bone2D>` node that is being used
as the second bone in the TwoBoneIK modification.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_joint\_one\_bone2d\_node**(bone2d\_node:
`NodePath<class_NodePath>`)
`🔗<class_SkeletonModification2DTwoBoneIK_method_set_joint_one_bone2d_node>`

Sets the `Bone2D<class_Bone2D>` node that is being used as the first
bone in the TwoBoneIK modification.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_joint\_one\_bone\_idx**(bone\_idx:
`int<class_int>`)
`🔗<class_SkeletonModification2DTwoBoneIK_method_set_joint_one_bone_idx>`

Sets the index of the `Bone2D<class_Bone2D>` node that is being used as
the first bone in the TwoBoneIK modification.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_joint\_two\_bone2d\_node**(bone2d\_node:
`NodePath<class_NodePath>`)
`🔗<class_SkeletonModification2DTwoBoneIK_method_set_joint_two_bone2d_node>`

Sets the `Bone2D<class_Bone2D>` node that is being used as the second
bone in the TwoBoneIK modification.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_joint\_two\_bone\_idx**(bone\_idx:
`int<class_int>`)
`🔗<class_SkeletonModification2DTwoBoneIK_method_set_joint_two_bone_idx>`

Sets the index of the `Bone2D<class_Bone2D>` node that is being used as
the second bone in the TwoBoneIK modification.
