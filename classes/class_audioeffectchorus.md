github\_url  
hide

# AudioEffectChorus

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Adds a chorus audio effect.

classref-introduction-group

## Description

Adds a chorus audio effect. The effect applies a filter with voices to
duplicate the audio source and manipulate it through the filter.

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
<tr>
</tr>
</tbody>
</table>

classref-reftable-group

## Methods

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **dry** = `1.0`
`🔗<class_AudioEffectChorus_property_dry>`

classref-property-setget

-   `void (No return value.)` **set\_dry**(value: `float<class_float>`)
-   `float<class_float>` **get\_dry**()

The effect's raw signal.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/1/cutoff\_hz** = `8000.0`
`🔗<class_AudioEffectChorus_property_voice/1/cutoff_hz>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_cutoff\_hz**(voice\_idx:
    `int<class_int>`, cutoff\_hz: `float<class_float>`)
-   `float<class_float>` **get\_voice\_cutoff\_hz**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's cutoff frequency.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/1/delay\_ms** = `15.0`
`🔗<class_AudioEffectChorus_property_voice/1/delay_ms>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_delay\_ms**(voice\_idx:
    `int<class_int>`, delay\_ms: `float<class_float>`)
-   `float<class_float>` **get\_voice\_delay\_ms**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's signal delay.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/1/depth\_ms** = `2.0`
`🔗<class_AudioEffectChorus_property_voice/1/depth_ms>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_depth\_ms**(voice\_idx:
    `int<class_int>`, depth\_ms: `float<class_float>`)
-   `float<class_float>` **get\_voice\_depth\_ms**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice filter's depth.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/1/level\_db** = `0.0`
`🔗<class_AudioEffectChorus_property_voice/1/level_db>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_level\_db**(voice\_idx:
    `int<class_int>`, level\_db: `float<class_float>`)
-   `float<class_float>` **get\_voice\_level\_db**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's volume.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/1/pan** = `-0.5`
`🔗<class_AudioEffectChorus_property_voice/1/pan>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_pan**(voice\_idx:
    `int<class_int>`, pan: `float<class_float>`)
-   `float<class_float>` **get\_voice\_pan**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's pan level.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/1/rate\_hz** = `0.8`
`🔗<class_AudioEffectChorus_property_voice/1/rate_hz>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_rate\_hz**(voice\_idx:
    `int<class_int>`, rate\_hz: `float<class_float>`)
-   `float<class_float>` **get\_voice\_rate\_hz**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's filter rate.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/2/cutoff\_hz** = `8000.0`
`🔗<class_AudioEffectChorus_property_voice/2/cutoff_hz>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_cutoff\_hz**(voice\_idx:
    `int<class_int>`, cutoff\_hz: `float<class_float>`)
-   `float<class_float>` **get\_voice\_cutoff\_hz**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's cutoff frequency.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/2/delay\_ms** = `20.0`
`🔗<class_AudioEffectChorus_property_voice/2/delay_ms>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_delay\_ms**(voice\_idx:
    `int<class_int>`, delay\_ms: `float<class_float>`)
-   `float<class_float>` **get\_voice\_delay\_ms**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's signal delay.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/2/depth\_ms** = `3.0`
`🔗<class_AudioEffectChorus_property_voice/2/depth_ms>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_depth\_ms**(voice\_idx:
    `int<class_int>`, depth\_ms: `float<class_float>`)
-   `float<class_float>` **get\_voice\_depth\_ms**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice filter's depth.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/2/level\_db** = `0.0`
`🔗<class_AudioEffectChorus_property_voice/2/level_db>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_level\_db**(voice\_idx:
    `int<class_int>`, level\_db: `float<class_float>`)
-   `float<class_float>` **get\_voice\_level\_db**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's volume.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/2/pan** = `0.5`
`🔗<class_AudioEffectChorus_property_voice/2/pan>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_pan**(voice\_idx:
    `int<class_int>`, pan: `float<class_float>`)
-   `float<class_float>` **get\_voice\_pan**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's pan level.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/2/rate\_hz** = `1.2`
`🔗<class_AudioEffectChorus_property_voice/2/rate_hz>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_rate\_hz**(voice\_idx:
    `int<class_int>`, rate\_hz: `float<class_float>`)
-   `float<class_float>` **get\_voice\_rate\_hz**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's filter rate.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/3/cutoff\_hz**
`🔗<class_AudioEffectChorus_property_voice/3/cutoff_hz>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_cutoff\_hz**(voice\_idx:
    `int<class_int>`, cutoff\_hz: `float<class_float>`)
-   `float<class_float>` **get\_voice\_cutoff\_hz**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's cutoff frequency.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/3/delay\_ms**
`🔗<class_AudioEffectChorus_property_voice/3/delay_ms>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_delay\_ms**(voice\_idx:
    `int<class_int>`, delay\_ms: `float<class_float>`)
