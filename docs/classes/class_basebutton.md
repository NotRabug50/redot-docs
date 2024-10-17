github\_url  
hide

# BaseButton

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `Button<class_Button>`,
`LinkButton<class_LinkButton>`, `TextureButton<class_TextureButton>`

Abstract base class for GUI buttons.

classref-introduction-group

## Description

**BaseButton** is an abstract base class for GUI buttons. It doesn't
display anything by itself.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**button\_down**() `🔗<class_BaseButton_signal_button_down>`

Emitted when the button starts being held down.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**button\_up**() `🔗<class_BaseButton_signal_button_up>`

Emitted when the button stops being held down.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**pressed**() `🔗<class_BaseButton_signal_pressed>`

Emitted when the button is toggled or pressed. This is on
`button_down<class_BaseButton_signal_button_down>` if
`action_mode<class_BaseButton_property_action_mode>` is
`ACTION_MODE_BUTTON_PRESS<class_BaseButton_constant_ACTION_MODE_BUTTON_PRESS>`
and on `button_up<class_BaseButton_signal_button_up>` otherwise.

If you need to know the button's pressed state (and
`toggle_mode<class_BaseButton_property_toggle_mode>` is active), use
`toggled<class_BaseButton_signal_toggled>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**toggled**(toggled\_on: `bool<class_bool>`)
`🔗<class_BaseButton_signal_toggled>`

Emitted when the button was just toggled between pressed and normal
states (only if `toggle_mode<class_BaseButton_property_toggle_mode>` is
active). The new state is contained in the `toggled_on` argument.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **DrawMode**: `🔗<enum_BaseButton_DrawMode>`

classref-enumeration-constant

`DrawMode<enum_BaseButton_DrawMode>` **DRAW\_NORMAL** = `0`

The normal state (i.e. not pressed, not hovered, not toggled and
enabled) of buttons.

classref-enumeration-constant

`DrawMode<enum_BaseButton_DrawMode>` **DRAW\_PRESSED** = `1`

The state of buttons are pressed.

classref-enumeration-constant

`DrawMode<enum_BaseButton_DrawMode>` **DRAW\_HOVER** = `2`

The state of buttons are hovered.

classref-enumeration-constant

`DrawMode<enum_BaseButton_DrawMode>` **DRAW\_DISABLED** = `3`

The state of buttons are disabled.

classref-enumeration-constant

`DrawMode<enum_BaseButton_DrawMode>` **DRAW\_HOVER\_PRESSED** = `4`

The state of buttons are both hovered and pressed.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ActionMode**: `🔗<enum_BaseButton_ActionMode>`

classref-enumeration-constant

`ActionMode<enum_BaseButton_ActionMode>` **ACTION\_MODE\_BUTTON\_PRESS**
= `0`

Require just a press to consider the button clicked.

classref-enumeration-constant

`ActionMode<enum_BaseButton_ActionMode>`
**ACTION\_MODE\_BUTTON\_RELEASE** = `1`

Require a press and a subsequent release before considering the button
clicked.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`ActionMode<enum_BaseButton_ActionMode>` **action\_mode** = `1`
`🔗<class_BaseButton_property_action_mode>`

classref-property-setget

-   `void (No return value.)` **set\_action\_mode**(value:
    `ActionMode<enum_BaseButton_ActionMode>`)
-   `ActionMode<enum_BaseButton_ActionMode>` **get\_action\_mode**()

Determines when the button is considered clicked, one of the
`ActionMode<enum_BaseButton_ActionMode>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ButtonGroup<class_ButtonGroup>` **button\_group**
`🔗<class_BaseButton_property_button_group>`

classref-property-setget

-   `void (No return value.)` **set\_button\_group**(value:
    `ButtonGroup<class_ButtonGroup>`)
-   `ButtonGroup<class_ButtonGroup>` **get\_button\_group**()

The `ButtonGroup<class_ButtonGroup>` associated with the button. Not to
be confused with node groups.

\*\*Note:\*\* The button will be configured as a radio button if a
`ButtonGroup<class_ButtonGroup>` is assigned to it.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`MouseButtonMask<enum_@GlobalScope_MouseButtonMask>`\]
**button\_mask** = `1` `🔗<class_BaseButton_property_button_mask>`

classref-property-setget

-   `void (No return value.)` **set\_button\_mask**(value:
    `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`MouseButtonMask<enum_@GlobalScope_MouseButtonMask>`\])
