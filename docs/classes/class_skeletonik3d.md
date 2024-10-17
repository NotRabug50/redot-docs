github\_url  
hide

# SkeletonIK3D

**Deprecated:** This class may be changed or removed in future versions.

**Inherits:** `SkeletonModifier3D<class_SkeletonModifier3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A node used to rotate all bones of a `Skeleton3D<class_Skeleton3D>` bone
chain a way that places the end bone at a desired 3D position.

classref-introduction-group

## Description

SkeletonIK3D is used to rotate all bones of a
`Skeleton3D<class_Skeleton3D>` bone chain a way that places the end bone
at a desired 3D position. A typical scenario for IK in games is to place
a character's feet on the ground or a character's hands on a currently
held object. SkeletonIK uses FabrikInverseKinematic internally to solve
the bone chain and applies the results to the
`Skeleton3D<class_Skeleton3D>` `bones_global_pose_override` property for
all affected bones in the chain. If fully applied, this overwrites any
bone transform from `Animation<class_Animation>`s or bone custom poses
set by users. The applied amount can be controlled with the
`SkeletonModifier3D.influence<class_SkeletonModifier3D_property_influence>`
property.

    # Apply IK effect automatically on every new frame (not the current)
    skeleton_ik_node.start()

    # Apply IK effect only on the current frame
    skeleton_ik_node.start(true)

    # Stop IK effect and reset bones_global_pose_override on Skeleton
    skeleton_ik_node.stop()

    # Apply full IK effect
    skeleton_ik_node.set_influence(1.0)

    # Apply half IK effect
    skeleton_ik_node.set_influence(0.5)

    # Apply zero IK effect (a value at or below 0.01 also removes bones_global_pose_override on Skeleton)
    skeleton_ik_node.set_influence(0.0)

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

`float<class_float>` **interpolation**
`🔗<class_SkeletonIK3D_property_interpolation>`

classref-property-setget

-   `void (No return value.)` **set\_interpolation**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_interpolation**()

**Deprecated:** Use
`SkeletonModifier3D.influence<class_SkeletonModifier3D_property_influence>`
instead.

Interpolation value for how much the IK results are applied to the
current skeleton bone chain. A value of `1.0` will overwrite all
skeleton bone transforms completely while a value of `0.0` will visually
disable the SkeletonIK.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **magnet** = `Vector3(0, 0, 0)`
`🔗<class_SkeletonIK3D_property_magnet>`

classref-property-setget

-   `void (No return value.)` **set\_magnet\_position**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_magnet\_position**()

Secondary target position (first is
`target<class_SkeletonIK3D_property_target>` property or
`target_node<class_SkeletonIK3D_property_target_node>`) for the IK
chain. Use magnet position (pole target) to control the bending of the
IK chain. Only works if the bone chain has more than 2 bones. The middle
chain bone position will be linearly interpolated with the magnet
position.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_iterations** = `10`
`🔗<class_SkeletonIK3D_property_max_iterations>`

classref-property-setget

-   `void (No return value.)` **set\_max\_iterations**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_iterations**()

Number of iteration loops used by the IK solver to produce more accurate
(and elegant) bone chain results.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **min\_distance** = `0.01`
`🔗<class_SkeletonIK3D_property_min_distance>`

classref-property-setget

-   `void (No return value.)` **set\_min\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_min\_distance**()

The minimum distance between bone and goal target. If the distance is
below this value, the IK solver stops further iterations.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **override\_tip\_basis** = `true`
`🔗<class_SkeletonIK3D_property_override_tip_basis>`

classref-property-setget

-   `void (No return value.)` **set\_override\_tip\_basis**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_override\_tip\_basis**()

If `true` overwrites the rotation of the tip bone with the rotation of
the `target<class_SkeletonIK3D_property_target>` (or
`target_node<class_SkeletonIK3D_property_target_node>` if defined).

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **root\_bone** = `&""`
`🔗<class_SkeletonIK3D_property_root_bone>`

classref-property-setget

-   `void (No return value.)` **set\_root\_bone**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_root\_bone**()

The name of the current root bone, the first bone in the IK chain.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform3D<class_Transform3D>` **target** =
`Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0)`
`🔗<class_SkeletonIK3D_property_target>`

classref-property-setget

-   `void (No return value.)` **set\_target\_transform**(value:
    `Transform3D<class_Transform3D>`)
-   `Transform3D<class_Transform3D>` **get\_target\_transform**()

First target of the IK chain where the tip bone is placed and, if
`override_tip_basis<class_SkeletonIK3D_property_override_tip_basis>` is
`true`, how the tip bone is rotated. If a
`target_node<class_SkeletonIK3D_property_target_node>` path is available
the nodes transform is used instead and this property is ignored.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **target\_node** = `NodePath("")`
`🔗<class_SkeletonIK3D_property_target_node>`

classref-property-setget

-   `void (No return value.)` **set\_target\_node**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_target\_node**()

Target node `NodePath<class_NodePath>` for the IK chain. If available,
the node's current `Transform3D<class_Transform3D>` is used instead of
the `target<class_SkeletonIK3D_property_target>` property.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **tip\_bone** = `&""`
`🔗<class_SkeletonIK3D_property_tip_bone>`

classref-property-setget

-   `void (No return value.)` **set\_tip\_bone**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_tip\_bone**()

The name of the current tip bone, the last bone in the IK chain placed
at the `target<class_SkeletonIK3D_property_target>` transform (or
`target_node<class_SkeletonIK3D_property_target_node>` if defined).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_magnet** = `false`
`🔗<class_SkeletonIK3D_property_use_magnet>`

classref-property-setget

-   `void (No return value.)` **set\_use\_magnet**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_magnet**()

If `true`, instructs the IK solver to consider the secondary magnet
target (pole target) when calculating the bone chain. Use the magnet
position (pole target) to control the bending of the IK chain.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Skeleton3D<class_Skeleton3D>` **get\_parent\_skeleton**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonIK3D_method_get_parent_skeleton>`

Returns the parent `Skeleton3D<class_Skeleton3D>` Node that was present
when SkeletonIK entered the `SceneTree<class_SceneTree>`. Returns null
if the parent node was not a `Skeleton3D<class_Skeleton3D>` Node when
SkeletonIK3D entered the `SceneTree<class_SceneTree>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_running**()
`🔗<class_SkeletonIK3D_method_is_running>`

Returns `true` if SkeletonIK is applying IK effects on continues frames
to the `Skeleton3D<class_Skeleton3D>` bones. Returns `false` if
SkeletonIK is stopped or `start<class_SkeletonIK3D_method_start>` was
used with the `one_time` parameter set to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **start**(one\_time: `bool<class_bool>` =
false) `🔗<class_SkeletonIK3D_method_start>`

Starts applying IK effects on each frame to the
`Skeleton3D<class_Skeleton3D>` bones but will only take effect starting
on the next frame. If `one_time` is `true`, this will take effect
immediately but also reset on the next frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop**()
`🔗<class_SkeletonIK3D_method_stop>`

Stops applying IK effects on each frame to the
`Skeleton3D<class_Skeleton3D>` bones and also calls
`Skeleton3D.clear_bones_global_pose_override<class_Skeleton3D_method_clear_bones_global_pose_override>`
to remove existing overrides on all bones.
