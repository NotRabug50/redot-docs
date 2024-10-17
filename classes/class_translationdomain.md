github\_url  
hide

# TranslationDomain

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

A self-contained collection of `Translation<class_Translation>`
resources.

classref-introduction-group

## Description

**TranslationDomain** is a self-contained collection of
`Translation<class_Translation>` resources. Translations can be added to
or removed from it.

If you're working with the main translation domain, it is more
convenient to use the wrap methods on
`TranslationServer<class_TranslationServer>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **pseudolocalization\_accents\_enabled** = `true`
`🔗<class_TranslationDomain_property_pseudolocalization_accents_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_pseudolocalization\_accents\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_pseudolocalization\_accents\_enabled**()

Replace all characters with their accented variants during
pseudolocalization.

\*\*Note:\*\* Updating this property does not automatically update texts
in the scene tree. Please propagate the
`MainLoop.NOTIFICATION_TRANSLATION_CHANGED<class_MainLoop_constant_NOTIFICATION_TRANSLATION_CHANGED>`
notification manually after you have finished modifying
pseudolocalization related options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **pseudolocalization\_double\_vowels\_enabled** =
`false`
`🔗<class_TranslationDomain_property_pseudolocalization_double_vowels_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_pseudolocalization\_double\_vowels\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>`
    **is\_pseudolocalization\_double\_vowels\_enabled**()

Double vowels in strings during pseudolocalization to simulate the
lengthening of text due to localization.

\*\*Note:\*\* Updating this property does not automatically update texts
in the scene tree. Please propagate the
`MainLoop.NOTIFICATION_TRANSLATION_CHANGED<class_MainLoop_constant_NOTIFICATION_TRANSLATION_CHANGED>`
notification manually after you have finished modifying
pseudolocalization related options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **pseudolocalization\_enabled** = `false`
`🔗<class_TranslationDomain_property_pseudolocalization_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_pseudolocalization\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_pseudolocalization\_enabled**()

If `true`, enables pseudolocalization for the project. This can be used
to spot untranslatable strings or layout issues that may occur once the
project is localized to languages that have longer strings than the
source language.

\*\*Note:\*\* Updating this property does not automatically update texts
in the scene tree. Please propagate the
`MainLoop.NOTIFICATION_TRANSLATION_CHANGED<class_MainLoop_constant_NOTIFICATION_TRANSLATION_CHANGED>`
notification manually after you have finished modifying
pseudolocalization related options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pseudolocalization\_expansion\_ratio** = `0.0`
`🔗<class_TranslationDomain_property_pseudolocalization_expansion_ratio>`

classref-property-setget

-   `void (No return value.)`
    **set\_pseudolocalization\_expansion\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pseudolocalization\_expansion\_ratio**()

The expansion ratio to use during pseudolocalization. A value of `0.3`
is sufficient for most practical purposes, and will increase the length
of each string by 30%.

\*\*Note:\*\* Updating this property does not automatically update texts
in the scene tree. Please propagate the
`MainLoop.NOTIFICATION_TRANSLATION_CHANGED<class_MainLoop_constant_NOTIFICATION_TRANSLATION_CHANGED>`
notification manually after you have finished modifying
pseudolocalization related options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **pseudolocalization\_fake\_bidi\_enabled** = `false`
`🔗<class_TranslationDomain_property_pseudolocalization_fake_bidi_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_pseudolocalization\_fake\_bidi\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_pseudolocalization\_fake\_bidi\_enabled**()

If `true`, emulate bidirectional (right-to-left) text when
pseudolocalization is enabled. This can be used to spot issues with RTL
layout and UI mirroring that will crop up if the project is localized to
RTL languages such as Arabic or Hebrew.

