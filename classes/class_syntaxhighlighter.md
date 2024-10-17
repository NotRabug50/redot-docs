github\_url  
hide

# SyntaxHighlighter

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `CodeHighlighter<class_CodeHighlighter>`,
`EditorSyntaxHighlighter<class_EditorSyntaxHighlighter>`

Base class for syntax highlighters. Provides syntax highlighting data to
a `TextEdit<class_TextEdit>`.

classref-introduction-group

## Description

Base class for syntax highlighters. Provides syntax highlighting data to
a `TextEdit<class_TextEdit>`. The associated `TextEdit<class_TextEdit>`
will call into the **SyntaxHighlighter** on an as-needed basis.

\*\*Note:\*\* A **SyntaxHighlighter** instance should not be used across
multiple `TextEdit<class_TextEdit>` nodes.

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

## Method Descriptions

classref-method

`void (No return value.)` **\_clear\_highlighting\_cache**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_SyntaxHighlighter_private_method__clear_highlighting_cache>`

Virtual method which can be overridden to clear any local caches.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**\_get\_line\_syntax\_highlighting**(line: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SyntaxHighlighter_private_method__get_line_syntax_highlighting>`

Virtual method which can be overridden to return syntax highlighting
data.

See
`get_line_syntax_highlighting<class_SyntaxHighlighter_method_get_line_syntax_highlighting>`
for more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_update\_cache**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_SyntaxHighlighter_private_method__update_cache>`

Virtual method which can be overridden to update any local caches.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_highlighting\_cache**()
`🔗<class_SyntaxHighlighter_method_clear_highlighting_cache>`

Clears all cached syntax highlighting data.

Then calls overridable method
`_clear_highlighting_cache<class_SyntaxHighlighter_private_method__clear_highlighting_cache>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_line\_syntax\_highlighting**(line:
`int<class_int>`)
`🔗<class_SyntaxHighlighter_method_get_line_syntax_highlighting>`

Returns syntax highlighting data for a single line. If the line is not
cached, calls
`_get_line_syntax_highlighting<class_SyntaxHighlighter_private_method__get_line_syntax_highlighting>`
to calculate the data.

The return `Dictionary<class_Dictionary>` is column number to
`Dictionary<class_Dictionary>`. The column number notes the start of a
region, the region will end if another region is found, or at the end of
the line. The nested `Dictionary<class_Dictionary>` contains the data
for that region, currently only the key "color" is supported.

\*\*Example return:\*\*

    var color_map = {
        0: {
            "color": Color(1, 0, 0)
        },
        5: {
            "color": Color(0, 1, 0)
        }
    }

This will color columns 0-4 red, and columns 5-eol in green.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TextEdit<class_TextEdit>` **get\_text\_edit**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SyntaxHighlighter_method_get_text_edit>`

Returns the associated `TextEdit<class_TextEdit>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update\_cache**()
`🔗<class_SyntaxHighlighter_method_update_cache>`

Clears then updates the **SyntaxHighlighter** caches. Override
`_update_cache<class_SyntaxHighlighter_private_method__update_cache>`
for a callback.

\*\*Note:\*\* This is called automatically when the associated
`TextEdit<class_TextEdit>` node, updates its own cache.
