github\_url  
hide

# RigidBody3D

**Inherits:** `PhysicsBody3D<class_PhysicsBody3D>` **&lt;**
`CollisionObject3D<class_CollisionObject3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `VehicleBody3D<class_VehicleBody3D>`

A 3D physics body that is moved by a physics simulation.

classref-introduction-group

## Description

**RigidBody3D** implements full 3D physics. It cannot be controlled
directly, instead, you must apply forces to it (gravity, impulses,
etc.), and the physics simulation will calculate the resulting movement,
rotation, react to collisions, and affect other physics bodies in its
path.

The body's behavior can be adjusted via
`lock_rotation<class_RigidBody3D_property_lock_rotation>`,
`freeze<class_RigidBody3D_property_freeze>`, and
`freeze_mode<class_RigidBody3D_property_freeze_mode>`. By changing
various properties of the object, such as
`mass<class_RigidBody3D_property_mass>`, you can control how the physics
simulation acts on it.

A rigid body will always maintain its shape and size, even when forces
are applied to it. It is useful for objects that can be interacted with
in an environment, such as a tree that can be knocked over or a stack of
crates that can be pushed around.

If you need to override the default physics behavior, you can write a
custom force integration function. See
`custom_integrator<class_RigidBody3D_property_custom_integrator>`.

\*\*Note:\*\* Changing the 3D transform or
`linear_velocity<class_RigidBody3D_property_linear_velocity>` of a
**RigidBody3D** very often may lead to some unpredictable behaviors. If
you need to directly affect the body, prefer
`_integrate_forces<class_RigidBody3D_private_method__integrate_forces>`
as it allows you to directly access the physics state.

classref-introduction-group

## Tutorials

-   `Physics introduction <../tutorials/physics/physics_introduction>`
-   [3D Truck Town
    Demo](https://godotengine.org/asset-library/asset/2752)
-   [3D Physics Tests
    Demo](https://godotengine.org/asset-library/asset/2747)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**body\_entered**(body: `Node<class_Node>`)
`🔗<class_RigidBody3D_signal_body_entered>`

Emitted when a collision with another
`PhysicsBody3D<class_PhysicsBody3D>` or `GridMap<class_GridMap>` occurs.
Requires `contact_monitor<class_RigidBody3D_property_contact_monitor>`
to be set to `true` and
`max_contacts_reported<class_RigidBody3D_property_max_contacts_reported>`
to be set high enough to detect all the collisions.
`GridMap<class_GridMap>`s are detected if the
`MeshLibrary<class_MeshLibrary>` has Collision
`Shape3D<class_Shape3D>`s.

`body` the `Node<class_Node>`, if it exists in the tree, of the other
`PhysicsBody3D<class_PhysicsBody3D>` or `GridMap<class_GridMap>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**body\_exited**(body: `Node<class_Node>`)
`🔗<class_RigidBody3D_signal_body_exited>`

Emitted when the collision with another
`PhysicsBody3D<class_PhysicsBody3D>` or `GridMap<class_GridMap>` ends.
Requires `contact_monitor<class_RigidBody3D_property_contact_monitor>`
to be set to `true` and
`max_contacts_reported<class_RigidBody3D_property_max_contacts_reported>`
to be set high enough to detect all the collisions.
`GridMap<class_GridMap>`s are detected if the
`MeshLibrary<class_MeshLibrary>` has Collision
`Shape3D<class_Shape3D>`s.

