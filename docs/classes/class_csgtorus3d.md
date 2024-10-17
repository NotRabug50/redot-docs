github\_url  
hide

# CSGTorus3D

**Inherits:** `CSGPrimitive3D<class_CSGPrimitive3D>` **&lt;**
`CSGShape3D<class_CSGShape3D>` **&lt;**
`GeometryInstance3D<class_GeometryInstance3D>` **&lt;**
`VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A CSG Torus shape.

classref-introduction-group

## Description

This node allows you to create a torus for use with the CSG system.

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **inner\_radius** = `0.5`
`🔗<class_CSGTorus3D_property_inner_radius>`

classref-property-setget

-   `void (No return value.)` **set\_inner\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_inner\_radius**()

The inner radius of the torus.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Material<class_Material>` **material**
`🔗<class_CSGTorus3D_property_material>`

classref-property-setget

-   `void (No return value.)` **set\_material**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_material**()

The material used to render the torus.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **outer\_radius** = `1.0`
`🔗<class_CSGTorus3D_property_outer_radius>`

classref-property-setget

-   `void (No return value.)` **set\_outer\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_outer\_radius**()

The outer radius of the torus.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **ring\_sides** = `6`
`🔗<class_CSGTorus3D_property_ring_sides>`

classref-property-setget

-   `void (No return value.)` **set\_ring\_sides**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_ring\_sides**()

The number of edges each ring of the torus is constructed of.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sides** = `8` `🔗<class_CSGTorus3D_property_sides>`

classref-property-setget

-   `void (No return value.)` **set\_sides**(value: `int<class_int>`)
-   `int<class_int>` **get\_sides**()

The number of slices the torus is constructed of.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **smooth\_faces** = `true`
`🔗<class_CSGTorus3D_property_smooth_faces>`

classref-property-setget

-   `void (No return value.)` **set\_smooth\_faces**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_smooth\_faces**()

If `true` the normals of the torus are set to give a smooth effect
making the torus seem rounded. If `false` the torus will have a flat
shaded look.
