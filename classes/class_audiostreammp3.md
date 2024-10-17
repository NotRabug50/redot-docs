github\_url  
hide

# AudioStreamMP3

**Inherits:** `AudioStream<class_AudioStream>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

MP3 audio stream driver.

classref-introduction-group

## Description

MP3 audio stream driver. See `data<class_AudioStreamMP3_property_data>`
if you want to load an MP3 file at run-time.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **bar\_beats** = `4`
`🔗<class_AudioStreamMP3_property_bar_beats>`

classref-property-setget

-   `void (No return value.)` **set\_bar\_beats**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_bar\_beats**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **beat\_count** = `0`
`🔗<class_AudioStreamMP3_property_beat_count>`

classref-property-setget

-   `void (No return value.)` **set\_beat\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_beat\_count**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **bpm** = `0.0`
`🔗<class_AudioStreamMP3_property_bpm>`

classref-property-setget

-   `void (No return value.)` **set\_bpm**(value: `float<class_float>`)
-   `float<class_float>` **get\_bpm**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedByteArray<class_PackedByteArray>` **data** = `PackedByteArray()`
`🔗<class_AudioStreamMP3_property_data>`

classref-property-setget

-   `void (No return value.)` **set\_data**(value:
    `PackedByteArray<class_PackedByteArray>`)
-   `PackedByteArray<class_PackedByteArray>` **get\_data**()

Contains the audio data in bytes.

You can load a file without having to import it beforehand using the
code snippet below. Keep in mind that this snippet loads the whole file
into memory and may not be ideal for huge files (hundreds of megabytes
or more).

gdscript

func load\_mp3(path):  
var file = FileAccess.open(path, FileAccess.READ) var sound =
AudioStreamMP3.new() sound.data = file.get\_buffer(file.get\_length())
return sound

csharp

public AudioStreamMP3 LoadMP3(string path) { using var file =
FileAccess.Open(path, FileAccess.ModeFlags.Read); var sound = new
AudioStreamMP3(); sound.Data = file.GetBuffer(file.GetLength()); return
sound; }

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedByteArray<class_PackedByteArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **loop** = `false`
`🔗<class_AudioStreamMP3_property_loop>`

classref-property-setget

-   `void (No return value.)` **set\_loop**(value: `bool<class_bool>`)
-   `bool<class_bool>` **has\_loop**()

If `true`, the stream will automatically loop when it reaches the end.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **loop\_offset** = `0.0`
`🔗<class_AudioStreamMP3_property_loop_offset>`

classref-property-setget

-   `void (No return value.)` **set\_loop\_offset**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_loop\_offset**()

Time in seconds at which the stream starts after being looped.
