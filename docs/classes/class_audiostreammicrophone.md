github\_url  
hide

# AudioStreamMicrophone

**Inherits:** `AudioStream<class_AudioStream>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Plays real-time audio input data.

classref-introduction-group

## Description

When used directly in an `AudioStreamPlayer<class_AudioStreamPlayer>`
node, **AudioStreamMicrophone** plays back microphone input in
real-time. This can be used in conjunction with
`AudioEffectCapture<class_AudioEffectCapture>` to process the data or
save it.

\*\*Note:\*\*
`ProjectSettings.audio/driver/enable_input<class_ProjectSettings_property_audio/driver/enable_input>`
must be `true` for audio input to work. See also that setting's
description for caveats related to permissions and operating system
privacy settings.

classref-introduction-group

## Tutorials

-   `Recording with microphone <../tutorials/audio/recording_with_microphone>`
-   [Audio Mic Record
    Demo](https://github.com/godotengine/godot-demo-projects/tree/master/audio/mic_record)
