github\_url  
hide

# AudioStreamPlaylist

**Inherits:** `AudioStream<class_AudioStream>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

`AudioStream<class_AudioStream>` that includes sub-streams and plays
them back like a playlist.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**MAX\_STREAMS** = `64`
`🔗<class_AudioStreamPlaylist_constant_MAX_STREAMS>`

Maximum amount of streams supported in the playlist.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **fade\_time** = `0.3`
`🔗<class_AudioStreamPlaylist_property_fade_time>`

classref-property-setget

-   `void (No return value.)` **set\_fade\_time**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fade\_time**()

Fade time used when a stream ends, when going to the next one. Streams
are expected to have an extra bit of audio after the end to help with
fading.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **loop** = `true`
`🔗<class_AudioStreamPlaylist_property_loop>`

classref-property-setget

-   `void (No return value.)` **set\_loop**(value: `bool<class_bool>`)
-   `bool<class_bool>` **has\_loop**()

If `true`, the playlist will loop, otherwise the playlist will end when
the last stream is finished.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shuffle** = `false`
`🔗<class_AudioStreamPlaylist_property_shuffle>`

classref-property-setget

-   `void (No return value.)` **set\_shuffle**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_shuffle**()

If `true`, the playlist will shuffle each time playback starts and each
time it loops.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **stream\_count** = `0`
`🔗<class_AudioStreamPlaylist_property_stream_count>`

classref-property-setget

-   `void (No return value.)` **set\_stream\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_stream\_count**()

Amount of streams in the playlist.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_bpm**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamPlaylist_method_get_bpm>`

Returns the BPM of the playlist, which can vary depending on the clip
being played.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AudioStream<class_AudioStream>` **get\_list\_stream**(stream\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamPlaylist_method_get_list_stream>`

Returns the stream at playback position index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_list\_stream**(stream\_index:
`int<class_int>`, audio\_stream: `AudioStream<class_AudioStream>`)
`🔗<class_AudioStreamPlaylist_method_set_list_stream>`

Sets the stream at playback position index.
