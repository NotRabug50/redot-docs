github\_url  
hide

# DirAccess

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides methods for managing directories and their content.

classref-introduction-group

## Description

This class is used to manage directories and their content, even outside
of the project folder.

\*\*DirAccess\*\* can't be instantiated directly. Instead it is created
with a static method that takes a path for which it will be opened.

Most of the methods have a static alternative that can be used without
creating a **DirAccess**. Static methods only support absolute paths
(including `res://` and `user://`).

    # Standard
    var dir = DirAccess.open("user://levels")
    dir.make_dir("world1")
    # Static
    DirAccess.make_dir_absolute("user://levels/world1")

\*\*Note:\*\* Many resources types are imported (e.g. textures or sound
files), and their source asset will not be included in the exported
game, as only the imported version is used. Use
`ResourceLoader<class_ResourceLoader>` to access imported resources.

Here is an example on how to iterate through the files of a directory:

gdscript

func dir\_contents(path):  
var dir = DirAccess.open(path) if dir: dir.list\_dir\_begin() var
file\_name = dir.get\_next() while file\_name != "": if
dir.current\_is\_dir(): print("Found directory: " + file\_name) else:
print("Found file: " + file\_name) file\_name = dir.get\_next() else:
print("An error occurred when trying to access the path.")

csharp

public void DirContents(string path) { using var dir =
DirAccess.Open(path); if (dir != null) { dir.ListDirBegin(); string
fileName = dir.GetNext(); while (fileName != "") { if
(dir.CurrentIsDir()) { GD.Print($"Found directory: {fileName}"); } else
{ GD.Print($"Found file: {fileName}"); } fileName = dir.GetNext(); } }
else { GD.Print("An error occurred when trying to access the path."); }
}

classref-introduction-group

## Tutorials

-   `File system <../tutorials/scripting/filesystem>`

classref-reftable-group

## Properties

<table>
<tbody>
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **include\_hidden**
`🔗<class_DirAccess_property_include_hidden>`

classref-property-setget

-   `void (No return value.)` **set\_include\_hidden**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_include\_hidden**()

If `true`, hidden files are included when navigating the directory.

Affects `list_dir_begin<class_DirAccess_method_list_dir_begin>`,
`get_directories<class_DirAccess_method_get_directories>` and
`get_files<class_DirAccess_method_get_files>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **include\_navigational**
`🔗<class_DirAccess_property_include_navigational>`

classref-property-setget

-   `void (No return value.)` **set\_include\_navigational**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_include\_navigational**()

If `true`, `.` and `..` are included when navigating the directory.

Affects `list_dir_begin<class_DirAccess_method_list_dir_begin>` and
`get_directories<class_DirAccess_method_get_directories>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **change\_dir**(to\_dir:
`String<class_String>`) `🔗<class_DirAccess_method_change_dir>`

Changes the currently opened directory to the one passed as an argument.
The argument can be relative to the current directory (e.g. `newdir` or
`../newdir`), or an absolute path (e.g. `/tmp/newdir` or
`res://somedir/newdir`).

