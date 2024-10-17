github\_url  
hide

# LightmapGI

**Inherits:** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Computes and stores baked lightmaps for fast global illumination.

classref-introduction-group

## Description

The **LightmapGI** node is used to compute and store baked lightmaps.
Lightmaps are used to provide high-quality indirect lighting with very
little light leaking. **LightmapGI** can also provide rough reflections
using spherical harmonics if
`directional<class_LightmapGI_property_directional>` is enabled. Dynamic
objects can receive indirect lighting thanks to *light probes*, which
can be automatically placed by setting
`generate_probes_subdiv<class_LightmapGI_property_generate_probes_subdiv>`
to a value other than
`GENERATE_PROBES_DISABLED<class_LightmapGI_constant_GENERATE_PROBES_DISABLED>`.
Additional lightmap probes can also be added by creating
`LightmapProbe<class_LightmapProbe>` nodes. The downside is that
lightmaps are fully static and cannot be baked in an exported project.
Baking a **LightmapGI** node is also slower compared to
`VoxelGI<class_VoxelGI>`.

\*\*Procedural generation:\*\* Lightmap baking functionality is only
available in the editor. This means **LightmapGI** is not suited to
procedurally generated or user-built levels. For procedurally generated
or user-built levels, use `VoxelGI<class_VoxelGI>` or SDFGI instead (see
`Environment.sdfgi_enabled<class_Environment_property_sdfgi_enabled>`).

\*\*Performance:\*\* **LightmapGI** provides the best possible run-time
performance for global illumination. It is suitable for low-end hardware
including integrated graphics and mobile devices.

\*\*Note:\*\* Due to how lightmaps work, most properties only have a
visible effect once lightmaps are baked again.

\*\*Note:\*\* Lightmap baking on `CSGShape3D<class_CSGShape3D>`s and
`PrimitiveMesh<class_PrimitiveMesh>`es is not supported, as these cannot
store UV2 data required for baking.

\*\*Note:\*\* If no custom lightmappers are installed, **LightmapGI**
can only be baked from devices that support the Forward+ or Mobile
rendering backends.

classref-introduction-group

## Tutorials

-   `Using Lightmap global illumination <../tutorials/3d/global_illumination/using_lightmap_gi>`

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

## Enumerations

classref-enumeration

enum **BakeQuality**: `🔗<enum_LightmapGI_BakeQuality>`

classref-enumeration-constant

`BakeQuality<enum_LightmapGI_BakeQuality>` **BAKE\_QUALITY\_LOW** = `0`

Low bake quality (fastest bake times). The quality of this preset can be
adjusted by changing
`ProjectSettings.rendering/lightmapping/bake_quality/low_quality_ray_count<class_ProjectSettings_property_rendering/lightmapping/bake_quality/low_quality_ray_count>`
and
`ProjectSettings.rendering/lightmapping/bake_quality/low_quality_probe_ray_count<class_ProjectSettings_property_rendering/lightmapping/bake_quality/low_quality_probe_ray_count>`.

classref-enumeration-constant

`BakeQuality<enum_LightmapGI_BakeQuality>` **BAKE\_QUALITY\_MEDIUM** =
`1`

Medium bake quality (fast bake times). The quality of this preset can be
adjusted by changing
`ProjectSettings.rendering/lightmapping/bake_quality/medium_quality_ray_count<class_ProjectSettings_property_rendering/lightmapping/bake_quality/medium_quality_ray_count>`
and
`ProjectSettings.rendering/lightmapping/bake_quality/medium_quality_probe_ray_count<class_ProjectSettings_property_rendering/lightmapping/bake_quality/medium_quality_probe_ray_count>`.

classref-enumeration-constant

`BakeQuality<enum_LightmapGI_BakeQuality>` **BAKE\_QUALITY\_HIGH** = `2`

High bake quality (slow bake times). The quality of this preset can be
adjusted by changing
`ProjectSettings.rendering/lightmapping/bake_quality/high_quality_ray_count<class_ProjectSettings_property_rendering/lightmapping/bake_quality/high_quality_ray_count>`
and
`ProjectSettings.rendering/lightmapping/bake_quality/high_quality_probe_ray_count<class_ProjectSettings_property_rendering/lightmapping/bake_quality/high_quality_probe_ray_count>`.

classref-enumeration-constant

`BakeQuality<enum_LightmapGI_BakeQuality>` **BAKE\_QUALITY\_ULTRA** =
`3`

