github\_url  
hide

# CollisionShape2D

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A node that provides a `Shape2D<class_Shape2D>` to a
`CollisionObject2D<class_CollisionObject2D>` parent.

classref-introduction-group

## Description

A node that provides a `Shape2D<class_Shape2D>` to a
`CollisionObject2D<class_CollisionObject2D>` parent and allows to edit
it. This can give a detection shape to an `Area2D<class_Area2D>` or turn
a `PhysicsBody2D<class_PhysicsBody2D>` into a solid object.

classref-introduction-group

## Tutorials

-   `Physics introduction <../tutorials/physics/physics_introduction>`
-   [2D Dodge The Creeps
    Demo](https://godotengine.org/asset-library/asset/2712)
-   [2D Pong Demo](https://godotengine.org/asset-library/asset/2728)
-   [2D Kinematic Character
    Demo](https://godotengine.org/asset-library/asset/2719)

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

## Property Descriptions

classref-property

`Color<class_Color>` **debug\_color** = `Color(0, 0, 0, 1)`
`🔗<class_CollisionShape2D_property_debug_color>`

classref-property-setget

-   `void (No return value.)` **set\_debug\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_debug\_color**()

The collision shape debug color.

\*\*Note:\*\* The default value is
`ProjectSettings.debug/shapes/collision/shape_color<class_ProjectSettings_property_debug/shapes/collision/shape_color>`.
The `Color(0, 0, 0, 1)` value documented here is a placeholder, and not
the actual default debug color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disabled** = `false`
`🔗<class_CollisionShape2D_property_disabled>`

classref-property-setget

-   `void (No return value.)` **set\_disabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_disabled**()

A disabled collision shape has no effect in the world. This property
should be changed with
`Object.set_deferred<class_Object_method_set_deferred>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **one\_way\_collision** = `false`
`🔗<class_CollisionShape2D_property_one_way_collision>`

classref-property-setget

-   `void (No return value.)` **set\_one\_way\_collision**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_one\_way\_collision\_enabled**()

Sets whether this collision shape should only detect collision on one
side (top or bottom).

\*\*Note:\*\* This property has no effect if this **CollisionShape2D**
is a child of an `Area2D<class_Area2D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **one\_way\_collision\_margin** = `1.0`
`🔗<class_CollisionShape2D_property_one_way_collision_margin>`

classref-property-setget

-   `void (No return value.)`
    **set\_one\_way\_collision\_margin**(value: `float<class_float>`)
-   `float<class_float>` **get\_one\_way\_collision\_margin**()

The margin used for one-way collision (in pixels). Higher values will
make the shape thicker, and work better for colliders that enter the
shape at a high velocity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Shape2D<class_Shape2D>` **shape**
`🔗<class_CollisionShape2D_property_shape>`

classref-property-setget

-   `void (No return value.)` **set\_shape**(value:
    `Shape2D<class_Shape2D>`)
-   `Shape2D<class_Shape2D>` **get\_shape**()

The actual shape owned by this collision shape.
