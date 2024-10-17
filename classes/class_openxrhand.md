github\_url  
hide

# OpenXRHand

**Deprecated:** Use `XRHandModifier3D<class_XRHandModifier3D>` instead.

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

Node supporting hand and finger tracking in OpenXR.

classref-introduction-group

## Description

This node enables OpenXR's hand tracking functionality. The node should
be a child node of an `XROrigin3D<class_XROrigin3D>` node, tracking will
update its position to the player's tracked hand Palm joint location
(the center of the middle finger's metacarpal bone). This node also
updates the skeleton of a properly skinned hand or avatar model.

If the skeleton is a hand (one of the hand bones is the root node of the
skeleton), then the skeleton will be placed relative to the hand palm
location and the hand mesh and skeleton should be children of the
OpenXRHand node.

If the hand bones are part of a full skeleton, then the root of the hand
will keep its location with the assumption that IK is used to position
the hand and arm.

By default the skeleton hand bones are repositioned to match the size of
the tracked hand. To preserve the modeled bone sizes change
`bone_update<class_OpenXRHand_property_bone_update>` to apply rotation
only.

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Hands**: `🔗<enum_OpenXRHand_Hands>`

classref-enumeration-constant

`Hands<enum_OpenXRHand_Hands>` **HAND\_LEFT** = `0`

Tracking the player's left hand.

classref-enumeration-constant

`Hands<enum_OpenXRHand_Hands>` **HAND\_RIGHT** = `1`

Tracking the player's right hand.

classref-enumeration-constant

`Hands<enum_OpenXRHand_Hands>` **HAND\_MAX** = `2`

Maximum supported hands.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **MotionRange**: `🔗<enum_OpenXRHand_MotionRange>`

classref-enumeration-constant

`MotionRange<enum_OpenXRHand_MotionRange>`
**MOTION\_RANGE\_UNOBSTRUCTED** = `0`

When player grips, hand skeleton will form a full fist.

classref-enumeration-constant

`MotionRange<enum_OpenXRHand_MotionRange>`
**MOTION\_RANGE\_CONFORM\_TO\_CONTROLLER** = `1`

When player grips, hand skeleton conforms to the controller the player
is holding.

classref-enumeration-constant

`MotionRange<enum_OpenXRHand_MotionRange>` **MOTION\_RANGE\_MAX** = `2`

Maximum supported motion ranges.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SkeletonRig**: `🔗<enum_OpenXRHand_SkeletonRig>`

classref-enumeration-constant

`SkeletonRig<enum_OpenXRHand_SkeletonRig>` **SKELETON\_RIG\_OPENXR** =
`0`

An OpenXR compliant skeleton.

classref-enumeration-constant

`SkeletonRig<enum_OpenXRHand_SkeletonRig>` **SKELETON\_RIG\_HUMANOID** =
`1`

A `SkeletonProfileHumanoid<class_SkeletonProfileHumanoid>` compliant
skeleton.

classref-enumeration-constant

`SkeletonRig<enum_OpenXRHand_SkeletonRig>` **SKELETON\_RIG\_MAX** = `2`

Maximum supported hands.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BoneUpdate**: `🔗<enum_OpenXRHand_BoneUpdate>`

classref-enumeration-constant

`BoneUpdate<enum_OpenXRHand_BoneUpdate>` **BONE\_UPDATE\_FULL** = `0`

The skeletons bones are fully updated (both position and rotation) to
match the tracked bones.

classref-enumeration-constant

`BoneUpdate<enum_OpenXRHand_BoneUpdate>`
**BONE\_UPDATE\_ROTATION\_ONLY** = `1`

The skeletons bones are only rotated to align with the tracked bones,
preserving bone length.

classref-enumeration-constant

`BoneUpdate<enum_OpenXRHand_BoneUpdate>` **BONE\_UPDATE\_MAX** = `2`

Maximum supported bone update mode.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`BoneUpdate<enum_OpenXRHand_BoneUpdate>` **bone\_update** = `0`
`🔗<class_OpenXRHand_property_bone_update>`

classref-property-setget

-   `void (No return value.)` **set\_bone\_update**(value:
    `BoneUpdate<enum_OpenXRHand_BoneUpdate>`)
-   `BoneUpdate<enum_OpenXRHand_BoneUpdate>` **get\_bone\_update**()

Specify the type of updates to perform on the bone.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Hands<enum_OpenXRHand_Hands>` **hand** = `0`
`🔗<class_OpenXRHand_property_hand>`

classref-property-setget

-   `void (No return value.)` **set\_hand**(value:
    `Hands<enum_OpenXRHand_Hands>`)
-   `Hands<enum_OpenXRHand_Hands>` **get\_hand**()

Specifies whether this node tracks the left or right hand of the player.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **hand\_skeleton** = `NodePath("")`
`🔗<class_OpenXRHand_property_hand_skeleton>`

classref-property-setget

-   `void (No return value.)` **set\_hand\_skeleton**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_hand\_skeleton**()

Set a `Skeleton3D<class_Skeleton3D>` node for which the pose positions
will be updated.

classref-item-separator

------------------------------------------------------------------------

classref-property

`MotionRange<enum_OpenXRHand_MotionRange>` **motion\_range** = `0`
`🔗<class_OpenXRHand_property_motion_range>`

classref-property-setget

-   `void (No return value.)` **set\_motion\_range**(value:
    `MotionRange<enum_OpenXRHand_MotionRange>`)
-   `MotionRange<enum_OpenXRHand_MotionRange>` **get\_motion\_range**()

Set the motion range (if supported) limiting the hand motion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SkeletonRig<enum_OpenXRHand_SkeletonRig>` **skeleton\_rig** = `0`
`🔗<class_OpenXRHand_property_skeleton_rig>`

classref-property-setget

-   `void (No return value.)` **set\_skeleton\_rig**(value:
    `SkeletonRig<enum_OpenXRHand_SkeletonRig>`)
-   `SkeletonRig<enum_OpenXRHand_SkeletonRig>` **get\_skeleton\_rig**()

Set the type of skeleton rig the
`hand_skeleton<class_OpenXRHand_property_hand_skeleton>` is compliant
with.
