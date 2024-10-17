github\_url  
hide

# ENetPacketPeer

**Inherits:** `PacketPeer<class_PacketPeer>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A wrapper class for an
[ENetPeer](http://enet.bespin.org/group__peer.html).

classref-introduction-group

## Description

A PacketPeer implementation representing a peer of an
`ENetConnection<class_ENetConnection>`.

This class cannot be instantiated directly but can be retrieved during
`ENetConnection.service<class_ENetConnection_method_service>` or via
`ENetConnection.get_peers<class_ENetConnection_method_get_peers>`.

\*\*Note:\*\* When exporting to Android, make sure to enable the
`INTERNET` permission in the Android export preset before exporting the
project or using one-click deploy. Otherwise, network communication of
any kind will be blocked by Android.

classref-introduction-group

## Tutorials

-   [API documentation on the ENet
    website](http://enet.bespin.org/usergroup0.html)

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

enum **PeerState**: `🔗<enum_ENetPacketPeer_PeerState>`

classref-enumeration-constant

`PeerState<enum_ENetPacketPeer_PeerState>` **STATE\_DISCONNECTED** = `0`

The peer is disconnected.

classref-enumeration-constant

`PeerState<enum_ENetPacketPeer_PeerState>` **STATE\_CONNECTING** = `1`

The peer is currently attempting to connect.

classref-enumeration-constant

`PeerState<enum_ENetPacketPeer_PeerState>`
**STATE\_ACKNOWLEDGING\_CONNECT** = `2`

The peer has acknowledged the connection request.

classref-enumeration-constant

`PeerState<enum_ENetPacketPeer_PeerState>`
**STATE\_CONNECTION\_PENDING** = `3`

The peer is currently connecting.

classref-enumeration-constant

`PeerState<enum_ENetPacketPeer_PeerState>`
**STATE\_CONNECTION\_SUCCEEDED** = `4`

The peer has successfully connected, but is not ready to communicate
with yet
(`STATE_CONNECTED<class_ENetPacketPeer_constant_STATE_CONNECTED>`).

classref-enumeration-constant

`PeerState<enum_ENetPacketPeer_PeerState>` **STATE\_CONNECTED** = `5`

The peer is currently connected and ready to communicate with.

classref-enumeration-constant

`PeerState<enum_ENetPacketPeer_PeerState>` **STATE\_DISCONNECT\_LATER**
= `6`

The peer is slated to disconnect after it has no more outgoing packets
to send.

classref-enumeration-constant

`PeerState<enum_ENetPacketPeer_PeerState>` **STATE\_DISCONNECTING** =
`7`

The peer is currently disconnecting.

classref-enumeration-constant

`PeerState<enum_ENetPacketPeer_PeerState>`
**STATE\_ACKNOWLEDGING\_DISCONNECT** = `8`

The peer has acknowledged the disconnection request.

classref-enumeration-constant

`PeerState<enum_ENetPacketPeer_PeerState>` **STATE\_ZOMBIE** = `9`

The peer has lost connection, but is not considered truly disconnected
(as the peer didn't acknowledge the disconnection request).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PeerStatistic**: `🔗<enum_ENetPacketPeer_PeerStatistic>`

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_PACKET\_LOSS** = `0`

Mean packet loss of reliable packets as a ratio with respect to the
`PACKET_LOSS_SCALE<class_ENetPacketPeer_constant_PACKET_LOSS_SCALE>`.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_PACKET\_LOSS\_VARIANCE** = `1`

Packet loss variance.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_PACKET\_LOSS\_EPOCH** = `2`

The time at which packet loss statistics were last updated (in
milliseconds since the connection started). The interval for packet loss
statistics updates is 10 seconds, and at least one packet must have been
sent since the last statistics update.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_ROUND\_TRIP\_TIME** = `3`

Mean packet round trip time for reliable packets.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_ROUND\_TRIP\_TIME\_VARIANCE** = `4`

Variance of the mean round trip time.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_LAST\_ROUND\_TRIP\_TIME** = `5`

Last recorded round trip time for a reliable packet.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_LAST\_ROUND\_TRIP\_TIME\_VARIANCE** = `6`

Variance of the last trip time recorded.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_PACKET\_THROTTLE** = `7`

The peer's current throttle status.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_PACKET\_THROTTLE\_LIMIT** = `8`

The maximum number of unreliable packets that should not be dropped.
This value is always greater than or equal to `1`. The initial value is
equal to
`PACKET_THROTTLE_SCALE<class_ENetPacketPeer_constant_PACKET_THROTTLE_SCALE>`.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_PACKET\_THROTTLE\_COUNTER** = `9`

Internal value used to increment the packet throttle counter. The value
is hardcoded to `7` and cannot be changed. You probably want to look at
`PEER_PACKET_THROTTLE_ACCELERATION<class_ENetPacketPeer_constant_PEER_PACKET_THROTTLE_ACCELERATION>`
instead.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_PACKET\_THROTTLE\_EPOCH** = `10`

The time at which throttle statistics were last updated (in milliseconds
since the connection started). The interval for throttle statistics
updates is
`PEER_PACKET_THROTTLE_INTERVAL<class_ENetPacketPeer_constant_PEER_PACKET_THROTTLE_INTERVAL>`.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_PACKET\_THROTTLE\_ACCELERATION** = `11`

The throttle's acceleration factor. Higher values will make ENet adapt
to fluctuating network conditions faster, causing unrelaible packets to
be sent *more* often. The default value is `2`.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_PACKET\_THROTTLE\_DECELERATION** = `12`

The throttle's deceleration factor. Higher values will make ENet adapt
to fluctuating network conditions faster, causing unrelaible packets to
be sent *less* often. The default value is `2`.

classref-enumeration-constant

`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`
**PEER\_PACKET\_THROTTLE\_INTERVAL** = `13`

The interval over which the lowest mean round trip time should be
measured for use by the throttle mechanism (in milliseconds). The
default value is `5000`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**PACKET\_LOSS\_SCALE** = `65536`
`🔗<class_ENetPacketPeer_constant_PACKET_LOSS_SCALE>`

The reference scale for packet loss. See
`get_statistic<class_ENetPacketPeer_method_get_statistic>` and
`PEER_PACKET_LOSS<class_ENetPacketPeer_constant_PEER_PACKET_LOSS>`.

classref-constant

**PACKET\_THROTTLE\_SCALE** = `32`
`🔗<class_ENetPacketPeer_constant_PACKET_THROTTLE_SCALE>`

The reference value for throttle configuration. The default value is
`32`. See
`throttle_configure<class_ENetPacketPeer_method_throttle_configure>`.

classref-constant

**FLAG\_RELIABLE** = `1`
`🔗<class_ENetPacketPeer_constant_FLAG_RELIABLE>`

Mark the packet to be sent as reliable.

classref-constant

**FLAG\_UNSEQUENCED** = `2`
`🔗<class_ENetPacketPeer_constant_FLAG_UNSEQUENCED>`

Mark the packet to be sent unsequenced (unreliable).

classref-constant

**FLAG\_UNRELIABLE\_FRAGMENT** = `8`
`🔗<class_ENetPacketPeer_constant_FLAG_UNRELIABLE_FRAGMENT>`

Mark the packet to be sent unreliable even if the packet is too big and
needs fragmentation (increasing the chance of it being dropped).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_channels**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ENetPacketPeer_method_get_channels>`

