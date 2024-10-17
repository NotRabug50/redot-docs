github\_url  
hide

# Geometry2D

**Inherits:** `Object<class_Object>`

Provides methods for some common 2D geometric operations.

classref-introduction-group

## Description

Provides a set of helper functions to create geometric shapes, compute
intersections between shapes, and process various other geometric
operations in 2D.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **PolyBooleanOperation**:
`🔗<enum_Geometry2D_PolyBooleanOperation>`

classref-enumeration-constant

`PolyBooleanOperation<enum_Geometry2D_PolyBooleanOperation>`
**OPERATION\_UNION** = `0`

Create regions where either subject or clip polygons (or both) are
filled.

classref-enumeration-constant

`PolyBooleanOperation<enum_Geometry2D_PolyBooleanOperation>`
**OPERATION\_DIFFERENCE** = `1`

Create regions where subject polygons are filled except where clip
polygons are filled.

classref-enumeration-constant

`PolyBooleanOperation<enum_Geometry2D_PolyBooleanOperation>`
**OPERATION\_INTERSECTION** = `2`

Create regions where both subject and clip polygons are filled.

classref-enumeration-constant

`PolyBooleanOperation<enum_Geometry2D_PolyBooleanOperation>`
**OPERATION\_XOR** = `3`

Create regions where either subject or clip polygons are filled but not
where both are filled.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PolyJoinType**: `🔗<enum_Geometry2D_PolyJoinType>`

classref-enumeration-constant

`PolyJoinType<enum_Geometry2D_PolyJoinType>` **JOIN\_SQUARE** = `0`

Squaring is applied uniformally at all convex edge joins at `1 * delta`.

classref-enumeration-constant

`PolyJoinType<enum_Geometry2D_PolyJoinType>` **JOIN\_ROUND** = `1`

While flattened paths can never perfectly trace an arc, they are
approximated by a series of arc chords.

classref-enumeration-constant

`PolyJoinType<enum_Geometry2D_PolyJoinType>` **JOIN\_MITER** = `2`

There's a necessary limit to mitered joins since offsetting edges that
join at very acute angles will produce excessively long and narrow
"spikes". For any given edge join, when miter offsetting would exceed
that maximum distance, "square" joining is applied.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PolyEndType**: `🔗<enum_Geometry2D_PolyEndType>`

classref-enumeration-constant

`PolyEndType<enum_Geometry2D_PolyEndType>` **END\_POLYGON** = `0`

Endpoints are joined using the
`PolyJoinType<enum_Geometry2D_PolyJoinType>` value and the path filled
as a polygon.

classref-enumeration-constant

`PolyEndType<enum_Geometry2D_PolyEndType>` **END\_JOINED** = `1`

Endpoints are joined using the
`PolyJoinType<enum_Geometry2D_PolyJoinType>` value and the path filled
as a polyline.

classref-enumeration-constant

`PolyEndType<enum_Geometry2D_PolyEndType>` **END\_BUTT** = `2`

Endpoints are squared off with no extension.

classref-enumeration-constant

`PolyEndType<enum_Geometry2D_PolyEndType>` **END\_SQUARE** = `3`

Endpoints are squared off and extended by `delta` units.

classref-enumeration-constant

`PolyEndType<enum_Geometry2D_PolyEndType>` **END\_ROUND** = `4`

