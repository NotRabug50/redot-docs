github\_url  
hide

# TileSetAtlasSource

**Inherits:** `TileSetSource<class_TileSetSource>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Exposes a 2D atlas texture as a set of tiles for a
`TileSet<class_TileSet>` resource.

classref-introduction-group

## Description

An atlas is a grid of tiles laid out on a texture. Each tile in the grid
must be exposed using
`create_tile<class_TileSetAtlasSource_method_create_tile>`. Those tiles
are then indexed using their coordinates in the grid.

Each tile can also have a size in the grid coordinates, making it more
or less cells in the atlas.

Alternatives version of a tile can be created using
`create_alternative_tile<class_TileSetAtlasSource_method_create_alternative_tile>`,
which are then indexed using an alternative ID. The main tile (the one
in the grid), is accessed with an alternative ID equal to 0.

Each tile alternate has a set of properties that is defined by the
source's `TileSet<class_TileSet>` layers. Those properties are stored in
a TileData object that can be accessed and modified using
`get_tile_data<class_TileSetAtlasSource_method_get_tile_data>`.

As TileData properties are stored directly in the TileSetAtlasSource
resource, their properties might also be set using
`TileSetAtlasSource.set("<coords_x>:<coords_y>/<alternative_id>/<tile_data_property>")`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **TileAnimationMode**:
`🔗<enum_TileSetAtlasSource_TileAnimationMode>`

classref-enumeration-constant

`TileAnimationMode<enum_TileSetAtlasSource_TileAnimationMode>`
**TILE\_ANIMATION\_MODE\_DEFAULT** = `0`

Tile animations start at same time, looking identical.

classref-enumeration-constant

`TileAnimationMode<enum_TileSetAtlasSource_TileAnimationMode>`
**TILE\_ANIMATION\_MODE\_RANDOM\_START\_TIMES** = `1`

Tile animations start at random times, looking varied.

classref-enumeration-constant

`TileAnimationMode<enum_TileSetAtlasSource_TileAnimationMode>`
**TILE\_ANIMATION\_MODE\_MAX** = `2`

Represents the size of the
`TileAnimationMode<enum_TileSetAtlasSource_TileAnimationMode>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**TRANSFORM\_FLIP\_H** = `4096`
`🔗<class_TileSetAtlasSource_constant_TRANSFORM_FLIP_H>`

Represents cell's horizontal flip flag. Should be used directly with
`TileMap<class_TileMap>` to flip placed tiles by altering their
alternative IDs.

    var alternate_id = $TileMap.get_cell_alternative_tile(0, Vector2i(2, 2))
    if not alternate_id & TileSetAtlasSource.TRANSFORM_FLIP_H:
        # If tile is not already flipped, flip it.
        $TileMap.set_cell(0, Vector2i(2, 2), source_id, atlas_coords, alternate_id | TileSetAtlasSource.TRANSFORM_FLIP_H)

\*\*Note:\*\* These transformations can be combined to do the equivalent
of 0, 90, 180, and 270 degree rotations, as shown below:

    enum TileTransform {
        ROTATE_0 = 0,
        ROTATE_90 = TileSetAtlasSource.TRANSFORM_TRANSPOSE | TileSetAtlasSource.TRANSFORM_FLIP_H,
        ROTATE_180 = TileSetAtlasSource.TRANSFORM_FLIP_H | TileSetAtlasSource.TRANSFORM_FLIP_V,
        ROTATE_270 = TileSetAtlasSource.TRANSFORM_TRANSPOSE | TileSetAtlasSource.TRANSFORM_FLIP_V,
    }

classref-constant

**TRANSFORM\_FLIP\_V** = `8192`
`🔗<class_TileSetAtlasSource_constant_TRANSFORM_FLIP_V>`

Represents cell's vertical flip flag. See
`TRANSFORM_FLIP_H<class_TileSetAtlasSource_constant_TRANSFORM_FLIP_H>`
for usage.

classref-constant

**TRANSFORM\_TRANSPOSE** = `16384`
`🔗<class_TileSetAtlasSource_constant_TRANSFORM_TRANSPOSE>`

