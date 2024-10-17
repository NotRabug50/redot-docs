github\_url  
hide

# PCKPacker

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Creates packages that can be loaded into a running project.

classref-introduction-group

## Description

The **PCKPacker** is used to create packages that can be loaded into a
running project using
`ProjectSettings.load_resource_pack<class_ProjectSettings_method_load_resource_pack>`.

gdscript

var packer = PCKPacker.new() packer.pck\_start("test.pck")
packer.add\_file("<res://text.txt>", "text.txt") packer.flush()

csharp

var packer = new PckPacker(); packer.PckStart("test.pck");
packer.AddFile("<res://text.txt>", "text.txt"); packer.Flush();

The above **PCKPacker** creates package `test.pck`, then adds a file
named `text.txt` at the root of the package.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **add\_file**(pck\_path:
`String<class_String>`, source\_path: `String<class_String>`, encrypt:
`bool<class_bool>` = false) `🔗<class_PCKPacker_method_add_file>`

Adds the `source_path` file to the current PCK package at the `pck_path`
internal path (should start with `res://`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **flush**(verbose: `bool<class_bool>` =
false) `🔗<class_PCKPacker_method_flush>`

Writes the files specified using all
`add_file<class_PCKPacker_method_add_file>` calls since the last flush.
If `verbose` is `true`, a list of files added will be printed to the
console for easier debugging.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **pck\_start**(pck\_path:
`String<class_String>`, alignment: `int<class_int>` = 32, key:
`String<class_String>` =
"0000000000000000000000000000000000000000000000000000000000000000",
encrypt\_directory: `bool<class_bool>` = false)
`🔗<class_PCKPacker_method_pck_start>`

Creates a new PCK file at the file path `pck_path`. The `.pck` file
extension isn't added automatically, so it should be part of `pck_path`
(even though it's not required).
