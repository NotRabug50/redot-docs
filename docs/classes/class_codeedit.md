github\_url  
hide

# CodeEdit

**Inherits:** `TextEdit<class_TextEdit>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

A multiline text editor designed for editing code.

classref-introduction-group

## Description

CodeEdit is a specialized `TextEdit<class_TextEdit>` designed for
editing plain text code files. It has many features commonly found in
code editors such as line numbers, line folding, code completion, indent
management, and string/comment management.

\*\*Note:\*\* Regardless of locale, **CodeEdit** will by default always
use left-to-right text direction to correctly display source code.

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

classref-reftable-group

## Theme Properties

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**breakpoint\_toggled**(line: `int<class_int>`)
`🔗<class_CodeEdit_signal_breakpoint_toggled>`

Emitted when a breakpoint is added or removed from a line. If the line
is moved via backspace a removed is emitted at the old line.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**code\_completion\_requested**()
`🔗<class_CodeEdit_signal_code_completion_requested>`

Emitted when the user requests code completion.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**symbol\_lookup**(symbol: `String<class_String>`, line:
`int<class_int>`, column: `int<class_int>`)
`🔗<class_CodeEdit_signal_symbol_lookup>`

Emitted when the user has clicked on a valid symbol.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**symbol\_validate**(symbol: `String<class_String>`)
`🔗<class_CodeEdit_signal_symbol_validate>`

Emitted when the user hovers over a symbol. The symbol should be
validated and responded to, by calling
`set_symbol_lookup_word_as_valid<class_CodeEdit_method_set_symbol_lookup_word_as_valid>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **CodeCompletionKind**: `🔗<enum_CodeEdit_CodeCompletionKind>`

classref-enumeration-constant

`CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>` **KIND\_CLASS** =
`0`

Marks the option as a class.

classref-enumeration-constant

`CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>`
**KIND\_FUNCTION** = `1`

Marks the option as a function.

classref-enumeration-constant

`CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>` **KIND\_SIGNAL**
= `2`

Marks the option as a Godot signal.

classref-enumeration-constant

`CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>`
**KIND\_VARIABLE** = `3`

Marks the option as a variable.

classref-enumeration-constant

`CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>` **KIND\_MEMBER**
= `4`

Marks the option as a member.

classref-enumeration-constant

`CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>` **KIND\_ENUM** =
`5`

Marks the option as an enum entry.

classref-enumeration-constant

`CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>`
**KIND\_CONSTANT** = `6`

Marks the option as a constant.

classref-enumeration-constant

`CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>`
**KIND\_NODE\_PATH** = `7`

Marks the option as a Godot node path.

classref-enumeration-constant

`CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>`
**KIND\_FILE\_PATH** = `8`

Marks the option as a file path.

classref-enumeration-constant

`CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>`
**KIND\_PLAIN\_TEXT** = `9`

Marks the option as unclassified or plain text.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CodeCompletionLocation**:
`🔗<enum_CodeEdit_CodeCompletionLocation>`

classref-enumeration-constant

`CodeCompletionLocation<enum_CodeEdit_CodeCompletionLocation>`
**LOCATION\_LOCAL** = `0`

The option is local to the location of the code completion query - e.g.
a local variable. Subsequent value of location represent options from
the outer class, the exact value represent how far they are (in terms of
inner classes).

classref-enumeration-constant

`CodeCompletionLocation<enum_CodeEdit_CodeCompletionLocation>`
**LOCATION\_PARENT\_MASK** = `256`

The option is from the containing class or a parent class, relative to
the location of the code completion query. Perform a bitwise OR with the
class depth (e.g. `0` for the local class, `1` for the parent, `2` for
the grandparent, etc.) to store the depth of an option in the class or a
parent class.

classref-enumeration-constant

`CodeCompletionLocation<enum_CodeEdit_CodeCompletionLocation>`
**LOCATION\_OTHER\_USER\_CODE** = `512`

