github\_url  
hide

# Light2D

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `DirectionalLight2D<class_DirectionalLight2D>`,
`PointLight2D<class_PointLight2D>`

Casts light in a 2D environment.

classref-introduction-group

## Description

Casts light in a 2D environment. A light is defined as a color, an
energy value, a mode (see constants), and various other parameters
(range and shadows-related).

classref-introduction-group

## Tutorials

-   `2D lights and shadows <../tutorials/2d/2d_lights_and_shadows>`

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

enum **ShadowFilter**: `🔗<enum_Light2D_ShadowFilter>`

classref-enumeration-constant

`ShadowFilter<enum_Light2D_ShadowFilter>` **SHADOW\_FILTER\_NONE** = `0`

No filter applies to the shadow map. This provides hard shadow edges and
is the fastest to render. See
`shadow_filter<class_Light2D_property_shadow_filter>`.

classref-enumeration-constant

`ShadowFilter<enum_Light2D_ShadowFilter>` **SHADOW\_FILTER\_PCF5** = `1`

Percentage closer filtering (5 samples) applies to the shadow map. This
is slower compared to hard shadow rendering. See
`shadow_filter<class_Light2D_property_shadow_filter>`.

classref-enumeration-constant

`ShadowFilter<enum_Light2D_ShadowFilter>` **SHADOW\_FILTER\_PCF13** =
`2`

Percentage closer filtering (13 samples) applies to the shadow map. This
is the slowest shadow filtering mode, and should be used sparingly. See
`shadow_filter<class_Light2D_property_shadow_filter>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **BlendMode**: `🔗<enum_Light2D_BlendMode>`

classref-enumeration-constant

`BlendMode<enum_Light2D_BlendMode>` **BLEND\_MODE\_ADD** = `0`

Adds the value of pixels corresponding to the Light2D to the values of
pixels under it. This is the common behavior of a light.

classref-enumeration-constant

`BlendMode<enum_Light2D_BlendMode>` **BLEND\_MODE\_SUB** = `1`

Subtracts the value of pixels corresponding to the Light2D to the values
of pixels under it, resulting in inversed light effect.

classref-enumeration-constant

`BlendMode<enum_Light2D_BlendMode>` **BLEND\_MODE\_MIX** = `2`

Mix the value of pixels corresponding to the Light2D to the values of
pixels under it by linear interpolation.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`BlendMode<enum_Light2D_BlendMode>` **blend\_mode** = `0`
`🔗<class_Light2D_property_blend_mode>`

classref-property-setget

-   `void (No return value.)` **set\_blend\_mode**(value:
    `BlendMode<enum_Light2D_BlendMode>`)
-   `BlendMode<enum_Light2D_BlendMode>` **get\_blend\_mode**()

The Light2D's blend mode. See `BlendMode<enum_Light2D_BlendMode>`
constants for values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **color** = `Color(1, 1, 1, 1)`
`🔗<class_Light2D_property_color>`

classref-property-setget

-   `void (No return value.)` **set\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_color**()

The Light2D's `Color<class_Color>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editor\_only** = `false`
`🔗<class_Light2D_property_editor_only>`

classref-property-setget

-   `void (No return value.)` **set\_editor\_only**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_editor\_only**()

If `true`, Light2D will only appear when editing the scene.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enabled** = `true`
`🔗<class_Light2D_property_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_enabled**()

If `true`, Light2D will emit light.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **energy** = `1.0`
`🔗<class_Light2D_property_energy>`

classref-property-setget

-   `void (No return value.)` **set\_energy**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_energy**()

The Light2D's energy value. The larger the value, the stronger the
light.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **range\_item\_cull\_mask** = `1`
`🔗<class_Light2D_property_range_item_cull_mask>`

classref-property-setget

-   `void (No return value.)` **set\_item\_cull\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_item\_cull\_mask**()

The layer mask. Only objects with a matching
`CanvasItem.light_mask<class_CanvasItem_property_light_mask>` will be
affected by the Light2D. See also
`shadow_item_cull_mask<class_Light2D_property_shadow_item_cull_mask>`,
which affects which objects can cast shadows.

\*\*Note:\*\*
`range_item_cull_mask<class_Light2D_property_range_item_cull_mask>` is
ignored by `DirectionalLight2D<class_DirectionalLight2D>`, which will
always light a 2D node regardless of the 2D node's
`CanvasItem.light_mask<class_CanvasItem_property_light_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **range\_layer\_max** = `0`
`🔗<class_Light2D_property_range_layer_max>`

