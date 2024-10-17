github\_url  
hide

# RenderSceneBuffersConfiguration

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Configuration object used to setup a
`RenderSceneBuffers<class_RenderSceneBuffers>` object.

classref-introduction-group

## Description

This configuration object is created and populated by the render engine
on a viewport change and used to (re)configure a
`RenderSceneBuffers<class_RenderSceneBuffers>` object.

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **fsr\_sharpness** = `0.0`
`🔗<class_RenderSceneBuffersConfiguration_property_fsr_sharpness>`

classref-property-setget

-   `void (No return value.)` **set\_fsr\_sharpness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fsr\_sharpness**()

FSR Sharpness applicable if FSR upscaling is used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **internal\_size** = `Vector2i(0, 0)`
`🔗<class_RenderSceneBuffersConfiguration_property_internal_size>`

classref-property-setget

-   `void (No return value.)` **set\_internal\_size**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_internal\_size**()

The size of the 3D render buffer used for rendering.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ViewportMSAA<enum_RenderingServer_ViewportMSAA>` **msaa\_3d** = `0`
`🔗<class_RenderSceneBuffersConfiguration_property_msaa_3d>`

classref-property-setget

-   `void (No return value.)` **set\_msaa\_3d**(value:
    `ViewportMSAA<enum_RenderingServer_ViewportMSAA>`)
-   `ViewportMSAA<enum_RenderingServer_ViewportMSAA>`
    **get\_msaa\_3d**()

The MSAA mode we're using for 3D rendering.

classref-item-separator

------------------------------------------------------------------------

classref-property

`RID<class_RID>` **render\_target** = `RID()`
`🔗<class_RenderSceneBuffersConfiguration_property_render_target>`

classref-property-setget

-   `void (No return value.)` **set\_render\_target**(value:
    `RID<class_RID>`)
-   `RID<class_RID>` **get\_render\_target**()

The render target associated with these buffer.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ViewportScaling3DMode<enum_RenderingServer_ViewportScaling3DMode>`
**scaling\_3d\_mode** = `255`
`🔗<class_RenderSceneBuffersConfiguration_property_scaling_3d_mode>`

classref-property-setget

-   `void (No return value.)` **set\_scaling\_3d\_mode**(value:
    `ViewportScaling3DMode<enum_RenderingServer_ViewportScaling3DMode>`)
-   `ViewportScaling3DMode<enum_RenderingServer_ViewportScaling3DMode>`
    **get\_scaling\_3d\_mode**()

The requested scaling mode with which we upscale/downscale if
`internal_size<class_RenderSceneBuffersConfiguration_property_internal_size>`
and
`target_size<class_RenderSceneBuffersConfiguration_property_target_size>`
are not equal.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ViewportScreenSpaceAA<enum_RenderingServer_ViewportScreenSpaceAA>`
**screen\_space\_aa** = `0`
`🔗<class_RenderSceneBuffersConfiguration_property_screen_space_aa>`

classref-property-setget

-   `void (No return value.)` **set\_screen\_space\_aa**(value:
    `ViewportScreenSpaceAA<enum_RenderingServer_ViewportScreenSpaceAA>`)
-   `ViewportScreenSpaceAA<enum_RenderingServer_ViewportScreenSpaceAA>`
    **get\_screen\_space\_aa**()

The requested screen space AA applied in post processing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **target\_size** = `Vector2i(0, 0)`
`🔗<class_RenderSceneBuffersConfiguration_property_target_size>`

classref-property-setget

-   `void (No return value.)` **set\_target\_size**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_target\_size**()

The target (upscale) size if scaling is used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **texture\_mipmap\_bias** = `0.0`
`🔗<class_RenderSceneBuffersConfiguration_property_texture_mipmap_bias>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_mipmap\_bias**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_texture\_mipmap\_bias**()

Bias applied to mipmaps.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **view\_count** = `1`
`🔗<class_RenderSceneBuffersConfiguration_property_view_count>`

classref-property-setget

-   `void (No return value.)` **set\_view\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_view\_count**()

The number of views we're rendering.
