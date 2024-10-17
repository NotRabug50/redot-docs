github\_url  
hide

# ConvexPolygonShape2D

**Inherits:** `Shape2D<class_Shape2D>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A 2D convex polygon shape used for physics collision.

classref-introduction-group

## Description

A 2D convex polygon shape, intended for use in physics. Used internally
in `CollisionPolygon2D<class_CollisionPolygon2D>` when it's in
`CollisionPolygon2D.BUILD_SOLIDS<class_CollisionPolygon2D_constant_BUILD_SOLIDS>`
mode.

\*\*ConvexPolygonShape2D\*\* is *solid*, which means it detects
collisions from objects that are fully inside it, unlike
`ConcavePolygonShape2D<class_ConcavePolygonShape2D>` which is hollow.
This makes it more suitable for both detection and physics.

\*\*Convex decomposition:\*\* A concave polygon can be split up into
several convex polygons. This allows dynamic physics bodies to have
complex concave collisions (at a performance cost) and can be achieved
by using several **ConvexPolygonShape2D** nodes or by using the
`CollisionPolygon2D<class_CollisionPolygon2D>` node in
`CollisionPolygon2D.BUILD_SOLIDS<class_CollisionPolygon2D_constant_BUILD_SOLIDS>`
mode. To generate a collision polygon from a sprite, select the
`Sprite2D<class_Sprite2D>` node, go to the **Sprite2D** menu that
appears above the viewport, and choose **Create Polygon2D Sibling**.

\*\*Performance:\*\* **ConvexPolygonShape2D** is faster to check
collisions against compared to
`ConcavePolygonShape2D<class_ConcavePolygonShape2D>`, but it is slower
than primitive collision shapes such as
`CircleShape2D<class_CircleShape2D>` and
`RectangleShape2D<class_RectangleShape2D>`. Its use should generally be
limited to medium-sized objects that cannot have their collision
accurately represented by primitive shapes.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`PackedVector2Array<class_PackedVector2Array>` **points** =
`PackedVector2Array()` `🔗<class_ConvexPolygonShape2D_property_points>`

classref-property-setget

-   `void (No return value.)` **set\_points**(value:
    `PackedVector2Array<class_PackedVector2Array>`)
-   `PackedVector2Array<class_PackedVector2Array>` **get\_points**()

The polygon's list of vertices that form a convex hull. Can be in either
clockwise or counterclockwise order.

\*\*Warning:\*\* Only set this property to a list of points that
actually form a convex hull. Use
`set_point_cloud<class_ConvexPolygonShape2D_method_set_point_cloud>` to
generate the convex hull of an arbitrary set of points.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedVector2Array<class_PackedVector2Array>` for more details.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **set\_point\_cloud**(point\_cloud:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_ConvexPolygonShape2D_method_set_point_cloud>`

Based on the set of points provided, this assigns the
`points<class_ConvexPolygonShape2D_property_points>` property using the
convex hull algorithm, removing all unneeded points. See
`Geometry2D.convex_hull<class_Geometry2D_method_convex_hull>` for
details.
