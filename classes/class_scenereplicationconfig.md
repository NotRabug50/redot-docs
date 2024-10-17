github\_url  
hide

# SceneReplicationConfig

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Configuration for properties to synchronize with a
`MultiplayerSynchronizer<class_MultiplayerSynchronizer>`.

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

## Enumerations

classref-enumeration

enum **ReplicationMode**:
`🔗<enum_SceneReplicationConfig_ReplicationMode>`

classref-enumeration-constant

`ReplicationMode<enum_SceneReplicationConfig_ReplicationMode>`
**REPLICATION\_MODE\_NEVER** = `0`

Do not keep the given property synchronized.

classref-enumeration-constant

`ReplicationMode<enum_SceneReplicationConfig_ReplicationMode>`
**REPLICATION\_MODE\_ALWAYS** = `1`

Replicate the given property on process by constantly sending updates
using unreliable transfer mode.

classref-enumeration-constant

`ReplicationMode<enum_SceneReplicationConfig_ReplicationMode>`
**REPLICATION\_MODE\_ON\_CHANGE** = `2`

Replicate the given property on process by sending updates using
reliable transfer mode when its value changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_property**(path:
`NodePath<class_NodePath>`, index: `int<class_int>` = -1)
`🔗<class_SceneReplicationConfig_method_add_property>`

Adds the property identified by the given `path` to the list of the
properties being synchronized, optionally passing an `index`.

\*\*Note:\*\* For details on restrictions and limitations on property
synchronization, see
`MultiplayerSynchronizer<class_MultiplayerSynchronizer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`NodePath<class_NodePath>`\] **get\_properties**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneReplicationConfig_method_get_properties>`

Returns a list of synchronized property `NodePath<class_NodePath>`s.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_property**(path: `NodePath<class_NodePath>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneReplicationConfig_method_has_property>`

Returns `true` if the given `path` is configured for synchronization.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **property\_get\_index**(path:
`NodePath<class_NodePath>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneReplicationConfig_method_property_get_index>`

Finds the index of the given `path`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ReplicationMode<enum_SceneReplicationConfig_ReplicationMode>`
**property\_get\_replication\_mode**(path: `NodePath<class_NodePath>`)
`🔗<class_SceneReplicationConfig_method_property_get_replication_mode>`

Returns the replication mode for the property identified by the given
`path`. See
`ReplicationMode<enum_SceneReplicationConfig_ReplicationMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **property\_get\_spawn**(path:
`NodePath<class_NodePath>`)
`🔗<class_SceneReplicationConfig_method_property_get_spawn>`

Returns `true` if the property identified by the given `path` is
configured to be synchronized on spawn.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **property\_get\_sync**(path:
`NodePath<class_NodePath>`)
`🔗<class_SceneReplicationConfig_method_property_get_sync>`

**Deprecated:** Use
`property_get_replication_mode<class_SceneReplicationConfig_method_property_get_replication_mode>`
instead.

Returns `true` if the property identified by the given `path` is
configured to be synchronized on process.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **property\_get\_watch**(path:
`NodePath<class_NodePath>`)
`🔗<class_SceneReplicationConfig_method_property_get_watch>`

**Deprecated:** Use
`property_get_replication_mode<class_SceneReplicationConfig_method_property_get_replication_mode>`
instead.

Returns `true` if the property identified by the given `path` is
configured to be reliably synchronized when changes are detected on
process.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **property\_set\_replication\_mode**(path:
`NodePath<class_NodePath>`, mode:
`ReplicationMode<enum_SceneReplicationConfig_ReplicationMode>`)
`🔗<class_SceneReplicationConfig_method_property_set_replication_mode>`

Sets the synchronization mode for the property identified by the given
`path`. See
`ReplicationMode<enum_SceneReplicationConfig_ReplicationMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **property\_set\_spawn**(path:
`NodePath<class_NodePath>`, enabled: `bool<class_bool>`)
`🔗<class_SceneReplicationConfig_method_property_set_spawn>`

Sets whether the property identified by the given `path` is configured
to be synchronized on spawn.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **property\_set\_sync**(path:
`NodePath<class_NodePath>`, enabled: `bool<class_bool>`)
`🔗<class_SceneReplicationConfig_method_property_set_sync>`

**Deprecated:** Use
`property_set_replication_mode<class_SceneReplicationConfig_method_property_set_replication_mode>`
with
`REPLICATION_MODE_ALWAYS<class_SceneReplicationConfig_constant_REPLICATION_MODE_ALWAYS>`
instead.

Sets whether the property identified by the given `path` is configured
to be synchronized on process.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **property\_set\_watch**(path:
`NodePath<class_NodePath>`, enabled: `bool<class_bool>`)
`🔗<class_SceneReplicationConfig_method_property_set_watch>`

**Deprecated:** Use
`property_set_replication_mode<class_SceneReplicationConfig_method_property_set_replication_mode>`
with
`REPLICATION_MODE_ON_CHANGE<class_SceneReplicationConfig_constant_REPLICATION_MODE_ON_CHANGE>`
instead.

Sets whether the property identified by the given `path` is configured
to be reliably synchronized when changes are detected on process.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_property**(path:
`NodePath<class_NodePath>`)
`🔗<class_SceneReplicationConfig_method_remove_property>`

Removes the property identified by the given `path` from the
configuration.