The option is from user code which is not local and not in a derived
class (e.g. Autoload Singletons).

classref-enumeration-constant

`CodeCompletionLocation<enum_CodeEdit_CodeCompletionLocation>`
**LOCATION\_OTHER** = `1024`

The option is from other engine code, not covered by the other enum
constants - e.g. built-in classes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **auto\_brace\_completion\_enabled** = `false`
`🔗<class_CodeEdit_property_auto_brace_completion_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_auto\_brace\_completion\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_auto\_brace\_completion\_enabled**()

Sets whether brace pairs should be autocompleted.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **auto\_brace\_completion\_highlight\_matching** =
`false`
`🔗<class_CodeEdit_property_auto_brace_completion_highlight_matching>`

classref-property-setget

-   `void (No return value.)`
    **set\_highlight\_matching\_braces\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_highlight\_matching\_braces\_enabled**()

Highlight mismatching brace pairs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Dictionary<class_Dictionary>` **auto\_brace\_completion\_pairs** =
`{ "\"": "\"", "'": "'", "(": ")", "[": "]", "{": "}" }`
`🔗<class_CodeEdit_property_auto_brace_completion_pairs>`

classref-property-setget

-   `void (No return value.)`
    **set\_auto\_brace\_completion\_pairs**(value:
    `Dictionary<class_Dictionary>`)
-   `Dictionary<class_Dictionary>`
    **get\_auto\_brace\_completion\_pairs**()

Sets the brace pairs to be autocompleted.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **code\_completion\_enabled** = `false`
`🔗<class_CodeEdit_property_code_completion_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_code\_completion\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_code\_completion\_enabled**()

Sets whether code completion is allowed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`String<class_String>`\]
**code\_completion\_prefixes** = `[]`
`🔗<class_CodeEdit_property_code_completion_prefixes>`

classref-property-setget

-   `void (No return value.)` **set\_code\_completion\_prefixes**(value:
    `Array<class_Array>`\[`String<class_String>`\])
-   `Array<class_Array>`\[`String<class_String>`\]
    **get\_code\_completion\_prefixes**()

Sets prefixes that will trigger code completion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`String<class_String>`\] **delimiter\_comments** =
`[]` `🔗<class_CodeEdit_property_delimiter_comments>`

classref-property-setget

-   `void (No return value.)` **set\_comment\_delimiters**(value:
    `Array<class_Array>`\[`String<class_String>`\])
-   `Array<class_Array>`\[`String<class_String>`\]
    **get\_comment\_delimiters**()

Sets the comment delimiters. All existing comment delimiters will be
removed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`String<class_String>`\] **delimiter\_strings** =
`["' '", "\" \""]` `🔗<class_CodeEdit_property_delimiter_strings>`

classref-property-setget

-   `void (No return value.)` **set\_string\_delimiters**(value:
    `Array<class_Array>`\[`String<class_String>`\])
-   `Array<class_Array>`\[`String<class_String>`\]
    **get\_string\_delimiters**()

Sets the string delimiters. All existing string delimiters will be
removed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gutters\_draw\_bookmarks** = `false`
`🔗<class_CodeEdit_property_gutters_draw_bookmarks>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_bookmarks\_gutter**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_drawing\_bookmarks\_gutter**()

Sets if bookmarked should be drawn in the gutter. This gutter is shared
with breakpoints and executing lines.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gutters\_draw\_breakpoints\_gutter** = `false`
`🔗<class_CodeEdit_property_gutters_draw_breakpoints_gutter>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_breakpoints\_gutter**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_drawing\_breakpoints\_gutter**()

Sets if breakpoints should be drawn in the gutter. This gutter is shared
with bookmarks and executing lines.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gutters\_draw\_executing\_lines** = `false`
`🔗<class_CodeEdit_property_gutters_draw_executing_lines>`

classref-property-setget

-   `void (No return value.)`
    **set\_draw\_executing\_lines\_gutter**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_drawing\_executing\_lines\_gutter**()

Sets if executing lines should be marked in the gutter. This gutter is
shared with breakpoints and bookmarks lines.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gutters\_draw\_fold\_gutter** = `false`
`🔗<class_CodeEdit_property_gutters_draw_fold_gutter>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_fold\_gutter**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_drawing\_fold\_gutter**()

