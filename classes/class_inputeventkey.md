github\_url  
hide

# InputEventKey

**Inherits:** `InputEventWithModifiers<class_InputEventWithModifiers>`
**&lt;** `InputEventFromWindow<class_InputEventFromWindow>` **&lt;**
`InputEvent<class_InputEvent>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Represents a key on a keyboard being pressed or released.

classref-introduction-group

## Description

An input event for keys on a keyboard. Supports key presses, key
releases and `echo<class_InputEventKey_property_echo>` events. It can
also be received in
`Node._unhandled_key_input<class_Node_private_method__unhandled_key_input>`.

\*\*Note:\*\* Events received from the keyboard usually have all
properties set. Event mappings should have only one of the
`keycode<class_InputEventKey_property_keycode>`,
`physical_keycode<class_InputEventKey_property_physical_keycode>` or
`unicode<class_InputEventKey_property_unicode>` set.

When events are compared, properties are checked in the following
priority - `keycode<class_InputEventKey_property_keycode>`,
`physical_keycode<class_InputEventKey_property_physical_keycode>` and
`unicode<class_InputEventKey_property_unicode>`. Events with the first
matching value will be considered equal.

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **echo** = `false`
`🔗<class_InputEventKey_property_echo>`

classref-property-setget

-   `void (No return value.)` **set\_echo**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_echo**()

If `true`, the key was already pressed before this event. An echo event
is a repeated key event sent when the user is holding down the key.

\*\*Note:\*\* The rate at which echo events are sent is typically around
20 events per second (after holding down the key for roughly half a
second). However, the key repeat delay/speed can be changed by the user
or disabled entirely in the operating system settings. To ensure your
project works correctly on all configurations, do not assume the user
has a specific key repeat configuration in your project's behavior.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Key<enum_@GlobalScope_Key>` **key\_label** = `0`
`🔗<class_InputEventKey_property_key_label>`

classref-property-setget

-   `void (No return value.)` **set\_key\_label**(value:
    `Key<enum_@GlobalScope_Key>`)
-   `Key<enum_@GlobalScope_Key>` **get\_key\_label**()

Represents the localized label printed on the key in the current
keyboard layout, which corresponds to one of the
`Key<enum_@GlobalScope_Key>` constants or any valid Unicode character.

For keyboard layouts with a single label on the key, it is equivalent to
`keycode<class_InputEventKey_property_keycode>`.

To get a human-readable representation of the **InputEventKey**, use
`OS.get_keycode_string(event.key_label)` where `event` is the
**InputEventKey**.

    +-----+ +-----+
    | Q   | | Q   | - "Q" - keycode
    |   Й | |  ض | - "Й" and "ض" - key_label
    +-----+ +-----+

classref-item-separator

------------------------------------------------------------------------

classref-property

`Key<enum_@GlobalScope_Key>` **keycode** = `0`
`🔗<class_InputEventKey_property_keycode>`

classref-property-setget

-   `void (No return value.)` **set\_keycode**(value:
    `Key<enum_@GlobalScope_Key>`)
-   `Key<enum_@GlobalScope_Key>` **get\_keycode**()

Latin label printed on the key in the current keyboard layout, which
corresponds to one of the `Key<enum_@GlobalScope_Key>` constants.

To get a human-readable representation of the **InputEventKey**, use
`OS.get_keycode_string(event.keycode)` where `event` is the
**InputEventKey**.

    +-----+ +-----+
    | Q   | | Q   | - "Q" - keycode
    |   Й | |  ض | - "Й" and "ض" - key_label
    +-----+ +-----+

classref-item-separator

------------------------------------------------------------------------

classref-property

`KeyLocation<enum_@GlobalScope_KeyLocation>` **location** = `0`
`🔗<class_InputEventKey_property_location>`

classref-property-setget

-   `void (No return value.)` **set\_location**(value:
    `KeyLocation<enum_@GlobalScope_KeyLocation>`)
-   `KeyLocation<enum_@GlobalScope_KeyLocation>` **get\_location**()

