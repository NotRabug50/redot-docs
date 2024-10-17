github\_url  
hide

# AudioEffectHardLimiter

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Adds a hard limiter audio effect to an Audio bus.

classref-introduction-group

## Description

A limiter is an effect designed to disallow sound from going over a
given dB threshold. Hard limiters predict volume peaks, and will
smoothly apply gain reduction when a peak crosses the ceiling threshold
to prevent clipping and distortion. It preserves the waveform and
prevents it from crossing the ceiling threshold. Adding one in the
Master bus is recommended as a safety measure to prevent sudden volume
peaks from occurring, and to prevent distortion caused by clipping.

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

## Property Descriptions

classref-property

`float<class_float>` **ceiling\_db** = `-0.3`
`🔗<class_AudioEffectHardLimiter_property_ceiling_db>`

classref-property-setget

-   `void (No return value.)` **set\_ceiling\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ceiling\_db**()

The waveform's maximum allowed value, in decibels. This value can range
from `-24.0` to `0.0`.

The default value of `-0.3` prevents potential inter-sample peaks (ISP)
from crossing over 0 dB, which can cause slight distortion on some older
hardware.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pre\_gain\_db** = `0.0`
`🔗<class_AudioEffectHardLimiter_property_pre_gain_db>`

classref-property-setget

-   `void (No return value.)` **set\_pre\_gain\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pre\_gain\_db**()

Gain to apply before limiting, in decibels.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **release** = `0.1`
`🔗<class_AudioEffectHardLimiter_property_release>`

classref-property-setget

-   `void (No return value.)` **set\_release**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_release**()

Time it takes in seconds for the gain reduction to fully release.
