github\_url  
hide

# AStarGrid2D

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

An implementation of A\* for finding the shortest path between two
points on a partial 2D grid.

classref-introduction-group

## Description

**AStarGrid2D** is a variant of `AStar2D<class_AStar2D>` that is
specialized for partial 2D grids. It is simpler to use because it
doesn't require you to manually create points and connect them together.
This class also supports multiple types of heuristics, modes for
diagonal movement, and a jumping mode to speed up calculations.

To use **AStarGrid2D**, you only need to set the
`region<class_AStarGrid2D_property_region>` of the grid, optionally set
the `cell_size<class_AStarGrid2D_property_cell_size>`, and then call the
`update<class_AStarGrid2D_method_update>` method:

gdscript

var astar\_grid = AStarGrid2D.new() astar\_grid.region = Rect2i(0, 0,
32, 32) astar\_grid.cell\_size = Vector2(16, 16) astar\_grid.update()
print(astar\_grid.get\_id\_path(Vector2i(0, 0), Vector2i(3, 4))) \#
prints (0, 0), (1, 1), (2, 2), (3, 3), (3, 4)
print(astar\_grid.get\_point\_path(Vector2i(0, 0), Vector2i(3, 4))) \#
prints (0, 0), (16, 16), (32, 32), (48, 48), (48, 64)

csharp

AStarGrid2D astarGrid = new AStarGrid2D(); astarGrid.Region = new
Rect2I(0, 0, 32, 32); astarGrid.CellSize = new Vector2I(16, 16);
astarGrid.Update(); GD.Print(astarGrid.GetIdPath(Vector2I.Zero, new
Vector2I(3, 4))); // prints (0, 0), (1, 1), (2, 2), (3, 3), (3, 4)
GD.Print(astarGrid.GetPointPath(Vector2I.Zero, new Vector2I(3, 4))); //
prints (0, 0), (16, 16), (32, 32), (48, 48), (48, 64)

To remove a point from the pathfinding grid, it must be set as "solid"
with `set_point_solid<class_AStarGrid2D_method_set_point_solid>`.

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

enum **Heuristic**: `🔗<enum_AStarGrid2D_Heuristic>`

classref-enumeration-constant

`Heuristic<enum_AStarGrid2D_Heuristic>` **HEURISTIC\_EUCLIDEAN** = `0`

