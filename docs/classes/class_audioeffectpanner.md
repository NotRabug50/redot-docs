github\_url  
hide

# AudioEffectPanner

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Adds a panner audio effect to an audio bus. Pans sound left or right.

classref-introduction-group

## Description

Determines how much of an audio signal is sent to the left and right
buses.

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

`float<class_float>` **pan** = `0.0`
`🔗<class_AudioEffectPanner_property_pan>`

classref-property-setget

-   `void (No return value.)` **set\_pan**(value: `float<class_float>`)
-   `float<class_float>` **get\_pan**()

Pan position. Value can range from -1 (fully left) to 1 (fully right).
