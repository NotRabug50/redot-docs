github\_url  
hide

# PlaneMesh

**Inherits:** `PrimitiveMesh<class_PrimitiveMesh>` **&lt;**
`Mesh<class_Mesh>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `QuadMesh<class_QuadMesh>`

Class representing a planar `PrimitiveMesh<class_PrimitiveMesh>`.

classref-introduction-group

## Description

Class representing a planar `PrimitiveMesh<class_PrimitiveMesh>`. This
flat mesh does not have a thickness. By default, this mesh is aligned on
the X and Z axes; this default rotation isn't suited for use with
billboarded materials. For billboarded materials, change
`orientation<class_PlaneMesh_property_orientation>` to
`FACE_Z<class_PlaneMesh_constant_FACE_Z>`.

\*\*Note:\*\* When using a large textured **PlaneMesh** (e.g. as a
floor), you may stumble upon UV jittering issues depending on the camera
angle. To solve this, increase
`subdivide_depth<class_PlaneMesh_property_subdivide_depth>` and
`subdivide_width<class_PlaneMesh_property_subdivide_width>` until you no
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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Orientation**: `🔗<enum_PlaneMesh_Orientation>`

classref-enumeration-constant

`Orientation<enum_PlaneMesh_Orientation>` **FACE\_X** = `0`

**PlaneMesh** will face the positive X-axis.

classref-enumeration-constant

`Orientation<enum_PlaneMesh_Orientation>` **FACE\_Y** = `1`

**PlaneMesh** will face the positive Y-axis. This matches the behavior
of the **PlaneMesh** in Godot 3.x.

classref-enumeration-constant

`Orientation<enum_PlaneMesh_Orientation>` **FACE\_Z** = `2`

**PlaneMesh** will face the positive Z-axis. This matches the behavior
of the QuadMesh in Godot 3.x.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Vector3<class_Vector3>` **center\_offset** = `Vector3(0, 0, 0)`
`🔗<class_PlaneMesh_property_center_offset>`

classref-property-setget

-   `void (No return value.)` **set\_center\_offset**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_center\_offset**()

Offset of the generated plane. Useful for particles.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Orientation<enum_PlaneMesh_Orientation>` **orientation** = `1`
`🔗<class_PlaneMesh_property_orientation>`

classref-property-setget

-   `void (No return value.)` **set\_orientation**(value:
    `Orientation<enum_PlaneMesh_Orientation>`)
-   `Orientation<enum_PlaneMesh_Orientation>` **get\_orientation**()

Direction that the **PlaneMesh** is facing. See
`Orientation<enum_PlaneMesh_Orientation>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **size** = `Vector2(2, 2)`
`🔗<class_PlaneMesh_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_size**()

Size of the generated plane.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **subdivide\_depth** = `0`
`🔗<class_PlaneMesh_property_subdivide_depth>`

classref-property-setget

-   `void (No return value.)` **set\_subdivide\_depth**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_subdivide\_depth**()

Number of subdivision along the Z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **subdivide\_width** = `0`
`🔗<class_PlaneMesh_property_subdivide_width>`

classref-property-setget

-   `void (No return value.)` **set\_subdivide\_width**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_subdivide\_width**()

Number of subdivision along the X axis.
