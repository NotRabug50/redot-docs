github\_url  
hide

# CSGPrimitive3D

**Inherits:** `CSGShape3D<class_CSGShape3D>` **&lt;**
`GeometryInstance3D<class_GeometryInstance3D>` **&lt;**
`VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `CSGBox3D<class_CSGBox3D>`,
`CSGCylinder3D<class_CSGCylinder3D>`, `CSGMesh3D<class_CSGMesh3D>`,
`CSGPolygon3D<class_CSGPolygon3D>`, `CSGSphere3D<class_CSGSphere3D>`,
`CSGTorus3D<class_CSGTorus3D>`

Base class for CSG primitives.

classref-introduction-group

## Description

Parent class for various CSG primitives. It contains code and
functionality that is common between them. It cannot be used directly.
Instead use one of the various classes that inherit from it.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **flip\_faces** = `false`
`🔗<class_CSGPrimitive3D_property_flip_faces>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_faces**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_flip\_faces**()

If set, the order of the vertices in each triangle are reversed
resulting in the backside of the mesh being drawn.
