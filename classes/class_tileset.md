github\_url  
hide

# TileSet

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Tile library for tilemaps.

classref-introduction-group

## Description

A TileSet is a library of tiles for a `TileMap<class_TileMap>`. A
TileSet handles a list of `TileSetSource<class_TileSetSource>`, each of
them storing a set of tiles.

Tiles can either be from a
`TileSetAtlasSource<class_TileSetAtlasSource>`, which renders tiles out
of a texture with support for physics, navigation, etc., or from a
`TileSetScenesCollectionSource<class_TileSetScenesCollectionSource>`,
which exposes scene-based tiles.

Tiles are referenced by using three IDs: their source ID, their atlas
coordinates ID, and their alternative tile ID.

A TileSet can be configured so that its tiles expose more or fewer
properties. To do so, the TileSet resources use property layers, which
you can add or remove depending on your needs.

For example, adding a physics layer allows giving collision shapes to
your tiles. Each layer has dedicated properties (physics layer and
mask), so you may add several TileSet physics layers for each type of
collision you need.

See the functions to add new layers for more information.

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

enum **TileShape**: `🔗<enum_TileSet_TileShape>`

classref-enumeration-constant

`TileShape<enum_TileSet_TileShape>` **TILE\_SHAPE\_SQUARE** = `0`

Rectangular tile shape.

classref-enumeration-constant

`TileShape<enum_TileSet_TileShape>` **TILE\_SHAPE\_ISOMETRIC** = `1`

Diamond tile shape (for isometric look).

\*\*Note:\*\* Isometric **TileSet** works best if
`TileMap<class_TileMap>` and all its layers have Y-sort enabled.

classref-enumeration-constant

`TileShape<enum_TileSet_TileShape>`
**TILE\_SHAPE\_HALF\_OFFSET\_SQUARE** = `2`

Rectangular tile shape with one row/column out of two offset by half a
tile.

classref-enumeration-constant

`TileShape<enum_TileSet_TileShape>` **TILE\_SHAPE\_HEXAGON** = `3`

Hexagonal tile shape.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TileLayout**: `🔗<enum_TileSet_TileLayout>`

classref-enumeration-constant

`TileLayout<enum_TileSet_TileLayout>` **TILE\_LAYOUT\_STACKED** = `0`

Tile coordinates layout where both axis stay consistent with their
respective local horizontal and vertical axis.

classref-enumeration-constant

`TileLayout<enum_TileSet_TileLayout>` **TILE\_LAYOUT\_STACKED\_OFFSET**
= `1`

Same as
`TILE_LAYOUT_STACKED<class_TileSet_constant_TILE_LAYOUT_STACKED>`, but
the first half-offset is negative instead of positive.

classref-enumeration-constant

`TileLayout<enum_TileSet_TileLayout>` **TILE\_LAYOUT\_STAIRS\_RIGHT** =
`2`

Tile coordinates layout where the horizontal axis stay horizontal, and
the vertical one goes down-right.

classref-enumeration-constant

`TileLayout<enum_TileSet_TileLayout>` **TILE\_LAYOUT\_STAIRS\_DOWN** =
`3`

Tile coordinates layout where the vertical axis stay vertical, and the
horizontal one goes down-right.

classref-enumeration-constant

`TileLayout<enum_TileSet_TileLayout>` **TILE\_LAYOUT\_DIAMOND\_RIGHT** =
`4`

Tile coordinates layout where the horizontal axis goes up-right, and the
vertical one goes down-right.

classref-enumeration-constant

`TileLayout<enum_TileSet_TileLayout>` **TILE\_LAYOUT\_DIAMOND\_DOWN** =
`5`

Tile coordinates layout where the horizontal axis goes down-right, and
the vertical one goes down-left.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TileOffsetAxis**: `🔗<enum_TileSet_TileOffsetAxis>`

classref-enumeration-constant

`TileOffsetAxis<enum_TileSet_TileOffsetAxis>`
**TILE\_OFFSET\_AXIS\_HORIZONTAL** = `0`

