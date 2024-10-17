github\_url  
hide

# CanvasLayer

**Inherits:** `Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `ParallaxBackground<class_ParallaxBackground>`

A node used for independent rendering of objects within a 2D scene.

classref-introduction-group

## Description

`CanvasItem<class_CanvasItem>`-derived nodes that are direct or indirect
children of a **CanvasLayer** will be drawn in that layer. The layer is
a numeric index that defines the draw order. The default 2D scene
renders with index `0`, so a **CanvasLayer** with index `-1` will be
drawn below, and a **CanvasLayer** with index `1` will be drawn above.
This order will hold regardless of the
`CanvasItem.z_index<class_CanvasItem_property_z_index>` of the nodes
within each layer.

\*\*CanvasLayer\*\*s can be hidden and they can also optionally follow
the viewport. This makes them useful for HUDs like health bar overlays
(on layers `1` and higher) or backgrounds (on layers `-1` and lower).

\*\*Note:\*\* Embedded `Window<class_Window>`s are placed on layer
`1024`. `CanvasItem<class_CanvasItem>`s on layers `1025` and higher
appear in front of embedded windows.

\*\*Note:\*\* Each **CanvasLayer** is drawn on one specific
`Viewport<class_Viewport>` and cannot be shared between multiple
`Viewport<class_Viewport>`s, see
`custom_viewport<class_CanvasLayer_property_custom_viewport>`. When
using multiple `Viewport<class_Viewport>`s, for example in a
split-screen game, you need create an individual **CanvasLayer** for
each `Viewport<class_Viewport>` you want it to be drawn on.

classref-introduction-group

## Tutorials

-   `Viewport and canvas transforms <../tutorials/2d/2d_transforms>`
-   `Canvas layers <../tutorials/2d/canvas_layers>`
-   [2D Dodge The Creeps
    Demo](https://godotengine.org/asset-library/asset/2712)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**visibility\_changed**()
`🔗<class_CanvasLayer_signal_visibility_changed>`

Emitted when visibility of the layer is changed. See
`visible<class_CanvasLayer_property_visible>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Node<class_Node>` **custom\_viewport**
`🔗<class_CanvasLayer_property_custom_viewport>`

classref-property-setget

-   `void (No return value.)` **set\_custom\_viewport**(value:
    `Node<class_Node>`)
-   `Node<class_Node>` **get\_custom\_viewport**()

The custom `Viewport<class_Viewport>` node assigned to the
**CanvasLayer**. If `null`, uses the default viewport instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **follow\_viewport\_enabled** = `false`
`🔗<class_CanvasLayer_property_follow_viewport_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_follow\_viewport**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_following\_viewport**()

If enabled, the **CanvasLayer** will use the viewport's transform, so it
will move when camera moves instead of being anchored in a fixed
position on the screen.

Together with
`follow_viewport_scale<class_CanvasLayer_property_follow_viewport_scale>`
it can be used for a pseudo 3D effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **follow\_viewport\_scale** = `1.0`
`🔗<class_CanvasLayer_property_follow_viewport_scale>`

classref-property-setget

-   `void (No return value.)` **set\_follow\_viewport\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_follow\_viewport\_scale**()

Scales the layer when using
`follow_viewport_enabled<class_CanvasLayer_property_follow_viewport_enabled>`.
Layers moving into the foreground should have increasing scales, while
layers moving into the background should have decreasing scales.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **layer** = `1` `🔗<class_CanvasLayer_property_layer>`

classref-property-setget

-   `void (No return value.)` **set\_layer**(value: `int<class_int>`)
-   `int<class_int>` **get\_layer**()

Layer index for draw order. Lower values are drawn behind higher values.

\*\*Note:\*\* If multiple CanvasLayers have the same layer index,
`CanvasItem<class_CanvasItem>` children of one CanvasLayer are drawn
behind the `CanvasItem<class_CanvasItem>` children of the other
CanvasLayer. Which CanvasLayer is drawn in front is non-deterministic.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **offset** = `Vector2(0, 0)`
`🔗<class_CanvasLayer_property_offset>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_offset**()

The layer's base offset.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **rotation** = `0.0`
`🔗<class_CanvasLayer_property_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_rotation**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_rotation**()

The layer's rotation in radians.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **scale** = `Vector2(1, 1)`
`🔗<class_CanvasLayer_property_scale>`

classref-property-setget

-   `void (No return value.)` **set\_scale**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_scale**()

The layer's scale.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform2D<class_Transform2D>` **transform** =
`Transform2D(1, 0, 0, 1, 0, 0)`
`🔗<class_CanvasLayer_property_transform>`

classref-property-setget

-   `void (No return value.)` **set\_transform**(value:
    `Transform2D<class_Transform2D>`)
-   `Transform2D<class_Transform2D>` **get\_transform**()

The layer's transform.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **visible** = `true`
`🔗<class_CanvasLayer_property_visible>`

classref-property-setget

-   `void (No return value.)` **set\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_visible**()

If `false`, any `CanvasItem<class_CanvasItem>` under this
**CanvasLayer** will be hidden.

Unlike `CanvasItem.visible<class_CanvasItem_property_visible>`,
visibility of a **CanvasLayer** isn't propagated to underlying layers.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`RID<class_RID>` **get\_canvas**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasLayer_method_get_canvas>`

Returns the RID of the canvas used by this layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **get\_final\_transform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasLayer_method_get_final_transform>`

Returns the transform from the **CanvasLayer**s coordinate system to the
`Viewport<class_Viewport>`s coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **hide**() `🔗<class_CanvasLayer_method_hide>`

Hides any `CanvasItem<class_CanvasItem>` under this **CanvasLayer**.
This is equivalent to setting
`visible<class_CanvasLayer_property_visible>` to `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **show**() `🔗<class_CanvasLayer_method_show>`

Shows any `CanvasItem<class_CanvasItem>` under this **CanvasLayer**.
This is equivalent to setting
`visible<class_CanvasLayer_property_visible>` to `true`.