\*\*Note:\*\* Updating this property does not automatically update texts
in the scene tree. Please propagate the
`MainLoop.NOTIFICATION_TRANSLATION_CHANGED<class_MainLoop_constant_NOTIFICATION_TRANSLATION_CHANGED>`
notification manually after you have finished modifying
pseudolocalization related options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **pseudolocalization\_override\_enabled** = `false`
`🔗<class_TranslationDomain_property_pseudolocalization_override_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_pseudolocalization\_override\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_pseudolocalization\_override\_enabled**()

Replace all characters in the string with `*`. Useful for finding
non-localizable strings.

\*\*Note:\*\* Updating this property does not automatically update texts
in the scene tree. Please propagate the
`MainLoop.NOTIFICATION_TRANSLATION_CHANGED<class_MainLoop_constant_NOTIFICATION_TRANSLATION_CHANGED>`
notification manually after you have finished modifying
pseudolocalization related options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **pseudolocalization\_prefix** = `"["`
`🔗<class_TranslationDomain_property_pseudolocalization_prefix>`

classref-property-setget

-   `void (No return value.)` **set\_pseudolocalization\_prefix**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_pseudolocalization\_prefix**()

Prefix that will be prepended to the pseudolocalized string.

\*\*Note:\*\* Updating this property does not automatically update texts
in the scene tree. Please propagate the
`MainLoop.NOTIFICATION_TRANSLATION_CHANGED<class_MainLoop_constant_NOTIFICATION_TRANSLATION_CHANGED>`
notification manually after you have finished modifying
pseudolocalization related options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **pseudolocalization\_skip\_placeholders\_enabled** =
`true`
`🔗<class_TranslationDomain_property_pseudolocalization_skip_placeholders_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_pseudolocalization\_skip\_placeholders\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>`
    **is\_pseudolocalization\_skip\_placeholders\_enabled**()

Skip placeholders for string formatting like `%s` or `%f` during
pseudolocalization. Useful to identify strings which need additional
control characters to display correctly.

\*\*Note:\*\* Updating this property does not automatically update texts
in the scene tree. Please propagate the
`MainLoop.NOTIFICATION_TRANSLATION_CHANGED<class_MainLoop_constant_NOTIFICATION_TRANSLATION_CHANGED>`
notification manually after you have finished modifying
pseudolocalization related options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **pseudolocalization\_suffix** = `"]"`
`🔗<class_TranslationDomain_property_pseudolocalization_suffix>`

classref-property-setget

-   `void (No return value.)` **set\_pseudolocalization\_suffix**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_pseudolocalization\_suffix**()

Suffix that will be appended to the pseudolocalized string.

\*\*Note:\*\* Updating this property does not automatically update texts
in the scene tree. Please propagate the
`MainLoop.NOTIFICATION_TRANSLATION_CHANGED<class_MainLoop_constant_NOTIFICATION_TRANSLATION_CHANGED>`
notification manually after you have finished modifying
pseudolocalization related options.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_translation**(translation:
`Translation<class_Translation>`)
`🔗<class_TranslationDomain_method_add_translation>`

Adds a translation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_TranslationDomain_method_clear>`

Removes all translations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Translation<class_Translation>` **get\_translation\_object**(locale:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationDomain_method_get_translation_object>`

Returns the `Translation<class_Translation>` instance that best matches
`locale`. Returns `null` if there are no matches.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **pseudolocalize**(message:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationDomain_method_pseudolocalize>`

Returns the pseudolocalized string based on the `message` passed in.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_translation**(translation:
`Translation<class_Translation>`)
`🔗<class_TranslationDomain_method_remove_translation>`

Removes the given translation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **translate**(message:
`StringName<class_StringName>`, context: `StringName<class_StringName>`
= &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationDomain_method_translate>`

Returns the current locale's translation for the given message and
context.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **translate\_plural**(message:
`StringName<class_StringName>`, message\_plural:
`StringName<class_StringName>`, n: `int<class_int>`, context:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TranslationDomain_method_translate_plural>`

Returns the current locale's translation for the given message, plural
message and context.

The number `n` is the number or quantity of the plural object. It will
be used to guide the translation system to fetch the correct plural form
for the selected language.
