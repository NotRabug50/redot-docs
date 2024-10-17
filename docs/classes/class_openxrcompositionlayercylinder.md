github\_url  
hide

# OpenXRCompositionLayerCylinder

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `OpenXRCompositionLayer<class_OpenXRCompositionLayer>`
**&lt;** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

An OpenXR composition layer that is rendered as an internal slice of a
cylinder.

classref-introduction-group

## Description

An OpenXR composition layer that allows rendering a
`SubViewport<class_SubViewport>` on an internal slice of a cylinder.

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

`float<class_float>` **aspect\_ratio** = `1.0`
`🔗<class_OpenXRCompositionLayerCylinder_property_aspect_ratio>`

classref-property-setget

-   `void (No return value.)` **set\_aspect\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_aspect\_ratio**()

The aspect ratio of the slice. Used to set the height relative to the
width.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **central\_angle** = `1.5708`
`🔗<class_OpenXRCompositionLayerCylinder_property_central_angle>`

classref-property-setget

-   `void (No return value.)` **set\_central\_angle**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_central\_angle**()

The central angle of the cylinder. Used to set the width.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **fallback\_segments** = `10`
`🔗<class_OpenXRCompositionLayerCylinder_property_fallback_segments>`

classref-property-setget

-   `void (No return value.)` **set\_fallback\_segments**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_fallback\_segments**()

The number of segments to use in the fallback mesh.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radius** = `1.0`
`🔗<class_OpenXRCompositionLayerCylinder_property_radius>`

classref-property-setget

-   `void (No return value.)` **set\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_radius**()

The radius of the cylinder.
