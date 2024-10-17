github\_url  
hide

# AudioEffectSpectrumAnalyzerInstance

**Inherits:** `AudioEffectInstance<class_AudioEffectInstance>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Queryable instance of an
`AudioEffectSpectrumAnalyzer<class_AudioEffectSpectrumAnalyzer>`.

classref-introduction-group

## Description

The runtime part of an
`AudioEffectSpectrumAnalyzer<class_AudioEffectSpectrumAnalyzer>`, which
can be used to query the magnitude of a frequency range on its host bus.

An instance of this class can be acquired with
`AudioServer.get_bus_effect_instance<class_AudioServer_method_get_bus_effect_instance>`.

classref-introduction-group

## Tutorials

-   [Audio Spectrum Visualizer
    Demo](https://godotengine.org/asset-library/asset/2762)

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

enum **MagnitudeMode**:
`🔗<enum_AudioEffectSpectrumAnalyzerInstance_MagnitudeMode>`

classref-enumeration-constant

`MagnitudeMode<enum_AudioEffectSpectrumAnalyzerInstance_MagnitudeMode>`
**MAGNITUDE\_AVERAGE** = `0`

Use the average value across the frequency range as magnitude.

classref-enumeration-constant

`MagnitudeMode<enum_AudioEffectSpectrumAnalyzerInstance_MagnitudeMode>`
**MAGNITUDE\_MAX** = `1`

Use the maximum value of the frequency range as magnitude.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Vector2<class_Vector2>`
**get\_magnitude\_for\_frequency\_range**(from\_hz:
`float<class_float>`, to\_hz: `float<class_float>`, mode:
`MagnitudeMode<enum_AudioEffectSpectrumAnalyzerInstance_MagnitudeMode>`
= 1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectSpectrumAnalyzerInstance_method_get_magnitude_for_frequency_range>`

Returns the magnitude of the frequencies from `from_hz` to `to_hz` in
linear energy as a Vector2. The `x` component of the return value
represents the left stereo channel, and `y` represents the right
channel.

`mode` determines how the frequency range will be processed. See
`MagnitudeMode<enum_AudioEffectSpectrumAnalyzerInstance_MagnitudeMode>`.