`body` the `Node<class_Node>`, if it exists in the tree, of the other
`PhysicsBody3D<class_PhysicsBody3D>` or `GridMap<class_GridMap>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**body\_shape\_entered**(body\_rid: `RID<class_RID>`, body:
`Node<class_Node>`, body\_shape\_index: `int<class_int>`,
local\_shape\_index: `int<class_int>`)
`🔗<class_RigidBody3D_signal_body_shape_entered>`

Emitted when one of this RigidBody3D's `Shape3D<class_Shape3D>`s
collides with another `PhysicsBody3D<class_PhysicsBody3D>` or
`GridMap<class_GridMap>`'s `Shape3D<class_Shape3D>`s. Requires
`contact_monitor<class_RigidBody3D_property_contact_monitor>` to be set
to `true` and
`max_contacts_reported<class_RigidBody3D_property_max_contacts_reported>`
to be set high enough to detect all the collisions.
`GridMap<class_GridMap>`s are detected if the
`MeshLibrary<class_MeshLibrary>` has Collision
`Shape3D<class_Shape3D>`s.

`body_rid` the `RID<class_RID>` of the other
`PhysicsBody3D<class_PhysicsBody3D>` or
`MeshLibrary<class_MeshLibrary>`'s
`CollisionObject3D<class_CollisionObject3D>` used by the
`PhysicsServer3D<class_PhysicsServer3D>`.

`body` the `Node<class_Node>`, if it exists in the tree, of the other
`PhysicsBody3D<class_PhysicsBody3D>` or `GridMap<class_GridMap>`.

`body_shape_index` the index of the `Shape3D<class_Shape3D>` of the
other `PhysicsBody3D<class_PhysicsBody3D>` or `GridMap<class_GridMap>`
used by the `PhysicsServer3D<class_PhysicsServer3D>`. Get the
`CollisionShape3D<class_CollisionShape3D>` node with
`body.shape_owner_get_owner(body.shape_find_owner(body_shape_index))`.

`local_shape_index` the index of the `Shape3D<class_Shape3D>` of this
RigidBody3D used by the `PhysicsServer3D<class_PhysicsServer3D>`. Get
the `CollisionShape3D<class_CollisionShape3D>` node with
`self.shape_owner_get_owner(self.shape_find_owner(local_shape_index))`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**body\_shape\_exited**(body\_rid: `RID<class_RID>`, body:
`Node<class_Node>`, body\_shape\_index: `int<class_int>`,
local\_shape\_index: `int<class_int>`)
`🔗<class_RigidBody3D_signal_body_shape_exited>`

Emitted when the collision between one of this RigidBody3D's
`Shape3D<class_Shape3D>`s and another
`PhysicsBody3D<class_PhysicsBody3D>` or `GridMap<class_GridMap>`'s
`Shape3D<class_Shape3D>`s ends. Requires
`contact_monitor<class_RigidBody3D_property_contact_monitor>` to be set
to `true` and
`max_contacts_reported<class_RigidBody3D_property_max_contacts_reported>`
to be set high enough to detect all the collisions.
`GridMap<class_GridMap>`s are detected if the
`MeshLibrary<class_MeshLibrary>` has Collision
`Shape3D<class_Shape3D>`s.

`body_rid` the `RID<class_RID>` of the other
`PhysicsBody3D<class_PhysicsBody3D>` or
`MeshLibrary<class_MeshLibrary>`'s
`CollisionObject3D<class_CollisionObject3D>` used by the
`PhysicsServer3D<class_PhysicsServer3D>`. `GridMap<class_GridMap>`s are
detected if the Meshes have `Shape3D<class_Shape3D>`s.

`body` the `Node<class_Node>`, if it exists in the tree, of the other
`PhysicsBody3D<class_PhysicsBody3D>` or `GridMap<class_GridMap>`.

`body_shape_index` the index of the `Shape3D<class_Shape3D>` of the
other `PhysicsBody3D<class_PhysicsBody3D>` or `GridMap<class_GridMap>`
used by the `PhysicsServer3D<class_PhysicsServer3D>`. Get the
`CollisionShape3D<class_CollisionShape3D>` node with
`body.shape_owner_get_owner(body.shape_find_owner(body_shape_index))`.

`local_shape_index` the index of the `Shape3D<class_Shape3D>` of this
RigidBody3D used by the `PhysicsServer3D<class_PhysicsServer3D>`. Get
the `CollisionShape3D<class_CollisionShape3D>` node with
`self.shape_owner_get_owner(self.shape_find_owner(local_shape_index))`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**sleeping\_state\_changed**()
`🔗<class_RigidBody3D_signal_sleeping_state_changed>`

Emitted when the physics engine changes the body's sleeping state.

\*\*Note:\*\* Changing the value
`sleeping<class_RigidBody3D_property_sleeping>` will not trigger this
signal. It is only emitted if the sleeping state is changed by the
physics engine or `emit_signal("sleeping_state_changed")` is used.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **FreezeMode**: `🔗<enum_RigidBody3D_FreezeMode>`

classref-enumeration-constant

`FreezeMode<enum_RigidBody3D_FreezeMode>` **FREEZE\_MODE\_STATIC** = `0`

Static body freeze mode (default). The body is not affected by gravity
and forces. It can be only moved by user code and doesn't collide with
other bodies along its path.

classref-enumeration-constant

`FreezeMode<enum_RigidBody3D_FreezeMode>` **FREEZE\_MODE\_KINEMATIC** =
`1`

Kinematic body freeze mode. Similar to
`FREEZE_MODE_STATIC<class_RigidBody3D_constant_FREEZE_MODE_STATIC>`, but
collides with other bodies along its path when moved. Useful for a
frozen body that needs to be animated.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CenterOfMassMode**: `🔗<enum_RigidBody3D_CenterOfMassMode>`

classref-enumeration-constant

`CenterOfMassMode<enum_RigidBody3D_CenterOfMassMode>`
**CENTER\_OF\_MASS\_MODE\_AUTO** = `0`

In this mode, the body's center of mass is calculated automatically
based on its shapes. This assumes that the shapes' origins are also
their center of mass.

classref-enumeration-constant

`CenterOfMassMode<enum_RigidBody3D_CenterOfMassMode>`
**CENTER\_OF\_MASS\_MODE\_CUSTOM** = `1`

In this mode, the body's center of mass is set through
`center_of_mass<class_RigidBody3D_property_center_of_mass>`. Defaults to
the body's origin position.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DampMode**: `🔗<enum_RigidBody3D_DampMode>`

classref-enumeration-constant

`DampMode<enum_RigidBody3D_DampMode>` **DAMP\_MODE\_COMBINE** = `0`

In this mode, the body's damping value is added to any value set in
areas or the default value.

classref-enumeration-constant

`DampMode<enum_RigidBody3D_DampMode>` **DAMP\_MODE\_REPLACE** = `1`

In this mode, the body's damping value replaces any value set in areas
or the default value.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **angular\_damp** = `0.0`
`🔗<class_RigidBody3D_property_angular_damp>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_damp**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_angular\_damp**()

