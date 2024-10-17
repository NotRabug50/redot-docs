github\_url  
hide

# TileData

**Inherits:** `Object<class_Object>`

Settings for a single tile in a `TileSet<class_TileSet>`.

classref-introduction-group

## Description

**TileData** object represents a single tile in a
`TileSet<class_TileSet>`. It is usually edited using the tileset editor,
but it can be modified at runtime using
`TileMap._tile_data_runtime_update<class_TileMap_private_method__tile_data_runtime_update>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**changed**() `🔗<class_TileData_signal_changed>`

Emitted when any of the properties are changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **flip\_h** = `false`
`🔗<class_TileData_property_flip_h>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_h**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_flip\_h**()

If `true`, the tile will have its texture flipped horizontally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **flip\_v** = `false`
`🔗<class_TileData_property_flip_v>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_v**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_flip\_v**()

If `true`, the tile will have its texture flipped vertically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Material<class_Material>` **material**
`🔗<class_TileData_property_material>`

classref-property-setget

-   `void (No return value.)` **set\_material**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_material**()

The `Material<class_Material>` to use for this **TileData**. This can be
a `CanvasItemMaterial<class_CanvasItemMaterial>` to use the default
shader, or a `ShaderMaterial<class_ShaderMaterial>` to use a custom
shader.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **modulate** = `Color(1, 1, 1, 1)`
`🔗<class_TileData_property_modulate>`

classref-property-setget

-   `void (No return value.)` **set\_modulate**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_modulate**()

Color modulation of the tile.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **probability** = `1.0`
`🔗<class_TileData_property_probability>`

classref-property-setget

-   `void (No return value.)` **set\_probability**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_probability**()

Relative probability of this tile being selected when drawing a pattern
of random tiles.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **terrain** = `-1`
`🔗<class_TileData_property_terrain>`

classref-property-setget

-   `void (No return value.)` **set\_terrain**(value: `int<class_int>`)
-   `int<class_int>` **get\_terrain**()

ID of the terrain from the terrain set that the tile uses.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **terrain\_set** = `-1`
`🔗<class_TileData_property_terrain_set>`

classref-property-setget

-   `void (No return value.)` **set\_terrain\_set**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_terrain\_set**()

ID of the terrain set that the tile uses.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **texture\_origin** = `Vector2i(0, 0)`
`🔗<class_TileData_property_texture_origin>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_origin**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_texture\_origin**()

Offsets the position of where the tile is drawn.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **transpose** = `false`
`🔗<class_TileData_property_transpose>`

classref-property-setget

-   `void (No return value.)` **set\_transpose**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_transpose**()

If `true`, the tile will display transposed, i.e. with horizontal and
vertical texture UVs swapped.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **y\_sort\_origin** = `0`
`🔗<class_TileData_property_y_sort_origin>`

classref-property-setget

-   `void (No return value.)` **set\_y\_sort\_origin**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_y\_sort\_origin**()

Vertical point of the tile used for determining y-sorted order.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **z\_index** = `0`
`🔗<class_TileData_property_z_index>`

classref-property-setget

-   `void (No return value.)` **set\_z\_index**(value: `int<class_int>`)
-   `int<class_int>` **get\_z\_index**()

Ordering index of this tile, relative to `TileMap<class_TileMap>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_collision\_polygon**(layer\_id:
`int<class_int>`) `🔗<class_TileData_method_add_collision_polygon>`

Adds a collision polygon to the tile on the given TileSet physics layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_occluder\_polygon**(layer\_id:
`int<class_int>`) `🔗<class_TileData_method_add_occluder_polygon>`

Adds an occlusion polygon to the tile on the TileSet occlusion layer
with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>`
**get\_collision\_polygon\_one\_way\_margin**(layer\_id:
`int<class_int>`, polygon\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_collision_polygon_one_way_margin>`