classref-property-setget

-   `void (No return value.)` **set\_layer\_range\_max**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_layer\_range\_max**()

Maximum layer value of objects that are affected by the Light2D.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **range\_layer\_min** = `0`
`🔗<class_Light2D_property_range_layer_min>`

classref-property-setget

-   `void (No return value.)` **set\_layer\_range\_min**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_layer\_range\_min**()

Minimum layer value of objects that are affected by the Light2D.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **range\_z\_max** = `1024`
`🔗<class_Light2D_property_range_z_max>`

classref-property-setget

-   `void (No return value.)` **set\_z\_range\_max**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_z\_range\_max**()

Maximum `z` value of objects that are affected by the Light2D.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **range\_z\_min** = `-1024`
`🔗<class_Light2D_property_range_z_min>`

classref-property-setget

-   `void (No return value.)` **set\_z\_range\_min**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_z\_range\_min**()

Minimum `z` value of objects that are affected by the Light2D.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **shadow\_color** = `Color(0, 0, 0, 0)`
`🔗<class_Light2D_property_shadow_color>`

classref-property-setget

-   `void (No return value.)` **set\_shadow\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_shadow\_color**()

`Color<class_Color>` of shadows cast by the Light2D.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shadow\_enabled** = `false`
`🔗<class_Light2D_property_shadow_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_shadow\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_shadow\_enabled**()

If `true`, the Light2D will cast shadows.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ShadowFilter<enum_Light2D_ShadowFilter>` **shadow\_filter** = `0`
`🔗<class_Light2D_property_shadow_filter>`

classref-property-setget

-   `void (No return value.)` **set\_shadow\_filter**(value:
    `ShadowFilter<enum_Light2D_ShadowFilter>`)
-   `ShadowFilter<enum_Light2D_ShadowFilter>` **get\_shadow\_filter**()

Shadow filter type. See `ShadowFilter<enum_Light2D_ShadowFilter>` for
possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **shadow\_filter\_smooth** = `0.0`
`🔗<class_Light2D_property_shadow_filter_smooth>`

classref-property-setget

-   `void (No return value.)` **set\_shadow\_smooth**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_shadow\_smooth**()

Smoothing value for shadows. Higher values will result in softer
shadows, at the cost of visible streaks that can appear in shadow
rendering.
`shadow_filter_smooth<class_Light2D_property_shadow_filter_smooth>` only
has an effect if `shadow_filter<class_Light2D_property_shadow_filter>`
is `SHADOW_FILTER_PCF5<class_Light2D_constant_SHADOW_FILTER_PCF5>` or
`SHADOW_FILTER_PCF13<class_Light2D_constant_SHADOW_FILTER_PCF13>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **shadow\_item\_cull\_mask** = `1`
`🔗<class_Light2D_property_shadow_item_cull_mask>`

classref-property-setget

-   `void (No return value.)` **set\_item\_shadow\_cull\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_item\_shadow\_cull\_mask**()

The shadow mask. Used with `LightOccluder2D<class_LightOccluder2D>` to
cast shadows. Only occluders with a matching
`CanvasItem.light_mask<class_CanvasItem_property_light_mask>` will cast
shadows. See also
`range_item_cull_mask<class_Light2D_property_range_item_cull_mask>`,
which affects which objects can *receive* the light.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_height**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Light2D_method_get_height>`

Returns the light's height, which is used in 2D normal mapping. See
`PointLight2D.height<class_PointLight2D_property_height>` and
`DirectionalLight2D.height<class_DirectionalLight2D_property_height>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_height**(height: `float<class_float>`)
`🔗<class_Light2D_method_set_height>`

Sets the light's height, which is used in 2D normal mapping. See
`PointLight2D.height<class_PointLight2D_property_height>` and
`DirectionalLight2D.height<class_DirectionalLight2D_property_height>`.
