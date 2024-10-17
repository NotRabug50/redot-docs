github\_url  
hide

# RDSamplerState

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Sampler state (used by `RenderingDevice<class_RenderingDevice>`).

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

`float<class_float>` **anisotropy\_max** = `1.0`
`🔗<class_RDSamplerState_property_anisotropy_max>`

classref-property-setget

-   `void (No return value.)` **set\_anisotropy\_max**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_anisotropy\_max**()

Maximum anisotropy that can be used when sampling. Only effective if
`use_anisotropy<class_RDSamplerState_property_use_anisotropy>` is
`true`. Higher values result in a sharper sampler at oblique angles, at
the cost of performance (due to memory bandwidth). This value may be
limited by the graphics hardware in use. Most graphics hardware only
supports values up to `16.0`.

If `anisotropy_max<class_RDSamplerState_property_anisotropy_max>` is
`1.0`, forcibly disables anisotropy even if
`use_anisotropy<class_RDSamplerState_property_use_anisotropy>` is
`true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SamplerBorderColor<enum_RenderingDevice_SamplerBorderColor>`
**border\_color** = `2` `🔗<class_RDSamplerState_property_border_color>`

classref-property-setget

-   `void (No return value.)` **set\_border\_color**(value:
    `SamplerBorderColor<enum_RenderingDevice_SamplerBorderColor>`)
-   `SamplerBorderColor<enum_RenderingDevice_SamplerBorderColor>`
    **get\_border\_color**()

The border color that will be returned when sampling outside the
sampler's bounds and the
`repeat_u<class_RDSamplerState_property_repeat_u>`,
`repeat_v<class_RDSamplerState_property_repeat_v>` or
`repeat_w<class_RDSamplerState_property_repeat_w>` modes have repeating
disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CompareOperator<enum_RenderingDevice_CompareOperator>` **compare\_op**
= `7` `🔗<class_RDSamplerState_property_compare_op>`

classref-property-setget

-   `void (No return value.)` **set\_compare\_op**(value:
    `CompareOperator<enum_RenderingDevice_CompareOperator>`)
-   `CompareOperator<enum_RenderingDevice_CompareOperator>`
    **get\_compare\_op**()

The compare operation to use. Only effective if
`enable_compare<class_RDSamplerState_property_enable_compare>` is
`true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enable\_compare** = `false`
`🔗<class_RDSamplerState_property_enable_compare>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_compare**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_enable\_compare**()

If `true`, returned values will be based on the comparison operation
defined in `compare_op<class_RDSamplerState_property_compare_op>`. This
is a hardware-based approach and is therefore faster than performing
this manually in a shader. For example, compare operations are used for
shadow map rendering by comparing depth values from a shadow sampler.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **lod\_bias** = `0.0`
`🔗<class_RDSamplerState_property_lod_bias>`

classref-property-setget

-   `void (No return value.)` **set\_lod\_bias**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_lod\_bias**()

The mipmap LOD bias to use. Positive values will make the sampler
blurrier at a given distance, while negative values will make the
sampler sharper at a given distance (at the risk of looking grainy).
Recommended values are between `-0.5` and `0.0`. Only effective if the
sampler has mipmaps available.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SamplerFilter<enum_RenderingDevice_SamplerFilter>` **mag\_filter** =
`0` `🔗<class_RDSamplerState_property_mag_filter>`

classref-property-setget

-   `void (No return value.)` **set\_mag\_filter**(value:
    `SamplerFilter<enum_RenderingDevice_SamplerFilter>`)
-   `SamplerFilter<enum_RenderingDevice_SamplerFilter>`
    **get\_mag\_filter**()

The sampler's magnification filter. It is the filtering method used when
sampling texels that appear bigger than on-screen pixels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **max\_lod** = `1e+20`
`🔗<class_RDSamplerState_property_max_lod>`

classref-property-setget

-   `void (No return value.)` **set\_max\_lod**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_max\_lod**()

The maximum mipmap LOD bias to display (lowest resolution). Only
effective if the sampler has mipmaps available.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SamplerFilter<enum_RenderingDevice_SamplerFilter>` **min\_filter** =
`0` `🔗<class_RDSamplerState_property_min_filter>`

classref-property-setget

-   `void (No return value.)` **set\_min\_filter**(value:
    `SamplerFilter<enum_RenderingDevice_SamplerFilter>`)
-   `SamplerFilter<enum_RenderingDevice_SamplerFilter>`
    **get\_min\_filter**()

The sampler's minification filter. It is the filtering method used when
sampling texels that appear smaller than on-screen pixels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **min\_lod** = `0.0`
`🔗<class_RDSamplerState_property_min_lod>`

classref-property-setget

-   `void (No return value.)` **set\_min\_lod**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_min\_lod**()

The minimum mipmap LOD bias to display (highest resolution). Only
effective if the sampler has mipmaps available.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SamplerFilter<enum_RenderingDevice_SamplerFilter>` **mip\_filter** =
`0` `🔗<class_RDSamplerState_property_mip_filter>`

classref-property-setget

-   `void (No return value.)` **set\_mip\_filter**(value:
    `SamplerFilter<enum_RenderingDevice_SamplerFilter>`)
-   `SamplerFilter<enum_RenderingDevice_SamplerFilter>`
    **get\_mip\_filter**()

The filtering method to use for mipmaps.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
**repeat\_u** = `2` `🔗<class_RDSamplerState_property_repeat_u>`

classref-property-setget

-   `void (No return value.)` **set\_repeat\_u**(value:
    `SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`)
-   `SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
    **get\_repeat\_u**()

The repeat mode to use along the U axis of UV coordinates. This affects
the returned values if sampling outside the UV bounds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
**repeat\_v** = `2` `🔗<class_RDSamplerState_property_repeat_v>`

classref-property-setget

-   `void (No return value.)` **set\_repeat\_v**(value:
    `SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`)
-   `SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
    **get\_repeat\_v**()

The repeat mode to use along the V axis of UV coordinates. This affects
the returned values if sampling outside the UV bounds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
**repeat\_w** = `2` `🔗<class_RDSamplerState_property_repeat_w>`

classref-property-setget

-   `void (No return value.)` **set\_repeat\_w**(value:
    `SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`)
-   `SamplerRepeatMode<enum_RenderingDevice_SamplerRepeatMode>`
    **get\_repeat\_w**()

The repeat mode to use along the W axis of UV coordinates. This affects
the returned values if sampling outside the UV bounds. Only effective
for 3D samplers.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **unnormalized\_uvw** = `false`
`🔗<class_RDSamplerState_property_unnormalized_uvw>`

classref-property-setget

-   `void (No return value.)` **set\_unnormalized\_uvw**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_unnormalized\_uvw**()

If `true`, the texture will be sampled with coordinates ranging from 0
to the texture's resolution. Otherwise, the coordinates will be
normalized and range from 0 to 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_anisotropy** = `false`
`🔗<class_RDSamplerState_property_use_anisotropy>`

classref-property-setget

-   `void (No return value.)` **set\_use\_anisotropy**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_use\_anisotropy**()

If `true`, perform anisotropic sampling. See
`anisotropy_max<class_RDSamplerState_property_anisotropy_max>`.