Damps the body's rotation. By default, the body will use the **Default
Angular Damp** in **Project &gt; Project Settings &gt; Physics &gt; 3d**
or any value override set by an `Area3D<class_Area3D>` the body is in.
Depending on
`angular_damp_mode<class_RigidBody3D_property_angular_damp_mode>`, you
can set `angular_damp<class_RigidBody3D_property_angular_damp>` to be
added to or to replace the body's damping value.

See
`ProjectSettings.physics/3d/default_angular_damp<class_ProjectSettings_property_physics/3d/default_angular_damp>`
for more details about damping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DampMode<enum_RigidBody3D_DampMode>` **angular\_damp\_mode** = `0`
`🔗<class_RigidBody3D_property_angular_damp_mode>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_damp\_mode**(value:
    `DampMode<enum_RigidBody3D_DampMode>`)
-   `DampMode<enum_RigidBody3D_DampMode>` **get\_angular\_damp\_mode**()

Defines how `angular_damp<class_RigidBody3D_property_angular_damp>` is
applied. See `DampMode<enum_RigidBody3D_DampMode>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **angular\_velocity** = `Vector3(0, 0, 0)`
`🔗<class_RigidBody3D_property_angular_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_velocity**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_angular\_velocity**()

The RigidBody3D's rotational velocity in *radians* per second.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **can\_sleep** = `true`
`🔗<class_RigidBody3D_property_can_sleep>`

classref-property-setget

-   `void (No return value.)` **set\_can\_sleep**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_able\_to\_sleep**()

