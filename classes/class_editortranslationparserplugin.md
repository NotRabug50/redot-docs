github\_url  
hide

# EditorTranslationParserPlugin

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Plugin for adding custom parsers to extract strings that are to be
translated from custom files (.csv, .json etc.).

classref-introduction-group

## Description

**EditorTranslationParserPlugin** is invoked when a file is being parsed
to extract strings that require translation. To define the parsing and
string extraction logic, override the
`_parse_file<class_EditorTranslationParserPlugin_private_method__parse_file>`
method in script.

Add the extracted strings to argument `msgids` or
`msgids_context_plural` if context or plural is used.

When adding to `msgids_context_plural`, you must add the data using the
format `["A", "B", "C"]`, where `A` represents the extracted string, `B`
represents the context, and `C` represents the plural version of the
extracted string. If you want to add only context but not plural, put
`""` for the plural slot. The idea is the same if you only want to add
plural but not context. See the code below for concrete examples.

The extracted strings will be written into a POT file selected by user
under "POT Generation" in "Localization" tab in "Project Settings" menu.

Below shows an example of a custom parser that extracts strings from a
CSV file to write into a POT.

gdscript

@tool extends EditorTranslationParserPlugin

func \_parse\_file(path, msgids, msgids\_context\_plural):  
var file = FileAccess.open(path, FileAccess.READ) var text =
file.get\_as\_text() var split\_strs = text.split(",", false) for s in
split\_strs: msgids.append(s) \#print("Extracted string: " + s)

func \_get\_recognized\_extensions():  
return \["csv"\]

csharp

using Godot;

\[Tool\] public partial class CustomParser :
EditorTranslationParserPlugin { public override void \_ParseFile(string
path, Godot.Collections.Array&lt;string&gt; msgids,
Godot.Collections.Array&lt;Godot.Collections.Array&gt;
msgidsContextPlural) { using var file = FileAccess.Open(path,
FileAccess.ModeFlags.Read); string text = file.GetAsText(); string\[\]
splitStrs = text.Split(",", allowEmpty: false); foreach (string s in
splitStrs) { msgids.Add(s); //GD.Print($"Extracted string: {s}"); } }

> public override string\[\] \_GetRecognizedExtensions() { return new
> string\[\] { "csv" }; }

}

To add a translatable string associated with context or plural, add it
to `msgids_context_plural`:

gdscript

\# This will add a message with msgid "Test 1", msgctxt "context", and
msgid\_plural "test 1 plurals". msgids\_context\_plural.append(\["Test
1", "context", "test 1 plurals"\]) \# This will add a message with msgid
"A test without context" and msgid\_plural "plurals".
msgids\_context\_plural.append(\["A test without context", "",
"plurals"\]) \# This will add a message with msgid "Only with context"
and msgctxt "a friendly context". msgids\_context\_plural.append(\["Only
with context", "a friendly context", ""\])

csharp

// This will add a message with msgid "Test 1", msgctxt "context", and
msgid\_plural "test 1 plurals". msgidsContextPlural.Add(new
Godot.Collections.Array{"Test 1", "context", "test 1 Plurals"}); // This
will add a message with msgid "A test without context" and msgid\_plural
"plurals". msgidsContextPlural.Add(new Godot.Collections.Array{"A test
without context", "", "plurals"}); // This will add a message with msgid
"Only with context" and msgctxt "a friendly context".
msgidsContextPlural.Add(new Godot.Collections.Array{"Only with context",
"a friendly context", ""});

\*\*Note:\*\* If you override parsing logic for standard script types
(GDScript, C#, etc.), it would be better to load the `path` argument
using `ResourceLoader.load<class_ResourceLoader_method_load>`. This is
because built-in scripts are loaded as `Resource<class_Resource>` type,
not `FileAccess<class_FileAccess>` type.

For example:

gdscript

func \_parse\_file(path, msgids, msgids\_context\_plural):  
var res = ResourceLoader.load(path, "Script") var text =
res.source\_code \# Parsing logic.

func \_get\_recognized\_extensions():  
return \["gd"\]

csharp

public override void \_ParseFile(string path,
Godot.Collections.Array&lt;string&gt; msgids,
Godot.Collections.Array&lt;Godot.Collections.Array&gt;
msgidsContextPlural) { var res = ResourceLoader.Load&lt;Script&gt;(path,
"Script"); string text = res.SourceCode; // Parsing logic. }

public override string\[\] \_GetRecognizedExtensions() { return new
string\[\] { "gd" }; }

To use **EditorTranslationParserPlugin**, register it using the
`EditorPlugin.add_translation_parser_plugin<class_EditorPlugin_method_add_translation_parser_plugin>`
method first.

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

`PackedStringArray<class_PackedStringArray>`
**\_get\_recognized\_extensions**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorTranslationParserPlugin_private_method__get_recognized_extensions>`

Gets the list of file extensions to associate with this parser, e.g.
`["csv"]`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_parse\_file**(path:
`String<class_String>`, msgids:
`Array<class_Array>`\[`String<class_String>`\], msgids\_context\_plural:
`Array<class_Array>`\[`Array<class_Array>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorTranslationParserPlugin_private_method__parse_file>`

Override this method to define a custom parsing logic to extract the
translatable strings.
