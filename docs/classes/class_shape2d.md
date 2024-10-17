github\_url  
hide

# Shape2D

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `CapsuleShape2D<class_CapsuleShape2D>`,
`CircleShape2D<class_CircleShape2D>`,
`ConcavePolygonShape2D<class_ConcavePolygonShape2D>`,
`ConvexPolygonShape2D<class_ConvexPolygonShape2D>`,
`RectangleShape2D<class_RectangleShape2D>`,
`SegmentShape2D<class_SegmentShape2D>`,
`SeparationRayShape2D<class_SeparationRayShape2D>`,
`WorldBoundaryShape2D<class_WorldBoundaryShape2D>`

Abstract base class for 2D shapes used for physics collision.

classref-introduction-group

## Description

Abstract base class for all 2D shapes, intended for use in physics.

\*\*Performance:\*\* Primitive shapes, especially
`CircleShape2D<class_CircleShape2D>`, are fast to check collisions
against. `ConvexPolygonShape2D<class_ConvexPolygonShape2D>` is slower,
and `ConcavePolygonShape2D<class_ConcavePolygonShape2D>` is the slowest.

classref-introduction-group

## Tutorials

-   `Physics introduction <../tutorials/physics/physics_introduction>`

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-reftable-group

## Methods

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **custom\_solver\_bias** = `0.0`
`🔗<class_Shape2D_property_custom_solver_bias>`

classref-property-setget

-   `void (No return value.)` **set\_custom\_solver\_bias**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_custom\_solver\_bias**()

The shape's custom solver bias. Defines how much bodies react to enforce
contact separation when this shape is involved.

When set to `0`, the default value from
`ProjectSettings.physics/2d/solver/default_contact_bias<class_ProjectSettings_property_physics/2d/solver/default_contact_bias>`
is used.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **collide**(local\_xform:
`Transform2D<class_Transform2D>`, with\_shape: `Shape2D<class_Shape2D>`,
shape\_xform: `Transform2D<class_Transform2D>`)
`🔗<class_Shape2D_method_collide>`

Returns `true` if this shape is colliding with another.

This method needs the transformation matrix for this shape
(`local_xform`), the shape to check collisions with (`with_shape`), and
the transformation matrix of that shape (`shape_xform`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**collide\_and\_get\_contacts**(local\_xform:
`Transform2D<class_Transform2D>`, with\_shape: `Shape2D<class_Shape2D>`,
shape\_xform: `Transform2D<class_Transform2D>`)
`🔗<class_Shape2D_method_collide_and_get_contacts>`

Returns a list of contact point pairs where this shape touches another.

If there are no collisions, the returned list is empty. Otherwise, the
returned list contains contact points arranged in pairs, with entries
alternating between points on the boundary of this shape and points on
the boundary of `with_shape`.

A collision pair A, B can be used to calculate the collision normal with
`(B - A).normalized()`, and the collision depth with `(B - A).length()`.
This information is typically used to separate shapes, particularly in
collision solvers.

This method needs the transformation matrix for this shape
(`local_xform`), the shape to check collisions with (`with_shape`), and
the transformation matrix of that shape (`shape_xform`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **collide\_with\_motion**(local\_xform:
`Transform2D<class_Transform2D>`, local\_motion:
`Vector2<class_Vector2>`, with\_shape: `Shape2D<class_Shape2D>`,
shape\_xform: `Transform2D<class_Transform2D>`, shape\_motion:
`Vector2<class_Vector2>`) `🔗<class_Shape2D_method_collide_with_motion>`

Returns whether this shape would collide with another, if a given
movement was applied.

This method needs the transformation matrix for this shape
(`local_xform`), the movement to test on this shape (`local_motion`),
the shape to check collisions with (`with_shape`), the transformation
matrix of that shape (`shape_xform`), and the movement to test onto the
other object (`shape_motion`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**collide\_with\_motion\_and\_get\_contacts**(local\_xform:
`Transform2D<class_Transform2D>`, local\_motion:
`Vector2<class_Vector2>`, with\_shape: `Shape2D<class_Shape2D>`,
shape\_xform: `Transform2D<class_Transform2D>`, shape\_motion:
`Vector2<class_Vector2>`)
`🔗<class_Shape2D_method_collide_with_motion_and_get_contacts>`

Returns a list of contact point pairs where this shape would touch
another, if a given movement was applied.

If there would be no collisions, the returned list is empty. Otherwise,
the returned list contains contact points arranged in pairs, with
entries alternating between points on the boundary of this shape and
points on the boundary of `with_shape`.

A collision pair A, B can be used to calculate the collision normal with
`(B - A).normalized()`, and the collision depth with `(B - A).length()`.
This information is typically used to separate shapes, particularly in
collision solvers.

This method needs the transformation matrix for this shape
(`local_xform`), the movement to test on this shape (`local_motion`),
the shape to check collisions with (`with_shape`), the transformation
matrix of that shape (`shape_xform`), and the movement to test onto the
other object (`shape_motion`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw**(canvas\_item: `RID<class_RID>`,
color: `Color<class_Color>`) `🔗<class_Shape2D_method_draw>`

Draws a solid shape onto a `CanvasItem<class_CanvasItem>` with the
`RenderingServer<class_RenderingServer>` API filled with the specified
`color`. The exact drawing method is specific for each shape and cannot
be configured.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_rect**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Shape2D_method_get_rect>`

Returns a `Rect2<class_Rect2>` representing the shapes boundary.
