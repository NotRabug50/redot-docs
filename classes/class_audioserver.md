github\_url  
hide

# AudioServer

**Inherits:** `Object<class_Object>`

Server interface for low-level audio access.

classref-introduction-group

## Description

**AudioServer** is a low-level server interface for audio access. It is
in charge of creating sample data (playable audio) as well as its
playback via a voice interface.

classref-introduction-group

## Tutorials

-   `Audio buses <../tutorials/audio/audio_buses>`
-   [Audio Device Changer
    Demo](https://godotengine.org/asset-library/asset/2758)
-   [Audio Microphone Record
    Demo](https://godotengine.org/asset-library/asset/2760)
-   [Audio Spectrum Visualizer
    Demo](https://godotengine.org/asset-library/asset/2762)

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

**bus\_layout\_changed**()
`🔗<class_AudioServer_signal_bus_layout_changed>`

Emitted when an audio bus is added, deleted, or moved.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**bus\_renamed**(bus\_index: `int<class_int>`, old\_name:
`StringName<class_StringName>`, new\_name:
`StringName<class_StringName>`)
`🔗<class_AudioServer_signal_bus_renamed>`

Emitted when the audio bus at `bus_index` is renamed from `old_name` to
`new_name`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **SpeakerMode**: `🔗<enum_AudioServer_SpeakerMode>`

classref-enumeration-constant

`SpeakerMode<enum_AudioServer_SpeakerMode>` **SPEAKER\_MODE\_STEREO** =
`0`

Two or fewer speakers were detected.

classref-enumeration-constant

`SpeakerMode<enum_AudioServer_SpeakerMode>` **SPEAKER\_SURROUND\_31** =
`1`

A 3.1 channel surround setup was detected.

classref-enumeration-constant

`SpeakerMode<enum_AudioServer_SpeakerMode>` **SPEAKER\_SURROUND\_51** =
`2`

A 5.1 channel surround setup was detected.

classref-enumeration-constant

`SpeakerMode<enum_AudioServer_SpeakerMode>` **SPEAKER\_SURROUND\_71** =
`3`

A 7.1 channel surround setup was detected.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PlaybackType**: `🔗<enum_AudioServer_PlaybackType>`

classref-enumeration-constant

`PlaybackType<enum_AudioServer_PlaybackType>`
**PLAYBACK\_TYPE\_DEFAULT** = `0`

**Experimental:** This constant may be changed or removed in future
versions.

The playback will be considered of the type declared at
`ProjectSettings.audio/general/default_playback_type<class_ProjectSettings_property_audio/general/default_playback_type>`.

classref-enumeration-constant

`PlaybackType<enum_AudioServer_PlaybackType>` **PLAYBACK\_TYPE\_STREAM**
= `1`

**Experimental:** This constant may be changed or removed in future
versions.

Force the playback to be considered as a stream.

classref-enumeration-constant

`PlaybackType<enum_AudioServer_PlaybackType>` **PLAYBACK\_TYPE\_SAMPLE**
= `2`

**Experimental:** This constant may be changed or removed in future
versions.

Force the playback to be considered as a sample. This can provide lower
latency and more stable playback (with less risk of audio crackling), at
the cost of having less flexibility.

\*\*Note:\*\* Only currently supported on the web platform.

\*\*Note:\*\* `AudioEffect<class_AudioEffect>`s are not supported when
playback is considered as a sample.

classref-enumeration-constant

`PlaybackType<enum_AudioServer_PlaybackType>` **PLAYBACK\_TYPE\_MAX** =
`3`

**Experimental:** This constant may be changed or removed in future
versions.

Represents the size of the `PlaybackType<enum_AudioServer_PlaybackType>`
enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **bus\_count** = `1`
`🔗<class_AudioServer_property_bus_count>`

classref-property-setget

-   `void (No return value.)` **set\_bus\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_bus\_count**()

Number of available audio buses.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **input\_device** = `"Default"`
`🔗<class_AudioServer_property_input_device>`

classref-property-setget

-   `void (No return value.)` **set\_input\_device**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_input\_device**()

Name of the current device for audio input (see
`get_input_device_list<class_AudioServer_method_get_input_device_list>`).
On systems with multiple audio inputs (such as analog, USB and HDMI
audio), this can be used to select the audio input device. The value
`"Default"` will record audio on the system-wide default audio input. If
an invalid device name is set, the value will be reverted back to
`"Default"`.

\*\*Note:\*\*
`ProjectSettings.audio/driver/enable_input<class_ProjectSettings_property_audio/driver/enable_input>`
must be `true` for audio input to work. See also that setting's
description for caveats related to permissions and operating system
privacy settings.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **output\_device** = `"Default"`
`🔗<class_AudioServer_property_output_device>`

classref-property-setget

-   `void (No return value.)` **set\_output\_device**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_output\_device**()

Name of the current device for audio output (see
`get_output_device_list<class_AudioServer_method_get_output_device_list>`).
On systems with multiple audio outputs (such as analog, USB and HDMI
audio), this can be used to select the audio output device. The value
`"Default"` will play audio on the system-wide default audio output. If
an invalid device name is set, the value will be reverted back to
`"Default"`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **playback\_speed\_scale** = `1.0`
`🔗<class_AudioServer_property_playback_speed_scale>`

classref-property-setget

-   `void (No return value.)` **set\_playback\_speed\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_playback\_speed\_scale**()

Scales the rate at which audio is played (i.e. setting it to `0.5` will
make the audio be played at half its speed). See also
`Engine.time_scale<class_Engine_property_time_scale>` to affect the
general simulation speed, which is independent from
`playback_speed_scale<class_AudioServer_property_playback_speed_scale>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_bus**(at\_position: `int<class_int>` =
-1) `🔗<class_AudioServer_method_add_bus>`

Adds a bus at `at_position`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_bus\_effect**(bus\_idx:
`int<class_int>`, effect: `AudioEffect<class_AudioEffect>`,
at\_position: `int<class_int>` = -1)
`🔗<class_AudioServer_method_add_bus_effect>`

Adds an `AudioEffect<class_AudioEffect>` effect to the bus `bus_idx` at
`at_position`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioBusLayout<class_AudioBusLayout>` **generate\_bus\_layout**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_generate_bus_layout>`

Generates an `AudioBusLayout<class_AudioBusLayout>` using the available
buses and effects.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_bus\_channels**(bus\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_bus_channels>`

Returns the number of channels of the bus at index `bus_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioEffect<class_AudioEffect>` **get\_bus\_effect**(bus\_idx:
`int<class_int>`, effect\_idx: `int<class_int>`)
`🔗<class_AudioServer_method_get_bus_effect>`

Returns the `AudioEffect<class_AudioEffect>` at position `effect_idx` in
bus `bus_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_bus\_effect\_count**(bus\_idx: `int<class_int>`)
`🔗<class_AudioServer_method_get_bus_effect_count>`

Returns the number of effects on the bus at `bus_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioEffectInstance<class_AudioEffectInstance>`
**get\_bus\_effect\_instance**(bus\_idx: `int<class_int>`, effect\_idx:
`int<class_int>`, channel: `int<class_int>` = 0)
`🔗<class_AudioServer_method_get_bus_effect_instance>`

Returns the `AudioEffectInstance<class_AudioEffectInstance>` assigned to
the given bus and effect indices (and optionally channel).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_bus\_index**(bus\_name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_bus_index>`

Returns the index of the bus with the name `bus_name`. Returns `-1` if
no bus with the specified name exist.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_bus\_name**(bus\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_bus_name>`

Returns the name of the bus with the index `bus_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_bus\_peak\_volume\_left\_db**(bus\_idx:
`int<class_int>`, channel: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_bus_peak_volume_left_db>`

Returns the peak volume of the left speaker at bus index `bus_idx` and
channel index `channel`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_bus\_peak\_volume\_right\_db**(bus\_idx:
`int<class_int>`, channel: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_bus_peak_volume_right_db>`

Returns the peak volume of the right speaker at bus index `bus_idx` and
channel index `channel`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_bus\_send**(bus\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_bus_send>`

Returns the name of the bus that the bus at index `bus_idx` sends to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_bus\_volume\_db**(bus\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_bus_volume_db>`

Returns the volume of the bus at index `bus_idx` in dB.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_input\_device\_list**()
`🔗<class_AudioServer_method_get_input_device_list>`

Returns the names of all audio input devices detected on the system.

\*\*Note:\*\*
`ProjectSettings.audio/driver/enable_input<class_ProjectSettings_property_audio/driver/enable_input>`
must be `true` for audio input to work. See also that setting's
description for caveats related to permissions and operating system
privacy settings.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_mix\_rate**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_mix_rate>`

Returns the sample rate at the output of the **AudioServer**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_output\_device\_list**()
`🔗<class_AudioServer_method_get_output_device_list>`

Returns the names of all audio output devices detected on the system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_output\_latency**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_output_latency>`

Returns the audio driver's effective output latency. This is based on
`ProjectSettings.audio/driver/output_latency<class_ProjectSettings_property_audio/driver/output_latency>`,
but the exact returned value will differ depending on the operating
system and audio driver.

\*\*Note:\*\* This can be expensive; it is not recommended to call
`get_output_latency<class_AudioServer_method_get_output_latency>` every
frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`SpeakerMode<enum_AudioServer_SpeakerMode>` **get\_speaker\_mode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_speaker_mode>`

Returns the speaker configuration.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_time\_since\_last\_mix**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_time_since_last_mix>`

Returns the relative time since the last mix occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_time\_to\_next\_mix**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_get_time_to_next_mix>`

Returns the relative time until the next mix occurs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_bus\_bypassing\_effects**(bus\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_is_bus_bypassing_effects>`

If `true`, the bus at index `bus_idx` is bypassing effects.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_bus\_effect\_enabled**(bus\_idx:
`int<class_int>`, effect\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_is_bus_effect_enabled>`

If `true`, the effect at index `effect_idx` on the bus at index
`bus_idx` is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_bus\_mute**(bus\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_is_bus_mute>`

If `true`, the bus at index `bus_idx` is muted.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_bus\_solo**(bus\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioServer_method_is_bus_solo>`

If `true`, the bus at index `bus_idx` is in solo mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_stream\_registered\_as\_sample**(stream:
`AudioStream<class_AudioStream>`)
`🔗<class_AudioServer_method_is_stream_registered_as_sample>`

**Experimental:** This method may be changed or removed in future
versions.

If `true`, the stream is registered as a sample. The engine will not
have to register it before playing the sample.

If `false`, the stream will have to be registered before playing it. To
prevent lag spikes, register the stream as sample with
`register_stream_as_sample<class_AudioServer_method_register_stream_as_sample>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **lock**() `🔗<class_AudioServer_method_lock>`

Locks the audio driver's main loop.

\*\*Note:\*\* Remember to unlock it afterwards.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_bus**(index: `int<class_int>`,
to\_index: `int<class_int>`) `🔗<class_AudioServer_method_move_bus>`

Moves the bus from index `index` to index `to_index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **register\_stream\_as\_sample**(stream:
`AudioStream<class_AudioStream>`)
`🔗<class_AudioServer_method_register_stream_as_sample>`

**Experimental:** This method may be changed or removed in future
versions.

Forces the registration of a stream as a sample.

\*\*Note:\*\* Lag spikes may occur when calling this method, especially
on single-threaded builds. It is suggested to call this method while
loading assets, where the lag spike could be masked, instead of
registering the sample right before it needs to be played.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_bus**(index: `int<class_int>`)
`🔗<class_AudioServer_method_remove_bus>`

Removes the bus at index `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_bus\_effect**(bus\_idx:
`int<class_int>`, effect\_idx: `int<class_int>`)
`🔗<class_AudioServer_method_remove_bus_effect>`

Removes the effect at index `effect_idx` from the bus at index
`bus_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bus\_bypass\_effects**(bus\_idx:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_AudioServer_method_set_bus_bypass_effects>`

If `true`, the bus at index `bus_idx` is bypassing effects.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bus\_effect\_enabled**(bus\_idx:
`int<class_int>`, effect\_idx: `int<class_int>`, enabled:
`bool<class_bool>`)
`🔗<class_AudioServer_method_set_bus_effect_enabled>`

If `true`, the effect at index `effect_idx` on the bus at index
`bus_idx` is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bus\_layout**(bus\_layout:
`AudioBusLayout<class_AudioBusLayout>`)
`🔗<class_AudioServer_method_set_bus_layout>`

Overwrites the currently used `AudioBusLayout<class_AudioBusLayout>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bus\_mute**(bus\_idx: `int<class_int>`,
enable: `bool<class_bool>`) `🔗<class_AudioServer_method_set_bus_mute>`

If `true`, the bus at index `bus_idx` is muted.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bus\_name**(bus\_idx: `int<class_int>`,
name: `String<class_String>`)
`🔗<class_AudioServer_method_set_bus_name>`

Sets the name of the bus at index `bus_idx` to `name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bus\_send**(bus\_idx: `int<class_int>`,
send: `StringName<class_StringName>`)
`🔗<class_AudioServer_method_set_bus_send>`

Connects the output of the bus at `bus_idx` to the bus named `send`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bus\_solo**(bus\_idx: `int<class_int>`,
enable: `bool<class_bool>`) `🔗<class_AudioServer_method_set_bus_solo>`

If `true`, the bus at index `bus_idx` is in solo mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bus\_volume\_db**(bus\_idx:
`int<class_int>`, volume\_db: `float<class_float>`)
`🔗<class_AudioServer_method_set_bus_volume_db>`

Sets the volume of the bus at index `bus_idx` to `volume_db`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_enable\_tagging\_used\_audio\_streams**(enable:
`bool<class_bool>`)
`🔗<class_AudioServer_method_set_enable_tagging_used_audio_streams>`

If set to `true`, all instances of
`AudioStreamPlayback<class_AudioStreamPlayback>` will call
`AudioStreamPlayback._tag_used_streams<class_AudioStreamPlayback_private_method__tag_used_streams>`
every mix step.

\*\*Note:\*\* This is enabled by default in the editor, as it is used by
editor plugins for the audio stream previews.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **swap\_bus\_effects**(bus\_idx:
`int<class_int>`, effect\_idx: `int<class_int>`, by\_effect\_idx:
`int<class_int>`) `🔗<class_AudioServer_method_swap_bus_effects>`

Swaps the position of two effects in bus `bus_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unlock**()
`🔗<class_AudioServer_method_unlock>`

Unlocks the audio driver's main loop. (After locking it, you should
always unlock it.)
