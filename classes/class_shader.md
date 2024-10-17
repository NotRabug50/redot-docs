github\_url  
hide

# Shader

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `VisualShader<class_VisualShader>`

A shader implemented in the Godot shading language.

classref-introduction-group

## Description

A custom shader program implemented in the Godot shading language, saved
with the `.gdshader` extension.

This class is used by a `ShaderMaterial<class_ShaderMaterial>` and
allows you to write your own custom behavior for rendering visual items
or updating particle information. For a detailed explanation and usage,
please see the tutorials linked below.

classref-introduction-group

## Tutorials

-   `Shaders documentation index <../tutorials/shaders/index>`

classref-reftable-group

## Properties

<table>
<tbody>
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

## Enumerations

classref-enumeration

enum **Mode**: `🔗<enum_Shader_Mode>`

classref-enumeration-constant

`Mode<enum_Shader_Mode>` **MODE\_SPATIAL** = `0`

Mode used to draw all 3D objects.

classref-enumeration-constant

`Mode<enum_Shader_Mode>` **MODE\_CANVAS\_ITEM** = `1`

Mode used to draw all 2D objects.

classref-enumeration-constant

`Mode<enum_Shader_Mode>` **MODE\_PARTICLES** = `2`

Mode used to calculate particle information on a per-particle basis. Not
used for drawing.

classref-enumeration-constant

`Mode<enum_Shader_Mode>` **MODE\_SKY** = `3`

Mode used for drawing skies. Only works with shaders attached to
`Sky<class_Sky>` objects.

classref-enumeration-constant

`Mode<enum_Shader_Mode>` **MODE\_FOG** = `4`

Mode used for setting the color and density of volumetric fog effect.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **code** = `""` `🔗<class_Shader_property_code>`

classref-property-setget

-   `void (No return value.)` **set\_code**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_code**()

Returns the shader's code as the user has written it, not the full
generated code used internally.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Texture<class_Texture>` **get\_default\_texture\_parameter**(name:
`StringName<class_StringName>`, index: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Shader_method_get_default_texture_parameter>`

Returns the texture that is set as default for the specified parameter.

\*\*Note:\*\* `name` must match the name of the uniform in the code
exactly.

\*\*Note:\*\* If the sampler array is used use `index` to access the
specified texture.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Mode<enum_Shader_Mode>` **get\_mode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Shader_method_get_mode>`

Returns the shader mode for the shader.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_shader\_uniform\_list**(get\_groups:
`bool<class_bool>` = false)
`🔗<class_Shader_method_get_shader_uniform_list>`

Get the list of shader uniforms that can be assigned to a
`ShaderMaterial<class_ShaderMaterial>`, for use with
`ShaderMaterial.set_shader_parameter<class_ShaderMaterial_method_set_shader_parameter>`
and
`ShaderMaterial.get_shader_parameter<class_ShaderMaterial_method_get_shader_parameter>`.
The parameters returned are contained in dictionaries in a similar
format to the ones returned by
`Object.get_property_list<class_Object_method_get_property_list>`.

If argument `get_groups` is true, parameter grouping hints will be
provided.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_default\_texture\_parameter**(name:
`StringName<class_StringName>`, texture: `Texture<class_Texture>`,
index: `int<class_int>` = 0)
`🔗<class_Shader_method_set_default_texture_parameter>`

Sets the default texture to be used with a texture uniform. The default
is used if a texture is not set in the
`ShaderMaterial<class_ShaderMaterial>`.

\*\*Note:\*\* `name` must match the name of the uniform in the code
exactly.

\*\*Note:\*\* If the sampler array is used use `index` to access the
specified texture.
