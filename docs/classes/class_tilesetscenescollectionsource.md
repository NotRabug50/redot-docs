github\_url  
hide

# TileSetScenesCollectionSource

**Inherits:** `TileSetSource<class_TileSetSource>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Exposes a set of scenes as tiles for a `TileSet<class_TileSet>`
resource.

classref-introduction-group

## Description

When placed on a `TileMap<class_TileMap>`, tiles from
**TileSetScenesCollectionSource** will automatically instantiate an
associated scene at the cell's position in the TileMap.

Scenes are instantiated as children of the `TileMap<class_TileMap>` when
it enters the tree. If you add/remove a scene tile in the
`TileMap<class_TileMap>` that is already inside the tree, the
`TileMap<class_TileMap>` will automatically instantiate/free the scene
accordingly.

\*\*Note:\*\* Scene tiles all occupy one tile slot and instead use
alternate tile ID to identify scene index.
`TileSetSource.get_tiles_count<class_TileSetSource_method_get_tiles_count>`
will always return `1`. Use
`get_scene_tiles_count<class_TileSetScenesCollectionSource_method_get_scene_tiles_count>`
to get a number of scenes in a **TileSetScenesCollectionSource**.

Use this code if you want to find the scene path at a given tile in
`TileMapLayer<class_TileMapLayer>`:

gdscript

var source\_id = tile\_map\_layer.get\_cell\_source\_id(Vector2i(x, y))
if source\_id &gt; -1: var scene\_source =
tile\_map\_layer.tile\_set.get\_source(source\_id) if scene\_source is
TileSetScenesCollectionSource: var alt\_id =
tile\_map\_layer.get\_cell\_alternative\_tile(Vector2i(x, y)) \# The
assigned PackedScene. var scene =
scene\_source.get\_scene\_tile\_scene(alt\_id)

csharp

int sourceId = tileMapLayer.GetCellSourceId(new Vector2I(x, y)); if
(sourceId &gt; -1) { TileSetSource source =
tileMapLayer.TileSet.GetSource(sourceId); if (source is
TileSetScenesCollectionSource sceneSource) { int altId =
tileMapLayer.GetCellAlternativeTile(new Vector2I(x, y)); // The assigned
PackedScene. PackedScene scene = sceneSource.GetSceneTileScene(altId); }
}

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **create\_scene\_tile**(packed\_scene:
`PackedScene<class_PackedScene>`, id\_override: `int<class_int>` = -1)
`🔗<class_TileSetScenesCollectionSource_method_create_scene_tile>`

Creates a scene-based tile out of the given scene.

Returns a newly generated unique ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_next\_scene\_tile\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetScenesCollectionSource_method_get_next_scene_tile_id>`

Returns the scene ID a following call to
`create_scene_tile<class_TileSetScenesCollectionSource_method_create_scene_tile>`
would return.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_scene\_tile\_display\_placeholder**(id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetScenesCollectionSource_method_get_scene_tile_display_placeholder>`

Returns whether the scene tile with `id` displays a placeholder in the
editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_scene\_tile\_id**(index: `int<class_int>`)
`🔗<class_TileSetScenesCollectionSource_method_get_scene_tile_id>`

Returns the scene tile ID of the scene tile at `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedScene<class_PackedScene>` **get\_scene\_tile\_scene**(id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileSetScenesCollectionSource_method_get_scene_tile_scene>`

Returns the `PackedScene<class_PackedScene>` resource of scene tile with
`id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_scene\_tiles\_count**()
`🔗<class_TileSetScenesCollectionSource_method_get_scene_tiles_count>`

Returns the number or scene tiles this TileSet source has.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_scene\_tile\_id**(id: `int<class_int>`)
`🔗<class_TileSetScenesCollectionSource_method_has_scene_tile_id>`

Returns whether this TileSet source has a scene tile with `id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_scene\_tile**(id: `int<class_int>`)
`🔗<class_TileSetScenesCollectionSource_method_remove_scene_tile>`

Remove the scene tile with `id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_scene\_tile\_display\_placeholder**(id:
`int<class_int>`, display\_placeholder: `bool<class_bool>`)
`🔗<class_TileSetScenesCollectionSource_method_set_scene_tile_display_placeholder>`

Sets whether or not the scene tile with `id` should display a
placeholder in the editor. This might be useful for scenes that are not
visible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_scene\_tile\_id**(id: `int<class_int>`,
new\_id: `int<class_int>`)
`🔗<class_TileSetScenesCollectionSource_method_set_scene_tile_id>`

Changes a scene tile's ID from `id` to `new_id`. This will fail if there
is already a tile with an ID equal to `new_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_scene\_tile\_scene**(id:
`int<class_int>`, packed\_scene: `PackedScene<class_PackedScene>`)
`🔗<class_TileSetScenesCollectionSource_method_set_scene_tile_scene>`

Assigns a `PackedScene<class_PackedScene>` resource to the scene tile
with `id`. This will fail if the scene does not extend CanvasItem, as
positioning properties are needed to place the scene on the TileMap.
