github\_url  
hide

# Node3D

**Inherits:** `Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `AudioListener3D<class_AudioListener3D>`,
`AudioStreamPlayer3D<class_AudioStreamPlayer3D>`,
`BoneAttachment3D<class_BoneAttachment3D>`, `Camera3D<class_Camera3D>`,
`CollisionObject3D<class_CollisionObject3D>`,
`CollisionPolygon3D<class_CollisionPolygon3D>`,
`CollisionShape3D<class_CollisionShape3D>`, `GridMap<class_GridMap>`,
`ImporterMeshInstance3D<class_ImporterMeshInstance3D>`,
`Joint3D<class_Joint3D>`, `LightmapProbe<class_LightmapProbe>`,
`Marker3D<class_Marker3D>`, `NavigationLink3D<class_NavigationLink3D>`,
`NavigationObstacle3D<class_NavigationObstacle3D>`,
`NavigationRegion3D<class_NavigationRegion3D>`,
`OpenXRCompositionLayer<class_OpenXRCompositionLayer>`,
`OpenXRHand<class_OpenXRHand>`, `Path3D<class_Path3D>`,
`PathFollow3D<class_PathFollow3D>`, `RayCast3D<class_RayCast3D>`,
`RemoteTransform3D<class_RemoteTransform3D>`,
`ShapeCast3D<class_ShapeCast3D>`, `Skeleton3D<class_Skeleton3D>`,
`SkeletonModifier3D<class_SkeletonModifier3D>`,
`SpringArm3D<class_SpringArm3D>`,
`VehicleWheel3D<class_VehicleWheel3D>`,
`VisualInstance3D<class_VisualInstance3D>`,
`XRFaceModifier3D<class_XRFaceModifier3D>`, `XRNode3D<class_XRNode3D>`,
`XROrigin3D<class_XROrigin3D>`

Most basic 3D game object, parent of all 3D-related nodes.

classref-introduction-group

## Description

Most basic 3D game object, with a `Transform3D<class_Transform3D>` and
visibility settings. All other 3D game objects inherit from **Node3D**.
Use **Node3D** as a parent node to move, scale, rotate and show/hide
children in a 3D project.

Affine operations (rotate, scale, translate) happen in parent's local
coordinate system, unless the **Node3D** object is set as top-level.
Affine operations in this coordinate system correspond to direct affine
operations on the **Node3D**'s transform. The word local below refers to
this coordinate system. The coordinate system that is attached to the
**Node3D** object itself is referred to as object-local coordinate
system.

\*\*Note:\*\* Unless otherwise specified, all methods that have angle
parameters must have angles specified as *radians*. To convert degrees
to radians, use
`@GlobalScope.deg_to_rad<class_@GlobalScope_method_deg_to_rad>`.

\*\*Note:\*\* Be aware that "Spatial" nodes are now called "Node3D"
starting with Godot 4. Any Godot 3.x references to "Spatial" nodes refer
to "Node3D" in Godot 4.

classref-introduction-group

## Tutorials

-   `Introduction to 3D <../tutorials/3d/introduction_to_3d>`
-   [All 3D
    Demos](https://github.com/godotengine/godot-demo-projects/tree/master/3d)

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

## Signals

classref-signal

**visibility\_changed**() `🔗<class_Node3D_signal_visibility_changed>`

Emitted when node visibility changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **RotationEditMode**: `🔗<enum_Node3D_RotationEditMode>`

classref-enumeration-constant

`RotationEditMode<enum_Node3D_RotationEditMode>`
**ROTATION\_EDIT\_MODE\_EULER** = `0`

The rotation is edited using `Vector3<class_Vector3>` Euler angles.

classref-enumeration-constant

`RotationEditMode<enum_Node3D_RotationEditMode>`
**ROTATION\_EDIT\_MODE\_QUATERNION** = `1`

The rotation is edited using a `Quaternion<class_Quaternion>`.

classref-enumeration-constant

`RotationEditMode<enum_Node3D_RotationEditMode>`
**ROTATION\_EDIT\_MODE\_BASIS** = `2`

The rotation is edited using a `Basis<class_Basis>`. In this mode,
`scale<class_Node3D_property_scale>` can't be edited separately.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NOTIFICATION\_TRANSFORM\_CHANGED** = `2000`
`🔗<class_Node3D_constant_NOTIFICATION_TRANSFORM_CHANGED>`

**Node3D** nodes receive this notification when their global transform
changes. This means that either the current or a parent node changed its
transform.

In order for
`NOTIFICATION_TRANSFORM_CHANGED<class_Node3D_constant_NOTIFICATION_TRANSFORM_CHANGED>`
to work, users first need to ask for it, with
`set_notify_transform<class_Node3D_method_set_notify_transform>`. The
notification is also sent if the node is in the editor context and it
has at least one valid gizmo.

classref-constant

**NOTIFICATION\_ENTER\_WORLD** = `41`
`🔗<class_Node3D_constant_NOTIFICATION_ENTER_WORLD>`

**Node3D** nodes receive this notification when they are registered to
new `World3D<class_World3D>` resource.

classref-constant

**NOTIFICATION\_EXIT\_WORLD** = `42`
`🔗<class_Node3D_constant_NOTIFICATION_EXIT_WORLD>`

**Node3D** nodes receive this notification when they are unregistered
from current `World3D<class_World3D>` resource.

classref-constant

**NOTIFICATION\_VISIBILITY\_CHANGED** = `43`
`🔗<class_Node3D_constant_NOTIFICATION_VISIBILITY_CHANGED>`

**Node3D** nodes receive this notification when their visibility
changes.

classref-constant

**NOTIFICATION\_LOCAL\_TRANSFORM\_CHANGED** = `44`
`🔗<class_Node3D_constant_NOTIFICATION_LOCAL_TRANSFORM_CHANGED>`

**Node3D** nodes receive this notification when their local transform
changes. This is not received when the transform of a parent node is
changed.

In order for
`NOTIFICATION_LOCAL_TRANSFORM_CHANGED<class_Node3D_constant_NOTIFICATION_LOCAL_TRANSFORM_CHANGED>`
to work, users first need to ask for it, with
`set_notify_local_transform<class_Node3D_method_set_notify_local_transform>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Basis<class_Basis>` **basis** `🔗<class_Node3D_property_basis>`

classref-property-setget

-   `void (No return value.)` **set\_basis**(value:
    `Basis<class_Basis>`)
-   `Basis<class_Basis>` **get\_basis**()

Basis of the `transform<class_Node3D_property_transform>` property.
Represents the rotation, scale, and shear of this node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Basis<class_Basis>` **global\_basis**
`🔗<class_Node3D_property_global_basis>`

