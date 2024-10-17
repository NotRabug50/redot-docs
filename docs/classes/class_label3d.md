github\_url  
hide

# Label3D

**Inherits:** `GeometryInstance3D<class_GeometryInstance3D>` **&lt;**
`VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A node for displaying plain text in 3D space.

classref-introduction-group

## Description

A node for displaying plain text in 3D space. By adjusting various
properties of this node, you can configure things such as the text's
appearance and whether it always faces the camera.

classref-introduction-group

## Tutorials

-   `3D text <../tutorials/3d/3d_text>`

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
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
</tr>
<tr>
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
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **DrawFlags**: `🔗<enum_Label3D_DrawFlags>`

classref-enumeration-constant

`DrawFlags<enum_Label3D_DrawFlags>` **FLAG\_SHADED** = `0`

If set, lights in the environment affect the label.

classref-enumeration-constant

`DrawFlags<enum_Label3D_DrawFlags>` **FLAG\_DOUBLE\_SIDED** = `1`

If set, text can be seen from the back as well. If not, the text is
invisible when looking at it from behind.

classref-enumeration-constant

`DrawFlags<enum_Label3D_DrawFlags>` **FLAG\_DISABLE\_DEPTH\_TEST** = `2`

Disables the depth test, so this object is drawn on top of all others.
However, objects drawn after it in the draw order may cover it.

classref-enumeration-constant

`DrawFlags<enum_Label3D_DrawFlags>` **FLAG\_FIXED\_SIZE** = `3`

Label is scaled by depth so that it always appears the same size on
screen.

classref-enumeration-constant

`DrawFlags<enum_Label3D_DrawFlags>` **FLAG\_MAX** = `4`

Represents the size of the `DrawFlags<enum_Label3D_DrawFlags>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AlphaCutMode**: `🔗<enum_Label3D_AlphaCutMode>`

classref-enumeration-constant

`AlphaCutMode<enum_Label3D_AlphaCutMode>` **ALPHA\_CUT\_DISABLED** = `0`

This mode performs standard alpha blending. It can display translucent
areas, but transparency sorting issues may be visible when multiple
transparent materials are overlapping.
`GeometryInstance3D.cast_shadow<class_GeometryInstance3D_property_cast_shadow>`
has no effect when this transparency mode is used; the **Label3D** will
never cast shadows.

classref-enumeration-constant

`AlphaCutMode<enum_Label3D_AlphaCutMode>` **ALPHA\_CUT\_DISCARD** = `1`

This mode only allows fully transparent or fully opaque pixels. Harsh
edges will be visible unless some form of screen-space antialiasing is
enabled (see
`ProjectSettings.rendering/anti_aliasing/quality/screen_space_aa<class_ProjectSettings_property_rendering/anti_aliasing/quality/screen_space_aa>`).
This mode is also known as *alpha testing* or *1-bit transparency*.

\*\*Note:\*\* This mode might have issues with anti-aliased fonts and
outlines, try adjusting
`alpha_scissor_threshold<class_Label3D_property_alpha_scissor_threshold>`
or using MSDF font.

\*\*Note:\*\* When using text with overlapping glyphs (e.g., cursive
scripts), this mode might have transparency sorting issues between the
main text and the outline.

classref-enumeration-constant

`AlphaCutMode<enum_Label3D_AlphaCutMode>`
**ALPHA\_CUT\_OPAQUE\_PREPASS** = `2`

This mode draws fully opaque pixels in the depth prepass. This is slower
than `ALPHA_CUT_DISABLED<class_Label3D_constant_ALPHA_CUT_DISABLED>` or
`ALPHA_CUT_DISCARD<class_Label3D_constant_ALPHA_CUT_DISCARD>`, but it
allows displaying translucent areas and smooth edges while using proper
sorting.

\*\*Note:\*\* When using text with overlapping glyphs (e.g., cursive
scripts), this mode might have transparency sorting issues between the
main text and the outline.

classref-enumeration-constant

`AlphaCutMode<enum_Label3D_AlphaCutMode>` **ALPHA\_CUT\_HASH** = `3`

