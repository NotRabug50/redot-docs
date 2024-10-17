github\_url  
hide

# StreamPeerTLS

**Inherits:** `StreamPeer<class_StreamPeer>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A stream peer that handles TLS connections.

classref-introduction-group

## Description

A stream peer that handles TLS connections. This object can be used to
connect to a TLS server or accept a single TLS client connection.

\*\*Note:\*\* When exporting to Android, make sure to enable the
`INTERNET` permission in the Android export preset before exporting the
project or using one-click deploy. Otherwise, network communication of
any kind will be blocked by Android.

classref-introduction-group

## Tutorials

-   `TLS certificates <../tutorials/networking/ssl_certificates>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Status**: `🔗<enum_StreamPeerTLS_Status>`

classref-enumeration-constant

`Status<enum_StreamPeerTLS_Status>` **STATUS\_DISCONNECTED** = `0`

A status representing a **StreamPeerTLS** that is disconnected.

classref-enumeration-constant

`Status<enum_StreamPeerTLS_Status>` **STATUS\_HANDSHAKING** = `1`

A status representing a **StreamPeerTLS** during handshaking.

classref-enumeration-constant

`Status<enum_StreamPeerTLS_Status>` **STATUS\_CONNECTED** = `2`

A status representing a **StreamPeerTLS** that is connected to a host.

classref-enumeration-constant

`Status<enum_StreamPeerTLS_Status>` **STATUS\_ERROR** = `3`

A status representing a **StreamPeerTLS** in error state.

classref-enumeration-constant

`Status<enum_StreamPeerTLS_Status>`
**STATUS\_ERROR\_HOSTNAME\_MISMATCH** = `4`

An error status that shows a mismatch in the TLS certificate domain
presented by the host and the domain requested for validation.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **accept\_stream**(stream:
`StreamPeer<class_StreamPeer>`, server\_options:
`TLSOptions<class_TLSOptions>`)
`🔗<class_StreamPeerTLS_method_accept_stream>`

Accepts a peer connection as a server using the given `server_options`.
See `TLSOptions.server<class_TLSOptions_method_server>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **connect\_to\_stream**(stream:
`StreamPeer<class_StreamPeer>`, common\_name: `String<class_String>`,
client\_options: `TLSOptions<class_TLSOptions>` = null)
`🔗<class_StreamPeerTLS_method_connect_to_stream>`

Connects to a peer using an underlying `StreamPeer<class_StreamPeer>`
`stream` and verifying the remote certificate is correctly signed for
the given `common_name`. You can pass the optional `client_options`
parameter to customize the trusted certification authorities, or disable
the common name verification. See
`TLSOptions.client<class_TLSOptions_method_client>` and
`TLSOptions.client_unsafe<class_TLSOptions_method_client_unsafe>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **disconnect\_from\_stream**()
`🔗<class_StreamPeerTLS_method_disconnect_from_stream>`

Disconnects from host.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Status<enum_StreamPeerTLS_Status>` **get\_status**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StreamPeerTLS_method_get_status>`

Returns the status of the connection. See
`Status<enum_StreamPeerTLS_Status>` for values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StreamPeer<class_StreamPeer>` **get\_stream**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StreamPeerTLS_method_get_stream>`

Returns the underlying `StreamPeer<class_StreamPeer>` connection, used
in `accept_stream<class_StreamPeerTLS_method_accept_stream>` or
`connect_to_stream<class_StreamPeerTLS_method_connect_to_stream>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **poll**()
`🔗<class_StreamPeerTLS_method_poll>`

Poll the connection to check for incoming bytes. Call this right before
`StreamPeer.get_available_bytes<class_StreamPeer_method_get_available_bytes>`
for it to work properly.
