github\_url  
hide

# RDShaderSPIRV

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

SPIR-V intermediate representation as part of a
`RDShaderFile<class_RDShaderFile>` (used by
`RenderingDevice<class_RenderingDevice>`).

classref-introduction-group

## Description

**RDShaderSPIRV** represents a `RDShaderFile<class_RDShaderFile>`'s
[SPIR-V](https://www.khronos.org/spir/) code for various shader stages,
as well as possible compilation error messages. SPIR-V is a low-level
intermediate shader representation. This intermediate representation is
not used directly by GPUs for rendering, but it can be compiled into
binary shaders that GPUs can understand. Unlike compiled shaders, SPIR-V
is portable across GPU models and driver versions.

This object is used by `RenderingDevice<class_RenderingDevice>`.

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

`PackedByteArray<class_PackedByteArray>` **bytecode\_compute** =
`PackedByteArray()` `🔗<class_RDShaderSPIRV_property_bytecode_compute>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_bytecode**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, bytecode:
    `PackedByteArray<class_PackedByteArray>`)
-   `PackedByteArray<class_PackedByteArray>`
    **get\_stage\_bytecode**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The SPIR-V bytecode for the compute shader stage.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedByteArray<class_PackedByteArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedByteArray<class_PackedByteArray>` **bytecode\_fragment** =
`PackedByteArray()` `🔗<class_RDShaderSPIRV_property_bytecode_fragment>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_bytecode**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, bytecode:
    `PackedByteArray<class_PackedByteArray>`)
-   `PackedByteArray<class_PackedByteArray>`
    **get\_stage\_bytecode**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The SPIR-V bytecode for the fragment shader stage.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedByteArray<class_PackedByteArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedByteArray<class_PackedByteArray>`
**bytecode\_tesselation\_control** = `PackedByteArray()`
`🔗<class_RDShaderSPIRV_property_bytecode_tesselation_control>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_bytecode**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, bytecode:
    `PackedByteArray<class_PackedByteArray>`)
-   `PackedByteArray<class_PackedByteArray>`
    **get\_stage\_bytecode**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The SPIR-V bytecode for the tessellation control shader stage.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedByteArray<class_PackedByteArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedByteArray<class_PackedByteArray>`
**bytecode\_tesselation\_evaluation** = `PackedByteArray()`
`🔗<class_RDShaderSPIRV_property_bytecode_tesselation_evaluation>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_bytecode**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, bytecode:
    `PackedByteArray<class_PackedByteArray>`)
-   `PackedByteArray<class_PackedByteArray>`
    **get\_stage\_bytecode**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The SPIR-V bytecode for the tessellation evaluation shader stage.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedByteArray<class_PackedByteArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedByteArray<class_PackedByteArray>` **bytecode\_vertex** =
`PackedByteArray()` `🔗<class_RDShaderSPIRV_property_bytecode_vertex>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_bytecode**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, bytecode:
    `PackedByteArray<class_PackedByteArray>`)
-   `PackedByteArray<class_PackedByteArray>`
    **get\_stage\_bytecode**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The SPIR-V bytecode for the vertex shader stage.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedByteArray<class_PackedByteArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **compile\_error\_compute** = `""`
`🔗<class_RDShaderSPIRV_property_compile_error_compute>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_compile\_error**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, compile\_error:
    `String<class_String>`)
-   `String<class_String>` **get\_stage\_compile\_error**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The compilation error message for the compute shader stage (set by the
SPIR-V compiler and Godot). If empty, shader compilation was successful.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **compile\_error\_fragment** = `""`
`🔗<class_RDShaderSPIRV_property_compile_error_fragment>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_compile\_error**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, compile\_error:
    `String<class_String>`)
-   `String<class_String>` **get\_stage\_compile\_error**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The compilation error message for the fragment shader stage (set by the
SPIR-V compiler and Godot). If empty, shader compilation was successful.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **compile\_error\_tesselation\_control** = `""`
`🔗<class_RDShaderSPIRV_property_compile_error_tesselation_control>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_compile\_error**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, compile\_error:
    `String<class_String>`)
