github\_url  
hide

# WorldBoundaryShape3D

**Inherits:** `Shape3D<class_Shape3D>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A 3D world boundary (half-space) shape used for physics collision.

classref-introduction-group

## Description

A 3D world boundary shape, intended for use in physics.
**WorldBoundaryShape3D** works like an infinite plane that forces all
physics bodies to stay above it. The
`plane<class_WorldBoundaryShape3D_property_plane>`'s normal determines
which direction is considered as "above" and in the editor, the line
over the plane represents this direction. It can for example be used for
endless flat floors.

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

`Plane<class_Plane>` **plane** = `Plane(0, 1, 0, 0)`
`🔗<class_WorldBoundaryShape3D_property_plane>`

classref-property-setget

-   `void (No return value.)` **set\_plane**(value:
    `Plane<class_Plane>`)
-   `Plane<class_Plane>` **get\_plane**()

The `Plane<class_Plane>` used by the **WorldBoundaryShape3D** for
collision.
