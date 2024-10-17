github\_url  
hide

# ScriptLanguageExtension

**Inherits:** `ScriptLanguage<class_ScriptLanguage>` **&lt;**
`Object<class_Object>`

There is currently no description for this class. Please help us by
`contributing one <doc_updating_the_class_reference>`!

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

enum **LookupResultType**:
`🔗<enum_ScriptLanguageExtension_LookupResultType>`

classref-enumeration-constant

`LookupResultType<enum_ScriptLanguageExtension_LookupResultType>`
**LOOKUP\_RESULT\_SCRIPT\_LOCATION** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`LookupResultType<enum_ScriptLanguageExtension_LookupResultType>`
**LOOKUP\_RESULT\_CLASS** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`LookupResultType<enum_ScriptLanguageExtension_LookupResultType>`
**LOOKUP\_RESULT\_CLASS\_CONSTANT** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`LookupResultType<enum_ScriptLanguageExtension_LookupResultType>`
**LOOKUP\_RESULT\_CLASS\_PROPERTY** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`LookupResultType<enum_ScriptLanguageExtension_LookupResultType>`
**LOOKUP\_RESULT\_CLASS\_METHOD** = `4`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`LookupResultType<enum_ScriptLanguageExtension_LookupResultType>`
**LOOKUP\_RESULT\_CLASS\_SIGNAL** = `5`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`LookupResultType<enum_ScriptLanguageExtension_LookupResultType>`
**LOOKUP\_RESULT\_CLASS\_ENUM** = `6`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`LookupResultType<enum_ScriptLanguageExtension_LookupResultType>`
**LOOKUP\_RESULT\_CLASS\_TBD\_GLOBALSCOPE** = `7`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`LookupResultType<enum_ScriptLanguageExtension_LookupResultType>`
**LOOKUP\_RESULT\_CLASS\_ANNOTATION** = `8`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`LookupResultType<enum_ScriptLanguageExtension_LookupResultType>`
**LOOKUP\_RESULT\_MAX** = `9`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CodeCompletionLocation**:
`🔗<enum_ScriptLanguageExtension_CodeCompletionLocation>`

classref-enumeration-constant

`CodeCompletionLocation<enum_ScriptLanguageExtension_CodeCompletionLocation>`
**LOCATION\_LOCAL** = `0`

The option is local to the location of the code completion query - e.g.
a local variable. Subsequent value of location represent options from
the outer class, the exact value represent how far they are (in terms of
inner classes).

classref-enumeration-constant

`CodeCompletionLocation<enum_ScriptLanguageExtension_CodeCompletionLocation>`
**LOCATION\_PARENT\_MASK** = `256`

The option is from the containing class or a parent class, relative to
the location of the code completion query. Perform a bitwise OR with the
class depth (e.g. `0` for the local class, `1` for the parent, `2` for
the grandparent, etc.) to store the depth of an option in the class or a
parent class.

classref-enumeration-constant

`CodeCompletionLocation<enum_ScriptLanguageExtension_CodeCompletionLocation>`
**LOCATION\_OTHER\_USER\_CODE** = `512`

The option is from user code which is not local and not in a derived
class (e.g. Autoload Singletons).

classref-enumeration-constant

`CodeCompletionLocation<enum_ScriptLanguageExtension_CodeCompletionLocation>`
**LOCATION\_OTHER** = `1024`

The option is from other engine code, not covered by the other enum
constants - e.g. built-in classes.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CodeCompletionKind**:
`🔗<enum_ScriptLanguageExtension_CodeCompletionKind>`

classref-enumeration-constant