classref-property-setget

-   `void (No return value.)` **set\_global\_basis**(value:
    `Basis<class_Basis>`)
-   `Basis<class_Basis>` **get\_global\_basis**()

Global basis of this node. This is equivalent to
`global_transform.basis`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **global\_position**
`🔗<class_Node3D_property_global_position>`

classref-property-setget

-   `void (No return value.)` **set\_global\_position**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_global\_position**()

Global position of this node. This is equivalent to
`global_transform.origin`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **global\_rotation**
`🔗<class_Node3D_property_global_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_global\_rotation**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_global\_rotation**()

Rotation part of the global transformation in radians, specified in
terms of YXZ-Euler angles in the format (X angle, Y angle, Z angle).

\*\*Note:\*\* In the mathematical sense, rotation is a matrix and not a
vector. The three Euler angles, which are the three independent
parameters of the Euler-angle parametrization of the rotation matrix,
are stored in a `Vector3<class_Vector3>` data structure not because the
rotation is a vector, but only because `Vector3<class_Vector3>` exists
as a convenient data-structure to store 3 floating-point numbers.
Therefore, applying affine operations on the rotation "vector" is not
meaningful.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **global\_rotation\_degrees**
`🔗<class_Node3D_property_global_rotation_degrees>`

classref-property-setget

-   `void (No return value.)` **set\_global\_rotation\_degrees**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_global\_rotation\_degrees**()

Helper property to access
`global_rotation<class_Node3D_property_global_rotation>` in degrees
instead of radians.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform3D<class_Transform3D>` **global\_transform**
`🔗<class_Node3D_property_global_transform>`

