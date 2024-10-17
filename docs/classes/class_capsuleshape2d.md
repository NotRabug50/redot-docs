github\_url  
hide

# CapsuleShape2D

**Inherits:** `Shape2D<class_Shape2D>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A 2D capsule shape used for physics collision.

classref-introduction-group

## Description

A 2D capsule shape, intended for use in physics. Usually used to provide
a shape for a `CollisionShape2D<class_CollisionShape2D>`.

\*\*Performance:\*\* **CapsuleShape2D** is fast to check collisions
against, but it is slower than
`RectangleShape2D<class_RectangleShape2D>` and
`CircleShape2D<class_CircleShape2D>`.

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

`float<class_float>` **height** = `30.0`
`🔗<class_CapsuleShape2D_property_height>`

classref-property-setget

-   `void (No return value.)` **set\_height**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_height**()

The capsule's height.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radius** = `10.0`
`🔗<class_CapsuleShape2D_property_radius>`

classref-property-setget

-   `void (No return value.)` **set\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_radius**()

The capsule's radius.
