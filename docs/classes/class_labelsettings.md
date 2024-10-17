github\_url  
hide

# LabelSettings

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Provides common settings to customize the text in a
`Label<class_Label>`.

classref-introduction-group

## Description

**LabelSettings** is a resource that provides common settings to
customize the text in a `Label<class_Label>`. It will take priority over
the properties defined in `Control.theme<class_Control_property_theme>`.
The resource can be shared between multiple labels and changed on the
fly, so it's convenient and flexible way to setup text style.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Font<class_Font>` **font** `🔗<class_LabelSettings_property_font>`

classref-property-setget

-   `void (No return value.)` **set\_font**(value: `Font<class_Font>`)
-   `Font<class_Font>` **get\_font**()

`Font<class_Font>` used for the text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **font\_color** = `Color(1, 1, 1, 1)`
`🔗<class_LabelSettings_property_font_color>`

classref-property-setget

-   `void (No return value.)` **set\_font\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_font\_color**()

Color of the text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **font\_size** = `16`
`🔗<class_LabelSettings_property_font_size>`

classref-property-setget

-   `void (No return value.)` **set\_font\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_font\_size**()

Size of the text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **line\_spacing** = `3.0`
`🔗<class_LabelSettings_property_line_spacing>`

classref-property-setget

-   `void (No return value.)` **set\_line\_spacing**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_line\_spacing**()

Vertical space between lines when the text is multiline.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **outline\_color** = `Color(1, 1, 1, 1)`
`🔗<class_LabelSettings_property_outline_color>`

classref-property-setget

-   `void (No return value.)` **set\_outline\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_outline\_color**()

The color of the outline.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **outline\_size** = `0`
`🔗<class_LabelSettings_property_outline_size>`

classref-property-setget

-   `void (No return value.)` **set\_outline\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_outline\_size**()

Text outline size.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **shadow\_color** = `Color(0, 0, 0, 0)`
`🔗<class_LabelSettings_property_shadow_color>`

classref-property-setget

-   `void (No return value.)` **set\_shadow\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_shadow\_color**()

Color of the shadow effect. If alpha is `0`, no shadow will be drawn.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **shadow\_offset** = `Vector2(1, 1)`
`🔗<class_LabelSettings_property_shadow_offset>`

classref-property-setget

-   `void (No return value.)` **set\_shadow\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_shadow\_offset**()

Offset of the shadow effect, in pixels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **shadow\_size** = `1`
`🔗<class_LabelSettings_property_shadow_size>`

classref-property-setget

-   `void (No return value.)` **set\_shadow\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_shadow\_size**()

Size of the shadow effect.
