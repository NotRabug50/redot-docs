github\_url  
hide

# AudioEffectCapture

**Inherits:** `AudioEffect<class_AudioEffect>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Captures audio from an audio bus in real-time.

classref-introduction-group

## Description

AudioEffectCapture is an AudioEffect which copies all audio frames from
the attached audio effect bus into its internal ring buffer.

Application code should consume these audio frames from this ring buffer
using `get_buffer<class_AudioEffectCapture_method_get_buffer>` and
process it as needed, for example to capture data from an
`AudioStreamMicrophone<class_AudioStreamMicrophone>`, implement
application-defined effects, or to transmit audio over the network. When
capturing audio data from a microphone, the format of the samples will
be stereo 32-bit floating-point PCM.

Unlike `AudioEffectRecord<class_AudioEffectRecord>`, this effect only
returns the raw audio samples instead of encoding them into an
`AudioStream<class_AudioStream>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **buffer\_length** = `0.1`
`🔗<class_AudioEffectCapture_property_buffer_length>`

classref-property-setget

-   `void (No return value.)` **set\_buffer\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_buffer\_length**()

Length of the internal ring buffer, in seconds. Setting the buffer
length will have no effect if already initialized.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **can\_get\_buffer**(frames: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectCapture_method_can_get_buffer>`

Returns `true` if at least `frames` audio frames are available to read
in the internal ring buffer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_buffer**()
`🔗<class_AudioEffectCapture_method_clear_buffer>`

Clears the internal ring buffer.

\*\*Note:\*\* Calling this during a capture can cause the loss of
samples which causes popping in the playback.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>` **get\_buffer**(frames:
`int<class_int>`) `🔗<class_AudioEffectCapture_method_get_buffer>`

Gets the next `frames` audio samples from the internal ring buffer.

Returns a `PackedVector2Array<class_PackedVector2Array>` containing
exactly `frames` audio samples if available, or an empty
`PackedVector2Array<class_PackedVector2Array>` if insufficient data was
available.

The samples are signed floating-point PCM between `-1` and `1`. You will
have to scale them if you want to use them as 8 or 16-bit integer
samples. (`v = 0x7fff * samples[0].x`)

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_buffer\_length\_frames**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectCapture_method_get_buffer_length_frames>`

Returns the total size of the internal ring buffer in frames.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_discarded\_frames**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectCapture_method_get_discarded_frames>`

Returns the number of audio frames discarded from the audio bus due to
full buffer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_frames\_available**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectCapture_method_get_frames_available>`

Returns the number of frames available to read using
`get_buffer<class_AudioEffectCapture_method_get_buffer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_pushed\_frames**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioEffectCapture_method_get_pushed_frames>`

Returns the number of audio frames inserted from the audio bus.
