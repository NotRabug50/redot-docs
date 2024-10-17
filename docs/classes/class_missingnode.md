github\_url  
hide

# MissingNode

**Inherits:** `Node<class_Node>` **&lt;** `Object<class_Object>`

An internal editor class intended for keeping the data of unrecognized
nodes.

classref-introduction-group

## Description

This is an internal editor class intended for keeping data of nodes of
unknown type (most likely this type was supplied by an extension that is
no longer loaded). It can't be manually instantiated or placed in a
scene.

\*\*Warning:\*\* Ignore missing nodes unless you know what you are
doing. Existing properties on a missing node can be freely modified in
code, regardless of the type they are intended to be.

classref-reftable-group

## Properties

<table>
<tbody>
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

`String<class_String>` **original\_class**
`🔗<class_MissingNode_property_original_class>`

classref-property-setget

-   `void (No return value.)` **set\_original\_class**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_original\_class**()

The name of the class this node was supposed to be (see
`Object.get_class<class_Object_method_get_class>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **original\_scene**
`🔗<class_MissingNode_property_original_scene>`

classref-property-setget

-   `void (No return value.)` **set\_original\_scene**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_original\_scene**()

Returns the path of the scene this node was instance of originally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **recording\_properties**
`🔗<class_MissingNode_property_recording_properties>`

classref-property-setget

-   `void (No return value.)` **set\_recording\_properties**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_recording\_properties**()

If `true`, allows new properties to be set along with existing ones. If
`false`, only existing properties' values can be set, and new properties
cannot be added.
