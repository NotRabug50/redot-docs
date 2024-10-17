github\_url  
hide

# PacketPeerStream

**Inherits:** `PacketPeer<class_PacketPeer>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Wrapper to use a PacketPeer over a StreamPeer.

classref-introduction-group

## Description

PacketStreamPeer provides a wrapper for working using packets over a
stream. This allows for using packet based code with StreamPeers.
PacketPeerStream implements a custom protocol over the StreamPeer, so
the user should not read or write to the wrapped StreamPeer directly.

\*\*Note:\*\* When exporting to Android, make sure to enable the
`INTERNET` permission in the Android export preset before exporting the
project or using one-click deploy. Otherwise, network communication of
any kind will be blocked by Android.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **input\_buffer\_max\_size** = `65532`
`🔗<class_PacketPeerStream_property_input_buffer_max_size>`

classref-property-setget

-   `void (No return value.)` **set\_input\_buffer\_max\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_input\_buffer\_max\_size**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **output\_buffer\_max\_size** = `65532`
`🔗<class_PacketPeerStream_property_output_buffer_max_size>`

classref-property-setget

-   `void (No return value.)` **set\_output\_buffer\_max\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_output\_buffer\_max\_size**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`StreamPeer<class_StreamPeer>` **stream\_peer**
`🔗<class_PacketPeerStream_property_stream_peer>`

classref-property-setget

-   `void (No return value.)` **set\_stream\_peer**(value:
    `StreamPeer<class_StreamPeer>`)
-   `StreamPeer<class_StreamPeer>` **get\_stream\_peer**()

The wrapped `StreamPeer<class_StreamPeer>` object.
