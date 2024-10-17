github\_url  
hide

# PhysicsServer2D

**Inherits:** `Object<class_Object>`

**Inherited By:**
`PhysicsServer2DExtension<class_PhysicsServer2DExtension>`

A server interface for low-level 2D physics access.

classref-introduction-group

## Description

PhysicsServer2D is the server responsible for all 2D physics. It can
directly create and manipulate all physics objects:

-   A *space* is a self-contained world for a physics simulation. It
    contains bodies, areas, and joints. Its state can be queried for
    collision and intersection information, and several parameters of
    the simulation can be modified.
-   A *shape* is a geometric shape such as a circle, a rectangle, a
    capsule, or a polygon. It can be used for collision detection by
    adding it to a body/area, possibly with an extra transformation
    relative to the body/area's origin. Bodies/areas can have multiple
    (transformed) shapes added to them, and a single shape can be added
    to bodies/areas multiple times with different local transformations.
-   A *body* is a physical object which can be in static, kinematic, or
    rigid mode. Its state (such as position and velocity) can be queried
    and updated. A force integration callback can be set to customize
    the body's physics.
-   An *area* is a region in space which can be used to detect bodies
    and areas entering and exiting it. A body monitoring callback can be
    set to report entering/exiting body shapes, and similarly an area
    monitoring callback can be set. Gravity and damping can be
    overridden within the area by setting area parameters.
-   A *joint* is a constraint, either between two bodies or on one body
    relative to a point. Parameters such as the joint bias and the rest
    length of a spring joint can be adjusted.

Physics objects in **PhysicsServer2D** may be created and manipulated
independently; they do not have to be tied to nodes in the scene tree.

\*\*Note:\*\* All the 2D physics nodes use the physics server
internally. Adding a physics node to the scene tree will cause a
corresponding physics object to be created in the physics server. A
rigid body node registers a callback that updates the node's transform
with the transform of the respective body object in the physics server
(every physics update). An area node registers a callback to inform the
area node about overlaps with the respective area object in the physics
server. The raycast node queries the direct state of the relevant space
in the physics server.

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

## Enumerations

classref-enumeration

enum **SpaceParameter**: `🔗<enum_PhysicsServer2D_SpaceParameter>`

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`
**SPACE\_PARAM\_CONTACT\_RECYCLE\_RADIUS** = `0`

Constant to set/get the maximum distance a pair of bodies has to move
before their collision status has to be recalculated. The default value
of this parameter is
`ProjectSettings.physics/2d/solver/contact_recycle_radius<class_ProjectSettings_property_physics/2d/solver/contact_recycle_radius>`.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`
**SPACE\_PARAM\_CONTACT\_MAX\_SEPARATION** = `1`

Constant to set/get the maximum distance a shape can be from another
before they are considered separated and the contact is discarded. The
default value of this parameter is
`ProjectSettings.physics/2d/solver/contact_max_separation<class_ProjectSettings_property_physics/2d/solver/contact_max_separation>`.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`
**SPACE\_PARAM\_CONTACT\_MAX\_ALLOWED\_PENETRATION** = `2`

Constant to set/get the maximum distance a shape can penetrate another
shape before it is considered a collision. The default value of this
parameter is
`ProjectSettings.physics/2d/solver/contact_max_allowed_penetration<class_ProjectSettings_property_physics/2d/solver/contact_max_allowed_penetration>`.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`
**SPACE\_PARAM\_CONTACT\_DEFAULT\_BIAS** = `3`

Constant to set/get the default solver bias for all physics contacts. A
solver bias is a factor controlling how much two objects "rebound",
after overlapping, to avoid leaving them in that state because of
numerical imprecision. The default value of this parameter is
`ProjectSettings.physics/2d/solver/default_contact_bias<class_ProjectSettings_property_physics/2d/solver/default_contact_bias>`.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`
**SPACE\_PARAM\_BODY\_LINEAR\_VELOCITY\_SLEEP\_THRESHOLD** = `4`

Constant to set/get the threshold linear velocity of activity. A body
marked as potentially inactive for both linear and angular velocity will
be put to sleep after the time given. The default value of this
parameter is
`ProjectSettings.physics/2d/sleep_threshold_linear<class_ProjectSettings_property_physics/2d/sleep_threshold_linear>`.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`
**SPACE\_PARAM\_BODY\_ANGULAR\_VELOCITY\_SLEEP\_THRESHOLD** = `5`

Constant to set/get the threshold angular velocity of activity. A body
marked as potentially inactive for both linear and angular velocity will
be put to sleep after the time given. The default value of this
parameter is
`ProjectSettings.physics/2d/sleep_threshold_angular<class_ProjectSettings_property_physics/2d/sleep_threshold_angular>`.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`
**SPACE\_PARAM\_BODY\_TIME\_TO\_SLEEP** = `6`

Constant to set/get the maximum time of activity. A body marked as
potentially inactive for both linear and angular velocity will be put to
sleep after this time. The default value of this parameter is
`ProjectSettings.physics/2d/time_before_sleep<class_ProjectSettings_property_physics/2d/time_before_sleep>`.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`
**SPACE\_PARAM\_CONSTRAINT\_DEFAULT\_BIAS** = `7`

Constant to set/get the default solver bias for all physics constraints.
A solver bias is a factor controlling how much two objects "rebound",
after violating a constraint, to avoid leaving them in that state
because of numerical imprecision. The default value of this parameter is
`ProjectSettings.physics/2d/solver/default_constraint_bias<class_ProjectSettings_property_physics/2d/solver/default_constraint_bias>`.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`
**SPACE\_PARAM\_SOLVER\_ITERATIONS** = `8`

Constant to set/get the number of solver iterations for all contacts and
constraints. The greater the number of iterations, the more accurate the
collisions will be. However, a greater number of iterations requires
more CPU power, which can decrease performance. The default value of
this parameter is
`ProjectSettings.physics/2d/solver/solver_iterations<class_ProjectSettings_property_physics/2d/solver/solver_iterations>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ShapeType**: `🔗<enum_PhysicsServer2D_ShapeType>`

classref-enumeration-constant

`ShapeType<enum_PhysicsServer2D_ShapeType>` **SHAPE\_WORLD\_BOUNDARY** =
`0`

This is the constant for creating world boundary shapes. A world
boundary shape is an *infinite* line with an origin point, and a normal.
Thus, it can be used for front/behind checks.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer2D_ShapeType>` **SHAPE\_SEPARATION\_RAY** =
`1`

This is the constant for creating separation ray shapes. A separation
ray is defined by a length and separates itself from what is touching
its far endpoint. Useful for character controllers.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer2D_ShapeType>` **SHAPE\_SEGMENT** = `2`

This is the constant for creating segment shapes. A segment shape is a
*finite* line from a point A to a point B. It can be checked for
intersections.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer2D_ShapeType>` **SHAPE\_CIRCLE** = `3`

This is the constant for creating circle shapes. A circle shape only has
a radius. It can be used for intersections and inside/outside checks.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer2D_ShapeType>` **SHAPE\_RECTANGLE** = `4`

This is the constant for creating rectangle shapes. A rectangle shape is
defined by a width and a height. It can be used for intersections and
inside/outside checks.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer2D_ShapeType>` **SHAPE\_CAPSULE** = `5`

This is the constant for creating capsule shapes. A capsule shape is
defined by a radius and a length. It can be used for intersections and
inside/outside checks.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer2D_ShapeType>` **SHAPE\_CONVEX\_POLYGON** =
`6`

This is the constant for creating convex polygon shapes. A polygon is
defined by a list of points. It can be used for intersections and
inside/outside checks.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer2D_ShapeType>` **SHAPE\_CONCAVE\_POLYGON**
= `7`

This is the constant for creating concave polygon shapes. A polygon is
defined by a list of points. It can be used for intersections checks,
but not for inside/outside checks.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer2D_ShapeType>` **SHAPE\_CUSTOM** = `8`

This constant is used internally by the engine. Any attempt to create
this kind of shape results in an error.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AreaParameter**: `🔗<enum_PhysicsServer2D_AreaParameter>`

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer2D_AreaParameter>`
**AREA\_PARAM\_GRAVITY\_OVERRIDE\_MODE** = `0`

Constant to set/get gravity override mode in an area. See
`AreaSpaceOverrideMode<enum_PhysicsServer2D_AreaSpaceOverrideMode>` for
possible values. The default value of this parameter is
`AREA_SPACE_OVERRIDE_DISABLED<class_PhysicsServer2D_constant_AREA_SPACE_OVERRIDE_DISABLED>`.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer2D_AreaParameter>`
**AREA\_PARAM\_GRAVITY** = `1`

Constant to set/get gravity strength in an area. The default value of
this parameter is `9.80665`.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer2D_AreaParameter>`
**AREA\_PARAM\_GRAVITY\_VECTOR** = `2`

Constant to set/get gravity vector/center in an area. The default value
of this parameter is `Vector2(0, -1)`.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer2D_AreaParameter>`
**AREA\_PARAM\_GRAVITY\_IS\_POINT** = `3`

