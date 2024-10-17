github\_url  
hide

# ResourceImporterTextureAtlas

**Inherits:** `ResourceImporter<class_ResourceImporter>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Imports a collection of textures from a PNG image into an optimized
`AtlasTexture<class_AtlasTexture>` for 2D rendering.

classref-introduction-group

## Description

This imports a collection of textures from a PNG image into an
`AtlasTexture<class_AtlasTexture>` or 2D `ArrayMesh<class_ArrayMesh>`.
This can be used to save memory when importing 2D animations from
spritesheets. Texture atlases are only supported in 2D rendering, not
3D. See also `ResourceImporterTexture<class_ResourceImporterTexture>`
and
`ResourceImporterLayeredTexture<class_ResourceImporterLayeredTexture>`.

\*\*Note:\*\* **ResourceImporterTextureAtlas** does not handle importing
`TileSetAtlasSource<class_TileSetAtlasSource>`, which is created using
the `TileSet<class_TileSet>` editor instead.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **atlas\_file** = `""`
`🔗<class_ResourceImporterTextureAtlas_property_atlas_file>`

Path to the atlas spritesheet. This *must* be set to valid path to a PNG
image. Otherwise, the atlas will fail to import.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **crop\_to\_region** = `false`
`🔗<class_ResourceImporterTextureAtlas_property_crop_to_region>`

If `true`, discards empty areas from the atlas. This only affects final
sprite positioning, not storage. See also
`trim_alpha_border_from_region<class_ResourceImporterTextureAtlas_property_trim_alpha_border_from_region>`.

\*\*Note:\*\* Only effective if
`import_mode<class_ResourceImporterTextureAtlas_property_import_mode>`
is **Region**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **import\_mode** = `0`
`🔗<class_ResourceImporterTextureAtlas_property_import_mode>`

**Region:** Imports the atlas in an `AtlasTexture<class_AtlasTexture>`
resource, which is rendered as a rectangle. This is fast to render, but
transparent areas still have to be rendered if they can't be trimmed
effectively by
`trim_alpha_border_from_region<class_ResourceImporterTextureAtlas_property_trim_alpha_border_from_region>`.
This can reduce performance when rendering large sprites on screen.

\*\*Mesh:\*\* Imports the atlas as an `ArrayMesh<class_ArrayMesh>`
resource, keeping the original bitmap visible (but rendered as a
polygon). This can be used to reduce fill rate when rendering large
transparent sprites, at the cost of slower rendering if there are little
to no transparent areas in the sprite.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **trim\_alpha\_border\_from\_region** = `true`
`🔗<class_ResourceImporterTextureAtlas_property_trim_alpha_border_from_region>`

If `true`, trims the region to exclude fully transparent pixels using a
clipping rectangle (which is never rotated). This can be used to save
memory. See also
`crop_to_region<class_ResourceImporterTextureAtlas_property_crop_to_region>`.

\*\*Note:\*\* Only effective if
`import_mode<class_ResourceImporterTextureAtlas_property_import_mode>`
is **Region**.
