github\_url  
hide

# PhysicsServer3D

**Inherits:** `Object<class_Object>`

**Inherited By:**
`PhysicsServer3DExtension<class_PhysicsServer3DExtension>`

A server interface for low-level 3D physics access.

classref-introduction-group

## Description

PhysicsServer3D is the server responsible for all 3D physics. It can
directly create and manipulate all physics objects:

-   A *space* is a self-contained world for a physics simulation. It
    contains bodies, areas, and joints. Its state can be queried for
    collision and intersection information, and several parameters of
    the simulation can be modified.
-   A *shape* is a geometric shape such as a sphere, a box, a cylinder,
    or a polygon. It can be used for collision detection by adding it to
    a body/area, possibly with an extra transformation relative to the
    body/area's origin. Bodies/areas can have multiple (transformed)
    shapes added to them, and a single shape can be added to
    bodies/areas multiple times with different local transformations.
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

Physics objects in **PhysicsServer3D** may be created and manipulated
independently; they do not have to be tied to nodes in the scene tree.

\*\*Note:\*\* All the 3D physics nodes use the physics server
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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

enum **JointType**: `🔗<enum_PhysicsServer3D_JointType>`

classref-enumeration-constant

`JointType<enum_PhysicsServer3D_JointType>` **JOINT\_TYPE\_PIN** = `0`

The `Joint3D<class_Joint3D>` is a `PinJoint3D<class_PinJoint3D>`.

classref-enumeration-constant

`JointType<enum_PhysicsServer3D_JointType>` **JOINT\_TYPE\_HINGE** = `1`

The `Joint3D<class_Joint3D>` is a `HingeJoint3D<class_HingeJoint3D>`.

classref-enumeration-constant

`JointType<enum_PhysicsServer3D_JointType>` **JOINT\_TYPE\_SLIDER** =
`2`

The `Joint3D<class_Joint3D>` is a `SliderJoint3D<class_SliderJoint3D>`.

classref-enumeration-constant

`JointType<enum_PhysicsServer3D_JointType>` **JOINT\_TYPE\_CONE\_TWIST**
= `3`

The `Joint3D<class_Joint3D>` is a
`ConeTwistJoint3D<class_ConeTwistJoint3D>`.

classref-enumeration-constant

`JointType<enum_PhysicsServer3D_JointType>` **JOINT\_TYPE\_6DOF** = `4`

The `Joint3D<class_Joint3D>` is a
`Generic6DOFJoint3D<class_Generic6DOFJoint3D>`.

classref-enumeration-constant

`JointType<enum_PhysicsServer3D_JointType>` **JOINT\_TYPE\_MAX** = `5`

Represents the size of the `JointType<enum_PhysicsServer3D_JointType>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PinJointParam**: `🔗<enum_PhysicsServer3D_PinJointParam>`

classref-enumeration-constant

`PinJointParam<enum_PhysicsServer3D_PinJointParam>` **PIN\_JOINT\_BIAS**
= `0`

The strength with which the pinned objects try to stay in positional
relation to each other.

The higher, the stronger.

classref-enumeration-constant

`PinJointParam<enum_PhysicsServer3D_PinJointParam>`
**PIN\_JOINT\_DAMPING** = `1`

The strength with which the pinned objects try to stay in velocity
relation to each other.

The higher, the stronger.

classref-enumeration-constant

`PinJointParam<enum_PhysicsServer3D_PinJointParam>`
**PIN\_JOINT\_IMPULSE\_CLAMP** = `2`

If above 0, this value is the maximum value for an impulse that this
Joint3D puts on its ends.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **HingeJointParam**: `🔗<enum_PhysicsServer3D_HingeJointParam>`

classref-enumeration-constant

`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>`
**HINGE\_JOINT\_BIAS** = `0`

The speed with which the two bodies get pulled together when they move
in different directions.

classref-enumeration-constant

`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>`
**HINGE\_JOINT\_LIMIT\_UPPER** = `1`

The maximum rotation across the Hinge.

classref-enumeration-constant

`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>`
**HINGE\_JOINT\_LIMIT\_LOWER** = `2`

The minimum rotation across the Hinge.

classref-enumeration-constant

`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>`
**HINGE\_JOINT\_LIMIT\_BIAS** = `3`

The speed with which the rotation across the axis perpendicular to the
hinge gets corrected.

classref-enumeration-constant

`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>`
**HINGE\_JOINT\_LIMIT\_SOFTNESS** = `4`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>`
**HINGE\_JOINT\_LIMIT\_RELAXATION** = `5`

The lower this value, the more the rotation gets slowed down.

classref-enumeration-constant

`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>`
**HINGE\_JOINT\_MOTOR\_TARGET\_VELOCITY** = `6`

Target speed for the motor.

classref-enumeration-constant

`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>`
**HINGE\_JOINT\_MOTOR\_MAX\_IMPULSE** = `7`

Maximum acceleration for the motor.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **HingeJointFlag**: `🔗<enum_PhysicsServer3D_HingeJointFlag>`

classref-enumeration-constant

`HingeJointFlag<enum_PhysicsServer3D_HingeJointFlag>`
**HINGE\_JOINT\_FLAG\_USE\_LIMIT** = `0`

If `true`, the Hinge has a maximum and a minimum rotation.

classref-enumeration-constant

`HingeJointFlag<enum_PhysicsServer3D_HingeJointFlag>`
**HINGE\_JOINT\_FLAG\_ENABLE\_MOTOR** = `1`

If `true`, a motor turns the Hinge.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SliderJointParam**: `🔗<enum_PhysicsServer3D_SliderJointParam>`

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_LINEAR\_LIMIT\_UPPER** = `0`

The maximum difference between the pivot points on their X axis before
damping happens.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_LINEAR\_LIMIT\_LOWER** = `1`

The minimum difference between the pivot points on their X axis before
damping happens.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_LINEAR\_LIMIT\_SOFTNESS** = `2`

A factor applied to the movement across the slider axis once the limits
get surpassed. The lower, the slower the movement.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_LINEAR\_LIMIT\_RESTITUTION** = `3`

The amount of restitution once the limits are surpassed. The lower, the
more velocity-energy gets lost.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_LINEAR\_LIMIT\_DAMPING** = `4`

The amount of damping once the slider limits are surpassed.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_LINEAR\_MOTION\_SOFTNESS** = `5`

A factor applied to the movement across the slider axis as long as the
slider is in the limits. The lower, the slower the movement.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_LINEAR\_MOTION\_RESTITUTION** = `6`

The amount of restitution inside the slider limits.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_LINEAR\_MOTION\_DAMPING** = `7`

The amount of damping inside the slider limits.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_LINEAR\_ORTHOGONAL\_SOFTNESS** = `8`

A factor applied to the movement across axes orthogonal to the slider.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_LINEAR\_ORTHOGONAL\_RESTITUTION** = `9`

The amount of restitution when movement is across axes orthogonal to the
slider.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_LINEAR\_ORTHOGONAL\_DAMPING** = `10`

The amount of damping when movement is across axes orthogonal to the
slider.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_ANGULAR\_LIMIT\_UPPER** = `11`

The upper limit of rotation in the slider.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_ANGULAR\_LIMIT\_LOWER** = `12`

The lower limit of rotation in the slider.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_ANGULAR\_LIMIT\_SOFTNESS** = `13`

A factor applied to the all rotation once the limit is surpassed.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_ANGULAR\_LIMIT\_RESTITUTION** = `14`

The amount of restitution of the rotation when the limit is surpassed.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_ANGULAR\_LIMIT\_DAMPING** = `15`

The amount of damping of the rotation when the limit is surpassed.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_ANGULAR\_MOTION\_SOFTNESS** = `16`

A factor that gets applied to the all rotation in the limits.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_ANGULAR\_MOTION\_RESTITUTION** = `17`

The amount of restitution of the rotation in the limits.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_ANGULAR\_MOTION\_DAMPING** = `18`

The amount of damping of the rotation in the limits.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_ANGULAR\_ORTHOGONAL\_SOFTNESS** = `19`

A factor that gets applied to the all rotation across axes orthogonal to
the slider.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_ANGULAR\_ORTHOGONAL\_RESTITUTION** = `20`

The amount of restitution of the rotation across axes orthogonal to the
slider.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_ANGULAR\_ORTHOGONAL\_DAMPING** = `21`

The amount of damping of the rotation across axes orthogonal to the
slider.

classref-enumeration-constant

`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`
**SLIDER\_JOINT\_MAX** = `22`

