github\_url  
hide

# EncodedObjectAsID

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Holds a reference to an `Object<class_Object>`'s instance ID.

classref-introduction-group

## Description

Utility class which holds a reference to the internal identifier of an
`Object<class_Object>` instance, as given by
`Object.get_instance_id<class_Object_method_get_instance_id>`. This ID
can then be used to retrieve the object instance with
`@GlobalScope.instance_from_id<class_@GlobalScope_method_instance_from_id>`.

This class is used internally by the editor inspector and script
debugger, but can also be used in plugins to pass and display objects as
their IDs.

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

`int<class_int>` **object\_id** = `0`
`🔗<class_EncodedObjectAsID_property_object_id>`

classref-property-setget

-   `void (No return value.)` **set\_object\_id**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_object\_id**()

The `Object<class_Object>` identifier stored in this
**EncodedObjectAsID** instance. The object instance can be retrieved
with
`@GlobalScope.instance_from_id<class_@GlobalScope_method_instance_from_id>`.
