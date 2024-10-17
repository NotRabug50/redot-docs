github\_url  
hide

# RDPipelineSpecializationConstant

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Pipeline specialization constant (used by
`RenderingDevice<class_RenderingDevice>`).

classref-introduction-group

## Description

A *specialization constant* is a way to create additional variants of
shaders without actually increasing the number of shader versions that
are compiled. This allows improving performance by reducing the number
of shader versions and reducing `if` branching, while still allowing
shaders to be flexible for different use cases.

This object is used by `RenderingDevice<class_RenderingDevice>`.

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

`int<class_int>` **constant\_id** = `0`
`🔗<class_RDPipelineSpecializationConstant_property_constant_id>`

classref-property-setget

-   `void (No return value.)` **set\_constant\_id**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_constant\_id**()

The identifier of the specialization constant. This is a value starting
from `0` and that increments for every different specialization constant
for a given shader.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Variant<class_Variant>` **value**
`🔗<class_RDPipelineSpecializationConstant_property_value>`

classref-property-setget

-   `void (No return value.)` **set\_value**(value:
    `Variant<class_Variant>`)
-   `Variant<class_Variant>` **get\_value**()

The specialization constant's value. Only `bool<class_bool>`,
`int<class_int>` and `float<class_float>` types are valid for
specialization constants.
