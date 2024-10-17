github\_url  
hide

# PhysicsDirectBodyState2D

**Inherits:** `Object<class_Object>`

**Inherited By:**
`PhysicsDirectBodyState2DExtension<class_PhysicsDirectBodyState2DExtension>`

Provides direct access to a physics body in the
`PhysicsServer2D<class_PhysicsServer2D>`.

classref-introduction-group

## Description

Provides direct access to a physics body in the
`PhysicsServer2D<class_PhysicsServer2D>`, allowing safe changes to
physics properties. This object is passed via the direct state callback
of `RigidBody2D<class_RigidBody2D>`, and is intended for changing the
direct state of that body. See
`RigidBody2D._integrate_forces<class_RigidBody2D_private_method__integrate_forces>`.

classref-introduction-group

## Tutorials

-   `Physics introduction <../tutorials/physics/physics_introduction>`
-   `Ray-casting <../tutorials/physics/ray-casting>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **angular\_velocity**
`🔗<class_PhysicsDirectBodyState2D_property_angular_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_velocity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_angular\_velocity**()

The body's rotational velocity in *radians* per second.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **center\_of\_mass**
`🔗<class_PhysicsDirectBodyState2D_property_center_of_mass>`

classref-property-setget

-   `Vector2<class_Vector2>` **get\_center\_of\_mass**()

The body's center of mass position relative to the body's center in the
global coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **center\_of\_mass\_local**
`🔗<class_PhysicsDirectBodyState2D_property_center_of_mass_local>`

classref-property-setget

-   `Vector2<class_Vector2>` **get\_center\_of\_mass\_local**()

The body's center of mass position in the body's local coordinate
system.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **inverse\_inertia**
`🔗<class_PhysicsDirectBodyState2D_property_inverse_inertia>`

classref-property-setget

-   `float<class_float>` **get\_inverse\_inertia**()

The inverse of the inertia of the body.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **inverse\_mass**
`🔗<class_PhysicsDirectBodyState2D_property_inverse_mass>`

classref-property-setget

-   `float<class_float>` **get\_inverse\_mass**()

The inverse of the mass of the body.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **linear\_velocity**
`🔗<class_PhysicsDirectBodyState2D_property_linear_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_linear\_velocity**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_linear\_velocity**()

The body's linear velocity in pixels per second.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **sleeping**
`🔗<class_PhysicsDirectBodyState2D_property_sleeping>`

classref-property-setget

-   `void (No return value.)` **set\_sleep\_state**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_sleeping**()

If `true`, this body is currently sleeping (not active).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **step**
`🔗<class_PhysicsDirectBodyState2D_property_step>`

classref-property-setget

-   `float<class_float>` **get\_step**()

The timestep (delta) used for the simulation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **total\_angular\_damp**
`🔗<class_PhysicsDirectBodyState2D_property_total_angular_damp>`

classref-property-setget

-   `float<class_float>` **get\_total\_angular\_damp**()

The rate at which the body stops rotating, if there are not any other
forces moving it.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **total\_gravity**
`🔗<class_PhysicsDirectBodyState2D_property_total_gravity>`

classref-property-setget

-   `Vector2<class_Vector2>` **get\_total\_gravity**()

The total gravity vector being currently applied to this body.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **total\_linear\_damp**
`🔗<class_PhysicsDirectBodyState2D_property_total_linear_damp>`

classref-property-setget

-   `float<class_float>` **get\_total\_linear\_damp**()

The rate at which the body stops moving, if there are not any other
forces moving it.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform2D<class_Transform2D>` **transform**
`🔗<class_PhysicsDirectBodyState2D_property_transform>`

classref-property-setget

-   `void (No return value.)` **set\_transform**(value:
    `Transform2D<class_Transform2D>`)
-   `Transform2D<class_Transform2D>` **get\_transform**()

The body's transformation matrix.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_constant\_central\_force**(force:
`Vector2<class_Vector2>` = Vector2(0, 0))
`🔗<class_PhysicsDirectBodyState2D_method_add_constant_central_force>`

Adds a constant directional force without affecting rotation that keeps
being applied over time until cleared with
`constant_force = Vector2(0, 0)`.

This is equivalent to using
`add_constant_force<class_PhysicsDirectBodyState2D_method_add_constant_force>`
at the body's center of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_constant\_force**(force:
`Vector2<class_Vector2>`, position: `Vector2<class_Vector2>` =
Vector2(0, 0))
`🔗<class_PhysicsDirectBodyState2D_method_add_constant_force>`

Adds a constant positioned force to the body that keeps being applied
over time until cleared with `constant_force = Vector2(0, 0)`.

`position` is the offset from the body origin in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_constant\_torque**(torque:
`float<class_float>`)
`🔗<class_PhysicsDirectBodyState2D_method_add_constant_torque>`

