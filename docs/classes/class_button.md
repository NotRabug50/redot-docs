github\_url  
hide

# Button

**Inherits:** `BaseButton<class_BaseButton>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `CheckBox<class_CheckBox>`,
`CheckButton<class_CheckButton>`,
`ColorPickerButton<class_ColorPickerButton>`,
`MenuButton<class_MenuButton>`, `OptionButton<class_OptionButton>`

A themed button that can contain text and an icon.

classref-introduction-group

## Description

**Button** is the standard themed button. It can contain text and an
icon, and it will display them according to the current
`Theme<class_Theme>`.

\*\*Example of creating a button and assigning an action when pressed by
code:\*\*

gdscript

func \_ready():  
var button = Button.new() button.text = "Click me"
button.pressed.connect(self.\_button\_pressed) add\_child(button)

func \_button\_pressed():  
print("Hello world!")

csharp

public override void \_Ready() { var button = new Button(); button.Text
= "Click me"; button.Pressed += ButtonPressed; AddChild(button); }

private void ButtonPressed() { GD.Print("Hello world!"); }

See also `BaseButton<class_BaseButton>` which contains common properties
and methods associated with this node.

\*\*Note:\*\* Buttons do not interpret touch input and therefore don't
support multitouch, since mouse emulation can only press one button at a
given time. Use `TouchScreenButton<class_TouchScreenButton>` for buttons
that trigger gameplay movement or actions.

classref-introduction-group

## Tutorials

-   [2D Dodge The Creeps
    Demo](https://godotengine.org/asset-library/asset/2712)
-   [Operating System Testing
    Demo](https://godotengine.org/asset-library/asset/2789)

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
</tbody>
</table>

classref-reftable-group

## Theme Properties

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
**alignment** = `1` `🔗<class_Button_property_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_text\_alignment**(value:
    `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`)
-   `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
    **get\_text\_alignment**()

Text alignment policy for the button's text, use one of the
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AutowrapMode<enum_TextServer_AutowrapMode>` **autowrap\_mode** = `0`
`🔗<class_Button_property_autowrap_mode>`

classref-property-setget

-   `void (No return value.)` **set\_autowrap\_mode**(value:
    `AutowrapMode<enum_TextServer_AutowrapMode>`)
-   `AutowrapMode<enum_TextServer_AutowrapMode>`
    **get\_autowrap\_mode**()

If set to something other than
`TextServer.AUTOWRAP_OFF<class_TextServer_constant_AUTOWRAP_OFF>`, the
text gets wrapped inside the node's bounding rectangle.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **clip\_text** = `false`
`🔗<class_Button_property_clip_text>`

classref-property-setget

-   `void (No return value.)` **set\_clip\_text**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_clip\_text**()

When this property is enabled, text that is too large to fit the button
is clipped, when disabled the Button will always be wide enough to hold
the text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **expand\_icon** = `false`
`🔗<class_Button_property_expand_icon>`

classref-property-setget

-   `void (No return value.)` **set\_expand\_icon**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_expand\_icon**()

When enabled, the button's icon will expand/shrink to fit the button's
size while keeping its aspect. See also
`icon_max_width<class_Button_theme_constant_icon_max_width>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **flat** = `false` `🔗<class_Button_property_flat>`

classref-property-setget

-   `void (No return value.)` **set\_flat**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_flat**()

Flat buttons don't display decoration.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **icon** `🔗<class_Button_property_icon>`

classref-property-setget

-   `void (No return value.)` **set\_button\_icon**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_button\_icon**()

Button's icon, if text is present the icon will be placed before the
text.

To edit margin and spacing of the icon, use
`h_separation<class_Button_theme_constant_h_separation>` theme property
and `content_margin_*` properties of the used
`StyleBox<class_StyleBox>`es.

classref-item-separator

------------------------------------------------------------------------

classref-property

`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
**icon\_alignment** = `0` `🔗<class_Button_property_icon_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_icon\_alignment**(value:
    `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`)
-   `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
    **get\_icon\_alignment**()

Specifies if the icon should be aligned horizontally to the left, right,
or center of a button. Uses the same
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` constants
as the text alignment. If centered horizontally and vertically, text
will draw on top of the icon.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **language** = `""`
`🔗<class_Button_property_language>`

classref-property-setget

-   `void (No return value.)` **set\_language**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_language**()

Language code used for line-breaking and text shaping algorithms, if
left empty current locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **text** = `""` `🔗<class_Button_property_text>`

classref-property-setget

-   `void (No return value.)` **set\_text**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_text**()

The button's text that will be displayed inside the button's area.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextDirection<enum_Control_TextDirection>` **text\_direction** = `0`
`🔗<class_Button_property_text_direction>`

