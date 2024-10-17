github\_url  
hide

# XRVRS

**Inherits:** `Object<class_Object>`

Helper class for XR interfaces that generates VRS images.

classref-introduction-group

## Description

This class is used by various XR interfaces to generate VRS textures
that can be used to speed up rendering.

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

classref-reftable-group

## Methods

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

`float<class_float>` **vrs\_min\_radius** = `20.0`
`🔗<class_XRVRS_property_vrs_min_radius>`

classref-property-setget

-   `void (No return value.)` **set\_vrs\_min\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_vrs\_min\_radius**()

The minimum radius around the focal point where full quality is
guaranteed if VRS is used as a percentage of screen size.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **vrs\_strength** = `1.0`
`🔗<class_XRVRS_property_vrs_strength>`

classref-property-setget

-   `void (No return value.)` **set\_vrs\_strength**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_vrs\_strength**()

The strength used to calculate the VRS density map. The greater this
value, the more noticeable VRS is.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`RID<class_RID>` **make\_vrs\_texture**(target\_size:
`Vector2<class_Vector2>`, eye\_foci:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_XRVRS_method_make_vrs_texture>`

Generates the VRS texture based on a render `target_size` adjusted by
our VRS tile size. For each eyes focal point passed in `eye_foci` a
layer is created. Focal point should be in NDC.

The result will be cached, requesting a VRS texture with unchanged
parameters and settings will return the cached RID.
