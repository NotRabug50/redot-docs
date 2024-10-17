github\_url  
hide

# EditorImportPlugin

**Inherits:** `ResourceImporter<class_ResourceImporter>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Registers a custom resource importer in the editor. Use the class to
parse any file and import it as a new resource type.

classref-introduction-group

## Description

**EditorImportPlugin**s provide a way to extend the editor's resource
import functionality. Use them to import resources from custom files or
to provide alternatives to the editor's existing importers.

EditorImportPlugins work by associating with specific file extensions
and a resource type. See
`_get_recognized_extensions<class_EditorImportPlugin_private_method__get_recognized_extensions>`
and
`_get_resource_type<class_EditorImportPlugin_private_method__get_resource_type>`.
They may optionally specify some import presets that affect the import
process. EditorImportPlugins are responsible for creating the resources
and saving them in the `.godot/imported` directory (see
`ProjectSettings.application/config/use_hidden_project_data_directory<class_ProjectSettings_property_application/config/use_hidden_project_data_directory>`).

Below is an example EditorImportPlugin that imports a `Mesh<class_Mesh>`
from a file with the extension ".special" or ".spec":

gdscript

@tool extends EditorImportPlugin

func \_get\_importer\_name():  
return "my.special.plugin"

func \_get\_visible\_name():  
return "Special Mesh"

func \_get\_recognized\_extensions():  
return \["special", "spec"\]

func \_get\_save\_extension():  
return "mesh"

func \_get\_resource\_type():  
return "Mesh"

func \_get\_preset\_count():  
return 1

func \_get\_preset\_name(preset\_index):  
return "Default"

func \_get\_import\_options(path, preset\_index):  
return \[{"name": "my\_option", "default\_value": false}\]

func \_import(source\_file, save\_path, options, platform\_variants, gen\_files):  
var file = FileAccess.open(source\_file, FileAccess.READ) if file ==
null: return FAILED var mesh = ArrayMesh.new() \# Fill the Mesh with
data read in "file", left as an exercise to the reader.

var filename = save\_path + "." + \_get\_save\_extension() return
ResourceSaver.save(mesh, filename)

csharp

using Godot;

public partial class MySpecialPlugin : EditorImportPlugin { public
override string \_GetImporterName() { return "my.special.plugin"; }

> public override string \_GetVisibleName() { return "Special Mesh"; }
>
> public override string\[\] \_GetRecognizedExtensions() { return new
> string\[\] { "special", "spec" }; }
>
> public override string \_GetSaveExtension() { return "mesh"; }
>
> public override string \_GetResourceType() { return "Mesh"; }
>
> public override int \_GetPresetCount() { return 1; }
>
> public override string \_GetPresetName(int presetIndex) { return
> "Default"; }
>
> public override
> Godot.Collections.Array&lt;Godot.Collections.Dictionary&gt;
> \_GetImportOptions(string path, int presetIndex) { return new
> Godot.Collections.Array&lt;Godot.Collections.Dictionary&gt; { new
> Godot.Collections.Dictionary { { "name", "myOption" }, {
> "default\_value", false }, } }; }
>
> public override Error \_Import(string sourceFile, string savePath,
> Godot.Collections.Dictionary options,
> Godot.Collections.Array&lt;string&gt; platformVariants,
> Godot.Collections.Array&lt;string&gt; genFiles) { using var file =
> FileAccess.Open(sourceFile, FileAccess.ModeFlags.Read); if
> (file.GetError() != Error.Ok) { return Error.Failed; }
>
> > var mesh = new ArrayMesh(); // Fill the Mesh with data read in
> > "file", left as an exercise to the reader. string filename =
> > $"{savePath}.{\_GetSaveExtension()}"; return
> > ResourceSaver.Save(mesh, filename);
>
> }

}

To use **EditorImportPlugin**, register it using the
`EditorPlugin.add_import_plugin<class_EditorPlugin_method_add_import_plugin>`
method first.

classref-introduction-group

## Tutorials

-   `Import plugins <../tutorials/plugins/editor/import_plugins>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **\_can\_import\_threaded**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__can_import_threaded>`

Tells whether this importer can be run in parallel on threads, or, on
the contrary, it's only safe for the editor to call it from the main
thread, for one file at a time.

If this method is not overridden, it will return `true` by default
(i.e., safe for parallel importing).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_import\_options**(path: `String<class_String>`, preset\_index:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__get_import_options>`

