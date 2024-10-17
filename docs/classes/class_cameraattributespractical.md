github\_url  
hide

# CameraAttributesPractical

**Inherits:** `CameraAttributes<class_CameraAttributes>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Camera settings in an easy to use format.

classref-introduction-group

## Description

Controls camera-specific attributes such as auto-exposure, depth of
field, and exposure override.

When used in a `WorldEnvironment<class_WorldEnvironment>` it provides
default settings for exposure, auto-exposure, and depth of field that
will be used by all cameras without their own
`CameraAttributes<class_CameraAttributes>`, including the editor camera.
When used in a `Camera3D<class_Camera3D>` it will override any
`CameraAttributes<class_CameraAttributes>` set in the
`WorldEnvironment<class_WorldEnvironment>`. When used in
`VoxelGI<class_VoxelGI>` or `LightmapGI<class_LightmapGI>`, only the
exposure settings will be used.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **auto\_exposure\_max\_sensitivity** = `800.0`
`🔗<class_CameraAttributesPractical_property_auto_exposure_max_sensitivity>`

classref-property-setget

-   `void (No return value.)`
    **set\_auto\_exposure\_max\_sensitivity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_auto\_exposure\_max\_sensitivity**()

The maximum sensitivity (in ISO) used when calculating auto exposure.
When calculating scene average luminance, color values will be clamped
to at least this value. This limits the auto-exposure from exposing
below a certain brightness, resulting in a cut off point where the scene
will remain bright.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **auto\_exposure\_min\_sensitivity** = `0.0`
`🔗<class_CameraAttributesPractical_property_auto_exposure_min_sensitivity>`

classref-property-setget

-   `void (No return value.)`
    **set\_auto\_exposure\_min\_sensitivity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_auto\_exposure\_min\_sensitivity**()

The minimum sensitivity (in ISO) used when calculating auto exposure.
When calculating scene average luminance, color values will be clamped
to at least this value. This limits the auto-exposure from exposing
above a certain brightness, resulting in a cut off point where the scene
will remain dark.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **dof\_blur\_amount** = `0.1`
`🔗<class_CameraAttributesPractical_property_dof_blur_amount>`

classref-property-setget

-   `void (No return value.)` **set\_dof\_blur\_amount**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_dof\_blur\_amount**()

Sets the maximum amount of blur. When using physically-based blur
amounts, will instead act as a multiplier. High values lead to an
increased amount of blurriness, but can be much more expensive to
calculate. It is best to keep this as low as possible for a given art
style.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **dof\_blur\_far\_distance** = `10.0`
`🔗<class_CameraAttributesPractical_property_dof_blur_far_distance>`

classref-property-setget

-   `void (No return value.)` **set\_dof\_blur\_far\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_dof\_blur\_far\_distance**()

Objects further from the `Camera3D<class_Camera3D>` by this amount will
be blurred by the depth of field effect. Measured in meters.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **dof\_blur\_far\_enabled** = `false`
`🔗<class_CameraAttributesPractical_property_dof_blur_far_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_dof\_blur\_far\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_dof\_blur\_far\_enabled**()

Enables depth of field blur for objects further than
`dof_blur_far_distance<class_CameraAttributesPractical_property_dof_blur_far_distance>`.
Strength of blur is controlled by
`dof_blur_amount<class_CameraAttributesPractical_property_dof_blur_amount>`
and modulated by
`dof_blur_far_transition<class_CameraAttributesPractical_property_dof_blur_far_transition>`.

\*\*Note:\*\* Depth of field blur is only supported in the Forward+ and
Mobile rendering methods, not Compatibility.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **dof\_blur\_far\_transition** = `5.0`
`🔗<class_CameraAttributesPractical_property_dof_blur_far_transition>`

classref-property-setget

-   `void (No return value.)` **set\_dof\_blur\_far\_transition**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_dof\_blur\_far\_transition**()

When positive, distance over which (starting from
`dof_blur_far_distance<class_CameraAttributesPractical_property_dof_blur_far_distance>`)
blur effect will scale from 0 to
`dof_blur_amount<class_CameraAttributesPractical_property_dof_blur_amount>`.
When negative, uses physically-based scaling so depth of field effect
will scale from 0 at
`dof_blur_far_distance<class_CameraAttributesPractical_property_dof_blur_far_distance>`
and will increase in a physically accurate way as objects get further
from the `Camera3D<class_Camera3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **dof\_blur\_near\_distance** = `2.0`
`🔗<class_CameraAttributesPractical_property_dof_blur_near_distance>`

classref-property-setget

-   `void (No return value.)` **set\_dof\_blur\_near\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_dof\_blur\_near\_distance**()

Objects closer from the `Camera3D<class_Camera3D>` by this amount will
be blurred by the depth of field effect. Measured in meters.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **dof\_blur\_near\_enabled** = `false`
`🔗<class_CameraAttributesPractical_property_dof_blur_near_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_dof\_blur\_near\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_dof\_blur\_near\_enabled**()

Enables depth of field blur for objects closer than
`dof_blur_near_distance<class_CameraAttributesPractical_property_dof_blur_near_distance>`.
Strength of blur is controlled by
`dof_blur_amount<class_CameraAttributesPractical_property_dof_blur_amount>`
and modulated by
`dof_blur_near_transition<class_CameraAttributesPractical_property_dof_blur_near_transition>`.

\*\*Note:\*\* Depth of field blur is only supported in the Forward+ and
Mobile rendering methods, not Compatibility.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **dof\_blur\_near\_transition** = `1.0`
`🔗<class_CameraAttributesPractical_property_dof_blur_near_transition>`

classref-property-setget

-   `void (No return value.)`
    **set\_dof\_blur\_near\_transition**(value: `float<class_float>`)
-   `float<class_float>` **get\_dof\_blur\_near\_transition**()

When positive, distance over which blur effect will scale from 0 to
`dof_blur_amount<class_CameraAttributesPractical_property_dof_blur_amount>`,
ending at
`dof_blur_near_distance<class_CameraAttributesPractical_property_dof_blur_near_distance>`.
When negative, uses physically-based scaling so depth of field effect
will scale from 0 at
`dof_blur_near_distance<class_CameraAttributesPractical_property_dof_blur_near_distance>`
and will increase in a physically accurate way as objects get closer to
the `Camera3D<class_Camera3D>`.
