github\_url  
hide

# BoxShape3D

**Inherits:** `Shape3D<class_Shape3D>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A 3D box shape used for physics collision.

classref-introduction-group

## Description

A 3D box shape, intended for use in physics. Usually used to provide a
shape for a `CollisionShape3D<class_CollisionShape3D>`.

\*\*Performance:\*\* **BoxShape3D** is fast to check collisions against.
It is faster than `CapsuleShape3D<class_CapsuleShape3D>` and
`CylinderShape3D<class_CylinderShape3D>`, but slower than
`SphereShape3D<class_SphereShape3D>`.

classref-introduction-group

## Tutorials

-   [3D Physics Tests
    Demo](https://godotengine.org/asset-library/asset/2747)
-   [3D Kinematic Character
    Demo](https://godotengine.org/asset-library/asset/2739)
-   [3D Platformer
    Demo](https://godotengine.org/asset-library/asset/2748)

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

`Vector3<class_Vector3>` **size** = `Vector3(1, 1, 1)`
`🔗<class_BoxShape3D_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_size**()

The box's width, height and depth.