Returns one of the `Error<enum_@GlobalScope_Error>` code constants
(`@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success).

\*\*Note:\*\* The new directory must be within the same scope, e.g. when
you had opened a directory inside `res://`, you can't change it to
`user://` directory. If you need to open a directory in another access
scope, use `open<class_DirAccess_method_open>` to create a new instance
instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **copy**(from: `String<class_String>`,
to: `String<class_String>`, chmod\_flags: `int<class_int>` = -1)
`🔗<class_DirAccess_method_copy>`

Copies the `from` file to the `to` destination. Both arguments should be
paths to files, either relative or absolute. If the destination file
exists and is not access-protected, it will be overwritten.

If `chmod_flags` is different than `-1`, the Unix permissions for the
destination path will be set to the provided value, if available on the
current operating system.

Returns one of the `Error<enum_@GlobalScope_Error>` code constants
(`@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **copy\_absolute**(from:
`String<class_String>`, to: `String<class_String>`, chmod\_flags:
`int<class_int>` = -1)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_copy_absolute>`

Static version of `copy<class_DirAccess_method_copy>`. Supports only
absolute paths.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **create\_link**(source:
`String<class_String>`, target: `String<class_String>`)
`🔗<class_DirAccess_method_create_link>`

Creates symbolic link between files or folders.

\*\*Note:\*\* On Windows, this method works only if the application is
running with elevated privileges or Developer Mode is enabled.

\*\*Note:\*\* This method is implemented on macOS, Linux, and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **current\_is\_dir**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DirAccess_method_current_is_dir>`

Returns whether the current item processed with the last
`get_next<class_DirAccess_method_get_next>` call is a directory (`.` and
`..` are considered directories).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **dir\_exists**(path: `String<class_String>`)
`🔗<class_DirAccess_method_dir_exists>`

Returns whether the target directory exists. The argument can be
relative to the current directory, or an absolute path.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **dir\_exists\_absolute**(path:
`String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_dir_exists_absolute>`

Static version of `dir_exists<class_DirAccess_method_dir_exists>`.
Supports only absolute paths.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **file\_exists**(path: `String<class_String>`)
`🔗<class_DirAccess_method_file_exists>`

Returns whether the target file exists. The argument can be relative to
the current directory, or an absolute path.

For a static equivalent, use
`FileAccess.file_exists<class_FileAccess_method_file_exists>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_current\_dir**(include\_drive:
`bool<class_bool>` = true)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DirAccess_method_get_current_dir>`

Returns the absolute path to the currently opened directory (e.g.
`res://folder` or `C:\tmp\folder`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_current\_drive**()
`🔗<class_DirAccess_method_get_current_drive>`

Returns the currently opened directory's drive index. See
`get_drive_name<class_DirAccess_method_get_drive_name>` to convert
returned index to the name of the drive.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_directories**()
`🔗<class_DirAccess_method_get_directories>`

Returns a `PackedStringArray<class_PackedStringArray>` containing
filenames of the directory contents, excluding files. The array is
sorted alphabetically.

Affected by `include_hidden<class_DirAccess_property_include_hidden>`
and
`include_navigational<class_DirAccess_property_include_navigational>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_directories\_at**(path: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_get_directories_at>`

Returns a `PackedStringArray<class_PackedStringArray>` containing
filenames of the directory contents, excluding files, at the given
`path`. The array is sorted alphabetically.

Use `get_directories<class_DirAccess_method_get_directories>` if you
want more control of what gets included.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_drive\_count**()
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_get_drive_count>`

On Windows, returns the number of drives (partitions) mounted on the
current filesystem.

On macOS, returns the number of mounted volumes.

On Linux, returns the number of mounted volumes and GTK 3 bookmarks.

On other platforms, the method returns 0.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_drive\_name**(idx: `int<class_int>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_get_drive_name>`

On Windows, returns the name of the drive (partition) passed as an
argument (e.g. `C:`).

On macOS, returns the path to the mounted volume passed as an argument.

On Linux, returns the path to the mounted volume or GTK 3 bookmark
passed as an argument.

On other platforms, or if the requested drive does not exist, the method
returns an empty String.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_files**()
`🔗<class_DirAccess_method_get_files>`

Returns a `PackedStringArray<class_PackedStringArray>` containing
filenames of the directory contents, excluding directories. The array is
sorted alphabetically.

Affected by `include_hidden<class_DirAccess_property_include_hidden>`.

\*\*Note:\*\* When used on a `res://` path in an exported project, only
the files actually included in the PCK at the given folder level are
returned. In practice, this means that since imported resources are
stored in a top-level `.godot/` folder, only paths to `*.gd` and
`*.import` files are returned (plus a few files such as `project.godot`
or `project.binary` and the project icon). In an exported project, the
list of returned files will also vary depending on whether
`ProjectSettings.editor/export/convert_text_resources_to_binary<class_ProjectSettings_property_editor/export/convert_text_resources_to_binary>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_files\_at**(path:
`String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_get_files_at>`

Returns a `PackedStringArray<class_PackedStringArray>` containing
filenames of the directory contents, excluding directories, at the given
`path`. The array is sorted alphabetically.

Use `get_files<class_DirAccess_method_get_files>` if you want more
control of what gets included.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_next**()
`🔗<class_DirAccess_method_get_next>`

Returns the next element (file or directory) in the current directory.

The name of the file or directory is returned (and not its full path).
Once the stream has been fully processed, the method returns an empty
`String<class_String>` and closes the stream automatically (i.e.
`list_dir_end<class_DirAccess_method_list_dir_end>` would not be
mandatory in such a case).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **get\_open\_error**()
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_get_open_error>`

Returns the result of the last `open<class_DirAccess_method_open>` call
in the current thread.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_space\_left**()
`🔗<class_DirAccess_method_get_space_left>`

Returns the available space on the current directory's disk, in bytes.
Returns `0` if the platform-specific method to query the available space
fails.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_case\_sensitive**(path: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_DirAccess_method_is_case_sensitive>`

Returns `true` if the file system or directory use case sensitive file
names.

\*\*Note:\*\* This method is implemented on macOS, Linux (for EXT4 and
F2FS filesystems only) and Windows. On other platforms, it always
returns `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_link**(path: `String<class_String>`)
`🔗<class_DirAccess_method_is_link>`

Returns `true` if the file or directory is a symbolic link, directory
junction, or other reparse point.

\*\*Note:\*\* This method is implemented on macOS, Linux, and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **list\_dir\_begin**()
`🔗<class_DirAccess_method_list_dir_begin>`

Initializes the stream used to list all files and directories using the
`get_next<class_DirAccess_method_get_next>` function, closing the
currently opened stream if needed. Once the stream has been processed,
it should typically be closed with
`list_dir_end<class_DirAccess_method_list_dir_end>`.

Affected by `include_hidden<class_DirAccess_property_include_hidden>`
and
`include_navigational<class_DirAccess_property_include_navigational>`.

\*\*Note:\*\* The order of files and directories returned by this method
is not deterministic, and can vary between operating systems. If you
want a list of all files or folders sorted alphabetically, use
`get_files<class_DirAccess_method_get_files>` or
`get_directories<class_DirAccess_method_get_directories>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **list\_dir\_end**()
`🔗<class_DirAccess_method_list_dir_end>`

Closes the current stream opened with
`list_dir_begin<class_DirAccess_method_list_dir_begin>` (whether it has
been fully processed with `get_next<class_DirAccess_method_get_next>`
does not matter).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **make\_dir**(path:
`String<class_String>`) `🔗<class_DirAccess_method_make_dir>`

Creates a directory. The argument can be relative to the current
directory, or an absolute path. The target directory should be placed in
an already existing directory (to create the full path recursively, see
`make_dir_recursive<class_DirAccess_method_make_dir_recursive>`).

Returns one of the `Error<enum_@GlobalScope_Error>` code constants
(`@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **make\_dir\_absolute**(path:
`String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_make_dir_absolute>`

Static version of `make_dir<class_DirAccess_method_make_dir>`. Supports
only absolute paths.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **make\_dir\_recursive**(path:
`String<class_String>`) `🔗<class_DirAccess_method_make_dir_recursive>`

Creates a target directory and all necessary intermediate directories in
its path, by calling `make_dir<class_DirAccess_method_make_dir>`
recursively. The argument can be relative to the current directory, or
an absolute path.

Returns one of the `Error<enum_@GlobalScope_Error>` code constants
(`@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**make\_dir\_recursive\_absolute**(path: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_make_dir_recursive_absolute>`

Static version of
`make_dir_recursive<class_DirAccess_method_make_dir_recursive>`.
Supports only absolute paths.

classref-item-separator

------------------------------------------------------------------------

classref-method

`DirAccess<class_DirAccess>` **open**(path: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_open>`

Creates a new **DirAccess** object and opens an existing directory of
the filesystem. The `path` argument can be within the project tree
(`res://folder`), the user directory (`user://folder`) or an absolute
path of the user filesystem (e.g. `/tmp/folder` or `C:\tmp\folder`).

Returns `null` if opening the directory failed. You can use
`get_open_error<class_DirAccess_method_get_open_error>` to check the
error that occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **read\_link**(path: `String<class_String>`)
`🔗<class_DirAccess_method_read_link>`

Returns target of the symbolic link.

\*\*Note:\*\* This method is implemented on macOS, Linux, and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **remove**(path:
`String<class_String>`) `🔗<class_DirAccess_method_remove>`

Permanently deletes the target file or an empty directory. The argument
can be relative to the current directory, or an absolute path. If the
target directory is not empty, the operation will fail.

If you don't want to delete the file/directory permanently, use
`OS.move_to_trash<class_OS_method_move_to_trash>` instead.

Returns one of the `Error<enum_@GlobalScope_Error>` code constants
(`@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **remove\_absolute**(path:
`String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_remove_absolute>`

Static version of `remove<class_DirAccess_method_remove>`. Supports only
absolute paths.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **rename**(from:
`String<class_String>`, to: `String<class_String>`)
`🔗<class_DirAccess_method_rename>`

Renames (move) the `from` file or directory to the `to` destination.
Both arguments should be paths to files or directories, either relative
or absolute. If the destination file or directory exists and is not
access-protected, it will be overwritten.

Returns one of the `Error<enum_@GlobalScope_Error>` code constants
(`@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **rename\_absolute**(from:
`String<class_String>`, to: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_DirAccess_method_rename_absolute>`

Static version of `rename<class_DirAccess_method_rename>`. Supports only
absolute paths.