Represents the size of the
`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ConeTwistJointParam**:
`🔗<enum_PhysicsServer3D_ConeTwistJointParam>`

classref-enumeration-constant

`ConeTwistJointParam<enum_PhysicsServer3D_ConeTwistJointParam>`
**CONE\_TWIST\_JOINT\_SWING\_SPAN** = `0`

Swing is rotation from side to side, around the axis perpendicular to
the twist axis.

The swing span defines, how much rotation will not get corrected along
the swing axis.

Could be defined as looseness in the
`ConeTwistJoint3D<class_ConeTwistJoint3D>`.

If below 0.05, this behavior is locked.

classref-enumeration-constant

`ConeTwistJointParam<enum_PhysicsServer3D_ConeTwistJointParam>`
**CONE\_TWIST\_JOINT\_TWIST\_SPAN** = `1`

Twist is the rotation around the twist axis, this value defined how far
the joint can twist.

Twist is locked if below 0.05.

classref-enumeration-constant

`ConeTwistJointParam<enum_PhysicsServer3D_ConeTwistJointParam>`
**CONE\_TWIST\_JOINT\_BIAS** = `2`

The speed with which the swing or twist will take place.

The higher, the faster.

classref-enumeration-constant

`ConeTwistJointParam<enum_PhysicsServer3D_ConeTwistJointParam>`
**CONE\_TWIST\_JOINT\_SOFTNESS** = `3`

The ease with which the Joint3D twists, if it's too low, it takes more
force to twist the joint.

classref-enumeration-constant

`ConeTwistJointParam<enum_PhysicsServer3D_ConeTwistJointParam>`
**CONE\_TWIST\_JOINT\_RELAXATION** = `4`

Defines, how fast the swing- and twist-speed-difference on both sides
gets synced.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **G6DOFJointAxisParam**:
`🔗<enum_PhysicsServer3D_G6DOFJointAxisParam>`

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_LINEAR\_LOWER\_LIMIT** = `0`

The minimum difference between the pivot points' axes.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_LINEAR\_UPPER\_LIMIT** = `1`

The maximum difference between the pivot points' axes.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_LINEAR\_LIMIT\_SOFTNESS** = `2`

A factor that gets applied to the movement across the axes. The lower,
the slower the movement.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_LINEAR\_RESTITUTION** = `3`

The amount of restitution on the axes movement. The lower, the more
velocity-energy gets lost.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_LINEAR\_DAMPING** = `4`

The amount of damping that happens at the linear motion across the axes.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_LINEAR\_MOTOR\_TARGET\_VELOCITY** = `5`

The velocity that the joint's linear motor will attempt to reach.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_LINEAR\_MOTOR\_FORCE\_LIMIT** = `6`

The maximum force that the linear motor can apply while trying to reach
the target velocity.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_LINEAR\_SPRING\_STIFFNESS** = `7`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_LINEAR\_SPRING\_DAMPING** = `8`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_LINEAR\_SPRING\_EQUILIBRIUM\_POINT** = `9`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_LOWER\_LIMIT** = `10`

The minimum rotation in negative direction to break loose and rotate
around the axes.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_UPPER\_LIMIT** = `11`

The minimum rotation in positive direction to break loose and rotate
around the axes.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_LIMIT\_SOFTNESS** = `12`

A factor that gets multiplied onto all rotations across the axes.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_DAMPING** = `13`

The amount of rotational damping across the axes. The lower, the more
damping occurs.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_RESTITUTION** = `14`

The amount of rotational restitution across the axes. The lower, the
more restitution occurs.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_FORCE\_LIMIT** = `15`

The maximum amount of force that can occur, when rotating around the
axes.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_ERP** = `16`

When correcting the crossing of limits in rotation across the axes, this
error tolerance factor defines how much the correction gets slowed down.
The lower, the slower.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_MOTOR\_TARGET\_VELOCITY** = `17`

Target speed for the motor at the axes.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_MOTOR\_FORCE\_LIMIT** = `18`

Maximum acceleration for the motor at the axes.

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_SPRING\_STIFFNESS** = `19`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_SPRING\_DAMPING** = `20`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_ANGULAR\_SPRING\_EQUILIBRIUM\_POINT** = `21`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`
**G6DOF\_JOINT\_MAX** = `22`

Represents the size of the
`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **G6DOFJointAxisFlag**:
`🔗<enum_PhysicsServer3D_G6DOFJointAxisFlag>`

classref-enumeration-constant

`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>`
**G6DOF\_JOINT\_FLAG\_ENABLE\_LINEAR\_LIMIT** = `0`

If set, linear motion is possible within the given limits.

classref-enumeration-constant

`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>`
**G6DOF\_JOINT\_FLAG\_ENABLE\_ANGULAR\_LIMIT** = `1`

If set, rotational motion is possible.

classref-enumeration-constant

`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>`
**G6DOF\_JOINT\_FLAG\_ENABLE\_ANGULAR\_SPRING** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>`
**G6DOF\_JOINT\_FLAG\_ENABLE\_LINEAR\_SPRING** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>`
**G6DOF\_JOINT\_FLAG\_ENABLE\_MOTOR** = `4`

If set, there is a rotational motor across these axes.

classref-enumeration-constant

`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>`
**G6DOF\_JOINT\_FLAG\_ENABLE\_LINEAR\_MOTOR** = `5`

If set, there is a linear motor on this axis that targets a specific
velocity.

classref-enumeration-constant

`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>`
**G6DOF\_JOINT\_FLAG\_MAX** = `6`

Represents the size of the
`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ShapeType**: `🔗<enum_PhysicsServer3D_ShapeType>`

classref-enumeration-constant

`ShapeType<enum_PhysicsServer3D_ShapeType>` **SHAPE\_WORLD\_BOUNDARY** =
`0`

The `Shape3D<class_Shape3D>` is a
`WorldBoundaryShape3D<class_WorldBoundaryShape3D>`.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer3D_ShapeType>` **SHAPE\_SEPARATION\_RAY** =
`1`

The `Shape3D<class_Shape3D>` is a
`SeparationRayShape3D<class_SeparationRayShape3D>`.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer3D_ShapeType>` **SHAPE\_SPHERE** = `2`

The `Shape3D<class_Shape3D>` is a `SphereShape3D<class_SphereShape3D>`.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer3D_ShapeType>` **SHAPE\_BOX** = `3`

The `Shape3D<class_Shape3D>` is a `BoxShape3D<class_BoxShape3D>`.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer3D_ShapeType>` **SHAPE\_CAPSULE** = `4`

The `Shape3D<class_Shape3D>` is a
`CapsuleShape3D<class_CapsuleShape3D>`.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer3D_ShapeType>` **SHAPE\_CYLINDER** = `5`

The `Shape3D<class_Shape3D>` is a
`CylinderShape3D<class_CylinderShape3D>`.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer3D_ShapeType>` **SHAPE\_CONVEX\_POLYGON** =
`6`

The `Shape3D<class_Shape3D>` is a
`ConvexPolygonShape3D<class_ConvexPolygonShape3D>`.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer3D_ShapeType>` **SHAPE\_CONCAVE\_POLYGON**
= `7`

The `Shape3D<class_Shape3D>` is a
`ConcavePolygonShape3D<class_ConcavePolygonShape3D>`.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer3D_ShapeType>` **SHAPE\_HEIGHTMAP** = `8`