Highest bake quality (slowest bake times). The quality of this preset
can be adjusted by changing
`ProjectSettings.rendering/lightmapping/bake_quality/ultra_quality_ray_count<class_ProjectSettings_property_rendering/lightmapping/bake_quality/ultra_quality_ray_count>`
and
`ProjectSettings.rendering/lightmapping/bake_quality/ultra_quality_probe_ray_count<class_ProjectSettings_property_rendering/lightmapping/bake_quality/ultra_quality_probe_ray_count>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **GenerateProbes**: `🔗<enum_LightmapGI_GenerateProbes>`

classref-enumeration-constant

`GenerateProbes<enum_LightmapGI_GenerateProbes>`
**GENERATE\_PROBES\_DISABLED** = `0`

Don't generate lightmap probes for lighting dynamic objects.

classref-enumeration-constant

`GenerateProbes<enum_LightmapGI_GenerateProbes>`
**GENERATE\_PROBES\_SUBDIV\_4** = `1`

Lowest level of subdivision (fastest bake times, smallest file sizes).

classref-enumeration-constant

`GenerateProbes<enum_LightmapGI_GenerateProbes>`
**GENERATE\_PROBES\_SUBDIV\_8** = `2`

Low level of subdivision (fast bake times, small file sizes).

classref-enumeration-constant

`GenerateProbes<enum_LightmapGI_GenerateProbes>`
**GENERATE\_PROBES\_SUBDIV\_16** = `3`

High level of subdivision (slow bake times, large file sizes).

classref-enumeration-constant

`GenerateProbes<enum_LightmapGI_GenerateProbes>`
**GENERATE\_PROBES\_SUBDIV\_32** = `4`

Highest level of subdivision (slowest bake times, largest file sizes).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BakeError**: `🔗<enum_LightmapGI_BakeError>`

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>` **BAKE\_ERROR\_OK** = `0`

Lightmap baking was successful.

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>` **BAKE\_ERROR\_NO\_SCENE\_ROOT**
= `1`

Lightmap baking failed because the root node for the edited scene could
not be accessed.

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>` **BAKE\_ERROR\_FOREIGN\_DATA** =
`2`

Lightmap baking failed as the lightmap data resource is embedded in a
foreign resource.

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>` **BAKE\_ERROR\_NO\_LIGHTMAPPER**
= `3`

Lightmap baking failed as there is no lightmapper available in this
Godot build.

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>` **BAKE\_ERROR\_NO\_SAVE\_PATH** =
`4`

Lightmap baking failed as the `LightmapGIData<class_LightmapGIData>`
save path isn't configured in the resource.

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>` **BAKE\_ERROR\_NO\_MESHES** = `5`

Lightmap baking failed as there are no meshes whose
`GeometryInstance3D.gi_mode<class_GeometryInstance3D_property_gi_mode>`
is
`GeometryInstance3D.GI_MODE_STATIC<class_GeometryInstance3D_constant_GI_MODE_STATIC>`
and with valid UV2 mapping in the current scene. You may need to select
3D scenes in the Import dock and change their global illumination mode
accordingly.

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>` **BAKE\_ERROR\_MESHES\_INVALID**
= `6`

Lightmap baking failed as the lightmapper failed to analyze some of the
meshes marked as static for baking.

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>`
**BAKE\_ERROR\_CANT\_CREATE\_IMAGE** = `7`

Lightmap baking failed as the resulting image couldn't be saved or
imported by Godot after it was saved.

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>` **BAKE\_ERROR\_USER\_ABORTED** =
`8`

The user aborted the lightmap baking operation (typically by clicking
the **Cancel** button in the progress dialog).

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>`
**BAKE\_ERROR\_TEXTURE\_SIZE\_TOO\_SMALL** = `9`

Lightmap baking failed as the maximum texture size is too small to fit
some of the meshes marked for baking.

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>`
**BAKE\_ERROR\_LIGHTMAP\_TOO\_SMALL** = `10`

Lightmap baking failed as the lightmap is too small.

classref-enumeration-constant

`BakeError<enum_LightmapGI_BakeError>`
**BAKE\_ERROR\_ATLAS\_TOO\_SMALL** = `11`

Lightmap baking failed as the lightmap was unable to fit into an atlas.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentMode**: `🔗<enum_LightmapGI_EnvironmentMode>`

classref-enumeration-constant

`EnvironmentMode<enum_LightmapGI_EnvironmentMode>`
**ENVIRONMENT\_MODE\_DISABLED** = `0`

