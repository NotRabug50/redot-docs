github\_url  
hide

# Path2D

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Contains a `Curve2D<class_Curve2D>` path for
`PathFollow2D<class_PathFollow2D>` nodes to follow.

classref-introduction-group

## Description

Can have `PathFollow2D<class_PathFollow2D>` child nodes moving along the
`Curve2D<class_Curve2D>`. See `PathFollow2D<class_PathFollow2D>` for
more information on usage.

\*\*Note:\*\* The path is considered as relative to the moved nodes
(children of `PathFollow2D<class_PathFollow2D>`). As such, the curve
should usually start with a zero vector (`(0, 0)`).

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

`Curve2D<class_Curve2D>` **curve** `🔗<class_Path2D_property_curve>`

classref-property-setget

-   `void (No return value.)` **set\_curve**(value:
    `Curve2D<class_Curve2D>`)
-   `Curve2D<class_Curve2D>` **get\_curve**()

A `Curve2D<class_Curve2D>` describing the path.
