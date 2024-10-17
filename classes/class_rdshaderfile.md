github\_url  
hide

# RDShaderFile

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Compiled shader file in SPIR-V form (used by
`RenderingDevice<class_RenderingDevice>`). Not to be confused with
Godot's own `Shader<class_Shader>`.

classref-introduction-group

## Description

Compiled shader file in SPIR-V form.

See also `RDShaderSource<class_RDShaderSource>`. **RDShaderFile** is
only meant to be used with the `RenderingDevice<class_RenderingDevice>`
API. It should not be confused with Godot's own `Shader<class_Shader>`
resource, which is what Godot's various nodes use for high-level shader
programming.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **base\_error** = `""`
`🔗<class_RDShaderFile_property_base_error>`

classref-property-setget

-   `void (No return value.)` **set\_base\_error**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_base\_error**()

The base compilation error message, which indicates errors not related
to a specific shader stage if non-empty. If empty, shader compilation is
not necessarily successful (check `RDShaderSPIRV<class_RDShaderSPIRV>`'s
error message members).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`RDShaderSPIRV<class_RDShaderSPIRV>` **get\_spirv**(version:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RDShaderFile_method_get_spirv>`

Returns the SPIR-V intermediate representation for the specified shader
`version`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`StringName<class_StringName>`\]
**get\_version\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RDShaderFile_method_get_version_list>`

Returns the list of compiled versions for this shader.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bytecode**(bytecode:
`RDShaderSPIRV<class_RDShaderSPIRV>`, version:
`StringName<class_StringName>` = &"")
`🔗<class_RDShaderFile_method_set_bytecode>`

Sets the SPIR-V `bytecode` that will be compiled for the specified
`version`.
