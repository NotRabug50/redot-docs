github\_url  
hide

# AnimationPlayer

**Inherits:** `AnimationMixer<class_AnimationMixer>` **&lt;**
`Node<class_Node>` **&lt;** `Object<class_Object>`

A node used for animation playback.

classref-introduction-group

## Description

An animation player is used for general-purpose playback of animations.
It contains a dictionary of `AnimationLibrary<class_AnimationLibrary>`
resources and custom blend times between animation transitions.

Some methods and properties use a single key to reference an animation
directly. These keys are formatted as the key for the library, followed
by a forward slash, then the key for the animation within the library,
for example `"movement/run"`. If the library's key is an empty string
(known as the default library), the forward slash is omitted, being the
same key used by the library.

\*\*AnimationPlayer\*\* is better-suited than `Tween<class_Tween>` for
more complex animations, for example ones with non-trivial timings. It
can also be used over `Tween<class_Tween>` if the animation track editor
is more convenient than doing it in code.

Updating the target properties of animations occurs at the process
frame.

classref-introduction-group

## Tutorials

-   `2D Sprite animation <../tutorials/2d/2d_sprite_animation>`
-   `Animation documentation index <../tutorials/animation/index>`
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

**animation\_changed**(old\_name: `StringName<class_StringName>`,
new\_name: `StringName<class_StringName>`)
`🔗<class_AnimationPlayer_signal_animation_changed>`

Emitted when a queued animation plays after the previous animation
finished. See also `queue<class_AnimationPlayer_method_queue>`.

\*\*Note:\*\* The signal is not emitted when the animation is changed
via `play<class_AnimationPlayer_method_play>` or by an
`AnimationTree<class_AnimationTree>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**current\_animation\_changed**(name: `String<class_String>`)
`🔗<class_AnimationPlayer_signal_current_animation_changed>`

Emitted when
`current_animation<class_AnimationPlayer_property_current_animation>`
changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **AnimationProcessCallback**:
`🔗<enum_AnimationPlayer_AnimationProcessCallback>`

classref-enumeration-constant

`AnimationProcessCallback<enum_AnimationPlayer_AnimationProcessCallback>`
**ANIMATION\_PROCESS\_PHYSICS** = `0`

**Deprecated:** See
`AnimationMixer.ANIMATION_CALLBACK_MODE_PROCESS_PHYSICS<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_PROCESS_PHYSICS>`.

classref-enumeration-constant

`AnimationProcessCallback<enum_AnimationPlayer_AnimationProcessCallback>`
**ANIMATION\_PROCESS\_IDLE** = `1`

**Deprecated:** See
`AnimationMixer.ANIMATION_CALLBACK_MODE_PROCESS_IDLE<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_PROCESS_IDLE>`.

classref-enumeration-constant

`AnimationProcessCallback<enum_AnimationPlayer_AnimationProcessCallback>`
**ANIMATION\_PROCESS\_MANUAL** = `2`

**Deprecated:** See
`AnimationMixer.ANIMATION_CALLBACK_MODE_PROCESS_MANUAL<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_PROCESS_MANUAL>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AnimationMethodCallMode**:
`🔗<enum_AnimationPlayer_AnimationMethodCallMode>`

classref-enumeration-constant

`AnimationMethodCallMode<enum_AnimationPlayer_AnimationMethodCallMode>`
**ANIMATION\_METHOD\_CALL\_DEFERRED** = `0`

**Deprecated:** See
`AnimationMixer.ANIMATION_CALLBACK_MODE_METHOD_DEFERRED<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_METHOD_DEFERRED>`.

classref-enumeration-constant

`AnimationMethodCallMode<enum_AnimationPlayer_AnimationMethodCallMode>`
**ANIMATION\_METHOD\_CALL\_IMMEDIATE** = `1`

**Deprecated:** See
`AnimationMixer.ANIMATION_CALLBACK_MODE_METHOD_IMMEDIATE<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_METHOD_IMMEDIATE>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **assigned\_animation**
`🔗<class_AnimationPlayer_property_assigned_animation>`

classref-property-setget

-   `void (No return value.)` **set\_assigned\_animation**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_assigned\_animation**()

If playing, the current animation's key, otherwise, the animation last
played. When set, this changes the animation, but will not play it
unless already playing. See also
`current_animation<class_AnimationPlayer_property_current_animation>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **autoplay** = `""`
`🔗<class_AnimationPlayer_property_autoplay>`

