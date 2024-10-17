github\_url  
hide

# EditorExportPlatformExtension

**Inherits:** `EditorExportPlatform<class_EditorExportPlatform>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Base class for custom `EditorExportPlatform<class_EditorExportPlatform>`
implementations (plugins).

classref-introduction-group

## Description

External `EditorExportPlatform<class_EditorExportPlatform>`
implementations should inherit from this class.

To use `EditorExportPlatform<class_EditorExportPlatform>`, register it
using the
`EditorPlugin.add_export_platform<class_EditorPlugin_method_add_export_platform>`
method first.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **\_can\_export**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__can_export>`

**Optional.**

Returns `true`, if specified `preset` is valid and can be exported. Use
`set_config_error<class_EditorExportPlatformExtension_method_set_config_error>`
and
`set_config_missing_templates<class_EditorExportPlatformExtension_method_set_config_missing_templates>`
to set error details.

Usual implementation can call
`_has_valid_export_configuration<class_EditorExportPlatformExtension_private_method__has_valid_export_configuration>`
and
`_has_valid_project_configuration<class_EditorExportPlatformExtension_private_method__has_valid_project_configuration>`
to determine if export is possible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_cleanup**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlatformExtension_private_method__cleanup>`

**Optional.**

Called by the editor before platform is unregistered.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_export\_pack**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`, flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlatformExtension_private_method__export_pack>`

**Optional.**

Creates a PCK archive at `path` for the specified `preset`.

This method is called when "Export PCK/ZIP" button is pressed in the
export dialog, with "Export as Patch" disabled, and PCK is selected as a
file type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_export\_pack\_patch**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`, patches:
`PackedStringArray<class_PackedStringArray>`, flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlatformExtension_private_method__export_pack_patch>`

**Optional.**

Creates a patch PCK archive at `path` for the specified `preset`,
containing only the files that have changed since the last patch.

This method is called when "Export PCK/ZIP" button is pressed in the
export dialog, with "Export as Patch" enabled, and PCK is selected as a
file type.

\*\*Note:\*\* The patches provided in `patches` have already been loaded
when this method is called and are merely provided as context. When
empty the patches defined in the export preset have been loaded instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_export\_project**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`, flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlatformExtension_private_method__export_project>`

**Required.**

Creates a full project at `path` for the specified `preset`.

This method is called when "Export" button is pressed in the export
dialog.

This method implementation can call
`EditorExportPlatform.save_pack<class_EditorExportPlatform_method_save_pack>`
or
`EditorExportPlatform.save_zip<class_EditorExportPlatform_method_save_zip>`
to use default PCK/ZIP export process, or calls
`EditorExportPlatform.export_project_files<class_EditorExportPlatform_method_export_project_files>`
and implement custom callback for processing each exported file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_export\_zip**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`, flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlatformExtension_private_method__export_zip>`

**Optional.**

Create a ZIP archive at `path` for the specified `preset`.

This method is called when "Export PCK/ZIP" button is pressed in the
export dialog, with "Export as Patch" disabled, and ZIP is selected as a
file type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_export\_zip\_patch**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`, patches:
`PackedStringArray<class_PackedStringArray>`, flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlatformExtension_private_method__export_zip_patch>`

**Optional.**

Create a ZIP archive at `path` for the specified `preset`, containing
only the files that have changed since the last patch.

This method is called when "Export PCK/ZIP" button is pressed in the
export dialog, with "Export as Patch" enabled, and ZIP is selected as a
file type.

\*\*Note:\*\* The patches provided in `patches` have already been loaded
when this method is called and are merely provided as context. When
empty the patches defined in the export preset have been loaded instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_binary\_extensions**(preset:
`EditorExportPreset<class_EditorExportPreset>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_binary_extensions>`

**Required.**

Returns array of supported binary extensions for the full project
export.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_debug\_protocol**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_debug_protocol>`

**Optional.**

