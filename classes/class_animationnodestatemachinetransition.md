github\_url  
hide

# AnimationNodeStateMachineTransition

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A transition within an
`AnimationNodeStateMachine<class_AnimationNodeStateMachine>` connecting
two `AnimationRootNode<class_AnimationRootNode>`s.

classref-introduction-group

## Description

The path generated when using
`AnimationNodeStateMachinePlayback.travel<class_AnimationNodeStateMachinePlayback_method_travel>`
is limited to the nodes connected by
**AnimationNodeStateMachineTransition**.

You can set the timing and conditions of the transition in detail.

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**advance\_condition\_changed**()
`🔗<class_AnimationNodeStateMachineTransition_signal_advance_condition_changed>`

Emitted when
`advance_condition<class_AnimationNodeStateMachineTransition_property_advance_condition>`
is changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **SwitchMode**:
`🔗<enum_AnimationNodeStateMachineTransition_SwitchMode>`

classref-enumeration-constant

`SwitchMode<enum_AnimationNodeStateMachineTransition_SwitchMode>`
**SWITCH\_MODE\_IMMEDIATE** = `0`

Switch to the next state immediately. The current state will end and
blend into the beginning of the new one.

classref-enumeration-constant

`SwitchMode<enum_AnimationNodeStateMachineTransition_SwitchMode>`
**SWITCH\_MODE\_SYNC** = `1`

Switch to the next state immediately, but will seek the new state to the
playback position of the old state.

classref-enumeration-constant

`SwitchMode<enum_AnimationNodeStateMachineTransition_SwitchMode>`
**SWITCH\_MODE\_AT\_END** = `2`

Wait for the current state playback to end, then switch to the beginning
of the next state animation.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AdvanceMode**:
`🔗<enum_AnimationNodeStateMachineTransition_AdvanceMode>`

classref-enumeration-constant

`AdvanceMode<enum_AnimationNodeStateMachineTransition_AdvanceMode>`
**ADVANCE\_MODE\_DISABLED** = `0`

Don't use this transition.

classref-enumeration-constant

`AdvanceMode<enum_AnimationNodeStateMachineTransition_AdvanceMode>`
**ADVANCE\_MODE\_ENABLED** = `1`

Only use this transition during
`AnimationNodeStateMachinePlayback.travel<class_AnimationNodeStateMachinePlayback_method_travel>`.

classref-enumeration-constant

`AdvanceMode<enum_AnimationNodeStateMachineTransition_AdvanceMode>`
**ADVANCE\_MODE\_AUTO** = `2`

Automatically use this transition if the
`advance_condition<class_AnimationNodeStateMachineTransition_property_advance_condition>`
and
`advance_expression<class_AnimationNodeStateMachineTransition_property_advance_expression>`
checks are true (if assigned).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`StringName<class_StringName>` **advance\_condition** = `&""`
`🔗<class_AnimationNodeStateMachineTransition_property_advance_condition>`

classref-property-setget

-   `void (No return value.)` **set\_advance\_condition**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_advance\_condition**()