classref-property-setget

-   `void (No return value.)` **set\_global\_transform**(value:
    `Transform3D<class_Transform3D>`)
-   `Transform3D<class_Transform3D>` **get\_global\_transform**()

World3D space (global) `Transform3D<class_Transform3D>` of this node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **position** = `Vector3(0, 0, 0)`
`🔗<class_Node3D_property_position>`

classref-property-setget

-   `void (No return value.)` **set\_position**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_position**()

Local position or translation of this node relative to the parent. This
is equivalent to `transform.origin`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Quaternion<class_Quaternion>` **quaternion**
`🔗<class_Node3D_property_quaternion>`

classref-property-setget

-   `void (No return value.)` **set\_quaternion**(value:
    `Quaternion<class_Quaternion>`)
-   `Quaternion<class_Quaternion>` **get\_quaternion**()

Access to the node rotation as a `Quaternion<class_Quaternion>`. This
property is ideal for tweening complex rotations.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **rotation** = `Vector3(0, 0, 0)`
`🔗<class_Node3D_property_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_rotation**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_rotation**()

Rotation part of the local transformation in radians, specified in terms
of Euler angles. The angles construct a rotation in the order specified
by the `rotation_order<class_Node3D_property_rotation_order>` property.

\*\*Note:\*\* In the mathematical sense, rotation is a matrix and not a
vector. The three Euler angles, which are the three independent
parameters of the Euler-angle parametrization of the rotation matrix,
are stored in a `Vector3<class_Vector3>` data structure not because the
rotation is a vector, but only because `Vector3<class_Vector3>` exists
as a convenient data-structure to store 3 floating-point numbers.
Therefore, applying affine operations on the rotation "vector" is not
meaningful.

\*\*Note:\*\* This property is edited in the inspector in degrees. If
you want to use degrees in a script, use
`rotation_degrees<class_Node3D_property_rotation_degrees>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **rotation\_degrees**
`🔗<class_Node3D_property_rotation_degrees>`

classref-property-setget

-   `void (No return value.)` **set\_rotation\_degrees**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_rotation\_degrees**()

Helper property to access `rotation<class_Node3D_property_rotation>` in
degrees instead of radians.

classref-item-separator

------------------------------------------------------------------------

classref-property

`RotationEditMode<enum_Node3D_RotationEditMode>`
**rotation\_edit\_mode** = `0`
`🔗<class_Node3D_property_rotation_edit_mode>`

classref-property-setget

-   `void (No return value.)` **set\_rotation\_edit\_mode**(value:
    `RotationEditMode<enum_Node3D_RotationEditMode>`)
-   `RotationEditMode<enum_Node3D_RotationEditMode>`
    **get\_rotation\_edit\_mode**()

Specify how rotation (and scale) will be presented in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`EulerOrder<enum_@GlobalScope_EulerOrder>` **rotation\_order** = `2`
`🔗<class_Node3D_property_rotation_order>`

classref-property-setget

-   `void (No return value.)` **set\_rotation\_order**(value:
    `EulerOrder<enum_@GlobalScope_EulerOrder>`)
-   `EulerOrder<enum_@GlobalScope_EulerOrder>`
    **get\_rotation\_order**()

Specify the axis rotation order of the
`rotation<class_Node3D_property_rotation>` property. The final
orientation is constructed by rotating the Euler angles in the order
specified by this property.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **scale** = `Vector3(1, 1, 1)`
`🔗<class_Node3D_property_scale>`

classref-property-setget

-   `void (No return value.)` **set\_scale**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_scale**()

Scale part of the local transformation.

\*\*Note:\*\* Mixed negative scales in 3D are not decomposable from the
transformation matrix. Due to the way scale is represented with
transformation matrices in Godot, the scale values will either be all
positive or all negative.

\*\*Note:\*\* Not all nodes are visually scaled by the
`scale<class_Node3D_property_scale>` property. For example,
`Light3D<class_Light3D>`s are not visually affected by
`scale<class_Node3D_property_scale>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **top\_level** = `false`
`🔗<class_Node3D_property_top_level>`

