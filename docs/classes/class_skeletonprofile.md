github\_url  
hide

# SkeletonProfile

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:**
`SkeletonProfileHumanoid<class_SkeletonProfileHumanoid>`

Base class for a profile of a virtual skeleton used as a target for
retargeting.

classref-introduction-group

## Description

This resource is used in
`EditorScenePostImport<class_EditorScenePostImport>`. Some parameters
are referring to bones in `Skeleton3D<class_Skeleton3D>`,
`Skin<class_Skin>`, `Animation<class_Animation>`, and some other nodes
are rewritten based on the parameters of **SkeletonProfile**.

\*\*Note:\*\* These parameters need to be set only when creating a
custom profile. In
`SkeletonProfileHumanoid<class_SkeletonProfileHumanoid>`, they are
defined internally as read-only values.

classref-introduction-group

## Tutorials

-   `Retargeting 3D Skeletons <../tutorials/assets_pipeline/retargeting_3d_skeletons>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**profile\_updated**()
`🔗<class_SkeletonProfile_signal_profile_updated>`

This signal is emitted when change the value in profile. This is used to
update key name in the `BoneMap<class_BoneMap>` and to redraw the
`BoneMap<class_BoneMap>` editor.

\*\*Note:\*\* This signal is not connected directly to editor to
simplify the reference, instead it is passed on to editor through the
`BoneMap<class_BoneMap>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **TailDirection**: `🔗<enum_SkeletonProfile_TailDirection>`

classref-enumeration-constant

`TailDirection<enum_SkeletonProfile_TailDirection>`
**TAIL\_DIRECTION\_AVERAGE\_CHILDREN** = `0`

Direction to the average coordinates of bone children.

classref-enumeration-constant

`TailDirection<enum_SkeletonProfile_TailDirection>`
**TAIL\_DIRECTION\_SPECIFIC\_CHILD** = `1`

Direction to the coordinates of specified bone child.

classref-enumeration-constant

`TailDirection<enum_SkeletonProfile_TailDirection>`
**TAIL\_DIRECTION\_END** = `2`

Direction is not calculated.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **bone\_size** = `0`
`🔗<class_SkeletonProfile_property_bone_size>`

classref-property-setget

-   `void (No return value.)` **set\_bone\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_bone\_size**()

The amount of bones in retargeting section's `BoneMap<class_BoneMap>`
editor. For example,
`SkeletonProfileHumanoid<class_SkeletonProfileHumanoid>` has 56 bones.

The size of elements in `BoneMap<class_BoneMap>` updates when changing
this property in it's assigned **SkeletonProfile**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **group\_size** = `0`
`🔗<class_SkeletonProfile_property_group_size>`

classref-property-setget

-   `void (No return value.)` **set\_group\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_group\_size**()

The amount of groups of bones in retargeting section's
`BoneMap<class_BoneMap>` editor. For example,
`SkeletonProfileHumanoid<class_SkeletonProfileHumanoid>` has 4 groups.

This property exists to separate the bone list into several sections in
the editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **root\_bone** = `&""`
`🔗<class_SkeletonProfile_property_root_bone>`

classref-property-setget

-   `void (No return value.)` **set\_root\_bone**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_root\_bone**()

A bone name that will be used as the root bone in
`AnimationTree<class_AnimationTree>`. This should be the bone of the
parent of hips that exists at the world origin.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **scale\_base\_bone** = `&""`
`🔗<class_SkeletonProfile_property_scale_base_bone>`

classref-property-setget

-   `void (No return value.)` **set\_scale\_base\_bone**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_scale\_base\_bone**()

