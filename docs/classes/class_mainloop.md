github\_url  
hide

# MainLoop

**Inherits:** `Object<class_Object>`

**Inherited By:** `SceneTree<class_SceneTree>`

Abstract base class for the game's main loop.

classref-introduction-group

## Description

**MainLoop** is the abstract base class for a Godot project's game loop.
It is inherited by `SceneTree<class_SceneTree>`, which is the default
game loop implementation used in Godot projects, though it is also
possible to write and use one's own **MainLoop** subclass instead of the
scene tree.

Upon the application start, a **MainLoop** implementation must be
provided to the OS; otherwise, the application will exit. This happens
automatically (and a `SceneTree<class_SceneTree>` is created) unless a
**MainLoop** `Script<class_Script>` is provided from the command line
(with e.g. `godot -s my_loop.gd`) or the "Main Loop Type" project
setting is overwritten.

Here is an example script implementing a simple **MainLoop**:

gdscript

class\_name CustomMainLoop extends MainLoop

var time\_elapsed = 0

func \_initialize():  
print("Initialized:") print(" Starting time: %s" % str(time\_elapsed))

func \_process(delta):  
time\_elapsed += delta \# Return true to end the main loop. return
Input.get\_mouse\_button\_mask() != 0 ||
Input.is\_key\_pressed(KEY\_ESCAPE)

func \_finalize():  
print("Finalized:") print(" End time: %s" % str(time\_elapsed))

csharp

using Godot;

\[GlobalClass\] public partial class CustomMainLoop : MainLoop { private
double \_timeElapsed = 0;

> public override void \_Initialize() { GD.Print("Initialized:");
> GD.Print($" Starting Time: {\_timeElapsed}"); }
>
> public override bool \_Process(double delta) { \_timeElapsed += delta;
> // Return true to end the main loop. return Input.GetMouseButtonMask()
> != 0 || Input.IsKeyPressed(Key.Escape); }
>
> private void \_Finalize() { GD.Print("Finalized:"); GD.Print($" End
> Time: {\_timeElapsed}"); }

}

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**on\_request\_permissions\_result**(permission: `String<class_String>`,
granted: `bool<class_bool>`)
`🔗<class_MainLoop_signal_on_request_permissions_result>`

Emitted when a user responds to a permission request.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NOTIFICATION\_OS\_MEMORY\_WARNING** = `2009`
`🔗<class_MainLoop_constant_NOTIFICATION_OS_MEMORY_WARNING>`

Notification received from the OS when the application is exceeding its
allocated memory.

Specific to the iOS platform.

classref-constant

**NOTIFICATION\_TRANSLATION\_CHANGED** = `2010`
`🔗<class_MainLoop_constant_NOTIFICATION_TRANSLATION_CHANGED>`

Notification received when translations may have changed. Can be
triggered by the user changing the locale. Can be used to respond to
language changes, for example to change the UI strings on the fly.
Useful when working with the built-in translation support, like
`Object.tr<class_Object_method_tr>`.

classref-constant

**NOTIFICATION\_WM\_ABOUT** = `2011`
`🔗<class_MainLoop_constant_NOTIFICATION_WM_ABOUT>`

Notification received from the OS when a request for "About" information
is sent.

Specific to the macOS platform.

classref-constant

**NOTIFICATION\_CRASH** = `2012`
`🔗<class_MainLoop_constant_NOTIFICATION_CRASH>`

Notification received from Godot's crash handler when the engine is
about to crash.

Implemented on desktop platforms if the crash handler is enabled.

classref-constant

**NOTIFICATION\_OS\_IME\_UPDATE** = `2013`
`🔗<class_MainLoop_constant_NOTIFICATION_OS_IME_UPDATE>`

Notification received from the OS when an update of the Input Method
Engine occurs (e.g. change of IME cursor position or composition
string).

Specific to the macOS platform.

classref-constant

**NOTIFICATION\_APPLICATION\_RESUMED** = `2014`
`🔗<class_MainLoop_constant_NOTIFICATION_APPLICATION_RESUMED>`

Notification received from the OS when the application is resumed.

Specific to the Android and iOS platforms.

classref-constant

**NOTIFICATION\_APPLICATION\_PAUSED** = `2015`
`🔗<class_MainLoop_constant_NOTIFICATION_APPLICATION_PAUSED>`

Notification received from the OS when the application is paused.

Specific to the Android and iOS platforms.

\*\*Note:\*\* On iOS, you only have approximately 5 seconds to finish a
task started by this signal. If you go over this allotment, iOS will
kill the app instead of pausing it.

classref-constant

**NOTIFICATION\_APPLICATION\_FOCUS\_IN** = `2016`
`🔗<class_MainLoop_constant_NOTIFICATION_APPLICATION_FOCUS_IN>`

Notification received from the OS when the application is focused, i.e.
when changing the focus from the OS desktop or a thirdparty application
to any open window of the Godot instance.

Implemented on desktop and mobile platforms.

classref-constant

**NOTIFICATION\_APPLICATION\_FOCUS\_OUT** = `2017`
`🔗<class_MainLoop_constant_NOTIFICATION_APPLICATION_FOCUS_OUT>`

Notification received from the OS when the application is defocused,
i.e. when changing the focus from any open window of the Godot instance
to the OS desktop or a thirdparty application.

Implemented on desktop and mobile platforms.

classref-constant

**NOTIFICATION\_TEXT\_SERVER\_CHANGED** = `2018`
`🔗<class_MainLoop_constant_NOTIFICATION_TEXT_SERVER_CHANGED>`

Notification received when text server is changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_finalize**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_MainLoop_private_method__finalize>`

Called before the program exits.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_initialize**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_MainLoop_private_method__initialize>`

Called once during initialization.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_physics\_process**(delta: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_MainLoop_private_method__physics_process>`

Called each physics frame with the time since the last physics frame as
argument (`delta`, in seconds). Equivalent to
`Node._physics_process<class_Node_private_method__physics_process>`.

If implemented, the method must return a boolean value. `true` ends the
main loop, while `false` lets it proceed to the next frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_process**(delta: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_MainLoop_private_method__process>`

Called each process (idle) frame with the time since the last process
frame as argument (in seconds). Equivalent to
`Node._process<class_Node_private_method__process>`.

If implemented, the method must return a boolean value. `true` ends the
main loop, while `false` lets it proceed to the next frame.
