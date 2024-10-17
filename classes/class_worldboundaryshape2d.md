github\_url  
hide

# WorldBoundaryShape2D

**Inherits:** `Shape2D<class_Shape2D>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A 2D world boundary (half-plane) shape used for physics collision.

classref-introduction-group

## Description

A 2D world boundary shape, intended for use in physics.
**WorldBoundaryShape2D** works like an infinite straight line that
forces all physics bodies to stay above it. The line's normal determines
which direction is considered as "above" and in the editor, the smaller
line over it represents this direction. It can for example be used for
endless flat floors.

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

`float<class_float>` **distance** = `0.0`
`🔗<class_WorldBoundaryShape2D_property_distance>`

classref-property-setget

-   `void (No return value.)` **set\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_distance**()

The distance from the origin to the line, expressed in terms of
`normal<class_WorldBoundaryShape2D_property_normal>` (according to its
direction and magnitude). Actual absolute distance from the origin to
the line can be calculated as `abs(distance) / normal.length()`.

In the scalar equation of the line `ax + by = d`, this is `d`, while the
`(a, b)` coordinates are represented by the
`normal<class_WorldBoundaryShape2D_property_normal>` property.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **normal** = `Vector2(0, -1)`
`🔗<class_WorldBoundaryShape2D_property_normal>`

classref-property-setget

-   `void (No return value.)` **set\_normal**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_normal**()

The line's normal, typically a unit vector. Its direction indicates the
non-colliding half-plane. Can be of any length but zero. Defaults to
`Vector2.UP<class_Vector2_constant_UP>`.
