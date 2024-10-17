github\_url  
hide

# VisualShaderNodeColorParameter

**Inherits:**
`VisualShaderNodeParameter<class_VisualShaderNodeParameter>` **&lt;**
`VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A `Color<class_Color>` parameter to be used within the visual shader
graph.

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

`Color<class_Color>` **default\_value** = `Color(1, 1, 1, 1)`
`🔗<class_VisualShaderNodeColorParameter_property_default_value>`

classref-property-setget

-   `void (No return value.)` **set\_default\_value**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_default\_value**()

A default value to be assigned within the shader.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **default\_value\_enabled** = `false`
`🔗<class_VisualShaderNodeColorParameter_property_default_value_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_default\_value\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_default\_value\_enabled**()

Enables usage of the
`default_value<class_VisualShaderNodeColorParameter_property_default_value>`.
