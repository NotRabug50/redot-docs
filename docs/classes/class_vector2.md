github\_url  
hide

# Vector2

A 2D vector using floating-point coordinates.

classref-introduction-group

## Description

A 2-element structure that can be used to represent 2D coordinates or
any other pair of numeric values.

It uses floating-point coordinates. By default, these floating-point
values use 32-bit precision, unlike `float<class_float>` which is always
64-bit. If double precision is needed, compile the engine with the
option `precision=double`.

See `Vector2i<class_Vector2i>` for its integer counterpart.

\*\*Note:\*\* In a boolean context, a Vector2 will evaluate to `false`
if it's equal to `Vector2(0, 0)`. Otherwise, a Vector2 will always
evaluate to `true`.

classref-introduction-group

## Tutorials

-   `Math documentation index <../tutorials/math/index>`
-   `Vector math <../tutorials/math/vector_math>`
-   `Advanced vector math <../tutorials/math/vectors_advanced>`
-   [3Blue1Brown Essence of Linear
    Algebra](https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab)
-   [Matrix Transform
    Demo](https://godotengine.org/asset-library/asset/2787)
-   [All 2D
    Demos](https://github.com/godotengine/godot-demo-projects/tree/master/2d)

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-reftable-group

## Constructors

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

## Operators

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

## Constants

classref-constant

**AXIS\_X** = `0` `🔗<class_Vector2_constant_AXIS_X>`

Enumerated value for the X axis. Returned by
`max_axis_index<class_Vector2_method_max_axis_index>` and
`min_axis_index<class_Vector2_method_min_axis_index>`.

classref-constant

**AXIS\_Y** = `1` `🔗<class_Vector2_constant_AXIS_Y>`

Enumerated value for the Y axis. Returned by
`max_axis_index<class_Vector2_method_max_axis_index>` and
`min_axis_index<class_Vector2_method_min_axis_index>`.

classref-constant

**ZERO** = `Vector2(0, 0)` `🔗<class_Vector2_constant_ZERO>`

Zero vector, a vector with all components set to `0`.

classref-constant

**ONE** = `Vector2(1, 1)` `🔗<class_Vector2_constant_ONE>`

One vector, a vector with all components set to `1`.

classref-constant

**INF** = `Vector2(inf, inf)` `🔗<class_Vector2_constant_INF>`

Infinity vector, a vector with all components set to
`@GDScript.INF<class_@GDScript_constant_INF>`.

classref-constant

**LEFT** = `Vector2(-1, 0)` `🔗<class_Vector2_constant_LEFT>`

Left unit vector. Represents the direction of left.

classref-constant

**RIGHT** = `Vector2(1, 0)` `🔗<class_Vector2_constant_RIGHT>`

Right unit vector. Represents the direction of right.

classref-constant

**UP** = `Vector2(0, -1)` `🔗<class_Vector2_constant_UP>`

Up unit vector. Y is down in 2D, so this vector points -Y.

classref-constant

**DOWN** = `Vector2(0, 1)` `🔗<class_Vector2_constant_DOWN>`

Down unit vector. Y is down in 2D, so this vector points +Y.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **x** = `0.0` `🔗<class_Vector2_property_x>`

The vector's X component. Also accessible by using the index position
`[0]`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **y** = `0.0` `🔗<class_Vector2_property_y>`

The vector's Y component. Also accessible by using the index position
`[1]`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constructor Descriptions

classref-constructor

`Vector2<class_Vector2>` **Vector2**()
`🔗<class_Vector2_constructor_Vector2>`

Constructs a default-initialized **Vector2** with all components set to
`0`.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Vector2<class_Vector2>` **Vector2**(from: `Vector2<class_Vector2>`)

Constructs a **Vector2** as a copy of the given **Vector2**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Vector2<class_Vector2>` **Vector2**(from: `Vector2i<class_Vector2i>`)

Constructs a new **Vector2** from `Vector2i<class_Vector2i>`.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Vector2<class_Vector2>` **Vector2**(x: `float<class_float>`, y:
`float<class_float>`)

Constructs a new **Vector2** from the given `x` and `y`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Vector2<class_Vector2>` **abs**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_abs>`

Returns a new vector with all components in absolute values (i.e.
positive).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **angle**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_angle>`

Returns this vector's angle with respect to the positive X axis, or
`(1, 0)` vector, in radians.

For example, `Vector2.RIGHT.angle()` will return zero,
`Vector2.DOWN.angle()` will return `PI / 2` (a quarter turn, or 90
degrees), and `Vector2(1, -1).angle()` will return `-PI / 4` (a negative
eighth turn, or -45 degrees).

[Illustration of the returned
angle.](https://raw.githubusercontent.com/godotengine/godot-docs/master/img/vector2_angle.png)

Equivalent to the result of
`@GlobalScope.atan2<class_@GlobalScope_method_atan2>` when called with
the vector's `y<class_Vector2_property_y>` and
`x<class_Vector2_property_x>` as parameters: `atan2(y, x)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **angle\_to**(to: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_angle_to>`

Returns the angle to the given vector, in radians.

[Illustration of the returned
angle.](https://raw.githubusercontent.com/godotengine/godot-docs/master/img/vector2_angle_to.png)

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **angle\_to\_point**(to: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_angle_to_point>`

Returns the angle between the line connecting the two points and the X
axis, in radians.

`a.angle_to_point(b)` is equivalent of doing `(b - a).angle()`.

[Illustration of the returned
angle.](https://raw.githubusercontent.com/godotengine/godot-docs/master/img/vector2_angle_to_point.png)

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **aspect**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_aspect>`

Returns the aspect ratio of this vector, the ratio of
`x<class_Vector2_property_x>` to `y<class_Vector2_property_y>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **bezier\_derivative**(control\_1:
`Vector2<class_Vector2>`, control\_2: `Vector2<class_Vector2>`, end:
`Vector2<class_Vector2>`, t: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_bezier_derivative>`

Returns the derivative at the given `t` on the [Bézier
curve](https://en.wikipedia.org/wiki/B%C3%A9zier_curve) defined by this
vector and the given `control_1`, `control_2`, and `end` points.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **bezier\_interpolate**(control\_1:
`Vector2<class_Vector2>`, control\_2: `Vector2<class_Vector2>`, end:
`Vector2<class_Vector2>`, t: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_bezier_interpolate>`

Returns the point at the given `t` on the [Bézier
curve](https://en.wikipedia.org/wiki/B%C3%A9zier_curve) defined by this
vector and the given `control_1`, `control_2`, and `end` points.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **bounce**(n: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_bounce>`

Returns the vector "bounced off" from a line defined by the given normal
`n` perpendicular to the line.

\*\*Note:\*\* `bounce<class_Vector2_method_bounce>` performs the
operation that most engines and frameworks call `reflect()`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **ceil**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_ceil>`

Returns a new vector with all components rounded up (towards positive
infinity).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **clamp**(min: `Vector2<class_Vector2>`, max:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_clamp>`

Returns a new vector with all components clamped between the components
of `min` and `max`, by running
`@GlobalScope.clamp<class_@GlobalScope_method_clamp>` on each component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **clampf**(min: `float<class_float>`, max:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_clampf>`

Returns a new vector with all components clamped between `min` and
`max`, by running `@GlobalScope.clamp<class_@GlobalScope_method_clamp>`
on each component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **cross**(with: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_cross>`

Returns the 2D analog of the cross product for this vector and `with`.

This is the signed area of the parallelogram formed by the two vectors.
If the second vector is clockwise from the first vector, then the cross
product is the positive area. If counter-clockwise, the cross product is
the negative area. If the two vectors are parallel this returns zero,
making it useful for testing if two vectors are parallel.

\*\*Note:\*\* Cross product is not defined in 2D mathematically. This
method embeds the 2D vectors in the XY plane of 3D space and uses their
cross product's Z component as the analog.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **cubic\_interpolate**(b:
`Vector2<class_Vector2>`, pre\_a: `Vector2<class_Vector2>`, post\_b:
`Vector2<class_Vector2>`, weight: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_cubic_interpolate>`

Performs a cubic interpolation between this vector and `b` using `pre_a`
and `post_b` as handles, and returns the result at position `weight`.
`weight` is on the range of 0.0 to 1.0, representing the amount of
interpolation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **cubic\_interpolate\_in\_time**(b:
`Vector2<class_Vector2>`, pre\_a: `Vector2<class_Vector2>`, post\_b:
`Vector2<class_Vector2>`, weight: `float<class_float>`, b\_t:
`float<class_float>`, pre\_a\_t: `float<class_float>`, post\_b\_t:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_cubic_interpolate_in_time>`

Performs a cubic interpolation between this vector and `b` using `pre_a`
and `post_b` as handles, and returns the result at position `weight`.
`weight` is on the range of 0.0 to 1.0, representing the amount of
interpolation.

It can perform smoother interpolation than
`cubic_interpolate<class_Vector2_method_cubic_interpolate>` by the time
values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **direction\_to**(to: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_direction_to>`

Returns the normalized vector pointing from this vector to `to`. This is
equivalent to using `(b - a).normalized()`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **distance\_squared\_to**(to:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_distance_squared_to>`

Returns the squared distance between this vector and `to`.

This method runs faster than
`distance_to<class_Vector2_method_distance_to>`, so prefer it if you
need to compare vectors or need the squared distance for some formula.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **distance\_to**(to: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_distance_to>`

Returns the distance between this vector and `to`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **dot**(with: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_dot>`

Returns the dot product of this vector and `with`. This can be used to
compare the angle between two vectors. For example, this can be used to
determine whether an enemy is facing the player.

The dot product will be `0` for a right angle (90 degrees), greater than
0 for angles narrower than 90 degrees and lower than 0 for angles wider
than 90 degrees.

When using unit (normalized) vectors, the result will always be between
`-1.0` (180 degree angle) when the vectors are facing opposite
directions, and `1.0` (0 degree angle) when the vectors are aligned.

\*\*Note:\*\* `a.dot(b)` is equivalent to `b.dot(a)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **floor**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_floor>`

Returns a new vector with all components rounded down (towards negative
infinity).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **from\_angle**(angle: `float<class_float>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_Vector2_method_from_angle>`

Creates a unit **Vector2** rotated to the given `angle` in radians. This
is equivalent to doing `Vector2(cos(angle), sin(angle))` or
`Vector2.RIGHT.rotated(angle)`.

    print(Vector2.from_angle(0)) # Prints (1, 0).
    print(Vector2(1, 0).angle()) # Prints 0, which is the angle used above.
    print(Vector2.from_angle(PI / 2)) # Prints (0, 1).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_equal\_approx**(to: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_is_equal_approx>`

Returns `true` if this vector and `to` are approximately equal, by
running
`@GlobalScope.is_equal_approx<class_@GlobalScope_method_is_equal_approx>`
on each component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_finite**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_is_finite>`

Returns `true` if this vector is finite, by calling
`@GlobalScope.is_finite<class_@GlobalScope_method_is_finite>` on each
component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_normalized**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_is_normalized>`

Returns `true` if the vector is normalized, i.e. its length is
approximately equal to 1.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_zero\_approx**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_is_zero_approx>`

Returns `true` if this vector's values are approximately zero, by
running
`@GlobalScope.is_zero_approx<class_@GlobalScope_method_is_zero_approx>`
on each component.

This method is faster than using
`is_equal_approx<class_Vector2_method_is_equal_approx>` with one value
as a zero vector.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **length**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_length>`

Returns the length (magnitude) of this vector.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **length\_squared**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_length_squared>`

Returns the squared length (squared magnitude) of this vector.

This method runs faster than `length<class_Vector2_method_length>`, so
prefer it if you need to compare vectors or need the squared distance
for some formula.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **lerp**(to: `Vector2<class_Vector2>`, weight:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_lerp>`

Returns the result of the linear interpolation between this vector and
`to` by amount `weight`. `weight` is on the range of `0.0` to `1.0`,
representing the amount of interpolation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **limit\_length**(length: `float<class_float>`
= 1.0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_limit_length>`

Returns the vector with a maximum length by limiting its length to
`length`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **max**(with: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_max>`

Returns the component-wise maximum of this and `with`, equivalent to
`Vector2(maxf(x, with.x), maxf(y, with.y))`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **max\_axis\_index**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_max_axis_index>`

Returns the axis of the vector's highest value. See `AXIS_*` constants.
If all components are equal, this method returns
`AXIS_X<class_Vector2_constant_AXIS_X>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **maxf**(with: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_maxf>`

Returns the component-wise maximum of this and `with`, equivalent to
`Vector2(maxf(x, with), maxf(y, with))`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **min**(with: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_min>`

Returns the component-wise minimum of this and `with`, equivalent to
`Vector2(minf(x, with.x), minf(y, with.y))`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **min\_axis\_index**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_min_axis_index>`

Returns the axis of the vector's lowest value. See `AXIS_*` constants.
If all components are equal, this method returns
`AXIS_Y<class_Vector2_constant_AXIS_Y>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **minf**(with: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_minf>`

Returns the component-wise minimum of this and `with`, equivalent to
`Vector2(minf(x, with), minf(y, with))`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **move\_toward**(to: `Vector2<class_Vector2>`,
delta: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_move_toward>`

Returns a new vector moved toward `to` by the fixed `delta` amount. Will
not go past the final value.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **normalized**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_normalized>`

Returns the result of scaling the vector to unit length. Equivalent to
`v / v.length()`. Returns `(0, 0)` if `v.length() == 0`. See also
`is_normalized<class_Vector2_method_is_normalized>`.

\*\*Note:\*\* This function may return incorrect values if the input
vector length is near zero.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **orthogonal**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_orthogonal>`

Returns a perpendicular vector rotated 90 degrees counter-clockwise
compared to the original, with the same length.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **posmod**(mod: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_posmod>`

Returns a vector composed of the
`@GlobalScope.fposmod<class_@GlobalScope_method_fposmod>` of this
vector's components and `mod`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **posmodv**(modv: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_posmodv>`

Returns a vector composed of the
`@GlobalScope.fposmod<class_@GlobalScope_method_fposmod>` of this
vector's components and `modv`'s components.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **project**(b: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_project>`

Returns a new vector resulting from projecting this vector onto the
given vector `b`. The resulting new vector is parallel to `b`. See also
`slide<class_Vector2_method_slide>`.

\*\*Note:\*\* If the vector `b` is a zero vector, the components of the
resulting new vector will be
`@GDScript.NAN<class_@GDScript_constant_NAN>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **reflect**(line: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_reflect>`

Returns the result of reflecting the vector from a line defined by the
given direction vector `line`.

\*\*Note:\*\* `reflect<class_Vector2_method_reflect>` differs from what
other engines and frameworks call `reflect()`. In other engines,
`reflect()` takes a normal direction which is a direction perpendicular
to the line. In Godot, you specify the direction of the line directly.
See also `bounce<class_Vector2_method_bounce>` which does what most
engines call `reflect()`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **rotated**(angle: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_rotated>`

Returns the result of rotating this vector by `angle` (in radians). See
also `@GlobalScope.deg_to_rad<class_@GlobalScope_method_deg_to_rad>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **round**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_round>`

Returns a new vector with all components rounded to the nearest integer,
with halfway cases rounded away from zero.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **sign**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_sign>`

Returns a new vector with each component set to `1.0` if it's positive,
`-1.0` if it's negative, and `0.0` if it's zero. The result is identical
to calling `@GlobalScope.sign<class_@GlobalScope_method_sign>` on each
component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **slerp**(to: `Vector2<class_Vector2>`, weight:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_slerp>`

Returns the result of spherical linear interpolation between this vector
and `to`, by amount `weight`. `weight` is on the range of 0.0 to 1.0,
representing the amount of interpolation.

This method also handles interpolating the lengths if the input vectors
have different lengths. For the special case of one or both input
vectors having zero length, this method behaves like
`lerp<class_Vector2_method_lerp>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **slide**(n: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_slide>`

Returns a new vector resulting from sliding this vector along a line
with normal `n`. The resulting new vector is perpendicular to `n`, and
is equivalent to this vector minus its projection on `n`. See also
`project<class_Vector2_method_project>`.

\*\*Note:\*\* The vector `n` must be normalized. See also
`normalized<class_Vector2_method_normalized>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **snapped**(step: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_snapped>`

Returns a new vector with each component snapped to the nearest multiple
of the corresponding component in `step`. This can also be used to round
the components to an arbitrary number of decimals.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **snappedf**(step: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector2_method_snappedf>`

Returns a new vector with each component snapped to the nearest multiple
of `step`. This can also be used to round the components to an arbitrary
number of decimals.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Operator Descriptions

classref-operator

`bool<class_bool>` **operator !=**(right: `Vector2<class_Vector2>`)
`🔗<class_Vector2_operator_neq_Vector2>`

Returns `true` if the vectors are not equal.

\*\*Note:\*\* Due to floating-point precision errors, consider using
`is_equal_approx<class_Vector2_method_is_equal_approx>` instead, which
is more reliable.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator**\*(right:
`Transform2D<class_Transform2D>`)
`🔗<class_Vector2_operator_mul_Transform2D>`

Inversely transforms (multiplies) the **Vector2** by the given
`Transform2D<class_Transform2D>` transformation matrix, under the
assumption that the transformation basis is orthonormal (i.e.
rotation/reflection is fine, scaling/skew is not).

`vector * transform` is equivalent to `transform.inverse() * vector`.
See `Transform2D.inverse<class_Transform2D_method_inverse>`.

For transforming by inverse of an affine transformation (e.g. with
scaling) `transform.affine_inverse() * vector` can be used instead. See
`Transform2D.affine_inverse<class_Transform2D_method_affine_inverse>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator**\*(right: `Vector2<class_Vector2>`)
`🔗<class_Vector2_operator_mul_Vector2>`

Multiplies each component of the **Vector2** by the components of the
given **Vector2**.

    print(Vector2(10, 20) * Vector2(3, 4)) # Prints "(30, 80)"

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator**\*(right: `float<class_float>`)
`🔗<class_Vector2_operator_mul_float>`

Multiplies each component of the **Vector2** by the given
`float<class_float>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator**\*(right: `int<class_int>`)
`🔗<class_Vector2_operator_mul_int>`

Multiplies each component of the **Vector2** by the given
`int<class_int>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator +**(right: `Vector2<class_Vector2>`)
`🔗<class_Vector2_operator_sum_Vector2>`

Adds each component of the **Vector2** by the components of the given
**Vector2**.

    print(Vector2(10, 20) + Vector2(3, 4)) # Prints "(13, 24)"

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator -**(right: `Vector2<class_Vector2>`)
`🔗<class_Vector2_operator_dif_Vector2>`

Subtracts each component of the **Vector2** by the components of the
given **Vector2**.

    print(Vector2(10, 20) - Vector2(3, 4)) # Prints "(7, 16)"

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator /**(right: `Vector2<class_Vector2>`)
`🔗<class_Vector2_operator_div_Vector2>`

Divides each component of the **Vector2** by the components of the given
**Vector2**.

    print(Vector2(10, 20) / Vector2(2, 5)) # Prints "(5, 4)"

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator /**(right: `float<class_float>`)
`🔗<class_Vector2_operator_div_float>`

Divides each component of the **Vector2** by the given
`float<class_float>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator /**(right: `int<class_int>`)
`🔗<class_Vector2_operator_div_int>`

Divides each component of the **Vector2** by the given `int<class_int>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &lt;**(right: `Vector2<class_Vector2>`)
`🔗<class_Vector2_operator_lt_Vector2>`

Compares two **Vector2** vectors by first checking if the X value of the
left vector is less than the X value of the `right` vector. If the X
values are exactly equal, then it repeats this check with the Y values
of the two vectors. This operator is useful for sorting vectors.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &lt;=**(right: `Vector2<class_Vector2>`)
`🔗<class_Vector2_operator_lte_Vector2>`

Compares two **Vector2** vectors by first checking if the X value of the
left vector is less than or equal to the X value of the `right` vector.
If the X values are exactly equal, then it repeats this check with the Y
values of the two vectors. This operator is useful for sorting vectors.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right: `Vector2<class_Vector2>`)
`🔗<class_Vector2_operator_eq_Vector2>`

Returns `true` if the vectors are exactly equal.

\*\*Note:\*\* Due to floating-point precision errors, consider using
`is_equal_approx<class_Vector2_method_is_equal_approx>` instead, which
is more reliable.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &gt;**(right: `Vector2<class_Vector2>`)
`🔗<class_Vector2_operator_gt_Vector2>`

Compares two **Vector2** vectors by first checking if the X value of the
left vector is greater than the X value of the `right` vector. If the X
values are exactly equal, then it repeats this check with the Y values
of the two vectors. This operator is useful for sorting vectors.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &gt;=**(right: `Vector2<class_Vector2>`)
`🔗<class_Vector2_operator_gte_Vector2>`

Compares two **Vector2** vectors by first checking if the X value of the
left vector is greater than or equal to the X value of the `right`
vector. If the X values are exactly equal, then it repeats this check
with the Y values of the two vectors. This operator is useful for
sorting vectors.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`float<class_float>` **operator \[\]**(index: `int<class_int>`)
`🔗<class_Vector2_operator_idx_int>`

Access vector components using their `index`. `v[0]` is equivalent to
`v.x`, and `v[1]` is equivalent to `v.y`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator unary+**()
`🔗<class_Vector2_operator_unplus>`

Returns the same value as if the `+` was not there. Unary `+` does
nothing, but sometimes it can make your code more readable.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator unary-**()
`🔗<class_Vector2_operator_unminus>`

Returns the negative value of the **Vector2**. This is the same as
writing `Vector2(-v.x, -v.y)`. This operation flips the direction of the
vector while keeping the same magnitude. With floats, the number zero
can be either positive or negative.