classref-property-setget

-   `void (No return value.)` **set\_autoplay**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_autoplay**()

The key of the animation to play when the scene loads.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **current\_animation** = `""`
`🔗<class_AnimationPlayer_property_current_animation>`

classref-property-setget

-   `void (No return value.)` **set\_current\_animation**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_current\_animation**()

The key of the currently playing animation. If no animation is playing,
the property's value is an empty string. Changing this value does not
restart the animation. See `play<class_AnimationPlayer_method_play>` for
more information on playing animations.

\*\*Note:\*\* While this property appears in the Inspector, it's not
meant to be edited, and it's not saved in the scene. This property is
mainly used to get the currently playing animation, and internally for
animation playback tracks. For more information, see
`Animation<class_Animation>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **current\_animation\_length**
`🔗<class_AnimationPlayer_property_current_animation_length>`

classref-property-setget

-   `float<class_float>` **get\_current\_animation\_length**()

The length (in seconds) of the currently playing animation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **current\_animation\_position**
`🔗<class_AnimationPlayer_property_current_animation_position>`

classref-property-setget

-   `float<class_float>` **get\_current\_animation\_position**()

The position (in seconds) of the currently playing animation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **movie\_quit\_on\_finish** = `false`
`🔗<class_AnimationPlayer_property_movie_quit_on_finish>`

classref-property-setget

-   `void (No return value.)`
    **set\_movie\_quit\_on\_finish\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_movie\_quit\_on\_finish\_enabled**()

If `true` and the engine is running in Movie Maker mode (see
`MovieWriter<class_MovieWriter>`), exits the engine with
`SceneTree.quit<class_SceneTree_method_quit>` as soon as an animation is
done playing in this **AnimationPlayer**. A message is printed when the
engine quits for this reason.

\*\*Note:\*\* This obeys the same logic as the
`AnimationMixer.animation_finished<class_AnimationMixer_signal_animation_finished>`
signal, so it will not quit the engine if the animation is set to be
looping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **playback\_auto\_capture** = `true`
`🔗<class_AnimationPlayer_property_playback_auto_capture>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_capture**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_auto\_capture**()

If `true`, performs
`AnimationMixer.capture<class_AnimationMixer_method_capture>` before
playback automatically. This means just
`play_with_capture<class_AnimationPlayer_method_play_with_capture>` is
executed with default arguments instead of
`play<class_AnimationPlayer_method_play>`.

\*\*Note:\*\* Capture interpolation is only performed if the animation
contains a capture track. See also
`Animation.UPDATE_CAPTURE<class_Animation_constant_UPDATE_CAPTURE>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **playback\_auto\_capture\_duration** = `-1.0`
`🔗<class_AnimationPlayer_property_playback_auto_capture_duration>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_capture\_duration**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_auto\_capture\_duration**()

See also
`play_with_capture<class_AnimationPlayer_method_play_with_capture>` and
`AnimationMixer.capture<class_AnimationMixer_method_capture>`.

If
`playback_auto_capture_duration<class_AnimationPlayer_property_playback_auto_capture_duration>`
is negative value, the duration is set to the interval between the
current position and the first key.

classref-item-separator

------------------------------------------------------------------------

classref-property

`EaseType<enum_Tween_EaseType>` **playback\_auto\_capture\_ease\_type**
= `0`
`🔗<class_AnimationPlayer_property_playback_auto_capture_ease_type>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_capture\_ease\_type**(value:
    `EaseType<enum_Tween_EaseType>`)
-   `EaseType<enum_Tween_EaseType>` **get\_auto\_capture\_ease\_type**()

The ease type of the capture interpolation. See also
`EaseType<enum_Tween_EaseType>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TransitionType<enum_Tween_TransitionType>`
**playback\_auto\_capture\_transition\_type** = `0`
`🔗<class_AnimationPlayer_property_playback_auto_capture_transition_type>`

classref-property-setget

-   `void (No return value.)`
    **set\_auto\_capture\_transition\_type**(value:
    `TransitionType<enum_Tween_TransitionType>`)
-   `TransitionType<enum_Tween_TransitionType>`
    **get\_auto\_capture\_transition\_type**()

The transition type of the capture interpolation. See also
`TransitionType<enum_Tween_TransitionType>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **playback\_default\_blend\_time** = `0.0`
`🔗<class_AnimationPlayer_property_playback_default_blend_time>`