Constant to set/get whether the gravity vector of an area is a
direction, or a center point. The default value of this parameter is
`false`.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer2D_AreaParameter>`
**AREA\_PARAM\_GRAVITY\_POINT\_UNIT\_DISTANCE** = `4`

Constant to set/get the distance at which the gravity strength is equal
to the gravity controlled by
`AREA_PARAM_GRAVITY<class_PhysicsServer2D_constant_AREA_PARAM_GRAVITY>`.
For example, on a planet 100 pixels in radius with a surface gravity of
4.0 px/s², set the gravity to 4.0 and the unit distance to 100.0. The
gravity will have falloff according to the inverse square law, so in the
example, at 200 pixels from the center the gravity will be 1.0 px/s²
(twice the distance, 1/4th the gravity), at 50 pixels it will be 16.0
px/s² (half the distance, 4x the gravity), and so on.

The above is true only when the unit distance is a positive number. When
the unit distance is set to 0.0, the gravity will be constant regardless
of distance. The default value of this parameter is `0.0`.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer2D_AreaParameter>`
**AREA\_PARAM\_LINEAR\_DAMP\_OVERRIDE\_MODE** = `5`

Constant to set/get linear damping override mode in an area. See
`AreaSpaceOverrideMode<enum_PhysicsServer2D_AreaSpaceOverrideMode>` for
possible values. The default value of this parameter is
`AREA_SPACE_OVERRIDE_DISABLED<class_PhysicsServer2D_constant_AREA_SPACE_OVERRIDE_DISABLED>`.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer2D_AreaParameter>`
**AREA\_PARAM\_LINEAR\_DAMP** = `6`

Constant to set/get the linear damping factor of an area. The default
value of this parameter is `0.1`.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer2D_AreaParameter>`
**AREA\_PARAM\_ANGULAR\_DAMP\_OVERRIDE\_MODE** = `7`

Constant to set/get angular damping override mode in an area. See
`AreaSpaceOverrideMode<enum_PhysicsServer2D_AreaSpaceOverrideMode>` for
possible values. The default value of this parameter is
`AREA_SPACE_OVERRIDE_DISABLED<class_PhysicsServer2D_constant_AREA_SPACE_OVERRIDE_DISABLED>`.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer2D_AreaParameter>`
**AREA\_PARAM\_ANGULAR\_DAMP** = `8`

Constant to set/get the angular damping factor of an area. The default
value of this parameter is `1.0`.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer2D_AreaParameter>`
**AREA\_PARAM\_PRIORITY** = `9`

Constant to set/get the priority (order of processing) of an area. The
default value of this parameter is `0`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AreaSpaceOverrideMode**:
`🔗<enum_PhysicsServer2D_AreaSpaceOverrideMode>`

classref-enumeration-constant

`AreaSpaceOverrideMode<enum_PhysicsServer2D_AreaSpaceOverrideMode>`
**AREA\_SPACE\_OVERRIDE\_DISABLED** = `0`

This area does not affect gravity/damp. These are generally areas that
exist only to detect collisions, and objects entering or exiting them.

classref-enumeration-constant

`AreaSpaceOverrideMode<enum_PhysicsServer2D_AreaSpaceOverrideMode>`
**AREA\_SPACE\_OVERRIDE\_COMBINE** = `1`

This area adds its gravity/damp values to whatever has been calculated
so far. This way, many overlapping areas can combine their physics to
make interesting effects.

classref-enumeration-constant

`AreaSpaceOverrideMode<enum_PhysicsServer2D_AreaSpaceOverrideMode>`
**AREA\_SPACE\_OVERRIDE\_COMBINE\_REPLACE** = `2`

This area adds its gravity/damp values to whatever has been calculated
so far. Then stops taking into account the rest of the areas, even the
default one.

classref-enumeration-constant

`AreaSpaceOverrideMode<enum_PhysicsServer2D_AreaSpaceOverrideMode>`
**AREA\_SPACE\_OVERRIDE\_REPLACE** = `3`

This area replaces any gravity/damp, even the default one, and stops
taking into account the rest of the areas.

classref-enumeration-constant

`AreaSpaceOverrideMode<enum_PhysicsServer2D_AreaSpaceOverrideMode>`
**AREA\_SPACE\_OVERRIDE\_REPLACE\_COMBINE** = `4`

This area replaces any gravity/damp calculated so far, but keeps
calculating the rest of the areas, down to the default one.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BodyMode**: `🔗<enum_PhysicsServer2D_BodyMode>`

classref-enumeration-constant

`BodyMode<enum_PhysicsServer2D_BodyMode>` **BODY\_MODE\_STATIC** = `0`

Constant for static bodies. In this mode, a body can be only moved by
user code and doesn't collide with other bodies along its path when
moved.

classref-enumeration-constant

`BodyMode<enum_PhysicsServer2D_BodyMode>` **BODY\_MODE\_KINEMATIC** =
`1`

Constant for kinematic bodies. In this mode, a body can be only moved by
user code and collides with other bodies along its path.

classref-enumeration-constant

`BodyMode<enum_PhysicsServer2D_BodyMode>` **BODY\_MODE\_RIGID** = `2`

Constant for rigid bodies. In this mode, a body can be pushed by other
bodies and has forces applied.

classref-enumeration-constant

`BodyMode<enum_PhysicsServer2D_BodyMode>` **BODY\_MODE\_RIGID\_LINEAR**
= `3`

Constant for linear rigid bodies. In this mode, a body can not rotate,
and only its linear velocity is affected by external forces.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BodyParameter**: `🔗<enum_PhysicsServer2D_BodyParameter>`

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer2D_BodyParameter>`
**BODY\_PARAM\_BOUNCE** = `0`

Constant to set/get a body's bounce factor. The default value of this
parameter is `0.0`.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer2D_BodyParameter>`
**BODY\_PARAM\_FRICTION** = `1`

Constant to set/get a body's friction. The default value of this
parameter is `1.0`.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer2D_BodyParameter>`
**BODY\_PARAM\_MASS** = `2`

Constant to set/get a body's mass. The default value of this parameter
is `1.0`. If the body's mode is set to
`BODY_MODE_RIGID<class_PhysicsServer2D_constant_BODY_MODE_RIGID>`, then
setting this parameter will have the following additional effects:

-   If the parameter
    `BODY_PARAM_CENTER_OF_MASS<class_PhysicsServer2D_constant_BODY_PARAM_CENTER_OF_MASS>`
    has never been set explicitly, then the value of that parameter will
    be recalculated based on the body's shapes.
-   If the parameter
    `BODY_PARAM_INERTIA<class_PhysicsServer2D_constant_BODY_PARAM_INERTIA>`
    is set to a value `<= 0.0`, then the value of that parameter will be
    recalculated based on the body's shapes, mass, and center of mass.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer2D_BodyParameter>`
**BODY\_PARAM\_INERTIA** = `3`

Constant to set/get a body's inertia. The default value of this
parameter is `0.0`. If the body's inertia is set to a value `<= 0.0`,
then the inertia will be recalculated based on the body's shapes, mass,
and center of mass.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer2D_BodyParameter>`
**BODY\_PARAM\_CENTER\_OF\_MASS** = `4`

Constant to set/get a body's center of mass position in the body's local
coordinate system. The default value of this parameter is
`Vector2(0,0)`. If this parameter is never set explicitly, then it is
recalculated based on the body's shapes when setting the parameter
`BODY_PARAM_MASS<class_PhysicsServer2D_constant_BODY_PARAM_MASS>` or
when calling
`body_set_space<class_PhysicsServer2D_method_body_set_space>`.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer2D_BodyParameter>`
**BODY\_PARAM\_GRAVITY\_SCALE** = `5`

Constant to set/get a body's gravity multiplier. The default value of
this parameter is `1.0`.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer2D_BodyParameter>`
**BODY\_PARAM\_LINEAR\_DAMP\_MODE** = `6`

Constant to set/get a body's linear damping mode. See
`BodyDampMode<enum_PhysicsServer2D_BodyDampMode>` for possible values.
The default value of this parameter is
`BODY_DAMP_MODE_COMBINE<class_PhysicsServer2D_constant_BODY_DAMP_MODE_COMBINE>`.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer2D_BodyParameter>`
**BODY\_PARAM\_ANGULAR\_DAMP\_MODE** = `7`

Constant to set/get a body's angular damping mode. See
`BodyDampMode<enum_PhysicsServer2D_BodyDampMode>` for possible values.
The default value of this parameter is
`BODY_DAMP_MODE_COMBINE<class_PhysicsServer2D_constant_BODY_DAMP_MODE_COMBINE>`.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer2D_BodyParameter>`
**BODY\_PARAM\_LINEAR\_DAMP** = `8`

Constant to set/get a body's linear damping factor. The default value of
this parameter is `0.0`.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer2D_BodyParameter>`
**BODY\_PARAM\_ANGULAR\_DAMP** = `9`

