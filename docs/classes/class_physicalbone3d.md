github\_url  
hide

# PhysicalBone3D

**Inherits:** `PhysicsBody3D<class_PhysicsBody3D>` **&lt;**
`CollisionObject3D<class_CollisionObject3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A physics body used to make bones in a `Skeleton3D<class_Skeleton3D>`
react to physics.

classref-introduction-group

## Description

The **PhysicalBone3D** node is a physics body that can be used to make
bones in a `Skeleton3D<class_Skeleton3D>` react to physics.

\*\*Note:\*\* In order to detect physical bones with raycasts, the
`SkeletonModifier3D.active<class_SkeletonModifier3D_property_active>`
property of the parent
`PhysicalBoneSimulator3D<class_PhysicalBoneSimulator3D>` must be `true`
and the `Skeleton3D<class_Skeleton3D>`'s bone must be assigned to
**PhysicalBone3D** correctly; it means that
`get_bone_id<class_PhysicalBone3D_method_get_bone_id>` should return a
valid id (`>= 0`).

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

## Enumerations

classref-enumeration

enum **DampMode**: `🔗<enum_PhysicalBone3D_DampMode>`

classref-enumeration-constant

`DampMode<enum_PhysicalBone3D_DampMode>` **DAMP\_MODE\_COMBINE** = `0`

In this mode, the body's damping value is added to any value set in
areas or the default value.

classref-enumeration-constant

`DampMode<enum_PhysicalBone3D_DampMode>` **DAMP\_MODE\_REPLACE** = `1`

In this mode, the body's damping value replaces any value set in areas
or the default value.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **JointType**: `🔗<enum_PhysicalBone3D_JointType>`

classref-enumeration-constant

`JointType<enum_PhysicalBone3D_JointType>` **JOINT\_TYPE\_NONE** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`JointType<enum_PhysicalBone3D_JointType>` **JOINT\_TYPE\_PIN** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`JointType<enum_PhysicalBone3D_JointType>` **JOINT\_TYPE\_CONE** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`JointType<enum_PhysicalBone3D_JointType>` **JOINT\_TYPE\_HINGE** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`JointType<enum_PhysicalBone3D_JointType>` **JOINT\_TYPE\_SLIDER** = `4`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`JointType<enum_PhysicalBone3D_JointType>` **JOINT\_TYPE\_6DOF** = `5`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **angular\_damp** = `0.0`
`🔗<class_PhysicalBone3D_property_angular_damp>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_damp**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_angular\_damp**()

Damps the body's rotation. By default, the body will use the **Default
Angular Damp** in **Project &gt; Project Settings &gt; Physics &gt; 3d**
or any value override set by an `Area3D<class_Area3D>` the body is in.
Depending on
`angular_damp_mode<class_PhysicalBone3D_property_angular_damp_mode>`,
you can set `angular_damp<class_PhysicalBone3D_property_angular_damp>`
to be added to or to replace the body's damping value.

See
`ProjectSettings.physics/3d/default_angular_damp<class_ProjectSettings_property_physics/3d/default_angular_damp>`
for more details about damping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DampMode<enum_PhysicalBone3D_DampMode>` **angular\_damp\_mode** = `0`
`🔗<class_PhysicalBone3D_property_angular_damp_mode>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_damp\_mode**(value:
    `DampMode<enum_PhysicalBone3D_DampMode>`)
-   `DampMode<enum_PhysicalBone3D_DampMode>`
    **get\_angular\_damp\_mode**()

Defines how `angular_damp<class_PhysicalBone3D_property_angular_damp>`
is applied. See `DampMode<enum_PhysicalBone3D_DampMode>` for possible
values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **angular\_velocity** = `Vector3(0, 0, 0)`
`🔗<class_PhysicalBone3D_property_angular_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_velocity**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_angular\_velocity**()

The PhysicalBone3D's rotational velocity in *radians* per second.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform3D<class_Transform3D>` **body\_offset** =
`Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0)`
`🔗<class_PhysicalBone3D_property_body_offset>`

classref-property-setget

-   `void (No return value.)` **set\_body\_offset**(value:
    `Transform3D<class_Transform3D>`)
-   `Transform3D<class_Transform3D>` **get\_body\_offset**()

Sets the body's transform.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **bounce** = `0.0`
`🔗<class_PhysicalBone3D_property_bounce>`

classref-property-setget

-   `void (No return value.)` **set\_bounce**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_bounce**()

The body's bounciness. Values range from `0` (no bounce) to `1` (full
bounciness).

