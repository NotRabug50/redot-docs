github\_url  
hide

# Curve

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A mathematical curve.

classref-introduction-group

## Description

This resource describes a mathematical curve by defining a set of points
and tangents at each point. By default, it ranges between `0` and `1` on
the Y axis and positions points relative to the `0.5` Y position.

See also `Gradient<class_Gradient>` which is designed for color
interpolation. See also `Curve2D<class_Curve2D>` and
`Curve3D<class_Curve3D>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**range\_changed**() `🔗<class_Curve_signal_range_changed>`

Emitted when `max_value<class_Curve_property_max_value>` or
`min_value<class_Curve_property_min_value>` is changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **TangentMode**: `🔗<enum_Curve_TangentMode>`

classref-enumeration-constant

`TangentMode<enum_Curve_TangentMode>` **TANGENT\_FREE** = `0`

The tangent on this side of the point is user-defined.

classref-enumeration-constant

`TangentMode<enum_Curve_TangentMode>` **TANGENT\_LINEAR** = `1`

The curve calculates the tangent on this side of the point as the slope
halfway towards the adjacent point.

classref-enumeration-constant

`TangentMode<enum_Curve_TangentMode>` **TANGENT\_MODE\_COUNT** = `2`

The total number of available tangent modes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **bake\_resolution** = `100`
`🔗<class_Curve_property_bake_resolution>`

classref-property-setget

-   `void (No return value.)` **set\_bake\_resolution**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_bake\_resolution**()

The number of points to include in the baked (i.e. cached) curve data.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **max\_value** = `1.0`
`🔗<class_Curve_property_max_value>`

classref-property-setget

-   `void (No return value.)` **set\_max\_value**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_max\_value**()

The maximum value the curve can reach.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **min\_value** = `0.0`
`🔗<class_Curve_property_min_value>`

classref-property-setget

-   `void (No return value.)` **set\_min\_value**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_min\_value**()

The minimum value the curve can reach.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **point\_count** = `0`
`🔗<class_Curve_property_point_count>`

classref-property-setget

-   `void (No return value.)` **set\_point\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_point\_count**()

The number of points describing the curve.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **add\_point**(position: `Vector2<class_Vector2>`,
left\_tangent: `float<class_float>` = 0, right\_tangent:
`float<class_float>` = 0, left\_mode:
`TangentMode<enum_Curve_TangentMode>` = 0, right\_mode:
`TangentMode<enum_Curve_TangentMode>` = 0)
`🔗<class_Curve_method_add_point>`

Adds a point to the curve. For each side, if the `*_mode` is
`TANGENT_LINEAR<class_Curve_constant_TANGENT_LINEAR>`, the `*_tangent`
angle (in degrees) uses the slope of the curve halfway to the adjacent
point. Allows custom assignments to the `*_tangent` angle if `*_mode` is
set to `TANGENT_FREE<class_Curve_constant_TANGENT_FREE>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **bake**() `🔗<class_Curve_method_bake>`

Recomputes the baked cache of points for the curve.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clean\_dupes**()
`🔗<class_Curve_method_clean_dupes>`

Removes duplicate points, i.e. points that are less than 0.00001 units
(engine epsilon value) away from their neighbor on the curve.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_points**()
`🔗<class_Curve_method_clear_points>`

Removes all points from the curve.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TangentMode<enum_Curve_TangentMode>` **get\_point\_left\_mode**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve_method_get_point_left_mode>`

Returns the left `TangentMode<enum_Curve_TangentMode>` for the point at
`index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_point\_left\_tangent**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve_method_get_point_left_tangent>`

Returns the left tangent angle (in degrees) for the point at `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_point\_position**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve_method_get_point_position>`

Returns the curve coordinates for the point at `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TangentMode<enum_Curve_TangentMode>` **get\_point\_right\_mode**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve_method_get_point_right_mode>`

Returns the right `TangentMode<enum_Curve_TangentMode>` for the point at
`index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_point\_right\_tangent**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve_method_get_point_right_tangent>`

Returns the right tangent angle (in degrees) for the point at `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_point**(index: `int<class_int>`)
`🔗<class_Curve_method_remove_point>`

Removes the point at `index` from the curve.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **sample**(offset: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve_method_sample>`

Returns the Y value for the point that would exist at the X position
`offset` along the curve.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **sample\_baked**(offset: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve_method_sample_baked>`

Returns the Y value for the point that would exist at the X position
`offset` along the curve using the baked cache. Bakes the curve's points
if not already baked.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_left\_mode**(index:
`int<class_int>`, mode: `TangentMode<enum_Curve_TangentMode>`)
`🔗<class_Curve_method_set_point_left_mode>`

Sets the left `TangentMode<enum_Curve_TangentMode>` for the point at
`index` to `mode`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_left\_tangent**(index:
`int<class_int>`, tangent: `float<class_float>`)
`🔗<class_Curve_method_set_point_left_tangent>`

Sets the left tangent angle for the point at `index` to `tangent`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **set\_point\_offset**(index: `int<class_int>`, offset:
`float<class_float>`) `🔗<class_Curve_method_set_point_offset>`

Sets the offset from `0.5`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_right\_mode**(index:
`int<class_int>`, mode: `TangentMode<enum_Curve_TangentMode>`)
`🔗<class_Curve_method_set_point_right_mode>`

Sets the right `TangentMode<enum_Curve_TangentMode>` for the point at
`index` to `mode`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_right\_tangent**(index:
`int<class_int>`, tangent: `float<class_float>`)
`🔗<class_Curve_method_set_point_right_tangent>`

Sets the right tangent angle for the point at `index` to `tangent`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_value**(index: `int<class_int>`,
y: `float<class_float>`) `🔗<class_Curve_method_set_point_value>`

Assigns the vertical position `y` to the point at `index`.