Constant to set/get a body's angular damping factor. The default value
of this parameter is `0.0`.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer2D_BodyParameter>` **BODY\_PARAM\_MAX**
= `10`

Represents the size of the
`BodyParameter<enum_PhysicsServer2D_BodyParameter>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BodyDampMode**: `🔗<enum_PhysicsServer2D_BodyDampMode>`

classref-enumeration-constant

`BodyDampMode<enum_PhysicsServer2D_BodyDampMode>`
**BODY\_DAMP\_MODE\_COMBINE** = `0`

The body's damping value is added to any value set in areas or the
default value.

classref-enumeration-constant

`BodyDampMode<enum_PhysicsServer2D_BodyDampMode>`
**BODY\_DAMP\_MODE\_REPLACE** = `1`

The body's damping value replaces any value set in areas or the default
value.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BodyState**: `🔗<enum_PhysicsServer2D_BodyState>`

classref-enumeration-constant

`BodyState<enum_PhysicsServer2D_BodyState>` **BODY\_STATE\_TRANSFORM** =
`0`

Constant to set/get the current transform matrix of the body.

classref-enumeration-constant

`BodyState<enum_PhysicsServer2D_BodyState>`
**BODY\_STATE\_LINEAR\_VELOCITY** = `1`

Constant to set/get the current linear velocity of the body.

classref-enumeration-constant

`BodyState<enum_PhysicsServer2D_BodyState>`
**BODY\_STATE\_ANGULAR\_VELOCITY** = `2`

Constant to set/get the current angular velocity of the body.

classref-enumeration-constant

`BodyState<enum_PhysicsServer2D_BodyState>` **BODY\_STATE\_SLEEPING** =
`3`

Constant to sleep/wake up a body, or to get whether it is sleeping.

classref-enumeration-constant

`BodyState<enum_PhysicsServer2D_BodyState>` **BODY\_STATE\_CAN\_SLEEP**
= `4`

Constant to set/get whether the body can sleep.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **JointType**: `🔗<enum_PhysicsServer2D_JointType>`

classref-enumeration-constant

`JointType<enum_PhysicsServer2D_JointType>` **JOINT\_TYPE\_PIN** = `0`

Constant to create pin joints.

classref-enumeration-constant

`JointType<enum_PhysicsServer2D_JointType>` **JOINT\_TYPE\_GROOVE** =
`1`

Constant to create groove joints.

classref-enumeration-constant

`JointType<enum_PhysicsServer2D_JointType>`
**JOINT\_TYPE\_DAMPED\_SPRING** = `2`

Constant to create damped spring joints.

classref-enumeration-constant

`JointType<enum_PhysicsServer2D_JointType>` **JOINT\_TYPE\_MAX** = `3`

Represents the size of the `JointType<enum_PhysicsServer2D_JointType>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **JointParam**: `🔗<enum_PhysicsServer2D_JointParam>`

classref-enumeration-constant

`JointParam<enum_PhysicsServer2D_JointParam>` **JOINT\_PARAM\_BIAS** =
`0`

Constant to set/get how fast the joint pulls the bodies back to satisfy
the joint constraint. The lower the value, the more the two bodies can
pull on the joint. The default value of this parameter is `0.0`.

\*\*Note:\*\* In Godot Physics, this parameter is only used for pin
joints and groove joints.

classref-enumeration-constant

`JointParam<enum_PhysicsServer2D_JointParam>`
**JOINT\_PARAM\_MAX\_BIAS** = `1`

Constant to set/get the maximum speed with which the joint can apply
corrections. The default value of this parameter is `3.40282e+38`.

\*\*Note:\*\* In Godot Physics, this parameter is only used for groove
joints.

classref-enumeration-constant

`JointParam<enum_PhysicsServer2D_JointParam>`
**JOINT\_PARAM\_MAX\_FORCE** = `2`

Constant to set/get the maximum force that the joint can use to act on
the two bodies. The default value of this parameter is `3.40282e+38`.

\*\*Note:\*\* In Godot Physics, this parameter is only used for groove
joints.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PinJointParam**: `🔗<enum_PhysicsServer2D_PinJointParam>`

classref-enumeration-constant

`PinJointParam<enum_PhysicsServer2D_PinJointParam>`
**PIN\_JOINT\_SOFTNESS** = `0`

Constant to set/get a how much the bond of the pin joint can flex. The
default value of this parameter is `0.0`.

classref-enumeration-constant

`PinJointParam<enum_PhysicsServer2D_PinJointParam>`
**PIN\_JOINT\_LIMIT\_UPPER** = `1`

The maximum rotation around the pin.

classref-enumeration-constant

`PinJointParam<enum_PhysicsServer2D_PinJointParam>`
**PIN\_JOINT\_LIMIT\_LOWER** = `2`

The minimum rotation around the pin.

classref-enumeration-constant

`PinJointParam<enum_PhysicsServer2D_PinJointParam>`
**PIN\_JOINT\_MOTOR\_TARGET\_VELOCITY** = `3`

Target speed for the motor. In radians per second.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PinJointFlag**: `🔗<enum_PhysicsServer2D_PinJointFlag>`

classref-enumeration-constant

`PinJointFlag<enum_PhysicsServer2D_PinJointFlag>`
**PIN\_JOINT\_FLAG\_ANGULAR\_LIMIT\_ENABLED** = `0`

If `true`, the pin has a maximum and a minimum rotation.

classref-enumeration-constant

`PinJointFlag<enum_PhysicsServer2D_PinJointFlag>`
**PIN\_JOINT\_FLAG\_MOTOR\_ENABLED** = `1`

If `true`, a motor turns the pin.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DampedSpringParam**: `🔗<enum_PhysicsServer2D_DampedSpringParam>`

classref-enumeration-constant

`DampedSpringParam<enum_PhysicsServer2D_DampedSpringParam>`
**DAMPED\_SPRING\_REST\_LENGTH** = `0`

Sets the resting length of the spring joint. The joint will always try
to go to back this length when pulled apart. The default value of this
parameter is the distance between the joint's anchor points.

classref-enumeration-constant

`DampedSpringParam<enum_PhysicsServer2D_DampedSpringParam>`
**DAMPED\_SPRING\_STIFFNESS** = `1`

Sets the stiffness of the spring joint. The joint applies a force equal
to the stiffness times the distance from its resting length. The default
value of this parameter is `20.0`.

classref-enumeration-constant

`DampedSpringParam<enum_PhysicsServer2D_DampedSpringParam>`
**DAMPED\_SPRING\_DAMPING** = `2`

Sets the damping ratio of the spring joint. A value of 0 indicates an
undamped spring, while 1 causes the system to reach equilibrium as fast
as possible (critical damping). The default value of this parameter is
`1.5`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CCDMode**: `🔗<enum_PhysicsServer2D_CCDMode>`

classref-enumeration-constant

`CCDMode<enum_PhysicsServer2D_CCDMode>` **CCD\_MODE\_DISABLED** = `0`

Disables continuous collision detection. This is the fastest way to
detect body collisions, but it can miss small and/or fast-moving
objects.

classref-enumeration-constant

`CCDMode<enum_PhysicsServer2D_CCDMode>` **CCD\_MODE\_CAST\_RAY** = `1`

Enables continuous collision detection by raycasting. It is faster than
shapecasting, but less precise.

classref-enumeration-constant

`CCDMode<enum_PhysicsServer2D_CCDMode>` **CCD\_MODE\_CAST\_SHAPE** = `2`

Enables continuous collision detection by shapecasting. It is the
slowest CCD method, and the most precise.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AreaBodyStatus**: `🔗<enum_PhysicsServer2D_AreaBodyStatus>`

classref-enumeration-constant

`AreaBodyStatus<enum_PhysicsServer2D_AreaBodyStatus>`
**AREA\_BODY\_ADDED** = `0`

The value of the first parameter and area callback function receives,
when an object enters one of its shapes.

classref-enumeration-constant

`AreaBodyStatus<enum_PhysicsServer2D_AreaBodyStatus>`
**AREA\_BODY\_REMOVED** = `1`

The value of the first parameter and area callback function receives,
when an object exits one of its shapes.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ProcessInfo**: `🔗<enum_PhysicsServer2D_ProcessInfo>`

classref-enumeration-constant

`ProcessInfo<enum_PhysicsServer2D_ProcessInfo>`
**INFO\_ACTIVE\_OBJECTS** = `0`

Constant to get the number of objects that are not sleeping.

classref-enumeration-constant

`ProcessInfo<enum_PhysicsServer2D_ProcessInfo>`
**INFO\_COLLISION\_PAIRS** = `1`

Constant to get the number of possible collisions.

classref-enumeration-constant

`ProcessInfo<enum_PhysicsServer2D_ProcessInfo>` **INFO\_ISLAND\_COUNT**
= `2`

Constant to get the number of space regions where a collision could
occur.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **area\_add\_shape**(area: `RID<class_RID>`,
shape: `RID<class_RID>`, transform: `Transform2D<class_Transform2D>` =
Transform2D(1, 0, 0, 1, 0, 0), disabled: `bool<class_bool>` = false)
`🔗<class_PhysicsServer2D_method_area_add_shape>`

Adds a shape to the area, with the given local transform. The shape
(together with its `transform` and `disabled` properties) is added to an
array of shapes, and the shapes of an area are usually referenced by
their index in this array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_attach\_canvas\_instance\_id**(area:
`RID<class_RID>`, id: `int<class_int>`)
`🔗<class_PhysicsServer2D_method_area_attach_canvas_instance_id>`

Attaches the `ObjectID` of a canvas to the area. Use
`Object.get_instance_id<class_Object_method_get_instance_id>` to get the
`ObjectID` of a `CanvasLayer<class_CanvasLayer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_attach\_object\_instance\_id**(area:
`RID<class_RID>`, id: `int<class_int>`)
`🔗<class_PhysicsServer2D_method_area_attach_object_instance_id>`

