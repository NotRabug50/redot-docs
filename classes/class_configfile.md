github\_url  
hide

# ConfigFile

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Helper class to handle INI-style files.

classref-introduction-group

## Description

This helper class can be used to store `Variant<class_Variant>` values
on the filesystem using INI-style formatting. The stored values are
identified by a section and a key:

    [section]
    some_key=42
    string_example="Hello World3D!"
    a_vector=Vector3(1, 0, 2)

The stored data can be saved to or parsed from a file, though ConfigFile
objects can also be used directly without accessing the filesystem.

The following example shows how to create a simple **ConfigFile** and
save it on disc:

gdscript

\# Create new ConfigFile object. var config = ConfigFile.new()

\# Store some values. config.set\_value("Player1", "player\_name",
"Steve") config.set\_value("Player1", "best\_score", 10)
config.set\_value("Player2", "player\_name", "V3geta")
config.set\_value("Player2", "best\_score", 9001)

\# Save it to a file (overwrite if already exists).
config.save("user://scores.cfg")

csharp

// Create new ConfigFile object. var config = new ConfigFile();

// Store some values. config.SetValue("Player1", "player\_name",
"Steve"); config.SetValue("Player1", "best\_score", 10);
config.SetValue("Player2", "player\_name", "V3geta");
config.SetValue("Player2", "best\_score", 9001);

// Save it to a file (overwrite if already exists).
config.Save("user://scores.cfg");

This example shows how the above file could be loaded:

gdscript

var score\_data = {} var config = ConfigFile.new()

\# Load data from a file. var err = config.load("user://scores.cfg")

\# If the file didn't load, ignore it. if err != OK: return

\# Iterate over all sections. for player in config.get\_sections(): \#
Fetch the data for each section. var player\_name =
config.get\_value(player, "player\_name") var player\_score =
config.get\_value(player, "best\_score") score\_data\[player\_name\] =
player\_score

csharp

var score\_data = new Godot.Collections.Dictionary(); var config = new
ConfigFile();

// Load data from a file. Error err = config.Load("user://scores.cfg");

// If the file didn't load, ignore it. if (err != Error.Ok) { return; }

// Iterate over all sections. foreach (String player in
config.GetSections()) { // Fetch the data for each section. var
player\_name = (String)config.GetValue(player, "player\_name"); var
player\_score = (int)config.GetValue(player, "best\_score");
score\_data\[player\_name\] = player\_score; }

Any operation that mutates the ConfigFile such as
`set_value<class_ConfigFile_method_set_value>`,
`clear<class_ConfigFile_method_clear>`, or
`erase_section<class_ConfigFile_method_erase_section>`, only changes
what is loaded in memory. If you want to write the change to a file, you
have to save the changes with `save<class_ConfigFile_method_save>`,
`save_encrypted<class_ConfigFile_method_save_encrypted>`, or
`save_encrypted_pass<class_ConfigFile_method_save_encrypted_pass>`.

Keep in mind that section and property names can't contain spaces.
Anything after a space will be ignored on save and on load.

ConfigFiles can also contain manually written comment lines starting
with a semicolon (`;`). Those lines will be ignored when parsing the
file. Note that comments will be lost when saving the ConfigFile. This
can still be useful for dedicated server configuration files, which are
typically never overwritten without explicit user action.

\*\*Note:\*\* The file extension given to a ConfigFile does not have any
impact on its formatting or behavior. By convention, the `.cfg`
extension is used here, but any other extension such as `.ini` is also
valid. Since neither `.cfg` nor `.ini` are standardized, Godot's
ConfigFile formatting may differ from files written by other programs.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **clear**()
`🔗<class_ConfigFile_method_clear>`

Removes the entire contents of the config.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **encode\_to\_text**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ConfigFile_method_encode_to_text>`

Obtain the text version of this config file (the same text that would be
written to a file).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase\_section**(section:
`String<class_String>`) `🔗<class_ConfigFile_method_erase_section>`

Deletes the specified section along with all the key-value pairs inside.
Raises an error if the section does not exist.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase\_section\_key**(section:
`String<class_String>`, key: `String<class_String>`)
`🔗<class_ConfigFile_method_erase_section_key>`

Deletes the specified key in a section. Raises an error if either the
section or the key do not exist.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_section\_keys**(section: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ConfigFile_method_get_section_keys>`