-   `String<class_String>` **get\_stage\_compile\_error**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The compilation error message for the tessellation control shader stage
(set by the SPIR-V compiler and Godot). If empty, shader compilation was
successful.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **compile\_error\_tesselation\_evaluation** =
`""`
`🔗<class_RDShaderSPIRV_property_compile_error_tesselation_evaluation>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_compile\_error**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, compile\_error:
    `String<class_String>`)
-   `String<class_String>` **get\_stage\_compile\_error**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The compilation error message for the tessellation evaluation shader
stage (set by the SPIR-V compiler and Godot). If empty, shader
compilation was successful.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **compile\_error\_vertex** = `""`
`🔗<class_RDShaderSPIRV_property_compile_error_vertex>`

classref-property-setget

-   `void (No return value.)` **set\_stage\_compile\_error**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`, compile\_error:
    `String<class_String>`)
-   `String<class_String>` **get\_stage\_compile\_error**(stage:
    `ShaderStage<enum_RenderingDevice_ShaderStage>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The compilation error message for the vertex shader stage (set by the
SPIR-V compiler and Godot). If empty, shader compilation was successful.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`PackedByteArray<class_PackedByteArray>` **get\_stage\_bytecode**(stage:
`ShaderStage<enum_RenderingDevice_ShaderStage>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RDShaderSPIRV_method_get_stage_bytecode>`

Equivalent to getting one of
`bytecode_compute<class_RDShaderSPIRV_property_bytecode_compute>`,
`bytecode_fragment<class_RDShaderSPIRV_property_bytecode_fragment>`,
`bytecode_tesselation_control<class_RDShaderSPIRV_property_bytecode_tesselation_control>`,
`bytecode_tesselation_evaluation<class_RDShaderSPIRV_property_bytecode_tesselation_evaluation>`,
`bytecode_vertex<class_RDShaderSPIRV_property_bytecode_vertex>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_stage\_compile\_error**(stage:
`ShaderStage<enum_RenderingDevice_ShaderStage>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RDShaderSPIRV_method_get_stage_compile_error>`

Returns the compilation error message for the given shader `stage`.
Equivalent to getting one of
`compile_error_compute<class_RDShaderSPIRV_property_compile_error_compute>`,
`compile_error_fragment<class_RDShaderSPIRV_property_compile_error_fragment>`,
`compile_error_tesselation_control<class_RDShaderSPIRV_property_compile_error_tesselation_control>`,
`compile_error_tesselation_evaluation<class_RDShaderSPIRV_property_compile_error_tesselation_evaluation>`,
`compile_error_vertex<class_RDShaderSPIRV_property_compile_error_vertex>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_stage\_bytecode**(stage:
`ShaderStage<enum_RenderingDevice_ShaderStage>`, bytecode:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_RDShaderSPIRV_method_set_stage_bytecode>`

Sets the SPIR-V `bytecode` for the given shader `stage`. Equivalent to
setting one of
`bytecode_compute<class_RDShaderSPIRV_property_bytecode_compute>`,
`bytecode_fragment<class_RDShaderSPIRV_property_bytecode_fragment>`,
`bytecode_tesselation_control<class_RDShaderSPIRV_property_bytecode_tesselation_control>`,
`bytecode_tesselation_evaluation<class_RDShaderSPIRV_property_bytecode_tesselation_evaluation>`,
`bytecode_vertex<class_RDShaderSPIRV_property_bytecode_vertex>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_stage\_compile\_error**(stage:
`ShaderStage<enum_RenderingDevice_ShaderStage>`, compile\_error:
`String<class_String>`)
`🔗<class_RDShaderSPIRV_method_set_stage_compile_error>`

Sets the compilation error message for the given shader `stage` to
`compile_error`. Equivalent to setting one of
`compile_error_compute<class_RDShaderSPIRV_property_compile_error_compute>`,
`compile_error_fragment<class_RDShaderSPIRV_property_compile_error_fragment>`,
`compile_error_tesselation_control<class_RDShaderSPIRV_property_compile_error_tesselation_control>`,
`compile_error_tesselation_evaluation<class_RDShaderSPIRV_property_compile_error_tesselation_evaluation>`,
`compile_error_vertex<class_RDShaderSPIRV_property_compile_error_vertex>`.
