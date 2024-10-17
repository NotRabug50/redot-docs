github\_url  
hide

# Path3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

Contains a `Curve3D<class_Curve3D>` path for
`PathFollow3D<class_PathFollow3D>` nodes to follow.

classref-introduction-group

## Description

Can have `PathFollow3D<class_PathFollow3D>` child nodes moving along the
`Curve3D<class_Curve3D>`. See `PathFollow3D<class_PathFollow3D>` for
more information on the usage.

Note that the path is considered as relative to the moved nodes
(children of `PathFollow3D<class_PathFollow3D>`). As such, the curve
should usually start with a zero vector `(0, 0, 0)`.

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

## Signals

classref-signal

**curve\_changed**() `🔗<class_Path3D_signal_curve_changed>`

Emitted when the `curve<class_Path3D_property_curve>` changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Curve3D<class_Curve3D>` **curve** `🔗<class_Path3D_property_curve>`

classref-property-setget

-   `void (No return value.)` **set\_curve**(value:
    `Curve3D<class_Curve3D>`)
-   `Curve3D<class_Curve3D>` **get\_curve**()

A `Curve3D<class_Curve3D>` describing the path.
