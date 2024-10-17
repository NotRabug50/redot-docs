github\_url  
hide

# InputEventWithModifiers

**Inherits:** `InputEventFromWindow<class_InputEventFromWindow>`
**&lt;** `InputEvent<class_InputEvent>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:** `InputEventGesture<class_InputEventGesture>`,
`InputEventKey<class_InputEventKey>`,
`InputEventMouse<class_InputEventMouse>`

Abstract base class for input events affected by modifier keys like
`Shift` and `Alt`.

classref-introduction-group

## Description

Stores information about mouse, keyboard, and touch gesture input
events. This includes information about which modifier keys are pressed,
such as `Shift` or `Alt`. See
`Node._input<class_Node_private_method__input>`.

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

## Property Descriptions

classref-property

`bool<class_bool>` **alt\_pressed** = `false`
`🔗<class_InputEventWithModifiers_property_alt_pressed>`

classref-property-setget

-   `void (No return value.)` **set\_alt\_pressed**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_alt\_pressed**()

State of the `Alt` modifier.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **command\_or\_control\_autoremap** = `false`
`🔗<class_InputEventWithModifiers_property_command_or_control_autoremap>`

classref-property-setget

-   `void (No return value.)`
    **set\_command\_or\_control\_autoremap**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_command\_or\_control\_autoremap**()

Automatically use `Meta` (`Cmd`) on macOS and `Ctrl` on other platforms.
If `true`,
`ctrl_pressed<class_InputEventWithModifiers_property_ctrl_pressed>` and
`meta_pressed<class_InputEventWithModifiers_property_meta_pressed>`
cannot be set.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ctrl\_pressed** = `false`
`🔗<class_InputEventWithModifiers_property_ctrl_pressed>`

classref-property-setget

-   `void (No return value.)` **set\_ctrl\_pressed**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_ctrl\_pressed**()

State of the `Ctrl` modifier.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **meta\_pressed** = `false`
`🔗<class_InputEventWithModifiers_property_meta_pressed>`

classref-property-setget

-   `void (No return value.)` **set\_meta\_pressed**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_meta\_pressed**()

State of the `Meta` modifier. On Windows and Linux, this represents the
Windows key (sometimes called "meta" or "super" on Linux). On macOS,
this represents the Command key.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shift\_pressed** = `false`
`🔗<class_InputEventWithModifiers_property_shift_pressed>`

classref-property-setget

-   `void (No return value.)` **set\_shift\_pressed**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_shift\_pressed**()

State of the `Shift` modifier.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`KeyModifierMask<enum_@GlobalScope_KeyModifierMask>`\]
**get\_modifiers\_mask**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InputEventWithModifiers_method_get_modifiers_mask>`

Returns the keycode combination of modifier keys.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_command\_or\_control\_pressed**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InputEventWithModifiers_method_is_command_or_control_pressed>`

On macOS, returns `true` if `Meta` (`Cmd`) is pressed.

On other platforms, returns `true` if `Ctrl` is pressed.
