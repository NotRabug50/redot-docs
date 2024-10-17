github\_url  
hide

# GDScriptSyntaxHighlighter

**Inherits:** `EditorSyntaxHighlighter<class_EditorSyntaxHighlighter>`
**&lt;** `SyntaxHighlighter<class_SyntaxHighlighter>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A GDScript syntax highlighter that can be used with
`TextEdit<class_TextEdit>` and `CodeEdit<class_CodeEdit>` nodes.

classref-introduction-group

## Description

**Note:** This class can only be used for editor plugins because it
relies on editor settings.

gdscript

var code\_preview = TextEdit.new() var highlighter =
GDScriptSyntaxHighlighter.new() code\_preview.syntax\_highlighter =
highlighter

csharp

var codePreview = new TextEdit(); var highlighter = new
GDScriptSyntaxHighlighter(); codePreview.SyntaxHighlighter =
highlighter;
