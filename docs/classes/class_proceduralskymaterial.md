github\_url  
hide

# ProceduralSkyMaterial

**Inherits:** `Material<class_Material>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A material that defines a simple sky for a `Sky<class_Sky>` resource.

classref-introduction-group

## Description

**ProceduralSkyMaterial** provides a way to create an effective
background quickly by defining procedural parameters for the sun, the
sky and the ground. The sky and ground are defined by a main color, a
color at the horizon, and an easing curve to interpolate between them.
Suns are described by a position in the sky, a color, and a max angle
from the sun at which the easing curve ends. The max angle therefore
defines the size of the sun in the sky.

\*\*ProceduralSkyMaterial\*\* supports up to 4 suns, using the color,
and energy, direction, and angular distance of the first four
`DirectionalLight3D<class_DirectionalLight3D>` nodes in the scene. This
means that the suns are defined individually by the properties of their
corresponding `DirectionalLight3D<class_DirectionalLight3D>`s and
globally by
`sun_angle_max<class_ProceduralSkyMaterial_property_sun_angle_max>` and
`sun_curve<class_ProceduralSkyMaterial_property_sun_curve>`.

\*\*ProceduralSkyMaterial\*\* uses a lightweight shader to draw the sky
and is therefore suited for real-time updates. This makes it a great
option for a sky that is simple and computationally cheap, but
unrealistic. If you need a more realistic procedural option, use
`PhysicalSkyMaterial<class_PhysicalSkyMaterial>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **energy\_multiplier** = `1.0`
`🔗<class_ProceduralSkyMaterial_property_energy_multiplier>`

classref-property-setget

-   `void (No return value.)` **set\_energy\_multiplier**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_energy\_multiplier**()

The sky's overall brightness multiplier. Higher values result in a
brighter sky.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **ground\_bottom\_color** =
`Color(0.2, 0.169, 0.133, 1)`
`🔗<class_ProceduralSkyMaterial_property_ground_bottom_color>`

classref-property-setget

-   `void (No return value.)` **set\_ground\_bottom\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_ground\_bottom\_color**()

Color of the ground at the bottom. Blends with
`ground_horizon_color<class_ProceduralSkyMaterial_property_ground_horizon_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ground\_curve** = `0.02`
`🔗<class_ProceduralSkyMaterial_property_ground_curve>`

classref-property-setget

-   `void (No return value.)` **set\_ground\_curve**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ground\_curve**()

How quickly the
`ground_horizon_color<class_ProceduralSkyMaterial_property_ground_horizon_color>`
fades into the
`ground_bottom_color<class_ProceduralSkyMaterial_property_ground_bottom_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ground\_energy\_multiplier** = `1.0`
`🔗<class_ProceduralSkyMaterial_property_ground_energy_multiplier>`

classref-property-setget

-   `void (No return value.)` **set\_ground\_energy\_multiplier**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ground\_energy\_multiplier**()

Multiplier for ground color. A higher value will make the ground
brighter.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **ground\_horizon\_color** =
`Color(0.6463, 0.6558, 0.6708, 1)`
`🔗<class_ProceduralSkyMaterial_property_ground_horizon_color>`

classref-property-setget

-   `void (No return value.)` **set\_ground\_horizon\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_ground\_horizon\_color**()

Color of the ground at the horizon. Blends with
`ground_bottom_color<class_ProceduralSkyMaterial_property_ground_bottom_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **sky\_cover**
`🔗<class_ProceduralSkyMaterial_property_sky_cover>`

classref-property-setget

-   `void (No return value.)` **set\_sky\_cover**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_sky\_cover**()

The sky cover texture to use. This texture must use an equirectangular
projection (similar to
`PanoramaSkyMaterial<class_PanoramaSkyMaterial>`). The texture's colors
will be *added* to the existing sky color, and will be multiplied by
`sky_energy_multiplier<class_ProceduralSkyMaterial_property_sky_energy_multiplier>`
and
`sky_cover_modulate<class_ProceduralSkyMaterial_property_sky_cover_modulate>`.
This is mainly suited to displaying stars at night, but it can also be
used to display clouds at day or night (with a non-physically-accurate
look).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **sky\_cover\_modulate** = `Color(1, 1, 1, 1)`
`🔗<class_ProceduralSkyMaterial_property_sky_cover_modulate>`

classref-property-setget

-   `void (No return value.)` **set\_sky\_cover\_modulate**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_sky\_cover\_modulate**()

The tint to apply to the
`sky_cover<class_ProceduralSkyMaterial_property_sky_cover>` texture.
This can be used to change the sky cover's colors or opacity
independently of the sky energy, which is useful for day/night or
weather transitions. Only effective if a texture is defined in
`sky_cover<class_ProceduralSkyMaterial_property_sky_cover>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sky\_curve** = `0.15`
`🔗<class_ProceduralSkyMaterial_property_sky_curve>`

classref-property-setget

-   `void (No return value.)` **set\_sky\_curve**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sky\_curve**()

How quickly the
`sky_horizon_color<class_ProceduralSkyMaterial_property_sky_horizon_color>`
fades into the
`sky_top_color<class_ProceduralSkyMaterial_property_sky_top_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sky\_energy\_multiplier** = `1.0`
`🔗<class_ProceduralSkyMaterial_property_sky_energy_multiplier>`

classref-property-setget

-   `void (No return value.)` **set\_sky\_energy\_multiplier**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sky\_energy\_multiplier**()

Multiplier for sky color. A higher value will make the sky brighter.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **sky\_horizon\_color** =
`Color(0.6463, 0.6558, 0.6708, 1)`
`🔗<class_ProceduralSkyMaterial_property_sky_horizon_color>`

classref-property-setget

-   `void (No return value.)` **set\_sky\_horizon\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_sky\_horizon\_color**()

Color of the sky at the horizon. Blends with
`sky_top_color<class_ProceduralSkyMaterial_property_sky_top_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **sky\_top\_color** =
`Color(0.385, 0.454, 0.55, 1)`
`🔗<class_ProceduralSkyMaterial_property_sky_top_color>`

classref-property-setget

-   `void (No return value.)` **set\_sky\_top\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_sky\_top\_color**()

Color of the sky at the top. Blends with
`sky_horizon_color<class_ProceduralSkyMaterial_property_sky_horizon_color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sun\_angle\_max** = `30.0`
`🔗<class_ProceduralSkyMaterial_property_sun_angle_max>`

classref-property-setget

-   `void (No return value.)` **set\_sun\_angle\_max**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sun\_angle\_max**()

Distance from center of sun where it fades out completely.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sun\_curve** = `0.15`
`🔗<class_ProceduralSkyMaterial_property_sun_curve>`

classref-property-setget

-   `void (No return value.)` **set\_sun\_curve**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sun\_curve**()

How quickly the sun fades away between the edge of the sun disk and
`sun_angle_max<class_ProceduralSkyMaterial_property_sun_angle_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_debanding** = `true`
`🔗<class_ProceduralSkyMaterial_property_use_debanding>`

classref-property-setget

-   `void (No return value.)` **set\_use\_debanding**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_use\_debanding**()

If `true`, enables debanding. Debanding adds a small amount of noise
which helps reduce banding that appears from the smooth changes in color
in the sky.
