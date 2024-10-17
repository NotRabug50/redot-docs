github\_url  
hide

# OpenXRIPBinding

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Defines a binding between an `OpenXRAction<class_OpenXRAction>` and an
XR input or output.

classref-introduction-group

## Description

This binding resource binds an `OpenXRAction<class_OpenXRAction>` to
inputs or outputs. As most controllers have left hand and right versions
that are handled by the same interaction profile we can specify multiple
bindings. For instance an action "Fire" could be bound to both
"/user/hand/left/input/trigger" and "/user/hand/right/input/trigger".

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

`OpenXRAction<class_OpenXRAction>` **action**
`🔗<class_OpenXRIPBinding_property_action>`

classref-property-setget

-   `void (No return value.)` **set\_action**(value:
    `OpenXRAction<class_OpenXRAction>`)
-   `OpenXRAction<class_OpenXRAction>` **get\_action**()

`OpenXRAction<class_OpenXRAction>` that is bound to these paths.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedStringArray<class_PackedStringArray>` **paths** =
`PackedStringArray()` `🔗<class_OpenXRIPBinding_property_paths>`

classref-property-setget

-   `void (No return value.)` **set\_paths**(value:
    `PackedStringArray<class_PackedStringArray>`)
-   `PackedStringArray<class_PackedStringArray>` **get\_paths**()

Paths that define the inputs or outputs bound on the device.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_path**(path: `String<class_String>`)
`🔗<class_OpenXRIPBinding_method_add_path>`

Add an input/output path to this binding.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_path\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRIPBinding_method_get_path_count>`

Get the number of input/output paths in this binding.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_path**(path: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRIPBinding_method_has_path>`

Returns `true` if this input/output path is part of this binding.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_path**(path: `String<class_String>`)
`🔗<class_OpenXRIPBinding_method_remove_path>`

Removes this input/output path from this binding.
