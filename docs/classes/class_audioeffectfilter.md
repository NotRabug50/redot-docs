github\_url  
hide

# AudioEffectFilter

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`AudioEffectBandLimitFilter<class_AudioEffectBandLimitFilter>`,
`AudioEffectBandPassFilter<class_AudioEffectBandPassFilter>`,
`AudioEffectHighPassFilter<class_AudioEffectHighPassFilter>`,
`AudioEffectHighShelfFilter<class_AudioEffectHighShelfFilter>`,
`AudioEffectLowPassFilter<class_AudioEffectLowPassFilter>`,
`AudioEffectLowShelfFilter<class_AudioEffectLowShelfFilter>`,
`AudioEffectNotchFilter<class_AudioEffectNotchFilter>`

Adds a filter to the audio bus.

classref-introduction-group

## Description

Allows frequencies other than the
`cutoff_hz<class_AudioEffectFilter_property_cutoff_hz>` to pass.

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **FilterDB**: `🔗<enum_AudioEffectFilter_FilterDB>`

classref-enumeration-constant

`FilterDB<enum_AudioEffectFilter_FilterDB>` **FILTER\_6DB** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`FilterDB<enum_AudioEffectFilter_FilterDB>` **FILTER\_12DB** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`FilterDB<enum_AudioEffectFilter_FilterDB>` **FILTER\_18DB** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`FilterDB<enum_AudioEffectFilter_FilterDB>` **FILTER\_24DB** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **cutoff\_hz** = `2000.0`
`🔗<class_AudioEffectFilter_property_cutoff_hz>`

classref-property-setget

-   `void (No return value.)` **set\_cutoff**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_cutoff**()

Threshold frequency for the filter, in Hz.

classref-item-separator

------------------------------------------------------------------------

classref-property

`FilterDB<enum_AudioEffectFilter_FilterDB>` **db** = `0`
`🔗<class_AudioEffectFilter_property_db>`

classref-property-setget

-   `void (No return value.)` **set\_db**(value:
    `FilterDB<enum_AudioEffectFilter_FilterDB>`)
-   `FilterDB<enum_AudioEffectFilter_FilterDB>` **get\_db**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **gain** = `1.0`
`🔗<class_AudioEffectFilter_property_gain>`

classref-property-setget

-   `void (No return value.)` **set\_gain**(value: `float<class_float>`)
-   `float<class_float>` **get\_gain**()

Gain amount of the frequencies after the filter.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **resonance** = `0.5`
`🔗<class_AudioEffectFilter_property_resonance>`

classref-property-setget

-   `void (No return value.)` **set\_resonance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_resonance**()

Amount of boost in the frequency range near the cutoff frequency.