The `Shape3D<class_Shape3D>` is a
`HeightMapShape3D<class_HeightMapShape3D>`.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer3D_ShapeType>` **SHAPE\_SOFT\_BODY** = `9`

The `Shape3D<class_Shape3D>` is used internally for a soft body. Any
attempt to create this kind of shape results in an error.

classref-enumeration-constant

`ShapeType<enum_PhysicsServer3D_ShapeType>` **SHAPE\_CUSTOM** = `10`

This constant is used internally by the engine. Any attempt to create
this kind of shape results in an error.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AreaParameter**: `🔗<enum_PhysicsServer3D_AreaParameter>`

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_GRAVITY\_OVERRIDE\_MODE** = `0`

Constant to set/get gravity override mode in an area. See
`AreaSpaceOverrideMode<enum_PhysicsServer3D_AreaSpaceOverrideMode>` for
possible values.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_GRAVITY** = `1`

Constant to set/get gravity strength in an area.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_GRAVITY\_VECTOR** = `2`

Constant to set/get gravity vector/center in an area.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_GRAVITY\_IS\_POINT** = `3`

Constant to set/get whether the gravity vector of an area is a
direction, or a center point.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_GRAVITY\_POINT\_UNIT\_DISTANCE** = `4`

Constant to set/get the distance at which the gravity strength is equal
to the gravity controlled by
`AREA_PARAM_GRAVITY<class_PhysicsServer3D_constant_AREA_PARAM_GRAVITY>`.
For example, on a planet 100 meters in radius with a surface gravity of
4.0 m/s², set the gravity to 4.0 and the unit distance to 100.0. The
gravity will have falloff according to the inverse square law, so in the
example, at 200 meters from the center the gravity will be 1.0 m/s²
(twice the distance, 1/4th the gravity), at 50 meters it will be 16.0
m/s² (half the distance, 4x the gravity), and so on.

The above is true only when the unit distance is a positive number. When
this is set to 0.0, the gravity will be constant regardless of distance.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_LINEAR\_DAMP\_OVERRIDE\_MODE** = `5`

Constant to set/get linear damping override mode in an area. See
`AreaSpaceOverrideMode<enum_PhysicsServer3D_AreaSpaceOverrideMode>` for
possible values.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_LINEAR\_DAMP** = `6`

Constant to set/get the linear damping factor of an area.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_ANGULAR\_DAMP\_OVERRIDE\_MODE** = `7`

Constant to set/get angular damping override mode in an area. See
`AreaSpaceOverrideMode<enum_PhysicsServer3D_AreaSpaceOverrideMode>` for
possible values.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_ANGULAR\_DAMP** = `8`

Constant to set/get the angular damping factor of an area.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_PRIORITY** = `9`

Constant to set/get the priority (order of processing) of an area.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_WIND\_FORCE\_MAGNITUDE** = `10`

Constant to set/get the magnitude of area-specific wind force. This wind
force only applies to `SoftBody3D<class_SoftBody3D>` nodes. Other
physics bodies are currently not affected by wind.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_WIND\_SOURCE** = `11`

Constant to set/get the 3D vector that specifies the origin from which
an area-specific wind blows.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_WIND\_DIRECTION** = `12`

Constant to set/get the 3D vector that specifies the direction in which
an area-specific wind blows.

classref-enumeration-constant

`AreaParameter<enum_PhysicsServer3D_AreaParameter>`
**AREA\_PARAM\_WIND\_ATTENUATION\_FACTOR** = `13`

Constant to set/get the exponential rate at which wind force decreases
with distance from its origin.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AreaSpaceOverrideMode**:
`🔗<enum_PhysicsServer3D_AreaSpaceOverrideMode>`

classref-enumeration-constant

`AreaSpaceOverrideMode<enum_PhysicsServer3D_AreaSpaceOverrideMode>`
**AREA\_SPACE\_OVERRIDE\_DISABLED** = `0`

This area does not affect gravity/damp. These are generally areas that
exist only to detect collisions, and objects entering or exiting them.

classref-enumeration-constant

`AreaSpaceOverrideMode<enum_PhysicsServer3D_AreaSpaceOverrideMode>`
**AREA\_SPACE\_OVERRIDE\_COMBINE** = `1`

This area adds its gravity/damp values to whatever has been calculated
so far. This way, many overlapping areas can combine their physics to
make interesting effects.

classref-enumeration-constant

`AreaSpaceOverrideMode<enum_PhysicsServer3D_AreaSpaceOverrideMode>`
**AREA\_SPACE\_OVERRIDE\_COMBINE\_REPLACE** = `2`

This area adds its gravity/damp values to whatever has been calculated
so far. Then stops taking into account the rest of the areas, even the
default one.

classref-enumeration-constant

`AreaSpaceOverrideMode<enum_PhysicsServer3D_AreaSpaceOverrideMode>`
**AREA\_SPACE\_OVERRIDE\_REPLACE** = `3`

This area replaces any gravity/damp, even the default one, and stops
taking into account the rest of the areas.

classref-enumeration-constant

`AreaSpaceOverrideMode<enum_PhysicsServer3D_AreaSpaceOverrideMode>`
**AREA\_SPACE\_OVERRIDE\_REPLACE\_COMBINE** = `4`

This area replaces any gravity/damp calculated so far, but keeps
calculating the rest of the areas, down to the default one.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BodyMode**: `🔗<enum_PhysicsServer3D_BodyMode>`

classref-enumeration-constant

`BodyMode<enum_PhysicsServer3D_BodyMode>` **BODY\_MODE\_STATIC** = `0`

Constant for static bodies. In this mode, a body can be only moved by
user code and doesn't collide with other bodies along its path when
moved.

classref-enumeration-constant

`BodyMode<enum_PhysicsServer3D_BodyMode>` **BODY\_MODE\_KINEMATIC** =
`1`

Constant for kinematic bodies. In this mode, a body can be only moved by
user code and collides with other bodies along its path.

classref-enumeration-constant

`BodyMode<enum_PhysicsServer3D_BodyMode>` **BODY\_MODE\_RIGID** = `2`

Constant for rigid bodies. In this mode, a body can be pushed by other
bodies and has forces applied.

classref-enumeration-constant

`BodyMode<enum_PhysicsServer3D_BodyMode>` **BODY\_MODE\_RIGID\_LINEAR**
= `3`

Constant for linear rigid bodies. In this mode, a body can not rotate,
and only its linear velocity is affected by external forces.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BodyParameter**: `🔗<enum_PhysicsServer3D_BodyParameter>`

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer3D_BodyParameter>`
**BODY\_PARAM\_BOUNCE** = `0`

Constant to set/get a body's bounce factor.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer3D_BodyParameter>`
**BODY\_PARAM\_FRICTION** = `1`

Constant to set/get a body's friction.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer3D_BodyParameter>`
**BODY\_PARAM\_MASS** = `2`

Constant to set/get a body's mass.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer3D_BodyParameter>`
**BODY\_PARAM\_INERTIA** = `3`

Constant to set/get a body's inertia.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer3D_BodyParameter>`
**BODY\_PARAM\_CENTER\_OF\_MASS** = `4`

Constant to set/get a body's center of mass position in the body's local
coordinate system.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer3D_BodyParameter>`
**BODY\_PARAM\_GRAVITY\_SCALE** = `5`

Constant to set/get a body's gravity multiplier.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer3D_BodyParameter>`
**BODY\_PARAM\_LINEAR\_DAMP\_MODE** = `6`

Constant to set/get a body's linear damping mode. See
`BodyDampMode<enum_PhysicsServer3D_BodyDampMode>` for possible values.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer3D_BodyParameter>`
**BODY\_PARAM\_ANGULAR\_DAMP\_MODE** = `7`

Constant to set/get a body's angular damping mode. See
`BodyDampMode<enum_PhysicsServer3D_BodyDampMode>` for possible values.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer3D_BodyParameter>`
**BODY\_PARAM\_LINEAR\_DAMP** = `8`

Constant to set/get a body's linear damping factor.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer3D_BodyParameter>`
**BODY\_PARAM\_ANGULAR\_DAMP** = `9`

Constant to set/get a body's angular damping factor.

classref-enumeration-constant

`BodyParameter<enum_PhysicsServer3D_BodyParameter>` **BODY\_PARAM\_MAX**
= `10`

Represents the size of the
`BodyParameter<enum_PhysicsServer3D_BodyParameter>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BodyDampMode**: `🔗<enum_PhysicsServer3D_BodyDampMode>`

classref-enumeration-constant

`BodyDampMode<enum_PhysicsServer3D_BodyDampMode>`
**BODY\_DAMP\_MODE\_COMBINE** = `0`

The body's damping value is added to any value set in areas or the
default value.

classref-enumeration-constant

`BodyDampMode<enum_PhysicsServer3D_BodyDampMode>`
**BODY\_DAMP\_MODE\_REPLACE** = `1`

The body's damping value replaces any value set in areas or the default
value.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BodyState**: `🔗<enum_PhysicsServer3D_BodyState>`

classref-enumeration-constant

`BodyState<enum_PhysicsServer3D_BodyState>` **BODY\_STATE\_TRANSFORM** =
`0`

Constant to set/get the current transform matrix of the body.

classref-enumeration-constant

`BodyState<enum_PhysicsServer3D_BodyState>`
**BODY\_STATE\_LINEAR\_VELOCITY** = `1`

Constant to set/get the current linear velocity of the body.

classref-enumeration-constant

`BodyState<enum_PhysicsServer3D_BodyState>`
**BODY\_STATE\_ANGULAR\_VELOCITY** = `2`

Constant to set/get the current angular velocity of the body.

classref-enumeration-constant

`BodyState<enum_PhysicsServer3D_BodyState>` **BODY\_STATE\_SLEEPING** =
`3`

Constant to sleep/wake up a body, or to get whether it is sleeping.

classref-enumeration-constant

`BodyState<enum_PhysicsServer3D_BodyState>` **BODY\_STATE\_CAN\_SLEEP**
= `4`

Constant to set/get whether the body can sleep.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AreaBodyStatus**: `🔗<enum_PhysicsServer3D_AreaBodyStatus>`

classref-enumeration-constant

`AreaBodyStatus<enum_PhysicsServer3D_AreaBodyStatus>`
**AREA\_BODY\_ADDED** = `0`

The value of the first parameter and area callback function receives,
when an object enters one of its shapes.

classref-enumeration-constant

`AreaBodyStatus<enum_PhysicsServer3D_AreaBodyStatus>`
**AREA\_BODY\_REMOVED** = `1`

The value of the first parameter and area callback function receives,
when an object exits one of its shapes.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ProcessInfo**: `🔗<enum_PhysicsServer3D_ProcessInfo>`

classref-enumeration-constant

`ProcessInfo<enum_PhysicsServer3D_ProcessInfo>`
**INFO\_ACTIVE\_OBJECTS** = `0`

Constant to get the number of objects that are not sleeping.

classref-enumeration-constant

`ProcessInfo<enum_PhysicsServer3D_ProcessInfo>`
**INFO\_COLLISION\_PAIRS** = `1`

Constant to get the number of possible collisions.

classref-enumeration-constant

`ProcessInfo<enum_PhysicsServer3D_ProcessInfo>` **INFO\_ISLAND\_COUNT**
= `2`

Constant to get the number of space regions where a collision could
occur.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SpaceParameter**: `🔗<enum_PhysicsServer3D_SpaceParameter>`

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer3D_SpaceParameter>`
**SPACE\_PARAM\_CONTACT\_RECYCLE\_RADIUS** = `0`

