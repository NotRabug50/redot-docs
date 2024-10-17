github\_url  
hide

# EditorExportPlatformWindows

**Inherits:** `EditorExportPlatformPC<class_EditorExportPlatformPC>`
**&lt;** `EditorExportPlatform<class_EditorExportPlatform>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Exporter for Windows.

classref-introduction-group

## Description

The Windows exporter customizes how a Windows build is handled. In the
editor's "Export" window, it is created when adding a new "Windows"
preset.

classref-introduction-group

## Tutorials

-   `Exporting for Windows <../tutorials/export/exporting_for_windows>`

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

`String<class_String>` **application/company\_name**
`🔗<class_EditorExportPlatformWindows_property_application/company_name>`

Company that produced the application. Required. See
[StringFileInfo](https://learn.microsoft.com/en-us/windows/win32/menurc/stringfileinfo-block).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **application/console\_wrapper\_icon**
`🔗<class_EditorExportPlatformWindows_property_application/console_wrapper_icon>`

Console wrapper icon file. If left empty, it will fallback to
`application/icon<class_EditorExportPlatformWindows_property_application/icon>`,
then to
`ProjectSettings.application/config/windows_native_icon<class_ProjectSettings_property_application/config/windows_native_icon>`,
and lastly,
`ProjectSettings.application/config/icon<class_ProjectSettings_property_application/config/icon>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **application/copyright**
`🔗<class_EditorExportPlatformWindows_property_application/copyright>`

