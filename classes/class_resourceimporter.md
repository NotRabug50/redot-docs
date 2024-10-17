github\_url  
hide

# ResourceImporter

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

**Inherited By:** `EditorImportPlugin<class_EditorImportPlugin>`,
`ResourceImporterBitMap<class_ResourceImporterBitMap>`,
`ResourceImporterBMFont<class_ResourceImporterBMFont>`,
`ResourceImporterCSVTranslation<class_ResourceImporterCSVTranslation>`,
`ResourceImporterDynamicFont<class_ResourceImporterDynamicFont>`,
`ResourceImporterImage<class_ResourceImporterImage>`,
`ResourceImporterImageFont<class_ResourceImporterImageFont>`,
`ResourceImporterLayeredTexture<class_ResourceImporterLayeredTexture>`,
`ResourceImporterMP3<class_ResourceImporterMP3>`,
`ResourceImporterOBJ<class_ResourceImporterOBJ>`,
`ResourceImporterOggVorbis<class_ResourceImporterOggVorbis>`,
`ResourceImporterScene<class_ResourceImporterScene>`,
`ResourceImporterShaderFile<class_ResourceImporterShaderFile>`,
`ResourceImporterTexture<class_ResourceImporterTexture>`,
`ResourceImporterTextureAtlas<class_ResourceImporterTextureAtlas>`,
`ResourceImporterWAV<class_ResourceImporterWAV>`

Base class for resource importers.

classref-introduction-group

## Description

This is the base class for Godot's resource importers. To implement your
own resource importers using editor plugins, see
`EditorImportPlugin<class_EditorImportPlugin>`.

classref-introduction-group

## Tutorials

-   `Import plugins <../tutorials/plugins/editor/import_plugins>`

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ImportOrder**: `🔗<enum_ResourceImporter_ImportOrder>`

classref-enumeration-constant

`ImportOrder<enum_ResourceImporter_ImportOrder>`
**IMPORT\_ORDER\_DEFAULT** = `0`

The default import order.

classref-enumeration-constant

`ImportOrder<enum_ResourceImporter_ImportOrder>`
**IMPORT\_ORDER\_SCENE** = `100`

The import order for scenes, which ensures scenes are imported *after*
all other core resources such as textures. Custom importers should
generally have an import order lower than `100` to avoid issues when
importing scenes that rely on custom resources.
