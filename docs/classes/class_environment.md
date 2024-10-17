github\_url  
hide

# Environment

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Resource for environment nodes (like
`WorldEnvironment<class_WorldEnvironment>`) that define multiple
rendering options.

classref-introduction-group

## Description

Resource for environment nodes (like
`WorldEnvironment<class_WorldEnvironment>`) that define multiple
environment operations (such as background `Sky<class_Sky>` or
`Color<class_Color>`, ambient light, fog, depth-of-field...). These
parameters affect the final render of the scene. The order of these
operations is:

-   Depth of Field Blur
-   Glow
-   Tonemap (Auto Exposure)
-   Adjustments

classref-introduction-group

## Tutorials

-   `Environment and post-processing <../tutorials/3d/environment_and_post_processing>`
-   `High dynamic range lighting <../tutorials/3d/high_dynamic_range>`
-   [3D Material Testers
    Demo](https://godotengine.org/asset-library/asset/2742)
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **BGMode**: `🔗<enum_Environment_BGMode>`

classref-enumeration-constant

`BGMode<enum_Environment_BGMode>` **BG\_CLEAR\_COLOR** = `0`

Clears the background using the clear color defined in
`ProjectSettings.rendering/environment/defaults/default_clear_color<class_ProjectSettings_property_rendering/environment/defaults/default_clear_color>`.

classref-enumeration-constant

`BGMode<enum_Environment_BGMode>` **BG\_COLOR** = `1`

Clears the background using a custom clear color.

classref-enumeration-constant

`BGMode<enum_Environment_BGMode>` **BG\_SKY** = `2`

Displays a user-defined sky in the background.

classref-enumeration-constant

`BGMode<enum_Environment_BGMode>` **BG\_CANVAS** = `3`

Displays a `CanvasLayer<class_CanvasLayer>` in the background.

classref-enumeration-constant

`BGMode<enum_Environment_BGMode>` **BG\_KEEP** = `4`

Keeps on screen every pixel drawn in the background. This is the fastest
background mode, but it can only be safely used in fully-interior scenes
(no visible sky or sky reflections). If enabled in a scene where the
background is visible, "ghost trail" artifacts will be visible when
moving the camera.

classref-enumeration-constant

`BGMode<enum_Environment_BGMode>` **BG\_CAMERA\_FEED** = `5`

Displays a camera feed in the background.

classref-enumeration-constant

`BGMode<enum_Environment_BGMode>` **BG\_MAX** = `6`

Represents the size of the `BGMode<enum_Environment_BGMode>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AmbientSource**: `🔗<enum_Environment_AmbientSource>`

classref-enumeration-constant

`AmbientSource<enum_Environment_AmbientSource>` **AMBIENT\_SOURCE\_BG**
= `0`

Gather ambient light from whichever source is specified as the
background.

classref-enumeration-constant

`AmbientSource<enum_Environment_AmbientSource>`
**AMBIENT\_SOURCE\_DISABLED** = `1`

Disable ambient light. This provides a slight performance boost over
`AMBIENT_SOURCE_SKY<class_Environment_constant_AMBIENT_SOURCE_SKY>`.

classref-enumeration-constant

`AmbientSource<enum_Environment_AmbientSource>`
**AMBIENT\_SOURCE\_COLOR** = `2`

Specify a specific `Color<class_Color>` for ambient light. This provides
a slight performance boost over
`AMBIENT_SOURCE_SKY<class_Environment_constant_AMBIENT_SOURCE_SKY>`.

classref-enumeration-constant

`AmbientSource<enum_Environment_AmbientSource>` **AMBIENT\_SOURCE\_SKY**
= `3`

Gather ambient light from the `Sky<class_Sky>` regardless of what the
background is.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ReflectionSource**: `🔗<enum_Environment_ReflectionSource>`

classref-enumeration-constant

`ReflectionSource<enum_Environment_ReflectionSource>`
**REFLECTION\_SOURCE\_BG** = `0`

Use the background for reflections.

classref-enumeration-constant

`ReflectionSource<enum_Environment_ReflectionSource>`
**REFLECTION\_SOURCE\_DISABLED** = `1`

Disable reflections. This provides a slight performance boost over other
options.

classref-enumeration-constant

`ReflectionSource<enum_Environment_ReflectionSource>`
**REFLECTION\_SOURCE\_SKY** = `2`

Use the `Sky<class_Sky>` for reflections regardless of what the
background is.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ToneMapper**: `🔗<enum_Environment_ToneMapper>`

classref-enumeration-constant

`ToneMapper<enum_Environment_ToneMapper>` **TONE\_MAPPER\_LINEAR** = `0`

Linear tonemapper operator. Reads the linear data and passes it on
unmodified. This can cause bright lighting to look blown out, with
noticeable clipping in the output colors.

classref-enumeration-constant

`ToneMapper<enum_Environment_ToneMapper>` **TONE\_MAPPER\_REINHARDT** =
`1`

Reinhard tonemapper operator. Performs a variation on rendered pixels'
colors by this formula:
`color = color * (1 + color / (white * white)) / (1 + color)`. This
avoids clipping bright highlights, but the resulting image can look a
bit dull. When `tonemap_white<class_Environment_property_tonemap_white>`
is left at the default value of `1.0` this is identical to
`TONE_MAPPER_LINEAR<class_Environment_constant_TONE_MAPPER_LINEAR>`
while also being slightly less performant.

classref-enumeration-constant

`ToneMapper<enum_Environment_ToneMapper>` **TONE\_MAPPER\_FILMIC** = `2`

Filmic tonemapper operator. This avoids clipping bright highlights, with
a resulting image that usually looks more vivid than
`TONE_MAPPER_REINHARDT<class_Environment_constant_TONE_MAPPER_REINHARDT>`.

classref-enumeration-constant

`ToneMapper<enum_Environment_ToneMapper>` **TONE\_MAPPER\_ACES** = `3`

Use the Academy Color Encoding System tonemapper. ACES is slightly more
expensive than other options, but it handles bright lighting in a more
realistic fashion by desaturating it as it becomes brighter. ACES
typically has a more contrasted output compared to
`TONE_MAPPER_REINHARDT<class_Environment_constant_TONE_MAPPER_REINHARDT>`
and `TONE_MAPPER_FILMIC<class_Environment_constant_TONE_MAPPER_FILMIC>`.

\*\*Note:\*\* This tonemapping operator is called "ACES Fitted" in Godot
3.x.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **GlowBlendMode**: `🔗<enum_Environment_GlowBlendMode>`

classref-enumeration-constant

`GlowBlendMode<enum_Environment_GlowBlendMode>`
**GLOW\_BLEND\_MODE\_ADDITIVE** = `0`

Additive glow blending mode. Mostly used for particles, glows (bloom),
lens flare, bright sources.

classref-enumeration-constant

`GlowBlendMode<enum_Environment_GlowBlendMode>`
**GLOW\_BLEND\_MODE\_SCREEN** = `1`

Screen glow blending mode. Increases brightness, used frequently with
bloom.

classref-enumeration-constant

`GlowBlendMode<enum_Environment_GlowBlendMode>`
**GLOW\_BLEND\_MODE\_SOFTLIGHT** = `2`

Soft light glow blending mode. Modifies contrast, exposes shadows and
highlights (vivid bloom).

classref-enumeration-constant

`GlowBlendMode<enum_Environment_GlowBlendMode>`
**GLOW\_BLEND\_MODE\_REPLACE** = `3`

Replace glow blending mode. Replaces all pixels' color by the glow
value. This can be used to simulate a full-screen blur effect by
tweaking the glow parameters to match the original image's brightness.

classref-enumeration-constant

`GlowBlendMode<enum_Environment_GlowBlendMode>`
**GLOW\_BLEND\_MODE\_MIX** = `4`

Mixes the glow with the underlying color to avoid increasing brightness
as much while still maintaining a glow effect.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **FogMode**: `🔗<enum_Environment_FogMode>`

classref-enumeration-constant

`FogMode<enum_Environment_FogMode>` **FOG\_MODE\_EXPONENTIAL** = `0`

Use a physically-based fog model defined primarily by fog density.

classref-enumeration-constant

`FogMode<enum_Environment_FogMode>` **FOG\_MODE\_DEPTH** = `1`

Use a simple fog model defined by start and end positions and a custom
curve. While not physically accurate, this model can be useful when you
need more artistic control.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SDFGIYScale**: `🔗<enum_Environment_SDFGIYScale>`

classref-enumeration-constant

`SDFGIYScale<enum_Environment_SDFGIYScale>`
**SDFGI\_Y\_SCALE\_50\_PERCENT** = `0`

Use 50% scale for SDFGI on the Y (vertical) axis. SDFGI cells will be
twice as short as they are wide. This allows providing increased GI
detail and reduced light leaking with thin floors and ceilings. This is
usually the best choice for scenes that don't feature much verticality.

classref-enumeration-constant

`SDFGIYScale<enum_Environment_SDFGIYScale>`
**SDFGI\_Y\_SCALE\_75\_PERCENT** = `1`

Use 75% scale for SDFGI on the Y (vertical) axis. This is a balance
between the 50% and 100% SDFGI Y scales.

classref-enumeration-constant

`SDFGIYScale<enum_Environment_SDFGIYScale>`
**SDFGI\_Y\_SCALE\_100\_PERCENT** = `2`

Use 100% scale for SDFGI on the Y (vertical) axis. SDFGI cells will be
as tall as they are wide. This is usually the best choice for highly
vertical scenes. The downside is that light leaking may become more
noticeable with thin floors and ceilings.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **adjustment\_brightness** = `1.0`
`🔗<class_Environment_property_adjustment_brightness>`

classref-property-setget

-   `void (No return value.)` **set\_adjustment\_brightness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_adjustment\_brightness**()

The global brightness value of the rendered scene. Effective only if
`adjustment_enabled<class_Environment_property_adjustment_enabled>` is
`true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture<class_Texture>` **adjustment\_color\_correction**
`🔗<class_Environment_property_adjustment_color_correction>`

classref-property-setget

-   `void (No return value.)`
    **set\_adjustment\_color\_correction**(value:
    `Texture<class_Texture>`)
-   `Texture<class_Texture>` **get\_adjustment\_color\_correction**()

The `Texture2D<class_Texture2D>` or `Texture3D<class_Texture3D>` lookup
table (LUT) to use for the built-in post-process color grading. Can use
a `GradientTexture1D<class_GradientTexture1D>` for a 1-dimensional LUT,
or a `Texture3D<class_Texture3D>` for a more complex LUT. Effective only
if `adjustment_enabled<class_Environment_property_adjustment_enabled>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **adjustment\_contrast** = `1.0`
`🔗<class_Environment_property_adjustment_contrast>`

classref-property-setget

-   `void (No return value.)` **set\_adjustment\_contrast**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_adjustment\_contrast**()

The global contrast value of the rendered scene (default value is 1).
Effective only if
`adjustment_enabled<class_Environment_property_adjustment_enabled>` is
`true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **adjustment\_enabled** = `false`
`🔗<class_Environment_property_adjustment_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_adjustment\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_adjustment\_enabled**()

If `true`, enables the `adjustment_*` properties provided by this
resource. If `false`, modifications to the `adjustment_*` properties
will have no effect on the rendered scene.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **adjustment\_saturation** = `1.0`
`🔗<class_Environment_property_adjustment_saturation>`

classref-property-setget

-   `void (No return value.)` **set\_adjustment\_saturation**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_adjustment\_saturation**()

The global color saturation value of the rendered scene (default value
is 1). Effective only if
`adjustment_enabled<class_Environment_property_adjustment_enabled>` is
`true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **ambient\_light\_color** = `Color(0, 0, 0, 1)`
`🔗<class_Environment_property_ambient_light_color>`

classref-property-setget

-   `void (No return value.)` **set\_ambient\_light\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_ambient\_light\_color**()

The ambient light's `Color<class_Color>`. Only effective if
`ambient_light_sky_contribution<class_Environment_property_ambient_light_sky_contribution>`
is lower than `1.0` (exclusive).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ambient\_light\_energy** = `1.0`
`🔗<class_Environment_property_ambient_light_energy>`

classref-property-setget

-   `void (No return value.)` **set\_ambient\_light\_energy**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ambient\_light\_energy**()

The ambient light's energy. The higher the value, the stronger the
light. Only effective if
`ambient_light_sky_contribution<class_Environment_property_ambient_light_sky_contribution>`
is lower than `1.0` (exclusive).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ambient\_light\_sky\_contribution** = `1.0`
`🔗<class_Environment_property_ambient_light_sky_contribution>`

classref-property-setget

-   `void (No return value.)`
    **set\_ambient\_light\_sky\_contribution**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ambient\_light\_sky\_contribution**()

Defines the amount of light that the sky brings on the scene. A value of
`0.0` means that the sky's light emission has no effect on the scene
illumination, thus all ambient illumination is provided by the ambient
light. On the contrary, a value of `1.0` means that *all* the light that
affects the scene is provided by the sky, thus the ambient light
parameter has no effect on the scene.

\*\*Note:\*\*
`ambient_light_sky_contribution<class_Environment_property_ambient_light_sky_contribution>`
is internally clamped between `0.0` and `1.0` (inclusive).

classref-item-separator

------------------------------------------------------------------------

classref-property

`AmbientSource<enum_Environment_AmbientSource>`
**ambient\_light\_source** = `0`
`🔗<class_Environment_property_ambient_light_source>`

classref-property-setget

-   `void (No return value.)` **set\_ambient\_source**(value:
    `AmbientSource<enum_Environment_AmbientSource>`)
-   `AmbientSource<enum_Environment_AmbientSource>`
    **get\_ambient\_source**()

The ambient light source to use for rendering materials and global
illumination.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **background\_camera\_feed\_id** = `1`
`🔗<class_Environment_property_background_camera_feed_id>`

classref-property-setget

-   `void (No return value.)` **set\_camera\_feed\_id**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_camera\_feed\_id**()

The ID of the camera feed to show in the background.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **background\_canvas\_max\_layer** = `0`
`🔗<class_Environment_property_background_canvas_max_layer>`

classref-property-setget

-   `void (No return value.)` **set\_canvas\_max\_layer**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_canvas\_max\_layer**()

The maximum layer ID to display. Only effective when using the
`BG_CANVAS<class_Environment_constant_BG_CANVAS>` background mode.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **background\_color** = `Color(0, 0, 0, 1)`
`🔗<class_Environment_property_background_color>`

classref-property-setget

-   `void (No return value.)` **set\_bg\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_bg\_color**()

The `Color<class_Color>` displayed for clear areas of the scene. Only
effective when using the `BG_COLOR<class_Environment_constant_BG_COLOR>`
background mode.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **background\_energy\_multiplier** = `1.0`
`🔗<class_Environment_property_background_energy_multiplier>`

classref-property-setget

-   `void (No return value.)` **set\_bg\_energy\_multiplier**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_bg\_energy\_multiplier**()

Multiplier for background energy. Increase to make background brighter,
decrease to make background dimmer.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **background\_intensity** = `30000.0`
`🔗<class_Environment_property_background_intensity>`

classref-property-setget

-   `void (No return value.)` **set\_bg\_intensity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_bg\_intensity**()

Luminance of background measured in nits (candela per square meter).
Only used when
`ProjectSettings.rendering/lights_and_shadows/use_physical_light_units<class_ProjectSettings_property_rendering/lights_and_shadows/use_physical_light_units>`
is enabled. The default value is roughly equivalent to the sky at
midday.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BGMode<enum_Environment_BGMode>` **background\_mode** = `0`
`🔗<class_Environment_property_background_mode>`

classref-property-setget

-   `void (No return value.)` **set\_background**(value:
    `BGMode<enum_Environment_BGMode>`)
-   `BGMode<enum_Environment_BGMode>` **get\_background**()

The background mode. See `BGMode<enum_Environment_BGMode>` for possible
values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fog\_aerial\_perspective** = `0.0`
`🔗<class_Environment_property_fog_aerial_perspective>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_aerial\_perspective**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fog\_aerial\_perspective**()

If set above `0.0` (exclusive), blends between the fog's color and the
color of the background `Sky<class_Sky>`, as read from the radiance
cubemap. This has a small performance cost when set above `0.0`. Must
have `background_mode<class_Environment_property_background_mode>` set
to `BG_SKY<class_Environment_constant_BG_SKY>`.

This is useful to simulate [aerial
perspective](https://en.wikipedia.org/wiki/Aerial_perspective) in large
scenes with low density fog. However, it is not very useful for
high-density fog, as the sky will shine through. When set to `1.0`, the
fog color comes completely from the `Sky<class_Sky>`. If set to `0.0`,
aerial perspective is disabled.

Notice that this does not sample the `Sky<class_Sky>` directly, but
rather the radiance cubemap. The cubemap is sampled at a mipmap level
depending on the depth of the rendered pixel; the farther away, the
higher the resolution of the sampled mipmap. This results in the actual
color being a blurred version of the sky, with more blur closer to the
camera. The highest mipmap resolution is used at a depth of
`Camera3D.far<class_Camera3D_property_far>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fog\_density** = `0.01`
`🔗<class_Environment_property_fog_density>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_density**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fog\_density**()

The fog density to be used. This is demonstrated in different ways
depending on the `fog_mode<class_Environment_property_fog_mode>` mode
chosen:

\*\*Exponential Fog Mode:\*\* Higher values result in denser fog. The
fog rendering is exponential like in real life.

\*\*Depth Fog mode:\*\* The maximum intensity of the deep fog, effect
will appear in the distance (relative to the camera). At `1.0` the fog
will fully obscure the scene, at `0.0` the fog will not be visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fog\_depth\_begin** = `10.0`
`🔗<class_Environment_property_fog_depth_begin>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_depth\_begin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fog\_depth\_begin**()

The fog's depth starting distance from the camera. Only available when
`fog_mode<class_Environment_property_fog_mode>` is set to
`FOG_MODE_DEPTH<class_Environment_constant_FOG_MODE_DEPTH>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fog\_depth\_curve** = `1.0`
`🔗<class_Environment_property_fog_depth_curve>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_depth\_curve**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fog\_depth\_curve**()

The fog depth's intensity curve. A number of presets are available in
the Inspector by right-clicking the curve. Only available when
`fog_mode<class_Environment_property_fog_mode>` is set to
`FOG_MODE_DEPTH<class_Environment_constant_FOG_MODE_DEPTH>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fog\_depth\_end** = `100.0`
`🔗<class_Environment_property_fog_depth_end>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_depth\_end**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fog\_depth\_end**()

The fog's depth end distance from the camera. If this value is set to
`0`, it will be equal to the current camera's
`Camera3D.far<class_Camera3D_property_far>` value. Only available when
`fog_mode<class_Environment_property_fog_mode>` is set to
`FOG_MODE_DEPTH<class_Environment_constant_FOG_MODE_DEPTH>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **fog\_enabled** = `false`
`🔗<class_Environment_property_fog_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_fog\_enabled**()

If `true`, fog effects are enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fog\_height** = `0.0`
`🔗<class_Environment_property_fog_height>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_height**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fog\_height**()

The height at which the height fog effect begins.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fog\_height\_density** = `0.0`
`🔗<class_Environment_property_fog_height_density>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_height\_density**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fog\_height\_density**()

The density used to increase fog as height decreases. To make fog
increase as height increases, use a negative value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **fog\_light\_color** =
`Color(0.518, 0.553, 0.608, 1)`
`🔗<class_Environment_property_fog_light_color>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_light\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_fog\_light\_color**()

The fog's color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fog\_light\_energy** = `1.0`
`🔗<class_Environment_property_fog_light_energy>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_light\_energy**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fog\_light\_energy**()

The fog's brightness. Higher values result in brighter fog.

classref-item-separator

------------------------------------------------------------------------

classref-property

`FogMode<enum_Environment_FogMode>` **fog\_mode** = `0`
`🔗<class_Environment_property_fog_mode>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_mode**(value:
    `FogMode<enum_Environment_FogMode>`)
-   `FogMode<enum_Environment_FogMode>` **get\_fog\_mode**()

The fog mode. See `FogMode<enum_Environment_FogMode>` for possible
values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fog\_sky\_affect** = `1.0`
`🔗<class_Environment_property_fog_sky_affect>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_sky\_affect**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fog\_sky\_affect**()

The factor to use when affecting the sky with non-volumetric fog. `1.0`
means that fog can fully obscure the sky. Lower values reduce the impact
of fog on sky rendering, with `0.0` not affecting sky rendering at all.

\*\*Note:\*\*
`fog_sky_affect<class_Environment_property_fog_sky_affect>` has no
visual effect if
`fog_aerial_perspective<class_Environment_property_fog_aerial_perspective>`
is `1.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fog\_sun\_scatter** = `0.0`
`🔗<class_Environment_property_fog_sun_scatter>`

classref-property-setget

-   `void (No return value.)` **set\_fog\_sun\_scatter**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fog\_sun\_scatter**()

If set above `0.0`, renders the scene's directional light(s) in the fog
color depending on the view angle. This can be used to give the
impression that the sun is "piercing" through the fog.

classref-item-separator

------------------------------------------------------------------------

classref-property

`GlowBlendMode<enum_Environment_GlowBlendMode>` **glow\_blend\_mode** =
`2` `🔗<class_Environment_property_glow_blend_mode>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_blend\_mode**(value:
    `GlowBlendMode<enum_Environment_GlowBlendMode>`)
-   `GlowBlendMode<enum_Environment_GlowBlendMode>`
    **get\_glow\_blend\_mode**()

The glow blending mode.

\*\*Note:\*\*
`glow_blend_mode<class_Environment_property_glow_blend_mode>` has no
effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_bloom** = `0.0`
`🔗<class_Environment_property_glow_bloom>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_bloom**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_glow\_bloom**()

The bloom's intensity. If set to a value higher than `0`, this will make
glow visible in areas darker than the
`glow_hdr_threshold<class_Environment_property_glow_hdr_threshold>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **glow\_enabled** = `false`
`🔗<class_Environment_property_glow_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_glow\_enabled**()

If `true`, the glow effect is enabled. This simulates real world
eye/camera behavior where bright pixels bleed onto surrounding pixels.

\*\*Note:\*\* When using the Mobile rendering method, glow looks
different due to the lower dynamic range available in the Mobile
rendering method.

\*\*Note:\*\* When using the Compatibility rendering method, glow uses a
different implementation with some properties being unavailable and
hidden from the inspector: `glow_levels/*`,
`glow_normalized<class_Environment_property_glow_normalized>`,
`glow_strength<class_Environment_property_glow_strength>`,
`glow_blend_mode<class_Environment_property_glow_blend_mode>`,
`glow_mix<class_Environment_property_glow_mix>`,
`glow_map<class_Environment_property_glow_map>`, and
`glow_map_strength<class_Environment_property_glow_map_strength>`. This
implementation is optimized to run on low-end devices and is less
flexible as a result.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_hdr\_luminance\_cap** = `12.0`
`🔗<class_Environment_property_glow_hdr_luminance_cap>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_hdr\_luminance\_cap**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_glow\_hdr\_luminance\_cap**()

The higher threshold of the HDR glow. Areas brighter than this threshold
will be clamped for the purposes of the glow effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_hdr\_scale** = `2.0`
`🔗<class_Environment_property_glow_hdr_scale>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_hdr\_bleed\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_glow\_hdr\_bleed\_scale**()

The bleed scale of the HDR glow.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_hdr\_threshold** = `1.0`
`🔗<class_Environment_property_glow_hdr_threshold>`

classref-property-setget

-   `void (No return value.)`
    **set\_glow\_hdr\_bleed\_threshold**(value: `float<class_float>`)
-   `float<class_float>` **get\_glow\_hdr\_bleed\_threshold**()

The lower threshold of the HDR glow. When using the Mobile rendering
method (which only supports a lower dynamic range up to `2.0`), this may
need to be below `1.0` for glow to be visible. A value of `0.9` works
well in this case. This value also needs to be decreased below `1.0`
when using glow in 2D, as 2D rendering is performed in SDR.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_intensity** = `0.8`
`🔗<class_Environment_property_glow_intensity>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_intensity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_glow\_intensity**()

The overall brightness multiplier of the glow effect. When using the
Mobile rendering method (which only supports a lower dynamic range up to
`2.0`), this should be increased to `1.5` to compensate.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_levels/1** = `0.0`
`🔗<class_Environment_property_glow_levels/1>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_level**(idx:
    `int<class_int>`, intensity: `float<class_float>`)
-   `float<class_float>` **get\_glow\_level**(idx: `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The intensity of the 1st level of glow. This is the most "local" level
(least blurry).

\*\*Note:\*\* `glow_levels/1<class_Environment_property_glow_levels/1>`
has no effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_levels/2** = `0.0`
`🔗<class_Environment_property_glow_levels/2>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_level**(idx:
    `int<class_int>`, intensity: `float<class_float>`)
-   `float<class_float>` **get\_glow\_level**(idx: `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The intensity of the 2nd level of glow.

\*\*Note:\*\* `glow_levels/2<class_Environment_property_glow_levels/2>`
has no effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_levels/3** = `1.0`
`🔗<class_Environment_property_glow_levels/3>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_level**(idx:
    `int<class_int>`, intensity: `float<class_float>`)
-   `float<class_float>` **get\_glow\_level**(idx: `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The intensity of the 3rd level of glow.

\*\*Note:\*\* `glow_levels/3<class_Environment_property_glow_levels/3>`
has no effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_levels/4** = `0.0`
`🔗<class_Environment_property_glow_levels/4>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_level**(idx:
    `int<class_int>`, intensity: `float<class_float>`)
-   `float<class_float>` **get\_glow\_level**(idx: `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The intensity of the 4th level of glow.

\*\*Note:\*\* `glow_levels/4<class_Environment_property_glow_levels/4>`
has no effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_levels/5** = `1.0`
`🔗<class_Environment_property_glow_levels/5>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_level**(idx:
    `int<class_int>`, intensity: `float<class_float>`)
-   `float<class_float>` **get\_glow\_level**(idx: `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The intensity of the 5th level of glow.

\*\*Note:\*\* `glow_levels/5<class_Environment_property_glow_levels/5>`
has no effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_levels/6** = `0.0`
`🔗<class_Environment_property_glow_levels/6>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_level**(idx:
    `int<class_int>`, intensity: `float<class_float>`)
-   `float<class_float>` **get\_glow\_level**(idx: `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The intensity of the 6th level of glow.

\*\*Note:\*\* `glow_levels/6<class_Environment_property_glow_levels/6>`
has no effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_levels/7** = `0.0`
`🔗<class_Environment_property_glow_levels/7>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_level**(idx:
    `int<class_int>`, intensity: `float<class_float>`)
-   `float<class_float>` **get\_glow\_level**(idx: `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The intensity of the 7th level of glow. This is the most "global" level
(blurriest).

\*\*Note:\*\* `glow_levels/7<class_Environment_property_glow_levels/7>`
has no effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture<class_Texture>` **glow\_map**
`🔗<class_Environment_property_glow_map>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_map**(value:
    `Texture<class_Texture>`)
-   `Texture<class_Texture>` **get\_glow\_map**()

The texture that should be used as a glow map to *multiply* the
resulting glow color according to
`glow_map_strength<class_Environment_property_glow_map_strength>`. This
can be used to create a "lens dirt" effect. The texture's RGB color
channels are used for modulation, but the alpha channel is ignored.

\*\*Note:\*\* The texture will be stretched to fit the screen.
Therefore, it's recommended to use a texture with an aspect ratio that
matches your project's base aspect ratio (typically 16:9).

\*\*Note:\*\* `glow_map<class_Environment_property_glow_map>` has no
effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_map\_strength** = `0.8`
`🔗<class_Environment_property_glow_map_strength>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_map\_strength**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_glow\_map\_strength**()

How strong of an impact the
`glow_map<class_Environment_property_glow_map>` should have on the
overall glow effect. A strength of `0.0` means the glow map has no
effect on the overall glow effect. A strength of `1.0` means the glow
has a full effect on the overall glow effect (and can turn off glow
entirely in specific areas of the screen if the glow map has black
areas).

\*\*Note:\*\*
`glow_map_strength<class_Environment_property_glow_map_strength>` has no
effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_mix** = `0.05`
`🔗<class_Environment_property_glow_mix>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_mix**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_glow\_mix**()

When using the
`GLOW_BLEND_MODE_MIX<class_Environment_constant_GLOW_BLEND_MODE_MIX>`
`glow_blend_mode<class_Environment_property_glow_blend_mode>`, this
controls how much the source image is blended with the glow layer. A
value of `0.0` makes the glow rendering invisible, while a value of
`1.0` is equivalent to
`GLOW_BLEND_MODE_REPLACE<class_Environment_constant_GLOW_BLEND_MODE_REPLACE>`.

\*\*Note:\*\* `glow_mix<class_Environment_property_glow_mix>` has no
effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **glow\_normalized** = `false`
`🔗<class_Environment_property_glow_normalized>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_normalized**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_glow\_normalized**()

If `true`, glow levels will be normalized so that summed together their
intensities equal `1.0`.

\*\*Note:\*\*
`glow_normalized<class_Environment_property_glow_normalized>` has no
effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **glow\_strength** = `1.0`
`🔗<class_Environment_property_glow_strength>`

classref-property-setget

-   `void (No return value.)` **set\_glow\_strength**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_glow\_strength**()

The strength of the glow effect. This applies as the glow is blurred
across the screen and increases the distance and intensity of the blur.
When using the Mobile rendering method, this should be increased to
compensate for the lower dynamic range.

\*\*Note:\*\* `glow_strength<class_Environment_property_glow_strength>`
has no effect when using the Compatibility rendering method, due to this
rendering method using a simpler glow implementation optimized for
low-end devices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ReflectionSource<enum_Environment_ReflectionSource>`
**reflected\_light\_source** = `0`
`🔗<class_Environment_property_reflected_light_source>`

classref-property-setget

-   `void (No return value.)` **set\_reflection\_source**(value:
    `ReflectionSource<enum_Environment_ReflectionSource>`)
-   `ReflectionSource<enum_Environment_ReflectionSource>`
    **get\_reflection\_source**()

The reflected (specular) light source.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sdfgi\_bounce\_feedback** = `0.5`
`🔗<class_Environment_property_sdfgi_bounce_feedback>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_bounce\_feedback**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sdfgi\_bounce\_feedback**()

The energy multiplier applied to light every time it bounces from a
surface when using SDFGI. Values greater than `0.0` will simulate
multiple bounces, resulting in a more realistic appearance. Increasing
`sdfgi_bounce_feedback<class_Environment_property_sdfgi_bounce_feedback>`
generally has no performance impact. See also
`sdfgi_energy<class_Environment_property_sdfgi_energy>`.

\*\*Note:\*\* Values greater than `0.5` can cause infinite feedback
loops and should be avoided in scenes with bright materials.

\*\*Note:\*\* If
`sdfgi_bounce_feedback<class_Environment_property_sdfgi_bounce_feedback>`
is `0.0`, indirect lighting will not be represented in reflections as
light will only bounce one time.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sdfgi\_cascade0\_distance** = `12.8`
`🔗<class_Environment_property_sdfgi_cascade0_distance>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_cascade0\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sdfgi\_cascade0\_distance**()

**Note:** This property is linked to
`sdfgi_min_cell_size<class_Environment_property_sdfgi_min_cell_size>`
and `sdfgi_max_distance<class_Environment_property_sdfgi_max_distance>`.
Changing its value will automatically change those properties as well.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sdfgi\_cascades** = `4`
`🔗<class_Environment_property_sdfgi_cascades>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_cascades**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_sdfgi\_cascades**()

The number of cascades to use for SDFGI (between 1 and 8). A higher
number of cascades allows displaying SDFGI further away while preserving
detail up close, at the cost of performance. When using SDFGI on
small-scale levels,
`sdfgi_cascades<class_Environment_property_sdfgi_cascades>` can often be
decreased between `1` and `4` to improve performance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **sdfgi\_enabled** = `false`
`🔗<class_Environment_property_sdfgi_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_sdfgi\_enabled**()

If `true`, enables signed distance field global illumination for meshes
that have their
`GeometryInstance3D.gi_mode<class_GeometryInstance3D_property_gi_mode>`
set to
`GeometryInstance3D.GI_MODE_STATIC<class_GeometryInstance3D_constant_GI_MODE_STATIC>`.
SDFGI is a real-time global illumination technique that works well with
procedurally generated and user-built levels, including in situations
where geometry is created during gameplay. The signed distance field is
automatically generated around the camera as it moves. Dynamic lights
are supported, but dynamic occluders and emissive surfaces are not.

\*\*Note:\*\* SDFGI is only supported in the Forward+ rendering method,
not Mobile or Compatibility.

\*\*Performance:\*\* SDFGI is relatively demanding on the GPU and is not
suited to low-end hardware such as integrated graphics (consider
`LightmapGI<class_LightmapGI>` instead). To improve SDFGI performance,
enable
`ProjectSettings.rendering/global_illumination/gi/use_half_resolution<class_ProjectSettings_property_rendering/global_illumination/gi/use_half_resolution>`
in the Project Settings.

\*\*Note:\*\* Meshes should have sufficiently thick walls to avoid light
leaks (avoid one-sided walls). For interior levels, enclose your level
geometry in a sufficiently large box and bridge the loops to close the
mesh.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sdfgi\_energy** = `1.0`
`🔗<class_Environment_property_sdfgi_energy>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_energy**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sdfgi\_energy**()

The energy multiplier to use for SDFGI. Higher values will result in
brighter indirect lighting and reflections. See also
`sdfgi_bounce_feedback<class_Environment_property_sdfgi_bounce_feedback>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sdfgi\_max\_distance** = `204.8`
`🔗<class_Environment_property_sdfgi_max_distance>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_max\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sdfgi\_max\_distance**()

The maximum distance at which SDFGI is visible. Beyond this distance,
environment lighting or other sources of GI such as
`ReflectionProbe<class_ReflectionProbe>` will be used as a fallback.

\*\*Note:\*\* This property is linked to
`sdfgi_min_cell_size<class_Environment_property_sdfgi_min_cell_size>`
and
`sdfgi_cascade0_distance<class_Environment_property_sdfgi_cascade0_distance>`.
Changing its value will automatically change those properties as well.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sdfgi\_min\_cell\_size** = `0.2`
`🔗<class_Environment_property_sdfgi_min_cell_size>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_min\_cell\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sdfgi\_min\_cell\_size**()

The cell size to use for the closest SDFGI cascade (in 3D units). Lower
values allow SDFGI to be more precise up close, at the cost of making
SDFGI updates more demanding. This can cause stuttering when the camera
moves fast. Higher values allow SDFGI to cover more ground, while also
reducing the performance impact of SDFGI updates.

\*\*Note:\*\* This property is linked to
`sdfgi_max_distance<class_Environment_property_sdfgi_max_distance>` and
`sdfgi_cascade0_distance<class_Environment_property_sdfgi_cascade0_distance>`.
Changing its value will automatically change those properties as well.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sdfgi\_normal\_bias** = `1.1`
`🔗<class_Environment_property_sdfgi_normal_bias>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_normal\_bias**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sdfgi\_normal\_bias**()

The normal bias to use for SDFGI probes. Increasing this value can
reduce visible streaking artifacts on sloped surfaces, at the cost of
increased light leaking.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sdfgi\_probe\_bias** = `1.1`
`🔗<class_Environment_property_sdfgi_probe_bias>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_probe\_bias**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sdfgi\_probe\_bias**()

The constant bias to use for SDFGI probes. Increasing this value can
reduce visible streaking artifacts on sloped surfaces, at the cost of
increased light leaking.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **sdfgi\_read\_sky\_light** = `true`
`🔗<class_Environment_property_sdfgi_read_sky_light>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_read\_sky\_light**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_sdfgi\_reading\_sky\_light**()

If `true`, SDFGI takes the environment lighting into account. This
should be set to `false` for interior scenes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **sdfgi\_use\_occlusion** = `false`
`🔗<class_Environment_property_sdfgi_use_occlusion>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_use\_occlusion**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_sdfgi\_using\_occlusion**()

If `true`, SDFGI uses an occlusion detection approach to reduce light
leaking. Occlusion may however introduce dark blotches in certain spots,
which may be undesired in mostly outdoor scenes.
`sdfgi_use_occlusion<class_Environment_property_sdfgi_use_occlusion>`
has a performance impact and should only be enabled when needed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SDFGIYScale<enum_Environment_SDFGIYScale>` **sdfgi\_y\_scale** = `1`
`🔗<class_Environment_property_sdfgi_y_scale>`

classref-property-setget

-   `void (No return value.)` **set\_sdfgi\_y\_scale**(value:
    `SDFGIYScale<enum_Environment_SDFGIYScale>`)
-   `SDFGIYScale<enum_Environment_SDFGIYScale>`
    **get\_sdfgi\_y\_scale**()

The Y scale to use for SDFGI cells. Lower values will result in SDFGI
cells being packed together more closely on the Y axis. This is used to
balance between quality and covering a lot of vertical ground.
`sdfgi_y_scale<class_Environment_property_sdfgi_y_scale>` should be set
depending on how vertical your scene is (and how fast your camera may
move on the Y axis).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Sky<class_Sky>` **sky** `🔗<class_Environment_property_sky>`

classref-property-setget

-   `void (No return value.)` **set\_sky**(value: `Sky<class_Sky>`)
-   `Sky<class_Sky>` **get\_sky**()

The `Sky<class_Sky>` resource used for this **Environment**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sky\_custom\_fov** = `0.0`
`🔗<class_Environment_property_sky_custom_fov>`

classref-property-setget

-   `void (No return value.)` **set\_sky\_custom\_fov**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sky\_custom\_fov**()

If set to a value greater than `0.0`, overrides the field of view to use
for sky rendering. If set to `0.0`, the same FOV as the current
`Camera3D<class_Camera3D>` is used for sky rendering.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **sky\_rotation** = `Vector3(0, 0, 0)`
`🔗<class_Environment_property_sky_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_sky\_rotation**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_sky\_rotation**()

The rotation to use for sky rendering.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssao\_ao\_channel\_affect** = `0.0`
`🔗<class_Environment_property_ssao_ao_channel_affect>`

classref-property-setget

-   `void (No return value.)` **set\_ssao\_ao\_channel\_affect**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssao\_ao\_channel\_affect**()

The screen-space ambient occlusion intensity on materials that have an
AO texture defined. Values higher than `0` will make the SSAO effect
visible in areas darkened by AO textures.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssao\_detail** = `0.5`
`🔗<class_Environment_property_ssao_detail>`

classref-property-setget

-   `void (No return value.)` **set\_ssao\_detail**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssao\_detail**()

Sets the strength of the additional level of detail for the screen-space
ambient occlusion effect. A high value makes the detail pass more
prominent, but it may contribute to aliasing in your final image.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ssao\_enabled** = `false`
`🔗<class_Environment_property_ssao_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_ssao\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_ssao\_enabled**()

If `true`, the screen-space ambient occlusion effect is enabled. This
darkens objects' corners and cavities to simulate ambient light not
reaching the entire object as in real life. This works well for small,
dynamic objects, but baked lighting or ambient occlusion textures will
do a better job at displaying ambient occlusion on large static objects.
Godot uses a form of SSAO called Adaptive Screen Space Ambient Occlusion
which is itself a form of Horizon Based Ambient Occlusion.

\*\*Note:\*\* SSAO is only supported in the Forward+ rendering method,
not Mobile or Compatibility.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssao\_horizon** = `0.06`
`🔗<class_Environment_property_ssao_horizon>`

classref-property-setget

-   `void (No return value.)` **set\_ssao\_horizon**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssao\_horizon**()

The threshold for considering whether a given point on a surface is
occluded or not represented as an angle from the horizon mapped into the
`0.0-1.0` range. A value of `1.0` results in no occlusion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssao\_intensity** = `2.0`
`🔗<class_Environment_property_ssao_intensity>`

classref-property-setget

-   `void (No return value.)` **set\_ssao\_intensity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssao\_intensity**()

The primary screen-space ambient occlusion intensity. Acts as a
multiplier for the screen-space ambient occlusion effect. A higher value
results in darker occlusion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssao\_light\_affect** = `0.0`
`🔗<class_Environment_property_ssao_light_affect>`

classref-property-setget

-   `void (No return value.)`
    **set\_ssao\_direct\_light\_affect**(value: `float<class_float>`)
-   `float<class_float>` **get\_ssao\_direct\_light\_affect**()

The screen-space ambient occlusion intensity in direct light. In real
life, ambient occlusion only applies to indirect light, which means its
effects can't be seen in direct light. Values higher than `0` will make
the SSAO effect visible in direct light.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssao\_power** = `1.5`
`🔗<class_Environment_property_ssao_power>`

classref-property-setget

-   `void (No return value.)` **set\_ssao\_power**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssao\_power**()

The distribution of occlusion. A higher value results in darker
occlusion, similar to
`ssao_intensity<class_Environment_property_ssao_intensity>`, but with a
sharper falloff.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssao\_radius** = `1.0`
`🔗<class_Environment_property_ssao_radius>`

classref-property-setget

-   `void (No return value.)` **set\_ssao\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssao\_radius**()

The distance at which objects can occlude each other when calculating
screen-space ambient occlusion. Higher values will result in occlusion
over a greater distance at the cost of performance and quality.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssao\_sharpness** = `0.98`
`🔗<class_Environment_property_ssao_sharpness>`

classref-property-setget

-   `void (No return value.)` **set\_ssao\_sharpness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssao\_sharpness**()

The amount that the screen-space ambient occlusion effect is allowed to
blur over the edges of objects. Setting too high will result in aliasing
around the edges of objects. Setting too low will make object edges
appear blurry.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ssil\_enabled** = `false`
`🔗<class_Environment_property_ssil_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_ssil\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_ssil\_enabled**()

If `true`, the screen-space indirect lighting effect is enabled. Screen
space indirect lighting is a form of indirect lighting that allows
diffuse light to bounce between nearby objects. Screen-space indirect
lighting works very similarly to screen-space ambient occlusion, in that
it only affects a limited range. It is intended to be used along with a
form of proper global illumination like SDFGI or
`VoxelGI<class_VoxelGI>`. Screen-space indirect lighting is not affected
by individual light's
`Light3D.light_indirect_energy<class_Light3D_property_light_indirect_energy>`.

\*\*Note:\*\* SSIL is only supported in the Forward+ rendering method,
not Mobile or Compatibility.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssil\_intensity** = `1.0`
`🔗<class_Environment_property_ssil_intensity>`

classref-property-setget

-   `void (No return value.)` **set\_ssil\_intensity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssil\_intensity**()

The brightness multiplier for the screen-space indirect lighting effect.
A higher value will result in brighter light.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssil\_normal\_rejection** = `1.0`
`🔗<class_Environment_property_ssil_normal_rejection>`

classref-property-setget

-   `void (No return value.)` **set\_ssil\_normal\_rejection**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssil\_normal\_rejection**()

Amount of normal rejection used when calculating screen-space indirect
lighting. Normal rejection uses the normal of a given sample point to
reject samples that are facing away from the current pixel. Normal
rejection is necessary to avoid light leaking when only one side of an
object is illuminated. However, normal rejection can be disabled if
light leaking is desirable, such as when the scene mostly contains
emissive objects that emit light from faces that cannot be seen from the
camera.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssil\_radius** = `5.0`
`🔗<class_Environment_property_ssil_radius>`

classref-property-setget

-   `void (No return value.)` **set\_ssil\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssil\_radius**()

The distance that bounced lighting can travel when using the screen
space indirect lighting effect. A larger value will result in light
bouncing further in a scene, but may result in under-sampling artifacts
which look like long spikes surrounding light sources.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssil\_sharpness** = `0.98`
`🔗<class_Environment_property_ssil_sharpness>`

classref-property-setget

-   `void (No return value.)` **set\_ssil\_sharpness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssil\_sharpness**()

The amount that the screen-space indirect lighting effect is allowed to
blur over the edges of objects. Setting too high will result in aliasing
around the edges of objects. Setting too low will make object edges
appear blurry.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssr\_depth\_tolerance** = `0.2`
`🔗<class_Environment_property_ssr_depth_tolerance>`

classref-property-setget

-   `void (No return value.)` **set\_ssr\_depth\_tolerance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssr\_depth\_tolerance**()

The depth tolerance for screen-space reflections.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ssr\_enabled** = `false`
`🔗<class_Environment_property_ssr_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_ssr\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_ssr\_enabled**()

If `true`, screen-space reflections are enabled. Screen-space
reflections are more accurate than reflections from
`VoxelGI<class_VoxelGI>`s or `ReflectionProbe<class_ReflectionProbe>`s,
but are slower and can't reflect surfaces occluded by others.

\*\*Note:\*\* SSR is only supported in the Forward+ rendering method,
not Mobile or Compatibility.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssr\_fade\_in** = `0.15`
`🔗<class_Environment_property_ssr_fade_in>`

classref-property-setget

-   `void (No return value.)` **set\_ssr\_fade\_in**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssr\_fade\_in**()

The fade-in distance for screen-space reflections. Affects the area from
the reflected material to the screen-space reflection. Only positive
values are valid (negative values will be clamped to `0.0`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ssr\_fade\_out** = `2.0`
`🔗<class_Environment_property_ssr_fade_out>`

classref-property-setget

-   `void (No return value.)` **set\_ssr\_fade\_out**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ssr\_fade\_out**()

The fade-out distance for screen-space reflections. Affects the area
from the screen-space reflection to the "global" reflection. Only
positive values are valid (negative values will be clamped to `0.0`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **ssr\_max\_steps** = `64`
`🔗<class_Environment_property_ssr_max_steps>`

classref-property-setget

-   `void (No return value.)` **set\_ssr\_max\_steps**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_ssr\_max\_steps**()

The maximum number of steps for screen-space reflections. Higher values
are slower.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **tonemap\_exposure** = `1.0`
`🔗<class_Environment_property_tonemap_exposure>`

classref-property-setget

-   `void (No return value.)` **set\_tonemap\_exposure**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_tonemap\_exposure**()

The default exposure used for tonemapping. Higher values result in a
brighter image. See also
`tonemap_white<class_Environment_property_tonemap_white>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ToneMapper<enum_Environment_ToneMapper>` **tonemap\_mode** = `0`
`🔗<class_Environment_property_tonemap_mode>`

classref-property-setget

-   `void (No return value.)` **set\_tonemapper**(value:
    `ToneMapper<enum_Environment_ToneMapper>`)
-   `ToneMapper<enum_Environment_ToneMapper>` **get\_tonemapper**()

The tonemapping mode to use. Tonemapping is the process that "converts"
HDR values to be suitable for rendering on an LDR display. (Godot
doesn't support rendering on HDR displays yet.)

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **tonemap\_white** = `1.0`
`🔗<class_Environment_property_tonemap_white>`

classref-property-setget

-   `void (No return value.)` **set\_tonemap\_white**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_tonemap\_white**()

The white reference value for tonemapping (also called "whitepoint").
Higher values can make highlights look less blown out, and will also
slightly darken the whole scene as a result. Only effective if the
`tonemap_mode<class_Environment_property_tonemap_mode>` isn't set to
`TONE_MAPPER_LINEAR<class_Environment_constant_TONE_MAPPER_LINEAR>`. See
also `tonemap_exposure<class_Environment_property_tonemap_exposure>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **volumetric\_fog\_albedo** = `Color(1, 1, 1, 1)`
`🔗<class_Environment_property_volumetric_fog_albedo>`

classref-property-setget

-   `void (No return value.)` **set\_volumetric\_fog\_albedo**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_volumetric\_fog\_albedo**()

The `Color<class_Color>` of the volumetric fog when interacting with
lights. Mist and fog have an albedo close to `Color(1, 1, 1, 1)` while
smoke has a darker albedo.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volumetric\_fog\_ambient\_inject** = `0.0`
`🔗<class_Environment_property_volumetric_fog_ambient_inject>`

classref-property-setget

-   `void (No return value.)`
    **set\_volumetric\_fog\_ambient\_inject**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_volumetric\_fog\_ambient\_inject**()

Scales the strength of ambient light used in the volumetric fog. A value
of `0.0` means that ambient light will not impact the volumetric fog.
`volumetric_fog_ambient_inject<class_Environment_property_volumetric_fog_ambient_inject>`
has a small performance cost when set above `0.0`.

\*\*Note:\*\* This has no visible effect if
`volumetric_fog_density<class_Environment_property_volumetric_fog_density>`
is `0.0` or if
`volumetric_fog_albedo<class_Environment_property_volumetric_fog_albedo>`
is a fully black color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volumetric\_fog\_anisotropy** = `0.2`
`🔗<class_Environment_property_volumetric_fog_anisotropy>`

classref-property-setget

-   `void (No return value.)`
    **set\_volumetric\_fog\_anisotropy**(value: `float<class_float>`)
-   `float<class_float>` **get\_volumetric\_fog\_anisotropy**()

The direction of scattered light as it goes through the volumetric fog.
A value close to `1.0` means almost all light is scattered forward. A
value close to `0.0` means light is scattered equally in all directions.
A value close to `-1.0` means light is scattered mostly backward. Fog
and mist scatter light slightly forward, while smoke scatters light
equally in all directions.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volumetric\_fog\_density** = `0.05`
`🔗<class_Environment_property_volumetric_fog_density>`

classref-property-setget

-   `void (No return value.)` **set\_volumetric\_fog\_density**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_volumetric\_fog\_density**()

The base *exponential* density of the volumetric fog. Set this to the
lowest density you want to have globally. `FogVolume<class_FogVolume>`s
can be used to add to or subtract from this density in specific areas.
Fog rendering is exponential as in real life.

A value of `0.0` disables global volumetric fog while allowing
`FogVolume<class_FogVolume>`s to display volumetric fog in specific
areas.

To make volumetric fog work as a volumetric *lighting* solution, set
`volumetric_fog_density<class_Environment_property_volumetric_fog_density>`
to the lowest non-zero value (`0.0001`) then increase lights'
`Light3D.light_volumetric_fog_energy<class_Light3D_property_light_volumetric_fog_energy>`
to values between `10000` and `100000` to compensate for the very low
density.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volumetric\_fog\_detail\_spread** = `2.0`
`🔗<class_Environment_property_volumetric_fog_detail_spread>`

classref-property-setget

-   `void (No return value.)`
    **set\_volumetric\_fog\_detail\_spread**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_volumetric\_fog\_detail\_spread**()

The distribution of size down the length of the froxel buffer. A higher
value compresses the froxels closer to the camera and places more detail
closer to the camera.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **volumetric\_fog\_emission** = `Color(0, 0, 0, 1)`
`🔗<class_Environment_property_volumetric_fog_emission>`

classref-property-setget

-   `void (No return value.)` **set\_volumetric\_fog\_emission**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_volumetric\_fog\_emission**()

The emitted light from the volumetric fog. Even with emission,
volumetric fog will not cast light onto other surfaces. Emission is
useful to establish an ambient color. As the volumetric fog effect uses
single-scattering only, fog tends to need a little bit of emission to
soften the harsh shadows.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volumetric\_fog\_emission\_energy** = `1.0`
`🔗<class_Environment_property_volumetric_fog_emission_energy>`

classref-property-setget

-   `void (No return value.)`
    **set\_volumetric\_fog\_emission\_energy**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_volumetric\_fog\_emission\_energy**()

The brightness of the emitted light from the volumetric fog.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **volumetric\_fog\_enabled** = `false`
`🔗<class_Environment_property_volumetric_fog_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_volumetric\_fog\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_volumetric\_fog\_enabled**()

Enables the volumetric fog effect. Volumetric fog uses a screen-aligned
froxel buffer to calculate accurate volumetric scattering in the short
to medium range. Volumetric fog interacts with
`FogVolume<class_FogVolume>`s and lights to calculate localized and
global fog. Volumetric fog uses a PBR single-scattering model based on
extinction, scattering, and emission which it exposes to users as
density, albedo, and emission.

\*\*Note:\*\* Volumetric fog is only supported in the Forward+ rendering
method, not Mobile or Compatibility.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volumetric\_fog\_gi\_inject** = `1.0`
`🔗<class_Environment_property_volumetric_fog_gi_inject>`

classref-property-setget

-   `void (No return value.)`
    **set\_volumetric\_fog\_gi\_inject**(value: `float<class_float>`)
-   `float<class_float>` **get\_volumetric\_fog\_gi\_inject**()

Scales the strength of Global Illumination used in the volumetric fog's
albedo color. A value of `0.0` means that Global Illumination will not
impact the volumetric fog.
`volumetric_fog_gi_inject<class_Environment_property_volumetric_fog_gi_inject>`
has a small performance cost when set above `0.0`.

\*\*Note:\*\* This has no visible effect if
`volumetric_fog_density<class_Environment_property_volumetric_fog_density>`
is `0.0` or if
`volumetric_fog_albedo<class_Environment_property_volumetric_fog_albedo>`
is a fully black color.

\*\*Note:\*\* Only `VoxelGI<class_VoxelGI>` and SDFGI
(`sdfgi_enabled<class_Environment_property_sdfgi_enabled>`) are taken
into account when using
`volumetric_fog_gi_inject<class_Environment_property_volumetric_fog_gi_inject>`.
Global illumination from `LightmapGI<class_LightmapGI>`,
`ReflectionProbe<class_ReflectionProbe>` and SSIL (see
`ssil_enabled<class_Environment_property_ssil_enabled>`) will be ignored
by volumetric fog.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volumetric\_fog\_length** = `64.0`
`🔗<class_Environment_property_volumetric_fog_length>`

classref-property-setget

-   `void (No return value.)` **set\_volumetric\_fog\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_volumetric\_fog\_length**()

The distance over which the volumetric fog is computed. Increase to
compute fog over a greater range, decrease to add more detail when a
long range is not needed. For best quality fog, keep this as low as
possible. See also
`ProjectSettings.rendering/environment/volumetric_fog/volume_depth<class_ProjectSettings_property_rendering/environment/volumetric_fog/volume_depth>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volumetric\_fog\_sky\_affect** = `1.0`
`🔗<class_Environment_property_volumetric_fog_sky_affect>`

classref-property-setget

-   `void (No return value.)`
    **set\_volumetric\_fog\_sky\_affect**(value: `float<class_float>`)
-   `float<class_float>` **get\_volumetric\_fog\_sky\_affect**()

The factor to use when affecting the sky with volumetric fog. `1.0`
means that volumetric fog can fully obscure the sky. Lower values reduce
the impact of volumetric fog on sky rendering, with `0.0` not affecting
sky rendering at all.

\*\*Note:\*\*
`volumetric_fog_sky_affect<class_Environment_property_volumetric_fog_sky_affect>`
also affects `FogVolume<class_FogVolume>`s, even if
`volumetric_fog_density<class_Environment_property_volumetric_fog_density>`
is `0.0`. If you notice `FogVolume<class_FogVolume>`s are disappearing
when looking towards the sky, set
`volumetric_fog_sky_affect<class_Environment_property_volumetric_fog_sky_affect>`
to `1.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volumetric\_fog\_temporal\_reprojection\_amount**
= `0.9`
`🔗<class_Environment_property_volumetric_fog_temporal_reprojection_amount>`

classref-property-setget

-   `void (No return value.)`
    **set\_volumetric\_fog\_temporal\_reprojection\_amount**(value:
    `float<class_float>`)
-   `float<class_float>`
    **get\_volumetric\_fog\_temporal\_reprojection\_amount**()

The amount by which to blend the last frame with the current frame. A
higher number results in smoother volumetric fog, but makes "ghosting"
much worse. A lower value reduces ghosting but can result in the
per-frame temporal jitter becoming visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **volumetric\_fog\_temporal\_reprojection\_enabled**
= `true`
`🔗<class_Environment_property_volumetric_fog_temporal_reprojection_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_volumetric\_fog\_temporal\_reprojection\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>`
    **is\_volumetric\_fog\_temporal\_reprojection\_enabled**()

Enables temporal reprojection in the volumetric fog. Temporal
reprojection blends the current frame's volumetric fog with the last
frame's volumetric fog to smooth out jagged edges. The performance cost
is minimal; however, it leads to moving `FogVolume<class_FogVolume>`s
and `Light3D<class_Light3D>`s "ghosting" and leaving a trail behind
them. When temporal reprojection is enabled, try to avoid moving
`FogVolume<class_FogVolume>`s or `Light3D<class_Light3D>`s too fast.
Short-lived dynamic lighting effects should have
`Light3D.light_volumetric_fog_energy<class_Light3D_property_light_volumetric_fog_energy>`
set to `0.0` to avoid ghosting.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_glow\_level**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Environment_method_get_glow_level>`

Returns the intensity of the glow level `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_glow\_level**(idx: `int<class_int>`,
intensity: `float<class_float>`)
`🔗<class_Environment_method_set_glow_level>`

Sets the intensity of the glow level `idx`. A value above `0.0` enables
the level. Each level relies on the previous level. This means that
enabling higher glow levels will slow down the glow effect rendering,
even if previous levels aren't enabled.
