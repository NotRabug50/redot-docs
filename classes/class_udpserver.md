github\_url  
hide

# UDPServer

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Helper class to implement a UDP server.

classref-introduction-group

## Description

A simple server that opens a UDP socket and returns connected
`PacketPeerUDP<class_PacketPeerUDP>` upon receiving new packets. See
also
`PacketPeerUDP.connect_to_host<class_PacketPeerUDP_method_connect_to_host>`.

After starting the server (`listen<class_UDPServer_method_listen>`), you
will need to `poll<class_UDPServer_method_poll>` it at regular intervals
(e.g. inside `Node._process<class_Node_private_method__process>`) for it
to process new packets, delivering them to the appropriate
`PacketPeerUDP<class_PacketPeerUDP>`, and taking new connections.

Below a small example of how it can be used:

gdscript

\# server\_node.gd class\_name ServerNode extends Node

var server := UDPServer.new() var peers = \[\]

func \_ready():  
server.listen(4242)

func \_process(delta):  
server.poll() \# Important! if server.is\_connection\_available(): var
peer: PacketPeerUDP = server.take\_connection() var packet =
peer.get\_packet() print("Accepted peer: %s:%s" %
\[peer.get\_packet\_ip(), peer.get\_packet\_port()\]) print("Received
data: %s" % \[packet.get\_string\_from\_utf8()\]) \# Reply so it knows
we received the message. peer.put\_packet(packet) \# Keep a reference so
we can keep contacting the remote peer. peers.append(peer)

for i in range(0, peers.size()):  
pass \# Do something with the connected peers.

csharp

// ServerNode.cs using Godot; using System.Collections.Generic;

public partial class ServerNode : Node { private UdpServer \_server =
new UdpServer(); private List&lt;PacketPeerUdp&gt; \_peers = new
List&lt;PacketPeerUdp&gt;();

> public override void \_Ready() { \_server.Listen(4242); }
>
> public override void \_Process(double delta) { \_server.Poll(); //
> Important! if (\_server.IsConnectionAvailable()) { PacketPeerUdp peer
> = \_server.TakeConnection(); byte\[\] packet = peer.GetPacket();
> GD.Print($"Accepted Peer:
> {peer.GetPacketIP()}:{peer.GetPacketPort()}"); GD.Print($"Received
> Data: {packet.GetStringFromUtf8()}"); // Reply so it knows we received
> the message. peer.PutPacket(packet); // Keep a reference so we can
> keep contacting the remote peer. \_peers.Add(peer); } foreach (var
> peer in \_peers) { // Do something with the peers. } }

}

gdscript

\# client\_node.gd class\_name ClientNode extends Node

var udp := PacketPeerUDP.new() var connected = false

func \_ready():  
udp.connect\_to\_host("127.0.0.1", 4242)

func \_process(delta):  
if !connected:  
\# Try to contact server udp.put\_packet("The answer is...
42!".to\_utf8\_buffer())

if udp.get\_available\_packet\_count() &gt; 0:  
print("Connected: %s" % udp.get\_packet().get\_string\_from\_utf8())
connected = true

csharp

// ClientNode.cs using Godot;

public partial class ClientNode : Node { private PacketPeerUdp \_udp =
new PacketPeerUdp(); private bool \_connected = false;

> public override void \_Ready() { \_udp.ConnectToHost("127.0.0.1",
> 4242); }
>
> public override void \_Process(double delta) { if (!\_connected) { //
> Try to contact server \_udp.PutPacket("The Answer
> Is..42!".ToUtf8Buffer()); } if (\_udp.GetAvailablePacketCount() &gt;
> 0) { GD.Print($"Connected: {\_udp.GetPacket().GetStringFromUtf8()}");
> \_connected = true; } }

}

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

`int<class_int>` **max\_pending\_connections** = `16`
`🔗<class_UDPServer_property_max_pending_connections>`

classref-property-setget

-   `void (No return value.)` **set\_max\_pending\_connections**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_pending\_connections**()

Define the maximum number of pending connections, during
`poll<class_UDPServer_method_poll>`, any new pending connection
exceeding that value will be automatically dropped. Setting this value
to `0` effectively prevents any new pending connection to be accepted
(e.g. when all your players have connected).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_local\_port**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UDPServer_method_get_local_port>`

Returns the local port this server is listening to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_connection\_available**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UDPServer_method_is_connection_available>`

Returns `true` if a packet with a new address/port combination was
received on the socket.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_listening**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UDPServer_method_is_listening>`

Returns `true` if the socket is open and listening on a port.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **listen**(port: `int<class_int>`,
bind\_address: `String<class_String>` = "\*")
`🔗<class_UDPServer_method_listen>`

Starts the server by opening a UDP socket listening on the given `port`.
You can optionally specify a `bind_address` to only listen for packets
sent to that address. See also
`PacketPeerUDP.bind<class_PacketPeerUDP_method_bind>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **poll**()
`🔗<class_UDPServer_method_poll>`

Call this method at regular intervals (e.g. inside
`Node._process<class_Node_private_method__process>`) to process new
packets. And packet from known address/port pair will be delivered to
the appropriate `PacketPeerUDP<class_PacketPeerUDP>`, any packet
received from an unknown address/port pair will be added as a pending
connection (see
`is_connection_available<class_UDPServer_method_is_connection_available>`,
`take_connection<class_UDPServer_method_take_connection>`). The maximum
number of pending connection is defined via
`max_pending_connections<class_UDPServer_property_max_pending_connections>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop**() `🔗<class_UDPServer_method_stop>`

Stops the server, closing the UDP socket if open. Will close all
connected `PacketPeerUDP<class_PacketPeerUDP>` accepted via
`take_connection<class_UDPServer_method_take_connection>` (remote peers
will not be notified).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PacketPeerUDP<class_PacketPeerUDP>` **take\_connection**()
`🔗<class_UDPServer_method_take_connection>`

Returns the first pending connection (connected to the appropriate
address/port). Will return `null` if no new connection is available. See
also
`is_connection_available<class_UDPServer_method_is_connection_available>`,
`PacketPeerUDP.connect_to_host<class_PacketPeerUDP_method_connect_to_host>`.
