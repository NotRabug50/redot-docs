github\_url  
hide

# ImmediateMesh

**Inherits:** `Mesh<class_Mesh>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Mesh optimized for creating geometry manually.

classref-introduction-group

## Description

A mesh type optimized for creating geometry manually, similar to OpenGL
1.x immediate mode.

Here's a sample on how to generate a triangular face:

gdscript

var mesh = ImmediateMesh.new()
mesh.surface\_begin(Mesh.PRIMITIVE\_TRIANGLES)
mesh.surface\_add\_vertex(Vector3.LEFT)
mesh.surface\_add\_vertex(Vector3.FORWARD)
mesh.surface\_add\_vertex(Vector3.ZERO) mesh.surface\_end()

csharp

var mesh = new ImmediateMesh();
mesh.SurfaceBegin(Mesh.PrimitiveType.Triangles);
mesh.SurfaceAddVertex(Vector3.Left);
mesh.SurfaceAddVertex(Vector3.Forward);
mesh.SurfaceAddVertex(Vector3.Zero); mesh.SurfaceEnd();

\*\*Note:\*\* Generating complex geometries with **ImmediateMesh** is
highly inefficient. Instead, it is designed to generate simple geometry
that changes often.

classref-introduction-group

## Tutorials

-   `Using ImmediateMesh <../tutorials/3d/procedural_geometry/immediatemesh>`

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

`void (No return value.)` **clear\_surfaces**()
`🔗<class_ImmediateMesh_method_clear_surfaces>`

Clear all surfaces.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **surface\_add\_vertex**(vertex:
`Vector3<class_Vector3>`)
`🔗<class_ImmediateMesh_method_surface_add_vertex>`

Add a 3D vertex using the current attributes previously set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **surface\_add\_vertex\_2d**(vertex:
`Vector2<class_Vector2>`)
`🔗<class_ImmediateMesh_method_surface_add_vertex_2d>`

Add a 2D vertex using the current attributes previously set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **surface\_begin**(primitive:
`PrimitiveType<enum_Mesh_PrimitiveType>`, material:
`Material<class_Material>` = null)
`🔗<class_ImmediateMesh_method_surface_begin>`

Begin a new surface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **surface\_end**()
`🔗<class_ImmediateMesh_method_surface_end>`

End and commit current surface. Note that surface being created will not
be visible until this function is called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **surface\_set\_color**(color:
`Color<class_Color>`) `🔗<class_ImmediateMesh_method_surface_set_color>`

Set the color attribute that will be pushed with the next vertex.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **surface\_set\_normal**(normal:
`Vector3<class_Vector3>`)
`🔗<class_ImmediateMesh_method_surface_set_normal>`

Set the normal attribute that will be pushed with the next vertex.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **surface\_set\_tangent**(tangent:
`Plane<class_Plane>`)
`🔗<class_ImmediateMesh_method_surface_set_tangent>`

Set the tangent attribute that will be pushed with the next vertex.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **surface\_set\_uv**(uv:
`Vector2<class_Vector2>`)
`🔗<class_ImmediateMesh_method_surface_set_uv>`

Set the UV attribute that will be pushed with the next vertex.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **surface\_set\_uv2**(uv2:
`Vector2<class_Vector2>`)
`🔗<class_ImmediateMesh_method_surface_set_uv2>`

Set the UV2 attribute that will be pushed with the next vertex.
