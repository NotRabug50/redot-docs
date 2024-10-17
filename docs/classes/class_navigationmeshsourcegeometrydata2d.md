github\_url  
hide

# NavigationMeshSourceGeometryData2D

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Container for parsed source geometry data used in navigation mesh
baking.

classref-introduction-group

## Description

Container for parsed source geometry data used in navigation mesh
baking.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_obstruction\_outline**(shape\_outline:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_NavigationMeshSourceGeometryData2D_method_add_obstruction_outline>`

Adds the outline points of a shape as obstructed area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_projected\_obstruction**(vertices:
`PackedVector2Array<class_PackedVector2Array>`, carve:
`bool<class_bool>`)
`🔗<class_NavigationMeshSourceGeometryData2D_method_add_projected_obstruction>`

Adds a projected obstruction shape to the source geometry. If `carve` is
`true` the carved shape will not be affected by additional offsets (e.g.
agent radius) of the navigation mesh baking process.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_traversable\_outline**(shape\_outline:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_NavigationMeshSourceGeometryData2D_method_add_traversable_outline>`

Adds the outline points of a shape as traversable area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**append\_obstruction\_outlines**(obstruction\_outlines:
`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\])
`🔗<class_NavigationMeshSourceGeometryData2D_method_append_obstruction_outlines>`

Appends another array of `obstruction_outlines` at the end of the
existing obstruction outlines array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**append\_traversable\_outlines**(traversable\_outlines:
`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\])
`🔗<class_NavigationMeshSourceGeometryData2D_method_append_traversable_outlines>`

Appends another array of `traversable_outlines` at the end of the
existing traversable outlines array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_NavigationMeshSourceGeometryData2D_method_clear>`

Clears the internal data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_projected\_obstructions**()
`🔗<class_NavigationMeshSourceGeometryData2D_method_clear_projected_obstructions>`

Clears all projected obstructions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_bounds**()
`🔗<class_NavigationMeshSourceGeometryData2D_method_get_bounds>`

Returns an axis-aligned bounding box that covers all the stored geometry
data. The bounds are calculated when calling this function with the
result cached until further geometry changes are made.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\]
**get\_obstruction\_outlines**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationMeshSourceGeometryData2D_method_get_obstruction_outlines>`

Returns all the obstructed area outlines arrays.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_projected\_obstructions**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationMeshSourceGeometryData2D_method_get_projected_obstructions>`

Returns the projected obstructions as an `Array<class_Array>` of
dictionaries. Each `Dictionary<class_Dictionary>` contains the following
entries:

-   `vertices` - A `PackedFloat32Array<class_PackedFloat32Array>` that
    defines the outline points of the projected shape.
-   `carve` - A `bool<class_bool>` that defines how the projected shape
    affects the navigation mesh baking. If `true` the projected shape
    will not be affected by addition offsets, e.g. agent radius.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\]
**get\_traversable\_outlines**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationMeshSourceGeometryData2D_method_get_traversable_outlines>`

Returns all the traversable area outlines arrays.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_data**()
`🔗<class_NavigationMeshSourceGeometryData2D_method_has_data>`

Returns `true` when parsed source geometry data exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **merge**(other\_geometry:
`NavigationMeshSourceGeometryData2D<class_NavigationMeshSourceGeometryData2D>`)
`🔗<class_NavigationMeshSourceGeometryData2D_method_merge>`

Adds the geometry data of another **NavigationMeshSourceGeometryData2D**
to the navigation mesh baking data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_obstruction\_outlines**(obstruction\_outlines:
`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\])
`🔗<class_NavigationMeshSourceGeometryData2D_method_set_obstruction_outlines>`

Sets all the obstructed area outlines arrays.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_projected\_obstructions**(projected\_obstructions:
`Array<class_Array>`)
`🔗<class_NavigationMeshSourceGeometryData2D_method_set_projected_obstructions>`

Sets the projected obstructions with an Array of Dictionaries with the
following key value pairs:

gdscript

"vertices" : PackedFloat32Array "carve" : bool

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_traversable\_outlines**(traversable\_outlines:
`Array<class_Array>`\[`PackedVector2Array<class_PackedVector2Array>`\])
`🔗<class_NavigationMeshSourceGeometryData2D_method_set_traversable_outlines>`

Sets all the traversable area outlines arrays.
