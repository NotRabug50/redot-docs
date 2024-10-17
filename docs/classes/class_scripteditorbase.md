github\_url  
hide

# ScriptEditorBase

**Inherits:** `VBoxContainer<class_VBoxContainer>` **&lt;**
`BoxContainer<class_BoxContainer>` **&lt;** `Container<class_Container>`
**&lt;** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Base editor for editing scripts in the
`ScriptEditor<class_ScriptEditor>`.

classref-introduction-group

## Description

Base editor for editing scripts in the
`ScriptEditor<class_ScriptEditor>`. This does not include documentation
items.

classref-reftable-group

## Methods

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

## Signals

classref-signal

**edited\_script\_changed**()
`🔗<class_ScriptEditorBase_signal_edited_script_changed>`

Emitted after script validation.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**go\_to\_help**(what: `String<class_String>`)
`🔗<class_ScriptEditorBase_signal_go_to_help>`

Emitted when the user requests a specific documentation page.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**go\_to\_method**(script: `Object<class_Object>`, method:
`String<class_String>`) `🔗<class_ScriptEditorBase_signal_go_to_method>`

Emitted when the user requests to view a specific method of a script,
similar to
`request_open_script_at_line<class_ScriptEditorBase_signal_request_open_script_at_line>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**name\_changed**() `🔗<class_ScriptEditorBase_signal_name_changed>`

Emitted after script validation or when the edited resource has changed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**replace\_in\_files\_requested**(text: `String<class_String>`)
`🔗<class_ScriptEditorBase_signal_replace_in_files_requested>`

Emitted when the user request to find and replace text in the file
system.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**request\_help**(topic: `String<class_String>`)
`🔗<class_ScriptEditorBase_signal_request_help>`

Emitted when the user requests contextual help.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**request\_open\_script\_at\_line**(script: `Object<class_Object>`,
line: `int<class_int>`)
`🔗<class_ScriptEditorBase_signal_request_open_script_at_line>`

Emitted when the user requests to view a specific line of a script,
similar to `go_to_method<class_ScriptEditorBase_signal_go_to_method>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**request\_save\_history**()
`🔗<class_ScriptEditorBase_signal_request_save_history>`

Emitted when the user contextual goto and the item is in the same
script.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**request\_save\_previous\_state**(state:
`Dictionary<class_Dictionary>`)
`🔗<class_ScriptEditorBase_signal_request_save_previous_state>`

Emitted when the user changes current script or moves caret by 10 or
more columns within the same script.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**search\_in\_files\_requested**(text: `String<class_String>`)
`🔗<class_ScriptEditorBase_signal_search_in_files_requested>`

Emitted when the user request to search text in the file system.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_syntax\_highlighter**(highlighter:
`EditorSyntaxHighlighter<class_EditorSyntaxHighlighter>`)
`🔗<class_ScriptEditorBase_method_add_syntax_highlighter>`

Adds a `EditorSyntaxHighlighter<class_EditorSyntaxHighlighter>` to the
open script.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Control<class_Control>` **get\_base\_editor**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ScriptEditorBase_method_get_base_editor>`

Returns the underlying `Control<class_Control>` used for editing
scripts. For text scripts, this is a `CodeEdit<class_CodeEdit>`.
