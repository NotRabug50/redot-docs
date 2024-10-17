github\_url  
hide

# AudioEffectReverb

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Adds a reverberation audio effect to an Audio bus.

classref-introduction-group

## Description

Simulates the sound of acoustic environments such as rooms, concert
halls, caverns, or an open spaces.

classref-introduction-group

## Tutorials

-   `Audio buses <../tutorials/audio/audio_buses>`
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **damping** = `0.5`
`🔗<class_AudioEffectReverb_property_damping>`

classref-property-setget

-   `void (No return value.)` **set\_damping**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_damping**()

Defines how reflective the imaginary room's walls are. Value can range
from 0 to 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **dry** = `1.0`
`🔗<class_AudioEffectReverb_property_dry>`

classref-property-setget

-   `void (No return value.)` **set\_dry**(value: `float<class_float>`)
-   `float<class_float>` **get\_dry**()

Output percent of original sound. At 0, only modified sound is
outputted. Value can range from 0 to 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **hipass** = `0.0`
`🔗<class_AudioEffectReverb_property_hipass>`

classref-property-setget

-   `void (No return value.)` **set\_hpf**(value: `float<class_float>`)
-   `float<class_float>` **get\_hpf**()

High-pass filter passes signals with a frequency higher than a certain
cutoff frequency and attenuates signals with frequencies lower than the
cutoff frequency. Value can range from 0 to 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **predelay\_feedback** = `0.4`
`🔗<class_AudioEffectReverb_property_predelay_feedback>`

classref-property-setget

-   `void (No return value.)` **set\_predelay\_feedback**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_predelay\_feedback**()

Output percent of predelay. Value can range from 0 to 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **predelay\_msec** = `150.0`
`🔗<class_AudioEffectReverb_property_predelay_msec>`

classref-property-setget

-   `void (No return value.)` **set\_predelay\_msec**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_predelay\_msec**()

Time between the original signal and the early reflections of the reverb
signal, in milliseconds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **room\_size** = `0.8`
`🔗<class_AudioEffectReverb_property_room_size>`

classref-property-setget

-   `void (No return value.)` **set\_room\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_room\_size**()

Dimensions of simulated room. Bigger means more echoes. Value can range
from 0 to 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **spread** = `1.0`
`🔗<class_AudioEffectReverb_property_spread>`

classref-property-setget

-   `void (No return value.)` **set\_spread**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_spread**()

Widens or narrows the stereo image of the reverb tail. 1 means fully
widens. Value can range from 0 to 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **wet** = `0.5`
`🔗<class_AudioEffectReverb_property_wet>`

classref-property-setget

-   `void (No return value.)` **set\_wet**(value: `float<class_float>`)
-   `float<class_float>` **get\_wet**()

Output percent of modified sound. At 0, only original sound is
outputted. Value can range from 0 to 1.
