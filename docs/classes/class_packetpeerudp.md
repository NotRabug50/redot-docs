github\_url  
hide

# PacketPeerUDP

**Inherits:** `PacketPeer<class_PacketPeer>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

UDP packet peer.

classref-introduction-group

## Description

UDP packet peer. Can be used to send raw UDP packets as well as
`Variant<class_Variant>`s.

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

`Error<enum_@GlobalScope_Error>` **bind**(port: `int<class_int>`,
bind\_address: `String<class_String>` = "\*", recv\_buf\_size:
`int<class_int>` = 65536) `🔗<class_PacketPeerUDP_method_bind>`

Binds this **PacketPeerUDP** to the specified `port` and `bind_address`
with a buffer size `recv_buf_size`, allowing it to receive incoming
packets.

If `bind_address` is set to `"*"` (default), the peer will be bound on
all available addresses (both IPv4 and IPv6).

If `bind_address` is set to `"0.0.0.0"` (for IPv4) or `"::"` (for IPv6),
the peer will be bound to all available addresses matching that IP type.

If `bind_address` is set to any valid address (e.g. `"192.168.1.101"`,
`"::1"`, etc.), the peer will only be bound to the interface with that
address (or fail if no interface with the given address exists).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **close**()
`🔗<class_PacketPeerUDP_method_close>`

Closes the **PacketPeerUDP**'s underlying UDP socket.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **connect\_to\_host**(host:
`String<class_String>`, port: `int<class_int>`)
`🔗<class_PacketPeerUDP_method_connect_to_host>`

Calling this method connects this UDP peer to the given `host`/`port`
pair. UDP is in reality connectionless, so this option only means that
incoming packets from different addresses are automatically discarded,
and that outgoing packets are always sent to the connected address
(future calls to
`set_dest_address<class_PacketPeerUDP_method_set_dest_address>` are not
allowed). This method does not send any data to the remote peer, to do
that, use `PacketPeer.put_var<class_PacketPeer_method_put_var>` or
`PacketPeer.put_packet<class_PacketPeer_method_put_packet>` as usual.
See also `UDPServer<class_UDPServer>`.

\*\*Note:\*\* Connecting to the remote peer does not help to protect
from malicious attacks like IP spoofing, etc. Think about using an
encryption technique like TLS or DTLS if you feel like your application
is transferring sensitive information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_local\_port**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PacketPeerUDP_method_get_local_port>`

Returns the local port to which this peer is bound.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_packet\_ip**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PacketPeerUDP_method_get_packet_ip>`

Returns the IP of the remote peer that sent the last packet(that was
received with
`PacketPeer.get_packet<class_PacketPeer_method_get_packet>` or
`PacketPeer.get_var<class_PacketPeer_method_get_var>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_packet\_port**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PacketPeerUDP_method_get_packet_port>`

Returns the port of the remote peer that sent the last packet(that was
received with
`PacketPeer.get_packet<class_PacketPeer_method_get_packet>` or
`PacketPeer.get_var<class_PacketPeer_method_get_var>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_bound**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PacketPeerUDP_method_is_bound>`

Returns whether this **PacketPeerUDP** is bound to an address and can
receive packets.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_socket\_connected**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PacketPeerUDP_method_is_socket_connected>`

Returns `true` if the UDP socket is open and has been connected to a
remote address. See
`connect_to_host<class_PacketPeerUDP_method_connect_to_host>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**join\_multicast\_group**(multicast\_address: `String<class_String>`,
interface\_name: `String<class_String>`)
`🔗<class_PacketPeerUDP_method_join_multicast_group>`

Joins the multicast group specified by `multicast_address` using the
interface identified by `interface_name`.

You can join the same multicast group with multiple interfaces. Use
`IP.get_local_interfaces<class_IP_method_get_local_interfaces>` to know
which are available.

\*\*Note:\*\* Some Android devices might require the
`CHANGE_WIFI_MULTICAST_STATE` permission for multicast to work.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**leave\_multicast\_group**(multicast\_address: `String<class_String>`,
interface\_name: `String<class_String>`)
`🔗<class_PacketPeerUDP_method_leave_multicast_group>`

Removes the interface identified by `interface_name` from the multicast
group specified by `multicast_address`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_broadcast\_enabled**(enabled:
`bool<class_bool>`)
`🔗<class_PacketPeerUDP_method_set_broadcast_enabled>`

Enable or disable sending of broadcast packets (e.g.
`set_dest_address("255.255.255.255", 4343)`. This option is disabled by
default.

\*\*Note:\*\* Some Android devices might require the
`CHANGE_WIFI_MULTICAST_STATE` permission and this option to be enabled
to receive broadcast packets too.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **set\_dest\_address**(host:
`String<class_String>`, port: `int<class_int>`)
`🔗<class_PacketPeerUDP_method_set_dest_address>`

Sets the destination address and port for sending packets and variables.
A hostname will be resolved using DNS if needed.

\*\*Note:\*\*
`set_broadcast_enabled<class_PacketPeerUDP_method_set_broadcast_enabled>`
must be enabled before sending packets to a broadcast address (e.g.
`255.255.255.255`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **wait**()
`🔗<class_PacketPeerUDP_method_wait>`

Waits for a packet to arrive on the bound address. See
`bind<class_PacketPeerUDP_method_bind>`.

\*\*Note:\*\* `wait<class_PacketPeerUDP_method_wait>` can't be
interrupted once it has been called. This can be worked around by
allowing the other party to send a specific "death pill" packet like
this:

gdscript

socket = PacketPeerUDP.new() \# Server
socket.set\_dest\_address("127.0.0.1", 789) socket.put\_packet("Time to
stop".to\_ascii\_buffer())

\# Client while socket.wait() == OK: var data =
socket.get\_packet().get\_string\_from\_ascii() if data == "Time to
stop": return

csharp

var socket = new PacketPeerUdp(); // Server
socket.SetDestAddress("127.0.0.1", 789); socket.PutPacket("Time to
stop".ToAsciiBuffer());

// Client while (socket.Wait() == OK) { string data =
socket.GetPacket().GetStringFromASCII(); if (data == "Time to stop") {
return; } }
