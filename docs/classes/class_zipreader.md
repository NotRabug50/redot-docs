github\_url  
hide

# ZIPReader

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Allows reading the content of a zip file.

classref-introduction-group

## Description

This class implements a reader that can extract the content of
individual files inside a zip archive.

    func read_zip_file():
        var reader := ZIPReader.new()
        var err := reader.open("user://archive.zip")
        if err != OK:
            return PackedByteArray()
        var res := reader.read_file("hello.txt")
        reader.close()
        return res

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **close**()
`🔗<class_ZIPReader_method_close>`

Closes the underlying resources used by this instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **file\_exists**(path: `String<class_String>`,
case\_sensitive: `bool<class_bool>` = true)
`🔗<class_ZIPReader_method_file_exists>`

Returns `true` if the file exists in the loaded zip archive.

Must be called after `open<class_ZIPReader_method_open>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_files**()
`🔗<class_ZIPReader_method_get_files>`

Returns the list of names of all files in the loaded archive.

Must be called after `open<class_ZIPReader_method_open>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **open**(path: `String<class_String>`)
`🔗<class_ZIPReader_method_open>`

Opens the zip archive at the given `path` and reads its file index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **read\_file**(path:
`String<class_String>`, case\_sensitive: `bool<class_bool>` = true)
`🔗<class_ZIPReader_method_read_file>`

Loads the whole content of a file in the loaded zip archive into memory
and returns it.

Must be called after `open<class_ZIPReader_method_open>`.
