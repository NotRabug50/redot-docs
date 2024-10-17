github\_url  
hide

# VisualShaderNodeVec4Parameter

**Inherits:**
`VisualShaderNodeParameter<class_VisualShaderNodeParameter>` **&lt;**
`VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A 4D vector parameter to be used within the visual shader graph.

classref-introduction-group

## Description

Translated to `uniform vec4` in the shader language.

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

## Property Descriptions

classref-property

`Vector4<class_Vector4>` **default\_value** = `Vector4(0, 0, 0, 0)`
`🔗<class_VisualShaderNodeVec4Parameter_property_default_value>`

classref-property-setget

-   `void (No return value.)` **set\_default\_value**(value:
    `Vector4<class_Vector4>`)
-   `Vector4<class_Vector4>` **get\_default\_value**()

A default value to be assigned within the shader.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **default\_value\_enabled** = `false`
`🔗<class_VisualShaderNodeVec4Parameter_property_default_value_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_default\_value\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_default\_value\_enabled**()

Enables usage of the
`default_value<class_VisualShaderNodeVec4Parameter_property_default_value>`.
