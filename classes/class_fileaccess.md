github\_url  
hide

# FileAccess

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides methods for file reading and writing operations.

classref-introduction-group

## Description

This class can be used to permanently store data in the user device's
file system and to read from it. This is useful for store game save data
or player configuration files.

Here's a sample on how to write and read from a file:

gdscript

func save\_to\_file(content):  
var file = FileAccess.open("user://save\_game.dat", FileAccess.WRITE)
file.store\_string(content)

func load\_from\_file():  
var file = FileAccess.open("user://save\_game.dat", FileAccess.READ) var
content = file.get\_as\_text() return content

csharp

public void SaveToFile(string content) { using var file =
FileAccess.Open("user://save\_game.dat", FileAccess.ModeFlags.Write);
file.StoreString(content); }

public string LoadFromFile() { using var file =
FileAccess.Open("user://save\_game.dat", FileAccess.ModeFlags.Read);
string content = file.GetAsText(); return content; }

In the example above, the file will be saved in the user data folder as
specified in the `Data paths <../tutorials/io/data_paths>`
documentation.

\*\*FileAccess\*\* will close when it's freed, which happens when it
goes out of scope or when it gets assigned with `null`.
`close<class_FileAccess_method_close>` can be used to close it before
then explicitly. In C# the reference must be disposed manually, which
can be done with the `using` statement or by calling the `Dispose`
method directly.

\*\*Note:\*\* To access project resources once exported, it is
recommended to use `ResourceLoader<class_ResourceLoader>` instead of
**FileAccess**, as some files are converted to engine-specific formats
and their original source files might not be present in the exported PCK
package.

\*\*Note:\*\* Files are automatically closed only if the process exits
"normally" (such as by clicking the window manager's close button or
pressing **Alt + F4**). If you stop the project execution by pressing
**F8** while the project is running, the file won't be closed as the
game process will be killed. You can work around this by calling
`flush<class_FileAccess_method_flush>` at regular intervals.

classref-introduction-group

## Tutorials

-   `File system <../tutorials/scripting/filesystem>`
-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`
-   [3D Voxel Demo](https://godotengine.org/asset-library/asset/2755)

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

enum **ModeFlags**: `🔗<enum_FileAccess_ModeFlags>`

classref-enumeration-constant

`ModeFlags<enum_FileAccess_ModeFlags>` **READ** = `1`

Opens the file for read operations. The cursor is positioned at the
beginning of the file.

classref-enumeration-constant

`ModeFlags<enum_FileAccess_ModeFlags>` **WRITE** = `2`

Opens the file for write operations. The file is created if it does not
exist, and truncated if it does.

\*\*Note:\*\* When creating a file it must be in an already existing
directory. To recursively create directories for a file path, see
`DirAccess.make_dir_recursive<class_DirAccess_method_make_dir_recursive>`.

classref-enumeration-constant

`ModeFlags<enum_FileAccess_ModeFlags>` **READ\_WRITE** = `3`

Opens the file for read and write operations. Does not truncate the
file. The cursor is positioned at the beginning of the file.

classref-enumeration-constant

`ModeFlags<enum_FileAccess_ModeFlags>` **WRITE\_READ** = `7`

Opens the file for read and write operations. The file is created if it
does not exist, and truncated if it does. The cursor is positioned at
the beginning of the file.

\*\*Note:\*\* When creating a file it must be in an already existing
directory. To recursively create directories for a file path, see
`DirAccess.make_dir_recursive<class_DirAccess_method_make_dir_recursive>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CompressionMode**: `🔗<enum_FileAccess_CompressionMode>`

classref-enumeration-constant

`CompressionMode<enum_FileAccess_CompressionMode>`
**COMPRESSION\_FASTLZ** = `0`