Gets the options and default values for the preset at this index.
Returns an Array of Dictionaries with the following keys: `name`,
`default_value`, `property_hint` (optional), `hint_string` (optional),
`usage` (optional).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_import\_order**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__get_import_order>`

Gets the order of this importer to be run when importing resources.
Importers with *lower* import orders will be called first, and higher
values will be called later. Use this to ensure the importer runs after
the dependencies are already imported. The default import order is `0`
unless overridden by a specific importer. See
`ImportOrder<enum_ResourceImporter_ImportOrder>` for some predefined
values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_importer\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__get_importer_name>`

Gets the unique name of the importer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_get\_option\_visibility**(path:
`String<class_String>`, option\_name: `StringName<class_StringName>`,
options: `Dictionary<class_Dictionary>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__get_option_visibility>`

This method can be overridden to hide specific import options if
conditions are met. This is mainly useful for hiding options that depend
on others if one of them is disabled. For example:

gdscript

func \_get\_option\_visibility(option, options):  
\# Only show the lossy quality setting if the compression mode is set to
"Lossy". if option == "compress/lossy\_quality" and
options.has("compress/mode"): return int(options\["compress/mode"\]) ==
COMPRESS\_LOSSY \# This is a constant that you set

return true

csharp

public void \_GetOptionVisibility(string option,
Godot.Collections.Dictionary options) { // Only show the lossy quality
setting if the compression mode is set to "Lossy". if (option ==
"compress/lossy\_quality" && options.ContainsKey("compress/mode")) {
return (int)options\["compress/mode"\] == CompressLossy; // This is a
constant you set }

> return true;

}

Returns `true` to make all options always visible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_preset\_count**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__get_preset_count>`

Gets the number of initial presets defined by the plugin. Use
`_get_import_options<class_EditorImportPlugin_private_method__get_import_options>`
to get the default options for the preset and
`_get_preset_name<class_EditorImportPlugin_private_method__get_preset_name>`
to get the name of the preset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_preset\_name**(preset\_index:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__get_preset_name>`

Gets the name of the options preset at this index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_get\_priority**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__get_priority>`

Gets the priority of this plugin for the recognized extension. Higher
priority plugins will be preferred. The default priority is `1.0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_recognized\_extensions**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__get_recognized_extensions>`

Gets the list of file extensions to associate with this loader
(case-insensitive). e.g. `["obj"]`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_resource\_type**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__get_resource_type>`

Gets the Godot resource type associated with this loader. e.g. `"Mesh"`
or `"Animation"`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_save\_extension**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__get_save_extension>`

Gets the extension used to save this resource in the `.godot/imported`
directory (see
`ProjectSettings.application/config/use_hidden_project_data_directory<class_ProjectSettings_property_application/config/use_hidden_project_data_directory>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_visible\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__get_visible_name>`

Gets the name to display in the import window. You should choose this
name as a continuation to "Import as", e.g. "Import as Special Mesh".

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_import**(source\_file:
`String<class_String>`, save\_path: `String<class_String>`, options:
`Dictionary<class_Dictionary>`, platform\_variants:
`Array<class_Array>`\[`String<class_String>`\], gen\_files:
`Array<class_Array>`\[`String<class_String>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorImportPlugin_private_method__import>`

Imports `source_file` into `save_path` with the import `options`
specified. The `platform_variants` and `gen_files` arrays will be
modified by this function.

This method must be overridden to do the actual importing work. See this
class' description for an example of overriding this method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**append\_import\_external\_resource**(path: `String<class_String>`,
custom\_options: `Dictionary<class_Dictionary>` = {}, custom\_importer:
`String<class_String>` = "", generator\_parameters:
`Variant<class_Variant>` = null)
`🔗<class_EditorImportPlugin_method_append_import_external_resource>`

This function can only be called during the
`_import<class_EditorImportPlugin_private_method__import>` callback and
it allows manually importing resources from it. This is useful when the
imported file generates external resources that require importing (as
example, images). Custom parameters for the ".import" file can be passed
via the `custom_options`. Additionally, in cases where multiple
importers can handle a file, the `custom_importer` can be specified to
force a specific one. This function performs a resource import and
returns immediately with a success or error code. `generator_parameters`
defines optional extra metadata which will be stored as
`generator_parameters` in the `remap` section of the `.import` file, for
example to store a md5 hash of the source data.