If `true`, the body can enter sleep mode when there is no movement. See
`sleeping<class_RigidBody3D_property_sleeping>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **center\_of\_mass** = `Vector3(0, 0, 0)`
`🔗<class_RigidBody3D_property_center_of_mass>`

classref-property-setget

-   `void (No return value.)` **set\_center\_of\_mass**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_center\_of\_mass**()

The body's custom center of mass, relative to the body's origin
position, when
`center_of_mass_mode<class_RigidBody3D_property_center_of_mass_mode>` is
set to
`CENTER_OF_MASS_MODE_CUSTOM<class_RigidBody3D_constant_CENTER_OF_MASS_MODE_CUSTOM>`.
This is the balanced point of the body, where applied forces only cause
linear acceleration. Applying forces outside of the center of mass
causes angular acceleration.

When
`center_of_mass_mode<class_RigidBody3D_property_center_of_mass_mode>` is
set to
`CENTER_OF_MASS_MODE_AUTO<class_RigidBody3D_constant_CENTER_OF_MASS_MODE_AUTO>`
(default value), the center of mass is automatically computed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CenterOfMassMode<enum_RigidBody3D_CenterOfMassMode>`
**center\_of\_mass\_mode** = `0`
`🔗<class_RigidBody3D_property_center_of_mass_mode>`

classref-property-setget

-   `void (No return value.)` **set\_center\_of\_mass\_mode**(value:
    `CenterOfMassMode<enum_RigidBody3D_CenterOfMassMode>`)
-   `CenterOfMassMode<enum_RigidBody3D_CenterOfMassMode>`
    **get\_center\_of\_mass\_mode**()

Defines the way the body's center of mass is set. See
`CenterOfMassMode<enum_RigidBody3D_CenterOfMassMode>` for possible
values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **constant\_force** = `Vector3(0, 0, 0)`
`🔗<class_RigidBody3D_property_constant_force>`

classref-property-setget

-   `void (No return value.)` **set\_constant\_force**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_constant\_force**()

The body's total constant positional forces applied during each physics
update.

See `add_constant_force<class_RigidBody3D_method_add_constant_force>`
and
`add_constant_central_force<class_RigidBody3D_method_add_constant_central_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **constant\_torque** = `Vector3(0, 0, 0)`
`🔗<class_RigidBody3D_property_constant_torque>`

classref-property-setget

-   `void (No return value.)` **set\_constant\_torque**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_constant\_torque**()

The body's total constant rotational forces applied during each physics
update.

See `add_constant_torque<class_RigidBody3D_method_add_constant_torque>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **contact\_monitor** = `false`
`🔗<class_RigidBody3D_property_contact_monitor>`

classref-property-setget

-   `void (No return value.)` **set\_contact\_monitor**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_contact\_monitor\_enabled**()

If `true`, the RigidBody3D will emit signals when it collides with
another body.

\*\*Note:\*\* By default the maximum contacts reported is set to 0,
meaning nothing will be recorded, see
`max_contacts_reported<class_RigidBody3D_property_max_contacts_reported>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **continuous\_cd** = `false`
`🔗<class_RigidBody3D_property_continuous_cd>`

classref-property-setget

-   `void (No return value.)`
    **set\_use\_continuous\_collision\_detection**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_continuous\_collision\_detection**()

If `true`, continuous collision detection is used.

Continuous collision detection tries to predict where a moving body will
collide, instead of moving it and correcting its movement if it
collided. Continuous collision detection is more precise, and misses
fewer impacts by small, fast-moving objects. Not using continuous
collision detection is faster to compute, but can miss small,
fast-moving objects.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **custom\_integrator** = `false`
`🔗<class_RigidBody3D_property_custom_integrator>`

classref-property-setget

-   `void (No return value.)` **set\_use\_custom\_integrator**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_custom\_integrator**()

If `true`, the standard force integration (like gravity or damping) will
be disabled for this body. Other than collision response, the body will
only move as determined by the
`_integrate_forces<class_RigidBody3D_private_method__integrate_forces>`
method, if that virtual method is overridden.

Setting this property will call the method
`PhysicsServer3D.body_set_omit_force_integration<class_PhysicsServer3D_method_body_set_omit_force_integration>`
internally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **freeze** = `false`
`🔗<class_RigidBody3D_property_freeze>`

classref-property-setget

-   `void (No return value.)` **set\_freeze\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_freeze\_enabled**()

If `true`, the body is frozen. Gravity and forces are not applied
anymore.

See `freeze_mode<class_RigidBody3D_property_freeze_mode>` to set the
body's behavior when frozen.

For a body that is always frozen, use `StaticBody3D<class_StaticBody3D>`
or `AnimatableBody3D<class_AnimatableBody3D>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`FreezeMode<enum_RigidBody3D_FreezeMode>` **freeze\_mode** = `0`
`🔗<class_RigidBody3D_property_freeze_mode>`

