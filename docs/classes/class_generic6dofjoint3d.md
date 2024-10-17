github\_url  
hide

# Generic6DOFJoint3D

**Inherits:** `Joint3D<class_Joint3D>` **&lt;** `Node3D<class_Node3D>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

A physics joint that allows for complex movement and rotation between
two 3D physics bodies.

classref-introduction-group

## Description

The **Generic6DOFJoint3D** (6 Degrees Of Freedom) joint allows for
implementing custom types of joints by locking the rotation and
translation of certain axes.

The first 3 DOF represent the linear motion of the physics bodies and
the last 3 DOF represent the angular motion of the physics bodies. Each
axis can be either locked, or limited.

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Param**: `🔗<enum_Generic6DOFJoint3D_Param>`

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>` **PARAM\_LINEAR\_LOWER\_LIMIT** =
`0`

The minimum difference between the pivot points' axes.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>` **PARAM\_LINEAR\_UPPER\_LIMIT** =
`1`

The maximum difference between the pivot points' axes.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_LINEAR\_LIMIT\_SOFTNESS** = `2`

A factor applied to the movement across the axes. The lower, the slower
the movement.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>` **PARAM\_LINEAR\_RESTITUTION** =
`3`

The amount of restitution on the axes' movement. The lower, the more
momentum gets lost.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>` **PARAM\_LINEAR\_DAMPING** = `4`

The amount of damping that happens at the linear motion across the axes.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_LINEAR\_MOTOR\_TARGET\_VELOCITY** = `5`

The velocity the linear motor will try to reach.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_LINEAR\_MOTOR\_FORCE\_LIMIT** = `6`

The maximum force the linear motor will apply while trying to reach the
velocity target.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_LINEAR\_SPRING\_STIFFNESS** = `7`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_LINEAR\_SPRING\_DAMPING** = `8`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_LINEAR\_SPRING\_EQUILIBRIUM\_POINT** = `9`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>` **PARAM\_ANGULAR\_LOWER\_LIMIT**
= `10`

The minimum rotation in negative direction to break loose and rotate
around the axes.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>` **PARAM\_ANGULAR\_UPPER\_LIMIT**
= `11`

The minimum rotation in positive direction to break loose and rotate
around the axes.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_ANGULAR\_LIMIT\_SOFTNESS** = `12`

The speed of all rotations across the axes.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>` **PARAM\_ANGULAR\_DAMPING** =
`13`

The amount of rotational damping across the axes. The lower, the more
damping occurs.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>` **PARAM\_ANGULAR\_RESTITUTION** =
`14`

The amount of rotational restitution across the axes. The lower, the
more restitution occurs.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>` **PARAM\_ANGULAR\_FORCE\_LIMIT**
= `15`

The maximum amount of force that can occur, when rotating around the
axes.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>` **PARAM\_ANGULAR\_ERP** = `16`

When rotating across the axes, this error tolerance factor defines how
much the correction gets slowed down. The lower, the slower.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_ANGULAR\_MOTOR\_TARGET\_VELOCITY** = `17`

Target speed for the motor at the axes.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_ANGULAR\_MOTOR\_FORCE\_LIMIT** = `18`

Maximum acceleration for the motor at the axes.

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_ANGULAR\_SPRING\_STIFFNESS** = `19`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_ANGULAR\_SPRING\_DAMPING** = `20`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>`
**PARAM\_ANGULAR\_SPRING\_EQUILIBRIUM\_POINT** = `21`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`Param<enum_Generic6DOFJoint3D_Param>` **PARAM\_MAX** = `22`

Represents the size of the `Param<enum_Generic6DOFJoint3D_Param>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Flag**: `🔗<enum_Generic6DOFJoint3D_Flag>`

classref-enumeration-constant

`Flag<enum_Generic6DOFJoint3D_Flag>` **FLAG\_ENABLE\_LINEAR\_LIMIT** =
`0`

