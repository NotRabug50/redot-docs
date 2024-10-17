github\_url  
hide

# EditorFileDialog

**Inherits:** `ConfirmationDialog<class_ConfirmationDialog>` **&lt;**
`AcceptDialog<class_AcceptDialog>` **&lt;** `Window<class_Window>`
**&lt;** `Viewport<class_Viewport>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A modified version of `FileDialog<class_FileDialog>` used by the editor.

classref-introduction-group

## Description

**EditorFileDialog** is an enhanced version of
`FileDialog<class_FileDialog>` available only to editor plugins.
Additional features include list of favorited/recent files and the
ability to see files as thumbnails grid instead of list.

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**dir\_selected**(dir: `String<class_String>`)
`🔗<class_EditorFileDialog_signal_dir_selected>`

Emitted when a directory is selected.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**file\_selected**(path: `String<class_String>`)
`🔗<class_EditorFileDialog_signal_file_selected>`

Emitted when a file is selected.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**files\_selected**(paths: `PackedStringArray<class_PackedStringArray>`)
`🔗<class_EditorFileDialog_signal_files_selected>`

Emitted when multiple files are selected.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **FileMode**: `🔗<enum_EditorFileDialog_FileMode>`

classref-enumeration-constant

`FileMode<enum_EditorFileDialog_FileMode>` **FILE\_MODE\_OPEN\_FILE** =
`0`

The **EditorFileDialog** can select only one file. Accepting the window
will open the file.

classref-enumeration-constant

`FileMode<enum_EditorFileDialog_FileMode>` **FILE\_MODE\_OPEN\_FILES** =
`1`

The **EditorFileDialog** can select multiple files. Accepting the window
will open all files.

classref-enumeration-constant

`FileMode<enum_EditorFileDialog_FileMode>` **FILE\_MODE\_OPEN\_DIR** =
`2`

The **EditorFileDialog** can select only one directory. Accepting the
window will open the directory.

classref-enumeration-constant

`FileMode<enum_EditorFileDialog_FileMode>` **FILE\_MODE\_OPEN\_ANY** =
`3`

The **EditorFileDialog** can select a file or directory. Accepting the
window will open it.

classref-enumeration-constant

`FileMode<enum_EditorFileDialog_FileMode>` **FILE\_MODE\_SAVE\_FILE** =
`4`

The **EditorFileDialog** can select only one file. Accepting the window
will save the file.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Access**: `🔗<enum_EditorFileDialog_Access>`

classref-enumeration-constant

`Access<enum_EditorFileDialog_Access>` **ACCESS\_RESOURCES** = `0`

The **EditorFileDialog** can only view `res://` directory contents.

classref-enumeration-constant

`Access<enum_EditorFileDialog_Access>` **ACCESS\_USERDATA** = `1`

The **EditorFileDialog** can only view `user://` directory contents.

classref-enumeration-constant

`Access<enum_EditorFileDialog_Access>` **ACCESS\_FILESYSTEM** = `2`

The **EditorFileDialog** can view the entire local file system.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DisplayMode**: `🔗<enum_EditorFileDialog_DisplayMode>`

classref-enumeration-constant

`DisplayMode<enum_EditorFileDialog_DisplayMode>` **DISPLAY\_THUMBNAILS**
= `0`

The **EditorFileDialog** displays resources as thumbnails.

classref-enumeration-constant

`DisplayMode<enum_EditorFileDialog_DisplayMode>` **DISPLAY\_LIST** = `1`

The **EditorFileDialog** displays resources as a list of filenames.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Access<enum_EditorFileDialog_Access>` **access** = `0`
`🔗<class_EditorFileDialog_property_access>`

classref-property-setget

-   `void (No return value.)` **set\_access**(value:
    `Access<enum_EditorFileDialog_Access>`)
-   `Access<enum_EditorFileDialog_Access>` **get\_access**()

The location from which the user may select a file, including `res://`,
`user://`, and the local file system.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **current\_dir**
`🔗<class_EditorFileDialog_property_current_dir>`

