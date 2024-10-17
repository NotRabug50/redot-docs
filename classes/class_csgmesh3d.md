github\_url  
hide

# CSGMesh3D

**Inherits:** `CSGPrimitive3D<class_CSGPrimitive3D>` **&lt;**
`CSGShape3D<class_CSGShape3D>` **&lt;**
`GeometryInstance3D<class_GeometryInstance3D>` **&lt;**
`VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A CSG Mesh shape that uses a mesh resource.

classref-introduction-group

## Description

This CSG node allows you to use any mesh resource as a CSG shape,
provided it is closed, does not self-intersect, does not contain
internal faces and has no edges that connect to more than two faces. See
also `CSGPolygon3D<class_CSGPolygon3D>` for drawing 2D extruded polygons
to be used as CSG nodes.

\*\*Note:\*\* CSG nodes are intended to be used for level prototyping.
Creating CSG nodes has a significant CPU cost compared to creating a
`MeshInstance3D<class_MeshInstance3D>` with a
`PrimitiveMesh<class_PrimitiveMesh>`. Moving a CSG node within another
CSG node also has a significant CPU cost, so it should be avoided during
gameplay.

classref-introduction-group

## Tutorials

-   `Prototyping levels with CSG <../tutorials/3d/csg_tools>`

classref-reftable-group

## Properties

<table>
<tbody>
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

`Material<class_Material>` **material**
`🔗<class_CSGMesh3D_property_material>`

classref-property-setget

-   `void (No return value.)` **set\_material**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_material**()

The `Material<class_Material>` used in drawing the CSG shape.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Mesh<class_Mesh>` **mesh** `🔗<class_CSGMesh3D_property_mesh>`

classref-property-setget

-   `void (No return value.)` **set\_mesh**(value: `Mesh<class_Mesh>`)
-   `Mesh<class_Mesh>` **get\_mesh**()

The `Mesh<class_Mesh>` resource to use as a CSG shape.

\*\*Note:\*\* When using an `ArrayMesh<class_ArrayMesh>`, all vertex
attributes except `Mesh.ARRAY_VERTEX<class_Mesh_constant_ARRAY_VERTEX>`,
`Mesh.ARRAY_NORMAL<class_Mesh_constant_ARRAY_NORMAL>` and
`Mesh.ARRAY_TEX_UV<class_Mesh_constant_ARRAY_TEX_UV>` are left unused.
Only `Mesh.ARRAY_VERTEX<class_Mesh_constant_ARRAY_VERTEX>` and
`Mesh.ARRAY_TEX_UV<class_Mesh_constant_ARRAY_TEX_UV>` will be passed to
the GPU.

`Mesh.ARRAY_NORMAL<class_Mesh_constant_ARRAY_NORMAL>` is only used to
determine which faces require the use of flat shading. By default,
CSGMesh will ignore the mesh's vertex normals, recalculate them for each
vertex and use a smooth shader. If a flat shader is required for a face,
ensure that all vertex normals of the face are approximately equal.
