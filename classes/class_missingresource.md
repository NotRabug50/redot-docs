github\_url  
hide

# MissingResource

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

An internal editor class intended for keeping the data of unrecognized
resources.

classref-introduction-group

## Description

This is an internal editor class intended for keeping data of resources
of unknown type (most likely this type was supplied by an extension that
is no longer loaded). It can't be manually instantiated or placed in a
scene.

\*\*Warning:\*\* Ignore missing resources unless you know what you are
doing. Existing properties on a missing resource can be freely modified
in code, regardless of the type they are intended to be.

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

`String<class_String>` **original\_class**
`🔗<class_MissingResource_property_original_class>`

classref-property-setget

-   `void (No return value.)` **set\_original\_class**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_original\_class**()

The name of the class this resource was supposed to be (see
`Object.get_class<class_Object_method_get_class>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **recording\_properties**
`🔗<class_MissingResource_property_recording_properties>`

classref-property-setget

-   `void (No return value.)` **set\_recording\_properties**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_recording\_properties**()

If set to `true`, allows new properties to be added on top of the
existing ones with `Object.set<class_Object_method_set>`.
