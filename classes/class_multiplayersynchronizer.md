github\_url  
hide

# MultiplayerSynchronizer

**Inherits:** `Node<class_Node>` **&lt;** `Object<class_Object>`

Synchronizes properties from the multiplayer authority to the remote
peers.

classref-introduction-group

## Description

By default, **MultiplayerSynchronizer** synchronizes configured
properties to all peers.

Visibility can be handled directly with
`set_visibility_for<class_MultiplayerSynchronizer_method_set_visibility_for>`
or as-needed with
`add_visibility_filter<class_MultiplayerSynchronizer_method_add_visibility_filter>`
and
`update_visibility<class_MultiplayerSynchronizer_method_update_visibility>`.

`MultiplayerSpawner<class_MultiplayerSpawner>`s will handle nodes
according to visibility of synchronizers as long as the node at
`root_path<class_MultiplayerSynchronizer_property_root_path>` was
spawned by one.

Internally, **MultiplayerSynchronizer** uses
`MultiplayerAPI.object_configuration_add<class_MultiplayerAPI_method_object_configuration_add>`
to notify synchronization start passing the `Node<class_Node>` at
`root_path<class_MultiplayerSynchronizer_property_root_path>` as the
`object` and itself as the `configuration`, and uses
`MultiplayerAPI.object_configuration_remove<class_MultiplayerAPI_method_object_configuration_remove>`
to notify synchronization end in a similar way.

\*\*Note:\*\* Synchronization is not supported for
`Object<class_Object>` type properties, like `Resource<class_Resource>`.
Properties that are unique to each peer, like the instance IDs of
`Object<class_Object>`s (see
`Object.get_instance_id<class_Object_method_get_instance_id>`) or
`RID<class_RID>`s, will also not work in synchronization.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**delta\_synchronized**()
`🔗<class_MultiplayerSynchronizer_signal_delta_synchronized>`

Emitted when a new delta synchronization state is received by this
synchronizer after the properties have been updated.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**synchronized**()
`🔗<class_MultiplayerSynchronizer_signal_synchronized>`

Emitted when a new synchronization state is received by this
synchronizer after the properties have been updated.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**visibility\_changed**(for\_peer: `int<class_int>`)
`🔗<class_MultiplayerSynchronizer_signal_visibility_changed>`

Emitted when visibility of `for_peer` is updated. See
`update_visibility<class_MultiplayerSynchronizer_method_update_visibility>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **VisibilityUpdateMode**:
`🔗<enum_MultiplayerSynchronizer_VisibilityUpdateMode>`

classref-enumeration-constant

`VisibilityUpdateMode<enum_MultiplayerSynchronizer_VisibilityUpdateMode>`
**VISIBILITY\_PROCESS\_IDLE** = `0`

Visibility filters are updated during process frames (see
`Node.NOTIFICATION_INTERNAL_PROCESS<class_Node_constant_NOTIFICATION_INTERNAL_PROCESS>`).

classref-enumeration-constant

`VisibilityUpdateMode<enum_MultiplayerSynchronizer_VisibilityUpdateMode>`
**VISIBILITY\_PROCESS\_PHYSICS** = `1`

Visibility filters are updated during physics frames (see
`Node.NOTIFICATION_INTERNAL_PHYSICS_PROCESS<class_Node_constant_NOTIFICATION_INTERNAL_PHYSICS_PROCESS>`).

classref-enumeration-constant

`VisibilityUpdateMode<enum_MultiplayerSynchronizer_VisibilityUpdateMode>`
**VISIBILITY\_PROCESS\_NONE** = `2`

Visibility filters are not updated automatically, and must be updated
manually by calling
`update_visibility<class_MultiplayerSynchronizer_method_update_visibility>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **delta\_interval** = `0.0`
`🔗<class_MultiplayerSynchronizer_property_delta_interval>`

classref-property-setget

-   `void (No return value.)` **set\_delta\_interval**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_delta\_interval**()

