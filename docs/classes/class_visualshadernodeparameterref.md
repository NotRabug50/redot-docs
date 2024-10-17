github\_url  
hide

# VisualShaderNodeParameterRef

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A reference to an existing
`VisualShaderNodeParameter<class_VisualShaderNodeParameter>`.

classref-introduction-group

## Description

Creating a reference to a
`VisualShaderNodeParameter<class_VisualShaderNodeParameter>` allows you
to reuse this parameter in different shaders or shader stages easily.

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **parameter\_name** = `"[None]"`
`🔗<class_VisualShaderNodeParameterRef_property_parameter_name>`

classref-property-setget

-   `void (No return value.)` **set\_parameter\_name**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_parameter\_name**()

The name of the parameter which this reference points to.