Represents the location of a key which has both left and right versions,
such as `Shift` or `Alt`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Key<enum_@GlobalScope_Key>` **physical\_keycode** = `0`
`🔗<class_InputEventKey_property_physical_keycode>`

classref-property-setget

-   `void (No return value.)` **set\_physical\_keycode**(value:
    `Key<enum_@GlobalScope_Key>`)
-   `Key<enum_@GlobalScope_Key>` **get\_physical\_keycode**()

Represents the physical location of a key on the 101/102-key US QWERTY
keyboard, which corresponds to one of the `Key<enum_@GlobalScope_Key>`
constants.

To get a human-readable representation of the **InputEventKey**, use
`OS.get_keycode_string<class_OS_method_get_keycode_string>` in
combination with
`DisplayServer.keyboard_get_keycode_from_physical<class_DisplayServer_method_keyboard_get_keycode_from_physical>`:

gdscript

func \_input(event):  
if event is InputEventKey:  
var keycode =
DisplayServer.keyboard\_get\_keycode\_from\_physical(event.physical\_keycode)
print(OS.get\_keycode\_string(keycode))

csharp

public override void \_Input(InputEvent @event) { if (@event is
InputEventKey inputEventKey) { var keycode =
DisplayServer.KeyboardGetKeycodeFromPhysical(inputEventKey.PhysicalKeycode);
GD.Print(OS.GetKeycodeString(keycode)); } }

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **pressed** = `false`
`🔗<class_InputEventKey_property_pressed>`

classref-property-setget

-   `void (No return value.)` **set\_pressed**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_pressed**()

If `true`, the key's state is pressed. If `false`, the key's state is
released.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **unicode** = `0`
`🔗<class_InputEventKey_property_unicode>`

classref-property-setget

-   `void (No return value.)` **set\_unicode**(value: `int<class_int>`)
-   `int<class_int>` **get\_unicode**()

The key Unicode character code (when relevant), shifted by modifier
keys. Unicode character codes for composite characters and complex
scripts may not be available unless IME input mode is active. See
`Window.set_ime_active<class_Window_method_set_ime_active>` for more
information.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`String<class_String>` **as\_text\_key\_label**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InputEventKey_method_as_text_key_label>`

Returns a `String<class_String>` representation of the event's
`key_label<class_InputEventKey_property_key_label>` and modifiers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **as\_text\_keycode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InputEventKey_method_as_text_keycode>`

Returns a `String<class_String>` representation of the event's
`keycode<class_InputEventKey_property_keycode>` and modifiers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **as\_text\_location**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InputEventKey_method_as_text_location>`

Returns a `String<class_String>` representation of the event's
`location<class_InputEventKey_property_location>`. This will be a blank
string if the event is not specific to a location.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **as\_text\_physical\_keycode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InputEventKey_method_as_text_physical_keycode>`

Returns a `String<class_String>` representation of the event's
`physical_keycode<class_InputEventKey_property_physical_keycode>` and
modifiers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Key<enum_@GlobalScope_Key>` **get\_key\_label\_with\_modifiers**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InputEventKey_method_get_key_label_with_modifiers>`

Returns the localized key label combined with modifier keys such as
`Shift` or `Alt`. See also
`InputEventWithModifiers<class_InputEventWithModifiers>`.

To get a human-readable representation of the **InputEventKey** with
modifiers, use
`OS.get_keycode_string(event.get_key_label_with_modifiers())` where
`event` is the **InputEventKey**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Key<enum_@GlobalScope_Key>` **get\_keycode\_with\_modifiers**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InputEventKey_method_get_keycode_with_modifiers>`

Returns the Latin keycode combined with modifier keys such as `Shift` or
`Alt`. See also
`InputEventWithModifiers<class_InputEventWithModifiers>`.

To get a human-readable representation of the **InputEventKey** with
modifiers, use
`OS.get_keycode_string(event.get_keycode_with_modifiers())` where
`event` is the **InputEventKey**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Key<enum_@GlobalScope_Key>`
**get\_physical\_keycode\_with\_modifiers**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InputEventKey_method_get_physical_keycode_with_modifiers>`

Returns the physical keycode combined with modifier keys such as `Shift`
or `Alt`. See also
`InputEventWithModifiers<class_InputEventWithModifiers>`.

To get a human-readable representation of the **InputEventKey** with
modifiers, use
`OS.get_keycode_string(event.get_physical_keycode_with_modifiers())`
where `event` is the **InputEventKey**.
