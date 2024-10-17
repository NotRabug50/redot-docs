github\_url  
hide

# AnimationNodeStateMachinePlayback

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Provides playback control for an
`AnimationNodeStateMachine<class_AnimationNodeStateMachine>`.

classref-introduction-group

## Description

Allows control of `AnimationTree<class_AnimationTree>` state machines
created with
`AnimationNodeStateMachine<class_AnimationNodeStateMachine>`. Retrieve
with `$AnimationTree.get("parameters/playback")`.

gdscript

var state\_machine = $AnimationTree.get("parameters/playback")
state\_machine.travel("some\_state")

csharp

var stateMachine =
GetNode&lt;AnimationTree&gt;("AnimationTree").Get("parameters/playback").As&lt;AnimationNodeStateMachinePlayback&gt;();
stateMachine.Travel("some\_state");

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`

classref-reftable-group

## Properties

<table>
<tbody>
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_current\_length**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeStateMachinePlayback_method_get_current_length>`

Returns the current state length.

\*\*Note:\*\* It is possible that any
`AnimationRootNode<class_AnimationRootNode>` can be nodes as well as
animations. This means that there can be multiple animations within a
single state. Which animation length has priority depends on the nodes
connected inside it. Also, if a transition does not reset, the remaining
length at that point will be returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_current\_node**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeStateMachinePlayback_method_get_current_node>`

Returns the currently playing animation state.

\*\*Note:\*\* When using a cross-fade, the current state changes to the
next state immediately after the cross-fade begins.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_current\_play\_position**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeStateMachinePlayback_method_get_current_play_position>`

Returns the playback position within the current animation state.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_fading\_from\_node**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeStateMachinePlayback_method_get_fading_from_node>`

Returns the starting state of currently fading animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`StringName<class_StringName>`\]
**get\_travel\_path**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeStateMachinePlayback_method_get_travel_path>`

Returns the current travel path as computed internally by the A\*
algorithm.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_playing**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeStateMachinePlayback_method_is_playing>`

Returns `true` if an animation is playing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **next**()
`🔗<class_AnimationNodeStateMachinePlayback_method_next>`

If there is a next path by travel or auto advance, immediately
transitions from the current state to the next state.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **start**(node:
`StringName<class_StringName>`, reset: `bool<class_bool>` = true)
`🔗<class_AnimationNodeStateMachinePlayback_method_start>`

Starts playing the given animation.

If `reset` is `true`, the animation is played from the beginning.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop**()
`🔗<class_AnimationNodeStateMachinePlayback_method_stop>`

Stops the currently playing animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **travel**(to\_node:
`StringName<class_StringName>`, reset\_on\_teleport: `bool<class_bool>`
= true) `🔗<class_AnimationNodeStateMachinePlayback_method_travel>`

Transitions from the current state to another one, following the
shortest path.

If the path does not connect from the current state, the animation will
play after the state teleports.

If `reset_on_teleport` is `true`, the animation is played from the
beginning when the travel cause a teleportation.
