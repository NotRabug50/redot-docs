github\_url  
hide

# EditorSpinSlider

**Inherits:** `Range<class_Range>` **&lt;** `Control<class_Control>`
**&lt;** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

Godot editor's control for editing numeric values.

classref-introduction-group

## Description

This `Control<class_Control>` node is used in the editor's Inspector
dock to allow editing of numeric values. Can be used with
`EditorInspectorPlugin<class_EditorInspectorPlugin>` to recreate the
same behavior.

If the `Range.step<class_Range_property_step>` value is `1`, the
**EditorSpinSlider** will display up/down arrows, similar to
`SpinBox<class_SpinBox>`. If the `Range.step<class_Range_property_step>`
value is not `1`, a slider will be displayed instead.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**grabbed**() `🔗<class_EditorSpinSlider_signal_grabbed>`

Emitted when the spinner/slider is grabbed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**ungrabbed**() `🔗<class_EditorSpinSlider_signal_ungrabbed>`

Emitted when the spinner/slider is ungrabbed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**value\_focus\_entered**()
`🔗<class_EditorSpinSlider_signal_value_focus_entered>`

Emitted when the value form gains focus.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**value\_focus\_exited**()
`🔗<class_EditorSpinSlider_signal_value_focus_exited>`

Emitted when the value form loses focus.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **flat** = `false`
`🔗<class_EditorSpinSlider_property_flat>`

classref-property-setget

-   `void (No return value.)` **set\_flat**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_flat**()

If `true`, the slider will not draw background.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **hide\_slider** = `false`
`🔗<class_EditorSpinSlider_property_hide_slider>`

classref-property-setget

-   `void (No return value.)` **set\_hide\_slider**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_hiding\_slider**()

If `true`, the slider and up/down arrows are hidden.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **label** = `""`
`🔗<class_EditorSpinSlider_property_label>`

classref-property-setget

-   `void (No return value.)` **set\_label**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_label**()

The text that displays to the left of the value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **read\_only** = `false`
`🔗<class_EditorSpinSlider_property_read_only>`

classref-property-setget

-   `void (No return value.)` **set\_read\_only**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_read\_only**()

If `true`, the slider can't be interacted with.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **suffix** = `""`
`🔗<class_EditorSpinSlider_property_suffix>`

classref-property-setget

-   `void (No return value.)` **set\_suffix**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_suffix**()

The suffix to display after the value (in a faded color). This should
generally be a plural word. You may have to use an abbreviation if the
suffix is too long to be displayed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Texture2D<class_Texture2D>` **updown**
`🔗<class_EditorSpinSlider_theme_icon_updown>`

Single texture representing both the up and down buttons.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **updown\_disabled**
`🔗<class_EditorSpinSlider_theme_icon_updown_disabled>`

Single texture representing both the up and down buttons, when the
control is readonly or disabled.
