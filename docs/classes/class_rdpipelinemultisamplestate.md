github\_url  
hide

# RDPipelineMultisampleState

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Pipeline multisample state (used by
`RenderingDevice<class_RenderingDevice>`).

classref-introduction-group

## Description

**RDPipelineMultisampleState** is used to control how multisample or
supersample antialiasing is being performed when rendering using
`RenderingDevice<class_RenderingDevice>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **enable\_alpha\_to\_coverage** = `false`
`🔗<class_RDPipelineMultisampleState_property_enable_alpha_to_coverage>`

classref-property-setget

-   `void (No return value.)`
    **set\_enable\_alpha\_to\_coverage**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_enable\_alpha\_to\_coverage**()

If `true`, alpha to coverage is enabled. This generates a temporary
coverage value based on the alpha component of the fragment's first
color output. This allows alpha transparency to make use of multisample
antialiasing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enable\_alpha\_to\_one** = `false`
`🔗<class_RDPipelineMultisampleState_property_enable_alpha_to_one>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_alpha\_to\_one**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_enable\_alpha\_to\_one**()

If `true`, alpha is forced to either `0.0` or `1.0`. This allows
hardening the edges of antialiased alpha transparencies. Only relevant
if
`enable_alpha_to_coverage<class_RDPipelineMultisampleState_property_enable_alpha_to_coverage>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enable\_sample\_shading** = `false`
`🔗<class_RDPipelineMultisampleState_property_enable_sample_shading>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_sample\_shading**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_enable\_sample\_shading**()

If `true`, enables per-sample shading which replaces MSAA by SSAA. This
provides higher quality antialiasing that works with transparent (alpha
scissor) edges. This has a very high performance cost. See also
`min_sample_shading<class_RDPipelineMultisampleState_property_min_sample_shading>`.
See the [per-sample shading Vulkan
documentation](https://registry.khronos.org/vulkan/specs/1.3-extensions/html/vkspec.html#primsrast-sampleshading)
for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **min\_sample\_shading** = `0.0`
`🔗<class_RDPipelineMultisampleState_property_min_sample_shading>`

classref-property-setget

-   `void (No return value.)` **set\_min\_sample\_shading**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_min\_sample\_shading**()

The multiplier of
`sample_count<class_RDPipelineMultisampleState_property_sample_count>`
that determines how many samples are performed for each fragment. Must
be between `0.0` and `1.0` (inclusive). Only effective if
`enable_sample_shading<class_RDPipelineMultisampleState_property_enable_sample_shading>`
is `true`. If
`min_sample_shading<class_RDPipelineMultisampleState_property_min_sample_shading>`
is `1.0`, fragment invocation must only read from the coverage index
sample. Tile image access must not be used if
`enable_sample_shading<class_RDPipelineMultisampleState_property_enable_sample_shading>`
is *not* `1.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureSamples<enum_RenderingDevice_TextureSamples>` **sample\_count**
= `0` `🔗<class_RDPipelineMultisampleState_property_sample_count>`

classref-property-setget

-   `void (No return value.)` **set\_sample\_count**(value:
    `TextureSamples<enum_RenderingDevice_TextureSamples>`)
-   `TextureSamples<enum_RenderingDevice_TextureSamples>`
    **get\_sample\_count**()

The number of MSAA samples (or SSAA samples if
`enable_sample_shading<class_RDPipelineMultisampleState_property_enable_sample_shading>`
is `true`) to perform. Higher values result in better antialiasing, at
the cost of performance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`int<class_int>`\] **sample\_masks** = `[]`
`🔗<class_RDPipelineMultisampleState_property_sample_masks>`

classref-property-setget

-   `void (No return value.)` **set\_sample\_masks**(value:
    `Array<class_Array>`\[`int<class_int>`\])
-   `Array<class_Array>`\[`int<class_int>`\] **get\_sample\_masks**()

The sample mask array. See the [sample mask Vulkan
documentation](https://registry.khronos.org/vulkan/specs/1.3-extensions/html/vkspec.html#fragops-samplemask)
for more details.
