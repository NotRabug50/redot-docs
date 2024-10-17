github\_url  
hide

# ParallaxLayer

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A parallax scrolling layer to be used with
`ParallaxBackground<class_ParallaxBackground>`.

classref-introduction-group

## Description

A ParallaxLayer must be the child of a
`ParallaxBackground<class_ParallaxBackground>` node. Each ParallaxLayer
can be set to move at different speeds relative to the camera movement
or the
`ParallaxBackground.scroll_offset<class_ParallaxBackground_property_scroll_offset>`
value.

This node's children will be affected by its scroll offset.

\*\*Note:\*\* Any changes to this node's position and scale made after
it enters the scene will be ignored.

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

`Vector2<class_Vector2>` **motion\_mirroring** = `Vector2(0, 0)`
`🔗<class_ParallaxLayer_property_motion_mirroring>`

classref-property-setget

-   `void (No return value.)` **set\_mirroring**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_mirroring**()

The interval, in pixels, at which the **ParallaxLayer** is drawn
repeatedly. Useful for creating an infinitely scrolling background. If
an axis is set to `0`, the **ParallaxLayer** will be drawn only once
along that direction.

\*\*Note:\*\* If you want the repetition to pixel-perfect match a
`Texture2D<class_Texture2D>` displayed by a child node, you should
account for any scale applied to the texture when defining this
interval. For example, if you use a child `Sprite2D<class_Sprite2D>`
scaled to `0.5` to display a 600x600 texture, and want this sprite to be
repeated continuously horizontally, you should set the mirroring to
`Vector2(300, 0)`.

\*\*Note:\*\* If the length of the viewport axis is bigger than twice
the repeated axis size, it will not repeat infinitely, as the parallax
layer only draws 2 instances of the layer at any given time. The
visibility window is calculated from the parent
`ParallaxBackground<class_ParallaxBackground>`'s position, not the
layer's own position. So, if you use mirroring, **do not** change the
**ParallaxLayer** position relative to its parent. Instead, if you need
to adjust the background's position, set the
`CanvasLayer.offset<class_CanvasLayer_property_offset>` property in the
parent `ParallaxBackground<class_ParallaxBackground>`.

\*\*Note:\*\* Despite the name, the layer will not be mirrored, it will
only be repeated.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **motion\_offset** = `Vector2(0, 0)`
`🔗<class_ParallaxLayer_property_motion_offset>`

classref-property-setget

-   `void (No return value.)` **set\_motion\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_motion\_offset**()

The ParallaxLayer's offset relative to the parent ParallaxBackground's
`ParallaxBackground.scroll_offset<class_ParallaxBackground_property_scroll_offset>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **motion\_scale** = `Vector2(1, 1)`
`🔗<class_ParallaxLayer_property_motion_scale>`

classref-property-setget

-   `void (No return value.)` **set\_motion\_scale**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_motion\_scale**()

Multiplies the ParallaxLayer's motion. If an axis is set to `0`, it will
not scroll.