classref-property-setget

-   `void (No return value.)` **set\_current\_dir**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_current\_dir**()

The currently occupied directory.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **current\_file**
`🔗<class_EditorFileDialog_property_current_file>`

classref-property-setget

-   `void (No return value.)` **set\_current\_file**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_current\_file**()

The currently selected file.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **current\_path**
`🔗<class_EditorFileDialog_property_current_path>`

classref-property-setget

-   `void (No return value.)` **set\_current\_path**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_current\_path**()

The file system path in the address bar.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disable\_overwrite\_warning** = `false`
`🔗<class_EditorFileDialog_property_disable_overwrite_warning>`

classref-property-setget

-   `void (No return value.)`
    **set\_disable\_overwrite\_warning**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_overwrite\_warning\_disabled**()

If `true`, the **EditorFileDialog** will not warn the user before
overwriting files.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DisplayMode<enum_EditorFileDialog_DisplayMode>` **display\_mode** = `0`
`🔗<class_EditorFileDialog_property_display_mode>`

classref-property-setget

-   `void (No return value.)` **set\_display\_mode**(value:
    `DisplayMode<enum_EditorFileDialog_DisplayMode>`)
-   `DisplayMode<enum_EditorFileDialog_DisplayMode>`
    **get\_display\_mode**()

The view format in which the **EditorFileDialog** displays resources to
the user.

classref-item-separator

------------------------------------------------------------------------

classref-property

`FileMode<enum_EditorFileDialog_FileMode>` **file\_mode** = `4`
`🔗<class_EditorFileDialog_property_file_mode>`

classref-property-setget

-   `void (No return value.)` **set\_file\_mode**(value:
    `FileMode<enum_EditorFileDialog_FileMode>`)
-   `FileMode<enum_EditorFileDialog_FileMode>` **get\_file\_mode**()

The dialog's open or save mode, which affects the selection behavior.
See `FileMode<enum_EditorFileDialog_FileMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedStringArray<class_PackedStringArray>` **filters** =
`PackedStringArray()` `🔗<class_EditorFileDialog_property_filters>`

classref-property-setget

-   `void (No return value.)` **set\_filters**(value:
    `PackedStringArray<class_PackedStringArray>`)
-   `PackedStringArray<class_PackedStringArray>` **get\_filters**()

The available file type filters. For example, this shows only `.png` and
`.gd` files:
`set_filters(PackedStringArray(["*.png ; PNG Images","*.gd ; GDScript Files"]))`.
Multiple file types can also be specified in a single filter.
`"*.png, *.jpg, *.jpeg ; Supported Images"` will show both PNG and JPEG
files when selected.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **option\_count** = `0`
`🔗<class_EditorFileDialog_property_option_count>`

classref-property-setget

-   `void (No return value.)` **set\_option\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_option\_count**()

The number of additional `OptionButton<class_OptionButton>`s and
`CheckBox<class_CheckBox>`es in the dialog.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_hidden\_files** = `false`
`🔗<class_EditorFileDialog_property_show_hidden_files>`

classref-property-setget

-   `void (No return value.)` **set\_show\_hidden\_files**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_showing\_hidden\_files**()

If `true`, hidden files and directories will be visible in the
**EditorFileDialog**. This property is synchronized with
`EditorSettings.filesystem/file_dialog/show_hidden_files<class_EditorSettings_property_filesystem/file_dialog/show_hidden_files>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_filter**(filter:
`String<class_String>`, description: `String<class_String>` = "")
`🔗<class_EditorFileDialog_method_add_filter>`

Adds a comma-delimited file name `filter` option to the
**EditorFileDialog** with an optional `description`, which restricts
what files can be picked.

