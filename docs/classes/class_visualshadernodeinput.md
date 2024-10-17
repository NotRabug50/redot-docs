github\_url  
hide

# VisualShaderNodeInput

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Represents the input shader parameter within the visual shader graph.

classref-introduction-group

## Description

Gives access to input variables (built-ins) available for the shader.
See the shading reference for the list of available built-ins for each
shader type (check `Tutorials` section for link).

classref-introduction-group

## Tutorials

-   `Shading reference index <../tutorials/shaders/shader_reference/index>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**input\_type\_changed**()
`🔗<class_VisualShaderNodeInput_signal_input_type_changed>`

Emitted when input is changed via
`input_name<class_VisualShaderNodeInput_property_input_name>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **input\_name** = `"[None]"`
`🔗<class_VisualShaderNodeInput_property_input_name>`

classref-property-setget

-   `void (No return value.)` **set\_input\_name**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_input\_name**()

One of the several input constants in lower-case style like: "vertex"
(`VERTEX`) or "point\_size" (`POINT_SIZE`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`String<class_String>` **get\_input\_real\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNodeInput_method_get_input_real_name>`

Returns a translated name of the current constant in the Godot Shader
Language. E.g. `"ALBEDO"` if the
`input_name<class_VisualShaderNodeInput_property_input_name>` equal to
`"albedo"`.
