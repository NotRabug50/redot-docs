github\_url  
hide

# VisualShaderNodeUIntParameter

**Inherits:**
`VisualShaderNodeParameter<class_VisualShaderNodeParameter>` **&lt;**
`VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A visual shader node for shader parameter (uniform) of type unsigned
`int<class_int>`.

classref-introduction-group

## Description

A `VisualShaderNodeParameter<class_VisualShaderNodeParameter>` of type
unsigned `int<class_int>`. Offers additional customization for range of
accepted values.

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

`int<class_int>` **default\_value** = `0`
`🔗<class_VisualShaderNodeUIntParameter_property_default_value>`

classref-property-setget

-   `void (No return value.)` **set\_default\_value**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_default\_value**()

Default value of this parameter, which will be used if not set
externally.
`default_value_enabled<class_VisualShaderNodeUIntParameter_property_default_value_enabled>`
must be enabled; defaults to `0` otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **default\_value\_enabled** = `false`
`🔗<class_VisualShaderNodeUIntParameter_property_default_value_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_default\_value\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_default\_value\_enabled**()

If `true`, the node will have a custom default value.