Uses the [FastLZ](https://fastlz.org/) compression method.

classref-enumeration-constant

`CompressionMode<enum_FileAccess_CompressionMode>`
**COMPRESSION\_DEFLATE** = `1`

Uses the [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) compression
method.

classref-enumeration-constant

`CompressionMode<enum_FileAccess_CompressionMode>` **COMPRESSION\_ZSTD**
= `2`

Uses the [Zstandard](https://facebook.github.io/zstd/) compression
method.

classref-enumeration-constant

`CompressionMode<enum_FileAccess_CompressionMode>` **COMPRESSION\_GZIP**
= `3`

Uses the [gzip](https://www.gzip.org/) compression method.

classref-enumeration-constant

`CompressionMode<enum_FileAccess_CompressionMode>`
**COMPRESSION\_BROTLI** = `4`

Uses the [brotli](https://github.com/google/brotli) compression method
(only decompression is supported).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **UnixPermissionFlags**: `🔗<enum_FileAccess_UnixPermissionFlags>`

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_READ\_OWNER** = `256`

Read for owner bit.

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_WRITE\_OWNER** = `128`

Write for owner bit.

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_EXECUTE\_OWNER** = `64`

Execute for owner bit.

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_READ\_GROUP** = `32`

Read for group bit.

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_WRITE\_GROUP** = `16`

Write for group bit.

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_EXECUTE\_GROUP** = `8`

Execute for group bit.

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_READ\_OTHER** = `4`

Read for other bit.

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_WRITE\_OTHER** = `2`

Write for other bit.

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_EXECUTE\_OTHER** = `1`

Execute for other bit.

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_SET\_USER\_ID** = `2048`

Set user id on execution bit.

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_SET\_GROUP\_ID** = `1024`

Set group id on execution bit.

classref-enumeration-constant

`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`
**UNIX\_RESTRICTED\_DELETE** = `512`

Restricted deletion (sticky) bit.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **big\_endian**
`🔗<class_FileAccess_property_big_endian>`

classref-property-setget

-   `void (No return value.)` **set\_big\_endian**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_big\_endian**()

If `true`, the file is read with big-endian
[endianness](https://en.wikipedia.org/wiki/Endianness). If `false`, the
file is read with little-endian endianness. If in doubt, leave this to
`false` as most files are written with little-endian endianness.

\*\*Note:\*\* `big_endian<class_FileAccess_property_big_endian>` is only
about the file format, not the CPU type. The CPU endianness doesn't
affect the default endianness for files written.

\*\*Note:\*\* This is always reset to `false` whenever you open the
file. Therefore, you must set
`big_endian<class_FileAccess_property_big_endian>` *after* opening the
file, not before.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **close**()
`🔗<class_FileAccess_method_close>`

Closes the currently opened file and prevents subsequent read/write
operations. Use `flush<class_FileAccess_method_flush>` to persist the
data to disk without closing the file.

\*\*Note:\*\* **FileAccess** will automatically close when it's freed,
which happens when it goes out of scope or when it gets assigned with
`null`. In C# the reference must be disposed after we are done using it,
this can be done with the `using` statement or calling the `Dispose`
method directly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **eof\_reached**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_eof_reached>`

Returns `true` if the file cursor has already read past the end of the
file.

\*\*Note:\*\* `eof_reached() == false` cannot be used to check whether
there is more data available. To loop while there is more data
available, use:

gdscript

while file.get\_position() &lt; file.get\_length():  
\# Read data

csharp

while (file.GetPosition() &lt; file.GetLength()) { // Read data }

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **file\_exists**(path: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_file_exists>`

Returns `true` if the file exists in the given path.

\*\*Note:\*\* Many resources types are imported (e.g. textures or sound
files), and their source asset will not be included in the exported
game, as only the imported version is used. See
`ResourceLoader.exists<class_ResourceLoader_method_exists>` for an
alternative approach that takes resource remapping into account.

For a non-static, relative equivalent, use
`DirAccess.file_exists<class_DirAccess_method_file_exists>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **flush**()
`🔗<class_FileAccess_method_flush>`

Writes the file's buffer to disk. Flushing is automatically performed
when the file is closed. This means you don't need to call
`flush<class_FileAccess_method_flush>` manually before closing a file.
Still, calling `flush<class_FileAccess_method_flush>` can be used to
ensure the data is safe even if the project crashes instead of being
closed gracefully.

\*\*Note:\*\* Only call `flush<class_FileAccess_method_flush>` when you
actually need it. Otherwise, it will decrease performance due to
constant disk writes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_8**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_8>`

Returns the next 8 bits from the file as an integer. See
`store_8<class_FileAccess_method_store_8>` for details on what values
can be stored and retrieved this way.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_16**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_16>`

Returns the next 16 bits from the file as an integer. See
`store_16<class_FileAccess_method_store_16>` for details on what values
can be stored and retrieved this way.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_32**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_32>`

Returns the next 32 bits from the file as an integer. See
`store_32<class_FileAccess_method_store_32>` for details on what values
can be stored and retrieved this way.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_64**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_64>`

Returns the next 64 bits from the file as an integer. See
`store_64<class_FileAccess_method_store_64>` for details on what values
can be stored and retrieved this way.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_as\_text**(skip\_cr: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_as_text>`

Returns the whole file as a `String<class_String>`. Text is interpreted
as being UTF-8 encoded.

If `skip_cr` is `true`, carriage return characters (`\r`, CR) will be
ignored when parsing the UTF-8, so that only line feed characters (`\n`,
LF) represent a new line (Unix convention).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **get\_buffer**(length:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_buffer>`

Returns next `length` bytes of the file as a
`PackedByteArray<class_PackedByteArray>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_csv\_line**(delim:
`String<class_String>` = ",")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_csv_line>`

Returns the next value of the file in CSV (Comma-Separated Values)
format. You can pass a different delimiter `delim` to use other than the
default `","` (comma). This delimiter must be one-character long, and
cannot be a double quotation mark.

Text is interpreted as being UTF-8 encoded. Text values must be enclosed
in double quotes if they include the delimiter character. Double quotes
within a text value can be escaped by doubling their occurrence.

For example, the following CSV lines are valid and will be properly
parsed as two strings each:

    Alice,"Hello, Bob!"
    Bob,Alice! What a surprise!
    Alice,"I thought you'd reply with ""Hello, world""."

Note how the second line can omit the enclosing quotes as it does not
include the delimiter. However it *could* very well use quotes, it was
only written without for demonstration purposes. The third line must use
`""` for each quotation mark that needs to be interpreted as such
instead of the end of a text value.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_double**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_double>`

Returns the next 64 bits from the file as a floating-point number.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **get\_error**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_error>`

Returns the last error that happened when trying to perform operations.
Compare with the `ERR_FILE_*` constants from
`Error<enum_@GlobalScope_Error>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **get\_file\_as\_bytes**(path:
`String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_get_file_as_bytes>`

Returns the whole `path` file contents as a
`PackedByteArray<class_PackedByteArray>` without any decoding.

Returns an empty `PackedByteArray<class_PackedByteArray>` if an error
occurred while opening the file. You can use
`get_open_error<class_FileAccess_method_get_open_error>` to check the
error that occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_file\_as\_string**(path:
`String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_get_file_as_string>`

Returns the whole `path` file contents as a `String<class_String>`. Text
is interpreted as being UTF-8 encoded.

Returns an empty `String<class_String>` if an error occurred while
opening the file. You can use
`get_open_error<class_FileAccess_method_get_open_error>` to check the
error that occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_float**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_float>`

Returns the next 32 bits from the file as a floating-point number.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_hidden\_attribute**(file:
`String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_get_hidden_attribute>`

Returns `true`, if file `hidden` attribute is set.

\*\*Note:\*\* This method is implemented on iOS, BSD, macOS, and
Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_length**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_length>`

Returns the size of the file in bytes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_line**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_line>`

Returns the next line of the file as a `String<class_String>`. The
returned string doesn't include newline (`\n`) or carriage return (`\r`)
characters, but does include any other leading or trailing whitespace.

Text is interpreted as being UTF-8 encoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_md5**(path: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_get_md5>`

Returns an MD5 String representing the file at the given path or an
empty `String<class_String>` on failure.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_modified\_time**(file: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_get_modified_time>`

Returns the last time the `file` was modified in Unix timestamp format,
or `0` on error. This Unix timestamp can be converted to another format
using the `Time<class_Time>` singleton.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **get\_open\_error**()
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_get_open_error>`

Returns the result of the last `open<class_FileAccess_method_open>` call
in the current thread.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_pascal\_string**()
`🔗<class_FileAccess_method_get_pascal_string>`

Returns a `String<class_String>` saved in Pascal format from the file.

Text is interpreted as being UTF-8 encoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_path**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_path>`

Returns the path as a `String<class_String>` for the current open file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_path\_absolute**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_path_absolute>`

Returns the absolute path as a `String<class_String>` for the current
open file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_position**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_position>`

Returns the file cursor's position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_read\_only\_attribute**(file:
`String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_get_read_only_attribute>`

Returns `true`, if file `read only` attribute is set.

\*\*Note:\*\* This method is implemented on iOS, BSD, macOS, and
Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_real**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_real>`

Returns the next bits from the file as a floating-point number.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_sha256**(path: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_get_sha256>`

Returns an SHA-256 `String<class_String>` representing the file at the
given path or an empty `String<class_String>` on failure.

classref-item-separator

------------------------------------------------------------------------

classref-method

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`\]
**get\_unix\_permissions**(file: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_get_unix_permissions>`

Returns file UNIX permissions.

\*\*Note:\*\* This method is implemented on iOS, Linux/BSD, and macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_var**(allow\_objects: `bool<class_bool>`
= false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_get_var>`

Returns the next `Variant<class_Variant>` value from the file. If
`allow_objects` is `true`, decoding objects is allowed.

Internally, this uses the same decoding mechanism as the
`@GlobalScope.bytes_to_var<class_@GlobalScope_method_bytes_to_var>`
method.

\*\*Warning:\*\* Deserialized objects can contain code which gets
executed. Do not use this option if the serialized object comes from
untrusted sources to avoid potential security threats such as remote
code execution.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_open**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileAccess_method_is_open>`

Returns `true` if the file is currently opened.

classref-item-separator

------------------------------------------------------------------------

classref-method

`FileAccess<class_FileAccess>` **open**(path: `String<class_String>`,
flags: `ModeFlags<enum_FileAccess_ModeFlags>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_open>`

Creates a new **FileAccess** object and opens the file for writing or
reading, depending on the flags.

Returns `null` if opening the file failed. You can use
`get_open_error<class_FileAccess_method_get_open_error>` to check the
error that occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`FileAccess<class_FileAccess>` **open\_compressed**(path:
`String<class_String>`, mode\_flags:
`ModeFlags<enum_FileAccess_ModeFlags>`, compression\_mode:
`CompressionMode<enum_FileAccess_CompressionMode>` = 0)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_open_compressed>`

Creates a new **FileAccess** object and opens a compressed file for
reading or writing.

\*\*Note:\*\* `open_compressed<class_FileAccess_method_open_compressed>`
can only read files that were saved by Godot, not third-party
compression formats. See [GitHub issue
\#28999](https://github.com/godotengine/godot/issues/28999) for a
workaround.

Returns `null` if opening the file failed. You can use
`get_open_error<class_FileAccess_method_get_open_error>` to check the
error that occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`FileAccess<class_FileAccess>` **open\_encrypted**(path:
`String<class_String>`, mode\_flags:
`ModeFlags<enum_FileAccess_ModeFlags>`, key:
`PackedByteArray<class_PackedByteArray>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_open_encrypted>`

Creates a new **FileAccess** object and opens an encrypted file in write
or read mode. You need to pass a binary key to encrypt/decrypt it.

\*\*Note:\*\* The provided key must be 32 bytes long.

Returns `null` if opening the file failed. You can use
`get_open_error<class_FileAccess_method_get_open_error>` to check the
error that occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`FileAccess<class_FileAccess>` **open\_encrypted\_with\_pass**(path:
`String<class_String>`, mode\_flags:
`ModeFlags<enum_FileAccess_ModeFlags>`, pass: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_open_encrypted_with_pass>`

Creates a new **FileAccess** object and opens an encrypted file in write
or read mode. You need to pass a password to encrypt/decrypt it.

Returns `null` if opening the file failed. You can use
`get_open_error<class_FileAccess_method_get_open_error>` to check the
error that occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **resize**(length: `int<class_int>`)
`🔗<class_FileAccess_method_resize>`

Resizes the file to a specified length. The file must be open in a mode
that permits writing. If the file is extended, NUL characters are
appended. If the file is truncated, all data from the end file to the
original length of the file is lost.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **seek**(position: `int<class_int>`)
`🔗<class_FileAccess_method_seek>`

Changes the file reading/writing cursor to the specified position (in
bytes from the beginning of the file).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **seek\_end**(position: `int<class_int>` = 0)
`🔗<class_FileAccess_method_seek_end>`

Changes the file reading/writing cursor to the specified position (in
bytes from the end of the file).

\*\*Note:\*\* This is an offset, so you should use negative numbers or
the cursor will be at the end of the file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **set\_hidden\_attribute**(file:
`String<class_String>`, hidden: `bool<class_bool>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_set_hidden_attribute>`

Sets file **hidden** attribute.

\*\*Note:\*\* This method is implemented on iOS, BSD, macOS, and
Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **set\_read\_only\_attribute**(file:
`String<class_String>`, ro: `bool<class_bool>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_set_read_only_attribute>`

Sets file **read only** attribute.

\*\*Note:\*\* This method is implemented on iOS, BSD, macOS, and
Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **set\_unix\_permissions**(file:
`String<class_String>`, permissions:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`UnixPermissionFlags<enum_FileAccess_UnixPermissionFlags>`\])
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_FileAccess_method_set_unix_permissions>`

Sets file UNIX permissions.

\*\*Note:\*\* This method is implemented on iOS, Linux/BSD, and macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_8**(value: `int<class_int>`)
`🔗<class_FileAccess_method_store_8>`

Stores an integer as 8 bits in the file.

\*\*Note:\*\* The `value` should lie in the interval `[0, 255]`. Any
other value will overflow and wrap around.

To store a signed integer, use
`store_64<class_FileAccess_method_store_64>`, or convert it manually
(see `store_16<class_FileAccess_method_store_16>` for an example).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_16**(value: `int<class_int>`)
`🔗<class_FileAccess_method_store_16>`

Stores an integer as 16 bits in the file.

\*\*Note:\*\* The `value` should lie in the interval `[0, 2^16 - 1]`.
Any other value will overflow and wrap around.

To store a signed integer, use
`store_64<class_FileAccess_method_store_64>` or store a signed integer
from the interval `[-2^15, 2^15 - 1]` (i.e. keeping one bit for the
signedness) and compute its sign manually when reading. For example:

gdscript

const MAX\_15B = 1 &lt;&lt; 15 const MAX\_16B = 1 &lt;&lt; 16

func unsigned16\_to\_signed(unsigned):  
return (unsigned + MAX\_15B) % MAX\_16B - MAX\_15B

func \_ready():  
var f = FileAccess.open("user://file.dat", FileAccess.WRITE\_READ)
f.store\_16(-42) \# This wraps around and stores 65494 (2^16 - 42).
f.store\_16(121) \# In bounds, will store 121. f.seek(0) \# Go back to
start to read the stored value. var read1 = f.get\_16() \# 65494 var
read2 = f.get\_16() \# 121 var converted1 =
unsigned16\_to\_signed(read1) \# -42 var converted2 =
unsigned16\_to\_signed(read2) \# 121

csharp

public override void \_Ready() { using var f =
FileAccess.Open("user://file.dat", FileAccess.ModeFlags.WriteRead);
f.Store16(unchecked((ushort)-42)); // This wraps around and stores 65494
(2^16 - 42). f.Store16(121); // In bounds, will store 121. f.Seek(0); //
Go back to start to read the stored value. ushort read1 = f.Get16(); //
65494 ushort read2 = f.Get16(); // 121 short converted1 = (short)read1;
// -42 short converted2 = (short)read2; // 121 }

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_32**(value: `int<class_int>`)
`🔗<class_FileAccess_method_store_32>`

Stores an integer as 32 bits in the file.

\*\*Note:\*\* The `value` should lie in the interval `[0, 2^32 - 1]`.
Any other value will overflow and wrap around.

To store a signed integer, use
`store_64<class_FileAccess_method_store_64>`, or convert it manually
(see `store_16<class_FileAccess_method_store_16>` for an example).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_64**(value: `int<class_int>`)
`🔗<class_FileAccess_method_store_64>`

Stores an integer as 64 bits in the file.

\*\*Note:\*\* The `value` must lie in the interval `[-2^63, 2^63 - 1]`
(i.e. be a valid `int<class_int>` value).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_buffer**(buffer:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_FileAccess_method_store_buffer>`

Stores the given array of bytes in the file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_csv\_line**(values:
`PackedStringArray<class_PackedStringArray>`, delim:
`String<class_String>` = ",")
`🔗<class_FileAccess_method_store_csv_line>`

Store the given `PackedStringArray<class_PackedStringArray>` in the file
as a line formatted in the CSV (Comma-Separated Values) format. You can
pass a different delimiter `delim` to use other than the default `","`
(comma). This delimiter must be one-character long.

Text will be encoded as UTF-8.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_double**(value: `float<class_float>`)
`🔗<class_FileAccess_method_store_double>`

Stores a floating-point number as 64 bits in the file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_float**(value: `float<class_float>`)
`🔗<class_FileAccess_method_store_float>`

Stores a floating-point number as 32 bits in the file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_line**(line: `String<class_String>`)
`🔗<class_FileAccess_method_store_line>`

Appends `line` to the file followed by a line return character (`\n`),
encoding the text as UTF-8.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_pascal\_string**(string:
`String<class_String>`)
`🔗<class_FileAccess_method_store_pascal_string>`

Stores the given `String<class_String>` as a line in the file in Pascal
format (i.e. also store the length of the string).

Text will be encoded as UTF-8.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_real**(value: `float<class_float>`)
`🔗<class_FileAccess_method_store_real>`

Stores a floating-point number in the file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_string**(string:
`String<class_String>`) `🔗<class_FileAccess_method_store_string>`

Appends `string` to the file without a line return, encoding the text as
UTF-8.

\*\*Note:\*\* This method is intended to be used to write text files.
The string is stored as a UTF-8 encoded buffer without string length or
terminating zero, which means that it can't be loaded back easily. If
you want to store a retrievable string in a binary file, consider using
`store_pascal_string<class_FileAccess_method_store_pascal_string>`
instead. For retrieving strings from a text file, you can use
`get_buffer(length).get_string_from_utf8()` (if you know the length) or
`get_as_text<class_FileAccess_method_get_as_text>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **store\_var**(value:
`Variant<class_Variant>`, full\_objects: `bool<class_bool>` = false)
`🔗<class_FileAccess_method_store_var>`

Stores any Variant value in the file. If `full_objects` is `true`,
encoding objects is allowed (and can potentially include code).

Internally, this uses the same encoding mechanism as the
`@GlobalScope.var_to_bytes<class_@GlobalScope_method_var_to_bytes>`
method.

\*\*Note:\*\* Not all properties are included. Only properties that are
configured with the
`@GlobalScope.PROPERTY_USAGE_STORAGE<class_@GlobalScope_constant_PROPERTY_USAGE_STORAGE>`
flag set will be serialized. You can add a new usage flag to a property
by overriding the
`Object._get_property_list<class_Object_private_method__get_property_list>`
method in your class. You can also check how property usage is
configured by calling
`Object._get_property_list<class_Object_private_method__get_property_list>`.
See `PropertyUsageFlags<enum_@GlobalScope_PropertyUsageFlags>` for the
possible usage flags.