classref-property-setget

-   `void (No return value.)` **set\_as\_top\_level**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_set\_as\_top\_level**()

If `true`, the node will not inherit its transformations from its
parent. Node transformations are only in global space.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform3D<class_Transform3D>` **transform** =
`Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0)`
`🔗<class_Node3D_property_transform>`

classref-property-setget

-   `void (No return value.)` **set\_transform**(value:
    `Transform3D<class_Transform3D>`)
-   `Transform3D<class_Transform3D>` **get\_transform**()

Local space `Transform3D<class_Transform3D>` of this node, with respect
to the parent node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **visibility\_parent** = `NodePath("")`
`🔗<class_Node3D_property_visibility_parent>`

classref-property-setget

-   `void (No return value.)` **set\_visibility\_parent**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_visibility\_parent**()

Defines the visibility range parent for this node and its subtree. The
visibility parent must be a GeometryInstance3D. Any visual instance will
only be visible if the visibility parent (and all of its visibility
ancestors) is hidden by being closer to the camera than its own
`GeometryInstance3D.visibility_range_begin<class_GeometryInstance3D_property_visibility_range_begin>`.
Nodes hidden via the `visible<class_Node3D_property_visible>` property
are essentially removed from the visibility dependency tree, so
dependent instances will not take the hidden node or its ancestors into
account.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **visible** = `true`
`🔗<class_Node3D_property_visible>`

classref-property-setget

-   `void (No return value.)` **set\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_visible**()

If `true`, this node is drawn. The node is only visible if all of its
ancestors are visible as well (in other words,
`is_visible_in_tree<class_Node3D_method_is_visible_in_tree>` must return
`true`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_gizmo**(gizmo:
`Node3DGizmo<class_Node3DGizmo>`) `🔗<class_Node3D_method_add_gizmo>`

Attach an editor gizmo to this **Node3D**.

\*\*Note:\*\* The gizmo object would typically be an instance of
`EditorNode3DGizmo<class_EditorNode3DGizmo>`, but the argument type is
kept generic to avoid creating a dependency on editor classes in
**Node3D**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_gizmos**()
`🔗<class_Node3D_method_clear_gizmos>`

Clear all gizmos attached to this **Node3D**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_subgizmo\_selection**()
`🔗<class_Node3D_method_clear_subgizmo_selection>`

Clears subgizmo selection for this node in the editor. Useful when
subgizmo IDs become invalid after a property change.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **force\_update\_transform**()
`🔗<class_Node3D_method_force_update_transform>`

Forces the transform to update. Transform changes in physics are not
instant for performance reasons. Transforms are accumulated and then
set. Use this if you need an up-to-date transform when doing physics
operations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Node3DGizmo<class_Node3DGizmo>`\]
**get\_gizmos**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node3D_method_get_gizmos>`

Returns all the gizmos attached to this **Node3D**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>`
**get\_global\_transform\_interpolated**()
`🔗<class_Node3D_method_get_global_transform_interpolated>`

When using physics interpolation, there will be circumstances in which
you want to know the interpolated (displayed) transform of a node rather
than the standard transform (which may only be accurate to the most
recent physics tick).

This is particularly important for frame-based operations that take
place in `Node._process<class_Node_private_method__process>`, rather
than
`Node._physics_process<class_Node_private_method__physics_process>`.
Examples include `Camera3D<class_Camera3D>`s focusing on a node, or
finding where to fire lasers from on a frame rather than physics tick.

\*\*Note:\*\* This function creates an interpolation pump on the
**Node3D** the first time it is called, which can respond to physics
interpolation resets. If you get problems with "streaking" when
initially following a **Node3D**, be sure to call
`get_global_transform_interpolated<class_Node3D_method_get_global_transform_interpolated>`
at least once *before* resetting the **Node3D** physics interpolation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node3D<class_Node3D>` **get\_parent\_node\_3d**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node3D_method_get_parent_node_3d>`