Constant to set/get the maximum distance a pair of bodies has to move
before their collision status has to be recalculated.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer3D_SpaceParameter>`
**SPACE\_PARAM\_CONTACT\_MAX\_SEPARATION** = `1`

Constant to set/get the maximum distance a shape can be from another
before they are considered separated and the contact is discarded.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer3D_SpaceParameter>`
**SPACE\_PARAM\_CONTACT\_MAX\_ALLOWED\_PENETRATION** = `2`

Constant to set/get the maximum distance a shape can penetrate another
shape before it is considered a collision.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer3D_SpaceParameter>`
**SPACE\_PARAM\_CONTACT\_DEFAULT\_BIAS** = `3`

Constant to set/get the default solver bias for all physics contacts. A
solver bias is a factor controlling how much two objects "rebound",
after overlapping, to avoid leaving them in that state because of
numerical imprecision.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer3D_SpaceParameter>`
**SPACE\_PARAM\_BODY\_LINEAR\_VELOCITY\_SLEEP\_THRESHOLD** = `4`

Constant to set/get the threshold linear velocity of activity. A body
marked as potentially inactive for both linear and angular velocity will
be put to sleep after the time given.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer3D_SpaceParameter>`
**SPACE\_PARAM\_BODY\_ANGULAR\_VELOCITY\_SLEEP\_THRESHOLD** = `5`

Constant to set/get the threshold angular velocity of activity. A body
marked as potentially inactive for both linear and angular velocity will
be put to sleep after the time given.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer3D_SpaceParameter>`
**SPACE\_PARAM\_BODY\_TIME\_TO\_SLEEP** = `6`

Constant to set/get the maximum time of activity. A body marked as
potentially inactive for both linear and angular velocity will be put to
sleep after this time.

classref-enumeration-constant

`SpaceParameter<enum_PhysicsServer3D_SpaceParameter>`
**SPACE\_PARAM\_SOLVER\_ITERATIONS** = `7`

Constant to set/get the number of solver iterations for contacts and
constraints. The greater the number of iterations, the more accurate the
collisions and constraints will be. However, a greater number of
iterations requires more CPU power, which can decrease performance.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BodyAxis**: `🔗<enum_PhysicsServer3D_BodyAxis>`

classref-enumeration-constant

`BodyAxis<enum_PhysicsServer3D_BodyAxis>` **BODY\_AXIS\_LINEAR\_X** =
`1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BodyAxis<enum_PhysicsServer3D_BodyAxis>` **BODY\_AXIS\_LINEAR\_Y** =
`2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BodyAxis<enum_PhysicsServer3D_BodyAxis>` **BODY\_AXIS\_LINEAR\_Z** =
`4`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BodyAxis<enum_PhysicsServer3D_BodyAxis>` **BODY\_AXIS\_ANGULAR\_X** =
`8`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BodyAxis<enum_PhysicsServer3D_BodyAxis>` **BODY\_AXIS\_ANGULAR\_Y** =
`16`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`BodyAxis<enum_PhysicsServer3D_BodyAxis>` **BODY\_AXIS\_ANGULAR\_Z** =
`32`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **area\_add\_shape**(area: `RID<class_RID>`,
shape: `RID<class_RID>`, transform: `Transform3D<class_Transform3D>` =
Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0), disabled:
`bool<class_bool>` = false)
`🔗<class_PhysicsServer3D_method_area_add_shape>`

Adds a shape to the area, along with a transform matrix. Shapes are
usually referenced by their index, so you should track which shape has a
given index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_attach\_object\_instance\_id**(area:
`RID<class_RID>`, id: `int<class_int>`)
`🔗<class_PhysicsServer3D_method_area_attach_object_instance_id>`

Assigns the area to a descendant of `Object<class_Object>`, so it can
exist in the node tree.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_clear\_shapes**(area:
`RID<class_RID>`) `🔗<class_PhysicsServer3D_method_area_clear_shapes>`

Removes all shapes from an area. It does not delete the shapes, so they
can be reassigned later.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **area\_create**()
`🔗<class_PhysicsServer3D_method_area_create>`

Creates a 3D area object in the physics server, and returns the
`RID<class_RID>` that identifies it. The default settings for the
created area include a collision layer and mask set to `1`, and
`monitorable` set to `false`.

Use `area_add_shape<class_PhysicsServer3D_method_area_add_shape>` to add
shapes to it, use
`area_set_transform<class_PhysicsServer3D_method_area_set_transform>` to
set its transform, and use
`area_set_space<class_PhysicsServer3D_method_area_set_space>` to add the
area to a space. If you want the area to be detectable use
`area_set_monitorable<class_PhysicsServer3D_method_area_set_monitorable>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **area\_get\_collision\_layer**(area: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_area_get_collision_layer>`

