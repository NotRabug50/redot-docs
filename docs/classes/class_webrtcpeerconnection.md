github\_url  
hide

# WebRTCPeerConnection

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

**Inherited By:**
`WebRTCPeerConnectionExtension<class_WebRTCPeerConnectionExtension>`

Interface to a WebRTC peer connection.

classref-introduction-group

## Description

A WebRTC connection between the local computer and a remote peer.
Provides an interface to connect, maintain and monitor the connection.

Setting up a WebRTC connection between two peers may not seem a trivial
task, but it can be broken down into 3 main steps:

-   The peer that wants to initiate the connection (`A` from now on)
    creates an offer and send it to the other peer (`B` from now on).
-   `B` receives the offer, generate and answer, and sends it to `A`).
-   `A` and `B` then generates and exchange ICE candidates with each
    other.

After these steps, the connection should become connected. Keep on
reading or look into the tutorial for more information.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**data\_channel\_received**(channel:
`WebRTCDataChannel<class_WebRTCDataChannel>`)
`🔗<class_WebRTCPeerConnection_signal_data_channel_received>`

Emitted when a new in-band channel is received, i.e. when the channel
was created with `negotiated: false` (default).

The object will be an instance of
`WebRTCDataChannel<class_WebRTCDataChannel>`. You must keep a reference
of it or it will be closed automatically. See
`create_data_channel<class_WebRTCPeerConnection_method_create_data_channel>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**ice\_candidate\_created**(media: `String<class_String>`, index:
`int<class_int>`, name: `String<class_String>`)
`🔗<class_WebRTCPeerConnection_signal_ice_candidate_created>`

Emitted when a new ICE candidate has been created. The three parameters
are meant to be passed to the remote peer over the signaling server.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**session\_description\_created**(type: `String<class_String>`, sdp:
`String<class_String>`)
`🔗<class_WebRTCPeerConnection_signal_session_description_created>`

Emitted after a successful call to
`create_offer<class_WebRTCPeerConnection_method_create_offer>` or
`set_remote_description<class_WebRTCPeerConnection_method_set_remote_description>`
(when it generates an answer). The parameters are meant to be passed to
`set_local_description<class_WebRTCPeerConnection_method_set_local_description>`
on this object, and sent to the remote peer over the signaling server.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ConnectionState**:
`🔗<enum_WebRTCPeerConnection_ConnectionState>`

classref-enumeration-constant

`ConnectionState<enum_WebRTCPeerConnection_ConnectionState>`
**STATE\_NEW** = `0`

The connection is new, data channels and an offer can be created in this
state.

classref-enumeration-constant

`ConnectionState<enum_WebRTCPeerConnection_ConnectionState>`
**STATE\_CONNECTING** = `1`

The peer is connecting, ICE is in progress, none of the transports has
failed.

classref-enumeration-constant

`ConnectionState<enum_WebRTCPeerConnection_ConnectionState>`
**STATE\_CONNECTED** = `2`

The peer is connected, all ICE transports are connected.

classref-enumeration-constant

`ConnectionState<enum_WebRTCPeerConnection_ConnectionState>`
**STATE\_DISCONNECTED** = `3`

At least one ICE transport is disconnected.

classref-enumeration-constant

`ConnectionState<enum_WebRTCPeerConnection_ConnectionState>`
**STATE\_FAILED** = `4`

One or more of the ICE transports failed.

classref-enumeration-constant

`ConnectionState<enum_WebRTCPeerConnection_ConnectionState>`
**STATE\_CLOSED** = `5`

The peer connection is closed (after calling
`close<class_WebRTCPeerConnection_method_close>` for example).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **GatheringState**: `🔗<enum_WebRTCPeerConnection_GatheringState>`

classref-enumeration-constant

`GatheringState<enum_WebRTCPeerConnection_GatheringState>`
**GATHERING\_STATE\_NEW** = `0`

The peer connection was just created and hasn't done any networking yet.

classref-enumeration-constant

`GatheringState<enum_WebRTCPeerConnection_GatheringState>`
**GATHERING\_STATE\_GATHERING** = `1`

The ICE agent is in the process of gathering candidates for the
connection.

classref-enumeration-constant

`GatheringState<enum_WebRTCPeerConnection_GatheringState>`
**GATHERING\_STATE\_COMPLETE** = `2`

The ICE agent has finished gathering candidates. If something happens
that requires collecting new candidates, such as a new interface being
added or the addition of a new ICE server, the state will revert to
gathering to gather those candidates.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SignalingState**: `🔗<enum_WebRTCPeerConnection_SignalingState>`

classref-enumeration-constant

`SignalingState<enum_WebRTCPeerConnection_SignalingState>`
**SIGNALING\_STATE\_STABLE** = `0`

There is no ongoing exchange of offer and answer underway. This may mean
that the **WebRTCPeerConnection** is new
(`STATE_NEW<class_WebRTCPeerConnection_constant_STATE_NEW>`) or that
negotiation is complete and a connection has been established
(`STATE_CONNECTED<class_WebRTCPeerConnection_constant_STATE_CONNECTED>`).

classref-enumeration-constant

`SignalingState<enum_WebRTCPeerConnection_SignalingState>`
**SIGNALING\_STATE\_HAVE\_LOCAL\_OFFER** = `1`

The local peer has called
`set_local_description<class_WebRTCPeerConnection_method_set_local_description>`,
passing in SDP representing an offer (usually created by calling
`create_offer<class_WebRTCPeerConnection_method_create_offer>`), and the
offer has been applied successfully.

classref-enumeration-constant

`SignalingState<enum_WebRTCPeerConnection_SignalingState>`
**SIGNALING\_STATE\_HAVE\_REMOTE\_OFFER** = `2`

The remote peer has created an offer and used the signaling server to
deliver it to the local peer, which has set the offer as the remote
description by calling
`set_remote_description<class_WebRTCPeerConnection_method_set_remote_description>`.

classref-enumeration-constant

`SignalingState<enum_WebRTCPeerConnection_SignalingState>`
**SIGNALING\_STATE\_HAVE\_LOCAL\_PRANSWER** = `3`

The offer sent by the remote peer has been applied and an answer has
been created and applied by calling
`set_local_description<class_WebRTCPeerConnection_method_set_local_description>`.
This provisional answer describes the supported media formats and so
forth, but may not have a complete set of ICE candidates included.
Further candidates will be delivered separately later.

classref-enumeration-constant

`SignalingState<enum_WebRTCPeerConnection_SignalingState>`
**SIGNALING\_STATE\_HAVE\_REMOTE\_PRANSWER** = `4`

A provisional answer has been received and successfully applied in
response to an offer previously sent and established by calling
`set_local_description<class_WebRTCPeerConnection_method_set_local_description>`.

classref-enumeration-constant

`SignalingState<enum_WebRTCPeerConnection_SignalingState>`
**SIGNALING\_STATE\_CLOSED** = `5`

The **WebRTCPeerConnection** has been closed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **add\_ice\_candidate**(media:
`String<class_String>`, index: `int<class_int>`, name:
`String<class_String>`)
`🔗<class_WebRTCPeerConnection_method_add_ice_candidate>`

Add an ice candidate generated by a remote peer (and received over the
signaling server). See
`ice_candidate_created<class_WebRTCPeerConnection_signal_ice_candidate_created>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **close**()
`🔗<class_WebRTCPeerConnection_method_close>`

