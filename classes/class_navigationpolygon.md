github\_url  
hide

# NavigationPolygon

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A 2D navigation mesh that describes a traversable surface for
pathfinding.

classref-introduction-group

## Description

A navigation mesh can be created either by baking it with the help of
the `NavigationServer2D<class_NavigationServer2D>`, or by adding
vertices and convex polygon indices arrays manually.

To bake a navigation mesh at least one outline needs to be added that
defines the outer bounds of the baked area.

gdscript

var new\_navigation\_mesh = NavigationPolygon.new() var
bounding\_outline = PackedVector2Array(\[Vector2(0, 0), Vector2(0, 50),
Vector2(50, 50), Vector2(50, 0)\])
new\_navigation\_mesh.add\_outline(bounding\_outline)
NavigationServer2D.bake\_from\_source\_geometry\_data(new\_navigation\_mesh,
NavigationMeshSourceGeometryData2D.new());
$NavigationRegion2D.navigation\_polygon = new\_navigation\_mesh

csharp

var newNavigationMesh = new NavigationPolygon(); var boundingOutline =
new Vector2\[\] { new Vector2(0, 0), new Vector2(0, 50), new Vector2(50,
50), new Vector2(50, 0) };
newNavigationMesh.AddOutline(boundingOutline);
NavigationServer2D.BakeFromSourceGeometryData(newNavigationMesh, new
NavigationMeshSourceGeometryData2D());
GetNode&lt;NavigationRegion2D&gt;("NavigationRegion2D").NavigationPolygon
= newNavigationMesh;

Adding vertices and polygon indices manually.

gdscript

var new\_navigation\_mesh = NavigationPolygon.new() var new\_vertices =
PackedVector2Array(\[Vector2(0, 0), Vector2(0, 50), Vector2(50, 50),
Vector2(50, 0)\]) new\_navigation\_mesh.vertices = new\_vertices var
new\_polygon\_indices = PackedInt32Array(\[0, 1, 2, 3\])
new\_navigation\_mesh.add\_polygon(new\_polygon\_indices)
$NavigationRegion2D.navigation\_polygon = new\_navigation\_mesh

csharp

var newNavigationMesh = new NavigationPolygon(); var newVertices = new
Vector2\[\] { new Vector2(0, 0), new Vector2(0, 50), new Vector2(50,
50), new Vector2(50, 0) }; newNavigationMesh.Vertices = newVertices; var
newPolygonIndices = new int\[\] { 0, 1, 2, 3 };
newNavigationMesh.AddPolygon(newPolygonIndices);
GetNode&lt;NavigationRegion2D&gt;("NavigationRegion2D").NavigationPolygon
= newNavigationMesh;

classref-introduction-group

## Tutorials