Copyright notice for the bundle visible to the user. Optional. See
[StringFileInfo](https://learn.microsoft.com/en-us/windows/win32/menurc/stringfileinfo-block).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **application/d3d12\_agility\_sdk\_multiarch**
`🔗<class_EditorExportPlatformWindows_property_application/d3d12_agility_sdk_multiarch>`

If `true`, and
`application/export_d3d12<class_EditorExportPlatformWindows_property_application/export_d3d12>`
is set, the Agility SDK DLLs will be stored in arch-specific
subdirectories.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **application/export\_angle**
`🔗<class_EditorExportPlatformWindows_property_application/export_angle>`

If set to `1`, ANGLE libraries are exported with the exported
application. If set to `0`, ANGLE libraries are exported only if
`ProjectSettings.rendering/gl_compatibility/driver<class_ProjectSettings_property_rendering/gl_compatibility/driver>`
is set to `"opengl3_angle"`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **application/export\_d3d12**
`🔗<class_EditorExportPlatformWindows_property_application/export_d3d12>`

If set to `1`, the Direct3D 12 runtime libraries (Agility SDK, PIX) are
exported with the exported application. If set to `0`, Direct3D 12
libraries are exported only if
`ProjectSettings.rendering/rendering_device/driver<class_ProjectSettings_property_rendering/rendering_device/driver>`
is set to `"d3d12"`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **application/file\_description**
`🔗<class_EditorExportPlatformWindows_property_application/file_description>`

File description to be presented to users. Required. See
[StringFileInfo](https://learn.microsoft.com/en-us/windows/win32/menurc/stringfileinfo-block).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **application/file\_version**
`🔗<class_EditorExportPlatformWindows_property_application/file_version>`

Version number of the file. Falls back to
`ProjectSettings.application/config/version<class_ProjectSettings_property_application/config/version>`
if left empty. See
[StringFileInfo](https://learn.microsoft.com/en-us/windows/win32/menurc/stringfileinfo-block).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **application/icon**
`🔗<class_EditorExportPlatformWindows_property_application/icon>`

Application icon file. If left empty, it will fallback to
`ProjectSettings.application/config/windows_native_icon<class_ProjectSettings_property_application/config/windows_native_icon>`,
and then to
`ProjectSettings.application/config/icon<class_ProjectSettings_property_application/config/icon>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **application/icon\_interpolation**
`🔗<class_EditorExportPlatformWindows_property_application/icon_interpolation>`

Interpolation method used to resize application icon.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **application/modify\_resources**
`🔗<class_EditorExportPlatformWindows_property_application/modify_resources>`

If enabled, icon and metadata of the exported executable is set
according to the other `application/*` values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **application/product\_name**
`🔗<class_EditorExportPlatformWindows_property_application/product_name>`

Name of the application. Required. See
[StringFileInfo](https://learn.microsoft.com/en-us/windows/win32/menurc/stringfileinfo-block).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **application/product\_version**
`🔗<class_EditorExportPlatformWindows_property_application/product_version>`

Application version visible to the user. Falls back to
`ProjectSettings.application/config/version<class_ProjectSettings_property_application/config/version>`
if left empty. See
[StringFileInfo](https://learn.microsoft.com/en-us/windows/win32/menurc/stringfileinfo-block).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **application/trademarks**
`🔗<class_EditorExportPlatformWindows_property_application/trademarks>`

Trademarks and registered trademarks that apply to the file. Optional.
See
[StringFileInfo](https://learn.microsoft.com/en-us/windows/win32/menurc/stringfileinfo-block).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **binary\_format/architecture**
`🔗<class_EditorExportPlatformWindows_property_binary_format/architecture>`

Application executable architecture.

Supported architectures: `x86_32`, `x86_64`, and `arm64`.

Official export templates include `x86_32` and `x86_64` binaries only.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **binary\_format/embed\_pck**
`🔗<class_EditorExportPlatformWindows_property_binary_format/embed_pck>`

If `true`, project resources are embedded into the executable.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedStringArray<class_PackedStringArray>`
**codesign/custom\_options**
`🔗<class_EditorExportPlatformWindows_property_codesign/custom_options>`

Array of the additional command line arguments passed to the code
signing tool. See [Sign
Tool](https://learn.microsoft.com/en-us/dotnet/framework/tools/signtool-exe).

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **codesign/description**
`🔗<class_EditorExportPlatformWindows_property_codesign/description>`

Description of the signed content. See [Sign
Tool](https://learn.microsoft.com/en-us/dotnet/framework/tools/signtool-exe).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **codesign/digest\_algorithm**
`🔗<class_EditorExportPlatformWindows_property_codesign/digest_algorithm>`

Digest algorithm to use for creating signature. See [Sign
Tool](https://learn.microsoft.com/en-us/dotnet/framework/tools/signtool-exe).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **codesign/enable**
`🔗<class_EditorExportPlatformWindows_property_codesign/enable>`

If `true`, executable signing is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **codesign/identity**
`🔗<class_EditorExportPlatformWindows_property_codesign/identity>`

PKCS \#12 certificate file used to sign executable or certificate SHA-1
hash (if
`codesign/identity_type<class_EditorExportPlatformWindows_property_codesign/identity_type>`
is set to "Use certificate store"). See [Sign
Tool](https://learn.microsoft.com/en-us/dotnet/framework/tools/signtool-exe).

Can be overridden with the environment variable
`GODOT_WINDOWS_CODESIGN_IDENTITY`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **codesign/identity\_type**
`🔗<class_EditorExportPlatformWindows_property_codesign/identity_type>`

Type of identity to use. See [Sign
Tool](https://learn.microsoft.com/en-us/dotnet/framework/tools/signtool-exe).

Can be overridden with the environment variable
`GODOT_WINDOWS_CODESIGN_IDENTITY_TYPE`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **codesign/password**
`🔗<class_EditorExportPlatformWindows_property_codesign/password>`

Password for the certificate file used to sign executable. See [Sign
Tool](https://learn.microsoft.com/en-us/dotnet/framework/tools/signtool-exe).

Can be overridden with the environment variable
`GODOT_WINDOWS_CODESIGN_PASSWORD`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **codesign/timestamp**
`🔗<class_EditorExportPlatformWindows_property_codesign/timestamp>`

If `true`, time-stamp is added to the signature. See [Sign
Tool](https://learn.microsoft.com/en-us/dotnet/framework/tools/signtool-exe).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **codesign/timestamp\_server\_url**
`🔗<class_EditorExportPlatformWindows_property_codesign/timestamp_server_url>`

URL of the time stamp server. If left empty, the default server is used.
See [Sign
Tool](https://learn.microsoft.com/en-us/dotnet/framework/tools/signtool-exe).

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **custom\_template/debug**
`🔗<class_EditorExportPlatformWindows_property_custom_template/debug>`

Path to the custom export template. If left empty, default template is
used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **custom\_template/release**
`🔗<class_EditorExportPlatformWindows_property_custom_template/release>`

Path to the custom export template. If left empty, default template is
used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **debug/export\_console\_wrapper**
`🔗<class_EditorExportPlatformWindows_property_debug/export_console_wrapper>`

If `true`, a console wrapper executable is exported alongside the main
executable, which allows running the project with enabled console
output.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/cleanup\_script**
`🔗<class_EditorExportPlatformWindows_property_ssh_remote_deploy/cleanup_script>`

Script code to execute on the remote host when app is finished.

The following variables can be used in the script:

-   `{temp_dir}` - Path of temporary folder on the remote, used to
    upload app and scripts to.
-   `{archive_name}` - Name of the ZIP containing uploaded application.
-   `{exe_name}` - Name of application executable.
-   `{cmd_args}` - Array of the command line argument for the
    application.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ssh\_remote\_deploy/enabled**
`🔗<class_EditorExportPlatformWindows_property_ssh_remote_deploy/enabled>`

Enables remote deploy using SSH/SCP.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/extra\_args\_scp**
`🔗<class_EditorExportPlatformWindows_property_ssh_remote_deploy/extra_args_scp>`

Array of the additional command line arguments passed to the SCP.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/extra\_args\_ssh**
`🔗<class_EditorExportPlatformWindows_property_ssh_remote_deploy/extra_args_ssh>`

Array of the additional command line arguments passed to the SSH.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/host**
`🔗<class_EditorExportPlatformWindows_property_ssh_remote_deploy/host>`

Remote host SSH user name and address, in `user@address` format.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/port**
`🔗<class_EditorExportPlatformWindows_property_ssh_remote_deploy/port>`

Remote host SSH port number.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/run\_script**
`🔗<class_EditorExportPlatformWindows_property_ssh_remote_deploy/run_script>`

Script code to execute on the remote host when running the app.

The following variables can be used in the script:

-   `{temp_dir}` - Path of temporary folder on the remote, used to
    upload app and scripts to.
-   `{archive_name}` - Name of the ZIP containing uploaded application.
-   `{exe_name}` - Name of application executable.
-   `{cmd_args}` - Array of the command line argument for the
    application.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **texture\_format/etc2\_astc**
`🔗<class_EditorExportPlatformWindows_property_texture_format/etc2_astc>`

If `true`, project textures are exported in the ETC2/ASTC format.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **texture\_format/s3tc\_bptc**
`🔗<class_EditorExportPlatformWindows_property_texture_format/s3tc_bptc>`

If `true`, project textures are exported in the S3TC/BPTC format.
