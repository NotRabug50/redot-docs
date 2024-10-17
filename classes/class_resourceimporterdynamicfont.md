github\_url  
hide

# ResourceImporterDynamicFont

**Inherits:** `ResourceImporter<class_ResourceImporter>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Imports a TTF, TTC, OTF, OTC, WOFF or WOFF2 font file for font rendering
that adapts to any size.

classref-introduction-group

## Description

Unlike bitmap fonts, dynamic fonts can be resized to any size and still
look crisp. Dynamic fonts also optionally support MSDF font rendering,
which allows for run-time scale changes with no re-rasterization cost.

While WOFF and especially WOFF2 tend to result in smaller file sizes,
there is no universally "better" font format. In most situations, it's
recommended to use the font format that was shipped on the font
developer's website.

See also `ResourceImporterBMFont<class_ResourceImporterBMFont>` and
`ResourceImporterImageFont<class_ResourceImporterImageFont>`.

classref-introduction-group

## Tutorials

-   [Dynamic fonts - Using
    fonts](../tutorials/ui/gui_using_fonts.html#dynamic-fonts)

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

`bool<class_bool>` **allow\_system\_fallback** = `true`
`🔗<class_ResourceImporterDynamicFont_property_allow_system_fallback>`

If `true`, automatically use system fonts as a fallback if a glyph isn't
found in this dynamic font. This makes supporting CJK characters or
emoji more straightforward, as you don't need to include a CJK/emoji
font in your project. See also
`fallbacks<class_ResourceImporterDynamicFont_property_fallbacks>`.

\*\*Note:\*\* The appearance of system fonts varies across platforms.
Loading system fonts is only supported on Windows, macOS, Linux, Android
and iOS.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **antialiasing** = `1`
`🔗<class_ResourceImporterDynamicFont_property_antialiasing>`

The font antialiasing method to use.

\*\*Disabled:\*\* Most suited for pixel art fonts, although you do not
*have* to change the antialiasing from the default **Grayscale** if the
font file was well-created and the font is used at an integer multiple
of its intended size. If pixel art fonts have a bad appearance at their
intended size, try setting
`subpixel_positioning<class_ResourceImporterDynamicFont_property_subpixel_positioning>`
to **Disabled** instead.

\*\*Grayscale:\*\* Use grayscale antialiasing. This is the approach used
by the operating system on macOS, Android and iOS.

\*\*LCD Subpixel:\*\* Use antialiasing with subpixel patterns to make
fonts sharper on LCD displays. This is the approach used by the
operating system on Windows and most Linux distributions. The downside
is that this can introduce "fringing" on edges, especially on display
technologies that don't use standard RGB subpixels (such as OLED
displays). The LCD subpixel layout is globally controlled by
`ProjectSettings.gui/theme/lcd_subpixel_layout<class_ProjectSettings_property_gui/theme/lcd_subpixel_layout>`,
which also allows falling back to grayscale antialiasing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **compress** = `true`
`🔗<class_ResourceImporterDynamicFont_property_compress>`

If `true`, uses lossless compression for the resulting font.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disable\_embedded\_bitmaps** = `true`
`🔗<class_ResourceImporterDynamicFont_property_disable_embedded_bitmaps>`

If set to `true`, embedded font bitmap loading is disabled (bitmap-only
and color fonts ignore this property).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>` **fallbacks** = `[]`
`🔗<class_ResourceImporterDynamicFont_property_fallbacks>`

List of font fallbacks to use if a glyph isn't found in this dynamic
font. Fonts at the beginning of the array are attempted first, but
fallback fonts that don't support the glyph's language and script are
attempted last (see
`language_support<class_ResourceImporterDynamicFont_property_language_support>`
and
`script_support<class_ResourceImporterDynamicFont_property_script_support>`).
See also
`allow_system_fallback<class_ResourceImporterDynamicFont_property_allow_system_fallback>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **force\_autohinter** = `false`
`🔗<class_ResourceImporterDynamicFont_property_force_autohinter>`

If `true`, forces generation of hinting data for the font using
[FreeType](https://freetype.org/)'s autohinter. This will make
`hinting<class_ResourceImporterDynamicFont_property_hinting>` effective
with fonts that don't include hinting data.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **generate\_mipmaps** = `false`
`🔗<class_ResourceImporterDynamicFont_property_generate_mipmaps>`

If `true`, this font will have mipmaps generated. This prevents text
from looking grainy when a `Control<class_Control>` is scaled down, or
when a `Label3D<class_Label3D>` is viewed from a long distance (if
`Label3D.texture_filter<class_Label3D_property_texture_filter>` is set
to a mode that displays mipmaps).

Enabling
`generate_mipmaps<class_ResourceImporterDynamicFont_property_generate_mipmaps>`
increases font generation time and memory usage. Only enable this
setting if you actually need it.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **hinting** = `1`
`🔗<class_ResourceImporterDynamicFont_property_hinting>`

The hinting mode to use. This controls how aggressively glyph edges
should be snapped to pixels when rasterizing the font. Depending on
personal preference, you may prefer using one hinting mode over the
other. Hinting modes other than **None** are only effective if the font
contains hinting data (see
`force_autohinter<class_ResourceImporterDynamicFont_property_force_autohinter>`).

\*\*None:\*\* Smoothest appearance, which can make the font look blurry
at small sizes.

\*\*Light:\*\* Sharp result by snapping glyph edges to pixels on the Y
axis only.

\*\*Full:\*\* Sharpest by snapping glyph edges to pixels on both X and Y
axes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Dictionary<class_Dictionary>` **language\_support** = `{}`
`🔗<class_ResourceImporterDynamicFont_property_language_support>`

