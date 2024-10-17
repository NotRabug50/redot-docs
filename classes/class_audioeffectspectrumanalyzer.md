github\_url  
hide

# AudioEffectSpectrumAnalyzer

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Audio effect that can be used for real-time audio visualizations.

classref-introduction-group

## Description

This audio effect does not affect sound output, but can be used for
real-time audio visualizations.

This resource configures an
`AudioEffectSpectrumAnalyzerInstance<class_AudioEffectSpectrumAnalyzerInstance>`,
which performs the actual analysis at runtime. An instance can be
acquired with
`AudioServer.get_bus_effect_instance<class_AudioServer_method_get_bus_effect_instance>`.

See also `AudioStreamGenerator<class_AudioStreamGenerator>` for
procedurally generating sounds.

classref-introduction-group

## Tutorials

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **FFTSize**: `🔗<enum_AudioEffectSpectrumAnalyzer_FFTSize>`

classref-enumeration-constant

`FFTSize<enum_AudioEffectSpectrumAnalyzer_FFTSize>` **FFT\_SIZE\_256** =
`0`

Use a buffer of 256 samples for the Fast Fourier transform. Lowest
latency, but least stable over time.

classref-enumeration-constant

`FFTSize<enum_AudioEffectSpectrumAnalyzer_FFTSize>` **FFT\_SIZE\_512** =
`1`

Use a buffer of 512 samples for the Fast Fourier transform. Low latency,
but less stable over time.

classref-enumeration-constant

`FFTSize<enum_AudioEffectSpectrumAnalyzer_FFTSize>` **FFT\_SIZE\_1024**
= `2`

Use a buffer of 1024 samples for the Fast Fourier transform. This is a
compromise between latency and stability over time.

classref-enumeration-constant

`FFTSize<enum_AudioEffectSpectrumAnalyzer_FFTSize>` **FFT\_SIZE\_2048**
= `3`

Use a buffer of 2048 samples for the Fast Fourier transform. High
latency, but stable over time.

classref-enumeration-constant

`FFTSize<enum_AudioEffectSpectrumAnalyzer_FFTSize>` **FFT\_SIZE\_4096**
= `4`

Use a buffer of 4096 samples for the Fast Fourier transform. Highest
latency, but most stable over time.

classref-enumeration-constant

`FFTSize<enum_AudioEffectSpectrumAnalyzer_FFTSize>` **FFT\_SIZE\_MAX** =
`5`

Represents the size of the
`FFTSize<enum_AudioEffectSpectrumAnalyzer_FFTSize>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **buffer\_length** = `2.0`
`🔗<class_AudioEffectSpectrumAnalyzer_property_buffer_length>`

classref-property-setget

-   `void (No return value.)` **set\_buffer\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_buffer\_length**()

The length of the buffer to keep (in seconds). Higher values keep data
around for longer, but require more memory.

classref-item-separator

------------------------------------------------------------------------

classref-property

`FFTSize<enum_AudioEffectSpectrumAnalyzer_FFTSize>` **fft\_size** = `2`
`🔗<class_AudioEffectSpectrumAnalyzer_property_fft_size>`

classref-property-setget

-   `void (No return value.)` **set\_fft\_size**(value:
    `FFTSize<enum_AudioEffectSpectrumAnalyzer_FFTSize>`)
-   `FFTSize<enum_AudioEffectSpectrumAnalyzer_FFTSize>`
    **get\_fft\_size**()

The size of the [Fast Fourier
transform](https://en.wikipedia.org/wiki/Fast_Fourier_transform) buffer.
Higher values smooth out the spectrum analysis over time, but have
greater latency. The effects of this higher latency are especially
noticeable with sudden amplitude changes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **tap\_back\_pos** = `0.01`
`🔗<class_AudioEffectSpectrumAnalyzer_property_tap_back_pos>`

classref-property-setget

-   `void (No return value.)` **set\_tap\_back\_pos**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_tap\_back\_pos**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!
