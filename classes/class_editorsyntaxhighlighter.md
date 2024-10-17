github\_url  
hide

# EditorSyntaxHighlighter

**Inherits:** `SyntaxHighlighter<class_SyntaxHighlighter>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`GDScriptSyntaxHighlighter<class_GDScriptSyntaxHighlighter>`

Base class for `SyntaxHighlighter<class_SyntaxHighlighter>` used by the
`ScriptEditor<class_ScriptEditor>`.

classref-introduction-group

## Description

Base class that all `SyntaxHighlighter<class_SyntaxHighlighter>`s used
by the `ScriptEditor<class_ScriptEditor>` extend from.

Add a syntax highlighter to an individual script by calling
`ScriptEditorBase.add_syntax_highlighter<class_ScriptEditorBase_method_add_syntax_highlighter>`.
To apply to all scripts on open, call
`ScriptEditor.register_syntax_highlighter<class_ScriptEditor_method_register_syntax_highlighter>`.

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

## Method Descriptions

classref-method

`String<class_String>` **\_get\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSyntaxHighlighter_private_method__get_name>`

Virtual method which can be overridden to return the syntax highlighter
name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_supported\_languages**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSyntaxHighlighter_private_method__get_supported_languages>`

Virtual method which can be overridden to return the supported language
names.
