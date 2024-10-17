github\_url  
hide

# DirectionalLight2D

**Inherits:** `Light2D<class_Light2D>` **&lt;** `Node2D<class_Node2D>`
**&lt;** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

Directional 2D light from a distance.

classref-introduction-group

## Description

A directional light is a type of `Light2D<class_Light2D>` node that
models an infinite number of parallel rays covering the entire scene. It
is used for lights with strong intensity that are located far away from
the scene (for example: to model sunlight or moonlight).

\*\*Note:\*\* **DirectionalLight2D** does not support light cull masks
(but it supports shadow cull masks). It will always light up 2D nodes,
regardless of the 2D node's
`CanvasItem.light_mask<class_CanvasItem_property_light_mask>`.

classref-introduction-group

## Tutorials

-   `2D lights and shadows <../tutorials/2d/2d_lights_and_shadows>`

classref-reftable-group

## Properties

<table>
<tbody>
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

`float<class_float>` **height** = `0.0`
`🔗<class_DirectionalLight2D_property_height>`

classref-property-setget

-   `void (No return value.)` **set\_height**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_height**()

The height of the light. Used with 2D normal mapping. Ranges from 0
(parallel to the plane) to 1 (perpendicular to the plane).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **max\_distance** = `10000.0`
`🔗<class_DirectionalLight2D_property_max_distance>`

classref-property-setget

-   `void (No return value.)` **set\_max\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_max\_distance**()

The maximum distance from the camera center objects can be before their
shadows are culled (in pixels). Decreasing this value can prevent
objects located outside the camera from casting shadows (while also
improving performance). `Camera2D.zoom<class_Camera2D_property_zoom>` is
not taken into account by
`max_distance<class_DirectionalLight2D_property_max_distance>`, which
means that at higher zoom values, shadows will appear to fade out sooner
when zooming onto a given point.
