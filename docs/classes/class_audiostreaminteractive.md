github\_url  
hide

# AudioStreamInteractive

**Inherits:** `AudioStream<class_AudioStream>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Audio stream that can playback music interactively, combining clips and
a transition table.

classref-introduction-group

## Description

This is an audio stream that can playback music interactively, combining
clips and a transition table. Clips must be added first, and then the
transition rules via the
`add_transition<class_AudioStreamInteractive_method_add_transition>`.
Additionally, this stream exports a property parameter to control the
playback via `AudioStreamPlayer<class_AudioStreamPlayer>`,
`AudioStreamPlayer2D<class_AudioStreamPlayer2D>`, or
`AudioStreamPlayer3D<class_AudioStreamPlayer3D>`.

The way this is used is by filling a number of clips, then configuring
the transition table. From there, clips are selected for playback and
the music will smoothly go from the current to the new one while using
the corresponding transition rule defined in the transition table.

classref-reftable-group

## Properties

<table>
<tbody>
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **TransitionFromTime**:
`🔗<enum_AudioStreamInteractive_TransitionFromTime>`

classref-enumeration-constant

`TransitionFromTime<enum_AudioStreamInteractive_TransitionFromTime>`
**TRANSITION\_FROM\_TIME\_IMMEDIATE** = `0`

Start transition as soon as possible, don't wait for any specific time
position.

classref-enumeration-constant

`TransitionFromTime<enum_AudioStreamInteractive_TransitionFromTime>`
**TRANSITION\_FROM\_TIME\_NEXT\_BEAT** = `1`

Transition when the clip playback position reaches the next beat.

classref-enumeration-constant

`TransitionFromTime<enum_AudioStreamInteractive_TransitionFromTime>`
**TRANSITION\_FROM\_TIME\_NEXT\_BAR** = `2`

Transition when the clip playback position reaches the next bar.

classref-enumeration-constant

`TransitionFromTime<enum_AudioStreamInteractive_TransitionFromTime>`
**TRANSITION\_FROM\_TIME\_END** = `3`

Transition when the current clip finished playing.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TransitionToTime**:
`🔗<enum_AudioStreamInteractive_TransitionToTime>`

classref-enumeration-constant

`TransitionToTime<enum_AudioStreamInteractive_TransitionToTime>`
**TRANSITION\_TO\_TIME\_SAME\_POSITION** = `0`

Transition to the same position in the destination clip. This is useful
when both clips have exactly the same length and the music should fade
between them.

classref-enumeration-constant

`TransitionToTime<enum_AudioStreamInteractive_TransitionToTime>`
**TRANSITION\_TO\_TIME\_START** = `1`

Transition to the start of the destination clip.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **FadeMode**: `🔗<enum_AudioStreamInteractive_FadeMode>`

classref-enumeration-constant

`FadeMode<enum_AudioStreamInteractive_FadeMode>` **FADE\_DISABLED** =
`0`

Do not use fade for the transition. This is useful when transitioning
from a clip-end to clip-beginning, and each clip has their begin/end.

classref-enumeration-constant

`FadeMode<enum_AudioStreamInteractive_FadeMode>` **FADE\_IN** = `1`

Use a fade-in in the next clip, let the current clip finish.

classref-enumeration-constant

`FadeMode<enum_AudioStreamInteractive_FadeMode>` **FADE\_OUT** = `2`

Use a fade-out in the current clip, the next clip will start by itself.

classref-enumeration-constant

`FadeMode<enum_AudioStreamInteractive_FadeMode>` **FADE\_CROSS** = `3`

Use a cross-fade between clips.

classref-enumeration-constant

`FadeMode<enum_AudioStreamInteractive_FadeMode>` **FADE\_AUTOMATIC** =
`4`

Use automatic fade logic depending on the transition from/to. It is
recommended to use this by default.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AutoAdvanceMode**:
`🔗<enum_AudioStreamInteractive_AutoAdvanceMode>`

classref-enumeration-constant

`AutoAdvanceMode<enum_AudioStreamInteractive_AutoAdvanceMode>`
**AUTO\_ADVANCE\_DISABLED** = `0`

Disable auto-advance (default).

classref-enumeration-constant

`AutoAdvanceMode<enum_AudioStreamInteractive_AutoAdvanceMode>`
**AUTO\_ADVANCE\_ENABLED** = `1`

Enable auto-advance, a clip must be specified.

classref-enumeration-constant

`AutoAdvanceMode<enum_AudioStreamInteractive_AutoAdvanceMode>`
**AUTO\_ADVANCE\_RETURN\_TO\_HOLD** = `2`

Enable auto-advance, but instead of specifying a clip, the playback will
return to hold (see
`add_transition<class_AudioStreamInteractive_method_add_transition>`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**CLIP\_ANY** = `-1`
`🔗<class_AudioStreamInteractive_constant_CLIP_ANY>`

This constant describes that any clip is valid for a specific transition
as either source or destination.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **clip\_count** = `0`
`🔗<class_AudioStreamInteractive_property_clip_count>`

classref-property-setget

-   `void (No return value.)` **set\_clip\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_clip\_count**()

Amount of clips contained in this interactive player.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **initial\_clip** = `0`
`🔗<class_AudioStreamInteractive_property_initial_clip>`

classref-property-setget

-   `void (No return value.)` **set\_initial\_clip**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_initial\_clip**()

Index of the initial clip, which will be played first when this stream
is played.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_transition**(from\_clip:
`int<class_int>`, to\_clip: `int<class_int>`, from\_time:
`TransitionFromTime<enum_AudioStreamInteractive_TransitionFromTime>`,
to\_time:
`TransitionToTime<enum_AudioStreamInteractive_TransitionToTime>`,
fade\_mode: `FadeMode<enum_AudioStreamInteractive_FadeMode>`,
fade\_beats: `float<class_float>`, use\_filler\_clip: `bool<class_bool>`
= false, filler\_clip: `int<class_int>` = -1, hold\_previous:
`bool<class_bool>` = false)
`🔗<class_AudioStreamInteractive_method_add_transition>`

Add a transition between two clips. Provide the indices of the source
and destination clips, or use the
`CLIP_ANY<class_AudioStreamInteractive_constant_CLIP_ANY>` constant to
indicate that transition happens to/from any clip to this one.

\* `from_time` indicates the moment in the current clip the transition
will begin after triggered.

\* `to_time` indicates the time in the next clip that the playback will
start from.

\* `fade_mode` indicates how the fade will happen between clips. If
unsure, just use
`FADE_AUTOMATIC<class_AudioStreamInteractive_constant_FADE_AUTOMATIC>`
which uses the most common type of fade for each situation.

\* `fade_beats` indicates how many beats the fade will take. Using
decimals is allowed.

\* `use_filler_clip` indicates that there will be a filler clip used
between the source and destination clips.

\* `filler_clip` the index of the filler clip.

\* If `hold_previous` is used, then this clip will be remembered. This
can be used together with
`AUTO_ADVANCE_RETURN_TO_HOLD<class_AudioStreamInteractive_constant_AUTO_ADVANCE_RETURN_TO_HOLD>`
to return to this clip after another is done playing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase\_transition**(from\_clip:
`int<class_int>`, to\_clip: `int<class_int>`)
`🔗<class_AudioStreamInteractive_method_erase_transition>`

Erase a transition by providing `from_clip` and `to_clip` clip indices.
`CLIP_ANY<class_AudioStreamInteractive_constant_CLIP_ANY>` can be used
for either argument or both.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AutoAdvanceMode<enum_AudioStreamInteractive_AutoAdvanceMode>`
**get\_clip\_auto\_advance**(clip\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_get_clip_auto_advance>`

Return whether a clip has auto-advance enabled. See
`set_clip_auto_advance<class_AudioStreamInteractive_method_set_clip_auto_advance>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_clip\_auto\_advance\_next\_clip**(clip\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_get_clip_auto_advance_next_clip>`

Return the clip towards which the clip referenced by `clip_index` will
auto-advance to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_clip\_name**(clip\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_get_clip_name>`

Return the name of a clip.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioStream<class_AudioStream>` **get\_clip\_stream**(clip\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_get_clip_stream>`

Return the `AudioStream<class_AudioStream>` associated with a clip.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_transition\_fade\_beats**(from\_clip:
`int<class_int>`, to\_clip: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_get_transition_fade_beats>`

Return the time (in beats) for a transition (see
`add_transition<class_AudioStreamInteractive_method_add_transition>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`FadeMode<enum_AudioStreamInteractive_FadeMode>`
**get\_transition\_fade\_mode**(from\_clip: `int<class_int>`, to\_clip:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_get_transition_fade_mode>`

Return the mode for a transition (see
`add_transition<class_AudioStreamInteractive_method_add_transition>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_transition\_filler\_clip**(from\_clip:
`int<class_int>`, to\_clip: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_get_transition_filler_clip>`

Return the filler clip for a transition (see
`add_transition<class_AudioStreamInteractive_method_add_transition>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`TransitionFromTime<enum_AudioStreamInteractive_TransitionFromTime>`
**get\_transition\_from\_time**(from\_clip: `int<class_int>`, to\_clip:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_get_transition_from_time>`

Return the source time position for a transition (see
`add_transition<class_AudioStreamInteractive_method_add_transition>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>` **get\_transition\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_get_transition_list>`

Return the list of transitions (from, to interleaved).

classref-item-separator

------------------------------------------------------------------------

classref-method

`TransitionToTime<enum_AudioStreamInteractive_TransitionToTime>`
**get\_transition\_to\_time**(from\_clip: `int<class_int>`, to\_clip:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_get_transition_to_time>`

Return the destination time position for a transition (see
`add_transition<class_AudioStreamInteractive_method_add_transition>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_transition**(from\_clip: `int<class_int>`,
to\_clip: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_has_transition>`

Return true if a given transition exists (was added via
`add_transition<class_AudioStreamInteractive_method_add_transition>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_transition\_holding\_previous**(from\_clip:
`int<class_int>`, to\_clip: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_is_transition_holding_previous>`

Return whether a transition uses the *hold previous* functionality (see
`add_transition<class_AudioStreamInteractive_method_add_transition>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_transition\_using\_filler\_clip**(from\_clip:
`int<class_int>`, to\_clip: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamInteractive_method_is_transition_using_filler_clip>`

Return whether a transition uses the *filler clip* functionality (see
`add_transition<class_AudioStreamInteractive_method_add_transition>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_clip\_auto\_advance**(clip\_index:
`int<class_int>`, mode:
`AutoAdvanceMode<enum_AudioStreamInteractive_AutoAdvanceMode>`)
`🔗<class_AudioStreamInteractive_method_set_clip_auto_advance>`

Set whether a clip will auto-advance by changing the auto-advance mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_clip\_auto\_advance\_next\_clip**(clip\_index: `int<class_int>`,
auto\_advance\_next\_clip: `int<class_int>`)
`🔗<class_AudioStreamInteractive_method_set_clip_auto_advance_next_clip>`

Set the index of the next clip towards which this clip will auto advance
to when finished. If the clip being played loops, then auto-advance will
be ignored.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_clip\_name**(clip\_index:
`int<class_int>`, name: `StringName<class_StringName>`)
`🔗<class_AudioStreamInteractive_method_set_clip_name>`

Set the name of the current clip (for easier identification).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_clip\_stream**(clip\_index:
`int<class_int>`, stream: `AudioStream<class_AudioStream>`)
`🔗<class_AudioStreamInteractive_method_set_clip_stream>`

Set the `AudioStream<class_AudioStream>` associated with the current
clip.
