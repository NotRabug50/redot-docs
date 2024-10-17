github\_url  
hide

# WebSocketPeer

**Inherits:** `PacketPeer<class_PacketPeer>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A WebSocket connection.

classref-introduction-group

## Description

This class represents WebSocket connection, and can be used as a
WebSocket client (RFC 6455-compliant) or as a remote peer of a WebSocket
server.

You can send WebSocket binary frames using
`PacketPeer.put_packet<class_PacketPeer_method_put_packet>`, and
WebSocket text frames using `send<class_WebSocketPeer_method_send>`
(prefer text frames when interacting with text-based API). You can check
the frame type of the last packet via
`was_string_packet<class_WebSocketPeer_method_was_string_packet>`.

To start a WebSocket client, first call
`connect_to_url<class_WebSocketPeer_method_connect_to_url>`, then
regularly call `poll<class_WebSocketPeer_method_poll>` (e.g. during
`Node<class_Node>` process). You can query the socket state via
`get_ready_state<class_WebSocketPeer_method_get_ready_state>`, get the
number of pending packets using
`PacketPeer.get_available_packet_count<class_PacketPeer_method_get_available_packet_count>`,
and retrieve them via
`PacketPeer.get_packet<class_PacketPeer_method_get_packet>`.

gdscript

extends Node

var socket = WebSocketPeer.new()

func \_ready():  
socket.connect\_to\_url("<wss://example.com>")

func \_process(delta):  
socket.poll() var state = socket.get\_ready\_state() if state ==
WebSocketPeer.STATE\_OPEN: while socket.get\_available\_packet\_count():
print("Packet: ", socket.get\_packet()) elif state ==
WebSocketPeer.STATE\_CLOSING: \# Keep polling to achieve proper close.
pass elif state == WebSocketPeer.STATE\_CLOSED: var code =
socket.get\_close\_code() var reason = socket.get\_close\_reason()
print("WebSocket closed with code: %d, reason %s. Clean: %s" % \[code,
reason, code != -1\]) set\_process(false) \# Stop processing.

To use the peer as part of a WebSocket server refer to
`accept_stream<class_WebSocketPeer_method_accept_stream>` and the online
tutorial.

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
<tr>
</tr>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **WriteMode**: `🔗<enum_WebSocketPeer_WriteMode>`

classref-enumeration-constant

`WriteMode<enum_WebSocketPeer_WriteMode>` **WRITE\_MODE\_TEXT** = `0`

Specifies that WebSockets messages should be transferred as text payload
(only valid UTF-8 is allowed).

classref-enumeration-constant

`WriteMode<enum_WebSocketPeer_WriteMode>` **WRITE\_MODE\_BINARY** = `1`

Specifies that WebSockets messages should be transferred as binary
payload (any byte combination is allowed).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **State**: `🔗<enum_WebSocketPeer_State>`

classref-enumeration-constant

`State<enum_WebSocketPeer_State>` **STATE\_CONNECTING** = `0`

Socket has been created. The connection is not yet open.

classref-enumeration-constant

`State<enum_WebSocketPeer_State>` **STATE\_OPEN** = `1`

The connection is open and ready to communicate.

classref-enumeration-constant

`State<enum_WebSocketPeer_State>` **STATE\_CLOSING** = `2`

The connection is in the process of closing. This means a close request
has been sent to the remote peer but confirmation has not been received.

classref-enumeration-constant

`State<enum_WebSocketPeer_State>` **STATE\_CLOSED** = `3`

The connection is closed or couldn't be opened.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`PackedStringArray<class_PackedStringArray>` **handshake\_headers** =
`PackedStringArray()`
`🔗<class_WebSocketPeer_property_handshake_headers>`

classref-property-setget

-   `void (No return value.)` **set\_handshake\_headers**(value:
    `PackedStringArray<class_PackedStringArray>`)
-   `PackedStringArray<class_PackedStringArray>`
    **get\_handshake\_headers**()

The extra HTTP headers to be sent during the WebSocket handshake.

\*\*Note:\*\* Not supported in Web exports due to browsers'
restrictions.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **inbound\_buffer\_size** = `65535`
`🔗<class_WebSocketPeer_property_inbound_buffer_size>`

classref-property-setget

-   `void (No return value.)` **set\_inbound\_buffer\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_inbound\_buffer\_size**()

The size of the input buffer in bytes (roughly the maximum amount of
memory that will be allocated for the inbound packets).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_queued\_packets** = `2048`
`🔗<class_WebSocketPeer_property_max_queued_packets>`

classref-property-setget

-   `void (No return value.)` **set\_max\_queued\_packets**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_queued\_packets**()

The maximum amount of packets that will be allowed in the queues (both
inbound and outbound).

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **outbound\_buffer\_size** = `65535`
`🔗<class_WebSocketPeer_property_outbound_buffer_size>`

classref-property-setget

-   `void (No return value.)` **set\_outbound\_buffer\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_outbound\_buffer\_size**()

The size of the input buffer in bytes (roughly the maximum amount of
memory that will be allocated for the outbound packets).

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedStringArray<class_PackedStringArray>` **supported\_protocols** =
`PackedStringArray()`
`🔗<class_WebSocketPeer_property_supported_protocols>`

classref-property-setget

-   `void (No return value.)` **set\_supported\_protocols**(value:
    `PackedStringArray<class_PackedStringArray>`)
-   `PackedStringArray<class_PackedStringArray>`
    **get\_supported\_protocols**()

