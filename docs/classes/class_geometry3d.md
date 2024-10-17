github\_url  
hide

# Geometry3D

**Inherits:** `Object<class_Object>`

Provides methods for some common 3D geometric operations.

classref-introduction-group

## Description

Provides a set of helper functions to create geometric shapes, compute
intersections between shapes, and process various other geometric
operations in 3D.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Array<class_Array>`\[`Plane<class_Plane>`\]
**build\_box\_planes**(extents: `Vector3<class_Vector3>`)
`🔗<class_Geometry3D_method_build_box_planes>`

Returns an array with 6 `Plane<class_Plane>`s that describe the sides of
a box centered at the origin. The box size is defined by `extents`,
which represents one (positive) corner of the box (i.e. half its actual
size).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Plane<class_Plane>`\]
**build\_capsule\_planes**(radius: `float<class_float>`, height:
`float<class_float>`, sides: `int<class_int>`, lats: `int<class_int>`,
axis: Vector3.Axis = 2)
`🔗<class_Geometry3D_method_build_capsule_planes>`

Returns an array of `Plane<class_Plane>`s closely bounding a faceted
capsule centered at the origin with radius `radius` and height `height`.
The parameter `sides` defines how many planes will be generated for the
side part of the capsule, whereas `lats` gives the number of latitudinal
steps at the bottom and top of the capsule. The parameter `axis`
describes the axis along which the capsule is oriented (0 for X, 1 for
Y, 2 for Z).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Plane<class_Plane>`\]
**build\_cylinder\_planes**(radius: `float<class_float>`, height:
`float<class_float>`, sides: `int<class_int>`, axis: Vector3.Axis = 2)
`🔗<class_Geometry3D_method_build_cylinder_planes>`

Returns an array of `Plane<class_Plane>`s closely bounding a faceted
cylinder centered at the origin with radius `radius` and height
`height`. The parameter `sides` defines how many planes will be
generated for the round part of the cylinder. The parameter `axis`
describes the axis along which the cylinder is oriented (0 for X, 1 for
Y, 2 for Z).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>` **clip\_polygon**(points:
`PackedVector3Array<class_PackedVector3Array>`, plane:
`Plane<class_Plane>`) `🔗<class_Geometry3D_method_clip_polygon>`

Clips the polygon defined by the points in `points` against the `plane`
and returns the points of the clipped polygon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>`
**compute\_convex\_mesh\_points**(planes:
`Array<class_Array>`\[`Plane<class_Plane>`\])
`🔗<class_Geometry3D_method_compute_convex_mesh_points>`

Calculates and returns all the vertex points of a convex shape defined
by an array of `planes`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_closest\_point\_to\_segment**(point:
`Vector3<class_Vector3>`, s1: `Vector3<class_Vector3>`, s2:
`Vector3<class_Vector3>`)
`🔗<class_Geometry3D_method_get_closest_point_to_segment>`

Returns the 3D point on the 3D segment (`s1`, `s2`) that is closest to
`point`. The returned point will always be inside the specified segment.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>`
**get\_closest\_point\_to\_segment\_uncapped**(point:
`Vector3<class_Vector3>`, s1: `Vector3<class_Vector3>`, s2:
`Vector3<class_Vector3>`)
`🔗<class_Geometry3D_method_get_closest_point_to_segment_uncapped>`

