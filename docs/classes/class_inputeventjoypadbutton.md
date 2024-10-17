github\_url  
hide

# InputEventJoypadButton

**Inherits:** `InputEvent<class_InputEvent>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Represents a gamepad button being pressed or released.

classref-introduction-group

## Description

Input event type for gamepad buttons. For gamepad analog sticks and
joysticks, see `InputEventJoypadMotion<class_InputEventJoypadMotion>`.

classref-introduction-group

## Tutorials

-   `Using InputEvent <../tutorials/inputs/inputevent>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`JoyButton<enum_@GlobalScope_JoyButton>` **button\_index** = `0`
`🔗<class_InputEventJoypadButton_property_button_index>`

classref-property-setget

-   `void (No return value.)` **set\_button\_index**(value:
    `JoyButton<enum_@GlobalScope_JoyButton>`)
-   `JoyButton<enum_@GlobalScope_JoyButton>` **get\_button\_index**()

Button identifier. One of the `JoyButton<enum_@GlobalScope_JoyButton>`
button constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **pressed** = `false`
`🔗<class_InputEventJoypadButton_property_pressed>`

classref-property-setget

-   `void (No return value.)` **set\_pressed**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_pressed**()

If `true`, the button's state is pressed. If `false`, the button's state
is released.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pressure** = `0.0`
`🔗<class_InputEventJoypadButton_property_pressure>`

classref-property-setget

-   `void (No return value.)` **set\_pressure**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pressure**()

**Deprecated:** This property is never set by the engine and is always
`0`.
