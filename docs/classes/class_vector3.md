github\_url  
hide

# Vector3

A 3D vector using floating-point coordinates.

classref-introduction-group

## Description

A 3-element structure that can be used to represent 3D coordinates or
any other triplet of numeric values.

It uses floating-point coordinates. By default, these floating-point
values use 32-bit precision, unlike `float<class_float>` which is always
64-bit. If double precision is needed, compile the engine with the
option `precision=double`.

See `Vector3i<class_Vector3i>` for its integer counterpart.

\*\*Note:\*\* In a boolean context, a Vector3 will evaluate to `false`
if it's equal to `Vector3(0, 0, 0)`. Otherwise, a Vector3 will always
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
-   [All 3D
    Demos](https://github.com/godotengine/godot-demo-projects/tree/master/3d)

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

**AXIS\_X** = `0` `🔗<class_Vector3_constant_AXIS_X>`

Enumerated value for the X axis. Returned by
`max_axis_index<class_Vector3_method_max_axis_index>` and
`min_axis_index<class_Vector3_method_min_axis_index>`.

classref-constant

**AXIS\_Y** = `1` `🔗<class_Vector3_constant_AXIS_Y>`

Enumerated value for the Y axis. Returned by
`max_axis_index<class_Vector3_method_max_axis_index>` and
`min_axis_index<class_Vector3_method_min_axis_index>`.

classref-constant

**AXIS\_Z** = `2` `🔗<class_Vector3_constant_AXIS_Z>`

Enumerated value for the Z axis. Returned by
`max_axis_index<class_Vector3_method_max_axis_index>` and
`min_axis_index<class_Vector3_method_min_axis_index>`.

classref-constant

**ZERO** = `Vector3(0, 0, 0)` `🔗<class_Vector3_constant_ZERO>`

Zero vector, a vector with all components set to `0`.

classref-constant

**ONE** = `Vector3(1, 1, 1)` `🔗<class_Vector3_constant_ONE>`

One vector, a vector with all components set to `1`.

classref-constant

**INF** = `Vector3(inf, inf, inf)` `🔗<class_Vector3_constant_INF>`

Infinity vector, a vector with all components set to
`@GDScript.INF<class_@GDScript_constant_INF>`.

classref-constant

**LEFT** = `Vector3(-1, 0, 0)` `🔗<class_Vector3_constant_LEFT>`

Left unit vector. Represents the local direction of left, and the global
direction of west.

classref-constant

**RIGHT** = `Vector3(1, 0, 0)` `🔗<class_Vector3_constant_RIGHT>`

Right unit vector. Represents the local direction of right, and the
global direction of east.

classref-constant

**UP** = `Vector3(0, 1, 0)` `🔗<class_Vector3_constant_UP>`

Up unit vector.

classref-constant

**DOWN** = `Vector3(0, -1, 0)` `🔗<class_Vector3_constant_DOWN>`

Down unit vector.

classref-constant

**FORWARD** = `Vector3(0, 0, -1)` `🔗<class_Vector3_constant_FORWARD>`

Forward unit vector. Represents the local direction of forward, and the
global direction of north. Keep in mind that the forward direction for
lights, cameras, etc is different from 3D assets like characters, which
face towards the camera by convention. Use
`MODEL_FRONT<class_Vector3_constant_MODEL_FRONT>` and similar constants
when working in 3D asset space.

classref-constant

**BACK** = `Vector3(0, 0, 1)` `🔗<class_Vector3_constant_BACK>`

Back unit vector. Represents the local direction of back, and the global
direction of south.

classref-constant

**MODEL\_LEFT** = `Vector3(1, 0, 0)`
`🔗<class_Vector3_constant_MODEL_LEFT>`

Unit vector pointing towards the left side of imported 3D assets.

classref-constant

**MODEL\_RIGHT** = `Vector3(-1, 0, 0)`
`🔗<class_Vector3_constant_MODEL_RIGHT>`

Unit vector pointing towards the right side of imported 3D assets.

classref-constant

**MODEL\_TOP** = `Vector3(0, 1, 0)`
`🔗<class_Vector3_constant_MODEL_TOP>`

Unit vector pointing towards the top side (up) of imported 3D assets.

classref-constant

**MODEL\_BOTTOM** = `Vector3(0, -1, 0)`
`🔗<class_Vector3_constant_MODEL_BOTTOM>`

Unit vector pointing towards the bottom side (down) of imported 3D
assets.

classref-constant

**MODEL\_FRONT** = `Vector3(0, 0, 1)`
`🔗<class_Vector3_constant_MODEL_FRONT>`

Unit vector pointing towards the front side (facing forward) of imported
3D assets.

classref-constant

**MODEL\_REAR** = `Vector3(0, 0, -1)`
`🔗<class_Vector3_constant_MODEL_REAR>`

Unit vector pointing towards the rear side (back) of imported 3D assets.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **x** = `0.0` `🔗<class_Vector3_property_x>`

The vector's X component. Also accessible by using the index position
`[0]`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **y** = `0.0` `🔗<class_Vector3_property_y>`

The vector's Y component. Also accessible by using the index position
`[1]`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **z** = `0.0` `🔗<class_Vector3_property_z>`

The vector's Z component. Also accessible by using the index position
`[2]`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constructor Descriptions

classref-constructor

`Vector3<class_Vector3>` **Vector3**()
`🔗<class_Vector3_constructor_Vector3>`

Constructs a default-initialized **Vector3** with all components set to
`0`.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Vector3<class_Vector3>` **Vector3**(from: `Vector3<class_Vector3>`)

Constructs a **Vector3** as a copy of the given **Vector3**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Vector3<class_Vector3>` **Vector3**(from: `Vector3i<class_Vector3i>`)

Constructs a new **Vector3** from `Vector3i<class_Vector3i>`.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Vector3<class_Vector3>` **Vector3**(x: `float<class_float>`, y:
`float<class_float>`, z: `float<class_float>`)

Returns a **Vector3** with the given components.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Vector3<class_Vector3>` **abs**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_abs>`

Returns a new vector with all components in absolute values (i.e.
positive).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **angle\_to**(to: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_angle_to>`

Returns the unsigned minimum angle to the given vector, in radians.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **bezier\_derivative**(control\_1:
`Vector3<class_Vector3>`, control\_2: `Vector3<class_Vector3>`, end:
`Vector3<class_Vector3>`, t: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_bezier_derivative>`

Returns the derivative at the given `t` on the [Bézier
curve](https://en.wikipedia.org/wiki/B%C3%A9zier_curve) defined by this
vector and the given `control_1`, `control_2`, and `end` points.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **bezier\_interpolate**(control\_1:
`Vector3<class_Vector3>`, control\_2: `Vector3<class_Vector3>`, end:
`Vector3<class_Vector3>`, t: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_bezier_interpolate>`

Returns the point at the given `t` on the [Bézier
curve](https://en.wikipedia.org/wiki/B%C3%A9zier_curve) defined by this
vector and the given `control_1`, `control_2`, and `end` points.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **bounce**(n: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_bounce>`

Returns the vector "bounced off" from a plane defined by the given
normal `n`.

\*\*Note:\*\* `bounce<class_Vector3_method_bounce>` performs the
operation that most engines and frameworks call `reflect()`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **ceil**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_ceil>`

Returns a new vector with all components rounded up (towards positive
infinity).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **clamp**(min: `Vector3<class_Vector3>`, max:
`Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_clamp>`

Returns a new vector with all components clamped between the components
of `min` and `max`, by running
`@GlobalScope.clamp<class_@GlobalScope_method_clamp>` on each component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **clampf**(min: `float<class_float>`, max:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_clampf>`

Returns a new vector with all components clamped between `min` and
`max`, by running `@GlobalScope.clamp<class_@GlobalScope_method_clamp>`
on each component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **cross**(with: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_cross>`

Returns the cross product of this vector and `with`.

This returns a vector perpendicular to both this and `with`, which would
be the normal vector of the plane defined by the two vectors. As there
are two such vectors, in opposite directions, this method returns the
vector defined by a right-handed coordinate system. If the two vectors
are parallel this returns an empty vector, making it useful for testing
if two vectors are parallel.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **cubic\_interpolate**(b:
`Vector3<class_Vector3>`, pre\_a: `Vector3<class_Vector3>`, post\_b:
`Vector3<class_Vector3>`, weight: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_cubic_interpolate>`

Performs a cubic interpolation between this vector and `b` using `pre_a`
and `post_b` as handles, and returns the result at position `weight`.
`weight` is on the range of 0.0 to 1.0, representing the amount of
interpolation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **cubic\_interpolate\_in\_time**(b:
`Vector3<class_Vector3>`, pre\_a: `Vector3<class_Vector3>`, post\_b:
`Vector3<class_Vector3>`, weight: `float<class_float>`, b\_t:
`float<class_float>`, pre\_a\_t: `float<class_float>`, post\_b\_t:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_cubic_interpolate_in_time>`

Performs a cubic interpolation between this vector and `b` using `pre_a`
and `post_b` as handles, and returns the result at position `weight`.
`weight` is on the range of 0.0 to 1.0, representing the amount of
interpolation.

It can perform smoother interpolation than
`cubic_interpolate<class_Vector3_method_cubic_interpolate>` by the time
values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **direction\_to**(to: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_direction_to>`

Returns the normalized vector pointing from this vector to `to`. This is
equivalent to using `(b - a).normalized()`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **distance\_squared\_to**(to:
`Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_distance_squared_to>`

Returns the squared distance between this vector and `to`.

This method runs faster than
`distance_to<class_Vector3_method_distance_to>`, so prefer it if you
need to compare vectors or need the squared distance for some formula.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **distance\_to**(to: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_distance_to>`

Returns the distance between this vector and `to`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **dot**(with: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_dot>`

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

`Vector3<class_Vector3>` **floor**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_floor>`

Returns a new vector with all components rounded down (towards negative
infinity).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **inverse**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_inverse>`

Returns the inverse of the vector. This is the same as
`Vector3(1.0 / v.x, 1.0 / v.y, 1.0 / v.z)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_equal\_approx**(to: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_is_equal_approx>`

Returns `true` if this vector and `to` are approximately equal, by
running
`@GlobalScope.is_equal_approx<class_@GlobalScope_method_is_equal_approx>`
on each component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_finite**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_is_finite>`

Returns `true` if this vector is finite, by calling
`@GlobalScope.is_finite<class_@GlobalScope_method_is_finite>` on each
component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_normalized**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_is_normalized>`

Returns `true` if the vector is normalized, i.e. its length is
approximately equal to 1.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_zero\_approx**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_is_zero_approx>`

Returns `true` if this vector's values are approximately zero, by
running
`@GlobalScope.is_zero_approx<class_@GlobalScope_method_is_zero_approx>`
on each component.

This method is faster than using
`is_equal_approx<class_Vector3_method_is_equal_approx>` with one value
as a zero vector.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **length**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_length>`

Returns the length (magnitude) of this vector.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **length\_squared**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_length_squared>`

Returns the squared length (squared magnitude) of this vector.

This method runs faster than `length<class_Vector3_method_length>`, so
prefer it if you need to compare vectors or need the squared distance
for some formula.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **lerp**(to: `Vector3<class_Vector3>`, weight:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_lerp>`

Returns the result of the linear interpolation between this vector and
`to` by amount `weight`. `weight` is on the range of `0.0` to `1.0`,
representing the amount of interpolation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **limit\_length**(length: `float<class_float>`
= 1.0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_limit_length>`

Returns the vector with a maximum length by limiting its length to
`length`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **max**(with: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_max>`

Returns the component-wise maximum of this and `with`, equivalent to
`Vector3(maxf(x, with.x), maxf(y, with.y), maxf(z, with.z))`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **max\_axis\_index**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_max_axis_index>`

Returns the axis of the vector's highest value. See `AXIS_*` constants.
If all components are equal, this method returns
`AXIS_X<class_Vector3_constant_AXIS_X>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **maxf**(with: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_maxf>`

Returns the component-wise maximum of this and `with`, equivalent to
`Vector3(maxf(x, with), maxf(y, with), maxf(z, with))`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **min**(with: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_min>`

Returns the component-wise minimum of this and `with`, equivalent to
`Vector3(minf(x, with.x), minf(y, with.y), minf(z, with.z))`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **min\_axis\_index**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_min_axis_index>`

Returns the axis of the vector's lowest value. See `AXIS_*` constants.
If all components are equal, this method returns
`AXIS_Z<class_Vector3_constant_AXIS_Z>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **minf**(with: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_minf>`

Returns the component-wise minimum of this and `with`, equivalent to
`Vector3(minf(x, with), minf(y, with), minf(z, with))`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **move\_toward**(to: `Vector3<class_Vector3>`,
delta: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_move_toward>`

Returns a new vector moved toward `to` by the fixed `delta` amount. Will
not go past the final value.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **normalized**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_normalized>`

Returns the result of scaling the vector to unit length. Equivalent to
`v / v.length()`. Returns `(0, 0, 0)` if `v.length() == 0`. See also
`is_normalized<class_Vector3_method_is_normalized>`.

\*\*Note:\*\* This function may return incorrect values if the input
vector length is near zero.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **octahedron\_decode**(uv:
`Vector2<class_Vector2>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_Vector3_method_octahedron_decode>`

Returns the **Vector3** from an octahedral-compressed form created using
`octahedron_encode<class_Vector3_method_octahedron_encode>` (stored as a
`Vector2<class_Vector2>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **octahedron\_encode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_octahedron_encode>`

Returns the octahedral-encoded (oct32) form of this **Vector3** as a
`Vector2<class_Vector2>`. Since a `Vector2<class_Vector2>` occupies 1/3
less memory compared to **Vector3**, this form of compression can be
used to pass greater amounts of
`normalized<class_Vector3_method_normalized>` **Vector3**s without
increasing storage or memory requirements. See also
`octahedron_decode<class_Vector3_method_octahedron_decode>`.

\*\*Note:\*\*
`octahedron_encode<class_Vector3_method_octahedron_encode>` can only be
used for `normalized<class_Vector3_method_normalized>` vectors.
`octahedron_encode<class_Vector3_method_octahedron_encode>` does *not*
check whether this **Vector3** is normalized, and will return a value
that does not decompress to the original value if the **Vector3** is not
normalized.

\*\*Note:\*\* Octahedral compression is *lossy*, although visual
differences are rarely perceptible in real world scenarios.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Basis<class_Basis>` **outer**(with: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_outer>`

Returns the outer product with `with`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **posmod**(mod: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_posmod>`

Returns a vector composed of the
`@GlobalScope.fposmod<class_@GlobalScope_method_fposmod>` of this
vector's components and `mod`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **posmodv**(modv: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_posmodv>`

Returns a vector composed of the
`@GlobalScope.fposmod<class_@GlobalScope_method_fposmod>` of this
vector's components and `modv`'s components.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **project**(b: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_project>`

Returns a new vector resulting from projecting this vector onto the
given vector `b`. The resulting new vector is parallel to `b`. See also
`slide<class_Vector3_method_slide>`.

\*\*Note:\*\* If the vector `b` is a zero vector, the components of the
resulting new vector will be
`@GDScript.NAN<class_@GDScript_constant_NAN>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **reflect**(n: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_reflect>`

Returns the result of reflecting the vector through a plane defined by
the given normal vector `n`.

\*\*Note:\*\* `reflect<class_Vector3_method_reflect>` differs from what
other engines and frameworks call `reflect()`. In other engines,
`reflect()` returns the result of the vector reflected by the given
plane. The reflection thus passes through the given normal. While in
Godot the reflection passes through the plane and can be thought of as
bouncing off the normal. See also `bounce<class_Vector3_method_bounce>`
which does what most engines call `reflect()`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **rotated**(axis: `Vector3<class_Vector3>`,
angle: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_rotated>`

Returns the result of rotating this vector around a given axis by
`angle` (in radians). The axis must be a normalized vector. See also
`@GlobalScope.deg_to_rad<class_@GlobalScope_method_deg_to_rad>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **round**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_round>`

Returns a new vector with all components rounded to the nearest integer,
with halfway cases rounded away from zero.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **sign**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_sign>`

Returns a new vector with each component set to `1.0` if it's positive,
`-1.0` if it's negative, and `0.0` if it's zero. The result is identical
to calling `@GlobalScope.sign<class_@GlobalScope_method_sign>` on each
component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **signed\_angle\_to**(to: `Vector3<class_Vector3>`,
axis: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_signed_angle_to>`

Returns the signed angle to the given vector, in radians. The sign of
the angle is positive in a counter-clockwise direction and negative in a
clockwise direction when viewed from the side specified by the `axis`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **slerp**(to: `Vector3<class_Vector3>`, weight:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_slerp>`

Returns the result of spherical linear interpolation between this vector
and `to`, by amount `weight`. `weight` is on the range of 0.0 to 1.0,
representing the amount of interpolation.

This method also handles interpolating the lengths if the input vectors
have different lengths. For the special case of one or both input
vectors having zero length, this method behaves like
`lerp<class_Vector3_method_lerp>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **slide**(n: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_slide>`

Returns a new vector resulting from sliding this vector along a plane
with normal `n`. The resulting new vector is perpendicular to `n`, and
is equivalent to this vector minus its projection on `n`. See also
`project<class_Vector3_method_project>`.

\*\*Note:\*\* The vector `n` must be normalized. See also
`normalized<class_Vector3_method_normalized>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **snapped**(step: `Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_snapped>`

Returns a new vector with each component snapped to the nearest multiple
of the corresponding component in `step`. This can also be used to round
the components to an arbitrary number of decimals.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **snappedf**(step: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Vector3_method_snappedf>`

Returns a new vector with each component snapped to the nearest multiple
of `step`. This can also be used to round the components to an arbitrary
number of decimals.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Operator Descriptions

classref-operator

`bool<class_bool>` **operator !=**(right: `Vector3<class_Vector3>`)
`🔗<class_Vector3_operator_neq_Vector3>`

Returns `true` if the vectors are not equal.

\*\*Note:\*\* Due to floating-point precision errors, consider using
`is_equal_approx<class_Vector3_method_is_equal_approx>` instead, which
is more reliable.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator**\*(right: `Basis<class_Basis>`)
`🔗<class_Vector3_operator_mul_Basis>`

Inversely transforms (multiplies) the **Vector3** by the given
`Basis<class_Basis>` matrix, under the assumption that the basis is
orthonormal (i.e. rotation/reflection is fine, scaling/skew is not).

`vector * basis` is equivalent to `basis.transposed() * vector`. See
`Basis.transposed<class_Basis_method_transposed>`.

For transforming by inverse of a non-orthonormal basis (e.g. with
scaling) `basis.inverse() * vector` can be used instead. See
`Basis.inverse<class_Basis_method_inverse>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator**\*(right:
`Quaternion<class_Quaternion>`)
`🔗<class_Vector3_operator_mul_Quaternion>`

Inversely transforms (multiplies) the **Vector3** by the given
`Quaternion<class_Quaternion>`.

`vector * quaternion` is equivalent to `quaternion.inverse() * vector`.
See `Quaternion.inverse<class_Quaternion_method_inverse>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator**\*(right:
`Transform3D<class_Transform3D>`)
`🔗<class_Vector3_operator_mul_Transform3D>`

Inversely transforms (multiplies) the **Vector3** by the given
`Transform3D<class_Transform3D>` transformation matrix, under the
assumption that the transformation basis is orthonormal (i.e.
rotation/reflection is fine, scaling/skew is not).

`vector * transform` is equivalent to `transform.inverse() * vector`.
See `Transform3D.inverse<class_Transform3D_method_inverse>`.

For transforming by inverse of an affine transformation (e.g. with
scaling) `transform.affine_inverse() * vector` can be used instead. See
`Transform3D.affine_inverse<class_Transform3D_method_affine_inverse>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator**\*(right: `Vector3<class_Vector3>`)
`🔗<class_Vector3_operator_mul_Vector3>`

Multiplies each component of the **Vector3** by the components of the
given **Vector3**.

    print(Vector3(10, 20, 30) * Vector3(3, 4, 5)) # Prints "(30, 80, 150)"

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator**\*(right: `float<class_float>`)
`🔗<class_Vector3_operator_mul_float>`

Multiplies each component of the **Vector3** by the given
`float<class_float>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator**\*(right: `int<class_int>`)
`🔗<class_Vector3_operator_mul_int>`

Multiplies each component of the **Vector3** by the given
`int<class_int>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator +**(right: `Vector3<class_Vector3>`)
`🔗<class_Vector3_operator_sum_Vector3>`

Adds each component of the **Vector3** by the components of the given
**Vector3**.

    print(Vector3(10, 20, 30) + Vector3(3, 4, 5)) # Prints "(13, 24, 35)"

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator -**(right: `Vector3<class_Vector3>`)
`🔗<class_Vector3_operator_dif_Vector3>`

Subtracts each component of the **Vector3** by the components of the
given **Vector3**.

    print(Vector3(10, 20, 30) - Vector3(3, 4, 5)) # Prints "(7, 16, 25)"

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator /**(right: `Vector3<class_Vector3>`)
`🔗<class_Vector3_operator_div_Vector3>`

Divides each component of the **Vector3** by the components of the given
**Vector3**.

    print(Vector3(10, 20, 30) / Vector3(2, 5, 3)) # Prints "(5, 4, 10)"

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator /**(right: `float<class_float>`)
`🔗<class_Vector3_operator_div_float>`

Divides each component of the **Vector3** by the given
`float<class_float>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator /**(right: `int<class_int>`)
`🔗<class_Vector3_operator_div_int>`

Divides each component of the **Vector3** by the given `int<class_int>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &lt;**(right: `Vector3<class_Vector3>`)
`🔗<class_Vector3_operator_lt_Vector3>`

Compares two **Vector3** vectors by first checking if the X value of the
left vector is less than the X value of the `right` vector. If the X
values are exactly equal, then it repeats this check with the Y values
of the two vectors, and then with the Z values. This operator is useful
for sorting vectors.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &lt;=**(right: `Vector3<class_Vector3>`)
`🔗<class_Vector3_operator_lte_Vector3>`

Compares two **Vector3** vectors by first checking if the X value of the
left vector is less than or equal to the X value of the `right` vector.
If the X values are exactly equal, then it repeats this check with the Y
values of the two vectors, and then with the Z values. This operator is
useful for sorting vectors.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right: `Vector3<class_Vector3>`)
`🔗<class_Vector3_operator_eq_Vector3>`

Returns `true` if the vectors are exactly equal.

\*\*Note:\*\* Due to floating-point precision errors, consider using
`is_equal_approx<class_Vector3_method_is_equal_approx>` instead, which
is more reliable.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &gt;**(right: `Vector3<class_Vector3>`)
`🔗<class_Vector3_operator_gt_Vector3>`

Compares two **Vector3** vectors by first checking if the X value of the
left vector is greater than the X value of the `right` vector. If the X
values are exactly equal, then it repeats this check with the Y values
of the two vectors, and then with the Z values. This operator is useful
for sorting vectors.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &gt;=**(right: `Vector3<class_Vector3>`)
`🔗<class_Vector3_operator_gte_Vector3>`

Compares two **Vector3** vectors by first checking if the X value of the
left vector is greater than or equal to the X value of the `right`
vector. If the X values are exactly equal, then it repeats this check
with the Y values of the two vectors, and then with the Z values. This
operator is useful for sorting vectors.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this operator may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`float<class_float>` **operator \[\]**(index: `int<class_int>`)
`🔗<class_Vector3_operator_idx_int>`

Access vector components using their `index`. `v[0]` is equivalent to
`v.x`, `v[1]` is equivalent to `v.y`, and `v[2]` is equivalent to `v.z`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator unary+**()
`🔗<class_Vector3_operator_unplus>`

Returns the same value as if the `+` was not there. Unary `+` does
nothing, but sometimes it can make your code more readable.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator unary-**()
`🔗<class_Vector3_operator_unminus>`

Returns the negative value of the **Vector3**. This is the same as
writing `Vector3(-v.x, -v.y, -v.z)`. This operation flips the direction
of the vector while keeping the same magnitude. With floats, the number
zero can be either positive or negative.