Close the peer connection and all data channels associated with it.

\*\*Note:\*\* You cannot reuse this object for a new connection unless
you call `initialize<class_WebRTCPeerConnection_method_initialize>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`WebRTCDataChannel<class_WebRTCDataChannel>`
**create\_data\_channel**(label: `String<class_String>`, options:
`Dictionary<class_Dictionary>` = {})
`🔗<class_WebRTCPeerConnection_method_create_data_channel>`

Returns a new `WebRTCDataChannel<class_WebRTCDataChannel>` (or `null` on
failure) with given `label` and optionally configured via the `options`
dictionary. This method can only be called when the connection is in
state `STATE_NEW<class_WebRTCPeerConnection_constant_STATE_NEW>`.

There are two ways to create a working data channel: either call
`create_data_channel<class_WebRTCPeerConnection_method_create_data_channel>`
on only one of the peer and listen to
`data_channel_received<class_WebRTCPeerConnection_signal_data_channel_received>`
on the other, or call
`create_data_channel<class_WebRTCPeerConnection_method_create_data_channel>`
on both peers, with the same values, and the `"negotiated"` option set
to `true`.

Valid `options` are:

    {
        "negotiated": true, # When set to true (default off), means the channel is negotiated out of band. "id" must be set too. "data_channel_received" will not be called.
        "id": 1, # When "negotiated" is true this value must also be set to the same value on both peer.

        # Only one of maxRetransmits and maxPacketLifeTime can be specified, not both. They make the channel unreliable (but also better at real time).
        "maxRetransmits": 1, # Specify the maximum number of attempt the peer will make to retransmits packets if they are not acknowledged.
        "maxPacketLifeTime": 100, # Specify the maximum amount of time before giving up retransmitions of unacknowledged packets (in milliseconds).
        "ordered": true, # When in unreliable mode (i.e. either "maxRetransmits" or "maxPacketLifetime" is set), "ordered" (true by default) specify if packet ordering is to be enforced.

        "protocol": "my-custom-protocol", # A custom sub-protocol string for this channel.
    }

\*\*Note:\*\* You must keep a reference to channels created this way, or
it will be closed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **create\_offer**()
`🔗<class_WebRTCPeerConnection_method_create_offer>`

Creates a new SDP offer to start a WebRTC connection with a remote peer.
At least one `WebRTCDataChannel<class_WebRTCDataChannel>` must have been
created before calling this method.

If this functions returns
`@GlobalScope.OK<class_@GlobalScope_constant_OK>`,
`session_description_created<class_WebRTCPeerConnection_signal_session_description_created>`
will be called when the session is ready to be sent.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ConnectionState<enum_WebRTCPeerConnection_ConnectionState>`
**get\_connection\_state**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebRTCPeerConnection_method_get_connection_state>`

Returns the connection state. See
`ConnectionState<enum_WebRTCPeerConnection_ConnectionState>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`GatheringState<enum_WebRTCPeerConnection_GatheringState>`
**get\_gathering\_state**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebRTCPeerConnection_method_get_gathering_state>`

Returns the ICE
`GatheringState<enum_WebRTCPeerConnection_GatheringState>` of the
connection. This lets you detect, for example, when collection of ICE
candidates has finished.

classref-item-separator

------------------------------------------------------------------------

classref-method

`SignalingState<enum_WebRTCPeerConnection_SignalingState>`
**get\_signaling\_state**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_WebRTCPeerConnection_method_get_signaling_state>`

