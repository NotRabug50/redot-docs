github\_url  
hide

# CollisionPolygon3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A node that provides a thickened polygon shape (a prism) to a
`CollisionObject3D<class_CollisionObject3D>` parent.

classref-introduction-group

## Description

A node that provides a thickened polygon shape (a prism) to a
`CollisionObject3D<class_CollisionObject3D>` parent and allows to edit
it. The polygon can be concave or convex. This can give a detection
shape to an `Area3D<class_Area3D>` or turn
`PhysicsBody3D<class_PhysicsBody3D>` into a solid object.

\*\*Warning:\*\* A non-uniformly scaled
`CollisionShape3D<class_CollisionShape3D>` will likely not behave as
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **depth** = `1.0`
`🔗<class_CollisionPolygon3D_property_depth>`

classref-property-setget

-   `void (No return value.)` **set\_depth**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_depth**()

Length that the resulting collision extends in either direction
perpendicular to its 2D polygon.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disabled** = `false`
`🔗<class_CollisionPolygon3D_property_disabled>`

classref-property-setget

-   `void (No return value.)` **set\_disabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_disabled**()

If `true`, no collision will be produced.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **margin** = `0.04`
`🔗<class_CollisionPolygon3D_property_margin>`

classref-property-setget

-   `void (No return value.)` **set\_margin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_margin**()

The collision margin for the generated `Shape3D<class_Shape3D>`. See
`Shape3D.margin<class_Shape3D_property_margin>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedVector2Array<class_PackedVector2Array>` **polygon** =
`PackedVector2Array()` `🔗<class_CollisionPolygon3D_property_polygon>`

classref-property-setget

-   `void (No return value.)` **set\_polygon**(value:
    `PackedVector2Array<class_PackedVector2Array>`)
-   `PackedVector2Array<class_PackedVector2Array>` **get\_polygon**()

Array of vertices which define the 2D polygon in the local XY plane.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedVector2Array<class_PackedVector2Array>` for more details.
