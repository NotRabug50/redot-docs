github\_url  
hide

# TileMap

**Deprecated:** Use multiple `TileMapLayer<class_TileMapLayer>` nodes
instead. To convert a TileMap to a set of TileMapLayer nodes, open the
TileMap bottom panel with the node selected, click the toolbox icon in
the top-right corner and choose 'Extract TileMap layers as individual
TileMapLayer nodes'.

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Node for 2D tile-based maps.

classref-introduction-group

## Description

Node for 2D tile-based maps. Tilemaps use a `TileSet<class_TileSet>`
which contain a list of tiles which are used to create grid-based maps.
A TileMap may have several layers, layouting tiles on top of each other.

For performance reasons, all TileMap updates are batched at the end of a
frame. Notably, this means that scene tiles from a
`TileSetScenesCollectionSource<class_TileSetScenesCollectionSource>` may
be initialized after their parent. This is only queued when inside the
scene tree.

To force an update earlier on, call
`update_internals<class_TileMap_method_update_internals>`.

classref-introduction-group

## Tutorials

-   `Using Tilemaps <../tutorials/2d/using_tilemaps>`
-   [2D Platformer
    Demo](https://godotengine.org/asset-library/asset/2727)
-   [2D Isometric
    Demo](https://godotengine.org/asset-library/asset/2718)
-   [2D Hexagonal
    Demo](https://godotengine.org/asset-library/asset/2717)
-   [2D Grid-based Navigation with AStarGrid2D
    Demo](https://godotengine.org/asset-library/asset/2723)
-   [2D Role Playing Game (RPG)
    Demo](https://godotengine.org/asset-library/asset/2729)
-   [2D Kinematic Character
    Demo](https://godotengine.org/asset-library/asset/2719)

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

**changed**() `🔗<class_TileMap_signal_changed>`

Emitted when the `TileSet<class_TileSet>` of this TileMap changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **VisibilityMode**: `🔗<enum_TileMap_VisibilityMode>`

classref-enumeration-constant

`VisibilityMode<enum_TileMap_VisibilityMode>`
**VISIBILITY\_MODE\_DEFAULT** = `0`

Use the debug settings to determine visibility.

classref-enumeration-constant

`VisibilityMode<enum_TileMap_VisibilityMode>`
**VISIBILITY\_MODE\_FORCE\_HIDE** = `2`

Always hide.

classref-enumeration-constant

`VisibilityMode<enum_TileMap_VisibilityMode>`
**VISIBILITY\_MODE\_FORCE\_SHOW** = `1`

Always show.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **collision\_animatable** = `false`
`🔗<class_TileMap_property_collision_animatable>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_animatable**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_collision\_animatable**()

If enabled, the TileMap will see its collisions synced to the physics
tick and change its collision type from static to kinematic. This is
required to create TileMap-based moving platform.

\*\*Note:\*\* Enabling
`collision_animatable<class_TileMap_property_collision_animatable>` may
have a small performance impact, only do it if the TileMap is moving and
has colliding tiles.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VisibilityMode<enum_TileMap_VisibilityMode>`
**collision\_visibility\_mode** = `0`
`🔗<class_TileMap_property_collision_visibility_mode>`

classref-property-setget

-   `void (No return value.)`
    **set\_collision\_visibility\_mode**(value:
    `VisibilityMode<enum_TileMap_VisibilityMode>`)
-   `VisibilityMode<enum_TileMap_VisibilityMode>`
    **get\_collision\_visibility\_mode**()

Show or hide the TileMap's collision shapes. If set to
`VISIBILITY_MODE_DEFAULT<class_TileMap_constant_VISIBILITY_MODE_DEFAULT>`,
this depends on the show collision debug settings.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VisibilityMode<enum_TileMap_VisibilityMode>`
**navigation\_visibility\_mode** = `0`
`🔗<class_TileMap_property_navigation_visibility_mode>`

classref-property-setget

-   `void (No return value.)`
    **set\_navigation\_visibility\_mode**(value:
    `VisibilityMode<enum_TileMap_VisibilityMode>`)
-   `VisibilityMode<enum_TileMap_VisibilityMode>`
    **get\_navigation\_visibility\_mode**()

Show or hide the TileMap's navigation meshes. If set to
`VISIBILITY_MODE_DEFAULT<class_TileMap_constant_VISIBILITY_MODE_DEFAULT>`,
this depends on the show navigation debug settings.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **rendering\_quadrant\_size** = `16`
`🔗<class_TileMap_property_rendering_quadrant_size>`

classref-property-setget

-   `void (No return value.)` **set\_rendering\_quadrant\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_rendering\_quadrant\_size**()

The TileMap's quadrant size. A quadrant is a group of tiles to be drawn
together on a single canvas item, for optimization purposes.
`rendering_quadrant_size<class_TileMap_property_rendering_quadrant_size>`
defines the length of a square's side, in the map's coordinate system,
that forms the quadrant. Thus, the default quadrant size groups together
`16 * 16 = 256` tiles.

The quadrant size does not apply on Y-sorted layers, as tiles are
grouped by Y position instead in that case.

\*\*Note:\*\* As quadrants are created according to the map's coordinate
system, the quadrant's "square shape" might not look like square in the
TileMap's local coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TileSet<class_TileSet>` **tile\_set**
`🔗<class_TileMap_property_tile_set>`

classref-property-setget

-   `void (No return value.)` **set\_tileset**(value:
    `TileSet<class_TileSet>`)
-   `TileSet<class_TileSet>` **get\_tileset**()

The `TileSet<class_TileSet>` used by this **TileMap**. The textures,
collisions, and additional behavior of all available tiles are stored
here.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_tile\_data\_runtime\_update**(layer:
`int<class_int>`, coords: `Vector2i<class_Vector2i>`, tile\_data:
`TileData<class_TileData>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TileMap_private_method__tile_data_runtime_update>`

Called with a TileData object about to be used internally by the
TileMap, allowing its modification at runtime.

This method is only called if
`_use_tile_data_runtime_update<class_TileMap_private_method__use_tile_data_runtime_update>`
is implemented and returns `true` for the given tile `coords` and
`layer`.

\*\*Warning:\*\* The `tile_data` object's sub-resources are the same as
the one in the TileSet. Modifying them might impact the whole TileSet.
Instead, make sure to duplicate those resources.

\*\*Note:\*\* If the properties of `tile_data` object should change over
time, use
`notify_runtime_tile_data_update<class_TileMap_method_notify_runtime_tile_data_update>`
to notify the TileMap it needs an update.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_use\_tile\_data\_runtime\_update**(layer:
`int<class_int>`, coords: `Vector2i<class_Vector2i>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TileMap_private_method__use_tile_data_runtime_update>`

Should return `true` if the tile at coordinates `coords` on layer
`layer` requires a runtime update.

\*\*Warning:\*\* Make sure this function only return `true` when needed.
Any tile processed at runtime without a need for it will imply a
significant performance penalty.

\*\*Note:\*\* If the result of this function should changed, use
`notify_runtime_tile_data_update<class_TileMap_method_notify_runtime_tile_data_update>`
to notify the TileMap it needs an update.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_layer**(to\_position: `int<class_int>`)
`🔗<class_TileMap_method_add_layer>`

Adds a layer at the given position `to_position` in the array. If
`to_position` is negative, the position is counted from the end, with
`-1` adding the layer at the end of the array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**() `🔗<class_TileMap_method_clear>`

Clears all cells.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_layer**(layer: `int<class_int>`)
`🔗<class_TileMap_method_clear_layer>`

Clears all cells on the given layer.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase\_cell**(layer: `int<class_int>`,
coords: `Vector2i<class_Vector2i>`)
`🔗<class_TileMap_method_erase_cell>`

Erases the cell on layer `layer` at coordinates `coords`.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fix\_invalid\_tiles**()
`🔗<class_TileMap_method_fix_invalid_tiles>`

Clears cells that do not exist in the tileset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **force\_update**(layer: `int<class_int>` =
-1) `🔗<class_TileMap_method_force_update>`

**Deprecated:** Use
`notify_runtime_tile_data_update<class_TileMap_method_notify_runtime_tile_data_update>`
and/or `update_internals<class_TileMap_method_update_internals>`
instead.

Forces the TileMap and the layer `layer` to update.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_cell\_alternative\_tile**(layer:
`int<class_int>`, coords: `Vector2i<class_Vector2i>`, use\_proxies:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_cell_alternative_tile>`

Returns the tile alternative ID of the cell on layer `layer` at
`coords`.

If `use_proxies` is `false`, ignores the `TileSet<class_TileSet>`'s tile
proxies, returning the raw alternative identifier. See
`TileSet.map_tile_proxy<class_TileSet_method_map_tile_proxy>`.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_cell\_atlas\_coords**(layer:
`int<class_int>`, coords: `Vector2i<class_Vector2i>`, use\_proxies:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_cell_atlas_coords>`

Returns the tile atlas coordinates ID of the cell on layer `layer` at
coordinates `coords`. Returns `Vector2i(-1, -1)` if the cell does not
exist.

If `use_proxies` is `false`, ignores the `TileSet<class_TileSet>`'s tile
proxies, returning the raw atlas coordinate identifier. See
`TileSet.map_tile_proxy<class_TileSet_method_map_tile_proxy>`.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_cell\_source\_id**(layer: `int<class_int>`,
coords: `Vector2i<class_Vector2i>`, use\_proxies: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_cell_source_id>`

Returns the tile source ID of the cell on layer `layer` at coordinates
`coords`. Returns `-1` if the cell does not exist.

If `use_proxies` is `false`, ignores the `TileSet<class_TileSet>`'s tile
proxies, returning the raw source identifier. See
`TileSet.map_tile_proxy<class_TileSet_method_map_tile_proxy>`.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TileData<class_TileData>` **get\_cell\_tile\_data**(layer:
`int<class_int>`, coords: `Vector2i<class_Vector2i>`, use\_proxies:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_cell_tile_data>`

Returns the `TileData<class_TileData>` object associated with the given
cell, or `null` if the cell does not exist or is not a
`TileSetAtlasSource<class_TileSetAtlasSource>`.

If `layer` is negative, the layers are accessed from the last one.

    func get_clicked_tile_power():
        var clicked_cell = tile_map.local_to_map(tile_map.get_local_mouse_position())
        var data = tile_map.get_cell_tile_data(0, clicked_cell)
        if data:
            return data.get_custom_data("power")
        else:
            return 0

If `use_proxies` is `false`, ignores the `TileSet<class_TileSet>`'s tile
proxies. See
`TileSet.map_tile_proxy<class_TileSet_method_map_tile_proxy>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_coords\_for\_body\_rid**(body:
`RID<class_RID>`) `🔗<class_TileMap_method_get_coords_for_body_rid>`

Returns the coordinates of the tile for given physics body RID. Such RID
can be retrieved from
`KinematicCollision2D.get_collider_rid<class_KinematicCollision2D_method_get_collider_rid>`,
when colliding with a tile.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_layer\_for\_body\_rid**(body: `RID<class_RID>`)
`🔗<class_TileMap_method_get_layer_for_body_rid>`

Returns the tilemap layer of the tile for given physics body RID. Such
RID can be retrieved from
`KinematicCollision2D.get_collider_rid<class_KinematicCollision2D_method_get_collider_rid>`,
when colliding with a tile.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_layer\_modulate**(layer: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_layer_modulate>`

Returns a TileMap layer's modulate.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_layer\_name**(layer: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_layer_name>`

Returns a TileMap layer's name.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_layer\_navigation\_map**(layer:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_layer_navigation_map>`

Returns the `RID<class_RID>` of the
`NavigationServer2D<class_NavigationServer2D>` navigation map assigned
to the specified TileMap layer `layer`.

By default the TileMap uses the default `World2D<class_World2D>`
navigation map for the first TileMap layer. For each additional TileMap
layer a new navigation map is created for the additional layer.

In order to make `NavigationAgent2D<class_NavigationAgent2D>` switch
between TileMap layer navigation maps use
`NavigationAgent2D.set_navigation_map<class_NavigationAgent2D_method_set_navigation_map>`
with the navigation map received from
`get_layer_navigation_map<class_TileMap_method_get_layer_navigation_map>`.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_layer\_y\_sort\_origin**(layer:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_layer_y_sort_origin>`

Returns a TileMap layer's Y sort origin.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_layer\_z\_index**(layer: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_layer_z_index>`

Returns a TileMap layer's Z-index value.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_layers\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_layers_count>`

Returns the number of layers in the TileMap.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_navigation\_map**(layer: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_navigation_map>`

**Deprecated:** Use
`get_layer_navigation_map<class_TileMap_method_get_layer_navigation_map>`
instead.

Returns the `RID<class_RID>` of the
`NavigationServer2D<class_NavigationServer2D>` navigation map assigned
to the specified TileMap layer `layer`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_neighbor\_cell**(coords:
`Vector2i<class_Vector2i>`, neighbor:
`CellNeighbor<enum_TileSet_CellNeighbor>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_neighbor_cell>`

Returns the neighboring cell to the one at coordinates `coords`,
identified by the `neighbor` direction. This method takes into account
the different layouts a TileMap can take.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TileMapPattern<class_TileMapPattern>` **get\_pattern**(layer:
`int<class_int>`, coords\_array:
`Array<class_Array>`\[`Vector2i<class_Vector2i>`\])
`🔗<class_TileMap_method_get_pattern>`

Creates a new `TileMapPattern<class_TileMapPattern>` from the given
layer and set of cells.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector2i<class_Vector2i>`\]
**get\_surrounding\_cells**(coords: `Vector2i<class_Vector2i>`)
`🔗<class_TileMap_method_get_surrounding_cells>`

Returns the list of all neighbourings cells to the one at `coords`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector2i<class_Vector2i>`\]
**get\_used\_cells**(layer: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_used_cells>`

Returns a `Vector2i<class_Vector2i>` array with the positions of all
cells containing a tile in the given layer. A cell is considered empty
if its source identifier equals -1, its atlas coordinates identifiers is
`Vector2(-1, -1)` and its alternative identifier is -1.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector2i<class_Vector2i>`\]
**get\_used\_cells\_by\_id**(layer: `int<class_int>`, source\_id:
`int<class_int>` = -1, atlas\_coords: `Vector2i<class_Vector2i>` =
Vector2i(-1, -1), alternative\_tile: `int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_used_cells_by_id>`

Returns a `Vector2i<class_Vector2i>` array with the positions of all
cells containing a tile in the given layer. Tiles may be filtered
according to their source (`source_id`), their atlas coordinates
(`atlas_coords`) or alternative id (`alternative_tile`).

If a parameter has its value set to the default one, this parameter is
not used to filter a cell. Thus, if all parameters have their respective
default value, this method returns the same result as
`get_used_cells<class_TileMap_method_get_used_cells>`.

A cell is considered empty if its source identifier equals -1, its atlas
coordinates identifiers is `Vector2(-1, -1)` and its alternative
identifier is -1.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2i<class_Rect2i>` **get\_used\_rect**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_get_used_rect>`

Returns a rectangle enclosing the used (non-empty) tiles of the map,
including all layers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_cell\_flipped\_h**(layer: `int<class_int>`,
coords: `Vector2i<class_Vector2i>`, use\_proxies: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_is_cell_flipped_h>`

Returns `true` if the cell on layer `layer` at coordinates `coords` is
flipped horizontally. The result is valid only for atlas sources.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_cell\_flipped\_v**(layer: `int<class_int>`,
coords: `Vector2i<class_Vector2i>`, use\_proxies: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_is_cell_flipped_v>`

Returns `true` if the cell on layer `layer` at coordinates `coords` is
flipped vertically. The result is valid only for atlas sources.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_cell\_transposed**(layer: `int<class_int>`,
coords: `Vector2i<class_Vector2i>`, use\_proxies: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_is_cell_transposed>`

Returns `true` if the cell on layer `layer` at coordinates `coords` is
transposed. The result is valid only for atlas sources.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_layer\_enabled**(layer: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_is_layer_enabled>`

Returns if a layer is enabled.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_layer\_navigation\_enabled**(layer:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_is_layer_navigation_enabled>`

Returns if a layer's built-in navigation regions generation is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_layer\_y\_sort\_enabled**(layer:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_is_layer_y_sort_enabled>`

Returns if a layer Y-sorts its tiles.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **local\_to\_map**(local\_position:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_local_to_map>`

Returns the map coordinates of the cell containing the given
`local_position`. If `local_position` is in global coordinates, consider
using `Node2D.to_local<class_Node2D_method_to_local>` before passing it
to this method. See also
`map_to_local<class_TileMap_method_map_to_local>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **map\_pattern**(position\_in\_tilemap:
`Vector2i<class_Vector2i>`, coords\_in\_pattern:
`Vector2i<class_Vector2i>`, pattern:
`TileMapPattern<class_TileMapPattern>`)
`🔗<class_TileMap_method_map_pattern>`

Returns for the given coordinate `coords_in_pattern` in a
`TileMapPattern<class_TileMapPattern>` the corresponding cell
coordinates if the pattern was pasted at the `position_in_tilemap`
coordinates (see `set_pattern<class_TileMap_method_set_pattern>`). This
mapping is required as in half-offset tile shapes, the mapping might not
work by calculating `position_in_tile_map + coords_in_pattern`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **map\_to\_local**(map\_position:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMap_method_map_to_local>`

Returns the centered position of a cell in the TileMap's local
coordinate space. To convert the returned value into global coordinates,
use `Node2D.to_global<class_Node2D_method_to_global>`. See also
`local_to_map<class_TileMap_method_local_to_map>`.

\*\*Note:\*\* This may not correspond to the visual position of the
tile, i.e. it ignores the
`TileData.texture_origin<class_TileData_property_texture_origin>`
property of individual tiles.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_layer**(layer: `int<class_int>`,
to\_position: `int<class_int>`) `🔗<class_TileMap_method_move_layer>`

Moves the layer at index `layer` to the given position `to_position` in
the array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **notify\_runtime\_tile\_data\_update**(layer:
`int<class_int>` = -1)
`🔗<class_TileMap_method_notify_runtime_tile_data_update>`

Notifies the TileMap node that calls to
`_use_tile_data_runtime_update<class_TileMap_private_method__use_tile_data_runtime_update>`
or
`_tile_data_runtime_update<class_TileMap_private_method__tile_data_runtime_update>`
will lead to different results. This will thus trigger a TileMap update.

If `layer` is provided, only notifies changes for the given layer.
Providing the `layer` argument (when applicable) is usually preferred
for performance reasons.

\*\*Warning:\*\* Updating the TileMap is computationally expensive and
may impact performance. Try to limit the number of calls to this
function to avoid unnecessary update.

\*\*Note:\*\* This does not trigger a direct update of the TileMap, the
update will be done at the end of the frame as usual (unless you call
`update_internals<class_TileMap_method_update_internals>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_layer**(layer: `int<class_int>`)
`🔗<class_TileMap_method_remove_layer>`

Removes the layer at index `layer`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_cell**(layer: `int<class_int>`, coords:
`Vector2i<class_Vector2i>`, source\_id: `int<class_int>` = -1,
atlas\_coords: `Vector2i<class_Vector2i>` = Vector2i(-1, -1),
alternative\_tile: `int<class_int>` = 0)
`🔗<class_TileMap_method_set_cell>`

Sets the tile identifiers for the cell on layer `layer` at coordinates
`coords`. Each tile of the `TileSet<class_TileSet>` is identified using
three parts:

-   The source identifier `source_id` identifies a
    `TileSetSource<class_TileSetSource>` identifier. See
    `TileSet.set_source_id<class_TileSet_method_set_source_id>`,
-   The atlas coordinates identifier `atlas_coords` identifies a tile
    coordinates in the atlas (if the source is a
    `TileSetAtlasSource<class_TileSetAtlasSource>`). For
    `TileSetScenesCollectionSource<class_TileSetScenesCollectionSource>`
    it should always be `Vector2i(0, 0)`),
-   The alternative tile identifier `alternative_tile` identifies a tile
    alternative in the atlas (if the source is a
    `TileSetAtlasSource<class_TileSetAtlasSource>`), and the scene for a
    `TileSetScenesCollectionSource<class_TileSetScenesCollectionSource>`.

If `source_id` is set to `-1`, `atlas_coords` to `Vector2i(-1, -1)` or
`alternative_tile` to `-1`, the cell will be erased. An erased cell gets
**all** its identifiers automatically set to their respective invalid
values, namely `-1`, `Vector2i(-1, -1)` and `-1`.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_cells\_terrain\_connect**(layer:
`int<class_int>`, cells:
`Array<class_Array>`\[`Vector2i<class_Vector2i>`\], terrain\_set:
`int<class_int>`, terrain: `int<class_int>`, ignore\_empty\_terrains:
`bool<class_bool>` = true)
`🔗<class_TileMap_method_set_cells_terrain_connect>`

Update all the cells in the `cells` coordinates array so that they use
the given `terrain` for the given `terrain_set`. If an updated cell has
the same terrain as one of its neighboring cells, this function tries to
join the two. This function might update neighboring tiles if needed to
create correct terrain transitions.

If `ignore_empty_terrains` is true, empty terrains will be ignored when
trying to find the best fitting tile for the given terrain constraints.

If `layer` is negative, the layers are accessed from the last one.

\*\*Note:\*\* To work correctly, this method requires the TileMap's
TileSet to have terrains set up with all required terrain combinations.
Otherwise, it may produce unexpected results.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_cells\_terrain\_path**(layer:
`int<class_int>`, path:
`Array<class_Array>`\[`Vector2i<class_Vector2i>`\], terrain\_set:
`int<class_int>`, terrain: `int<class_int>`, ignore\_empty\_terrains:
`bool<class_bool>` = true)
`🔗<class_TileMap_method_set_cells_terrain_path>`

Update all the cells in the `path` coordinates array so that they use
the given `terrain` for the given `terrain_set`. The function will also
connect two successive cell in the path with the same terrain. This
function might update neighboring tiles if needed to create correct
terrain transitions.

If `ignore_empty_terrains` is true, empty terrains will be ignored when
trying to find the best fitting tile for the given terrain constraints.

If `layer` is negative, the layers are accessed from the last one.

\*\*Note:\*\* To work correctly, this method requires the TileMap's
TileSet to have terrains set up with all required terrain combinations.
Otherwise, it may produce unexpected results.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_layer\_enabled**(layer:
`int<class_int>`, enabled: `bool<class_bool>`)
`🔗<class_TileMap_method_set_layer_enabled>`

Enables or disables the layer `layer`. A disabled layer is not processed
at all (no rendering, no physics, etc.).

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_layer\_modulate**(layer:
`int<class_int>`, modulate: `Color<class_Color>`)
`🔗<class_TileMap_method_set_layer_modulate>`

Sets a layer's color. It will be multiplied by tile's color and
TileMap's modulate.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_layer\_name**(layer: `int<class_int>`,
name: `String<class_String>`) `🔗<class_TileMap_method_set_layer_name>`

Sets a layer's name. This is mostly useful in the editor.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_layer\_navigation\_enabled**(layer:
`int<class_int>`, enabled: `bool<class_bool>`)
`🔗<class_TileMap_method_set_layer_navigation_enabled>`

Enables or disables a layer's built-in navigation regions generation.
Disable this if you need to bake navigation regions from a TileMap using
a `NavigationRegion2D<class_NavigationRegion2D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_layer\_navigation\_map**(layer:
`int<class_int>`, map: `RID<class_RID>`)
`🔗<class_TileMap_method_set_layer_navigation_map>`

Assigns `map` as a `NavigationServer2D<class_NavigationServer2D>`
navigation map for the specified TileMap layer `layer`.

By default the TileMap uses the default `World2D<class_World2D>`
navigation map for the first TileMap layer. For each additional TileMap
layer a new navigation map is created for the additional layer.

In order to make `NavigationAgent2D<class_NavigationAgent2D>` switch
between TileMap layer navigation maps use
`NavigationAgent2D.set_navigation_map<class_NavigationAgent2D_method_set_navigation_map>`
with the navigation map received from
`get_layer_navigation_map<class_TileMap_method_get_layer_navigation_map>`.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_layer\_y\_sort\_enabled**(layer:
`int<class_int>`, y\_sort\_enabled: `bool<class_bool>`)
`🔗<class_TileMap_method_set_layer_y_sort_enabled>`

Enables or disables a layer's Y-sorting. If a layer is Y-sorted, the
layer will behave as a CanvasItem node where each of its tile gets
Y-sorted.

Y-sorted layers should usually be on different Z-index values than not
Y-sorted layers, otherwise, each of those layer will be Y-sorted as
whole with the Y-sorted one. This is usually an undesired behavior.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_layer\_y\_sort\_origin**(layer:
`int<class_int>`, y\_sort\_origin: `int<class_int>`)
`🔗<class_TileMap_method_set_layer_y_sort_origin>`

Sets a layer's Y-sort origin value. This Y-sort origin value is added to
each tile's Y-sort origin value.

This allows, for example, to fake a different height level on each
layer. This can be useful for top-down view games.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_layer\_z\_index**(layer:
`int<class_int>`, z\_index: `int<class_int>`)
`🔗<class_TileMap_method_set_layer_z_index>`

Sets a layers Z-index value. This Z-index is added to each tile's
Z-index value.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_navigation\_map**(layer:
`int<class_int>`, map: `RID<class_RID>`)
`🔗<class_TileMap_method_set_navigation_map>`

**Deprecated:** Use
`set_layer_navigation_map<class_TileMap_method_set_layer_navigation_map>`
instead.

Assigns `map` as a `NavigationServer2D<class_NavigationServer2D>`
navigation map for the specified TileMap layer `layer`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_pattern**(layer: `int<class_int>`,
position: `Vector2i<class_Vector2i>`, pattern:
`TileMapPattern<class_TileMapPattern>`)
`🔗<class_TileMap_method_set_pattern>`

Paste the given `TileMapPattern<class_TileMapPattern>` at the given
`position` and `layer` in the tile map.

If `layer` is negative, the layers are accessed from the last one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update\_internals**()
`🔗<class_TileMap_method_update_internals>`

Triggers a direct update of the TileMap. Usually, calling this function
is not needed, as TileMap node updates automatically when one of its
properties or cells is modified.

However, for performance reasons, those updates are batched and delayed
to the end of the frame. Calling this function will force the TileMap to
update right away instead.

\*\*Warning:\*\* Updating the TileMap is computationally expensive and
may impact performance. Try to limit the number of updates and how many
tiles they impact.