Sets if foldable lines icons should be drawn in the gutter.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gutters\_draw\_line\_numbers** = `false`
`🔗<class_CodeEdit_property_gutters_draw_line_numbers>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_line\_numbers**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_draw\_line\_numbers\_enabled**()

Sets if line numbers should be drawn in the gutter.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gutters\_zero\_pad\_line\_numbers** = `false`
`🔗<class_CodeEdit_property_gutters_zero_pad_line_numbers>`

classref-property-setget

-   `void (No return value.)`
    **set\_line\_numbers\_zero\_padded**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_line\_numbers\_zero\_padded**()

Sets if line numbers drawn in the gutter are zero padded.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **indent\_automatic** = `false`
`🔗<class_CodeEdit_property_indent_automatic>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_indent\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_auto\_indent\_enabled**()

Sets whether automatic indent are enabled, this will add an extra indent
if a prefix or brace is found.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`String<class_String>`\]
**indent\_automatic\_prefixes** = `[":", "{", "[", "("]`
`🔗<class_CodeEdit_property_indent_automatic_prefixes>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_indent\_prefixes**(value:
    `Array<class_Array>`\[`String<class_String>`\])
-   `Array<class_Array>`\[`String<class_String>`\]
    **get\_auto\_indent\_prefixes**()

Prefixes to trigger an automatic indent.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **indent\_size** = `4`
`🔗<class_CodeEdit_property_indent_size>`

classref-property-setget

-   `void (No return value.)` **set\_indent\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_indent\_size**()

Size of the tabulation indent (one `Tab` press) in characters. If
`indent_use_spaces<class_CodeEdit_property_indent_use_spaces>` is
enabled the number of spaces to use.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **indent\_use\_spaces** = `false`
`🔗<class_CodeEdit_property_indent_use_spaces>`

classref-property-setget

-   `void (No return value.)` **set\_indent\_using\_spaces**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_indent\_using\_spaces**()

Use spaces instead of tabs for indentation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **line\_folding** = `false`
`🔗<class_CodeEdit_property_line_folding>`

classref-property-setget

-   `void (No return value.)` **set\_line\_folding\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_line\_folding\_enabled**()

Sets whether line folding is allowed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`int<class_int>`\] **line\_length\_guidelines** =
`[]` `🔗<class_CodeEdit_property_line_length_guidelines>`

classref-property-setget

-   `void (No return value.)` **set\_line\_length\_guidelines**(value:
    `Array<class_Array>`\[`int<class_int>`\])
-   `Array<class_Array>`\[`int<class_int>`\]
    **get\_line\_length\_guidelines**()

Draws vertical lines at the provided columns. The first entry is
considered a main hard guideline and is draw more prominently.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **symbol\_lookup\_on\_click** = `false`
`🔗<class_CodeEdit_property_symbol_lookup_on_click>`

classref-property-setget

-   `void (No return value.)`
    **set\_symbol\_lookup\_on\_click\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_symbol\_lookup\_on\_click\_enabled**()

Set when a validated word from
`symbol_validate<class_CodeEdit_signal_symbol_validate>` is clicked, the
`symbol_lookup<class_CodeEdit_signal_symbol_lookup>` should be emitted.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_confirm\_code\_completion**(replace:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_CodeEdit_private_method__confirm_code_completion>`

