github\_url  
hide

# Font

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `FontFile<class_FontFile>`,
`FontVariation<class_FontVariation>`, `SystemFont<class_SystemFont>`

Abstract base class for fonts and font variations.

classref-introduction-group

## Description

Abstract base class for different font types. It has methods for drawing
text and font character introspection.

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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

`Array<class_Array>`\[`Font<class_Font>`\] **fallbacks** = `[]`
`🔗<class_Font_property_fallbacks>`

classref-property-setget

-   `void (No return value.)` **set\_fallbacks**(value:
    `Array<class_Array>`\[`Font<class_Font>`\])
-   `Array<class_Array>`\[`Font<class_Font>`\] **get\_fallbacks**()

Array of fallback **Font**s to use as a substitute if a glyph is not
found in this current **Font**.

If this array is empty in a `FontVariation<class_FontVariation>`, the
`FontVariation.base_font<class_FontVariation_property_base_font>`'s
fallbacks are used instead.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **draw\_char**(canvas\_item: `RID<class_RID>`, pos:
`Vector2<class_Vector2>`, char: `int<class_int>`, font\_size:
`int<class_int>`, modulate: `Color<class_Color>` = Color(1, 1, 1, 1))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_draw_char>`

Draw a single Unicode character `char` into a canvas item using the
font, at a given position, with `modulate` color. `pos` specifies the
baseline, not the top. To draw from the top, *ascent* must be added to
the Y axis.

\*\*Note:\*\* Do not use this function to draw strings character by
character, use `draw_string<class_Font_method_draw_string>` or
`TextLine<class_TextLine>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **draw\_char\_outline**(canvas\_item:
`RID<class_RID>`, pos: `Vector2<class_Vector2>`, char: `int<class_int>`,
font\_size: `int<class_int>`, size: `int<class_int>` = -1, modulate:
`Color<class_Color>` = Color(1, 1, 1, 1))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_draw_char_outline>`

Draw a single Unicode character `char` outline into a canvas item using
the font, at a given position, with `modulate` color and `size` outline
size. `pos` specifies the baseline, not the top. To draw from the top,
*ascent* must be added to the Y axis.

\*\*Note:\*\* Do not use this function to draw strings character by
character, use `draw_string<class_Font_method_draw_string>` or
`TextLine<class_TextLine>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_multiline\_string**(canvas\_item:
`RID<class_RID>`, pos: `Vector2<class_Vector2>`, text:
`String<class_String>`, alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` = 0, width:
`float<class_float>` = -1, font\_size: `int<class_int>` = 16,
max\_lines: `int<class_int>` = -1, modulate: `Color<class_Color>` =
Color(1, 1, 1, 1), brk\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`LineBreakFlag<enum_TextServer_LineBreakFlag>`\]
= 3, justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
= 3, direction: `Direction<enum_TextServer_Direction>` = 0, orientation:
`Orientation<enum_TextServer_Orientation>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_draw_multiline_string>`

Breaks `text` into lines using rules specified by `brk_flags` and draws
it into a canvas item using the font, at a given position, with
`modulate` color, optionally clipping the width and aligning
horizontally. `pos` specifies the baseline of the first line, not the
top. To draw from the top, *ascent* must be added to the Y axis.

See also
`CanvasItem.draw_multiline_string<class_CanvasItem_method_draw_multiline_string>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**draw\_multiline\_string\_outline**(canvas\_item: `RID<class_RID>`,
pos: `Vector2<class_Vector2>`, text: `String<class_String>`, alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` = 0, width:
`float<class_float>` = -1, font\_size: `int<class_int>` = 16,
max\_lines: `int<class_int>` = -1, size: `int<class_int>` = 1, modulate:
`Color<class_Color>` = Color(1, 1, 1, 1), brk\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`LineBreakFlag<enum_TextServer_LineBreakFlag>`\]
= 3, justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
= 3, direction: `Direction<enum_TextServer_Direction>` = 0, orientation:
`Orientation<enum_TextServer_Orientation>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_draw_multiline_string_outline>`

Breaks `text` to the lines using rules specified by `brk_flags` and
draws text outline into a canvas item using the font, at a given
position, with `modulate` color and `size` outline size, optionally
clipping the width and aligning horizontally. `pos` specifies the
baseline of the first line, not the top. To draw from the top, *ascent*
must be added to the Y axis.

See also
`CanvasItem.draw_multiline_string_outline<class_CanvasItem_method_draw_multiline_string_outline>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_string**(canvas\_item:
`RID<class_RID>`, pos: `Vector2<class_Vector2>`, text:
`String<class_String>`, alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` = 0, width:
`float<class_float>` = -1, font\_size: `int<class_int>` = 16, modulate:
`Color<class_Color>` = Color(1, 1, 1, 1), justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
= 3, direction: `Direction<enum_TextServer_Direction>` = 0, orientation:
`Orientation<enum_TextServer_Orientation>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_draw_string>`

Draw `text` into a canvas item using the font, at a given position, with
`modulate` color, optionally clipping the width and aligning
horizontally. `pos` specifies the baseline, not the top. To draw from
the top, *ascent* must be added to the Y axis.

See also `CanvasItem.draw_string<class_CanvasItem_method_draw_string>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_string\_outline**(canvas\_item:
`RID<class_RID>`, pos: `Vector2<class_Vector2>`, text:
`String<class_String>`, alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` = 0, width:
`float<class_float>` = -1, font\_size: `int<class_int>` = 16, size:
`int<class_int>` = 1, modulate: `Color<class_Color>` = Color(1, 1, 1,
1), justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
= 3, direction: `Direction<enum_TextServer_Direction>` = 0, orientation:
`Orientation<enum_TextServer_Orientation>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_draw_string_outline>`

Draw `text` outline into a canvas item using the font, at a given
position, with `modulate` color and `size` outline size, optionally
clipping the width and aligning horizontally. `pos` specifies the
baseline, not the top. To draw from the top, *ascent* must be added to
the Y axis.

See also
`CanvasItem.draw_string_outline<class_CanvasItem_method_draw_string_outline>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **find\_variation**(variation\_coordinates:
`Dictionary<class_Dictionary>`, face\_index: `int<class_int>` = 0,
strength: `float<class_float>` = 0.0, transform:
`Transform2D<class_Transform2D>` = Transform2D(1, 0, 0, 1, 0, 0),
spacing\_top: `int<class_int>` = 0, spacing\_bottom: `int<class_int>` =
0, spacing\_space: `int<class_int>` = 0, spacing\_glyph:
`int<class_int>` = 0, baseline\_offset: `float<class_float>` = 0.0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_find_variation>`

Returns `TextServer<class_TextServer>` RID of the font cache for
specific variation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_ascent**(font\_size: `int<class_int>` = 16)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_ascent>`

Returns the average font ascent (number of pixels above the baseline).

\*\*Note:\*\* Real ascent of the string is context-dependent and can be
significantly different from the value returned by this function. Use it
only as rough estimate (e.g. as the ascent of empty line).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_char\_size**(char: `int<class_int>`,
font\_size: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_char_size>`

Returns the size of a character. Does not take kerning into account.

\*\*Note:\*\* Do not use this function to calculate width of the string
character by character, use
`get_string_size<class_Font_method_get_string_size>` or
`TextLine<class_TextLine>` instead. The height returned is the font
height (see also `get_height<class_Font_method_get_height>`) and has no
relation to the glyph height.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_descent**(font\_size: `int<class_int>` = 16)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_descent>`

Returns the average font descent (number of pixels below the baseline).

\*\*Note:\*\* Real descent of the string is context-dependent and can be
significantly different from the value returned by this function. Use it
only as rough estimate (e.g. as the descent of empty line).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_face\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_face_count>`

Returns number of faces in the TrueType / OpenType collection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_font\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_font_name>`

Returns font family name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_font\_stretch**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_font_stretch>`

Returns font stretch amount, compared to a normal width. A percentage
value between `50%` and `200%`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`FontStyle<enum_TextServer_FontStyle>`\]
**get\_font\_style**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_font_style>`

Returns font style flags, see `FontStyle<enum_TextServer_FontStyle>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_font\_style\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_font_style_name>`

Returns font style name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_font\_weight**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_font_weight>`

Returns weight (boldness) of the font. A value in the `100...999` range,
normal font weight is `400`, bold font weight is `700`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_height**(font\_size: `int<class_int>` = 16)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_height>`

Returns the total average font height (ascent plus descent) in pixels.

\*\*Note:\*\* Real height of the string is context-dependent and can be
significantly different from the value returned by this function. Use it
only as rough estimate (e.g. as the height of empty line).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_multiline\_string\_size**(text:
`String<class_String>`, alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` = 0, width:
`float<class_float>` = -1, font\_size: `int<class_int>` = 16,
max\_lines: `int<class_int>` = -1, brk\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`LineBreakFlag<enum_TextServer_LineBreakFlag>`\]
= 3, justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
= 3, direction: `Direction<enum_TextServer_Direction>` = 0, orientation:
`Orientation<enum_TextServer_Orientation>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_multiline_string_size>`

Returns the size of a bounding box of a string broken into the lines,
taking kerning and advance into account.

See also
`draw_multiline_string<class_Font_method_draw_multiline_string>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_opentype\_features**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_opentype_features>`

Returns a set of OpenType feature tags. More info: [OpenType feature
tags](https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_ot\_name\_strings**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_ot_name_strings>`

Returns `Dictionary<class_Dictionary>` with OpenType font name strings
(localized font names, version, description, license information, sample
text, etc.).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`RID<class_RID>`\] **get\_rids**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_rids>`

Returns `Array<class_Array>` of valid **Font** `RID<class_RID>`s, which
can be passed to the `TextServer<class_TextServer>` methods.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_spacing**(spacing:
`SpacingType<enum_TextServer_SpacingType>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_spacing>`

Returns the spacing for the given `type` (see
`SpacingType<enum_TextServer_SpacingType>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_string\_size**(text:
`String<class_String>`, alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` = 0, width:
`float<class_float>` = -1, font\_size: `int<class_int>` = 16,
justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
= 3, direction: `Direction<enum_TextServer_Direction>` = 0, orientation:
`Orientation<enum_TextServer_Orientation>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_string_size>`

Returns the size of a bounding box of a single-line string, taking
kerning, advance and subpixel positioning into account. See also
`get_multiline_string_size<class_Font_method_get_multiline_string_size>`
and `draw_string<class_Font_method_draw_string>`.

For example, to get the string size as displayed by a single-line Label,
use:

gdscript

var string\_size =
$Label.get\_theme\_font("font").get\_string\_size($Label.text,
HORIZONTAL\_ALIGNMENT\_LEFT, -1,
$Label.get\_theme\_font\_size("font\_size"))

csharp

Label label = GetNode&lt;Label&gt;("Label"); Vector2 stringSize =
label.GetThemeFont("font").GetStringSize(label.Text,
HorizontalAlignment.Left, -1, label.GetThemeFontSize("font\_size"));

\*\*Note:\*\* Since kerning, advance and subpixel positioning are taken
into account by `get_string_size<class_Font_method_get_string_size>`,
using separate `get_string_size<class_Font_method_get_string_size>`
calls on substrings of a string then adding the results together will
return a different result compared to using a single
`get_string_size<class_Font_method_get_string_size>` call on the full
string.

\*\*Note:\*\* Real height of the string is context-dependent and can be
significantly different from the value returned by
`get_height<class_Font_method_get_height>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_supported\_chars**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_supported_chars>`

Returns a string containing all the characters available in the font.

If a given character is included in more than one font data source, it
appears only once in the returned string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_supported\_feature\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_supported_feature_list>`

Returns list of OpenType features supported by font.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_supported\_variation\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_supported_variation_list>`

Returns list of supported [variation
coordinates](https://docs.microsoft.com/en-us/typography/opentype/spec/dvaraxisreg),
each coordinate is returned as
`tag: Vector3i(min_value,max_value,default_value)`.

Font variations allow for continuous change of glyph characteristics
along some given design axis, such as weight, width or slant.

To print available variation axes of a variable font:

    var fv = FontVariation.new()
    fv.base_font = load("res://RobotoFlex.ttf")
    var variation_list = fv.get_supported_variation_list()
    for tag in variation_list:
        var name = TextServerManager.get_primary_interface().tag_to_name(tag)
        var values = variation_list[tag]
        print("variation axis: %s (%d)\n\tmin, max, default: %s" % [name, tag, values])

\*\*Note:\*\* To set and get variation coordinates of a
`FontVariation<class_FontVariation>`, use
`FontVariation.variation_opentype<class_FontVariation_property_variation_opentype>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_underline\_position**(font\_size:
`int<class_int>` = 16)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_underline_position>`

Returns average pixel offset of the underline below the baseline.

\*\*Note:\*\* Real underline position of the string is context-dependent
and can be significantly different from the value returned by this
function. Use it only as rough estimate.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_underline\_thickness**(font\_size:
`int<class_int>` = 16)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_get_underline_thickness>`

Returns average thickness of the underline.

\*\*Note:\*\* Real underline thickness of the string is
context-dependent and can be significantly different from the value
returned by this function. Use it only as rough estimate.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_char**(char: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_has_char>`

Returns `true` if a Unicode `char` is available in the font.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_language\_supported**(language:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_is_language_supported>`

Returns `true`, if font supports given language ([ISO
639](https://en.wikipedia.org/wiki/ISO_639-1) code).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_script\_supported**(script:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Font_method_is_script_supported>`

Returns `true`, if font supports given script ([ISO
15924](https://en.wikipedia.org/wiki/ISO_15924) code).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_cache\_capacity**(single\_line:
`int<class_int>`, multi\_line: `int<class_int>`)
`🔗<class_Font_method_set_cache_capacity>`

Sets LRU cache capacity for `draw_*` methods.