The [Euclidean
heuristic](https://en.wikipedia.org/wiki/Euclidean_distance) to be used
for the pathfinding using the following formula:

    dx = abs(to_id.x - from_id.x)
    dy = abs(to_id.y - from_id.y)
    result = sqrt(dx * dx + dy * dy)

\*\*Note:\*\* This is also the internal heuristic used in
`AStar3D<class_AStar3D>` and `AStar2D<class_AStar2D>` by default (with
the inclusion of possible z-axis coordinate).

classref-enumeration-constant

`Heuristic<enum_AStarGrid2D_Heuristic>` **HEURISTIC\_MANHATTAN** = `1`

The [Manhattan
heuristic](https://en.wikipedia.org/wiki/Taxicab_geometry) to be used
for the pathfinding using the following formula:

    dx = abs(to_id.x - from_id.x)
    dy = abs(to_id.y - from_id.y)
    result = dx + dy

\*\*Note:\*\* This heuristic is intended to be used with 4-side
orthogonal movements, provided by setting the
`diagonal_mode<class_AStarGrid2D_property_diagonal_mode>` to
`DIAGONAL_MODE_NEVER<class_AStarGrid2D_constant_DIAGONAL_MODE_NEVER>`.

classref-enumeration-constant

`Heuristic<enum_AStarGrid2D_Heuristic>` **HEURISTIC\_OCTILE** = `2`

The Octile heuristic to be used for the pathfinding using the following
formula:

    dx = abs(to_id.x - from_id.x)
    dy = abs(to_id.y - from_id.y)
    f = sqrt(2) - 1
    result = (dx < dy) ? f * dx + dy : f * dy + dx;

classref-enumeration-constant

`Heuristic<enum_AStarGrid2D_Heuristic>` **HEURISTIC\_CHEBYSHEV** = `3`

The [Chebyshev
heuristic](https://en.wikipedia.org/wiki/Chebyshev_distance) to be used
for the pathfinding using the following formula:

    dx = abs(to_id.x - from_id.x)
    dy = abs(to_id.y - from_id.y)
    result = max(dx, dy)

classref-enumeration-constant

`Heuristic<enum_AStarGrid2D_Heuristic>` **HEURISTIC\_MAX** = `4`

Represents the size of the `Heuristic<enum_AStarGrid2D_Heuristic>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DiagonalMode**: `🔗<enum_AStarGrid2D_DiagonalMode>`

classref-enumeration-constant

`DiagonalMode<enum_AStarGrid2D_DiagonalMode>` **DIAGONAL\_MODE\_ALWAYS**
= `0`

The pathfinding algorithm will ignore solid neighbors around the target
cell and allow passing using diagonals.

classref-enumeration-constant

`DiagonalMode<enum_AStarGrid2D_DiagonalMode>` **DIAGONAL\_MODE\_NEVER**
= `1`

The pathfinding algorithm will ignore all diagonals and the way will be
always orthogonal.

classref-enumeration-constant

`DiagonalMode<enum_AStarGrid2D_DiagonalMode>`
**DIAGONAL\_MODE\_AT\_LEAST\_ONE\_WALKABLE** = `2`

The pathfinding algorithm will avoid using diagonals if at least two
obstacles have been placed around the neighboring cells of the specific
path segment.

classref-enumeration-constant

`DiagonalMode<enum_AStarGrid2D_DiagonalMode>`
**DIAGONAL\_MODE\_ONLY\_IF\_NO\_OBSTACLES** = `3`

The pathfinding algorithm will avoid using diagonals if any obstacle has
been placed around the neighboring cells of the specific path segment.

classref-enumeration-constant

`DiagonalMode<enum_AStarGrid2D_DiagonalMode>` **DIAGONAL\_MODE\_MAX** =
`4`

Represents the size of the `DiagonalMode<enum_AStarGrid2D_DiagonalMode>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CellShape**: `🔗<enum_AStarGrid2D_CellShape>`

classref-enumeration-constant

`CellShape<enum_AStarGrid2D_CellShape>` **CELL\_SHAPE\_SQUARE** = `0`

Rectangular cell shape.

classref-enumeration-constant

`CellShape<enum_AStarGrid2D_CellShape>`
**CELL\_SHAPE\_ISOMETRIC\_RIGHT** = `1`

Diamond cell shape (for isometric look). Cell coordinates layout where
the horizontal axis goes up-right, and the vertical one goes down-right.

classref-enumeration-constant

`CellShape<enum_AStarGrid2D_CellShape>` **CELL\_SHAPE\_ISOMETRIC\_DOWN**
= `2`

Diamond cell shape (for isometric look). Cell coordinates layout where
the horizontal axis goes down-right, and the vertical one goes
down-left.

classref-enumeration-constant

`CellShape<enum_AStarGrid2D_CellShape>` **CELL\_SHAPE\_MAX** = `3`

Represents the size of the `CellShape<enum_AStarGrid2D_CellShape>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`CellShape<enum_AStarGrid2D_CellShape>` **cell\_shape** = `0`
`🔗<class_AStarGrid2D_property_cell_shape>`

classref-property-setget

-   `void (No return value.)` **set\_cell\_shape**(value:
    `CellShape<enum_AStarGrid2D_CellShape>`)
-   `CellShape<enum_AStarGrid2D_CellShape>` **get\_cell\_shape**()

The cell shape. Affects how the positions are placed in the grid. If
changed, `update<class_AStarGrid2D_method_update>` needs to be called
before finding the next path.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **cell\_size** = `Vector2(1, 1)`
`🔗<class_AStarGrid2D_property_cell_size>`

classref-property-setget

-   `void (No return value.)` **set\_cell\_size**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_cell\_size**()

The size of the point cell which will be applied to calculate the
resulting point position returned by
`get_point_path<class_AStarGrid2D_method_get_point_path>`. If changed,
`update<class_AStarGrid2D_method_update>` needs to be called before
finding the next path.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Heuristic<enum_AStarGrid2D_Heuristic>` **default\_compute\_heuristic**
= `0` `🔗<class_AStarGrid2D_property_default_compute_heuristic>`

classref-property-setget

-   `void (No return value.)`
    **set\_default\_compute\_heuristic**(value:
    `Heuristic<enum_AStarGrid2D_Heuristic>`)
-   `Heuristic<enum_AStarGrid2D_Heuristic>`
    **get\_default\_compute\_heuristic**()

The default `Heuristic<enum_AStarGrid2D_Heuristic>` which will be used
to calculate the cost between two points if
`_compute_cost<class_AStarGrid2D_private_method__compute_cost>` was not
overridden.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Heuristic<enum_AStarGrid2D_Heuristic>` **default\_estimate\_heuristic**
= `0` `🔗<class_AStarGrid2D_property_default_estimate_heuristic>`

classref-property-setget

-   `void (No return value.)`
    **set\_default\_estimate\_heuristic**(value:
    `Heuristic<enum_AStarGrid2D_Heuristic>`)
-   `Heuristic<enum_AStarGrid2D_Heuristic>`
    **get\_default\_estimate\_heuristic**()

The default `Heuristic<enum_AStarGrid2D_Heuristic>` which will be used
to calculate the cost between the point and the end point if
`_estimate_cost<class_AStarGrid2D_private_method__estimate_cost>` was
not overridden.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DiagonalMode<enum_AStarGrid2D_DiagonalMode>` **diagonal\_mode** = `0`
`🔗<class_AStarGrid2D_property_diagonal_mode>`

classref-property-setget

-   `void (No return value.)` **set\_diagonal\_mode**(value:
    `DiagonalMode<enum_AStarGrid2D_DiagonalMode>`)
-   `DiagonalMode<enum_AStarGrid2D_DiagonalMode>`
    **get\_diagonal\_mode**()

A specific `DiagonalMode<enum_AStarGrid2D_DiagonalMode>` mode which will
force the path to avoid or accept the specified diagonals.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **jumping\_enabled** = `false`
`🔗<class_AStarGrid2D_property_jumping_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_jumping\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_jumping\_enabled**()

Enables or disables jumping to skip up the intermediate points and
speeds up the searching algorithm.

\*\*Note:\*\* Currently, toggling it on disables the consideration of
weight scaling in pathfinding.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **offset** = `Vector2(0, 0)`
`🔗<class_AStarGrid2D_property_offset>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_offset**()

The offset of the grid which will be applied to calculate the resulting
point position returned by
`get_point_path<class_AStarGrid2D_method_get_point_path>`. If changed,
`update<class_AStarGrid2D_method_update>` needs to be called before
finding the next path.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Rect2i<class_Rect2i>` **region** = `Rect2i(0, 0, 0, 0)`
`🔗<class_AStarGrid2D_property_region>`

classref-property-setget

-   `void (No return value.)` **set\_region**(value:
    `Rect2i<class_Rect2i>`)
-   `Rect2i<class_Rect2i>` **get\_region**()

The region of grid cells available for pathfinding. If changed,
`update<class_AStarGrid2D_method_update>` needs to be called before
finding the next path.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **size** = `Vector2i(0, 0)`
`🔗<class_AStarGrid2D_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_size**()

**Deprecated:** Use `region<class_AStarGrid2D_property_region>` instead.

The size of the grid (number of cells of size
`cell_size<class_AStarGrid2D_property_cell_size>` on each axis). If
changed, `update<class_AStarGrid2D_method_update>` needs to be called
before finding the next path.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **\_compute\_cost**(from\_id:
`Vector2i<class_Vector2i>`, to\_id: `Vector2i<class_Vector2i>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStarGrid2D_private_method__compute_cost>`

Called when computing the cost between two connected points.

Note that this function is hidden in the default **AStarGrid2D** class.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_estimate\_cost**(from\_id:
`Vector2i<class_Vector2i>`, end\_id: `Vector2i<class_Vector2i>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStarGrid2D_private_method__estimate_cost>`

Called when estimating the cost between a point and the path's ending
point.

Note that this function is hidden in the default **AStarGrid2D** class.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_AStarGrid2D_method_clear>`

Clears the grid and sets the `region<class_AStarGrid2D_property_region>`
to `Rect2i(0, 0, 0, 0)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fill\_solid\_region**(region:
`Rect2i<class_Rect2i>`, solid: `bool<class_bool>` = true)
`🔗<class_AStarGrid2D_method_fill_solid_region>`

Fills the given `region` on the grid with the specified value for the
solid flag.

\*\*Note:\*\* Calling `update<class_AStarGrid2D_method_update>` is not
needed after the call of this function.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fill\_weight\_scale\_region**(region:
`Rect2i<class_Rect2i>`, weight\_scale: `float<class_float>`)
`🔗<class_AStarGrid2D_method_fill_weight_scale_region>`

Fills the given `region` on the grid with the specified value for the
weight scale.

\*\*Note:\*\* Calling `update<class_AStarGrid2D_method_update>` is not
needed after the call of this function.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector2i<class_Vector2i>`\]
**get\_id\_path**(from\_id: `Vector2i<class_Vector2i>`, to\_id:
`Vector2i<class_Vector2i>`, allow\_partial\_path: `bool<class_bool>` =
false) `🔗<class_AStarGrid2D_method_get_id_path>`

Returns an array with the IDs of the points that form the path found by
AStar2D between the given points. The array is ordered from the starting
point to the ending point of the path.

If there is no valid path to the target, and `allow_partial_path` is
`true`, returns a path to the point closest to the target that can be
reached.

\*\*Note:\*\* When `allow_partial_path` is `true` and `to_id` is solid
the search may take an unusually long time to finish.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_point\_data\_in\_region**(region: `Rect2i<class_Rect2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStarGrid2D_method_get_point_data_in_region>`

Returns an array of dictionaries with point data (`id`:
`Vector2i<class_Vector2i>`, `position`: `Vector2<class_Vector2>`,
`solid`: `bool<class_bool>`, `weight_scale`: `float<class_float>`)
within a `region`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**get\_point\_path**(from\_id: `Vector2i<class_Vector2i>`, to\_id:
`Vector2i<class_Vector2i>`, allow\_partial\_path: `bool<class_bool>` =
false) `🔗<class_AStarGrid2D_method_get_point_path>`

Returns an array with the points that are in the path found by
**AStarGrid2D** between the given points. The array is ordered from the
starting point to the ending point of the path.

If there is no valid path to the target, and `allow_partial_path` is
`true`, returns a path to the point closest to the target that can be
reached.

\*\*Note:\*\* This method is not thread-safe. If called from a
`Thread<class_Thread>`, it will return an empty array and will print an
error message.

Additionally, when `allow_partial_path` is `true` and `to_id` is solid
the search may take an unusually long time to finish.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_point\_position**(id:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStarGrid2D_method_get_point_position>`

Returns the position of the point associated with the given `id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_point\_weight\_scale**(id:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStarGrid2D_method_get_point_weight_scale>`

Returns the weight scale of the point associated with the given `id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_dirty**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStarGrid2D_method_is_dirty>`

Indicates that the grid parameters were changed and
`update<class_AStarGrid2D_method_update>` needs to be called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_in\_bounds**(x: `int<class_int>`, y:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStarGrid2D_method_is_in_bounds>`

Returns `true` if the `x` and `y` is a valid grid coordinate (id), i.e.
if it is inside `region<class_AStarGrid2D_property_region>`. Equivalent
to `region.has_point(Vector2i(x, y))`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_in\_boundsv**(id: `Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStarGrid2D_method_is_in_boundsv>`

Returns `true` if the `id` vector is a valid grid coordinate, i.e. if it
is inside `region<class_AStarGrid2D_property_region>`. Equivalent to
`region.has_point(id)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_point\_solid**(id: `Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AStarGrid2D_method_is_point_solid>`

Returns `true` if a point is disabled for pathfinding. By default, all
points are enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_solid**(id:
`Vector2i<class_Vector2i>`, solid: `bool<class_bool>` = true)
`🔗<class_AStarGrid2D_method_set_point_solid>`

Disables or enables the specified point for pathfinding. Useful for
making an obstacle. By default, all points are enabled.

\*\*Note:\*\* Calling `update<class_AStarGrid2D_method_update>` is not
needed after the call of this function.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_weight\_scale**(id:
`Vector2i<class_Vector2i>`, weight\_scale: `float<class_float>`)
`🔗<class_AStarGrid2D_method_set_point_weight_scale>`

Sets the `weight_scale` for the point with the given `id`. The
`weight_scale` is multiplied by the result of
`_compute_cost<class_AStarGrid2D_private_method__compute_cost>` when
determining the overall cost of traveling across a segment from a
neighboring point to this point.

\*\*Note:\*\* Calling `update<class_AStarGrid2D_method_update>` is not
needed after the call of this function.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update**()
`🔗<class_AStarGrid2D_method_update>`

Updates the internal state of the grid according to the parameters to
prepare it to search the path. Needs to be called if parameters like
`region<class_AStarGrid2D_property_region>`,
`cell_size<class_AStarGrid2D_property_cell_size>` or
`offset<class_AStarGrid2D_property_offset>` are changed.
`is_dirty<class_AStarGrid2D_method_is_dirty>` will return `true` if this
is the case and this needs to be called.

\*\*Note:\*\* All point data (solidity and weight scale) will be
cleared.