Returns the 3D point on the 3D line defined by (`s1`, `s2`) that is
closest to `point`. The returned point can be inside the segment (`s1`,
`s2`) or outside of it, i.e. somewhere on the line extending from the
segment.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>`
**get\_closest\_points\_between\_segments**(p1:
`Vector3<class_Vector3>`, p2: `Vector3<class_Vector3>`, q1:
`Vector3<class_Vector3>`, q2: `Vector3<class_Vector3>`)
`🔗<class_Geometry3D_method_get_closest_points_between_segments>`

Given the two 3D segments (`p1`, `p2`) and (`q1`, `q2`), finds those two
points on the two segments that are closest to each other. Returns a
`PackedVector3Array<class_PackedVector3Array>` that contains this point
on (`p1`, `p2`) as well the accompanying point on (`q1`, `q2`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_triangle\_barycentric\_coords**(point:
`Vector3<class_Vector3>`, a: `Vector3<class_Vector3>`, b:
`Vector3<class_Vector3>`, c: `Vector3<class_Vector3>`)
`🔗<class_Geometry3D_method_get_triangle_barycentric_coords>`

Returns a `Vector3<class_Vector3>` containing weights based on how close
a 3D position (`point`) is to a triangle's different vertices (`a`, `b`
and `c`). This is useful for interpolating between the data of different
vertices in a triangle. One example use case is using this to smoothly
rotate over a mesh instead of relying solely on face normals.

[Here is a more detailed explanation of barycentric
coordinates.](https://en.wikipedia.org/wiki/Barycentric_coordinate_system)

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **ray\_intersects\_triangle**(from:
`Vector3<class_Vector3>`, dir: `Vector3<class_Vector3>`, a:
`Vector3<class_Vector3>`, b: `Vector3<class_Vector3>`, c:
`Vector3<class_Vector3>`)
`🔗<class_Geometry3D_method_ray_intersects_triangle>`

Tests if the 3D ray starting at `from` with the direction of `dir`
intersects the triangle specified by `a`, `b` and `c`. If yes, returns
the point of intersection as `Vector3<class_Vector3>`. If no
intersection takes place, returns `null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>`
**segment\_intersects\_convex**(from: `Vector3<class_Vector3>`, to:
`Vector3<class_Vector3>`, planes:
`Array<class_Array>`\[`Plane<class_Plane>`\])
`🔗<class_Geometry3D_method_segment_intersects_convex>`

Given a convex hull defined though the `Plane<class_Plane>`s in the
array `planes`, tests if the segment (`from`, `to`) intersects with that
hull. If an intersection is found, returns a
`PackedVector3Array<class_PackedVector3Array>` containing the point the
intersection and the hull's normal. Otherwise, returns an empty array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>`
**segment\_intersects\_cylinder**(from: `Vector3<class_Vector3>`, to:
`Vector3<class_Vector3>`, height: `float<class_float>`, radius:
`float<class_float>`)
`🔗<class_Geometry3D_method_segment_intersects_cylinder>`

Checks if the segment (`from`, `to`) intersects the cylinder with height
`height` that is centered at the origin and has radius `radius`. If no,
returns an empty `PackedVector3Array<class_PackedVector3Array>`. If an
intersection takes place, the returned array contains the point of
intersection and the cylinder's normal at the point of intersection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>`
**segment\_intersects\_sphere**(from: `Vector3<class_Vector3>`, to:
`Vector3<class_Vector3>`, sphere\_position: `Vector3<class_Vector3>`,
sphere\_radius: `float<class_float>`)
`🔗<class_Geometry3D_method_segment_intersects_sphere>`

Checks if the segment (`from`, `to`) intersects the sphere that is
located at `sphere_position` and has radius `sphere_radius`. If no,
returns an empty `PackedVector3Array<class_PackedVector3Array>`. If yes,
returns a `PackedVector3Array<class_PackedVector3Array>` containing the
point of intersection and the sphere's normal at the point of
intersection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **segment\_intersects\_triangle**(from:
`Vector3<class_Vector3>`, to: `Vector3<class_Vector3>`, a:
`Vector3<class_Vector3>`, b: `Vector3<class_Vector3>`, c:
`Vector3<class_Vector3>`)
`🔗<class_Geometry3D_method_segment_intersects_triangle>`

Tests if the segment (`from`, `to`) intersects the triangle `a`, `b`,
`c`. If yes, returns the point of intersection as
`Vector3<class_Vector3>`. If no intersection takes place, returns
`null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**tetrahedralize\_delaunay**(points:
`PackedVector3Array<class_PackedVector3Array>`)
`🔗<class_Geometry3D_method_tetrahedralize_delaunay>`

Tetrahedralizes the volume specified by a discrete set of `points` in 3D
space, ensuring that no point lies within the circumsphere of any
resulting tetrahedron. The method returns a
`PackedInt32Array<class_PackedInt32Array>` where each tetrahedron
consists of four consecutive point indices into the `points` array
(resulting in an array with `n * 4` elements, where `n` is the number of
tetrahedra found). If the tetrahedralization is unsuccessful, an empty
`PackedInt32Array<class_PackedInt32Array>` is returned.
