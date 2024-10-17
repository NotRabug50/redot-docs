github\_url  
hide

# AudioEffectPitchShift

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Adds a pitch-shifting audio effect to an audio bus.

Raises or lowers the pitch of original sound.

classref-introduction-group

## Description

Allows modulation of pitch independently of tempo. All frequencies can
be increased/decreased with minimal effect on transients.

classref-introduction-group

## Tutorials

-   `Audio buses <../tutorials/audio/audio_buses>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **FFTSize**: `🔗<enum_AudioEffectPitchShift_FFTSize>`

classref-enumeration-constant

`FFTSize<enum_AudioEffectPitchShift_FFTSize>` **FFT\_SIZE\_256** = `0`

Use a buffer of 256 samples for the Fast Fourier transform. Lowest
latency, but least stable over time.

classref-enumeration-constant

`FFTSize<enum_AudioEffectPitchShift_FFTSize>` **FFT\_SIZE\_512** = `1`

Use a buffer of 512 samples for the Fast Fourier transform. Low latency,
but less stable over time.

classref-enumeration-constant

`FFTSize<enum_AudioEffectPitchShift_FFTSize>` **FFT\_SIZE\_1024** = `2`

Use a buffer of 1024 samples for the Fast Fourier transform. This is a
compromise between latency and stability over time.

classref-enumeration-constant

`FFTSize<enum_AudioEffectPitchShift_FFTSize>` **FFT\_SIZE\_2048** = `3`

Use a buffer of 2048 samples for the Fast Fourier transform. High
latency, but stable over time.

classref-enumeration-constant

`FFTSize<enum_AudioEffectPitchShift_FFTSize>` **FFT\_SIZE\_4096** = `4`

Use a buffer of 4096 samples for the Fast Fourier transform. Highest
latency, but most stable over time.

classref-enumeration-constant

`FFTSize<enum_AudioEffectPitchShift_FFTSize>` **FFT\_SIZE\_MAX** = `5`

Represents the size of the `FFTSize<enum_AudioEffectPitchShift_FFTSize>`
enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`FFTSize<enum_AudioEffectPitchShift_FFTSize>` **fft\_size** = `3`
`🔗<class_AudioEffectPitchShift_property_fft_size>`

classref-property-setget

-   `void (No return value.)` **set\_fft\_size**(value:
    `FFTSize<enum_AudioEffectPitchShift_FFTSize>`)
-   `FFTSize<enum_AudioEffectPitchShift_FFTSize>` **get\_fft\_size**()

The size of the [Fast Fourier
transform](https://en.wikipedia.org/wiki/Fast_Fourier_transform) buffer.
Higher values smooth out the effect over time, but have greater latency.
The effects of this higher latency are especially noticeable on sounds
that have sudden amplitude changes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **oversampling** = `4`
`🔗<class_AudioEffectPitchShift_property_oversampling>`

classref-property-setget

-   `void (No return value.)` **set\_oversampling**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_oversampling**()

The oversampling factor to use. Higher values result in better quality,
but are more demanding on the CPU and may cause audio cracking if the
CPU can't keep up.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pitch\_scale** = `1.0`
`🔗<class_AudioEffectPitchShift_property_pitch_scale>`

classref-property-setget

-   `void (No return value.)` **set\_pitch\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pitch\_scale**()

The pitch scale to use. `1.0` is the default pitch and plays sounds
unaffected.
`pitch_scale<class_AudioEffectPitchShift_property_pitch_scale>` can
range from `0.0` (infinitely low pitch, inaudible) to `16` (16 times
higher than the initial pitch).
