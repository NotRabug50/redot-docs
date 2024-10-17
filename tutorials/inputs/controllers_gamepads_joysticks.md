# Controllers, gamepads, and joysticks

Godot supports hundreds of controller models thanks to the
community-sourced [SDL game controller
database](https://github.com/gabomdq/SDL_GameControllerDB).

Controllers are supported on Windows, macOS, Linux, Android, iOS, and
HTML5.

Note that more specialized devices such as steering wheels, rudder
pedals and [HOTAS](https://en.wikipedia.org/wiki/HOTAS) are less tested
and may not always work as expected. Overriding force feedback for those
devices is also not implemented yet. If you have access to one of those
devices, don't hesitate to [report bugs on
GitHub](https://github.com/godotengine/godot/blob/master/CONTRIBUTING.md#reporting-bugs).

In this guide, you will learn:

-   **How to write your input logic to support both keyboard and
    controller inputs.**
-   **How controllers can behave differently from keyboard/mouse
    input.**
-   **Troubleshooting issues with controllers in Godot.**

## Supporting universal input

Thanks to Godot's input action system, Godot makes it possible to
support both keyboard and controller input without having to write
separate code paths. Instead of hardcoding keys or controller buttons in
your scripts, you should create *input actions* in the Project Settings
which will then refer to specified key and controller inputs.

Input actions are explained in detail on the `doc_inputevent` page.

Note

Unlike keyboard input, supporting both mouse and controller input for an
action (such as looking around in a first-person game) will require
different code paths since these have to be handled separately.

### Which Input singleton method should I use?

There are 3 ways to get input in an analog-aware way:

-   When you have two axes (such as joystick or WASD movement) and want
    both axes to behave as a single input, use `Input.get_vector()`:

.. code-tab:: gdscript GDScript

\# <span class="title-ref">velocity</span> will be a Vector2 between
<span class="title-ref">Vector2(-1.0, -1.0)</span> and
<span class="title-ref">Vector2(1.0, 1.0)</span>. \# This handles
deadzone in a correct way for most use cases. \# The resulting deadzone
will have a circular shape as it generally should. var velocity =
Input.get\_vector("move\_left", "move\_right", "move\_forward",
"move\_back")

\# The line below is similar to
<span class="title-ref">get\_vector()</span>, except that it handles \#
the deadzone in a less optimal way. The resulting deadzone will have \#
a square-ish shape when it should ideally have a circular shape. var
velocity = Vector2( Input.get\_action\_strength("move\_right") -
Input.get\_action\_strength("move\_left"),
Input.get\_action\_strength("move\_back") -
Input.get\_action\_strength("move\_forward") ).limit\_length(1.0)

csharp

// <span class="title-ref">velocity</span> will be a Vector2 between
<span class="title-ref">Vector2(-1.0, -1.0)</span> and
<span class="title-ref">Vector2(1.0, 1.0)</span>. // This handles
deadzone in a correct way for most use cases. // The resulting deadzone
will have a circular shape as it generally should. Vector2 velocity =
Input.GetVector("move\_left", "move\_right", "move\_forward",
"move\_back");

// The line below is similar to
<span class="title-ref">get\_vector()</span>, except that it handles //
the deadzone in a less optimal way. The resulting deadzone will have //
a square-ish shape when it should ideally have a circular shape. Vector2
velocity = new Vector2( Input.GetActionStrength("move\_right") -
Input.GetActionStrength("move\_left"),
Input.GetActionStrength("move\_back") -
Input.GetActionStrength("move\_forward") ).LimitLength(1.0);

-   When you have one axis that can go both ways (such as a throttle on
    a flight stick), or when you want to handle separate axes
    individually, use `Input.get_axis()`:

.. code-tab:: gdscript GDScript

\# <span class="title-ref">walk</span> will be a floating-point number
between <span class="title-ref">-1.0</span> and
<span class="title-ref">1.0</span>. var walk =
Input.get\_axis("move\_left", "move\_right")

\# The line above is a shorter form of: var walk =
Input.get\_action\_strength("move\_right") -
Input.get\_action\_strength("move\_left")

csharp

// <span class="title-ref">walk</span> will be a floating-point number
between <span class="title-ref">-1.0</span> and
<span class="title-ref">1.0</span>. float walk =
Input.GetAxis("move\_left", "move\_right");

// The line above is a shorter form of: float walk =
Input.GetActionStrength("move\_right") -
Input.GetActionStrength("move\_left");

-   For other types of analog input, such as handling a trigger or
    handling one direction at a time, use `Input.get_action_strength()`:

.. code-tab:: gdscript GDScript

\# <span class="title-ref">strength</span> will be a floating-point
number between <span class="title-ref">0.0</span> and
<span class="title-ref">1.0</span>. var strength =
Input.get\_action\_strength("accelerate")

csharp

// <span class="title-ref">strength</span> will be a floating-point
number between <span class="title-ref">0.0</span> and
<span class="title-ref">1.0</span>. float strength =
Input.GetActionStrength("accelerate");

For non-analog digital/boolean input (only "pressed" or "not pressed"
values), such as controller buttons, mouse buttons or keyboard keys, use
`Input.is_action_pressed()`:

.. code-tab:: gdscript GDScript

\# <span class="title-ref">jumping</span> will be a boolean with a value
of <span class="title-ref">true</span> or
<span class="title-ref">false</span>. var jumping =
Input.is\_action\_pressed("jump")

csharp

// <span class="title-ref">jumping</span> will be a boolean with a value
of <span class="title-ref">true</span> or
<span class="title-ref">false</span>. bool jumping =
Input.IsActionPressed("jump");

Note

If you need to know whether an input was *just* pressed in the previous
frame, use `Input.is_action_just_pressed()` instead of
`Input.is_action_pressed()`. Unlike `Input.is_action_pressed()` which
returns `true` as long as the input is held,
`Input.is_action_just_pressed()` will only return `true` for one frame
after the button has been pressed.

In Godot versions before 3.4, such as 3.3, `Input.get_vector()` and
`Input.get_axis()` aren't available. Only `Input.get_action_strength()`
and `Input.is_action_pressed()` are available in Godot 3.3.

## Vibration

Vibration (also called *haptic feedback*) can be used to enhance the
feel of a game. For instance, in a racing game, you can convey the
surface the car is currently driving on through vibration, or create a
sudden vibration on a crash.

Use the Input singleton's
`start_joy_vibration<class_Input_method_start_joy_vibration>` method to
start vibrating a gamepad. Use
`stop_joy_vibration<class_Input_method_stop_joy_vibration>` to stop
vibration early (useful if no duration was specified when starting).

On mobile devices, you can also use
`vibrate_handheld<class_Input_method_vibrate_handheld>` to vibrate the
device itself (independently from the gamepad). On Android, this
requires the `VIBRATE` permission to be enabled in the Android export
preset before exporting the project.

Note

Vibration can be uncomfortable for certain players. Make sure to provide
an in-game slider to disable vibration or reduce its intensity.

## Differences between keyboard/mouse and controller input

If you're used to handling keyboard and mouse input, you may be
surprised by how controllers handle specific situations.

### Dead zone

Unlike keyboards and mice, controllers offer axes with *analog* inputs.
The upside of analog inputs is that they offer additional flexibility
for actions. Unlike digital inputs which can only provide strengths of
`0.0` and `1.0`, an analog input can provide *any* strength between
`0.0` and `1.0`. The downside is that without a deadzone system, an
analog axis' strength will never be equal to `0.0` due to how the
controller is physically built. Instead, it will linger at a low value
such as `0.062`. This phenomenon is known as *drifting* and can be more
noticeable on old or faulty controllers.

Let's take a racing game as a real-world example. Thanks to analog
inputs, we can steer the car slowly in one direction or another.
However, without a deadzone system, the car would slowly steer by itself
even if the player isn't touching the joystick. This is because the
directional axis strength won't be equal to `0.0` when we expect it to.
Since we don't want our car to steer by itself in this case, we define a
"dead zone" value of `0.2` which will ignore all input whose strength is
lower than `0.2`. An ideal dead zone value is high enough to ignore the
input caused by joystick drifting, but is low enough to not ignore
actual input from the player.

Godot features a built-in deadzone system to tackle this problem. The
default value is `0.5`, but you can adjust it on a per-action basis in
the Project Settings' Input Map tab. For `Input.get_vector()`, the
deadzone can be specified as an optional 5th parameter. If not
specified, it will calculate the average deadzone value from all of the
actions in the vector.

### "Echo" events

Unlike keyboard input, holding down a controller button such as a D-pad
direction will **not** generate repeated input events at fixed intervals
(also known as "echo" events). This is because the operating system
never sends "echo" events for controller input in the first place.

If you want controller buttons to send echo events, you will have to
generate `class_InputEvent` objects by code and parse them using
`Input.parse_input_event() <class_Input_method_parse_input_event>` at
regular intervals. This can be accomplished with the help of a
`class_Timer` node.

### Window focus

Unlike keyboard input, controller inputs can be seen by **all** windows
on the operating system, including unfocused windows.

While this is useful for [third-party split screen
functionality](https://nucleus-coop.github.io/), it can also have
adverse effects. Players may accidentally send controller inputs to the
running project while interacting with another window.

If you wish to ignore events when the project window isn't focused, you
will need to create an `autoload <doc_singletons_autoload>` called
`Focus` with the following script and use it to check all your inputs:

    # Focus.gd
    extends Node

    var focused := true

    func _notification(what: int) -> void:
        match what:
            NOTIFICATION_APPLICATION_FOCUS_OUT:
                focused = false
            NOTIFICATION_APPLICATION_FOCUS_IN:
                focused = true


    func input_is_action_pressed(action: StringName) -> bool:
        if focused:
            return Input.is_action_pressed(action)

        return false


    func event_is_action_pressed(event: InputEvent, action: StringName) -> bool:
        if focused:
            return event.is_action_pressed(action)

        return false

Then, instead of using `Input.is_action_pressed(action)`, use
`Focus.input_is_action_pressed(action)` where `action` is the name of
the input action. Also, instead of using
`event.is_action_pressed(action)`, use
`Focus.event_is_action_pressed(event, action)` where `event` is an
InputEvent reference and `action` is the name of the input action.

### Power saving prevention

Unlike keyboard and mouse input, controller inputs do **not** inhibit
sleep and power saving measures (such as turning off the screen after a
certain amount of time has passed).

To combat this, Godot enables power saving prevention by default when a
project is running. If you notice the system is turning off its display
when playing with a gamepad, check the value of **Display &gt; Window
&gt; Energy Saving &gt; Keep Screen On** in the Project Settings.

On Linux, power saving prevention requires the engine to be able to use
D-Bus. Check whether D-Bus is installed and reachable if running the
project within a Flatpak, as sandboxing restrictions may make this
impossible by default.

## Troubleshooting

You can view a list of [known issues with controller
support](https://github.com/godotengine/godot/issues?q=is%3Aopen+is%3Aissue+label%3Atopic%3Ainput+gamepad)
on GitHub.

### My controller isn't recognized by Godot.

First, check that your controller is recognized by other applications.
You can use the [Gamepad Tester](https://gamepad-tester.com/) website to
confirm that your controller is recognized.

On Windows Godot only supports up to 4 controllers at a time. This is
because Godot uses the XInput API, which is limited to supporting 4
controllers at once. Additional controllers above this limit are ignored
by Godot.

### My controller has incorrectly mapped buttons or axes.

First, if your controller provides some kind of firmware update utility,
make sure to run it to get the latest fixes from the manufacturer. For
instance, Xbox One and Xbox Series controllers can have their firmware
updated using the [Xbox Accessories
app](https://www.microsoft.com/en-us/p/xbox-accessories/9nblggh30xj3).
(This application only runs on Windows, so you have to use a Windows
machine or a Windows virtual machine with USB support to update the
controller's firmware.) After updating the controller's firmware, unpair
the controller and pair it again with your PC if you are using the
controller in wireless mode.

If buttons are incorrectly mapped, this may be due to an erroneous
mapping from the [SDL game controller
database](https://github.com/gabomdq/SDL_GameControllerDB). You can
contribute an updated mapping to be included in the next Godot version
by opening a pull request on the linked repository.

There are many ways to create mappings. One option is to use the mapping
wizard in the [official Joypads
demo](https://godotengine.org/asset-library/asset/2785). Once you have a
working mapping for your controller, you can test it by defining the
`SDL_GAMECONTROLLERCONFIG` environment variable before running Godot:

.. code-tab:: bash Linux/macOS

export SDL\_GAMECONTROLLERCONFIG="your:mapping:here"
./path/to/godot.x86\_64

bat Windows (cmd)

set SDL\_GAMECONTROLLERCONFIG=your:mapping:here pathtogodot.exe

powershell Windows (PowerShell)

$env:SDL\_GAMECONTROLLERCONFIG="your:mapping:here" pathtogodot.exe

To test mappings on non-desktop platforms or to distribute your project
with additional controller mappings, you can add them by calling
`Input.add_joy_mapping() <class_Input_method_add_joy_mapping>` as early
as possible in a script's `_ready()` function.

### My controller works on a given platform, but not on another platform.

#### Linux

If you're using a self-compiled engine binary, make sure it was compiled
with udev support. This is enabled by default, but it is possible to
disable udev support by specifying `udev=no` on the SCons command line.
If you're using an engine binary supplied by a Linux distribution,
double-check whether it was compiled with udev support.

Controllers can still work without udev support, but it is less reliable
as regular polling must be used to check for controllers being connected
or disconnected during gameplay (hotplugging).

#### HTML5

HTML5 controller support is often less reliable compared to "native"
platforms. The quality of controller support tends to vary wildly across
browsers. As a result, you may have to instruct your players to use a
different browser if they can't get their controller to work.
