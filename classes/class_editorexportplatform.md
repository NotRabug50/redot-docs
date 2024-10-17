github\_url  
hide

# EditorExportPlatform

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

**Inherited By:**
`EditorExportPlatformAndroid<class_EditorExportPlatformAndroid>`,
`EditorExportPlatformExtension<class_EditorExportPlatformExtension>`,
`EditorExportPlatformIOS<class_EditorExportPlatformIOS>`,
`EditorExportPlatformMacOS<class_EditorExportPlatformMacOS>`,
`EditorExportPlatformPC<class_EditorExportPlatformPC>`,
`EditorExportPlatformWeb<class_EditorExportPlatformWeb>`

Identifies a supported export platform, and internally provides the
functionality of exporting to that platform.

classref-introduction-group

## Description

Base resource that provides the functionality of exporting a release
build of a project to a platform, from the editor. Stores
platform-specific metadata such as the name and supported features of
the platform, and performs the exporting of projects, PCK files, and ZIP
files. Uses an export template for the platform provided at the time of
project exporting.

Used in scripting by `EditorExportPlugin<class_EditorExportPlugin>` to
configure platform-specific customization of scenes and resources. See
`EditorExportPlugin._begin_customize_scenes<class_EditorExportPlugin_private_method__begin_customize_scenes>`
and
`EditorExportPlugin._begin_customize_resources<class_EditorExportPlugin_private_method__begin_customize_resources>`
for more details.

classref-introduction-group

## Tutorials

-   `Console support in Godot <../tutorials/platform/consoles>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ExportMessageType**:
`🔗<enum_EditorExportPlatform_ExportMessageType>`

classref-enumeration-constant

`ExportMessageType<enum_EditorExportPlatform_ExportMessageType>`
**EXPORT\_MESSAGE\_NONE** = `0`

Invalid message type used as the default value when no type is
specified.

classref-enumeration-constant

`ExportMessageType<enum_EditorExportPlatform_ExportMessageType>`
**EXPORT\_MESSAGE\_INFO** = `1`

Message type for informational messages that have no effect on the
export.

classref-enumeration-constant

`ExportMessageType<enum_EditorExportPlatform_ExportMessageType>`
**EXPORT\_MESSAGE\_WARNING** = `2`

Message type for warning messages that should be addressed but still
allow to complete the export.

classref-enumeration-constant

`ExportMessageType<enum_EditorExportPlatform_ExportMessageType>`
**EXPORT\_MESSAGE\_ERROR** = `3`

Message type for error messages that must be addressed and fail the
export.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **DebugFlags**: `🔗<enum_EditorExportPlatform_DebugFlags>`

classref-enumeration-constant

`DebugFlags<enum_EditorExportPlatform_DebugFlags>`
**DEBUG\_FLAG\_DUMB\_CLIENT** = `1`

Flag is set if remotely debugged project is expected to use remote file
system. If set,
`gen_export_flags<class_EditorExportPlatform_method_gen_export_flags>`
will add `--remove-fs` and `--remote-fs-password` (if password is set in
the editor settings) command line arguments to the list.

classref-enumeration-constant

`DebugFlags<enum_EditorExportPlatform_DebugFlags>`
**DEBUG\_FLAG\_REMOTE\_DEBUG** = `2`

Flag is set if remote debug is enabled. If set,
`gen_export_flags<class_EditorExportPlatform_method_gen_export_flags>`
will add `--remote-debug` and `--breakpoints` (if breakpoints are
selected in the script editor or added by the plugin) command line
arguments to the list.

classref-enumeration-constant

`DebugFlags<enum_EditorExportPlatform_DebugFlags>`
**DEBUG\_FLAG\_REMOTE\_DEBUG\_LOCALHOST** = `4`

Flag is set if remotely debugged project is running on the localhost. If
set,
`gen_export_flags<class_EditorExportPlatform_method_gen_export_flags>`
will use `localhost` instead of
`EditorSettings.network/debug/remote_host<class_EditorSettings_property_network/debug/remote_host>`
as remote debugger host.

classref-enumeration-constant

`DebugFlags<enum_EditorExportPlatform_DebugFlags>`
**DEBUG\_FLAG\_VIEW\_COLLISIONS** = `8`

Flag is set if "Visible Collision Shapes" remote debug option is
enabled. If set,
`gen_export_flags<class_EditorExportPlatform_method_gen_export_flags>`
will add `--debug-collisions` command line arguments to the list.

classref-enumeration-constant

`DebugFlags<enum_EditorExportPlatform_DebugFlags>`
**DEBUG\_FLAG\_VIEW\_NAVIGATION** = `16`

Flag is set if Visible Navigation" remote debug option is enabled. If
set,
`gen_export_flags<class_EditorExportPlatform_method_gen_export_flags>`
will add `--debug-navigation` command line arguments to the list.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_message**(type:
`ExportMessageType<enum_EditorExportPlatform_ExportMessageType>`,
category: `String<class_String>`, message: `String<class_String>`)
`🔗<class_EditorExportPlatform_method_add_message>`

Adds a message to the export log that will be displayed when exporting
ends.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_messages**()
`🔗<class_EditorExportPlatform_method_clear_messages>`

Clears the export log.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorExportPreset<class_EditorExportPreset>` **create\_preset**()
`🔗<class_EditorExportPlatform_method_create_preset>`

