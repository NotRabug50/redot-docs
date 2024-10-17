github\_url  
hide

# RDShaderSource

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Shader source code (used by `RenderingDevice<class_RenderingDevice>`).

classref-introduction-group

## Description

Shader source code in text form.

See also `RDShaderFile<class_RDShaderFile>`. **RDShaderSource** is only
meant to be used with the `RenderingDevice<class_RenderingDevice>` API.
It should not be confused with Godot's own `Shader<class_Shader>`
resource, which is what Godot's various nodes use for high-level shader
programming.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`ShaderLanguage<enum_RenderingDevice_ShaderLanguage>` **language** = `0`
`🔗<class_RDShaderSource_property_language>`

classref-property-setget

-   `void (No return value.)` **set\_language**(value:
    `ShaderLanguage<enum_RenderingDevice_ShaderLanguage>`)
-   `ShaderLanguage<enum_RenderingDevice_ShaderLanguage>`
    **get\_language**()

The language the shader is written in.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **source\_compute** = `""`
`🔗<class_RDShaderSource_property_source_compute>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_source**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, source:
    `String<class_String>`)
-   `String<class_String>` **get\_stage\_source**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Source code for the shader's compute stage.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **source\_fragment** = `""`
`🔗<class_RDShaderSource_property_source_fragment>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_source**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, source:
    `String<class_String>`)
-   `String<class_String>` **get\_stage\_source**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Source code for the shader's fragment stage.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **source\_tesselation\_control** = `""`
`🔗<class_RDShaderSource_property_source_tesselation_control>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_source**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, source:
    `String<class_String>`)
-   `String<class_String>` **get\_stage\_source**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Source code for the shader's tessellation control stage.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **source\_tesselation\_evaluation** = `""`
`🔗<class_RDShaderSource_property_source_tesselation_evaluation>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_source**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, source:
    `String<class_String>`)
-   `String<class_String>` **get\_stage\_source**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Source code for the shader's tessellation evaluation stage.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **source\_vertex** = `""`
`🔗<class_RDShaderSource_property_source_vertex>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_source**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, source:
    `String<class_String>`)
-   `String<class_String>` **get\_stage\_source**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Source code for the shader's vertex stage.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`String<class_String>` **get\_stage\_source**(stage:
`ShaderStage<enum_RenderingDevice_ShaderStage>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RDShaderSource_method_get_stage_source>`

Returns source code for the specified shader `stage`. Equivalent to
getting one of
`source_compute<class_RDShaderSource_property_source_compute>`,
`source_fragment<class_RDShaderSource_property_source_fragment>`,
`source_tesselation_control<class_RDShaderSource_property_source_tesselation_control>`,
`source_tesselation_evaluation<class_RDShaderSource_property_source_tesselation_evaluation>`
or `source_vertex<class_RDShaderSource_property_source_vertex>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_stage\_source**(stage:
`ShaderStage<enum_RenderingDevice_ShaderStage>`, source:
`String<class_String>`)
`🔗<class_RDShaderSource_method_set_stage_source>`

Sets `source` code for the specified shader `stage`. Equivalent to
setting one of
`source_compute<class_RDShaderSource_property_source_compute>`,
`source_fragment<class_RDShaderSource_property_source_fragment>`,
`source_tesselation_control<class_RDShaderSource_property_source_tesselation_control>`,
`source_tesselation_evaluation<class_RDShaderSource_property_source_tesselation_evaluation>`
or `source_vertex<class_RDShaderSource_property_source_vertex>`.

\*\*Note:\*\* If you set the compute shader source code using this
method directly, remember to remove the Godot-specific hint
`#[compute]`.