Attaches the `ObjectID` of an `Object<class_Object>` to the area. Use
`Object.get_instance_id<class_Object_method_get_instance_id>` to get the
`ObjectID` of a `CollisionObject2D<class_CollisionObject2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_clear\_shapes**(area:
`RID<class_RID>`) `🔗<class_PhysicsServer2D_method_area_clear_shapes>`

Removes all shapes from the area. This does not delete the shapes
themselves, so they can continue to be used elsewhere or added back
later.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **area\_create**()
`🔗<class_PhysicsServer2D_method_area_create>`

Creates a 2D area object in the physics server, and returns the
`RID<class_RID>` that identifies it. The default settings for the
created area include a collision layer and mask set to `1`, and
`monitorable` set to `false`.

Use `area_add_shape<class_PhysicsServer2D_method_area_add_shape>` to add
shapes to it, use
`area_set_transform<class_PhysicsServer2D_method_area_set_transform>` to
set its transform, and use
`area_set_space<class_PhysicsServer2D_method_area_set_space>` to add the
area to a space. If you want the area to be detectable use
`area_set_monitorable<class_PhysicsServer2D_method_area_set_monitorable>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **area\_get\_canvas\_instance\_id**(area:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_area_get_canvas_instance_id>`

Returns the `ObjectID` of the canvas attached to the area. Use
`@GlobalScope.instance_from_id<class_@GlobalScope_method_instance_from_id>`
to retrieve a `CanvasLayer<class_CanvasLayer>` from a nonzero
`ObjectID`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **area\_get\_collision\_layer**(area: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_area_get_collision_layer>`

Returns the physics layer or layers the area belongs to, as a bitmask.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **area\_get\_collision\_mask**(area: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_area_get_collision_mask>`

Returns the physics layer or layers the area can contact with, as a
bitmask.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **area\_get\_object\_instance\_id**(area:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_area_get_object_instance_id>`

Returns the `ObjectID` attached to the area. Use
`@GlobalScope.instance_from_id<class_@GlobalScope_method_instance_from_id>`
to retrieve an `Object<class_Object>` from a nonzero `ObjectID`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **area\_get\_param**(area: `RID<class_RID>`,
param: `AreaParameter<enum_PhysicsServer2D_AreaParameter>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_area_get_param>`

Returns the value of the given area parameter. See
`AreaParameter<enum_PhysicsServer2D_AreaParameter>` for the list of
available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **area\_get\_shape**(area: `RID<class_RID>`,
shape\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_area_get_shape>`

Returns the `RID<class_RID>` of the shape with the given index in the
area's array of shapes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **area\_get\_shape\_count**(area: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_area_get_shape_count>`

Returns the number of shapes added to the area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **area\_get\_shape\_transform**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_area_get_shape_transform>`

Returns the local transform matrix of the shape with the given index in
the area's array of shapes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **area\_get\_space**(area: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_area_get_space>`

Returns the `RID<class_RID>` of the space assigned to the area. Returns
an empty `RID<class_RID>` if no space is assigned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **area\_get\_transform**(area:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_area_get_transform>`

Returns the transform matrix of the area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_remove\_shape**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`🔗<class_PhysicsServer2D_method_area_remove_shape>`

Removes the shape with the given index from the area's array of shapes.
The shape itself is not deleted, so it can continue to be used elsewhere
or added back later. As a result of this operation, the area's shapes
which used to have indices higher than `shape_idx` will have their index
decreased by one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_area\_monitor\_callback**(area:
`RID<class_RID>`, callback: `Callable<class_Callable>`)
`🔗<class_PhysicsServer2D_method_area_set_area_monitor_callback>`

Sets the area's area monitor callback. This callback will be called when
any other (shape of an) area enters or exits (a shape of) the given
area, and must take the following five parameters:

1.  an integer `status`: either
    `AREA_BODY_ADDED<class_PhysicsServer2D_constant_AREA_BODY_ADDED>` or
    `AREA_BODY_REMOVED<class_PhysicsServer2D_constant_AREA_BODY_REMOVED>`
    depending on whether the other area's shape entered or exited the
    area,
2.  an `RID<class_RID>` `area_rid`: the `RID<class_RID>` of the other
    area that entered or exited the area,
3.  an integer `instance_id`: the `ObjectID` attached to the other area,
4.  an integer `area_shape_idx`: the index of the shape of the other
    area that entered or exited the area,
5.  an integer `self_shape_idx`: the index of the shape of the area
    where the other area entered or exited.

By counting (or keeping track of) the shapes that enter and exit, it can
be determined if an area (with all its shapes) is entering for the first
time or exiting for the last time.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_collision\_layer**(area:
`RID<class_RID>`, layer: `int<class_int>`)
`🔗<class_PhysicsServer2D_method_area_set_collision_layer>`

Assigns the area to one or many physics layers, via a bitmask.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_collision\_mask**(area:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_PhysicsServer2D_method_area_set_collision_mask>`

Sets which physics layers the area will monitor, via a bitmask.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_monitor\_callback**(area:
`RID<class_RID>`, callback: `Callable<class_Callable>`)
`🔗<class_PhysicsServer2D_method_area_set_monitor_callback>`

Sets the area's body monitor callback. This callback will be called when
any other (shape of a) body enters or exits (a shape of) the given area,
and must take the following five parameters:

1.  an integer `status`: either
    `AREA_BODY_ADDED<class_PhysicsServer2D_constant_AREA_BODY_ADDED>` or
    `AREA_BODY_REMOVED<class_PhysicsServer2D_constant_AREA_BODY_REMOVED>`
    depending on whether the other body shape entered or exited the
    area,
2.  an `RID<class_RID>` `body_rid`: the `RID<class_RID>` of the body
    that entered or exited the area,
3.  an integer `instance_id`: the `ObjectID` attached to the body,
4.  an integer `body_shape_idx`: the index of the shape of the body that
    entered or exited the area,
5.  an integer `self_shape_idx`: the index of the shape of the area
    where the body entered or exited.

By counting (or keeping track of) the shapes that enter and exit, it can
be determined if a body (with all its shapes) is entering for the first
time or exiting for the last time.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_monitorable**(area:
`RID<class_RID>`, monitorable: `bool<class_bool>`)
`🔗<class_PhysicsServer2D_method_area_set_monitorable>`

Sets whether the area is monitorable or not. If `monitorable` is `true`,
the area monitoring callback of other areas will be called when this
area enters or exits them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_param**(area: `RID<class_RID>`,
param: `AreaParameter<enum_PhysicsServer2D_AreaParameter>`, value:
`Variant<class_Variant>`)
`🔗<class_PhysicsServer2D_method_area_set_param>`

Sets the value of the given area parameter. See
`AreaParameter<enum_PhysicsServer2D_AreaParameter>` for the list of
available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_shape**(area: `RID<class_RID>`,
shape\_idx: `int<class_int>`, shape: `RID<class_RID>`)
`🔗<class_PhysicsServer2D_method_area_set_shape>`

Replaces the area's shape at the given index by another shape, while not
affecting the `transform` and `disabled` properties at the same index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_shape\_disabled**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`, disabled:
`bool<class_bool>`)
`🔗<class_PhysicsServer2D_method_area_set_shape_disabled>`

Sets the disabled property of the area's shape with the given index. If
`disabled` is `true`, then the shape will not detect any other shapes
entering or exiting it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_shape\_transform**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`, transform:
`Transform2D<class_Transform2D>`)
`🔗<class_PhysicsServer2D_method_area_set_shape_transform>`

Sets the local transform matrix of the area's shape with the given
index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_space**(area: `RID<class_RID>`,
space: `RID<class_RID>`)
`🔗<class_PhysicsServer2D_method_area_set_space>`

Adds the area to the given space, after removing the area from the
previously assigned space (if any).

\*\*Note:\*\* To remove an area from a space without immediately adding
it back elsewhere, use `PhysicsServer2D.area_set_space(area, RID())`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_transform**(area:
`RID<class_RID>`, transform: `Transform2D<class_Transform2D>`)
`🔗<class_PhysicsServer2D_method_area_set_transform>`

Sets the transform matrix of the area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_add\_collision\_exception**(body:
`RID<class_RID>`, excepted\_body: `RID<class_RID>`)
`🔗<class_PhysicsServer2D_method_body_add_collision_exception>`

Adds `excepted_body` to the body's list of collision exceptions, so that
collisions with it are ignored.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_add\_constant\_central\_force**(body:
`RID<class_RID>`, force: `Vector2<class_Vector2>`)
`🔗<class_PhysicsServer2D_method_body_add_constant_central_force>`

Adds a constant directional force to the body. The force does not affect
rotation. The force remains applied over time until cleared with
`PhysicsServer2D.body_set_constant_force(body, Vector2(0, 0))`.

This is equivalent to using
`body_add_constant_force<class_PhysicsServer2D_method_body_add_constant_force>`
at the body's center of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_add\_constant\_force**(body:
`RID<class_RID>`, force: `Vector2<class_Vector2>`, position:
`Vector2<class_Vector2>` = Vector2(0, 0))
`🔗<class_PhysicsServer2D_method_body_add_constant_force>`

Adds a constant positioned force to the body. The force can affect
rotation if `position` is different from the body's center of mass. The
force remains applied over time until cleared with
`PhysicsServer2D.body_set_constant_force(body, Vector2(0, 0))`.

`position` is the offset from the body origin in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_add\_constant\_torque**(body:
`RID<class_RID>`, torque: `float<class_float>`)
`🔗<class_PhysicsServer2D_method_body_add_constant_torque>`

Adds a constant rotational force to the body. The force does not affect
position. The force remains applied over time until cleared with
`PhysicsServer2D.body_set_constant_torque(body, 0)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_add\_shape**(body: `RID<class_RID>`,
shape: `RID<class_RID>`, transform: `Transform2D<class_Transform2D>` =
Transform2D(1, 0, 0, 1, 0, 0), disabled: `bool<class_bool>` = false)
`🔗<class_PhysicsServer2D_method_body_add_shape>`

Adds a shape to the area, with the given local transform. The shape
(together with its `transform` and `disabled` properties) is added to an
array of shapes, and the shapes of a body are usually referenced by
their index in this array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_central\_force**(body:
`RID<class_RID>`, force: `Vector2<class_Vector2>`)
`🔗<class_PhysicsServer2D_method_body_apply_central_force>`

Applies a directional force to the body, at the body's center of mass.
The force does not affect rotation. A force is time dependent and meant
to be applied every physics update.

This is equivalent to using
`body_apply_force<class_PhysicsServer2D_method_body_apply_force>` at the
body's center of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_central\_impulse**(body:
`RID<class_RID>`, impulse: `Vector2<class_Vector2>`)
`🔗<class_PhysicsServer2D_method_body_apply_central_impulse>`

Applies a directional impulse to the body, at the body's center of mass.
The impulse does not affect rotation.

An impulse is time-independent! Applying an impulse every frame would
result in a framerate-dependent force. For this reason, it should only
be used when simulating one-time impacts (use the "\_force" functions
otherwise).

This is equivalent to using
`body_apply_impulse<class_PhysicsServer2D_method_body_apply_impulse>` at
the body's center of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_force**(body: `RID<class_RID>`,
force: `Vector2<class_Vector2>`, position: `Vector2<class_Vector2>` =
Vector2(0, 0)) `🔗<class_PhysicsServer2D_method_body_apply_force>`

Applies a positioned force to the body. The force can affect rotation if
`position` is different from the body's center of mass. A force is time
dependent and meant to be applied every physics update.

`position` is the offset from the body origin in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_impulse**(body:
`RID<class_RID>`, impulse: `Vector2<class_Vector2>`, position:
`Vector2<class_Vector2>` = Vector2(0, 0))
`🔗<class_PhysicsServer2D_method_body_apply_impulse>`

Applies a positioned impulse to the body. The impulse can affect
rotation if `position` is different from the body's center of mass.

An impulse is time-independent! Applying an impulse every frame would
result in a framerate-dependent force. For this reason, it should only
be used when simulating one-time impacts (use the "\_force" functions
otherwise).

`position` is the offset from the body origin in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_torque**(body:
`RID<class_RID>`, torque: `float<class_float>`)
`🔗<class_PhysicsServer2D_method_body_apply_torque>`

Applies a rotational force to the body. The force does not affect
position. A force is time dependent and meant to be applied every
physics update.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_torque\_impulse**(body:
`RID<class_RID>`, impulse: `float<class_float>`)
`🔗<class_PhysicsServer2D_method_body_apply_torque_impulse>`

Applies a rotational impulse to the body. The impulse does not affect
position.

An impulse is time-independent! Applying an impulse every frame would
result in a framerate-dependent force. For this reason, it should only
be used when simulating one-time impacts (use the "\_force" functions
otherwise).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_attach\_canvas\_instance\_id**(body:
`RID<class_RID>`, id: `int<class_int>`)
`🔗<class_PhysicsServer2D_method_body_attach_canvas_instance_id>`

Attaches the `ObjectID` of a canvas to the body. Use
`Object.get_instance_id<class_Object_method_get_instance_id>` to get the
`ObjectID` of a `CanvasLayer<class_CanvasLayer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_attach\_object\_instance\_id**(body:
`RID<class_RID>`, id: `int<class_int>`)
`🔗<class_PhysicsServer2D_method_body_attach_object_instance_id>`

Attaches the `ObjectID` of an `Object<class_Object>` to the body. Use
`Object.get_instance_id<class_Object_method_get_instance_id>` to get the
`ObjectID` of a `CollisionObject2D<class_CollisionObject2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_clear\_shapes**(body:
`RID<class_RID>`) `🔗<class_PhysicsServer2D_method_body_clear_shapes>`

Removes all shapes from the body. This does not delete the shapes
themselves, so they can continue to be used elsewhere or added back
later.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **body\_create**()
`🔗<class_PhysicsServer2D_method_body_create>`

Creates a 2D body object in the physics server, and returns the
`RID<class_RID>` that identifies it. The default settings for the
created area include a collision layer and mask set to `1`, and body
mode set to
`BODY_MODE_RIGID<class_PhysicsServer2D_constant_BODY_MODE_RIGID>`.

Use `body_add_shape<class_PhysicsServer2D_method_body_add_shape>` to add
shapes to it, use
`body_set_state<class_PhysicsServer2D_method_body_set_state>` to set its
transform, and use
`body_set_space<class_PhysicsServer2D_method_body_set_space>` to add the
body to a space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **body\_get\_canvas\_instance\_id**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_canvas_instance_id>`

Returns the `ObjectID` of the canvas attached to the body. Use
`@GlobalScope.instance_from_id<class_@GlobalScope_method_instance_from_id>`
to retrieve a `CanvasLayer<class_CanvasLayer>` from a nonzero
`ObjectID`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **body\_get\_collision\_layer**(body: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_collision_layer>`

Returns the physics layer or layers the body belongs to, as a bitmask.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **body\_get\_collision\_mask**(body: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_collision_mask>`

Returns the physics layer or layers the body can collide with, as a
bitmask.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **body\_get\_collision\_priority**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_collision_priority>`

Returns the body's collision priority. This is used in the depenetration
phase of
`body_test_motion<class_PhysicsServer2D_method_body_test_motion>`. The
higher the priority is, the lower the penetration into the body will be.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **body\_get\_constant\_force**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_constant_force>`

Returns the body's total constant positional force applied during each
physics update.

See
`body_add_constant_force<class_PhysicsServer2D_method_body_add_constant_force>`
and
`body_add_constant_central_force<class_PhysicsServer2D_method_body_add_constant_central_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **body\_get\_constant\_torque**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_constant_torque>`

Returns the body's total constant rotational force applied during each
physics update.

See
`body_add_constant_torque<class_PhysicsServer2D_method_body_add_constant_torque>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CCDMode<enum_PhysicsServer2D_CCDMode>`
**body\_get\_continuous\_collision\_detection\_mode**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_continuous_collision_detection_mode>`

Returns the body's continuous collision detection mode (see
`CCDMode<enum_PhysicsServer2D_CCDMode>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PhysicsDirectBodyState2D<class_PhysicsDirectBodyState2D>`
**body\_get\_direct\_state**(body: `RID<class_RID>`)
`🔗<class_PhysicsServer2D_method_body_get_direct_state>`

Returns the `PhysicsDirectBodyState2D<class_PhysicsDirectBodyState2D>`
of the body. Returns `null` if the body is destroyed or not assigned to
a space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **body\_get\_max\_contacts\_reported**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_max_contacts_reported>`

Returns the maximum number of contacts that the body can report. See
`body_set_max_contacts_reported<class_PhysicsServer2D_method_body_set_max_contacts_reported>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`BodyMode<enum_PhysicsServer2D_BodyMode>` **body\_get\_mode**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_mode>`

Returns the body's mode (see `BodyMode<enum_PhysicsServer2D_BodyMode>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **body\_get\_object\_instance\_id**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_object_instance_id>`

Returns the `ObjectID` attached to the body. Use
`@GlobalScope.instance_from_id<class_@GlobalScope_method_instance_from_id>`
to retrieve an `Object<class_Object>` from a nonzero `ObjectID`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **body\_get\_param**(body: `RID<class_RID>`,
param: `BodyParameter<enum_PhysicsServer2D_BodyParameter>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_param>`

Returns the value of the given body parameter. See
`BodyParameter<enum_PhysicsServer2D_BodyParameter>` for the list of
available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **body\_get\_shape**(body: `RID<class_RID>`,
shape\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_shape>`

Returns the `RID<class_RID>` of the shape with the given index in the
body's array of shapes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **body\_get\_shape\_count**(body: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_shape_count>`

Returns the number of shapes added to the body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **body\_get\_shape\_transform**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_shape_transform>`

Returns the local transform matrix of the shape with the given index in
the area's array of shapes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **body\_get\_space**(body: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_space>`

Returns the `RID<class_RID>` of the space assigned to the body. Returns
an empty `RID<class_RID>` if no space is assigned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **body\_get\_state**(body: `RID<class_RID>`,
state: `BodyState<enum_PhysicsServer2D_BodyState>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_get_state>`

Returns the value of the given state of the body. See
`BodyState<enum_PhysicsServer2D_BodyState>` for the list of available
states.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **body\_is\_omitting\_force\_integration**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_body_is_omitting_force_integration>`

Returns `true` if the body is omitting the standard force integration.
See
`body_set_omit_force_integration<class_PhysicsServer2D_method_body_set_omit_force_integration>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_remove\_collision\_exception**(body:
`RID<class_RID>`, excepted\_body: `RID<class_RID>`)
`🔗<class_PhysicsServer2D_method_body_remove_collision_exception>`

Removes `excepted_body` from the body's list of collision exceptions, so
that collisions with it are no longer ignored.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_remove\_shape**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`🔗<class_PhysicsServer2D_method_body_remove_shape>`

Removes the shape with the given index from the body's array of shapes.
The shape itself is not deleted, so it can continue to be used elsewhere
or added back later. As a result of this operation, the body's shapes
which used to have indices higher than `shape_idx` will have their index
decreased by one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_reset\_mass\_properties**(body:
`RID<class_RID>`)
`🔗<class_PhysicsServer2D_method_body_reset_mass_properties>`

Restores the default inertia and center of mass of the body based on its
shapes. This undoes any custom values previously set using
`body_set_param<class_PhysicsServer2D_method_body_set_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_axis\_velocity**(body:
`RID<class_RID>`, axis\_velocity: `Vector2<class_Vector2>`)
`🔗<class_PhysicsServer2D_method_body_set_axis_velocity>`

Modifies the body's linear velocity so that its projection to the axis
`axis_velocity.normalized()` is exactly `axis_velocity.length()`. This
is useful for jumping behavior.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_collision\_layer**(body:
`RID<class_RID>`, layer: `int<class_int>`)
`🔗<class_PhysicsServer2D_method_body_set_collision_layer>`

Sets the physics layer or layers the body belongs to, via a bitmask.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_collision\_mask**(body:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_PhysicsServer2D_method_body_set_collision_mask>`

Sets the physics layer or layers the body can collide with, via a
bitmask.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_collision\_priority**(body:
`RID<class_RID>`, priority: `float<class_float>`)
`🔗<class_PhysicsServer2D_method_body_set_collision_priority>`

Sets the body's collision priority. This is used in the depenetration
phase of
`body_test_motion<class_PhysicsServer2D_method_body_test_motion>`. The
higher the priority is, the lower the penetration into the body will be.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_constant\_force**(body:
`RID<class_RID>`, force: `Vector2<class_Vector2>`)
`🔗<class_PhysicsServer2D_method_body_set_constant_force>`

Sets the body's total constant positional force applied during each
physics update.

See
`body_add_constant_force<class_PhysicsServer2D_method_body_add_constant_force>`
and
`body_add_constant_central_force<class_PhysicsServer2D_method_body_add_constant_central_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_constant\_torque**(body:
`RID<class_RID>`, torque: `float<class_float>`)
`🔗<class_PhysicsServer2D_method_body_set_constant_torque>`

Sets the body's total constant rotational force applied during each
physics update.

See
`body_add_constant_torque<class_PhysicsServer2D_method_body_add_constant_torque>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**body\_set\_continuous\_collision\_detection\_mode**(body:
`RID<class_RID>`, mode: `CCDMode<enum_PhysicsServer2D_CCDMode>`)
`🔗<class_PhysicsServer2D_method_body_set_continuous_collision_detection_mode>`

Sets the continuous collision detection mode using one of the
`CCDMode<enum_PhysicsServer2D_CCDMode>` constants.

Continuous collision detection tries to predict where a moving body
would collide in between physics updates, instead of moving it and
correcting its movement if it collided.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**body\_set\_force\_integration\_callback**(body: `RID<class_RID>`,
callable: `Callable<class_Callable>`, userdata: `Variant<class_Variant>`
= null)
`🔗<class_PhysicsServer2D_method_body_set_force_integration_callback>`

Sets the body's custom force integration callback function to
`callable`. Use an empty `Callable<class_Callable>` (`Callable()`) to
clear the custom callback.

The function `callable` will be called every physics tick, before the
standard force integration (see
`body_set_omit_force_integration<class_PhysicsServer2D_method_body_set_omit_force_integration>`).
It can be used for example to update the body's linear and angular
velocity based on contact with other bodies.

If `userdata` is not `null`, the function `callable` must take the
following two parameters:

1.  `state`: a
    `PhysicsDirectBodyState2D<class_PhysicsDirectBodyState2D>` used to
    retrieve and modify the body's state,
2.  `userdata`: a `Variant<class_Variant>`; its value will be the
    `userdata` passed into this method.

If `userdata` is `null`, then `callable` must take only the `state`
parameter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_max\_contacts\_reported**(body:
`RID<class_RID>`, amount: `int<class_int>`)
`🔗<class_PhysicsServer2D_method_body_set_max_contacts_reported>`

Sets the maximum number of contacts that the body can report. If
`amount` is greater than zero, then the body will keep track of at most
this many contacts with other bodies.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_mode**(body: `RID<class_RID>`,
mode: `BodyMode<enum_PhysicsServer2D_BodyMode>`)
`🔗<class_PhysicsServer2D_method_body_set_mode>`

Sets the body's mode. See `BodyMode<enum_PhysicsServer2D_BodyMode>` for
the list of available modes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_omit\_force\_integration**(body:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_PhysicsServer2D_method_body_set_omit_force_integration>`

Sets whether the body omits the standard force integration. If `enable`
is `true`, the body will not automatically use applied forces, torques,
and damping to update the body's linear and angular velocity. In this
case,
`body_set_force_integration_callback<class_PhysicsServer2D_method_body_set_force_integration_callback>`
can be used to manually update the linear and angular velocity instead.

This method is called when the property
`RigidBody2D.custom_integrator<class_RigidBody2D_property_custom_integrator>`
is set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_param**(body: `RID<class_RID>`,
param: `BodyParameter<enum_PhysicsServer2D_BodyParameter>`, value:
`Variant<class_Variant>`)
`🔗<class_PhysicsServer2D_method_body_set_param>`

Sets the value of the given body parameter. See
`BodyParameter<enum_PhysicsServer2D_BodyParameter>` for the list of
available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_shape**(body: `RID<class_RID>`,
shape\_idx: `int<class_int>`, shape: `RID<class_RID>`)
`🔗<class_PhysicsServer2D_method_body_set_shape>`

Replaces the body's shape at the given index by another shape, while not
affecting the `transform`, `disabled`, and one-way collision properties
at the same index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**body\_set\_shape\_as\_one\_way\_collision**(body: `RID<class_RID>`,
shape\_idx: `int<class_int>`, enable: `bool<class_bool>`, margin:
`float<class_float>`)
`🔗<class_PhysicsServer2D_method_body_set_shape_as_one_way_collision>`

Sets the one-way collision properties of the body's shape with the given
index. If `enable` is `true`, the one-way collision direction given by
the shape's local upward axis
`body_get_shape_transform(body, shape_idx).y` will be used to ignore
collisions with the shape in the opposite direction, and to ensure
depenetration of kinematic bodies happens in this direction.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_shape\_disabled**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`, disabled:
`bool<class_bool>`)
`🔗<class_PhysicsServer2D_method_body_set_shape_disabled>`

Sets the disabled property of the body's shape with the given index. If
`disabled` is `true`, then the shape will be ignored in all collision
detection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_shape\_transform**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`, transform:
`Transform2D<class_Transform2D>`)
`🔗<class_PhysicsServer2D_method_body_set_shape_transform>`

Sets the local transform matrix of the body's shape with the given
index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_space**(body: `RID<class_RID>`,
space: `RID<class_RID>`)
`🔗<class_PhysicsServer2D_method_body_set_space>`

Adds the body to the given space, after removing the body from the
previously assigned space (if any). If the body's mode is set to
`BODY_MODE_RIGID<class_PhysicsServer2D_constant_BODY_MODE_RIGID>`, then
adding the body to a space will have the following additional effects:

-   If the parameter
    `BODY_PARAM_CENTER_OF_MASS<class_PhysicsServer2D_constant_BODY_PARAM_CENTER_OF_MASS>`
    has never been set explicitly, then the value of that parameter will
    be recalculated based on the body's shapes.
-   If the parameter
    `BODY_PARAM_INERTIA<class_PhysicsServer2D_constant_BODY_PARAM_INERTIA>`
    is set to a value `<= 0.0`, then the value of that parameter will be
    recalculated based on the body's shapes, mass, and center of mass.

\*\*Note:\*\* To remove a body from a space without immediately adding
it back elsewhere, use `PhysicsServer2D.body_set_space(body, RID())`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_state**(body: `RID<class_RID>`,
state: `BodyState<enum_PhysicsServer2D_BodyState>`, value:
`Variant<class_Variant>`)
`🔗<class_PhysicsServer2D_method_body_set_state>`

Sets the value of a body's state. See
`BodyState<enum_PhysicsServer2D_BodyState>` for the list of available
states.

\*\*Note:\*\* The state change doesn't take effect immediately. The
state will change on the next physics frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_state\_sync\_callback**(body:
`RID<class_RID>`, callable: `Callable<class_Callable>`)
`🔗<class_PhysicsServer2D_method_body_set_state_sync_callback>`

Sets the body's state synchronization callback function to `callable`.
Use an empty `Callable<class_Callable>` (`Callable()`) to clear the
callback.

The function `callable` will be called every physics frame, assuming
that the body was active during the previous physics tick, and can be
used to fetch the latest state from the physics server.

The function `callable` must take the following parameters:

1.  `state`: a
    `PhysicsDirectBodyState2D<class_PhysicsDirectBodyState2D>`, used to
    retrieve the body's state.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **body\_test\_motion**(body: `RID<class_RID>`,
parameters:
`PhysicsTestMotionParameters2D<class_PhysicsTestMotionParameters2D>`,
result: `PhysicsTestMotionResult2D<class_PhysicsTestMotionResult2D>` =
null) `🔗<class_PhysicsServer2D_method_body_test_motion>`

Returns `true` if a collision would result from moving the body along a
motion vector from a given point in space. See
`PhysicsTestMotionParameters2D<class_PhysicsTestMotionParameters2D>` for
the available motion parameters. Optionally a
`PhysicsTestMotionResult2D<class_PhysicsTestMotionResult2D>` object can
be passed, which will be used to store the information about the
resulting collision.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **capsule\_shape\_create**()
`🔗<class_PhysicsServer2D_method_capsule_shape_create>`

Creates a 2D capsule shape in the physics server, and returns the
`RID<class_RID>` that identifies it. Use
`shape_set_data<class_PhysicsServer2D_method_shape_set_data>` to set the
capsule's height and radius.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **circle\_shape\_create**()
`🔗<class_PhysicsServer2D_method_circle_shape_create>`

Creates a 2D circle shape in the physics server, and returns the
`RID<class_RID>` that identifies it. Use
`shape_set_data<class_PhysicsServer2D_method_shape_set_data>` to set the
circle's radius.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **concave\_polygon\_shape\_create**()
`🔗<class_PhysicsServer2D_method_concave_polygon_shape_create>`

Creates a 2D concave polygon shape in the physics server, and returns
the `RID<class_RID>` that identifies it. Use
`shape_set_data<class_PhysicsServer2D_method_shape_set_data>` to set the
concave polygon's segments.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **convex\_polygon\_shape\_create**()
`🔗<class_PhysicsServer2D_method_convex_polygon_shape_create>`

Creates a 2D convex polygon shape in the physics server, and returns the
`RID<class_RID>` that identifies it. Use
`shape_set_data<class_PhysicsServer2D_method_shape_set_data>` to set the
convex polygon's points.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **damped\_spring\_joint\_get\_param**(joint:
`RID<class_RID>`, param:
`DampedSpringParam<enum_PhysicsServer2D_DampedSpringParam>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_damped_spring_joint_get_param>`

Returns the value of the given damped spring joint parameter. See
`DampedSpringParam<enum_PhysicsServer2D_DampedSpringParam>` for the list
of available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **damped\_spring\_joint\_set\_param**(joint:
`RID<class_RID>`, param:
`DampedSpringParam<enum_PhysicsServer2D_DampedSpringParam>`, value:
`float<class_float>`)
`🔗<class_PhysicsServer2D_method_damped_spring_joint_set_param>`

Sets the value of the given damped spring joint parameter. See
`DampedSpringParam<enum_PhysicsServer2D_DampedSpringParam>` for the list
of available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **free\_rid**(rid: `RID<class_RID>`)
`🔗<class_PhysicsServer2D_method_free_rid>`

Destroys any of the objects created by PhysicsServer2D. If the
`RID<class_RID>` passed is not one of the objects that can be created by
PhysicsServer2D, an error will be printed to the console.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_process\_info**(process\_info:
`ProcessInfo<enum_PhysicsServer2D_ProcessInfo>`)
`🔗<class_PhysicsServer2D_method_get_process_info>`

Returns information about the current state of the 2D physics engine.
See `ProcessInfo<enum_PhysicsServer2D_ProcessInfo>` for the list of
available states.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_clear**(joint: `RID<class_RID>`)
`🔗<class_PhysicsServer2D_method_joint_clear>`

Destroys the joint with the given `RID<class_RID>`, creates a new
uninitialized joint, and makes the `RID<class_RID>` refer to this new
joint.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **joint\_create**()
`🔗<class_PhysicsServer2D_method_joint_create>`

Creates a 2D joint in the physics server, and returns the
`RID<class_RID>` that identifies it. To set the joint type, use
`joint_make_damped_spring<class_PhysicsServer2D_method_joint_make_damped_spring>`,
`joint_make_groove<class_PhysicsServer2D_method_joint_make_groove>` or
`joint_make_pin<class_PhysicsServer2D_method_joint_make_pin>`. Use
`joint_set_param<class_PhysicsServer2D_method_joint_set_param>` to set
generic joint parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**joint\_disable\_collisions\_between\_bodies**(joint: `RID<class_RID>`,
disable: `bool<class_bool>`)
`🔗<class_PhysicsServer2D_method_joint_disable_collisions_between_bodies>`

Sets whether the bodies attached to the `Joint2D<class_Joint2D>` will
collide with each other.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **joint\_get\_param**(joint: `RID<class_RID>`,
param: `JointParam<enum_PhysicsServer2D_JointParam>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_joint_get_param>`

Returns the value of the given joint parameter. See
`JointParam<enum_PhysicsServer2D_JointParam>` for the list of available
parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`JointType<enum_PhysicsServer2D_JointType>` **joint\_get\_type**(joint:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_joint_get_type>`

Returns the joint's type (see
`JointType<enum_PhysicsServer2D_JointType>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**joint\_is\_disabled\_collisions\_between\_bodies**(joint:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_joint_is_disabled_collisions_between_bodies>`

Returns whether the bodies attached to the `Joint2D<class_Joint2D>` will
collide with each other.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_make\_damped\_spring**(joint:
`RID<class_RID>`, anchor\_a: `Vector2<class_Vector2>`, anchor\_b:
`Vector2<class_Vector2>`, body\_a: `RID<class_RID>`, body\_b:
`RID<class_RID>` = RID())
`🔗<class_PhysicsServer2D_method_joint_make_damped_spring>`

Makes the joint a damped spring joint, attached at the point `anchor_a`
(given in global coordinates) on the body `body_a` and at the point
`anchor_b` (given in global coordinates) on the body `body_b`. To set
the parameters which are specific to the damped spring, see
`damped_spring_joint_set_param<class_PhysicsServer2D_method_damped_spring_joint_set_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_make\_groove**(joint:
`RID<class_RID>`, groove1\_a: `Vector2<class_Vector2>`, groove2\_a:
`Vector2<class_Vector2>`, anchor\_b: `Vector2<class_Vector2>`, body\_a:
`RID<class_RID>` = RID(), body\_b: `RID<class_RID>` = RID())
`🔗<class_PhysicsServer2D_method_joint_make_groove>`

Makes the joint a groove joint.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_make\_pin**(joint: `RID<class_RID>`,
anchor: `Vector2<class_Vector2>`, body\_a: `RID<class_RID>`, body\_b:
`RID<class_RID>` = RID())
`🔗<class_PhysicsServer2D_method_joint_make_pin>`

Makes the joint a pin joint. If `body_b` is an empty `RID<class_RID>`,
then `body_a` is pinned to the point `anchor` (given in global
coordinates); otherwise, `body_a` is pinned to `body_b` at the point
`anchor` (given in global coordinates). To set the parameters which are
specific to the pin joint, see
`pin_joint_set_param<class_PhysicsServer2D_method_pin_joint_set_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_set\_param**(joint: `RID<class_RID>`,
param: `JointParam<enum_PhysicsServer2D_JointParam>`, value:
`float<class_float>`) `🔗<class_PhysicsServer2D_method_joint_set_param>`

Sets the value of the given joint parameter. See
`JointParam<enum_PhysicsServer2D_JointParam>` for the list of available
parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **pin\_joint\_get\_flag**(joint: `RID<class_RID>`,
flag: `PinJointFlag<enum_PhysicsServer2D_PinJointFlag>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_pin_joint_get_flag>`

Gets a pin joint flag (see
`PinJointFlag<enum_PhysicsServer2D_PinJointFlag>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **pin\_joint\_get\_param**(joint: `RID<class_RID>`,
param: `PinJointParam<enum_PhysicsServer2D_PinJointParam>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_pin_joint_get_param>`

Returns the value of a pin joint parameter. See
`PinJointParam<enum_PhysicsServer2D_PinJointParam>` for a list of
available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **pin\_joint\_set\_flag**(joint:
`RID<class_RID>`, flag:
`PinJointFlag<enum_PhysicsServer2D_PinJointFlag>`, enabled:
`bool<class_bool>`)
`🔗<class_PhysicsServer2D_method_pin_joint_set_flag>`

Sets a pin joint flag (see
`PinJointFlag<enum_PhysicsServer2D_PinJointFlag>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **pin\_joint\_set\_param**(joint:
`RID<class_RID>`, param:
`PinJointParam<enum_PhysicsServer2D_PinJointParam>`, value:
`float<class_float>`)
`🔗<class_PhysicsServer2D_method_pin_joint_set_param>`

Sets a pin joint parameter. See
`PinJointParam<enum_PhysicsServer2D_PinJointParam>` for a list of
available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **rectangle\_shape\_create**()
`🔗<class_PhysicsServer2D_method_rectangle_shape_create>`

Creates a 2D rectangle shape in the physics server, and returns the
`RID<class_RID>` that identifies it. Use
`shape_set_data<class_PhysicsServer2D_method_shape_set_data>` to set the
rectangle's half-extents.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **segment\_shape\_create**()
`🔗<class_PhysicsServer2D_method_segment_shape_create>`

Creates a 2D segment shape in the physics server, and returns the
`RID<class_RID>` that identifies it. Use
`shape_set_data<class_PhysicsServer2D_method_shape_set_data>` to set the
segment's start and end points.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **separation\_ray\_shape\_create**()
`🔗<class_PhysicsServer2D_method_separation_ray_shape_create>`

Creates a 2D separation ray shape in the physics server, and returns the
`RID<class_RID>` that identifies it. Use
`shape_set_data<class_PhysicsServer2D_method_shape_set_data>` to set the
shape's `length` and `slide_on_slope` properties.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_active**(active: `bool<class_bool>`)
`🔗<class_PhysicsServer2D_method_set_active>`

Activates or deactivates the 2D physics server. If `active` is `false`,
then the physics server will not do anything in its physics step.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **shape\_get\_data**(shape: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_shape_get_data>`

Returns the shape data that defines the configuration of the shape, such
as the half-extents of a rectangle or the segments of a concave shape.
See `shape_set_data<class_PhysicsServer2D_method_shape_set_data>` for
the precise format of this data in each case.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ShapeType<enum_PhysicsServer2D_ShapeType>` **shape\_get\_type**(shape:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_shape_get_type>`

Returns the shape's type (see
`ShapeType<enum_PhysicsServer2D_ShapeType>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **shape\_set\_data**(shape: `RID<class_RID>`,
data: `Variant<class_Variant>`)
`🔗<class_PhysicsServer2D_method_shape_set_data>`

Sets the shape data that defines the configuration of the shape. The
`data` to be passed depends on the shape's type (see
`shape_get_type<class_PhysicsServer2D_method_shape_get_type>`):

-   `SHAPE_WORLD_BOUNDARY<class_PhysicsServer2D_constant_SHAPE_WORLD_BOUNDARY>`:
    an array of length two containing a `Vector2<class_Vector2>`
    `normal` direction and a `float<class_float>` distance `d`,
-   `SHAPE_SEPARATION_RAY<class_PhysicsServer2D_constant_SHAPE_SEPARATION_RAY>`:
    a dictionary containing the key `length` with a `float<class_float>`
    value and the key `slide_on_slope` with a `bool<class_bool>` value,
-   `SHAPE_SEGMENT<class_PhysicsServer2D_constant_SHAPE_SEGMENT>`: a
    `Rect2<class_Rect2>` `rect` containing the first point of the
    segment in `rect.position` and the second point of the segment in
    `rect.size`,
-   `SHAPE_CIRCLE<class_PhysicsServer2D_constant_SHAPE_CIRCLE>`: a
    `float<class_float>` `radius`,
-   `SHAPE_RECTANGLE<class_PhysicsServer2D_constant_SHAPE_RECTANGLE>`: a
    `Vector2<class_Vector2>` `half_extents`,
-   `SHAPE_CAPSULE<class_PhysicsServer2D_constant_SHAPE_CAPSULE>`: an
    array of length two (or a `Vector2<class_Vector2>`) containing a
    `float<class_float>` `height` and a `float<class_float>` `radius`,
-   `SHAPE_CONVEX_POLYGON<class_PhysicsServer2D_constant_SHAPE_CONVEX_POLYGON>`:
    either a `PackedVector2Array<class_PackedVector2Array>` of points
    defining a convex polygon in counterclockwise order (the clockwise
    outward normal of each segment formed by consecutive points is
    calculated internally), or a
    `PackedFloat32Array<class_PackedFloat32Array>` of length divisible
    by four so that every 4-tuple of `float<class_float>`s contains the
    coordinates of a point followed by the coordinates of the clockwise
    outward normal vector to the segment between the current point and
    the next point,
-   `SHAPE_CONCAVE_POLYGON<class_PhysicsServer2D_constant_SHAPE_CONCAVE_POLYGON>`:
    a `PackedVector2Array<class_PackedVector2Array>` of length divisible
    by two (each pair of points forms one segment).

\*\*Warning:\*\* In the case of
`SHAPE_CONVEX_POLYGON<class_PhysicsServer2D_constant_SHAPE_CONVEX_POLYGON>`,
this method does not check if the points supplied actually form a convex
polygon (unlike the
`CollisionPolygon2D.polygon<class_CollisionPolygon2D_property_polygon>`
property).

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **space\_create**()
`🔗<class_PhysicsServer2D_method_space_create>`

Creates a 2D space in the physics server, and returns the
`RID<class_RID>` that identifies it. A space contains bodies and areas,
and controls the stepping of the physics simulation of the objects in
it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PhysicsDirectSpaceState2D<class_PhysicsDirectSpaceState2D>`
**space\_get\_direct\_state**(space: `RID<class_RID>`)
`🔗<class_PhysicsServer2D_method_space_get_direct_state>`

Returns the state of a space, a
`PhysicsDirectSpaceState2D<class_PhysicsDirectSpaceState2D>`. This
object can be used for collision/intersection queries.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **space\_get\_param**(space: `RID<class_RID>`,
param: `SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_space_get_param>`

Returns the value of the given space parameter. See
`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>` for the list of
available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **space\_is\_active**(space: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2D_method_space_is_active>`

Returns `true` if the space is active.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **space\_set\_active**(space:
`RID<class_RID>`, active: `bool<class_bool>`)
`🔗<class_PhysicsServer2D_method_space_set_active>`

Activates or deactivates the space. If `active` is `false`, then the
physics server will not do anything with this space in its physics step.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **space\_set\_param**(space: `RID<class_RID>`,
param: `SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`, value:
`float<class_float>`) `🔗<class_PhysicsServer2D_method_space_set_param>`

Sets the value of the given space parameter. See
`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>` for the list of
available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **world\_boundary\_shape\_create**()
`🔗<class_PhysicsServer2D_method_world_boundary_shape_create>`

Creates a 2D world boundary shape in the physics server, and returns the
`RID<class_RID>` that identifies it. Use
`shape_set_data<class_PhysicsServer2D_method_shape_set_data>` to set the
shape's normal direction and distance properties.
