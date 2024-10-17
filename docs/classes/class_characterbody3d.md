github\_url  
hide

# CharacterBody3D

**Inherits:** `PhysicsBody3D<class_PhysicsBody3D>` **&lt;**
`CollisionObject3D<class_CollisionObject3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A 3D physics body specialized for characters moved by script.

classref-introduction-group

## Description

**CharacterBody3D** is a specialized class for physics bodies that are
meant to be user-controlled. They are not affected by physics at all,
but they affect other physics bodies in their path. They are mainly used
to provide high-level API to move objects with wall and slope detection
(`move_and_slide<class_CharacterBody3D_method_move_and_slide>` method)
in addition to the general collision detection provided by
`PhysicsBody3D.move_and_collide<class_PhysicsBody3D_method_move_and_collide>`.
This makes it useful for highly configurable physics bodies that must
move in specific ways and collide with the world, as is often the case
with user-controlled characters.

For game objects that don't require complex movement or collision
detection, such as moving platforms,
`AnimatableBody3D<class_AnimatableBody3D>` is simpler to configure.

classref-introduction-group

## Tutorials

-   `Kinematic character (2D) <../tutorials/physics/kinematic_character_2d>`
-   [3D Kinematic Character
    Demo](https://godotengine.org/asset-library/asset/2739)
-   [3D Platformer
    Demo](https://godotengine.org/asset-library/asset/2748)
-   [3D Voxel Demo](https://godotengine.org/asset-library/asset/2755)
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **MotionMode**: `🔗<enum_CharacterBody3D_MotionMode>`

classref-enumeration-constant

`MotionMode<enum_CharacterBody3D_MotionMode>` **MOTION\_MODE\_GROUNDED**
= `0`

Apply when notions of walls, ceiling and floor are relevant. In this
mode the body motion will react to slopes (acceleration/slowdown). This
mode is suitable for grounded games like platformers.

classref-enumeration-constant

`MotionMode<enum_CharacterBody3D_MotionMode>` **MOTION\_MODE\_FLOATING**
= `1`

Apply when there is no notion of floor or ceiling. All collisions will
be reported as `on_wall`. In this mode, when you slide, the speed will
always be constant. This mode is suitable for games without ground like
space games.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PlatformOnLeave**: `🔗<enum_CharacterBody3D_PlatformOnLeave>`

classref-enumeration-constant

`PlatformOnLeave<enum_CharacterBody3D_PlatformOnLeave>`
**PLATFORM\_ON\_LEAVE\_ADD\_VELOCITY** = `0`

Add the last platform velocity to the
`velocity<class_CharacterBody3D_property_velocity>` when you leave a
moving platform.

classref-enumeration-constant

`PlatformOnLeave<enum_CharacterBody3D_PlatformOnLeave>`
**PLATFORM\_ON\_LEAVE\_ADD\_UPWARD\_VELOCITY** = `1`

Add the last platform velocity to the
`velocity<class_CharacterBody3D_property_velocity>` when you leave a
moving platform, but any downward motion is ignored. It's useful to keep
full jump height even when the platform is moving down.

classref-enumeration-constant

`PlatformOnLeave<enum_CharacterBody3D_PlatformOnLeave>`
**PLATFORM\_ON\_LEAVE\_DO\_NOTHING** = `2`

Do nothing when leaving a platform.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **floor\_block\_on\_wall** = `true`
`🔗<class_CharacterBody3D_property_floor_block_on_wall>`

classref-property-setget

-   `void (No return value.)`
    **set\_floor\_block\_on\_wall\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_floor\_block\_on\_wall\_enabled**()

If `true`, the body will be able to move on the floor only. This option
avoids to be able to walk on walls, it will however allow to slide down
along them.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **floor\_constant\_speed** = `false`
`🔗<class_CharacterBody3D_property_floor_constant_speed>`

classref-property-setget

-   `void (No return value.)`
    **set\_floor\_constant\_speed\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_floor\_constant\_speed\_enabled**()

If `false` (by default), the body will move faster on downward slopes
and slower on upward slopes.

If `true`, the body will always move at the same speed on the ground no
matter the slope. Note that you need to use
`floor_snap_length<class_CharacterBody3D_property_floor_snap_length>` to
stick along a downward slope at constant speed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **floor\_max\_angle** = `0.785398`
`🔗<class_CharacterBody3D_property_floor_max_angle>`

classref-property-setget

-   `void (No return value.)` **set\_floor\_max\_angle**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_floor\_max\_angle**()

Maximum angle (in radians) where a slope is still considered a floor (or
a ceiling), rather than a wall, when calling
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`. The
default value equals 45 degrees.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **floor\_snap\_length** = `0.1`
`🔗<class_CharacterBody3D_property_floor_snap_length>`

