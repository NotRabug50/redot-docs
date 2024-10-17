github\_url  
hide

# Curve3D

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Describes a Bézier curve in 3D space.

classref-introduction-group

## Description

This class describes a Bézier curve in 3D space. It is mainly used to
give a shape to a `Path3D<class_Path3D>`, but can be manually sampled
for other purposes.

It keeps a cache of precalculated points along the curve, to speed up
further calculations.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **bake\_interval** = `0.2`
`🔗<class_Curve3D_property_bake_interval>`

classref-property-setget

-   `void (No return value.)` **set\_bake\_interval**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_bake\_interval**()

The distance in meters between two adjacent cached points. Changing it
forces the cache to be recomputed the next time the
`get_baked_points<class_Curve3D_method_get_baked_points>` or
`get_baked_length<class_Curve3D_method_get_baked_length>` function is
called. The smaller the distance, the more points in the cache and the
more memory it will consume, so use with care.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **point\_count** = `0`
`🔗<class_Curve3D_property_point_count>`

classref-property-setget

-   `void (No return value.)` **set\_point\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_point\_count**()

The number of points describing the curve.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **up\_vector\_enabled** = `true`
`🔗<class_Curve3D_property_up_vector_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_up\_vector\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_up\_vector\_enabled**()

If `true`, the curve will bake up vectors used for orientation. This is
used when
`PathFollow3D.rotation_mode<class_PathFollow3D_property_rotation_mode>`
is set to
`PathFollow3D.ROTATION_ORIENTED<class_PathFollow3D_constant_ROTATION_ORIENTED>`.
Changing it forces the cache to be recomputed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_point**(position:
`Vector3<class_Vector3>`, in: `Vector3<class_Vector3>` = Vector3(0, 0,
0), out: `Vector3<class_Vector3>` = Vector3(0, 0, 0), index:
`int<class_int>` = -1) `🔗<class_Curve3D_method_add_point>`

Adds a point with the specified `position` relative to the curve's own
position, with control points `in` and `out`. Appends the new point at
the end of the point list.

If `index` is given, the new point is inserted before the existing point
identified by index `index`. Every existing point starting from `index`
is shifted further down the list of points. The index must be greater
than or equal to `0` and must not exceed the number of existing points
in the line. See `point_count<class_Curve3D_property_point_count>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_points**()
`🔗<class_Curve3D_method_clear_points>`

Removes all points from the curve.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_baked\_length**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_get_baked_length>`

Returns the total length of the curve, based on the cached points. Given
enough density (see
`bake_interval<class_Curve3D_property_bake_interval>`), it should be
approximate enough.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>` **get\_baked\_points**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_get_baked_points>`

Returns the cache of points as a
`PackedVector3Array<class_PackedVector3Array>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedFloat32Array<class_PackedFloat32Array>` **get\_baked\_tilts**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_get_baked_tilts>`

Returns the cache of tilts as a
`PackedFloat32Array<class_PackedFloat32Array>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>`
**get\_baked\_up\_vectors**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_get_baked_up_vectors>`

Returns the cache of up vectors as a
`PackedVector3Array<class_PackedVector3Array>`.

If `up_vector_enabled<class_Curve3D_property_up_vector_enabled>` is
`false`, the cache will be empty.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_closest\_offset**(to\_point:
`Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_get_closest_offset>`

Returns the closest offset to `to_point`. This offset is meant to be
used in `sample_baked<class_Curve3D_method_sample_baked>` or
`sample_baked_up_vector<class_Curve3D_method_sample_baked_up_vector>`.

`to_point` must be in this curve's local space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_closest\_point**(to\_point:
`Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_get_closest_point>`

Returns the closest point on baked segments (in curve's local space) to
`to_point`.

`to_point` must be in this curve's local space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_point\_in**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_get_point_in>`

Returns the position of the control point leading to the vertex `idx`.
The returned position is relative to the vertex `idx`. If the index is
out of bounds, the function sends an error to the console, and returns
`(0, 0, 0)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_point\_out**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_get_point_out>`

Returns the position of the control point leading out of the vertex
`idx`. The returned position is relative to the vertex `idx`. If the
index is out of bounds, the function sends an error to the console, and
returns `(0, 0, 0)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_point\_position**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_get_point_position>`

Returns the position of the vertex `idx`. If the index is out of bounds,
the function sends an error to the console, and returns `(0, 0, 0)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_point\_tilt**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_get_point_tilt>`

Returns the tilt angle in radians for the point `idx`. If the index is
out of bounds, the function sends an error to the console, and returns
`0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_point**(idx: `int<class_int>`)
`🔗<class_Curve3D_method_remove_point>`

Deletes the point `idx` from the curve. Sends an error to the console if
`idx` is out of bounds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **sample**(idx: `int<class_int>`, t:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_sample>`

