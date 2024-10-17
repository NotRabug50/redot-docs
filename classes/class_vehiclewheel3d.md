github\_url  
hide

# VehicleWheel3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A 3D physics body for a `VehicleBody3D<class_VehicleBody3D>` that
simulates the behavior of a wheel.

classref-introduction-group

## Description

A node used as a child of a `VehicleBody3D<class_VehicleBody3D>` parent
to simulate the behavior of one of its wheels. This node also acts as a
collider to detect if the wheel is touching a surface.

\*\*Note:\*\* This class has known issues and isn't designed to provide
realistic 3D vehicle physics. If you want advanced vehicle physics, you
may need to write your own physics integration using another
`PhysicsBody3D<class_PhysicsBody3D>` class.

classref-introduction-group

## Tutorials

-   [3D Truck Town
    Demo](https://godotengine.org/asset-library/asset/2752)

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

`float<class_float>` **brake** = `0.0`
`🔗<class_VehicleWheel3D_property_brake>`

classref-property-setget

-   `void (No return value.)` **set\_brake**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_brake**()

Slows down the wheel by applying a braking force. The wheel is only
slowed down if it is in contact with a surface. The force you need to
apply to adequately slow down your vehicle depends on the
`RigidBody3D.mass<class_RigidBody3D_property_mass>` of the vehicle. For
a vehicle with a mass set to 1000, try a value in the 25 - 30 range for
hard braking.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **damping\_compression** = `0.83`
`🔗<class_VehicleWheel3D_property_damping_compression>`

classref-property-setget

-   `void (No return value.)` **set\_damping\_compression**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_damping\_compression**()

The damping applied to the suspension spring when being compressed,
meaning when the wheel is moving up relative to the vehicle. It is
measured in Newton-seconds per millimeter (N⋅s/mm), or megagrams per
second (Mg/s). This value should be between 0.0 (no damping) and 1.0,
but may be more. A value of 0.0 means the car will keep bouncing as the
spring keeps its energy. A good value for this is around 0.3 for a
normal car, 0.5 for a race car.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **damping\_relaxation** = `0.88`
`🔗<class_VehicleWheel3D_property_damping_relaxation>`

classref-property-setget

-   `void (No return value.)` **set\_damping\_relaxation**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_damping\_relaxation**()

The damping applied to the suspension spring when rebounding or
extending, meaning when the wheel is moving down relative to the
vehicle. It is measured in Newton-seconds per millimeter (N⋅s/mm), or
megagrams per second (Mg/s). This value should be between 0.0 (no
damping) and 1.0, but may be more. This value should always be slightly
higher than the
`damping_compression<class_VehicleWheel3D_property_damping_compression>`
property. For a
`damping_compression<class_VehicleWheel3D_property_damping_compression>`
value of 0.3, try a relaxation value of 0.5.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **engine\_force** = `0.0`
`🔗<class_VehicleWheel3D_property_engine_force>`

classref-property-setget

-   `void (No return value.)` **set\_engine\_force**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_engine\_force**()

Accelerates the wheel by applying an engine force. The wheel is only
sped up if it is in contact with a surface. The
`RigidBody3D.mass<class_RigidBody3D_property_mass>` of the vehicle has
an effect on the acceleration of the vehicle. For a vehicle with a mass
set to 1000, try a value in the 25 - 50 range for acceleration.

\*\*Note:\*\* The simulation does not take the effect of gears into
account, you will need to add logic for this if you wish to simulate
gears.

A negative value will result in the wheel reversing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **steering** = `0.0`
`🔗<class_VehicleWheel3D_property_steering>`

classref-property-setget

-   `void (No return value.)` **set\_steering**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_steering**()

The steering angle for the wheel, in radians. Setting this to a non-zero
value will result in the vehicle turning when it's moving.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **suspension\_max\_force** = `6000.0`
`🔗<class_VehicleWheel3D_property_suspension_max_force>`

classref-property-setget

-   `void (No return value.)` **set\_suspension\_max\_force**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_suspension\_max\_force**()

The maximum force the spring can resist. This value should be higher
than a quarter of the
`RigidBody3D.mass<class_RigidBody3D_property_mass>` of the
`VehicleBody3D<class_VehicleBody3D>` or the spring will not carry the
weight of the vehicle. Good results are often obtained by a value that
is about 3× to 4× this number.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **suspension\_stiffness** = `5.88`
`🔗<class_VehicleWheel3D_property_suspension_stiffness>`

classref-property-setget

-   `void (No return value.)` **set\_suspension\_stiffness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_suspension\_stiffness**()

The stiffness of the suspension, measured in Newtons per millimeter
(N/mm), or megagrams per second squared (Mg/s²). Use a value lower than
50 for an off-road car, a value between 50 and 100 for a race car and
try something around 200 for something like a Formula 1 car.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **suspension\_travel** = `0.2`
`🔗<class_VehicleWheel3D_property_suspension_travel>`

classref-property-setget

-   `void (No return value.)` **set\_suspension\_travel**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_suspension\_travel**()

This is the distance the suspension can travel. As Godot units are
equivalent to meters, keep this setting relatively low. Try a value
between 0.1 and 0.3 depending on the type of car.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_as\_steering** = `false`
`🔗<class_VehicleWheel3D_property_use_as_steering>`

classref-property-setget

-   `void (No return value.)` **set\_use\_as\_steering**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_used\_as\_steering**()

If `true`, this wheel will be turned when the car steers. This value is
used in conjunction with
`VehicleBody3D.steering<class_VehicleBody3D_property_steering>` and
ignored if you are using the per-wheel
`steering<class_VehicleWheel3D_property_steering>` value instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_as\_traction** = `false`
`🔗<class_VehicleWheel3D_property_use_as_traction>`

classref-property-setget

-   `void (No return value.)` **set\_use\_as\_traction**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_used\_as\_traction**()

If `true`, this wheel transfers engine force to the ground to propel the
vehicle forward. This value is used in conjunction with
`VehicleBody3D.engine_force<class_VehicleBody3D_property_engine_force>`
and ignored if you are using the per-wheel
`engine_force<class_VehicleWheel3D_property_engine_force>` value
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **wheel\_friction\_slip** = `10.5`
`🔗<class_VehicleWheel3D_property_wheel_friction_slip>`

classref-property-setget

-   `void (No return value.)` **set\_friction\_slip**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_friction\_slip**()

This determines how much grip this wheel has. It is combined with the
friction setting of the surface the wheel is in contact with. 0.0 means
no grip, 1.0 is normal grip. For a drift car setup, try setting the grip
of the rear wheels slightly lower than the front wheels, or use a lower
value to simulate tire wear.

It's best to set this to 1.0 when starting out.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **wheel\_radius** = `0.5`
`🔗<class_VehicleWheel3D_property_wheel_radius>`

classref-property-setget

-   `void (No return value.)` **set\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_radius**()

The radius of the wheel in meters.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **wheel\_rest\_length** = `0.15`
`🔗<class_VehicleWheel3D_property_wheel_rest_length>`

classref-property-setget

-   `void (No return value.)` **set\_suspension\_rest\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_suspension\_rest\_length**()

This is the distance in meters the wheel is lowered from its origin
point. Don't set this to 0.0 and move the wheel into position, instead
move the origin point of your wheel (the gizmo in Godot) to the position
the wheel will take when bottoming out, then use the rest length to move
the wheel down to the position it should be in when the car is in rest.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **wheel\_roll\_influence** = `0.1`
`🔗<class_VehicleWheel3D_property_wheel_roll_influence>`

classref-property-setget

-   `void (No return value.)` **set\_roll\_influence**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_roll\_influence**()

This value affects the roll of your vehicle. If set to 1.0 for all
wheels, your vehicle will resist body roll, while a value of 0.0 will be
prone to rolling over.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Node3D<class_Node3D>` **get\_contact\_body**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VehicleWheel3D_method_get_contact_body>`

Returns the contacting body node if valid in the tree, as
`Node3D<class_Node3D>`. At the moment, `GridMap<class_GridMap>` is not
supported so the node will be always of type
`PhysicsBody3D<class_PhysicsBody3D>`.

Returns `null` if the wheel is not in contact with a surface, or the
contact body is not a `PhysicsBody3D<class_PhysicsBody3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_contact\_normal**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VehicleWheel3D_method_get_contact_normal>`

Returns the normal of the suspension's collision in world space if the
wheel is in contact. If the wheel isn't in contact with anything,
returns a vector pointing directly along the suspension axis toward the
vehicle in world space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_contact\_point**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VehicleWheel3D_method_get_contact_point>`

Returns the point of the suspension's collision in world space if the
wheel is in contact. If the wheel isn't in contact with anything,
returns the maximum point of the wheel's ray cast in world space, which
is defined by `wheel_rest_length + wheel_radius`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_rpm**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VehicleWheel3D_method_get_rpm>`

Returns the rotational speed of the wheel in revolutions per minute.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_skidinfo**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VehicleWheel3D_method_get_skidinfo>`

Returns a value between 0.0 and 1.0 that indicates whether this wheel is
skidding. 0.0 is skidding (the wheel has lost grip, e.g. icy terrain),
1.0 means not skidding (the wheel has full grip, e.g. dry asphalt road).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_in\_contact**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VehicleWheel3D_method_is_in_contact>`

Returns `true` if this wheel is in contact with a surface.
