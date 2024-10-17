github\_url  
hide

# Sky

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Defines a 3D environment's background by using a
`Material<class_Material>`.

classref-introduction-group

## Description

The **Sky** class uses a `Material<class_Material>` to render a 3D
environment's background and the light it emits by updating the
reflection/radiance cubemaps.

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

## Enumerations

classref-enumeration

enum **RadianceSize**: `🔗<enum_Sky_RadianceSize>`

classref-enumeration-constant

`RadianceSize<enum_Sky_RadianceSize>` **RADIANCE\_SIZE\_32** = `0`

Radiance texture size is 32×32 pixels.

classref-enumeration-constant

`RadianceSize<enum_Sky_RadianceSize>` **RADIANCE\_SIZE\_64** = `1`

Radiance texture size is 64×64 pixels.

classref-enumeration-constant

`RadianceSize<enum_Sky_RadianceSize>` **RADIANCE\_SIZE\_128** = `2`

Radiance texture size is 128×128 pixels.

classref-enumeration-constant

`RadianceSize<enum_Sky_RadianceSize>` **RADIANCE\_SIZE\_256** = `3`

Radiance texture size is 256×256 pixels.

classref-enumeration-constant

`RadianceSize<enum_Sky_RadianceSize>` **RADIANCE\_SIZE\_512** = `4`

Radiance texture size is 512×512 pixels.

classref-enumeration-constant

`RadianceSize<enum_Sky_RadianceSize>` **RADIANCE\_SIZE\_1024** = `5`

Radiance texture size is 1024×1024 pixels.

classref-enumeration-constant

`RadianceSize<enum_Sky_RadianceSize>` **RADIANCE\_SIZE\_2048** = `6`

Radiance texture size is 2048×2048 pixels.

classref-enumeration-constant

`RadianceSize<enum_Sky_RadianceSize>` **RADIANCE\_SIZE\_MAX** = `7`

Represents the size of the `RadianceSize<enum_Sky_RadianceSize>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ProcessMode**: `🔗<enum_Sky_ProcessMode>`

classref-enumeration-constant

`ProcessMode<enum_Sky_ProcessMode>` **PROCESS\_MODE\_AUTOMATIC** = `0`

Automatically selects the appropriate process mode based on your sky
shader. If your shader uses `TIME` or `POSITION`, this will use
`PROCESS_MODE_REALTIME<class_Sky_constant_PROCESS_MODE_REALTIME>`. If
your shader uses any of the `LIGHT_*` variables or any custom uniforms,
this uses
`PROCESS_MODE_INCREMENTAL<class_Sky_constant_PROCESS_MODE_INCREMENTAL>`.
Otherwise, this defaults to
`PROCESS_MODE_QUALITY<class_Sky_constant_PROCESS_MODE_QUALITY>`.

classref-enumeration-constant

`ProcessMode<enum_Sky_ProcessMode>` **PROCESS\_MODE\_QUALITY** = `1`

Uses high quality importance sampling to process the radiance map. In
general, this results in much higher quality than
`PROCESS_MODE_REALTIME<class_Sky_constant_PROCESS_MODE_REALTIME>` but
takes much longer to generate. This should not be used if you plan on
changing the sky at runtime. If you are finding that the reflection is
not blurry enough and is showing sparkles or fireflies, try increasing
`ProjectSettings.rendering/reflections/sky_reflections/ggx_samples<class_ProjectSettings_property_rendering/reflections/sky_reflections/ggx_samples>`.

classref-enumeration-constant

`ProcessMode<enum_Sky_ProcessMode>` **PROCESS\_MODE\_INCREMENTAL** = `2`

Uses the same high quality importance sampling to process the radiance
map as `PROCESS_MODE_QUALITY<class_Sky_constant_PROCESS_MODE_QUALITY>`,
but updates over several frames. The number of frames is determined by
`ProjectSettings.rendering/reflections/sky_reflections/roughness_layers<class_ProjectSettings_property_rendering/reflections/sky_reflections/roughness_layers>`.
Use this when you need highest quality radiance maps, but have a sky
that updates slowly.

classref-enumeration-constant

`ProcessMode<enum_Sky_ProcessMode>` **PROCESS\_MODE\_REALTIME** = `3`

Uses the fast filtering algorithm to process the radiance map. In
general this results in lower quality, but substantially faster run
times. If you need better quality, but still need to update the sky
every frame, consider turning on
`ProjectSettings.rendering/reflections/sky_reflections/fast_filter_high_quality<class_ProjectSettings_property_rendering/reflections/sky_reflections/fast_filter_high_quality>`.

\*\*Note:\*\* The fast filtering algorithm is limited to 256×256
cubemaps, so `radiance_size<class_Sky_property_radiance_size>` must be
set to `RADIANCE_SIZE_256<class_Sky_constant_RADIANCE_SIZE_256>`.
Otherwise, a warning is printed and the overridden radiance size is
ignored.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`ProcessMode<enum_Sky_ProcessMode>` **process\_mode** = `0`
`🔗<class_Sky_property_process_mode>`

classref-property-setget

-   `void (No return value.)` **set\_process\_mode**(value:
    `ProcessMode<enum_Sky_ProcessMode>`)
-   `ProcessMode<enum_Sky_ProcessMode>` **get\_process\_mode**()

Sets the method for generating the radiance map from the sky. The
radiance map is a cubemap with increasingly blurry versions of the sky
corresponding to different levels of roughness. Radiance maps can be
expensive to calculate. See `ProcessMode<enum_Sky_ProcessMode>` for
options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`RadianceSize<enum_Sky_RadianceSize>` **radiance\_size** = `3`
`🔗<class_Sky_property_radiance_size>`

classref-property-setget

-   `void (No return value.)` **set\_radiance\_size**(value:
    `RadianceSize<enum_Sky_RadianceSize>`)
-   `RadianceSize<enum_Sky_RadianceSize>` **get\_radiance\_size**()

The **Sky**'s radiance map size. The higher the radiance map size, the
more detailed the lighting from the **Sky** will be.

See `RadianceSize<enum_Sky_RadianceSize>` constants for values.

\*\*Note:\*\* Some hardware will have trouble with higher radiance
sizes, especially
`RADIANCE_SIZE_512<class_Sky_constant_RADIANCE_SIZE_512>` and above.
Only use such high values on high-end hardware.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Material<class_Material>` **sky\_material**
`🔗<class_Sky_property_sky_material>`

classref-property-setget

-   `void (No return value.)` **set\_material**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_material**()

`Material<class_Material>` used to draw the background. Can be
`PanoramaSkyMaterial<class_PanoramaSkyMaterial>`,
`ProceduralSkyMaterial<class_ProceduralSkyMaterial>`,
`PhysicalSkyMaterial<class_PhysicalSkyMaterial>`, or even a
`ShaderMaterial<class_ShaderMaterial>` if you want to use your own
custom shader.
