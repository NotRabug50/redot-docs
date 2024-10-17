github\_url  
hide

# AudioEffectAmplify

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Adds an amplifying audio effect to an audio bus.

classref-introduction-group

## Description

Increases or decreases the volume being routed through the audio bus.

classref-introduction-group

## Tutorials

-   `Audio buses <../tutorials/audio/audio_buses>`

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **volume\_db** = `0.0`
`🔗<class_AudioEffectAmplify_property_volume_db>`

classref-property-setget

-   `void (No return value.)` **set\_volume\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_volume\_db**()

Amount of amplification in decibels. Positive values make the sound
louder, negative values make it quieter. Value can range from -80 to 24.