Returns the position between the vertex `idx` and the vertex `idx + 1`,
where `t` controls if the point is the first vertex (`t = 0.0`), the
last vertex (`t = 1.0`), or in between. Values of `t` outside the range
(`0.0 >= t <=1`) give strange, but predictable results.

If `idx` is out of bounds it is truncated to the first or last vertex,
and `t` is ignored. If the curve has no points, the function sends an
error to the console, and returns `(0, 0, 0)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **sample\_baked**(offset: `float<class_float>`
= 0.0, cubic: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_sample_baked>`

Returns a point within the curve at position `offset`, where `offset` is
measured as a distance in 3D units along the curve. To do that, it finds
the two cached points where the `offset` lies between, then interpolates
the values. This interpolation is cubic if `cubic` is set to `true`, or
linear if set to `false`.

Cubic interpolation tends to follow the curves better, but linear is
faster (and often, precise enough).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **sample\_baked\_up\_vector**(offset:
`float<class_float>`, apply\_tilt: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_sample_baked_up_vector>`

Returns an up vector within the curve at position `offset`, where
`offset` is measured as a distance in 3D units along the curve. To do
that, it finds the two cached up vectors where the `offset` lies
between, then interpolates the values. If `apply_tilt` is `true`, an
interpolated tilt is applied to the interpolated up vector.

If the curve has no up vectors, the function sends an error to the
console, and returns `(0, 1, 0)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>`
**sample\_baked\_with\_rotation**(offset: `float<class_float>` = 0.0,
cubic: `bool<class_bool>` = false, apply\_tilt: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_sample_baked_with_rotation>`

Returns a `Transform3D<class_Transform3D>` with `origin` as point
position, `basis.x` as sideway vector, `basis.y` as up vector, `basis.z`
as forward vector. When the curve length is 0, there is no reasonable
way to calculate the rotation, all vectors aligned with global space
axes. See also `sample_baked<class_Curve3D_method_sample_baked>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **samplef**(fofs: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_samplef>`

Returns the position at the vertex `fofs`. It calls
`sample<class_Curve3D_method_sample>` using the integer part of `fofs`
as `idx`, and its fractional part as `t`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_in**(idx: `int<class_int>`,
position: `Vector3<class_Vector3>`)
`🔗<class_Curve3D_method_set_point_in>`

Sets the position of the control point leading to the vertex `idx`. If
the index is out of bounds, the function sends an error to the console.
The position is relative to the vertex.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_out**(idx: `int<class_int>`,
position: `Vector3<class_Vector3>`)
`🔗<class_Curve3D_method_set_point_out>`

Sets the position of the control point leading out of the vertex `idx`.
If the index is out of bounds, the function sends an error to the
console. The position is relative to the vertex.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_position**(idx:
`int<class_int>`, position: `Vector3<class_Vector3>`)
`🔗<class_Curve3D_method_set_point_position>`

Sets the position for the vertex `idx`. If the index is out of bounds,
the function sends an error to the console.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_tilt**(idx: `int<class_int>`,
tilt: `float<class_float>`) `🔗<class_Curve3D_method_set_point_tilt>`

Sets the tilt angle in radians for the point `idx`. If the index is out
of bounds, the function sends an error to the console.

The tilt controls the rotation along the look-at axis an object
traveling the path would have. In the case of a curve controlling a
`PathFollow3D<class_PathFollow3D>`, this tilt is an offset over the
natural tilt the `PathFollow3D<class_PathFollow3D>` calculates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>`
**tessellate**(max\_stages: `int<class_int>` = 5, tolerance\_degrees:
`float<class_float>` = 4)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_tessellate>`

Returns a list of points along the curve, with a curvature controlled
point density. That is, the curvier parts will have more points than the
straighter parts.

This approximation makes straight segments between each point, then
subdivides those segments until the resulting shape is similar enough.

`max_stages` controls how many subdivisions a curve segment may face
before it is considered approximate enough. Each subdivision splits the
segment in half, so the default 5 stages may mean up to 32 subdivisions
per curve segment. Increase with care!

`tolerance_degrees` controls how many degrees the midpoint of a segment
may deviate from the real curve, before the segment has to be
subdivided.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>`
**tessellate\_even\_length**(max\_stages: `int<class_int>` = 5,
tolerance\_length: `float<class_float>` = 0.2)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Curve3D_method_tessellate_even_length>`

Returns a list of points along the curve, with almost uniform density.
`max_stages` controls how many subdivisions a curve segment may face
before it is considered approximate enough. Each subdivision splits the
segment in half, so the default 5 stages may mean up to 32 subdivisions
per curve segment. Increase with care!

`tolerance_length` controls the maximal distance between two neighboring
points, before the segment has to be subdivided.
