github\_url  
hide

# BoxMesh

**Inherits:** `PrimitiveMesh<class_PrimitiveMesh>` **&lt;**
`Mesh<class_Mesh>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Generate an axis-aligned box `PrimitiveMesh<class_PrimitiveMesh>`.

classref-introduction-group

## Description

Generate an axis-aligned box `PrimitiveMesh<class_PrimitiveMesh>`.

The box's UV layout is arranged in a 3×2 layout that allows texturing
each face individually. To apply the same texture on all faces, change
the material's UV property to `Vector3(3, 2, 1)`. This is equivalent to
adding `UV *= vec2(3.0, 2.0)` in a vertex shader.

\*\*Note:\*\* When using a large textured **BoxMesh** (e.g. as a floor),
you may stumble upon UV jittering issues depending on the camera angle.
To solve this, increase
`subdivide_depth<class_BoxMesh_property_subdivide_depth>`,
`subdivide_height<class_BoxMesh_property_subdivide_height>` and
`subdivide_width<class_BoxMesh_property_subdivide_width>` until you no
longer notice UV jittering.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Vector3<class_Vector3>` **size** = `Vector3(1, 1, 1)`
`🔗<class_BoxMesh_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_size**()

The box's width, height and depth.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **subdivide\_depth** = `0`
`🔗<class_BoxMesh_property_subdivide_depth>`

classref-property-setget

-   `void (No return value.)` **set\_subdivide\_depth**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_subdivide\_depth**()

Number of extra edge loops inserted along the Z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **subdivide\_height** = `0`
`🔗<class_BoxMesh_property_subdivide_height>`

classref-property-setget

-   `void (No return value.)` **set\_subdivide\_height**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_subdivide\_height**()

Number of extra edge loops inserted along the Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **subdivide\_width** = `0`
`🔗<class_BoxMesh_property_subdivide_width>`

classref-property-setget

-   `void (No return value.)` **set\_subdivide\_width**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_subdivide\_width**()

Number of extra edge loops inserted along the X axis.
