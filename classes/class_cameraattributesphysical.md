github\_url  
hide

# CameraAttributesPhysical

**Inherits:** `CameraAttributes<class_CameraAttributes>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Physically-based camera settings.

classref-introduction-group

## Description

**CameraAttributesPhysical** is used to set rendering settings based on
a physically-based camera's settings. It is responsible for exposure,
auto-exposure, and depth of field.

When used in a `WorldEnvironment<class_WorldEnvironment>` it provides
default settings for exposure, auto-exposure, and depth of field that
will be used by all cameras without their own
`CameraAttributes<class_CameraAttributes>`, including the editor camera.
When used in a `Camera3D<class_Camera3D>` it will override any
`CameraAttributes<class_CameraAttributes>` set in the
`WorldEnvironment<class_WorldEnvironment>` and will override the
`Camera3D<class_Camera3D>`s `Camera3D.far<class_Camera3D_property_far>`,
`Camera3D.near<class_Camera3D_property_near>`,
`Camera3D.fov<class_Camera3D_property_fov>`, and
`Camera3D.keep_aspect<class_Camera3D_property_keep_aspect>` properties.
When used in `VoxelGI<class_VoxelGI>` or `LightmapGI<class_LightmapGI>`,
only the exposure settings will be used.

The default settings are intended for use in an outdoor environment,
tips for settings for use in an indoor environment can be found in each
setting's documentation.

\*\*Note:\*\* Depth of field blur is only supported in the Forward+ and
Mobile rendering methods, not Compatibility.

classref-introduction-group

## Tutorials

-   `Physical light and camera units <../tutorials/3d/physical_light_and_camera_units>`

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

## Property Descriptions

classref-property

`float<class_float>` **auto\_exposure\_max\_exposure\_value** = `10.0`
`🔗<class_CameraAttributesPhysical_property_auto_exposure_max_exposure_value>`

classref-property-setget

-   `void (No return value.)`
    **set\_auto\_exposure\_max\_exposure\_value**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_auto\_exposure\_max\_exposure\_value**()

The maximum luminance (in EV100) used when calculating auto exposure.
When calculating scene average luminance, color values will be clamped
to at least this value. This limits the auto-exposure from exposing
below a certain brightness, resulting in a cut off point where the scene
will remain bright.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **auto\_exposure\_min\_exposure\_value** = `-8.0`
`🔗<class_CameraAttributesPhysical_property_auto_exposure_min_exposure_value>`

classref-property-setget

-   `void (No return value.)`
    **set\_auto\_exposure\_min\_exposure\_value**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_auto\_exposure\_min\_exposure\_value**()

The minimum luminance (in EV100) used when calculating auto exposure.
When calculating scene average luminance, color values will be clamped
to at least this value. This limits the auto-exposure from exposing
above a certain brightness, resulting in a cut off point where the scene
will remain dark.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **exposure\_aperture** = `16.0`
`🔗<class_CameraAttributesPhysical_property_exposure_aperture>`

classref-property-setget

-   `void (No return value.)` **set\_aperture**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_aperture**()

Size of the aperture of the camera, measured in f-stops. An f-stop is a
unitless ratio between the focal length of the camera and the diameter
of the aperture. A high aperture setting will result in a smaller
aperture which leads to a dimmer image and sharper focus. A low aperture
results in a wide aperture which lets in more light resulting in a
brighter, less-focused image. Default is appropriate for outdoors at
daytime (i.e. for use with a default
`DirectionalLight3D<class_DirectionalLight3D>`), for indoor lighting, a
value between 2 and 4 is more appropriate.

Only available when
`ProjectSettings.rendering/lights_and_shadows/use_physical_light_units<class_ProjectSettings_property_rendering/lights_and_shadows/use_physical_light_units>`
is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **exposure\_shutter\_speed** = `100.0`
`🔗<class_CameraAttributesPhysical_property_exposure_shutter_speed>`

classref-property-setget

-   `void (No return value.)` **set\_shutter\_speed**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_shutter\_speed**()

Time for shutter to open and close, evaluated as `1 / shutter_speed`
seconds. A higher value will allow less light (leading to a darker
image), while a lower value will allow more light (leading to a brighter
image).

Only available when
`ProjectSettings.rendering/lights_and_shadows/use_physical_light_units<class_ProjectSettings_property_rendering/lights_and_shadows/use_physical_light_units>`
is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **frustum\_far** = `4000.0`
`🔗<class_CameraAttributesPhysical_property_frustum_far>`

classref-property-setget

-   `void (No return value.)` **set\_far**(value: `float<class_float>`)
-   `float<class_float>` **get\_far**()

Override value for `Camera3D.far<class_Camera3D_property_far>`. Used
internally when calculating depth of field. When attached to a
`Camera3D<class_Camera3D>` as its
`Camera3D.attributes<class_Camera3D_property_attributes>`, it will
override the `Camera3D.far<class_Camera3D_property_far>` property.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **frustum\_focal\_length** = `35.0`
`🔗<class_CameraAttributesPhysical_property_frustum_focal_length>`

classref-property-setget

-   `void (No return value.)` **set\_focal\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_focal\_length**()

Distance between camera lens and camera aperture, measured in
millimeters. Controls field of view and depth of field. A larger focal
length will result in a smaller field of view and a narrower depth of
field meaning fewer objects will be in focus. A smaller focal length
will result in a wider field of view and a larger depth of field meaning
more objects will be in focus. When attached to a
`Camera3D<class_Camera3D>` as its
`Camera3D.attributes<class_Camera3D_property_attributes>`, it will
override the `Camera3D.fov<class_Camera3D_property_fov>` property and
the `Camera3D.keep_aspect<class_Camera3D_property_keep_aspect>`
property.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **frustum\_focus\_distance** = `10.0`
`🔗<class_CameraAttributesPhysical_property_frustum_focus_distance>`

classref-property-setget

-   `void (No return value.)` **set\_focus\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_focus\_distance**()

Distance from camera of object that will be in focus, measured in
meters. Internally this will be clamped to be at least 1 millimeter
larger than
`frustum_focal_length<class_CameraAttributesPhysical_property_frustum_focal_length>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **frustum\_near** = `0.05`
`🔗<class_CameraAttributesPhysical_property_frustum_near>`

classref-property-setget

-   `void (No return value.)` **set\_near**(value: `float<class_float>`)
-   `float<class_float>` **get\_near**()

Override value for `Camera3D.near<class_Camera3D_property_near>`. Used
internally when calculating depth of field. When attached to a
`Camera3D<class_Camera3D>` as its
`Camera3D.attributes<class_Camera3D_property_attributes>`, it will
override the `Camera3D.near<class_Camera3D_property_near>` property.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_fov**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CameraAttributesPhysical_method_get_fov>`

Returns the vertical field of view that corresponds to the
`frustum_focal_length<class_CameraAttributesPhysical_property_frustum_focal_length>`.
This value is calculated internally whenever
`frustum_focal_length<class_CameraAttributesPhysical_property_frustum_focal_length>`
is changed.
