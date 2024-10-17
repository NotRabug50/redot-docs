github\_url  
hide

# SeparationRayShape3D

**Inherits:** `Shape3D<class_Shape3D>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A 3D ray shape used for physics collision that tries to separate itself
from any collider.

classref-introduction-group

## Description

A 3D ray shape, intended for use in physics. Usually used to provide a
shape for a `CollisionShape3D<class_CollisionShape3D>`. When a
**SeparationRayShape3D** collides with an object, it tries to separate
itself from it by moving its endpoint to the collision point. For
example, a **SeparationRayShape3D** next to a character can allow it to
instantly move up when touching stairs.

classref-reftable-group

## Properties

<table>
<tbody>
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

`float<class_float>` **length** = `1.0`
`🔗<class_SeparationRayShape3D_property_length>`

classref-property-setget

-   `void (No return value.)` **set\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_length**()

The ray's length.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **slide\_on\_slope** = `false`
`🔗<class_SeparationRayShape3D_property_slide_on_slope>`

classref-property-setget

-   `void (No return value.)` **set\_slide\_on\_slope**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_slide\_on\_slope**()

If `false` (default), the shape always separates and returns a normal
along its own direction.

If `true`, the shape can return the correct normal and separate in any
direction, allowing sliding motion on slopes.