If enabled, linear motion is possible within the given limits.

classref-enumeration-constant

`Flag<enum_Generic6DOFJoint3D_Flag>` **FLAG\_ENABLE\_ANGULAR\_LIMIT** =
`1`

If enabled, rotational motion is possible within the given limits.

classref-enumeration-constant

`Flag<enum_Generic6DOFJoint3D_Flag>` **FLAG\_ENABLE\_LINEAR\_SPRING** =
`3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`Flag<enum_Generic6DOFJoint3D_Flag>` **FLAG\_ENABLE\_ANGULAR\_SPRING** =
`2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`Flag<enum_Generic6DOFJoint3D_Flag>` **FLAG\_ENABLE\_MOTOR** = `4`

If enabled, there is a rotational motor across these axes.

classref-enumeration-constant

`Flag<enum_Generic6DOFJoint3D_Flag>` **FLAG\_ENABLE\_LINEAR\_MOTOR** =
`5`

If enabled, there is a linear motor across these axes.

classref-enumeration-constant

`Flag<enum_Generic6DOFJoint3D_Flag>` **FLAG\_MAX** = `6`

Represents the size of the `Flag<enum_Generic6DOFJoint3D_Flag>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **angular\_limit\_x/damping** = `1.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_x/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of rotational damping across the X axis.

The lower, the longer an impulse from one side takes to travel to the
other side.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **angular\_limit\_x/enabled** = `true`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_x/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, rotation across the X axis is limited.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_x/erp** = `0.5`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_x/erp>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

When rotating across the X axis, this error tolerance factor defines how
much the correction gets slowed down. The lower, the slower.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_x/force\_limit** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_x/force_limit>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The maximum amount of force that can occur, when rotating around the X
axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_x/lower\_angle** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_x/lower_angle>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The minimum rotation in negative direction to break loose and rotate
around the X axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_x/restitution** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_x/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of rotational restitution across the X axis. The lower, the
more restitution occurs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_x/softness** = `0.5`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_x/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The speed of all rotations across the X axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_x/upper\_angle** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_x/upper_angle>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The minimum rotation in positive direction to break loose and rotate
around the X axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_y/damping** = `1.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_y/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of rotational damping across the Y axis. The lower, the more
damping occurs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **angular\_limit\_y/enabled** = `true`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_y/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, rotation across the Y axis is limited.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_y/erp** = `0.5`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_y/erp>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

When rotating across the Y axis, this error tolerance factor defines how
much the correction gets slowed down. The lower, the slower.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_y/force\_limit** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_y/force_limit>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The maximum amount of force that can occur, when rotating around the Y
axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_y/lower\_angle** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_y/lower_angle>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The minimum rotation in negative direction to break loose and rotate
around the Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_y/restitution** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_y/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of rotational restitution across the Y axis. The lower, the
more restitution occurs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_y/softness** = `0.5`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_y/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The speed of all rotations across the Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_y/upper\_angle** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_y/upper_angle>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The minimum rotation in positive direction to break loose and rotate
around the Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_z/damping** = `1.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_z/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of rotational damping across the Z axis. The lower, the more
damping occurs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **angular\_limit\_z/enabled** = `true`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_z/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, rotation across the Z axis is limited.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_z/erp** = `0.5`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_z/erp>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

