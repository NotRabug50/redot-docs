github\_url  
hide

# AudioEffectLimiter

**Deprecated:** Use
`AudioEffectHardLimiter<class_AudioEffectHardLimiter>` instead.

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Adds a soft-clip limiter audio effect to an Audio bus.

classref-introduction-group

## Description

A limiter is similar to a compressor, but it's less flexible and
designed to disallow sound going over a given dB threshold. Adding one
in the Master bus is always recommended to reduce the effects of
clipping.

Soft clipping starts to reduce the peaks a little below the threshold
level and progressively increases its effect as the input level
increases such that the threshold is never exceeded.

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

## Property Descriptions

classref-property

`float<class_float>` **ceiling\_db** = `-0.1`
`🔗<class_AudioEffectLimiter_property_ceiling_db>`

classref-property-setget

-   `void (No return value.)` **set\_ceiling\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ceiling\_db**()

The waveform's maximum allowed value, in decibels. Value can range from
-20 to -0.1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **soft\_clip\_db** = `2.0`
`🔗<class_AudioEffectLimiter_property_soft_clip_db>`

classref-property-setget

-   `void (No return value.)` **set\_soft\_clip\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_soft\_clip\_db**()

Applies a gain to the limited waves, in decibels. Value can range from 0
to 6.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **soft\_clip\_ratio** = `10.0`
`🔗<class_AudioEffectLimiter_property_soft_clip_ratio>`

classref-property-setget

-   `void (No return value.)` **set\_soft\_clip\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_soft\_clip\_ratio**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **threshold\_db** = `0.0`
`🔗<class_AudioEffectLimiter_property_threshold_db>`

classref-property-setget

-   `void (No return value.)` **set\_threshold\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_threshold\_db**()

Threshold from which the limiter begins to be active, in decibels. Value
can range from -30 to 0.
