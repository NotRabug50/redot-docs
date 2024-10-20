github\_url  
hide

# ConvexPolygonShape3D

**Inherits:** `Shape3D<class_Shape3D>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A 3D convex polyhedron shape used for physics collision.

classref-introduction-group

## Description

A 3D convex polyhedron shape, intended for use in physics. Usually used
to provide a shape for a `CollisionShape3D<class_CollisionShape3D>`.

\*\*ConvexPolygonShape3D\*\* is *solid*, which means it detects
collisions from objects that are fully inside it, unlike
`ConcavePolygonShape3D<class_ConcavePolygonShape3D>` which is hollow.
This makes it more suitable for both detection and physics.

\*\*Convex decomposition:\*\* A concave polyhedron can be split up into
several convex polyhedra. This allows dynamic physics bodies to have
complex concave collisions (at a performance cost) and can be achieved
by using several **ConvexPolygonShape3D** nodes. To generate a convex
decomposition from a mesh, select the
`MeshInstance3D<class_MeshInstance3D>` node, go to the **Mesh** menu
that appears above the viewport, and choose **Create Multiple Convex
Collision Siblings**. Alternatively,
`MeshInstance3D.create_multiple_convex_collisions<class_MeshInstance3D_method_create_multiple_convex_collisions>`
can be called in a script to perform this decomposition at run-time.

\*\*Performance:\*\* **ConvexPolygonShape3D** is faster to check
collisions against compared to
`ConcavePolygonShape3D<class_ConcavePolygonShape3D>`, but it is slower
than primitive collision shapes such as
`SphereShape3D<class_SphereShape3D>` and `BoxShape3D<class_BoxShape3D>`.
Its use should generally be limited to medium-sized objects that cannot
have their collision accurately represented by primitive shapes.

classref-introduction-group

## Tutorials

-   [3D Physics Tests
    Demo](https://godotengine.org/asset-library/asset/2747)

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`PackedVector3Array<class_PackedVector3Array>` **points** =
`PackedVector3Array()` `🔗<class_ConvexPolygonShape3D_property_points>`

classref-property-setget

-   `void (No return value.)` **set\_points**(value:
    `PackedVector3Array<class_PackedVector3Array>`)
-   `PackedVector3Array<class_PackedVector3Array>` **get\_points**()

The list of 3D points forming the convex polygon shape.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedVector3Array<class_PackedVector3Array>` for more details.
