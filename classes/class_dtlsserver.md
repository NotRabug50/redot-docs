github\_url  
hide

# DTLSServer

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Helper class to implement a DTLS server.

classref-introduction-group

## Description

This class is used to store the state of a DTLS server. Upon
`setup<class_DTLSServer_method_setup>` it converts connected
`PacketPeerUDP<class_PacketPeerUDP>` to
`PacketPeerDTLS<class_PacketPeerDTLS>` accepting them via
`take_connection<class_DTLSServer_method_take_connection>` as DTLS
clients. Under the hood, this class is used to store the DTLS state and
cookies of the server. The reason of why the state and cookies are
needed is outside of the scope of this documentation.

Below a small example of how to use it:

gdscript

\# server\_node.gd extends Node

var dtls := DTLSServer.new() var server := UDPServer.new() var peers =
\[\]

func \_ready():  
server.listen(4242) var key = load("key.key") \# Your private key. var
cert = load("cert.crt") \# Your X509 certificate. dtls.setup(key, cert)

func \_process(delta):  
while server.is\_connection\_available():  
var peer: PacketPeerUDP = server.take\_connection() var dtls\_peer:
PacketPeerDTLS = dtls.take\_connection(peer) if dtls\_peer.get\_status()
!= PacketPeerDTLS.STATUS\_HANDSHAKING: continue \# It is normal that 50%
of the connections fails due to cookie exchange. print("Peer
connected!") peers.append(dtls\_peer)

for p in peers:  
p.poll() \# Must poll to update the state. if p.get\_status() ==
PacketPeerDTLS.STATUS\_CONNECTED: while
p.get\_available\_packet\_count() &gt; 0: print("Received message from
client: %s" % p.get\_packet().get\_string\_from\_utf8())
p.put\_packet("Hello DTLS client".to\_utf8\_buffer())

csharp

// ServerNode.cs using Godot;

public partial class ServerNode : Node { private DtlsServer \_dtls = new
DtlsServer(); private UdpServer \_server = new UdpServer(); private
Godot.Collections.Array&lt;PacketPeerDtls&gt; \_peers = new
Godot.Collections.Array&lt;PacketPeerDtls&gt;();

> public override void \_Ready() { \_server.Listen(4242); var key =
> GD.Load&lt;CryptoKey&gt;("key.key"); // Your private key. var cert =
> GD.Load&lt;X509Certificate&gt;("cert.crt"); // Your X509 certificate.
> \_dtls.Setup(key, cert); }
>
> public override void \_Process(double delta) { while
> (Server.IsConnectionAvailable()) { PacketPeerUdp peer =
> \_server.TakeConnection(); PacketPeerDtls dtlsPeer =
> \_dtls.TakeConnection(peer); if (dtlsPeer.GetStatus() !=
> PacketPeerDtls.Status.Handshaking) { continue; // It is normal that
> 50% of the connections fails due to cookie exchange. } GD.Print("Peer
> connected!"); \_peers.Add(dtlsPeer); }
>
> > foreach (var p in \_peers) { p.Poll(); // Must poll to update the
> > state. if (p.GetStatus() == PacketPeerDtls.Status.Connected) { while
> > (p.GetAvailablePacketCount() &gt; 0) { GD.Print($"Received Message
> > From Client: {p.GetPacket().GetStringFromUtf8()}");
> > p.PutPacket("Hello DTLS Client".ToUtf8Buffer()); } } }
>
> }

}

gdscript

\# client\_node.gd extends Node

var dtls := PacketPeerDTLS.new() var udp := PacketPeerUDP.new() var
connected = false

func \_ready():  
udp.connect\_to\_host("127.0.0.1", 4242) dtls.connect\_to\_peer(udp,
false) \# Use true in production for certificate validation!

func \_process(delta):  
dtls.poll() if dtls.get\_status() == PacketPeerDTLS.STATUS\_CONNECTED:
if !connected: \# Try to contact server dtls.put\_packet("The answer
is... 42!".to\_utf8\_buffer()) while
dtls.get\_available\_packet\_count() &gt; 0: print("Connected: %s" %
dtls.get\_packet().get\_string\_from\_utf8()) connected = true

csharp

// ClientNode.cs using Godot; using System.Text;

public partial class ClientNode : Node { private PacketPeerDtls \_dtls =
new PacketPeerDtls(); private PacketPeerUdp \_udp = new PacketPeerUdp();
private bool \_connected = false;

> public override void \_Ready() { \_udp.ConnectToHost("127.0.0.1",
> 4242); \_dtls.ConnectToPeer(\_udp, validateCerts: false); // Use true
> in production for certificate validation! }
>
> public override void \_Process(double delta) { \_dtls.Poll(); if
> (\_dtls.GetStatus() == PacketPeerDtls.Status.Connected) { if
> (!\_connected) { // Try to contact server \_dtls.PutPacket("The Answer
> Is..42!".ToUtf8Buffer()); } while (\_dtls.GetAvailablePacketCount()
> &gt; 0) { GD.Print($"Connected:
> {\_dtls.GetPacket().GetStringFromUtf8()}"); \_connected = true; } } }

}

classref-reftable-group

## Methods

<table>
<tbody>
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

`Error<enum_@GlobalScope_Error>` **setup**(server\_options:
`TLSOptions<class_TLSOptions>`) `🔗<class_DTLSServer_method_setup>`

Setup the DTLS server to use the given `server_options`. See
`TLSOptions.server<class_TLSOptions_method_server>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PacketPeerDTLS<class_PacketPeerDTLS>` **take\_connection**(udp\_peer:
`PacketPeerUDP<class_PacketPeerUDP>`)
`🔗<class_DTLSServer_method_take_connection>`

Try to initiate the DTLS handshake with the given `udp_peer` which must
be already connected (see
`PacketPeerUDP.connect_to_host<class_PacketPeerUDP_method_connect_to_host>`).

\*\*Note:\*\* You must check that the state of the return PacketPeerUDP
is
`PacketPeerDTLS.STATUS_HANDSHAKING<class_PacketPeerDTLS_constant_STATUS_HANDSHAKING>`,
as it is normal that 50% of the new connections will be invalid due to
cookie exchange.
