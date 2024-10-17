github\_url  
hide

# EditorExportPreset

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Export preset configuration.

classref-introduction-group

## Description

Export preset configuration. Instances of **EditorExportPreset** by
editor UI and intended to be used a read-only configuration passed to
the `EditorExportPlatform<class_EditorExportPlatform>` methods when
exporting the project.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ExportFilter**: `🔗<enum_EditorExportPreset_ExportFilter>`

classref-enumeration-constant

`ExportFilter<enum_EditorExportPreset_ExportFilter>`
**EXPORT\_ALL\_RESOURCES** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ExportFilter<enum_EditorExportPreset_ExportFilter>`
**EXPORT\_SELECTED\_SCENES** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ExportFilter<enum_EditorExportPreset_ExportFilter>`
**EXPORT\_SELECTED\_RESOURCES** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ExportFilter<enum_EditorExportPreset_ExportFilter>`
**EXCLUDE\_SELECTED\_RESOURCES** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ExportFilter<enum_EditorExportPreset_ExportFilter>`
**EXPORT\_CUSTOMIZED** = `4`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **FileExportMode**: `🔗<enum_EditorExportPreset_FileExportMode>`

classref-enumeration-constant

`FileExportMode<enum_EditorExportPreset_FileExportMode>`
**MODE\_FILE\_NOT\_CUSTOMIZED** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`FileExportMode<enum_EditorExportPreset_FileExportMode>`
**MODE\_FILE\_STRIP** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`FileExportMode<enum_EditorExportPreset_FileExportMode>`
**MODE\_FILE\_KEEP** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`FileExportMode<enum_EditorExportPreset_FileExportMode>`
**MODE\_FILE\_REMOVE** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ScriptExportMode**:
`🔗<enum_EditorExportPreset_ScriptExportMode>`

classref-enumeration-constant

`ScriptExportMode<enum_EditorExportPreset_ScriptExportMode>`
**MODE\_SCRIPT\_TEXT** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ScriptExportMode<enum_EditorExportPreset_ScriptExportMode>`
**MODE\_SCRIPT\_BINARY\_TOKENS** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ScriptExportMode<enum_EditorExportPreset_ScriptExportMode>`
**MODE\_SCRIPT\_BINARY\_TOKENS\_COMPRESSED** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **are\_advanced\_options\_enabled**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_are_advanced_options_enabled>`

Returns `true`, is "Advanced" toggle is enabled in the export dialog.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_custom\_features**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_custom_features>`

Returns string with a comma separated list of custom features.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_customized\_files**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_customized_files>`

Returns `Dictionary<class_Dictionary>` of files selected in the
"Resources" tab of the export dialog. Dictionary keys are file names and
values are export mode - `"strip`, `"keep"`, or `"remove"`. See also
`get_file_export_mode<class_EditorExportPreset_method_get_file_export_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_customized\_files\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_customized_files_count>`

Returns number of files selected in the "Resources" tab of the export
dialog.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_encrypt\_directory**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_encrypt_directory>`

Returns `true`, PCK directory encryption is enabled in the export
dialog.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_encrypt\_pck**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_encrypt_pck>`

Returns `true`, PCK encryption is enabled in the export dialog.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_encryption\_ex\_filter**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_encryption_ex_filter>`

Returns file filters to exclude during PCK encryption.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_encryption\_in\_filter**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_encryption_in_filter>`

Returns file filters to include during PCK encryption.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_encryption\_key**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_encryption_key>`

Returns PCK encryption key.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_exclude\_filter**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_exclude_filter>`

Returns file filters to exclude during export.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ExportFilter<enum_EditorExportPreset_ExportFilter>`
**get\_export\_filter**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_export_filter>`

Returns export file filter mode selected in the "Resources" tab of the
export dialog.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_export\_path**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_export_path>`

Returns export target path.

classref-item-separator

------------------------------------------------------------------------

classref-method

`FileExportMode<enum_EditorExportPreset_FileExportMode>`
**get\_file\_export\_mode**(path: `String<class_String>`, default:
`FileExportMode<enum_EditorExportPreset_FileExportMode>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_file_export_mode>`

Returns file export mode for the specified file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_files\_to\_export**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_files_to_export>`

Returns array of files to export.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_include\_filter**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_include_filter>`

Returns file filters to include during export.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_or\_env**(name:
`StringName<class_StringName>`, env\_var: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_or_env>`

Returns export option value or value of environment variable if it is
set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_patches**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_patches>`

Returns the list of packs on which to base a patch export on.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_preset\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_preset_name>`

Returns export preset name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_script\_export\_mode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_script_export_mode>`

Returns script export mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_version**(name:
`StringName<class_StringName>`, windows\_version: `bool<class_bool>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_get_version>`

Returns the preset's version number, or fall back to the
`ProjectSettings.application/config/version<class_ProjectSettings_property_application/config/version>`
project setting if set to an empty string.

If `windows_version` is `true`, formats the returned version number to
be compatible with Windows executable metadata.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has**(property: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_has>`

Returns `true` if preset has specified property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_export\_file**(path: `String<class_String>`)
`🔗<class_EditorExportPreset_method_has_export_file>`

Returns `true` if specified file is exported.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_dedicated\_server**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_is_dedicated_server>`

Returns `true` if dedicated server export mode is selected in the export
dialog.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_runnable**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPreset_method_is_runnable>`

Returns `true` if "Runnable" toggle is enabled in the export dialog.
