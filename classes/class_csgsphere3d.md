github\_url  
hide

# CSGSphere3D

**Inherits:** `CSGPrimitive3D<class_CSGPrimitive3D>` **&lt;**
`CSGShape3D<class_CSGShape3D>` **&lt;**
`GeometryInstance3D<class_GeometryInstance3D>` **&lt;**
`VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A CSG Sphere shape.

classref-introduction-group

## Description

This node allows you to create a sphere for use with the CSG system.

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

`Material<class_Material>` **material**
`🔗<class_CSGSphere3D_property_material>`

classref-property-setget

-   `void (No return value.)` **set\_material**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_material**()

The material used to render the sphere.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **radial\_segments** = `12`
`🔗<class_CSGSphere3D_property_radial_segments>`

classref-property-setget

-   `void (No return value.)` **set\_radial\_segments**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_radial\_segments**()

Number of vertical slices for the sphere.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radius** = `0.5`
`🔗<class_CSGSphere3D_property_radius>`

classref-property-setget

-   `void (No return value.)` **set\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_radius**()

Radius of the sphere.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **rings** = `6` `🔗<class_CSGSphere3D_property_rings>`

classref-property-setget

-   `void (No return value.)` **set\_rings**(value: `int<class_int>`)
-   `int<class_int>` **get\_rings**()

Number of horizontal slices for the sphere.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **smooth\_faces** = `true`
`🔗<class_CSGSphere3D_property_smooth_faces>`

classref-property-setget

-   `void (No return value.)` **set\_smooth\_faces**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_smooth\_faces**()

If `true` the normals of the sphere are set to give a smooth effect
making the sphere seem rounded. If `false` the sphere will have a flat
shaded look.
