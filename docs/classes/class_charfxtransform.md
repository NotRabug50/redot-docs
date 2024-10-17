github\_url  
hide

# CharFXTransform

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Controls how an individual character will be displayed in a
`RichTextEffect<class_RichTextEffect>`.

classref-introduction-group

## Description

By setting various properties on this object, you can control how
individual characters will be displayed in a
`RichTextEffect<class_RichTextEffect>`.

classref-introduction-group

## Tutorials

-   `BBCode in RichTextLabel <../tutorials/ui/bbcode_in_richtextlabel>`
-   [RichTextEffect test project
    (third-party)](https://github.com/Eoin-ONeill-Yokai/Godot-Rich-Text-Effect-Test-Project)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Color<class_Color>` **color** = `Color(0, 0, 0, 1)`
`🔗<class_CharFXTransform_property_color>`

classref-property-setget

-   `void (No return value.)` **set\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_color**()

The color the character will be drawn with.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **elapsed\_time** = `0.0`
`🔗<class_CharFXTransform_property_elapsed_time>`

classref-property-setget

-   `void (No return value.)` **set\_elapsed\_time**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_elapsed\_time**()

The time elapsed since the `RichTextLabel<class_RichTextLabel>` was
added to the scene tree (in seconds). Time stops when the
`RichTextLabel<class_RichTextLabel>` is paused (see
`Node.process_mode<class_Node_property_process_mode>`). Resets when the
text in the `RichTextLabel<class_RichTextLabel>` is changed.

\*\*Note:\*\* Time still passes while the
`RichTextLabel<class_RichTextLabel>` is hidden.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Dictionary<class_Dictionary>` **env** = `{}`
`🔗<class_CharFXTransform_property_env>`

classref-property-setget

-   `void (No return value.)` **set\_environment**(value:
    `Dictionary<class_Dictionary>`)
-   `Dictionary<class_Dictionary>` **get\_environment**()

Contains the arguments passed in the opening BBCode tag. By default,
arguments are strings; if their contents match a type such as
`bool<class_bool>`, `int<class_int>` or `float<class_float>`, they will
be converted automatically. Color codes in the form `#rrggbb` or `#rgb`
will be converted to an opaque `Color<class_Color>`. String arguments
may not contain spaces, even if they're quoted. If present, quotes will
also be present in the final string.

For example, the opening BBCode tag
`[example foo=hello bar=true baz=42 color=#ffffff]` will map to the
following `Dictionary<class_Dictionary>`:

    {"foo": "hello", "bar": true, "baz": 42, "color": Color(1, 1, 1, 1)}

classref-item-separator

------------------------------------------------------------------------

classref-property

`RID<class_RID>` **font** = `RID()`
`🔗<class_CharFXTransform_property_font>`

classref-property-setget

-   `void (No return value.)` **set\_font**(value: `RID<class_RID>`)
-   `RID<class_RID>` **get\_font**()

Font resource used to render glyph.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **glyph\_count** = `0`
`🔗<class_CharFXTransform_property_glyph_count>`

classref-property-setget

-   `void (No return value.)` **set\_glyph\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_glyph\_count**()

Number of glyphs in the grapheme cluster. This value is set in the first
glyph of a cluster. Setting this property won't affect drawing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **glyph\_flags** = `0`
`🔗<class_CharFXTransform_property_glyph_flags>`

classref-property-setget

-   `void (No return value.)` **set\_glyph\_flags**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_glyph\_flags**()

Glyph flags. See `GraphemeFlag<enum_TextServer_GraphemeFlag>` for more
info. Setting this property won't affect drawing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **glyph\_index** = `0`
`🔗<class_CharFXTransform_property_glyph_index>`

classref-property-setget

-   `void (No return value.)` **set\_glyph\_index**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_glyph\_index**()

Font specific glyph index.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **offset** = `Vector2(0, 0)`
`🔗<class_CharFXTransform_property_offset>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_offset**()

The position offset the character will be drawn with (in pixels).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **outline** = `false`
`🔗<class_CharFXTransform_property_outline>`

classref-property-setget

-   `void (No return value.)` **set\_outline**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_outline**()

If `true`, FX transform is called for outline drawing. Setting this
property won't affect drawing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **range** = `Vector2i(0, 0)`
`🔗<class_CharFXTransform_property_range>`

classref-property-setget

-   `void (No return value.)` **set\_range**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_range**()

Absolute character range in the string, corresponding to the glyph.
Setting this property won't affect drawing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **relative\_index** = `0`
`🔗<class_CharFXTransform_property_relative_index>`

classref-property-setget

-   `void (No return value.)` **set\_relative\_index**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_relative\_index**()

The character offset of the glyph, relative to the current
`RichTextEffect<class_RichTextEffect>` custom block. Setting this
property won't affect drawing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform2D<class_Transform2D>` **transform** =
`Transform2D(1, 0, 0, 1, 0, 0)`
`🔗<class_CharFXTransform_property_transform>`

classref-property-setget

-   `void (No return value.)` **set\_transform**(value:
    `Transform2D<class_Transform2D>`)
-   `Transform2D<class_Transform2D>` **get\_transform**()

The current transform of the current glyph. It can be overridden (for
example, by driving the position and rotation from a curve). You can
also alter the existing value to apply transforms on top of other
effects.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **visible** = `true`
`🔗<class_CharFXTransform_property_visible>`

classref-property-setget

-   `void (No return value.)` **set\_visibility**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_visible**()

If `true`, the character will be drawn. If `false`, the character will
be hidden. Characters around hidden characters will reflow to take the
space of hidden characters. If this is not desired, set their
`color<class_CharFXTransform_property_color>` to `Color(1, 1, 1, 0)`
instead.
