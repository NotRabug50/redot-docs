github\_url  
hide

# AStar2D

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

An implementation of A\* for finding the shortest path between two
vertices on a connected graph in 2D space.

classref-introduction-group

## Description

An implementation of the A\* algorithm, used to find the shortest path
between two vertices on a connected graph in 2D space.

See `AStar3D<class_AStar3D>` for a more thorough explanation on how to
use this class. **AStar2D** is a wrapper for `AStar3D<class_AStar3D>`
that enforces 2D coordinates.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **\_compute\_cost**(from\_id: `int<class_int>`,
to\_id: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_private_method__compute_cost>`

Called when computing the cost between two connected points.

Note that this function is hidden in the default **AStar2D** class.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_estimate\_cost**(from\_id: `int<class_int>`,
end\_id: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_private_method__estimate_cost>`

Called when estimating the cost between a point and the path's ending
point.

Note that this function is hidden in the default **AStar2D** class.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_point**(id: `int<class_int>`, position:
`Vector2<class_Vector2>`, weight\_scale: `float<class_float>` = 1.0)
`🔗<class_AStar2D_method_add_point>`

Adds a new point at the given position with the given identifier. The
`id` must be 0 or larger, and the `weight_scale` must be 0.0 or greater.

The `weight_scale` is multiplied by the result of
`_compute_cost<class_AStar2D_private_method__compute_cost>` when
determining the overall cost of traveling across a segment from a
neighboring point to this point. Thus, all else being equal, the
algorithm prefers points with lower `weight_scale`s to form a path.

gdscript

var astar = AStar2D.new() astar.add\_point(1, Vector2(1, 0), 4) \# Adds
the point (1, 0) with weight\_scale 4 and id 1

csharp

var astar = new AStar2D(); astar.AddPoint(1, new Vector2(1, 0), 4); //
Adds the point (1, 0) with weight\_scale 4 and id 1

If there already exists a point for the given `id`, its position and
weight scale are updated to the given values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **are\_points\_connected**(id: `int<class_int>`,
to\_id: `int<class_int>`, bidirectional: `bool<class_bool>` = true)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_method_are_points_connected>`

Returns whether there is a connection/segment between the given points.
If `bidirectional` is `false`, returns whether movement from `id` to
`to_id` is possible through this segment.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**() `🔗<class_AStar2D_method_clear>`

Clears all the points and segments.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **connect\_points**(id: `int<class_int>`,
to\_id: `int<class_int>`, bidirectional: `bool<class_bool>` = true)
`🔗<class_AStar2D_method_connect_points>`

Creates a segment between the given points. If `bidirectional` is
`false`, only movement from `id` to `to_id` is allowed, not the reverse
direction.

gdscript

var astar = AStar2D.new() astar.add\_point(1, Vector2(1, 1))
astar.add\_point(2, Vector2(0, 5)) astar.connect\_points(1, 2, false)

csharp

var astar = new AStar2D(); astar.AddPoint(1, new Vector2(1, 1));
astar.AddPoint(2, new Vector2(0, 5)); astar.ConnectPoints(1, 2, false);

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **disconnect\_points**(id: `int<class_int>`,
to\_id: `int<class_int>`, bidirectional: `bool<class_bool>` = true)
`🔗<class_AStar2D_method_disconnect_points>`

Deletes the segment between the given points. If `bidirectional` is
`false`, only movement from `id` to `to_id` is prevented, and a
unidirectional segment possibly remains.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_available\_point\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_method_get_available_point_id>`

Returns the next available point ID with no point associated to it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_closest\_point**(to\_position:
`Vector2<class_Vector2>`, include\_disabled: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_method_get_closest_point>`

Returns the ID of the closest point to `to_position`, optionally taking
disabled points into account. Returns `-1` if there are no points in the
points pool.

\*\*Note:\*\* If several points are the closest to `to_position`, the
one with the smallest ID will be returned, ensuring a deterministic
result.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**get\_closest\_position\_in\_segment**(to\_position:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_method_get_closest_position_in_segment>`

Returns the closest position to `to_position` that resides inside a
segment between two connected points.

gdscript

var astar = AStar2D.new() astar.add\_point(1, Vector2(0, 0))
astar.add\_point(2, Vector2(0, 5)) astar.connect\_points(1, 2) var res =
astar.get\_closest\_position\_in\_segment(Vector2(3, 3)) \# Returns (0,
3)

csharp

var astar = new AStar2D(); astar.AddPoint(1, new Vector2(0, 0));
astar.AddPoint(2, new Vector2(0, 5)); astar.ConnectPoints(1, 2); Vector2
res = astar.GetClosestPositionInSegment(new Vector2(3, 3)); // Returns
(0, 3)

The result is in the segment that goes from `y = 0` to `y = 5`. It's the
closest position in the segment to the given point.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt64Array<class_PackedInt64Array>` **get\_id\_path**(from\_id:
`int<class_int>`, to\_id: `int<class_int>`, allow\_partial\_path:
`bool<class_bool>` = false) `🔗<class_AStar2D_method_get_id_path>`

Returns an array with the IDs of the points that form the path found by
AStar2D between the given points. The array is ordered from the starting
point to the ending point of the path.

If there is no valid path to the target, and `allow_partial_path` is
`true`, returns a path to the point closest to the target that can be
reached.

\*\*Note:\*\* When `allow_partial_path` is `true` and `to_id` is
disabled the search may take an unusually long time to finish.

gdscript

var astar = AStar2D.new() astar.add\_point(1, Vector2(0, 0))
astar.add\_point(2, Vector2(0, 1), 1) \# Default weight is 1
astar.add\_point(3, Vector2(1, 1)) astar.add\_point(4, Vector2(2, 0))

astar.connect\_points(1, 2, false) astar.connect\_points(2, 3, false)
astar.connect\_points(4, 3, false) astar.connect\_points(1, 4, false)

var res = astar.get\_id\_path(1, 3) \# Returns \[1, 2, 3\]

csharp

var astar = new AStar2D(); astar.AddPoint(1, new Vector2(0, 0));
astar.AddPoint(2, new Vector2(0, 1), 1); // Default weight is 1
astar.AddPoint(3, new Vector2(1, 1)); astar.AddPoint(4, new Vector2(2,
0));

astar.ConnectPoints(1, 2, false); astar.ConnectPoints(2, 3, false);
astar.ConnectPoints(4, 3, false); astar.ConnectPoints(1, 4, false);
long\[\] res = astar.GetIdPath(1, 3); // Returns \[1, 2, 3\]

If you change the 2nd point's weight to 3, then the result will be
`[1, 4, 3]` instead, because now even though the distance is longer,
it's "easier" to get through point 4 than through point 2.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_point\_capacity**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_method_get_point_capacity>`

Returns the capacity of the structure backing the points, useful in
conjunction with `reserve_space<class_AStar2D_method_reserve_space>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt64Array<class_PackedInt64Array>`
**get\_point\_connections**(id: `int<class_int>`)
`🔗<class_AStar2D_method_get_point_connections>`

Returns an array with the IDs of the points that form the connection
with the given point.

gdscript

var astar = AStar2D.new() astar.add\_point(1, Vector2(0, 0))
astar.add\_point(2, Vector2(0, 1)) astar.add\_point(3, Vector2(1, 1))
astar.add\_point(4, Vector2(2, 0))

astar.connect\_points(1, 2, true) astar.connect\_points(1, 3, true)

var neighbors = astar.get\_point\_connections(1) \# Returns \[2, 3\]

csharp

var astar = new AStar2D(); astar.AddPoint(1, new Vector2(0, 0));
astar.AddPoint(2, new Vector2(0, 1)); astar.AddPoint(3, new Vector2(1,
1)); astar.AddPoint(4, new Vector2(2, 0));

astar.ConnectPoints(1, 2, true); astar.ConnectPoints(1, 3, true);

long\[\] neighbors = astar.GetPointConnections(1); // Returns \[2, 3\]

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_point\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_method_get_point_count>`

Returns the number of points currently in the points pool.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt64Array<class_PackedInt64Array>` **get\_point\_ids**()
`🔗<class_AStar2D_method_get_point_ids>`

Returns an array of all point IDs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**get\_point\_path**(from\_id: `int<class_int>`, to\_id:
`int<class_int>`, allow\_partial\_path: `bool<class_bool>` = false)
`🔗<class_AStar2D_method_get_point_path>`

Returns an array with the points that are in the path found by AStar2D
between the given points. The array is ordered from the starting point
to the ending point of the path.

If there is no valid path to the target, and `allow_partial_path` is
`true`, returns a path to the point closest to the target that can be
reached.

\*\*Note:\*\* This method is not thread-safe. If called from a
`Thread<class_Thread>`, it will return an empty array and will print an
error message.

Additionally, when `allow_partial_path` is `true` and `to_id` is
disabled the search may take an unusually long time to finish.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_point\_position**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_method_get_point_position>`

Returns the position of the point associated with the given `id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_point\_weight\_scale**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_method_get_point_weight_scale>`

Returns the weight scale of the point associated with the given `id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_point**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_method_has_point>`

Returns whether a point associated with the given `id` exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_point\_disabled**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStar2D_method_is_point_disabled>`

Returns whether a point is disabled or not for pathfinding. By default,
all points are enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_point**(id: `int<class_int>`)
`🔗<class_AStar2D_method_remove_point>`

Removes the point associated with the given `id` from the points pool.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reserve\_space**(num\_nodes:
`int<class_int>`) `🔗<class_AStar2D_method_reserve_space>`

Reserves space internally for `num_nodes` points, useful if you're
adding a known large number of points at once, such as points on a grid.
New capacity must be greater or equals to old capacity.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_disabled**(id: `int<class_int>`,
disabled: `bool<class_bool>` = true)
`🔗<class_AStar2D_method_set_point_disabled>`

Disables or enables the specified point for pathfinding. Useful for
making a temporary obstacle.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_position**(id: `int<class_int>`,
position: `Vector2<class_Vector2>`)
`🔗<class_AStar2D_method_set_point_position>`

Sets the `position` for the point with the given `id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_weight\_scale**(id:
`int<class_int>`, weight\_scale: `float<class_float>`)
`🔗<class_AStar2D_method_set_point_weight_scale>`

Sets the `weight_scale` for the point with the given `id`. The
`weight_scale` is multiplied by the result of
`_compute_cost<class_AStar2D_private_method__compute_cost>` when
determining the overall cost of traveling across a segment from a
neighboring point to this point.
