github\_url  
hide

# TextMesh

**Inherits:** `PrimitiveMesh<class_PrimitiveMesh>` **&lt;**
`Mesh<class_Mesh>` **&lt;** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Generate an `PrimitiveMesh<class_PrimitiveMesh>` from the text.

classref-introduction-group

## Description

Generate an `PrimitiveMesh<class_PrimitiveMesh>` from the text.

TextMesh can be generated only when using dynamic fonts with vector
glyph contours. Bitmap fonts (including bitmap data in the
TrueType/OpenType containers, like color emoji fonts) are not supported.

The UV layout is arranged in 4 horizontal strips, top to bottom: 40% of
the height for the front face, 40% for the back face, 10% for the outer
edges and 10% for the inner edges.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`AutowrapMode<enum_TextServer_AutowrapMode>` **autowrap\_mode** = `0`
`🔗<class_TextMesh_property_autowrap_mode>`

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

`float<class_float>` **curve\_step** = `0.5`
`🔗<class_TextMesh_property_curve_step>`

classref-property-setget

-   `void (No return value.)` **set\_curve\_step**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_curve\_step**()

Step (in pixels) used to approximate Bézier curves.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **depth** = `0.05`
`🔗<class_TextMesh_property_depth>`

classref-property-setget

-   `void (No return value.)` **set\_depth**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_depth**()

Depths of the mesh, if set to `0.0` only front surface, is generated,
and UV layout is changed to use full texture for the front face only.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Font<class_Font>` **font** `🔗<class_TextMesh_property_font>`

classref-property-setget

-   `void (No return value.)` **set\_font**(value: `Font<class_Font>`)
-   `Font<class_Font>` **get\_font**()

Font configuration used to display text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **font\_size** = `16`
`🔗<class_TextMesh_property_font_size>`

classref-property-setget

-   `void (No return value.)` **set\_font\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_font\_size**()

Font size of the **TextMesh**'s text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
**horizontal\_alignment** = `1`
`🔗<class_TextMesh_property_horizontal_alignment>`

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
`🔗<class_TextMesh_property_justification_flags>`

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
`🔗<class_TextMesh_property_language>`

classref-property-setget

-   `void (No return value.)` **set\_language**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_language**()

Language code used for text shaping algorithms, if left empty current
locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **line\_spacing** = `0.0`
`🔗<class_TextMesh_property_line_spacing>`

classref-property-setget

-   `void (No return value.)` **set\_line\_spacing**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_line\_spacing**()

Vertical space between lines in multiline **TextMesh**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **offset** = `Vector2(0, 0)`
`🔗<class_TextMesh_property_offset>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_offset**()

The text drawing offset (in pixels).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pixel\_size** = `0.01`
`🔗<class_TextMesh_property_pixel_size>`

classref-property-setget

-   `void (No return value.)` **set\_pixel\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pixel\_size**()

The size of one pixel's width on the text to scale it in 3D.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StructuredTextParser<enum_TextServer_StructuredTextParser>`
**structured\_text\_bidi\_override** = `0`
`🔗<class_TextMesh_property_structured_text_bidi_override>`

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
`[]` `🔗<class_TextMesh_property_structured_text_bidi_override_options>`

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

`String<class_String>` **text** = `""`
`🔗<class_TextMesh_property_text>`

classref-property-setget

-   `void (No return value.)` **set\_text**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_text**()

The text to generate mesh from.

\*\*Note:\*\* Due to being a `Resource<class_Resource>`, it doesn't
follow the rules of
`Node.auto_translate_mode<class_Node_property_auto_translate_mode>`. If
disabling translation is desired, it should be done manually with
`Object.set_message_translation<class_Object_method_set_message_translation>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Direction<enum_TextServer_Direction>` **text\_direction** = `0`
`🔗<class_TextMesh_property_text_direction>`

classref-property-setget

-   `void (No return value.)` **set\_text\_direction**(value:
    `Direction<enum_TextServer_Direction>`)
-   `Direction<enum_TextServer_Direction>` **get\_text\_direction**()

Base text writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **uppercase** = `false`
`🔗<class_TextMesh_property_uppercase>`

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
`🔗<class_TextMesh_property_vertical_alignment>`

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
`🔗<class_TextMesh_property_width>`

classref-property-setget

-   `void (No return value.)` **set\_width**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_width**()

Text width (in pixels), used for fill alignment.