The WebSocket sub-protocols allowed during the WebSocket handshake.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedStringArray<class_PackedStringArray>` for more details.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **accept\_stream**(stream:
`StreamPeer<class_StreamPeer>`)
`🔗<class_WebSocketPeer_method_accept_stream>`

Accepts a peer connection performing the HTTP handshake as a WebSocket
server. The `stream` must be a valid TCP stream retrieved via
`TCPServer.take_connection<class_TCPServer_method_take_connection>`, or
a TLS stream accepted via
`StreamPeerTLS.accept_stream<class_StreamPeerTLS_method_accept_stream>`.

\*\*Note:\*\* Not supported in Web exports due to browsers'
restrictions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **close**(code: `int<class_int>` = 1000,
reason: `String<class_String>` = "")
`🔗<class_WebSocketPeer_method_close>`

Closes this WebSocket connection. `code` is the status code for the
closure (see RFC 6455 section 7.4 for a list of valid status codes).
`reason` is the human readable reason for closing the connection (can be
any UTF-8 string that's smaller than 123 bytes). If `code` is negative,
the connection will be closed immediately without notifying the remote
peer.

\*\*Note:\*\* To achieve a clean close, you will need to keep polling
until `STATE_CLOSED<class_WebSocketPeer_constant_STATE_CLOSED>` is
reached.

\*\*Note:\*\* The Web export might not support all status codes. Please
refer to browser-specific documentation for more details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **connect\_to\_url**(url:
`String<class_String>`, tls\_client\_options:
`TLSOptions<class_TLSOptions>` = null)
`🔗<class_WebSocketPeer_method_connect_to_url>`

Connects to the given URL. TLS certificates will be verified against the
hostname when connecting using the `wss://` protocol. You can pass the
optional `tls_client_options` parameter to customize the trusted
certification authorities, or disable the common name verification. See
`TLSOptions.client<class_TLSOptions_method_client>` and
`TLSOptions.client_unsafe<class_TLSOptions_method_client_unsafe>`.

\*\*Note:\*\* To avoid mixed content warnings or errors in Web, you may
have to use a `url` that starts with `wss://` (secure) instead of
`ws://`. When doing so, make sure to use the fully qualified domain name
that matches the one defined in the server's TLS certificate. Do not
connect directly via the IP address for `wss://` connections, as it
won't match with the TLS certificate.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_close\_code**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketPeer_method_get_close_code>`

Returns the received WebSocket close frame status code, or `-1` when the
connection was not cleanly closed. Only call this method when
`get_ready_state<class_WebSocketPeer_method_get_ready_state>` returns
`STATE_CLOSED<class_WebSocketPeer_constant_STATE_CLOSED>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_close\_reason**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketPeer_method_get_close_reason>`

Returns the received WebSocket close frame status reason string. Only
call this method when
`get_ready_state<class_WebSocketPeer_method_get_ready_state>` returns
`STATE_CLOSED<class_WebSocketPeer_constant_STATE_CLOSED>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_connected\_host**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketPeer_method_get_connected_host>`

Returns the IP address of the connected peer.

\*\*Note:\*\* Not available in the Web export.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_connected\_port**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketPeer_method_get_connected_port>`

Returns the remote port of the connected peer.

\*\*Note:\*\* Not available in the Web export.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_current\_outbound\_buffered\_amount**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketPeer_method_get_current_outbound_buffered_amount>`

Returns the current amount of data in the outbound websocket buffer.
**Note:** Web exports use WebSocket.bufferedAmount, while other
platforms use an internal buffer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`State<enum_WebSocketPeer_State>` **get\_ready\_state**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketPeer_method_get_ready_state>`

Returns the ready state of the connection. See
`State<enum_WebSocketPeer_State>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_requested\_url**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketPeer_method_get_requested_url>`

Returns the URL requested by this peer. The URL is derived from the
`url` passed to
`connect_to_url<class_WebSocketPeer_method_connect_to_url>` or from the
HTTP headers when acting as server (i.e. when using
`accept_stream<class_WebSocketPeer_method_accept_stream>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_selected\_protocol**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketPeer_method_get_selected_protocol>`

Returns the selected WebSocket sub-protocol for this connection or an
empty string if the sub-protocol has not been selected yet.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **poll**()
`🔗<class_WebSocketPeer_method_poll>`

Updates the connection state and receive incoming packets. Call this
function regularly to keep it in a clean state.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **send**(message:
`PackedByteArray<class_PackedByteArray>`, write\_mode:
`WriteMode<enum_WebSocketPeer_WriteMode>` = 1)
`🔗<class_WebSocketPeer_method_send>`

Sends the given `message` using the desired `write_mode`. When sending a
`String<class_String>`, prefer using
`send_text<class_WebSocketPeer_method_send_text>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **send\_text**(message:
`String<class_String>`) `🔗<class_WebSocketPeer_method_send_text>`

Sends the given `message` using WebSocket text mode. Prefer this method
over `PacketPeer.put_packet<class_PacketPeer_method_put_packet>` when
interacting with third-party text-based API (e.g. when using
`JSON<class_JSON>` formatted messages).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_no\_delay**(enabled:
`bool<class_bool>`) `🔗<class_WebSocketPeer_method_set_no_delay>`

Disable Nagle's algorithm on the underlying TCP socket (default). See
`StreamPeerTCP.set_no_delay<class_StreamPeerTCP_method_set_no_delay>`
for more information.

\*\*Note:\*\* Not available in the Web export.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **was\_string\_packet**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebSocketPeer_method_was_string_packet>`

Returns `true` if the last received packet was sent as a text payload.
See `WriteMode<enum_WebSocketPeer_WriteMode>`.