Ignore environment lighting when baking lightmaps.

classref-enumeration-constant

`EnvironmentMode<enum_LightmapGI_EnvironmentMode>`
**ENVIRONMENT\_MODE\_SCENE** = `1`

Use the scene's environment lighting when baking lightmaps.

\*\*Note:\*\* If baking lightmaps in a scene with no
`WorldEnvironment<class_WorldEnvironment>` node, this will act like
`ENVIRONMENT_MODE_DISABLED<class_LightmapGI_constant_ENVIRONMENT_MODE_DISABLED>`.
The editor's preview sky and sun is *not* taken into account by
**LightmapGI** when baking lightmaps.

classref-enumeration-constant

`EnvironmentMode<enum_LightmapGI_EnvironmentMode>`
**ENVIRONMENT\_MODE\_CUSTOM\_SKY** = `2`

Use
`environment_custom_sky<class_LightmapGI_property_environment_custom_sky>`
as a source of environment lighting when baking lightmaps.

classref-enumeration-constant

`EnvironmentMode<enum_LightmapGI_EnvironmentMode>`
**ENVIRONMENT\_MODE\_CUSTOM\_COLOR** = `3`

Use
`environment_custom_color<class_LightmapGI_property_environment_custom_color>`
multiplied by
`environment_custom_energy<class_LightmapGI_property_environment_custom_energy>`
as a constant source of environment lighting when baking lightmaps.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **bias** = `0.0005`
`🔗<class_LightmapGI_property_bias>`

classref-property-setget

-   `void (No return value.)` **set\_bias**(value: `float<class_float>`)
-   `float<class_float>` **get\_bias**()

The bias to use when computing shadows. Increasing
`bias<class_LightmapGI_property_bias>` can fix shadow acne on the
resulting baked lightmap, but can introduce peter-panning (shadows not
connecting to their casters). Real-time `Light3D<class_Light3D>` shadows
are not affected by this `bias<class_LightmapGI_property_bias>`
property.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **bounce\_indirect\_energy** = `1.0`
`🔗<class_LightmapGI_property_bounce_indirect_energy>`

classref-property-setget

-   `void (No return value.)` **set\_bounce\_indirect\_energy**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_bounce\_indirect\_energy**()

The energy multiplier for each bounce. Higher values will make indirect
lighting brighter. A value of `1.0` represents physically accurate
behavior, but higher values can be used to make indirect lighting
propagate more visibly when using a low number of bounces. This can be
used to speed up bake times by lowering the number of
`bounces<class_LightmapGI_property_bounces>` then increasing
`bounce_indirect_energy<class_LightmapGI_property_bounce_indirect_energy>`.

\*\*Note:\*\*
`bounce_indirect_energy<class_LightmapGI_property_bounce_indirect_energy>`
only has an effect if `bounces<class_LightmapGI_property_bounces>` is
set to a value greater than or equal to `1`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **bounces** = `3`
`🔗<class_LightmapGI_property_bounces>`

classref-property-setget

-   `void (No return value.)` **set\_bounces**(value: `int<class_int>`)
-   `int<class_int>` **get\_bounces**()

