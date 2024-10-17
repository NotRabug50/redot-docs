github\_url  
hide

# AnimationNodeTransition

**Inherits:** `AnimationNodeSync<class_AnimationNodeSync>` **&lt;**
`AnimationNode<class_AnimationNode>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A transition within an `AnimationTree<class_AnimationTree>` connecting
two `AnimationNode<class_AnimationNode>`s.

classref-introduction-group

## Description

Simple state machine for cases which don't require a more advanced
`AnimationNodeStateMachine<class_AnimationNodeStateMachine>`. Animations
can be connected to the inputs and transition times can be specified.

After setting the request and changing the animation playback, the
transition node automatically clears the request on the next process
frame by setting its `transition_request` value to empty.

\*\*Note:\*\* When using a cross-fade, `current_state` and
`current_index` change to the next state immediately after the
cross-fade begins.

gdscript

\# Play child animation connected to "state\_2" port.
animation\_tree.set("parameters/Transition/transition\_request",
"state\_2") \# Alternative syntax (same result as above).
animation\_tree\["parameters/Transition/transition\_request"\] =
"state\_2"

\# Get current state name (read-only).
animation\_tree.get("parameters/Transition/current\_state") \#
Alternative syntax (same result as above).
animation\_tree\["parameters/Transition/current\_state"\]

\# Get current state index (read-only).
animation\_tree.get("parameters/Transition/current\_index") \#
Alternative syntax (same result as above).
animation\_tree\["parameters/Transition/current\_index"\]

csharp

// Play child animation connected to "state\_2" port.
animationTree.Set("parameters/Transition/transition\_request",
"state\_2");

// Get current state name (read-only).
animationTree.Get("parameters/Transition/current\_state");

// Get current state index (read-only).
animationTree.Get("parameters/Transition/current\_index");

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`
-   [3D Platformer
    Demo](https://godotengine.org/asset-library/asset/2748)
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **allow\_transition\_to\_self** = `false`
`🔗<class_AnimationNodeTransition_property_allow_transition_to_self>`

classref-property-setget

-   `void (No return value.)`
    **set\_allow\_transition\_to\_self**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_allow\_transition\_to\_self**()

If `true`, allows transition to the self state. When the reset option is
enabled in input, the animation is restarted. If `false`, nothing
happens on the transition to the self state.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **input\_count** = `0`
`🔗<class_AnimationNodeTransition_property_input_count>`

classref-property-setget

-   `void (No return value.)` **set\_input\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_input\_count**()

The number of enabled input ports for this animation node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Curve<class_Curve>` **xfade\_curve**
`🔗<class_AnimationNodeTransition_property_xfade_curve>`

classref-property-setget

-   `void (No return value.)` **set\_xfade\_curve**(value:
    `Curve<class_Curve>`)
-   `Curve<class_Curve>` **get\_xfade\_curve**()

Determines how cross-fading between animations is eased. If empty, the
transition will be linear.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **xfade\_time** = `0.0`
`🔗<class_AnimationNodeTransition_property_xfade_time>`

classref-property-setget

-   `void (No return value.)` **set\_xfade\_time**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_xfade\_time**()

Cross-fading time (in seconds) between each animation connected to the
inputs.

\*\*Note:\*\* **AnimationNodeTransition** transitions the current state
immediately after the start of the fading. The precise remaining time
can only be inferred from the main animation. When
`AnimationNodeOutput<class_AnimationNodeOutput>` is considered as the
most upstream, so the
`xfade_time<class_AnimationNodeTransition_property_xfade_time>` is not
scaled depending on the downstream delta. See also
`AnimationNodeOneShot.fadeout_time<class_AnimationNodeOneShot_property_fadeout_time>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **is\_input\_loop\_broken\_at\_end**(input:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeTransition_method_is_input_loop_broken_at_end>`

Returns whether the animation breaks the loop at the end of the loop
cycle for transition.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_input\_reset**(input: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeTransition_method_is_input_reset>`

Returns whether the animation restarts when the animation transitions
from the other animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_input\_set\_as\_auto\_advance**(input:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeTransition_method_is_input_set_as_auto_advance>`

Returns `true` if auto-advance is enabled for the given `input` index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_input\_as\_auto\_advance**(input:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_AnimationNodeTransition_method_set_input_as_auto_advance>`

Enables or disables auto-advance for the given `input` index. If
enabled, state changes to the next input after playing the animation
once. If enabled for the last input state, it loops to the first.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_input\_break\_loop\_at\_end**(input:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_AnimationNodeTransition_method_set_input_break_loop_at_end>`

If `true`, breaks the loop at the end of the loop cycle for transition,
even if the animation is looping.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_input\_reset**(input: `int<class_int>`,
enable: `bool<class_bool>`)
`🔗<class_AnimationNodeTransition_method_set_input_reset>`

If `true`, the destination animation is restarted when the animation
transitions.
