github\_url  
hide

# SphereShape3D

**Inherits:** `Shape3D<class_Shape3D>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A 3D sphere shape used for physics collision.

classref-introduction-group

## Description

A 3D sphere shape, intended for use in physics. Usually used to provide
a shape for a `CollisionShape3D<class_CollisionShape3D>`.

\*\*Performance:\*\* **SphereShape3D** is fast to check collisions
against. It is faster than `BoxShape3D<class_BoxShape3D>`,
`CapsuleShape3D<class_CapsuleShape3D>`, and
`CylinderShape3D<class_CylinderShape3D>`.

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

`float<class_float>` **radius** = `0.5`
`🔗<class_SphereShape3D_property_radius>`

classref-property-setget

-   `void (No return value.)` **set\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_radius**()

The sphere's radius. The shape's diameter is double the radius.