-   `float<class_float>` **get\_voice\_delay\_ms**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's signal delay.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/3/depth\_ms**
`🔗<class_AudioEffectChorus_property_voice/3/depth_ms>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_depth\_ms**(voice\_idx:
    `int<class_int>`, depth\_ms: `float<class_float>`)
-   `float<class_float>` **get\_voice\_depth\_ms**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice filter's depth.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/3/level\_db**
`🔗<class_AudioEffectChorus_property_voice/3/level_db>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_level\_db**(voice\_idx:
    `int<class_int>`, level\_db: `float<class_float>`)
-   `float<class_float>` **get\_voice\_level\_db**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's volume.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/3/pan**
`🔗<class_AudioEffectChorus_property_voice/3/pan>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_pan**(voice\_idx:
    `int<class_int>`, pan: `float<class_float>`)
-   `float<class_float>` **get\_voice\_pan**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's pan level.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/3/rate\_hz**
`🔗<class_AudioEffectChorus_property_voice/3/rate_hz>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_rate\_hz**(voice\_idx:
    `int<class_int>`, rate\_hz: `float<class_float>`)
-   `float<class_float>` **get\_voice\_rate\_hz**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's filter rate.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/4/cutoff\_hz**
`🔗<class_AudioEffectChorus_property_voice/4/cutoff_hz>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_cutoff\_hz**(voice\_idx:
    `int<class_int>`, cutoff\_hz: `float<class_float>`)
-   `float<class_float>` **get\_voice\_cutoff\_hz**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's cutoff frequency.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/4/delay\_ms**
`🔗<class_AudioEffectChorus_property_voice/4/delay_ms>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_delay\_ms**(voice\_idx:
    `int<class_int>`, delay\_ms: `float<class_float>`)
-   `float<class_float>` **get\_voice\_delay\_ms**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's signal delay.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/4/depth\_ms**
`🔗<class_AudioEffectChorus_property_voice/4/depth_ms>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_depth\_ms**(voice\_idx:
    `int<class_int>`, depth\_ms: `float<class_float>`)
-   `float<class_float>` **get\_voice\_depth\_ms**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice filter's depth.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/4/level\_db**
`🔗<class_AudioEffectChorus_property_voice/4/level_db>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_level\_db**(voice\_idx:
    `int<class_int>`, level\_db: `float<class_float>`)
-   `float<class_float>` **get\_voice\_level\_db**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's volume.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/4/pan**
`🔗<class_AudioEffectChorus_property_voice/4/pan>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_pan**(voice\_idx:
    `int<class_int>`, pan: `float<class_float>`)
-   `float<class_float>` **get\_voice\_pan**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's pan level.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **voice/4/rate\_hz**
`🔗<class_AudioEffectChorus_property_voice/4/rate_hz>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_rate\_hz**(voice\_idx:
    `int<class_int>`, rate\_hz: `float<class_float>`)
-   `float<class_float>` **get\_voice\_rate\_hz**(voice\_idx:
    `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The voice's filter rate.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **voice\_count** = `2`
`🔗<class_AudioEffectChorus_property_voice_count>`

classref-property-setget

-   `void (No return value.)` **set\_voice\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_voice\_count**()

The number of voices in the effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **wet** = `0.5`
`🔗<class_AudioEffectChorus_property_wet>`

classref-property-setget

-   `void (No return value.)` **set\_wet**(value: `float<class_float>`)
-   `float<class_float>` **get\_wet**()

The effect's processed signal.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_voice\_cutoff\_hz**(voice\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectChorus_method_get_voice_cutoff_hz>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_voice\_delay\_ms**(voice\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectChorus_method_get_voice_delay_ms>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_voice\_depth\_ms**(voice\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectChorus_method_get_voice_depth_ms>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_voice\_level\_db**(voice\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectChorus_method_get_voice_level_db>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_voice\_pan**(voice\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectChorus_method_get_voice_pan>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_voice\_rate\_hz**(voice\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectChorus_method_get_voice_rate_hz>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_voice\_cutoff\_hz**(voice\_idx:
`int<class_int>`, cutoff\_hz: `float<class_float>`)
`🔗<class_AudioEffectChorus_method_set_voice_cutoff_hz>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_voice\_delay\_ms**(voice\_idx:
`int<class_int>`, delay\_ms: `float<class_float>`)
`🔗<class_AudioEffectChorus_method_set_voice_delay_ms>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_voice\_depth\_ms**(voice\_idx:
`int<class_int>`, depth\_ms: `float<class_float>`)
`🔗<class_AudioEffectChorus_method_set_voice_depth_ms>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_voice\_level\_db**(voice\_idx:
`int<class_int>`, level\_db: `float<class_float>`)
`🔗<class_AudioEffectChorus_method_set_voice_level_db>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_voice\_pan**(voice\_idx:
`int<class_int>`, pan: `float<class_float>`)
`🔗<class_AudioEffectChorus_method_set_voice_pan>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_voice\_rate\_hz**(voice\_idx:
`int<class_int>`, rate\_hz: `float<class_float>`)
`🔗<class_AudioEffectChorus_method_set_voice_rate_hz>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