Returns protocol used for remote debugging. Default implementation
return `tcp://`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_device\_architecture**(device:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_device_architecture>`

**Optional.**

Returns device architecture for one-click deploy.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_get\_export\_option\_visibility**(preset:
`EditorExportPreset<class_EditorExportPreset>`, option:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_export_option_visibility>`

**Optional.**

Validates `option` and returns visibility for the specified `preset`.
Default implementation return `true` for all options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_export\_option\_warning**(preset:
`EditorExportPreset<class_EditorExportPreset>`, option:
`StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_export_option_warning>`

**Optional.**

Validates `option` and returns warning message for the specified
`preset`. Default implementation return empty string for all options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_export\_options**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_export_options>`

**Optional.**

Returns a property list, as an `Array<class_Array>` of dictionaries.
Each `Dictionary<class_Dictionary>` must at least contain the
`name: StringName` and `type: Variant.Type` entries.

Additionally, the following keys are supported:

-   `hint: PropertyHint`
-   `hint_string: String`
-   `usage: PropertyUsageFlags`
-   `class_name: StringName`
-   `default_value: Variant`, default value of the property.
-   `update_visibility: bool`, if set to `true`,
    `_get_export_option_visibility<class_EditorExportPlatformExtension_private_method__get_export_option_visibility>`
    is called for each property when this property is changed.
-   `required: bool`, if set to `true`, this property warnings are
    critical, and should be resolved to make export possible. This value
    is a hint for the
    `_has_valid_export_configuration<class_EditorExportPlatformExtension_private_method__has_valid_export_configuration>`
    implementation, and not used by the engine directly.

See also
`Object._get_property_list<class_Object_private_method__get_property_list>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **\_get\_logo**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_logo>`

**Required.**

Returns platform logo displayed in the export dialog, logo should be
32x32 adjusted to the current editor scale, see
`EditorInterface.get_editor_scale<class_EditorInterface_method_get_editor_scale>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_name>`

**Required.**

Returns export platform name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ImageTexture<class_ImageTexture>` **\_get\_option\_icon**(device:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_option_icon>`

**Optional.**

Returns one-click deploy menu item icon for the specified `device`, icon
should be 16x16 adjusted to the current editor scale, see
`EditorInterface.get_editor_scale<class_EditorInterface_method_get_editor_scale>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_option\_label**(device:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_option_label>`

**Optional.**

Returns one-click deploy menu item label for the specified `device`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_option\_tooltip**(device:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_option_tooltip>`

**Optional.**

Returns one-click deploy menu item tooltip for the specified `device`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_options\_count**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_options_count>`

**Optional.**

Returns number one-click deploy devices (or other one-click option
displayed in the menu).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_options\_tooltip**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_options_tooltip>`

**Optional.**

Returns tooltip of the one-click deploy menu button.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_os\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_os_name>`

**Required.**

Returns target OS name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_platform\_features**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_platform_features>`

**Required.**

Returns array of platform specific features.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_preset\_features**(preset:
`EditorExportPreset<class_EditorExportPreset>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_preset_features>`

**Required.**

Returns array of platform specific features for the specified `preset`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **\_get\_run\_icon**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__get_run_icon>`

**Optional.**

Returns icon of the one-click deploy menu button, icon should be 16x16
adjusted to the current editor scale, see
`EditorInterface.get_editor_scale<class_EditorInterface_method_get_editor_scale>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_has\_valid\_export\_configuration**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__has_valid_export_configuration>`

**Required.**

Returns `true` if export configuration is valid.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_has\_valid\_project\_configuration**(preset:
`EditorExportPreset<class_EditorExportPreset>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__has_valid_project_configuration>`

**Required.**

Returns `true` if project configuration is valid.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_executable**(path: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_private_method__is_executable>`

**Optional.**

Returns `true` if specified file is a valid executable (native
executable or script) for the target platform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_poll\_export**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlatformExtension_private_method__poll_export>`

**Optional.**

Returns `true` if one-click deploy options are changed and editor
interface should be updated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_run**(preset:
`EditorExportPreset<class_EditorExportPreset>`, device:
`int<class_int>`, debug\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlatformExtension_private_method__run>`

**Optional.**

This method is called when `device` one-click deploy menu option is
selected.

Implementation should export project to a temporary location, upload and
run it on the specific `device`, or perform another action associated
with the menu item.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_should\_update\_export\_options**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlatformExtension_private_method__should_update_export_options>`

**Optional.**

Returns `true` if export options list is changed and presets should be
updated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_config\_error**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_method_get_config_error>`

Returns current configuration error message text. This method should be
called only from the
`_can_export<class_EditorExportPlatformExtension_private_method__can_export>`,
`_has_valid_export_configuration<class_EditorExportPlatformExtension_private_method__has_valid_export_configuration>`,
or
`_has_valid_project_configuration<class_EditorExportPlatformExtension_private_method__has_valid_project_configuration>`
implementations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_config\_missing\_templates**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_method_get_config_missing_templates>`

Returns `true` is export templates are missing from the current
configuration. This method should be called only from the
`_can_export<class_EditorExportPlatformExtension_private_method__can_export>`,
`_has_valid_export_configuration<class_EditorExportPlatformExtension_private_method__has_valid_export_configuration>`,
or
`_has_valid_project_configuration<class_EditorExportPlatformExtension_private_method__has_valid_project_configuration>`
implementations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_config\_error**(error\_text:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_method_set_config_error>`

Sets current configuration error message text. This method should be
called only from the
`_can_export<class_EditorExportPlatformExtension_private_method__can_export>`,
`_has_valid_export_configuration<class_EditorExportPlatformExtension_private_method__has_valid_export_configuration>`,
or
`_has_valid_project_configuration<class_EditorExportPlatformExtension_private_method__has_valid_project_configuration>`
implementations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_config\_missing\_templates**(missing\_templates:
`bool<class_bool>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatformExtension_method_set_config_missing_templates>`

Set to `true` is export templates are missing from the current
configuration. This method should be called only from the
`_can_export<class_EditorExportPlatformExtension_private_method__can_export>`,
`_has_valid_export_configuration<class_EditorExportPlatformExtension_private_method__has_valid_export_configuration>`,
or
`_has_valid_project_configuration<class_EditorExportPlatformExtension_private_method__has_valid_project_configuration>`
implementations.