Number of light bounces that are taken into account during baking.
Higher values result in brighter, more realistic lighting, at the cost
of longer bake times. If set to `0`, only environment lighting, direct
light and emissive lighting is baked.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CameraAttributes<class_CameraAttributes>` **camera\_attributes**
`🔗<class_LightmapGI_property_camera_attributes>`

classref-property-setget

-   `void (No return value.)` **set\_camera\_attributes**(value:
    `CameraAttributes<class_CameraAttributes>`)
-   `CameraAttributes<class_CameraAttributes>`
    **get\_camera\_attributes**()

The `CameraAttributes<class_CameraAttributes>` resource that specifies
exposure levels to bake at. Auto-exposure and non exposure properties
will be ignored. Exposure settings should be used to reduce the dynamic
range present when baking. If exposure is too high, the **LightmapGI**
will have banding artifacts or may have over-exposure artifacts.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **denoiser\_range** = `10`
`🔗<class_LightmapGI_property_denoiser_range>`

classref-property-setget

-   `void (No return value.)` **set\_denoiser\_range**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_denoiser\_range**()

The distance in pixels from which the denoiser samples. Lower values
preserve more details, but may give blotchy results if the lightmap
quality is not high enough. Only effective if
`use_denoiser<class_LightmapGI_property_use_denoiser>` is `true` and
`ProjectSettings.rendering/lightmapping/denoising/denoiser<class_ProjectSettings_property_rendering/lightmapping/denoising/denoiser>`
is set to JNLM.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **denoiser\_strength** = `0.1`
`🔗<class_LightmapGI_property_denoiser_strength>`

classref-property-setget

-   `void (No return value.)` **set\_denoiser\_strength**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_denoiser\_strength**()

The strength of denoising step applied to the generated lightmaps. Only
effective if `use_denoiser<class_LightmapGI_property_use_denoiser>` is
`true` and
`ProjectSettings.rendering/lightmapping/denoising/denoiser<class_ProjectSettings_property_rendering/lightmapping/denoising/denoiser>`
is set to JNLM.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **directional** = `false`
`🔗<class_LightmapGI_property_directional>`

classref-property-setget

-   `void (No return value.)` **set\_directional**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_directional**()

If `true`, bakes lightmaps to contain directional information as
spherical harmonics. This results in more realistic lighting appearance,
especially with normal mapped materials and for lights that have their
direct light baked
(`Light3D.light_bake_mode<class_Light3D_property_light_bake_mode>` set
to `Light3D.BAKE_STATIC<class_Light3D_constant_BAKE_STATIC>` and with
`Light3D.editor_only<class_Light3D_property_editor_only>` set to
`false`). The directional information is also used to provide rough
reflections for static and dynamic objects. This has a small run-time
performance cost as the shader has to perform more work to interpret the
direction information from the lightmap. Directional lightmaps also take
longer to bake and result in larger file sizes.

\*\*Note:\*\* The property's name has no relationship with
`DirectionalLight3D<class_DirectionalLight3D>`.
`directional<class_LightmapGI_property_directional>` works with all
light types.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **environment\_custom\_color**
`🔗<class_LightmapGI_property_environment_custom_color>`

classref-property-setget

-   `void (No return value.)` **set\_environment\_custom\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_environment\_custom\_color**()

The color to use for environment lighting. Only effective if
`environment_mode<class_LightmapGI_property_environment_mode>` is
`ENVIRONMENT_MODE_CUSTOM_COLOR<class_LightmapGI_constant_ENVIRONMENT_MODE_CUSTOM_COLOR>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **environment\_custom\_energy**
`🔗<class_LightmapGI_property_environment_custom_energy>`

classref-property-setget

-   `void (No return value.)`
    **set\_environment\_custom\_energy**(value: `float<class_float>`)
-   `float<class_float>` **get\_environment\_custom\_energy**()

The color multiplier to use for environment lighting. Only effective if
`environment_mode<class_LightmapGI_property_environment_mode>` is
`ENVIRONMENT_MODE_CUSTOM_COLOR<class_LightmapGI_constant_ENVIRONMENT_MODE_CUSTOM_COLOR>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Sky<class_Sky>` **environment\_custom\_sky**
`🔗<class_LightmapGI_property_environment_custom_sky>`

classref-property-setget

-   `void (No return value.)` **set\_environment\_custom\_sky**(value:
    `Sky<class_Sky>`)
-   `Sky<class_Sky>` **get\_environment\_custom\_sky**()

