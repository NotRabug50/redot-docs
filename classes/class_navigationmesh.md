github\_url  
hide

# NavigationMesh

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A navigation mesh that defines traversable areas and obstacles.

classref-introduction-group

## Description

A navigation mesh is a collection of polygons that define which areas of
an environment are traversable to aid agents in pathfinding through
complicated spaces.

classref-introduction-group

## Tutorials

-   `Using NavigationMeshes <../tutorials/navigation/navigation_using_navigationmeshes>`
-   [3D Navigation
    Demo](https://godotengine.org/asset-library/asset/2743)

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **SamplePartitionType**:
`🔗<enum_NavigationMesh_SamplePartitionType>`

classref-enumeration-constant

`SamplePartitionType<enum_NavigationMesh_SamplePartitionType>`
**SAMPLE\_PARTITION\_WATERSHED** = `0`

Watershed partitioning. Generally the best choice if you precompute the
navigation mesh, use this if you have large open areas.

classref-enumeration-constant

`SamplePartitionType<enum_NavigationMesh_SamplePartitionType>`
**SAMPLE\_PARTITION\_MONOTONE** = `1`

Monotone partitioning. Use this if you want fast navigation mesh
generation.

classref-enumeration-constant

`SamplePartitionType<enum_NavigationMesh_SamplePartitionType>`
**SAMPLE\_PARTITION\_LAYERS** = `2`

Layer partitioning. Good choice to use for tiled navigation mesh with
medium and small sized tiles.

classref-enumeration-constant

`SamplePartitionType<enum_NavigationMesh_SamplePartitionType>`
**SAMPLE\_PARTITION\_MAX** = `3`

Represents the size of the
`SamplePartitionType<enum_NavigationMesh_SamplePartitionType>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ParsedGeometryType**:
`🔗<enum_NavigationMesh_ParsedGeometryType>`

classref-enumeration-constant

`ParsedGeometryType<enum_NavigationMesh_ParsedGeometryType>`
**PARSED\_GEOMETRY\_MESH\_INSTANCES** = `0`

Parses mesh instances as geometry. This includes
`MeshInstance3D<class_MeshInstance3D>`, `CSGShape3D<class_CSGShape3D>`,
and `GridMap<class_GridMap>` nodes.

classref-enumeration-constant

`ParsedGeometryType<enum_NavigationMesh_ParsedGeometryType>`
**PARSED\_GEOMETRY\_STATIC\_COLLIDERS** = `1`

Parses `StaticBody3D<class_StaticBody3D>` colliders as geometry. The
collider should be in any of the layers specified by
`geometry_collision_mask<class_NavigationMesh_property_geometry_collision_mask>`.

classref-enumeration-constant

`ParsedGeometryType<enum_NavigationMesh_ParsedGeometryType>`
**PARSED\_GEOMETRY\_BOTH** = `2`

Both
`PARSED_GEOMETRY_MESH_INSTANCES<class_NavigationMesh_constant_PARSED_GEOMETRY_MESH_INSTANCES>`
and
`PARSED_GEOMETRY_STATIC_COLLIDERS<class_NavigationMesh_constant_PARSED_GEOMETRY_STATIC_COLLIDERS>`.

classref-enumeration-constant

`ParsedGeometryType<enum_NavigationMesh_ParsedGeometryType>`
**PARSED\_GEOMETRY\_MAX** = `3`

Represents the size of the
`ParsedGeometryType<enum_NavigationMesh_ParsedGeometryType>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SourceGeometryMode**:
`🔗<enum_NavigationMesh_SourceGeometryMode>`

classref-enumeration-constant

`SourceGeometryMode<enum_NavigationMesh_SourceGeometryMode>`
**SOURCE\_GEOMETRY\_ROOT\_NODE\_CHILDREN** = `0`

Scans the child nodes of the root node recursively for geometry.

classref-enumeration-constant

`SourceGeometryMode<enum_NavigationMesh_SourceGeometryMode>`
**SOURCE\_GEOMETRY\_GROUPS\_WITH\_CHILDREN** = `1`

Scans nodes in a group and their child nodes recursively for geometry.
The group is specified by
`geometry_source_group_name<class_NavigationMesh_property_geometry_source_group_name>`.

classref-enumeration-constant

`SourceGeometryMode<enum_NavigationMesh_SourceGeometryMode>`
**SOURCE\_GEOMETRY\_GROUPS\_EXPLICIT** = `2`

Uses nodes in a group for geometry. The group is specified by
`geometry_source_group_name<class_NavigationMesh_property_geometry_source_group_name>`.

classref-enumeration-constant

`SourceGeometryMode<enum_NavigationMesh_SourceGeometryMode>`
**SOURCE\_GEOMETRY\_MAX** = `3`

Represents the size of the
`SourceGeometryMode<enum_NavigationMesh_SourceGeometryMode>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **agent\_height** = `1.5`
`🔗<class_NavigationMesh_property_agent_height>`

classref-property-setget

-   `void (No return value.)` **set\_agent\_height**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_agent\_height**()

The minimum floor to ceiling height that will still allow the floor area
to be considered walkable.

\*\*Note:\*\* While baking, this value will be rounded up to the nearest
multiple of `cell_height<class_NavigationMesh_property_cell_height>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **agent\_max\_climb** = `0.25`
`🔗<class_NavigationMesh_property_agent_max_climb>`

classref-property-setget

-   `void (No return value.)` **set\_agent\_max\_climb**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_agent\_max\_climb**()

The minimum ledge height that is considered to still be traversable.

\*\*Note:\*\* While baking, this value will be rounded down to the
nearest multiple of
`cell_height<class_NavigationMesh_property_cell_height>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **agent\_max\_slope** = `45.0`
`🔗<class_NavigationMesh_property_agent_max_slope>`

classref-property-setget

-   `void (No return value.)` **set\_agent\_max\_slope**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_agent\_max\_slope**()

The maximum slope that is considered walkable, in degrees.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **agent\_radius** = `0.5`
`🔗<class_NavigationMesh_property_agent_radius>`

classref-property-setget

-   `void (No return value.)` **set\_agent\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_agent\_radius**()

The distance to erode/shrink the walkable area of the heightfield away
from obstructions.

\*\*Note:\*\* While baking, this value will be rounded up to the nearest
multiple of `cell_size<class_NavigationMesh_property_cell_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **border\_size** = `0.0`
`🔗<class_NavigationMesh_property_border_size>`

classref-property-setget

-   `void (No return value.)` **set\_border\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_border\_size**()

The size of the non-navigable border around the bake bounding area.

In conjunction with the
`filter_baking_aabb<class_NavigationMesh_property_filter_baking_aabb>`
and a `edge_max_error<class_NavigationMesh_property_edge_max_error>`
value at `1.0` or below the border size can be used to bake tile aligned
navigation meshes without the tile edges being shrunk by
`agent_radius<class_NavigationMesh_property_agent_radius>`.

\*\*Note:\*\* While baking and not zero, this value will be rounded up
to the nearest multiple of
`cell_size<class_NavigationMesh_property_cell_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **cell\_height** = `0.25`
`🔗<class_NavigationMesh_property_cell_height>`

classref-property-setget

-   `void (No return value.)` **set\_cell\_height**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_cell\_height**()

The cell height used to rasterize the navigation mesh vertices on the Y
axis. Must match with the cell height on the navigation map.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **cell\_size** = `0.25`
`🔗<class_NavigationMesh_property_cell_size>`

classref-property-setget

-   `void (No return value.)` **set\_cell\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_cell\_size**()

The cell size used to rasterize the navigation mesh vertices on the XZ
plane. Must match with the cell size on the navigation map.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **detail\_sample\_distance** = `6.0`
`🔗<class_NavigationMesh_property_detail_sample_distance>`

classref-property-setget

-   `void (No return value.)` **set\_detail\_sample\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_detail\_sample\_distance**()

The sampling distance to use when generating the detail mesh, in cell
unit.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **detail\_sample\_max\_error** = `1.0`
`🔗<class_NavigationMesh_property_detail_sample_max_error>`

classref-property-setget

-   `void (No return value.)` **set\_detail\_sample\_max\_error**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_detail\_sample\_max\_error**()

The maximum distance the detail mesh surface should deviate from
heightfield, in cell unit.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **edge\_max\_error** = `1.3`
`🔗<class_NavigationMesh_property_edge_max_error>`

classref-property-setget

-   `void (No return value.)` **set\_edge\_max\_error**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_edge\_max\_error**()

The maximum distance a simplified contour's border edges should deviate
the original raw contour.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **edge\_max\_length** = `0.0`
`🔗<class_NavigationMesh_property_edge_max_length>`

classref-property-setget

-   `void (No return value.)` **set\_edge\_max\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_edge\_max\_length**()

The maximum allowed length for contour edges along the border of the
mesh. A value of `0.0` disables this feature.

\*\*Note:\*\* While baking, this value will be rounded up to the nearest
multiple of `cell_size<class_NavigationMesh_property_cell_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AABB<class_AABB>` **filter\_baking\_aabb** = `AABB(0, 0, 0, 0, 0, 0)`
`🔗<class_NavigationMesh_property_filter_baking_aabb>`

classref-property-setget

-   `void (No return value.)` **set\_filter\_baking\_aabb**(value:
    `AABB<class_AABB>`)
-   `AABB<class_AABB>` **get\_filter\_baking\_aabb**()

If the baking `AABB<class_AABB>` has a volume the navigation mesh baking
will be restricted to its enclosing area.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **filter\_baking\_aabb\_offset** =
`Vector3(0, 0, 0)`
`🔗<class_NavigationMesh_property_filter_baking_aabb_offset>`

classref-property-setget

-   `void (No return value.)`
    **set\_filter\_baking\_aabb\_offset**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_filter\_baking\_aabb\_offset**()

The position offset applied to the
`filter_baking_aabb<class_NavigationMesh_property_filter_baking_aabb>`
`AABB<class_AABB>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **filter\_ledge\_spans** = `false`
`🔗<class_NavigationMesh_property_filter_ledge_spans>`

classref-property-setget

-   `void (No return value.)` **set\_filter\_ledge\_spans**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_filter\_ledge\_spans**()

If `true`, marks spans that are ledges as non-walkable.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **filter\_low\_hanging\_obstacles** = `false`
`🔗<class_NavigationMesh_property_filter_low_hanging_obstacles>`

classref-property-setget

-   `void (No return value.)`
    **set\_filter\_low\_hanging\_obstacles**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_filter\_low\_hanging\_obstacles**()

If `true`, marks non-walkable spans as walkable if their maximum is
within `agent_max_climb<class_NavigationMesh_property_agent_max_climb>`
of a walkable neighbor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **filter\_walkable\_low\_height\_spans** = `false`
`🔗<class_NavigationMesh_property_filter_walkable_low_height_spans>`

classref-property-setget

-   `void (No return value.)`
    **set\_filter\_walkable\_low\_height\_spans**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_filter\_walkable\_low\_height\_spans**()

If `true`, marks walkable spans as not walkable if the clearance above
the span is less than
`agent_height<class_NavigationMesh_property_agent_height>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **geometry\_collision\_mask** = `4294967295`
`🔗<class_NavigationMesh_property_geometry_collision_mask>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_collision\_mask**()

The physics layers to scan for static colliders.

Only used when
`geometry_parsed_geometry_type<class_NavigationMesh_property_geometry_parsed_geometry_type>`
is
`PARSED_GEOMETRY_STATIC_COLLIDERS<class_NavigationMesh_constant_PARSED_GEOMETRY_STATIC_COLLIDERS>`
or
`PARSED_GEOMETRY_BOTH<class_NavigationMesh_constant_PARSED_GEOMETRY_BOTH>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ParsedGeometryType<enum_NavigationMesh_ParsedGeometryType>`
**geometry\_parsed\_geometry\_type** = `2`
`🔗<class_NavigationMesh_property_geometry_parsed_geometry_type>`

classref-property-setget

-   `void (No return value.)` **set\_parsed\_geometry\_type**(value:
    `ParsedGeometryType<enum_NavigationMesh_ParsedGeometryType>`)
-   `ParsedGeometryType<enum_NavigationMesh_ParsedGeometryType>`
    **get\_parsed\_geometry\_type**()

Determines which type of nodes will be parsed as geometry. See
`ParsedGeometryType<enum_NavigationMesh_ParsedGeometryType>` for
possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SourceGeometryMode<enum_NavigationMesh_SourceGeometryMode>`
**geometry\_source\_geometry\_mode** = `0`
`🔗<class_NavigationMesh_property_geometry_source_geometry_mode>`

classref-property-setget

-   `void (No return value.)` **set\_source\_geometry\_mode**(value:
    `SourceGeometryMode<enum_NavigationMesh_SourceGeometryMode>`)
-   `SourceGeometryMode<enum_NavigationMesh_SourceGeometryMode>`
    **get\_source\_geometry\_mode**()

The source of the geometry used when baking. See
`SourceGeometryMode<enum_NavigationMesh_SourceGeometryMode>` for
possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **geometry\_source\_group\_name** =
`&"navigation_mesh_source_group"`
`🔗<class_NavigationMesh_property_geometry_source_group_name>`

classref-property-setget

-   `void (No return value.)` **set\_source\_group\_name**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_source\_group\_name**()

The name of the group to scan for geometry.

Only used when
`geometry_source_geometry_mode<class_NavigationMesh_property_geometry_source_geometry_mode>`
is
`SOURCE_GEOMETRY_GROUPS_WITH_CHILDREN<class_NavigationMesh_constant_SOURCE_GEOMETRY_GROUPS_WITH_CHILDREN>`
or
`SOURCE_GEOMETRY_GROUPS_EXPLICIT<class_NavigationMesh_constant_SOURCE_GEOMETRY_GROUPS_EXPLICIT>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **region\_merge\_size** = `20.0`
`🔗<class_NavigationMesh_property_region_merge_size>`

classref-property-setget

-   `void (No return value.)` **set\_region\_merge\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_region\_merge\_size**()

Any regions with a size smaller than this will be merged with larger
regions if possible.

\*\*Note:\*\* This value will be squared to calculate the number of
cells. For example, a value of 20 will set the number of cells to 400.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **region\_min\_size** = `2.0`
`🔗<class_NavigationMesh_property_region_min_size>`

classref-property-setget

-   `void (No return value.)` **set\_region\_min\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_region\_min\_size**()

The minimum size of a region for it to be created.

\*\*Note:\*\* This value will be squared to calculate the minimum number
of cells allowed to form isolated island areas. For example, a value of
8 will set the number of cells to 64.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SamplePartitionType<enum_NavigationMesh_SamplePartitionType>`
**sample\_partition\_type** = `0`
`🔗<class_NavigationMesh_property_sample_partition_type>`

classref-property-setget

-   `void (No return value.)` **set\_sample\_partition\_type**(value:
    `SamplePartitionType<enum_NavigationMesh_SamplePartitionType>`)
-   `SamplePartitionType<enum_NavigationMesh_SamplePartitionType>`
    **get\_sample\_partition\_type**()

Partitioning algorithm for creating the navigation mesh polys. See
`SamplePartitionType<enum_NavigationMesh_SamplePartitionType>` for
possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **vertices\_per\_polygon** = `6.0`
`🔗<class_NavigationMesh_property_vertices_per_polygon>`

classref-property-setget

-   `void (No return value.)` **set\_vertices\_per\_polygon**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_vertices\_per\_polygon**()

The maximum number of vertices allowed for polygons generated during the
contour to polygon conversion process.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_polygon**(polygon:
`PackedInt32Array<class_PackedInt32Array>`)
`🔗<class_NavigationMesh_method_add_polygon>`

Adds a polygon using the indices of the vertices you get when calling
`get_vertices<class_NavigationMesh_method_get_vertices>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_NavigationMesh_method_clear>`

Clears the internal arrays for vertices and polygon indices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_polygons**()
`🔗<class_NavigationMesh_method_clear_polygons>`

Clears the array of polygons, but it doesn't clear the array of
vertices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **create\_from\_mesh**(mesh:
`Mesh<class_Mesh>`) `🔗<class_NavigationMesh_method_create_from_mesh>`

Initializes the navigation mesh by setting the vertices and indices
according to a `Mesh<class_Mesh>`.

\*\*Note:\*\* The given `mesh` must be of type
`Mesh.PRIMITIVE_TRIANGLES<class_Mesh_constant_PRIMITIVE_TRIANGLES>` and
have an index array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_collision\_mask\_value**(layer\_number:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationMesh_method_get_collision_mask_value>`

Returns whether or not the specified layer of the
`geometry_collision_mask<class_NavigationMesh_property_geometry_collision_mask>`
is enabled, given a `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>` **get\_polygon**(idx:
`int<class_int>`) `🔗<class_NavigationMesh_method_get_polygon>`

Returns a `PackedInt32Array<class_PackedInt32Array>` containing the
indices of the vertices of a created polygon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_polygon\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationMesh_method_get_polygon_count>`

Returns the number of polygons in the navigation mesh.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>` **get\_vertices**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_NavigationMesh_method_get_vertices>`

Returns a `PackedVector3Array<class_PackedVector3Array>` containing all
the vertices being used to create the polygons.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_collision\_mask\_value**(layer\_number:
`int<class_int>`, value: `bool<class_bool>`)
`🔗<class_NavigationMesh_method_set_collision_mask_value>`

Based on `value`, enables or disables the specified layer in the
`geometry_collision_mask<class_NavigationMesh_property_geometry_collision_mask>`,
given a `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_vertices**(vertices:
`PackedVector3Array<class_PackedVector3Array>`)
`🔗<class_NavigationMesh_method_set_vertices>`

Sets the vertices that can be then indexed to create polygons with the
`add_polygon<class_NavigationMesh_method_add_polygon>` method.