-   `Using NavigationMeshes <../tutorials/navigation/navigation_using_navigationmeshes>`
-   [Navigation Polygon 2D
    Demo](https://godotengine.org/asset-library/asset/2722)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **SamplePartitionType**:
`🔗<enum_NavigationPolygon_SamplePartitionType>`

classref-enumeration-constant

`SamplePartitionType<enum_NavigationPolygon_SamplePartitionType>`
**SAMPLE\_PARTITION\_CONVEX\_PARTITION** = `0`

Convex partitioning that yields navigation mesh with convex polygons.

classref-enumeration-constant

`SamplePartitionType<enum_NavigationPolygon_SamplePartitionType>`
**SAMPLE\_PARTITION\_TRIANGULATE** = `1`

Triangulation partitioning that yields navigation mesh with triangle
polygons.

classref-enumeration-constant

`SamplePartitionType<enum_NavigationPolygon_SamplePartitionType>`
**SAMPLE\_PARTITION\_MAX** = `2`

Represents the size of the
`SamplePartitionType<enum_NavigationPolygon_SamplePartitionType>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ParsedGeometryType**:
`🔗<enum_NavigationPolygon_ParsedGeometryType>`

classref-enumeration-constant

`ParsedGeometryType<enum_NavigationPolygon_ParsedGeometryType>`
**PARSED\_GEOMETRY\_MESH\_INSTANCES** = `0`

Parses mesh instances as obstruction geometry. This includes
`Polygon2D<class_Polygon2D>`, `MeshInstance2D<class_MeshInstance2D>`,
`MultiMeshInstance2D<class_MultiMeshInstance2D>`, and
`TileMap<class_TileMap>` nodes.

Meshes are only parsed when they use a 2D vertices surface format.

classref-enumeration-constant

`ParsedGeometryType<enum_NavigationPolygon_ParsedGeometryType>`
**PARSED\_GEOMETRY\_STATIC\_COLLIDERS** = `1`

Parses `StaticBody2D<class_StaticBody2D>` and `TileMap<class_TileMap>`
colliders as obstruction geometry. The collider should be in any of the
layers specified by
`parsed_collision_mask<class_NavigationPolygon_property_parsed_collision_mask>`.

classref-enumeration-constant

`ParsedGeometryType<enum_NavigationPolygon_ParsedGeometryType>`
**PARSED\_GEOMETRY\_BOTH** = `2`

Both
`PARSED_GEOMETRY_MESH_INSTANCES<class_NavigationPolygon_constant_PARSED_GEOMETRY_MESH_INSTANCES>`
and
`PARSED_GEOMETRY_STATIC_COLLIDERS<class_NavigationPolygon_constant_PARSED_GEOMETRY_STATIC_COLLIDERS>`.

classref-enumeration-constant

`ParsedGeometryType<enum_NavigationPolygon_ParsedGeometryType>`
**PARSED\_GEOMETRY\_MAX** = `3`

Represents the size of the
`ParsedGeometryType<enum_NavigationPolygon_ParsedGeometryType>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SourceGeometryMode**:
`🔗<enum_NavigationPolygon_SourceGeometryMode>`

classref-enumeration-constant

`SourceGeometryMode<enum_NavigationPolygon_SourceGeometryMode>`
**SOURCE\_GEOMETRY\_ROOT\_NODE\_CHILDREN** = `0`

Scans the child nodes of the root node recursively for geometry.

classref-enumeration-constant

`SourceGeometryMode<enum_NavigationPolygon_SourceGeometryMode>`
**SOURCE\_GEOMETRY\_GROUPS\_WITH\_CHILDREN** = `1`

Scans nodes in a group and their child nodes recursively for geometry.
The group is specified by
`source_geometry_group_name<class_NavigationPolygon_property_source_geometry_group_name>`.

classref-enumeration-constant

`SourceGeometryMode<enum_NavigationPolygon_SourceGeometryMode>`
**SOURCE\_GEOMETRY\_GROUPS\_EXPLICIT** = `2`

Uses nodes in a group for geometry. The group is specified by
`source_geometry_group_name<class_NavigationPolygon_property_source_geometry_group_name>`.

classref-enumeration-constant

`SourceGeometryMode<enum_NavigationPolygon_SourceGeometryMode>`
**SOURCE\_GEOMETRY\_MAX** = `3`

Represents the size of the
`SourceGeometryMode<enum_NavigationPolygon_SourceGeometryMode>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **agent\_radius** = `10.0`
`🔗<class_NavigationPolygon_property_agent_radius>`

classref-property-setget

-   `void (No return value.)` **set\_agent\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_agent\_radius**()

The distance to erode/shrink the walkable surface when baking the
navigation mesh.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Rect2<class_Rect2>` **baking\_rect** = `Rect2(0, 0, 0, 0)`
`🔗<class_NavigationPolygon_property_baking_rect>`

classref-property-setget

-   `void (No return value.)` **set\_baking\_rect**(value:
    `Rect2<class_Rect2>`)
-   `Rect2<class_Rect2>` **get\_baking\_rect**()

If the baking `Rect2<class_Rect2>` has an area the navigation mesh
baking will be restricted to its enclosing area.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **baking\_rect\_offset** = `Vector2(0, 0)`
`🔗<class_NavigationPolygon_property_baking_rect_offset>`

classref-property-setget

-   `void (No return value.)` **set\_baking\_rect\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_baking\_rect\_offset**()

The position offset applied to the
`baking_rect<class_NavigationPolygon_property_baking_rect>`
`Rect2<class_Rect2>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **border\_size** = `0.0`
`🔗<class_NavigationPolygon_property_border_size>`

classref-property-setget

-   `void (No return value.)` **set\_border\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_border\_size**()

The size of the non-navigable border around the bake bounding area
defined by the
`baking_rect<class_NavigationPolygon_property_baking_rect>`
`Rect2<class_Rect2>`.

In conjunction with the
`baking_rect<class_NavigationPolygon_property_baking_rect>` the border
size can be used to bake tile aligned navigation meshes without the tile
edges being shrunk by
`agent_radius<class_NavigationPolygon_property_agent_radius>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **cell\_size** = `1.0`
`🔗<class_NavigationPolygon_property_cell_size>`

classref-property-setget

-   `void (No return value.)` **set\_cell\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_cell\_size**()

The cell size used to rasterize the navigation mesh vertices. Must match
with the cell size on the navigation map.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **parsed\_collision\_mask** = `4294967295`
`🔗<class_NavigationPolygon_property_parsed_collision_mask>`

classref-property-setget

-   `void (No return value.)` **set\_parsed\_collision\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_parsed\_collision\_mask**()

The physics layers to scan for static colliders.

Only used when
`parsed_geometry_type<class_NavigationPolygon_property_parsed_geometry_type>`
is
`PARSED_GEOMETRY_STATIC_COLLIDERS<class_NavigationPolygon_constant_PARSED_GEOMETRY_STATIC_COLLIDERS>`
or
`PARSED_GEOMETRY_BOTH<class_NavigationPolygon_constant_PARSED_GEOMETRY_BOTH>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ParsedGeometryType<enum_NavigationPolygon_ParsedGeometryType>`
**parsed\_geometry\_type** = `2`
`🔗<class_NavigationPolygon_property_parsed_geometry_type>`

classref-property-setget

-   `void (No return value.)` **set\_parsed\_geometry\_type**(value:
    `ParsedGeometryType<enum_NavigationPolygon_ParsedGeometryType>`)
-   `ParsedGeometryType<enum_NavigationPolygon_ParsedGeometryType>`
    **get\_parsed\_geometry\_type**()

Determines which type of nodes will be parsed as geometry. See
`ParsedGeometryType<enum_NavigationPolygon_ParsedGeometryType>` for
possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SamplePartitionType<enum_NavigationPolygon_SamplePartitionType>`
**sample\_partition\_type** = `0`
`🔗<class_NavigationPolygon_property_sample_partition_type>`

classref-property-setget

-   `void (No return value.)` **set\_sample\_partition\_type**(value:
    `SamplePartitionType<enum_NavigationPolygon_SamplePartitionType>`)
-   `SamplePartitionType<enum_NavigationPolygon_SamplePartitionType>`
    **get\_sample\_partition\_type**()

Partitioning algorithm for creating the navigation mesh polys. See
`SamplePartitionType<enum_NavigationPolygon_SamplePartitionType>` for
possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **source\_geometry\_group\_name** =
`&"navigation_polygon_source_geometry_group"`
`🔗<class_NavigationPolygon_property_source_geometry_group_name>`

classref-property-setget

-   `void (No return value.)`
    **set\_source\_geometry\_group\_name**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>`
    **get\_source\_geometry\_group\_name**()

The group name of nodes that should be parsed for baking source
geometry.

Only used when
`source_geometry_mode<class_NavigationPolygon_property_source_geometry_mode>`
is
`SOURCE_GEOMETRY_GROUPS_WITH_CHILDREN<class_NavigationPolygon_constant_SOURCE_GEOMETRY_GROUPS_WITH_CHILDREN>`
or
`SOURCE_GEOMETRY_GROUPS_EXPLICIT<class_NavigationPolygon_constant_SOURCE_GEOMETRY_GROUPS_EXPLICIT>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SourceGeometryMode<enum_NavigationPolygon_SourceGeometryMode>`
**source\_geometry\_mode** = `0`
`🔗<class_NavigationPolygon_property_source_geometry_mode>`

classref-property-setget

-   `void (No return value.)` **set\_source\_geometry\_mode**(value:
    `SourceGeometryMode<enum_NavigationPolygon_SourceGeometryMode>`)
-   `SourceGeometryMode<enum_NavigationPolygon_SourceGeometryMode>`
    **get\_source\_geometry\_mode**()

The source of the geometry used when baking. See
`SourceGeometryMode<enum_NavigationPolygon_SourceGeometryMode>` for
possible values.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_outline**(outline:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_NavigationPolygon_method_add_outline>`

Appends a `PackedVector2Array<class_PackedVector2Array>` that contains
the vertices of an outline to the internal array that contains all the
outlines.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_outline\_at\_index**(outline:
`PackedVector2Array<class_PackedVector2Array>`, index: `int<class_int>`)
`🔗<class_NavigationPolygon_method_add_outline_at_index>`

Adds a `PackedVector2Array<class_PackedVector2Array>` that contains the
vertices of an outline to the internal array that contains all the
outlines at a fixed position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_polygon**(polygon:
`PackedInt32Array<class_PackedInt32Array>`)
`🔗<class_NavigationPolygon_method_add_polygon>`

Adds a polygon using the indices of the vertices you get when calling
`get_vertices<class_NavigationPolygon_method_get_vertices>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_NavigationPolygon_method_clear>`

Clears the internal arrays for vertices and polygon indices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_outlines**()
`🔗<class_NavigationPolygon_method_clear_outlines>`

Clears the array of the outlines, but it doesn't clear the vertices and
the polygons that were created by them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_polygons**()
`🔗<class_NavigationPolygon_method_clear_polygons>`

Clears the array of polygons, but it doesn't clear the array of outlines
and vertices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NavigationMesh<class_NavigationMesh>` **get\_navigation\_mesh**()
`🔗<class_NavigationPolygon_method_get_navigation_mesh>`

Returns the `NavigationMesh<class_NavigationMesh>` resulting from this
navigation polygon. This navigation mesh can be used to update the
navigation mesh of a region with the
`NavigationServer3D.region_set_navigation_mesh<class_NavigationServer3D_method_region_set_navigation_mesh>`
API directly (as 2D uses the 3D server behind the scene).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>` **get\_outline**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationPolygon_method_get_outline>`

Returns a `PackedVector2Array<class_PackedVector2Array>` containing the
vertices of an outline that was created in the editor or by script.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_outline\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationPolygon_method_get_outline_count>`

Returns the number of outlines that were created in the editor or by
script.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**get\_parsed\_collision\_mask\_value**(layer\_number: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationPolygon_method_get_parsed_collision_mask_value>`

Returns whether or not the specified layer of the
`parsed_collision_mask<class_NavigationPolygon_property_parsed_collision_mask>`
is enabled, given a `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>` **get\_polygon**(idx:
`int<class_int>`) `🔗<class_NavigationPolygon_method_get_polygon>`

Returns a `PackedInt32Array<class_PackedInt32Array>` containing the
indices of the vertices of a created polygon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_polygon\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationPolygon_method_get_polygon_count>`

Returns the count of all polygons.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>` **get\_vertices**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationPolygon_method_get_vertices>`

Returns a `PackedVector2Array<class_PackedVector2Array>` containing all
the vertices being used to create the polygons.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **make\_polygons\_from\_outlines**()
`🔗<class_NavigationPolygon_method_make_polygons_from_outlines>`

**Deprecated:** Use
`NavigationServer2D.parse_source_geometry_data<class_NavigationServer2D_method_parse_source_geometry_data>`
and
`NavigationServer2D.bake_from_source_geometry_data<class_NavigationServer2D_method_bake_from_source_geometry_data>`
instead.

Creates polygons from the outlines added in the editor or by script.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_outline**(idx: `int<class_int>`)
`🔗<class_NavigationPolygon_method_remove_outline>`

Removes an outline created in the editor or by script. You have to call
`make_polygons_from_outlines<class_NavigationPolygon_method_make_polygons_from_outlines>`
for the polygons to update.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_outline**(idx: `int<class_int>`,
outline: `PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_NavigationPolygon_method_set_outline>`

Changes an outline created in the editor or by script. You have to call
`make_polygons_from_outlines<class_NavigationPolygon_method_make_polygons_from_outlines>`
for the polygons to update.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_parsed\_collision\_mask\_value**(layer\_number: `int<class_int>`,
value: `bool<class_bool>`)
`🔗<class_NavigationPolygon_method_set_parsed_collision_mask_value>`

Based on `value`, enables or disables the specified layer in the
`parsed_collision_mask<class_NavigationPolygon_property_parsed_collision_mask>`,
given a `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_vertices**(vertices:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_NavigationPolygon_method_set_vertices>`

Sets the vertices that can be then indexed to create polygons with the
`add_polygon<class_NavigationPolygon_method_add_polygon>` method.