Returns the parent **Node3D**, or `null` if no parent exists, the parent
is not of type **Node3D**, or
`top_level<class_Node3D_property_top_level>` is `true`.

\*\*Note:\*\* Calling this method is not equivalent to
`get_parent() as Node3D`, which does not take
`top_level<class_Node3D_property_top_level>` into account.

classref-item-separator

------------------------------------------------------------------------

classref-method

`World3D<class_World3D>` **get\_world\_3d**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node3D_method_get_world_3d>`

Returns the current `World3D<class_World3D>` resource this **Node3D**
node is registered to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_rotate**(axis:
`Vector3<class_Vector3>`, angle: `float<class_float>`)
`🔗<class_Node3D_method_global_rotate>`

Rotates the global (world) transformation around axis, a unit
`Vector3<class_Vector3>`, by specified angle in radians. The rotation
axis is in global coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_scale**(scale:
`Vector3<class_Vector3>`) `🔗<class_Node3D_method_global_scale>`

Scales the global (world) transformation by the given
`Vector3<class_Vector3>` scale factors.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_translate**(offset:
`Vector3<class_Vector3>`) `🔗<class_Node3D_method_global_translate>`

Moves the global (world) transformation by `Vector3<class_Vector3>`
offset. The offset is in global coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **hide**() `🔗<class_Node3D_method_hide>`

Disables rendering of this node. Changes
`visible<class_Node3D_property_visible>` to `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_local\_transform\_notification\_enabled**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node3D_method_is_local_transform_notification_enabled>`

Returns whether node notifies about its local transformation changes.
**Node3D** will not propagate this by default.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_scale\_disabled**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node3D_method_is_scale_disabled>`

Returns whether this node uses a scale of `(1, 1, 1)` or its local
transformation scale.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_transform\_notification\_enabled**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node3D_method_is_transform_notification_enabled>`

Returns whether the node notifies about its global and local
transformation changes. **Node3D** will not propagate this by default.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_visible\_in\_tree**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node3D_method_is_visible_in_tree>`

Returns `true` if the node is present in the
`SceneTree<class_SceneTree>`, its
`visible<class_Node3D_property_visible>` property is `true` and all its
ancestors are also visible. If any ancestor is hidden, this node will
not be visible in the scene tree.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **look\_at**(target: `Vector3<class_Vector3>`,
up: `Vector3<class_Vector3>` = Vector3(0, 1, 0), use\_model\_front:
`bool<class_bool>` = false) `🔗<class_Node3D_method_look_at>`

Rotates the node so that the local forward axis (-Z,
`Vector3.FORWARD<class_Vector3_constant_FORWARD>`) points toward the
`target` position.

The local up axis (+Y) points as close to the `up` vector as possible
while staying perpendicular to the local forward axis. The resulting
transform is orthogonal, and the scale is preserved. Non-uniform scaling
may not work correctly.

The `target` position cannot be the same as the node's position, the
`up` vector cannot be zero, and the direction from the node's position
to the `target` vector cannot be parallel to the `up` vector.

Operations take place in global space, which means that the node must be
in the scene tree.

If `use_model_front` is `true`, the +Z axis (asset front) is treated as
forward (implies +X is left) and points toward the `target` position. By
default, the -Z axis (camera forward) is treated as forward (implies +X
is right).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **look\_at\_from\_position**(position:
`Vector3<class_Vector3>`, target: `Vector3<class_Vector3>`, up:
`Vector3<class_Vector3>` = Vector3(0, 1, 0), use\_model\_front:
`bool<class_bool>` = false)
`🔗<class_Node3D_method_look_at_from_position>`

Moves the node to the specified `position`, and then rotates the node to
point toward the `target` as per `look_at<class_Node3D_method_look_at>`.
Operations take place in global space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **orthonormalize**()
`🔗<class_Node3D_method_orthonormalize>`

