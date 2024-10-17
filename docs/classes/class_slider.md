github\_url  
hide

# Slider

**Inherits:** `Range<class_Range>` **&lt;** `Control<class_Control>`
**&lt;** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

**Inherited By:** `HSlider<class_HSlider>`, `VSlider<class_VSlider>`

Abstract base class for sliders.

classref-introduction-group

## Description

Abstract base class for sliders, used to adjust a value by moving a
grabber along a horizontal or vertical axis. Sliders are
`Range<class_Range>`-based controls.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**drag\_ended**(value\_changed: `bool<class_bool>`)
`🔗<class_Slider_signal_drag_ended>`

Emitted when dragging stops. If `value_changed` is true,
`Range.value<class_Range_property_value>` is different from the value
when you started the dragging.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**drag\_started**() `🔗<class_Slider_signal_drag_started>`

Emitted when dragging is started. This is emitted before the
corresponding `Range.value_changed<class_Range_signal_value_changed>`
signal.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **editable** = `true`
`🔗<class_Slider_property_editable>`

classref-property-setget

-   `void (No return value.)` **set\_editable**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_editable**()

If `true`, the slider can be interacted with. If `false`, the value can
be changed only by code.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **scrollable** = `true`
`🔗<class_Slider_property_scrollable>`

classref-property-setget

-   `void (No return value.)` **set\_scrollable**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_scrollable**()

If `true`, the value can be changed using the mouse wheel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **tick\_count** = `0`
`🔗<class_Slider_property_tick_count>`

classref-property-setget

-   `void (No return value.)` **set\_ticks**(value: `int<class_int>`)
-   `int<class_int>` **get\_ticks**()

Number of ticks displayed on the slider, including border ticks. Ticks
are uniformly-distributed value markers.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ticks\_on\_borders** = `false`
`🔗<class_Slider_property_ticks_on_borders>`

classref-property-setget

-   `void (No return value.)` **set\_ticks\_on\_borders**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_ticks\_on\_borders**()

If `true`, the slider will display ticks for minimum and maximum values.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`int<class_int>` **center\_grabber** = `0`
`🔗<class_Slider_theme_constant_center_grabber>`

Boolean constant. If `1`, the grabber texture size will be ignored and
it will fit within slider's bounds based only on its center position.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **grabber\_offset** = `0`
`🔗<class_Slider_theme_constant_grabber_offset>`

Vertical or horizontal offset of the grabber.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **grabber**
`🔗<class_Slider_theme_icon_grabber>`

The texture for the grabber (the draggable element).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **grabber\_disabled**
`🔗<class_Slider_theme_icon_grabber_disabled>`

The texture for the grabber when it's disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **grabber\_highlight**
`🔗<class_Slider_theme_icon_grabber_highlight>`

The texture for the grabber when it's focused.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **tick** `🔗<class_Slider_theme_icon_tick>`

The texture for the ticks, visible when
`tick_count<class_Slider_property_tick_count>` is greater than 0.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **grabber\_area**
`🔗<class_Slider_theme_style_grabber_area>`

The background of the area to the left or bottom of the grabber.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **grabber\_area\_highlight**
`🔗<class_Slider_theme_style_grabber_area_highlight>`

The background of the area to the left or bottom of the grabber that
displays when it's being hovered or focused.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **slider**
`🔗<class_Slider_theme_style_slider>`

The background for the whole slider. Affects the height or width of the
`grabber_area<class_Slider_theme_style_grabber_area>`.
