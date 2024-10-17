github\_url  
hide

# VisualShaderNodeParameter

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`VisualShaderNodeBooleanParameter<class_VisualShaderNodeBooleanParameter>`,
`VisualShaderNodeColorParameter<class_VisualShaderNodeColorParameter>`,
`VisualShaderNodeFloatParameter<class_VisualShaderNodeFloatParameter>`,
`VisualShaderNodeIntParameter<class_VisualShaderNodeIntParameter>`,
`VisualShaderNodeTextureParameter<class_VisualShaderNodeTextureParameter>`,
`VisualShaderNodeTransformParameter<class_VisualShaderNodeTransformParameter>`,
`VisualShaderNodeUIntParameter<class_VisualShaderNodeUIntParameter>`,
`VisualShaderNodeVec2Parameter<class_VisualShaderNodeVec2Parameter>`,
`VisualShaderNodeVec3Parameter<class_VisualShaderNodeVec3Parameter>`,
`VisualShaderNodeVec4Parameter<class_VisualShaderNodeVec4Parameter>`

A base type for the parameters within the visual shader graph.

classref-introduction-group

## Description

A parameter represents a variable in the shader which is set externally,
i.e. from the `ShaderMaterial<class_ShaderMaterial>`. Parameters are
exposed as properties in the `ShaderMaterial<class_ShaderMaterial>` and
can be assigned from the Inspector or from a script.

classref-reftable-group

## Properties

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

## Enumerations

classref-enumeration

enum **Qualifier**: `🔗<enum_VisualShaderNodeParameter_Qualifier>`

classref-enumeration-constant

`Qualifier<enum_VisualShaderNodeParameter_Qualifier>` **QUAL\_NONE** =
`0`

The parameter will be tied to the `ShaderMaterial<class_ShaderMaterial>`
using this shader.

classref-enumeration-constant

`Qualifier<enum_VisualShaderNodeParameter_Qualifier>` **QUAL\_GLOBAL** =
`1`

The parameter will use a global value, defined in Project Settings.

classref-enumeration-constant

`Qualifier<enum_VisualShaderNodeParameter_Qualifier>` **QUAL\_INSTANCE**
= `2`

The parameter will be tied to the node with attached
`ShaderMaterial<class_ShaderMaterial>` using this shader.

classref-enumeration-constant

`Qualifier<enum_VisualShaderNodeParameter_Qualifier>` **QUAL\_MAX** =
`3`

Represents the size of the
`Qualifier<enum_VisualShaderNodeParameter_Qualifier>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **parameter\_name** = `""`
`🔗<class_VisualShaderNodeParameter_property_parameter_name>`

classref-property-setget

-   `void (No return value.)` **set\_parameter\_name**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_parameter\_name**()

Name of the parameter, by which it can be accessed through the
`ShaderMaterial<class_ShaderMaterial>` properties.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Qualifier<enum_VisualShaderNodeParameter_Qualifier>` **qualifier** =
`0` `🔗<class_VisualShaderNodeParameter_property_qualifier>`

classref-property-setget

-   `void (No return value.)` **set\_qualifier**(value:
    `Qualifier<enum_VisualShaderNodeParameter_Qualifier>`)
-   `Qualifier<enum_VisualShaderNodeParameter_Qualifier>`
    **get\_qualifier**()

Defines the scope of the parameter.