Returns the one-way margin (for one-way platforms) of the polygon at
index `polygon_index` for TileSet physics layer with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**get\_collision\_polygon\_points**(layer\_id: `int<class_int>`,
polygon\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_collision_polygon_points>`

Returns the points of the polygon at index `polygon_index` for TileSet
physics layer with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_collision\_polygons\_count**(layer\_id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_collision_polygons_count>`

Returns how many polygons the tile has for TileSet physics layer with
index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_constant\_angular\_velocity**(layer\_id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_constant_angular_velocity>`

Returns the constant angular velocity applied to objects colliding with
this tile.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_constant\_linear\_velocity**(layer\_id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_constant_linear_velocity>`

Returns the constant linear velocity applied to objects colliding with
this tile.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_custom\_data**(layer\_name:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_custom_data>`

Returns the custom data value for custom data layer named `layer_name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_custom\_data\_by\_layer\_id**(layer\_id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_custom_data_by_layer_id>`

Returns the custom data value for custom data layer with index
`layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NavigationPolygon<class_NavigationPolygon>`
**get\_navigation\_polygon**(layer\_id: `int<class_int>`, flip\_h:
`bool<class_bool>` = false, flip\_v: `bool<class_bool>` = false,
transpose: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_navigation_polygon>`

Returns the navigation polygon of the tile for the TileSet navigation
layer with index `layer_id`.

`flip_h`, `flip_v`, and `transpose` allow transforming the returned
polygon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`OccluderPolygon2D<class_OccluderPolygon2D>`
**get\_occluder**(layer\_id: `int<class_int>`, flip\_h:
`bool<class_bool>` = false, flip\_v: `bool<class_bool>` = false,
transpose: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_occluder>`

**Deprecated:** Use
`get_occluder_polygon<class_TileData_method_get_occluder_polygon>`
instead.

Returns the occluder polygon of the tile for the TileSet occlusion layer
with index `layer_id`.

`flip_h`, `flip_v`, and `transpose` allow transforming the returned
polygon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`OccluderPolygon2D<class_OccluderPolygon2D>`
**get\_occluder\_polygon**(layer\_id: `int<class_int>`, polygon\_index:
`int<class_int>`, flip\_h: `bool<class_bool>` = false, flip\_v:
`bool<class_bool>` = false, transpose: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_occluder_polygon>`

Returns the occluder polygon at index `polygon_index` from the TileSet
occlusion layer with index `layer_id`.

The `flip_h`, `flip_v`, and `transpose` parameters can be `true` to
transform the returned polygon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_occluder\_polygons\_count**(layer\_id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_occluder_polygons_count>`

Returns the number of occluder polygons of the tile in the TileSet
occlusion layer with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_terrain\_peering\_bit**(peering\_bit:
`CellNeighbor<enum_TileSet_CellNeighbor>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_get_terrain_peering_bit>`

Returns the tile's terrain bit for the given `peering_bit` direction. To
check that a direction is valid, use
`is_valid_terrain_peering_bit<class_TileData_method_is_valid_terrain_peering_bit>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_collision\_polygon\_one\_way**(layer\_id:
`int<class_int>`, polygon\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_is_collision_polygon_one_way>`

Returns whether one-way collisions are enabled for the polygon at index
`polygon_index` for TileSet physics layer with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_terrain\_peering\_bit**(peering\_bit:
`CellNeighbor<enum_TileSet_CellNeighbor>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileData_method_is_valid_terrain_peering_bit>`

Returns whether the given `peering_bit` direction is valid for this
tile.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_collision\_polygon**(layer\_id:
`int<class_int>`, polygon\_index: `int<class_int>`)
`🔗<class_TileData_method_remove_collision_polygon>`

Removes the polygon at index `polygon_index` for TileSet physics layer
with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_occluder\_polygon**(layer\_id:
`int<class_int>`, polygon\_index: `int<class_int>`)
`🔗<class_TileData_method_remove_occluder_polygon>`

Removes the polygon at index `polygon_index` for TileSet occlusion layer
with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_collision\_polygon\_one\_way**(layer\_id: `int<class_int>`,
polygon\_index: `int<class_int>`, one\_way: `bool<class_bool>`)
`🔗<class_TileData_method_set_collision_polygon_one_way>`

Enables/disables one-way collisions on the polygon at index
`polygon_index` for TileSet physics layer with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_collision\_polygon\_one\_way\_margin**(layer\_id:
`int<class_int>`, polygon\_index: `int<class_int>`, one\_way\_margin:
`float<class_float>`)
`🔗<class_TileData_method_set_collision_polygon_one_way_margin>`

Sets the one-way margin (for one-way platforms) of the polygon at index
`polygon_index` for TileSet physics layer with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_collision\_polygon\_points**(layer\_id:
`int<class_int>`, polygon\_index: `int<class_int>`, polygon:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_TileData_method_set_collision_polygon_points>`

Sets the points of the polygon at index `polygon_index` for TileSet
physics layer with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_collision\_polygons\_count**(layer\_id:
`int<class_int>`, polygons\_count: `int<class_int>`)
`🔗<class_TileData_method_set_collision_polygons_count>`

Sets the polygons count for TileSet physics layer with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_constant\_angular\_velocity**(layer\_id: `int<class_int>`,
velocity: `float<class_float>`)
`🔗<class_TileData_method_set_constant_angular_velocity>`

Sets the constant angular velocity. This does not rotate the tile. This
angular velocity is applied to objects colliding with this tile.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_constant\_linear\_velocity**(layer\_id:
`int<class_int>`, velocity: `Vector2<class_Vector2>`)
`🔗<class_TileData_method_set_constant_linear_velocity>`

Sets the constant linear velocity. This does not move the tile. This
linear velocity is applied to objects colliding with this tile. This is
useful to create conveyor belts.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_custom\_data**(layer\_name:
`String<class_String>`, value: `Variant<class_Variant>`)
`🔗<class_TileData_method_set_custom_data>`

Sets the tile's custom data value for the TileSet custom data layer with
name `layer_name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_custom\_data\_by\_layer\_id**(layer\_id: `int<class_int>`, value:
`Variant<class_Variant>`)
`🔗<class_TileData_method_set_custom_data_by_layer_id>`

Sets the tile's custom data value for the TileSet custom data layer with
index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_navigation\_polygon**(layer\_id:
`int<class_int>`, navigation\_polygon:
`NavigationPolygon<class_NavigationPolygon>`)
`🔗<class_TileData_method_set_navigation_polygon>`

Sets the navigation polygon for the TileSet navigation layer with index
`layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_occluder**(layer\_id: `int<class_int>`,
occluder\_polygon: `OccluderPolygon2D<class_OccluderPolygon2D>`)
`🔗<class_TileData_method_set_occluder>`

**Deprecated:** Use
`set_occluder_polygon<class_TileData_method_set_occluder_polygon>`
instead.

Sets the occluder for the TileSet occlusion layer with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_occluder\_polygon**(layer\_id:
`int<class_int>`, polygon\_index: `int<class_int>`, polygon:
`OccluderPolygon2D<class_OccluderPolygon2D>`)
`🔗<class_TileData_method_set_occluder_polygon>`

Sets the occluder for polygon with index `polygon_index` in the TileSet
occlusion layer with index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_occluder\_polygons\_count**(layer\_id:
`int<class_int>`, polygons\_count: `int<class_int>`)
`🔗<class_TileData_method_set_occluder_polygons_count>`

Sets the occluder polygon count in the TileSet occlusion layer with
index `layer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_terrain\_peering\_bit**(peering\_bit:
`CellNeighbor<enum_TileSet_CellNeighbor>`, terrain: `int<class_int>`)
`🔗<class_TileData_method_set_terrain_peering_bit>`

Sets the tile's terrain bit for the given `peering_bit` direction. To
check that a direction is valid, use
`is_valid_terrain_peering_bit<class_TileData_method_is_valid_terrain_peering_bit>`.
