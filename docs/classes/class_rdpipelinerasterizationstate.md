github\_url  
hide

# RDPipelineRasterizationState

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Pipeline rasterization state (used by
`RenderingDevice<class_RenderingDevice>`).

classref-introduction-group

## Description

This object is used by `RenderingDevice<class_RenderingDevice>`.

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

`PolygonCullMode<enum_RenderingDevice_PolygonCullMode>` **cull\_mode** =
`0` `🔗<class_RDPipelineRasterizationState_property_cull_mode>`

classref-property-setget

-   `void (No return value.)` **set\_cull\_mode**(value:
    `PolygonCullMode<enum_RenderingDevice_PolygonCullMode>`)
-   `PolygonCullMode<enum_RenderingDevice_PolygonCullMode>`
    **get\_cull\_mode**()

The cull mode to use when drawing polygons, which determines whether
front faces or backfaces are hidden.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **depth\_bias\_clamp** = `0.0`
`🔗<class_RDPipelineRasterizationState_property_depth_bias_clamp>`

classref-property-setget

-   `void (No return value.)` **set\_depth\_bias\_clamp**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_depth\_bias\_clamp**()

A limit for how much each depth value can be offset. If negative, it
serves as a minimum value, but if positive, it serves as a maximum
value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **depth\_bias\_constant\_factor** = `0.0`
`🔗<class_RDPipelineRasterizationState_property_depth_bias_constant_factor>`

classref-property-setget

-   `void (No return value.)`
    **set\_depth\_bias\_constant\_factor**(value: `float<class_float>`)
-   `float<class_float>` **get\_depth\_bias\_constant\_factor**()

A constant offset added to each depth value. Applied after
`depth_bias_slope_factor<class_RDPipelineRasterizationState_property_depth_bias_slope_factor>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **depth\_bias\_enabled** = `false`
`🔗<class_RDPipelineRasterizationState_property_depth_bias_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_depth\_bias\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_depth\_bias\_enabled**()

If `true`, each generated depth value will by offset by some amount. The
specific amount is generated per polygon based on the values of
`depth_bias_slope_factor<class_RDPipelineRasterizationState_property_depth_bias_slope_factor>`
and
`depth_bias_constant_factor<class_RDPipelineRasterizationState_property_depth_bias_constant_factor>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **depth\_bias\_slope\_factor** = `0.0`
`🔗<class_RDPipelineRasterizationState_property_depth_bias_slope_factor>`

classref-property-setget

-   `void (No return value.)` **set\_depth\_bias\_slope\_factor**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_depth\_bias\_slope\_factor**()

A constant scale applied to the slope of each polygons' depth. Applied
before
`depth_bias_constant_factor<class_RDPipelineRasterizationState_property_depth_bias_constant_factor>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **discard\_primitives** = `false`
`🔗<class_RDPipelineRasterizationState_property_discard_primitives>`

classref-property-setget

-   `void (No return value.)` **set\_discard\_primitives**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_discard\_primitives**()

If `true`, primitives are discarded immediately before the rasterization
stage.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enable\_depth\_clamp** = `false`
`🔗<class_RDPipelineRasterizationState_property_enable_depth_clamp>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_depth\_clamp**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_enable\_depth\_clamp**()

If `true`, clamps depth values according to the minimum and maximum
depth of the associated viewport.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PolygonFrontFace<enum_RenderingDevice_PolygonFrontFace>`
**front\_face** = `0`
`🔗<class_RDPipelineRasterizationState_property_front_face>`

classref-property-setget

-   `void (No return value.)` **set\_front\_face**(value:
    `PolygonFrontFace<enum_RenderingDevice_PolygonFrontFace>`)
-   `PolygonFrontFace<enum_RenderingDevice_PolygonFrontFace>`
    **get\_front\_face**()

The winding order to use to determine which face of a triangle is
considered its front face.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **line\_width** = `1.0`
`🔗<class_RDPipelineRasterizationState_property_line_width>`

classref-property-setget

-   `void (No return value.)` **set\_line\_width**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_line\_width**()

The line width to use when drawing lines (in pixels). Thick lines may
not be supported on all hardware.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **patch\_control\_points** = `1`
`🔗<class_RDPipelineRasterizationState_property_patch_control_points>`

classref-property-setget

-   `void (No return value.)` **set\_patch\_control\_points**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_patch\_control\_points**()

The number of control points to use when drawing a patch with
tessellation enabled. Higher values result in higher quality at the cost
of performance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **wireframe** = `false`
`🔗<class_RDPipelineRasterizationState_property_wireframe>`

classref-property-setget

-   `void (No return value.)` **set\_wireframe**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_wireframe**()

If `true`, performs wireframe rendering for triangles instead of flat or
textured rendering.
