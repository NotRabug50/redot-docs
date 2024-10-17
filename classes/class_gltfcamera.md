github\_url  
hide

# GLTFCamera

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Represents a glTF camera.

classref-introduction-group

## Description

Represents a camera as defined by the base glTF spec.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`
-   [glTF camera detailed
    specification](https://registry.khronos.org/glTF/specs/2.0/glTF-2.0.html#reference-camera)
-   [glTF camera spec and example
    file](https://github.com/KhronosGroup/glTF-Tutorials/blob/master/gltfTutorial/gltfTutorial_015_SimpleCameras.md)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **depth\_far** = `4000.0`
`🔗<class_GLTFCamera_property_depth_far>`

classref-property-setget

-   `void (No return value.)` **set\_depth\_far**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_depth\_far**()

The distance to the far culling boundary for this camera relative to its
local Z axis, in meters. This maps to glTF's `zfar` property.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **depth\_near** = `0.05`
`🔗<class_GLTFCamera_property_depth_near>`

classref-property-setget

-   `void (No return value.)` **set\_depth\_near**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_depth\_near**()

The distance to the near culling boundary for this camera relative to
its local Z axis, in meters. This maps to glTF's `znear` property.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **fov** = `1.309`
`🔗<class_GLTFCamera_property_fov>`

classref-property-setget

-   `void (No return value.)` **set\_fov**(value: `float<class_float>`)
-   `float<class_float>` **get\_fov**()

The FOV of the camera. This class and glTF define the camera FOV in
radians, while Godot uses degrees. This maps to glTF's `yfov` property.
This value is only used for perspective cameras, when
`perspective<class_GLTFCamera_property_perspective>` is true.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **perspective** = `true`
`🔗<class_GLTFCamera_property_perspective>`

classref-property-setget

-   `void (No return value.)` **set\_perspective**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_perspective**()

Whether or not the camera is in perspective mode. If false, the camera
is in orthographic/orthogonal mode. This maps to glTF's camera `type`
property. See `Camera3D.projection<class_Camera3D_property_projection>`
and the glTF spec for more information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **size\_mag** = `0.5`
`🔗<class_GLTFCamera_property_size_mag>`

classref-property-setget

-   `void (No return value.)` **set\_size\_mag**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_size\_mag**()

The size of the camera. This class and glTF define the camera size
magnitude as a radius in meters, while Godot defines it as a diameter in
meters. This maps to glTF's `ymag` property. This value is only used for
orthographic/orthogonal cameras, when
`perspective<class_GLTFCamera_property_perspective>` is false.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`GLTFCamera<class_GLTFCamera>` **from\_dictionary**(dictionary:
`Dictionary<class_Dictionary>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFCamera_method_from_dictionary>`

Creates a new GLTFCamera instance by parsing the given
`Dictionary<class_Dictionary>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`GLTFCamera<class_GLTFCamera>` **from\_node**(camera\_node:
`Camera3D<class_Camera3D>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFCamera_method_from_node>`

Create a new GLTFCamera instance from the given Godot
`Camera3D<class_Camera3D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **to\_dictionary**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GLTFCamera_method_to_dictionary>`

Serializes this GLTFCamera instance into a
`Dictionary<class_Dictionary>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Camera3D<class_Camera3D>` **to\_node**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GLTFCamera_method_to_node>`

Converts this GLTFCamera instance into a Godot
`Camera3D<class_Camera3D>` node.