This mode draws cuts off all values below a spatially-deterministic
threshold, the rest will remain opaque.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **alpha\_antialiasing\_edge** = `0.0`
`🔗<class_Label3D_property_alpha_antialiasing_edge>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_antialiasing\_edge**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_alpha\_antialiasing\_edge**()

Threshold at which antialiasing will be applied on the alpha channel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`
**alpha\_antialiasing\_mode** = `0`
`🔗<class_Label3D_property_alpha_antialiasing_mode>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_antialiasing**(value:
    `AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`)
-   `AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`
    **get\_alpha\_antialiasing**()

The type of alpha antialiasing to apply. See
`AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AlphaCutMode<enum_Label3D_AlphaCutMode>` **alpha\_cut** = `0`
`🔗<class_Label3D_property_alpha_cut>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_cut\_mode**(value:
    `AlphaCutMode<enum_Label3D_AlphaCutMode>`)
-   `AlphaCutMode<enum_Label3D_AlphaCutMode>`
    **get\_alpha\_cut\_mode**()

The alpha cutting mode to use for the sprite. See
`AlphaCutMode<enum_Label3D_AlphaCutMode>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **alpha\_hash\_scale** = `1.0`
`🔗<class_Label3D_property_alpha_hash_scale>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_hash\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_alpha\_hash\_scale**()

The hashing scale for Alpha Hash. Recommended values between `0` and
`2`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **alpha\_scissor\_threshold** = `0.5`
`🔗<class_Label3D_property_alpha_scissor_threshold>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_scissor\_threshold**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_alpha\_scissor\_threshold**()

Threshold at which the alpha scissor will discard values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AutowrapMode<enum_TextServer_AutowrapMode>` **autowrap\_mode** = `0`
`🔗<class_Label3D_property_autowrap_mode>`

classref-property-setget

-   `void (No return value.)` **set\_autowrap\_mode**(value:
    `AutowrapMode<enum_TextServer_AutowrapMode>`)
-   `AutowrapMode<enum_TextServer_AutowrapMode>`
    **get\_autowrap\_mode**()

If set to something other than
`TextServer.AUTOWRAP_OFF<class_TextServer_constant_AUTOWRAP_OFF>`, the
text gets wrapped inside the node's bounding rectangle. If you resize
the node, it will change its height automatically to show all the text.
To see how each mode behaves, see
`AutowrapMode<enum_TextServer_AutowrapMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BillboardMode<enum_BaseMaterial3D_BillboardMode>` **billboard** = `0`
`🔗<class_Label3D_property_billboard>`

classref-property-setget

-   `void (No return value.)` **set\_billboard\_mode**(value:
    `BillboardMode<enum_BaseMaterial3D_BillboardMode>`)
-   `BillboardMode<enum_BaseMaterial3D_BillboardMode>`
    **get\_billboard\_mode**()

The billboard mode to use for the label. See
`BillboardMode<enum_BaseMaterial3D_BillboardMode>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **double\_sided** = `true`
`🔗<class_Label3D_property_double_sided>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_flag**(flag:
    `DrawFlags<enum_Label3D_DrawFlags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_draw\_flag**(flag:
    `DrawFlags<enum_Label3D_DrawFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, text can be seen from the back as well, if `false`, it is
invisible when looking at it from behind.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **fixed\_size** = `false`
`🔗<class_Label3D_property_fixed_size>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_flag**(flag:
    `DrawFlags<enum_Label3D_DrawFlags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_draw\_flag**(flag:
    `DrawFlags<enum_Label3D_DrawFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the label is rendered at the same size regardless of
distance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Font<class_Font>` **font** `🔗<class_Label3D_property_font>`

classref-property-setget

-   `void (No return value.)` **set\_font**(value: `Font<class_Font>`)
-   `Font<class_Font>` **get\_font**()

Font configuration used to display text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **font\_size** = `32`
`🔗<class_Label3D_property_font_size>`

classref-property-setget

-   `void (No return value.)` **set\_font\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_font\_size**()

Font size of the **Label3D**'s text. To make the font look more detailed
when up close, increase `font_size<class_Label3D_property_font_size>`
while decreasing `pixel_size<class_Label3D_property_pixel_size>` at the
same time.

Higher font sizes require more time to render new characters, which can
cause stuttering during gameplay.

classref-item-separator

------------------------------------------------------------------------

classref-property

`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
**horizontal\_alignment** = `1`
`🔗<class_Label3D_property_horizontal_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_horizontal\_alignment**(value:
    `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`)
-   `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
    **get\_horizontal\_alignment**()

Controls the text's horizontal alignment. Supports left, center, right,
and fill, or justify. Set it to one of the
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
**justification\_flags** = `163`
`🔗<class_Label3D_property_justification_flags>`

classref-property-setget

-   `void (No return value.)` **set\_justification\_flags**(value:
    `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\])
