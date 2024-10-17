github\_url  
hide

# AudioStreamSynchronized

**Inherits:** `AudioStream<class_AudioStream>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Stream that can be fitted with sub-streams, which will be played
in-sync.

classref-introduction-group

## Description

This is a stream that can be fitted with sub-streams, which will be
played in-sync. The streams being at exactly the same time when play is
pressed, and will end when the last of them ends. If one of the
sub-streams loops, then playback will continue.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**MAX\_STREAMS** = `32`
`🔗<class_AudioStreamSynchronized_constant_MAX_STREAMS>`

Maximum amount of streams that can be synchronized.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **stream\_count** = `0`
`🔗<class_AudioStreamSynchronized_property_stream_count>`

classref-property-setget

-   `void (No return value.)` **set\_stream\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_stream\_count**()

Set the total amount of streams that will be played back synchronized.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`AudioStream<class_AudioStream>` **get\_sync\_stream**(stream\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamSynchronized_method_get_sync_stream>`

Get one of the synchronized streams, by index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_sync\_stream\_volume**(stream\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AudioStreamSynchronized_method_get_sync_stream_volume>`

Get the volume of one of the synchronized streams, by index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_sync\_stream**(stream\_index:
`int<class_int>`, audio\_stream: `AudioStream<class_AudioStream>`)
`🔗<class_AudioStreamSynchronized_method_set_sync_stream>`

Set one of the synchronized streams, by index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_sync\_stream\_volume**(stream\_index:
`int<class_int>`, volume\_db: `float<class_float>`)
`🔗<class_AudioStreamSynchronized_method_set_sync_stream_volume>`

Set the volume of one of the synchronized streams, by index.