classref-property-setget

-   `void (No return value.)` **set\_floor\_snap\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_floor\_snap\_length**()

Sets a snapping distance. When set to a value different from `0.0`, the
body is kept attached to slopes when calling
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`. The
snapping vector is determined by the given distance along the opposite
direction of the
`up_direction<class_CharacterBody3D_property_up_direction>`.

As long as the snapping vector is in contact with the ground and the
body moves against
`up_direction<class_CharacterBody3D_property_up_direction>`, the body
will remain attached to the surface. Snapping is not applied if the body
moves along `up_direction<class_CharacterBody3D_property_up_direction>`,
meaning it contains vertical rising velocity, so it will be able to
detach from the ground when jumping or when the body is pushed up by
something. If you want to apply a snap without taking into account the
velocity, use
`apply_floor_snap<class_CharacterBody3D_method_apply_floor_snap>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **floor\_stop\_on\_slope** = `true`
`🔗<class_CharacterBody3D_property_floor_stop_on_slope>`

classref-property-setget

-   `void (No return value.)`
    **set\_floor\_stop\_on\_slope\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_floor\_stop\_on\_slope\_enabled**()

If `true`, the body will not slide on slopes when calling
`move_and_slide<class_CharacterBody3D_method_move_and_slide>` when the
body is standing still.

If `false`, the body will slide on floor's slopes when
`velocity<class_CharacterBody3D_property_velocity>` applies a downward
force.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_slides** = `6`
`🔗<class_CharacterBody3D_property_max_slides>`

classref-property-setget

-   `void (No return value.)` **set\_max\_slides**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_slides**()

Maximum number of times the body can change direction before it stops
when calling
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`MotionMode<enum_CharacterBody3D_MotionMode>` **motion\_mode** = `0`
`🔗<class_CharacterBody3D_property_motion_mode>`

classref-property-setget

-   `void (No return value.)` **set\_motion\_mode**(value:
    `MotionMode<enum_CharacterBody3D_MotionMode>`)
-   `MotionMode<enum_CharacterBody3D_MotionMode>`
    **get\_motion\_mode**()

Sets the motion mode which defines the behavior of
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`. See
`MotionMode<enum_CharacterBody3D_MotionMode>` constants for available
modes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **platform\_floor\_layers** = `4294967295`
`🔗<class_CharacterBody3D_property_platform_floor_layers>`

classref-property-setget

-   `void (No return value.)` **set\_platform\_floor\_layers**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_platform\_floor\_layers**()

Collision layers that will be included for detecting floor bodies that
will act as moving platforms to be followed by the **CharacterBody3D**.
By default, all floor bodies are detected and propagate their velocity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PlatformOnLeave<enum_CharacterBody3D_PlatformOnLeave>`
**platform\_on\_leave** = `0`
`🔗<class_CharacterBody3D_property_platform_on_leave>`

classref-property-setget

-   `void (No return value.)` **set\_platform\_on\_leave**(value:
    `PlatformOnLeave<enum_CharacterBody3D_PlatformOnLeave>`)
-   `PlatformOnLeave<enum_CharacterBody3D_PlatformOnLeave>`
    **get\_platform\_on\_leave**()

Sets the behavior to apply when you leave a moving platform. By default,
to be physically accurate, when you leave the last platform velocity is
applied. See `PlatformOnLeave<enum_CharacterBody3D_PlatformOnLeave>`
constants for available behavior.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **platform\_wall\_layers** = `0`
`🔗<class_CharacterBody3D_property_platform_wall_layers>`

classref-property-setget

-   `void (No return value.)` **set\_platform\_wall\_layers**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_platform\_wall\_layers**()

Collision layers that will be included for detecting wall bodies that
will act as moving platforms to be followed by the **CharacterBody3D**.
By default, all wall bodies are ignored.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **safe\_margin** = `0.001`
`🔗<class_CharacterBody3D_property_safe_margin>`

classref-property-setget

-   `void (No return value.)` **set\_safe\_margin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_safe\_margin**()

