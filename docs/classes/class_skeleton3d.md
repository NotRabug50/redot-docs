github\_url  
hide

# Skeleton3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A node containing a bone hierarchy, used to create a 3D skeletal
animation.

classref-introduction-group

## Description

**Skeleton3D** provides an interface for managing a hierarchy of bones,
including pose, rest and animation (see `Animation<class_Animation>`).
It can also use ragdoll physics.

The overall transform of a bone with respect to the skeleton is
determined by bone pose. Bone rest defines the initial transform of the
bone pose.

Note that "global pose" below refers to the overall transform of the
bone with respect to skeleton, so it is not the actual global/world
transform of the bone.

classref-introduction-group

## Tutorials

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

**bone\_enabled\_changed**(bone\_idx: `int<class_int>`)
`🔗<class_Skeleton3D_signal_bone_enabled_changed>`

Emitted when the bone at `bone_idx` is toggled with
`set_bone_enabled<class_Skeleton3D_method_set_bone_enabled>`. Use
`is_bone_enabled<class_Skeleton3D_method_is_bone_enabled>` to check the
new value.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**bone\_list\_changed**()
`🔗<class_Skeleton3D_signal_bone_list_changed>`

There is currently no description for this signal. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-signal

**pose\_updated**() `🔗<class_Skeleton3D_signal_pose_updated>`

Emitted when the pose is updated.

\*\*Note:\*\* During the update process, this signal is not fired, so
modification by `SkeletonModifier3D<class_SkeletonModifier3D>` is not
detected.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**show\_rest\_only\_changed**()
`🔗<class_Skeleton3D_signal_show_rest_only_changed>`

Emitted when the value of
`show_rest_only<class_Skeleton3D_property_show_rest_only>` changes.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**skeleton\_updated**() `🔗<class_Skeleton3D_signal_skeleton_updated>`

Emitted when the final pose has been calculated will be applied to the
skin in the update process.

This means that all `SkeletonModifier3D<class_SkeletonModifier3D>`
processing is complete. In order to detect the completion of the
processing of each `SkeletonModifier3D<class_SkeletonModifier3D>`, use
`SkeletonModifier3D.modification_processed<class_SkeletonModifier3D_signal_modification_processed>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ModifierCallbackModeProcess**:
`🔗<enum_Skeleton3D_ModifierCallbackModeProcess>`

classref-enumeration-constant

`ModifierCallbackModeProcess<enum_Skeleton3D_ModifierCallbackModeProcess>`
**MODIFIER\_CALLBACK\_MODE\_PROCESS\_PHYSICS** = `0`

Set a flag to process modification during physics frames (see
`Node.NOTIFICATION_INTERNAL_PHYSICS_PROCESS<class_Node_constant_NOTIFICATION_INTERNAL_PHYSICS_PROCESS>`).

classref-enumeration-constant

`ModifierCallbackModeProcess<enum_Skeleton3D_ModifierCallbackModeProcess>`
**MODIFIER\_CALLBACK\_MODE\_PROCESS\_IDLE** = `1`

Set a flag to process modification during process frames (see
`Node.NOTIFICATION_INTERNAL_PROCESS<class_Node_constant_NOTIFICATION_INTERNAL_PROCESS>`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NOTIFICATION\_UPDATE\_SKELETON** = `50`
`🔗<class_Skeleton3D_constant_NOTIFICATION_UPDATE_SKELETON>`

Notification received when this skeleton's pose needs to be updated. In
that case, this is called only once per frame in a deferred process.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **animate\_physical\_bones** = `true`
`🔗<class_Skeleton3D_property_animate_physical_bones>`

classref-property-setget

-   `void (No return value.)` **set\_animate\_physical\_bones**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_animate\_physical\_bones**()

**Deprecated:** This property may be changed or removed in future
versions.

If you follow the recommended workflow and explicitly have
`PhysicalBoneSimulator3D<class_PhysicalBoneSimulator3D>` as a child of
**Skeleton3D**, you can control whether it is affected by raycasting
without running
`physical_bones_start_simulation<class_Skeleton3D_method_physical_bones_start_simulation>`,
by its
`SkeletonModifier3D.active<class_SkeletonModifier3D_property_active>`.

However, for old (deprecated) configurations, **Skeleton3D** has an
internal virtual
`PhysicalBoneSimulator3D<class_PhysicalBoneSimulator3D>` for
compatibility. This property controls the internal virtual
`PhysicalBoneSimulator3D<class_PhysicalBoneSimulator3D>`'s
`SkeletonModifier3D.active<class_SkeletonModifier3D_property_active>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ModifierCallbackModeProcess<enum_Skeleton3D_ModifierCallbackModeProcess>`
**modifier\_callback\_mode\_process** = `1`
`🔗<class_Skeleton3D_property_modifier_callback_mode_process>`

classref-property-setget

-   `void (No return value.)`
    **set\_modifier\_callback\_mode\_process**(value:
    `ModifierCallbackModeProcess<enum_Skeleton3D_ModifierCallbackModeProcess>`)
-   `ModifierCallbackModeProcess<enum_Skeleton3D_ModifierCallbackModeProcess>`
    **get\_modifier\_callback\_mode\_process**()

Sets the processing timing for the Modifier.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **motion\_scale** = `1.0`
`🔗<class_Skeleton3D_property_motion_scale>`

classref-property-setget

-   `void (No return value.)` **set\_motion\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_motion\_scale**()

Multiplies the 3D position track animation.

\*\*Note:\*\* Unless this value is `1.0`, the key value in animation
will not match the actual position value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_rest\_only** = `false`
`🔗<class_Skeleton3D_property_show_rest_only>`

classref-property-setget

-   `void (No return value.)` **set\_show\_rest\_only**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_show\_rest\_only**()

If `true`, forces the bones in their default rest pose, regardless of
their values. In the editor, this also prevents the bones from being
edited.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **add\_bone**(name: `String<class_String>`)
`🔗<class_Skeleton3D_method_add_bone>`

Adds a new bone with the given name. Returns the new bone's index, or
`-1` if this method fails.

\*\*Note:\*\* Bone names should be unique, non empty, and cannot include
the `:` and `/` characters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_bones**()
`🔗<class_Skeleton3D_method_clear_bones>`

Clear all the bones in this skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_bones\_global\_pose\_override**()
`🔗<class_Skeleton3D_method_clear_bones_global_pose_override>`

**Deprecated:** This method may be changed or removed in future
versions.

Removes the global pose override on all bones in the skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Skin<class_Skin>` **create\_skin\_from\_rest\_transforms**()
`🔗<class_Skeleton3D_method_create_skin_from_rest_transforms>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **find\_bone**(name: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_find_bone>`

