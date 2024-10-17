github\_url  
hide

# SceneTreeTimer

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

One-shot timer.

classref-introduction-group

## Description

A one-shot timer managed by the scene tree, which emits
`timeout<class_SceneTreeTimer_signal_timeout>` on completion. See also
`SceneTree.create_timer<class_SceneTree_method_create_timer>`.

As opposed to `Timer<class_Timer>`, it does not require the
instantiation of a node. Commonly used to create a one-shot delay timer
as in the following example:

gdscript

func some\_function():  
print("Timer started.") await get\_tree().create\_timer(1.0).timeout
print("Timer ended.")

csharp

public async Task SomeFunction() { GD.Print("Timer started."); await
ToSignal(GetTree().CreateTimer(1.0f),
SceneTreeTimer.SignalName.Timeout); GD.Print("Timer ended."); }

The timer will be dereferenced after its time elapses. To preserve the
timer, you can keep a reference to it. See
`RefCounted<class_RefCounted>`.

\*\*Note:\*\* The timer is processed after all of the nodes in the
current frame, i.e. node's
`Node._process<class_Node_private_method__process>` method would be
called before the timer (or
`Node._physics_process<class_Node_private_method__physics_process>` if
`process_in_physics` in
`SceneTree.create_timer<class_SceneTree_method_create_timer>` has been
set to `true`).

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**timeout**() `🔗<class_SceneTreeTimer_signal_timeout>`

Emitted when the timer reaches 0.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **time\_left**
`🔗<class_SceneTreeTimer_property_time_left>`

classref-property-setget

-   `void (No return value.)` **set\_time\_left**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_time\_left**()

The time remaining (in seconds).
