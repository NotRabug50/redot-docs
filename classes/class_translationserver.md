github\_url  
hide

# TranslationServer

**Inherits:** `Object<class_Object>`

The server responsible for language translations.

classref-introduction-group

## Description

The translation server is the API backend that manages all language
translations.

Translations are stored in
`TranslationDomain<class_TranslationDomain>`s, which can be accessed by
name. The most commonly used translation domain is the main translation
domain. It always exists and can be accessed using an empty
`StringName<class_StringName>`. The translation server provides wrapper
methods for accessing the main translation domain directly, without
having to fetch the translation domain first. Custom translation domains
are mainly for advanced usages like editor plugins. Names starting with
`godot.` are reserved for engine internals.

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

## Property Descriptions

classref-property

`bool<class_bool>` **pseudolocalization\_enabled** = `false`
`🔗<class_TranslationServer_property_pseudolocalization_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_pseudolocalization\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_pseudolocalization\_enabled**()

If `true`, enables the use of pseudolocalization on the main translation
domain. See
`ProjectSettings.internationalization/pseudolocalization/use_pseudolocalization<class_ProjectSettings_property_internationalization/pseudolocalization/use_pseudolocalization>`
for details.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_translation**(translation:
`Translation<class_Translation>`)
`🔗<class_TranslationServer_method_add_translation>`

Adds a translation to the main translation domain.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_TranslationServer_method_clear>`

Removes all translations from the main translation domain.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **compare\_locales**(locale\_a: `String<class_String>`,
locale\_b: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_compare_locales>`

Compares two locales and returns a similarity score between `0` (no
match) and `10` (full match).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_all\_countries**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_get_all_countries>`

Returns an array of known country codes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_all\_languages**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_get_all_languages>`

Returns array of known language codes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_all\_scripts**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_get_all_scripts>`

Returns an array of known script codes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_country\_name**(country:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_get_country_name>`

Returns a readable country name for the `country` code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_language\_name**(language:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_get_language_name>`

Returns a readable language name for the `language` code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_loaded\_locales**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_get_loaded_locales>`

Returns an array of all loaded locales of the project.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_locale**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_get_locale>`

Returns the current locale of the project.

See also `OS.get_locale<class_OS_method_get_locale>` and
`OS.get_locale_language<class_OS_method_get_locale_language>` to query
the locale of the user system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_locale\_name**(locale:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_get_locale_name>`

Returns a locale's language and its variant (e.g. `"en_US"` would return
`"English (United States)"`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`TranslationDomain<class_TranslationDomain>`
**get\_or\_add\_domain**(domain: `StringName<class_StringName>`)
`🔗<class_TranslationServer_method_get_or_add_domain>`

Returns the translation domain with the specified name. An empty
translation domain will be created and added if it does not exist.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_script\_name**(script:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_get_script_name>`

Returns a readable script name for the `script` code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_tool\_locale**()
`🔗<class_TranslationServer_method_get_tool_locale>`

Returns the current locale of the editor.

\*\*Note:\*\* When called from an exported project returns the same
value as `get_locale<class_TranslationServer_method_get_locale>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Translation<class_Translation>` **get\_translation\_object**(locale:
`String<class_String>`)
`🔗<class_TranslationServer_method_get_translation_object>`

Returns the `Translation<class_Translation>` instance that best matches
`locale` in the main translation domain. Returns `null` if there are no
matches.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_domain**(domain:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_has_domain>`

Returns `true` if a translation domain with the specified name exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **pseudolocalize**(message:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_pseudolocalize>`

Returns the pseudolocalized string based on the `message` passed in.

\*\*Note:\*\* This method always uses the main translation domain.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reload\_pseudolocalization**()
`🔗<class_TranslationServer_method_reload_pseudolocalization>`

Reparses the pseudolocalization options and reloads the translation for
the main translation domain.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_domain**(domain:
`StringName<class_StringName>`)
`🔗<class_TranslationServer_method_remove_domain>`

Removes the translation domain with the specified name.

\*\*Note:\*\* Trying to remove the main translation domain is an error.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_translation**(translation:
`Translation<class_Translation>`)
`🔗<class_TranslationServer_method_remove_translation>`

Removes the given translation from the main translation domain.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_locale**(locale:
`String<class_String>`) `🔗<class_TranslationServer_method_set_locale>`

Sets the locale of the project. The `locale` string will be standardized
to match known locales (e.g. `en-US` would be matched to `en_US`).

If translations have been loaded beforehand for the new locale, they
will be applied.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **standardize\_locale**(locale:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_standardize_locale>`

Returns a `locale` string standardized to match known locales (e.g.
`en-US` would be matched to `en_US`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **translate**(message:
`StringName<class_StringName>`, context: `StringName<class_StringName>`
= &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_translate>`

Returns the current locale's translation for the given message and
context.

\*\*Note:\*\* This method always uses the main translation domain.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **translate\_plural**(message:
`StringName<class_StringName>`, plural\_message:
`StringName<class_StringName>`, n: `int<class_int>`, context:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationServer_method_translate_plural>`

Returns the current locale's translation for the given message, plural
message and context.

The number `n` is the number or quantity of the plural object. It will
be used to guide the translation system to fetch the correct plural form
for the selected language.

\*\*Note:\*\* This method always uses the main translation domain.