When rotating across the Z axis, this error tolerance factor defines how
much the correction gets slowed down. The lower, the slower.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_z/force\_limit** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_z/force_limit>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The maximum amount of force that can occur, when rotating around the Z
axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_z/lower\_angle** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_z/lower_angle>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The minimum rotation in negative direction to break loose and rotate
around the Z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_z/restitution** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_z/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of rotational restitution across the Z axis. The lower, the
more restitution occurs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_z/softness** = `0.5`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_z/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The speed of all rotations across the Z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_limit\_z/upper\_angle** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_limit_z/upper_angle>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The minimum rotation in positive direction to break loose and rotate
around the Z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **angular\_motor\_x/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_angular_motor_x/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, a rotating motor at the X axis is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_motor\_x/force\_limit** = `300.0`
`🔗<class_Generic6DOFJoint3D_property_angular_motor_x/force_limit>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum acceleration for the motor at the X axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_motor\_x/target\_velocity** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_motor_x/target_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Target speed for the motor at the X axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **angular\_motor\_y/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_angular_motor_y/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, a rotating motor at the Y axis is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_motor\_y/force\_limit** = `300.0`
`🔗<class_Generic6DOFJoint3D_property_angular_motor_y/force_limit>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum acceleration for the motor at the Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_motor\_y/target\_velocity** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_motor_y/target_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Target speed for the motor at the Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **angular\_motor\_z/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_angular_motor_z/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, a rotating motor at the Z axis is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_motor\_z/force\_limit** = `300.0`
`🔗<class_Generic6DOFJoint3D_property_angular_motor_z/force_limit>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum acceleration for the motor at the Z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_motor\_z/target\_velocity** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_motor_z/target_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Target speed for the motor at the Z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_spring\_x/damping** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_x/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **angular\_spring\_x/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_x/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_spring\_x/equilibrium\_point** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_x/equilibrium_point>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_spring\_x/stiffness** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_x/stiffness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_spring\_y/damping** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_y/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **angular\_spring\_y/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_y/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_spring\_y/equilibrium\_point** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_y/equilibrium_point>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_spring\_y/stiffness** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_y/stiffness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_spring\_z/damping** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_z/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **angular\_spring\_z/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_z/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_spring\_z/equilibrium\_point** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_z/equilibrium_point>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_spring\_z/stiffness** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_angular_spring_z/stiffness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_x/damping** = `1.0`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_x/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of damping that happens at the X motion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **linear\_limit\_x/enabled** = `true`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_x/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the linear motion across the X axis is limited.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_x/lower\_distance** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_x/lower_distance>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The minimum difference between the pivot points' X axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_x/restitution** = `0.5`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_x/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of restitution on the X axis movement. The lower, the more
momentum gets lost.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_x/softness** = `0.7`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_x/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

A factor applied to the movement across the X axis. The lower, the
slower the movement.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_x/upper\_distance** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_x/upper_distance>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The maximum difference between the pivot points' X axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_y/damping** = `1.0`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_y/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of damping that happens at the Y motion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **linear\_limit\_y/enabled** = `true`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_y/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the linear motion across the Y axis is limited.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_y/lower\_distance** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_y/lower_distance>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The minimum difference between the pivot points' Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_y/restitution** = `0.5`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_y/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of restitution on the Y axis movement. The lower, the more
momentum gets lost.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_y/softness** = `0.7`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_y/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

A factor applied to the movement across the Y axis. The lower, the
slower the movement.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_y/upper\_distance** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_y/upper_distance>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The maximum difference between the pivot points' Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_z/damping** = `1.0`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_z/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of damping that happens at the Z motion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **linear\_limit\_z/enabled** = `true`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_z/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the linear motion across the Z axis is limited.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_z/lower\_distance** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_z/lower_distance>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The minimum difference between the pivot points' Z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_z/restitution** = `0.5`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_z/restitution>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The amount of restitution on the Z axis movement. The lower, the more
momentum gets lost.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_z/softness** = `0.7`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_z/softness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

A factor applied to the movement across the Z axis. The lower, the
slower the movement.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_limit\_z/upper\_distance** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_limit_z/upper_distance>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The maximum difference between the pivot points' Z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **linear\_motor\_x/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_linear_motor_x/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, then there is a linear motor on the X axis. It will attempt
to reach the target velocity while staying within the force limits.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_motor\_x/force\_limit** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_motor_x/force_limit>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The maximum force the linear motor can apply on the X axis while trying
to reach the target velocity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_motor\_x/target\_velocity** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_motor_x/target_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The speed that the linear motor will attempt to reach on the X axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **linear\_motor\_y/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_linear_motor_y/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, then there is a linear motor on the Y axis. It will attempt
to reach the target velocity while staying within the force limits.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_motor\_y/force\_limit** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_motor_y/force_limit>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The maximum force the linear motor can apply on the Y axis while trying
to reach the target velocity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_motor\_y/target\_velocity** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_motor_y/target_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The speed that the linear motor will attempt to reach on the Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **linear\_motor\_z/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_linear_motor_z/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, then there is a linear motor on the Z axis. It will attempt
to reach the target velocity while staying within the force limits.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_motor\_z/force\_limit** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_motor_z/force_limit>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The maximum force the linear motor can apply on the Z axis while trying
to reach the target velocity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_motor\_z/target\_velocity** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_motor_z/target_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The speed that the linear motor will attempt to reach on the Z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_spring\_x/damping** = `0.01`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_x/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **linear\_spring\_x/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_x/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_x**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_spring\_x/equilibrium\_point** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_x/equilibrium_point>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_spring\_x/stiffness** = `0.01`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_x/stiffness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_x**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_spring\_y/damping** = `0.01`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_y/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **linear\_spring\_y/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_y/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_y**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_spring\_y/equilibrium\_point** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_y/equilibrium_point>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_spring\_y/stiffness** = `0.01`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_y/stiffness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_y**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_spring\_z/damping** = `0.01`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_z/damping>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **linear\_spring\_z/enabled** = `false`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_z/enabled>`