Returns the bone index that matches `name` as its name. Returns `-1` if
no bone with this name exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **force\_update\_all\_bone\_transforms**()
`🔗<class_Skeleton3D_method_force_update_all_bone_transforms>`

**Deprecated:** This method should only be called internally.

Force updates the bone transforms/poses for all bones in the skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**force\_update\_bone\_child\_transform**(bone\_idx: `int<class_int>`)
`🔗<class_Skeleton3D_method_force_update_bone_child_transform>`

Force updates the bone transform for the bone at `bone_idx` and all of
its children.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**get\_bone\_children**(bone\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_children>`

Returns an array containing the bone indexes of all the child node of
the passed in bone, `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_bone\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_count>`

Returns the number of bones in the skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **get\_bone\_global\_pose**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_global_pose>`

Returns the overall transform of the specified bone, with respect to the
skeleton. Being relative to the skeleton frame, this is not the actual
"global" transform of the bone.

\*\*Note:\*\* This is the global pose you set to the skeleton in the
process, the final global pose can get overridden by modifiers in the
deferred process, if you want to access the final global pose, use
`SkeletonModifier3D.modification_processed<class_SkeletonModifier3D_signal_modification_processed>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>`
**get\_bone\_global\_pose\_no\_override**(bone\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_global_pose_no_override>`

**Deprecated:** This method may be changed or removed in future
versions.

Returns the overall transform of the specified bone, with respect to the
skeleton, but without any global pose overrides. Being relative to the
skeleton frame, this is not the actual "global" transform of the bone.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>`
**get\_bone\_global\_pose\_override**(bone\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_global_pose_override>`

**Deprecated:** This method may be changed or removed in future
versions.

Returns the global pose override transform for `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **get\_bone\_global\_rest**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_global_rest>`

Returns the global rest transform for `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_bone\_meta**(bone\_idx:
`int<class_int>`, key: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_meta>`

Returns bone metadata for `bone_idx` with `key`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`StringName<class_StringName>`\]
**get\_bone\_meta\_list**(bone\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_meta_list>`

Returns a list of all metadata keys for `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_bone\_name**(bone\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_name>`

Returns the name of the bone at index `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_bone\_parent**(bone\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_parent>`

Returns the bone index which is the parent of the bone at `bone_idx`. If
-1, then bone has no parent.

\*\*Note:\*\* The parent bone returned will always be less than
`bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **get\_bone\_pose**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_pose>`

Returns the pose transform of the specified bone.

\*\*Note:\*\* This is the pose you set to the skeleton in the process,
the final pose can get overridden by modifiers in the deferred process,
if you want to access the final pose, use
`SkeletonModifier3D.modification_processed<class_SkeletonModifier3D_signal_modification_processed>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_bone\_pose\_position**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_pose_position>`

Returns the pose position of the bone at `bone_idx`. The returned
`Vector3<class_Vector3>` is in the local coordinate space of the
**Skeleton3D** node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Quaternion<class_Quaternion>` **get\_bone\_pose\_rotation**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_pose_rotation>`

Returns the pose rotation of the bone at `bone_idx`. The returned
`Quaternion<class_Quaternion>` is local to the bone with respect to the
rotation of any parent bones.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_bone\_pose\_scale**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_pose_scale>`

Returns the pose scale of the bone at `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **get\_bone\_rest**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_bone_rest>`

Returns the rest transform for a bone `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_concatenated\_bone\_names**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_concatenated_bone_names>`

Returns all bone names concatenated with commas (`,`) as a single
`StringName<class_StringName>`.

It is useful to set it as a hint for the enum property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>` **get\_parentless\_bones**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_parentless_bones>`

Returns an array with all of the bones that are parentless. Another way
to look at this is that it returns the indexes of all the bones that are
not dependent or modified by other bones in the Skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_version**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_get_version>`

Returns the number of times the bone hierarchy has changed within this
skeleton, including renames.

The Skeleton version is not serialized: only use within a single
instance of Skeleton3D.

Use for invalidating caches in IK solvers and other nodes which process
bones.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_bone\_meta**(bone\_idx: `int<class_int>`, key:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_has_bone_meta>`

Returns whether there exists any bone metadata for `bone_idx` with key
`key`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_bone\_enabled**(bone\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Skeleton3D_method_is_bone_enabled>`

Returns whether the bone pose for the bone at `bone_idx` is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **localize\_rests**()
`🔗<class_Skeleton3D_method_localize_rests>`

Returns all bones in the skeleton to their rest poses.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**physical\_bones\_add\_collision\_exception**(exception:
`RID<class_RID>`)
`🔗<class_Skeleton3D_method_physical_bones_add_collision_exception>`

**Deprecated:** This method may be changed or removed in future
versions.

Adds a collision exception to the physical bone.

Works just like the `RigidBody3D<class_RigidBody3D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**physical\_bones\_remove\_collision\_exception**(exception:
`RID<class_RID>`)
`🔗<class_Skeleton3D_method_physical_bones_remove_collision_exception>`

**Deprecated:** This method may be changed or removed in future
versions.

Removes a collision exception to the physical bone.

Works just like the `RigidBody3D<class_RigidBody3D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **physical\_bones\_start\_simulation**(bones:
`Array<class_Array>`\[`StringName<class_StringName>`\] = \[\])
`🔗<class_Skeleton3D_method_physical_bones_start_simulation>`

**Deprecated:** This method may be changed or removed in future
versions.

Tells the `PhysicalBone3D<class_PhysicalBone3D>` nodes in the Skeleton
to start simulating and reacting to the physics world.

Optionally, a list of bone names can be passed-in, allowing only the
passed-in bones to be simulated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **physical\_bones\_stop\_simulation**()
`🔗<class_Skeleton3D_method_physical_bones_stop_simulation>`

**Deprecated:** This method may be changed or removed in future
versions.

Tells the `PhysicalBone3D<class_PhysicalBone3D>` nodes in the Skeleton
to stop simulating.

classref-item-separator

------------------------------------------------------------------------

classref-method

`SkinReference<class_SkinReference>` **register\_skin**(skin:
`Skin<class_Skin>`) `🔗<class_Skeleton3D_method_register_skin>`

Binds the given Skin to the Skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reset\_bone\_pose**(bone\_idx:
`int<class_int>`) `🔗<class_Skeleton3D_method_reset_bone_pose>`

Sets the bone pose to rest for `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reset\_bone\_poses**()
`🔗<class_Skeleton3D_method_reset_bone_poses>`

Sets all bone poses to rests.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_enabled**(bone\_idx:
`int<class_int>`, enabled: `bool<class_bool>` = true)
`🔗<class_Skeleton3D_method_set_bone_enabled>`

Disables the pose for the bone at `bone_idx` if `false`, enables the
bone pose if `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_global\_pose**(bone\_idx:
`int<class_int>`, pose: `Transform3D<class_Transform3D>`)
`🔗<class_Skeleton3D_method_set_bone_global_pose>`

Sets the global pose transform, `pose`, for the bone at `bone_idx`.

\*\*Note:\*\* If other bone poses have been changed, this method
executes a dirty poses recalculation and will cause performance to
deteriorate. If you know that multiple global poses will be applied,
consider using `set_bone_pose<class_Skeleton3D_method_set_bone_pose>`
with precalculation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_bone\_global\_pose\_override**(bone\_idx: `int<class_int>`, pose:
`Transform3D<class_Transform3D>`, amount: `float<class_float>`,
persistent: `bool<class_bool>` = false)
`🔗<class_Skeleton3D_method_set_bone_global_pose_override>`

**Deprecated:** This method may be changed or removed in future
versions.

Sets the global pose transform, `pose`, for the bone at `bone_idx`.

`amount` is the interpolation strength that will be used when applying
the pose, and `persistent` determines if the applied pose will remain.

\*\*Note:\*\* The pose transform needs to be a global pose! To convert a
world transform from a `Node3D<class_Node3D>` to a global bone pose,
multiply the
`Transform3D.affine_inverse<class_Transform3D_method_affine_inverse>` of
the node's
`Node3D.global_transform<class_Node3D_property_global_transform>` by the
desired world transform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_meta**(bone\_idx:
`int<class_int>`, key: `StringName<class_StringName>`, value:
`Variant<class_Variant>`) `🔗<class_Skeleton3D_method_set_bone_meta>`

Sets bone metadata for `bone_idx`, will set the `key` meta to `value`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_name**(bone\_idx:
`int<class_int>`, name: `String<class_String>`)
`🔗<class_Skeleton3D_method_set_bone_name>`

Sets the bone name, `name`, for the bone at `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_parent**(bone\_idx:
`int<class_int>`, parent\_idx: `int<class_int>`)
`🔗<class_Skeleton3D_method_set_bone_parent>`

Sets the bone index `parent_idx` as the parent of the bone at
`bone_idx`. If -1, then bone has no parent.

\*\*Note:\*\* `parent_idx` must be less than `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_pose**(bone\_idx:
`int<class_int>`, pose: `Transform3D<class_Transform3D>`)
`🔗<class_Skeleton3D_method_set_bone_pose>`

Sets the pose transform, `pose`, for the bone at `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_pose\_position**(bone\_idx:
`int<class_int>`, position: `Vector3<class_Vector3>`)
`🔗<class_Skeleton3D_method_set_bone_pose_position>`

Sets the pose position of the bone at `bone_idx` to `position`.
`position` is a `Vector3<class_Vector3>` describing a position local to
the **Skeleton3D** node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_pose\_rotation**(bone\_idx:
`int<class_int>`, rotation: `Quaternion<class_Quaternion>`)
`🔗<class_Skeleton3D_method_set_bone_pose_rotation>`

Sets the pose rotation of the bone at `bone_idx` to `rotation`.
`rotation` is a `Quaternion<class_Quaternion>` describing a rotation in
the bone's local coordinate space with respect to the rotation of any
parent bones.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_pose\_scale**(bone\_idx:
`int<class_int>`, scale: `Vector3<class_Vector3>`)
`🔗<class_Skeleton3D_method_set_bone_pose_scale>`

Sets the pose scale of the bone at `bone_idx` to `scale`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_rest**(bone\_idx:
`int<class_int>`, rest: `Transform3D<class_Transform3D>`)
`🔗<class_Skeleton3D_method_set_bone_rest>`

Sets the rest transform for bone `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unparent\_bone\_and\_rest**(bone\_idx:
`int<class_int>`) `🔗<class_Skeleton3D_method_unparent_bone_and_rest>`

Unparents the bone at `bone_idx` and sets its rest position to that of
its parent prior to being reset.
