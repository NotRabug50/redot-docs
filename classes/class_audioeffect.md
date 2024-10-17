github\_url  
hide

# AudioEffect

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `AudioEffectAmplify<class_AudioEffectAmplify>`,
`AudioEffectCapture<class_AudioEffectCapture>`,
`AudioEffectChorus<class_AudioEffectChorus>`,
`AudioEffectCompressor<class_AudioEffectCompressor>`,
`AudioEffectDelay<class_AudioEffectDelay>`,
`AudioEffectDistortion<class_AudioEffectDistortion>`,
`AudioEffectEQ<class_AudioEffectEQ>`,
`AudioEffectFilter<class_AudioEffectFilter>`,
`AudioEffectHardLimiter<class_AudioEffectHardLimiter>`,
`AudioEffectLimiter<class_AudioEffectLimiter>`,
`AudioEffectPanner<class_AudioEffectPanner>`,
`AudioEffectPhaser<class_AudioEffectPhaser>`,
`AudioEffectPitchShift<class_AudioEffectPitchShift>`,
`AudioEffectRecord<class_AudioEffectRecord>`,
`AudioEffectReverb<class_AudioEffectReverb>`,
`AudioEffectSpectrumAnalyzer<class_AudioEffectSpectrumAnalyzer>`,
`AudioEffectStereoEnhance<class_AudioEffectStereoEnhance>`

Base class for audio effect resources.

classref-introduction-group

## Description

The base `Resource<class_Resource>` for every audio effect. In the
editor, an audio effect can be added to the current bus layout through
the Audio panel. At run-time, it is also possible to manipulate audio
effects through
`AudioServer.add_bus_effect<class_AudioServer_method_add_bus_effect>`,
`AudioServer.remove_bus_effect<class_AudioServer_method_remove_bus_effect>`,
and
`AudioServer.get_bus_effect<class_AudioServer_method_get_bus_effect>`.

When applied on a bus, an audio effect creates a corresponding
`AudioEffectInstance<class_AudioEffectInstance>`. The instance is
directly responsible for manipulating the sound, based on the original
audio effect's properties.

classref-introduction-group

## Tutorials

-   `Audio buses <../tutorials/audio/audio_buses>`
-   [Audio Microphone Record
    Demo](https://godotengine.org/asset-library/asset/2760)

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`AudioEffectInstance<class_AudioEffectInstance>` **\_instantiate**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_AudioEffect_private_method__instantiate>`

Override this method to customize the
`AudioEffectInstance<class_AudioEffectInstance>` created when this
effect is applied on a bus in the editor's Audio panel, or through
`AudioServer.add_bus_effect<class_AudioServer_method_add_bus_effect>`.

    extends AudioEffect

    @export var strength = 4.0

    func _instantiate():
        var effect = CustomAudioEffectInstance.new()
        effect.base = self

        return effect

\*\*Note:\*\* It is recommended to keep a reference to the original
**AudioEffect** in the new instance. Depending on the implementation
this allows the effect instance to listen for changes at run-time and be
modified accordingly.