Represents cell's transposed flag. See
`TRANSFORM_FLIP_H<class_TileSetAtlasSource_constant_TRANSFORM_FLIP_H>`
for usage.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Vector2i<class_Vector2i>` **margins** = `Vector2i(0, 0)`
`🔗<class_TileSetAtlasSource_property_margins>`

classref-property-setget

-   `void (No return value.)` **set\_margins**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_margins**()

Margins, in pixels, to offset the origin of the grid in the texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **separation** = `Vector2i(0, 0)`
`🔗<class_TileSetAtlasSource_property_separation>`

classref-property-setget

-   `void (No return value.)` **set\_separation**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_separation**()

Separation, in pixels, between each tile texture region of the grid.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture**
`🔗<class_TileSetAtlasSource_property_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**()

The atlas texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **texture\_region\_size** =
`Vector2i(16, 16)`
`🔗<class_TileSetAtlasSource_property_texture_region_size>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_region\_size**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_texture\_region\_size**()

The base tile size in the texture (in pixel). This size must be bigger
than the TileSet's `tile_size` value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_texture\_padding** = `true`
`🔗<class_TileSetAtlasSource_property_use_texture_padding>`

classref-property-setget

-   `void (No return value.)` **set\_use\_texture\_padding**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_use\_texture\_padding**()

If `true`, generates an internal texture with an additional one pixel
padding around each tile. Texture padding avoids a common artifact where
lines appear between tiles.

Disabling this setting might lead a small performance improvement, as
generating the internal texture requires both memory and processing time
when the TileSetAtlasSource resource is modified.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **clear\_tiles\_outside\_texture**()
`🔗<class_TileSetAtlasSource_method_clear_tiles_outside_texture>`

Removes all tiles that don't fit the available texture area. This method
iterates over all the source's tiles, so it's advised to use
`has_tiles_outside_texture<class_TileSetAtlasSource_method_has_tiles_outside_texture>`
beforehand.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **create\_alternative\_tile**(atlas\_coords:
`Vector2i<class_Vector2i>`, alternative\_id\_override: `int<class_int>`
= -1) `🔗<class_TileSetAtlasSource_method_create_alternative_tile>`

Creates an alternative tile for the tile at coordinates `atlas_coords`.
If `alternative_id_override` is -1, give it an automatically generated
unique ID, or assigns it the given ID otherwise.

Returns the new alternative identifier, or -1 if the alternative could
not be created with a provided `alternative_id_override`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **create\_tile**(atlas\_coords:
`Vector2i<class_Vector2i>`, size: `Vector2i<class_Vector2i>` =
Vector2i(1, 1)) `🔗<class_TileSetAtlasSource_method_create_tile>`

Creates a new tile at coordinates `atlas_coords` with the given `size`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_atlas\_grid\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_atlas_grid_size>`

Returns the atlas grid size, which depends on how many tiles can fit in
the texture. It thus depends on the
`texture<class_TileSetAtlasSource_property_texture>`'s size, the atlas
`margins<class_TileSetAtlasSource_property_margins>`, and the tiles'
`texture_region_size<class_TileSetAtlasSource_property_texture_region_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_next\_alternative\_tile\_id**(atlas\_coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_next_alternative_tile_id>`

