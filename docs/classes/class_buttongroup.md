github\_url  
hide

# ButtonGroup

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A group of buttons that doesn't allow more than one button to be pressed
at a time.

classref-introduction-group

## Description

A group of `BaseButton<class_BaseButton>`-derived buttons. The buttons
in a **ButtonGroup** are treated like radio buttons: No more than one
button can be pressed at a time. Some types of buttons (such as
`CheckBox<class_CheckBox>`) may have a special appearance in this state.

Every member of a **ButtonGroup** should have
`BaseButton.toggle_mode<class_BaseButton_property_toggle_mode>` set to
`true`.

classref-reftable-group

## Properties

<table>
<tbody>
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**pressed**(button: `BaseButton<class_BaseButton>`)
`🔗<class_ButtonGroup_signal_pressed>`

Emitted when one of the buttons of the group is pressed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **allow\_unpress** = `false`
`🔗<class_ButtonGroup_property_allow_unpress>`

classref-property-setget

-   `void (No return value.)` **set\_allow\_unpress**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_allow\_unpress**()

If `true`, it is possible to unpress all buttons in this
**ButtonGroup**.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Array<class_Array>`\[`BaseButton<class_BaseButton>`\]
**get\_buttons**() `🔗<class_ButtonGroup_method_get_buttons>`

Returns an `Array<class_Array>` of `Button<class_Button>`s who have this
as their **ButtonGroup** (see
`BaseButton.button_group<class_BaseButton_property_button_group>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`BaseButton<class_BaseButton>` **get\_pressed\_button**()
`🔗<class_ButtonGroup_method_get_pressed_button>`

Returns the current pressed button.
