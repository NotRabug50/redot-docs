github\_url  
hide

# TextServerExtension

**Inherits:** `TextServer<class_TextServer>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `TextServerAdvanced<class_TextServerAdvanced>`,
`TextServerDummy<class_TextServerDummy>`,
`TextServerFallback<class_TextServerFallback>`

Base class for custom `TextServer<class_TextServer>` implementations
(plugins).

classref-introduction-group

## Description

External `TextServer<class_TextServer>` implementations should inherit
from this class.

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

`void (No return value.)` **\_cleanup**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__cleanup>`

**Optional.**

This method is called before text server is unregistered.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_create\_font**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__create_font>`

**Required.**

Creates a new, empty font cache entry resource.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_create\_font\_linked\_variation**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__create_font_linked_variation>`

Optional, implement if font supports extra spacing or baseline offset.

Creates a new variation existing font which is reusing the same glyph
cache and font data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_create\_shaped\_text**(direction:
`Direction<enum_TextServer_Direction>`, orientation:
`Orientation<enum_TextServer_Orientation>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__create_shaped_text>`

**Required.**

Creates a new buffer for complex text layout, with the given `direction`
and `orientation`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_draw\_hex\_code\_box**(canvas:
`RID<class_RID>`, size: `int<class_int>`, pos: `Vector2<class_Vector2>`,
index: `int<class_int>`, color: `Color<class_Color>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__draw_hex_code_box>`

**Optional.**

Draws box displaying character hexadecimal code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_clear\_glyphs**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_clear_glyphs>`

**Required.**

Removes all rendered glyph information from the cache entry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_clear\_kerning\_map**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_clear_kerning_map>`

**Optional.**

Removes all kerning overrides.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_clear\_size\_cache**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_clear_size_cache>`

**Required.**

Removes all font sizes from the cache entry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_clear\_textures**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_clear_textures>`

**Required.**

Removes all textures from font cache entry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_draw\_glyph**(font\_rid:
`RID<class_RID>`, canvas: `RID<class_RID>`, size: `int<class_int>`, pos:
`Vector2<class_Vector2>`, index: `int<class_int>`, color:
`Color<class_Color>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_draw_glyph>`

**Required.**

Draws single glyph into a canvas item at the position, using `font_rid`
at the size `size`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_draw\_glyph\_outline**(font\_rid:
`RID<class_RID>`, canvas: `RID<class_RID>`, size: `int<class_int>`,
outline\_size: `int<class_int>`, pos: `Vector2<class_Vector2>`, index:
`int<class_int>`, color: `Color<class_Color>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_draw_glyph_outline>`

**Required.**

Draws single glyph outline of size `outline_size` into a canvas item at
the position, using `font_rid` at the size `size`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`FontAntialiasing<enum_TextServer_FontAntialiasing>`
**\_font\_get\_antialiasing**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_antialiasing>`

**Optional.**

Returns font anti-aliasing mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_font\_get\_ascent**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_ascent>`

**Required.**

Returns the font ascent (number of pixels above the baseline).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_font\_get\_baseline\_offset**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_baseline_offset>`

**Optional.**

Returns extra baseline offset (as a fraction of font height).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_char\_from\_glyph\_index**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`, glyph\_index:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_char_from_glyph_index>`

**Required.**

Returns character code associated with `glyph_index`, or `0` if
`glyph_index` is invalid.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_font\_get\_descent**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_descent>`

**Required.**

Returns the font descent (number of pixels below the baseline).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**\_font\_get\_disable\_embedded\_bitmaps**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_disable_embedded_bitmaps>`

**Optional.**

Returns whether the font's embedded bitmap loading is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_font\_get\_embolden**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_embolden>`

**Optional.**

Returns font embolden strength.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_face\_count**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_face_count>`

**Optional.**

Returns number of faces in the TrueType / OpenType collection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_face\_index**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_face_index>`

**Optional.**

Returns an active face index in the TrueType / OpenType collection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_fixed\_size**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_fixed_size>`

**Required.**

Returns bitmap font fixed size.

classref-item-separator

------------------------------------------------------------------------

classref-method

`FixedSizeScaleMode<enum_TextServer_FixedSizeScaleMode>`
**\_font\_get\_fixed\_size\_scale\_mode**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_fixed_size_scale_mode>`

**Required.**

Returns bitmap font scaling mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_font\_get\_generate\_mipmaps**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_generate_mipmaps>`

**Optional.**

Returns `true` if font texture mipmap generation is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_font\_get\_global\_oversampling**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_global_oversampling>`

**Optional.**

Returns the font oversampling factor, shared by all fonts in the
TextServer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **\_font\_get\_glyph\_advance**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`, glyph: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_glyph_advance>`

**Required.**

Returns glyph advance (offset of the next glyph).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**\_font\_get\_glyph\_contours**(font\_rid: `RID<class_RID>`, size:
`int<class_int>`, index: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_glyph_contours>`

**Optional.**

Returns outline contours of the glyph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_glyph\_index**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`, char: `int<class_int>`,
variation\_selector: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_glyph_index>`

**Required.**

Returns the glyph index of a `char`, optionally modified by the
`variation_selector`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**\_font\_get\_glyph\_list**(font\_rid: `RID<class_RID>`, size:
`Vector2i<class_Vector2i>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_glyph_list>`

**Required.**

Returns list of rendered glyphs in the cache entry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **\_font\_get\_glyph\_offset**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, glyph:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_glyph_offset>`

**Required.**

Returns glyph offset from the baseline.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **\_font\_get\_glyph\_size**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, glyph:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_glyph_size>`

**Required.**

Returns size of the glyph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_glyph\_texture\_idx**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, glyph:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_glyph_texture_idx>`

**Required.**

Returns index of the cache texture containing the glyph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_font\_get\_glyph\_texture\_rid**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, glyph:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_glyph_texture_rid>`

**Required.**

Returns resource ID of the cache texture containing the glyph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**\_font\_get\_glyph\_texture\_size**(font\_rid: `RID<class_RID>`, size:
`Vector2i<class_Vector2i>`, glyph: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_glyph_texture_size>`

**Required.**

Returns size of the cache texture containing the glyph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **\_font\_get\_glyph\_uv\_rect**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, glyph:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_glyph_uv_rect>`

**Required.**

Returns rectangle in the cache texture containing the glyph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Hinting<enum_TextServer_Hinting>` **\_font\_get\_hinting**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_hinting>`

**Optional.**

Returns the font hinting mode. Used by dynamic fonts only.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **\_font\_get\_kerning**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`, glyph\_pair:
`Vector2i<class_Vector2i>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_kerning>`

**Optional.**

Returns kerning for the pair of glyphs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector2i<class_Vector2i>`\]
**\_font\_get\_kerning\_list**(font\_rid: `RID<class_RID>`, size:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_kerning_list>`

**Optional.**

Returns list of the kerning overrides.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**\_font\_get\_language\_support\_override**(font\_rid:
`RID<class_RID>`, language: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_get_language_support_override>`

**Optional.**

Returns `true` if support override is enabled for the `language`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_font\_get\_language\_support\_overrides**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_get_language_support_overrides>`

**Optional.**

Returns list of language support overrides.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_msdf\_pixel\_range**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_msdf_pixel_range>`

**Optional.**

Returns the width of the range around the shape between the minimum and
maximum representable signed distance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_msdf\_size**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_msdf_size>`

**Optional.**

Returns source font size used to generate MSDF textures.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_font\_get\_name**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_name>`

**Optional.**

Returns font family name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**\_font\_get\_opentype\_feature\_overrides**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_opentype_feature_overrides>`

**Optional.**

Returns font OpenType feature set override.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**\_font\_get\_ot\_name\_strings**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_ot_name_strings>`

**Optional.**

Returns `Dictionary<class_Dictionary>` with OpenType font name strings
(localized font names, version, description, license information, sample
text, etc.).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_font\_get\_oversampling**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_oversampling>`

**Optional.**

Returns font oversampling factor, if set to `0.0` global oversampling
factor is used instead. Used by dynamic fonts only.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_font\_get\_scale**(font\_rid: `RID<class_RID>`,
size: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_scale>`

**Required.**

Returns scaling factor of the color bitmap font.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_font\_get\_script\_support\_override**(font\_rid:
`RID<class_RID>`, script: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_get_script_support_override>`

**Optional.**

Returns `true` if support override is enabled for the `script`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_font\_get\_script\_support\_overrides**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_get_script_support_overrides>`

**Optional.**

Returns list of script support overrides.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector2i<class_Vector2i>`\]
**\_font\_get\_size\_cache\_list**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_size_cache_list>`

**Required.**

Returns list of the font sizes in the cache. Each size is
`Vector2i<class_Vector2i>` with font size and outline size.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_spacing**(font\_rid: `RID<class_RID>`,
spacing: `SpacingType<enum_TextServer_SpacingType>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_spacing>`

**Optional.**

Returns the spacing for `spacing` (see
`SpacingType<enum_TextServer_SpacingType>`) in pixels (not relative to
the font size).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_stretch**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_stretch>`

**Optional.**

Returns font stretch amount, compared to a normal width. A percentage
value between `50%` and `200%`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`FontStyle<enum_TextServer_FontStyle>`\]
**\_font\_get\_style**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_style>`

**Optional.**

Returns font style flags, see `FontStyle<enum_TextServer_FontStyle>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_font\_get\_style\_name**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_style_name>`

**Optional.**

Returns font style name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`SubpixelPositioning<enum_TextServer_SubpixelPositioning>`
**\_font\_get\_subpixel\_positioning**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_subpixel_positioning>`

**Optional.**

Returns font subpixel glyph positioning mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_font\_get\_supported\_chars**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_supported_chars>`

**Required.**

Returns a string containing all the characters available in the font.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**\_font\_get\_supported\_glyphs**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_supported_glyphs>`

**Required.**

Returns an array containing all glyph indices in the font.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_texture\_count**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_texture_count>`

**Required.**

Returns number of textures used by font cache entry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Image<class_Image>` **\_font\_get\_texture\_image**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, texture\_index:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_texture_image>`

**Required.**

Returns font cache texture image data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**\_font\_get\_texture\_offsets**(font\_rid: `RID<class_RID>`, size:
`Vector2i<class_Vector2i>`, texture\_index: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_texture_offsets>`

**Optional.**

Returns array containing glyph packing data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **\_font\_get\_transform**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_transform>`

**Optional.**

Returns 2D transform applied to the font outlines.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_font\_get\_underline\_position**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_underline_position>`

**Required.**

Returns pixel offset of the underline below the baseline.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_font\_get\_underline\_thickness**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_underline_thickness>`

**Required.**

Returns thickness of the underline in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**\_font\_get\_variation\_coordinates**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_variation_coordinates>`

**Optional.**

Returns variation coordinates for the specified font cache entry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_font\_get\_weight**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_get_weight>`

**Optional.**

Returns weight (boldness) of the font. A value in the `100...999` range,
normal font weight is `400`, bold font weight is `700`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_font\_has\_char**(font\_rid: `RID<class_RID>`,
char: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_has_char>`

**Required.**

Returns `true` if a Unicode `char` is available in the font.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_font\_is\_allow\_system\_fallback**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_is_allow_system_fallback>`

**Optional.**

Returns `true` if system fonts can be automatically used as fallbacks.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_font\_is\_force\_autohinter**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_is_force_autohinter>`

**Optional.**

Returns `true` if auto-hinting is supported and preferred over font
built-in hinting.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_font\_is\_language\_supported**(font\_rid:
`RID<class_RID>`, language: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_is_language_supported>`

**Optional.**

Returns `true`, if font supports given language ([ISO
639](https://en.wikipedia.org/wiki/ISO_639-1) code).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**\_font\_is\_multichannel\_signed\_distance\_field**(font\_rid:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_is_multichannel_signed_distance_field>`

**Optional.**

Returns `true` if glyphs of all sizes are rendered using single
multichannel signed distance field generated from the dynamic font
vector data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_font\_is\_script\_supported**(font\_rid:
`RID<class_RID>`, script: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_is_script_supported>`

**Optional.**

Returns `true`, if font supports given script (ISO 15924 code).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_remove\_glyph**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, glyph:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_remove_glyph>`

**Required.**

Removes specified rendered glyph information from the cache entry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_remove\_kerning**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`, glyph\_pair:
`Vector2i<class_Vector2i>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_remove_kerning>`

**Optional.**

Removes kerning override for the pair of glyphs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_remove\_language\_support\_override**(font\_rid:
`RID<class_RID>`, language: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_remove_language_support_override>`

**Optional.**

Remove language support override.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_remove\_script\_support\_override**(font\_rid:
`RID<class_RID>`, script: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_remove_script_support_override>`

**Optional.**

Removes script support override.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_remove\_size\_cache**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_remove_size_cache>`

**Required.**

Removes specified font size from the cache entry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_remove\_texture**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, texture\_index:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_remove_texture>`

**Required.**

Removes specified texture from the cache entry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_render\_glyph**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, index:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_render_glyph>`

**Optional.**

Renders specified glyph to the font cache texture.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_render\_range**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, start:
`int<class_int>`, end: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_render_range>`

**Optional.**

Renders the range of characters to the font cache texture.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_allow\_system\_fallback**(font\_rid: `RID<class_RID>`,
allow\_system\_fallback: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_allow_system_fallback>`

**Optional.**

If set to `true`, system fonts can be automatically used as fallbacks.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_antialiasing**(font\_rid:
`RID<class_RID>`, antialiasing:
`FontAntialiasing<enum_TextServer_FontAntialiasing>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_antialiasing>`

**Optional.**

Sets font anti-aliasing mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_ascent**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`, ascent: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_ascent>`

**Required.**

Sets the font ascent (number of pixels above the baseline).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_baseline\_offset**(font\_rid:
`RID<class_RID>`, baseline\_offset: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_baseline_offset>`

**Optional.**

Sets extra baseline offset (as a fraction of font height).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_data**(font\_rid:
`RID<class_RID>`, data: `PackedByteArray<class_PackedByteArray>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_data>`

**Optional.**

Sets font source data, e.g contents of the dynamic font source file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_data\_ptr**(font\_rid:
`RID<class_RID>`, data\_ptr: `const uint8_t*`, data\_size:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_data_ptr>`

**Optional.**

Sets pointer to the font source data, e.g contents of the dynamic font
source file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_descent**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`, descent: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_descent>`

**Required.**

Sets the font descent (number of pixels below the baseline).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_disable\_embedded\_bitmaps**(font\_rid: `RID<class_RID>`,
disable\_embedded\_bitmaps: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_disable_embedded_bitmaps>`

**Optional.**

If set to `true`, embedded font bitmap loading is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_embolden**(font\_rid:
`RID<class_RID>`, strength: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_embolden>`

Sets font embolden strength. If `strength` is not equal to zero,
emboldens the font outlines. Negative values reduce the outline
thickness.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_face\_index**(font\_rid:
`RID<class_RID>`, face\_index: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_face_index>`

**Optional.**

Sets an active face index in the TrueType / OpenType collection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_fixed\_size**(font\_rid:
`RID<class_RID>`, fixed\_size: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_fixed_size>`

**Required.**

Sets bitmap font fixed size. If set to value greater than zero, same
cache entry will be used for all font sizes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_fixed\_size\_scale\_mode**(font\_rid: `RID<class_RID>`,
fixed\_size\_scale\_mode:
`FixedSizeScaleMode<enum_TextServer_FixedSizeScaleMode>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_fixed_size_scale_mode>`

**Required.**

Sets bitmap font scaling mode. This property is used only if
`fixed_size` is greater than zero.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_force\_autohinter**(font\_rid:
`RID<class_RID>`, force\_autohinter: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_force_autohinter>`

**Optional.**

If set to `true` auto-hinting is preferred over font built-in hinting.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_generate\_mipmaps**(font\_rid:
`RID<class_RID>`, generate\_mipmaps: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_generate_mipmaps>`

**Optional.**

If set to `true` font texture mipmap generation is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_global\_oversampling**(oversampling:
`float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_global_oversampling>`

**Optional.**

Sets oversampling factor, shared by all font in the TextServer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_glyph\_advance**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`, glyph: `int<class_int>`,
advance: `Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_glyph_advance>`

**Required.**

Sets glyph advance (offset of the next glyph).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_glyph\_offset**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, glyph:
`int<class_int>`, offset: `Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_glyph_offset>`

**Required.**

Sets glyph offset from the baseline.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_glyph\_size**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, glyph:
`int<class_int>`, gl\_size: `Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_glyph_size>`

**Required.**

Sets size of the glyph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_glyph\_texture\_idx**(font\_rid: `RID<class_RID>`, size:
`Vector2i<class_Vector2i>`, glyph: `int<class_int>`, texture\_idx:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_glyph_texture_idx>`

**Required.**

Sets index of the cache texture containing the glyph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_glyph\_uv\_rect**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, glyph:
`int<class_int>`, uv\_rect: `Rect2<class_Rect2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_glyph_uv_rect>`

**Required.**

Sets rectangle in the cache texture containing the glyph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_hinting**(font\_rid:
`RID<class_RID>`, hinting: `Hinting<enum_TextServer_Hinting>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_hinting>`

**Optional.**

Sets font hinting mode. Used by dynamic fonts only.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_kerning**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`, glyph\_pair:
`Vector2i<class_Vector2i>`, kerning: `Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_kerning>`

**Optional.**

Sets kerning for the pair of glyphs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_language\_support\_override**(font\_rid:
`RID<class_RID>`, language: `String<class_String>`, supported:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_language_support_override>`

**Optional.**

Adds override for
`_font_is_language_supported<class_TextServerExtension_private_method__font_is_language_supported>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_msdf\_pixel\_range**(font\_rid:
`RID<class_RID>`, msdf\_pixel\_range: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_msdf_pixel_range>`

**Optional.**

Sets the width of the range around the shape between the minimum and
maximum representable signed distance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_msdf\_size**(font\_rid:
`RID<class_RID>`, msdf\_size: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_msdf_size>`

**Optional.**

Sets source font size used to generate MSDF textures.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_multichannel\_signed\_distance\_field**(font\_rid:
`RID<class_RID>`, msdf: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_multichannel_signed_distance_field>`

**Optional.**

If set to `true`, glyphs of all sizes are rendered using single
multichannel signed distance field generated from the dynamic font
vector data. MSDF rendering allows displaying the font at any scaling
factor without blurriness, and without incurring a CPU cost when the
font size changes (since the font no longer needs to be rasterized on
the CPU). As a downside, font hinting is not available with MSDF. The
lack of font hinting may result in less crisp and less readable fonts at
small sizes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_name**(font\_rid:
`RID<class_RID>`, name: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_name>`

**Optional.**

Sets the font family name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_opentype\_feature\_overrides**(font\_rid:
`RID<class_RID>`, overrides: `Dictionary<class_Dictionary>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_opentype_feature_overrides>`

**Optional.**

Sets font OpenType feature set override.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_oversampling**(font\_rid:
`RID<class_RID>`, oversampling: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_oversampling>`

**Optional.**

Sets font oversampling factor, if set to `0.0` global oversampling
factor is used instead. Used by dynamic fonts only.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_scale**(font\_rid:
`RID<class_RID>`, size: `int<class_int>`, scale: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_scale>`

**Required.**

Sets scaling factor of the color bitmap font.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_script\_support\_override**(font\_rid: `RID<class_RID>`,
script: `String<class_String>`, supported: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_script_support_override>`

**Optional.**

Adds override for
`_font_is_script_supported<class_TextServerExtension_private_method__font_is_script_supported>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_spacing**(font\_rid:
`RID<class_RID>`, spacing: `SpacingType<enum_TextServer_SpacingType>`,
value: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_spacing>`

**Optional.**

Sets the spacing for `spacing` (see
`SpacingType<enum_TextServer_SpacingType>`) to `value` in pixels (not
relative to the font size).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_stretch**(font\_rid:
`RID<class_RID>`, stretch: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_stretch>`

**Optional.**

Sets font stretch amount, compared to a normal width. A percentage value
between `50%` and `200%`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_style**(font\_rid:
`RID<class_RID>`, style:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`FontStyle<enum_TextServer_FontStyle>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_style>`

**Optional.**

Sets the font style flags, see `FontStyle<enum_TextServer_FontStyle>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_style\_name**(font\_rid:
`RID<class_RID>`, name\_style: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_style_name>`

**Optional.**

Sets the font style name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_subpixel\_positioning**(font\_rid: `RID<class_RID>`,
subpixel\_positioning:
`SubpixelPositioning<enum_TextServer_SubpixelPositioning>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_subpixel_positioning>`

**Optional.**

Sets font subpixel glyph positioning mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_texture\_image**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, texture\_index:
`int<class_int>`, image: `Image<class_Image>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_texture_image>`

**Required.**

Sets font cache texture image data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_texture\_offsets**(font\_rid:
`RID<class_RID>`, size: `Vector2i<class_Vector2i>`, texture\_index:
`int<class_int>`, offset: `PackedInt32Array<class_PackedInt32Array>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_texture_offsets>`

**Optional.**

Sets array containing glyph packing data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_transform**(font\_rid:
`RID<class_RID>`, transform: `Transform2D<class_Transform2D>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_transform>`

**Optional.**

Sets 2D transform, applied to the font outlines, can be used for
slanting, flipping, and rotating glyphs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_underline\_position**(font\_rid: `RID<class_RID>`, size:
`int<class_int>`, underline\_position: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_underline_position>`

**Required.**

Sets pixel offset of the underline below the baseline.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_underline\_thickness**(font\_rid: `RID<class_RID>`, size:
`int<class_int>`, underline\_thickness: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_underline_thickness>`

**Required.**

Sets thickness of the underline in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_font\_set\_variation\_coordinates**(font\_rid: `RID<class_RID>`,
variation\_coordinates: `Dictionary<class_Dictionary>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_variation_coordinates>`

**Optional.**

Sets variation coordinates for the specified font cache entry.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_font\_set\_weight**(font\_rid:
`RID<class_RID>`, weight: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__font_set_weight>`

**Optional.**

Sets weight (boldness) of the font. A value in the `100...999` range,
normal font weight is `400`, bold font weight is `700`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**\_font\_supported\_feature\_list**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_supported_feature_list>`

**Optional.**

Returns the dictionary of the supported OpenType features.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**\_font\_supported\_variation\_list**(font\_rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__font_supported_variation_list>`

**Optional.**

Returns the dictionary of the supported OpenType variation coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_format\_number**(number:
`String<class_String>`, language: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__format_number>`

**Optional.**

Converts a number from the Western Arabic (0..9) to the numeral systems
used in `language`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_free\_rid**(rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__free_rid>`

**Required.**

Frees an object created by this `TextServer<class_TextServer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_features**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__get_features>`

**Required.**

Returns text server features, see `Feature<enum_TextServer_Feature>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **\_get\_hex\_code\_box\_size**(size:
`int<class_int>`, index: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__get_hex_code_box_size>`

**Optional.**

Returns size of the replacement character (box with character
hexadecimal code that is drawn in place of invalid characters).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__get_name>`

**Required.**

Returns the name of the server interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_support\_data\_filename**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__get_support_data_filename>`

**Optional.**

Returns default TextServer database (e.g. ICU break iterators and
dictionaries) filename.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_support\_data\_info**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__get_support_data_info>`

**Optional.**

Returns TextServer database (e.g. ICU break iterators and dictionaries)
description.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_has**(rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__has>`

**Required.**

Returns `true` if `rid` is valid resource owned by this text server.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_has\_feature**(feature:
`Feature<enum_TextServer_Feature>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__has_feature>`

**Required.**

Returns `true` if the server supports a feature.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_is\_confusable**(string: `String<class_String>`,
dict: `PackedStringArray<class_PackedStringArray>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__is_confusable>`

**Optional.**

Returns index of the first string in `dict` which is visually confusable
with the `string`, or `-1` if none is found.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_locale\_right\_to\_left**(locale:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__is_locale_right_to_left>`

**Required.**

Returns `true` if locale is right-to-left.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_valid\_identifier**(string:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__is_valid_identifier>`

**Optional.**

Returns `true` if `string` is a valid identifier.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_valid\_letter**(unicode: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__is_valid_letter>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_load\_support\_data**(filename:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__load_support_data>`

**Optional.**

Loads optional TextServer database (e.g. ICU break iterators and
dictionaries).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_name\_to\_tag**(name: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__name_to_tag>`

**Optional.**

Converts readable feature, variation, script, or language name to
OpenType tag.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_parse\_number**(number:
`String<class_String>`, language: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__parse_number>`

**Optional.**

Converts `number` from the numeral systems used in `language` to Western
Arabic (0..9).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Vector3i<class_Vector3i>`\]
**\_parse\_structured\_text**(parser\_type:
`StructuredTextParser<enum_TextServer_StructuredTextParser>`, args:
`Array<class_Array>`, text: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__parse_structured_text>`

**Optional.**

Default implementation of the BiDi algorithm override function. See
`StructuredTextParser<enum_TextServer_StructuredTextParser>` for more
info.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_percent\_sign**(language:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__percent_sign>`

**Optional.**

Returns percent sign used in the `language`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_save\_support\_data**(filename:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__save_support_data>`

**Optional.**

Saves optional TextServer database (e.g. ICU break iterators and
dictionaries) to the file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_get\_span\_count**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_get_span_count>`

**Required.**

Returns number of text spans added using
`_shaped_text_add_string<class_TextServerExtension_private_method__shaped_text_add_string>`
or
`_shaped_text_add_object<class_TextServerExtension_private_method__shaped_text_add_object>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_shaped\_get\_span\_meta**(shaped:
`RID<class_RID>`, index: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_get_span_meta>`

**Required.**

Returns text span metadata.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_shaped\_set\_span\_update\_font**(shaped:
`RID<class_RID>`, index: `int<class_int>`, fonts:
`Array<class_Array>`\[`RID<class_RID>`\], size: `int<class_int>`,
opentype\_features: `Dictionary<class_Dictionary>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_set_span_update_font>`

**Required.**

Changes text span font, font size, and OpenType features, without
changing the text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_shaped\_text\_add\_object**(shaped:
`RID<class_RID>`, key: `Variant<class_Variant>`, size:
`Vector2<class_Vector2>`, inline\_align:
`InlineAlignment<enum_@GlobalScope_InlineAlignment>`, length:
`int<class_int>`, baseline: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_add_object>`

**Required.**

Adds inline object to the text buffer, `key` must be unique. In the
text, object is represented as `length` object replacement characters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_shaped\_text\_add\_string**(shaped:
`RID<class_RID>`, text: `String<class_String>`, fonts:
`Array<class_Array>`\[`RID<class_RID>`\], size: `int<class_int>`,
opentype\_features: `Dictionary<class_Dictionary>`, language:
`String<class_String>`, meta: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_add_string>`

**Required.**

Adds text span and font to draw it to the text buffer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_shaped\_text\_clear**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_clear>`

**Required.**

Clears text buffer (removes text and inline objects).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_closest\_character\_pos**(shaped:
`RID<class_RID>`, pos: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_closest_character_pos>`

**Optional.**

Returns composite character position closest to the `pos`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_shaped\_text\_draw**(shaped:
`RID<class_RID>`, canvas: `RID<class_RID>`, pos:
`Vector2<class_Vector2>`, clip\_l: `float<class_float>`, clip\_r:
`float<class_float>`, color: `Color<class_Color>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_draw>`

**Optional.**

Draw shaped text into a canvas item at a given position, with `color`.
`pos` specifies the leftmost point of the baseline (for horizontal
layout) or topmost point of the baseline (for vertical layout).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_shaped\_text\_draw\_outline**(shaped:
`RID<class_RID>`, canvas: `RID<class_RID>`, pos:
`Vector2<class_Vector2>`, clip\_l: `float<class_float>`, clip\_r:
`float<class_float>`, outline\_size: `int<class_int>`, color:
`Color<class_Color>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_draw_outline>`

**Optional.**

Draw the outline of the shaped text into a canvas item at a given
position, with `color`. `pos` specifies the leftmost point of the
baseline (for horizontal layout) or topmost point of the baseline (for
vertical layout).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_shaped\_text\_fit\_to\_width**(shaped:
`RID<class_RID>`, width: `float<class_float>`, justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_fit_to_width>`

**Optional.**

Adjusts text width to fit to specified width, returns new text width.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_shaped\_text\_get\_ascent**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_ascent>`

**Required.**

Returns the text ascent (number of pixels above the baseline for
horizontal layout or to the left of baseline for vertical).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_shaped\_text\_get\_carets**(shaped:
`RID<class_RID>`, position: `int<class_int>`, caret: `CaretInfo*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_carets>`

**Optional.**

Returns shapes of the carets corresponding to the character offset
`position` in the text. Returned caret shape is 1 pixel wide rectangle.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**\_shaped\_text\_get\_character\_breaks**(shaped: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_character_breaks>`

**Optional.**

Returns array of the composite character boundaries.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_get\_custom\_ellipsis**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_custom_ellipsis>`

**Optional.**

Returns ellipsis character used for text clipping.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>`
**\_shaped\_text\_get\_custom\_punctuation**(shaped: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_custom_punctuation>`

**Optional.**

Returns custom punctuation character list, used for word breaking. If
set to empty string, server defaults are used.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_shaped\_text\_get\_descent**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_descent>`

**Required.**

Returns the text descent (number of pixels below the baseline for
horizontal layout or to the right of baseline for vertical).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Direction<enum_TextServer_Direction>`
**\_shaped\_text\_get\_direction**(shaped: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_direction>`

**Optional.**

Returns direction of the text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**\_shaped\_text\_get\_dominant\_direction\_in\_range**(shaped:
`RID<class_RID>`, start: `int<class_int>`, end: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_dominant_direction_in_range>`

**Optional.**

Returns dominant direction of in the range of text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_get\_ellipsis\_glyph\_count**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_ellipsis_glyph_count>`

**Required.**

Returns number of glyphs in the ellipsis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`const Glyph*` **\_shaped\_text\_get\_ellipsis\_glyphs**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_ellipsis_glyphs>`

**Required.**

Returns array of the glyphs in the ellipsis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_get\_ellipsis\_pos**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_ellipsis_pos>`

**Required.**

Returns position of the ellipsis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_get\_glyph\_count**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_glyph_count>`

**Required.**

Returns number of glyphs in the buffer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`const Glyph*` **\_shaped\_text\_get\_glyphs**(shaped: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_glyphs>`

**Required.**

Returns an array of glyphs in the visual order.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**\_shaped\_text\_get\_grapheme\_bounds**(shaped: `RID<class_RID>`, pos:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_grapheme_bounds>`

**Optional.**

Returns composite character's bounds as offsets from the start of the
line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Direction<enum_TextServer_Direction>`
**\_shaped\_text\_get\_inferred\_direction**(shaped: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_inferred_direction>`

**Optional.**

Returns direction of the text, inferred by the BiDi algorithm.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**\_shaped\_text\_get\_line\_breaks**(shaped: `RID<class_RID>`, width:
`float<class_float>`, start: `int<class_int>`, break\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`LineBreakFlag<enum_TextServer_LineBreakFlag>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_line_breaks>`

**Optional.**

Breaks text to the lines and returns character ranges for each line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**\_shaped\_text\_get\_line\_breaks\_adv**(shaped: `RID<class_RID>`,
width: `PackedFloat32Array<class_PackedFloat32Array>`, start:
`int<class_int>`, once: `bool<class_bool>`, break\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`LineBreakFlag<enum_TextServer_LineBreakFlag>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_line_breaks_adv>`

**Optional.**

Breaks text to the lines and columns. Returns character ranges for each
segment.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_get\_object\_glyph**(shaped:
`RID<class_RID>`, key: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_object_glyph>`

**Required.**

Returns the glyph index of the inline object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>`
**\_shaped\_text\_get\_object\_range**(shaped: `RID<class_RID>`, key:
`Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_object_range>`

**Required.**

Returns the character range of the inline object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **\_shaped\_text\_get\_object\_rect**(shaped:
`RID<class_RID>`, key: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_object_rect>`

**Required.**

Returns bounding rectangle of the inline object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **\_shaped\_text\_get\_objects**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_objects>`

**Required.**

Returns array of inline objects.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Orientation<enum_TextServer_Orientation>`
**\_shaped\_text\_get\_orientation**(shaped: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_orientation>`

**Optional.**

Returns text orientation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_shaped\_text\_get\_parent**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_parent>`

**Required.**

Returns the parent buffer from which the substring originates.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_shaped\_text\_get\_preserve\_control**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_preserve_control>`

**Optional.**

Returns `true` if text buffer is configured to display control
characters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_shaped\_text\_get\_preserve\_invalid**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_preserve_invalid>`

**Optional.**

Returns `true` if text buffer is configured to display hexadecimal codes
in place of invalid characters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2i<class_Vector2i>` **\_shaped\_text\_get\_range**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_range>`

**Required.**

Returns substring buffer character range in the parent buffer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**\_shaped\_text\_get\_selection**(shaped: `RID<class_RID>`, start:
`int<class_int>`, end: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_selection>`

**Optional.**

Returns selection rectangles for the specified character range.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **\_shaped\_text\_get\_size**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_size>`

**Required.**

Returns size of the text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_get\_spacing**(shaped:
`RID<class_RID>`, spacing: `SpacingType<enum_TextServer_SpacingType>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_spacing>`

**Optional.**

Returns extra spacing added between glyphs or lines in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_get\_trim\_pos**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_trim_pos>`

**Required.**

Returns the position of the overrun trim.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>`
**\_shaped\_text\_get\_underline\_position**(shaped: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_underline_position>`

**Required.**

Returns pixel offset of the underline below the baseline.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>`
**\_shaped\_text\_get\_underline\_thickness**(shaped: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_underline_thickness>`

**Required.**

Returns thickness of the underline.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_shaped\_text\_get\_width**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_width>`

**Required.**

Returns width (for horizontal layout) or height (for vertical) of the
text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**\_shaped\_text\_get\_word\_breaks**(shaped: `RID<class_RID>`,
grapheme\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`GraphemeFlag<enum_TextServer_GraphemeFlag>`\],
skip\_grapheme\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`GraphemeFlag<enum_TextServer_GraphemeFlag>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_get_word_breaks>`

**Optional.**

Breaks text into words and returns array of character ranges. Use
`grapheme_flags` to set what characters are used for breaking (see
`GraphemeFlag<enum_TextServer_GraphemeFlag>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_hit\_test\_grapheme**(shaped:
`RID<class_RID>`, coord: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_hit_test_grapheme>`

**Optional.**

Returns grapheme index at the specified pixel offset at the baseline, or
`-1` if none is found.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_hit\_test\_position**(shaped:
`RID<class_RID>`, coord: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_hit_test_position>`

**Optional.**

Returns caret character offset at the specified pixel offset at the
baseline. This function always returns a valid position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_shaped\_text\_is\_ready**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_is_ready>`

**Required.**

Returns `true` if buffer is successfully shaped.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_next\_character\_pos**(shaped:
`RID<class_RID>`, pos: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_next_character_pos>`

**Optional.**

Returns composite character end position closest to the `pos`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_next\_grapheme\_pos**(shaped:
`RID<class_RID>`, pos: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_next_grapheme_pos>`

**Optional.**

Returns grapheme end position closest to the `pos`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_shaped\_text\_overrun\_trim\_to\_width**(shaped: `RID<class_RID>`,
width: `float<class_float>`, trim\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`TextOverrunFlag<enum_TextServer_TextOverrunFlag>`\])
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_overrun_trim_to_width>`

**Optional.**

Trims text if it exceeds the given width.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_prev\_character\_pos**(shaped:
`RID<class_RID>`, pos: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_prev_character_pos>`

**Optional.**

Returns composite character start position closest to the `pos`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_shaped\_text\_prev\_grapheme\_pos**(shaped:
`RID<class_RID>`, pos: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_prev_grapheme_pos>`

**Optional.**

Returns grapheme start position closest to the `pos`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_shaped\_text\_resize\_object**(shaped:
`RID<class_RID>`, key: `Variant<class_Variant>`, size:
`Vector2<class_Vector2>`, inline\_align:
`InlineAlignment<enum_@GlobalScope_InlineAlignment>`, baseline:
`float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_resize_object>`

**Required.**

Sets new size and alignment of embedded object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_shaped\_text\_set\_bidi\_override**(shaped: `RID<class_RID>`,
override: `Array<class_Array>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_set_bidi_override>`

**Optional.**

Overrides BiDi for the structured text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_shaped\_text\_set\_custom\_ellipsis**(shaped: `RID<class_RID>`,
char: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_set_custom_ellipsis>`

**Optional.**

Sets ellipsis character used for text clipping.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_shaped\_text\_set\_custom\_punctuation**(shaped: `RID<class_RID>`,
punct: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_set_custom_punctuation>`

**Optional.**

Sets custom punctuation character list, used for word breaking. If set
to empty string, server defaults are used.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_shaped\_text\_set\_direction**(shaped:
`RID<class_RID>`, direction: `Direction<enum_TextServer_Direction>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_set_direction>`

**Optional.**

Sets desired text direction. If set to
`TextServer.DIRECTION_AUTO<class_TextServer_constant_DIRECTION_AUTO>`,
direction will be detected based on the buffer contents and current
locale.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_shaped\_text\_set\_orientation**(shaped:
`RID<class_RID>`, orientation:
`Orientation<enum_TextServer_Orientation>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_set_orientation>`

**Optional.**

Sets desired text orientation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_shaped\_text\_set\_preserve\_control**(shaped: `RID<class_RID>`,
enabled: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_set_preserve_control>`

**Optional.**

If set to `true` text buffer will display control characters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_shaped\_text\_set\_preserve\_invalid**(shaped: `RID<class_RID>`,
enabled: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_set_preserve_invalid>`

**Optional.**

If set to `true` text buffer will display invalid characters as
hexadecimal codes, otherwise nothing is displayed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_shaped\_text\_set\_spacing**(shaped:
`RID<class_RID>`, spacing: `SpacingType<enum_TextServer_SpacingType>`,
value: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_set_spacing>`

**Optional.**

Sets extra spacing added between glyphs or lines in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_shaped\_text\_shape**(shaped: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_shape>`

**Required.**

Shapes buffer if it's not shaped. Returns `true` if the string is shaped
successfully.

classref-item-separator

------------------------------------------------------------------------

classref-method

`const Glyph*` **\_shaped\_text\_sort\_logical**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_sort_logical>`

**Required.**

Returns text glyphs in the logical order.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_shaped\_text\_substr**(shaped: `RID<class_RID>`,
start: `int<class_int>`, length: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__shaped_text_substr>`

**Required.**

Returns text buffer for the substring of the text in the `shaped` text
buffer (including inline objects).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_shaped\_text\_tab\_align**(shaped:
`RID<class_RID>`, tab\_stops:
`PackedFloat32Array<class_PackedFloat32Array>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_tab_align>`

**Optional.**

Aligns shaped text to the given tab-stops.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_shaped\_text\_update\_breaks**(shaped:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_update_breaks>`

**Optional.**

Updates break points in the shaped text. This method is called by
default implementation of text breaking functions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**\_shaped\_text\_update\_justification\_ops**(shaped: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_TextServerExtension_private_method__shaped_text_update_justification_ops>`

**Optional.**

Updates justification points in the shaped text. This method is called
by default implementation of text justification functions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_spoof\_check**(string: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__spoof_check>`

**Optional.**

Returns `true` if `string` is likely to be an attempt at confusing the
reader.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**\_string\_get\_character\_breaks**(string: `String<class_String>`,
language: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__string_get_character_breaks>`

**Optional.**

Returns array of the composite character boundaries.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**\_string\_get\_word\_breaks**(string: `String<class_String>`,
language: `String<class_String>`, chars\_per\_line: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__string_get_word_breaks>`

**Optional.**

Returns an array of the word break boundaries. Elements in the returned
array are the offsets of the start and end of words. Therefore the
length of the array is always even.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_string\_to\_lower**(string:
`String<class_String>`, language: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__string_to_lower>`

**Optional.**

Returns the string converted to lowercase.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_string\_to\_title**(string:
`String<class_String>`, language: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__string_to_title>`

**Optional.**

Returns the string converted to title case.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_string\_to\_upper**(string:
`String<class_String>`, language: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__string_to_upper>`

**Optional.**

Returns the string converted to uppercase.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_strip\_diacritics**(string:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__strip_diacritics>`

**Optional.**

Strips diacritics from the string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_tag\_to\_name**(tag: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TextServerExtension_private_method__tag_to_name>`

**Optional.**

Converts OpenType tag to readable feature, variation, script, or
language name.
