github\_url  
hide

# SliderJoint3D

**Inherits:** `Joint3D<class_Joint3D>` **&lt;** `Node3D<class_Node3D>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

A physics joint that restricts the movement of a 3D physics body along
an axis relative to another physics body.

classref-introduction-group

## Description

A physics joint that restricts the movement of a 3D physics body along
an axis relative to another physics body. For example, Body A could be a
`StaticBody3D<class_StaticBody3D>` representing a piston base, while
Body B could be a `RigidBody3D<class_RigidBody3D>` representing the
piston head, moving up and down.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Param**: `🔗<enum_SliderJoint3D_Param>`

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_LINEAR\_LIMIT\_UPPER** = `0`

Constant for accessing
`linear_limit/upper_distance<class_SliderJoint3D_property_linear_limit/upper_distance>`.
The maximum difference between the pivot points on their X axis before
damping happens.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_LINEAR\_LIMIT\_LOWER** = `1`

Constant for accessing
`linear_limit/lower_distance<class_SliderJoint3D_property_linear_limit/lower_distance>`.
The minimum difference between the pivot points on their X axis before
damping happens.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_LINEAR\_LIMIT\_SOFTNESS** =
`2`

Constant for accessing
`linear_limit/softness<class_SliderJoint3D_property_linear_limit/softness>`.
A factor applied to the movement across the slider axis once the limits
get surpassed. The lower, the slower the movement.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_LINEAR\_LIMIT\_RESTITUTION**
= `3`

Constant for accessing
`linear_limit/restitution<class_SliderJoint3D_property_linear_limit/restitution>`.
The amount of restitution once the limits are surpassed. The lower, the
more velocity-energy gets lost.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_LINEAR\_LIMIT\_DAMPING** =
`4`

Constant for accessing
`linear_limit/damping<class_SliderJoint3D_property_linear_limit/damping>`.
The amount of damping once the slider limits are surpassed.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_LINEAR\_MOTION\_SOFTNESS** =
`5`

Constant for accessing
`linear_motion/softness<class_SliderJoint3D_property_linear_motion/softness>`.
A factor applied to the movement across the slider axis as long as the
slider is in the limits. The lower, the slower the movement.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_LINEAR\_MOTION\_RESTITUTION**
= `6`

Constant for accessing
`linear_motion/restitution<class_SliderJoint3D_property_linear_motion/restitution>`.
The amount of restitution inside the slider limits.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_LINEAR\_MOTION\_DAMPING** =
`7`

Constant for accessing
`linear_motion/damping<class_SliderJoint3D_property_linear_motion/damping>`.
The amount of damping inside the slider limits.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>`
**PARAM\_LINEAR\_ORTHOGONAL\_SOFTNESS** = `8`

Constant for accessing
`linear_ortho/softness<class_SliderJoint3D_property_linear_ortho/softness>`.
A factor applied to the movement across axes orthogonal to the slider.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>`
**PARAM\_LINEAR\_ORTHOGONAL\_RESTITUTION** = `9`

Constant for accessing
`linear_motion/restitution<class_SliderJoint3D_property_linear_motion/restitution>`.
The amount of restitution when movement is across axes orthogonal to the
slider.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_LINEAR\_ORTHOGONAL\_DAMPING**
= `10`

Constant for accessing
`linear_motion/damping<class_SliderJoint3D_property_linear_motion/damping>`.
The amount of damping when movement is across axes orthogonal to the
slider.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_ANGULAR\_LIMIT\_UPPER** =
`11`

Constant for accessing
`angular_limit/upper_angle<class_SliderJoint3D_property_angular_limit/upper_angle>`.
The upper limit of rotation in the slider.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_ANGULAR\_LIMIT\_LOWER** =
`12`

Constant for accessing
`angular_limit/lower_angle<class_SliderJoint3D_property_angular_limit/lower_angle>`.
The lower limit of rotation in the slider.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_ANGULAR\_LIMIT\_SOFTNESS** =
`13`

Constant for accessing
`angular_limit/softness<class_SliderJoint3D_property_angular_limit/softness>`.
A factor applied to the all rotation once the limit is surpassed.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_ANGULAR\_LIMIT\_RESTITUTION**
= `14`

Constant for accessing
`angular_limit/restitution<class_SliderJoint3D_property_angular_limit/restitution>`.
The amount of restitution of the rotation when the limit is surpassed.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_ANGULAR\_LIMIT\_DAMPING** =
`15`

Constant for accessing
`angular_limit/damping<class_SliderJoint3D_property_angular_limit/damping>`.
The amount of damping of the rotation when the limit is surpassed.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_ANGULAR\_MOTION\_SOFTNESS** =
`16`

Constant for accessing
`angular_motion/softness<class_SliderJoint3D_property_angular_motion/softness>`.
A factor applied to the all rotation in the limits.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>`
**PARAM\_ANGULAR\_MOTION\_RESTITUTION** = `17`

Constant for accessing
`angular_motion/restitution<class_SliderJoint3D_property_angular_motion/restitution>`.
The amount of restitution of the rotation in the limits.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_ANGULAR\_MOTION\_DAMPING** =
`18`

