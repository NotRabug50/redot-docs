github\_url  
hide

# CompositorEffect

**Experimental:** The implementation may change as more of the rendering
internals are exposed over time.

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

This resource allows for creating a custom rendering effect.

classref-introduction-group

## Description

This resource defines a custom rendering effect that can be applied to
`Viewport<class_Viewport>`s through the viewports'
`Environment<class_Environment>`. You can implement a callback that is
called during rendering at a given stage of the rendering pipeline and
allows you to insert additional passes. Note that this callback happens
on the rendering thread. CompositorEffect is an abstract base class and
must be extended to implement specific rendering logic.

classref-introduction-group

## Tutorials

-   `The Compositor <../tutorials/rendering/compositor>`

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

## Enumerations

classref-enumeration

enum **EffectCallbackType**:
`🔗<enum_CompositorEffect_EffectCallbackType>`

classref-enumeration-constant

`EffectCallbackType<enum_CompositorEffect_EffectCallbackType>`
**EFFECT\_CALLBACK\_TYPE\_PRE\_OPAQUE** = `0`

The callback is called before our opaque rendering pass, but after depth
prepass (if applicable).

classref-enumeration-constant

`EffectCallbackType<enum_CompositorEffect_EffectCallbackType>`
**EFFECT\_CALLBACK\_TYPE\_POST\_OPAQUE** = `1`

The callback is called after our opaque rendering pass, but before our
sky is rendered.

classref-enumeration-constant

`EffectCallbackType<enum_CompositorEffect_EffectCallbackType>`
**EFFECT\_CALLBACK\_TYPE\_POST\_SKY** = `2`

The callback is called after our sky is rendered, but before our back
buffers are created (and if enabled, before subsurface scattering and/or
screen space reflections).

classref-enumeration-constant

`EffectCallbackType<enum_CompositorEffect_EffectCallbackType>`
**EFFECT\_CALLBACK\_TYPE\_PRE\_TRANSPARENT** = `3`

The callback is called before our transparent rendering pass, but after
our sky is rendered and we've created our back buffers.

classref-enumeration-constant

`EffectCallbackType<enum_CompositorEffect_EffectCallbackType>`
**EFFECT\_CALLBACK\_TYPE\_POST\_TRANSPARENT** = `4`

The callback is called after our transparent rendering pass, but before
any built-in post-processing effects and output to our render target.

classref-enumeration-constant

`EffectCallbackType<enum_CompositorEffect_EffectCallbackType>`
**EFFECT\_CALLBACK\_TYPE\_MAX** = `5`

Represents the size of the
`EffectCallbackType<enum_CompositorEffect_EffectCallbackType>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **access\_resolved\_color**
`🔗<class_CompositorEffect_property_access_resolved_color>`

classref-property-setget

-   `void (No return value.)` **set\_access\_resolved\_color**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_access\_resolved\_color**()

If `true` and MSAA is enabled, this will trigger a color buffer resolve
before the effect is run.

\*\*Note:\*\* In
`_render_callback<class_CompositorEffect_private_method__render_callback>`,
to access the resolved buffer use:

    var render_scene_buffers : RenderSceneBuffersRD = render_data.get_render_scene_buffers()
    var color_buffer = render_scene_buffers.get_texture("render_buffers", "color")

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **access\_resolved\_depth**
`🔗<class_CompositorEffect_property_access_resolved_depth>`

classref-property-setget

-   `void (No return value.)` **set\_access\_resolved\_depth**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_access\_resolved\_depth**()

If `true` and MSAA is enabled, this will trigger a depth buffer resolve
before the effect is run.

\*\*Note:\*\* In
`_render_callback<class_CompositorEffect_private_method__render_callback>`,
to access the resolved buffer use:

    var render_scene_buffers : RenderSceneBuffersRD = render_data.get_render_scene_buffers()
    var depth_buffer = render_scene_buffers.get_texture("render_buffers", "depth")

classref-item-separator

------------------------------------------------------------------------

classref-property

`EffectCallbackType<enum_CompositorEffect_EffectCallbackType>`
**effect\_callback\_type**
`🔗<class_CompositorEffect_property_effect_callback_type>`

classref-property-setget

-   `void (No return value.)` **set\_effect\_callback\_type**(value:
    `EffectCallbackType<enum_CompositorEffect_EffectCallbackType>`)
-   `EffectCallbackType<enum_CompositorEffect_EffectCallbackType>`
    **get\_effect\_callback\_type**()

The type of effect that is implemented, determines at what stage of
rendering the callback is called.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enabled**
`🔗<class_CompositorEffect_property_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_enabled**()

If `true` this rendering effect is applied to any viewport it is added
to.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **needs\_motion\_vectors**
`🔗<class_CompositorEffect_property_needs_motion_vectors>`

classref-property-setget

-   `void (No return value.)` **set\_needs\_motion\_vectors**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_needs\_motion\_vectors**()

If `true` this triggers motion vectors being calculated during the
opaque render state.

\*\*Note:\*\* In
`_render_callback<class_CompositorEffect_private_method__render_callback>`,
to access the motion vector buffer use:

    var render_scene_buffers : RenderSceneBuffersRD = render_data.get_render_scene_buffers()
    var motion_buffer = render_scene_buffers.get_velocity_texture()

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **needs\_normal\_roughness**
`🔗<class_CompositorEffect_property_needs_normal_roughness>`

classref-property-setget

-   `void (No return value.)` **set\_needs\_normal\_roughness**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_needs\_normal\_roughness**()

If `true` this triggers normal and roughness data to be output during
our depth pre-pass, only applicable for the Forward+ renderer.

\*\*Note:\*\* In
`_render_callback<class_CompositorEffect_private_method__render_callback>`,
to access the roughness buffer use:

    var render_scene_buffers : RenderSceneBuffersRD = render_data.get_render_scene_buffers()
    var roughness_buffer = render_scene_buffers.get_texture("forward_clustered", "normal_roughness")

The raw normal and roughness buffer is stored in an optimized format,
different than the one available in Spatial shaders. When sampling the
buffer, a conversion function must be applied. Use this function, copied
from
[here](https://github.com/godotengine/godot/blob/da5f39889f155658cef7f7ec3cc1abb94e17d815/servers/rendering/renderer_rd/shaders/forward_clustered/scene_forward_clustered_inc.glsl#L334-L341):

    vec4 normal_roughness_compatibility(vec4 p_normal_roughness) {
        float roughness = p_normal_roughness.w;
        if (roughness > 0.5) {
            roughness = 1.0 - roughness;
        }
        roughness /= (127.0 / 255.0);
        return vec4(normalize(p_normal_roughness.xyz * 2.0 - 1.0) * 0.5 + 0.5, roughness);
    }

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **needs\_separate\_specular**
`🔗<class_CompositorEffect_property_needs_separate_specular>`

classref-property-setget

-   `void (No return value.)` **set\_needs\_separate\_specular**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_needs\_separate\_specular**()

If `true` this triggers specular data being rendered to a separate
buffer and combined after effects have been applied, only applicable for
the Forward+ renderer.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_render\_callback**(effect\_callback\_type:
`int<class_int>`, render\_data: `RenderData<class_RenderData>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_CompositorEffect_private_method__render_callback>`

Implement this function with your custom rendering code.
`effect_callback_type` should always match the effect callback type
you've specified in
`effect_callback_type<class_CompositorEffect_property_effect_callback_type>`.
`render_data` provides access to the rendering state, it is only valid
during rendering and should not be stored.
