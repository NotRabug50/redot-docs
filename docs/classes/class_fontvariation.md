github\_url  
hide

# FontVariation

**Inherits:** `Font<class_Font>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A variation of a font with additional settings.

classref-introduction-group

## Description

Provides OpenType variations, simulated bold / slant, and additional
font settings like OpenType features and extra spacing.

To use simulated bold font variant:

gdscript

var fv = FontVariation.new() fv.base\_font =
load("<res://BarlowCondensed-Regular.ttf>") fv.variation\_embolden = 1.2
$Label.add\_theme\_font\_override("font", fv)
$Label.add\_theme\_font\_size\_override("font\_size", 64)

csharp

var fv = new FontVariation();
fv.SetBaseFont(ResourceLoader.Load&lt;FontFile&gt;("<res://BarlowCondensed-Regular.ttf>"));
fv.SetVariationEmbolden(1.2);
GetNode("Label").AddThemeFontOverride("font", fv);
GetNode("Label").AddThemeFontSizeOverride("font\_size", 64);

To set the coordinate of multiple variation axes:

    var fv = FontVariation.new();
    var ts = TextServerManager.get_primary_interface()
    fv.base_font = load("res://BarlowCondensed-Regular.ttf")
    fv.variation_opentype = { ts.name_to_tag("wght"): 900, ts.name_to_tag("custom_hght"): 900 }

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

`Font<class_Font>` **base\_font**
`🔗<class_FontVariation_property_base_font>`

classref-property-setget

-   `void (No return value.)` **set\_base\_font**(value:
    `Font<class_Font>`)
-   `Font<class_Font>` **get\_base\_font**()

Base font used to create a variation. If not set, default
`Theme<class_Theme>` font is used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **baseline\_offset** = `0.0`
`🔗<class_FontVariation_property_baseline_offset>`

classref-property-setget

-   `void (No return value.)` **set\_baseline\_offset**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_baseline\_offset**()

Extra baseline offset (as a fraction of font height).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Dictionary<class_Dictionary>` **opentype\_features** = `{}`
`🔗<class_FontVariation_property_opentype_features>`

classref-property-setget

-   `void (No return value.)` **set\_opentype\_features**(value:
    `Dictionary<class_Dictionary>`)
-   `Dictionary<class_Dictionary>` **get\_opentype\_features**()

A set of OpenType feature tags. More info: [OpenType feature
tags](https://docs.microsoft.com/en-us/typography/opentype/spec/featuretags).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **spacing\_bottom** = `0`
`🔗<class_FontVariation_property_spacing_bottom>`

classref-property-setget

-   `void (No return value.)` **set\_spacing**(spacing:
    `SpacingType<enum_TextServer_SpacingType>`, value: `int<class_int>`)
-   `int<class_int>` **get\_spacing**()

Extra spacing at the bottom of the line in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **spacing\_glyph** = `0`
`🔗<class_FontVariation_property_spacing_glyph>`

classref-property-setget

-   `void (No return value.)` **set\_spacing**(spacing:
    `SpacingType<enum_TextServer_SpacingType>`, value: `int<class_int>`)
-   `int<class_int>` **get\_spacing**()

Extra spacing between graphical glyphs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **spacing\_space** = `0`
`🔗<class_FontVariation_property_spacing_space>`

classref-property-setget

-   `void (No return value.)` **set\_spacing**(spacing:
    `SpacingType<enum_TextServer_SpacingType>`, value: `int<class_int>`)
-   `int<class_int>` **get\_spacing**()

Extra width of the space glyphs.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **spacing\_top** = `0`
`🔗<class_FontVariation_property_spacing_top>`

classref-property-setget

-   `void (No return value.)` **set\_spacing**(spacing:
    `SpacingType<enum_TextServer_SpacingType>`, value: `int<class_int>`)
-   `int<class_int>` **get\_spacing**()

Extra spacing at the top of the line in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **variation\_embolden** = `0.0`
`🔗<class_FontVariation_property_variation_embolden>`

classref-property-setget

-   `void (No return value.)` **set\_variation\_embolden**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_variation\_embolden**()

If is not equal to zero, emboldens the font outlines. Negative values
reduce the outline thickness.

\*\*Note:\*\* Emboldened fonts might have self-intersecting outlines,
which will prevent MSDF fonts and `TextMesh<class_TextMesh>` from
working correctly.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **variation\_face\_index** = `0`
`🔗<class_FontVariation_property_variation_face_index>`

classref-property-setget

-   `void (No return value.)` **set\_variation\_face\_index**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_variation\_face\_index**()

Active face index in the TrueType / OpenType collection file.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Dictionary<class_Dictionary>` **variation\_opentype** = `{}`
`🔗<class_FontVariation_property_variation_opentype>`

classref-property-setget

-   `void (No return value.)` **set\_variation\_opentype**(value:
    `Dictionary<class_Dictionary>`)
-   `Dictionary<class_Dictionary>` **get\_variation\_opentype**()

Font OpenType variation coordinates. More info: [OpenType variation
tags](https://docs.microsoft.com/en-us/typography/opentype/spec/dvaraxisreg).

\*\*Note:\*\* This `Dictionary<class_Dictionary>` uses OpenType tags as
keys. Variation axes can be identified both by tags (`int<class_int>`,
e.g. `0x77678674`) and names (`String<class_String>`, e.g. `wght`). Some
axes might be accessible by multiple names. For example, `wght` refers
to the same axis as `weight`. Tags on the other hand are unique. To
convert between names and tags, use
`TextServer.name_to_tag<class_TextServer_method_name_to_tag>` and
`TextServer.tag_to_name<class_TextServer_method_tag_to_name>`.

\*\*Note:\*\* To get available variation axes of a font, use
`Font.get_supported_variation_list<class_Font_method_get_supported_variation_list>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform2D<class_Transform2D>` **variation\_transform** =
`Transform2D(1, 0, 0, 1, 0, 0)`
`🔗<class_FontVariation_property_variation_transform>`

classref-property-setget

-   `void (No return value.)` **set\_variation\_transform**(value:
    `Transform2D<class_Transform2D>`)
-   `Transform2D<class_Transform2D>` **get\_variation\_transform**()

2D transform, applied to the font outlines, can be used for slanting,
flipping and rotating glyphs.

For example, to simulate italic typeface by slanting, apply the
following transform `Transform2D(1.0, slant, 0.0, 1.0, 0.0, 0.0)`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **set\_spacing**(spacing:
`SpacingType<enum_TextServer_SpacingType>`, value: `int<class_int>`)
`🔗<class_FontVariation_method_set_spacing>`

Sets the spacing for `spacing` (see
`SpacingType<enum_TextServer_SpacingType>`) to `value` in pixels (not
relative to the font size).