Horizontal half-offset.

classref-enumeration-constant

`TileOffsetAxis<enum_TileSet_TileOffsetAxis>`
**TILE\_OFFSET\_AXIS\_VERTICAL** = `1`

Vertical half-offset.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CellNeighbor**: `🔗<enum_TileSet_CellNeighbor>`

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_RIGHT\_SIDE** = `0`

Neighbor on the right side.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_RIGHT\_CORNER** = `1`

Neighbor in the right corner.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_BOTTOM\_RIGHT\_SIDE** = `2`

Neighbor on the bottom right side.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_BOTTOM\_RIGHT\_CORNER** = `3`

Neighbor in the bottom right corner.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_BOTTOM\_SIDE** = `4`

Neighbor on the bottom side.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_BOTTOM\_CORNER** = `5`

Neighbor in the bottom corner.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_BOTTOM\_LEFT\_SIDE** = `6`

Neighbor on the bottom left side.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_BOTTOM\_LEFT\_CORNER** = `7`

Neighbor in the bottom left corner.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>` **CELL\_NEIGHBOR\_LEFT\_SIDE**
= `8`

Neighbor on the left side.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_LEFT\_CORNER** = `9`

Neighbor in the left corner.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_TOP\_LEFT\_SIDE** = `10`

Neighbor on the top left side.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_TOP\_LEFT\_CORNER** = `11`

Neighbor in the top left corner.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>` **CELL\_NEIGHBOR\_TOP\_SIDE**
= `12`

Neighbor on the top side.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_TOP\_CORNER** = `13`

Neighbor in the top corner.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_TOP\_RIGHT\_SIDE** = `14`

Neighbor on the top right side.

classref-enumeration-constant

`CellNeighbor<enum_TileSet_CellNeighbor>`
**CELL\_NEIGHBOR\_TOP\_RIGHT\_CORNER** = `15`

Neighbor in the top right corner.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TerrainMode**: `🔗<enum_TileSet_TerrainMode>`

classref-enumeration-constant

`TerrainMode<enum_TileSet_TerrainMode>`
**TERRAIN\_MODE\_MATCH\_CORNERS\_AND\_SIDES** = `0`

Requires both corners and side to match with neighboring tiles'
terrains.

classref-enumeration-constant

`TerrainMode<enum_TileSet_TerrainMode>`
**TERRAIN\_MODE\_MATCH\_CORNERS** = `1`

Requires corners to match with neighboring tiles' terrains.

classref-enumeration-constant

`TerrainMode<enum_TileSet_TerrainMode>` **TERRAIN\_MODE\_MATCH\_SIDES**
= `2`

Requires sides to match with neighboring tiles' terrains.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`TileLayout<enum_TileSet_TileLayout>` **tile\_layout** = `0`
`🔗<class_TileSet_property_tile_layout>`

classref-property-setget

-   `void (No return value.)` **set\_tile\_layout**(value:
    `TileLayout<enum_TileSet_TileLayout>`)
-   `TileLayout<enum_TileSet_TileLayout>` **get\_tile\_layout**()

For all half-offset shapes (Isometric, Hexagonal and Half-Offset
square), changes the way tiles are indexed in the TileMap grid.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TileOffsetAxis<enum_TileSet_TileOffsetAxis>` **tile\_offset\_axis** =
`0` `🔗<class_TileSet_property_tile_offset_axis>`

classref-property-setget

-   `void (No return value.)` **set\_tile\_offset\_axis**(value:
    `TileOffsetAxis<enum_TileSet_TileOffsetAxis>`)
-   `TileOffsetAxis<enum_TileSet_TileOffsetAxis>`
    **get\_tile\_offset\_axis**()

For all half-offset shapes (Isometric, Hexagonal and Half-Offset
square), determines the offset axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TileShape<enum_TileSet_TileShape>` **tile\_shape** = `0`
`🔗<class_TileSet_property_tile_shape>`

classref-property-setget

