github\_url  
hide

# SceneState

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides access to a scene file's information.

classref-introduction-group

## Description

Maintains a list of resources, nodes, exported and overridden
properties, and built-in scripts associated with a scene. They cannot be
modified from a **SceneState**, only accessed. Useful for peeking into
what a `PackedScene<class_PackedScene>` contains without instantiating
it.

This class cannot be instantiated directly, it is retrieved for a given
scene as the result of
`PackedScene.get_state<class_PackedScene_method_get_state>`.

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

enum **GenEditState**: `🔗<enum_SceneState_GenEditState>`

classref-enumeration-constant

`GenEditState<enum_SceneState_GenEditState>`
**GEN\_EDIT\_STATE\_DISABLED** = `0`

If passed to
`PackedScene.instantiate<class_PackedScene_method_instantiate>`, blocks
edits to the scene state.

classref-enumeration-constant

`GenEditState<enum_SceneState_GenEditState>`
**GEN\_EDIT\_STATE\_INSTANCE** = `1`

If passed to
`PackedScene.instantiate<class_PackedScene_method_instantiate>`,
provides inherited scene resources to the local scene.

\*\*Note:\*\* Only available in editor builds.

classref-enumeration-constant

`GenEditState<enum_SceneState_GenEditState>` **GEN\_EDIT\_STATE\_MAIN**
= `2`

If passed to
`PackedScene.instantiate<class_PackedScene_method_instantiate>`,
provides local scene resources to the local scene. Only the main scene
should receive the main edit state.

\*\*Note:\*\* Only available in editor builds.

classref-enumeration-constant

`GenEditState<enum_SceneState_GenEditState>`
**GEN\_EDIT\_STATE\_MAIN\_INHERITED** = `3`

If passed to
`PackedScene.instantiate<class_PackedScene_method_instantiate>`, it's
similar to
`GEN_EDIT_STATE_MAIN<class_SceneState_constant_GEN_EDIT_STATE_MAIN>`,
but for the case where the scene is being instantiated to be the base of
another one.

\*\*Note:\*\* Only available in editor builds.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Array<class_Array>` **get\_connection\_binds**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_connection_binds>`

Returns the list of bound parameters for the signal at `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_connection\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_connection_count>`

Returns the number of signal connections in the scene.

The `idx` argument used to query connection metadata in other
`get_connection_*` methods in the interval
`[0, get_connection_count() - 1]`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_connection\_flags**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_connection_flags>`

Returns the connection flags for the signal at `idx`. See
`ConnectFlags<enum_Object_ConnectFlags>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_connection\_method**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_connection_method>`

Returns the method connected to the signal at `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_connection\_signal**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_connection_signal>`

Returns the name of the signal at `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **get\_connection\_source**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_connection_source>`

Returns the path to the node that owns the signal at `idx`, relative to
the root node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **get\_connection\_target**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_connection_target>`

Returns the path to the node that owns the method connected to the
signal at `idx`, relative to the root node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_connection\_unbinds**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_connection_unbinds>`

Returns the number of unbound parameters for the signal at `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_node\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_count>`

Returns the number of nodes in the scene.

The `idx` argument used to query node data in other `get_node_*` methods
in the interval `[0, get_node_count() - 1]`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_node\_groups**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_groups>`

Returns the list of group names associated with the node at `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_node\_index**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_index>`

Returns the node's index, which is its position relative to its
siblings. This is only relevant and saved in scenes for cases where new
nodes are added to an instantiated or inherited scene among siblings
from the base scene. Despite the name, this index is not related to the
`idx` argument used here and in other methods.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedScene<class_PackedScene>` **get\_node\_instance**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_instance>`

Returns a `PackedScene<class_PackedScene>` for the node at `idx` (i.e.
the whole branch starting at this node, with its child nodes and
resources), or `null` if the node is not an instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_node\_instance\_placeholder**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_instance_placeholder>`

Returns the path to the represented scene file if the node at `idx` is
an `InstancePlaceholder<class_InstancePlaceholder>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_node\_name**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_name>`

Returns the name of the node at `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **get\_node\_owner\_path**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_owner_path>`

Returns the path to the owner of the node at `idx`, relative to the root
node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **get\_node\_path**(idx: `int<class_int>`,
for\_parent: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_path>`

Returns the path to the node at `idx`.

If `for_parent` is `true`, returns the path of the `idx` node's parent
instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_node\_property\_count**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_property_count>`

Returns the number of exported or overridden properties for the node at
`idx`.

The `prop_idx` argument used to query node property data in other
`get_node_property_*` methods in the interval
`[0, get_node_property_count() - 1]`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_node\_property\_name**(idx:
`int<class_int>`, prop\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_property_name>`

Returns the name of the property at `prop_idx` for the node at `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_node\_property\_value**(idx:
`int<class_int>`, prop\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_property_value>`

Returns the value of the property at `prop_idx` for the node at `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_node\_type**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_get_node_type>`

Returns the type of the node at `idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_node\_instance\_placeholder**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneState_method_is_node_instance_placeholder>`

Returns `true` if the node at `idx` is an
`InstancePlaceholder<class_InstancePlaceholder>`.