A bone name which will use model's height as the coefficient for
normalization. For example,
`SkeletonProfileHumanoid<class_SkeletonProfileHumanoid>` defines it as
`Hips`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **find\_bone**(bone\_name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonProfile_method_find_bone>`

Returns the bone index that matches `bone_name` as its name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_bone\_name**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonProfile_method_get_bone_name>`

Returns the name of the bone at `bone_idx` that will be the key name in
the `BoneMap<class_BoneMap>`.

In the retargeting process, the returned bone name is the bone name of
the target skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_bone\_parent**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonProfile_method_get_bone_parent>`

Returns the name of the bone which is the parent to the bone at
`bone_idx`. The result is empty if the bone has no parent.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_bone\_tail**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonProfile_method_get_bone_tail>`

Returns the name of the bone which is the tail of the bone at
`bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_group**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonProfile_method_get_group>`

Returns the group of the bone at `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_group\_name**(group\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonProfile_method_get_group_name>`

Returns the name of the group at `group_idx` that will be the drawing
group in the `BoneMap<class_BoneMap>` editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_handle\_offset**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonProfile_method_get_handle_offset>`

Returns the offset of the bone at `bone_idx` that will be the button
position in the `BoneMap<class_BoneMap>` editor.

This is the offset with origin at the top left corner of the square.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **get\_reference\_pose**(bone\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonProfile_method_get_reference_pose>`

Returns the reference pose transform for bone `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TailDirection<enum_SkeletonProfile_TailDirection>`
**get\_tail\_direction**(bone\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonProfile_method_get_tail_direction>`

Returns the tail direction of the bone at `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_texture**(group\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonProfile_method_get_texture>`

Returns the texture of the group at `group_idx` that will be the drawing
group background image in the `BoneMap<class_BoneMap>` editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_required**(bone\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonProfile_method_is_required>`

Returns whether the bone at `bone_idx` is required for retargeting.

This value is used by the bone map editor. If this method returns
`true`, and no bone is assigned, the handle color will be red on the
bone map editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_name**(bone\_idx:
`int<class_int>`, bone\_name: `StringName<class_StringName>`)
`🔗<class_SkeletonProfile_method_set_bone_name>`

Sets the name of the bone at `bone_idx` that will be the key name in the
`BoneMap<class_BoneMap>`.

In the retargeting process, the setting bone name is the bone name of
the target skeleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_parent**(bone\_idx:
`int<class_int>`, bone\_parent: `StringName<class_StringName>`)
`🔗<class_SkeletonProfile_method_set_bone_parent>`

Sets the bone with name `bone_parent` as the parent of the bone at
`bone_idx`. If an empty string is passed, then the bone has no parent.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_tail**(bone\_idx:
`int<class_int>`, bone\_tail: `StringName<class_StringName>`)
`🔗<class_SkeletonProfile_method_set_bone_tail>`

Sets the bone with name `bone_tail` as the tail of the bone at
`bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_group**(bone\_idx: `int<class_int>`,
group: `StringName<class_StringName>`)
`🔗<class_SkeletonProfile_method_set_group>`

Sets the group of the bone at `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_group\_name**(group\_idx:
`int<class_int>`, group\_name: `StringName<class_StringName>`)
`🔗<class_SkeletonProfile_method_set_group_name>`

Sets the name of the group at `group_idx` that will be the drawing group
in the `BoneMap<class_BoneMap>` editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_handle\_offset**(bone\_idx:
`int<class_int>`, handle\_offset: `Vector2<class_Vector2>`)
`🔗<class_SkeletonProfile_method_set_handle_offset>`

Sets the offset of the bone at `bone_idx` that will be the button
position in the `BoneMap<class_BoneMap>` editor.

This is the offset with origin at the top left corner of the square.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_reference\_pose**(bone\_idx:
`int<class_int>`, bone\_name: `Transform3D<class_Transform3D>`)
`🔗<class_SkeletonProfile_method_set_reference_pose>`

Sets the reference pose transform for bone `bone_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_required**(bone\_idx: `int<class_int>`,
required: `bool<class_bool>`)
`🔗<class_SkeletonProfile_method_set_required>`

Sets the required status for bone `bone_idx` to `required`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tail\_direction**(bone\_idx:
`int<class_int>`, tail\_direction:
`TailDirection<enum_SkeletonProfile_TailDirection>`)
`🔗<class_SkeletonProfile_method_set_tail_direction>`

Sets the tail direction of the bone at `bone_idx`.

\*\*Note:\*\* This only specifies the method of calculation. The actual
coordinates required should be stored in an external skeleton, so the
calculation itself needs to be done externally.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_texture**(group\_idx: `int<class_int>`,
texture: `Texture2D<class_Texture2D>`)
`🔗<class_SkeletonProfile_method_set_texture>`

Sets the texture of the group at `group_idx` that will be the drawing
group background image in the `BoneMap<class_BoneMap>` editor.
