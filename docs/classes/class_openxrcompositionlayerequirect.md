github\_url  
hide

# OpenXRCompositionLayerEquirect

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `OpenXRCompositionLayer<class_OpenXRCompositionLayer>`
**&lt;** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

An OpenXR composition layer that is rendered as an internal slice of a
sphere.

classref-introduction-group

## Description

An OpenXR composition layer that allows rendering a
`SubViewport<class_SubViewport>` on an internal slice of a sphere.

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

`float<class_float>` **central\_horizontal\_angle** = `1.5708`
`🔗<class_OpenXRCompositionLayerEquirect_property_central_horizontal_angle>`

classref-property-setget

-   `void (No return value.)` **set\_central\_horizontal\_angle**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_central\_horizontal\_angle**()

The central horizontal angle of the sphere. Used to set the width.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **fallback\_segments** = `10`
`🔗<class_OpenXRCompositionLayerEquirect_property_fallback_segments>`

classref-property-setget

-   `void (No return value.)` **set\_fallback\_segments**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_fallback\_segments**()

The number of segments to use in the fallback mesh.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **lower\_vertical\_angle** = `0.785398`
`🔗<class_OpenXRCompositionLayerEquirect_property_lower_vertical_angle>`

classref-property-setget

-   `void (No return value.)` **set\_lower\_vertical\_angle**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_lower\_vertical\_angle**()

The lower vertical angle of the sphere. Used (together with
`upper_vertical_angle<class_OpenXRCompositionLayerEquirect_property_upper_vertical_angle>`)
to set the height.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radius** = `1.0`
`🔗<class_OpenXRCompositionLayerEquirect_property_radius>`

classref-property-setget

-   `void (No return value.)` **set\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_radius**()

The radius of the sphere.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **upper\_vertical\_angle** = `0.785398`
`🔗<class_OpenXRCompositionLayerEquirect_property_upper_vertical_angle>`

classref-property-setget

-   `void (No return value.)` **set\_upper\_vertical\_angle**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_upper\_vertical\_angle**()

The upper vertical angle of the sphere. Used (together with
`lower_vertical_angle<class_OpenXRCompositionLayerEquirect_property_lower_vertical_angle>`)
to set the height.