Returns the signaling state on the local end of the connection while
connecting or reconnecting to another peer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **initialize**(configuration:
`Dictionary<class_Dictionary>` = {})
`🔗<class_WebRTCPeerConnection_method_initialize>`

Re-initialize this peer connection, closing any previously active
connection, and going back to state
`STATE_NEW<class_WebRTCPeerConnection_constant_STATE_NEW>`. A dictionary
of `configuration` options can be passed to configure the peer
connection.

Valid `configuration` options are:

    {
        "iceServers": [
            {
                "urls": [ "stun:stun.example.com:3478" ], # One or more STUN servers.
            },
            {
                "urls": [ "turn:turn.example.com:3478" ], # One or more TURN servers.
                "username": "a_username", # Optional username for the TURN server.
                "credential": "a_password", # Optional password for the TURN server.
            }
        ]
    }

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **poll**()
`🔗<class_WebRTCPeerConnection_method_poll>`

Call this method frequently (e.g. in
`Node._process<class_Node_private_method__process>` or
`Node._physics_process<class_Node_private_method__physics_process>`) to
properly receive signals.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_default\_extension**(extension\_class:
`StringName<class_StringName>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_WebRTCPeerConnection_method_set_default_extension>`

Sets the `extension_class` as the default
`WebRTCPeerConnectionExtension<class_WebRTCPeerConnectionExtension>`
returned when creating a new **WebRTCPeerConnection**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **set\_local\_description**(type:
`String<class_String>`, sdp: `String<class_String>`)
`🔗<class_WebRTCPeerConnection_method_set_local_description>`

Sets the SDP description of the local peer. This should be called in
response to
`session_description_created<class_WebRTCPeerConnection_signal_session_description_created>`.

After calling this function the peer will start emitting
`ice_candidate_created<class_WebRTCPeerConnection_signal_ice_candidate_created>`
(unless an `Error<enum_@GlobalScope_Error>` different from
`@GlobalScope.OK<class_@GlobalScope_constant_OK>` is returned).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **set\_remote\_description**(type:
`String<class_String>`, sdp: `String<class_String>`)
`🔗<class_WebRTCPeerConnection_method_set_remote_description>`

Sets the SDP description of the remote peer. This should be called with
the values generated by a remote peer and received over the signaling
server.

If `type` is `"offer"` the peer will emit
`session_description_created<class_WebRTCPeerConnection_signal_session_description_created>`
with the appropriate answer.

If `type` is `"answer"` the peer will start emitting
`ice_candidate_created<class_WebRTCPeerConnection_signal_ice_candidate_created>`.
