github\_url  
hide

# FileDialog

**Inherits:** `ConfirmationDialog<class_ConfirmationDialog>` **&lt;**
`AcceptDialog<class_AcceptDialog>` **&lt;** `Window<class_Window>`
**&lt;** `Viewport<class_Viewport>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A dialog for selecting files or directories in the filesystem.

classref-introduction-group

## Description

**FileDialog** is a preset dialog used to choose files and directories
in the filesystem. It supports filter masks. **FileDialog**
automatically sets its window title according to the
`file_mode<class_FileDialog_property_file_mode>`. If you want to use a
custom title, disable this by setting
`mode_overrides_title<class_FileDialog_property_mode_overrides_title>`
to `false`.

classref-reftable-group

## Properties

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
</tbody>
</table>

classref-reftable-group

## Theme Properties

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**dir\_selected**(dir: `String<class_String>`)
`🔗<class_FileDialog_signal_dir_selected>`

Emitted when the user selects a directory.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**file\_selected**(path: `String<class_String>`)
`🔗<class_FileDialog_signal_file_selected>`

Emitted when the user selects a file by double-clicking it or pressing
the **OK** button.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**filename\_filter\_changed**(filter: `String<class_String>`)
`🔗<class_FileDialog_signal_filename_filter_changed>`

Emitted when the filter for file names changes.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**files\_selected**(paths: `PackedStringArray<class_PackedStringArray>`)
`🔗<class_FileDialog_signal_files_selected>`

Emitted when the user selects multiple files.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **FileMode**: `🔗<enum_FileDialog_FileMode>`

classref-enumeration-constant

`FileMode<enum_FileDialog_FileMode>` **FILE\_MODE\_OPEN\_FILE** = `0`

The dialog allows selecting one, and only one file.

classref-enumeration-constant

`FileMode<enum_FileDialog_FileMode>` **FILE\_MODE\_OPEN\_FILES** = `1`

The dialog allows selecting multiple files.

classref-enumeration-constant

`FileMode<enum_FileDialog_FileMode>` **FILE\_MODE\_OPEN\_DIR** = `2`

The dialog only allows selecting a directory, disallowing the selection
of any file.

classref-enumeration-constant

`FileMode<enum_FileDialog_FileMode>` **FILE\_MODE\_OPEN\_ANY** = `3`

The dialog allows selecting one file or directory.

classref-enumeration-constant

`FileMode<enum_FileDialog_FileMode>` **FILE\_MODE\_SAVE\_FILE** = `4`

The dialog will warn when a file exists.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Access**: `🔗<enum_FileDialog_Access>`

classref-enumeration-constant

`Access<enum_FileDialog_Access>` **ACCESS\_RESOURCES** = `0`

The dialog only allows accessing files under the
`Resource<class_Resource>` path (`res://`).

classref-enumeration-constant

`Access<enum_FileDialog_Access>` **ACCESS\_USERDATA** = `1`

The dialog only allows accessing files under user data path (`user://`).

classref-enumeration-constant

`Access<enum_FileDialog_Access>` **ACCESS\_FILESYSTEM** = `2`

The dialog allows accessing files on the whole file system.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Access<enum_FileDialog_Access>` **access** = `0`
`🔗<class_FileDialog_property_access>`

classref-property-setget

-   `void (No return value.)` **set\_access**(value:
    `Access<enum_FileDialog_Access>`)
-   `Access<enum_FileDialog_Access>` **get\_access**()

The file system access scope. See `Access<enum_FileDialog_Access>`
constants.

\*\*Warning:\*\* In Web builds, FileDialog cannot access the host file
system. In sandboxed Linux and macOS environments,
`use_native_dialog<class_FileDialog_property_use_native_dialog>` is
automatically used to allow limited access to host file system.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **current\_dir**
`🔗<class_FileDialog_property_current_dir>`

classref-property-setget

-   `void (No return value.)` **set\_current\_dir**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_current\_dir**()

The current working directory of the file dialog.

\*\*Note:\*\* For native file dialogs, this property is only treated as
a hint and may not be respected by specific OS implementations.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **current\_file**
`🔗<class_FileDialog_property_current_file>`

classref-property-setget

-   `void (No return value.)` **set\_current\_file**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_current\_file**()

The currently selected file of the file dialog.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **current\_path**
`🔗<class_FileDialog_property_current_path>`

classref-property-setget

-   `void (No return value.)` **set\_current\_path**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_current\_path**()

The currently selected file path of the file dialog.

classref-item-separator

------------------------------------------------------------------------

classref-property

`FileMode<enum_FileDialog_FileMode>` **file\_mode** = `4`
`🔗<class_FileDialog_property_file_mode>`

classref-property-setget

-   `void (No return value.)` **set\_file\_mode**(value:
    `FileMode<enum_FileDialog_FileMode>`)
-   `FileMode<enum_FileDialog_FileMode>` **get\_file\_mode**()

The dialog's open or save mode, which affects the selection behavior.
See `FileMode<enum_FileDialog_FileMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **filename\_filter** = `""`
`🔗<class_FileDialog_property_filename_filter>`

