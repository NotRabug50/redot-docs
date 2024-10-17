github\_url  
hide

# AudioStreamGenerator

**Inherits:** `AudioStream<class_AudioStream>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

An audio stream with utilities for procedural sound generation.

classref-introduction-group

## Description

**AudioStreamGenerator** is a type of audio stream that does not play
back sounds on its own; instead, it expects a script to generate audio
data for it. See also
`AudioStreamGeneratorPlayback<class_AudioStreamGeneratorPlayback>`.

Here's a sample on how to use it to generate a sine wave:

gdscript

var playback \# Will hold the AudioStreamGeneratorPlayback. @onready var
sample\_hz = $AudioStreamPlayer.stream.mix\_rate var pulse\_hz = 440.0
\# The frequency of the sound wave.

func \_ready():  
$AudioStreamPlayer.play() playback =
$AudioStreamPlayer.get\_stream\_playback() fill\_buffer()

func fill\_buffer():  
var phase = 0.0 var increment = pulse\_hz / sample\_hz var
frames\_available = playback.get\_frames\_available()

for i in range(frames\_available):  
playback.push\_frame(Vector2.ONE \* sin(phase \* TAU)) phase =
fmod(phase + increment, 1.0)

csharp

\[Export\] public AudioStreamPlayer Player { get; set; }

private AudioStreamGeneratorPlayback \_playback; // Will hold the
AudioStreamGeneratorPlayback. private float \_sampleHz; private float
\_pulseHz = 440.0f; // The frequency of the sound wave.

public override void \_Ready() { if (Player.Stream is
AudioStreamGenerator generator) // Type as a generator to access
MixRate. { \_sampleHz = generator.MixRate; Player.Play(); \_playback =
(AudioStreamGeneratorPlayback)Player.GetStreamPlayback(); FillBuffer();
} }

public void FillBuffer() { double phase = 0.0; float increment =
\_pulseHz / \_sampleHz; int framesAvailable =
\_playback.GetFramesAvailable();

> for (int i = 0; i &lt; framesAvailable; i++) {
> \_playback.PushFrame(Vector2.One \* (float)Mathf.Sin(phase \*
> Mathf.Tau)); phase = Mathf.PosMod(phase + increment, 1.0); }

}

In the example above, the "AudioStreamPlayer" node must use an
**AudioStreamGenerator** as its stream. The `fill_buffer` function
provides audio data for approximating a sine wave.

See also
`AudioEffectSpectrumAnalyzer<class_AudioEffectSpectrumAnalyzer>` for
performing real-time audio spectrum analysis.

\*\*Note:\*\* Due to performance constraints, this class is best used
from C# or from a compiled language via GDExtension. If you still want
to use this class from GDScript, consider using a lower
`mix_rate<class_AudioStreamGenerator_property_mix_rate>` such as 11,025
Hz or 22,050 Hz.

classref-introduction-group

## Tutorials

-   [Audio Generator
    Demo](https://godotengine.org/asset-library/asset/2759)

classref-reftable-group

## Properties

<table>
<tbody>
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

`float<class_float>` **buffer\_length** = `0.5`
`🔗<class_AudioStreamGenerator_property_buffer_length>`

classref-property-setget

-   `void (No return value.)` **set\_buffer\_length**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_buffer\_length**()

The length of the buffer to generate (in seconds). Lower values result
in less latency, but require the script to generate audio data faster,
resulting in increased CPU usage and more risk for audio cracking if the
CPU can't keep up.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **mix\_rate** = `44100.0`
`🔗<class_AudioStreamGenerator_property_mix_rate>`

classref-property-setget

-   `void (No return value.)` **set\_mix\_rate**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_mix\_rate**()

The sample rate to use (in Hz). Higher values are more demanding for the
CPU to generate, but result in better quality.

In games, common sample rates in use are `11025`, `16000`, `22050`,
`32000`, `44100`, and `48000`.

According to the [Nyquist-Shannon sampling
theorem](https://en.wikipedia.org/wiki/Nyquist%E2%80%93Shannon_sampling_theorem),
there is no quality difference to human hearing when going past 40,000
Hz (since most humans can only hear up to ~20,000 Hz, often less). If
you are generating lower-pitched sounds such as voices, lower sample
rates such as `32000` or `22050` may be usable with no loss in quality.