Constant for accessing
`angular_motion/damping<class_SliderJoint3D_property_angular_motion/damping>`.
The amount of damping of the rotation in the limits.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>`
**PARAM\_ANGULAR\_ORTHOGONAL\_SOFTNESS** = `19`

Constant for accessing
`angular_ortho/softness<class_SliderJoint3D_property_angular_ortho/softness>`.
A factor applied to the all rotation across axes orthogonal to the
slider.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>`
**PARAM\_ANGULAR\_ORTHOGONAL\_RESTITUTION** = `20`

Constant for accessing
`angular_ortho/restitution<class_SliderJoint3D_property_angular_ortho/restitution>`.
The amount of restitution of the rotation across axes orthogonal to the
slider.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>`
**PARAM\_ANGULAR\_ORTHOGONAL\_DAMPING** = `21`

Constant for accessing
`angular_ortho/damping<class_SliderJoint3D_property_angular_ortho/damping>`.
The amount of damping of the rotation across axes orthogonal to the
slider.

classref-enumeration-constant

`Param<enum_SliderJoint3D_Param>` **PARAM\_MAX** = `22`

Represents the size of the `Param<enum_SliderJoint3D_Param>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **angular\_limit/damping** = `0.0`
`🔗<class_SliderJoint3D_property_angular_limit/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of damping of the rotation when the limit is surpassed.

A lower damping value allows a rotation initiated by body A to travel to
body B slower.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit/lower\_angle** = `0.0`
`🔗<class_SliderJoint3D_property_angular_limit/lower_angle>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The lower limit of rotation in the slider.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit/restitution** = `0.7`
`🔗<class_SliderJoint3D_property_angular_limit/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of restitution of the rotation when the limit is surpassed.

Does not affect damping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit/softness** = `1.0`
`🔗<class_SliderJoint3D_property_angular_limit/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

A factor applied to the all rotation once the limit is surpassed.

Makes all rotation slower when between 0 and 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit/upper\_angle** = `0.0`
`🔗<class_SliderJoint3D_property_angular_limit/upper_angle>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The upper limit of rotation in the slider.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_motion/damping** = `1.0`
`🔗<class_SliderJoint3D_property_angular_motion/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of damping of the rotation in the limits.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_motion/restitution** = `0.7`
`🔗<class_SliderJoint3D_property_angular_motion/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of restitution of the rotation in the limits.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_motion/softness** = `1.0`
`🔗<class_SliderJoint3D_property_angular_motion/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

A factor applied to the all rotation in the limits.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_ortho/damping** = `1.0`
`🔗<class_SliderJoint3D_property_angular_ortho/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of damping of the rotation across axes orthogonal to the
slider.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_ortho/restitution** = `0.7`
`🔗<class_SliderJoint3D_property_angular_ortho/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of restitution of the rotation across axes orthogonal to the
slider.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_ortho/softness** = `1.0`
`🔗<class_SliderJoint3D_property_angular_ortho/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

A factor applied to the all rotation across axes orthogonal to the
slider.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit/damping** = `1.0`
`🔗<class_SliderJoint3D_property_linear_limit/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of damping that happens once the limit defined by
`linear_limit/lower_distance<class_SliderJoint3D_property_linear_limit/lower_distance>`
and
`linear_limit/upper_distance<class_SliderJoint3D_property_linear_limit/upper_distance>`
is surpassed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit/lower\_distance** = `-1.0`
`🔗<class_SliderJoint3D_property_linear_limit/lower_distance>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The minimum difference between the pivot points on their X axis before
damping happens.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit/restitution** = `0.7`
`🔗<class_SliderJoint3D_property_linear_limit/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of restitution once the limits are surpassed. The lower, the
more velocity-energy gets lost.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit/softness** = `1.0`
`🔗<class_SliderJoint3D_property_linear_limit/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

A factor applied to the movement across the slider axis once the limits
get surpassed. The lower, the slower the movement.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit/upper\_distance** = `1.0`
`🔗<class_SliderJoint3D_property_linear_limit/upper_distance>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The maximum difference between the pivot points on their X axis before
damping happens.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_motion/damping** = `0.0`
`🔗<class_SliderJoint3D_property_linear_motion/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of damping inside the slider limits.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_motion/restitution** = `0.7`
`🔗<class_SliderJoint3D_property_linear_motion/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of restitution inside the slider limits.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_motion/softness** = `1.0`
`🔗<class_SliderJoint3D_property_linear_motion/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

A factor applied to the movement across the slider axis as long as the
slider is in the limits. The lower, the slower the movement.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_ortho/damping** = `1.0`
`🔗<class_SliderJoint3D_property_linear_ortho/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of damping when movement is across axes orthogonal to the
slider.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_ortho/restitution** = `0.7`
`🔗<class_SliderJoint3D_property_linear_ortho/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of restitution when movement is across axes orthogonal to the
slider.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_ortho/softness** = `1.0`
`🔗<class_SliderJoint3D_property_linear_ortho/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param**(param:
    `Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param**(param:
    `Param<enum_SliderJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

A factor applied to the movement across axes orthogonal to the slider.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_param**(param:
`Param<enum_SliderJoint3D_Param>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SliderJoint3D_method_get_param>`

Returns the value of the given parameter (see
`Param<enum_SliderJoint3D_Param>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_param**(param:
`Param<enum_SliderJoint3D_Param>`, value: `float<class_float>`)
`🔗<class_SliderJoint3D_method_set_param>`

Assigns `value` to the given parameter (see
`Param<enum_SliderJoint3D_Param>` constants).