Extra margin used for collision recovery when calling
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`.

If the body is at least this close to another body, it will consider
them to be colliding and will be pushed away before performing the
actual motion.

A higher value means it's more flexible for detecting collision, which
helps with consistently detecting walls and floors.

A lower value forces the collision algorithm to use more exact
detection, so it can be used in cases that specifically require
precision, e.g at very low scale to avoid visible jittering, or for
stability with a stack of character bodies.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **slide\_on\_ceiling** = `true`
`🔗<class_CharacterBody3D_property_slide_on_ceiling>`

classref-property-setget

-   `void (No return value.)`
    **set\_slide\_on\_ceiling\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_slide\_on\_ceiling\_enabled**()

If `true`, during a jump against the ceiling, the body will slide, if
`false` it will be stopped and will fall vertically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **up\_direction** = `Vector3(0, 1, 0)`
`🔗<class_CharacterBody3D_property_up_direction>`

classref-property-setget

-   `void (No return value.)` **set\_up\_direction**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_up\_direction**()

Vector pointing upwards, used to determine what is a wall and what is a
floor (or a ceiling) when calling
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`. Defaults
to `Vector3.UP<class_Vector3_constant_UP>`. As the vector will be
normalized it can't be equal to
`Vector3.ZERO<class_Vector3_constant_ZERO>`, if you want all collisions
to be reported as walls, consider using
`MOTION_MODE_FLOATING<class_CharacterBody3D_constant_MOTION_MODE_FLOATING>`
as `motion_mode<class_CharacterBody3D_property_motion_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **velocity** = `Vector3(0, 0, 0)`
`🔗<class_CharacterBody3D_property_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_velocity**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_velocity**()

Current velocity vector (typically meters per second), used and modified
during calls to
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **wall\_min\_slide\_angle** = `0.261799`
`🔗<class_CharacterBody3D_property_wall_min_slide_angle>`

classref-property-setget

-   `void (No return value.)` **set\_wall\_min\_slide\_angle**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_wall\_min\_slide\_angle**()

Minimum angle (in radians) where the body is allowed to slide when it
encounters a slope. The default value equals 15 degrees. When
`motion_mode<class_CharacterBody3D_property_motion_mode>` is
`MOTION_MODE_GROUNDED<class_CharacterBody3D_constant_MOTION_MODE_GROUNDED>`,
it only affects movement if
`floor_block_on_wall<class_CharacterBody3D_property_floor_block_on_wall>`
is `true`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **apply\_floor\_snap**()
`🔗<class_CharacterBody3D_method_apply_floor_snap>`

Allows to manually apply a snap to the floor regardless of the body's
velocity. This function does nothing when
`is_on_floor<class_CharacterBody3D_method_is_on_floor>` returns `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_floor\_angle**(up\_direction:
`Vector3<class_Vector3>` = Vector3(0, 1, 0))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_get_floor_angle>`

Returns the floor's collision angle at the last collision point
according to `up_direction`, which is
`Vector3.UP<class_Vector3_constant_UP>` by default. This value is always
positive and only valid after calling
`move_and_slide<class_CharacterBody3D_method_move_and_slide>` and when
`is_on_floor<class_CharacterBody3D_method_is_on_floor>` returns `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_floor\_normal**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_get_floor_normal>`

Returns the collision normal of the floor at the last collision point.
Only valid after calling
`move_and_slide<class_CharacterBody3D_method_move_and_slide>` and when
`is_on_floor<class_CharacterBody3D_method_is_on_floor>` returns `true`.

\*\*Warning:\*\* The collision normal is not always the same as the
surface normal.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_last\_motion**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_get_last_motion>`

Returns the last motion applied to the **CharacterBody3D** during the
last call to
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`. The
movement can be split into multiple motions when sliding occurs, and
this method return the last one, which is useful to retrieve the current
direction of the movement.

classref-item-separator

------------------------------------------------------------------------

classref-method

`KinematicCollision3D<class_KinematicCollision3D>`
**get\_last\_slide\_collision**()
`🔗<class_CharacterBody3D_method_get_last_slide_collision>`

Returns a `KinematicCollision3D<class_KinematicCollision3D>`, which
contains information about the latest collision that occurred during the
last call to
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_platform\_angular\_velocity**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_get_platform_angular_velocity>`

Returns the angular velocity of the platform at the last collision
point. Only valid after calling
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_platform\_velocity**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_get_platform_velocity>`

Returns the linear velocity of the platform at the last collision point.
Only valid after calling
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_position\_delta**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_get_position_delta>`

Returns the travel (position delta) that occurred during the last call
to `move_and_slide<class_CharacterBody3D_method_move_and_slide>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_real\_velocity**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_get_real_velocity>`

Returns the current real velocity since the last call to
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`. For
example, when you climb a slope, you will move diagonally even though
the velocity is horizontal. This method returns the diagonal movement,
as opposed to `velocity<class_CharacterBody3D_property_velocity>` which
returns the requested velocity.