Returns the number of channels allocated for communication with peer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_packet\_flags**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ENetPacketPeer_method_get_packet_flags>`

Returns the ENet flags of the next packet in the received queue. See
`FLAG_*` constants for available packet flags. Note that not all flags
are replicated from the sending peer to the receiving peer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_remote\_address**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ENetPacketPeer_method_get_remote_address>`

Returns the IP address of this peer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_remote\_port**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ENetPacketPeer_method_get_remote_port>`

Returns the remote port of this peer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PeerState<enum_ENetPacketPeer_PeerState>` **get\_state**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ENetPacketPeer_method_get_state>`

Returns the current peer state. See
`PeerState<enum_ENetPacketPeer_PeerState>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_statistic**(statistic:
`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`)
`🔗<class_ENetPacketPeer_method_get_statistic>`

Returns the requested `statistic` for this peer. See
`PeerStatistic<enum_ENetPacketPeer_PeerStatistic>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_active**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ENetPacketPeer_method_is_active>`

Returns `true` if the peer is currently active (i.e. the associated
`ENetConnection<class_ENetConnection>` is still valid).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **peer\_disconnect**(data: `int<class_int>` =
0) `🔗<class_ENetPacketPeer_method_peer_disconnect>`

Request a disconnection from a peer. An
`ENetConnection.EVENT_DISCONNECT<class_ENetConnection_constant_EVENT_DISCONNECT>`
will be generated during
`ENetConnection.service<class_ENetConnection_method_service>` once the
disconnection is complete.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **peer\_disconnect\_later**(data:
`int<class_int>` = 0)
`🔗<class_ENetPacketPeer_method_peer_disconnect_later>`

