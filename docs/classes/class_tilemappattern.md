github\_url  
hide

# TileMapPattern

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Holds a pattern to be copied from or pasted into
`TileMap<class_TileMap>`s.

classref-introduction-group

## Description

This resource holds a set of cells to help bulk manipulations of
`TileMap<class_TileMap>`.

A pattern always start at the `(0,0)` coordinates and cannot have cells
with negative coordinates.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_cell\_alternative\_tile**(coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMapPattern_method_get_cell_alternative_tile>`

Returns the tile alternative ID of the cell at `coords`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_cell\_atlas\_coords**(coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMapPattern_method_get_cell_atlas_coords>`

Returns the tile atlas coordinates ID of the cell at `coords`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_cell\_source\_id**(coords:
`Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMapPattern_method_get_cell_source_id>`

Returns the tile source ID of the cell at `coords`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMapPattern_method_get_size>`

Returns the size, in cells, of the pattern.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector2i<class_Vector2i>`\]
**get\_used\_cells**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMapPattern_method_get_used_cells>`

Returns the list of used cell coordinates in the pattern.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_cell**(coords: `Vector2i<class_Vector2i>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMapPattern_method_has_cell>`

Returns whether the pattern has a tile at the given coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_empty**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TileMapPattern_method_is_empty>`

Returns whether the pattern is empty or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_cell**(coords:
`Vector2i<class_Vector2i>`, update\_size: `bool<class_bool>`)
`🔗<class_TileMapPattern_method_remove_cell>`

Remove the cell at the given coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_cell**(coords:
`Vector2i<class_Vector2i>`, source\_id: `int<class_int>` = -1,
atlas\_coords: `Vector2i<class_Vector2i>` = Vector2i(-1, -1),
alternative\_tile: `int<class_int>` = -1)
`🔗<class_TileMapPattern_method_set_cell>`

Sets the tile identifiers for the cell at coordinates `coords`. See
`TileMap.set_cell<class_TileMap_method_set_cell>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_size**(size:
`Vector2i<class_Vector2i>`) `🔗<class_TileMapPattern_method_set_size>`

Sets the size of the pattern.
