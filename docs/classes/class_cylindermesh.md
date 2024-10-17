github\_url  
hide

# CylinderMesh

**Inherits:** `PrimitiveMesh<class_PrimitiveMesh>` **&lt;**
`Mesh<class_Mesh>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Class representing a cylindrical `PrimitiveMesh<class_PrimitiveMesh>`.

classref-introduction-group

## Description

Class representing a cylindrical `PrimitiveMesh<class_PrimitiveMesh>`.
This class can be used to create cones by setting either the
`top_radius<class_CylinderMesh_property_top_radius>` or
`bottom_radius<class_CylinderMesh_property_bottom_radius>` properties to
`0.0`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **bottom\_radius** = `0.5`
`🔗<class_CylinderMesh_property_bottom_radius>`

classref-property-setget

-   `void (No return value.)` **set\_bottom\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_bottom\_radius**()

Bottom radius of the cylinder. If set to `0.0`, the bottom faces will
not be generated, resulting in a conic shape. See also
`cap_bottom<class_CylinderMesh_property_cap_bottom>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **cap\_bottom** = `true`
`🔗<class_CylinderMesh_property_cap_bottom>`

classref-property-setget

-   `void (No return value.)` **set\_cap\_bottom**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_cap\_bottom**()

If `true`, generates a cap at the bottom of the cylinder. This can be
set to `false` to speed up generation and rendering when the cap is
never seen by the camera. See also
`bottom_radius<class_CylinderMesh_property_bottom_radius>`.

\*\*Note:\*\* If
`bottom_radius<class_CylinderMesh_property_bottom_radius>` is `0.0`, cap
generation is always skipped even if
`cap_bottom<class_CylinderMesh_property_cap_bottom>` is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **cap\_top** = `true`
`🔗<class_CylinderMesh_property_cap_top>`

classref-property-setget

-   `void (No return value.)` **set\_cap\_top**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_cap\_top**()

If `true`, generates a cap at the top of the cylinder. This can be set
to `false` to speed up generation and rendering when the cap is never
seen by the camera. See also
`top_radius<class_CylinderMesh_property_top_radius>`.

\*\*Note:\*\* If `top_radius<class_CylinderMesh_property_top_radius>` is
`0.0`, cap generation is always skipped even if
`cap_top<class_CylinderMesh_property_cap_top>` is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **height** = `2.0`
`🔗<class_CylinderMesh_property_height>`

classref-property-setget

-   `void (No return value.)` **set\_height**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_height**()

Full height of the cylinder.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **radial\_segments** = `64`
`🔗<class_CylinderMesh_property_radial_segments>`

classref-property-setget

-   `void (No return value.)` **set\_radial\_segments**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_radial\_segments**()

Number of radial segments on the cylinder. Higher values result in a
more detailed cylinder/cone at the cost of performance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **rings** = `4` `🔗<class_CylinderMesh_property_rings>`

classref-property-setget

-   `void (No return value.)` **set\_rings**(value: `int<class_int>`)
-   `int<class_int>` **get\_rings**()

Number of edge rings along the height of the cylinder. Changing
`rings<class_CylinderMesh_property_rings>` does not have any visual
impact unless a shader or procedural mesh tool is used to alter the
vertex data. Higher values result in more subdivisions, which can be
used to create smoother-looking effects with shaders or procedural mesh
tools (at the cost of performance). When not altering the vertex data
using a shader or procedural mesh tool,
`rings<class_CylinderMesh_property_rings>` should be kept to its default
value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **top\_radius** = `0.5`
`🔗<class_CylinderMesh_property_top_radius>`

classref-property-setget

-   `void (No return value.)` **set\_top\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_top\_radius**()

Top radius of the cylinder. If set to `0.0`, the top faces will not be
generated, resulting in a conic shape. See also
`cap_top<class_CylinderMesh_property_cap_top>`.
