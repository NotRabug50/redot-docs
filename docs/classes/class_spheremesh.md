github\_url  
hide

# SphereMesh

**Inherits:** `PrimitiveMesh<class_PrimitiveMesh>` **&lt;**
`Mesh<class_Mesh>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Class representing a spherical `PrimitiveMesh<class_PrimitiveMesh>`.

classref-introduction-group

## Description

Class representing a spherical `PrimitiveMesh<class_PrimitiveMesh>`.

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

`float<class_float>` **height** = `1.0`
`🔗<class_SphereMesh_property_height>`

classref-property-setget

-   `void (No return value.)` **set\_height**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_height**()

Full height of the sphere.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **is\_hemisphere** = `false`
`🔗<class_SphereMesh_property_is_hemisphere>`

classref-property-setget

-   `void (No return value.)` **set\_is\_hemisphere**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_is\_hemisphere**()

If `true`, a hemisphere is created rather than a full sphere.

\*\*Note:\*\* To get a regular hemisphere, the height and radius of the
sphere must be equal.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **radial\_segments** = `64`
`🔗<class_SphereMesh_property_radial_segments>`

classref-property-setget

-   `void (No return value.)` **set\_radial\_segments**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_radial\_segments**()

Number of radial segments on the sphere.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radius** = `0.5`
`🔗<class_SphereMesh_property_radius>`

classref-property-setget

-   `void (No return value.)` **set\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_radius**()

Radius of sphere.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **rings** = `32` `🔗<class_SphereMesh_property_rings>`

classref-property-setget

-   `void (No return value.)` **set\_rings**(value: `int<class_int>`)
-   `int<class_int>` **get\_rings**()

Number of segments along the height of the sphere.