classref-property-setget

-   `void (No return value.)` **set\_filename\_filter**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_filename\_filter**()

The filter for file names (case-insensitive). When set to a non-empty
string, only files that contains the substring will be shown.
`filename_filter<class_FileDialog_property_filename_filter>` can be
edited by the user with the filter button at the top of the file dialog.

See also `filters<class_FileDialog_property_filters>`, which should be
used to restrict the file types that can be selected instead of
`filename_filter<class_FileDialog_property_filename_filter>` which is
meant to be set by the user.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedStringArray<class_PackedStringArray>` **filters** =
`PackedStringArray()` `🔗<class_FileDialog_property_filters>`

classref-property-setget

-   `void (No return value.)` **set\_filters**(value:
    `PackedStringArray<class_PackedStringArray>`)
-   `PackedStringArray<class_PackedStringArray>` **get\_filters**()

The available file type filters. Each filter string in the array should
be formatted like this: `*.txt,*.doc;Text Files`. The description text
of the filter is optional and can be omitted.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **mode\_overrides\_title** = `true`
`🔗<class_FileDialog_property_mode_overrides_title>`

classref-property-setget

-   `void (No return value.)` **set\_mode\_overrides\_title**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_mode\_overriding\_title**()

If `true`, changing the `file_mode<class_FileDialog_property_file_mode>`
property will set the window title accordingly (e.g. setting
`file_mode<class_FileDialog_property_file_mode>` to
`FILE_MODE_OPEN_FILE<class_FileDialog_constant_FILE_MODE_OPEN_FILE>`
will change the window title to "Open a File").

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **option\_count** = `0`
`🔗<class_FileDialog_property_option_count>`

classref-property-setget

-   `void (No return value.)` **set\_option\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_option\_count**()

The number of additional `OptionButton<class_OptionButton>`s and
`CheckBox<class_CheckBox>`es in the dialog.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **root\_subfolder** = `""`
`🔗<class_FileDialog_property_root_subfolder>`

classref-property-setget

-   `void (No return value.)` **set\_root\_subfolder**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_root\_subfolder**()

If non-empty, the given sub-folder will be "root" of this
**FileDialog**, i.e. user won't be able to go to its parent directory.

\*\*Note:\*\* This property is ignored by native file dialogs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_hidden\_files** = `false`
`🔗<class_FileDialog_property_show_hidden_files>`

classref-property-setget

-   `void (No return value.)` **set\_show\_hidden\_files**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_showing\_hidden\_files**()

If `true`, the dialog will show hidden files.

\*\*Note:\*\* This property is ignored by native file dialogs on Linux.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_native\_dialog** = `false`
`🔗<class_FileDialog_property_use_native_dialog>`

classref-property-setget

-   `void (No return value.)` **set\_use\_native\_dialog**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_use\_native\_dialog**()

If `true`, `access<class_FileDialog_property_access>` is set to
`ACCESS_FILESYSTEM<class_FileDialog_constant_ACCESS_FILESYSTEM>`, and it
is supported by the current `DisplayServer<class_DisplayServer>`, OS
native dialog will be used instead of custom one.

\*\*Note:\*\* On Linux and macOS, sandboxed apps always use native
dialogs to access the host file system.

\*\*Note:\*\* On macOS, sandboxed apps will save security-scoped
bookmarks to retain access to the opened folders across multiple
sessions. Use
`OS.get_granted_permissions<class_OS_method_get_granted_permissions>` to
get a list of saved bookmarks.

\*\*Note:\*\* Native dialogs are isolated from the base process, file
dialog properties can't be modified once the dialog is shown.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_filter**(filter:
`String<class_String>`, description: `String<class_String>` = "")
`🔗<class_FileDialog_method_add_filter>`

Adds a comma-delimited file name `filter` option to the **FileDialog**
with an optional `description`, which restricts what files can be
picked.

A `filter` should be of the form `"filename.extension"`, where filename
and extension can be `*` to match any string. Filters starting with `.`
(i.e. empty filenames) are not allowed.

For example, a `filter` of `"*.png, *.jpg"` and a `description` of
`"Images"` results in filter text "Images (\*.png, \*.jpg)".

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_option**(name: `String<class_String>`,
values: `PackedStringArray<class_PackedStringArray>`,
default\_value\_index: `int<class_int>`)
`🔗<class_FileDialog_method_add_option>`

Adds an additional `OptionButton<class_OptionButton>` to the file
dialog. If `values` is empty, a `CheckBox<class_CheckBox>` is added
instead.

`default_value_index` should be an index of the value in the `values`.
If `values` is empty it should be either `1` (checked), or `0`
(unchecked).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_filename\_filter**()
`🔗<class_FileDialog_method_clear_filename_filter>`

Clear the filter for file names.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_filters**()
`🔗<class_FileDialog_method_clear_filters>`

Clear all the added filters in the dialog.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **deselect\_all**()
`🔗<class_FileDialog_method_deselect_all>`

Clear all currently selected items in the dialog.

classref-item-separator

------------------------------------------------------------------------

classref-method

`LineEdit<class_LineEdit>` **get\_line\_edit**()
`🔗<class_FileDialog_method_get_line_edit>`

Returns the LineEdit for the selected file.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to hide it or any of its children, use
their `CanvasItem.visible<class_CanvasItem_property_visible>` property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_option\_default**(option: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileDialog_method_get_option_default>`

