github\_url  
hide

# WebSocketMultiplayerPeer

**Inherits:** `MultiplayerPeer<class_MultiplayerPeer>` **&lt;**
`PacketPeer<class_PacketPeer>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Base class for WebSocket server and client.

classref-introduction-group

## Description

Base class for WebSocket server and client, allowing them to be used as
multiplayer peer for the `MultiplayerAPI<class_MultiplayerAPI>`.

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

`PackedStringArray<class_PackedStringArray>` **handshake\_headers** =
`PackedStringArray()`
`🔗<class_WebSocketMultiplayerPeer_property_handshake_headers>`

classref-property-setget

-   `void (No return value.)` **set\_handshake\_headers**(value:
    `PackedStringArray<class_PackedStringArray>`)
-   `PackedStringArray<class_PackedStringArray>`
    **get\_handshake\_headers**()

The extra headers to use during handshake. See
`WebSocketPeer.handshake_headers<class_WebSocketPeer_property_handshake_headers>`
for more details.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **handshake\_timeout** = `3.0`
`🔗<class_WebSocketMultiplayerPeer_property_handshake_timeout>`

classref-property-setget

-   `void (No return value.)` **set\_handshake\_timeout**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_handshake\_timeout**()

The maximum time each peer can stay in a connecting state before being
dropped.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **inbound\_buffer\_size** = `65535`
`🔗<class_WebSocketMultiplayerPeer_property_inbound_buffer_size>`

classref-property-setget

-   `void (No return value.)` **set\_inbound\_buffer\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_inbound\_buffer\_size**()

The inbound buffer size for connected peers. See
`WebSocketPeer.inbound_buffer_size<class_WebSocketPeer_property_inbound_buffer_size>`
for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_queued\_packets** = `2048`
`🔗<class_WebSocketMultiplayerPeer_property_max_queued_packets>`

classref-property-setget

-   `void (No return value.)` **set\_max\_queued\_packets**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_queued\_packets**()

The maximum number of queued packets for connected peers. See
`WebSocketPeer.max_queued_packets<class_WebSocketPeer_property_max_queued_packets>`
for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **outbound\_buffer\_size** = `65535`
`🔗<class_WebSocketMultiplayerPeer_property_outbound_buffer_size>`

classref-property-setget

-   `void (No return value.)` **set\_outbound\_buffer\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_outbound\_buffer\_size**()

The outbound buffer size for connected peers. See
`WebSocketPeer.outbound_buffer_size<class_WebSocketPeer_property_outbound_buffer_size>`
for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedStringArray<class_PackedStringArray>` **supported\_protocols** =
`PackedStringArray()`
`🔗<class_WebSocketMultiplayerPeer_property_supported_protocols>`

classref-property-setget

-   `void (No return value.)` **set\_supported\_protocols**(value:
    `PackedStringArray<class_PackedStringArray>`)
-   `PackedStringArray<class_PackedStringArray>`
    **get\_supported\_protocols**()

The supported WebSocket sub-protocols. See
`WebSocketPeer.supported_protocols<class_WebSocketPeer_property_supported_protocols>`
for more details.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **create\_client**(url:
`String<class_String>`, tls\_client\_options:
`TLSOptions<class_TLSOptions>` = null)
`🔗<class_WebSocketMultiplayerPeer_method_create_client>`

Starts a new multiplayer client connecting to the given `url`. TLS
certificates will be verified against the hostname when connecting using
the `wss://` protocol. You can pass the optional `tls_client_options`
parameter to customize the trusted certification authorities, or disable
the common name verification. See
`TLSOptions.client<class_TLSOptions_method_client>` and
`TLSOptions.client_unsafe<class_TLSOptions_method_client_unsafe>`.

\*\*Note:\*\* It is recommended to specify the scheme part of the URL,
i.e. the `url` should start with either `ws://` or `wss://`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **create\_server**(port:
`int<class_int>`, bind\_address: `String<class_String>` = "\*",
tls\_server\_options: `TLSOptions<class_TLSOptions>` = null)
`🔗<class_WebSocketMultiplayerPeer_method_create_server>`

Starts a new multiplayer server listening on the given `port`. You can
optionally specify a `bind_address`, and provide valid
`tls_server_options` to use TLS. See
`TLSOptions.server<class_TLSOptions_method_server>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`WebSocketPeer<class_WebSocketPeer>` **get\_peer**(peer\_id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketMultiplayerPeer_method_get_peer>`

Returns the `WebSocketPeer<class_WebSocketPeer>` associated to the given
`peer_id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_peer\_address**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketMultiplayerPeer_method_get_peer_address>`

Returns the IP address of the given peer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_peer\_port**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketMultiplayerPeer_method_get_peer_port>`

Returns the remote port of the given peer.