Adds a constant rotational force without affecting position that keeps
being applied over time until cleared with `constant_torque = 0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_central\_force**(force:
`Vector2<class_Vector2>` = Vector2(0, 0))
`🔗<class_PhysicsDirectBodyState2D_method_apply_central_force>`

Applies a directional force without affecting rotation. A force is time
dependent and meant to be applied every physics update.

This is equivalent to using
`apply_force<class_PhysicsDirectBodyState2D_method_apply_force>` at the
body's center of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_central\_impulse**(impulse:
`Vector2<class_Vector2>`)
`🔗<class_PhysicsDirectBodyState2D_method_apply_central_impulse>`

Applies a directional impulse without affecting rotation.

An impulse is time-independent! Applying an impulse every frame would
result in a framerate-dependent force. For this reason, it should only
be used when simulating one-time impacts (use the "\_force" functions
otherwise).

This is equivalent to using
`apply_impulse<class_PhysicsDirectBodyState2D_method_apply_impulse>` at
the body's center of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_force**(force:
`Vector2<class_Vector2>`, position: `Vector2<class_Vector2>` =
Vector2(0, 0)) `🔗<class_PhysicsDirectBodyState2D_method_apply_force>`

Applies a positioned force to the body. A force is time dependent and
meant to be applied every physics update.

`position` is the offset from the body origin in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_impulse**(impulse:
`Vector2<class_Vector2>`, position: `Vector2<class_Vector2>` =
Vector2(0, 0)) `🔗<class_PhysicsDirectBodyState2D_method_apply_impulse>`

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
`float<class_float>`)
`🔗<class_PhysicsDirectBodyState2D_method_apply_torque>`

Applies a rotational force without affecting position. A force is time
dependent and meant to be applied every physics update.

\*\*Note:\*\*
`inverse_inertia<class_PhysicsDirectBodyState2D_property_inverse_inertia>`
is required for this to work. To have
`inverse_inertia<class_PhysicsDirectBodyState2D_property_inverse_inertia>`,
an active `CollisionShape2D<class_CollisionShape2D>` must be a child of
the node, or you can manually set
`inverse_inertia<class_PhysicsDirectBodyState2D_property_inverse_inertia>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **apply\_torque\_impulse**(impulse:
`float<class_float>`)
`🔗<class_PhysicsDirectBodyState2D_method_apply_torque_impulse>`

Applies a rotational impulse to the body without affecting the position.

An impulse is time-independent! Applying an impulse every frame would
result in a framerate-dependent force. For this reason, it should only
be used when simulating one-time impacts (use the "\_force" functions
otherwise).

\*\*Note:\*\*
`inverse_inertia<class_PhysicsDirectBodyState2D_property_inverse_inertia>`
is required for this to work. To have
`inverse_inertia<class_PhysicsDirectBodyState2D_property_inverse_inertia>`,
an active `CollisionShape2D<class_CollisionShape2D>` must be a child of
the node, or you can manually set
`inverse_inertia<class_PhysicsDirectBodyState2D_property_inverse_inertia>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_constant\_force**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_constant_force>`

Returns the body's total constant positional forces applied during each
physics update.

See
`add_constant_force<class_PhysicsDirectBodyState2D_method_add_constant_force>`
and
`add_constant_central_force<class_PhysicsDirectBodyState2D_method_add_constant_central_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_constant\_torque**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_constant_torque>`

Returns the body's total constant rotational forces applied during each
physics update.

See
`add_constant_torque<class_PhysicsDirectBodyState2D_method_add_constant_torque>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_contact\_collider**(contact\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_collider>`

Returns the collider's `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_contact\_collider\_id**(contact\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_collider_id>`

Returns the collider's object id.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Object<class_Object>` **get\_contact\_collider\_object**(contact\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_collider_object>`

Returns the collider object. This depends on how it was created (will
return a scene node if such was used to create it).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**get\_contact\_collider\_position**(contact\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_collider_position>`

Returns the position of the contact point on the collider in the global
coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_contact\_collider\_shape**(contact\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_collider_shape>`

Returns the collider's shape index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**get\_contact\_collider\_velocity\_at\_position**(contact\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_collider_velocity_at_position>`

Returns the velocity vector at the collider's contact point.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_contact\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_count>`

Returns the number of contacts this body has with other bodies.

\*\*Note:\*\* By default, this returns 0 unless bodies are configured to
monitor contacts. See
`RigidBody2D.contact_monitor<class_RigidBody2D_property_contact_monitor>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_contact\_impulse**(contact\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_impulse>`

Returns the impulse created by the contact.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_contact\_local\_normal**(contact\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_local_normal>`

Returns the local normal at the contact point.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_contact\_local\_position**(contact\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_local_position>`

Returns the position of the contact point on the body in the global
coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_contact\_local\_shape**(contact\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_local_shape>`

Returns the local shape index of the collision.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**get\_contact\_local\_velocity\_at\_position**(contact\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_contact_local_velocity_at_position>`

Returns the velocity vector at the body's contact point.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PhysicsDirectSpaceState2D<class_PhysicsDirectSpaceState2D>`
**get\_space\_state**()
`🔗<class_PhysicsDirectBodyState2D_method_get_space_state>`

Returns the current state of the space, useful for queries.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**get\_velocity\_at\_local\_position**(local\_position:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectBodyState2D_method_get_velocity_at_local_position>`

Returns the body's velocity at the given relative position, including
both translation and rotation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **integrate\_forces**()
`🔗<class_PhysicsDirectBodyState2D_method_integrate_forces>`

Updates the body's linear and angular velocity by applying gravity and
damping for the equivalent of one physics tick.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_constant\_force**(force:
`Vector2<class_Vector2>`)
`🔗<class_PhysicsDirectBodyState2D_method_set_constant_force>`

Sets the body's total constant positional forces applied during each
physics update.

See
`add_constant_force<class_PhysicsDirectBodyState2D_method_add_constant_force>`
and
`add_constant_central_force<class_PhysicsDirectBodyState2D_method_add_constant_central_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_constant\_torque**(torque:
`float<class_float>`)
`🔗<class_PhysicsDirectBodyState2D_method_set_constant_torque>`

Sets the body's total constant rotational forces applied during each
physics update.

See
`add_constant_torque<class_PhysicsDirectBodyState2D_method_add_constant_torque>`.