Returns the physics layer or layers an area belongs to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **area\_get\_collision\_mask**(area: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_area_get_collision_mask>`

Returns the physics layer or layers an area can contact with.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **area\_get\_object\_instance\_id**(area:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_area_get_object_instance_id>`

Gets the instance ID of the object the area is assigned to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **area\_get\_param**(area: `RID<class_RID>`,
param: `AreaParameter<enum_PhysicsServer3D_AreaParameter>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_area_get_param>`

Returns an area parameter value. A list of available parameters is on
the `AreaParameter<enum_PhysicsServer3D_AreaParameter>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **area\_get\_shape**(area: `RID<class_RID>`,
shape\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_area_get_shape>`

Returns the `RID<class_RID>` of the nth shape of an area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **area\_get\_shape\_count**(area: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_area_get_shape_count>`

Returns the number of shapes assigned to an area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **area\_get\_shape\_transform**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_area_get_shape_transform>`

Returns the transform matrix of a shape within an area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **area\_get\_space**(area: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_area_get_space>`

Returns the space assigned to the area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **area\_get\_transform**(area:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_area_get_transform>`

Returns the transform matrix for an area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_remove\_shape**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`🔗<class_PhysicsServer3D_method_area_remove_shape>`

Removes a shape from an area. It does not delete the shape, so it can be
reassigned later.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_area\_monitor\_callback**(area:
`RID<class_RID>`, callback: `Callable<class_Callable>`)
`🔗<class_PhysicsServer3D_method_area_set_area_monitor_callback>`

Sets the area's area monitor callback. This callback will be called when
any other (shape of an) area enters or exits (a shape of) the given
area, and must take the following five parameters:

1.  an integer `status`: either
    `AREA_BODY_ADDED<class_PhysicsServer3D_constant_AREA_BODY_ADDED>` or
    `AREA_BODY_REMOVED<class_PhysicsServer3D_constant_AREA_BODY_REMOVED>`
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
`🔗<class_PhysicsServer3D_method_area_set_collision_layer>`

Assigns the area to one or many physics layers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_collision\_mask**(area:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_PhysicsServer3D_method_area_set_collision_mask>`

Sets which physics layers the area will monitor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_monitor\_callback**(area:
`RID<class_RID>`, callback: `Callable<class_Callable>`)
`🔗<class_PhysicsServer3D_method_area_set_monitor_callback>`

Sets the area's body monitor callback. This callback will be called when
any other (shape of a) body enters or exits (a shape of) the given area,
and must take the following five parameters:

1.  an integer `status`: either
    `AREA_BODY_ADDED<class_PhysicsServer3D_constant_AREA_BODY_ADDED>` or
    `AREA_BODY_REMOVED<class_PhysicsServer3D_constant_AREA_BODY_REMOVED>`
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
`🔗<class_PhysicsServer3D_method_area_set_monitorable>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_param**(area: `RID<class_RID>`,
param: `AreaParameter<enum_PhysicsServer3D_AreaParameter>`, value:
`Variant<class_Variant>`)
`🔗<class_PhysicsServer3D_method_area_set_param>`

Sets the value for an area parameter. A list of available parameters is
on the `AreaParameter<enum_PhysicsServer3D_AreaParameter>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_ray\_pickable**(area:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_area_set_ray_pickable>`

Sets object pickable with rays.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_shape**(area: `RID<class_RID>`,
shape\_idx: `int<class_int>`, shape: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_area_set_shape>`

Substitutes a given area shape by another. The old shape is selected by
its index, the new one by its `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_shape\_disabled**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`, disabled:
`bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_area_set_shape_disabled>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_shape\_transform**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`, transform:
`Transform3D<class_Transform3D>`)
`🔗<class_PhysicsServer3D_method_area_set_shape_transform>`

Sets the transform matrix for an area shape.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_space**(area: `RID<class_RID>`,
space: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_area_set_space>`

Assigns a space to the area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **area\_set\_transform**(area:
`RID<class_RID>`, transform: `Transform3D<class_Transform3D>`)
`🔗<class_PhysicsServer3D_method_area_set_transform>`

Sets the transform matrix for an area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_add\_collision\_exception**(body:
`RID<class_RID>`, excepted\_body: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_body_add_collision_exception>`

Adds a body to the list of bodies exempt from collisions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_add\_constant\_central\_force**(body:
`RID<class_RID>`, force: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_body_add_constant_central_force>`

Adds a constant directional force without affecting rotation that keeps
being applied over time until cleared with
`body_set_constant_force(body, Vector3(0, 0, 0))`.

This is equivalent to using
`body_add_constant_force<class_PhysicsServer3D_method_body_add_constant_force>`
at the body's center of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_add\_constant\_force**(body:
`RID<class_RID>`, force: `Vector3<class_Vector3>`, position:
`Vector3<class_Vector3>` = Vector3(0, 0, 0))
`🔗<class_PhysicsServer3D_method_body_add_constant_force>`

Adds a constant positioned force to the body that keeps being applied
over time until cleared with
`body_set_constant_force(body, Vector3(0, 0, 0))`.

`position` is the offset from the body origin in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_add\_constant\_torque**(body:
`RID<class_RID>`, torque: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_body_add_constant_torque>`

Adds a constant rotational force without affecting position that keeps
being applied over time until cleared with
`body_set_constant_torque(body, Vector3(0, 0, 0))`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_add\_shape**(body: `RID<class_RID>`,
shape: `RID<class_RID>`, transform: `Transform3D<class_Transform3D>` =
Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0), disabled:
`bool<class_bool>` = false)
`🔗<class_PhysicsServer3D_method_body_add_shape>`

Adds a shape to the body, along with a transform matrix. Shapes are
usually referenced by their index, so you should track which shape has a
given index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_central\_force**(body:
`RID<class_RID>`, force: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_body_apply_central_force>`

Applies a directional force without affecting rotation. A force is time
dependent and meant to be applied every physics update.

This is equivalent to using
`body_apply_force<class_PhysicsServer3D_method_body_apply_force>` at the
body's center of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_central\_impulse**(body:
`RID<class_RID>`, impulse: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_body_apply_central_impulse>`

Applies a directional impulse without affecting rotation.

An impulse is time-independent! Applying an impulse every frame would
result in a framerate-dependent force. For this reason, it should only
be used when simulating one-time impacts (use the "\_force" functions
otherwise).

This is equivalent to using
`body_apply_impulse<class_PhysicsServer3D_method_body_apply_impulse>` at
the body's center of mass.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_force**(body: `RID<class_RID>`,
force: `Vector3<class_Vector3>`, position: `Vector3<class_Vector3>` =
Vector3(0, 0, 0)) `🔗<class_PhysicsServer3D_method_body_apply_force>`

Applies a positioned force to the body. A force is time dependent and
meant to be applied every physics update.

`position` is the offset from the body origin in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_impulse**(body:
`RID<class_RID>`, impulse: `Vector3<class_Vector3>`, position:
`Vector3<class_Vector3>` = Vector3(0, 0, 0))
`🔗<class_PhysicsServer3D_method_body_apply_impulse>`

Applies a positioned impulse to the body.

An impulse is time-independent! Applying an impulse every frame would
result in a framerate-dependent force. For this reason, it should only
be used when simulating one-time impacts (use the "\_force" functions
otherwise).

`position` is the offset from the body origin in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_torque**(body:
`RID<class_RID>`, torque: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_body_apply_torque>`

Applies a rotational force without affecting position. A force is time
dependent and meant to be applied every physics update.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_apply\_torque\_impulse**(body:
`RID<class_RID>`, impulse: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_body_apply_torque_impulse>`

Applies a rotational impulse to the body without affecting the position.

An impulse is time-independent! Applying an impulse every frame would
result in a framerate-dependent force. For this reason, it should only
be used when simulating one-time impacts (use the "\_force" functions
otherwise).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_attach\_object\_instance\_id**(body:
`RID<class_RID>`, id: `int<class_int>`)
`🔗<class_PhysicsServer3D_method_body_attach_object_instance_id>`

Assigns the area to a descendant of `Object<class_Object>`, so it can
exist in the node tree.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_clear\_shapes**(body:
`RID<class_RID>`) `🔗<class_PhysicsServer3D_method_body_clear_shapes>`

Removes all shapes from a body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **body\_create**()
`🔗<class_PhysicsServer3D_method_body_create>`

Creates a 3D body object in the physics server, and returns the
`RID<class_RID>` that identifies it. The default settings for the
created area include a collision layer and mask set to `1`, and body
mode set to
`BODY_MODE_RIGID<class_PhysicsServer3D_constant_BODY_MODE_RIGID>`.

Use `body_add_shape<class_PhysicsServer3D_method_body_add_shape>` to add
shapes to it, use
`body_set_state<class_PhysicsServer3D_method_body_set_state>` to set its
transform, and use
`body_set_space<class_PhysicsServer3D_method_body_set_space>` to add the
body to a space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **body\_get\_collision\_layer**(body: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_collision_layer>`

Returns the physics layer or layers a body belongs to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **body\_get\_collision\_mask**(body: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_collision_mask>`

Returns the physics layer or layers a body can collide with.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **body\_get\_collision\_priority**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_collision_priority>`

Returns the body's collision priority.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **body\_get\_constant\_force**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_constant_force>`

Returns the body's total constant positional forces applied during each
physics update.

See
`body_add_constant_force<class_PhysicsServer3D_method_body_add_constant_force>`
and
`body_add_constant_central_force<class_PhysicsServer3D_method_body_add_constant_central_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **body\_get\_constant\_torque**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_constant_torque>`

Returns the body's total constant rotational forces applied during each
physics update.

See
`body_add_constant_torque<class_PhysicsServer3D_method_body_add_constant_torque>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PhysicsDirectBodyState3D<class_PhysicsDirectBodyState3D>`
**body\_get\_direct\_state**(body: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_body_get_direct_state>`

Returns the `PhysicsDirectBodyState3D<class_PhysicsDirectBodyState3D>`
of the body. Returns `null` if the body is destroyed or removed from the
physics space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **body\_get\_max\_contacts\_reported**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_max_contacts_reported>`

Returns the maximum contacts that can be reported. See
`body_set_max_contacts_reported<class_PhysicsServer3D_method_body_set_max_contacts_reported>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`BodyMode<enum_PhysicsServer3D_BodyMode>` **body\_get\_mode**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_mode>`

Returns the body mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **body\_get\_object\_instance\_id**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_object_instance_id>`

Gets the instance ID of the object the area is assigned to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **body\_get\_param**(body: `RID<class_RID>`,
param: `BodyParameter<enum_PhysicsServer3D_BodyParameter>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_param>`

Returns the value of a body parameter. A list of available parameters is
on the `BodyParameter<enum_PhysicsServer3D_BodyParameter>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **body\_get\_shape**(body: `RID<class_RID>`,
shape\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_shape>`

Returns the `RID<class_RID>` of the nth shape of a body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **body\_get\_shape\_count**(body: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_shape_count>`

Returns the number of shapes assigned to a body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **body\_get\_shape\_transform**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_shape_transform>`

Returns the transform matrix of a body shape.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **body\_get\_space**(body: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_space>`

Returns the `RID<class_RID>` of the space assigned to a body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **body\_get\_state**(body: `RID<class_RID>`,
state: `BodyState<enum_PhysicsServer3D_BodyState>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_get_state>`

Returns a body state.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **body\_is\_axis\_locked**(body: `RID<class_RID>`,
axis: `BodyAxis<enum_PhysicsServer3D_BodyAxis>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_is_axis_locked>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**body\_is\_continuous\_collision\_detection\_enabled**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_is_continuous_collision_detection_enabled>`

If `true`, the continuous collision detection mode is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **body\_is\_omitting\_force\_integration**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_body_is_omitting_force_integration>`

Returns `true` if the body is omitting the standard force integration.
See
`body_set_omit_force_integration<class_PhysicsServer3D_method_body_set_omit_force_integration>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_remove\_collision\_exception**(body:
`RID<class_RID>`, excepted\_body: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_body_remove_collision_exception>`

Removes a body from the list of bodies exempt from collisions.

Continuous collision detection tries to predict where a moving body will
collide, instead of moving it and correcting its movement if it
collided.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_remove\_shape**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`🔗<class_PhysicsServer3D_method_body_remove_shape>`

Removes a shape from a body. The shape is not deleted, so it can be
reused afterwards.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_reset\_mass\_properties**(body:
`RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_body_reset_mass_properties>`

Restores the default inertia and center of mass based on shapes to
cancel any custom values previously set using
`body_set_param<class_PhysicsServer3D_method_body_set_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_axis\_lock**(body:
`RID<class_RID>`, axis: `BodyAxis<enum_PhysicsServer3D_BodyAxis>`, lock:
`bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_body_set_axis_lock>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_axis\_velocity**(body:
`RID<class_RID>`, axis\_velocity: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_body_set_axis_velocity>`

Sets an axis velocity. The velocity in the given vector axis will be set
as the given vector length. This is useful for jumping behavior.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_collision\_layer**(body:
`RID<class_RID>`, layer: `int<class_int>`)
`🔗<class_PhysicsServer3D_method_body_set_collision_layer>`

Sets the physics layer or layers a body belongs to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_collision\_mask**(body:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_PhysicsServer3D_method_body_set_collision_mask>`

Sets the physics layer or layers a body can collide with.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_collision\_priority**(body:
`RID<class_RID>`, priority: `float<class_float>`)
`🔗<class_PhysicsServer3D_method_body_set_collision_priority>`

Sets the body's collision priority.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_constant\_force**(body:
`RID<class_RID>`, force: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_body_set_constant_force>`

Sets the body's total constant positional forces applied during each
physics update.

See
`body_add_constant_force<class_PhysicsServer3D_method_body_add_constant_force>`
and
`body_add_constant_central_force<class_PhysicsServer3D_method_body_add_constant_central_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_constant\_torque**(body:
`RID<class_RID>`, torque: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_body_set_constant_torque>`

Sets the body's total constant rotational forces applied during each
physics update.

See
`body_add_constant_torque<class_PhysicsServer3D_method_body_add_constant_torque>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**body\_set\_enable\_continuous\_collision\_detection**(body:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_body_set_enable_continuous_collision_detection>`

If `true`, the continuous collision detection mode is enabled.

Continuous collision detection tries to predict where a moving body will
collide, instead of moving it and correcting its movement if it
collided.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**body\_set\_force\_integration\_callback**(body: `RID<class_RID>`,
callable: `Callable<class_Callable>`, userdata: `Variant<class_Variant>`
= null)
`🔗<class_PhysicsServer3D_method_body_set_force_integration_callback>`

Sets the body's custom force integration callback function to
`callable`. Use an empty `Callable<class_Callable>` (`Callable()`) to
clear the custom callback.

The function `callable` will be called every physics tick, before the
standard force integration (see
`body_set_omit_force_integration<class_PhysicsServer3D_method_body_set_omit_force_integration>`).
It can be used for example to update the body's linear and angular
velocity based on contact with other bodies.

If `userdata` is not `null`, the function `callable` must take the
following two parameters:

1.  `state`: a
    `PhysicsDirectBodyState3D<class_PhysicsDirectBodyState3D>`, used to
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
`🔗<class_PhysicsServer3D_method_body_set_max_contacts_reported>`

Sets the maximum contacts to report. Bodies can keep a log of the
contacts with other bodies. This is enabled by setting the maximum
number of contacts reported to a number greater than 0.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_mode**(body: `RID<class_RID>`,
mode: `BodyMode<enum_PhysicsServer3D_BodyMode>`)
`🔗<class_PhysicsServer3D_method_body_set_mode>`

Sets the body mode, from one of the
`BodyMode<enum_PhysicsServer3D_BodyMode>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_omit\_force\_integration**(body:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_body_set_omit_force_integration>`

Sets whether the body omits the standard force integration. If `enable`
is `true`, the body will not automatically use applied forces, torques,
and damping to update the body's linear and angular velocity. In this
case,
`body_set_force_integration_callback<class_PhysicsServer3D_method_body_set_force_integration_callback>`
can be used to manually update the linear and angular velocity instead.

This method is called when the property
`RigidBody3D.custom_integrator<class_RigidBody3D_property_custom_integrator>`
is set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_param**(body: `RID<class_RID>`,
param: `BodyParameter<enum_PhysicsServer3D_BodyParameter>`, value:
`Variant<class_Variant>`)
`🔗<class_PhysicsServer3D_method_body_set_param>`

Sets a body parameter. A list of available parameters is on the
`BodyParameter<enum_PhysicsServer3D_BodyParameter>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_ray\_pickable**(body:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_body_set_ray_pickable>`

Sets the body pickable with rays if `enable` is set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_shape**(body: `RID<class_RID>`,
shape\_idx: `int<class_int>`, shape: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_body_set_shape>`

Substitutes a given body shape by another. The old shape is selected by
its index, the new one by its `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_shape\_disabled**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`, disabled:
`bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_body_set_shape_disabled>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_shape\_transform**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`, transform:
`Transform3D<class_Transform3D>`)
`🔗<class_PhysicsServer3D_method_body_set_shape_transform>`

Sets the transform matrix for a body shape.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_space**(body: `RID<class_RID>`,
space: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_body_set_space>`

Assigns a space to the body (see
`space_create<class_PhysicsServer3D_method_space_create>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_state**(body: `RID<class_RID>`,
state: `BodyState<enum_PhysicsServer3D_BodyState>`, value:
`Variant<class_Variant>`)
`🔗<class_PhysicsServer3D_method_body_set_state>`

Sets a body state (see `BodyState<enum_PhysicsServer3D_BodyState>`
constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **body\_set\_state\_sync\_callback**(body:
`RID<class_RID>`, callable: `Callable<class_Callable>`)
`🔗<class_PhysicsServer3D_method_body_set_state_sync_callback>`

Sets the body's state synchronization callback function to `callable`.
Use an empty `Callable<class_Callable>` (`Callable()`) to clear the
callback.

The function `callable` will be called every physics frame, assuming
that the body was active during the previous physics tick, and can be
used to fetch the latest state from the physics server.

The function `callable` must take the following parameters:

1.  `state`: a
    `PhysicsDirectBodyState3D<class_PhysicsDirectBodyState3D>`, used to
    retrieve the body's state.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **body\_test\_motion**(body: `RID<class_RID>`,
parameters:
`PhysicsTestMotionParameters3D<class_PhysicsTestMotionParameters3D>`,
result: `PhysicsTestMotionResult3D<class_PhysicsTestMotionResult3D>` =
null) `🔗<class_PhysicsServer3D_method_body_test_motion>`

Returns `true` if a collision would result from moving along a motion
vector from a given point in space.
`PhysicsTestMotionParameters3D<class_PhysicsTestMotionParameters3D>` is
passed to set motion parameters.
`PhysicsTestMotionResult3D<class_PhysicsTestMotionResult3D>` can be
passed to return additional information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **box\_shape\_create**()
`🔗<class_PhysicsServer3D_method_box_shape_create>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **capsule\_shape\_create**()
`🔗<class_PhysicsServer3D_method_capsule_shape_create>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **concave\_polygon\_shape\_create**()
`🔗<class_PhysicsServer3D_method_concave_polygon_shape_create>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **cone\_twist\_joint\_get\_param**(joint:
`RID<class_RID>`, param:
`ConeTwistJointParam<enum_PhysicsServer3D_ConeTwistJointParam>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_cone_twist_joint_get_param>`

Gets a cone\_twist\_joint parameter (see
`ConeTwistJointParam<enum_PhysicsServer3D_ConeTwistJointParam>`
constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **cone\_twist\_joint\_set\_param**(joint:
`RID<class_RID>`, param:
`ConeTwistJointParam<enum_PhysicsServer3D_ConeTwistJointParam>`, value:
`float<class_float>`)
`🔗<class_PhysicsServer3D_method_cone_twist_joint_set_param>`

Sets a cone\_twist\_joint parameter (see
`ConeTwistJointParam<enum_PhysicsServer3D_ConeTwistJointParam>`
constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **convex\_polygon\_shape\_create**()
`🔗<class_PhysicsServer3D_method_convex_polygon_shape_create>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **custom\_shape\_create**()
`🔗<class_PhysicsServer3D_method_custom_shape_create>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **cylinder\_shape\_create**()
`🔗<class_PhysicsServer3D_method_cylinder_shape_create>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **free\_rid**(rid: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_free_rid>`

Destroys any of the objects created by PhysicsServer3D. If the
`RID<class_RID>` passed is not one of the objects that can be created by
PhysicsServer3D, an error will be sent to the console.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **generic\_6dof\_joint\_get\_flag**(joint:
`RID<class_RID>`, axis: Vector3.Axis, flag:
`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_generic_6dof_joint_get_flag>`

Returns the value of a generic 6DOF joint flag. See
`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>` for the
list of available flags.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **generic\_6dof\_joint\_get\_param**(joint:
`RID<class_RID>`, axis: Vector3.Axis, param:
`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_generic_6dof_joint_get_param>`

Returns the value of a generic 6DOF joint parameter. See
`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>` for the
list of available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **generic\_6dof\_joint\_set\_flag**(joint:
`RID<class_RID>`, axis: Vector3.Axis, flag:
`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>`, enable:
`bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_generic_6dof_joint_set_flag>`

Sets the value of a given generic 6DOF joint flag. See
`G6DOFJointAxisFlag<enum_PhysicsServer3D_G6DOFJointAxisFlag>` for the
list of available flags.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **generic\_6dof\_joint\_set\_param**(joint:
`RID<class_RID>`, axis: Vector3.Axis, param:
`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>`, value:
`float<class_float>`)
`🔗<class_PhysicsServer3D_method_generic_6dof_joint_set_param>`

Sets the value of a given generic 6DOF joint parameter. See
`G6DOFJointAxisParam<enum_PhysicsServer3D_G6DOFJointAxisParam>` for the
list of available parameters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_process\_info**(process\_info:
`ProcessInfo<enum_PhysicsServer3D_ProcessInfo>`)
`🔗<class_PhysicsServer3D_method_get_process_info>`

Returns information about the current state of the 3D physics engine.
See `ProcessInfo<enum_PhysicsServer3D_ProcessInfo>` for a list of
available states.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **heightmap\_shape\_create**()
`🔗<class_PhysicsServer3D_method_heightmap_shape_create>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **hinge\_joint\_get\_flag**(joint: `RID<class_RID>`,
flag: `HingeJointFlag<enum_PhysicsServer3D_HingeJointFlag>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_hinge_joint_get_flag>`

Gets a hinge\_joint flag (see
`HingeJointFlag<enum_PhysicsServer3D_HingeJointFlag>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **hinge\_joint\_get\_param**(joint:
`RID<class_RID>`, param:
`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_hinge_joint_get_param>`

Gets a hinge\_joint parameter (see
`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **hinge\_joint\_set\_flag**(joint:
`RID<class_RID>`, flag:
`HingeJointFlag<enum_PhysicsServer3D_HingeJointFlag>`, enabled:
`bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_hinge_joint_set_flag>`

Sets a hinge\_joint flag (see
`HingeJointFlag<enum_PhysicsServer3D_HingeJointFlag>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **hinge\_joint\_set\_param**(joint:
`RID<class_RID>`, param:
`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>`, value:
`float<class_float>`)
`🔗<class_PhysicsServer3D_method_hinge_joint_set_param>`

Sets a hinge\_joint parameter (see
`HingeJointParam<enum_PhysicsServer3D_HingeJointParam>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_clear**(joint: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_joint_clear>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **joint\_create**()
`🔗<class_PhysicsServer3D_method_joint_create>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**joint\_disable\_collisions\_between\_bodies**(joint: `RID<class_RID>`,
disable: `bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_joint_disable_collisions_between_bodies>`

Sets whether the bodies attached to the `Joint3D<class_Joint3D>` will
collide with each other.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **joint\_get\_solver\_priority**(joint:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_joint_get_solver_priority>`

Gets the priority value of the Joint3D.

classref-item-separator

------------------------------------------------------------------------

classref-method

`JointType<enum_PhysicsServer3D_JointType>` **joint\_get\_type**(joint:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_joint_get_type>`

Returns the type of the Joint3D.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**joint\_is\_disabled\_collisions\_between\_bodies**(joint:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_joint_is_disabled_collisions_between_bodies>`

Returns whether the bodies attached to the `Joint3D<class_Joint3D>` will
collide with each other.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_make\_cone\_twist**(joint:
`RID<class_RID>`, body\_A: `RID<class_RID>`, local\_ref\_A:
`Transform3D<class_Transform3D>`, body\_B: `RID<class_RID>`,
local\_ref\_B: `Transform3D<class_Transform3D>`)
`🔗<class_PhysicsServer3D_method_joint_make_cone_twist>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_make\_generic\_6dof**(joint:
`RID<class_RID>`, body\_A: `RID<class_RID>`, local\_ref\_A:
`Transform3D<class_Transform3D>`, body\_B: `RID<class_RID>`,
local\_ref\_B: `Transform3D<class_Transform3D>`)
`🔗<class_PhysicsServer3D_method_joint_make_generic_6dof>`

Make the joint a generic six degrees of freedom (6DOF) joint. Use
`generic_6dof_joint_set_flag<class_PhysicsServer3D_method_generic_6dof_joint_set_flag>`
and
`generic_6dof_joint_set_param<class_PhysicsServer3D_method_generic_6dof_joint_set_param>`
to set the joint's flags and parameters respectively.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_make\_hinge**(joint:
`RID<class_RID>`, body\_A: `RID<class_RID>`, hinge\_A:
`Transform3D<class_Transform3D>`, body\_B: `RID<class_RID>`, hinge\_B:
`Transform3D<class_Transform3D>`)
`🔗<class_PhysicsServer3D_method_joint_make_hinge>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_make\_pin**(joint: `RID<class_RID>`,
body\_A: `RID<class_RID>`, local\_A: `Vector3<class_Vector3>`, body\_B:
`RID<class_RID>`, local\_B: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_joint_make_pin>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_make\_slider**(joint:
`RID<class_RID>`, body\_A: `RID<class_RID>`, local\_ref\_A:
`Transform3D<class_Transform3D>`, body\_B: `RID<class_RID>`,
local\_ref\_B: `Transform3D<class_Transform3D>`)
`🔗<class_PhysicsServer3D_method_joint_make_slider>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **joint\_set\_solver\_priority**(joint:
`RID<class_RID>`, priority: `int<class_int>`)
`🔗<class_PhysicsServer3D_method_joint_set_solver_priority>`

Sets the priority value of the Joint3D.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **pin\_joint\_get\_local\_a**(joint:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_pin_joint_get_local_a>`

Returns position of the joint in the local space of body a of the joint.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **pin\_joint\_get\_local\_b**(joint:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_pin_joint_get_local_b>`

Returns position of the joint in the local space of body b of the joint.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **pin\_joint\_get\_param**(joint: `RID<class_RID>`,
param: `PinJointParam<enum_PhysicsServer3D_PinJointParam>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_pin_joint_get_param>`

Gets a pin\_joint parameter (see
`PinJointParam<enum_PhysicsServer3D_PinJointParam>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **pin\_joint\_set\_local\_a**(joint:
`RID<class_RID>`, local\_A: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_pin_joint_set_local_a>`

Sets position of the joint in the local space of body a of the joint.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **pin\_joint\_set\_local\_b**(joint:
`RID<class_RID>`, local\_B: `Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_pin_joint_set_local_b>`

Sets position of the joint in the local space of body b of the joint.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **pin\_joint\_set\_param**(joint:
`RID<class_RID>`, param:
`PinJointParam<enum_PhysicsServer3D_PinJointParam>`, value:
`float<class_float>`)
`🔗<class_PhysicsServer3D_method_pin_joint_set_param>`

Sets a pin\_joint parameter (see
`PinJointParam<enum_PhysicsServer3D_PinJointParam>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **separation\_ray\_shape\_create**()
`🔗<class_PhysicsServer3D_method_separation_ray_shape_create>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_active**(active: `bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_set_active>`

Activates or deactivates the 3D physics engine.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **shape\_get\_data**(shape: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_shape_get_data>`

Returns the shape data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **shape\_get\_margin**(shape: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_shape_get_margin>`

Returns the collision margin for the shape.

\*\*Note:\*\* This is not used in Godot Physics, so will always return
`0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ShapeType<enum_PhysicsServer3D_ShapeType>` **shape\_get\_type**(shape:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_shape_get_type>`

Returns the type of shape (see
`ShapeType<enum_PhysicsServer3D_ShapeType>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **shape\_set\_data**(shape: `RID<class_RID>`,
data: `Variant<class_Variant>`)
`🔗<class_PhysicsServer3D_method_shape_set_data>`

Sets the shape data that defines its shape and size. The data to be
passed depends on the kind of shape created
`shape_get_type<class_PhysicsServer3D_method_shape_get_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **shape\_set\_margin**(shape:
`RID<class_RID>`, margin: `float<class_float>`)
`🔗<class_PhysicsServer3D_method_shape_set_margin>`

Sets the collision margin for the shape.

\*\*Note:\*\* This is not used in Godot Physics.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **slider\_joint\_get\_param**(joint:
`RID<class_RID>`, param:
`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_slider_joint_get_param>`

Gets a slider\_joint parameter (see
`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **slider\_joint\_set\_param**(joint:
`RID<class_RID>`, param:
`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>`, value:
`float<class_float>`)
`🔗<class_PhysicsServer3D_method_slider_joint_set_param>`

Gets a slider\_joint parameter (see
`SliderJointParam<enum_PhysicsServer3D_SliderJointParam>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**soft\_body\_add\_collision\_exception**(body: `RID<class_RID>`,
body\_b: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_soft_body_add_collision_exception>`

Adds the given body to the list of bodies exempt from collisions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **soft\_body\_create**()
`🔗<class_PhysicsServer3D_method_soft_body_create>`

Creates a new soft body and returns its internal `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AABB<class_AABB>` **soft\_body\_get\_bounds**(body: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_bounds>`

Returns the bounds of the given soft body in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **soft\_body\_get\_collision\_layer**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_collision_layer>`

Returns the physics layer or layers that the given soft body belongs to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **soft\_body\_get\_collision\_mask**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_collision_mask>`

Returns the physics layer or layers that the given soft body can collide
with.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **soft\_body\_get\_damping\_coefficient**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_damping_coefficient>`

Returns the damping coefficient of the given soft body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **soft\_body\_get\_drag\_coefficient**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_drag_coefficient>`

Returns the drag coefficient of the given soft body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **soft\_body\_get\_linear\_stiffness**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_linear_stiffness>`

Returns the linear stiffness of the given soft body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>`
**soft\_body\_get\_point\_global\_position**(body: `RID<class_RID>`,
point\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_point_global_position>`

Returns the current position of the given soft body point in global
coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **soft\_body\_get\_pressure\_coefficient**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_pressure_coefficient>`

Returns the pressure coefficient of the given soft body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **soft\_body\_get\_simulation\_precision**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_simulation_precision>`

Returns the simulation precision of the given soft body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **soft\_body\_get\_space**(body: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_space>`

Returns the `RID<class_RID>` of the space assigned to the given soft
body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **soft\_body\_get\_state**(body:
`RID<class_RID>`, state: `BodyState<enum_PhysicsServer3D_BodyState>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_state>`

Returns the given soft body state (see
`BodyState<enum_PhysicsServer3D_BodyState>` constants).

\*\*Note:\*\* Godot's default physics implementation does not support
`BODY_STATE_LINEAR_VELOCITY<class_PhysicsServer3D_constant_BODY_STATE_LINEAR_VELOCITY>`,
`BODY_STATE_ANGULAR_VELOCITY<class_PhysicsServer3D_constant_BODY_STATE_ANGULAR_VELOCITY>`,
`BODY_STATE_SLEEPING<class_PhysicsServer3D_constant_BODY_STATE_SLEEPING>`,
or
`BODY_STATE_CAN_SLEEP<class_PhysicsServer3D_constant_BODY_STATE_CAN_SLEEP>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **soft\_body\_get\_total\_mass**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_get_total_mass>`

Returns the total mass assigned to the given soft body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **soft\_body\_is\_point\_pinned**(body:
`RID<class_RID>`, point\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_soft_body_is_point_pinned>`

Returns whether the given soft body point is pinned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_move\_point**(body:
`RID<class_RID>`, point\_index: `int<class_int>`, global\_position:
`Vector3<class_Vector3>`)
`🔗<class_PhysicsServer3D_method_soft_body_move_point>`

Moves the given soft body point to a position in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_pin\_point**(body:
`RID<class_RID>`, point\_index: `int<class_int>`, pin:
`bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_soft_body_pin_point>`

Pins or unpins the given soft body point based on the value of `pin`.

\*\*Note:\*\* Pinning a point effectively makes it kinematic, preventing
it from being affected by forces, but you can still move it using
`soft_body_move_point<class_PhysicsServer3D_method_soft_body_move_point>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**soft\_body\_remove\_all\_pinned\_points**(body: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_soft_body_remove_all_pinned_points>`

Unpins all points of the given soft body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**soft\_body\_remove\_collision\_exception**(body: `RID<class_RID>`,
body\_b: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_soft_body_remove_collision_exception>`

Removes the given body from the list of bodies exempt from collisions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_set\_collision\_layer**(body:
`RID<class_RID>`, layer: `int<class_int>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_collision_layer>`

Sets the physics layer or layers the given soft body belongs to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_set\_collision\_mask**(body:
`RID<class_RID>`, mask: `int<class_int>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_collision_mask>`

Sets the physics layer or layers the given soft body can collide with.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**soft\_body\_set\_damping\_coefficient**(body: `RID<class_RID>`,
damping\_coefficient: `float<class_float>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_damping_coefficient>`

Sets the damping coefficient of the given soft body. Higher values will
slow down the body more noticeably when forces are applied.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_set\_drag\_coefficient**(body:
`RID<class_RID>`, drag\_coefficient: `float<class_float>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_drag_coefficient>`

Sets the drag coefficient of the given soft body. Higher values increase
this body's air resistance.

\*\*Note:\*\* This value is currently unused by Godot's default physics
implementation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_set\_linear\_stiffness**(body:
`RID<class_RID>`, stiffness: `float<class_float>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_linear_stiffness>`

Sets the linear stiffness of the given soft body. Higher values will
result in a stiffer body, while lower values will increase the body's
ability to bend. The value can be between `0.0` and `1.0` (inclusive).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_set\_mesh**(body:
`RID<class_RID>`, mesh: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_mesh>`

Sets the mesh of the given soft body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**soft\_body\_set\_pressure\_coefficient**(body: `RID<class_RID>`,
pressure\_coefficient: `float<class_float>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_pressure_coefficient>`

Sets the pressure coefficient of the given soft body. Simulates pressure
build-up from inside this body. Higher values increase the strength of
this effect.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_set\_ray\_pickable**(body:
`RID<class_RID>`, enable: `bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_ray_pickable>`

Sets whether the given soft body will be pickable when using object
picking.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**soft\_body\_set\_simulation\_precision**(body: `RID<class_RID>`,
simulation\_precision: `int<class_int>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_simulation_precision>`

Sets the simulation precision of the given soft body. Increasing this
value will improve the resulting simulation, but can affect performance.
Use with care.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_set\_space**(body:
`RID<class_RID>`, space: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_space>`

Assigns a space to the given soft body (see
`space_create<class_PhysicsServer3D_method_space_create>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_set\_state**(body:
`RID<class_RID>`, state: `BodyState<enum_PhysicsServer3D_BodyState>`,
variant: `Variant<class_Variant>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_state>`

Sets the given body state for the given body (see
`BodyState<enum_PhysicsServer3D_BodyState>` constants).

\*\*Note:\*\* Godot's default physics implementation does not support
`BODY_STATE_LINEAR_VELOCITY<class_PhysicsServer3D_constant_BODY_STATE_LINEAR_VELOCITY>`,
`BODY_STATE_ANGULAR_VELOCITY<class_PhysicsServer3D_constant_BODY_STATE_ANGULAR_VELOCITY>`,
`BODY_STATE_SLEEPING<class_PhysicsServer3D_constant_BODY_STATE_SLEEPING>`,
or
`BODY_STATE_CAN_SLEEP<class_PhysicsServer3D_constant_BODY_STATE_CAN_SLEEP>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_set\_total\_mass**(body:
`RID<class_RID>`, total\_mass: `float<class_float>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_total_mass>`

Sets the total mass for the given soft body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **soft\_body\_set\_transform**(body:
`RID<class_RID>`, transform: `Transform3D<class_Transform3D>`)
`🔗<class_PhysicsServer3D_method_soft_body_set_transform>`

Sets the global transform of the given soft body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**soft\_body\_update\_rendering\_server**(body: `RID<class_RID>`,
rendering\_server\_handler:
`PhysicsServer3DRenderingServerHandler<class_PhysicsServer3DRenderingServerHandler>`)
`🔗<class_PhysicsServer3D_method_soft_body_update_rendering_server>`

Requests that the physics server updates the rendering server with the
latest positions of the given soft body's points through the
`rendering_server_handler` interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **space\_create**()
`🔗<class_PhysicsServer3D_method_space_create>`

Creates a space. A space is a collection of parameters for the physics
engine that can be assigned to an area or a body. It can be assigned to
an area with
`area_set_space<class_PhysicsServer3D_method_area_set_space>`, or to a
body with `body_set_space<class_PhysicsServer3D_method_body_set_space>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PhysicsDirectSpaceState3D<class_PhysicsDirectSpaceState3D>`
**space\_get\_direct\_state**(space: `RID<class_RID>`)
`🔗<class_PhysicsServer3D_method_space_get_direct_state>`

Returns the state of a space, a
`PhysicsDirectSpaceState3D<class_PhysicsDirectSpaceState3D>`. This
object can be used to make collision/intersection queries.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **space\_get\_param**(space: `RID<class_RID>`,
param: `SpaceParameter<enum_PhysicsServer3D_SpaceParameter>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_space_get_param>`

Returns the value of a space parameter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **space\_is\_active**(space: `RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer3D_method_space_is_active>`

Returns whether the space is active.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **space\_set\_active**(space:
`RID<class_RID>`, active: `bool<class_bool>`)
`🔗<class_PhysicsServer3D_method_space_set_active>`

Marks a space as active. It will not have an effect, unless it is
assigned to an area or body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **space\_set\_param**(space: `RID<class_RID>`,
param: `SpaceParameter<enum_PhysicsServer3D_SpaceParameter>`, value:
`float<class_float>`) `🔗<class_PhysicsServer3D_method_space_set_param>`

Sets the value for a space parameter. A list of available parameters is
on the `SpaceParameter<enum_PhysicsServer3D_SpaceParameter>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **sphere\_shape\_create**()
`🔗<class_PhysicsServer3D_method_sphere_shape_create>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **world\_boundary\_shape\_create**()
`🔗<class_PhysicsServer3D_method_world_boundary_shape_create>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
