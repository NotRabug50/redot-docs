github\_url  
hide

# AudioStreamWAV

**Inherits:** `AudioStream<class_AudioStream>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Stores audio data loaded from WAV files.

classref-introduction-group

## Description

AudioStreamWAV stores sound samples loaded from WAV files. To play the
stored sound, use an `AudioStreamPlayer<class_AudioStreamPlayer>` (for
non-positional audio) or
`AudioStreamPlayer2D<class_AudioStreamPlayer2D>`/`AudioStreamPlayer3D<class_AudioStreamPlayer3D>`
(for positional audio). The sound can be looped.

This class can also be used to store dynamically-generated PCM audio
data. See also `AudioStreamGenerator<class_AudioStreamGenerator>` for
procedural audio generation.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Format**: `🔗<enum_AudioStreamWAV_Format>`

classref-enumeration-constant

`Format<enum_AudioStreamWAV_Format>` **FORMAT\_8\_BITS** = `0`

8-bit PCM audio codec.

classref-enumeration-constant

`Format<enum_AudioStreamWAV_Format>` **FORMAT\_16\_BITS** = `1`

16-bit PCM audio codec.

classref-enumeration-constant

`Format<enum_AudioStreamWAV_Format>` **FORMAT\_IMA\_ADPCM** = `2`

Audio is lossily compressed as IMA ADPCM.

classref-enumeration-constant

`Format<enum_AudioStreamWAV_Format>` **FORMAT\_QOA** = `3`

Audio is lossily compressed as [Quite OK Audio](https://qoaformat.org/).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LoopMode**: `🔗<enum_AudioStreamWAV_LoopMode>`

classref-enumeration-constant

`LoopMode<enum_AudioStreamWAV_LoopMode>` **LOOP\_DISABLED** = `0`

Audio does not loop.

classref-enumeration-constant

`LoopMode<enum_AudioStreamWAV_LoopMode>` **LOOP\_FORWARD** = `1`

Audio loops the data between
`loop_begin<class_AudioStreamWAV_property_loop_begin>` and
`loop_end<class_AudioStreamWAV_property_loop_end>`, playing forward
only.

classref-enumeration-constant

`LoopMode<enum_AudioStreamWAV_LoopMode>` **LOOP\_PINGPONG** = `2`

Audio loops the data between
`loop_begin<class_AudioStreamWAV_property_loop_begin>` and
`loop_end<class_AudioStreamWAV_property_loop_end>`, playing back and
forth.

classref-enumeration-constant

`LoopMode<enum_AudioStreamWAV_LoopMode>` **LOOP\_BACKWARD** = `3`

Audio loops the data between
`loop_begin<class_AudioStreamWAV_property_loop_begin>` and
`loop_end<class_AudioStreamWAV_property_loop_end>`, playing backward
only.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`PackedByteArray<class_PackedByteArray>` **data** = `PackedByteArray()`
`🔗<class_AudioStreamWAV_property_data>`

classref-property-setget

-   `void (No return value.)` **set\_data**(value:
    `PackedByteArray<class_PackedByteArray>`)
-   `PackedByteArray<class_PackedByteArray>` **get\_data**()

Contains the audio data in bytes.

\*\*Note:\*\* If `format<class_AudioStreamWAV_property_format>` is set
to `FORMAT_8_BITS<class_AudioStreamWAV_constant_FORMAT_8_BITS>`, this
property expects signed 8-bit PCM data. To convert from unsigned 8-bit
PCM, subtract 128 from each byte.

\*\*Note:\*\* If `format<class_AudioStreamWAV_property_format>` is set
to `FORMAT_QOA<class_AudioStreamWAV_constant_FORMAT_QOA>`, this property
expects data from a full QOA file.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedByteArray<class_PackedByteArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Format<enum_AudioStreamWAV_Format>` **format** = `0`
`🔗<class_AudioStreamWAV_property_format>`

classref-property-setget

-   `void (No return value.)` **set\_format**(value:
    `Format<enum_AudioStreamWAV_Format>`)
-   `Format<enum_AudioStreamWAV_Format>` **get\_format**()

Audio format. See `Format<enum_AudioStreamWAV_Format>` constants for
values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **loop\_begin** = `0`
`🔗<class_AudioStreamWAV_property_loop_begin>`

classref-property-setget

-   `void (No return value.)` **set\_loop\_begin**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_loop\_begin**()

The loop start point (in number of samples, relative to the beginning of
the stream).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **loop\_end** = `0`
`🔗<class_AudioStreamWAV_property_loop_end>`

classref-property-setget

-   `void (No return value.)` **set\_loop\_end**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_loop\_end**()

The loop end point (in number of samples, relative to the beginning of
the stream).

classref-item-separator

------------------------------------------------------------------------

classref-property

`LoopMode<enum_AudioStreamWAV_LoopMode>` **loop\_mode** = `0`
`🔗<class_AudioStreamWAV_property_loop_mode>`

classref-property-setget

-   `void (No return value.)` **set\_loop\_mode**(value:
    `LoopMode<enum_AudioStreamWAV_LoopMode>`)
-   `LoopMode<enum_AudioStreamWAV_LoopMode>` **get\_loop\_mode**()

The loop mode. See `LoopMode<enum_AudioStreamWAV_LoopMode>` constants
for values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **mix\_rate** = `44100`
`🔗<class_AudioStreamWAV_property_mix_rate>`

classref-property-setget

-   `void (No return value.)` **set\_mix\_rate**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_mix\_rate**()

The sample rate for mixing this audio. Higher values require more
storage space, but result in better quality.

In games, common sample rates in use are `11025`, `16000`, `22050`,
`32000`, `44100`, and `48000`.

According to the [Nyquist-Shannon sampling
theorem](https://en.wikipedia.org/wiki/Nyquist%E2%80%93Shannon_sampling_theorem),
there is no quality difference to human hearing when going past 40,000
Hz (since most humans can only hear up to ~20,000 Hz, often less). If
you are using lower-pitched sounds such as voices, lower sample rates
such as `32000` or `22050` may be usable with no loss in quality.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **stereo** = `false`
`🔗<class_AudioStreamWAV_property_stereo>`

classref-property-setget

-   `void (No return value.)` **set\_stereo**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_stereo**()

If `true`, audio is stereo.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **save\_to\_wav**(path:
`String<class_String>`) `🔗<class_AudioStreamWAV_method_save_to_wav>`

Saves the AudioStreamWAV as a WAV file to `path`. Samples with IMA ADPCM
or Quite OK Audio formats can't be saved.

\*\*Note:\*\* A `.wav` extension is automatically appended to `path` if
it is missing.