Override this method to define how the selected entry should be
inserted. If `replace` is `true`, any existing text should be replaced.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_filter\_code\_completion\_candidates**(candidates:
`Array<class_Array>`\[`Dictionary<class_Dictionary>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_private_method__filter_code_completion_candidates>`

Override this method to define what items in `candidates` should be
displayed.

Both `candidates` and the return is a `Array<class_Array>` of
`Dictionary<class_Dictionary>`, see
`get_code_completion_option<class_CodeEdit_method_get_code_completion_option>`
for `Dictionary<class_Dictionary>` content.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_request\_code\_completion**(force:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_CodeEdit_private_method__request_code_completion>`

Override this method to define what happens when the user requests code
completion. If `force` is `true`, any checks should be bypassed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**add\_auto\_brace\_completion\_pair**(start\_key:
`String<class_String>`, end\_key: `String<class_String>`)
`🔗<class_CodeEdit_method_add_auto_brace_completion_pair>`

Adds a brace pair.

Both the start and end keys must be symbols. Only the start key has to
be unique.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_code\_completion\_option**(type:
`CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>`, display\_text:
`String<class_String>`, insert\_text: `String<class_String>`,
text\_color: `Color<class_Color>` = Color(1, 1, 1, 1), icon:
`Resource<class_Resource>` = null, value: `Variant<class_Variant>` =
null, location: `int<class_int>` = 1024)
`🔗<class_CodeEdit_method_add_code_completion_option>`

Submits an item to the queue of potential candidates for the
autocomplete menu. Call
`update_code_completion_options<class_CodeEdit_method_update_code_completion_options>`
to update the list.

`location` indicates location of the option relative to the location of
the code completion query. See
`CodeCompletionLocation<enum_CodeEdit_CodeCompletionLocation>` for how
to set this value.

\*\*Note:\*\* This list will replace all current candidates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_comment\_delimiter**(start\_key:
`String<class_String>`, end\_key: `String<class_String>`, line\_only:
`bool<class_bool>` = false)
`🔗<class_CodeEdit_method_add_comment_delimiter>`

Adds a comment delimiter from `start_key` to `end_key`. Both keys should
be symbols, and `start_key` must not be shared with other delimiters.

If `line_only` is `true` or `end_key` is an empty
`String<class_String>`, the region does not carry over to the next line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_string\_delimiter**(start\_key:
`String<class_String>`, end\_key: `String<class_String>`, line\_only:
`bool<class_bool>` = false)
`🔗<class_CodeEdit_method_add_string_delimiter>`

Defines a string delimiter from `start_key` to `end_key`. Both keys
should be symbols, and `start_key` must not be shared with other
delimiters.

If `line_only` is `true` or `end_key` is an empty
`String<class_String>`, the region does not carry over to the next line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **can\_fold\_line**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_can_fold_line>`

Returns if the given line is foldable, that is, it has indented lines
right below it or a comment / string block.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **cancel\_code\_completion**()
`🔗<class_CodeEdit_method_cancel_code_completion>`

Cancels the autocomplete menu.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_bookmarked\_lines**()
`🔗<class_CodeEdit_method_clear_bookmarked_lines>`

Clears all bookmarked lines.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_breakpointed\_lines**()
`🔗<class_CodeEdit_method_clear_breakpointed_lines>`

Clears all breakpointed lines.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_comment\_delimiters**()
`🔗<class_CodeEdit_method_clear_comment_delimiters>`

Removes all comment delimiters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_executing\_lines**()
`🔗<class_CodeEdit_method_clear_executing_lines>`

Clears all executed lines.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_string\_delimiters**()
`🔗<class_CodeEdit_method_clear_string_delimiters>`

Removes all string delimiters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **confirm\_code\_completion**(replace:
`bool<class_bool>` = false)
`🔗<class_CodeEdit_method_confirm_code_completion>`

Inserts the selected entry into the text. If `replace` is `true`, any
existing text is replaced rather than merged.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **convert\_indent**(from\_line:
`int<class_int>` = -1, to\_line: `int<class_int>` = -1)
`🔗<class_CodeEdit_method_convert_indent>`

Converts the indents of lines between `from_line` and `to_line` to tabs
or spaces as set by
`indent_use_spaces<class_CodeEdit_property_indent_use_spaces>`.

Values of `-1` convert the entire text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **create\_code\_region**()
`🔗<class_CodeEdit_method_create_code_region>`

Creates a new code region with the selection. At least one single line
comment delimiter have to be defined (see
`add_comment_delimiter<class_CodeEdit_method_add_comment_delimiter>`).

A code region is a part of code that is highlighted when folded and can
help organize your script.

Code region start and end tags can be customized (see
`set_code_region_tags<class_CodeEdit_method_set_code_region_tags>`).

Code regions are delimited using start and end tags (respectively
`region` and `endregion` by default) preceded by one line comment
delimiter. (eg. `#region` and `#endregion`)

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **delete\_lines**()
`🔗<class_CodeEdit_method_delete_lines>`

Deletes all lines that are selected or have a caret on them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **do\_indent**()
`🔗<class_CodeEdit_method_do_indent>`

Perform an indent as if the user activated the "ui\_text\_indent"
action.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **duplicate\_lines**()
`🔗<class_CodeEdit_method_duplicate_lines>`

Duplicates all lines currently selected with any caret. Duplicates the
entire line beneath the current one no matter where the caret is within
the line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **duplicate\_selection**()
`🔗<class_CodeEdit_method_duplicate_selection>`

Duplicates all selected text and duplicates all lines with a caret on
them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fold\_all\_lines**()
`🔗<class_CodeEdit_method_fold_all_lines>`

Folds all lines that are possible to be folded (see
`can_fold_line<class_CodeEdit_method_can_fold_line>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fold\_line**(line: `int<class_int>`)
`🔗<class_CodeEdit_method_fold_line>`

Folds the given line, if possible (see
`can_fold_line<class_CodeEdit_method_can_fold_line>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>`
**get\_auto\_brace\_completion\_close\_key**(open\_key:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_auto_brace_completion_close_key>`

Gets the matching auto brace close key for `open_key`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>` **get\_bookmarked\_lines**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_bookmarked_lines>`

Gets all bookmarked lines.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**get\_breakpointed\_lines**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_breakpointed_lines>`

Gets all breakpointed lines.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_code\_completion\_option**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_code_completion_option>`

Gets the completion option at `index`. The return
`Dictionary<class_Dictionary>` has the following key-values:

`kind`: `CodeCompletionKind<enum_CodeEdit_CodeCompletionKind>`

`display_text`: Text that is shown on the autocomplete menu.

`insert_text`: Text that is to be inserted when this item is selected.

`font_color`: Color of the text on the autocomplete menu.

`icon`: Icon to draw on the autocomplete menu.

`default_value`: Value of the symbol.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_code\_completion\_options**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_code_completion_options>`

Gets all completion options, see
`get_code_completion_option<class_CodeEdit_method_get_code_completion_option>`
for return content.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_code\_completion\_selected\_index**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_code_completion_selected_index>`

Gets the index of the current selected completion option.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_code\_region\_end\_tag**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_code_region_end_tag>`

Returns the code region end tag (without comment delimiter).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_code\_region\_start\_tag**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_code_region_start_tag>`

Returns the code region start tag (without comment delimiter).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_delimiter\_end\_key**(delimiter\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_delimiter_end_key>`

Gets the end key for a string or comment region index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_delimiter\_end\_position**(line:
`int<class_int>`, column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_delimiter_end_position>`

If `line` `column` is in a string or comment, returns the end position
of the region. If not or no end could be found, both
`Vector2<class_Vector2>` values will be `-1`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_delimiter\_start\_key**(delimiter\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_delimiter_start_key>`

Gets the start key for a string or comment region index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_delimiter\_start\_position**(line:
`int<class_int>`, column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_delimiter_start_position>`

If `line` `column` is in a string or comment, returns the start position
of the region. If not or no start could be found, both
`Vector2<class_Vector2>` values will be `-1`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>` **get\_executing\_lines**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_executing_lines>`

Gets all executing lines.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`int<class_int>`\] **get\_folded\_lines**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_folded_lines>`

Returns all lines that are current folded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_text\_for\_code\_completion**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_text_for_code_completion>`

Returns the full text with char `0xFFFF` at the caret location.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_text\_for\_symbol\_lookup**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_text_for_symbol_lookup>`

Returns the full text with char `0xFFFF` at the cursor location.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_text\_with\_cursor\_char**(line:
`int<class_int>`, column: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_get_text_with_cursor_char>`

Returns the full text with char `0xFFFF` at the specified location.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**has\_auto\_brace\_completion\_close\_key**(close\_key:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_has_auto_brace_completion_close_key>`

Returns `true` if close key `close_key` exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**has\_auto\_brace\_completion\_open\_key**(open\_key:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_has_auto_brace_completion_open_key>`

Returns `true` if open key `open_key` exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_comment\_delimiter**(start\_key:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_has_comment_delimiter>`

Returns `true` if comment `start_key` exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_string\_delimiter**(start\_key:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_has_string_delimiter>`

Returns `true` if string `start_key` exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **indent\_lines**()
`🔗<class_CodeEdit_method_indent_lines>`

Indents selected lines, or in the case of no selection the caret line by
one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **is\_in\_comment**(line: `int<class_int>`, column:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_is_in_comment>`

Returns delimiter index if `line` `column` is in a comment. If `column`
is not provided, will return delimiter index if the entire `line` is a
comment. Otherwise `-1`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **is\_in\_string**(line: `int<class_int>`, column:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_is_in_string>`

Returns the delimiter index if `line` `column` is in a string. If
`column` is not provided, will return the delimiter index if the entire
`line` is a string. Otherwise `-1`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_line\_bookmarked**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_is_line_bookmarked>`

Returns whether the line at the specified index is bookmarked or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_line\_breakpointed**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_is_line_breakpointed>`

Returns whether the line at the specified index is breakpointed or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_line\_code\_region\_end**(line:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_is_line_code_region_end>`

Returns whether the line at the specified index is a code region end.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_line\_code\_region\_start**(line:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_is_line_code_region_start>`

Returns whether the line at the specified index is a code region start.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_line\_executing**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_is_line_executing>`

Returns whether the line at the specified index is marked as executing
or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_line\_folded**(line: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeEdit_method_is_line_folded>`

Returns whether the line at the specified index is folded or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_lines\_down**()
`🔗<class_CodeEdit_method_move_lines_down>`

Moves all lines down that are selected or have a caret on them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_lines\_up**()
`🔗<class_CodeEdit_method_move_lines_up>`

Moves all lines up that are selected or have a caret on them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_comment\_delimiter**(start\_key:
`String<class_String>`)
`🔗<class_CodeEdit_method_remove_comment_delimiter>`

Removes the comment delimiter with `start_key`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_string\_delimiter**(start\_key:
`String<class_String>`)
`🔗<class_CodeEdit_method_remove_string_delimiter>`

Removes the string delimiter with `start_key`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **request\_code\_completion**(force:
`bool<class_bool>` = false)
`🔗<class_CodeEdit_method_request_code_completion>`

Emits
`code_completion_requested<class_CodeEdit_signal_code_completion_requested>`,
if `force` is `true` will bypass all checks. Otherwise will check that
the caret is in a word or in front of a prefix. Will ignore the request
if all current options are of type file path, node path, or signal.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_code\_completion\_selected\_index**(index: `int<class_int>`)
`🔗<class_CodeEdit_method_set_code_completion_selected_index>`

Sets the current selected completion option.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_code\_hint**(code\_hint:
`String<class_String>`) `🔗<class_CodeEdit_method_set_code_hint>`

Sets the code hint text. Pass an empty string to clear.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_code\_hint\_draw\_below**(draw\_below:
`bool<class_bool>`) `🔗<class_CodeEdit_method_set_code_hint_draw_below>`

Sets if the code hint should draw below the text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_code\_region\_tags**(start:
`String<class_String>` = "region", end: `String<class_String>` =
"endregion") `🔗<class_CodeEdit_method_set_code_region_tags>`

Sets the code region start and end tags (without comment delimiter).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_as\_bookmarked**(line:
`int<class_int>`, bookmarked: `bool<class_bool>`)
`🔗<class_CodeEdit_method_set_line_as_bookmarked>`

Sets the line as bookmarked.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_as\_breakpoint**(line:
`int<class_int>`, breakpointed: `bool<class_bool>`)
`🔗<class_CodeEdit_method_set_line_as_breakpoint>`

Sets the line as breakpointed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_line\_as\_executing**(line:
`int<class_int>`, executing: `bool<class_bool>`)
`🔗<class_CodeEdit_method_set_line_as_executing>`

Sets the line as executing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_symbol\_lookup\_word\_as\_valid**(valid: `bool<class_bool>`)
`🔗<class_CodeEdit_method_set_symbol_lookup_word_as_valid>`

Sets the symbol emitted by
`symbol_validate<class_CodeEdit_signal_symbol_validate>` as a valid
lookup.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **toggle\_foldable\_line**(line:
`int<class_int>`) `🔗<class_CodeEdit_method_toggle_foldable_line>`

Toggle the folding of the code block at the given line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **toggle\_foldable\_lines\_at\_carets**()
`🔗<class_CodeEdit_method_toggle_foldable_lines_at_carets>`

Toggle the folding of the code block on all lines with a caret on them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unfold\_all\_lines**()
`🔗<class_CodeEdit_method_unfold_all_lines>`

Unfolds all lines, folded or not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unfold\_line**(line: `int<class_int>`)
`🔗<class_CodeEdit_method_unfold_line>`

Unfolds all lines that were previously folded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unindent\_lines**()
`🔗<class_CodeEdit_method_unindent_lines>`

Unindents selected lines, or in the case of no selection the caret line
by one. Same as performing "ui\_text\_unindent" action.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update\_code\_completion\_options**(force:
`bool<class_bool>`)
`🔗<class_CodeEdit_method_update_code_completion_options>`

Submits all completion options added with
`add_code_completion_option<class_CodeEdit_method_add_code_completion_option>`.
Will try to force the autocomplete menu to popup, if `force` is `true`.

\*\*Note:\*\* This will replace all current candidates.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **bookmark\_color** = `Color(0.5, 0.64, 1, 0.8)`
`🔗<class_CodeEdit_theme_color_bookmark_color>`

`Color<class_Color>` of the bookmark icon for bookmarked lines.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **brace\_mismatch\_color** =
`Color(1, 0.2, 0.2, 1)`
`🔗<class_CodeEdit_theme_color_brace_mismatch_color>`

`Color<class_Color>` of the text to highlight mismatched braces.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **breakpoint\_color** = `Color(0.9, 0.29, 0.3, 1)`
`🔗<class_CodeEdit_theme_color_breakpoint_color>`

`Color<class_Color>` of the breakpoint icon for bookmarked lines.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **code\_folding\_color** =
`Color(0.8, 0.8, 0.8, 0.8)`
`🔗<class_CodeEdit_theme_color_code_folding_color>`

`Color<class_Color>` for all icons related to line folding.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **completion\_background\_color** =
`Color(0.17, 0.16, 0.2, 1)`
`🔗<class_CodeEdit_theme_color_completion_background_color>`

Sets the background `Color<class_Color>` for the code completion popup.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **completion\_existing\_color** =
`Color(0.87, 0.87, 0.87, 0.13)`
`🔗<class_CodeEdit_theme_color_completion_existing_color>`

Background highlight `Color<class_Color>` for matching text in code
completion options.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **completion\_scroll\_color** =
`Color(1, 1, 1, 0.29)`
`🔗<class_CodeEdit_theme_color_completion_scroll_color>`

`Color<class_Color>` of the scrollbar in the code completion popup.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **completion\_scroll\_hovered\_color** =
`Color(1, 1, 1, 0.4)`
`🔗<class_CodeEdit_theme_color_completion_scroll_hovered_color>`

`Color<class_Color>` of the scrollbar in the code completion popup when
hovered.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **completion\_selected\_color** =
`Color(0.26, 0.26, 0.27, 1)`
`🔗<class_CodeEdit_theme_color_completion_selected_color>`

Background highlight `Color<class_Color>` for the current selected
option item in the code completion popup.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **executing\_line\_color** =
`Color(0.98, 0.89, 0.27, 1)`
`🔗<class_CodeEdit_theme_color_executing_line_color>`

`Color<class_Color>` of the executing icon for executing lines.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **folded\_code\_region\_color** =
`Color(0.68, 0.46, 0.77, 0.2)`
`🔗<class_CodeEdit_theme_color_folded_code_region_color>`

`Color<class_Color>` of background line highlight for folded code
region.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **line\_length\_guideline\_color** =
`Color(0.3, 0.5, 0.8, 0.1)`
`🔗<class_CodeEdit_theme_color_line_length_guideline_color>`

`Color<class_Color>` of the main line length guideline, secondary
guidelines will have 50% alpha applied.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **line\_number\_color** =
`Color(0.67, 0.67, 0.67, 0.4)`
`🔗<class_CodeEdit_theme_color_line_number_color>`

Sets the `Color<class_Color>` of line numbers.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **completion\_lines** = `7`
`🔗<class_CodeEdit_theme_constant_completion_lines>`

Max number of options to display in the code completion popup at any one
time.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **completion\_max\_width** = `50`
`🔗<class_CodeEdit_theme_constant_completion_max_width>`

Max width of options in the code completion popup. Options longer than
this will be cut off.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **completion\_scroll\_width** = `6`
`🔗<class_CodeEdit_theme_constant_completion_scroll_width>`

Width of the scrollbar in the code completion popup.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **bookmark**
`🔗<class_CodeEdit_theme_icon_bookmark>`

Sets a custom `Texture2D<class_Texture2D>` to draw in the bookmark
gutter for bookmarked lines.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **breakpoint**
`🔗<class_CodeEdit_theme_icon_breakpoint>`

Sets a custom `Texture2D<class_Texture2D>` to draw in the breakpoint
gutter for breakpointed lines.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **can\_fold**
`🔗<class_CodeEdit_theme_icon_can_fold>`

Sets a custom `Texture2D<class_Texture2D>` to draw in the line folding
gutter when a line can be folded.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **can\_fold\_code\_region**
`🔗<class_CodeEdit_theme_icon_can_fold_code_region>`

Sets a custom `Texture2D<class_Texture2D>` to draw in the line folding
gutter when a code region can be folded.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **completion\_color\_bg**
`🔗<class_CodeEdit_theme_icon_completion_color_bg>`

Background panel for the color preview box in autocompletion (visible
when the color is translucent).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **executing\_line**
`🔗<class_CodeEdit_theme_icon_executing_line>`

Icon to draw in the executing gutter for executing lines.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **folded**
`🔗<class_CodeEdit_theme_icon_folded>`

Sets a custom `Texture2D<class_Texture2D>` to draw in the line folding
gutter when a line is folded and can be unfolded.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **folded\_code\_region**
`🔗<class_CodeEdit_theme_icon_folded_code_region>`

Sets a custom `Texture2D<class_Texture2D>` to draw in the line folding
gutter when a code region is folded and can be unfolded.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **folded\_eol\_icon**
`🔗<class_CodeEdit_theme_icon_folded_eol_icon>`

Sets a custom `Texture2D<class_Texture2D>` to draw at the end of a
folded line.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **completion**
`🔗<class_CodeEdit_theme_style_completion>`

`StyleBox<class_StyleBox>` for the code completion popup.