Returns the default value index of the
`OptionButton<class_OptionButton>` or `CheckBox<class_CheckBox>` with
index `option`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_option\_name**(option: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileDialog_method_get_option_name>`

Returns the name of the `OptionButton<class_OptionButton>` or
`CheckBox<class_CheckBox>` with index `option`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_option\_values**(option: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileDialog_method_get_option_values>`

Returns an array of values of the `OptionButton<class_OptionButton>`
with index `option`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_selected\_options**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FileDialog_method_get_selected_options>`

Returns a `Dictionary<class_Dictionary>` with the selected values of the
additional `OptionButton<class_OptionButton>`s and/or
`CheckBox<class_CheckBox>`es. `Dictionary<class_Dictionary>` keys are
names and values are selected value indices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`VBoxContainer<class_VBoxContainer>` **get\_vbox**()
`🔗<class_FileDialog_method_get_vbox>`

Returns the vertical box container of the dialog, custom controls can be
added to it.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to hide it or any of its children, use
their `CanvasItem.visible<class_CanvasItem_property_visible>` property.

\*\*Note:\*\* Changes to this node are ignored by native file dialogs,
use `add_option<class_FileDialog_method_add_option>` to add custom
elements to the dialog instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **invalidate**()
`🔗<class_FileDialog_method_invalidate>`

Invalidate and update the current dialog content list.

\*\*Note:\*\* This method does nothing on native file dialogs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_option\_default**(option:
`int<class_int>`, default\_value\_index: `int<class_int>`)
`🔗<class_FileDialog_method_set_option_default>`

Sets the default value index of the `OptionButton<class_OptionButton>`
or `CheckBox<class_CheckBox>` with index `option`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_option\_name**(option:
`int<class_int>`, name: `String<class_String>`)
`🔗<class_FileDialog_method_set_option_name>`

Sets the name of the `OptionButton<class_OptionButton>` or
`CheckBox<class_CheckBox>` with index `option`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_option\_values**(option:
`int<class_int>`, values: `PackedStringArray<class_PackedStringArray>`)
`🔗<class_FileDialog_method_set_option_values>`

Sets the option values of the `OptionButton<class_OptionButton>` with
index `option`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **file\_disabled\_color** = `Color(1, 1, 1, 0.25)`
`🔗<class_FileDialog_theme_color_file_disabled_color>`

The color tint for disabled files (when the **FileDialog** is used in
open folder mode).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **file\_icon\_color** = `Color(1, 1, 1, 1)`
`🔗<class_FileDialog_theme_color_file_icon_color>`

The color modulation applied to the file icon.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **folder\_icon\_color** = `Color(1, 1, 1, 1)`
`🔗<class_FileDialog_theme_color_folder_icon_color>`

The color modulation applied to the folder icon.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **back\_folder**
`🔗<class_FileDialog_theme_icon_back_folder>`

Custom icon for the back arrow.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **create\_folder**
`🔗<class_FileDialog_theme_icon_create_folder>`

Custom icon for the create folder button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **file**
`🔗<class_FileDialog_theme_icon_file>`

Custom icon for files.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **folder**
`🔗<class_FileDialog_theme_icon_folder>`

Custom icon for folders.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **forward\_folder**
`🔗<class_FileDialog_theme_icon_forward_folder>`

Custom icon for the forward arrow.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **parent\_folder**
`🔗<class_FileDialog_theme_icon_parent_folder>`

Custom icon for the parent folder arrow.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **reload**
`🔗<class_FileDialog_theme_icon_reload>`

Custom icon for the reload button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **toggle\_filename\_filter**
`🔗<class_FileDialog_theme_icon_toggle_filename_filter>`

Custom icon for the toggle button for the filter for file names.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **toggle\_hidden**
`🔗<class_FileDialog_theme_icon_toggle_hidden>`

Custom icon for the toggle hidden button.
