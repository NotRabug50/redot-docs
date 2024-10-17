github\_url  
hide

# Input

**Inherits:** `Object<class_Object>`

A singleton for handling inputs.

classref-introduction-group

## Description

The **Input** singleton handles key presses, mouse buttons and movement,
gamepads, and input actions. Actions and their events can be set in the
**Input Map** tab in **Project &gt; Project Settings**, or with the
`InputMap<class_InputMap>` class.

\*\*Note:\*\* **Input**'s methods reflect the global input state and are
not affected by
`Control.accept_event<class_Control_method_accept_event>` or
`Viewport.set_input_as_handled<class_Viewport_method_set_input_as_handled>`,
as those methods only deal with the way input is propagated in the
`SceneTree<class_SceneTree>`.

classref-introduction-group

## Tutorials

-   `Inputs documentation index <../tutorials/inputs/index>`
-   [2D Dodge The Creeps
    Demo](https://godotengine.org/asset-library/asset/2712)
-   [3D Voxel Demo](https://godotengine.org/asset-library/asset/2755)

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

**joy\_connection\_changed**(device: `int<class_int>`, connected:
`bool<class_bool>`) `🔗<class_Input_signal_joy_connection_changed>`

Emitted when a joypad device has been connected or disconnected.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **MouseMode**: `🔗<enum_Input_MouseMode>`

classref-enumeration-constant

`MouseMode<enum_Input_MouseMode>` **MOUSE\_MODE\_VISIBLE** = `0`

Makes the mouse cursor visible if it is hidden.

classref-enumeration-constant

`MouseMode<enum_Input_MouseMode>` **MOUSE\_MODE\_HIDDEN** = `1`

Makes the mouse cursor hidden if it is visible.

classref-enumeration-constant

`MouseMode<enum_Input_MouseMode>` **MOUSE\_MODE\_CAPTURED** = `2`

Captures the mouse. The mouse will be hidden and its position locked at
the center of the window manager's window.

\*\*Note:\*\* If you want to process the mouse's movement in this mode,
you need to use
`InputEventMouseMotion.relative<class_InputEventMouseMotion_property_relative>`.

classref-enumeration-constant

`MouseMode<enum_Input_MouseMode>` **MOUSE\_MODE\_CONFINED** = `3`

Confines the mouse cursor to the game window, and make it visible.

classref-enumeration-constant

`MouseMode<enum_Input_MouseMode>` **MOUSE\_MODE\_CONFINED\_HIDDEN** =
`4`

Confines the mouse cursor to the game window, and make it hidden.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CursorShape**: `🔗<enum_Input_CursorShape>`

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_ARROW** = `0`

Arrow cursor. Standard, default pointing cursor.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_IBEAM** = `1`

I-beam cursor. Usually used to show where the text cursor will appear
when the mouse is clicked.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_POINTING\_HAND** = `2`

Pointing hand cursor. Usually used to indicate the pointer is over a
link or other interactable item.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_CROSS** = `3`

Cross cursor. Typically appears over regions in which a drawing
operation can be performed or for selections.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_WAIT** = `4`

Wait cursor. Indicates that the application is busy performing an
operation, and that it cannot be used during the operation (e.g.
something is blocking its main thread).

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_BUSY** = `5`

Busy cursor. Indicates that the application is busy performing an
operation, and that it is still usable during the operation.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_DRAG** = `6`

Drag cursor. Usually displayed when dragging something.

\*\*Note:\*\* Windows lacks a dragging cursor, so
`CURSOR_DRAG<class_Input_constant_CURSOR_DRAG>` is the same as
`CURSOR_MOVE<class_Input_constant_CURSOR_MOVE>` for this platform.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_CAN\_DROP** = `7`

Can drop cursor. Usually displayed when dragging something to indicate
that it can be dropped at the current position.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_FORBIDDEN** = `8`

Forbidden cursor. Indicates that the current action is forbidden (for
example, when dragging something) or that the control at a position is
disabled.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_VSIZE** = `9`

Vertical resize mouse cursor. A double-headed vertical arrow. It tells
the user they can resize the window or the panel vertically.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_HSIZE** = `10`

Horizontal resize mouse cursor. A double-headed horizontal arrow. It
tells the user they can resize the window or the panel horizontally.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_BDIAGSIZE** = `11`

Window resize mouse cursor. The cursor is a double-headed arrow that
goes from the bottom left to the top right. It tells the user they can
resize the window or the panel both horizontally and vertically.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_FDIAGSIZE** = `12`

Window resize mouse cursor. The cursor is a double-headed arrow that
goes from the top left to the bottom right, the opposite of
`CURSOR_BDIAGSIZE<class_Input_constant_CURSOR_BDIAGSIZE>`. It tells the
user they can resize the window or the panel both horizontally and
vertically.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_MOVE** = `13`

Move cursor. Indicates that something can be moved.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_VSPLIT** = `14`

Vertical split mouse cursor. On Windows, it's the same as
`CURSOR_VSIZE<class_Input_constant_CURSOR_VSIZE>`.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_HSPLIT** = `15`

Horizontal split mouse cursor. On Windows, it's the same as
`CURSOR_HSIZE<class_Input_constant_CURSOR_HSIZE>`.

classref-enumeration-constant

`CursorShape<enum_Input_CursorShape>` **CURSOR\_HELP** = `16`

Help cursor. Usually a question mark.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **emulate\_mouse\_from\_touch**
`🔗<class_Input_property_emulate_mouse_from_touch>`

classref-property-setget

-   `void (No return value.)`
    **set\_emulate\_mouse\_from\_touch**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_emulating\_mouse\_from\_touch**()

If `true`, sends mouse input events when tapping or swiping on the
touchscreen. See also
`ProjectSettings.input_devices/pointing/emulate_mouse_from_touch<class_ProjectSettings_property_input_devices/pointing/emulate_mouse_from_touch>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **emulate\_touch\_from\_mouse**
`🔗<class_Input_property_emulate_touch_from_mouse>`

classref-property-setget

-   `void (No return value.)`
    **set\_emulate\_touch\_from\_mouse**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_emulating\_touch\_from\_mouse**()

If `true`, sends touch input events when clicking or dragging the mouse.
See also
`ProjectSettings.input_devices/pointing/emulate_touch_from_mouse<class_ProjectSettings_property_input_devices/pointing/emulate_touch_from_mouse>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`MouseMode<enum_Input_MouseMode>` **mouse\_mode**
`🔗<class_Input_property_mouse_mode>`

classref-property-setget

-   `void (No return value.)` **set\_mouse\_mode**(value:
    `MouseMode<enum_Input_MouseMode>`)
-   `MouseMode<enum_Input_MouseMode>` **get\_mouse\_mode**()

Controls the mouse mode. See `MouseMode<enum_Input_MouseMode>` for more
information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_accumulated\_input**
`🔗<class_Input_property_use_accumulated_input>`

classref-property-setget

-   `void (No return value.)` **set\_use\_accumulated\_input**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_accumulated\_input**()

If `true`, similar input events sent by the operating system are
accumulated. When input accumulation is enabled, all input events
generated during a frame will be merged and emitted when the frame is
done rendering. Therefore, this limits the number of input method calls
per second to the rendering FPS.

Input accumulation can be disabled to get slightly more precise/reactive
input at the cost of increased CPU usage. In applications where drawing
freehand lines is required, input accumulation should generally be
disabled while the user is drawing the line to get results that closely
follow the actual input.

\*\*Note:\*\* Input accumulation is *enabled* by default.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **action\_press**(action:
`StringName<class_StringName>`, strength: `float<class_float>` = 1.0)
`🔗<class_Input_method_action_press>`

This will simulate pressing the specified action.

The strength can be used for non-boolean actions, it's ranged between 0
and 1 representing the intensity of the given action.

\*\*Note:\*\* This method will not cause any
`Node._input<class_Node_private_method__input>` calls. It is intended to
be used with `is_action_pressed<class_Input_method_is_action_pressed>`
and `is_action_just_pressed<class_Input_method_is_action_just_pressed>`.
If you want to simulate `_input`, use
`parse_input_event<class_Input_method_parse_input_event>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **action\_release**(action:
`StringName<class_StringName>`) `🔗<class_Input_method_action_release>`

If the specified action is already pressed, this will release it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_joy\_mapping**(mapping:
`String<class_String>`, update\_existing: `bool<class_bool>` = false)
`🔗<class_Input_method_add_joy_mapping>`

Adds a new mapping entry (in SDL2 format) to the mapping database.
Optionally update already connected devices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **flush\_buffered\_events**()
`🔗<class_Input_method_flush_buffered_events>`

Sends all input events which are in the current buffer to the game loop.
These events may have been buffered as a result of accumulated input
(`use_accumulated_input<class_Input_property_use_accumulated_input>`) or
agile input flushing
(`ProjectSettings.input_devices/buffering/agile_event_flushing<class_ProjectSettings_property_input_devices/buffering/agile_event_flushing>`).

The engine will already do this itself at key execution points (at least
once per frame). However, this can be useful in advanced cases where you
want precise control over the timing of event handling.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_accelerometer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_accelerometer>`

Returns the acceleration in m/s² of the device's accelerometer sensor,
if the device has one. Otherwise, the method returns
`Vector3.ZERO<class_Vector3_constant_ZERO>`.

Note this method returns an empty `Vector3<class_Vector3>` when running
from the editor even when your device has an accelerometer. You must
export your project to a supported device to read values from the
accelerometer.

\*\*Note:\*\* This method only works on Android and iOS. On other
platforms, it always returns
`Vector3.ZERO<class_Vector3_constant_ZERO>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_action\_raw\_strength**(action:
`StringName<class_StringName>`, exact\_match: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_action_raw_strength>`

Returns a value between 0 and 1 representing the raw intensity of the
given action, ignoring the action's deadzone. In most cases, you should
use `get_action_strength<class_Input_method_get_action_strength>`
instead.

If `exact_match` is `false`, it ignores additional input modifiers for
`InputEventKey<class_InputEventKey>` and
`InputEventMouseButton<class_InputEventMouseButton>` events, and the
direction for `InputEventJoypadMotion<class_InputEventJoypadMotion>`
events.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_action\_strength**(action:
`StringName<class_StringName>`, exact\_match: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_action_strength>`

Returns a value between 0 and 1 representing the intensity of the given
action. In a joypad, for example, the further away the axis (analog
sticks or L2, R2 triggers) is from the dead zone, the closer the value
will be to 1. If the action is mapped to a control that has no axis such
as the keyboard, the value returned will be 0 or 1.

If `exact_match` is `false`, it ignores additional input modifiers for
`InputEventKey<class_InputEventKey>` and
`InputEventMouseButton<class_InputEventMouseButton>` events, and the
direction for `InputEventJoypadMotion<class_InputEventJoypadMotion>`
events.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_axis**(negative\_action:
`StringName<class_StringName>`, positive\_action:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_axis>`

Get axis input by specifying two actions, one negative and one positive.

This is a shorthand for writing
`Input.get_action_strength("positive_action") - Input.get_action_strength("negative_action")`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`int<class_int>`\] **get\_connected\_joypads**()
`🔗<class_Input_method_get_connected_joypads>`

Returns an `Array<class_Array>` containing the device IDs of all
currently connected joypads.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CursorShape<enum_Input_CursorShape>` **get\_current\_cursor\_shape**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_current_cursor_shape>`

Returns the currently assigned cursor shape (see
`CursorShape<enum_Input_CursorShape>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_gravity**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_gravity>`

Returns the gravity in m/s² of the device's accelerometer sensor, if the
device has one. Otherwise, the method returns
`Vector3.ZERO<class_Vector3_constant_ZERO>`.

\*\*Note:\*\* This method only works on Android and iOS. On other
platforms, it always returns
`Vector3.ZERO<class_Vector3_constant_ZERO>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_gyroscope**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_gyroscope>`

Returns the rotation rate in rad/s around a device's X, Y, and Z axes of
the gyroscope sensor, if the device has one. Otherwise, the method
returns `Vector3.ZERO<class_Vector3_constant_ZERO>`.

\*\*Note:\*\* This method only works on Android and iOS. On other
platforms, it always returns
`Vector3.ZERO<class_Vector3_constant_ZERO>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_joy\_axis**(device: `int<class_int>`, axis:
`JoyAxis<enum_@GlobalScope_JoyAxis>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_joy_axis>`

Returns the current value of the joypad axis at given index (see
`JoyAxis<enum_@GlobalScope_JoyAxis>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_joy\_guid**(device: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_joy_guid>`

Returns an SDL2-compatible device GUID on platforms that use gamepad
remapping, e.g. `030000004c050000c405000000010000`. Returns
`"Default Gamepad"` otherwise. Godot uses the [SDL2 game controller
database](https://github.com/gabomdq/SDL_GameControllerDB) to determine
gamepad names and mappings based on this GUID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_joy\_info**(device:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_joy_info>`

Returns a dictionary with extra platform-specific information about the
device, e.g. the raw gamepad name from the OS or the Steam Input index.

On Windows the dictionary contains the following fields:

`xinput_index`: The index of the controller in the XInput system.

On Linux:

`raw_name`: The name of the controller as it came from the OS, before
getting renamed by the godot controller database.

`vendor_id`: The USB vendor ID of the device.

`product_id`: The USB product ID of the device.

`steam_input_index`: The Steam Input gamepad index, if the device is not
a Steam Input device this key won't be present.

\*\*Note:\*\* The returned dictionary is always empty on Web, iOS,
Android, and macOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_joy\_name**(device: `int<class_int>`)
`🔗<class_Input_method_get_joy_name>`

Returns the name of the joypad at the specified device index, e.g.
`PS4 Controller`. Godot uses the [SDL2 game controller
database](https://github.com/gabomdq/SDL_GameControllerDB) to determine
gamepad names.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_joy\_vibration\_duration**(device:
`int<class_int>`) `🔗<class_Input_method_get_joy_vibration_duration>`

Returns the duration of the current vibration effect in seconds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_joy\_vibration\_strength**(device:
`int<class_int>`) `🔗<class_Input_method_get_joy_vibration_strength>`

Returns the strength of the joypad vibration: x is the strength of the
weak motor, and y is the strength of the strong motor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_last\_mouse\_screen\_velocity**()
`🔗<class_Input_method_get_last_mouse_screen_velocity>`

Returns the last mouse velocity in screen coordinates. To provide a
precise and jitter-free velocity, mouse velocity is only calculated
every 0.1s. Therefore, mouse velocity will lag mouse movements.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_last\_mouse\_velocity**()
`🔗<class_Input_method_get_last_mouse_velocity>`

Returns the last mouse velocity. To provide a precise and jitter-free
velocity, mouse velocity is only calculated every 0.1s. Therefore, mouse
velocity will lag mouse movements.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_magnetometer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_magnetometer>`

Returns the magnetic field strength in micro-Tesla for all axes of the
device's magnetometer sensor, if the device has one. Otherwise, the
method returns `Vector3.ZERO<class_Vector3_constant_ZERO>`.

\*\*Note:\*\* This method only works on Android and iOS. On other
platforms, it always returns
`Vector3.ZERO<class_Vector3_constant_ZERO>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`MouseButtonMask<enum_@GlobalScope_MouseButtonMask>`\]
**get\_mouse\_button\_mask**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_mouse_button_mask>`

Returns mouse buttons as a bitmask. If multiple mouse buttons are
pressed at the same time, the bits are added together. Equivalent to
`DisplayServer.mouse_get_button_state<class_DisplayServer_method_mouse_get_button_state>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_vector**(negative\_x:
`StringName<class_StringName>`, positive\_x:
`StringName<class_StringName>`, negative\_y:
`StringName<class_StringName>`, positive\_y:
`StringName<class_StringName>`, deadzone: `float<class_float>` = -1.0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_get_vector>`

Gets an input vector by specifying four actions for the positive and
negative X and Y axes.

This method is useful when getting vector input, such as from a
joystick, directional pad, arrows, or WASD. The vector has its length
limited to 1 and has a circular deadzone, which is useful for using
vector input as movement.

By default, the deadzone is automatically calculated from the average of
the action deadzones. However, you can override the deadzone to be
whatever you want (on the range of 0 to 1).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_action\_just\_pressed**(action:
`StringName<class_StringName>`, exact\_match: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_is_action_just_pressed>`

Returns `true` when the user has *started* pressing the action event in
the current frame or physics tick. It will only return `true` on the
frame or tick that the user pressed down the button.

This is useful for code that needs to run only once when an action is
pressed, instead of every frame while it's pressed.

If `exact_match` is `false`, it ignores additional input modifiers for
`InputEventKey<class_InputEventKey>` and
`InputEventMouseButton<class_InputEventMouseButton>` events, and the
direction for `InputEventJoypadMotion<class_InputEventJoypadMotion>`
events.

\*\*Note:\*\* Returning `true` does not imply that the action is *still*
pressed. An action can be pressed and released again rapidly, and `true`
will still be returned so as not to miss input.

\*\*Note:\*\* Due to keyboard ghosting,
`is_action_just_pressed<class_Input_method_is_action_just_pressed>` may
return `false` even if one of the action's keys is pressed. See [Input
examples](../tutorials/inputs/input_examples.html#keyboard-events) in
the documentation for more information.

\*\*Note:\*\* During input handling (e.g.
`Node._input<class_Node_private_method__input>`), use
`InputEvent.is_action_pressed<class_InputEvent_method_is_action_pressed>`
instead to query the action state of the current event.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_action\_just\_released**(action:
`StringName<class_StringName>`, exact\_match: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_is_action_just_released>`

Returns `true` when the user *stops* pressing the action event in the
current frame or physics tick. It will only return `true` on the frame
or tick that the user releases the button.

\*\*Note:\*\* Returning `true` does not imply that the action is *still*
not pressed. An action can be released and pressed again rapidly, and
`true` will still be returned so as not to miss input.

If `exact_match` is `false`, it ignores additional input modifiers for
`InputEventKey<class_InputEventKey>` and
`InputEventMouseButton<class_InputEventMouseButton>` events, and the
direction for `InputEventJoypadMotion<class_InputEventJoypadMotion>`
events.

\*\*Note:\*\* During input handling (e.g.
`Node._input<class_Node_private_method__input>`), use
`InputEvent.is_action_released<class_InputEvent_method_is_action_released>`
instead to query the action state of the current event.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_action\_pressed**(action:
`StringName<class_StringName>`, exact\_match: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_is_action_pressed>`

Returns `true` if you are pressing the action event.

If `exact_match` is `false`, it ignores additional input modifiers for
`InputEventKey<class_InputEventKey>` and
`InputEventMouseButton<class_InputEventMouseButton>` events, and the
direction for `InputEventJoypadMotion<class_InputEventJoypadMotion>`
events.

\*\*Note:\*\* Due to keyboard ghosting,
`is_action_pressed<class_Input_method_is_action_pressed>` may return
`false` even if one of the action's keys is pressed. See [Input
examples](../tutorials/inputs/input_examples.html#keyboard-events) in
the documentation for more information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_anything\_pressed**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_is_anything_pressed>`

Returns `true` if any action, key, joypad button, or mouse button is
being pressed. This will also return `true` if any action is simulated
via code by calling `action_press<class_Input_method_action_press>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_joy\_button\_pressed**(device:
`int<class_int>`, button: `JoyButton<enum_@GlobalScope_JoyButton>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_is_joy_button_pressed>`

Returns `true` if you are pressing the joypad button (see
`JoyButton<enum_@GlobalScope_JoyButton>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_joy\_known**(device: `int<class_int>`)
`🔗<class_Input_method_is_joy_known>`

Returns `true` if the system knows the specified device. This means that
it sets all button and axis indices. Unknown joypads are not expected to
match these constants, but you can still retrieve events from them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_key\_label\_pressed**(keycode:
`Key<enum_@GlobalScope_Key>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_is_key_label_pressed>`

Returns `true` if you are pressing the key with the `keycode` printed on
it. You can pass a `Key<enum_@GlobalScope_Key>` constant or any Unicode
character code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_key\_pressed**(keycode:
`Key<enum_@GlobalScope_Key>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_is_key_pressed>`

Returns `true` if you are pressing the Latin key in the current keyboard
layout. You can pass a `Key<enum_@GlobalScope_Key>` constant.

`is_key_pressed<class_Input_method_is_key_pressed>` is only recommended
over
`is_physical_key_pressed<class_Input_method_is_physical_key_pressed>` in
non-game applications. This ensures that shortcut keys behave as
expected depending on the user's keyboard layout, as keyboard shortcuts
are generally dependent on the keyboard layout in non-game applications.
If in doubt, use
`is_physical_key_pressed<class_Input_method_is_physical_key_pressed>`.

\*\*Note:\*\* Due to keyboard ghosting,
`is_key_pressed<class_Input_method_is_key_pressed>` may return `false`
even if one of the action's keys is pressed. See [Input
examples](../tutorials/inputs/input_examples.html#keyboard-events) in
the documentation for more information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_mouse\_button\_pressed**(button:
`MouseButton<enum_@GlobalScope_MouseButton>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_is_mouse_button_pressed>`

Returns `true` if you are pressing the mouse button specified with
`MouseButton<enum_@GlobalScope_MouseButton>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_physical\_key\_pressed**(keycode:
`Key<enum_@GlobalScope_Key>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_is_physical_key_pressed>`

Returns `true` if you are pressing the key in the physical location on
the 101/102-key US QWERTY keyboard. You can pass a
`Key<enum_@GlobalScope_Key>` constant.

`is_physical_key_pressed<class_Input_method_is_physical_key_pressed>` is
recommended over `is_key_pressed<class_Input_method_is_key_pressed>` for
in-game actions, as it will make `W`/`A`/`S`/`D` layouts work regardless
of the user's keyboard layout.
`is_physical_key_pressed<class_Input_method_is_physical_key_pressed>`
will also ensure that the top row number keys work on any keyboard
layout. If in doubt, use
`is_physical_key_pressed<class_Input_method_is_physical_key_pressed>`.

\*\*Note:\*\* Due to keyboard ghosting,
`is_physical_key_pressed<class_Input_method_is_physical_key_pressed>`
may return `false` even if one of the action's keys is pressed. See
[Input
examples](../tutorials/inputs/input_examples.html#keyboard-events) in
the documentation for more information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **parse\_input\_event**(event:
`InputEvent<class_InputEvent>`)
`🔗<class_Input_method_parse_input_event>`

Feeds an `InputEvent<class_InputEvent>` to the game. Can be used to
artificially trigger input events from code. Also generates
`Node._input<class_Node_private_method__input>` calls.

gdscript

var cancel\_event = InputEventAction.new() cancel\_event.action =
"ui\_cancel" cancel\_event.pressed = true
Input.parse\_input\_event(cancel\_event)

csharp

var cancelEvent = new InputEventAction(); cancelEvent.Action =
"ui\_cancel"; cancelEvent.Pressed = true;
Input.ParseInputEvent(cancelEvent);

\*\*Note:\*\* Calling this function has no influence on the operating
system. So for example sending an
`InputEventMouseMotion<class_InputEventMouseMotion>` will not move the
OS mouse cursor to the specified position (use
`warp_mouse<class_Input_method_warp_mouse>` instead) and sending
`Alt/Cmd + Tab` as `InputEventKey<class_InputEventKey>` won't toggle
between active windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_joy\_mapping**(guid:
`String<class_String>`) `🔗<class_Input_method_remove_joy_mapping>`

Removes all mappings from the internal database that match the given
GUID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_accelerometer**(value:
`Vector3<class_Vector3>`) `🔗<class_Input_method_set_accelerometer>`

Sets the acceleration value of the accelerometer sensor. Can be used for
debugging on devices without a hardware sensor, for example in an editor
on a PC.

\*\*Note:\*\* This value can be immediately overwritten by the hardware
sensor value on Android and iOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_custom\_mouse\_cursor**(image:
`Resource<class_Resource>`, shape: `CursorShape<enum_Input_CursorShape>`
= 0, hotspot: `Vector2<class_Vector2>` = Vector2(0, 0))
`🔗<class_Input_method_set_custom_mouse_cursor>`

Sets a custom mouse cursor image, which is only visible inside the game
window. The hotspot can also be specified. Passing `null` to the image
parameter resets to the system cursor. See
`CursorShape<enum_Input_CursorShape>` for the list of shapes.

`image` can be either `Texture2D<class_Texture2D>` or
`Image<class_Image>` and its size must be lower than or equal to
256×256. To avoid rendering issues, sizes lower than or equal to 128×128
are recommended.

`hotspot` must be within `image`'s size.

\*\*Note:\*\* `AnimatedTexture<class_AnimatedTexture>`s aren't supported
as custom mouse cursors. If using an
`AnimatedTexture<class_AnimatedTexture>`, only the first frame will be
displayed.

\*\*Note:\*\* The **Lossless**, **Lossy** or **Uncompressed**
compression modes are recommended. The **Video RAM** compression mode
can be used, but it will be decompressed on the CPU, which means loading
times are slowed down and no memory is saved compared to lossless modes.

\*\*Note:\*\* On the web platform, the maximum allowed cursor image size
is 128×128. Cursor images larger than 32×32 will also only be displayed
if the mouse cursor image is entirely located within the page for
[security reasons](https://chromestatus.com/feature/5825971391299584).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_default\_cursor\_shape**(shape:
`CursorShape<enum_Input_CursorShape>` = 0)
`🔗<class_Input_method_set_default_cursor_shape>`

Sets the default cursor shape to be used in the viewport instead of
`CURSOR_ARROW<class_Input_constant_CURSOR_ARROW>`.

\*\*Note:\*\* If you want to change the default cursor shape for
`Control<class_Control>`'s nodes, use
`Control.mouse_default_cursor_shape<class_Control_property_mouse_default_cursor_shape>`
instead.

\*\*Note:\*\* This method generates an
`InputEventMouseMotion<class_InputEventMouseMotion>` to update cursor
immediately.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_gravity**(value:
`Vector3<class_Vector3>`) `🔗<class_Input_method_set_gravity>`

Sets the gravity value of the accelerometer sensor. Can be used for
debugging on devices without a hardware sensor, for example in an editor
on a PC.

\*\*Note:\*\* This value can be immediately overwritten by the hardware
sensor value on Android and iOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_gyroscope**(value:
`Vector3<class_Vector3>`) `🔗<class_Input_method_set_gyroscope>`

Sets the value of the rotation rate of the gyroscope sensor. Can be used
for debugging on devices without a hardware sensor, for example in an
editor on a PC.

\*\*Note:\*\* This value can be immediately overwritten by the hardware
sensor value on Android and iOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_magnetometer**(value:
`Vector3<class_Vector3>`) `🔗<class_Input_method_set_magnetometer>`

Sets the value of the magnetic field of the magnetometer sensor. Can be
used for debugging on devices without a hardware sensor, for example in
an editor on a PC.

\*\*Note:\*\* This value can be immediately overwritten by the hardware
sensor value on Android and iOS.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **should\_ignore\_device**(vendor\_id:
`int<class_int>`, product\_id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Input_method_should_ignore_device>`

Queries whether an input device should be ignored or not. Devices can be
ignored by setting the environment variable
`SDL_GAMECONTROLLER_IGNORE_DEVICES`. Read the [SDL
documentation](https://wiki.libsdl.org/SDL2) for more information.

\*\*Note:\*\* Some 3rd party tools can contribute to the list of ignored
devices. For example, *SteamInput* creates virtual devices from physical
devices for remapping purposes. To avoid handling the same input device
twice, the original device is added to the ignore list.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **start\_joy\_vibration**(device:
`int<class_int>`, weak\_magnitude: `float<class_float>`,
strong\_magnitude: `float<class_float>`, duration: `float<class_float>`
= 0) `🔗<class_Input_method_start_joy_vibration>`

Starts to vibrate the joypad. Joypads usually come with two rumble
motors, a strong and a weak one. `weak_magnitude` is the strength of the
weak motor (between 0 and 1) and `strong_magnitude` is the strength of
the strong motor (between 0 and 1). `duration` is the duration of the
effect in seconds (a duration of 0 will try to play the vibration
indefinitely). The vibration can be stopped early by calling
`stop_joy_vibration<class_Input_method_stop_joy_vibration>`.

\*\*Note:\*\* Not every hardware is compatible with long effect
durations; it is recommended to restart an effect if it has to be played
for more than a few seconds.

\*\*Note:\*\* For macOS, vibration is only supported in macOS 11 and
later.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop\_joy\_vibration**(device:
`int<class_int>`) `🔗<class_Input_method_stop_joy_vibration>`

Stops the vibration of the joypad started with
`start_joy_vibration<class_Input_method_start_joy_vibration>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **vibrate\_handheld**(duration\_ms:
`int<class_int>` = 500, amplitude: `float<class_float>` = -1.0)
`🔗<class_Input_method_vibrate_handheld>`

Vibrate the handheld device for the specified duration in milliseconds.

`amplitude` is the strength of the vibration, as a value between `0.0`
and `1.0`. If set to `-1.0`, the default vibration strength of the
device is used.

\*\*Note:\*\* This method is implemented on Android, iOS, and Web. It
has no effect on other platforms.

\*\*Note:\*\* For Android,
`vibrate_handheld<class_Input_method_vibrate_handheld>` requires
enabling the `VIBRATE` permission in the export preset. Otherwise,
`vibrate_handheld<class_Input_method_vibrate_handheld>` will have no
effect.

\*\*Note:\*\* For iOS, specifying the duration is only supported in iOS
13 and later.

\*\*Note:\*\* For Web, the amplitude cannot be changed.

\*\*Note:\*\* Some web browsers such as Safari and Firefox for Android
do not support `vibrate_handheld<class_Input_method_vibrate_handheld>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **warp\_mouse**(position:
`Vector2<class_Vector2>`) `🔗<class_Input_method_warp_mouse>`

Sets the mouse position to the specified vector, provided in pixels and
relative to an origin at the upper left corner of the currently focused
Window Manager game window.

Mouse position is clipped to the limits of the screen resolution, or to
the limits of the game window if `MouseMode<enum_Input_MouseMode>` is
set to `MOUSE_MODE_CONFINED<class_Input_constant_MOUSE_MODE_CONFINED>`
or
`MOUSE_MODE_CONFINED_HIDDEN<class_Input_constant_MOUSE_MODE_CONFINED_HIDDEN>`.

\*\*Note:\*\* `warp_mouse<class_Input_method_warp_mouse>` is only
supported on Windows, macOS and Linux. It has no effect on Android, iOS
and Web.
