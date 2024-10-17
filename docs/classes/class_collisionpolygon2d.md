github\_url  
hide

# CollisionPolygon2D

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A node that provides a polygon shape to a
`CollisionObject2D<class_CollisionObject2D>` parent.

classref-introduction-group

## Description

A node that provides a polygon shape to a
`CollisionObject2D<class_CollisionObject2D>` parent and allows to edit
it. The polygon can be concave or convex. This can give a detection
shape to an `Area2D<class_Area2D>`, turn
`PhysicsBody2D<class_PhysicsBody2D>` into a solid object, or give a
hollow shape to a `StaticBody2D<class_StaticBody2D>`.

\*\*Warning:\*\* A non-uniformly scaled
`CollisionShape2D<class_CollisionShape2D>` will likely not behave as
expected. Make sure to keep its scale the same on all axes and adjust
its shape resource instead.

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

enum **BuildMode**: `🔗<enum_CollisionPolygon2D_BuildMode>`

classref-enumeration-constant

`BuildMode<enum_CollisionPolygon2D_BuildMode>` **BUILD\_SOLIDS** = `0`

Collisions will include the polygon and its contained area. In this mode
the node has the same effect as several
`ConvexPolygonShape2D<class_ConvexPolygonShape2D>` nodes, one for each
convex shape in the convex decomposition of the polygon (but without the
overhead of multiple nodes).

classref-enumeration-constant

`BuildMode<enum_CollisionPolygon2D_BuildMode>` **BUILD\_SEGMENTS** = `1`

Collisions will only include the polygon edges. In this mode the node
has the same effect as a single
`ConcavePolygonShape2D<class_ConcavePolygonShape2D>` made of segments,
with the restriction that each segment (after the first one) starts
where the previous one ends, and the last one ends where the first one
starts (forming a closed but hollow polygon).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`BuildMode<enum_CollisionPolygon2D_BuildMode>` **build\_mode** = `0`
`🔗<class_CollisionPolygon2D_property_build_mode>`

classref-property-setget

-   `void (No return value.)` **set\_build\_mode**(value:
    `BuildMode<enum_CollisionPolygon2D_BuildMode>`)
-   `BuildMode<enum_CollisionPolygon2D_BuildMode>`
    **get\_build\_mode**()

Collision build mode. Use one of the
`BuildMode<enum_CollisionPolygon2D_BuildMode>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disabled** = `false`
`🔗<class_CollisionPolygon2D_property_disabled>`

classref-property-setget

-   `void (No return value.)` **set\_disabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_disabled**()

If `true`, no collisions will be detected.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **one\_way\_collision** = `false`
`🔗<class_CollisionPolygon2D_property_one_way_collision>`

classref-property-setget

-   `void (No return value.)` **set\_one\_way\_collision**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_one\_way\_collision\_enabled**()

If `true`, only edges that face up, relative to **CollisionPolygon2D**'s
rotation, will collide with other objects.

\*\*Note:\*\* This property has no effect if this **CollisionPolygon2D**
is a child of an `Area2D<class_Area2D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **one\_way\_collision\_margin** = `1.0`
`🔗<class_CollisionPolygon2D_property_one_way_collision_margin>`

classref-property-setget

-   `void (No return value.)`
    **set\_one\_way\_collision\_margin**(value: `float<class_float>`)
-   `float<class_float>` **get\_one\_way\_collision\_margin**()

The margin used for one-way collision (in pixels). Higher values will
make the shape thicker, and work better for colliders that enter the
polygon at a high velocity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedVector2Array<class_PackedVector2Array>` **polygon** =
`PackedVector2Array()` `🔗<class_CollisionPolygon2D_property_polygon>`

classref-property-setget

-   `void (No return value.)` **set\_polygon**(value:
    `PackedVector2Array<class_PackedVector2Array>`)
-   `PackedVector2Array<class_PackedVector2Array>` **get\_polygon**()

The polygon's list of vertices. Each point will be connected to the
next, and the final point will be connected to the first.

\*\*Note:\*\* The returned vertices are in the local coordinate space of
the given **CollisionPolygon2D**.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedVector2Array<class_PackedVector2Array>` for more details.
