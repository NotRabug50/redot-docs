github\_url  
hide

# ResourceUID

**Inherits:** `Object<class_Object>`

A singleton that manages the unique identifiers of all resources within
a project.

classref-introduction-group

## Description

Resource UIDs (Unique IDentifiers) allow the engine to keep references
between resources intact, even if files are renamed or moved. They can
be accessed with `uid://`.

\*\*ResourceUID\*\* keeps track of all registered resource UIDs in a
project, generates new UIDs, and converts between their string and
integer representations.

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

## Constants

classref-constant

**INVALID\_ID** = `-1` `🔗<class_ResourceUID_constant_INVALID_ID>`

The value to use for an invalid UID, for example if the resource could
not be loaded.

Its text representation is `uid://<invalid>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_id**(id: `int<class_int>`, path:
`String<class_String>`) `🔗<class_ResourceUID_method_add_id>`

Adds a new UID value which is mapped to the given resource path.

Fails with an error if the UID already exists, so be sure to check
`has_id<class_ResourceUID_method_has_id>` beforehand, or use
`set_id<class_ResourceUID_method_set_id>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **create\_id**()
`🔗<class_ResourceUID_method_create_id>`

Generates a random resource UID which is guaranteed to be unique within
the list of currently loaded UIDs.

In order for this UID to be registered, you must call
`add_id<class_ResourceUID_method_add_id>` or
`set_id<class_ResourceUID_method_set_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_id\_path**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceUID_method_get_id_path>`

Returns the path that the given UID value refers to.

Fails with an error if the UID does not exist, so be sure to check
`has_id<class_ResourceUID_method_has_id>` beforehand.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_id**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceUID_method_has_id>`

Returns whether the given UID value is known to the cache.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **id\_to\_text**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceUID_method_id_to_text>`

Converts the given UID to a `uid://` string value.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_id**(id: `int<class_int>`)
`🔗<class_ResourceUID_method_remove_id>`

Removes a loaded UID value from the cache.

Fails with an error if the UID does not exist, so be sure to check
`has_id<class_ResourceUID_method_has_id>` beforehand.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_id**(id: `int<class_int>`, path:
`String<class_String>`) `🔗<class_ResourceUID_method_set_id>`

Updates the resource path of an existing UID.

Fails with an error if the UID does not exist, so be sure to check
`has_id<class_ResourceUID_method_has_id>` beforehand, or use
`add_id<class_ResourceUID_method_add_id>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **text\_to\_id**(text\_id: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceUID_method_text_to_id>`

Extracts the UID value from the given `uid://` string.
