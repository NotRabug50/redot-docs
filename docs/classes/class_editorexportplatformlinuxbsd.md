github\_url  
hide

# EditorExportPlatformLinuxBSD

**Inherits:** `EditorExportPlatformPC<class_EditorExportPlatformPC>`
**&lt;** `EditorExportPlatform<class_EditorExportPlatform>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Exporter for Linux/BSD.

classref-introduction-group

## Tutorials

-   `Exporting for Linux <../tutorials/export/exporting_for_linux>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **binary\_format/architecture**
`🔗<class_EditorExportPlatformLinuxBSD_property_binary_format/architecture>`

Application executable architecture.

Supported architectures: `x86_32`, `x86_64`, `arm64`, `arm32`, `rv64`,
`ppc64`, and `ppc32`.

Official export templates include `x86_32` and `x86_64` binaries only.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **binary\_format/embed\_pck**
`🔗<class_EditorExportPlatformLinuxBSD_property_binary_format/embed_pck>`

If `true`, project resources are embedded into the executable.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **custom\_template/debug**
`🔗<class_EditorExportPlatformLinuxBSD_property_custom_template/debug>`

Path to the custom export template. If left empty, default template is
used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **custom\_template/release**
`🔗<class_EditorExportPlatformLinuxBSD_property_custom_template/release>`

Path to the custom export template. If left empty, default template is
used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **debug/export\_console\_wrapper**
`🔗<class_EditorExportPlatformLinuxBSD_property_debug/export_console_wrapper>`

If `true`, a console wrapper is exported alongside the main executable,
which allows running the project with enabled console output.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/cleanup\_script**
`🔗<class_EditorExportPlatformLinuxBSD_property_ssh_remote_deploy/cleanup_script>`

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
`🔗<class_EditorExportPlatformLinuxBSD_property_ssh_remote_deploy/enabled>`

Enables remote deploy using SSH/SCP.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/extra\_args\_scp**
`🔗<class_EditorExportPlatformLinuxBSD_property_ssh_remote_deploy/extra_args_scp>`

Array of the additional command line arguments passed to the SCP.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/extra\_args\_ssh**
`🔗<class_EditorExportPlatformLinuxBSD_property_ssh_remote_deploy/extra_args_ssh>`

Array of the additional command line arguments passed to the SSH.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/host**
`🔗<class_EditorExportPlatformLinuxBSD_property_ssh_remote_deploy/host>`

Remote host SSH user name and address, in `user@address` format.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/port**
`🔗<class_EditorExportPlatformLinuxBSD_property_ssh_remote_deploy/port>`

Remote host SSH port number.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **ssh\_remote\_deploy/run\_script**
`🔗<class_EditorExportPlatformLinuxBSD_property_ssh_remote_deploy/run_script>`

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
`🔗<class_EditorExportPlatformLinuxBSD_property_texture_format/etc2_astc>`

If `true`, project textures are exported in the ETC2/ASTC format.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **texture\_format/s3tc\_bptc**
`🔗<class_EditorExportPlatformLinuxBSD_property_texture_format/s3tc_bptc>`

If `true`, project textures are exported in the S3TC/BPTC format.
