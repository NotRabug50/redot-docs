github\_url  
hide

# ColorPicker

**Inherits:** `VBoxContainer<class_VBoxContainer>` **&lt;**
`BoxContainer<class_BoxContainer>` **&lt;** `Container<class_Container>`
**&lt;** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A widget that provides an interface for selecting or modifying a color.

classref-introduction-group

## Description

A widget that provides an interface for selecting or modifying a color.
It can optionally provide functionalities like a color sampler
(eyedropper), color modes, and presets.

\*\*Note:\*\* This control is the color picker widget itself. You can
use a `ColorPickerButton<class_ColorPickerButton>` instead if you need a
button that brings up a **ColorPicker** in a popup.

classref-introduction-group

## Tutorials

-   [Tween Interpolation
    Demo](https://godotengine.org/asset-library/asset/2733)

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
<tr>
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**color\_changed**(color: `Color<class_Color>`)
`🔗<class_ColorPicker_signal_color_changed>`

Emitted when the color is changed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**preset\_added**(color: `Color<class_Color>`)
`🔗<class_ColorPicker_signal_preset_added>`

Emitted when a preset is added.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**preset\_removed**(color: `Color<class_Color>`)
`🔗<class_ColorPicker_signal_preset_removed>`

Emitted when a preset is removed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ColorModeType**: `🔗<enum_ColorPicker_ColorModeType>`

classref-enumeration-constant

`ColorModeType<enum_ColorPicker_ColorModeType>` **MODE\_RGB** = `0`

Allows editing the color with Red/Green/Blue sliders.

classref-enumeration-constant

`ColorModeType<enum_ColorPicker_ColorModeType>` **MODE\_HSV** = `1`

Allows editing the color with Hue/Saturation/Value sliders.

classref-enumeration-constant

`ColorModeType<enum_ColorPicker_ColorModeType>` **MODE\_RAW** = `2`

Allows the color R, G, B component values to go beyond 1.0, which can be
used for certain special operations that require it (like tinting
without darkening or rendering sprites in HDR).

classref-enumeration-constant

`ColorModeType<enum_ColorPicker_ColorModeType>` **MODE\_OKHSL** = `3`

Allows editing the color with Hue/Saturation/Lightness sliders.

OKHSL is a new color space similar to HSL but that better match
perception by leveraging the Oklab color space which is designed to be
simple to use, while doing a good job at predicting perceived lightness,
chroma and hue.

[Okhsv and Okhsl color
spaces](https://bottosson.github.io/posts/colorpicker/)

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PickerShapeType**: `🔗<enum_ColorPicker_PickerShapeType>`

classref-enumeration-constant

`PickerShapeType<enum_ColorPicker_PickerShapeType>`
**SHAPE\_HSV\_RECTANGLE** = `0`

HSV Color Model rectangle color space.

classref-enumeration-constant

`PickerShapeType<enum_ColorPicker_PickerShapeType>`
**SHAPE\_HSV\_WHEEL** = `1`

HSV Color Model rectangle color space with a wheel.

classref-enumeration-constant

`PickerShapeType<enum_ColorPicker_PickerShapeType>`
**SHAPE\_VHS\_CIRCLE** = `2`

HSV Color Model circle color space. Use Saturation as a radius.

classref-enumeration-constant

`PickerShapeType<enum_ColorPicker_PickerShapeType>`
**SHAPE\_OKHSL\_CIRCLE** = `3`

HSL OK Color Model circle color space.

classref-enumeration-constant

`PickerShapeType<enum_ColorPicker_PickerShapeType>` **SHAPE\_NONE** =
`4`

The color space shape and the shape select button are hidden. Can't be
selected from the shapes popup.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **can\_add\_swatches** = `true`
`🔗<class_ColorPicker_property_can_add_swatches>`

classref-property-setget

-   `void (No return value.)` **set\_can\_add\_swatches**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **are\_swatches\_enabled**()

If `true`, it's possible to add presets under Swatches. If `false`, the
button to add presets is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **color** = `Color(1, 1, 1, 1)`
`🔗<class_ColorPicker_property_color>`

classref-property-setget

-   `void (No return value.)` **set\_pick\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_pick\_color**()

The currently selected color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ColorModeType<enum_ColorPicker_ColorModeType>` **color\_mode** = `0`
`🔗<class_ColorPicker_property_color_mode>`

classref-property-setget

-   `void (No return value.)` **set\_color\_mode**(value:
    `ColorModeType<enum_ColorPicker_ColorModeType>`)
-   `ColorModeType<enum_ColorPicker_ColorModeType>`
    **get\_color\_mode**()

The currently selected color mode. See
`ColorModeType<enum_ColorPicker_ColorModeType>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **color\_modes\_visible** = `true`
`🔗<class_ColorPicker_property_color_modes_visible>`

classref-property-setget

-   `void (No return value.)` **set\_modes\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **are\_modes\_visible**()

If `true`, the color mode buttons are visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **deferred\_mode** = `false`
`🔗<class_ColorPicker_property_deferred_mode>`

classref-property-setget

-   `void (No return value.)` **set\_deferred\_mode**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_deferred\_mode**()

If `true`, the color will apply only after the user releases the mouse
button, otherwise it will apply immediately even in mouse motion event
(which can cause performance issues).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **edit\_alpha** = `true`
`🔗<class_ColorPicker_property_edit_alpha>`

classref-property-setget

-   `void (No return value.)` **set\_edit\_alpha**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_editing\_alpha**()

If `true`, shows an alpha channel slider (opacity).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **hex\_visible** = `true`
`🔗<class_ColorPicker_property_hex_visible>`

classref-property-setget

-   `void (No return value.)` **set\_hex\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_hex\_visible**()

If `true`, the hex color code input field is visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PickerShapeType<enum_ColorPicker_PickerShapeType>` **picker\_shape** =
`0` `🔗<class_ColorPicker_property_picker_shape>`

classref-property-setget

-   `void (No return value.)` **set\_picker\_shape**(value:
    `PickerShapeType<enum_ColorPicker_PickerShapeType>`)
-   `PickerShapeType<enum_ColorPicker_PickerShapeType>`
    **get\_picker\_shape**()

The shape of the color space view. See
`PickerShapeType<enum_ColorPicker_PickerShapeType>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **presets\_visible** = `true`
`🔗<class_ColorPicker_property_presets_visible>`

classref-property-setget

-   `void (No return value.)` **set\_presets\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **are\_presets\_visible**()

If `true`, the Swatches and Recent Colors presets are visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **sampler\_visible** = `true`
`🔗<class_ColorPicker_property_sampler_visible>`

classref-property-setget

-   `void (No return value.)` **set\_sampler\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_sampler\_visible**()

If `true`, the color sampler and color preview are visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **sliders\_visible** = `true`
`🔗<class_ColorPicker_property_sliders_visible>`

classref-property-setget

-   `void (No return value.)` **set\_sliders\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **are\_sliders\_visible**()

If `true`, the color sliders are visible.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_preset**(color: `Color<class_Color>`)
`🔗<class_ColorPicker_method_add_preset>`

Adds the given color to a list of color presets. The presets are
displayed in the color picker and the user will be able to select them.

\*\*Note:\*\* The presets list is only for *this* color picker.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_recent\_preset**(color:
`Color<class_Color>`) `🔗<class_ColorPicker_method_add_recent_preset>`

Adds the given color to a list of color recent presets so that it can be
picked later. Recent presets are the colors that were picked recently, a
new preset is automatically created and added to recent presets when you
pick a new color.

\*\*Note:\*\* The recent presets list is only for *this* color picker.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase\_preset**(color: `Color<class_Color>`)
`🔗<class_ColorPicker_method_erase_preset>`

Removes the given color from the list of color presets of this color
picker.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase\_recent\_preset**(color:
`Color<class_Color>`) `🔗<class_ColorPicker_method_erase_recent_preset>`

Removes the given color from the list of color recent presets of this
color picker.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedColorArray<class_PackedColorArray>` **get\_presets**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ColorPicker_method_get_presets>`

Returns the list of colors in the presets of the color picker.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedColorArray<class_PackedColorArray>` **get\_recent\_presets**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ColorPicker_method_get_recent_presets>`

Returns the list of colors in the recent presets of the color picker.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`int<class_int>` **center\_slider\_grabbers** = `1`
`🔗<class_ColorPicker_theme_constant_center_slider_grabbers>`

Overrides the
`Slider.center_grabber<class_Slider_theme_constant_center_grabber>`
theme property of the sliders.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **h\_width** = `30`
`🔗<class_ColorPicker_theme_constant_h_width>`

The width of the hue selection slider.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **label\_width** = `10`
`🔗<class_ColorPicker_theme_constant_label_width>`

The minimum width of the color labels next to sliders.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **margin** = `4`
`🔗<class_ColorPicker_theme_constant_margin>`

The margin around the **ColorPicker**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **sv\_height** = `256`
`🔗<class_ColorPicker_theme_constant_sv_height>`

The height of the saturation-value selection box.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **sv\_width** = `256`
`🔗<class_ColorPicker_theme_constant_sv_width>`

The width of the saturation-value selection box.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **add\_preset**
`🔗<class_ColorPicker_theme_icon_add_preset>`

The icon for the "Add Preset" button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **bar\_arrow**
`🔗<class_ColorPicker_theme_icon_bar_arrow>`

The texture for the arrow grabber.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **color\_hue**
`🔗<class_ColorPicker_theme_icon_color_hue>`

Custom texture for the hue selection slider on the right.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **color\_okhsl\_hue**
`🔗<class_ColorPicker_theme_icon_color_okhsl_hue>`

Custom texture for the H slider in the OKHSL color mode.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **expanded\_arrow**
`🔗<class_ColorPicker_theme_icon_expanded_arrow>`

The icon for color preset drop down menu when expanded.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **folded\_arrow**
`🔗<class_ColorPicker_theme_icon_folded_arrow>`

The icon for color preset drop down menu when folded.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **overbright\_indicator**
`🔗<class_ColorPicker_theme_icon_overbright_indicator>`

The indicator used to signalize that the color value is outside the 0-1
range.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **picker\_cursor**
`🔗<class_ColorPicker_theme_icon_picker_cursor>`

The image displayed over the color box/circle (depending on the
`picker_shape<class_ColorPicker_property_picker_shape>`), marking the
currently selected color.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **sample\_bg**
`🔗<class_ColorPicker_theme_icon_sample_bg>`

Background panel for the color preview box (visible when the color is
translucent).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **sample\_revert**
`🔗<class_ColorPicker_theme_icon_sample_revert>`

The icon for the revert button (visible on the middle of the "old" color
when it differs from the currently selected color). This icon is
modulated with a dark color if the "old" color is bright enough, so the
icon should be bright to ensure visibility in both scenarios.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **screen\_picker**
`🔗<class_ColorPicker_theme_icon_screen_picker>`

The icon for the screen color picker button.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **shape\_circle**
`🔗<class_ColorPicker_theme_icon_shape_circle>`

The icon for circular picker shapes.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **shape\_rect**
`🔗<class_ColorPicker_theme_icon_shape_rect>`

The icon for rectangular picker shapes.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **shape\_rect\_wheel**
`🔗<class_ColorPicker_theme_icon_shape_rect_wheel>`

The icon for rectangular wheel picker shapes.
