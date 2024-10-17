github\_url  
hide

# AudioEffectEQ

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:** `AudioEffectEQ10<class_AudioEffectEQ10>`,
`AudioEffectEQ21<class_AudioEffectEQ21>`,
`AudioEffectEQ6<class_AudioEffectEQ6>`

Base class for audio equalizers. Gives you control over frequencies.

Use it to create a custom equalizer if
`AudioEffectEQ6<class_AudioEffectEQ6>`,
`AudioEffectEQ10<class_AudioEffectEQ10>` or
`AudioEffectEQ21<class_AudioEffectEQ21>` don't fit your needs.

classref-introduction-group

## Description

AudioEffectEQ gives you control over frequencies. Use it to compensate
for existing deficiencies in audio. AudioEffectEQs are useful on the
Master bus to completely master a mix and give it more character. They
are also useful when a game is run on a mobile device, to adjust the mix
to that kind of speakers (it can be added but disabled when headphones
are plugged).

classref-introduction-group

## Tutorials

-   `Audio buses <../tutorials/audio/audio_buses>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_band\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectEQ_method_get_band_count>`

Returns the number of bands of the equalizer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_band\_gain\_db**(band\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectEQ_method_get_band_gain_db>`

Returns the band's gain at the specified index, in dB.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_band\_gain\_db**(band\_idx:
`int<class_int>`, volume\_db: `float<class_float>`)
`🔗<class_AudioEffectEQ_method_set_band_gain_db>`

Sets band's gain at the specified index, in dB.