Create a new preset for this platform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **export\_pack**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`, flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\]
= 0) `🔗<class_EditorExportPlatform_method_export_pack>`

Creates a PCK archive at `path` for the specified `preset`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **export\_pack\_patch**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`, patches:
`PackedStringArray<class_PackedStringArray>` = PackedStringArray(),
flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\]
= 0) `🔗<class_EditorExportPlatform_method_export_pack_patch>`

Creates a patch PCK archive at `path` for the specified `preset`,
containing only the files that have changed since the last patch.

\*\*Note:\*\* `patches` is an optional override of the set of patches
defined in the export preset. When empty the patches defined in the
export preset will be used instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **export\_project**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`, flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\]
= 0) `🔗<class_EditorExportPlatform_method_export_project>`

Creates a full project at `path` for the specified `preset`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **export\_project\_files**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, save\_cb: `Callable<class_Callable>`, shared\_cb:
`Callable<class_Callable>` = Callable())
`🔗<class_EditorExportPlatform_method_export_project_files>`

Exports project files for the specified preset. This method can be used
to implement custom export format, other than PCK and ZIP. One of the
callbacks is called for each exported file.

`save_cb` is called for all exported files and have the following
arguments: `file_path: String`, `file_data: PackedByteArray`,
`file_index: int`, `file_count: int`,
`encryption_include_filters: PackedStringArray`,
`encryption_exclude_filters: PackedStringArray`,
`encryption_key: PackedByteArray`.

`shared_cb` is called for exported native shared/static libraries and
have the following arguments: `file_path: String`,
`tags: PackedStringArray`, `target_folder: String`.

\*\*Note:\*\* `file_index` and `file_count` are intended for progress
tracking only and aren't necesserely unique and precise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **export\_zip**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`, flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\]
= 0) `🔗<class_EditorExportPlatform_method_export_zip>`

Create a ZIP archive at `path` for the specified `preset`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **export\_zip\_patch**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`, patches:
`PackedStringArray<class_PackedStringArray>` = PackedStringArray(),
flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\]
= 0) `🔗<class_EditorExportPlatform_method_export_zip_patch>`

Create a patch ZIP archive at `path` for the specified `preset`,
containing only the files that have changed since the last patch.

\*\*Note:\*\* `patches` is an optional override of the set of patches
defined in the export preset. When empty the patches defined in the
export preset will be used instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**find\_export\_template**(template\_file\_name: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatform_method_find_export_template>`

Locates export template for the platform, and returns
`Dictionary<class_Dictionary>` with the following keys: `path: String`
and `error: String`. This method is provided for convenience and custom
export platforms aren't required to use it or keep export templates
stored in the same way official templates are.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**gen\_export\_flags**(flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`DebugFlags<enum_EditorExportPlatform_DebugFlags>`\])
`🔗<class_EditorExportPlatform_method_gen_export_flags>`