-   `void (No return value.)` **set\_tile\_shape**(value:
    `TileShape<enum_TileSet_TileShape>`)
-   `TileShape<enum_TileSet_TileShape>` **get\_tile\_shape**()

The tile shape.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **tile\_size** = `Vector2i(16, 16)`
`🔗<class_TileSet_property_tile_size>`

classref-property-setget

-   `void (No return value.)` **set\_tile\_size**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_tile\_size**()

The tile size, in pixels. For all tile shapes, this size corresponds to
the encompassing rectangle of the tile shape. This is thus the minimal
cell size required in an atlas.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **uv\_clipping** = `false`
`🔗<class_TileSet_property_uv_clipping>`

classref-property-setget

-   `void (No return value.)` **set\_uv\_clipping**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_uv\_clipping**()

Enables/Disable uv clipping when rendering the tiles.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_custom\_data\_layer**(to\_position:
`int<class_int>` = -1) `🔗<class_TileSet_method_add_custom_data_layer>`

Adds a custom data layer to the TileSet at the given position
`to_position` in the array. If `to_position` is -1, adds it at the end
of the array.

Custom data layers allow assigning custom properties to atlas tiles.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_navigation\_layer**(to\_position:
`int<class_int>` = -1) `🔗<class_TileSet_method_add_navigation_layer>`

Adds a navigation layer to the TileSet at the given position
`to_position` in the array. If `to_position` is -1, adds it at the end
of the array.

Navigation layers allow assigning a navigable area to atlas tiles.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_occlusion\_layer**(to\_position:
`int<class_int>` = -1) `🔗<class_TileSet_method_add_occlusion_layer>`

Adds an occlusion layer to the TileSet at the given position
`to_position` in the array. If `to_position` is -1, adds it at the end
of the array.

Occlusion layers allow assigning occlusion polygons to atlas tiles.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **add\_pattern**(pattern:
`TileMapPattern<class_TileMapPattern>`, index: `int<class_int>` = -1)
`🔗<class_TileSet_method_add_pattern>`

Adds a `TileMapPattern<class_TileMapPattern>` to be stored in the
TileSet resource. If provided, insert it at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_physics\_layer**(to\_position:
`int<class_int>` = -1) `🔗<class_TileSet_method_add_physics_layer>`

Adds a physics layer to the TileSet at the given position `to_position`
in the array. If `to_position` is -1, adds it at the end of the array.

Physics layers allow assigning collision polygons to atlas tiles.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **add\_source**(source:
`TileSetSource<class_TileSetSource>`, atlas\_source\_id\_override:
`int<class_int>` = -1) `🔗<class_TileSet_method_add_source>`

Adds a `TileSetSource<class_TileSetSource>` to the TileSet. If
`atlas_source_id_override` is not -1, also set its source ID. Otherwise,
a unique identifier is automatically generated.

The function returns the added source ID or -1 if the source could not
be added.

\*\*Warning:\*\* A source cannot belong to two TileSets at the same
time. If the added source was attached to another **TileSet**, it will
be removed from that one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_terrain**(terrain\_set:
`int<class_int>`, to\_position: `int<class_int>` = -1)
`🔗<class_TileSet_method_add_terrain>`

Adds a new terrain to the given terrain set `terrain_set` at the given
position `to_position` in the array. If `to_position` is -1, adds it at
the end of the array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_terrain\_set**(to\_position:
`int<class_int>` = -1) `🔗<class_TileSet_method_add_terrain_set>`

Adds a new terrain set at the given position `to_position` in the array.
If `to_position` is -1, adds it at the end of the array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **cleanup\_invalid\_tile\_proxies**()
`🔗<class_TileSet_method_cleanup_invalid_tile_proxies>`

Clears tile proxies pointing to invalid tiles.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_tile\_proxies**()
`🔗<class_TileSet_method_clear_tile_proxies>`