Returns the alternative ID a following call to
`create_alternative_tile<class_TileSetAtlasSource_method_create_alternative_tile>`
would return.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_runtime\_texture**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_runtime_texture>`

If
`use_texture_padding<class_TileSetAtlasSource_property_use_texture_padding>`
is `false`, returns
`texture<class_TileSetAtlasSource_property_texture>`. Otherwise, returns
and internal `ImageTexture<class_ImageTexture>` created that includes
the padding.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2i<class_Rect2i>`
**get\_runtime\_tile\_texture\_region**(atlas\_coords:
`Vector2i<class_Vector2i>`, frame: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_runtime_tile_texture_region>`

Returns the region of the tile at coordinates `atlas_coords` for the
given `frame` inside the texture returned by
`get_runtime_texture<class_TileSetAtlasSource_method_get_runtime_texture>`.

\*\*Note:\*\* If
`use_texture_padding<class_TileSetAtlasSource_property_use_texture_padding>`
is `false`, returns the same as
`get_tile_texture_region<class_TileSetAtlasSource_method_get_tile_texture_region>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_tile\_animation\_columns**(atlas\_coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_tile_animation_columns>`

Returns how many columns the tile at `atlas_coords` has in its animation
layout.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>`
**get\_tile\_animation\_frame\_duration**(atlas\_coords:
`Vector2i<class_Vector2i>`, frame\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_tile_animation_frame_duration>`

Returns the animation frame duration of frame `frame_index` for the tile
at coordinates `atlas_coords`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_tile\_animation\_frames\_count**(atlas\_coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_tile_animation_frames_count>`

Returns how many animation frames has the tile at coordinates
`atlas_coords`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TileAnimationMode<enum_TileSetAtlasSource_TileAnimationMode>`
**get\_tile\_animation\_mode**(atlas\_coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_tile_animation_mode>`

Returns the tile animation mode of the tile at `atlas_coords`. See also
`set_tile_animation_mode<class_TileSetAtlasSource_method_set_tile_animation_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>`
**get\_tile\_animation\_separation**(atlas\_coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_tile_animation_separation>`

Returns the separation (as in the atlas grid) between each frame of an
animated tile at coordinates `atlas_coords`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_tile\_animation\_speed**(atlas\_coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_tile_animation_speed>`

Returns the animation speed of the tile at coordinates `atlas_coords`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>`
**get\_tile\_animation\_total\_duration**(atlas\_coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_tile_animation_total_duration>`

Returns the sum of the sum of the frame durations of the tile at
coordinates `atlas_coords`. This value needs to be divided by the
animation speed to get the actual animation loop duration.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_tile\_at\_coords**(atlas\_coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_tile_at_coords>`

If there is a tile covering the `atlas_coords` coordinates, returns the
top-left coordinates of the tile (thus its coordinate ID). Returns
`Vector2i(-1, -1)` otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TileData<class_TileData>` **get\_tile\_data**(atlas\_coords:
`Vector2i<class_Vector2i>`, alternative\_tile: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_tile_data>`

Returns the `TileData<class_TileData>` object for the given atlas
coordinates and alternative ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_tile\_size\_in\_atlas**(atlas\_coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_tile_size_in_atlas>`

Returns the size of the tile (in the grid coordinates system) at
coordinates `atlas_coords`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2i<class_Rect2i>` **get\_tile\_texture\_region**(atlas\_coords:
`Vector2i<class_Vector2i>`, frame: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_get_tile_texture_region>`

Returns a tile's texture region in the atlas texture. For animated
tiles, a `frame` argument might be provided for the different frames of
the animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**get\_tiles\_to\_be\_removed\_on\_change**(texture:
`Texture2D<class_Texture2D>`, margins: `Vector2i<class_Vector2i>`,
separation: `Vector2i<class_Vector2i>`, texture\_region\_size:
`Vector2i<class_Vector2i>`)
`🔗<class_TileSetAtlasSource_method_get_tiles_to_be_removed_on_change>`

Returns an array of tiles coordinates ID that will be automatically
removed when modifying one or several of those properties: `texture`,
`margins`, `separation` or `texture_region_size`. This can be used to
undo changes that would have caused tiles data loss.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_room\_for\_tile**(atlas\_coords:
`Vector2i<class_Vector2i>`, size: `Vector2i<class_Vector2i>`,
animation\_columns: `int<class_int>`, animation\_separation:
`Vector2i<class_Vector2i>`, frames\_count: `int<class_int>`,
ignored\_tile: `Vector2i<class_Vector2i>` = Vector2i(-1, -1))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_has_room_for_tile>`

Returns whether there is enough room in an atlas to create/modify a tile
with the given properties. If `ignored_tile` is provided, act as is the
given tile was not present in the atlas. This may be used when you want
to modify a tile's properties.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_tiles\_outside\_texture**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetAtlasSource_method_has_tiles_outside_texture>`

Checks if the source has any tiles that don't fit the texture area
(either partially or completely).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_tile\_in\_atlas**(atlas\_coords:
`Vector2i<class_Vector2i>`, new\_atlas\_coords:
`Vector2i<class_Vector2i>` = Vector2i(-1, -1), new\_size:
`Vector2i<class_Vector2i>` = Vector2i(-1, -1))
`🔗<class_TileSetAtlasSource_method_move_tile_in_atlas>`

Move the tile and its alternatives at the `atlas_coords` coordinates to
the `new_atlas_coords` coordinates with the `new_size` size. This
functions will fail if a tile is already present in the given area.

If `new_atlas_coords` is `Vector2i(-1, -1)`, keeps the tile's
coordinates. If `new_size` is `Vector2i(-1, -1)`, keeps the tile's size.

To avoid an error, first check if a move is possible using
`has_room_for_tile<class_TileSetAtlasSource_method_has_room_for_tile>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_alternative\_tile**(atlas\_coords:
`Vector2i<class_Vector2i>`, alternative\_tile: `int<class_int>`)
`🔗<class_TileSetAtlasSource_method_remove_alternative_tile>`

Remove a tile's alternative with alternative ID `alternative_tile`.

Calling this function with `alternative_tile` equals to 0 will fail, as
the base tile alternative cannot be removed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_tile**(atlas\_coords:
`Vector2i<class_Vector2i>`)
`🔗<class_TileSetAtlasSource_method_remove_tile>`

Remove a tile and its alternative at coordinates `atlas_coords`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_alternative\_tile\_id**(atlas\_coords:
`Vector2i<class_Vector2i>`, alternative\_tile: `int<class_int>`,
new\_id: `int<class_int>`)
`🔗<class_TileSetAtlasSource_method_set_alternative_tile_id>`

Change a tile's alternative ID from `alternative_tile` to `new_id`.

Calling this function with `new_id` of 0 will fail, as the base tile
alternative cannot be moved.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_tile\_animation\_columns**(atlas\_coords:
`Vector2i<class_Vector2i>`, frame\_columns: `int<class_int>`)
`🔗<class_TileSetAtlasSource_method_set_tile_animation_columns>`

Sets the number of columns in the animation layout of the tile at
coordinates `atlas_coords`. If set to 0, then the different frames of
the animation are laid out as a single horizontal line in the atlas.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_tile\_animation\_frame\_duration**(atlas\_coords:
`Vector2i<class_Vector2i>`, frame\_index: `int<class_int>`, duration:
`float<class_float>`)
`🔗<class_TileSetAtlasSource_method_set_tile_animation_frame_duration>`

Sets the animation frame `duration` of frame `frame_index` for the tile
at coordinates `atlas_coords`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_tile\_animation\_frames\_count**(atlas\_coords:
`Vector2i<class_Vector2i>`, frames\_count: `int<class_int>`)
`🔗<class_TileSetAtlasSource_method_set_tile_animation_frames_count>`

Sets how many animation frames the tile at coordinates `atlas_coords`
has.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tile\_animation\_mode**(atlas\_coords:
`Vector2i<class_Vector2i>`, mode:
`TileAnimationMode<enum_TileSetAtlasSource_TileAnimationMode>`)
`🔗<class_TileSetAtlasSource_method_set_tile_animation_mode>`

Sets the tile animation mode of the tile at `atlas_coords` to `mode`.
See also
`get_tile_animation_mode<class_TileSetAtlasSource_method_get_tile_animation_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_tile\_animation\_separation**(atlas\_coords:
`Vector2i<class_Vector2i>`, separation: `Vector2i<class_Vector2i>`)
`🔗<class_TileSetAtlasSource_method_set_tile_animation_separation>`

Sets the margin (in grid tiles) between each tile in the animation
layout of the tile at coordinates `atlas_coords` has.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tile\_animation\_speed**(atlas\_coords:
`Vector2i<class_Vector2i>`, speed: `float<class_float>`)
`🔗<class_TileSetAtlasSource_method_set_tile_animation_speed>`

Sets the animation speed of the tile at coordinates `atlas_coords` has.