Endpoints are rounded off and extended by `delta` units.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\]
**clip\_polygons**(polygon\_a:
`PackedVector2Array<class_PackedVector2Array>`, polygon\_b:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_clip_polygons>`

Clips `polygon_a` against `polygon_b` and returns an array of clipped
polygons. This performs
`OPERATION_DIFFERENCE<class_Geometry2D_constant_OPERATION_DIFFERENCE>`
between polygons. Returns an empty array if `polygon_b` completely
overlaps `polygon_a`.

If `polygon_b` is enclosed by `polygon_a`, returns an outer polygon
(boundary) and inner polygon (hole) which could be distinguished by
calling
`is_polygon_clockwise<class_Geometry2D_method_is_polygon_clockwise>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\]
**clip\_polyline\_with\_polygon**(polyline:
`PackedVector2Array<class_PackedVector2Array>`, polygon:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_clip_polyline_with_polygon>`

Clips `polyline` against `polygon` and returns an array of clipped
polylines. This performs
`OPERATION_DIFFERENCE<class_Geometry2D_constant_OPERATION_DIFFERENCE>`
between the polyline and the polygon. This operation can be thought of
as cutting a line with a closed shape.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>` **convex\_hull**(points:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_convex_hull>`

Given an array of `Vector2<class_Vector2>`s, returns the convex hull as
a list of points in counterclockwise order. The last point is the same
as the first one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\]
**decompose\_polygon\_in\_convex**(polygon:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_decompose_polygon_in_convex>`

Decomposes the `polygon` into multiple convex hulls and returns an array
of `PackedVector2Array<class_PackedVector2Array>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\]
**exclude\_polygons**(polygon\_a:
`PackedVector2Array<class_PackedVector2Array>`, polygon\_b:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_exclude_polygons>`

Mutually excludes common area defined by intersection of `polygon_a` and
`polygon_b` (see
`intersect_polygons<class_Geometry2D_method_intersect_polygons>`) and
returns an array of excluded polygons. This performs
`OPERATION_XOR<class_Geometry2D_constant_OPERATION_XOR>` between
polygons. In other words, returns all but common area between polygons.

The operation may result in an outer polygon (boundary) and inner
polygon (hole) produced which could be distinguished by calling
`is_polygon_clockwise<class_Geometry2D_method_is_polygon_clockwise>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_closest\_point\_to\_segment**(point:
`Vector2<class_Vector2>`, s1: `Vector2<class_Vector2>`, s2:
`Vector2<class_Vector2>`)
`🔗<class_Geometry2D_method_get_closest_point_to_segment>`

Returns the 2D point on the 2D segment (`s1`, `s2`) that is closest to
`point`. The returned point will always be inside the specified segment.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**get\_closest\_point\_to\_segment\_uncapped**(point:
`Vector2<class_Vector2>`, s1: `Vector2<class_Vector2>`, s2:
`Vector2<class_Vector2>`)
`🔗<class_Geometry2D_method_get_closest_point_to_segment_uncapped>`

Returns the 2D point on the 2D line defined by (`s1`, `s2`) that is
closest to `point`. The returned point can be inside the segment (`s1`,
`s2`) or outside of it, i.e. somewhere on the line extending from the
segment.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**get\_closest\_points\_between\_segments**(p1:
`Vector2<class_Vector2>`, q1: `Vector2<class_Vector2>`, p2:
`Vector2<class_Vector2>`, q2: `Vector2<class_Vector2>`)
`🔗<class_Geometry2D_method_get_closest_points_between_segments>`

Given the two 2D segments (`p1`, `q1`) and (`p2`, `q2`), finds those two
points on the two segments that are closest to each other. Returns a
`PackedVector2Array<class_PackedVector2Array>` that contains this point
on (`p1`, `q1`) as well the accompanying point on (`p2`, `q2`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\]
**intersect\_polygons**(polygon\_a:
`PackedVector2Array<class_PackedVector2Array>`, polygon\_b:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_intersect_polygons>`

Intersects `polygon_a` with `polygon_b` and returns an array of
intersected polygons. This performs
`OPERATION_INTERSECTION<class_Geometry2D_constant_OPERATION_INTERSECTION>`
between polygons. In other words, returns common area shared by
polygons. Returns an empty array if no intersection occurs.

The operation may result in an outer polygon (boundary) and inner
polygon (hole) produced which could be distinguished by calling
`is_polygon_clockwise<class_Geometry2D_method_is_polygon_clockwise>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\]
**intersect\_polyline\_with\_polygon**(polyline:
`PackedVector2Array<class_PackedVector2Array>`, polygon:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_intersect_polyline_with_polygon>`

Intersects `polyline` with `polygon` and returns an array of intersected
polylines. This performs
`OPERATION_INTERSECTION<class_Geometry2D_constant_OPERATION_INTERSECTION>`
between the polyline and the polygon. This operation can be thought of
as chopping a line with a closed shape.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_point\_in\_circle**(point:
`Vector2<class_Vector2>`, circle\_position: `Vector2<class_Vector2>`,
circle\_radius: `float<class_float>`)
`🔗<class_Geometry2D_method_is_point_in_circle>`

Returns `true` if `point` is inside the circle or if it's located
exactly *on* the circle's boundary, otherwise returns `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_point\_in\_polygon**(point:
`Vector2<class_Vector2>`, polygon:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_is_point_in_polygon>`

Returns `true` if `point` is inside `polygon` or if it's located exactly
*on* polygon's boundary, otherwise returns `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_polygon\_clockwise**(polygon:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_is_polygon_clockwise>`

Returns `true` if `polygon`'s vertices are ordered in clockwise order,
otherwise returns `false`.

\*\*Note:\*\* Assumes a Cartesian coordinate system where `+x` is right
and `+y` is up. If using screen coordinates (`+y` is down), the result
will need to be flipped (i.e. a `true` result will indicate
counter-clockwise).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **line\_intersects\_line**(from\_a:
`Vector2<class_Vector2>`, dir\_a: `Vector2<class_Vector2>`, from\_b:
`Vector2<class_Vector2>`, dir\_b: `Vector2<class_Vector2>`)
`🔗<class_Geometry2D_method_line_intersects_line>`

Returns the point of intersection between the two lines (`from_a`,
`dir_a`) and (`from_b`, `dir_b`). Returns a `Vector2<class_Vector2>`, or
`null` if the lines are parallel.

`from` and `dir` are *not* endpoints of a line segment or ray but the
slope (`dir`) and a known point (`from`) on that line.

gdscript

var from\_a = Vector2.ZERO var dir\_a = Vector2.RIGHT var from\_b =
Vector2.DOWN

\# Returns Vector2(1, 0) Geometry2D.line\_intersects\_line(from\_a,
dir\_a, from\_b, Vector2(1, -1)) \# Returns Vector2(-1, 0)
Geometry2D.line\_intersects\_line(from\_a, dir\_a, from\_b, Vector2(-1,
-1)) \# Returns null Geometry2D.line\_intersects\_line(from\_a, dir\_a,
from\_b, Vector2.RIGHT)

csharp

var fromA = Vector2.Zero; var dirA = Vector2.Right; var fromB =
Vector2.Down;

// Returns new Vector2(1, 0) Geometry2D.LineIntersectsLine(fromA, dirA,
fromB, new Vector2(1, -1)); // Returns new Vector2(-1, 0)
Geometry2D.LineIntersectsLine(fromA, dirA, fromB, new Vector2(-1, -1));
// Returns null Geometry2D.LineIntersectsLine(fromA, dirA, fromB,
Vector2.Right);

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **make\_atlas**(sizes:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_make_atlas>`

Given an array of `Vector2<class_Vector2>`s representing tiles, builds
an atlas. The returned dictionary has two keys: `points` is a
`PackedVector2Array<class_PackedVector2Array>` that specifies the
positions of each tile, `size` contains the overall size of the whole
atlas as `Vector2i<class_Vector2i>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\]
**merge\_polygons**(polygon\_a:
`PackedVector2Array<class_PackedVector2Array>`, polygon\_b:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_merge_polygons>`

Merges (combines) `polygon_a` and `polygon_b` and returns an array of
merged polygons. This performs
`OPERATION_UNION<class_Geometry2D_constant_OPERATION_UNION>` between
polygons.

The operation may result in an outer polygon (boundary) and multiple
inner polygons (holes) produced which could be distinguished by calling
`is_polygon_clockwise<class_Geometry2D_method_is_polygon_clockwise>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\]
**offset\_polygon**(polygon:
`PackedVector2Array<class_PackedVector2Array>`, delta:
`float<class_float>`, join\_type:
`PolyJoinType<enum_Geometry2D_PolyJoinType>` = 0)
`🔗<class_Geometry2D_method_offset_polygon>`

Inflates or deflates `polygon` by `delta` units (pixels). If `delta` is
positive, makes the polygon grow outward. If `delta` is negative,
shrinks the polygon inward. Returns an array of polygons because
inflating/deflating may result in multiple discrete polygons. Returns an
empty array if `delta` is negative and the absolute value of it
approximately exceeds the minimum bounding rectangle dimensions of the
polygon.

Each polygon's vertices will be rounded as determined by `join_type`,
see `PolyJoinType<enum_Geometry2D_PolyJoinType>`.

The operation may result in an outer polygon (boundary) and inner
polygon (hole) produced which could be distinguished by calling
`is_polygon_clockwise<class_Geometry2D_method_is_polygon_clockwise>`.

\*\*Note:\*\* To translate the polygon's vertices specifically, multiply
them to a `Transform2D<class_Transform2D>`:

gdscript

var polygon = PackedVector2Array(\[Vector2(0, 0), Vector2(100, 0),
Vector2(100, 100), Vector2(0, 100)\]) var offset = Vector2(50, 50)
polygon = Transform2D(0, offset) \* polygon print(polygon) \# prints
\[(50, 50), (150, 50), (150, 150), (50, 150)\]

csharp

var polygon = new Vector2\[\] { new Vector2(0, 0), new Vector2(100, 0),
new Vector2(100, 100), new Vector2(0, 100) }; var offset = new
Vector2(50, 50); polygon = new Transform2D(0, offset) \* polygon;
GD.Print((Variant)polygon); // prints \[(50, 50), (150, 50), (150, 150),
(50, 150)\]

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\]
**offset\_polyline**(polyline:
`PackedVector2Array<class_PackedVector2Array>`, delta:
`float<class_float>`, join\_type:
`PolyJoinType<enum_Geometry2D_PolyJoinType>` = 0, end\_type:
`PolyEndType<enum_Geometry2D_PolyEndType>` = 3)
`🔗<class_Geometry2D_method_offset_polyline>`

Inflates or deflates `polyline` by `delta` units (pixels), producing
polygons. If `delta` is positive, makes the polyline grow outward.
Returns an array of polygons because inflating/deflating may result in
multiple discrete polygons. If `delta` is negative, returns an empty
array.

Each polygon's vertices will be rounded as determined by `join_type`,
see `PolyJoinType<enum_Geometry2D_PolyJoinType>`.

Each polygon's endpoints will be rounded as determined by `end_type`,
see `PolyEndType<enum_Geometry2D_PolyEndType>`.

The operation may result in an outer polygon (boundary) and inner
polygon (hole) produced which could be distinguished by calling
`is_polygon_clockwise<class_Geometry2D_method_is_polygon_clockwise>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **point\_is\_inside\_triangle**(point:
`Vector2<class_Vector2>`, a: `Vector2<class_Vector2>`, b:
`Vector2<class_Vector2>`, c: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Geometry2D_method_point_is_inside_triangle>`

Returns if `point` is inside the triangle specified by `a`, `b` and `c`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **segment\_intersects\_circle**(segment\_from:
`Vector2<class_Vector2>`, segment\_to: `Vector2<class_Vector2>`,
circle\_position: `Vector2<class_Vector2>`, circle\_radius:
`float<class_float>`)
`🔗<class_Geometry2D_method_segment_intersects_circle>`

Given the 2D segment (`segment_from`, `segment_to`), returns the
position on the segment (as a number between 0 and 1) at which the
segment hits the circle that is located at position `circle_position`
and has radius `circle_radius`. If the segment does not intersect the
circle, -1 is returned (this is also the case if the line extending the
segment would intersect the circle, but the segment does not).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **segment\_intersects\_segment**(from\_a:
`Vector2<class_Vector2>`, to\_a: `Vector2<class_Vector2>`, from\_b:
`Vector2<class_Vector2>`, to\_b: `Vector2<class_Vector2>`)
`🔗<class_Geometry2D_method_segment_intersects_segment>`

Checks if the two segments (`from_a`, `to_a`) and (`from_b`, `to_b`)
intersect. If yes, return the point of intersection as
`Vector2<class_Vector2>`. If no intersection takes place, returns
`null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**triangulate\_delaunay**(points:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_triangulate_delaunay>`

Triangulates the area specified by discrete set of `points` such that no
point is inside the circumcircle of any resulting triangle. Returns a
`PackedInt32Array<class_PackedInt32Array>` where each triangle consists
of three consecutive point indices into `points` (i.e. the returned
array will have `n * 3` elements, with `n` being the number of found
triangles). If the triangulation did not succeed, an empty
`PackedInt32Array<class_PackedInt32Array>` is returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**triangulate\_polygon**(polygon:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Geometry2D_method_triangulate_polygon>`

Triangulates the polygon specified by the points in `polygon`. Returns a
`PackedInt32Array<class_PackedInt32Array>` where each triangle consists
of three consecutive point indices into `polygon` (i.e. the returned
array will have `n * 3` elements, with `n` being the number of found
triangles). Output triangles will always be counter clockwise, and the
contour will be flipped if it's clockwise. If the triangulation did not
succeed, an empty `PackedInt32Array<class_PackedInt32Array>` is
returned.