-   `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
    **get\_justification\_flags**()

Line fill alignment rules. See
`JustificationFlag<enum_TextServer_JustificationFlag>` for more
information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **language** = `""`
`🔗<class_Label3D_property_language>`

classref-property-setget

-   `void (No return value.)` **set\_language**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_language**()

Language code used for line-breaking and text shaping algorithms, if
left empty current locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **line\_spacing** = `0.0`
`🔗<class_Label3D_property_line_spacing>`

classref-property-setget

-   `void (No return value.)` **set\_line\_spacing**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_line\_spacing**()

Vertical space between lines in multiline **Label3D**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **modulate** = `Color(1, 1, 1, 1)`
`🔗<class_Label3D_property_modulate>`

classref-property-setget

-   `void (No return value.)` **set\_modulate**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_modulate**()

Text `Color<class_Color>` of the **Label3D**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **no\_depth\_test** = `false`
`🔗<class_Label3D_property_no_depth_test>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_flag**(flag:
    `DrawFlags<enum_Label3D_DrawFlags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_draw\_flag**(flag:
    `DrawFlags<enum_Label3D_DrawFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, depth testing is disabled and the object will be drawn in
render order.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **offset** = `Vector2(0, 0)`
`🔗<class_Label3D_property_offset>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_offset**()

The text drawing offset (in pixels).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **outline\_modulate** = `Color(0, 0, 0, 1)`
`🔗<class_Label3D_property_outline_modulate>`

classref-property-setget

-   `void (No return value.)` **set\_outline\_modulate**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_outline\_modulate**()

The tint of text outline.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **outline\_render\_priority** = `-1`
`🔗<class_Label3D_property_outline_render_priority>`

classref-property-setget

-   `void (No return value.)` **set\_outline\_render\_priority**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_outline\_render\_priority**()

Sets the render priority for the text outline. Higher priority objects
will be sorted in front of lower priority objects.

\*\*Note:\*\* This only applies if
`alpha_cut<class_Label3D_property_alpha_cut>` is set to
`ALPHA_CUT_DISABLED<class_Label3D_constant_ALPHA_CUT_DISABLED>` (default
value).

\*\*Note:\*\* This only applies to sorting of transparent objects. This
will not impact how transparent objects are sorted relative to opaque
objects. This is because opaque objects are not sorted, while
transparent objects are sorted from back to front (subject to priority).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **outline\_size** = `12`
`🔗<class_Label3D_property_outline_size>`

classref-property-setget

-   `void (No return value.)` **set\_outline\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_outline\_size**()

Text outline size.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pixel\_size** = `0.005`
`🔗<class_Label3D_property_pixel_size>`

classref-property-setget

-   `void (No return value.)` **set\_pixel\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pixel\_size**()

The size of one pixel's width on the label to scale it in 3D. To make
the font look more detailed when up close, increase
`font_size<class_Label3D_property_font_size>` while decreasing
`pixel_size<class_Label3D_property_pixel_size>` at the same time.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **render\_priority** = `0`
`🔗<class_Label3D_property_render_priority>`

classref-property-setget

-   `void (No return value.)` **set\_render\_priority**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_render\_priority**()

Sets the render priority for the text. Higher priority objects will be
sorted in front of lower priority objects.

\*\*Note:\*\* This only applies if
`alpha_cut<class_Label3D_property_alpha_cut>` is set to
`ALPHA_CUT_DISABLED<class_Label3D_constant_ALPHA_CUT_DISABLED>` (default
value).

\*\*Note:\*\* This only applies to sorting of transparent objects. This
will not impact how transparent objects are sorted relative to opaque
objects. This is because opaque objects are not sorted, while
transparent objects are sorted from back to front (subject to priority).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shaded** = `false`
`🔗<class_Label3D_property_shaded>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_flag**(flag:
    `DrawFlags<enum_Label3D_DrawFlags>`, enabled: `bool<class_bool>`)
-   `bool<class_bool>` **get\_draw\_flag**(flag:
    `DrawFlags<enum_Label3D_DrawFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the `Light3D<class_Light3D>` in the
`Environment<class_Environment>` has effects on the label.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StructuredTextParser<enum_TextServer_StructuredTextParser>`
**structured\_text\_bidi\_override** = `0`
`🔗<class_Label3D_property_structured_text_bidi_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_structured\_text\_bidi\_override**(value:
    `StructuredTextParser<enum_TextServer_StructuredTextParser>`)
-   `StructuredTextParser<enum_TextServer_StructuredTextParser>`
    **get\_structured\_text\_bidi\_override**()

Set BiDi algorithm override for the structured text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>` **structured\_text\_bidi\_override\_options** =
`[]` `🔗<class_Label3D_property_structured_text_bidi_override_options>`

classref-property-setget

-   `void (No return value.)`
    **set\_structured\_text\_bidi\_override\_options**(value:
    `Array<class_Array>`)
-   `Array<class_Array>`
    **get\_structured\_text\_bidi\_override\_options**()

Set additional options for BiDi override.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **text** = `""` `🔗<class_Label3D_property_text>`

classref-property-setget

-   `void (No return value.)` **set\_text**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_text**()

The text to display on screen.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Direction<enum_TextServer_Direction>` **text\_direction** = `0`
`🔗<class_Label3D_property_text_direction>`

classref-property-setget

-   `void (No return value.)` **set\_text\_direction**(value:
    `Direction<enum_TextServer_Direction>`)
-   `Direction<enum_TextServer_Direction>` **get\_text\_direction**()

Base text writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureFilter<enum_BaseMaterial3D_TextureFilter>` **texture\_filter** =
`3` `🔗<class_Label3D_property_texture_filter>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_filter**(value:
    `TextureFilter<enum_BaseMaterial3D_TextureFilter>`)
-   `TextureFilter<enum_BaseMaterial3D_TextureFilter>`
    **get\_texture\_filter**()

Filter flags for the texture. See
`TextureFilter<enum_BaseMaterial3D_TextureFilter>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **uppercase** = `false`
`🔗<class_Label3D_property_uppercase>`

classref-property-setget

-   `void (No return value.)` **set\_uppercase**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_uppercase**()

If `true`, all the text displays as UPPERCASE.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VerticalAlignment<enum_@GlobalScope_VerticalAlignment>`
**vertical\_alignment** = `1`
`🔗<class_Label3D_property_vertical_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_vertical\_alignment**(value:
    `VerticalAlignment<enum_@GlobalScope_VerticalAlignment>`)
-   `VerticalAlignment<enum_@GlobalScope_VerticalAlignment>`
    **get\_vertical\_alignment**()

Controls the text's vertical alignment. Supports top, center, bottom.
Set it to one of the
`VerticalAlignment<enum_@GlobalScope_VerticalAlignment>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **width** = `500.0`
`🔗<class_Label3D_property_width>`

classref-property-setget

-   `void (No return value.)` **set\_width**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_width**()

Text width (in pixels), used for autowrap and fill alignment.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`TriangleMesh<class_TriangleMesh>` **generate\_triangle\_mesh**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Label3D_method_generate_triangle_mesh>`

Returns a `TriangleMesh<class_TriangleMesh>` with the label's vertices
following its current configuration (such as its
`pixel_size<class_Label3D_property_pixel_size>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_draw\_flag**(flag:
`DrawFlags<enum_Label3D_DrawFlags>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Label3D_method_get_draw_flag>`

Returns the value of the specified flag.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_draw\_flag**(flag:
`DrawFlags<enum_Label3D_DrawFlags>`, enabled: `bool<class_bool>`)
`🔗<class_Label3D_method_set_draw_flag>`

If `true`, the specified flag will be enabled. See
`DrawFlags<enum_Label3D_DrawFlags>` for a list of flags.