classref-property-setget

-   `void (No return value.)` **set\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_flag\_z**(flag:
    `Flag<enum_Generic6DOFJoint3D_Flag>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_spring\_z/equilibrium\_point** = `0.0`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_z/equilibrium_point>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_spring\_z/stiffness** = `0.01`
`🔗<class_Generic6DOFJoint3D_property_linear_spring_z/stiffness>`

classref-property-setget

-   `void (No return value.)` **set\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
-   `float<class_float>` **get\_param\_z**(param:
    `Param<enum_Generic6DOFJoint3D_Param>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **get\_flag\_x**(flag:
`Flag<enum_Generic6DOFJoint3D_Flag>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Generic6DOFJoint3D_method_get_flag_x>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_flag\_y**(flag:
`Flag<enum_Generic6DOFJoint3D_Flag>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Generic6DOFJoint3D_method_get_flag_y>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_flag\_z**(flag:
`Flag<enum_Generic6DOFJoint3D_Flag>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Generic6DOFJoint3D_method_get_flag_z>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_param\_x**(param:
`Param<enum_Generic6DOFJoint3D_Param>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Generic6DOFJoint3D_method_get_param_x>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_param\_y**(param:
`Param<enum_Generic6DOFJoint3D_Param>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Generic6DOFJoint3D_method_get_param_y>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_param\_z**(param:
`Param<enum_Generic6DOFJoint3D_Param>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Generic6DOFJoint3D_method_get_param_z>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_flag\_x**(flag:
`Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
`🔗<class_Generic6DOFJoint3D_method_set_flag_x>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_flag\_y**(flag:
`Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
`🔗<class_Generic6DOFJoint3D_method_set_flag_y>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_flag\_z**(flag:
`Flag<enum_Generic6DOFJoint3D_Flag>`, value: `bool<class_bool>`)
`🔗<class_Generic6DOFJoint3D_method_set_flag_z>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_param\_x**(param:
`Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
`🔗<class_Generic6DOFJoint3D_method_set_param_x>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_param\_y**(param:
`Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
`🔗<class_Generic6DOFJoint3D_method_set_param_y>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_param\_z**(param:
`Param<enum_Generic6DOFJoint3D_Param>`, value: `float<class_float>`)
`🔗<class_Generic6DOFJoint3D_method_set_param_z>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