Turn on auto advance when this condition is set. The provided name will
become a boolean parameter on the `AnimationTree<class_AnimationTree>`
that can be controlled from code (see [Using
AnimationTree](../tutorials/animation/animation_tree.html#controlling-from-code)).
For example, if
`AnimationTree.tree_root<class_AnimationTree_property_tree_root>` is an
`AnimationNodeStateMachine<class_AnimationNodeStateMachine>` and
`advance_condition<class_AnimationNodeStateMachineTransition_property_advance_condition>`
is set to `"idle"`:

gdscript

$animation\_tree.set("parameters/conditions/idle", is\_on\_floor and
(linear\_velocity.x == 0))

csharp

GetNode&lt;AnimationTree&gt;("animation\_tree").Set("parameters/conditions/idle",
IsOnFloor && (LinearVelocity.X == 0));

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **advance\_expression** = `""`
`🔗<class_AnimationNodeStateMachineTransition_property_advance_expression>`

classref-property-setget

-   `void (No return value.)` **set\_advance\_expression**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_advance\_expression**()

Use an expression as a condition for state machine transitions. It is
possible to create complex animation advance conditions for switching
between states and gives much greater flexibility for creating complex
state machines by directly interfacing with the script code.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AdvanceMode<enum_AnimationNodeStateMachineTransition_AdvanceMode>`
**advance\_mode** = `1`
`🔗<class_AnimationNodeStateMachineTransition_property_advance_mode>`

classref-property-setget

-   `void (No return value.)` **set\_advance\_mode**(value:
    `AdvanceMode<enum_AnimationNodeStateMachineTransition_AdvanceMode>`)
-   `AdvanceMode<enum_AnimationNodeStateMachineTransition_AdvanceMode>`
    **get\_advance\_mode**()

Determines whether the transition should disabled, enabled when using
`AnimationNodeStateMachinePlayback.travel<class_AnimationNodeStateMachinePlayback_method_travel>`,
or traversed automatically if the
`advance_condition<class_AnimationNodeStateMachineTransition_property_advance_condition>`
and
`advance_expression<class_AnimationNodeStateMachineTransition_property_advance_expression>`
checks are true (if assigned).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **break\_loop\_at\_end** = `false`
`🔗<class_AnimationNodeStateMachineTransition_property_break_loop_at_end>`

classref-property-setget

-   `void (No return value.)` **set\_break\_loop\_at\_end**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_loop\_broken\_at\_end**()

If `true`, breaks the loop at the end of the loop cycle for transition,
even if the animation is looping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **priority** = `1`
`🔗<class_AnimationNodeStateMachineTransition_property_priority>`

classref-property-setget

-   `void (No return value.)` **set\_priority**(value: `int<class_int>`)
-   `int<class_int>` **get\_priority**()

Lower priority transitions are preferred when travelling through the
tree via
`AnimationNodeStateMachinePlayback.travel<class_AnimationNodeStateMachinePlayback_method_travel>`
or
`advance_mode<class_AnimationNodeStateMachineTransition_property_advance_mode>`
is set to
`ADVANCE_MODE_AUTO<class_AnimationNodeStateMachineTransition_constant_ADVANCE_MODE_AUTO>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **reset** = `true`
`🔗<class_AnimationNodeStateMachineTransition_property_reset>`

classref-property-setget

-   `void (No return value.)` **set\_reset**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_reset**()

If `true`, the destination animation is played back from the beginning
when switched.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SwitchMode<enum_AnimationNodeStateMachineTransition_SwitchMode>`
**switch\_mode** = `0`
`🔗<class_AnimationNodeStateMachineTransition_property_switch_mode>`

classref-property-setget

-   `void (No return value.)` **set\_switch\_mode**(value:
    `SwitchMode<enum_AnimationNodeStateMachineTransition_SwitchMode>`)
-   `SwitchMode<enum_AnimationNodeStateMachineTransition_SwitchMode>`
    **get\_switch\_mode**()

The transition type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Curve<class_Curve>` **xfade\_curve**
`🔗<class_AnimationNodeStateMachineTransition_property_xfade_curve>`

classref-property-setget

-   `void (No return value.)` **set\_xfade\_curve**(value:
    `Curve<class_Curve>`)
-   `Curve<class_Curve>` **get\_xfade\_curve**()

Ease curve for better control over cross-fade between this state and the
next.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **xfade\_time** = `0.0`
`🔗<class_AnimationNodeStateMachineTransition_property_xfade_time>`

classref-property-setget

-   `void (No return value.)` **set\_xfade\_time**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_xfade\_time**()

The time to cross-fade between this state and the next.

\*\*Note:\*\*
`AnimationNodeStateMachine<class_AnimationNodeStateMachine>` transitions
the current state immediately after the start of the fading. The precise
remaining time can only be inferred from the main animation. When
`AnimationNodeOutput<class_AnimationNodeOutput>` is considered as the
most upstream, so the
`xfade_time<class_AnimationNodeStateMachineTransition_property_xfade_time>`
is not scaled depending on the downstream delta. See also
`AnimationNodeOneShot.fadeout_time<class_AnimationNodeOneShot_property_fadeout_time>`.