classref-property-setget

-   `void (No return value.)` **set\_freeze\_mode**(value:
    `FreezeMode<enum_RigidBody3D_FreezeMode>`)
-   `FreezeMode<enum_RigidBody3D_FreezeMode>` **get\_freeze\_mode**()

The body's freeze mode. Can be used to set the body's behavior when
`freeze<class_RigidBody3D_property_freeze>` is enabled. See
`FreezeMode<enum_RigidBody3D_FreezeMode>` for possible values.

For a body that is always frozen, use `StaticBody3D<class_StaticBody3D>`
or `AnimatableBody3D<class_AnimatableBody3D>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **gravity\_scale** = `1.0`
`🔗<class_RigidBody3D_property_gravity_scale>`

classref-property-setget

-   `void (No return value.)` **set\_gravity\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_gravity\_scale**()

This is multiplied by the global 3D gravity setting found in **Project
&gt; Project Settings &gt; Physics &gt; 3d** to produce RigidBody3D's
gravity. For example, a value of 1 will be normal gravity, 2 will apply
double gravity, and 0.5 will apply half gravity to this object.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **inertia** = `Vector3(0, 0, 0)`
`🔗<class_RigidBody3D_property_inertia>`

classref-property-setget

-   `void (No return value.)` **set\_inertia**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_inertia**()

The body's moment of inertia. This is like mass, but for rotation: it
determines how much torque it takes to rotate the body on each axis. The
moment of inertia is usually computed automatically from the mass and
the shapes, but this property allows you to set a custom value.

If set to `Vector3.ZERO<class_Vector3_constant_ZERO>`, inertia is
automatically computed (default value).

\*\*Note:\*\* This value does not change when inertia is automatically
computed. Use `PhysicsServer3D<class_PhysicsServer3D>` to get the
computed inertia.

gdscript

@onready var ball = $Ball

func get\_ball\_inertia():  
return
PhysicsServer3D.body\_get\_direct\_state(ball.get\_rid()).inverse\_inertia.inverse()

csharp

private RigidBody3D \_ball;

public override void \_Ready() { \_ball =
GetNode&lt;RigidBody3D&gt;("Ball"); }

private Vector3 GetBallInertia() { return
PhysicsServer3D.BodyGetDirectState(\_ball.GetRid()).InverseInertia.Inverse();
}

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_damp** = `0.0`
`🔗<class_RigidBody3D_property_linear_damp>`

classref-property-setget

-   `void (No return value.)` **set\_linear\_damp**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_linear\_damp**()

Damps the body's movement. By default, the body will use the **Default
Linear Damp** in **Project &gt; Project Settings &gt; Physics &gt; 3d**
or any value override set by an `Area3D<class_Area3D>` the body is in.
Depending on
`linear_damp_mode<class_RigidBody3D_property_linear_damp_mode>`, you can
set `linear_damp<class_RigidBody3D_property_linear_damp>` to be added to
or to replace the body's damping value.

See
`ProjectSettings.physics/3d/default_linear_damp<class_ProjectSettings_property_physics/3d/default_linear_damp>`
for more details about damping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DampMode<enum_RigidBody3D_DampMode>` **linear\_damp\_mode** = `0`
`🔗<class_RigidBody3D_property_linear_damp_mode>`

classref-property-setget

-   `void (No return value.)` **set\_linear\_damp\_mode**(value:
    `DampMode<enum_RigidBody3D_DampMode>`)
-   `DampMode<enum_RigidBody3D_DampMode>` **get\_linear\_damp\_mode**()

Defines how `linear_damp<class_RigidBody3D_property_linear_damp>` is
applied. See `DampMode<enum_RigidBody3D_DampMode>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **linear\_velocity** = `Vector3(0, 0, 0)`
`🔗<class_RigidBody3D_property_linear_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_linear\_velocity**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_linear\_velocity**()

