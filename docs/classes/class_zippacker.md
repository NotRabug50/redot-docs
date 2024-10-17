github\_url  
hide

# ZIPPacker

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Allows the creation of zip files.

classref-introduction-group

## Description

This class implements a writer that allows storing the multiple blobs in
a zip archive.

    func write_zip_file():
        var writer := ZIPPacker.new()
        var err := writer.open("user://archive.zip")
        if err != OK:
            return err
        writer.start_file("hello.txt")
        writer.write_file("Hello World".to_utf8_buffer())
        writer.close_file()

        writer.close()
        return OK

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

## Enumerations

classref-enumeration

enum **ZipAppend**: `🔗<enum_ZIPPacker_ZipAppend>`

classref-enumeration-constant

`ZipAppend<enum_ZIPPacker_ZipAppend>` **APPEND\_CREATE** = `0`

Create a new zip archive at the given path.

classref-enumeration-constant

`ZipAppend<enum_ZIPPacker_ZipAppend>` **APPEND\_CREATEAFTER** = `1`

Append a new zip archive to the end of the already existing file at the
given path.

classref-enumeration-constant

`ZipAppend<enum_ZIPPacker_ZipAppend>` **APPEND\_ADDINZIP** = `2`

Add new files to the existing zip archive at the given path.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **close**()
`🔗<class_ZIPPacker_method_close>`

Closes the underlying resources used by this instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **close\_file**()
`🔗<class_ZIPPacker_method_close_file>`

Stops writing to a file within the archive.

It will fail if there is no open file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **open**(path: `String<class_String>`,
append: `ZipAppend<enum_ZIPPacker_ZipAppend>` = 0)
`🔗<class_ZIPPacker_method_open>`

Opens a zip file for writing at the given path using the specified write
mode.

This must be called before everything else.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **start\_file**(path:
`String<class_String>`) `🔗<class_ZIPPacker_method_start_file>`

Starts writing to a file within the archive. Only one file can be
written at the same time.

Must be called after `open<class_ZIPPacker_method_open>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **write\_file**(data:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_ZIPPacker_method_write_file>`

Write the given `data` to the file.

Needs to be called after
`start_file<class_ZIPPacker_method_start_file>`.