A `filter` should be of the form `"filename.extension"`, where filename
and extension can be `*` to match any string. Filters starting with `.`
(i.e. empty filenames) are not allowed.

For example, a `filter` of `"*.tscn, *.scn"` and a `description` of
`"Scenes"` results in filter text "Scenes (\*.tscn, \*.scn)".

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_option**(name: `String<class_String>`,
values: `PackedStringArray<class_PackedStringArray>`,
default\_value\_index: `int<class_int>`)
`🔗<class_EditorFileDialog_method_add_option>`

Adds an additional `OptionButton<class_OptionButton>` to the file
dialog. If `values` is empty, a `CheckBox<class_CheckBox>` is added
instead.

`default_value_index` should be an index of the value in the `values`.
If `values` is empty it should be either `1` (checked), or `0`
(unchecked).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_side\_menu**(menu:
`Control<class_Control>`, title: `String<class_String>` = "")
`🔗<class_EditorFileDialog_method_add_side_menu>`

Adds the given `menu` to the side of the file dialog with the given
`title` text on top. Only one side menu is allowed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_filters**()
`🔗<class_EditorFileDialog_method_clear_filters>`

Removes all filters except for "All Files (\*)".

classref-item-separator

------------------------------------------------------------------------

classref-method

`LineEdit<class_LineEdit>` **get\_line\_edit**()
`🔗<class_EditorFileDialog_method_get_line_edit>`

Returns the LineEdit for the selected file.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to hide it or any of its children, use
their `CanvasItem.visible<class_CanvasItem_property_visible>` property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_option\_default**(option: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorFileDialog_method_get_option_default>`

Returns the default value index of the
`OptionButton<class_OptionButton>` or `CheckBox<class_CheckBox>` with
index `option`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_option\_name**(option: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorFileDialog_method_get_option_name>`

Returns the name of the `OptionButton<class_OptionButton>` or
`CheckBox<class_CheckBox>` with index `option`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_option\_values**(option: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorFileDialog_method_get_option_values>`

Returns an array of values of the `OptionButton<class_OptionButton>`
with index `option`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_selected\_options**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorFileDialog_method_get_selected_options>`

Returns a `Dictionary<class_Dictionary>` with the selected values of the
additional `OptionButton<class_OptionButton>`s and/or
`CheckBox<class_CheckBox>`es. `Dictionary<class_Dictionary>` keys are
names and values are selected value indices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`VBoxContainer<class_VBoxContainer>` **get\_vbox**()
`🔗<class_EditorFileDialog_method_get_vbox>`

Returns the `VBoxContainer<class_VBoxContainer>` used to display the
file system.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to hide it or any of its children, use
their `CanvasItem.visible<class_CanvasItem_property_visible>` property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **invalidate**()
`🔗<class_EditorFileDialog_method_invalidate>`

Notify the **EditorFileDialog** that its view of the data is no longer
accurate. Updates the view contents on next view update.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **popup\_file\_dialog**()
`🔗<class_EditorFileDialog_method_popup_file_dialog>`

Shows the **EditorFileDialog** at the default size and position for file
dialogs in the editor, and selects the file name if there is a current
file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_option\_default**(option:
`int<class_int>`, default\_value\_index: `int<class_int>`)
`🔗<class_EditorFileDialog_method_set_option_default>`

Sets the default value index of the `OptionButton<class_OptionButton>`
or `CheckBox<class_CheckBox>` with index `option`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_option\_name**(option:
`int<class_int>`, name: `String<class_String>`)
`🔗<class_EditorFileDialog_method_set_option_name>`

Sets the name of the `OptionButton<class_OptionButton>` or
`CheckBox<class_CheckBox>` with index `option`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_option\_values**(option:
`int<class_int>`, values: `PackedStringArray<class_PackedStringArray>`)
`🔗<class_EditorFileDialog_method_set_option_values>`

Sets the option values of the `OptionButton<class_OptionButton>` with
index `option`.