classref-property-setget

-   `void (No return value.)` **set\_text\_direction**(value:
    `TextDirection<enum_Control_TextDirection>`)
-   `TextDirection<enum_Control_TextDirection>`
    **get\_text\_direction**()

Base text writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`OverrunBehavior<enum_TextServer_OverrunBehavior>`
**text\_overrun\_behavior** = `0`
`🔗<class_Button_property_text_overrun_behavior>`

classref-property-setget

-   `void (No return value.)` **set\_text\_overrun\_behavior**(value:
    `OverrunBehavior<enum_TextServer_OverrunBehavior>`)
-   `OverrunBehavior<enum_TextServer_OverrunBehavior>`
    **get\_text\_overrun\_behavior**()

Sets the clipping behavior when the text exceeds the node's bounding
rectangle. See `OverrunBehavior<enum_TextServer_OverrunBehavior>` for a
description of all modes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VerticalAlignment<enum_@GlobalScope_VerticalAlignment>`
**vertical\_icon\_alignment** = `1`
`🔗<class_Button_property_vertical_icon_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_vertical\_icon\_alignment**(value:
    `VerticalAlignment<enum_@GlobalScope_VerticalAlignment>`)
-   `VerticalAlignment<enum_@GlobalScope_VerticalAlignment>`
    **get\_vertical\_icon\_alignment**()

Specifies if the icon should be aligned vertically to the top, bottom,
or center of a button. Uses the same
`VerticalAlignment<enum_@GlobalScope_VerticalAlignment>` constants as
the text alignment. If centered horizontally and vertically, text will
draw on top of the icon.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **font\_color** = `Color(0.875, 0.875, 0.875, 1)`
`🔗<class_Button_theme_color_font_color>`

Default text `Color<class_Color>` of the **Button**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_disabled\_color** =
`Color(0.875, 0.875, 0.875, 0.5)`
`🔗<class_Button_theme_color_font_disabled_color>`

Text `Color<class_Color>` used when the **Button** is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_focus\_color** =
`Color(0.95, 0.95, 0.95, 1)`
`🔗<class_Button_theme_color_font_focus_color>`

Text `Color<class_Color>` used when the **Button** is focused. Only
replaces the normal text color of the button. Disabled, hovered, and
pressed states take precedence over this color.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_hover\_color** =
`Color(0.95, 0.95, 0.95, 1)`
`🔗<class_Button_theme_color_font_hover_color>`

Text `Color<class_Color>` used when the **Button** is being hovered.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_hover\_pressed\_color** =
`Color(1, 1, 1, 1)`
`🔗<class_Button_theme_color_font_hover_pressed_color>`

Text `Color<class_Color>` used when the **Button** is being hovered and
pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_outline\_color** = `Color(0, 0, 0, 1)`
`🔗<class_Button_theme_color_font_outline_color>`

The tint of text outline of the **Button**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_pressed\_color** = `Color(1, 1, 1, 1)`
`🔗<class_Button_theme_color_font_pressed_color>`

Text `Color<class_Color>` used when the **Button** is being pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **icon\_disabled\_color** = `Color(1, 1, 1, 0.4)`
`🔗<class_Button_theme_color_icon_disabled_color>`

Icon modulate `Color<class_Color>` used when the **Button** is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **icon\_focus\_color** = `Color(1, 1, 1, 1)`
`🔗<class_Button_theme_color_icon_focus_color>`

Icon modulate `Color<class_Color>` used when the **Button** is focused.
Only replaces the normal modulate color of the button. Disabled,
hovered, and pressed states take precedence over this color.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **icon\_hover\_color** = `Color(1, 1, 1, 1)`
`🔗<class_Button_theme_color_icon_hover_color>`

Icon modulate `Color<class_Color>` used when the **Button** is being
hovered.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **icon\_hover\_pressed\_color** =
`Color(1, 1, 1, 1)`
`🔗<class_Button_theme_color_icon_hover_pressed_color>`

Icon modulate `Color<class_Color>` used when the **Button** is being
hovered and pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **icon\_normal\_color** = `Color(1, 1, 1, 1)`
`🔗<class_Button_theme_color_icon_normal_color>`