classref-item-separator

------------------------------------------------------------------------

classref-method

`KinematicCollision3D<class_KinematicCollision3D>`
**get\_slide\_collision**(slide\_idx: `int<class_int>`)
`🔗<class_CharacterBody3D_method_get_slide_collision>`

Returns a `KinematicCollision3D<class_KinematicCollision3D>`, which
contains information about a collision that occurred during the last
call to `move_and_slide<class_CharacterBody3D_method_move_and_slide>`.
Since the body can collide several times in a single call to
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`, you must
specify the index of the collision in the range 0 to
(`get_slide_collision_count<class_CharacterBody3D_method_get_slide_collision_count>` -
1).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_slide\_collision\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_get_slide_collision_count>`

Returns the number of times the body collided and changed direction
during the last call to
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_wall\_normal**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_get_wall_normal>`

Returns the collision normal of the wall at the last collision point.
Only valid after calling
`move_and_slide<class_CharacterBody3D_method_move_and_slide>` and when
`is_on_wall<class_CharacterBody3D_method_is_on_wall>` returns `true`.

\*\*Warning:\*\* The collision normal is not always the same as the
surface normal.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_on\_ceiling**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_is_on_ceiling>`

Returns `true` if the body collided with the ceiling on the last call of
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`.
Otherwise, returns `false`. The
`up_direction<class_CharacterBody3D_property_up_direction>` and
`floor_max_angle<class_CharacterBody3D_property_floor_max_angle>` are
used to determine whether a surface is "ceiling" or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_on\_ceiling\_only**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_is_on_ceiling_only>`

Returns `true` if the body collided only with the ceiling on the last
call of `move_and_slide<class_CharacterBody3D_method_move_and_slide>`.
Otherwise, returns `false`. The
`up_direction<class_CharacterBody3D_property_up_direction>` and
`floor_max_angle<class_CharacterBody3D_property_floor_max_angle>` are
used to determine whether a surface is "ceiling" or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_on\_floor**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_is_on_floor>`

Returns `true` if the body collided with the floor on the last call of
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`.
Otherwise, returns `false`. The
`up_direction<class_CharacterBody3D_property_up_direction>` and
`floor_max_angle<class_CharacterBody3D_property_floor_max_angle>` are
used to determine whether a surface is "floor" or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_on\_floor\_only**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_is_on_floor_only>`

Returns `true` if the body collided only with the floor on the last call
of `move_and_slide<class_CharacterBody3D_method_move_and_slide>`.
Otherwise, returns `false`. The
`up_direction<class_CharacterBody3D_property_up_direction>` and
`floor_max_angle<class_CharacterBody3D_property_floor_max_angle>` are
used to determine whether a surface is "floor" or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_on\_wall**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_is_on_wall>`

Returns `true` if the body collided with a wall on the last call of
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`.
Otherwise, returns `false`. The
`up_direction<class_CharacterBody3D_property_up_direction>` and
`floor_max_angle<class_CharacterBody3D_property_floor_max_angle>` are
used to determine whether a surface is "wall" or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_on\_wall\_only**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CharacterBody3D_method_is_on_wall_only>`

Returns `true` if the body collided only with a wall on the last call of
`move_and_slide<class_CharacterBody3D_method_move_and_slide>`.
Otherwise, returns `false`. The
`up_direction<class_CharacterBody3D_property_up_direction>` and
`floor_max_angle<class_CharacterBody3D_property_floor_max_angle>` are
used to determine whether a surface is "wall" or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **move\_and\_slide**()
`🔗<class_CharacterBody3D_method_move_and_slide>`

Moves the body based on
`velocity<class_CharacterBody3D_property_velocity>`. If the body
collides with another, it will slide along the other body rather than
stop immediately. If the other body is a **CharacterBody3D** or
`RigidBody3D<class_RigidBody3D>`, it will also be affected by the motion
of the other body. You can use this to make moving and rotating
platforms, or to make nodes push other nodes.

Modifies `velocity<class_CharacterBody3D_property_velocity>` if a slide
collision occurred. To get the latest collision call
`get_last_slide_collision<class_CharacterBody3D_method_get_last_slide_collision>`,
for more detailed information about collisions that occurred, use
`get_slide_collision<class_CharacterBody3D_method_get_slide_collision>`.

When the body touches a moving platform, the platform's velocity is
automatically added to the body motion. If a collision occurs due to the
platform's motion, it will always be first in the slide collisions.

Returns `true` if the body collided, otherwise, returns `false`.
