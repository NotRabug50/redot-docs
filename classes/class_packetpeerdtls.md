github\_url  
hide

# PacketPeerDTLS

**Inherits:** `PacketPeer<class_PacketPeer>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

DTLS packet peer.

classref-introduction-group

## Description

This class represents a DTLS peer connection. It can be used to connect
to a DTLS server, and is returned by
`DTLSServer.take_connection<class_DTLSServer_method_take_connection>`.

\*\*Note:\*\* When exporting to Android, make sure to enable the
`INTERNET` permission in the Android export preset before exporting the
project or using one-click deploy. Otherwise, network communication of
any kind will be blocked by Android.

\*\*Warning:\*\* TLS certificate revocation and certificate pinning are
currently not supported. Revoked certificates are accepted as long as
they are otherwise valid. If this is a concern, you may want to use
automatically managed certificates with a short validity period.

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

## Enumerations

classref-enumeration

enum **Status**: `🔗<enum_PacketPeerDTLS_Status>`

classref-enumeration-constant

`Status<enum_PacketPeerDTLS_Status>` **STATUS\_DISCONNECTED** = `0`

A status representing a **PacketPeerDTLS** that is disconnected.

classref-enumeration-constant

`Status<enum_PacketPeerDTLS_Status>` **STATUS\_HANDSHAKING** = `1`

A status representing a **PacketPeerDTLS** that is currently performing
the handshake with a remote peer.

classref-enumeration-constant

`Status<enum_PacketPeerDTLS_Status>` **STATUS\_CONNECTED** = `2`

A status representing a **PacketPeerDTLS** that is connected to a remote
peer.

classref-enumeration-constant

`Status<enum_PacketPeerDTLS_Status>` **STATUS\_ERROR** = `3`

A status representing a **PacketPeerDTLS** in a generic error state.

classref-enumeration-constant

`Status<enum_PacketPeerDTLS_Status>`
**STATUS\_ERROR\_HOSTNAME\_MISMATCH** = `4`

An error status that shows a mismatch in the DTLS certificate domain
presented by the host and the domain requested for validation.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **connect\_to\_peer**(packet\_peer:
`PacketPeerUDP<class_PacketPeerUDP>`, hostname: `String<class_String>`,
client\_options: `TLSOptions<class_TLSOptions>` = null)
`🔗<class_PacketPeerDTLS_method_connect_to_peer>`

Connects a `packet_peer` beginning the DTLS handshake using the
underlying `PacketPeerUDP<class_PacketPeerUDP>` which must be connected
(see
`PacketPeerUDP.connect_to_host<class_PacketPeerUDP_method_connect_to_host>`).
You can optionally specify the `client_options` to be used while
verifying the TLS connections. See
`TLSOptions.client<class_TLSOptions_method_client>` and
`TLSOptions.client_unsafe<class_TLSOptions_method_client_unsafe>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **disconnect\_from\_peer**()
`🔗<class_PacketPeerDTLS_method_disconnect_from_peer>`

Disconnects this peer, terminating the DTLS session.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Status<enum_PacketPeerDTLS_Status>` **get\_status**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PacketPeerDTLS_method_get_status>`

Returns the status of the connection. See
`Status<enum_PacketPeerDTLS_Status>` for values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **poll**()
`🔗<class_PacketPeerDTLS_method_poll>`

Poll the connection to check for incoming packets. Call this frequently
to update the status and keep the connection working.
