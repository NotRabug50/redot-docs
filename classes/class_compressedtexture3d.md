github\_url  
hide

# CompressedTexture3D

**Inherits:** `Texture3D<class_Texture3D>` **&lt;**
`Texture<class_Texture>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Texture with 3 dimensions, optionally compressed.

classref-introduction-group

## Description

**CompressedTexture3D** is the VRAM-compressed counterpart of
`ImageTexture3D<class_ImageTexture3D>`. The file extension for
**CompressedTexture3D** files is `.ctex3d`. This file format is internal
to Godot; it is created by importing other image formats with the import
system.

\*\*CompressedTexture3D\*\* uses VRAM compression, which allows to
reduce memory usage on the GPU when rendering the texture. This also
improves loading times, as VRAM-compressed textures are faster to load
compared to textures using lossless compression. VRAM compression can
exhibit noticeable artifacts and is intended to be used for 3D
rendering, not 2D.

See `Texture3D<class_Texture3D>` for a general description of 3D
textures.

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **load\_path** = `""`
`🔗<class_CompressedTexture3D_property_load_path>`

classref-property-setget

-   `Error<enum_@GlobalScope_Error>` **load**(path:
    `String<class_String>`)
-   `String<class_String>` **get\_load\_path**()

The **CompressedTexture3D**'s file path to a `.ctex3d` file.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **load**(path: `String<class_String>`)
`🔗<class_CompressedTexture3D_method_load>`

Loads the texture from the specified `path`.