Returns an array of all defined key identifiers in the specified
section. Raises an error and returns an empty array if the section does
not exist.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_sections**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ConfigFile_method_get_sections>`

Returns an array of all defined section identifiers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_value**(section: `String<class_String>`,
key: `String<class_String>`, default: `Variant<class_Variant>` = null)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ConfigFile_method_get_value>`

Returns the current value for the specified section and key. If either
the section or the key do not exist, the method returns the fallback
`default` value. If `default` is not specified or set to `null`, an
error is also raised.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_section**(section: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ConfigFile_method_has_section>`

Returns `true` if the specified section exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_section\_key**(section:
`String<class_String>`, key: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ConfigFile_method_has_section_key>`

Returns `true` if the specified section-key pair exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load**(path: `String<class_String>`)
`🔗<class_ConfigFile_method_load>`

Loads the config file specified as a parameter. The file's contents are
parsed and loaded in the **ConfigFile** object which the method was
called on.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success, or
one of the other `Error<enum_@GlobalScope_Error>` values if the
operation failed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load\_encrypted**(path:
`String<class_String>`, key: `PackedByteArray<class_PackedByteArray>`)
`🔗<class_ConfigFile_method_load_encrypted>`

Loads the encrypted config file specified as a parameter, using the
provided `key` to decrypt it. The file's contents are parsed and loaded
in the **ConfigFile** object which the method was called on.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success, or
one of the other `Error<enum_@GlobalScope_Error>` values if the
operation failed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load\_encrypted\_pass**(path:
`String<class_String>`, password: `String<class_String>`)
`🔗<class_ConfigFile_method_load_encrypted_pass>`

Loads the encrypted config file specified as a parameter, using the
provided `password` to decrypt it. The file's contents are parsed and
loaded in the **ConfigFile** object which the method was called on.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success, or
one of the other `Error<enum_@GlobalScope_Error>` values if the
operation failed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **parse**(data: `String<class_String>`)
`🔗<class_ConfigFile_method_parse>`

Parses the passed string as the contents of a config file. The string is
parsed and loaded in the ConfigFile object which the method was called
on.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success, or
one of the other `Error<enum_@GlobalScope_Error>` values if the
operation failed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **save**(path: `String<class_String>`)
`🔗<class_ConfigFile_method_save>`

Saves the contents of the **ConfigFile** object to the file specified as
a parameter. The output file uses an INI-style structure.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success, or
one of the other `Error<enum_@GlobalScope_Error>` values if the
operation failed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **save\_encrypted**(path:
`String<class_String>`, key: `PackedByteArray<class_PackedByteArray>`)
`🔗<class_ConfigFile_method_save_encrypted>`

Saves the contents of the **ConfigFile** object to the AES-256 encrypted
file specified as a parameter, using the provided `key` to encrypt it.
The output file uses an INI-style structure.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success, or
one of the other `Error<enum_@GlobalScope_Error>` values if the
operation failed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **save\_encrypted\_pass**(path:
`String<class_String>`, password: `String<class_String>`)
`🔗<class_ConfigFile_method_save_encrypted_pass>`

Saves the contents of the **ConfigFile** object to the AES-256 encrypted
file specified as a parameter, using the provided `password` to encrypt
it. The output file uses an INI-style structure.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success, or
one of the other `Error<enum_@GlobalScope_Error>` values if the
operation failed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_value**(section:
`String<class_String>`, key: `String<class_String>`, value:
`Variant<class_Variant>`) `🔗<class_ConfigFile_method_set_value>`

Assigns a value to the specified key of the specified section. If either
the section or the key do not exist, they are created. Passing a `null`
value deletes the specified key if it exists, and deletes the section if
it ends up empty once the key has been removed.
