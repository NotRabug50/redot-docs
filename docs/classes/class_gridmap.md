github\_url  
hide

# GridMap

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

Node for 3D tile-based maps.

classref-introduction-group

## Description

GridMap lets you place meshes on a grid interactively. It works both
from the editor and from scripts, which can help you create in-game
level editors.

GridMaps use a `MeshLibrary<class_MeshLibrary>` which contains a list of
tiles. Each tile is a mesh with materials plus optional collision and
navigation shapes.

A GridMap contains a collection of cells. Each grid cell refers to a
tile in the `MeshLibrary<class_MeshLibrary>`. All cells in the map have
the same dimensions.

Internally, a GridMap is split into a sparse collection of octants for
efficient rendering and physics processing. Every octant has the same
dimensions and can contain several cells.

\*\*Note:\*\* GridMap doesn't extend
`VisualInstance3D<class_VisualInstance3D>` and therefore can't be hidden
or cull masked based on
`VisualInstance3D.layers<class_VisualInstance3D_property_layers>`. If
you make a light not affect the first layer, the whole GridMap won't be
lit by the light in question.

classref-introduction-group

## Tutorials

-   `Using gridmaps <../tutorials/3d/using_gridmaps>`
-   [3D Platformer
    Demo](https://godotengine.org/asset-library/asset/2748)
-   [3D Kinematic Character
    Demo](https://godotengine.org/asset-library/asset/2739)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**cell\_size\_changed**(cell\_size: `Vector3<class_Vector3>`)
`🔗<class_GridMap_signal_cell_size_changed>`

Emitted when `cell_size<class_GridMap_property_cell_size>` changes.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**changed**() `🔗<class_GridMap_signal_changed>`

Emitted when the `MeshLibrary<class_MeshLibrary>` of this GridMap
changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**INVALID\_CELL\_ITEM** = `-1`
`🔗<class_GridMap_constant_INVALID_CELL_ITEM>`

Invalid cell item that can be used in
`set_cell_item<class_GridMap_method_set_cell_item>` to clear cells (or
represent an empty cell in
`get_cell_item<class_GridMap_method_get_cell_item>`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **bake\_navigation** = `false`
`🔗<class_GridMap_property_bake_navigation>`

classref-property-setget

-   `void (No return value.)` **set\_bake\_navigation**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_baking\_navigation**()

If `true`, this GridMap creates a navigation region for each cell that
uses a `mesh_library<class_GridMap_property_mesh_library>` item with a
navigation mesh. The created navigation region will use the navigation
layers bitmask assigned to the `MeshLibrary<class_MeshLibrary>`'s item.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **cell\_center\_x** = `true`
`🔗<class_GridMap_property_cell_center_x>`

classref-property-setget

-   `void (No return value.)` **set\_center\_x**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_center\_x**()

If `true`, grid items are centered on the X axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **cell\_center\_y** = `true`
`🔗<class_GridMap_property_cell_center_y>`

classref-property-setget

-   `void (No return value.)` **set\_center\_y**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_center\_y**()

If `true`, grid items are centered on the Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **cell\_center\_z** = `true`
`🔗<class_GridMap_property_cell_center_z>`

classref-property-setget

-   `void (No return value.)` **set\_center\_z**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_center\_z**()

If `true`, grid items are centered on the Z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **cell\_octant\_size** = `8`
`🔗<class_GridMap_property_cell_octant_size>`

classref-property-setget

-   `void (No return value.)` **set\_octant\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_octant\_size**()

The size of each octant measured in number of cells. This applies to all
three axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **cell\_scale** = `1.0`
`🔗<class_GridMap_property_cell_scale>`

classref-property-setget

-   `void (No return value.)` **set\_cell\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_cell\_scale**()

The scale of the cell items.

This does not affect the size of the grid cells themselves, only the
items in them. This can be used to make cell items overlap their
neighbors.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **cell\_size** = `Vector3(2, 2, 2)`
`🔗<class_GridMap_property_cell_size>`

classref-property-setget

-   `void (No return value.)` **set\_cell\_size**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_cell\_size**()

The dimensions of the grid's cells.

This does not affect the size of the meshes. See
`cell_scale<class_GridMap_property_cell_scale>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **collision\_layer** = `1`
`🔗<class_GridMap_property_collision_layer>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_layer**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_collision\_layer**()

The physics layers this GridMap is in.

GridMaps act as static bodies, meaning they aren't affected by gravity
or other forces. They only affect other physics bodies that collide with
them.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **collision\_mask** = `1`
`🔗<class_GridMap_property_collision_mask>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_collision\_mask**()

The physics layers this GridMap detects collisions in. See [Collision
layers and
masks](../tutorials/physics/physics_introduction.html#collision-layers-and-masks)
in the documentation for more information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **collision\_priority** = `1.0`
`🔗<class_GridMap_property_collision_priority>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_priority**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_collision\_priority**()

The priority used to solve colliding when occurring penetration. The
higher the priority is, the lower the penetration into the object will
be. This can for example be used to prevent the player from breaking
through the boundaries of a level.

classref-item-separator

------------------------------------------------------------------------

classref-property

`MeshLibrary<class_MeshLibrary>` **mesh\_library**
`🔗<class_GridMap_property_mesh_library>`

classref-property-setget

-   `void (No return value.)` **set\_mesh\_library**(value:
    `MeshLibrary<class_MeshLibrary>`)
-   `MeshLibrary<class_MeshLibrary>` **get\_mesh\_library**()

The assigned `MeshLibrary<class_MeshLibrary>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PhysicsMaterial<class_PhysicsMaterial>` **physics\_material**
`🔗<class_GridMap_property_physics_material>`

classref-property-setget

-   `void (No return value.)` **set\_physics\_material**(value:
    `PhysicsMaterial<class_PhysicsMaterial>`)
-   `PhysicsMaterial<class_PhysicsMaterial>`
    **get\_physics\_material**()

Overrides the default friction and bounce physics properties for the
whole **GridMap**.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **clear**() `🔗<class_GridMap_method_clear>`

Clear all cells.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_baked\_meshes**()
`🔗<class_GridMap_method_clear_baked_meshes>`

Clears all baked meshes. See
`make_baked_meshes<class_GridMap_method_make_baked_meshes>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_bake\_mesh\_instance**(idx: `int<class_int>`)
`🔗<class_GridMap_method_get_bake_mesh_instance>`

Returns `RID<class_RID>` of a baked mesh with the given `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_bake\_meshes**()
`🔗<class_GridMap_method_get_bake_meshes>`

Returns an array of `ArrayMesh<class_ArrayMesh>`es and
`Transform3D<class_Transform3D>` references of all bake meshes that
exist within the current GridMap.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Basis<class_Basis>` **get\_basis\_with\_orthogonal\_index**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_get_basis_with_orthogonal_index>`

Returns one of 24 possible rotations that lie along the vectors (x,y,z)
with each component being either -1, 0, or 1. For further details, refer
to the Godot source code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_cell\_item**(position:
`Vector3i<class_Vector3i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_get_cell_item>`

The `MeshLibrary<class_MeshLibrary>` item index located at the given
grid coordinates. If the cell is empty,
`INVALID_CELL_ITEM<class_GridMap_constant_INVALID_CELL_ITEM>` will be
returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Basis<class_Basis>` **get\_cell\_item\_basis**(position:
`Vector3i<class_Vector3i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_get_cell_item_basis>`

Returns the basis that gives the specified cell its orientation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_cell\_item\_orientation**(position:
`Vector3i<class_Vector3i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_get_cell_item_orientation>`

The orientation of the cell at the given grid coordinates. `-1` is
returned if the cell is empty.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_collision\_layer\_value**(layer\_number:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_get_collision_layer_value>`

Returns whether or not the specified layer of the
`collision_layer<class_GridMap_property_collision_layer>` is enabled,
given a `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_collision\_mask\_value**(layer\_number:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_get_collision_mask_value>`

Returns whether or not the specified layer of the
`collision_mask<class_GridMap_property_collision_mask>` is enabled,
given a `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_meshes**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_get_meshes>`

Returns an array of `Transform3D<class_Transform3D>` and
`Mesh<class_Mesh>` references corresponding to the non-empty cells in
the grid. The transforms are specified in local space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_navigation\_map**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_get_navigation_map>`

Returns the `RID<class_RID>` of the navigation map this GridMap node
uses for its cell baked navigation meshes.

This function returns always the map set on the GridMap node and not the
map on the NavigationServer. If the map is changed directly with the
NavigationServer API the GridMap node will not be aware of the map
change.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_orthogonal\_index\_from\_basis**(basis:
`Basis<class_Basis>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_get_orthogonal_index_from_basis>`

This function considers a discretization of rotations into 24 points on
unit sphere, lying along the vectors (x,y,z) with each component being
either -1, 0, or 1, and returns the index (in the range from 0 to 23) of
the point best representing the orientation of the object. For further
details, refer to the Godot source code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector3i<class_Vector3i>`\]
**get\_used\_cells**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_get_used_cells>`

Returns an array of `Vector3<class_Vector3>` with the non-empty cell
coordinates in the grid map.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector3i<class_Vector3i>`\]
**get\_used\_cells\_by\_item**(item: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_get_used_cells_by_item>`

Returns an array of all cells with the given item index specified in
`item`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3i<class_Vector3i>` **local\_to\_map**(local\_position:
`Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_local_to_map>`

Returns the map coordinates of the cell containing the given
`local_position`. If `local_position` is in global coordinates, consider
using `Node3D.to_local<class_Node3D_method_to_local>` before passing it
to this method. See also
`map_to_local<class_GridMap_method_map_to_local>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **make\_baked\_meshes**(gen\_lightmap\_uv:
`bool<class_bool>` = false, lightmap\_uv\_texel\_size:
`float<class_float>` = 0.1) `🔗<class_GridMap_method_make_baked_meshes>`

Bakes lightmap data for all meshes in the assigned
`MeshLibrary<class_MeshLibrary>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **map\_to\_local**(map\_position:
`Vector3i<class_Vector3i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GridMap_method_map_to_local>`

Returns the position of a grid cell in the GridMap's local coordinate
space. To convert the returned value into global coordinates, use
`Node3D.to_global<class_Node3D_method_to_global>`. See also
`local_to_map<class_GridMap_method_local_to_map>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **resource\_changed**(resource:
`Resource<class_Resource>`) `🔗<class_GridMap_method_resource_changed>`

**Deprecated:** Use `Resource.changed<class_Resource_signal_changed>`
instead.

This method does nothing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_cell\_item**(position:
`Vector3i<class_Vector3i>`, item: `int<class_int>`, orientation:
`int<class_int>` = 0) `🔗<class_GridMap_method_set_cell_item>`

Sets the mesh index for the cell referenced by its grid coordinates.

A negative item index such as
`INVALID_CELL_ITEM<class_GridMap_constant_INVALID_CELL_ITEM>` will clear
the cell.

Optionally, the item's orientation can be passed. For valid orientation
values, see
`get_orthogonal_index_from_basis<class_GridMap_method_get_orthogonal_index_from_basis>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_collision\_layer\_value**(layer\_number: `int<class_int>`, value:
`bool<class_bool>`) `🔗<class_GridMap_method_set_collision_layer_value>`

Based on `value`, enables or disables the specified layer in the
`collision_layer<class_GridMap_property_collision_layer>`, given a
`layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_collision\_mask\_value**(layer\_number:
`int<class_int>`, value: `bool<class_bool>`)
`🔗<class_GridMap_method_set_collision_mask_value>`

Based on `value`, enables or disables the specified layer in the
`collision_mask<class_GridMap_property_collision_mask>`, given a
`layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_navigation\_map**(navigation\_map:
`RID<class_RID>`) `🔗<class_GridMap_method_set_navigation_map>`

Sets the `RID<class_RID>` of the navigation map this GridMap node should
use for its cell baked navigation meshes.
