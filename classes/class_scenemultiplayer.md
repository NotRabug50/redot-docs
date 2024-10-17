github\_url  
hide

# SceneMultiplayer

**Inherits:** `MultiplayerAPI<class_MultiplayerAPI>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

High-level multiplayer API implementation.

classref-introduction-group

## Description

This class is the default implementation of
`MultiplayerAPI<class_MultiplayerAPI>`, used to provide multiplayer
functionalities in Godot Engine.

This implementation supports RPCs via `Node.rpc<class_Node_method_rpc>`
and `Node.rpc_id<class_Node_method_rpc_id>` and requires
`MultiplayerAPI.rpc<class_MultiplayerAPI_method_rpc>` to be passed a
`Node<class_Node>` (it will fail for other object types).

This implementation additionally provide `SceneTree<class_SceneTree>`
replication via the `MultiplayerSpawner<class_MultiplayerSpawner>` and
`MultiplayerSynchronizer<class_MultiplayerSynchronizer>` nodes, and the
`SceneReplicationConfig<class_SceneReplicationConfig>` resource.

\*\*Note:\*\* The high-level multiplayer API protocol is an
implementation detail and isn't meant to be used by non-Godot servers.
It may change without notice.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**peer\_authenticating**(id: `int<class_int>`)
`🔗<class_SceneMultiplayer_signal_peer_authenticating>`

Emitted when this MultiplayerAPI's
`MultiplayerAPI.multiplayer_peer<class_MultiplayerAPI_property_multiplayer_peer>`
connects to a new peer and a valid
`auth_callback<class_SceneMultiplayer_property_auth_callback>` is set.
In this case, the
`MultiplayerAPI.peer_connected<class_MultiplayerAPI_signal_peer_connected>`
will not be emitted until
`complete_auth<class_SceneMultiplayer_method_complete_auth>` is called
with given peer `id`. While in this state, the peer will not be included
in the list returned by
`MultiplayerAPI.get_peers<class_MultiplayerAPI_method_get_peers>` (but
in the one returned by
`get_authenticating_peers<class_SceneMultiplayer_method_get_authenticating_peers>`),
and only authentication data will be sent or received. See
`send_auth<class_SceneMultiplayer_method_send_auth>` for sending
authentication data.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**peer\_authentication\_failed**(id: `int<class_int>`)
`🔗<class_SceneMultiplayer_signal_peer_authentication_failed>`

Emitted when this MultiplayerAPI's
`MultiplayerAPI.multiplayer_peer<class_MultiplayerAPI_property_multiplayer_peer>`
disconnects from a peer for which authentication had not yet completed.
See
`peer_authenticating<class_SceneMultiplayer_signal_peer_authenticating>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**peer\_packet**(id: `int<class_int>`, packet:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_SceneMultiplayer_signal_peer_packet>`

Emitted when this MultiplayerAPI's
`MultiplayerAPI.multiplayer_peer<class_MultiplayerAPI_property_multiplayer_peer>`
receives a `packet` with custom data (see
`send_bytes<class_SceneMultiplayer_method_send_bytes>`). ID is the peer
ID of the peer that sent the packet.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **allow\_object\_decoding** = `false`
`🔗<class_SceneMultiplayer_property_allow_object_decoding>`

classref-property-setget

-   `void (No return value.)` **set\_allow\_object\_decoding**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_object\_decoding\_allowed**()

If `true`, the MultiplayerAPI will allow encoding and decoding of object
during RPCs.

\*\*Warning:\*\* Deserialized objects can contain code which gets
executed. Do not use this option if the serialized object comes from
untrusted sources to avoid potential security threat such as remote code
execution.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Callable<class_Callable>` **auth\_callback** = `Callable()`
`🔗<class_SceneMultiplayer_property_auth_callback>`

classref-property-setget

-   `void (No return value.)` **set\_auth\_callback**(value:
    `Callable<class_Callable>`)
-   `Callable<class_Callable>` **get\_auth\_callback**()

The callback to execute when receiving authentication data sent via
`send_auth<class_SceneMultiplayer_method_send_auth>`. If the
`Callable<class_Callable>` is empty (default), peers will be
automatically accepted as soon as they connect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **auth\_timeout** = `3.0`
`🔗<class_SceneMultiplayer_property_auth_timeout>`

classref-property-setget

-   `void (No return value.)` **set\_auth\_timeout**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_auth\_timeout**()

If set to a value greater than `0.0`, the maximum duration in seconds
peers can stay in the authenticating state, after which the
authentication will automatically fail. See the
`peer_authenticating<class_SceneMultiplayer_signal_peer_authenticating>`
and
`peer_authentication_failed<class_SceneMultiplayer_signal_peer_authentication_failed>`
signals.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_delta\_packet\_size** = `65535`
`🔗<class_SceneMultiplayer_property_max_delta_packet_size>`

classref-property-setget

-   `void (No return value.)` **set\_max\_delta\_packet\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_delta\_packet\_size**()

Maximum size of each delta packet. Higher values increase the chance of
receiving full updates in a single frame, but also the chance of causing
networking congestion (higher latency, disconnections). See
`MultiplayerSynchronizer<class_MultiplayerSynchronizer>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_sync\_packet\_size** = `1350`
`🔗<class_SceneMultiplayer_property_max_sync_packet_size>`

classref-property-setget

-   `void (No return value.)` **set\_max\_sync\_packet\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_sync\_packet\_size**()

Maximum size of each synchronization packet. Higher values increase the
chance of receiving full updates in a single frame, but also the chance
of packet loss. See
`MultiplayerSynchronizer<class_MultiplayerSynchronizer>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **refuse\_new\_connections** = `false`
`🔗<class_SceneMultiplayer_property_refuse_new_connections>`

classref-property-setget

-   `void (No return value.)` **set\_refuse\_new\_connections**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_refusing\_new\_connections**()

If `true`, the MultiplayerAPI's
`MultiplayerAPI.multiplayer_peer<class_MultiplayerAPI_property_multiplayer_peer>`
refuses new incoming connections.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **root\_path** = `NodePath("")`
`🔗<class_SceneMultiplayer_property_root_path>`

classref-property-setget

-   `void (No return value.)` **set\_root\_path**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_root\_path**()

The root path to use for RPCs and replication. Instead of an absolute
path, a relative path will be used to find the node upon which the RPC
should be executed.

This effectively allows to have different branches of the scene tree to
be managed by different MultiplayerAPI, allowing for example to run both
client and server in the same scene.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **server\_relay** = `true`
`🔗<class_SceneMultiplayer_property_server_relay>`

classref-property-setget

-   `void (No return value.)` **set\_server\_relay\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_server\_relay\_enabled**()

Enable or disable the server feature that notifies clients of other
peers' connection/disconnection, and relays messages between them. When
this option is `false`, clients won't be automatically notified of other
peers and won't be able to send them packets through the server.

\*\*Note:\*\* Changing this option while other peers are connected may
lead to unexpected behaviors.

\*\*Note:\*\* Support for this feature may depend on the current
`MultiplayerPeer<class_MultiplayerPeer>` configuration. See
`MultiplayerPeer.is_server_relay_supported<class_MultiplayerPeer_method_is_server_relay_supported>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **clear**()
`🔗<class_SceneMultiplayer_method_clear>`

Clears the current SceneMultiplayer network state (you shouldn't call
this unless you know what you are doing).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **complete\_auth**(id:
`int<class_int>`) `🔗<class_SceneMultiplayer_method_complete_auth>`

Mark the authentication step as completed for the remote peer identified
by `id`. The
`MultiplayerAPI.peer_connected<class_MultiplayerAPI_signal_peer_connected>`
signal will be emitted for this peer once the remote side also completes
the authentication. No further authentication messages are expected to
be received from this peer.

If a peer disconnects before completing authentication, either due to a
network issue, the
`auth_timeout<class_SceneMultiplayer_property_auth_timeout>` expiring,
or manually calling
`disconnect_peer<class_SceneMultiplayer_method_disconnect_peer>`, the
`peer_authentication_failed<class_SceneMultiplayer_signal_peer_authentication_failed>`
signal will be emitted instead of
`MultiplayerAPI.peer_disconnected<class_MultiplayerAPI_signal_peer_disconnected>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **disconnect\_peer**(id: `int<class_int>`)
`🔗<class_SceneMultiplayer_method_disconnect_peer>`

Disconnects the peer identified by `id`, removing it from the list of
connected peers, and closing the underlying connection with it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**get\_authenticating\_peers**()
`🔗<class_SceneMultiplayer_method_get_authenticating_peers>`

Returns the IDs of the peers currently trying to authenticate with this
`MultiplayerAPI<class_MultiplayerAPI>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **send\_auth**(id: `int<class_int>`,
data: `PackedByteArray<class_PackedByteArray>`)
`🔗<class_SceneMultiplayer_method_send_auth>`

Sends the specified `data` to the remote peer identified by `id` as part
of an authentication message. This can be used to authenticate peers,
and control when
`MultiplayerAPI.peer_connected<class_MultiplayerAPI_signal_peer_connected>`
is emitted (and the remote peer accepted as one of the connected peers).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **send\_bytes**(bytes:
`PackedByteArray<class_PackedByteArray>`, id: `int<class_int>` = 0,
mode: `TransferMode<enum_MultiplayerPeer_TransferMode>` = 2, channel:
`int<class_int>` = 0) `🔗<class_SceneMultiplayer_method_send_bytes>`

Sends the given raw `bytes` to a specific peer identified by `id` (see
`MultiplayerPeer.set_target_peer<class_MultiplayerPeer_method_set_target_peer>`).
Default ID is `0`, i.e. broadcast to all peers.