Time interval between delta synchronizations. When set to `0.0` (the
default), delta synchronizations happen every network process frame.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **public\_visibility** = `true`
`🔗<class_MultiplayerSynchronizer_property_public_visibility>`

classref-property-setget

-   `void (No return value.)` **set\_visibility\_public**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_visibility\_public**()

Whether synchronization should be visible to all peers by default. See
`set_visibility_for<class_MultiplayerSynchronizer_method_set_visibility_for>`
and
`add_visibility_filter<class_MultiplayerSynchronizer_method_add_visibility_filter>`
for ways of configuring fine-grained visibility options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SceneReplicationConfig<class_SceneReplicationConfig>`
**replication\_config**
`🔗<class_MultiplayerSynchronizer_property_replication_config>`

classref-property-setget

-   `void (No return value.)` **set\_replication\_config**(value:
    `SceneReplicationConfig<class_SceneReplicationConfig>`)
-   `SceneReplicationConfig<class_SceneReplicationConfig>`
    **get\_replication\_config**()

Resource containing which properties to synchronize.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **replication\_interval** = `0.0`
`🔗<class_MultiplayerSynchronizer_property_replication_interval>`

classref-property-setget

-   `void (No return value.)` **set\_replication\_interval**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_replication\_interval**()

Time interval between synchronizations. When set to `0.0` (the default),
synchronizations happen every network process frame.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **root\_path** = `NodePath("..")`
`🔗<class_MultiplayerSynchronizer_property_root_path>`

classref-property-setget

-   `void (No return value.)` **set\_root\_path**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_root\_path**()

Node path that replicated properties are relative to.

If `root_path<class_MultiplayerSynchronizer_property_root_path>` was
spawned by a `MultiplayerSpawner<class_MultiplayerSpawner>`, the node
will be also be spawned and despawned based on this synchronizer
visibility options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VisibilityUpdateMode<enum_MultiplayerSynchronizer_VisibilityUpdateMode>`
**visibility\_update\_mode** = `0`
`🔗<class_MultiplayerSynchronizer_property_visibility_update_mode>`

classref-property-setget

-   `void (No return value.)` **set\_visibility\_update\_mode**(value:
    `VisibilityUpdateMode<enum_MultiplayerSynchronizer_VisibilityUpdateMode>`)
-   `VisibilityUpdateMode<enum_MultiplayerSynchronizer_VisibilityUpdateMode>`
    **get\_visibility\_update\_mode**()

Specifies when visibility filters are updated (see
`VisibilityUpdateMode<enum_MultiplayerSynchronizer_VisibilityUpdateMode>`
for options).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_visibility\_filter**(filter:
`Callable<class_Callable>`)
`🔗<class_MultiplayerSynchronizer_method_add_visibility_filter>`

Adds a peer visibility filter for this synchronizer.

`filter` should take a peer ID `int<class_int>` and return a
`bool<class_bool>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_visibility\_for**(peer: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MultiplayerSynchronizer_method_get_visibility_for>`

Queries the current visibility for peer `peer`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_visibility\_filter**(filter:
`Callable<class_Callable>`)
`🔗<class_MultiplayerSynchronizer_method_remove_visibility_filter>`

Removes a peer visibility filter from this synchronizer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_visibility\_for**(peer:
`int<class_int>`, visible: `bool<class_bool>`)
`🔗<class_MultiplayerSynchronizer_method_set_visibility_for>`

Sets the visibility of `peer` to `visible`. If `peer` is `0`, the value
of
`public_visibility<class_MultiplayerSynchronizer_property_public_visibility>`
will be updated instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update\_visibility**(for\_peer:
`int<class_int>` = 0)
`🔗<class_MultiplayerSynchronizer_method_update_visibility>`

Updates the visibility of `for_peer` according to visibility filters. If
`for_peer` is `0` (the default), all peers' visibilties are updated.
