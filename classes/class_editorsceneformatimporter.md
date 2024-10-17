github\_url  
hide

# EditorSceneFormatImporter

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

**Inherited By:**
`EditorSceneFormatImporterBlend<class_EditorSceneFormatImporterBlend>`,
`EditorSceneFormatImporterFBX2GLTF<class_EditorSceneFormatImporterFBX2GLTF>`,
`EditorSceneFormatImporterGLTF<class_EditorSceneFormatImporterGLTF>`,
`EditorSceneFormatImporterUFBX<class_EditorSceneFormatImporterUFBX>`

Imports scenes from third-parties' 3D files.

classref-introduction-group

## Description

**EditorSceneFormatImporter** allows to define an importer script for a
third-party 3D format.

To use **EditorSceneFormatImporter**, register it using the
`EditorPlugin.add_scene_format_importer_plugin<class_EditorPlugin_method_add_scene_format_importer_plugin>`
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**IMPORT\_SCENE** = `1`
`🔗<class_EditorSceneFormatImporter_constant_IMPORT_SCENE>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-constant

**IMPORT\_ANIMATION** = `2`
`🔗<class_EditorSceneFormatImporter_constant_IMPORT_ANIMATION>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-constant

**IMPORT\_FAIL\_ON\_MISSING\_DEPENDENCIES** = `4`
`🔗<class_EditorSceneFormatImporter_constant_IMPORT_FAIL_ON_MISSING_DEPENDENCIES>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-constant

**IMPORT\_GENERATE\_TANGENT\_ARRAYS** = `8`
`🔗<class_EditorSceneFormatImporter_constant_IMPORT_GENERATE_TANGENT_ARRAYS>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-constant

**IMPORT\_USE\_NAMED\_SKIN\_BINDS** = `16`
`🔗<class_EditorSceneFormatImporter_constant_IMPORT_USE_NAMED_SKIN_BINDS>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-constant

**IMPORT\_DISCARD\_MESHES\_AND\_MATERIALS** = `32`
`🔗<class_EditorSceneFormatImporter_constant_IMPORT_DISCARD_MESHES_AND_MATERIALS>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-constant

**IMPORT\_FORCE\_DISABLE\_MESH\_COMPRESSION** = `64`
`🔗<class_EditorSceneFormatImporter_constant_IMPORT_FORCE_DISABLE_MESH_COMPRESSION>`

There is currently no description for this constant. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`PackedStringArray<class_PackedStringArray>` **\_get\_extensions**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSceneFormatImporter_private_method__get_extensions>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_import\_flags**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSceneFormatImporter_private_method__get_import_flags>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_get\_import\_options**(path:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorSceneFormatImporter_private_method__get_import_options>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_get\_option\_visibility**(path:
`String<class_String>`, for\_animation: `bool<class_bool>`, option:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorSceneFormatImporter_private_method__get_option_visibility>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Object<class_Object>` **\_import\_scene**(path: `String<class_String>`,
flags: `int<class_int>`, options: `Dictionary<class_Dictionary>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorSceneFormatImporter_private_method__import_scene>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
