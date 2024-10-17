github\_url  
hide

# CameraAttributes

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:**
`CameraAttributesPhysical<class_CameraAttributesPhysical>`,
`CameraAttributesPractical<class_CameraAttributesPractical>`

Parent class for camera settings.

classref-introduction-group

## Description

Controls camera-specific attributes such as depth of field and exposure
override.

When used in a `WorldEnvironment<class_WorldEnvironment>` it provides
default settings for exposure, auto-exposure, and depth of field that
will be used by all cameras without their own **CameraAttributes**,
including the editor camera. When used in a `Camera3D<class_Camera3D>`
it will override any **CameraAttributes** set in the
`WorldEnvironment<class_WorldEnvironment>`. When used in
`VoxelGI<class_VoxelGI>` or `LightmapGI<class_LightmapGI>`, only the
exposure settings will be used.

See also `Environment<class_Environment>` for general 3D environment
settings.

This is a pure virtual class that is inherited by
`CameraAttributesPhysical<class_CameraAttributesPhysical>` and
`CameraAttributesPractical<class_CameraAttributesPractical>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **auto\_exposure\_enabled** = `false`
`🔗<class_CameraAttributes_property_auto_exposure_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_exposure\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_auto\_exposure\_enabled**()

If `true`, enables the tonemapping auto exposure mode of the scene
renderer. If `true`, the renderer will automatically determine the
exposure setting to adapt to the scene's illumination and the observed
light.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **auto\_exposure\_scale** = `0.4`
`🔗<class_CameraAttributes_property_auto_exposure_scale>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_exposure\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_auto\_exposure\_scale**()

The scale of the auto exposure effect. Affects the intensity of auto
exposure.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **auto\_exposure\_speed** = `0.5`
`🔗<class_CameraAttributes_property_auto_exposure_speed>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_exposure\_speed**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_auto\_exposure\_speed**()

The speed of the auto exposure effect. Affects the time needed for the
camera to perform auto exposure.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **exposure\_multiplier** = `1.0`
`🔗<class_CameraAttributes_property_exposure_multiplier>`

classref-property-setget

-   `void (No return value.)` **set\_exposure\_multiplier**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_exposure\_multiplier**()

Multiplier for the exposure amount. A higher value results in a brighter
image.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **exposure\_sensitivity** = `100.0`
`🔗<class_CameraAttributes_property_exposure_sensitivity>`

classref-property-setget

-   `void (No return value.)` **set\_exposure\_sensitivity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_exposure\_sensitivity**()

Sensitivity of camera sensors, measured in ISO. A higher sensitivity
results in a brighter image. Only available when
`ProjectSettings.rendering/lights_and_shadows/use_physical_light_units<class_ProjectSettings_property_rendering/lights_and_shadows/use_physical_light_units>`
is enabled. When
`auto_exposure_enabled<class_CameraAttributes_property_auto_exposure_enabled>`
this can be used as a method of exposure compensation, doubling the
value will increase the exposure value (measured in EV100) by 1 stop.