Resets this node's transformations (like scale, skew and taper)
preserving its rotation and translation by performing Gram-Schmidt
orthonormalization on this node's `Transform3D<class_Transform3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **rotate**(axis: `Vector3<class_Vector3>`,
angle: `float<class_float>`) `🔗<class_Node3D_method_rotate>`

Rotates the local transformation around axis, a unit
`Vector3<class_Vector3>`, by specified angle in radians.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **rotate\_object\_local**(axis:
`Vector3<class_Vector3>`, angle: `float<class_float>`)
`🔗<class_Node3D_method_rotate_object_local>`

Rotates the local transformation around axis, a unit
`Vector3<class_Vector3>`, by specified angle in radians. The rotation
axis is in object-local coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **rotate\_x**(angle: `float<class_float>`)
`🔗<class_Node3D_method_rotate_x>`

Rotates the local transformation around the X axis by angle in radians.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **rotate\_y**(angle: `float<class_float>`)
`🔗<class_Node3D_method_rotate_y>`

Rotates the local transformation around the Y axis by angle in radians.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **rotate\_z**(angle: `float<class_float>`)
`🔗<class_Node3D_method_rotate_z>`

Rotates the local transformation around the Z axis by angle in radians.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **scale\_object\_local**(scale:
`Vector3<class_Vector3>`) `🔗<class_Node3D_method_scale_object_local>`

Scales the local transformation by given 3D scale factors in
object-local coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_disable\_scale**(disable:
`bool<class_bool>`) `🔗<class_Node3D_method_set_disable_scale>`

Sets whether the node uses a scale of `(1, 1, 1)` or its local
transformation scale. Changes to the local transformation scale are
preserved.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_identity**()
`🔗<class_Node3D_method_set_identity>`

Reset all transformations for this node (sets its
`Transform3D<class_Transform3D>` to the identity matrix).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_ignore\_transform\_notification**(enabled: `bool<class_bool>`)
`🔗<class_Node3D_method_set_ignore_transform_notification>`

Sets whether the node ignores notification that its transformation
(global or local) changed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_notify\_local\_transform**(enable:
`bool<class_bool>`) `🔗<class_Node3D_method_set_notify_local_transform>`

Sets whether the node notifies about its local transformation changes.
**Node3D** will not propagate this by default.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_notify\_transform**(enable:
`bool<class_bool>`) `🔗<class_Node3D_method_set_notify_transform>`

Sets whether the node notifies about its global and local transformation
changes. **Node3D** will not propagate this by default, unless it is in
the editor context and it has a valid gizmo.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_subgizmo\_selection**(gizmo:
`Node3DGizmo<class_Node3DGizmo>`, id: `int<class_int>`, transform:
`Transform3D<class_Transform3D>`)
`🔗<class_Node3D_method_set_subgizmo_selection>`

Set subgizmo selection for this node in the editor.

\*\*Note:\*\* The gizmo object would typically be an instance of
`EditorNode3DGizmo<class_EditorNode3DGizmo>`, but the argument type is
kept generic to avoid creating a dependency on editor classes in
**Node3D**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **show**() `🔗<class_Node3D_method_show>`

Enables rendering of this node. Changes
`visible<class_Node3D_property_visible>` to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **to\_global**(local\_point:
`Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node3D_method_to_global>`

Transforms `local_point` from this node's local space to world space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **to\_local**(global\_point:
`Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node3D_method_to_local>`

Transforms `global_point` from world space to this node's local space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **translate**(offset:
`Vector3<class_Vector3>`) `🔗<class_Node3D_method_translate>`

Changes the node's position by the given offset
`Vector3<class_Vector3>`.

Note that the translation `offset` is affected by the node's scale, so
if scaled by e.g. `(10, 1, 1)`, a translation by an offset of
`(2, 0, 0)` would actually add 20 (`2 * 10`) to the X coordinate.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **translate\_object\_local**(offset:
`Vector3<class_Vector3>`)
`🔗<class_Node3D_method_translate_object_local>`

Changes the node's position by the given offset `Vector3<class_Vector3>`
in local space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update\_gizmos**()
`🔗<class_Node3D_method_update_gizmos>`

Updates all the **Node3D** gizmos attached to this node.
