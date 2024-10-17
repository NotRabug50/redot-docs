github\_url  
hide

# GLTFLight

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Represents a glTF light.

classref-introduction-group

## Description

Represents a light as defined by the `KHR_lights_punctual` glTF
extension.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`
-   [KHR\_lights\_punctual glTF extension
    spec](https://github.com/KhronosGroup/glTF/blob/main/extensions/2.0/Khronos/KHR_lights_punctual)

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

classref-reftable-group

## Methods

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

`Color<class_Color>` **color** = `Color(1, 1, 1, 1)`
`🔗<class_GLTFLight_property_color>`

classref-property-setget

-   `void (No return value.)` **set\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_color**()

The `Color<class_Color>` of the light. Defaults to white. A black color
causes the light to have no effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **inner\_cone\_angle** = `0.0`
`🔗<class_GLTFLight_property_inner_cone_angle>`

classref-property-setget

-   `void (No return value.)` **set\_inner\_cone\_angle**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_inner\_cone\_angle**()

The inner angle of the cone in a spotlight. Must be less than or equal
to the outer cone angle.

Within this angle, the light is at full brightness. Between the inner
and outer cone angles, there is a transition from full brightness to
zero brightness. When creating a Godot `SpotLight3D<class_SpotLight3D>`,
the ratio between the inner and outer cone angles is used to calculate
the attenuation of the light.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **intensity** = `1.0`
`🔗<class_GLTFLight_property_intensity>`

classref-property-setget

-   `void (No return value.)` **set\_intensity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_intensity**()

The intensity of the light. This is expressed in candelas (lumens per
steradian) for point and spot lights, and lux (lumens per m²) for
directional lights. When creating a Godot light, this value is converted
to a unitless multiplier.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **light\_type** = `""`
`🔗<class_GLTFLight_property_light_type>`

classref-property-setget

-   `void (No return value.)` **set\_light\_type**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_light\_type**()

The type of the light. The values accepted by Godot are "point", "spot",
and "directional", which correspond to Godot's
`OmniLight3D<class_OmniLight3D>`, `SpotLight3D<class_SpotLight3D>`, and
`DirectionalLight3D<class_DirectionalLight3D>` respectively.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **outer\_cone\_angle** = `0.785398`
`🔗<class_GLTFLight_property_outer_cone_angle>`

classref-property-setget

-   `void (No return value.)` **set\_outer\_cone\_angle**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_outer\_cone\_angle**()

The outer angle of the cone in a spotlight. Must be greater than or
equal to the inner angle.

At this angle, the light drops off to zero brightness. Between the inner
and outer cone angles, there is a transition from full brightness to
zero brightness. If this angle is a half turn, then the spotlight emits
in all directions. When creating a Godot
`SpotLight3D<class_SpotLight3D>`, the outer cone angle is used as the
angle of the spotlight.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **range** = `inf`
`🔗<class_GLTFLight_property_range>`

classref-property-setget

-   `void (No return value.)` **set\_range**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_range**()

The range of the light, beyond which the light has no effect. glTF
lights with no range defined behave like physical lights (which have
infinite range). When creating a Godot light, the range is clamped to
4096.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`GLTFLight<class_GLTFLight>` **from\_dictionary**(dictionary:
`Dictionary<class_Dictionary>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFLight_method_from_dictionary>`

Creates a new GLTFLight instance by parsing the given
`Dictionary<class_Dictionary>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`GLTFLight<class_GLTFLight>` **from\_node**(light\_node:
`Light3D<class_Light3D>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFLight_method_from_node>`

Create a new GLTFLight instance from the given Godot
`Light3D<class_Light3D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_additional\_data**(extension\_name:
`StringName<class_StringName>`)
`🔗<class_GLTFLight_method_get_additional_data>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_additional\_data**(extension\_name:
`StringName<class_StringName>`, additional\_data:
`Variant<class_Variant>`)
`🔗<class_GLTFLight_method_set_additional_data>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **to\_dictionary**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GLTFLight_method_to_dictionary>`

Serializes this GLTFLight instance into a
`Dictionary<class_Dictionary>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Light3D<class_Light3D>` **to\_node**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GLTFLight_method_to_node>`

Converts this GLTFLight instance into a Godot `Light3D<class_Light3D>`
node.
