github\_url  
hide

# StreamPeerGZIP

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `StreamPeer<class_StreamPeer>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A stream peer that handles GZIP and deflate compression/decompression.

classref-introduction-group

## Description

This class allows to compress or decompress data using GZIP/deflate in a
streaming fashion. This is particularly useful when compressing or
decompressing files that have to be sent through the network without
needing to allocate them all in memory.

After starting the stream via
`start_compression<class_StreamPeerGZIP_method_start_compression>` (or
`start_decompression<class_StreamPeerGZIP_method_start_decompression>`),
calling
`StreamPeer.put_partial_data<class_StreamPeer_method_put_partial_data>`
on this stream will compress (or decompress) the data, writing it to the
internal buffer. Calling
`StreamPeer.get_available_bytes<class_StreamPeer_method_get_available_bytes>`
will return the pending bytes in the internal buffer, and
`StreamPeer.get_partial_data<class_StreamPeer_method_get_partial_data>`
will retrieve the compressed (or decompressed) bytes from it. When the
stream is over, you must call
`finish<class_StreamPeerGZIP_method_finish>` to ensure the internal
buffer is properly flushed (make sure to call
`StreamPeer.get_available_bytes<class_StreamPeer_method_get_available_bytes>`
on last time to check if more data needs to be read after that).

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

## Method Descriptions

classref-method

`void (No return value.)` **clear**()
`🔗<class_StreamPeerGZIP_method_clear>`

Clears this stream, resetting the internal state.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **finish**()
`🔗<class_StreamPeerGZIP_method_finish>`

Finalizes the stream, compressing or decompressing any buffered chunk
left.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **start\_compression**(use\_deflate:
`bool<class_bool>` = false, buffer\_size: `int<class_int>` = 65535)
`🔗<class_StreamPeerGZIP_method_start_compression>`

Start the stream in compression mode with the given `buffer_size`, if
`use_deflate` is `true` uses deflate instead of GZIP.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **start\_decompression**(use\_deflate:
`bool<class_bool>` = false, buffer\_size: `int<class_int>` = 65535)
`🔗<class_StreamPeerGZIP_method_start_decompression>`

Start the stream in decompression mode with the given `buffer_size`, if
`use_deflate` is `true` uses deflate instead of GZIP.
