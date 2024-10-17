github\_url  
hide

# AudioStreamPlayer3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

Plays positional sound in 3D space.

classref-introduction-group

## Description

Plays audio with positional sound effects, based on the relative
position of the audio listener. Positional effects include distance
attenuation, directionality, and the Doppler effect. For greater
realism, a low-pass filter is applied to distant sounds. This can be
disabled by setting
`attenuation_filter_cutoff_hz<class_AudioStreamPlayer3D_property_attenuation_filter_cutoff_hz>`
to `20500`.

By default, audio is heard from the camera position. This can be changed
by adding an `AudioListener3D<class_AudioListener3D>` node to the scene
and enabling it by calling
`AudioListener3D.make_current<class_AudioListener3D_method_make_current>`
on it.

See also `AudioStreamPlayer<class_AudioStreamPlayer>` to play a sound
non-positionally.

\*\*Note:\*\* Hiding an **AudioStreamPlayer3D** node does not disable
its audio output. To temporarily disable an **AudioStreamPlayer3D**'s
audio output, set
`volume_db<class_AudioStreamPlayer3D_property_volume_db>` to a very low
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

**finished**() `🔗<class_AudioStreamPlayer3D_signal_finished>`

Emitted when the audio stops playing.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **AttenuationModel**:
`🔗<enum_AudioStreamPlayer3D_AttenuationModel>`

classref-enumeration-constant

`AttenuationModel<enum_AudioStreamPlayer3D_AttenuationModel>`
**ATTENUATION\_INVERSE\_DISTANCE** = `0`

Attenuation of loudness according to linear distance.

classref-enumeration-constant

`AttenuationModel<enum_AudioStreamPlayer3D_AttenuationModel>`
**ATTENUATION\_INVERSE\_SQUARE\_DISTANCE** = `1`

Attenuation of loudness according to squared distance.

classref-enumeration-constant

`AttenuationModel<enum_AudioStreamPlayer3D_AttenuationModel>`
**ATTENUATION\_LOGARITHMIC** = `2`

Attenuation of loudness according to logarithmic distance.

classref-enumeration-constant

`AttenuationModel<enum_AudioStreamPlayer3D_AttenuationModel>`
**ATTENUATION\_DISABLED** = `3`

No attenuation of loudness according to distance. The sound will still
be heard positionally, unlike an
`AudioStreamPlayer<class_AudioStreamPlayer>`.
`ATTENUATION_DISABLED<class_AudioStreamPlayer3D_constant_ATTENUATION_DISABLED>`
can be combined with a
`max_distance<class_AudioStreamPlayer3D_property_max_distance>` value
greater than `0.0` to achieve linear attenuation clamped to a sphere of
a defined size.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DopplerTracking**: `🔗<enum_AudioStreamPlayer3D_DopplerTracking>`

classref-enumeration-constant

`DopplerTracking<enum_AudioStreamPlayer3D_DopplerTracking>`
**DOPPLER\_TRACKING\_DISABLED** = `0`

Disables doppler tracking.

classref-enumeration-constant

`DopplerTracking<enum_AudioStreamPlayer3D_DopplerTracking>`
**DOPPLER\_TRACKING\_IDLE\_STEP** = `1`

Executes doppler tracking during process frames (see
`Node.NOTIFICATION_INTERNAL_PROCESS<class_Node_constant_NOTIFICATION_INTERNAL_PROCESS>`).

classref-enumeration-constant

`DopplerTracking<enum_AudioStreamPlayer3D_DopplerTracking>`
**DOPPLER\_TRACKING\_PHYSICS\_STEP** = `2`

