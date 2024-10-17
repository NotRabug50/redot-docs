github\_url  
hide

# MultiplayerAPIExtension

**Inherits:** `MultiplayerAPI<class_MultiplayerAPI>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Base class used for extending the
`MultiplayerAPI<class_MultiplayerAPI>`.

classref-introduction-group

## Description

This class can be used to augment or replace the default
`MultiplayerAPI<class_MultiplayerAPI>` implementation via script or
extensions.

The following example augment the default implementation
(`SceneMultiplayer<class_SceneMultiplayer>`) by logging every RPC being
made, and every object being configured for replication.

gdscript

extends MultiplayerAPIExtension class\_name LogMultiplayer

\# We want to augment the default SceneMultiplayer. var
base\_multiplayer = SceneMultiplayer.new()

func \_init():  
\# Just passthrough base signals (copied to var to avoid cyclic
reference) var cts = connected\_to\_server var cf = connection\_failed
var pc = peer\_connected var pd = peer\_disconnected
base\_multiplayer.connected\_to\_server.connect(func(): cts.emit())
base\_multiplayer.connection\_failed.connect(func(): cf.emit())
base\_multiplayer.peer\_connected.connect(func(id): pc.emit(id))
base\_multiplayer.peer\_disconnected.connect(func(id): pd.emit(id))

func \_poll():  
return base\_multiplayer.poll()

\# Log RPC being made and forward it to the default multiplayer. func
\_rpc(peer: int, object: Object, method: StringName, args: Array) -&gt;
Error: print("Got RPC for %d: %s::%s(%s)" % \[peer, object, method,
args\]) return base\_multiplayer.rpc(peer, object, method, args)

\# Log configuration add. E.g. root path (nullptr, NodePath),
replication (Node, Spawner|Synchronizer), custom. func
\_object\_configuration\_add(object, config: Variant) -&gt; Error: if
config is MultiplayerSynchronizer: print("Adding synchronization
configuration for %s. Synchronizer: %s" % \[object, config\]) elif
config is MultiplayerSpawner: print("Adding node %s to the spawn list.
Spawner: %s" % \[object, config\]) return
base\_multiplayer.object\_configuration\_add(object, config)

\# Log configuration remove. E.g. root path (nullptr, NodePath),
replication (Node, Spawner|Synchronizer), custom. func
\_object\_configuration\_remove(object, config: Variant) -&gt; Error: if
config is MultiplayerSynchronizer: print("Removing synchronization
configuration for %s. Synchronizer: %s" % \[object, config\]) elif
config is MultiplayerSpawner: print("Removing node %s from the spawn
list. Spawner: %s" % \[object, config\]) return
base\_multiplayer.object\_configuration\_remove(object, config)

\# These can be optional, but in our case we want to augment
SceneMultiplayer, so forward everything. func
\_set\_multiplayer\_peer(p\_peer: MultiplayerPeer):
base\_multiplayer.multiplayer\_peer = p\_peer

func \_get\_multiplayer\_peer() -&gt; MultiplayerPeer:  
return base\_multiplayer.multiplayer\_peer

func \_get\_unique\_id() -&gt; int:  
return base\_multiplayer.get\_unique\_id()

func \_get\_peer\_ids() -&gt; PackedInt32Array:  
return base\_multiplayer.get\_peers()

Then in your main scene or in an autoload call
`SceneTree.set_multiplayer<class_SceneTree_method_set_multiplayer>` to
start using your custom `MultiplayerAPI<class_MultiplayerAPI>`:

gdscript

\# autoload.gd func \_enter\_tree(): \# Sets our custom multiplayer as
the main one in SceneTree.
get\_tree().set\_multiplayer(LogMultiplayer.new())

Native extensions can alternatively use the
`MultiplayerAPI.set_default_interface<class_MultiplayerAPI_method_set_default_interface>`
method during initialization to configure themselves as the default
implementation.

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

## Method Descriptions

classref-method

`MultiplayerPeer<class_MultiplayerPeer>` **\_get\_multiplayer\_peer**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_MultiplayerAPIExtension_private_method__get_multiplayer_peer>`

Called when the
`MultiplayerAPI.multiplayer_peer<class_MultiplayerAPI_property_multiplayer_peer>`
is retrieved.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>` **\_get\_peer\_ids**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MultiplayerAPIExtension_private_method__get_peer_ids>`

Callback for
`MultiplayerAPI.get_peers<class_MultiplayerAPI_method_get_peers>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_remote\_sender\_id**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MultiplayerAPIExtension_private_method__get_remote_sender_id>`

Callback for
`MultiplayerAPI.get_remote_sender_id<class_MultiplayerAPI_method_get_remote_sender_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_unique\_id**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MultiplayerAPIExtension_private_method__get_unique_id>`

Callback for
`MultiplayerAPI.get_unique_id<class_MultiplayerAPI_method_get_unique_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**\_object\_configuration\_add**(object: `Object<class_Object>`,
configuration: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_MultiplayerAPIExtension_private_method__object_configuration_add>`

Callback for
`MultiplayerAPI.object_configuration_add<class_MultiplayerAPI_method_object_configuration_add>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**\_object\_configuration\_remove**(object: `Object<class_Object>`,
configuration: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_MultiplayerAPIExtension_private_method__object_configuration_remove>`

Callback for
`MultiplayerAPI.object_configuration_remove<class_MultiplayerAPI_method_object_configuration_remove>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_poll**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_MultiplayerAPIExtension_private_method__poll>`

Callback for `MultiplayerAPI.poll<class_MultiplayerAPI_method_poll>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_rpc**(peer: `int<class_int>`,
object: `Object<class_Object>`, method: `StringName<class_StringName>`,
args: `Array<class_Array>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_MultiplayerAPIExtension_private_method__rpc>`

Callback for `MultiplayerAPI.rpc<class_MultiplayerAPI_method_rpc>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_set\_multiplayer\_peer**(multiplayer\_peer:
`MultiplayerPeer<class_MultiplayerPeer>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_MultiplayerAPIExtension_private_method__set_multiplayer_peer>`

Called when the
`MultiplayerAPI.multiplayer_peer<class_MultiplayerAPI_property_multiplayer_peer>`
is set.
