github\_url  
hide

# ImporterMesh

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A `Resource<class_Resource>` that contains vertex array-based geometry
during the import process.

classref-introduction-group

## Description

ImporterMesh is a type of `Resource<class_Resource>` analogous to
`ArrayMesh<class_ArrayMesh>`. It contains vertex array-based geometry,
divided in *surfaces*. Each surface contains a completely separate array
and a material used to draw it. Design wise, a mesh with multiple
surfaces is preferred to a single surface, because objects created in 3D
editing software commonly contain multiple materials.

Unlike its runtime counterpart, **ImporterMesh** contains mesh data
before various import steps, such as lod and shadow mesh generation,
have taken place. Modify surface data by calling
`clear<class_ImporterMesh_method_clear>`, followed by
`add_surface<class_ImporterMesh_method_add_surface>` for each surface.

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

## Method Descriptions

classref-method

`void (No return value.)` **add\_blend\_shape**(name:
`String<class_String>`) `🔗<class_ImporterMesh_method_add_blend_shape>`

Adds name for a blend shape that will be added with
`add_surface<class_ImporterMesh_method_add_surface>`. Must be called
before surface is added.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_surface**(primitive:
`PrimitiveType<enum_Mesh_PrimitiveType>`, arrays: `Array<class_Array>`,
blend\_shapes: `Array<class_Array>`\[`Array<class_Array>`\] = \[\],
lods: `Dictionary<class_Dictionary>` = {}, material:
`Material<class_Material>` = null, name: `String<class_String>` = "",
flags: `int<class_int>` = 0) `🔗<class_ImporterMesh_method_add_surface>`

Creates a new surface.
`Mesh.get_surface_count<class_Mesh_method_get_surface_count>` will
become the `surf_idx` for this new surface.

Surfaces are created to be rendered using a `primitive`, which may be
any of the values defined in `PrimitiveType<enum_Mesh_PrimitiveType>`.

The `arrays` argument is an array of arrays. Each of the
`Mesh.ARRAY_MAX<class_Mesh_constant_ARRAY_MAX>` elements contains an
array with some of the mesh data for this surface as described by the
corresponding member of `ArrayType<enum_Mesh_ArrayType>` or `null` if it
is not used by the surface. For example, `arrays[0]` is the array of
vertices. That first vertex sub-array is always required; the others are
optional. Adding an index array puts this surface into "index mode"
where the vertex and other arrays become the sources of data and the
index array defines the vertex order. All sub-arrays must have the same
length as the vertex array (or be an exact multiple of the vertex
array's length, when multiple elements of a sub-array correspond to a
single vertex) or be empty, except for
`Mesh.ARRAY_INDEX<class_Mesh_constant_ARRAY_INDEX>` if it is used.

The `blend_shapes` argument is an array of vertex data for each blend
shape. Each element is an array of the same structure as `arrays`, but
`Mesh.ARRAY_VERTEX<class_Mesh_constant_ARRAY_VERTEX>`,
`Mesh.ARRAY_NORMAL<class_Mesh_constant_ARRAY_NORMAL>`, and
`Mesh.ARRAY_TANGENT<class_Mesh_constant_ARRAY_TANGENT>` are set if and
only if they are set in `arrays` and all other entries are `null`.

The `lods` argument is a dictionary with `float<class_float>` keys and
`PackedInt32Array<class_PackedInt32Array>` values. Each entry in the
dictionary represents an LOD level of the surface, where the value is
the `Mesh.ARRAY_INDEX<class_Mesh_constant_ARRAY_INDEX>` array to use for
the LOD level and the key is roughly proportional to the distance at
which the LOD stats being used. I.e., increasing the key of an LOD also
increases the distance that the objects has to be from the camera before
the LOD is used.

The `flags` argument is the bitwise or of, as required: One value of
`ArrayCustomFormat<enum_Mesh_ArrayCustomFormat>` left shifted by
`ARRAY_FORMAT_CUSTOMn_SHIFT` for each custom channel in use,
`Mesh.ARRAY_FLAG_USE_DYNAMIC_UPDATE<class_Mesh_constant_ARRAY_FLAG_USE_DYNAMIC_UPDATE>`,
`Mesh.ARRAY_FLAG_USE_8_BONE_WEIGHTS<class_Mesh_constant_ARRAY_FLAG_USE_8_BONE_WEIGHTS>`,
or
`Mesh.ARRAY_FLAG_USES_EMPTY_VERTEX_ARRAY<class_Mesh_constant_ARRAY_FLAG_USES_EMPTY_VERTEX_ARRAY>`.