Override the list of languages supported by this font. If left empty,
this is supplied by the font metadata. There is usually no need to
change this. See also
`script_support<class_ResourceImporterDynamicFont_property_script_support>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **msdf\_pixel\_range** = `8`
`🔗<class_ResourceImporterDynamicFont_property_msdf_pixel_range>`

The width of the range around the shape between the minimum and maximum
representable signed distance. If using font outlines,
`msdf_pixel_range<class_ResourceImporterDynamicFont_property_msdf_pixel_range>`
must be set to at least *twice* the size of the largest font outline.
The default
`msdf_pixel_range<class_ResourceImporterDynamicFont_property_msdf_pixel_range>`
value of `8` allows outline sizes up to `4` to look correct.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **msdf\_size** = `48`
`🔗<class_ResourceImporterDynamicFont_property_msdf_size>`

Source font size used to generate MSDF textures. Higher values allow for
more precision, but are slower to render and require more memory. Only
increase this value if you notice a visible lack of precision in glyph
rendering. Only effective if
`multichannel_signed_distance_field<class_ResourceImporterDynamicFont_property_multichannel_signed_distance_field>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **multichannel\_signed\_distance\_field** = `false`
`🔗<class_ResourceImporterDynamicFont_property_multichannel_signed_distance_field>`

If set to `true`, the font will use multichannel signed distance field
(MSDF) for crisp rendering at any size. Since this approach does not
rely on rasterizing the font every time its size changes, this allows
for resizing the font in real-time without any performance penalty. Text
will also not look grainy for `Control<class_Control>`s that are scaled
down (or for `Label3D<class_Label3D>`s viewed from a long distance).

MSDF font rendering can be combined with
`generate_mipmaps<class_ResourceImporterDynamicFont_property_generate_mipmaps>`
to further improve font rendering quality when scaled down.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Dictionary<class_Dictionary>` **opentype\_features** = `{}`
`🔗<class_ResourceImporterDynamicFont_property_opentype_features>`

The OpenType features to enable, disable or set a value for this font.
This can be used to enable optional features provided by the font, such
as ligatures or alternative glyphs. The list of supported OpenType
features varies on a per-font basis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **oversampling** = `0.0`
`🔗<class_ResourceImporterDynamicFont_property_oversampling>`

If set to a value greater than `0.0`, overrides the oversampling factor
for the font. This can be used to render the font at a higher or lower
resolution than intended without affecting its physical size. In most
cases, this should be left at `0.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>` **preload** = `[]`
`🔗<class_ResourceImporterDynamicFont_property_preload>`

The glyph ranges to prerender. This can avoid stuttering during gameplay
when new characters need to be rendered, especially if
`subpixel_positioning<class_ResourceImporterDynamicFont_property_subpixel_positioning>`
is enabled. The downside of using preloading is that initial project
load times will increase, as well as memory usage.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Dictionary<class_Dictionary>` **script\_support** = `{}`
`🔗<class_ResourceImporterDynamicFont_property_script_support>`

Override the list of language scripts supported by this font. If left
empty, this is supplied by the font metadata. There is usually no need
to change this. See also
`language_support<class_ResourceImporterDynamicFont_property_language_support>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **subpixel\_positioning** = `4`
`🔗<class_ResourceImporterDynamicFont_property_subpixel_positioning>`

Subpixel positioning improves font rendering appearance, especially at
smaller font sizes. The downside is that it takes more time to initially
render the font, which can cause stuttering during gameplay, especially
if used with large font sizes. This should be set to **Disabled** for
fonts with a pixel art appearance.

\*\*Disabled:\*\* No subpixel positioning. Lowest quality, fastest
rendering.

\*\*Auto:\*\* Use subpixel positioning at small font sizes (the chosen
quality varies depending on font size). Large fonts will not use
subpixel positioning. This is a good tradeoff between performance and
quality.

\*\*One Half of a Pixel:\*\* Always perform intermediate subpixel
positioning regardless of font size. High quality, slow rendering.

\*\*One Quarter of a Pixel:\*\* Always perform precise subpixel
positioning regardless of font size. Highest quality, slowest rendering.

\*\*Auto (Except Pixel Fonts):\*\* **Disabled** for the pixel style
fonts (each glyph contours contain only straight horizontal and vertical
lines), **Auto** for the other fonts.
