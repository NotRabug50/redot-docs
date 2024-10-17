github\_url  
hide

# Parallax2D

**Experimental:** This node is meant to replace
`ParallaxBackground<class_ParallaxBackground>` and
`ParallaxLayer<class_ParallaxLayer>`. The implementation may change in
the future.

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A node used to create a parallax scrolling background.

classref-introduction-group

## Description

A **Parallax2D** is used to create a parallax effect. It can move at a
different speed relative to the camera movement using
`scroll_scale<class_Parallax2D_property_scroll_scale>`. This creates an
illusion of depth in a 2D game. If manual scrolling is desired, the
`Camera2D<class_Camera2D>` position can be ignored with
`ignore_camera_scroll<class_Parallax2D_property_ignore_camera_scroll>`.

\*\*Note:\*\* Any changes to this node's position made after it enters
the scene tree will be overridden if
`ignore_camera_scroll<class_Parallax2D_property_ignore_camera_scroll>`
is `false` or `screen_offset<class_Parallax2D_property_screen_offset>`
is modified.

classref-introduction-group

## Tutorials

-   `2D Parallax <../tutorials/2d/2d_parallax>`

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

`Vector2<class_Vector2>` **autoscroll** = `Vector2(0, 0)`
`🔗<class_Parallax2D_property_autoscroll>`

classref-property-setget

-   `void (No return value.)` **set\_autoscroll**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_autoscroll**()

Velocity at which the offset scrolls automatically, in pixels per
second.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **follow\_viewport** = `true`
`🔗<class_Parallax2D_property_follow_viewport>`

classref-property-setget

-   `void (No return value.)` **set\_follow\_viewport**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_follow\_viewport**()

If `true`, this **Parallax2D** is offset by the current camera's
position. If the **Parallax2D** is in a `CanvasLayer<class_CanvasLayer>`
separate from the current camera, it may be desired to match the value
with
`CanvasLayer.follow_viewport_enabled<class_CanvasLayer_property_follow_viewport_enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ignore\_camera\_scroll** = `false`
`🔗<class_Parallax2D_property_ignore_camera_scroll>`

classref-property-setget

-   `void (No return value.)` **set\_ignore\_camera\_scroll**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_ignore\_camera\_scroll**()

If `true`, **Parallax2D**'s position is not affected by the position of
the camera.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **limit\_begin** = `Vector2(-1e+07, -1e+07)`
`🔗<class_Parallax2D_property_limit_begin>`

classref-property-setget

-   `void (No return value.)` **set\_limit\_begin**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_limit\_begin**()

Top-left limits for scrolling to begin. If the camera is outside of this
limit, the **Parallax2D** stops scrolling. Must be lower than
`limit_end<class_Parallax2D_property_limit_end>` minus the viewport size
to work.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **limit\_end** = `Vector2(1e+07, 1e+07)`
`🔗<class_Parallax2D_property_limit_end>`

classref-property-setget

-   `void (No return value.)` **set\_limit\_end**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_limit\_end**()

Bottom-right limits for scrolling to end. If the camera is outside of
this limit, the **Parallax2D** will stop scrolling. Must be higher than
`limit_begin<class_Parallax2D_property_limit_begin>` and the viewport
size combined to work.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **repeat\_size** = `Vector2(0, 0)`
`🔗<class_Parallax2D_property_repeat_size>`

classref-property-setget

-   `void (No return value.)` **set\_repeat\_size**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_repeat\_size**()

Repeats the `Texture2D<class_Texture2D>` of each of this node's children
and offsets them by this value. When scrolling, the node's position
loops, giving the illusion of an infinite scrolling background if the
values are larger than the screen size. If an axis is set to `0`, the
`Texture2D<class_Texture2D>` will not be repeated.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **repeat\_times** = `1`
`🔗<class_Parallax2D_property_repeat_times>`

classref-property-setget

-   `void (No return value.)` **set\_repeat\_times**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_repeat\_times**()

Overrides the amount of times the texture repeats. Each texture copy
spreads evenly from the original by
`repeat_size<class_Parallax2D_property_repeat_size>`. Useful for when
zooming out with a camera.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **screen\_offset** = `Vector2(0, 0)`
`🔗<class_Parallax2D_property_screen_offset>`

classref-property-setget

-   `void (No return value.)` **set\_screen\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_screen\_offset**()

Offset used to scroll this **Parallax2D**. This value is updated
automatically unless
`ignore_camera_scroll<class_Parallax2D_property_ignore_camera_scroll>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **scroll\_offset** = `Vector2(0, 0)`
`🔗<class_Parallax2D_property_scroll_offset>`

classref-property-setget

-   `void (No return value.)` **set\_scroll\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_scroll\_offset**()

The **Parallax2D**'s offset. Similar to
`screen_offset<class_Parallax2D_property_screen_offset>` and
`Node2D.position<class_Node2D_property_position>`, but will not be
overridden.

\*\*Note:\*\* Values will loop if
`repeat_size<class_Parallax2D_property_repeat_size>` is set higher than
`0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **scroll\_scale** = `Vector2(1, 1)`
`🔗<class_Parallax2D_property_scroll_scale>`

classref-property-setget

-   `void (No return value.)` **set\_scroll\_scale**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_scroll\_scale**()

Multiplier to the final **Parallax2D**'s offset. Can be used to simulate
distance from the camera.

For example, a value of `1` scrolls at the same speed as the camera. A
value greater than `1` scrolls faster, making objects appear closer.
Less than `1` scrolls slower, making objects appear further, and a value
of `0` stops the objects completely.