`CodeCompletionKind<enum_ScriptLanguageExtension_CodeCompletionKind>`
**CODE\_COMPLETION\_KIND\_CLASS** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CodeCompletionKind<enum_ScriptLanguageExtension_CodeCompletionKind>`
**CODE\_COMPLETION\_KIND\_FUNCTION** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CodeCompletionKind<enum_ScriptLanguageExtension_CodeCompletionKind>`
**CODE\_COMPLETION\_KIND\_SIGNAL** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CodeCompletionKind<enum_ScriptLanguageExtension_CodeCompletionKind>`
**CODE\_COMPLETION\_KIND\_VARIABLE** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CodeCompletionKind<enum_ScriptLanguageExtension_CodeCompletionKind>`
**CODE\_COMPLETION\_KIND\_MEMBER** = `4`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CodeCompletionKind<enum_ScriptLanguageExtension_CodeCompletionKind>`
**CODE\_COMPLETION\_KIND\_ENUM** = `5`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CodeCompletionKind<enum_ScriptLanguageExtension_CodeCompletionKind>`
**CODE\_COMPLETION\_KIND\_CONSTANT** = `6`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CodeCompletionKind<enum_ScriptLanguageExtension_CodeCompletionKind>`
**CODE\_COMPLETION\_KIND\_NODE\_PATH** = `7`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CodeCompletionKind<enum_ScriptLanguageExtension_CodeCompletionKind>`
**CODE\_COMPLETION\_KIND\_FILE\_PATH** = `8`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CodeCompletionKind<enum_ScriptLanguageExtension_CodeCompletionKind>`
**CODE\_COMPLETION\_KIND\_PLAIN\_TEXT** = `9`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`CodeCompletionKind<enum_ScriptLanguageExtension_CodeCompletionKind>`
**CODE\_COMPLETION\_KIND\_MAX** = `10`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_add\_global\_constant**(name:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__add_global_constant>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_add\_named\_global\_constant**(name:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__add_named_global_constant>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_auto\_indent\_code**(code:
`String<class_String>`, from\_line: `int<class_int>`, to\_line:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__auto_indent_code>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_can\_inherit\_from\_file**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__can_inherit_from_file>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_can\_make\_function**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__can_make_function>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **\_complete\_code**(code:
`String<class_String>`, path: `String<class_String>`, owner:
`Object<class_Object>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__complete_code>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Object<class_Object>` **\_create\_script**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__create_script>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_debug\_get\_current\_stack\_info**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__debug_get_current_stack_info>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_debug\_get\_error**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__debug_get_error>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **\_debug\_get\_globals**(max\_subitems:
`int<class_int>`, max\_depth: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__debug_get_globals>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_debug\_get\_stack\_level\_count**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__debug_get_stack_level_count>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_debug\_get\_stack\_level\_function**(level:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__debug_get_stack_level_function>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void*` **\_debug\_get\_stack\_level\_instance**(level:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__debug_get_stack_level_instance>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_debug\_get\_stack\_level\_line**(level:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__debug_get_stack_level_line>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**\_debug\_get\_stack\_level\_locals**(level: `int<class_int>`,
max\_subitems: `int<class_int>`, max\_depth: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__debug_get_stack_level_locals>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**\_debug\_get\_stack\_level\_members**(level: `int<class_int>`,
max\_subitems: `int<class_int>`, max\_depth: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__debug_get_stack_level_members>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_debug\_get\_stack\_level\_source**(level:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__debug_get_stack_level_source>`

Returns the source associated with a given debug stack position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>`
**\_debug\_parse\_stack\_level\_expression**(level: `int<class_int>`,
expression: `String<class_String>`, max\_subitems: `int<class_int>`,
max\_depth: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__debug_parse_stack_level_expression>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_find\_function**(function: `String<class_String>`,
code: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__find_function>`

Returns the line where the function is defined in the code, or `-1` if
the function is not present.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_finish**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__finish>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_frame**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__frame>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_built\_in\_templates**(object: `StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_built_in_templates>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_comment\_delimiters**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_comment_delimiters>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_doc\_comment\_delimiters**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_doc_comment_delimiters>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_extension**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_extension>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **\_get\_global\_class\_name**(path:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_global_class_name>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_name>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_public\_annotations**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_public_annotations>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **\_get\_public\_constants**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_public_constants>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_public\_functions**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_public_functions>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_recognized\_extensions**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_recognized_extensions>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_reserved\_words**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_reserved_words>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_string\_delimiters**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_string_delimiters>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_type**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__get_type>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_handles\_global\_class\_type**(type:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__handles_global_class_type>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_has\_named\_classes**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__has_named_classes>`

**Deprecated:** This method is not called by the engine.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_init**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__init>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_control\_flow\_keyword**(keyword:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__is_control_flow_keyword>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_using\_templates**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__is_using_templates>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **\_lookup\_code**(code:
`String<class_String>`, symbol: `String<class_String>`, path:
`String<class_String>`, owner: `Object<class_Object>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__lookup_code>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_make\_function**(class\_name:
`String<class_String>`, function\_name: `String<class_String>`,
function\_args: `PackedStringArray<class_PackedStringArray>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__make_function>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Script<class_Script>` **\_make\_template**(template:
`String<class_String>`, class\_name: `String<class_String>`,
base\_class\_name: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__make_template>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**\_open\_in\_external\_editor**(script: `Script<class_Script>`, line:
`int<class_int>`, column: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__open_in_external_editor>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_overrides\_external\_editor**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__overrides_external_editor>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`ScriptNameCasing<enum_ScriptLanguage_ScriptNameCasing>`
**\_preferred\_file\_name\_casing**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__preferred_file_name_casing>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_profiling\_get\_accumulated\_data**(info\_array:
`ScriptLanguageExtensionProfilingInfo*`, info\_max: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__profiling_get_accumulated_data>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_profiling\_get\_frame\_data**(info\_array:
`ScriptLanguageExtensionProfilingInfo*`, info\_max: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__profiling_get_frame_data>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_profiling\_set\_save\_native\_calls**(enable: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__profiling_set_save_native_calls>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_profiling\_start**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__profiling_start>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_profiling\_stop**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__profiling_stop>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_reload\_all\_scripts**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__reload_all_scripts>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_reload\_scripts**(scripts:
`Array<class_Array>`, soft\_reload: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__reload_scripts>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_reload\_tool\_script**(script:
`Script<class_Script>`, soft\_reload: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__reload_tool_script>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_remove\_named\_global\_constant**(name:
`StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__remove_named_global_constant>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_supports\_builtin\_mode**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__supports_builtin_mode>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_supports\_documentation**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__supports_documentation>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_thread\_enter**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__thread_enter>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_thread\_exit**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_ScriptLanguageExtension_private_method__thread_exit>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **\_validate**(script:
`String<class_String>`, path: `String<class_String>`,
validate\_functions: `bool<class_bool>`, validate\_errors:
`bool<class_bool>`, validate\_warnings: `bool<class_bool>`,
validate\_safe\_lines: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__validate>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_validate\_path**(path:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptLanguageExtension_private_method__validate_path>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