\*\*Note:\*\* Even with `bounce<class_PhysicalBone3D_property_bounce>`
set to `1.0`, some energy will be lost over time due to linear and
angular damping. To have a **PhysicalBone3D** that preserves all its
energy over time, set `bounce<class_PhysicalBone3D_property_bounce>` to
`1.0`,
`linear_damp_mode<class_PhysicalBone3D_property_linear_damp_mode>` to
`DAMP_MODE_REPLACE<class_PhysicalBone3D_constant_DAMP_MODE_REPLACE>`,
`linear_damp<class_PhysicalBone3D_property_linear_damp>` to `0.0`,
`angular_damp_mode<class_PhysicalBone3D_property_angular_damp_mode>` to
`DAMP_MODE_REPLACE<class_PhysicalBone3D_constant_DAMP_MODE_REPLACE>`,
and `angular_damp<class_PhysicalBone3D_property_angular_damp>` to `0.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **can\_sleep** = `true`
`🔗<class_PhysicalBone3D_property_can_sleep>`

classref-property-setget

-   `void (No return value.)` **set\_can\_sleep**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_able\_to\_sleep**()

If `true`, the body is deactivated when there is no movement, so it will
not take part in the simulation until it is awakened by an external
force.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **custom\_integrator** = `false`
`🔗<class_PhysicalBone3D_property_custom_integrator>`

classref-property-setget

-   `void (No return value.)` **set\_use\_custom\_integrator**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_custom\_integrator**()

If `true`, the standard force integration (like gravity or damping) will
be disabled for this body. Other than collision response, the body will
only move as determined by the
`_integrate_forces<class_PhysicalBone3D_private_method__integrate_forces>`
method, if that virtual method is overridden.

Setting this property will call the method
`PhysicsServer3D.body_set_omit_force_integration<class_PhysicsServer3D_method_body_set_omit_force_integration>`
internally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **friction** = `1.0`
`🔗<class_PhysicalBone3D_property_friction>`

classref-property-setget

-   `void (No return value.)` **set\_friction**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_friction**()

The body's friction, from `0` (frictionless) to `1` (max friction).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **gravity\_scale** = `1.0`
`🔗<class_PhysicalBone3D_property_gravity_scale>`

classref-property-setget

-   `void (No return value.)` **set\_gravity\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_gravity\_scale**()

This is multiplied by the global 3D gravity setting found in **Project
&gt; Project Settings &gt; Physics &gt; 3d** to produce the body's
gravity. For example, a value of 1 will be normal gravity, 2 will apply
double gravity, and 0.5 will apply half gravity to this object.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform3D<class_Transform3D>` **joint\_offset** =
`Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0)`
`🔗<class_PhysicalBone3D_property_joint_offset>`

classref-property-setget

-   `void (No return value.)` **set\_joint\_offset**(value:
    `Transform3D<class_Transform3D>`)
-   `Transform3D<class_Transform3D>` **get\_joint\_offset**()

Sets the joint's transform.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **joint\_rotation** = `Vector3(0, 0, 0)`
`🔗<class_PhysicalBone3D_property_joint_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_joint\_rotation**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_joint\_rotation**()

Sets the joint's rotation in radians.

classref-item-separator

------------------------------------------------------------------------

classref-property

`JointType<enum_PhysicalBone3D_JointType>` **joint\_type** = `0`
`🔗<class_PhysicalBone3D_property_joint_type>`

classref-property-setget

-   `void (No return value.)` **set\_joint\_type**(value:
    `JointType<enum_PhysicalBone3D_JointType>`)
-   `JointType<enum_PhysicalBone3D_JointType>` **get\_joint\_type**()

Sets the joint type. See `JointType<enum_PhysicalBone3D_JointType>` for
possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_damp** = `0.0`
`🔗<class_PhysicalBone3D_property_linear_damp>`

classref-property-setget

-   `void (No return value.)` **set\_linear\_damp**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_linear\_damp**()

Damps the body's movement. By default, the body will use the **Default
Linear Damp** in **Project &gt; Project Settings &gt; Physics &gt; 3d**
or any value override set by an `Area3D<class_Area3D>` the body is in.
Depending on
`linear_damp_mode<class_PhysicalBone3D_property_linear_damp_mode>`, you
can set `linear_damp<class_PhysicalBone3D_property_linear_damp>` to be
added to or to replace the body's damping value.

See
`ProjectSettings.physics/3d/default_linear_damp<class_ProjectSettings_property_physics/3d/default_linear_damp>`
for more details about damping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DampMode<enum_PhysicalBone3D_DampMode>` **linear\_damp\_mode** = `0`
`🔗<class_PhysicalBone3D_property_linear_damp_mode>`

classref-property-setget

-   `void (No return value.)` **set\_linear\_damp\_mode**(value:
    `DampMode<enum_PhysicalBone3D_DampMode>`)
-   `DampMode<enum_PhysicalBone3D_DampMode>`
    **get\_linear\_damp\_mode**()

Defines how `linear_damp<class_PhysicalBone3D_property_linear_damp>` is
applied. See `DampMode<enum_PhysicalBone3D_DampMode>` for possible
values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **linear\_velocity** = `Vector3(0, 0, 0)`
`🔗<class_PhysicalBone3D_property_linear_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_linear\_velocity**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_linear\_velocity**()

The body's linear velocity in units per second. Can be used
sporadically, but **don't set this every frame**, because physics may
run in another thread and runs at a different granularity. Use
`_integrate_forces<class_PhysicalBone3D_private_method__integrate_forces>`
as your process loop for precise control of the body state.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **mass** = `1.0`
`🔗<class_PhysicalBone3D_property_mass>`

classref-property-setget

-   `void (No return value.)` **set\_mass**(value: `float<class_float>`)
-   `float<class_float>` **get\_mass**()

The body's mass.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_integrate\_forces**(state:
`PhysicsDirectBodyState3D<class_PhysicsDirectBodyState3D>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicalBone3D_private_method__integrate_forces>`

Called during physics processing, allowing you to read and safely modify
the simulation state for the object. By default, it is called before the
standard force integration, but the
`custom_integrator<class_PhysicalBone3D_property_custom_integrator>`
property allows you to disable the standard force integration and do
fully custom force integration for a body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_central\_impulse**(impulse:
`Vector3<class_Vector3>`)
`🔗<class_PhysicalBone3D_method_apply_central_impulse>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_impulse**(impulse:
`Vector3<class_Vector3>`, position: `Vector3<class_Vector3>` =
Vector3(0, 0, 0)) `🔗<class_PhysicalBone3D_method_apply_impulse>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_bone\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicalBone3D_method_get_bone_id>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_simulate\_physics**()
`🔗<class_PhysicalBone3D_method_get_simulate_physics>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_simulating\_physics**()
`🔗<class_PhysicalBone3D_method_is_simulating_physics>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
