github\_url  
hide

# PrimitiveMesh

**Inherits:** `Mesh<class_Mesh>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `BoxMesh<class_BoxMesh>`,
`CapsuleMesh<class_CapsuleMesh>`, `CylinderMesh<class_CylinderMesh>`,
`PlaneMesh<class_PlaneMesh>`, `PointMesh<class_PointMesh>`,
`PrismMesh<class_PrismMesh>`, `RibbonTrailMesh<class_RibbonTrailMesh>`,
`SphereMesh<class_SphereMesh>`, `TextMesh<class_TextMesh>`,
`TorusMesh<class_TorusMesh>`, `TubeTrailMesh<class_TubeTrailMesh>`

Base class for all primitive meshes. Handles applying a
`Material<class_Material>` to a primitive mesh.

classref-introduction-group

## Description

Base class for all primitive meshes. Handles applying a
`Material<class_Material>` to a primitive mesh. Examples include
`BoxMesh<class_BoxMesh>`, `CapsuleMesh<class_CapsuleMesh>`,
`CylinderMesh<class_CylinderMesh>`, `PlaneMesh<class_PlaneMesh>`,
`PrismMesh<class_PrismMesh>`, and `SphereMesh<class_SphereMesh>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **add\_uv2** = `false`
`🔗<class_PrimitiveMesh_property_add_uv2>`

classref-property-setget

-   `void (No return value.)` **set\_add\_uv2**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_add\_uv2**()

If set, generates UV2 UV coordinates applying a padding using the
`uv2_padding<class_PrimitiveMesh_property_uv2_padding>` setting. UV2 is
needed for lightmapping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AABB<class_AABB>` **custom\_aabb** = `AABB(0, 0, 0, 0, 0, 0)`
`🔗<class_PrimitiveMesh_property_custom_aabb>`

classref-property-setget

-   `void (No return value.)` **set\_custom\_aabb**(value:
    `AABB<class_AABB>`)
-   `AABB<class_AABB>` **get\_custom\_aabb**()

Overrides the `AABB<class_AABB>` with one defined by user for use with
frustum culling. Especially useful to avoid unexpected culling when
using a shader to offset vertices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **flip\_faces** = `false`
`🔗<class_PrimitiveMesh_property_flip_faces>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_faces**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_flip\_faces**()

If set, the order of the vertices in each triangle are reversed
resulting in the backside of the mesh being drawn.

This gives the same result as using
`BaseMaterial3D.CULL_FRONT<class_BaseMaterial3D_constant_CULL_FRONT>` in
`BaseMaterial3D.cull_mode<class_BaseMaterial3D_property_cull_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Material<class_Material>` **material**
`🔗<class_PrimitiveMesh_property_material>`

classref-property-setget

-   `void (No return value.)` **set\_material**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_material**()

The current `Material<class_Material>` of the primitive mesh.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **uv2\_padding** = `2.0`
`🔗<class_PrimitiveMesh_property_uv2_padding>`

classref-property-setget

-   `void (No return value.)` **set\_uv2\_padding**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_uv2\_padding**()

If `add_uv2<class_PrimitiveMesh_property_add_uv2>` is set, specifies the
padding in pixels applied along seams of the mesh. Lower padding values
allow making better use of the lightmap texture (resulting in higher
texel density), but may introduce visible lightmap bleeding along edges.

If the size of the lightmap texture can't be determined when generating
the mesh, UV2 is calculated assuming a texture size of 1024x1024.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Array<class_Array>` **\_create\_mesh\_array**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PrimitiveMesh_private_method__create_mesh_array>`

Override this method to customize how this primitive mesh should be
generated. Should return an `Array<class_Array>` where each element is
another Array of values required for the mesh (see the
`ArrayType<enum_Mesh_ArrayType>` constants).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_mesh\_arrays**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PrimitiveMesh_method_get_mesh_arrays>`

Returns mesh arrays used to constitute surface of `Mesh<class_Mesh>`.
The result can be passed to
`ArrayMesh.add_surface_from_arrays<class_ArrayMesh_method_add_surface_from_arrays>`
to create a new surface. For example:

gdscript

var c = CylinderMesh.new() var arr\_mesh = ArrayMesh.new()
arr\_mesh.add\_surface\_from\_arrays(Mesh.PRIMITIVE\_TRIANGLES,
c.get\_mesh\_arrays())

csharp

var c = new CylinderMesh(); var arrMesh = new ArrayMesh();
arrMesh.AddSurfaceFromArrays(Mesh.PrimitiveType.Triangles,
c.GetMeshArrays());

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **request\_update**()
`🔗<class_PrimitiveMesh_method_request_update>`

Request an update of this primitive mesh based on its properties.
