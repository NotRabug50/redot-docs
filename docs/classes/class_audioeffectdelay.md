github\_url  
hide

# AudioEffectDelay

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Adds a delay audio effect to an audio bus. Plays input signal back after
a period of time.

Two tap delay and feedback options.

classref-introduction-group

## Description

Plays input signal back after a period of time. The delayed signal may
be played back multiple times to create the sound of a repeating,
decaying echo. Delay effects range from a subtle echo effect to a
pronounced blending of previous sounds with new sounds.

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

`float<class_float>` **dry** = `1.0`
`🔗<class_AudioEffectDelay_property_dry>`

classref-property-setget

-   `void (No return value.)` **set\_dry**(value: `float<class_float>`)
-   `float<class_float>` **get\_dry**()

Output percent of original sound. At 0, only delayed sounds are output.
Value can range from 0 to 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **feedback\_active** = `false`
`🔗<class_AudioEffectDelay_property_feedback_active>`

classref-property-setget

-   `void (No return value.)` **set\_feedback\_active**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_feedback\_active**()

If `true`, feedback is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **feedback\_delay\_ms** = `340.0`
`🔗<class_AudioEffectDelay_property_feedback_delay_ms>`

classref-property-setget

-   `void (No return value.)` **set\_feedback\_delay\_ms**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_feedback\_delay\_ms**()

Feedback delay time in milliseconds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **feedback\_level\_db** = `-6.0`
`🔗<class_AudioEffectDelay_property_feedback_level_db>`

classref-property-setget

-   `void (No return value.)` **set\_feedback\_level\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_feedback\_level\_db**()

Sound level for feedback.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **feedback\_lowpass** = `16000.0`
`🔗<class_AudioEffectDelay_property_feedback_lowpass>`

classref-property-setget

-   `void (No return value.)` **set\_feedback\_lowpass**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_feedback\_lowpass**()

Low-pass filter for feedback, in Hz. Frequencies below this value are
filtered out of the source signal.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **tap1\_active** = `true`
`🔗<class_AudioEffectDelay_property_tap1_active>`

classref-property-setget

-   `void (No return value.)` **set\_tap1\_active**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_tap1\_active**()

If `true`, the first tap will be enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **tap1\_delay\_ms** = `250.0`
`🔗<class_AudioEffectDelay_property_tap1_delay_ms>`

classref-property-setget

-   `void (No return value.)` **set\_tap1\_delay\_ms**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_tap1\_delay\_ms**()

First tap delay time in milliseconds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **tap1\_level\_db** = `-6.0`
`🔗<class_AudioEffectDelay_property_tap1_level_db>`

classref-property-setget

-   `void (No return value.)` **set\_tap1\_level\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_tap1\_level\_db**()

Sound level for the first tap.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **tap1\_pan** = `0.2`
`🔗<class_AudioEffectDelay_property_tap1_pan>`

classref-property-setget

-   `void (No return value.)` **set\_tap1\_pan**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_tap1\_pan**()

Pan position for the first tap. Value can range from -1 (fully left) to
1 (fully right).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **tap2\_active** = `true`
`🔗<class_AudioEffectDelay_property_tap2_active>`

classref-property-setget

-   `void (No return value.)` **set\_tap2\_active**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_tap2\_active**()

If `true`, the second tap will be enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **tap2\_delay\_ms** = `500.0`
`🔗<class_AudioEffectDelay_property_tap2_delay_ms>`

classref-property-setget

-   `void (No return value.)` **set\_tap2\_delay\_ms**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_tap2\_delay\_ms**()

Second tap delay time in milliseconds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **tap2\_level\_db** = `-12.0`
`🔗<class_AudioEffectDelay_property_tap2_level_db>`

classref-property-setget

-   `void (No return value.)` **set\_tap2\_level\_db**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_tap2\_level\_db**()

Sound level for the second tap.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **tap2\_pan** = `-0.4`
`🔗<class_AudioEffectDelay_property_tap2_pan>`

classref-property-setget

-   `void (No return value.)` **set\_tap2\_pan**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_tap2\_pan**()

Pan position for the second tap. Value can range from -1 (fully left) to
1 (fully right).
