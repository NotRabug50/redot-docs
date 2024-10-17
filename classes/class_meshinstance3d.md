github\_url  
hide

# MeshInstance3D

**Inherits:** `GeometryInstance3D<class_GeometryInstance3D>` **&lt;**
`VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `SoftBody3D<class_SoftBody3D>`

Node that instances meshes into a scenario.

classref-introduction-group

## Description

MeshInstance3D is a node that takes a `Mesh<class_Mesh>` resource and
adds it to the current scenario by creating an instance of it. This is
the class most often used render 3D geometry and can be used to instance
a single `Mesh<class_Mesh>` in many places. This allows reusing
geometry, which can save on resources. When a `Mesh<class_Mesh>` has to
be instantiated more than thousands of times at close proximity,
consider using a `MultiMesh<class_MultiMesh>` in a
`MultiMeshInstance3D<class_MultiMeshInstance3D>` instead.

classref-introduction-group

## Tutorials

-   [3D Material Testers
    Demo](https://godotengine.org/asset-library/asset/2742)
-   [3D Kinematic Character
    Demo](https://godotengine.org/asset-library/asset/2739)
-   [3D Platformer
    Demo](https://godotengine.org/asset-library/asset/2748)
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Mesh<class_Mesh>` **mesh** `🔗<class_MeshInstance3D_property_mesh>`

classref-property-setget

-   `void (No return value.)` **set\_mesh**(value: `Mesh<class_Mesh>`)
-   `Mesh<class_Mesh>` **get\_mesh**()

The `Mesh<class_Mesh>` resource for the instance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **skeleton** = `NodePath("..")`
`🔗<class_MeshInstance3D_property_skeleton>`

classref-property-setget

-   `void (No return value.)` **set\_skeleton\_path**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_skeleton\_path**()

`NodePath<class_NodePath>` to the `Skeleton3D<class_Skeleton3D>`
associated with the instance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Skin<class_Skin>` **skin** `🔗<class_MeshInstance3D_property_skin>`

classref-property-setget

-   `void (No return value.)` **set\_skin**(value: `Skin<class_Skin>`)
-   `Skin<class_Skin>` **get\_skin**()

The `Skin<class_Skin>` to be used by this instance.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`ArrayMesh<class_ArrayMesh>`
**bake\_mesh\_from\_current\_blend\_shape\_mix**(existing:
`ArrayMesh<class_ArrayMesh>` = null)
`🔗<class_MeshInstance3D_method_bake_mesh_from_current_blend_shape_mix>`

Takes a snapshot from the current `ArrayMesh<class_ArrayMesh>` with all
blend shapes applied according to their current weights and bakes it to
the provided `existing` mesh. If no `existing` mesh is provided a new
`ArrayMesh<class_ArrayMesh>` is created, baked and returned. Mesh
surface materials are not copied.

\*\*Performance:\*\* `Mesh<class_Mesh>` data needs to be received from
the GPU, stalling the `RenderingServer<class_RenderingServer>` in the
process.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ArrayMesh<class_ArrayMesh>`
**bake\_mesh\_from\_current\_skeleton\_pose**(existing:
`ArrayMesh<class_ArrayMesh>` = null)
`🔗<class_MeshInstance3D_method_bake_mesh_from_current_skeleton_pose>`

Takes a snapshot of the current animated skeleton pose of the skinned
mesh and bakes it to the provided `existing` mesh. If no `existing` mesh
is provided a new `ArrayMesh<class_ArrayMesh>` is created, baked, and
returned. Requires a skeleton with a registered skin to work.
Blendshapes are ignored. Mesh surface materials are not copied.

\*\*Performance:\*\* `Mesh<class_Mesh>` data needs to be retrieved from
the GPU, stalling the `RenderingServer<class_RenderingServer>` in the
process.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **create\_convex\_collision**(clean:
`bool<class_bool>` = true, simplify: `bool<class_bool>` = false)
`🔗<class_MeshInstance3D_method_create_convex_collision>`

This helper creates a `StaticBody3D<class_StaticBody3D>` child node with
a `ConvexPolygonShape3D<class_ConvexPolygonShape3D>` collision shape
calculated from the mesh geometry. It's mainly used for testing.

If `clean` is `true` (default), duplicate and interior vertices are
removed automatically. You can set it to `false` to make the process
faster if not needed.

If `simplify` is `true`, the geometry can be further simplified to
reduce the number of vertices. Disabled by default.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **create\_debug\_tangents**()
`🔗<class_MeshInstance3D_method_create_debug_tangents>`

This helper creates a **MeshInstance3D** child node with gizmos at every
vertex calculated from the mesh geometry. It's mainly used for testing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**create\_multiple\_convex\_collisions**(settings:
`MeshConvexDecompositionSettings<class_MeshConvexDecompositionSettings>`
= null)
`🔗<class_MeshInstance3D_method_create_multiple_convex_collisions>`