Executes doppler tracking during physics frames (see
`Node.NOTIFICATION_INTERNAL_PHYSICS_PROCESS<class_Node_constant_NOTIFICATION_INTERNAL_PHYSICS_PROCESS>`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **area\_mask** = `1`
`🔗<class_AudioStreamPlayer3D_property_area_mask>`

classref-property-setget

-   `void (No return value.)` **set\_area\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_area\_mask**()

Determines which `Area3D<class_Area3D>` layers affect the sound for
reverb and audio bus effects. Areas can be used to redirect
`AudioStream<class_AudioStream>`s so that they play in a certain audio
bus. An example of how you might use this is making a "water" area so
that sounds played in the water are redirected through an audio bus to
make them sound like they are being played underwater.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **attenuation\_filter\_cutoff\_hz** = `5000.0`
`🔗<class_AudioStreamPlayer3D_property_attenuation_filter_cutoff_hz>`

classref-property-setget

-   `void (No return value.)`
    **set\_attenuation\_filter\_cutoff\_hz**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_attenuation\_filter\_cutoff\_hz**()

The cutoff frequency of the attenuation low-pass filter, in Hz. A sound
above this frequency is attenuated more than a sound below this
frequency. To disable this effect, set this to `20500` as this frequency
is above the human hearing limit.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **attenuation\_filter\_db** = `-24.0`
`🔗<class_AudioStreamPlayer3D_property_attenuation_filter_db>`

classref-property-setget

-   `void (No return value.)` **set\_attenuation\_filter\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_attenuation\_filter\_db**()

Amount how much the filter affects the loudness, in decibels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AttenuationModel<enum_AudioStreamPlayer3D_AttenuationModel>`
**attenuation\_model** = `0`
`🔗<class_AudioStreamPlayer3D_property_attenuation_model>`

classref-property-setget

-   `void (No return value.)` **set\_attenuation\_model**(value:
    `AttenuationModel<enum_AudioStreamPlayer3D_AttenuationModel>`)
-   `AttenuationModel<enum_AudioStreamPlayer3D_AttenuationModel>`
    **get\_attenuation\_model**()

Decides if audio should get quieter with distance linearly,
quadratically, logarithmically, or not be affected by distance,
effectively disabling attenuation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **autoplay** = `false`
`🔗<class_AudioStreamPlayer3D_property_autoplay>`

classref-property-setget

-   `void (No return value.)` **set\_autoplay**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_autoplay\_enabled**()

If `true`, audio plays when the AudioStreamPlayer3D node is added to
scene tree.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **bus** = `&"Master"`
`🔗<class_AudioStreamPlayer3D_property_bus>`

classref-property-setget

-   `void (No return value.)` **set\_bus**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_bus**()

The bus on which this audio is playing.

\*\*Note:\*\* When setting this property, keep in mind that no
validation is performed to see if the given name matches an existing
bus. This is because audio bus layouts might be loaded after this
property is set. If this given name can't be resolved at runtime, it
will fall back to `"Master"`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DopplerTracking<enum_AudioStreamPlayer3D_DopplerTracking>`
**doppler\_tracking** = `0`
`🔗<class_AudioStreamPlayer3D_property_doppler_tracking>`

classref-property-setget

-   `void (No return value.)` **set\_doppler\_tracking**(value:
    `DopplerTracking<enum_AudioStreamPlayer3D_DopplerTracking>`)
-   `DopplerTracking<enum_AudioStreamPlayer3D_DopplerTracking>`
    **get\_doppler\_tracking**()

Decides in which step the Doppler effect should be calculated.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **emission\_angle\_degrees** = `45.0`
`🔗<class_AudioStreamPlayer3D_property_emission_angle_degrees>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_angle**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_emission\_angle**()

The angle in which the audio reaches a listener unattenuated.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **emission\_angle\_enabled** = `false`
`🔗<class_AudioStreamPlayer3D_property_emission_angle_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_angle\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_emission\_angle\_enabled**()

If `true`, the audio should be attenuated according to the direction of
the sound.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **emission\_angle\_filter\_attenuation\_db** =
`-12.0`
`🔗<class_AudioStreamPlayer3D_property_emission_angle_filter_attenuation_db>`

classref-property-setget

-   `void (No return value.)`
    **set\_emission\_angle\_filter\_attenuation\_db**(value:
    `float<class_float>`)
-   `float<class_float>`
    **get\_emission\_angle\_filter\_attenuation\_db**()

Attenuation factor used if listener is outside of
`emission_angle_degrees<class_AudioStreamPlayer3D_property_emission_angle_degrees>`
and
`emission_angle_enabled<class_AudioStreamPlayer3D_property_emission_angle_enabled>`
is set, in decibels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **max\_db** = `3.0`
`🔗<class_AudioStreamPlayer3D_property_max_db>`

classref-property-setget

-   `void (No return value.)` **set\_max\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_max\_db**()

Sets the absolute maximum of the sound level, in decibels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **max\_distance** = `0.0`
`🔗<class_AudioStreamPlayer3D_property_max_distance>`

classref-property-setget

-   `void (No return value.)` **set\_max\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_max\_distance**()

The distance past which the sound can no longer be heard at all. Only
has an effect if set to a value greater than `0.0`.
`max_distance<class_AudioStreamPlayer3D_property_max_distance>` works in
tandem with `unit_size<class_AudioStreamPlayer3D_property_unit_size>`.
However, unlike
`unit_size<class_AudioStreamPlayer3D_property_unit_size>` whose behavior
depends on the
`attenuation_model<class_AudioStreamPlayer3D_property_attenuation_model>`,
`max_distance<class_AudioStreamPlayer3D_property_max_distance>` always
works in a linear fashion. This can be used to prevent the
**AudioStreamPlayer3D** from requiring audio mixing when the listener is
far away, which saves CPU resources.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_polyphony** = `1`
`🔗<class_AudioStreamPlayer3D_property_max_polyphony>`

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
`🔗<class_AudioStreamPlayer3D_property_panning_strength>`

classref-property-setget

-   `void (No return value.)` **set\_panning\_strength**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_panning\_strength**()

Scales the panning strength for this node by multiplying the base
`ProjectSettings.audio/general/3d_panning_strength<class_ProjectSettings_property_audio/general/3d_panning_strength>`
with this factor. Higher values will pan audio from left to right more
dramatically than lower values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pitch\_scale** = `1.0`
`🔗<class_AudioStreamPlayer3D_property_pitch_scale>`

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
`🔗<class_AudioStreamPlayer3D_property_playback_type>`

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
`🔗<class_AudioStreamPlayer3D_property_playing>`

classref-property-setget

-   `void (No return value.)` **set\_playing**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_playing**()

If `true`, audio is playing or is queued to be played (see
`play<class_AudioStreamPlayer3D_method_play>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`AudioStream<class_AudioStream>` **stream**
`🔗<class_AudioStreamPlayer3D_property_stream>`

classref-property-setget

-   `void (No return value.)` **set\_stream**(value:
    `AudioStream<class_AudioStream>`)
-   `AudioStream<class_AudioStream>` **get\_stream**()

The `AudioStream<class_AudioStream>` resource to be played.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **stream\_paused** = `false`
`🔗<class_AudioStreamPlayer3D_property_stream_paused>`

classref-property-setget

-   `void (No return value.)` **set\_stream\_paused**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_stream\_paused**()

If `true`, the playback is paused. You can resume it by setting
`stream_paused<class_AudioStreamPlayer3D_property_stream_paused>` to
`false`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **unit\_size** = `10.0`
`🔗<class_AudioStreamPlayer3D_property_unit_size>`

classref-property-setget

-   `void (No return value.)` **set\_unit\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_unit\_size**()

The factor for the attenuation effect. Higher values make the sound
audible over a larger distance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **volume\_db** = `0.0`
`🔗<class_AudioStreamPlayer3D_property_volume_db>`

classref-property-setget

-   `void (No return value.)` **set\_volume\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_volume\_db**()

The base sound level before attenuation, in decibels.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_playback\_position**()
`🔗<class_AudioStreamPlayer3D_method_get_playback_position>`

Returns the position in the `AudioStream<class_AudioStream>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioStreamPlayback<class_AudioStreamPlayback>`
**get\_stream\_playback**()
`🔗<class_AudioStreamPlayer3D_method_get_stream_playback>`

Returns the `AudioStreamPlayback<class_AudioStreamPlayback>` object
associated with this **AudioStreamPlayer3D**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_stream\_playback**()
`🔗<class_AudioStreamPlayer3D_method_has_stream_playback>`

Returns whether the `AudioStreamPlayer<class_AudioStreamPlayer>` can
return the `AudioStreamPlayback<class_AudioStreamPlayback>` object or
not.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **play**(from\_position: `float<class_float>`
= 0.0) `🔗<class_AudioStreamPlayer3D_method_play>`

Queues the audio to play on the next physics frame, from the given
position `from_position`, in seconds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **seek**(to\_position: `float<class_float>`)
`🔗<class_AudioStreamPlayer3D_method_seek>`

Sets the position from which audio will be played, in seconds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop**()
`🔗<class_AudioStreamPlayer3D_method_stop>`

Stops the audio.
