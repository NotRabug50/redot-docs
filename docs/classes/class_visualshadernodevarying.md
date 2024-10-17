github\_url  
hide

# VisualShaderNodeVarying

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`VisualShaderNodeVaryingGetter<class_VisualShaderNodeVaryingGetter>`,
`VisualShaderNodeVaryingSetter<class_VisualShaderNodeVaryingSetter>`

A visual shader node that represents a "varying" shader value.

classref-introduction-group

## Description

Varying values are shader variables that can be passed between shader
functions, e.g. from Vertex shader to Fragment shader.

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

`String<class_String>` **varying\_name** = `"[None]"`
`🔗<class_VisualShaderNodeVarying_property_varying_name>`

classref-property-setget

-   `void (No return value.)` **set\_varying\_name**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_varying\_name**()

Name of the variable. Must be unique.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VaryingType<enum_VisualShader_VaryingType>` **varying\_type** = `0`
`🔗<class_VisualShaderNodeVarying_property_varying_type>`

classref-property-setget

-   `void (No return value.)` **set\_varying\_type**(value:
    `VaryingType<enum_VisualShader_VaryingType>`)
-   `VaryingType<enum_VisualShader_VaryingType>`
    **get\_varying\_type**()

Type of the variable. Determines where the variable can be accessed.
