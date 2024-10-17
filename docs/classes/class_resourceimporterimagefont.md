github\_url  
hide

# ResourceImporterImageFont

**Inherits:** `ResourceImporter<class_ResourceImporter>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Imports a bitmap font where all glyphs have the same width and height.

classref-introduction-group

## Description

This image-based workflow can be easier to use than
`ResourceImporterBMFont<class_ResourceImporterBMFont>`, but it requires
all glyphs to have the same width and height, glyph advances and drawing
offsets can be customized. This makes **ResourceImporterImageFont** most
suited to fixed-width fonts.

See also
`ResourceImporterDynamicFont<class_ResourceImporterDynamicFont>`.

classref-introduction-group

## Tutorials

-   [Bitmap fonts - Using
    fonts](../tutorials/ui/gui_using_fonts.html#bitmap-fonts)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **ascent** = `0`
`🔗<class_ResourceImporterImageFont_property_ascent>`

Font ascent (number of pixels above the baseline). If set to `0`, half
of the character height is used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Rect2i<class_Rect2i>` **character\_margin** = `Rect2i(0, 0, 0, 0)`
`🔗<class_ResourceImporterImageFont_property_character_margin>`

Margin applied around every imported glyph. If your font image contains
guides (in the form of lines between glyphs) or if spacing between
characters appears incorrect, try adjusting
`character_margin<class_ResourceImporterImageFont_property_character_margin>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedStringArray<class_PackedStringArray>` **character\_ranges** =
`PackedStringArray()`
`🔗<class_ResourceImporterImageFont_property_character_ranges>`

The character ranges to import from the font image. This is an array
that maps each position on the image (in tile coordinates, not pixels).
The font atlas is traversed from left to right and top to bottom.
Characters can be specified with decimal numbers (127), hexadecimal
numbers (`0x007f`, or `U+007f`) or between single quotes (`'~'`). Ranges
can be specified with a hyphen between characters.

For example, `0-127` represents the full ASCII range. It can also be
written as `0x0000-0x007f` (or `U+0000-U+007f`). As another example,
`' '-'~'` is equivalent to `32-127` and represents the range of
printable (visible) ASCII characters.

For any range, the character advance and offset can be customized by
appending three space-separated integer values (additional advance, x
offset, y offset) to the end. For example `'a'-'b' 4 5 2` sets the
advance to `char_width + 4` and offset to `Vector2(5, 2)` for both
<span class="title-ref">a</span> and <span class="title-ref">b</span>
characters.

Make sure
`character_ranges<class_ResourceImporterImageFont_property_character_ranges>`
doesn't exceed the number of
`columns<class_ResourceImporterImageFont_property_columns>` \*
`rows<class_ResourceImporterImageFont_property_rows>` defined.
Otherwise, the font will fail to import.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **columns** = `1`
`🔗<class_ResourceImporterImageFont_property_columns>`

Number of columns in the font image. See also
`rows<class_ResourceImporterImageFont_property_rows>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **compress** = `true`
`🔗<class_ResourceImporterImageFont_property_compress>`

If `true`, uses lossless compression for the resulting font.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **descent** = `0`
`🔗<class_ResourceImporterImageFont_property_descent>`

Font descent (number of pixels below the baseline). If set to `0`, half
of the character height is used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>` **fallbacks** = `[]`
`🔗<class_ResourceImporterImageFont_property_fallbacks>`

List of font fallbacks to use if a glyph isn't found in this bitmap
font. Fonts at the beginning of the array are attempted first.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Rect2i<class_Rect2i>` **image\_margin** = `Rect2i(0, 0, 0, 0)`
`🔗<class_ResourceImporterImageFont_property_image_margin>`

Margin to cut on the sides of the entire image. This can be used to cut
parts of the image that contain attribution information or similar.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedStringArray<class_PackedStringArray>` **kerning\_pairs** =
`PackedStringArray()`
`🔗<class_ResourceImporterImageFont_property_kerning_pairs>`

Kerning pairs for the font. Kerning pair adjust the spacing between two
characters.

Each string consist of three space separated values: "from" string, "to"
string and integer offset. Each combination form the two string for a
kerning pair, e.g, `ab cd -3` will create kerning pairs `ac`, `ad`,
`bc`, and `bd` with offset `-3`. `\uXXXX` escape sequences can be used
to add Unicode characters.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **rows** = `1`
`🔗<class_ResourceImporterImageFont_property_rows>`

Number of rows in the font image. See also
`columns<class_ResourceImporterImageFont_property_columns>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **scaling\_mode** = `2`
`🔗<class_ResourceImporterImageFont_property_scaling_mode>`

Font scaling mode.
