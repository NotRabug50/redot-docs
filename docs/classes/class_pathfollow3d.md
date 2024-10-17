github\_url  
hide

# PathFollow3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

Point sampler for a `Path3D<class_Path3D>`.

classref-introduction-group

## Description

This node takes its parent `Path3D<class_Path3D>`, and returns the
coordinates of a point within it, given a distance from the first
vertex.

It is useful for making other nodes follow a path, without coding the
movement pattern. For that, the nodes must be children of this node. The
descendant nodes will then move accordingly when setting the
`progress<class_PathFollow3D_property_progress>` in this node.

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
</tbody>
</table>

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **RotationMode**: `🔗<enum_PathFollow3D_RotationMode>`

classref-enumeration-constant

`RotationMode<enum_PathFollow3D_RotationMode>` **ROTATION\_NONE** = `0`

Forbids the PathFollow3D to rotate.

classref-enumeration-constant

`RotationMode<enum_PathFollow3D_RotationMode>` **ROTATION\_Y** = `1`

Allows the PathFollow3D to rotate in the Y axis only.

classref-enumeration-constant

`RotationMode<enum_PathFollow3D_RotationMode>` **ROTATION\_XY** = `2`

Allows the PathFollow3D to rotate in both the X, and Y axes.

classref-enumeration-constant

`RotationMode<enum_PathFollow3D_RotationMode>` **ROTATION\_XYZ** = `3`

Allows the PathFollow3D to rotate in any axis.

classref-enumeration-constant

`RotationMode<enum_PathFollow3D_RotationMode>` **ROTATION\_ORIENTED** =
`4`

Uses the up vector information in a `Curve3D<class_Curve3D>` to enforce
orientation. This rotation mode requires the `Path3D<class_Path3D>`'s
`Curve3D.up_vector_enabled<class_Curve3D_property_up_vector_enabled>`
property to be set to `true`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **cubic\_interp** = `true`
`🔗<class_PathFollow3D_property_cubic_interp>`

classref-property-setget

-   `void (No return value.)` **set\_cubic\_interpolation**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_cubic\_interpolation**()

If `true`, the position between two cached points is interpolated
cubically, and linearly otherwise.

The points along the `Curve3D<class_Curve3D>` of the
`Path3D<class_Path3D>` are precomputed before use, for faster
calculations. The point at the requested offset is then calculated
interpolating between two adjacent cached points. This may present a
problem if the curve makes sharp turns, as the cached points may not
follow the curve closely enough.

There are two answers to this problem: either increase the number of
cached points and increase memory consumption, or make a cubic
interpolation between two points at the cost of (slightly) slower
calculations.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **h\_offset** = `0.0`
`🔗<class_PathFollow3D_property_h_offset>`

classref-property-setget

-   `void (No return value.)` **set\_h\_offset**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_h\_offset**()

The node's offset along the curve.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **loop** = `true`
`🔗<class_PathFollow3D_property_loop>`

classref-property-setget

-   `void (No return value.)` **set\_loop**(value: `bool<class_bool>`)
-   `bool<class_bool>` **has\_loop**()

If `true`, any offset outside the path's length will wrap around,
instead of stopping at the ends. Use it for cyclic paths.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **progress** = `0.0`
`🔗<class_PathFollow3D_property_progress>`

classref-property-setget

-   `void (No return value.)` **set\_progress**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_progress**()

The distance from the first vertex, measured in 3D units along the path.
Changing this value sets this node's position to a point within the
path.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **progress\_ratio** = `0.0`
`🔗<class_PathFollow3D_property_progress_ratio>`

classref-property-setget

-   `void (No return value.)` **set\_progress\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_progress\_ratio**()

The distance from the first vertex, considering 0.0 as the first vertex
and 1.0 as the last. This is just another way of expressing the progress
within the path, as the progress supplied is multiplied internally by
the path's length.

It can be set or get only if the **PathFollow3D** is the child of a
`Path3D<class_Path3D>` which is part of the scene tree, and that this
`Path3D<class_Path3D>` has a `Curve3D<class_Curve3D>` with a non-zero
length. Otherwise, trying to set this field will print an error, and
getting this field will return `0.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`RotationMode<enum_PathFollow3D_RotationMode>` **rotation\_mode** = `3`
`🔗<class_PathFollow3D_property_rotation_mode>`

classref-property-setget

-   `void (No return value.)` **set\_rotation\_mode**(value:
    `RotationMode<enum_PathFollow3D_RotationMode>`)
-   `RotationMode<enum_PathFollow3D_RotationMode>`
    **get\_rotation\_mode**()

Allows or forbids rotation on one or more axes, depending on the
`RotationMode<enum_PathFollow3D_RotationMode>` constants being used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **tilt\_enabled** = `true`
`🔗<class_PathFollow3D_property_tilt_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_tilt\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_tilt\_enabled**()

If `true`, the tilt property of `Curve3D<class_Curve3D>` takes effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_model\_front** = `false`
`🔗<class_PathFollow3D_property_use_model_front>`

classref-property-setget

-   `void (No return value.)` **set\_use\_model\_front**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_model\_front**()

If `true`, the node moves on the travel path with orienting the +Z axis
as forward. See also `Vector3.FORWARD<class_Vector3_constant_FORWARD>`
and `Vector3.MODEL_FRONT<class_Vector3_constant_MODEL_FRONT>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **v\_offset** = `0.0`
`🔗<class_PathFollow3D_property_v_offset>`

classref-property-setget

-   `void (No return value.)` **set\_v\_offset**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_v\_offset**()

The node's offset perpendicular to the curve.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Transform3D<class_Transform3D>` **correct\_posture**(transform:
`Transform3D<class_Transform3D>`, rotation\_mode:
`RotationMode<enum_PathFollow3D_RotationMode>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_PathFollow3D_method_correct_posture>`

Correct the `transform`. `rotation_mode` implicitly specifies how
posture (forward, up and sideway direction) is calculated.
