github\_url  
hide

# ClassDB

**Inherits:** `Object<class_Object>`

A class information repository.

classref-introduction-group

## Description

Provides access to metadata stored for every available class.

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

## Enumerations

classref-enumeration

enum **APIType**: `🔗<enum_ClassDB_APIType>`

classref-enumeration-constant

`APIType<enum_ClassDB_APIType>` **API\_CORE** = `0`

Native Core class type.

classref-enumeration-constant

`APIType<enum_ClassDB_APIType>` **API\_EDITOR** = `1`

Native Editor class type.

classref-enumeration-constant

`APIType<enum_ClassDB_APIType>` **API\_EXTENSION** = `2`

GDExtension class type.

classref-enumeration-constant

`APIType<enum_ClassDB_APIType>` **API\_EDITOR\_EXTENSION** = `3`

GDExtension Editor class type.

classref-enumeration-constant

`APIType<enum_ClassDB_APIType>` **API\_NONE** = `4`

Unknown class type.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **can\_instantiate**(class:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_can_instantiate>`

Returns `true` if objects can be instantiated from the specified
`class`, otherwise returns `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **class\_call\_static\_method**(class:
`StringName<class_StringName>`, method: `StringName<class_StringName>`,
...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_ClassDB_method_class_call_static_method>`

Calls a static method on a class.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **class\_exists**(class:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_exists>`

Returns whether the specified `class` is available or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`APIType<enum_ClassDB_APIType>` **class\_get\_api\_type**(class:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_api_type>`

Returns the API type of `class`. See `APIType<enum_ClassDB_APIType>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**class\_get\_enum\_constants**(class: `StringName<class_StringName>`,
enum: `StringName<class_StringName>`, no\_inheritance:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_enum_constants>`

Returns an array with all the keys in `enum` of `class` or its ancestry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**class\_get\_enum\_list**(class: `StringName<class_StringName>`,
no\_inheritance: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_enum_list>`

Returns an array with all the enums of `class` or its ancestry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **class\_get\_integer\_constant**(class:
`StringName<class_StringName>`, name: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_integer_constant>`

Returns the value of the integer constant `name` of `class` or its
ancestry. Always returns 0 when the constant could not be found.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>`
**class\_get\_integer\_constant\_enum**(class:
`StringName<class_StringName>`, name: `StringName<class_StringName>`,
no\_inheritance: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_integer_constant_enum>`

Returns which enum the integer constant `name` of `class` or its
ancestry belongs to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**class\_get\_integer\_constant\_list**(class:
`StringName<class_StringName>`, no\_inheritance: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_integer_constant_list>`

Returns an array with the names all the integer constants of `class` or
its ancestry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **class\_get\_method\_argument\_count**(class:
`StringName<class_StringName>`, method: `StringName<class_StringName>`,
no\_inheritance: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_method_argument_count>`

Returns the number of arguments of the method `method` of `class` or its
ancestry if `no_inheritance` is `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**class\_get\_method\_list**(class: `StringName<class_StringName>`,
no\_inheritance: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_method_list>`

Returns an array with all the methods of `class` or its ancestry if
`no_inheritance` is `false`. Every element of the array is a
`Dictionary<class_Dictionary>` with the following keys: `args`,
`default_args`, `flags`, `id`, `name`,
`return: (class_name, hint, hint_string, name, type, usage)`.

\*\*Note:\*\* In exported release builds the debug info is not
available, so the returned dictionaries will contain only method names.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **class\_get\_property**(object:
`Object<class_Object>`, property: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_property>`

Returns the value of `property` of `object` or its ancestry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **class\_get\_property\_default\_value**(class:
`StringName<class_StringName>`, property:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_property_default_value>`

Returns the default value of `property` of `class` or its ancestor
classes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **class\_get\_property\_getter**(class:
`StringName<class_StringName>`, property:
`StringName<class_StringName>`)
`🔗<class_ClassDB_method_class_get_property_getter>`

Returns the getter method name of `property` of `class`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**class\_get\_property\_list**(class: `StringName<class_StringName>`,
no\_inheritance: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_property_list>`

Returns an array with all the properties of `class` or its ancestry if
`no_inheritance` is `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **class\_get\_property\_setter**(class:
`StringName<class_StringName>`, property:
`StringName<class_StringName>`)
`🔗<class_ClassDB_method_class_get_property_setter>`

Returns the setter method name of `property` of `class`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **class\_get\_signal**(class:
`StringName<class_StringName>`, signal: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_signal>`

Returns the `signal` data of `class` or its ancestry. The returned value
is a `Dictionary<class_Dictionary>` with the following keys: `args`,
`default_args`, `flags`, `id`, `name`,
`return: (class_name, hint, hint_string, name, type, usage)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**class\_get\_signal\_list**(class: `StringName<class_StringName>`,
no\_inheritance: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_get_signal_list>`

Returns an array with all the signals of `class` or its ancestry if
`no_inheritance` is `false`. Every element of the array is a
`Dictionary<class_Dictionary>` as described in
`class_get_signal<class_ClassDB_method_class_get_signal>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **class\_has\_enum**(class:
`StringName<class_StringName>`, name: `StringName<class_StringName>`,
no\_inheritance: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_has_enum>`

Returns whether `class` or its ancestry has an enum called `name` or
not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **class\_has\_integer\_constant**(class:
`StringName<class_StringName>`, name: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_has_integer_constant>`

Returns whether `class` or its ancestry has an integer constant called
`name` or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **class\_has\_method**(class:
`StringName<class_StringName>`, method: `StringName<class_StringName>`,
no\_inheritance: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_has_method>`

Returns whether `class` (or its ancestry if `no_inheritance` is `false`)
has a method called `method` or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **class\_has\_signal**(class:
`StringName<class_StringName>`, signal: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_has_signal>`

Returns whether `class` or its ancestry has a signal called `signal` or
not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **class\_set\_property**(object:
`Object<class_Object>`, property: `StringName<class_StringName>`, value:
`Variant<class_Variant>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_class_set_property>`

Sets `property` value of `object` to `value`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_class\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_get_class_list>`

Returns the names of all the classes available.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_inheriters\_from\_class**(class: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_get_inheriters_from_class>`

Returns the names of all the classes that directly or indirectly inherit
from `class`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_parent\_class**(class:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_get_parent_class>`

Returns the parent class of `class`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **instantiate**(class:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_instantiate>`

Creates an instance of `class`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_class\_enabled**(class:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_is_class_enabled>`

Returns whether this `class` is enabled or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_class\_enum\_bitfield**(class:
`StringName<class_StringName>`, enum: `StringName<class_StringName>`,
no\_inheritance: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_is_class_enum_bitfield>`

Returns whether `class` (or its ancestor classes if `no_inheritance` is
`false`) has an enum called `enum` that is a bitfield.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_parent\_class**(class:
`StringName<class_StringName>`, inherits:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ClassDB_method_is_parent_class>`

Returns whether `inherits` is an ancestor of `class` or not.