\*\*Note:\*\* When using indices, it is recommended to only use points,
lines, or triangles.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_ImporterMesh_method_clear>`

Removes all surfaces and blend shapes from this **ImporterMesh**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **generate\_lods**(normal\_merge\_angle:
`float<class_float>`, normal\_split\_angle: `float<class_float>`,
bone\_transform\_array: `Array<class_Array>`)
`🔗<class_ImporterMesh_method_generate_lods>`

Generates all lods for this ImporterMesh.

`normal_merge_angle` and `normal_split_angle` are in degrees and used in
the same way as the importer settings in `lods`. As a good default, use
25 and 60 respectively.

The number of generated lods can be accessed using
`get_surface_lod_count<class_ImporterMesh_method_get_surface_lod_count>`,
and each LOD is available in
`get_surface_lod_size<class_ImporterMesh_method_get_surface_lod_size>`
and
`get_surface_lod_indices<class_ImporterMesh_method_get_surface_lod_indices>`.

`bone_transform_array` is an `Array<class_Array>` which can be either
empty or contain `Transform3D<class_Transform3D>`s which, for each of
the mesh's bone IDs, will apply mesh skinning when generating the LOD
mesh variations. This is usually used to account for discrepancies in
scale between the mesh itself and its skinning data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_blend\_shape\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_blend_shape_count>`

Returns the number of blend shapes that the mesh holds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`BlendShapeMode<enum_Mesh_BlendShapeMode>` **get\_blend\_shape\_mode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_blend_shape_mode>`

Returns the blend shape mode for this Mesh.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_blend\_shape\_name**(blend\_shape\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_blend_shape_name>`

Returns the name of the blend shape at this index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **get\_lightmap\_size\_hint**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_lightmap_size_hint>`

Returns the size hint of this mesh for lightmap-unwrapping in UV-space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ArrayMesh<class_ArrayMesh>` **get\_mesh**(base\_mesh:
`ArrayMesh<class_ArrayMesh>` = null)
`🔗<class_ImporterMesh_method_get_mesh>`

Returns the mesh data represented by this **ImporterMesh** as a usable
`ArrayMesh<class_ArrayMesh>`.

This method caches the returned mesh, and subsequent calls will return
the cached data until `clear<class_ImporterMesh_method_clear>` is
called.

If not yet cached and `base_mesh` is provided, `base_mesh` will be used
and mutated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_surface\_arrays**(surface\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_surface_arrays>`

Returns the arrays for the vertices, normals, UVs, etc. that make up the
requested surface. See
`add_surface<class_ImporterMesh_method_add_surface>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`
**get\_surface\_blend\_shape\_arrays**(surface\_idx: `int<class_int>`,
blend\_shape\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_surface_blend_shape_arrays>`

Returns a single set of blend shape arrays for the requested blend shape
index for a surface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_surface\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_surface_count>`

Returns the number of surfaces that the mesh holds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_surface\_format**(surface\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_surface_format>`

Returns the format of the surface that the mesh holds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_surface\_lod\_count**(surface\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_surface_lod_count>`

Returns the number of lods that the mesh holds on a given surface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**get\_surface\_lod\_indices**(surface\_idx: `int<class_int>`, lod\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_surface_lod_indices>`

Returns the index buffer of a lod for a surface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_surface\_lod\_size**(surface\_idx:
`int<class_int>`, lod\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_surface_lod_size>`

Returns the screen ratio which activates a lod for a surface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Material<class_Material>` **get\_surface\_material**(surface\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_surface_material>`

Returns a `Material<class_Material>` in a given surface. Surface is
rendered using this material.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_surface\_name**(surface\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ImporterMesh_method_get_surface_name>`

Gets the name assigned to this surface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PrimitiveType<enum_Mesh_PrimitiveType>`
**get\_surface\_primitive\_type**(surface\_idx: `int<class_int>`)
`🔗<class_ImporterMesh_method_get_surface_primitive_type>`

Returns the primitive type of the requested surface (see
`add_surface<class_ImporterMesh_method_add_surface>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_blend\_shape\_mode**(mode:
`BlendShapeMode<enum_Mesh_BlendShapeMode>`)
`🔗<class_ImporterMesh_method_set_blend_shape_mode>`

Sets the blend shape mode to one of
`BlendShapeMode<enum_Mesh_BlendShapeMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_lightmap\_size\_hint**(size:
`Vector2i<class_Vector2i>`)
`🔗<class_ImporterMesh_method_set_lightmap_size_hint>`

Sets the size hint of this mesh for lightmap-unwrapping in UV-space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_surface\_material**(surface\_idx:
`int<class_int>`, material: `Material<class_Material>`)
`🔗<class_ImporterMesh_method_set_surface_material>`

Sets a `Material<class_Material>` for a given surface. Surface will be
rendered using this material.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_surface\_name**(surface\_idx:
`int<class_int>`, name: `String<class_String>`)
`🔗<class_ImporterMesh_method_set_surface_name>`

Sets a name for a given surface.