The sky to use as a source of environment lighting. Only effective if
`environment_mode<class_LightmapGI_property_environment_mode>` is
`ENVIRONMENT_MODE_CUSTOM_SKY<class_LightmapGI_constant_ENVIRONMENT_MODE_CUSTOM_SKY>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`EnvironmentMode<enum_LightmapGI_EnvironmentMode>` **environment\_mode**
= `1` `🔗<class_LightmapGI_property_environment_mode>`

classref-property-setget

-   `void (No return value.)` **set\_environment\_mode**(value:
    `EnvironmentMode<enum_LightmapGI_EnvironmentMode>`)
-   `EnvironmentMode<enum_LightmapGI_EnvironmentMode>`
    **get\_environment\_mode**()

The environment mode to use when baking lightmaps.

classref-item-separator

------------------------------------------------------------------------

classref-property

`GenerateProbes<enum_LightmapGI_GenerateProbes>`
**generate\_probes\_subdiv** = `2`
`🔗<class_LightmapGI_property_generate_probes_subdiv>`

classref-property-setget

-   `void (No return value.)` **set\_generate\_probes**(value:
    `GenerateProbes<enum_LightmapGI_GenerateProbes>`)
-   `GenerateProbes<enum_LightmapGI_GenerateProbes>`
    **get\_generate\_probes**()

The level of subdivision to use when automatically generating
`LightmapProbe<class_LightmapProbe>`s for dynamic object lighting.
Higher values result in more accurate indirect lighting on dynamic
objects, at the cost of longer bake times and larger file sizes.

\*\*Note:\*\* Automatically generated
`LightmapProbe<class_LightmapProbe>`s are not visible as nodes in the
Scene tree dock, and cannot be modified this way after they are
generated.

\*\*Note:\*\* Regardless of
`generate_probes_subdiv<class_LightmapGI_property_generate_probes_subdiv>`,
direct lighting on dynamic objects is always applied using
`Light3D<class_Light3D>` nodes in real-time.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interior** = `false`
`🔗<class_LightmapGI_property_interior>`

classref-property-setget

-   `void (No return value.)` **set\_interior**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_interior**()

If `true`, ignore environment lighting when baking lightmaps.

classref-item-separator

------------------------------------------------------------------------

classref-property

`LightmapGIData<class_LightmapGIData>` **light\_data**
`🔗<class_LightmapGI_property_light_data>`

classref-property-setget

-   `void (No return value.)` **set\_light\_data**(value:
    `LightmapGIData<class_LightmapGIData>`)
-   `LightmapGIData<class_LightmapGIData>` **get\_light\_data**()

The `LightmapGIData<class_LightmapGIData>` associated to this
**LightmapGI** node. This resource is automatically created after
baking, and is not meant to be created manually.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_texture\_size** = `16384`
`🔗<class_LightmapGI_property_max_texture_size>`

classref-property-setget

-   `void (No return value.)` **set\_max\_texture\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_texture\_size**()

The maximum texture size for the generated texture atlas. Higher values
will result in fewer slices being generated, but may not work on all
hardware as a result of hardware limitations on texture sizes. Leave
`max_texture_size<class_LightmapGI_property_max_texture_size>` at its
default value of `16384` if unsure.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BakeQuality<enum_LightmapGI_BakeQuality>` **quality** = `1`
`🔗<class_LightmapGI_property_quality>`

classref-property-setget

-   `void (No return value.)` **set\_bake\_quality**(value:
    `BakeQuality<enum_LightmapGI_BakeQuality>`)
-   `BakeQuality<enum_LightmapGI_BakeQuality>` **get\_bake\_quality**()

The quality preset to use when baking lightmaps. This affects bake
times, but output file sizes remain mostly identical across quality
levels.

To further speed up bake times, decrease
`bounces<class_LightmapGI_property_bounces>`, disable
`use_denoiser<class_LightmapGI_property_use_denoiser>` and increase the
lightmap texel size on 3D scenes in the Import doc.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **texel\_scale** = `1.0`
`🔗<class_LightmapGI_property_texel_scale>`

classref-property-setget

-   `void (No return value.)` **set\_texel\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_texel\_scale**()

Scales the lightmap texel density of all meshes for the current bake.
This is a multiplier that builds upon the existing lightmap texel size
defined in each imported 3D scene, along with the per-mesh density
multiplier (which is designed to be used when the same mesh is used at
different scales). Lower values will result in faster bake times.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_denoiser** = `true`
`🔗<class_LightmapGI_property_use_denoiser>`

classref-property-setget

-   `void (No return value.)` **set\_use\_denoiser**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_denoiser**()

If `true`, uses a GPU-based denoising algorithm on the generated
lightmap. This eliminates most noise within the generated lightmap at
the cost of longer bake times. File sizes are generally not impacted
significantly by the use of a denoiser, although lossless compression
may do a better job at compressing a denoised image.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_texture\_for\_bounces** = `true`
`🔗<class_LightmapGI_property_use_texture_for_bounces>`

classref-property-setget

-   `void (No return value.)` **set\_use\_texture\_for\_bounces**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_texture\_for\_bounces**()

If `true`, a texture with the lighting information will be generated to
speed up the generation of indirect lighting at the cost of some
accuracy. The geometry might exhibit extra light leak artifacts when
using low resolution lightmaps or UVs that stretch the lightmap
significantly across surfaces. Leave
`use_texture_for_bounces<class_LightmapGI_property_use_texture_for_bounces>`
at its default value of `true` if unsure.

\*\*Note:\*\*
`use_texture_for_bounces<class_LightmapGI_property_use_texture_for_bounces>`
only has an effect if `bounces<class_LightmapGI_property_bounces>` is
set to a value greater than or equal to `1`.