-   `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`MouseButtonMask<enum_@GlobalScope_MouseButtonMask>`\]
    **get\_button\_mask**()

Binary mask to choose which mouse buttons this button will respond to.

To allow both left-click and right-click, use
`MOUSE_BUTTON_MASK_LEFT | MOUSE_BUTTON_MASK_RIGHT`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **button\_pressed** = `false`
`🔗<class_BaseButton_property_button_pressed>`

classref-property-setget

-   `void (No return value.)` **set\_pressed**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_pressed**()

If `true`, the button's state is pressed. Means the button is pressed
down or toggled (if `toggle_mode<class_BaseButton_property_toggle_mode>`
is active). Only works if
`toggle_mode<class_BaseButton_property_toggle_mode>` is `true`.

\*\*Note:\*\* Changing the value of
`button_pressed<class_BaseButton_property_button_pressed>` will result
in `toggled<class_BaseButton_signal_toggled>` to be emitted. If you want
to change the pressed state without emitting that signal, use
`set_pressed_no_signal<class_BaseButton_method_set_pressed_no_signal>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **disabled** = `false`
`🔗<class_BaseButton_property_disabled>`

classref-property-setget

-   `void (No return value.)` **set\_disabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_disabled**()

If `true`, the button is in disabled state and can't be clicked or
toggled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **keep\_pressed\_outside** = `false`
`🔗<class_BaseButton_property_keep_pressed_outside>`

classref-property-setget

-   `void (No return value.)` **set\_keep\_pressed\_outside**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_keep\_pressed\_outside**()

If `true`, the button stays pressed when moving the cursor outside the
button while pressing it.

\*\*Note:\*\* This property only affects the button's visual appearance.
Signals will be emitted at the same moment regardless of this property's
value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Shortcut<class_Shortcut>` **shortcut**
`🔗<class_BaseButton_property_shortcut>`

classref-property-setget

-   `void (No return value.)` **set\_shortcut**(value:
    `Shortcut<class_Shortcut>`)
-   `Shortcut<class_Shortcut>` **get\_shortcut**()

`Shortcut<class_Shortcut>` associated to the button.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shortcut\_feedback** = `true`
`🔗<class_BaseButton_property_shortcut_feedback>`

classref-property-setget

-   `void (No return value.)` **set\_shortcut\_feedback**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_shortcut\_feedback**()

If `true`, the button will highlight for a short amount of time when its
shortcut is activated. If `false` and
`toggle_mode<class_BaseButton_property_toggle_mode>` is `false`, the
shortcut will activate without any visual feedback.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shortcut\_in\_tooltip** = `true`
`🔗<class_BaseButton_property_shortcut_in_tooltip>`

classref-property-setget

-   `void (No return value.)` **set\_shortcut\_in\_tooltip**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_shortcut\_in\_tooltip\_enabled**()

If `true`, the button will add information about its shortcut in the
tooltip.

\*\*Note:\*\* This property does nothing when the tooltip control is
customized using
`Control._make_custom_tooltip<class_Control_private_method__make_custom_tooltip>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **toggle\_mode** = `false`
`🔗<class_BaseButton_property_toggle_mode>`

classref-property-setget

-   `void (No return value.)` **set\_toggle\_mode**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_toggle\_mode**()

If `true`, the button is in toggle mode. Makes the button flip state
between pressed and unpressed each time its area is clicked.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_pressed**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_BaseButton_private_method__pressed>`

Called when the button is pressed. If you need to know the button's
pressed state (and `toggle_mode<class_BaseButton_property_toggle_mode>`
is active), use `_toggled<class_BaseButton_private_method__toggled>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_toggled**(toggled\_on: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_BaseButton_private_method__toggled>`

Called when the button is toggled (only if
`toggle_mode<class_BaseButton_property_toggle_mode>` is active).

classref-item-separator

------------------------------------------------------------------------

classref-method

`DrawMode<enum_BaseButton_DrawMode>` **get\_draw\_mode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_BaseButton_method_get_draw_mode>`

Returns the visual state used to draw the button. This is useful mainly
when implementing your own draw code by either overriding \_draw() or
connecting to "draw" signal. The visual state of the button is defined
by the `DrawMode<enum_BaseButton_DrawMode>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_hovered**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_BaseButton_method_is_hovered>`

Returns `true` if the mouse has entered the button and has not left it
yet.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_pressed\_no\_signal**(pressed:
`bool<class_bool>`) `🔗<class_BaseButton_method_set_pressed_no_signal>`

Changes the `button_pressed<class_BaseButton_property_button_pressed>`
state of the button, without emitting
`toggled<class_BaseButton_signal_toggled>`. Use when you just want to
change the state of the button without sending the pressed event (e.g.
when initializing scene). Only works if
`toggle_mode<class_BaseButton_property_toggle_mode>` is `true`.

\*\*Note:\*\* This method doesn't unpress other buttons in
`button_group<class_BaseButton_property_button_group>`.