The body's linear velocity in units per second. Can be used
sporadically, but **don't set this every frame**, because physics may
run in another thread and runs at a different granularity. Use
`_integrate_forces<class_RigidBody3D_private_method__integrate_forces>`
as your process loop for precise control of the body state.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **lock\_rotation** = `false`
`🔗<class_RigidBody3D_property_lock_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_lock\_rotation\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_lock\_rotation\_enabled**()

If `true`, the body cannot rotate. Gravity and forces only apply linear
movement.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **mass** = `1.0`
`🔗<class_RigidBody3D_property_mass>`

classref-property-setget

-   `void (No return value.)` **set\_mass**(value: `float<class_float>`)
-   `float<class_float>` **get\_mass**()

The body's mass.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_contacts\_reported** = `0`
`🔗<class_RigidBody3D_property_max_contacts_reported>`

classref-property-setget

-   `void (No return value.)` **set\_max\_contacts\_reported**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_contacts\_reported**()

The maximum number of contacts that will be recorded. Requires a value
greater than 0 and
`contact_monitor<class_RigidBody3D_property_contact_monitor>` to be set
to `true` to start to register contacts. Use
`get_contact_count<class_RigidBody3D_method_get_contact_count>` to
retrieve the count or
`get_colliding_bodies<class_RigidBody3D_method_get_colliding_bodies>` to
retrieve bodies that have been collided with.

\*\*Note:\*\* The number of contacts is different from the number of
collisions. Collisions between parallel edges will result in two
contacts (one at each end), and collisions between parallel faces will
result in four contacts (one at each corner).

classref-item-separator

------------------------------------------------------------------------

classref-property

`PhysicsMaterial<class_PhysicsMaterial>` **physics\_material\_override**
`🔗<class_RigidBody3D_property_physics_material_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_physics\_material\_override**(value:
    `PhysicsMaterial<class_PhysicsMaterial>`)
-   `PhysicsMaterial<class_PhysicsMaterial>`
    **get\_physics\_material\_override**()

The physics material override for the body.

If a material is assigned to this property, it will be used instead of
any other physics material, such as an inherited one.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **sleeping** = `false`
`🔗<class_RigidBody3D_property_sleeping>`

classref-property-setget

-   `void (No return value.)` **set\_sleeping**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_sleeping**()

If `true`, the body will not move and will not calculate forces until
woken up by another body through, for example, a collision, or by using
the `apply_impulse<class_RigidBody3D_method_apply_impulse>` or
`apply_force<class_RigidBody3D_method_apply_force>` methods.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_integrate\_forces**(state:
`PhysicsDirectBodyState3D<class_PhysicsDirectBodyState3D>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_RigidBody3D_private_method__integrate_forces>`

Called during physics processing, allowing you to read and safely modify
the simulation state for the object. By default, it is called before the
standard force integration, but the
`custom_integrator<class_RigidBody3D_property_custom_integrator>`
property allows you to disable the standard force integration and do
fully custom force integration for a body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_constant\_central\_force**(force:
`Vector3<class_Vector3>`)
`🔗<class_RigidBody3D_method_add_constant_central_force>`

Adds a constant directional force without affecting rotation that keeps
being applied over time until cleared with
`constant_force = Vector3(0, 0, 0)`.

This is equivalent to using
`add_constant_force<class_RigidBody3D_method_add_constant_force>` at the
body's center of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_constant\_force**(force:
`Vector3<class_Vector3>`, position: `Vector3<class_Vector3>` =
Vector3(0, 0, 0)) `🔗<class_RigidBody3D_method_add_constant_force>`

Adds a constant positioned force to the body that keeps being applied
over time until cleared with `constant_force = Vector3(0, 0, 0)`.

`position` is the offset from the body origin in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_constant\_torque**(torque:
`Vector3<class_Vector3>`)
`🔗<class_RigidBody3D_method_add_constant_torque>`