This helper creates a `StaticBody3D<class_StaticBody3D>` child node with
multiple `ConvexPolygonShape3D<class_ConvexPolygonShape3D>` collision
shapes calculated from the mesh geometry via convex decomposition. The
convex decomposition operation can be controlled with parameters from
the optional `settings`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **create\_trimesh\_collision**()
`🔗<class_MeshInstance3D_method_create_trimesh_collision>`

This helper creates a `StaticBody3D<class_StaticBody3D>` child node with
a `ConcavePolygonShape3D<class_ConcavePolygonShape3D>` collision shape
calculated from the mesh geometry. It's mainly used for testing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **find\_blend\_shape\_by\_name**(name:
`StringName<class_StringName>`)
`🔗<class_MeshInstance3D_method_find_blend_shape_by_name>`

Returns the index of the blend shape with the given `name`. Returns `-1`
if no blend shape with this name exists, including when
`mesh<class_MeshInstance3D_property_mesh>` is `null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Material<class_Material>` **get\_active\_material**(surface:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MeshInstance3D_method_get_active_material>`

Returns the `Material<class_Material>` that will be used by the
`Mesh<class_Mesh>` when drawing. This can return the
`GeometryInstance3D.material_override<class_GeometryInstance3D_property_material_override>`,
the surface override `Material<class_Material>` defined in this
**MeshInstance3D**, or the surface `Material<class_Material>` defined in
the `mesh<class_MeshInstance3D_property_mesh>`. For example, if
`GeometryInstance3D.material_override<class_GeometryInstance3D_property_material_override>`
is used, all surfaces will return the override material.

Returns `null` if no material is active, including when
`mesh<class_MeshInstance3D_property_mesh>` is `null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_blend\_shape\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MeshInstance3D_method_get_blend_shape_count>`

Returns the number of blend shapes available. Produces an error if
`mesh<class_MeshInstance3D_property_mesh>` is `null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_blend\_shape\_value**(blend\_shape\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MeshInstance3D_method_get_blend_shape_value>`

Returns the value of the blend shape at the given `blend_shape_idx`.
Returns `0.0` and produces an error if
`mesh<class_MeshInstance3D_property_mesh>` is `null` or doesn't have a
blend shape at that index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`SkinReference<class_SkinReference>` **get\_skin\_reference**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MeshInstance3D_method_get_skin_reference>`

Returns the internal `SkinReference<class_SkinReference>` containing the
skeleton's `RID<class_RID>` attached to this RID. See also
`Resource.get_rid<class_Resource_method_get_rid>`,
`SkinReference.get_skeleton<class_SkinReference_method_get_skeleton>`,
and
`RenderingServer.instance_attach_skeleton<class_RenderingServer_method_instance_attach_skeleton>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Material<class_Material>` **get\_surface\_override\_material**(surface:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MeshInstance3D_method_get_surface_override_material>`

Returns the override `Material<class_Material>` for the specified
`surface` of the `Mesh<class_Mesh>` resource. See also
`get_surface_override_material_count<class_MeshInstance3D_method_get_surface_override_material_count>`.

\*\*Note:\*\* This returns the `Material<class_Material>` associated to
the **MeshInstance3D**'s Surface Material Override properties, not the
material within the `Mesh<class_Mesh>` resource. To get the material
within the `Mesh<class_Mesh>` resource, use
`Mesh.surface_get_material<class_Mesh_method_surface_get_material>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_surface\_override\_material\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MeshInstance3D_method_get_surface_override_material_count>`

Returns the number of surface override materials. This is equivalent to
`Mesh.get_surface_count<class_Mesh_method_get_surface_count>`. See also
`get_surface_override_material<class_MeshInstance3D_method_get_surface_override_material>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_blend\_shape\_value**(blend\_shape\_idx: `int<class_int>`, value:
`float<class_float>`)
`🔗<class_MeshInstance3D_method_set_blend_shape_value>`

Sets the value of the blend shape at `blend_shape_idx` to `value`.
Produces an error if `mesh<class_MeshInstance3D_property_mesh>` is
`null` or doesn't have a blend shape at that index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_surface\_override\_material**(surface:
`int<class_int>`, material: `Material<class_Material>`)
`🔗<class_MeshInstance3D_method_set_surface_override_material>`

Sets the override `material` for the specified `surface` of the
`Mesh<class_Mesh>` resource. This material is associated with this
**MeshInstance3D** rather than with
`mesh<class_MeshInstance3D_property_mesh>`.

\*\*Note:\*\* This assigns the `Material<class_Material>` associated to
the **MeshInstance3D**'s Surface Material Override properties, not the
material within the `Mesh<class_Mesh>` resource. To set the material
within the `Mesh<class_Mesh>` resource, use
`Mesh.surface_get_material<class_Mesh_method_surface_get_material>`
instead.
