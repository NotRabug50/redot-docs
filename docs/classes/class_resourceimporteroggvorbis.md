github\_url  
hide

# ResourceImporterOggVorbis

**Inherits:** `ResourceImporter<class_ResourceImporter>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Imports an Ogg Vorbis audio file for playback.

classref-introduction-group

## Description

Ogg Vorbis is a lossy audio format, with better audio quality compared
to `ResourceImporterMP3<class_ResourceImporterMP3>` at a given bitrate.

In most cases, it's recommended to use Ogg Vorbis over MP3. However, if
you're using an MP3 sound source with no higher quality source
available, then it's recommended to use the MP3 file directly to avoid
double lossy compression.

Ogg Vorbis requires more CPU to decode than
`ResourceImporterWAV<class_ResourceImporterWAV>`. If you need to play a
lot of simultaneous sounds, it's recommended to use WAV for those sounds
instead, especially if targeting low-end devices.

classref-introduction-group

## Tutorials

-   `Importing audio samples <../tutorials/assets_pipeline/importing_audio_samples>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **bar\_beats** = `4`
`🔗<class_ResourceImporterOggVorbis_property_bar_beats>`

The number of bars within a single beat in the audio track. This is only
relevant for music that wishes to make use of interactive music
functionality (not implemented yet), not sound effects.

A more convenient editor for
`bar_beats<class_ResourceImporterOggVorbis_property_bar_beats>` is
provided in the **Advanced Import Settings** dialog, as it lets you
preview your changes without having to reimport the audio.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **beat\_count** = `0`
`🔗<class_ResourceImporterOggVorbis_property_beat_count>`

The beat count of the audio track. This is only relevant for music that
wishes to make use of interactive music functionality (not implemented
yet), not sound effects.

A more convenient editor for
`beat_count<class_ResourceImporterOggVorbis_property_beat_count>` is
provided in the **Advanced Import Settings** dialog, as it lets you
preview your changes without having to reimport the audio.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **bpm** = `0`
`🔗<class_ResourceImporterOggVorbis_property_bpm>`

The Beats Per Minute of the audio track. This should match the BPM
measure that was used to compose the track. This is only relevant for
music that wishes to make use of interactive music functionality (not
implemented yet), not sound effects.

A more convenient editor for
`bpm<class_ResourceImporterOggVorbis_property_bpm>` is provided in the
**Advanced Import Settings** dialog, as it lets you preview your changes
without having to reimport the audio.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **loop** = `false`
`🔗<class_ResourceImporterOggVorbis_property_loop>`

If enabled, the audio will begin playing at the beginning after playback
ends by reaching the end of the audio.

\*\*Note:\*\* In `AudioStreamPlayer<class_AudioStreamPlayer>`, the
`AudioStreamPlayer.finished<class_AudioStreamPlayer_signal_finished>`
signal won't be emitted for looping audio when it reaches the end of the
audio file, as the audio will keep playing indefinitely.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **loop\_offset** = `0`
`🔗<class_ResourceImporterOggVorbis_property_loop_offset>`

Determines where audio will start to loop after playback reaches the end
of the audio. This can be used to only loop a part of the audio file,
which is useful for some ambient sounds or music. The value is
determined in seconds relative to the beginning of the audio. A value of
`0.0` will loop the entire audio file.

Only has an effect if
`loop<class_ResourceImporterOggVorbis_property_loop>` is `true`.

A more convenient editor for
`loop_offset<class_ResourceImporterOggVorbis_property_loop_offset>` is
provided in the **Advanced Import Settings** dialog, as it lets you
preview your changes without having to reimport the audio.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`AudioStreamOggVorbis<class_AudioStreamOggVorbis>`
**load\_from\_buffer**(buffer: `PackedByteArray<class_PackedByteArray>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_ResourceImporterOggVorbis_method_load_from_buffer>`

This method loads audio data from a PackedByteArray buffer into an
AudioStreamOggVorbis object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioStreamOggVorbis<class_AudioStreamOggVorbis>`
**load\_from\_file**(path: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_ResourceImporterOggVorbis_method_load_from_file>`

This method loads audio data from a file into an AudioStreamOggVorbis
object. The file path is provided as a string.
