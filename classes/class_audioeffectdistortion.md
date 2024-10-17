github\_url  
hide

# AudioEffectDistortion

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Adds a distortion audio effect to an Audio bus.

Modifies the sound to make it distorted.

classref-introduction-group

## Description

Different types are available: clip, tan, lo-fi (bit crushing),
overdrive, or waveshape.

By distorting the waveform the frequency content changes, which will
often make the sound "crunchy" or "abrasive". For games, it can simulate
sound coming from some saturated device or speaker very efficiently.

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

## Enumerations

classref-enumeration

enum **Mode**: `🔗<enum_AudioEffectDistortion_Mode>`

classref-enumeration-constant

`Mode<enum_AudioEffectDistortion_Mode>` **MODE\_CLIP** = `0`

Digital distortion effect which cuts off peaks at the top and bottom of
the waveform.

classref-enumeration-constant

`Mode<enum_AudioEffectDistortion_Mode>` **MODE\_ATAN** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`Mode<enum_AudioEffectDistortion_Mode>` **MODE\_LOFI** = `2`

Low-resolution digital distortion effect (bit depth reduction). You can
use it to emulate the sound of early digital audio devices.

classref-enumeration-constant

`Mode<enum_AudioEffectDistortion_Mode>` **MODE\_OVERDRIVE** = `3`

Emulates the warm distortion produced by a field effect transistor,
which is commonly used in solid-state musical instrument amplifiers. The
`drive<class_AudioEffectDistortion_property_drive>` property has no
effect in this mode.

classref-enumeration-constant

`Mode<enum_AudioEffectDistortion_Mode>` **MODE\_WAVESHAPE** = `4`

Waveshaper distortions are used mainly by electronic musicians to
achieve an extra-abrasive sound.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **drive** = `0.0`
`🔗<class_AudioEffectDistortion_property_drive>`

classref-property-setget

-   `void (No return value.)` **set\_drive**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_drive**()

Distortion power. Value can range from 0 to 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **keep\_hf\_hz** = `16000.0`
`🔗<class_AudioEffectDistortion_property_keep_hf_hz>`

classref-property-setget

-   `void (No return value.)` **set\_keep\_hf\_hz**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_keep\_hf\_hz**()

High-pass filter, in Hz. Frequencies higher than this value will not be
affected by the distortion. Value can range from 1 to 20000.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Mode<enum_AudioEffectDistortion_Mode>` **mode** = `0`
`🔗<class_AudioEffectDistortion_property_mode>`

classref-property-setget

-   `void (No return value.)` **set\_mode**(value:
    `Mode<enum_AudioEffectDistortion_Mode>`)
-   `Mode<enum_AudioEffectDistortion_Mode>` **get\_mode**()

Distortion type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **post\_gain** = `0.0`
`🔗<class_AudioEffectDistortion_property_post_gain>`

classref-property-setget

-   `void (No return value.)` **set\_post\_gain**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_post\_gain**()

Increases or decreases the volume after the effect, in decibels. Value
can range from -80 to 24.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pre\_gain** = `0.0`
`🔗<class_AudioEffectDistortion_property_pre_gain>`

classref-property-setget

-   `void (No return value.)` **set\_pre\_gain**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pre\_gain**()

Increases or decreases the volume before the effect, in decibels. Value
can range from -60 to 60.