Default icon modulate `Color<class_Color>` of the **Button**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **icon\_pressed\_color** = `Color(1, 1, 1, 1)`
`🔗<class_Button_theme_color_icon_pressed_color>`

Icon modulate `Color<class_Color>` used when the **Button** is being
pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **align\_to\_largest\_stylebox** = `0`
`🔗<class_Button_theme_constant_align_to_largest_stylebox>`

This constant acts as a boolean. If `true`, the minimum size of the
button and text/icon alignment is always based on the largest stylebox
margins, otherwise it's based on the current button state stylebox
margins.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **h\_separation** = `4`
`🔗<class_Button_theme_constant_h_separation>`

The horizontal space between **Button**'s icon and text. Negative values
will be treated as `0` when used.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **icon\_max\_width** = `0`
`🔗<class_Button_theme_constant_icon_max_width>`

The maximum allowed width of the **Button**'s icon. This limit is
applied on top of the default size of the icon, or its expanded size if
`expand_icon<class_Button_property_expand_icon>` is `true`. The height
is adjusted according to the icon's ratio. If the button has additional
icons (e.g. `CheckBox<class_CheckBox>`), they will also be limited.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **outline\_size** = `0`
`🔗<class_Button_theme_constant_outline_size>`

The size of the text outline.

\*\*Note:\*\* If using a font with
`FontFile.multichannel_signed_distance_field<class_FontFile_property_multichannel_signed_distance_field>`
enabled, its
`FontFile.msdf_pixel_range<class_FontFile_property_msdf_pixel_range>`
must be set to at least *twice* the value of
`outline_size<class_Button_theme_constant_outline_size>` for outline
rendering to look correct. Otherwise, the outline may appear to be cut
off earlier than intended.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **font** `🔗<class_Button_theme_font_font>`

`Font<class_Font>` of the **Button**'s text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **font\_size**
`🔗<class_Button_theme_font_size_font_size>`

Font size of the **Button**'s text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **icon** `🔗<class_Button_theme_icon_icon>`

Default icon for the **Button**. Appears only if
`icon<class_Button_property_icon>` is not assigned.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **disabled**
`🔗<class_Button_theme_style_disabled>`

`StyleBox<class_StyleBox>` used when the **Button** is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **disabled\_mirrored**
`🔗<class_Button_theme_style_disabled_mirrored>`

`StyleBox<class_StyleBox>` used when the **Button** is disabled (for
right-to-left layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **focus**
`🔗<class_Button_theme_style_focus>`

`StyleBox<class_StyleBox>` used when the **Button** is focused. The
`focus<class_Button_theme_style_focus>` `StyleBox<class_StyleBox>` is
displayed *over* the base `StyleBox<class_StyleBox>`, so a partially
transparent `StyleBox<class_StyleBox>` should be used to ensure the base
`StyleBox<class_StyleBox>` remains visible. A `StyleBox<class_StyleBox>`
that represents an outline or an underline works well for this purpose.
To disable the focus visual effect, assign a
`StyleBoxEmpty<class_StyleBoxEmpty>` resource. Note that disabling the
focus visual effect will harm keyboard/controller navigation usability,
so this is not recommended for accessibility reasons.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **hover**
`🔗<class_Button_theme_style_hover>`

`StyleBox<class_StyleBox>` used when the **Button** is being hovered.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **hover\_mirrored**
`🔗<class_Button_theme_style_hover_mirrored>`

`StyleBox<class_StyleBox>` used when the **Button** is being hovered
(for right-to-left layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **hover\_pressed**
`🔗<class_Button_theme_style_hover_pressed>`

`StyleBox<class_StyleBox>` used when the **Button** is being pressed and
hovered at the same time.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **hover\_pressed\_mirrored**
`🔗<class_Button_theme_style_hover_pressed_mirrored>`

`StyleBox<class_StyleBox>` used when the **Button** is being pressed and
hovered at the same time (for right-to-left layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **normal**
`🔗<class_Button_theme_style_normal>`

Default `StyleBox<class_StyleBox>` for the **Button**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **normal\_mirrored**
`🔗<class_Button_theme_style_normal_mirrored>`

Default `StyleBox<class_StyleBox>` for the **Button** (for right-to-left
layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **pressed**
`🔗<class_Button_theme_style_pressed>`

`StyleBox<class_StyleBox>` used when the **Button** is being pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **pressed\_mirrored**
`🔗<class_Button_theme_style_pressed_mirrored>`

`StyleBox<class_StyleBox>` used when the **Button** is being pressed
(for right-to-left layouts).