classref-property-setget

-   `void (No return value.)` **set\_default\_blend\_time**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_default\_blend\_time**()

The default time in which to blend animations. Ranges from 0 to 4096
with 0.01 precision.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **speed\_scale** = `1.0`
`🔗<class_AnimationPlayer_property_speed_scale>`

classref-property-setget

-   `void (No return value.)` **set\_speed\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_speed\_scale**()

The speed scaling ratio. For example, if this value is `1`, then the
animation plays at normal speed. If it's `0.5`, then it plays at half
speed. If it's `2`, then it plays at double speed.

If set to a negative value, the animation is played in reverse. If set
to `0`, the animation will not advance.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`StringName<class_StringName>` **animation\_get\_next**(animation\_from:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationPlayer_method_animation_get_next>`

Returns the key of the animation which is queued to play after the
`animation_from` animation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **animation\_set\_next**(animation\_from:
`StringName<class_StringName>`, animation\_to:
`StringName<class_StringName>`)
`🔗<class_AnimationPlayer_method_animation_set_next>`

Triggers the `animation_to` animation when the `animation_from`
animation completes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_queue**()
`🔗<class_AnimationPlayer_method_clear_queue>`

Clears all queued, unplayed animations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_blend\_time**(animation\_from:
`StringName<class_StringName>`, animation\_to:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationPlayer_method_get_blend_time>`

Returns the blend time (in seconds) between two animations, referenced
by their keys.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AnimationMethodCallMode<enum_AnimationPlayer_AnimationMethodCallMode>`
**get\_method\_call\_mode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationPlayer_method_get_method_call_mode>`

**Deprecated:** Use
`AnimationMixer.callback_mode_method<class_AnimationMixer_property_callback_mode_method>`
instead.

Returns the call mode used for "Call Method" tracks.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_playing\_speed**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationPlayer_method_get_playing_speed>`

Returns the actual playing speed of current animation or `0` if not
playing. This speed is the
`speed_scale<class_AnimationPlayer_property_speed_scale>` property
multiplied by `custom_speed` argument specified when calling the
`play<class_AnimationPlayer_method_play>` method.

Returns a negative value if the current animation is playing backwards.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AnimationProcessCallback<enum_AnimationPlayer_AnimationProcessCallback>`
**get\_process\_callback**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationPlayer_method_get_process_callback>`

**Deprecated:** Use
`AnimationMixer.callback_mode_process<class_AnimationMixer_property_callback_mode_process>`
instead.

Returns the process notification in which to update animations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_queue**()
`🔗<class_AnimationPlayer_method_get_queue>`

Returns a list of the animation keys that are currently queued to play.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **get\_root**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationPlayer_method_get_root>`

**Deprecated:** Use
`AnimationMixer.root_node<class_AnimationMixer_property_root_node>`
instead.

Returns the node which node path references will travel from.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_section\_end\_time**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationPlayer_method_get_section_end_time>`

Returns the end time of the section currently being played.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_section\_start\_time**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationPlayer_method_get_section_start_time>`

Returns the start time of the section currently being played.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_section**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationPlayer_method_has_section>`

Returns `true` if an animation is currently playing with section.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_playing**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationPlayer_method_is_playing>`

Returns `true` if an animation is currently playing (even if
`speed_scale<class_AnimationPlayer_property_speed_scale>` and/or
`custom_speed` are `0`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **pause**()
`🔗<class_AnimationPlayer_method_pause>`

Pauses the currently playing animation. The
`current_animation_position<class_AnimationPlayer_property_current_animation_position>`
will be kept and calling `play<class_AnimationPlayer_method_play>` or
`play_backwards<class_AnimationPlayer_method_play_backwards>` without
arguments or with the same animation name as
`assigned_animation<class_AnimationPlayer_property_assigned_animation>`
will resume the animation.

See also `stop<class_AnimationPlayer_method_stop>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play**(name: `StringName<class_StringName>`
= &"", custom\_blend: `float<class_float>` = -1, custom\_speed:
`float<class_float>` = 1.0, from\_end: `bool<class_bool>` = false)
`🔗<class_AnimationPlayer_method_play>`

Plays the animation with key `name`. Custom blend times and speed can be
set.

The `from_end` option only affects when switching to a new animation
track, or if the same track but at the start or end. It does not affect
resuming playback that was paused in the middle of an animation. If
`custom_speed` is negative and `from_end` is `true`, the animation will
play backwards (which is equivalent to calling
`play_backwards<class_AnimationPlayer_method_play_backwards>`).

The **AnimationPlayer** keeps track of its current or last played
animation with
`assigned_animation<class_AnimationPlayer_property_assigned_animation>`.
If this method is called with that same animation `name`, or with no
`name` parameter, the assigned animation will resume playing if it was
paused.

\*\*Note:\*\* The animation will be updated the next time the
**AnimationPlayer** is processed. If other variables are updated at the
same time this is called, they may be updated too early. To perform the
update immediately, call `advance(0)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play\_backwards**(name:
`StringName<class_StringName>` = &"", custom\_blend:
`float<class_float>` = -1)
`🔗<class_AnimationPlayer_method_play_backwards>`

Plays the animation with key `name` in reverse.

This method is a shorthand for `play<class_AnimationPlayer_method_play>`
with `custom_speed = -1.0` and `from_end = true`, so see its description
for more information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play\_section**(name:
`StringName<class_StringName>` = &"", start\_time: `float<class_float>`
= -1, end\_time: `float<class_float>` = -1, custom\_blend:
`float<class_float>` = -1, custom\_speed: `float<class_float>` = 1.0,
from\_end: `bool<class_bool>` = false)
`🔗<class_AnimationPlayer_method_play_section>`

Plays the animation with key `name` and the section starting from
`start_time` and ending on `end_time`. See also
`play<class_AnimationPlayer_method_play>`.

Setting `start_time` to a value outside the range of the animation means
the start of the animation will be used instead, and setting `end_time`
to a value outside the range of the animation means the end of the
animation will be used instead. `start_time` cannot be equal to
`end_time`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play\_section\_backwards**(name:
`StringName<class_StringName>` = &"", start\_time: `float<class_float>`
= -1, end\_time: `float<class_float>` = -1, custom\_blend:
`float<class_float>` = -1)
`🔗<class_AnimationPlayer_method_play_section_backwards>`

Plays the animation with key `name` and the section starting from
`start_time` and ending on `end_time` in reverse.

This method is a shorthand for
`play_section<class_AnimationPlayer_method_play_section>` with
`custom_speed = -1.0` and `from_end = true`, see its description for
more information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play\_section\_with\_markers**(name:
`StringName<class_StringName>` = &"", start\_marker:
`StringName<class_StringName>` = &"", end\_marker:
`StringName<class_StringName>` = &"", custom\_blend:
`float<class_float>` = -1, custom\_speed: `float<class_float>` = 1.0,
from\_end: `bool<class_bool>` = false)
`🔗<class_AnimationPlayer_method_play_section_with_markers>`

Plays the animation with key `name` and the section starting from
`start_marker` and ending on `end_marker`.

If the start marker is empty, the section starts from the beginning of
the animation. If the end marker is empty, the section ends on the end
of the animation. See also `play<class_AnimationPlayer_method_play>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**play\_section\_with\_markers\_backwards**(name:
`StringName<class_StringName>` = &"", start\_marker:
`StringName<class_StringName>` = &"", end\_marker:
`StringName<class_StringName>` = &"", custom\_blend:
`float<class_float>` = -1)
`🔗<class_AnimationPlayer_method_play_section_with_markers_backwards>`

Plays the animation with key `name` and the section starting from
`start_marker` and ending on `end_marker` in reverse.

This method is a shorthand for
`play_section_with_markers<class_AnimationPlayer_method_play_section_with_markers>`
with `custom_speed = -1.0` and `from_end = true`, see its description
for more information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play\_with\_capture**(name:
`StringName<class_StringName>` = &"", duration: `float<class_float>` =
-1.0, custom\_blend: `float<class_float>` = -1, custom\_speed:
`float<class_float>` = 1.0, from\_end: `bool<class_bool>` = false,
trans\_type: `TransitionType<enum_Tween_TransitionType>` = 0,
ease\_type: `EaseType<enum_Tween_EaseType>` = 0)
`🔗<class_AnimationPlayer_method_play_with_capture>`

See also `AnimationMixer.capture<class_AnimationMixer_method_capture>`.

You can use this method to use more detailed options for capture than
those performed by
`playback_auto_capture<class_AnimationPlayer_property_playback_auto_capture>`.
When
`playback_auto_capture<class_AnimationPlayer_property_playback_auto_capture>`
is `false`, this method is almost the same as the following:

    capture(name, duration, trans_type, ease_type)
    play(name, custom_blend, custom_speed, from_end)

If `name` is blank, it specifies
`assigned_animation<class_AnimationPlayer_property_assigned_animation>`.

If `duration` is a negative value, the duration is set to the interval
between the current position and the first key, when `from_end` is
`true`, uses the interval between the current position and the last key
instead.

\*\*Note:\*\* The `duration` takes
`speed_scale<class_AnimationPlayer_property_speed_scale>` into account,
but `custom_speed` does not, because the capture cache is interpolated
with the blend result and the result may contain multiple animations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **queue**(name:
`StringName<class_StringName>`) `🔗<class_AnimationPlayer_method_queue>`

Queues an animation for playback once the current animation and all
previously queued animations are done.

\*\*Note:\*\* If a looped animation is currently playing, the queued
animation will never play unless the looped animation is stopped
somehow.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reset\_section**()
`🔗<class_AnimationPlayer_method_reset_section>`

Resets the current section if section is set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **seek**(seconds: `float<class_float>`,
update: `bool<class_bool>` = false, update\_only: `bool<class_bool>` =
false) `🔗<class_AnimationPlayer_method_seek>`

Seeks the animation to the `seconds` point in time (in seconds). If
`update` is `true`, the animation updates too, otherwise it updates at
process time. Events between the current frame and `seconds` are
skipped.

If `update_only` is `true`, the method / audio / animation playback
tracks will not be processed.

\*\*Note:\*\* Seeking to the end of the animation doesn't emit
`AnimationMixer.animation_finished<class_AnimationMixer_signal_animation_finished>`.
If you want to skip animation and emit the signal, use
`AnimationMixer.advance<class_AnimationMixer_method_advance>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_blend\_time**(animation\_from:
`StringName<class_StringName>`, animation\_to:
`StringName<class_StringName>`, sec: `float<class_float>`)
`🔗<class_AnimationPlayer_method_set_blend_time>`

Specifies a blend time (in seconds) between two animations, referenced
by their keys.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_method\_call\_mode**(mode:
`AnimationMethodCallMode<enum_AnimationPlayer_AnimationMethodCallMode>`)
`🔗<class_AnimationPlayer_method_set_method_call_mode>`

**Deprecated:** Use
`AnimationMixer.callback_mode_method<class_AnimationMixer_property_callback_mode_method>`
instead.

Sets the call mode used for "Call Method" tracks.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_process\_callback**(mode:
`AnimationProcessCallback<enum_AnimationPlayer_AnimationProcessCallback>`)
`🔗<class_AnimationPlayer_method_set_process_callback>`

**Deprecated:** Use
`AnimationMixer.callback_mode_process<class_AnimationMixer_property_callback_mode_process>`
instead.

Sets the process notification in which to update animations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_root**(path:
`NodePath<class_NodePath>`) `🔗<class_AnimationPlayer_method_set_root>`

**Deprecated:** Use
`AnimationMixer.root_node<class_AnimationMixer_property_root_node>`
instead.

Sets the node which node path references will travel from.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_section**(start\_time:
`float<class_float>` = -1, end\_time: `float<class_float>` = -1)
`🔗<class_AnimationPlayer_method_set_section>`

Changes the start and end times of the section being played. The current
playback position will be clamped within the new section. See also
`play_section<class_AnimationPlayer_method_play_section>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_section\_with\_markers**(start\_marker:
`StringName<class_StringName>` = &"", end\_marker:
`StringName<class_StringName>` = &"")
`🔗<class_AnimationPlayer_method_set_section_with_markers>`

Changes the start and end markers of the section being played. The
current playback position will be clamped within the new section. See
also
`play_section_with_markers<class_AnimationPlayer_method_play_section_with_markers>`.

If the argument is empty, the section uses the beginning or end of the
animation. If both are empty, it means that the section is not set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop**(keep\_state: `bool<class_bool>` =
false) `🔗<class_AnimationPlayer_method_stop>`

Stops the currently playing animation. The animation position is reset
to `0` and the `custom_speed` is reset to `1.0`. See also
`pause<class_AnimationPlayer_method_pause>`.

If `keep_state` is `true`, the animation state is not updated visually.

\*\*Note:\*\* The method / audio / animation playback tracks will not be
processed by this method.
