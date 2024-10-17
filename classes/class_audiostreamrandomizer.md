github\_url  
hide

# AudioStreamRandomizer

**Inherits:** `AudioStream<class_AudioStream>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Wraps a pool of audio streams with pitch and volume shifting.

classref-introduction-group

## Description

Picks a random AudioStream from the pool, depending on the playback
mode, and applies random pitch shifting and volume shifting during
playback.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **PlaybackMode**: `🔗<enum_AudioStreamRandomizer_PlaybackMode>`

classref-enumeration-constant

`PlaybackMode<enum_AudioStreamRandomizer_PlaybackMode>`
**PLAYBACK\_RANDOM\_NO\_REPEATS** = `0`

Pick a stream at random according to the probability weights chosen for
each stream, but avoid playing the same stream twice in a row whenever
possible. If only 1 sound is present in the pool, the same sound will
always play, effectively allowing repeats to occur.

classref-enumeration-constant

`PlaybackMode<enum_AudioStreamRandomizer_PlaybackMode>`
**PLAYBACK\_RANDOM** = `1`

Pick a stream at random according to the probability weights chosen for
each stream. If only 1 sound is present in the pool, the same sound will
always play.

classref-enumeration-constant

`PlaybackMode<enum_AudioStreamRandomizer_PlaybackMode>`
**PLAYBACK\_SEQUENTIAL** = `2`

Play streams in the order they appear in the stream pool. If only 1
sound is present in the pool, the same sound will always play.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`PlaybackMode<enum_AudioStreamRandomizer_PlaybackMode>`
**playback\_mode** = `0`
`🔗<class_AudioStreamRandomizer_property_playback_mode>`

classref-property-setget

-   `void (No return value.)` **set\_playback\_mode**(value:
    `PlaybackMode<enum_AudioStreamRandomizer_PlaybackMode>`)
-   `PlaybackMode<enum_AudioStreamRandomizer_PlaybackMode>`
    **get\_playback\_mode**()

Controls how this AudioStreamRandomizer picks which AudioStream to play
next.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **random\_pitch** = `1.0`
`🔗<class_AudioStreamRandomizer_property_random_pitch>`

classref-property-setget

-   `void (No return value.)` **set\_random\_pitch**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_random\_pitch**()

The intensity of random pitch variation. A value of 1 means no
variation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **random\_volume\_offset\_db** = `0.0`
`🔗<class_AudioStreamRandomizer_property_random_volume_offset_db>`

classref-property-setget

-   `void (No return value.)` **set\_random\_volume\_offset\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_random\_volume\_offset\_db**()

The intensity of random volume variation. A value of 0 means no
variation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **streams\_count** = `0`
`🔗<class_AudioStreamRandomizer_property_streams_count>`

classref-property-setget

-   `void (No return value.)` **set\_streams\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_streams\_count**()

The number of streams in the stream pool.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_stream**(index: `int<class_int>`,
stream: `AudioStream<class_AudioStream>`, weight: `float<class_float>` =
1.0) `🔗<class_AudioStreamRandomizer_method_add_stream>`

Insert a stream at the specified index. If the index is less than zero,
the insertion occurs at the end of the underlying pool.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioStream<class_AudioStream>` **get\_stream**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamRandomizer_method_get_stream>`

Returns the stream at the specified index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_stream\_probability\_weight**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamRandomizer_method_get_stream_probability_weight>`

Returns the probability weight associated with the stream at the given
index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_stream**(index\_from:
`int<class_int>`, index\_to: `int<class_int>`)
`🔗<class_AudioStreamRandomizer_method_move_stream>`

Move a stream from one index to another.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_stream**(index: `int<class_int>`)
`🔗<class_AudioStreamRandomizer_method_remove_stream>`

Remove the stream at the specified index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_stream**(index: `int<class_int>`,
stream: `AudioStream<class_AudioStream>`)
`🔗<class_AudioStreamRandomizer_method_set_stream>`

Set the AudioStream at the specified index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_stream\_probability\_weight**(index:
`int<class_int>`, weight: `float<class_float>`)
`🔗<class_AudioStreamRandomizer_method_set_stream_probability_weight>`

Set the probability weight of the stream at the specified index. The
higher this value, the more likely that the randomizer will choose this
stream during random playback modes.