Adds a constant rotational force without affecting position that keeps
being applied over time until cleared with
`constant_torque = Vector3(0, 0, 0)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_central\_force**(force:
`Vector3<class_Vector3>`)
`🔗<class_RigidBody3D_method_apply_central_force>`

Applies a directional force without affecting rotation. A force is time
dependent and meant to be applied every physics update.

This is equivalent to using
`apply_force<class_RigidBody3D_method_apply_force>` at the body's center
of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_central\_impulse**(impulse:
`Vector3<class_Vector3>`)
`🔗<class_RigidBody3D_method_apply_central_impulse>`

Applies a directional impulse without affecting rotation.

An impulse is time-independent! Applying an impulse every frame would
result in a framerate-dependent force. For this reason, it should only
be used when simulating one-time impacts (use the "\_force" functions
otherwise).

This is equivalent to using
`apply_impulse<class_RigidBody3D_method_apply_impulse>` at the body's
center of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_force**(force:
`Vector3<class_Vector3>`, position: `Vector3<class_Vector3>` =
Vector3(0, 0, 0)) `🔗<class_RigidBody3D_method_apply_force>`

Applies a positioned force to the body. A force is time dependent and
meant to be applied every physics update.

`position` is the offset from the body origin in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_impulse**(impulse:
`Vector3<class_Vector3>`, position: `Vector3<class_Vector3>` =
Vector3(0, 0, 0)) `🔗<class_RigidBody3D_method_apply_impulse>`

Applies a positioned impulse to the body.

An impulse is time-independent! Applying an impulse every frame would
result in a framerate-dependent force. For this reason, it should only
be used when simulating one-time impacts (use the "\_force" functions
otherwise).

`position` is the offset from the body origin in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_torque**(torque:
`Vector3<class_Vector3>`) `🔗<class_RigidBody3D_method_apply_torque>`

Applies a rotational force without affecting position. A force is time
dependent and meant to be applied every physics update.

\*\*Note:\*\* `inertia<class_RigidBody3D_property_inertia>` is required
for this to work. To have `inertia<class_RigidBody3D_property_inertia>`,
an active `CollisionShape3D<class_CollisionShape3D>` must be a child of
the node, or you can manually set
`inertia<class_RigidBody3D_property_inertia>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_torque\_impulse**(impulse:
`Vector3<class_Vector3>`)
`🔗<class_RigidBody3D_method_apply_torque_impulse>`

Applies a rotational impulse to the body without affecting the position.

An impulse is time-independent! Applying an impulse every frame would
result in a framerate-dependent force. For this reason, it should only
be used when simulating one-time impacts (use the "\_force" functions
otherwise).

\*\*Note:\*\* `inertia<class_RigidBody3D_property_inertia>` is required
for this to work. To have `inertia<class_RigidBody3D_property_inertia>`,
an active `CollisionShape3D<class_CollisionShape3D>` must be a child of
the node, or you can manually set
`inertia<class_RigidBody3D_property_inertia>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Node3D<class_Node3D>`\]
**get\_colliding\_bodies**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RigidBody3D_method_get_colliding_bodies>`

Returns a list of the bodies colliding with this one. Requires
`contact_monitor<class_RigidBody3D_property_contact_monitor>` to be set
to `true` and
`max_contacts_reported<class_RigidBody3D_property_max_contacts_reported>`
to be set high enough to detect all the collisions.

\*\*Note:\*\* The result of this test is not immediate after moving
objects. For performance, list of collisions is updated once per frame
and before the physics step. Consider using signals instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_contact\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RigidBody3D_method_get_contact_count>`

Returns the number of contacts this body has with other bodies. By
default, this returns 0 unless bodies are configured to monitor contacts
(see `contact_monitor<class_RigidBody3D_property_contact_monitor>`).

\*\*Note:\*\* To retrieve the colliding bodies, use
`get_colliding_bodies<class_RigidBody3D_method_get_colliding_bodies>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Basis<class_Basis>` **get\_inverse\_inertia\_tensor**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RigidBody3D_method_get_inverse_inertia_tensor>`

Returns the inverse inertia tensor basis. This is used to calculate the
angular acceleration resulting from a torque applied to the
**RigidBody3D**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_axis\_velocity**(axis\_velocity:
`Vector3<class_Vector3>`)
`🔗<class_RigidBody3D_method_set_axis_velocity>`

Sets an axis velocity. The velocity in the given vector axis will be set
as the given vector length. This is useful for jumping behavior.
