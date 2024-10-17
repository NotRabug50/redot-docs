github\_url  
hide

# TubeTrailMesh

**Inherits:** `PrimitiveMesh<class_PrimitiveMesh>` **&lt;**
`Mesh<class_Mesh>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Represents a straight tube-shaped `PrimitiveMesh<class_PrimitiveMesh>`
with variable width.

classref-introduction-group

## Description

**TubeTrailMesh** represents a straight tube-shaped mesh with variable
width. The tube is composed of a number of cylindrical sections, each
with the same
`section_length<class_TubeTrailMesh_property_section_length>` and number
of `section_rings<class_TubeTrailMesh_property_section_rings>`. A
`curve<class_TubeTrailMesh_property_curve>` is sampled along the total
length of the tube, meaning that the curve determines the radius of the
tube along its length.

This primitive mesh is usually used for particle trails.

classref-introduction-group

## Tutorials

-   `3D Particle trails <../tutorials/3d/particles/trails>`
-   `Particle systems (3D) <../tutorials/3d/particles/index>`

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **cap\_bottom** = `true`
`🔗<class_TubeTrailMesh_property_cap_bottom>`

classref-property-setget

-   `void (No return value.)` **set\_cap\_bottom**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_cap\_bottom**()

If `true`, generates a cap at the bottom of the tube. This can be set to
`false` to speed up generation and rendering when the cap is never seen
by the camera.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **cap\_top** = `true`
`🔗<class_TubeTrailMesh_property_cap_top>`

classref-property-setget

-   `void (No return value.)` **set\_cap\_top**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_cap\_top**()

If `true`, generates a cap at the top of the tube. This can be set to
`false` to speed up generation and rendering when the cap is never seen
by the camera.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Curve<class_Curve>` **curve** `🔗<class_TubeTrailMesh_property_curve>`

classref-property-setget

-   `void (No return value.)` **set\_curve**(value:
    `Curve<class_Curve>`)
-   `Curve<class_Curve>` **get\_curve**()

Determines the radius of the tube along its length. The radius of a
particular section ring is obtained by multiplying the baseline
`radius<class_TubeTrailMesh_property_radius>` by the value of this curve
at the given distance. For values smaller than `0`, the faces will be
inverted.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **radial\_steps** = `8`
`🔗<class_TubeTrailMesh_property_radial_steps>`

classref-property-setget

-   `void (No return value.)` **set\_radial\_steps**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_radial\_steps**()

The number of sides on the tube. For example, a value of `5` means the
tube will be pentagonal. Higher values result in a more detailed tube at
the cost of performance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radius** = `0.5`
`🔗<class_TubeTrailMesh_property_radius>`

classref-property-setget

-   `void (No return value.)` **set\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_radius**()

The baseline radius of the tube. The radius of a particular section ring
is obtained by multiplying this radius by the value of the
`curve<class_TubeTrailMesh_property_curve>` at the given distance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **section\_length** = `0.2`
`🔗<class_TubeTrailMesh_property_section_length>`

classref-property-setget

-   `void (No return value.)` **set\_section\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_section\_length**()

The length of a section of the tube.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **section\_rings** = `3`
`🔗<class_TubeTrailMesh_property_section_rings>`

classref-property-setget

-   `void (No return value.)` **set\_section\_rings**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_section\_rings**()

The number of rings in a section. The
`curve<class_TubeTrailMesh_property_curve>` is sampled on each ring to
determine its radius. Higher values result in a more detailed tube at
the cost of performance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sections** = `5`
`🔗<class_TubeTrailMesh_property_sections>`

classref-property-setget

-   `void (No return value.)` **set\_sections**(value: `int<class_int>`)
-   `int<class_int>` **get\_sections**()

The total number of sections on the tube.
