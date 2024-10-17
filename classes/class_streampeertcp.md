github\_url  
hide

# StreamPeerTCP

**Inherits:** `StreamPeer<class_StreamPeer>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A stream peer that handles TCP connections.

classref-introduction-group

## Description

A stream peer that handles TCP connections. This object can be used to
connect to TCP servers, or also is returned by a TCP server.

\*\*Note:\*\* When exporting to Android, make sure to enable the
`INTERNET` permission in the Android export preset before exporting the
project or using one-click deploy. Otherwise, network communication of
any kind will be blocked by Android.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Status**: `🔗<enum_StreamPeerTCP_Status>`

classref-enumeration-constant

`Status<enum_StreamPeerTCP_Status>` **STATUS\_NONE** = `0`

The initial status of the **StreamPeerTCP**. This is also the status
after disconnecting.

classref-enumeration-constant

`Status<enum_StreamPeerTCP_Status>` **STATUS\_CONNECTING** = `1`

A status representing a **StreamPeerTCP** that is connecting to a host.

classref-enumeration-constant

`Status<enum_StreamPeerTCP_Status>` **STATUS\_CONNECTED** = `2`

A status representing a **StreamPeerTCP** that is connected to a host.

classref-enumeration-constant

`Status<enum_StreamPeerTCP_Status>` **STATUS\_ERROR** = `3`

A status representing a **StreamPeerTCP** in error state.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **bind**(port: `int<class_int>`, host:
`String<class_String>` = "\*") `🔗<class_StreamPeerTCP_method_bind>`

Opens the TCP socket, and binds it to the specified local address.

This method is generally not needed, and only used to force the
subsequent call to
`connect_to_host<class_StreamPeerTCP_method_connect_to_host>` to use the
specified `host` and `port` as source address. This can be desired in
some NAT punchthrough techniques, or when forcing the source network
interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **connect\_to\_host**(host:
`String<class_String>`, port: `int<class_int>`)
`🔗<class_StreamPeerTCP_method_connect_to_host>`

Connects to the specified `host:port` pair. A hostname will be resolved
if valid. Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on
success.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **disconnect\_from\_host**()
`🔗<class_StreamPeerTCP_method_disconnect_from_host>`

Disconnects from host.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_connected\_host**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StreamPeerTCP_method_get_connected_host>`

Returns the IP of this peer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_connected\_port**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StreamPeerTCP_method_get_connected_port>`

Returns the port of this peer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_local\_port**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StreamPeerTCP_method_get_local_port>`

Returns the local port to which this peer is bound.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Status<enum_StreamPeerTCP_Status>` **get\_status**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StreamPeerTCP_method_get_status>`

Returns the status of the connection, see
`Status<enum_StreamPeerTCP_Status>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **poll**()
`🔗<class_StreamPeerTCP_method_poll>`

Poll the socket, updating its state. See
`get_status<class_StreamPeerTCP_method_get_status>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_no\_delay**(enabled:
`bool<class_bool>`) `🔗<class_StreamPeerTCP_method_set_no_delay>`

If `enabled` is `true`, packets will be sent immediately. If `enabled`
is `false` (the default), packet transfers will be delayed and combined
using [Nagle's
algorithm](https://en.wikipedia.org/wiki/Nagle%27s_algorithm).

\*\*Note:\*\* It's recommended to leave this disabled for applications
that send large packets or need to transfer a lot of data, as enabling
this can decrease the total available bandwidth.
