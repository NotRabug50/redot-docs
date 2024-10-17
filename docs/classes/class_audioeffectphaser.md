github\_url  
hide

# AudioEffectPhaser

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Adds a phaser audio effect to an audio bus.

Combines the original signal with a copy that is slightly out of phase
with the original.

classref-introduction-group

## Description

Combines phase-shifted signals with the original signal. The movement of
the phase-shifted signals is controlled using a low-frequency
oscillator.

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **depth** = `1.0`
`🔗<class_AudioEffectPhaser_property_depth>`

classref-property-setget

-   `void (No return value.)` **set\_depth**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_depth**()

Governs how high the filter frequencies sweep. Low value will primarily
affect bass frequencies. High value can sweep high into the treble.
Value can range from 0.1 to 4.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **feedback** = `0.7`
`🔗<class_AudioEffectPhaser_property_feedback>`

classref-property-setget

-   `void (No return value.)` **set\_feedback**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_feedback**()

Output percent of modified sound. Value can range from 0.1 to 0.9.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **range\_max\_hz** = `1600.0`
`🔗<class_AudioEffectPhaser_property_range_max_hz>`

classref-property-setget

-   `void (No return value.)` **set\_range\_max\_hz**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_range\_max\_hz**()

Determines the maximum frequency affected by the LFO modulations, in Hz.
Value can range from 10 to 10000.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **range\_min\_hz** = `440.0`
`🔗<class_AudioEffectPhaser_property_range_min_hz>`

classref-property-setget

-   `void (No return value.)` **set\_range\_min\_hz**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_range\_min\_hz**()

Determines the minimum frequency affected by the LFO modulations, in Hz.
Value can range from 10 to 10000.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **rate\_hz** = `0.5`
`🔗<class_AudioEffectPhaser_property_rate_hz>`

classref-property-setget

-   `void (No return value.)` **set\_rate\_hz**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_rate\_hz**()

Adjusts the rate in Hz at which the effect sweeps up and down across the
frequency range.
