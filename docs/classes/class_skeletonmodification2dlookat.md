github\_url  
hide

# SkeletonModification2DLookAt

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `SkeletonModification2D<class_SkeletonModification2D>`
**&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A modification that rotates a `Bone2D<class_Bone2D>` node to look at a
target.

classref-introduction-group

## Description

This `SkeletonModification2D<class_SkeletonModification2D>` rotates a
bone to look a target. This is extremely helpful for moving character's
head to look at the player, rotating a turret to look at a target, or
any other case where you want to make a bone rotate towards something
quickly and easily.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`NodePath<class_NodePath>` **bone2d\_node** = `NodePath("")`
`🔗<class_SkeletonModification2DLookAt_property_bone2d_node>`

classref-property-setget

-   `void (No return value.)` **set\_bone2d\_node**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_bone2d\_node**()

The `Bone2D<class_Bone2D>` node that the modification will operate on.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **bone\_index** = `-1`
`🔗<class_SkeletonModification2DLookAt_property_bone_index>`

classref-property-setget

-   `void (No return value.)` **set\_bone\_index**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_bone\_index**()

The index of the `Bone2D<class_Bone2D>` node that the modification will
operate on.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **target\_nodepath** = `NodePath("")`
`🔗<class_SkeletonModification2DLookAt_property_target_nodepath>`

classref-property-setget

-   `void (No return value.)` **set\_target\_node**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_target\_node**()

The NodePath to the node that is the target for the LookAt modification.
This node is what the modification will rotate the
`Bone2D<class_Bone2D>` to.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_additional\_rotation**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DLookAt_method_get_additional_rotation>`

Returns the amount of additional rotation that is applied after the
LookAt modification executes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_constraint\_angle\_invert**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DLookAt_method_get_constraint_angle_invert>`

Returns whether the constraints to this modification are inverted or
not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_constraint\_angle\_max**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DLookAt_method_get_constraint_angle_max>`

Returns the constraint's maximum allowed angle.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_constraint\_angle\_min**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DLookAt_method_get_constraint_angle_min>`

Returns the constraint's minimum allowed angle.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_enable\_constraint**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SkeletonModification2DLookAt_method_get_enable_constraint>`

Returns `true` if the LookAt modification is using constraints.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_additional\_rotation**(rotation:
`float<class_float>`)
`🔗<class_SkeletonModification2DLookAt_method_set_additional_rotation>`

Sets the amount of additional rotation that is to be applied after
executing the modification. This allows for offsetting the results by
the inputted rotation amount.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_constraint\_angle\_invert**(invert:
`bool<class_bool>`)
`🔗<class_SkeletonModification2DLookAt_method_set_constraint_angle_invert>`

When `true`, the modification will use an inverted joint constraint.

An inverted joint constraint only constraints the `Bone2D<class_Bone2D>`
to the angles *outside of* the inputted minimum and maximum angles. For
this reason, it is referred to as an inverted joint constraint, as it
constraints the joint to the outside of the inputted values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_constraint\_angle\_max**(angle\_max:
`float<class_float>`)
`🔗<class_SkeletonModification2DLookAt_method_set_constraint_angle_max>`

Sets the constraint's maximum allowed angle.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_constraint\_angle\_min**(angle\_min:
`float<class_float>`)
`🔗<class_SkeletonModification2DLookAt_method_set_constraint_angle_min>`

Sets the constraint's minimum allowed angle.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_enable\_constraint**(enable\_constraint: `bool<class_bool>`)
`🔗<class_SkeletonModification2DLookAt_method_set_enable_constraint>`

Sets whether this modification will use constraints or not. When `true`,
constraints will be applied when solving the LookAt modification.
