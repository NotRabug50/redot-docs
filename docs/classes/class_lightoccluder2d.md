github\_url  
hide

# LightOccluder2D

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Occludes light cast by a Light2D, casting shadows.

classref-introduction-group

## Description

Occludes light cast by a Light2D, casting shadows. The LightOccluder2D
must be provided with an `OccluderPolygon2D<class_OccluderPolygon2D>` in
order for the shadow to be computed.

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`OccluderPolygon2D<class_OccluderPolygon2D>` **occluder**
`🔗<class_LightOccluder2D_property_occluder>`

classref-property-setget

-   `void (No return value.)` **set\_occluder\_polygon**(value:
    `OccluderPolygon2D<class_OccluderPolygon2D>`)
-   `OccluderPolygon2D<class_OccluderPolygon2D>`
    **get\_occluder\_polygon**()

The `OccluderPolygon2D<class_OccluderPolygon2D>` used to compute the
shadow.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **occluder\_light\_mask** = `1`
`🔗<class_LightOccluder2D_property_occluder_light_mask>`

classref-property-setget

-   `void (No return value.)` **set\_occluder\_light\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_occluder\_light\_mask**()

The LightOccluder2D's occluder light mask. The LightOccluder2D will cast
shadows only from Light2D(s) that have the same light mask(s).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **sdf\_collision** = `true`
`🔗<class_LightOccluder2D_property_sdf_collision>`

classref-property-setget

-   `void (No return value.)` **set\_as\_sdf\_collision**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_set\_as\_sdf\_collision**()

If enabled, the occluder will be part of a real-time generated signed
distance field that can be used in custom shaders.
