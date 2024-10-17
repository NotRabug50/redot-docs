github\_url  
hide

# Translation

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `OptimizedTranslation<class_OptimizedTranslation>`

A language translation that maps a collection of strings to their
individual translations.

classref-introduction-group

## Description

**Translation**s are resources that can be loaded and unloaded on
demand. They map a collection of strings to their individual
translations, and they also provide convenience methods for
pluralization.

classref-introduction-group

## Tutorials

-   `Internationalizing games <../tutorials/i18n/internationalizing_games>`
-   `Locales <../tutorials/i18n/locales>`

classref-reftable-group

## Properties

<table>
<tbody>
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

## Property Descriptions

classref-property

`String<class_String>` **locale** = `"en"`
`🔗<class_Translation_property_locale>`

classref-property-setget

-   `void (No return value.)` **set\_locale**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_locale**()

The locale of the translation.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`StringName<class_StringName>` **\_get\_message**(src\_message:
`StringName<class_StringName>`, context: `StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Translation_private_method__get_message>`

Virtual method to override
`get_message<class_Translation_method_get_message>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **\_get\_plural\_message**(src\_message:
`StringName<class_StringName>`, src\_plural\_message:
`StringName<class_StringName>`, n: `int<class_int>`, context:
`StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Translation_private_method__get_plural_message>`

Virtual method to override
`get_plural_message<class_Translation_method_get_plural_message>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_message**(src\_message:
`StringName<class_StringName>`, xlated\_message:
`StringName<class_StringName>`, context: `StringName<class_StringName>`
= &"") `🔗<class_Translation_method_add_message>`

Adds a message if nonexistent, followed by its translation.

An additional context could be used to specify the translation context
or differentiate polysemic words.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_plural\_message**(src\_message:
`StringName<class_StringName>`, xlated\_messages:
`PackedStringArray<class_PackedStringArray>`, context:
`StringName<class_StringName>` = &"")
`🔗<class_Translation_method_add_plural_message>`

Adds a message involving plural translation if nonexistent, followed by
its translation.

An additional context could be used to specify the translation context
or differentiate polysemic words.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase\_message**(src\_message:
`StringName<class_StringName>`, context: `StringName<class_StringName>`
= &"") `🔗<class_Translation_method_erase_message>`

Erases a message.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_message**(src\_message:
`StringName<class_StringName>`, context: `StringName<class_StringName>`
= &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Translation_method_get_message>`

Returns a message's translation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_message\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Translation_method_get_message_count>`

Returns the number of existing messages.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_message\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Translation_method_get_message_list>`

Returns all the messages (keys).

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_plural\_message**(src\_message:
`StringName<class_StringName>`, src\_plural\_message:
`StringName<class_StringName>`, n: `int<class_int>`, context:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Translation_method_get_plural_message>`

Returns a message's translation involving plurals.

The number `n` is the number or quantity of the plural object. It will
be used to guide the translation system to fetch the correct plural form
for the selected language.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_translated\_message\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Translation_method_get_translated_message_list>`

Returns all the messages (translated text).
