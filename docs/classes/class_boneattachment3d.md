github\_url  
hide

# BoneAttachment3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

А node that dynamically copies or overrides the 3D transform of a bone
in its parent `Skeleton3D<class_Skeleton3D>`.

classref-introduction-group

## Description

This node selects a bone in a `Skeleton3D<class_Skeleton3D>` and
attaches to it. This means that the **BoneAttachment3D** node will
either dynamically copy or override the 3D transform of the selected
bone.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **bone\_idx** = `-1`
`🔗<class_BoneAttachment3D_property_bone_idx>`

classref-property-setget

-   `void (No return value.)` **set\_bone\_idx**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_bone\_idx**()

The index of the attached bone.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **bone\_name** = `""`
`🔗<class_BoneAttachment3D_property_bone_name>`

classref-property-setget

-   `void (No return value.)` **set\_bone\_name**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_bone\_name**()

The name of the attached bone.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **override\_pose** = `false`
`🔗<class_BoneAttachment3D_property_override_pose>`

classref-property-setget

-   `void (No return value.)` **set\_override\_pose**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_override\_pose**()

Whether the BoneAttachment3D node will override the bone pose of the
bone it is attached to. When set to `true`, the BoneAttachment3D node
can change the pose of the bone. When set to `false`, the
BoneAttachment3D will always be set to the bone's transform.

\*\*Note:\*\* This override performs interruptively in the skeleton
update process using signals due to the old design. It may cause
unintended behavior when used at the same time with
`SkeletonModifier3D<class_SkeletonModifier3D>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`NodePath<class_NodePath>` **get\_external\_skeleton**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_BoneAttachment3D_method_get_external_skeleton>`

Returns the `NodePath<class_NodePath>` to the external
`Skeleton3D<class_Skeleton3D>` node, if one has been set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Skeleton3D<class_Skeleton3D>` **get\_skeleton**()
`🔗<class_BoneAttachment3D_method_get_skeleton>`

Get parent or external `Skeleton3D<class_Skeleton3D>` node if found.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_use\_external\_skeleton**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_BoneAttachment3D_method_get_use_external_skeleton>`

Returns whether the BoneAttachment3D node is using an external
`Skeleton3D<class_Skeleton3D>` rather than attempting to use its parent
node as the `Skeleton3D<class_Skeleton3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **on\_skeleton\_update**()
`🔗<class_BoneAttachment3D_method_on_skeleton_update>`

A function that is called automatically when the
`Skeleton3D<class_Skeleton3D>` is updated. This function is where the
**BoneAttachment3D** node updates its position so it is correctly bound
when it is *not* set to override the bone pose.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_external\_skeleton**(external\_skeleton:
`NodePath<class_NodePath>`)
`🔗<class_BoneAttachment3D_method_set_external_skeleton>`

Sets the `NodePath<class_NodePath>` to the external skeleton that the
BoneAttachment3D node should use. See
`set_use_external_skeleton<class_BoneAttachment3D_method_set_use_external_skeleton>`
to enable the external `Skeleton3D<class_Skeleton3D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_use\_external\_skeleton**(use\_external\_skeleton:
`bool<class_bool>`)
`🔗<class_BoneAttachment3D_method_set_use_external_skeleton>`

Sets whether the BoneAttachment3D node will use an external
`Skeleton3D<class_Skeleton3D>` node rather than attempting to use its
parent node as the `Skeleton3D<class_Skeleton3D>`. When set to `true`,
the BoneAttachment3D node will use the external
`Skeleton3D<class_Skeleton3D>` node set in
`set_external_skeleton<class_BoneAttachment3D_method_set_external_skeleton>`.
