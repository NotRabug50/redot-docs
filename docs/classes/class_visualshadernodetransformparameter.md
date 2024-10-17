github\_url  
hide

# VisualShaderNodeTransformParameter

**Inherits:**
`VisualShaderNodeParameter<class_VisualShaderNodeParameter>` **&lt;**
`VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A `Transform3D<class_Transform3D>` parameter for use within the visual
shader graph.

classref-introduction-group

## Description

Translated to `uniform mat4` in the shader language.

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

`Transform3D<class_Transform3D>` **default\_value** =
`Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0)`
`🔗<class_VisualShaderNodeTransformParameter_property_default_value>`

classref-property-setget

-   `void (No return value.)` **set\_default\_value**(value:
    `Transform3D<class_Transform3D>`)
-   `Transform3D<class_Transform3D>` **get\_default\_value**()

A default value to be assigned within the shader.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **default\_value\_enabled** = `false`
`🔗<class_VisualShaderNodeTransformParameter_property_default_value_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_default\_value\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_default\_value\_enabled**()

Enables usage of the
`default_value<class_VisualShaderNodeTransformParameter_property_default_value>`.