Request a disconnection from a peer, but only after all queued outgoing
packets are sent. An
`ENetConnection.EVENT_DISCONNECT<class_ENetConnection_constant_EVENT_DISCONNECT>`
will be generated during
`ENetConnection.service<class_ENetConnection_method_service>` once the
disconnection is complete.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **peer\_disconnect\_now**(data:
`int<class_int>` = 0)
`🔗<class_ENetPacketPeer_method_peer_disconnect_now>`

Force an immediate disconnection from a peer. No
`ENetConnection.EVENT_DISCONNECT<class_ENetConnection_constant_EVENT_DISCONNECT>`
will be generated. The foreign peer is not guaranteed to receive the
disconnect notification, and is reset immediately upon return from this
function.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **ping**()
`🔗<class_ENetPacketPeer_method_ping>`

Sends a ping request to a peer. ENet automatically pings all connected
peers at regular intervals, however, this function may be called to
ensure more frequent ping requests.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **ping\_interval**(ping\_interval:
`int<class_int>`) `🔗<class_ENetPacketPeer_method_ping_interval>`

Sets the `ping_interval` in milliseconds at which pings will be sent to
a peer. Pings are used both to monitor the liveness of the connection
and also to dynamically adjust the throttle during periods of low
traffic so that the throttle has reasonable responsiveness during
traffic spikes. The default ping interval is `500` milliseconds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reset**()
`🔗<class_ENetPacketPeer_method_reset>`

Forcefully disconnects a peer. The foreign host represented by the peer
is not notified of the disconnection and will timeout on its connection
to the local host.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **send**(channel: `int<class_int>`,
packet: `PackedByteArray<class_PackedByteArray>`, flags:
`int<class_int>`) `🔗<class_ENetPacketPeer_method_send>`

Queues a `packet` to be sent over the specified `channel`. See `FLAG_*`
constants for available packet flags.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_timeout**(timeout: `int<class_int>`,
timeout\_min: `int<class_int>`, timeout\_max: `int<class_int>`)
`🔗<class_ENetPacketPeer_method_set_timeout>`

Sets the timeout parameters for a peer. The timeout parameters control
how and when a peer will timeout from a failure to acknowledge reliable
traffic. Timeout values are expressed in milliseconds.

The `timeout` is a factor that, multiplied by a value based on the
average round trip time, will determine the timeout limit for a reliable
packet. When that limit is reached, the timeout will be doubled, and the
peer will be disconnected if that limit has reached `timeout_min`. The
`timeout_max` parameter, on the other hand, defines a fixed timeout for
which any packet must be acknowledged or the peer will be dropped.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **throttle\_configure**(interval:
`int<class_int>`, acceleration: `int<class_int>`, deceleration:
`int<class_int>`) `🔗<class_ENetPacketPeer_method_throttle_configure>`

Configures throttle parameter for a peer.

Unreliable packets are dropped by ENet in response to the varying
conditions of the Internet connection to the peer. The throttle
represents a probability that an unreliable packet should not be dropped
and thus sent by ENet to the peer. By measuring fluctuations in round
trip times of reliable packets over the specified `interval`, ENet will
either increase the probability by the amount specified in the
`acceleration` parameter, or decrease it by the amount specified in the
`deceleration` parameter (both are ratios to
`PACKET_THROTTLE_SCALE<class_ENetPacketPeer_constant_PACKET_THROTTLE_SCALE>`).

When the throttle has a value of
`PACKET_THROTTLE_SCALE<class_ENetPacketPeer_constant_PACKET_THROTTLE_SCALE>`,
no unreliable packets are dropped by ENet, and so 100% of all unreliable
packets will be sent.

When the throttle has a value of `0`, all unreliable packets are dropped
by ENet, and so 0% of all unreliable packets will be sent.

Intermediate values for the throttle represent intermediate
probabilities between 0% and 100% of unreliable packets being sent. The
bandwidth limits of the local and foreign hosts are taken into account
to determine a sensible limit for the throttle probability above which
it should not raise even in the best of conditions.
