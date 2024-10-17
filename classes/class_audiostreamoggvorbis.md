github\_url  
hide

# AudioStreamOggVorbis

**Inherits:** `AudioStream<class_AudioStream>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A class representing an Ogg Vorbis audio stream.

classref-introduction-group

## Description

The AudioStreamOggVorbis class is a specialized
`AudioStream<class_AudioStream>` for handling Ogg Vorbis file formats.
It offers functionality for loading and playing back Ogg Vorbis files,
as well as managing looping and other playback properties. This class is
part of the audio stream system, which also supports WAV files through
the `AudioStreamWAV<class_AudioStreamWAV>` class.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`

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
`🔗<class_AudioStreamOggVorbis_property_bar_beats>`

classref-property-setget

-   `void (No return value.)` **set\_bar\_beats**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_bar\_beats**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **beat\_count** = `0`
`🔗<class_AudioStreamOggVorbis_property_beat_count>`

classref-property-setget

-   `void (No return value.)` **set\_beat\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_beat\_count**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **bpm** = `0.0`
`🔗<class_AudioStreamOggVorbis_property_bpm>`

classref-property-setget

-   `void (No return value.)` **set\_bpm**(value: `float<class_float>`)
-   `float<class_float>` **get\_bpm**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **loop** = `false`
`🔗<class_AudioStreamOggVorbis_property_loop>`

classref-property-setget

-   `void (No return value.)` **set\_loop**(value: `bool<class_bool>`)
-   `bool<class_bool>` **has\_loop**()

If `true`, the audio will play again from the specified
`loop_offset<class_AudioStreamOggVorbis_property_loop_offset>` once it
is done playing. Useful for ambient sounds and background music.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **loop\_offset** = `0.0`
`🔗<class_AudioStreamOggVorbis_property_loop_offset>`

classref-property-setget

-   `void (No return value.)` **set\_loop\_offset**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_loop\_offset**()

Time in seconds at which the stream starts after being looped.

classref-item-separator

------------------------------------------------------------------------

classref-property

`OggPacketSequence<class_OggPacketSequence>` **packet\_sequence**
`🔗<class_AudioStreamOggVorbis_property_packet_sequence>`

classref-property-setget

-   `void (No return value.)` **set\_packet\_sequence**(value:
    `OggPacketSequence<class_OggPacketSequence>`)
-   `OggPacketSequence<class_OggPacketSequence>`
    **get\_packet\_sequence**()

Contains the raw Ogg data for this stream.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`AudioStreamOggVorbis<class_AudioStreamOggVorbis>`
**load\_from\_buffer**(buffer: `PackedByteArray<class_PackedByteArray>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_AudioStreamOggVorbis_method_load_from_buffer>`

Creates a new AudioStreamOggVorbis instance from the given buffer. The
buffer must contain Ogg Vorbis data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioStreamOggVorbis<class_AudioStreamOggVorbis>`
**load\_from\_file**(path: `String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_AudioStreamOggVorbis_method_load_from_file>`

Creates a new AudioStreamOggVorbis instance from the given file path.
The file must be in Ogg Vorbis format.
