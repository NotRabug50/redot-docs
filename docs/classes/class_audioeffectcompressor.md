github\_url  
hide

# AudioEffectCompressor

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Adds a compressor audio effect to an audio bus.

Reduces sounds that exceed a certain threshold level, smooths out the
dynamics and increases the overall volume.

classref-introduction-group

## Description

Dynamic range compressor reduces the level of the sound when the
amplitude goes over a certain threshold in Decibels. One of the main
uses of a compressor is to increase the dynamic range by clipping as
little as possible (when sound goes over 0dB).

Compressor has many uses in the mix:

-   In the Master bus to compress the whole output (although an
    `AudioEffectLimiter<class_AudioEffectLimiter>` is probably better).
-   In voice channels to ensure they sound as balanced as possible.
-   Sidechained. This can reduce the sound level sidechained with
    another audio bus for threshold detection. This technique is common
    in video game mixing to the level of music and SFX while voices are
    being heard.
-   Accentuates transients by using a wider attack, making effects sound
    more punchy.

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

`float<class_float>` **attack\_us** = `20.0`
`🔗<class_AudioEffectCompressor_property_attack_us>`

classref-property-setget

-   `void (No return value.)` **set\_attack\_us**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_attack\_us**()

Compressor's reaction time when the signal exceeds the threshold, in
microseconds. Value can range from 20 to 2000.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **gain** = `0.0`
`🔗<class_AudioEffectCompressor_property_gain>`

classref-property-setget

-   `void (No return value.)` **set\_gain**(value: `float<class_float>`)
-   `float<class_float>` **get\_gain**()

Gain applied to the output signal.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **mix** = `1.0`
`🔗<class_AudioEffectCompressor_property_mix>`

classref-property-setget

-   `void (No return value.)` **set\_mix**(value: `float<class_float>`)
-   `float<class_float>` **get\_mix**()

Balance between original signal and effect signal. Value can range from
0 (totally dry) to 1 (totally wet).

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ratio** = `4.0`
`🔗<class_AudioEffectCompressor_property_ratio>`

classref-property-setget

-   `void (No return value.)` **set\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ratio**()

Amount of compression applied to the audio once it passes the threshold
level. The higher the ratio, the more the loud parts of the audio will
be compressed. Value can range from 1 to 48.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **release\_ms** = `250.0`
`🔗<class_AudioEffectCompressor_property_release_ms>`

classref-property-setget

-   `void (No return value.)` **set\_release\_ms**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_release\_ms**()

Compressor's delay time to stop reducing the signal after the signal
level falls below the threshold, in milliseconds. Value can range from
20 to 2000.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **sidechain** = `&""`
`🔗<class_AudioEffectCompressor_property_sidechain>`

classref-property-setget

-   `void (No return value.)` **set\_sidechain**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_sidechain**()

Reduce the sound level using another audio bus for threshold detection.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **threshold** = `0.0`
`🔗<class_AudioEffectCompressor_property_threshold>`

classref-property-setget

-   `void (No return value.)` **set\_threshold**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_threshold**()

The level above which compression is applied to the audio. Value can
range from -60 to 0.
