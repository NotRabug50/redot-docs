github\_url  
hide

# AudioStreamPlayer2D

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Plays positional sound in 2D space.

classref-introduction-group

## Description

Plays audio that is attenuated with distance to the listener.

By default, audio is heard from the screen center. This can be changed
by adding an `AudioListener2D<class_AudioListener2D>` node to the scene
and enabling it by calling
`AudioListener2D.make_current<class_AudioListener2D_method_make_current>`
on it.

See also `AudioStreamPlayer<class_AudioStreamPlayer>` to play a sound
non-positionally.

\*\*Note:\*\* Hiding an **AudioStreamPlayer2D** node does not disable
its audio output. To temporarily disable an **AudioStreamPlayer2D**'s
audio output, set
`volume_db<class_AudioStreamPlayer2D_property_volume_db>` to a very low
value like `-100` (which isn't audible to human hearing).

classref-introduction-group

## Tutorials

-   `Audio streams <../tutorials/audio/audio_streams>`

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

## Signals

classref-signal

**finished**() `🔗<class_AudioStreamPlayer2D_signal_finished>`

Emitted when the audio stops playing.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **area\_mask** = `1`
`🔗<class_AudioStreamPlayer2D_property_area_mask>`

classref-property-setget

-   `void (No return value.)` **set\_area\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_area\_mask**()

Determines which `Area2D<class_Area2D>` layers affect the sound for
reverb and audio bus effects. Areas can be used to redirect
`AudioStream<class_AudioStream>`s so that they play in a certain audio
bus. An example of how you might use this is making a "water" area so
that sounds played in the water are redirected through an audio bus to
make them sound like they are being played underwater.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **attenuation** = `1.0`
`🔗<class_AudioStreamPlayer2D_property_attenuation>`

classref-property-setget

-   `void (No return value.)` **set\_attenuation**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_attenuation**()

The volume is attenuated over distance with this as an exponent.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **autoplay** = `false`
`🔗<class_AudioStreamPlayer2D_property_autoplay>`

classref-property-setget

-   `void (No return value.)` **set\_autoplay**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_autoplay\_enabled**()

If `true`, audio plays when added to scene tree.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **bus** = `&"Master"`
`🔗<class_AudioStreamPlayer2D_property_bus>`

classref-property-setget

-   `void (No return value.)` **set\_bus**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_bus**()

Bus on which this audio is playing.

\*\*Note:\*\* When setting this property, keep in mind that no
validation is performed to see if the given name matches an existing
bus. This is because audio bus layouts might be loaded after this
property is set. If this given name can't be resolved at runtime, it
will fall back to `"Master"`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **max\_distance** = `2000.0`
`🔗<class_AudioStreamPlayer2D_property_max_distance>`

classref-property-setget

-   `void (No return value.)` **set\_max\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_max\_distance**()

Maximum distance from which audio is still hearable.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_polyphony** = `1`
`🔗<class_AudioStreamPlayer2D_property_max_polyphony>`

classref-property-setget

-   `void (No return value.)` **set\_max\_polyphony**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_polyphony**()

The maximum number of sounds this node can play at the same time.
Playing additional sounds after this value is reached will cut off the
oldest sounds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **panning\_strength** = `1.0`
`🔗<class_AudioStreamPlayer2D_property_panning_strength>`

classref-property-setget

-   `void (No return value.)` **set\_panning\_strength**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_panning\_strength**()

Scales the panning strength for this node by multiplying the base
`ProjectSettings.audio/general/2d_panning_strength<class_ProjectSettings_property_audio/general/2d_panning_strength>`
with this factor. Higher values will pan audio from left to right more
dramatically than lower values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pitch\_scale** = `1.0`
`🔗<class_AudioStreamPlayer2D_property_pitch_scale>`

classref-property-setget

-   `void (No return value.)` **set\_pitch\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pitch\_scale**()

The pitch and the tempo of the audio, as a multiplier of the audio
sample's sample rate.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PlaybackType<enum_AudioServer_PlaybackType>` **playback\_type** = `0`
`🔗<class_AudioStreamPlayer2D_property_playback_type>`

classref-property-setget

-   `void (No return value.)` **set\_playback\_type**(value:
    `PlaybackType<enum_AudioServer_PlaybackType>`)
-   `PlaybackType<enum_AudioServer_PlaybackType>`
    **get\_playback\_type**()

**Experimental:** This property may be changed or removed in future
versions.

The playback type of the stream player. If set other than to the default
value, it will force that playback type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **playing** = `false`
`🔗<class_AudioStreamPlayer2D_property_playing>`

classref-property-setget

-   `void (No return value.)` **set\_playing**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_playing**()

If `true`, audio is playing or is queued to be played (see
`play<class_AudioStreamPlayer2D_method_play>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`AudioStream<class_AudioStream>` **stream**
`🔗<class_AudioStreamPlayer2D_property_stream>`

classref-property-setget

-   `void (No return value.)` **set\_stream**(value:
    `AudioStream<class_AudioStream>`)
-   `AudioStream<class_AudioStream>` **get\_stream**()

The `AudioStream<class_AudioStream>` object to be played.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **stream\_paused** = `false`
`🔗<class_AudioStreamPlayer2D_property_stream_paused>`

classref-property-setget

-   `void (No return value.)` **set\_stream\_paused**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_stream\_paused**()

If `true`, the playback is paused. You can resume it by setting
`stream_paused<class_AudioStreamPlayer2D_property_stream_paused>` to
`false`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volume\_db** = `0.0`
`🔗<class_AudioStreamPlayer2D_property_volume_db>`

classref-property-setget

-   `void (No return value.)` **set\_volume\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_volume\_db**()

Base volume before attenuation.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_playback\_position**()
`🔗<class_AudioStreamPlayer2D_method_get_playback_position>`

Returns the position in the `AudioStream<class_AudioStream>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioStreamPlayback<class_AudioStreamPlayback>`
**get\_stream\_playback**()
`🔗<class_AudioStreamPlayer2D_method_get_stream_playback>`

Returns the `AudioStreamPlayback<class_AudioStreamPlayback>` object
associated with this **AudioStreamPlayer2D**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_stream\_playback**()
`🔗<class_AudioStreamPlayer2D_method_has_stream_playback>`

Returns whether the `AudioStreamPlayer<class_AudioStreamPlayer>` can
return the `AudioStreamPlayback<class_AudioStreamPlayback>` object or
not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play**(from\_position: `float<class_float>`
= 0.0) `🔗<class_AudioStreamPlayer2D_method_play>`

Queues the audio to play on the next physics frame, from the given
position `from_position`, in seconds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **seek**(to\_position: `float<class_float>`)
`🔗<class_AudioStreamPlayer2D_method_seek>`

Sets the position from which audio will be played, in seconds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop**()
`🔗<class_AudioStreamPlayer2D_method_stop>`

Stops the audio.