Clears all tile proxies.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`
**get\_alternative\_level\_tile\_proxy**(source\_from: `int<class_int>`,
coords\_from: `Vector2i<class_Vector2i>`, alternative\_from:
`int<class_int>`)
`🔗<class_TileSet_method_get_alternative_level_tile_proxy>`

Returns the alternative-level proxy for the given identifiers. The
returned array contains the three proxie's target identifiers (source
ID, atlas coords ID and alternative tile ID).

If the TileSet has no proxy for the given identifiers, returns an empty
Array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_coords\_level\_tile\_proxy**(source\_from:
`int<class_int>`, coords\_from: `Vector2i<class_Vector2i>`)
`🔗<class_TileSet_method_get_coords_level_tile_proxy>`

Returns the coordinate-level proxy for the given identifiers. The
returned array contains the two target identifiers of the proxy (source
ID and atlas coordinates ID).

If the TileSet has no proxy for the given identifiers, returns an empty
Array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_custom\_data\_layer\_by\_name**(layer\_name:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_custom_data_layer_by_name>`

Returns the index of the custom data layer identified by the given name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_custom\_data\_layer\_name**(layer\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_custom_data_layer_name>`

Returns the name of the custom data layer identified by the given index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant.Type<enum_@GlobalScope_Variant.Type>`
**get\_custom\_data\_layer\_type**(layer\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_custom_data_layer_type>`

Returns the type of the custom data layer identified by the given index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_custom\_data\_layers\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_custom_data_layers_count>`

Returns the custom data layers count.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**get\_navigation\_layer\_layer\_value**(layer\_index: `int<class_int>`,
layer\_number: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_navigation_layer_layer_value>`

Returns whether or not the specified navigation layer of the TileSet
navigation data layer identified by the given `layer_index` is enabled,
given a navigation\_layers `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_navigation\_layer\_layers**(layer\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_navigation_layer_layers>`

Returns the navigation layers (as in the Navigation server) of the given
TileSet navigation layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_navigation\_layers\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_navigation_layers_count>`

Returns the navigation layers count.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_next\_source\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_next_source_id>`

Returns a new unused source ID. This generated ID is the same that a
call to `add_source<class_TileSet_method_add_source>` would return.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_occlusion\_layer\_light\_mask**(layer\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_occlusion_layer_light_mask>`

Returns the light mask of the occlusion layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**get\_occlusion\_layer\_sdf\_collision**(layer\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_occlusion_layer_sdf_collision>`

Returns if the occluders from this layer use `sdf_collision`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_occlusion\_layers\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_occlusion_layers_count>`

Returns the occlusion layers count.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TileMapPattern<class_TileMapPattern>` **get\_pattern**(index:
`int<class_int>` = -1) `🔗<class_TileSet_method_get_pattern>`

Returns the `TileMapPattern<class_TileMapPattern>` at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_patterns\_count**()
`🔗<class_TileSet_method_get_patterns_count>`

Returns the number of `TileMapPattern<class_TileMapPattern>` this tile
set handles.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_physics\_layer\_collision\_layer**(layer\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_physics_layer_collision_layer>`

Returns the collision layer (as in the physics server) bodies on the
given TileSet's physics layer are in.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_physics\_layer\_collision\_mask**(layer\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_physics_layer_collision_mask>`

Returns the collision mask of bodies on the given TileSet's physics
layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PhysicsMaterial<class_PhysicsMaterial>`
**get\_physics\_layer\_physics\_material**(layer\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_physics_layer_physics_material>`

Returns the physics material of bodies on the given TileSet's physics
layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_physics\_layers\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_physics_layers_count>`

Returns the physics layers count.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TileSetSource<class_TileSetSource>` **get\_source**(source\_id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_source>`

Returns the `TileSetSource<class_TileSetSource>` with ID `source_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_source\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_source_count>`

Returns the number of `TileSetSource<class_TileSetSource>` in this
TileSet.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_source\_id**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_source_id>`

Returns the source ID for source with index `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_source\_level\_tile\_proxy**(source\_from:
`int<class_int>`) `🔗<class_TileSet_method_get_source_level_tile_proxy>`

Returns the source-level proxy for the given source identifier.

If the TileSet has no proxy for the given identifier, returns -1.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_terrain\_color**(terrain\_set:
`int<class_int>`, terrain\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_terrain_color>`

Returns a terrain's color.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_terrain\_name**(terrain\_set:
`int<class_int>`, terrain\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_terrain_name>`

Returns a terrain's name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TerrainMode<enum_TileSet_TerrainMode>`
**get\_terrain\_set\_mode**(terrain\_set: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_terrain_set_mode>`

Returns a terrain set mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_terrain\_sets\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_terrain_sets_count>`

Returns the terrain sets count.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_terrains\_count**(terrain\_set:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_get_terrains_count>`

Returns the number of terrains in the given terrain set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**has\_alternative\_level\_tile\_proxy**(source\_from: `int<class_int>`,
coords\_from: `Vector2i<class_Vector2i>`, alternative\_from:
`int<class_int>`)
`🔗<class_TileSet_method_has_alternative_level_tile_proxy>`

Returns if there is an alternative-level proxy for the given
identifiers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_coords\_level\_tile\_proxy**(source\_from:
`int<class_int>`, coords\_from: `Vector2i<class_Vector2i>`)
`🔗<class_TileSet_method_has_coords_level_tile_proxy>`

Returns if there is a coodinates-level proxy for the given identifiers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_source**(source\_id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_has_source>`

Returns if this TileSet has a source for the given source ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_source\_level\_tile\_proxy**(source\_from:
`int<class_int>`) `🔗<class_TileSet_method_has_source_level_tile_proxy>`

Returns if there is a source-level proxy for the given source ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **map\_tile\_proxy**(source\_from:
`int<class_int>`, coords\_from: `Vector2i<class_Vector2i>`,
alternative\_from: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSet_method_map_tile_proxy>`

According to the configured proxies, maps the provided identifiers to a
new set of identifiers. The source ID, atlas coordinates ID and
alternative tile ID are returned as a 3 elements Array.

This function first look for matching alternative-level proxies, then
coordinates-level proxies, then source-level proxies.

If no proxy corresponding to provided identifiers are found, returns the
same values the ones used as arguments.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_custom\_data\_layer**(layer\_index:
`int<class_int>`, to\_position: `int<class_int>`)
`🔗<class_TileSet_method_move_custom_data_layer>`

Moves the custom data layer at index `layer_index` to the given position
`to_position` in the array. Also updates the atlas tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_navigation\_layer**(layer\_index:
`int<class_int>`, to\_position: `int<class_int>`)
`🔗<class_TileSet_method_move_navigation_layer>`

Moves the navigation layer at index `layer_index` to the given position
`to_position` in the array. Also updates the atlas tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_occlusion\_layer**(layer\_index:
`int<class_int>`, to\_position: `int<class_int>`)
`🔗<class_TileSet_method_move_occlusion_layer>`

Moves the occlusion layer at index `layer_index` to the given position
`to_position` in the array. Also updates the atlas tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_physics\_layer**(layer\_index:
`int<class_int>`, to\_position: `int<class_int>`)
`🔗<class_TileSet_method_move_physics_layer>`

Moves the physics layer at index `layer_index` to the given position
`to_position` in the array. Also updates the atlas tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_terrain**(terrain\_set:
`int<class_int>`, terrain\_index: `int<class_int>`, to\_position:
`int<class_int>`) `🔗<class_TileSet_method_move_terrain>`

Moves the terrain at index `terrain_index` for terrain set `terrain_set`
to the given position `to_position` in the array. Also updates the atlas
tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_terrain\_set**(terrain\_set:
`int<class_int>`, to\_position: `int<class_int>`)
`🔗<class_TileSet_method_move_terrain_set>`

Moves the terrain set at index `terrain_set` to the given position
`to_position` in the array. Also updates the atlas tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_alternative\_level\_tile\_proxy**(source\_from:
`int<class_int>`, coords\_from: `Vector2i<class_Vector2i>`,
alternative\_from: `int<class_int>`)
`🔗<class_TileSet_method_remove_alternative_level_tile_proxy>`

Removes an alternative-level proxy for the given identifiers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_coords\_level\_tile\_proxy**(source\_from: `int<class_int>`,
coords\_from: `Vector2i<class_Vector2i>`)
`🔗<class_TileSet_method_remove_coords_level_tile_proxy>`

Removes a coordinates-level proxy for the given identifiers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_custom\_data\_layer**(layer\_index:
`int<class_int>`) `🔗<class_TileSet_method_remove_custom_data_layer>`

Removes the custom data layer at index `layer_index`. Also updates the
atlas tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_navigation\_layer**(layer\_index:
`int<class_int>`) `🔗<class_TileSet_method_remove_navigation_layer>`

Removes the navigation layer at index `layer_index`. Also updates the
atlas tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_occlusion\_layer**(layer\_index:
`int<class_int>`) `🔗<class_TileSet_method_remove_occlusion_layer>`

Removes the occlusion layer at index `layer_index`. Also updates the
atlas tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_pattern**(index: `int<class_int>`)
`🔗<class_TileSet_method_remove_pattern>`

Remove the `TileMapPattern<class_TileMapPattern>` at the given index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_physics\_layer**(layer\_index:
`int<class_int>`) `🔗<class_TileSet_method_remove_physics_layer>`

Removes the physics layer at index `layer_index`. Also updates the atlas
tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_source**(source\_id:
`int<class_int>`) `🔗<class_TileSet_method_remove_source>`

Removes the source with the given source ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_source\_level\_tile\_proxy**(source\_from: `int<class_int>`)
`🔗<class_TileSet_method_remove_source_level_tile_proxy>`

Removes a source-level tile proxy.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_terrain**(terrain\_set:
`int<class_int>`, terrain\_index: `int<class_int>`)
`🔗<class_TileSet_method_remove_terrain>`

Removes the terrain at index `terrain_index` in the given terrain set
`terrain_set`. Also updates the atlas tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_terrain\_set**(terrain\_set:
`int<class_int>`) `🔗<class_TileSet_method_remove_terrain_set>`

Removes the terrain set at index `terrain_set`. Also updates the atlas
tiles accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_alternative\_level\_tile\_proxy**(source\_from: `int<class_int>`,
coords\_from: `Vector2i<class_Vector2i>`, alternative\_from:
`int<class_int>`, source\_to: `int<class_int>`, coords\_to:
`Vector2i<class_Vector2i>`, alternative\_to: `int<class_int>`)
`🔗<class_TileSet_method_set_alternative_level_tile_proxy>`

Create an alternative-level proxy for the given identifiers. A proxy
will map set of tile identifiers to another set of identifiers.

This can be used to replace a tile in all TileMaps using this TileSet,
as TileMap nodes will find and use the proxy's target tile when one is
available.

Proxied tiles can be automatically replaced in TileMap nodes using the
editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_coords\_level\_tile\_proxy**(p\_source\_from: `int<class_int>`,
coords\_from: `Vector2i<class_Vector2i>`, source\_to: `int<class_int>`,
coords\_to: `Vector2i<class_Vector2i>`)
`🔗<class_TileSet_method_set_coords_level_tile_proxy>`

Creates a coordinates-level proxy for the given identifiers. A proxy
will map set of tile identifiers to another set of identifiers. The
alternative tile ID is kept the same when using coordinates-level
proxies.

This can be used to replace a tile in all TileMaps using this TileSet,
as TileMap nodes will find and use the proxy's target tile when one is
available.

Proxied tiles can be automatically replaced in TileMap nodes using the
editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_custom\_data\_layer\_name**(layer\_index: `int<class_int>`,
layer\_name: `String<class_String>`)
`🔗<class_TileSet_method_set_custom_data_layer_name>`

Sets the name of the custom data layer identified by the given index.
Names are identifiers of the layer therefore if the name is already
taken it will fail and raise an error.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_custom\_data\_layer\_type**(layer\_index: `int<class_int>`,
layer\_type: `Variant.Type<enum_@GlobalScope_Variant.Type>`)
`🔗<class_TileSet_method_set_custom_data_layer_type>`

Sets the type of the custom data layer identified by the given index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_navigation\_layer\_layer\_value**(layer\_index: `int<class_int>`,
layer\_number: `int<class_int>`, value: `bool<class_bool>`)
`🔗<class_TileSet_method_set_navigation_layer_layer_value>`

Based on `value`, enables or disables the specified navigation layer of
the TileSet navigation data layer identified by the given `layer_index`,
given a navigation\_layers `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_navigation\_layer\_layers**(layer\_index: `int<class_int>`,
layers: `int<class_int>`)
`🔗<class_TileSet_method_set_navigation_layer_layers>`

Sets the navigation layers (as in the navigation server) for navigation
regions in the given TileSet navigation layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_occlusion\_layer\_light\_mask**(layer\_index: `int<class_int>`,
light\_mask: `int<class_int>`)
`🔗<class_TileSet_method_set_occlusion_layer_light_mask>`

Sets the occlusion layer (as in the rendering server) for occluders in
the given TileSet occlusion layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_occlusion\_layer\_sdf\_collision**(layer\_index:
`int<class_int>`, sdf\_collision: `bool<class_bool>`)
`🔗<class_TileSet_method_set_occlusion_layer_sdf_collision>`

Enables or disables SDF collision for occluders in the given TileSet
occlusion layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_physics\_layer\_collision\_layer**(layer\_index:
`int<class_int>`, layer: `int<class_int>`)
`🔗<class_TileSet_method_set_physics_layer_collision_layer>`

Sets the physics layer (as in the physics server) for bodies in the
given TileSet physics layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_physics\_layer\_collision\_mask**(layer\_index: `int<class_int>`,
mask: `int<class_int>`)
`🔗<class_TileSet_method_set_physics_layer_collision_mask>`

Sets the physics layer (as in the physics server) for bodies in the
given TileSet physics layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_physics\_layer\_physics\_material**(layer\_index:
`int<class_int>`, physics\_material:
`PhysicsMaterial<class_PhysicsMaterial>`)
`🔗<class_TileSet_method_set_physics_layer_physics_material>`

Sets the physics material for bodies in the given TileSet physics layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_source\_id**(source\_id:
`int<class_int>`, new\_source\_id: `int<class_int>`)
`🔗<class_TileSet_method_set_source_id>`

Changes a source's ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_source\_level\_tile\_proxy**(source\_from: `int<class_int>`,
source\_to: `int<class_int>`)
`🔗<class_TileSet_method_set_source_level_tile_proxy>`

Creates a source-level proxy for the given source ID. A proxy will map
set of tile identifiers to another set of identifiers. Both the atlas
coordinates ID and the alternative tile ID are kept the same when using
source-level proxies.

This can be used to replace a source in all TileMaps using this TileSet,
as TileMap nodes will find and use the proxy's target source when one is
available.

Proxied tiles can be automatically replaced in TileMap nodes using the
editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_terrain\_color**(terrain\_set:
`int<class_int>`, terrain\_index: `int<class_int>`, color:
`Color<class_Color>`) `🔗<class_TileSet_method_set_terrain_color>`

Sets a terrain's color. This color is used for identifying the different
terrains in the TileSet editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_terrain\_name**(terrain\_set:
`int<class_int>`, terrain\_index: `int<class_int>`, name:
`String<class_String>`) `🔗<class_TileSet_method_set_terrain_name>`

Sets a terrain's name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_terrain\_set\_mode**(terrain\_set:
`int<class_int>`, mode: `TerrainMode<enum_TileSet_TerrainMode>`)
`🔗<class_TileSet_method_set_terrain_set_mode>`

Sets a terrain mode. Each mode determines which bits of a tile shape is
used to match the neighboring tiles' terrains.