Generates array of command line arguments for the default export
templates for the debug flags and editor settings.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_current\_presets**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatform_method_get_current_presets>`

Returns array of `EditorExportPreset<class_EditorExportPreset>`s for
this platform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_forced\_export\_files**()
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_EditorExportPlatform_method_get_forced_export_files>`

Returns array of core file names that always should be exported
regardless of preset config.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_message\_category**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatform_method_get_message_category>`

Returns message category, for the message with `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_message\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatform_method_get_message_count>`

Returns number of messages in the export log.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_message\_text**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatform_method_get_message_text>`

Returns message text, for the message with `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ExportMessageType<enum_EditorExportPlatform_ExportMessageType>`
**get\_message\_type**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatform_method_get_message_type>`

Returns message type, for the message with `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_os\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatform_method_get_os_name>`

Returns the name of the export operating system handled by this
**EditorExportPlatform** class, as a friendly string. Possible return
values are `Windows`, `Linux`, `macOS`, `Android`, `iOS`, and `Web`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ExportMessageType<enum_EditorExportPlatform_ExportMessageType>`
**get\_worst\_message\_type**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatform_method_get_worst_message_type>`

Returns most severe message type currently present in the export log.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **save\_pack**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`, embed:
`bool<class_bool>` = false)
`🔗<class_EditorExportPlatform_method_save_pack>`

Saves PCK archive and returns `Dictionary<class_Dictionary>` with the
following keys: `result: Error`, `so_files: Array` (array of the
shared/static objects which contains dictionaries with the following
keys: `path: String`, `tags: PackedStringArray`, and
`target_folder: String`).

If `embed` is `true`, PCK content is appended to the end of `path` file
and return `Dictionary<class_Dictionary>` additionally include following
keys: `embedded_start: int` (embedded PCK offset) and
`embedded_size: int` (embedded PCK size).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **save\_pack\_patch**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`)
`🔗<class_EditorExportPlatform_method_save_pack_patch>`

Saves patch PCK archive and returns `Dictionary<class_Dictionary>` with
the following keys: `result: Error`, `so_files: Array` (array of the
shared/static objects which contains dictionaries with the following
keys: `path: String`, `tags: PackedStringArray`, and
`target_folder: String`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **save\_zip**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`)
`🔗<class_EditorExportPlatform_method_save_zip>`

Saves ZIP archive and returns `Dictionary<class_Dictionary>` with the
following keys: `result: Error`, `so_files: Array` (array of the
shared/static objects which contains dictionaries with the following
keys: `path: String`, `tags: PackedStringArray`, and
`target_folder: String`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **save\_zip\_patch**(preset:
`EditorExportPreset<class_EditorExportPreset>`, debug:
`bool<class_bool>`, path: `String<class_String>`)
`🔗<class_EditorExportPlatform_method_save_zip_patch>`

Saves patch ZIP archive and returns `Dictionary<class_Dictionary>` with
the following keys: `result: Error`, `so_files: Array` (array of the
shared/static objects which contains dictionaries with the following
keys: `path: String`, `tags: PackedStringArray`, and
`target_folder: String`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **ssh\_push\_to\_remote**(host:
`String<class_String>`, port: `String<class_String>`, scp\_args:
`PackedStringArray<class_PackedStringArray>`, src\_file:
`String<class_String>`, dst\_file: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatform_method_ssh_push_to_remote>`

Uploads specified file over SCP protocol to the remote host.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **ssh\_run\_on\_remote**(host:
`String<class_String>`, port: `String<class_String>`, ssh\_arg:
`PackedStringArray<class_PackedStringArray>`, cmd\_args:
`String<class_String>`, output: `Array<class_Array>` = \[\], port\_fwd:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatform_method_ssh_run_on_remote>`

Executes specified command on the remote host via SSH protocol and
returns command output in the `output`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **ssh\_run\_on\_remote\_no\_wait**(host:
`String<class_String>`, port: `String<class_String>`, ssh\_args:
`PackedStringArray<class_PackedStringArray>`, cmd\_args:
`String<class_String>`, port\_fwd: `int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlatform_method_ssh_run_on_remote_no_wait>`

Executes specified command on the remote host via SSH protocol and
returns process ID (on the remote host) without waiting for command to
finish.
