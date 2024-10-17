github\_url  
hide

# Node

**Inherits:** `Object<class_Object>`

**Inherited By:** `AnimationMixer<class_AnimationMixer>`,
`AudioStreamPlayer<class_AudioStreamPlayer>`,
`CanvasItem<class_CanvasItem>`, `CanvasLayer<class_CanvasLayer>`,
`EditorFileSystem<class_EditorFileSystem>`,
`EditorPlugin<class_EditorPlugin>`,
`EditorResourcePreview<class_EditorResourcePreview>`,
`HTTPRequest<class_HTTPRequest>`,
`InstancePlaceholder<class_InstancePlaceholder>`,
`MissingNode<class_MissingNode>`,
`MultiplayerSpawner<class_MultiplayerSpawner>`,
`MultiplayerSynchronizer<class_MultiplayerSynchronizer>`,
`NavigationAgent2D<class_NavigationAgent2D>`,
`NavigationAgent3D<class_NavigationAgent3D>`, `Node3D<class_Node3D>`,
`ResourcePreloader<class_ResourcePreloader>`,
`ShaderGlobalsOverride<class_ShaderGlobalsOverride>`,
`StatusIndicator<class_StatusIndicator>`, `Timer<class_Timer>`,
`Viewport<class_Viewport>`, `WorldEnvironment<class_WorldEnvironment>`

Base class for all scene objects.

classref-introduction-group

## Description

Nodes are Godot's building blocks. They can be assigned as the child of
another node, resulting in a tree arrangement. A given node can contain
any number of nodes as children with the requirement that all siblings
(direct children of a node) should have unique names.

A tree of nodes is called a *scene*. Scenes can be saved to the disk and
then instantiated into other scenes. This allows for very high
flexibility in the architecture and data model of Godot projects.

\*\*Scene tree:\*\* The `SceneTree<class_SceneTree>` contains the active
tree of nodes. When a node is added to the scene tree, it receives the
`NOTIFICATION_ENTER_TREE<class_Node_constant_NOTIFICATION_ENTER_TREE>`
notification and its
`_enter_tree<class_Node_private_method__enter_tree>` callback is
triggered. Child nodes are always added *after* their parent node, i.e.
the `_enter_tree<class_Node_private_method__enter_tree>` callback of a
parent node will be triggered before its child's.

Once all nodes have been added in the scene tree, they receive the
`NOTIFICATION_READY<class_Node_constant_NOTIFICATION_READY>`
notification and their respective
`_ready<class_Node_private_method__ready>` callbacks are triggered. For
groups of nodes, the `_ready<class_Node_private_method__ready>` callback
is called in reverse order, starting with the children and moving up to
the parent nodes.

This means that when adding a node to the scene tree, the following
order will be used for the callbacks:
`_enter_tree<class_Node_private_method__enter_tree>` of the parent,
`_enter_tree<class_Node_private_method__enter_tree>` of the children,
`_ready<class_Node_private_method__ready>` of the children and finally
`_ready<class_Node_private_method__ready>` of the parent (recursively
for the entire scene tree).

\*\*Processing:\*\* Nodes can override the "process" state, so that they
receive a callback on each frame requesting them to process (do
something). Normal processing (callback
`_process<class_Node_private_method__process>`, toggled with
`set_process<class_Node_method_set_process>`) happens as fast as
possible and is dependent on the frame rate, so the processing time
*delta* (in seconds) is passed as an argument. Physics processing
(callback
`_physics_process<class_Node_private_method__physics_process>`, toggled
with `set_physics_process<class_Node_method_set_physics_process>`)
happens a fixed number of times per second (60 by default) and is useful
for code related to the physics engine.

Nodes can also process input events. When present, the
`_input<class_Node_private_method__input>` function will be called for
each input that the program receives. In many cases, this can be
overkill (unless used for simple projects), and the
`_unhandled_input<class_Node_private_method__unhandled_input>` function
might be preferred; it is called when the input event was not handled by
anyone else (typically, GUI `Control<class_Control>` nodes), ensuring
that the node only receives the events that were meant for it.

To keep track of the scene hierarchy (especially when instantiating
scenes into other scenes), an "owner" can be set for the node with the
`owner<class_Node_property_owner>` property. This keeps track of who
instantiated what. This is mostly useful when writing editors and tools,
though.

Finally, when a node is freed with
`Object.free<class_Object_method_free>` or
`queue_free<class_Node_method_queue_free>`, it will also free all its
children.

\*\*Groups:\*\* Nodes can be added to as many groups as you want to be
easy to manage, you could create groups like "enemies" or "collectables"
for example, depending on your game. See
`add_to_group<class_Node_method_add_to_group>`,
`is_in_group<class_Node_method_is_in_group>` and
`remove_from_group<class_Node_method_remove_from_group>`. You can then
retrieve all nodes in these groups, iterate them and even call methods
on groups via the methods on `SceneTree<class_SceneTree>`.

\*\*Networking with nodes:\*\* After connecting to a server (or making
one, see `ENetMultiplayerPeer<class_ENetMultiplayerPeer>`), it is
possible to use the built-in RPC (remote procedure call) system to
communicate over the network. By calling `rpc<class_Node_method_rpc>`
with a method name, it will be called locally and in all connected peers
(peers = clients and the server that accepts connections). To identify
which node receives the RPC call, Godot will use its
`NodePath<class_NodePath>` (make sure node names are the same on all
peers). Also, take a look at the high-level networking tutorial and
corresponding demos.

\*\*Note:\*\* The `script` property is part of the
`Object<class_Object>` class, not **Node**. It isn't exposed like most
properties but does have a setter and getter (see
`Object.set_script<class_Object_method_set_script>` and
`Object.get_script<class_Object_method_get_script>`).

classref-introduction-group

## Tutorials

-   `Nodes and scenes <../getting_started/step_by_step/nodes_and_scenes>`
-   [All Demos](https://github.com/godotengine/godot-demo-projects/)

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

**child\_entered\_tree**(node: `Node<class_Node>`)
`🔗<class_Node_signal_child_entered_tree>`

Emitted when the child `node` enters the `SceneTree<class_SceneTree>`,
usually because this node entered the tree (see
`tree_entered<class_Node_signal_tree_entered>`), or
`add_child<class_Node_method_add_child>` has been called.

This signal is emitted *after* the child node's own
`NOTIFICATION_ENTER_TREE<class_Node_constant_NOTIFICATION_ENTER_TREE>`
and `tree_entered<class_Node_signal_tree_entered>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**child\_exiting\_tree**(node: `Node<class_Node>`)
`🔗<class_Node_signal_child_exiting_tree>`

Emitted when the child `node` is about to exit the
`SceneTree<class_SceneTree>`, usually because this node is exiting the
tree (see `tree_exiting<class_Node_signal_tree_exiting>`), or because
the child `node` is being removed or freed.

When this signal is received, the child `node` is still accessible
inside the tree. This signal is emitted *after* the child node's own
`tree_exiting<class_Node_signal_tree_exiting>` and
`NOTIFICATION_EXIT_TREE<class_Node_constant_NOTIFICATION_EXIT_TREE>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**child\_order\_changed**() `🔗<class_Node_signal_child_order_changed>`

Emitted when the list of children is changed. This happens when child
nodes are added, moved or removed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**editor\_description\_changed**(node: `Node<class_Node>`)
`🔗<class_Node_signal_editor_description_changed>`

Emitted when the node's editor description field changed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**ready**() `🔗<class_Node_signal_ready>`

Emitted when the node is considered ready, after
`_ready<class_Node_private_method__ready>` is called.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**renamed**() `🔗<class_Node_signal_renamed>`

Emitted when the node's `name<class_Node_property_name>` is changed, if
the node is inside the tree.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**replacing\_by**(node: `Node<class_Node>`)
`🔗<class_Node_signal_replacing_by>`

Emitted when this node is being replaced by the `node`, see
`replace_by<class_Node_method_replace_by>`.

This signal is emitted *after* `node` has been added as a child of the
original parent node, but *before* all original child nodes have been
reparented to `node`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tree\_entered**() `🔗<class_Node_signal_tree_entered>`

Emitted when the node enters the tree.

This signal is emitted *after* the related
`NOTIFICATION_ENTER_TREE<class_Node_constant_NOTIFICATION_ENTER_TREE>`
notification.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tree\_exited**() `🔗<class_Node_signal_tree_exited>`

Emitted after the node exits the tree and is no longer active.

This signal is emitted *after* the related
`NOTIFICATION_EXIT_TREE<class_Node_constant_NOTIFICATION_EXIT_TREE>`
notification.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tree\_exiting**() `🔗<class_Node_signal_tree_exiting>`

Emitted when the node is just about to exit the tree. The node is still
valid. As such, this is the right place for de-initialization (or a
"destructor", if you will).

This signal is emitted *after* the node's
`_exit_tree<class_Node_private_method__exit_tree>`, and *before* the
related
`NOTIFICATION_EXIT_TREE<class_Node_constant_NOTIFICATION_EXIT_TREE>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ProcessMode**: `🔗<enum_Node_ProcessMode>`

classref-enumeration-constant

`ProcessMode<enum_Node_ProcessMode>` **PROCESS\_MODE\_INHERIT** = `0`

Inherits `process_mode<class_Node_property_process_mode>` from the
node's parent. This is the default for any newly created node.

classref-enumeration-constant

`ProcessMode<enum_Node_ProcessMode>` **PROCESS\_MODE\_PAUSABLE** = `1`

Stops processing when
`SceneTree.paused<class_SceneTree_property_paused>` is `true`. This is
the inverse of
`PROCESS_MODE_WHEN_PAUSED<class_Node_constant_PROCESS_MODE_WHEN_PAUSED>`,
and the default for the root node.

classref-enumeration-constant

`ProcessMode<enum_Node_ProcessMode>` **PROCESS\_MODE\_WHEN\_PAUSED** =
`2`

Process **only** when
`SceneTree.paused<class_SceneTree_property_paused>` is `true`. This is
the inverse of
`PROCESS_MODE_PAUSABLE<class_Node_constant_PROCESS_MODE_PAUSABLE>`.

classref-enumeration-constant

`ProcessMode<enum_Node_ProcessMode>` **PROCESS\_MODE\_ALWAYS** = `3`

Always process. Keeps processing, ignoring
`SceneTree.paused<class_SceneTree_property_paused>`. This is the inverse
of `PROCESS_MODE_DISABLED<class_Node_constant_PROCESS_MODE_DISABLED>`.

classref-enumeration-constant

`ProcessMode<enum_Node_ProcessMode>` **PROCESS\_MODE\_DISABLED** = `4`

Never process. Completely disables processing, ignoring
`SceneTree.paused<class_SceneTree_property_paused>`. This is the inverse
of `PROCESS_MODE_ALWAYS<class_Node_constant_PROCESS_MODE_ALWAYS>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ProcessThreadGroup**: `🔗<enum_Node_ProcessThreadGroup>`

classref-enumeration-constant

`ProcessThreadGroup<enum_Node_ProcessThreadGroup>`
**PROCESS\_THREAD\_GROUP\_INHERIT** = `0`

Process this node based on the thread group mode of the first parent (or
grandparent) node that has a thread group mode that is not inherit. See
`process_thread_group<class_Node_property_process_thread_group>` for
more information.

classref-enumeration-constant

`ProcessThreadGroup<enum_Node_ProcessThreadGroup>`
**PROCESS\_THREAD\_GROUP\_MAIN\_THREAD** = `1`

Process this node (and child nodes set to inherit) on the main thread.
See `process_thread_group<class_Node_property_process_thread_group>` for
more information.

classref-enumeration-constant

`ProcessThreadGroup<enum_Node_ProcessThreadGroup>`
**PROCESS\_THREAD\_GROUP\_SUB\_THREAD** = `2`

Process this node (and child nodes set to inherit) on a sub-thread. See
`process_thread_group<class_Node_property_process_thread_group>` for
more information.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **ProcessThreadMessages**: `🔗<enum_Node_ProcessThreadMessages>`

classref-enumeration-constant

`ProcessThreadMessages<enum_Node_ProcessThreadMessages>`
**FLAG\_PROCESS\_THREAD\_MESSAGES** = `1`

Allows this node to process threaded messages created with
`call_deferred_thread_group<class_Node_method_call_deferred_thread_group>`
right before `_process<class_Node_private_method__process>` is called.

classref-enumeration-constant

`ProcessThreadMessages<enum_Node_ProcessThreadMessages>`
**FLAG\_PROCESS\_THREAD\_MESSAGES\_PHYSICS** = `2`

Allows this node to process threaded messages created with
`call_deferred_thread_group<class_Node_method_call_deferred_thread_group>`
right before
`_physics_process<class_Node_private_method__physics_process>` is
called.

classref-enumeration-constant

`ProcessThreadMessages<enum_Node_ProcessThreadMessages>`
**FLAG\_PROCESS\_THREAD\_MESSAGES\_ALL** = `3`

Allows this node to process threaded messages created with
`call_deferred_thread_group<class_Node_method_call_deferred_thread_group>`
right before either `_process<class_Node_private_method__process>` or
`_physics_process<class_Node_private_method__physics_process>` are
called.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PhysicsInterpolationMode**:
`🔗<enum_Node_PhysicsInterpolationMode>`

classref-enumeration-constant

`PhysicsInterpolationMode<enum_Node_PhysicsInterpolationMode>`
**PHYSICS\_INTERPOLATION\_MODE\_INHERIT** = `0`

Inherits
`physics_interpolation_mode<class_Node_property_physics_interpolation_mode>`
from the node's parent. This is the default for any newly created node.

classref-enumeration-constant

`PhysicsInterpolationMode<enum_Node_PhysicsInterpolationMode>`
**PHYSICS\_INTERPOLATION\_MODE\_ON** = `1`

Enables physics interpolation for this node and for children set to
`PHYSICS_INTERPOLATION_MODE_INHERIT<class_Node_constant_PHYSICS_INTERPOLATION_MODE_INHERIT>`.
This is the default for the root node.

classref-enumeration-constant

`PhysicsInterpolationMode<enum_Node_PhysicsInterpolationMode>`
**PHYSICS\_INTERPOLATION\_MODE\_OFF** = `2`

Disables physics interpolation for this node and for children set to
`PHYSICS_INTERPOLATION_MODE_INHERIT<class_Node_constant_PHYSICS_INTERPOLATION_MODE_INHERIT>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **DuplicateFlags**: `🔗<enum_Node_DuplicateFlags>`

classref-enumeration-constant

`DuplicateFlags<enum_Node_DuplicateFlags>` **DUPLICATE\_SIGNALS** = `1`

Duplicate the node's signal connections.

classref-enumeration-constant

`DuplicateFlags<enum_Node_DuplicateFlags>` **DUPLICATE\_GROUPS** = `2`

Duplicate the node's groups.

classref-enumeration-constant

`DuplicateFlags<enum_Node_DuplicateFlags>` **DUPLICATE\_SCRIPTS** = `4`

Duplicate the node's script (also overriding the duplicated children's
scripts, if combined with
`DUPLICATE_USE_INSTANTIATION<class_Node_constant_DUPLICATE_USE_INSTANTIATION>`).

classref-enumeration-constant

`DuplicateFlags<enum_Node_DuplicateFlags>`
**DUPLICATE\_USE\_INSTANTIATION** = `8`

Duplicate using
`PackedScene.instantiate<class_PackedScene_method_instantiate>`. If the
node comes from a scene saved on disk, re-uses
`PackedScene.instantiate<class_PackedScene_method_instantiate>` as the
base for the duplicated node and its children.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **InternalMode**: `🔗<enum_Node_InternalMode>`

classref-enumeration-constant

`InternalMode<enum_Node_InternalMode>` **INTERNAL\_MODE\_DISABLED** =
`0`

The node will not be internal.

classref-enumeration-constant

`InternalMode<enum_Node_InternalMode>` **INTERNAL\_MODE\_FRONT** = `1`

The node will be placed at the beginning of the parent's children,
before any non-internal sibling.

classref-enumeration-constant

`InternalMode<enum_Node_InternalMode>` **INTERNAL\_MODE\_BACK** = `2`

The node will be placed at the end of the parent's children, after any
non-internal sibling.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AutoTranslateMode**: `🔗<enum_Node_AutoTranslateMode>`

classref-enumeration-constant

`AutoTranslateMode<enum_Node_AutoTranslateMode>`
**AUTO\_TRANSLATE\_MODE\_INHERIT** = `0`

Inherits `auto_translate_mode<class_Node_property_auto_translate_mode>`
from the node's parent. This is the default for any newly created node.

classref-enumeration-constant

`AutoTranslateMode<enum_Node_AutoTranslateMode>`
**AUTO\_TRANSLATE\_MODE\_ALWAYS** = `1`

Always automatically translate. This is the inverse of
`AUTO_TRANSLATE_MODE_DISABLED<class_Node_constant_AUTO_TRANSLATE_MODE_DISABLED>`,
and the default for the root node.

classref-enumeration-constant

`AutoTranslateMode<enum_Node_AutoTranslateMode>`
**AUTO\_TRANSLATE\_MODE\_DISABLED** = `2`

Never automatically translate. This is the inverse of
`AUTO_TRANSLATE_MODE_ALWAYS<class_Node_constant_AUTO_TRANSLATE_MODE_ALWAYS>`.

String parsing for POT generation will be skipped for this node and
children that are set to
`AUTO_TRANSLATE_MODE_INHERIT<class_Node_constant_AUTO_TRANSLATE_MODE_INHERIT>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NOTIFICATION\_ENTER\_TREE** = `10`
`🔗<class_Node_constant_NOTIFICATION_ENTER_TREE>`

Notification received when the node enters a
`SceneTree<class_SceneTree>`. See
`_enter_tree<class_Node_private_method__enter_tree>`.

This notification is received *before* the related
`tree_entered<class_Node_signal_tree_entered>` signal.

classref-constant

**NOTIFICATION\_EXIT\_TREE** = `11`
`🔗<class_Node_constant_NOTIFICATION_EXIT_TREE>`

Notification received when the node is about to exit a
`SceneTree<class_SceneTree>`. See
`_exit_tree<class_Node_private_method__exit_tree>`.

This notification is received *after* the related
`tree_exiting<class_Node_signal_tree_exiting>` signal.

classref-constant

**NOTIFICATION\_MOVED\_IN\_PARENT** = `12`
`🔗<class_Node_constant_NOTIFICATION_MOVED_IN_PARENT>`

**Deprecated:** This notification is no longer sent by the engine. Use
`NOTIFICATION_CHILD_ORDER_CHANGED<class_Node_constant_NOTIFICATION_CHILD_ORDER_CHANGED>`
instead.

classref-constant

**NOTIFICATION\_READY** = `13`
`🔗<class_Node_constant_NOTIFICATION_READY>`

Notification received when the node is ready. See
`_ready<class_Node_private_method__ready>`.

classref-constant

**NOTIFICATION\_PAUSED** = `14`
`🔗<class_Node_constant_NOTIFICATION_PAUSED>`

Notification received when the node is paused. See
`process_mode<class_Node_property_process_mode>`.

classref-constant

**NOTIFICATION\_UNPAUSED** = `15`
`🔗<class_Node_constant_NOTIFICATION_UNPAUSED>`

Notification received when the node is unpaused. See
`process_mode<class_Node_property_process_mode>`.

classref-constant

**NOTIFICATION\_PHYSICS\_PROCESS** = `16`
`🔗<class_Node_constant_NOTIFICATION_PHYSICS_PROCESS>`

Notification received from the tree every physics frame when
`is_physics_processing<class_Node_method_is_physics_processing>` returns
`true`. See
`_physics_process<class_Node_private_method__physics_process>`.

classref-constant

**NOTIFICATION\_PROCESS** = `17`
`🔗<class_Node_constant_NOTIFICATION_PROCESS>`

Notification received from the tree every rendered frame when
`is_processing<class_Node_method_is_processing>` returns `true`. See
`_process<class_Node_private_method__process>`.

classref-constant

**NOTIFICATION\_PARENTED** = `18`
`🔗<class_Node_constant_NOTIFICATION_PARENTED>`

Notification received when the node is set as a child of another node
(see `add_child<class_Node_method_add_child>` and
`add_sibling<class_Node_method_add_sibling>`).

\*\*Note:\*\* This does *not* mean that the node entered the
`SceneTree<class_SceneTree>`.

classref-constant

**NOTIFICATION\_UNPARENTED** = `19`
`🔗<class_Node_constant_NOTIFICATION_UNPARENTED>`

Notification received when the parent node calls
`remove_child<class_Node_method_remove_child>` on this node.

\*\*Note:\*\* This does *not* mean that the node exited the
`SceneTree<class_SceneTree>`.

classref-constant

**NOTIFICATION\_SCENE\_INSTANTIATED** = `20`
`🔗<class_Node_constant_NOTIFICATION_SCENE_INSTANTIATED>`

Notification received *only* by the newly instantiated scene root node,
when `PackedScene.instantiate<class_PackedScene_method_instantiate>` is
completed.

classref-constant

**NOTIFICATION\_DRAG\_BEGIN** = `21`
`🔗<class_Node_constant_NOTIFICATION_DRAG_BEGIN>`

Notification received when a drag operation begins. All nodes receive
this notification, not only the dragged one.

Can be triggered either by dragging a `Control<class_Control>` that
provides drag data (see
`Control._get_drag_data<class_Control_private_method__get_drag_data>`)
or using `Control.force_drag<class_Control_method_force_drag>`.

Use
`Viewport.gui_get_drag_data<class_Viewport_method_gui_get_drag_data>` to
get the dragged data.

classref-constant

**NOTIFICATION\_DRAG\_END** = `22`
`🔗<class_Node_constant_NOTIFICATION_DRAG_END>`

Notification received when a drag operation ends.

Use
`Viewport.gui_is_drag_successful<class_Viewport_method_gui_is_drag_successful>`
to check if the drag succeeded.

classref-constant

**NOTIFICATION\_PATH\_RENAMED** = `23`
`🔗<class_Node_constant_NOTIFICATION_PATH_RENAMED>`

Notification received when the node's `name<class_Node_property_name>`
or one of its ancestors' `name<class_Node_property_name>` is changed.
This notification is *not* received when the node is removed from the
`SceneTree<class_SceneTree>`.

classref-constant

**NOTIFICATION\_CHILD\_ORDER\_CHANGED** = `24`
`🔗<class_Node_constant_NOTIFICATION_CHILD_ORDER_CHANGED>`

Notification received when the list of children is changed. This happens
when child nodes are added, moved or removed.

classref-constant

**NOTIFICATION\_INTERNAL\_PROCESS** = `25`
`🔗<class_Node_constant_NOTIFICATION_INTERNAL_PROCESS>`

Notification received from the tree every rendered frame when
`is_processing_internal<class_Node_method_is_processing_internal>`
returns `true`.

classref-constant

**NOTIFICATION\_INTERNAL\_PHYSICS\_PROCESS** = `26`
`🔗<class_Node_constant_NOTIFICATION_INTERNAL_PHYSICS_PROCESS>`

Notification received from the tree every physics frame when
`is_physics_processing_internal<class_Node_method_is_physics_processing_internal>`
returns `true`.

classref-constant

**NOTIFICATION\_POST\_ENTER\_TREE** = `27`
`🔗<class_Node_constant_NOTIFICATION_POST_ENTER_TREE>`

Notification received when the node enters the tree, just before
`NOTIFICATION_READY<class_Node_constant_NOTIFICATION_READY>` may be
received. Unlike the latter, it is sent every time the node enters tree,
not just once.

classref-constant

**NOTIFICATION\_DISABLED** = `28`
`🔗<class_Node_constant_NOTIFICATION_DISABLED>`

Notification received when the node is disabled. See
`PROCESS_MODE_DISABLED<class_Node_constant_PROCESS_MODE_DISABLED>`.

classref-constant

**NOTIFICATION\_ENABLED** = `29`
`🔗<class_Node_constant_NOTIFICATION_ENABLED>`

Notification received when the node is enabled again after being
disabled. See
`PROCESS_MODE_DISABLED<class_Node_constant_PROCESS_MODE_DISABLED>`.

classref-constant

**NOTIFICATION\_RESET\_PHYSICS\_INTERPOLATION** = `2001`
`🔗<class_Node_constant_NOTIFICATION_RESET_PHYSICS_INTERPOLATION>`

Notification received when
`reset_physics_interpolation<class_Node_method_reset_physics_interpolation>`
is called on the node or its ancestors.

classref-constant

**NOTIFICATION\_EDITOR\_PRE\_SAVE** = `9001`
`🔗<class_Node_constant_NOTIFICATION_EDITOR_PRE_SAVE>`

Notification received right before the scene with the node is saved in
the editor. This notification is only sent in the Godot editor and will
not occur in exported projects.

classref-constant

**NOTIFICATION\_EDITOR\_POST\_SAVE** = `9002`
`🔗<class_Node_constant_NOTIFICATION_EDITOR_POST_SAVE>`

Notification received right after the scene with the node is saved in
the editor. This notification is only sent in the Godot editor and will
not occur in exported projects.

classref-constant

**NOTIFICATION\_WM\_MOUSE\_ENTER** = `1002`
`🔗<class_Node_constant_NOTIFICATION_WM_MOUSE_ENTER>`

Notification received when the mouse enters the window.

Implemented for embedded windows and on desktop and web platforms.

classref-constant

**NOTIFICATION\_WM\_MOUSE\_EXIT** = `1003`
`🔗<class_Node_constant_NOTIFICATION_WM_MOUSE_EXIT>`

Notification received when the mouse leaves the window.

Implemented for embedded windows and on desktop and web platforms.

classref-constant

**NOTIFICATION\_WM\_WINDOW\_FOCUS\_IN** = `1004`
`🔗<class_Node_constant_NOTIFICATION_WM_WINDOW_FOCUS_IN>`

Notification received from the OS when the node's `Window<class_Window>`
ancestor is focused. This may be a change of focus between two windows
of the same engine instance, or from the OS desktop or a third-party
application to a window of the game (in which case
`NOTIFICATION_APPLICATION_FOCUS_IN<class_Node_constant_NOTIFICATION_APPLICATION_FOCUS_IN>`
is also received).

A `Window<class_Window>` node receives this notification when it is
focused.

classref-constant

**NOTIFICATION\_WM\_WINDOW\_FOCUS\_OUT** = `1005`
`🔗<class_Node_constant_NOTIFICATION_WM_WINDOW_FOCUS_OUT>`

Notification received from the OS when the node's `Window<class_Window>`
ancestor is defocused. This may be a change of focus between two windows
of the same engine instance, or from a window of the game to the OS
desktop or a third-party application (in which case
`NOTIFICATION_APPLICATION_FOCUS_OUT<class_Node_constant_NOTIFICATION_APPLICATION_FOCUS_OUT>`
is also received).

A `Window<class_Window>` node receives this notification when it is
defocused.

classref-constant

**NOTIFICATION\_WM\_CLOSE\_REQUEST** = `1006`
`🔗<class_Node_constant_NOTIFICATION_WM_CLOSE_REQUEST>`

Notification received from the OS when a close request is sent (e.g.
closing the window with a "Close" button or `Alt + F4`).

Implemented on desktop platforms.

classref-constant

**NOTIFICATION\_WM\_GO\_BACK\_REQUEST** = `1007`
`🔗<class_Node_constant_NOTIFICATION_WM_GO_BACK_REQUEST>`

Notification received from the OS when a go back request is sent (e.g.
pressing the "Back" button on Android).

Implemented only on Android.

classref-constant

**NOTIFICATION\_WM\_SIZE\_CHANGED** = `1008`
`🔗<class_Node_constant_NOTIFICATION_WM_SIZE_CHANGED>`

Notification received when the window is resized.

\*\*Note:\*\* Only the resized `Window<class_Window>` node receives this
notification, and it's not propagated to the child nodes.

classref-constant

**NOTIFICATION\_WM\_DPI\_CHANGE** = `1009`
`🔗<class_Node_constant_NOTIFICATION_WM_DPI_CHANGE>`

Notification received from the OS when the screen's dots per inch (DPI)
scale is changed. Only implemented on macOS.

classref-constant

**NOTIFICATION\_VP\_MOUSE\_ENTER** = `1010`
`🔗<class_Node_constant_NOTIFICATION_VP_MOUSE_ENTER>`

Notification received when the mouse cursor enters the
`Viewport<class_Viewport>`'s visible area, that is not occluded behind
other `Control<class_Control>`s or `Window<class_Window>`s, provided its
`Viewport.gui_disable_input<class_Viewport_property_gui_disable_input>`
is `false` and regardless if it's currently focused or not.

classref-constant

**NOTIFICATION\_VP\_MOUSE\_EXIT** = `1011`
`🔗<class_Node_constant_NOTIFICATION_VP_MOUSE_EXIT>`

Notification received when the mouse cursor leaves the
`Viewport<class_Viewport>`'s visible area, that is not occluded behind
other `Control<class_Control>`s or `Window<class_Window>`s, provided its
`Viewport.gui_disable_input<class_Viewport_property_gui_disable_input>`
is `false` and regardless if it's currently focused or not.

classref-constant

**NOTIFICATION\_OS\_MEMORY\_WARNING** = `2009`
`🔗<class_Node_constant_NOTIFICATION_OS_MEMORY_WARNING>`

Notification received from the OS when the application is exceeding its
allocated memory.

Implemented only on iOS.

classref-constant

**NOTIFICATION\_TRANSLATION\_CHANGED** = `2010`
`🔗<class_Node_constant_NOTIFICATION_TRANSLATION_CHANGED>`

Notification received when translations may have changed. Can be
triggered by the user changing the locale, changing
`auto_translate_mode<class_Node_property_auto_translate_mode>` or when
the node enters the scene tree. Can be used to respond to language
changes, for example to change the UI strings on the fly. Useful when
working with the built-in translation support, like
`Object.tr<class_Object_method_tr>`.

\*\*Note:\*\* This notification is received alongside
`NOTIFICATION_ENTER_TREE<class_Node_constant_NOTIFICATION_ENTER_TREE>`,
so if you are instantiating a scene, the child nodes will not be
initialized yet. You can use it to setup translations for this node,
child nodes created from script, or if you want to access child nodes
added in the editor, make sure the node is ready using
`is_node_ready<class_Node_method_is_node_ready>`.

    func _notification(what):
        if what == NOTIFICATION_TRANSLATION_CHANGED:
            if not is_node_ready():
                await ready # Wait until ready signal.
            $Label.text = atr("%d Bananas") % banana_counter

classref-constant

**NOTIFICATION\_WM\_ABOUT** = `2011`
`🔗<class_Node_constant_NOTIFICATION_WM_ABOUT>`

Notification received from the OS when a request for "About" information
is sent.

Implemented only on macOS.

classref-constant

**NOTIFICATION\_CRASH** = `2012`
`🔗<class_Node_constant_NOTIFICATION_CRASH>`

Notification received from Godot's crash handler when the engine is
about to crash.

Implemented on desktop platforms, if the crash handler is enabled.

classref-constant

**NOTIFICATION\_OS\_IME\_UPDATE** = `2013`
`🔗<class_Node_constant_NOTIFICATION_OS_IME_UPDATE>`

Notification received from the OS when an update of the Input Method
Engine occurs (e.g. change of IME cursor position or composition
string).

Implemented only on macOS.

classref-constant

**NOTIFICATION\_APPLICATION\_RESUMED** = `2014`
`🔗<class_Node_constant_NOTIFICATION_APPLICATION_RESUMED>`

Notification received from the OS when the application is resumed.

Specific to the Android and iOS platforms.

classref-constant

**NOTIFICATION\_APPLICATION\_PAUSED** = `2015`
`🔗<class_Node_constant_NOTIFICATION_APPLICATION_PAUSED>`

Notification received from the OS when the application is paused.

Specific to the Android and iOS platforms.

\*\*Note:\*\* On iOS, you only have approximately 5 seconds to finish a
task started by this signal. If you go over this allotment, iOS will
kill the app instead of pausing it.

classref-constant

**NOTIFICATION\_APPLICATION\_FOCUS\_IN** = `2016`
`🔗<class_Node_constant_NOTIFICATION_APPLICATION_FOCUS_IN>`

Notification received from the OS when the application is focused, i.e.
when changing the focus from the OS desktop or a thirdparty application
to any open window of the Godot instance.

Implemented on desktop and mobile platforms.

classref-constant

**NOTIFICATION\_APPLICATION\_FOCUS\_OUT** = `2017`
`🔗<class_Node_constant_NOTIFICATION_APPLICATION_FOCUS_OUT>`

Notification received from the OS when the application is defocused,
i.e. when changing the focus from any open window of the Godot instance
to the OS desktop or a thirdparty application.

Implemented on desktop and mobile platforms.

classref-constant

**NOTIFICATION\_TEXT\_SERVER\_CHANGED** = `2018`
`🔗<class_Node_constant_NOTIFICATION_TEXT_SERVER_CHANGED>`

Notification received when the `TextServer<class_TextServer>` is
changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`AutoTranslateMode<enum_Node_AutoTranslateMode>`
**auto\_translate\_mode** = `0`
`🔗<class_Node_property_auto_translate_mode>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_translate\_mode**(value:
    `AutoTranslateMode<enum_Node_AutoTranslateMode>`)
-   `AutoTranslateMode<enum_Node_AutoTranslateMode>`
    **get\_auto\_translate\_mode**()

Defines if any text should automatically change to its translated
version depending on the current locale (for nodes such as
`Label<class_Label>`, `RichTextLabel<class_RichTextLabel>`,
`Window<class_Window>`, etc.). Also decides if the node's strings should
be parsed for POT generation.

\*\*Note:\*\* For the root node, auto translate mode can also be set via
`ProjectSettings.internationalization/rendering/root_node_auto_translate<class_ProjectSettings_property_internationalization/rendering/root_node_auto_translate>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **editor\_description** = `""`
`🔗<class_Node_property_editor_description>`

classref-property-setget

-   `void (No return value.)` **set\_editor\_description**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_editor\_description**()

An optional description to the node. It will be displayed as a tooltip
when hovering over the node in the editor's Scene dock.

classref-item-separator

------------------------------------------------------------------------

classref-property

`MultiplayerAPI<class_MultiplayerAPI>` **multiplayer**
`🔗<class_Node_property_multiplayer>`

classref-property-setget

-   `MultiplayerAPI<class_MultiplayerAPI>` **get\_multiplayer**()

The `MultiplayerAPI<class_MultiplayerAPI>` instance associated with this
node. See
`SceneTree.get_multiplayer<class_SceneTree_method_get_multiplayer>`.

\*\*Note:\*\* Renaming the node, or moving it in the tree, will not move
the `MultiplayerAPI<class_MultiplayerAPI>` to the new path, you will
have to update this manually.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **name** `🔗<class_Node_property_name>`

classref-property-setget

-   `void (No return value.)` **set\_name**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_name**()

The name of the node. This name must be unique among the siblings (other
child nodes from the same parent). When set to an existing sibling's
name, the node is automatically renamed.

\*\*Note:\*\* When changing the name, the following characters will be
replaced with an underscore: (`.` `:` `@` `/` `"` `%`). In particular,
the `@` character is reserved for auto-generated names. See also
`String.validate_node_name<class_String_method_validate_node_name>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Node<class_Node>` **owner** `🔗<class_Node_property_owner>`

classref-property-setget

-   `void (No return value.)` **set\_owner**(value: `Node<class_Node>`)
-   `Node<class_Node>` **get\_owner**()

The owner of this node. The owner must be an ancestor of this node. When
packing the owner node in a `PackedScene<class_PackedScene>`, all the
nodes it owns are also saved with it.

\*\*Note:\*\* In the editor, nodes not owned by the scene root are
usually not displayed in the Scene dock, and will **not** be saved. To
prevent this, remember to set the owner after calling
`add_child<class_Node_method_add_child>`. See also (see
`unique_name_in_owner<class_Node_property_unique_name_in_owner>`)

classref-item-separator

------------------------------------------------------------------------

classref-property

`PhysicsInterpolationMode<enum_Node_PhysicsInterpolationMode>`
**physics\_interpolation\_mode** = `0`
`🔗<class_Node_property_physics_interpolation_mode>`

classref-property-setget

-   `void (No return value.)`
    **set\_physics\_interpolation\_mode**(value:
    `PhysicsInterpolationMode<enum_Node_PhysicsInterpolationMode>`)
-   `PhysicsInterpolationMode<enum_Node_PhysicsInterpolationMode>`
    **get\_physics\_interpolation\_mode**()

Allows enabling or disabling physics interpolation per node, offering a
finer grain of control than turning physics interpolation on and off
globally. See
`ProjectSettings.physics/common/physics_interpolation<class_ProjectSettings_property_physics/common/physics_interpolation>`
and
`SceneTree.physics_interpolation<class_SceneTree_property_physics_interpolation>`
for the global setting.

\*\*Note:\*\* When teleporting a node to a distant position you should
temporarily disable interpolation with
`reset_physics_interpolation<class_Node_method_reset_physics_interpolation>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ProcessMode<enum_Node_ProcessMode>` **process\_mode** = `0`
`🔗<class_Node_property_process_mode>`

classref-property-setget

-   `void (No return value.)` **set\_process\_mode**(value:
    `ProcessMode<enum_Node_ProcessMode>`)
-   `ProcessMode<enum_Node_ProcessMode>` **get\_process\_mode**()

The node's processing behavior (see
`ProcessMode<enum_Node_ProcessMode>`). To check if the node can process
in its current mode, use `can_process<class_Node_method_can_process>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **process\_physics\_priority** = `0`
`🔗<class_Node_property_process_physics_priority>`

classref-property-setget

-   `void (No return value.)` **set\_physics\_process\_priority**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_physics\_process\_priority**()

Similar to `process_priority<class_Node_property_process_priority>` but
for
`NOTIFICATION_PHYSICS_PROCESS<class_Node_constant_NOTIFICATION_PHYSICS_PROCESS>`,
`_physics_process<class_Node_private_method__physics_process>` or the
internal version.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **process\_priority** = `0`
`🔗<class_Node_property_process_priority>`

classref-property-setget

-   `void (No return value.)` **set\_process\_priority**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_process\_priority**()

The node's execution order of the process callbacks
(`_process<class_Node_private_method__process>`,
`_physics_process<class_Node_private_method__physics_process>`, and
internal processing). Nodes whose priority value is *lower* call their
process callbacks first, regardless of tree order.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ProcessThreadGroup<enum_Node_ProcessThreadGroup>`
**process\_thread\_group** = `0`
`🔗<class_Node_property_process_thread_group>`

classref-property-setget

-   `void (No return value.)` **set\_process\_thread\_group**(value:
    `ProcessThreadGroup<enum_Node_ProcessThreadGroup>`)
-   `ProcessThreadGroup<enum_Node_ProcessThreadGroup>`
    **get\_process\_thread\_group**()

Set the process thread group for this node (basically, whether it
receives
`NOTIFICATION_PROCESS<class_Node_constant_NOTIFICATION_PROCESS>`,
`NOTIFICATION_PHYSICS_PROCESS<class_Node_constant_NOTIFICATION_PHYSICS_PROCESS>`,
`_process<class_Node_private_method__process>` or
`_physics_process<class_Node_private_method__physics_process>` (and the
internal versions) on the main thread or in a sub-thread.

By default, the thread group is
`PROCESS_THREAD_GROUP_INHERIT<class_Node_constant_PROCESS_THREAD_GROUP_INHERIT>`,
which means that this node belongs to the same thread group as the
parent node. The thread groups means that nodes in a specific thread
group will process together, separate to other thread groups (depending
on
`process_thread_group_order<class_Node_property_process_thread_group_order>`).
If the value is set is
`PROCESS_THREAD_GROUP_SUB_THREAD<class_Node_constant_PROCESS_THREAD_GROUP_SUB_THREAD>`,
this thread group will occur on a sub thread (not the main thread),
otherwise if set to
`PROCESS_THREAD_GROUP_MAIN_THREAD<class_Node_constant_PROCESS_THREAD_GROUP_MAIN_THREAD>`
it will process on the main thread. If there is not a parent or
grandparent node set to something other than inherit, the node will
belong to the *default thread group*. This default group will process on
the main thread and its group order is 0.

During processing in a sub-thread, accessing most functions in nodes
outside the thread group is forbidden (and it will result in an error in
debug mode). Use
`Object.call_deferred<class_Object_method_call_deferred>`,
`call_thread_safe<class_Node_method_call_thread_safe>`,
`call_deferred_thread_group<class_Node_method_call_deferred_thread_group>`
and the likes in order to communicate from the thread groups to the main
thread (or to other thread groups).

To better understand process thread groups, the idea is that any node
set to any other value than
`PROCESS_THREAD_GROUP_INHERIT<class_Node_constant_PROCESS_THREAD_GROUP_INHERIT>`
will include any child (and grandchild) nodes set to inherit into its
process thread group. This means that the processing of all the nodes in
the group will happen together, at the same time as the node including
them.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **process\_thread\_group\_order**
`🔗<class_Node_property_process_thread_group_order>`

classref-property-setget

-   `void (No return value.)`
    **set\_process\_thread\_group\_order**(value: `int<class_int>`)
-   `int<class_int>` **get\_process\_thread\_group\_order**()

Change the process thread group order. Groups with a lesser order will
process before groups with a greater order. This is useful when a large
amount of nodes process in sub thread and, afterwards, another group
wants to collect their result in the main thread, as an example.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`ProcessThreadMessages<enum_Node_ProcessThreadMessages>`\]
**process\_thread\_messages**
`🔗<class_Node_property_process_thread_messages>`

classref-property-setget

-   `void (No return value.)` **set\_process\_thread\_messages**(value:
    `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`ProcessThreadMessages<enum_Node_ProcessThreadMessages>`\])
-   `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`ProcessThreadMessages<enum_Node_ProcessThreadMessages>`\]
    **get\_process\_thread\_messages**()

Set whether the current thread group will process messages (calls to
`call_deferred_thread_group<class_Node_method_call_deferred_thread_group>`
on threads), and whether it wants to receive them during regular process
or physics process callbacks.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **scene\_file\_path**
`🔗<class_Node_property_scene_file_path>`

classref-property-setget

-   `void (No return value.)` **set\_scene\_file\_path**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_scene\_file\_path**()

The original scene's file path, if the node has been instantiated from a
`PackedScene<class_PackedScene>` file. Only scene root nodes contains
this.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **unique\_name\_in\_owner** = `false`
`🔗<class_Node_property_unique_name_in_owner>`

classref-property-setget

-   `void (No return value.)` **set\_unique\_name\_in\_owner**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_unique\_name\_in\_owner**()

If `true`, the node can be accessed from any node sharing the same
`owner<class_Node_property_owner>` or from the
`owner<class_Node_property_owner>` itself, with special `%Name` syntax
in `get_node<class_Node_method_get_node>`.

\*\*Note:\*\* If another node with the same
`owner<class_Node_property_owner>` shares the same
`name<class_Node_property_name>` as this node, the other node will no
longer be accessible as unique.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_enter\_tree**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Node_private_method__enter_tree>`

Called when the node enters the `SceneTree<class_SceneTree>` (e.g. upon
instantiating, scene changing, or after calling
`add_child<class_Node_method_add_child>` in a script). If the node has
children, its `_enter_tree<class_Node_private_method__enter_tree>`
callback will be called first, and then that of the children.

Corresponds to the
`NOTIFICATION_ENTER_TREE<class_Node_constant_NOTIFICATION_ENTER_TREE>`
notification in
`Object._notification<class_Object_private_method__notification>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_exit\_tree**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Node_private_method__exit_tree>`

Called when the node is about to leave the `SceneTree<class_SceneTree>`
(e.g. upon freeing, scene changing, or after calling
`remove_child<class_Node_method_remove_child>` in a script). If the node
has children, its `_exit_tree<class_Node_private_method__exit_tree>`
callback will be called last, after all its children have left the tree.

Corresponds to the
`NOTIFICATION_EXIT_TREE<class_Node_constant_NOTIFICATION_EXIT_TREE>`
notification in
`Object._notification<class_Object_private_method__notification>` and
signal `tree_exiting<class_Node_signal_tree_exiting>`. To get notified
when the node has already left the active tree, connect to the
`tree_exited<class_Node_signal_tree_exited>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_configuration\_warnings**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_private_method__get_configuration_warnings>`

The elements in the array returned from this method are displayed as
warnings in the Scene dock if the script that overrides it is a `tool`
script.

Returning an empty array produces no warnings.

Call
`update_configuration_warnings<class_Node_method_update_configuration_warnings>`
when the warnings need to be updated for this node.

    @export var energy = 0:
        set(value):
            energy = value
            update_configuration_warnings()

    func _get_configuration_warnings():
        if energy < 0:
            return ["Energy must be 0 or greater."]
        else:
            return []

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_input**(event:
`InputEvent<class_InputEvent>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Node_private_method__input>`

Called when there is an input event. The input event propagates up
through the node tree until a node consumes it.

It is only called if input processing is enabled, which is done
automatically if this method is overridden, and can be toggled with
`set_process_input<class_Node_method_set_process_input>`.

To consume the input event and stop it propagating further to other
nodes,
`Viewport.set_input_as_handled<class_Viewport_method_set_input_as_handled>`
can be called.

For gameplay input,
`_unhandled_input<class_Node_private_method__unhandled_input>` and
`_unhandled_key_input<class_Node_private_method__unhandled_key_input>`
are usually a better fit as they allow the GUI to intercept the events
first.

\*\*Note:\*\* This method is only called if the node is present in the
scene tree (i.e. if it's not an orphan).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_physics\_process**(delta:
`float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Node_private_method__physics_process>`

Called during the physics processing step of the main loop. Physics
processing means that the frame rate is synced to the physics, i.e. the
`delta` variable should be constant. `delta` is in seconds.

It is only called if physics processing is enabled, which is done
automatically if this method is overridden, and can be toggled with
`set_physics_process<class_Node_method_set_physics_process>`.

Corresponds to the
`NOTIFICATION_PHYSICS_PROCESS<class_Node_constant_NOTIFICATION_PHYSICS_PROCESS>`
notification in
`Object._notification<class_Object_private_method__notification>`.

\*\*Note:\*\* This method is only called if the node is present in the
scene tree (i.e. if it's not an orphan).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_process**(delta: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Node_private_method__process>`

Called during the processing step of the main loop. Processing happens
at every frame and as fast as possible, so the `delta` time since the
previous frame is not constant. `delta` is in seconds.

It is only called if processing is enabled, which is done automatically
if this method is overridden, and can be toggled with
`set_process<class_Node_method_set_process>`.

Corresponds to the
`NOTIFICATION_PROCESS<class_Node_constant_NOTIFICATION_PROCESS>`
notification in
`Object._notification<class_Object_private_method__notification>`.

\*\*Note:\*\* This method is only called if the node is present in the
scene tree (i.e. if it's not an orphan).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_ready**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Node_private_method__ready>`

Called when the node is "ready", i.e. when both the node and its
children have entered the scene tree. If the node has children, their
`_ready<class_Node_private_method__ready>` callbacks get triggered
first, and the parent node will receive the ready notification
afterwards.

Corresponds to the
`NOTIFICATION_READY<class_Node_constant_NOTIFICATION_READY>`
notification in
`Object._notification<class_Object_private_method__notification>`. See
also the `@onready` annotation for variables.

Usually used for initialization. For even earlier initialization,
`Object._init<class_Object_private_method__init>` may be used. See also
`_enter_tree<class_Node_private_method__enter_tree>`.

\*\*Note:\*\* This method may be called only once for each node. After
removing a node from the scene tree and adding it again,
`_ready<class_Node_private_method__ready>` will **not** be called a
second time. This can be bypassed by requesting another call with
`request_ready<class_Node_method_request_ready>`, which may be called
anywhere before adding the node again.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_shortcut\_input**(event:
`InputEvent<class_InputEvent>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Node_private_method__shortcut_input>`

Called when an `InputEventKey<class_InputEventKey>`,
`InputEventShortcut<class_InputEventShortcut>`, or
`InputEventJoypadButton<class_InputEventJoypadButton>` hasn't been
consumed by `_input<class_Node_private_method__input>` or any GUI
`Control<class_Control>` item. It is called before
`_unhandled_key_input<class_Node_private_method__unhandled_key_input>`
and `_unhandled_input<class_Node_private_method__unhandled_input>`. The
input event propagates up through the node tree until a node consumes
it.

It is only called if shortcut processing is enabled, which is done
automatically if this method is overridden, and can be toggled with
`set_process_shortcut_input<class_Node_method_set_process_shortcut_input>`.

To consume the input event and stop it propagating further to other
nodes,
`Viewport.set_input_as_handled<class_Viewport_method_set_input_as_handled>`
can be called.

This method can be used to handle shortcuts. For generic GUI events, use
`_input<class_Node_private_method__input>` instead. Gameplay events
should usually be handled with either
`_unhandled_input<class_Node_private_method__unhandled_input>` or
`_unhandled_key_input<class_Node_private_method__unhandled_key_input>`.

\*\*Note:\*\* This method is only called if the node is present in the
scene tree (i.e. if it's not orphan).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_unhandled\_input**(event:
`InputEvent<class_InputEvent>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Node_private_method__unhandled_input>`

Called when an `InputEvent<class_InputEvent>` hasn't been consumed by
`_input<class_Node_private_method__input>` or any GUI
`Control<class_Control>` item. It is called after
`_shortcut_input<class_Node_private_method__shortcut_input>` and after
`_unhandled_key_input<class_Node_private_method__unhandled_key_input>`.
The input event propagates up through the node tree until a node
consumes it.

It is only called if unhandled input processing is enabled, which is
done automatically if this method is overridden, and can be toggled with
`set_process_unhandled_input<class_Node_method_set_process_unhandled_input>`.

To consume the input event and stop it propagating further to other
nodes,
`Viewport.set_input_as_handled<class_Viewport_method_set_input_as_handled>`
can be called.

For gameplay input, this method is usually a better fit than
`_input<class_Node_private_method__input>`, as GUI events need a higher
priority. For keyboard shortcuts, consider using
`_shortcut_input<class_Node_private_method__shortcut_input>` instead, as
it is called before this method. Finally, to handle keyboard events,
consider using
`_unhandled_key_input<class_Node_private_method__unhandled_key_input>`
for performance reasons.

\*\*Note:\*\* This method is only called if the node is present in the
scene tree (i.e. if it's not an orphan).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_unhandled\_key\_input**(event:
`InputEvent<class_InputEvent>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Node_private_method__unhandled_key_input>`

Called when an `InputEventKey<class_InputEventKey>` hasn't been consumed
by `_input<class_Node_private_method__input>` or any GUI
`Control<class_Control>` item. It is called after
`_shortcut_input<class_Node_private_method__shortcut_input>` but before
`_unhandled_input<class_Node_private_method__unhandled_input>`. The
input event propagates up through the node tree until a node consumes
it.

It is only called if unhandled key input processing is enabled, which is
done automatically if this method is overridden, and can be toggled with
`set_process_unhandled_key_input<class_Node_method_set_process_unhandled_key_input>`.

To consume the input event and stop it propagating further to other
nodes,
`Viewport.set_input_as_handled<class_Viewport_method_set_input_as_handled>`
can be called.

This method can be used to handle Unicode character input with `Alt`,
`Alt + Ctrl`, and `Alt + Shift` modifiers, after shortcuts were handled.

For gameplay input, this and
`_unhandled_input<class_Node_private_method__unhandled_input>` are
usually a better fit than `_input<class_Node_private_method__input>`, as
GUI events should be handled first. This method also performs better
than `_unhandled_input<class_Node_private_method__unhandled_input>`,
since unrelated events such as
`InputEventMouseMotion<class_InputEventMouseMotion>` are automatically
filtered. For shortcuts, consider using
`_shortcut_input<class_Node_private_method__shortcut_input>` instead.

\*\*Note:\*\* This method is only called if the node is present in the
scene tree (i.e. if it's not an orphan).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_child**(node: `Node<class_Node>`,
force\_readable\_name: `bool<class_bool>` = false, internal:
`InternalMode<enum_Node_InternalMode>` = 0)
`🔗<class_Node_method_add_child>`

Adds a child `node`. Nodes can have any number of children, but every
child must have a unique name. Child nodes are automatically deleted
when the parent node is deleted, so an entire scene can be removed by
deleting its topmost node.

If `force_readable_name` is `true`, improves the readability of the
added `node`. If not named, the `node` is renamed to its type, and if it
shares `name<class_Node_property_name>` with a sibling, a number is
suffixed more appropriately. This operation is very slow. As such, it is
recommended leaving this to `false`, which assigns a dummy name
featuring `@` in both situations.

If `internal` is different than
`INTERNAL_MODE_DISABLED<class_Node_constant_INTERNAL_MODE_DISABLED>`,
the child will be added as internal node. These nodes are ignored by
methods like `get_children<class_Node_method_get_children>`, unless
their parameter `include_internal` is `true`. The intended usage is to
hide the internal nodes from the user, so the user won't accidentally
delete or modify them. Used by some GUI nodes, e.g.
`ColorPicker<class_ColorPicker>`. See
`InternalMode<enum_Node_InternalMode>` for available modes.

\*\*Note:\*\* If `node` already has a parent, this method will fail. Use
`remove_child<class_Node_method_remove_child>` first to remove `node`
from its current parent. For example:

gdscript

var child\_node = get\_child(0) if child\_node.get\_parent():
child\_node.get\_parent().remove\_child(child\_node)
add\_child(child\_node)

csharp

Node childNode = GetChild(0); if (childNode.GetParent() != null) {
childNode.GetParent().RemoveChild(childNode); } AddChild(childNode);

If you need the child node to be added below a specific node in the list
of children, use `add_sibling<class_Node_method_add_sibling>` instead of
this method.

\*\*Note:\*\* If you want a child to be persisted to a
`PackedScene<class_PackedScene>`, you must set
`owner<class_Node_property_owner>` in addition to calling
`add_child<class_Node_method_add_child>`. This is typically relevant for
`tool scripts <../tutorials/plugins/running_code_in_the_editor>` and
`editor plugins <../tutorials/plugins/editor/index>`. If
`add_child<class_Node_method_add_child>` is called without setting
`owner<class_Node_property_owner>`, the newly added **Node** will not be
visible in the scene tree, though it will be visible in the 2D/3D view.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_sibling**(sibling: `Node<class_Node>`,
force\_readable\_name: `bool<class_bool>` = false)
`🔗<class_Node_method_add_sibling>`

Adds a `sibling` node to this node's parent, and moves the added sibling
right below this node.

If `force_readable_name` is `true`, improves the readability of the
added `sibling`. If not named, the `sibling` is renamed to its type, and
if it shares `name<class_Node_property_name>` with a sibling, a number
is suffixed more appropriately. This operation is very slow. As such, it
is recommended leaving this to `false`, which assigns a dummy name
featuring `@` in both situations.

Use `add_child<class_Node_method_add_child>` instead of this method if
you don't need the child node to be added below a specific node in the
list of children.

\*\*Note:\*\* If this node is internal, the added sibling will be
internal too (see `add_child<class_Node_method_add_child>`'s `internal`
parameter).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_to\_group**(group:
`StringName<class_StringName>`, persistent: `bool<class_bool>` = false)
`🔗<class_Node_method_add_to_group>`

Adds the node to the `group`. Groups can be helpful to organize a subset
of nodes, for example `"enemies"` or `"collectables"`. See notes in the
description, and the group methods in `SceneTree<class_SceneTree>`.

If `persistent` is `true`, the group will be stored when saved inside a
`PackedScene<class_PackedScene>`. All groups created and displayed in
the Node dock are persistent.

\*\*Note:\*\* To improve performance, the order of group names is *not*
guaranteed and may vary between project runs. Therefore, do not rely on
the group order.

\*\*Note:\*\* `SceneTree<class_SceneTree>`'s group methods will *not*
work on this node if not inside the tree (see
`is_inside_tree<class_Node_method_is_inside_tree>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **atr**(message: `String<class_String>`, context:
`StringName<class_StringName>` = "")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_atr>`

Translates a `message`, using the translation catalogs configured in the
Project Settings. Further `context` can be specified to help with the
translation. Note that most `Control<class_Control>` nodes automatically
translate their strings, so this method is mostly useful for formatted
strings or custom drawn text.

This method works the same as `Object.tr<class_Object_method_tr>`, with
the addition of respecting the
`auto_translate_mode<class_Node_property_auto_translate_mode>` state.

If
`Object.can_translate_messages<class_Object_method_can_translate_messages>`
is `false`, or no translation is available, this method returns the
`message` without changes. See
`Object.set_message_translation<class_Object_method_set_message_translation>`.

For detailed examples, see
`Internationalizing games <../tutorials/i18n/internationalizing_games>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **atr\_n**(message: `String<class_String>`,
plural\_message: `StringName<class_StringName>`, n: `int<class_int>`,
context: `StringName<class_StringName>` = "")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_atr_n>`

Translates a `message` or `plural_message`, using the translation
catalogs configured in the Project Settings. Further `context` can be
specified to help with the translation.

This method works the same as `Object.tr_n<class_Object_method_tr_n>`,
with the addition of respecting the
`auto_translate_mode<class_Node_property_auto_translate_mode>` state.

If
`Object.can_translate_messages<class_Object_method_can_translate_messages>`
is `false`, or no translation is available, this method returns
`message` or `plural_message`, without changes. See
`Object.set_message_translation<class_Object_method_set_message_translation>`.

The `n` is the number, or amount, of the message's subject. It is used
by the translation system to fetch the correct plural form for the
current language.

For detailed examples, see
`Localization using gettext <../tutorials/i18n/localization_using_gettext>`.

\*\*Note:\*\* Negative and `float<class_float>` numbers may not properly
apply to some countable subjects. It's recommended to handle these cases
with `atr<class_Node_method_atr>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **call\_deferred\_thread\_group**(method:
`StringName<class_StringName>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_Node_method_call_deferred_thread_group>`

This function is similar to
`Object.call_deferred<class_Object_method_call_deferred>` except that
the call will take place when the node thread group is processed. If the
node thread group processes in sub-threads, then the call will be done
on that thread, right before
`NOTIFICATION_PROCESS<class_Node_constant_NOTIFICATION_PROCESS>` or
`NOTIFICATION_PHYSICS_PROCESS<class_Node_constant_NOTIFICATION_PHYSICS_PROCESS>`,
the `_process<class_Node_private_method__process>` or
`_physics_process<class_Node_private_method__physics_process>` or their
internal versions are called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **call\_thread\_safe**(method:
`StringName<class_StringName>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_Node_method_call_thread_safe>`

This function ensures that the calling of this function will succeed, no
matter whether it's being done from a thread or not. If called from a
thread that is not allowed to call the function, the call will become
deferred. Otherwise, the call will go through directly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **can\_process**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_can_process>`

Returns `true` if the node can receive processing notifications and
input callbacks
(`NOTIFICATION_PROCESS<class_Node_constant_NOTIFICATION_PROCESS>`,
`_input<class_Node_private_method__input>`, etc.) from the
`SceneTree<class_SceneTree>` and `Viewport<class_Viewport>`. The
returned value depends on
`process_mode<class_Node_property_process_mode>`:

-   If set to
    `PROCESS_MODE_PAUSABLE<class_Node_constant_PROCESS_MODE_PAUSABLE>`,
    returns `true` when the game is processing, i.e.
    `SceneTree.paused<class_SceneTree_property_paused>` is `false`;
-   If set to
    `PROCESS_MODE_WHEN_PAUSED<class_Node_constant_PROCESS_MODE_WHEN_PAUSED>`,
    returns `true` when the game is paused, i.e.
    `SceneTree.paused<class_SceneTree_property_paused>` is `true`;
-   If set to
    `PROCESS_MODE_ALWAYS<class_Node_constant_PROCESS_MODE_ALWAYS>`,
    always returns `true`;
-   If set to
    `PROCESS_MODE_DISABLED<class_Node_constant_PROCESS_MODE_DISABLED>`,
    always returns `false`;
-   If set to
    `PROCESS_MODE_INHERIT<class_Node_constant_PROCESS_MODE_INHERIT>`,
    use the parent node's
    `process_mode<class_Node_property_process_mode>` to determine the
    result.

If the node is not inside the tree, returns `false` no matter the value
of `process_mode<class_Node_property_process_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tween<class_Tween>` **create\_tween**()
`🔗<class_Node_method_create_tween>`

Creates a new `Tween<class_Tween>` and binds it to this node.

This is the equivalent of doing:

gdscript

get\_tree().create\_tween().bind\_node(self)

csharp

GetTree().CreateTween().BindNode(this);

The Tween will start automatically on the next process frame or physics
frame (depending on `TweenProcessMode<enum_Tween_TweenProcessMode>`).
See `Tween.bind_node<class_Tween_method_bind_node>` for more info on
Tweens bound to nodes.

\*\*Note:\*\* The method can still be used when the node is not inside
`SceneTree<class_SceneTree>`. It can fail in an unlikely case of using a
custom `MainLoop<class_MainLoop>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **duplicate**(flags: `int<class_int>` = 15)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_duplicate>`

Duplicates the node, returning a new node with all of its properties,
signals, groups, and children copied from the original. The behavior can
be tweaked through the `flags` (see
`DuplicateFlags<enum_Node_DuplicateFlags>`).

\*\*Note:\*\* For nodes with a `Script<class_Script>` attached, if
`Object._init<class_Object_private_method__init>` has been defined with
required parameters, the duplicated node will not have a
`Script<class_Script>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **find\_child**(pattern: `String<class_String>`,
recursive: `bool<class_bool>` = true, owned: `bool<class_bool>` = true)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_find_child>`

Finds the first descendant of this node whose
`name<class_Node_property_name>` matches `pattern`, returning `null` if
no match is found. The matching is done against node names, *not* their
paths, through `String.match<class_String_method_match>`. As such, it is
case-sensitive, `"*"` matches zero or more characters, and `"?"` matches
any single character.

If `recursive` is `false`, only this node's direct children are checked.
Nodes are checked in tree order, so this node's first direct child is
checked first, then its own direct children, etc., before moving to the
second direct child, and so on. Internal children are also included in
the search (see `internal` parameter in
`add_child<class_Node_method_add_child>`).

If `owned` is `true`, only descendants with a valid
`owner<class_Node_property_owner>` node are checked.

\*\*Note:\*\* This method can be very slow. Consider storing a reference
to the found node in a variable. Alternatively, use
`get_node<class_Node_method_get_node>` with unique names (see
`unique_name_in_owner<class_Node_property_unique_name_in_owner>`).

\*\*Note:\*\* To find all descendant nodes matching a pattern or a class
type, see `find_children<class_Node_method_find_children>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Node<class_Node>`\] **find\_children**(pattern:
`String<class_String>`, type: `String<class_String>` = "", recursive:
`bool<class_bool>` = true, owned: `bool<class_bool>` = true)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_find_children>`

Finds all descendants of this node whose names match `pattern`,
returning an empty `Array<class_Array>` if no match is found. The
matching is done against node names, *not* their paths, through
`String.match<class_String_method_match>`. As such, it is
case-sensitive, `"*"` matches zero or more characters, and `"?"` matches
any single character.

If `type` is not empty, only ancestors inheriting from `type` are
included (see `Object.is_class<class_Object_method_is_class>`).

If `recursive` is `false`, only this node's direct children are checked.
Nodes are checked in tree order, so this node's first direct child is
checked first, then its own direct children, etc., before moving to the
second direct child, and so on. Internal children are also included in
the search (see `internal` parameter in
`add_child<class_Node_method_add_child>`).

If `owned` is `true`, only descendants with a valid
`owner<class_Node_property_owner>` node are checked.

\*\*Note:\*\* This method can be very slow. Consider storing references
to the found nodes in a variable.

\*\*Note:\*\* To find a single descendant node matching a pattern, see
`find_child<class_Node_method_find_child>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **find\_parent**(pattern: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_find_parent>`

Finds the first ancestor of this node whose
`name<class_Node_property_name>` matches `pattern`, returning `null` if
no match is found. The matching is done through
`String.match<class_String_method_match>`. As such, it is
case-sensitive, `"*"` matches zero or more characters, and `"?"` matches
any single character. See also
`find_child<class_Node_method_find_child>` and
`find_children<class_Node_method_find_children>`.

\*\*Note:\*\* As this method walks upwards in the scene tree, it can be
slow in large, deeply nested nodes. Consider storing a reference to the
found node in a variable. Alternatively, use
`get_node<class_Node_method_get_node>` with unique names (see
`unique_name_in_owner<class_Node_property_unique_name_in_owner>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **get\_child**(idx: `int<class_int>`,
include\_internal: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_child>`

Fetches a child node by its index. Each child node has an index relative
its siblings (see `get_index<class_Node_method_get_index>`). The first
child is at index 0. Negative values can also be used to start from the
end of the list. This method can be used in combination with
`get_child_count<class_Node_method_get_child_count>` to iterate over
this node's children. If no child exists at the given index, this method
returns `null` and an error is generated.

If `include_internal` is `false`, internal children are ignored (see
`add_child<class_Node_method_add_child>`'s `internal` parameter).

    # Assuming the following are children of this node, in order:
    # First, Middle, Last.

    var a = get_child(0).name  # a is "First"
    var b = get_child(1).name  # b is "Middle"
    var b = get_child(2).name  # b is "Last"
    var c = get_child(-1).name # c is "Last"

\*\*Note:\*\* To fetch a node by `NodePath<class_NodePath>`, use
`get_node<class_Node_method_get_node>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_child\_count**(include\_internal:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_child_count>`

Returns the number of children of this node.

If `include_internal` is `false`, internal children are not counted (see
`add_child<class_Node_method_add_child>`'s `internal` parameter).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Node<class_Node>`\]
**get\_children**(include\_internal: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_children>`

Returns all children of this node inside an `Array<class_Array>`.

If `include_internal` is `false`, excludes internal children from the
returned array (see `add_child<class_Node_method_add_child>`'s
`internal` parameter).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`StringName<class_StringName>`\] **get\_groups**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_groups>`

Returns an `Array<class_Array>` of group names that the node has been
added to.

\*\*Note:\*\* To improve performance, the order of group names is *not*
guaranteed and may vary between project runs. Therefore, do not rely on
the group order.

\*\*Note:\*\* This method may also return some group names starting with
an underscore (`_`). These are internally used by the engine. To avoid
conflicts, do not use custom groups starting with underscores. To
exclude internal groups, see the following code snippet:

gdscript

\# Stores the node's non-internal groups only (as an array of
StringNames). var non\_internal\_groups = \[\] for group in
get\_groups(): if not str(group).begins\_with("\_"):
non\_internal\_groups.push\_back(group)

csharp

// Stores the node's non-internal groups only (as a List of
StringNames). List&lt;string&gt; nonInternalGroups = new
List&lt;string&gt;(); foreach (string group in GetGroups()) { if
(!group.BeginsWith("\_")) nonInternalGroups.Add(group); }

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_index**(include\_internal: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_index>`

Returns this node's order among its siblings. The first node's index is
`0`. See also `get_child<class_Node_method_get_child>`.

If `include_internal` is `false`, returns the index ignoring internal
children. The first, non-internal child will have an index of `0` (see
`add_child<class_Node_method_add_child>`'s `internal` parameter).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Window<class_Window>` **get\_last\_exclusive\_window**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_last_exclusive_window>`

Returns the `Window<class_Window>` that contains this node, or the last
exclusive child in a chain of windows starting with the one that
contains this node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_multiplayer\_authority**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_multiplayer_authority>`

Returns the peer ID of the multiplayer authority for this node. See
`set_multiplayer_authority<class_Node_method_set_multiplayer_authority>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **get\_node**(path: `NodePath<class_NodePath>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_node>`

Fetches a node. The `NodePath<class_NodePath>` can either be a relative
path (from this node), or an absolute path (from the
`SceneTree.root<class_SceneTree_property_root>`) to a node. If `path`
does not point to a valid node, generates an error and returns `null`.
Attempts to access methods on the return value will result in an
*"Attempt to call &lt;method&gt; on a null instance."* error.

\*\*Note:\*\* Fetching by absolute path only works when the node is
inside the scene tree (see
`is_inside_tree<class_Node_method_is_inside_tree>`).

\*\*Example:\*\* Assume this method is called from the Character node,
inside the following tree:

    ┖╴root
       ┠╴Character (you are here!)
       ┃  ┠╴Sword
       ┃  ┖╴Backpack
       ┃     ┖╴Dagger
       ┠╴MyGame
       ┖╴Swamp
          ┠╴Alligator
          ┠╴Mosquito
          ┖╴Goblin

The following calls will return a valid node:

gdscript

get\_node("Sword") get\_node("Backpack/Dagger")
get\_node("../Swamp/Alligator") get\_node("/root/MyGame")

csharp

GetNode("Sword"); GetNode("Backpack/Dagger");
GetNode("../Swamp/Alligator"); GetNode("/root/MyGame");

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_node\_and\_resource**(path:
`NodePath<class_NodePath>`)
`🔗<class_Node_method_get_node_and_resource>`

Fetches a node and its most nested resource as specified by the
`NodePath<class_NodePath>`'s subname. Returns an `Array<class_Array>` of
size `3` where:

-   Element `0` is the **Node**, or `null` if not found;
-   Element `1` is the subname's last nested `Resource<class_Resource>`,
    or `null` if not found;
-   Element `2` is the remaining `NodePath<class_NodePath>`, referring
    to an existing, non-`Resource<class_Resource>` property (see
    `Object.get_indexed<class_Object_method_get_indexed>`).

\*\*Example:\*\* Assume that the child's
`Sprite2D.texture<class_Sprite2D_property_texture>` has been assigned a
`AtlasTexture<class_AtlasTexture>`:

gdscript

var a = get\_node\_and\_resource("Area2D/Sprite2D") print(a\[0\].name)
\# Prints Sprite2D print(a\[1\]) \# Prints &lt;null&gt; print(a\[2\]) \#
Prints ^""

var b = get\_node\_and\_resource("Area2D/Sprite2D:texture:atlas")
print(b\[0\].name) \# Prints Sprite2D print(b\[1\].get\_class()) \#
Prints AtlasTexture print(b\[2\]) \# Prints ^""

var c = get\_node\_and\_resource("Area2D/Sprite2D:texture:atlas:region")
print(c\[0\].name) \# Prints Sprite2D print(c\[1\].get\_class()) \#
Prints AtlasTexture print(c\[2\]) \# Prints ^":region"

csharp

var a = GetNodeAndResource(NodePath("Area2D/Sprite2D"));
GD.Print(a\[0\].Name); // Prints Sprite2D GD.Print(a\[1\]); // Prints
&lt;null&gt; GD.Print(a\[2\]); // Prints ^"

var b = GetNodeAndResource(NodePath("Area2D/Sprite2D:texture:atlas"));
GD.Print(b\[0\].name); // Prints Sprite2D GD.Print(b\[1\].get\_class());
// Prints AtlasTexture GD.Print(b\[2\]); // Prints ^""

var c =
GetNodeAndResource(NodePath("Area2D/Sprite2D:texture:atlas:region"));
GD.Print(c\[0\].name); // Prints Sprite2D GD.Print(c\[1\].get\_class());
// Prints AtlasTexture GD.Print(c\[2\]); // Prints ^":region"

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **get\_node\_or\_null**(path:
`NodePath<class_NodePath>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_node_or_null>`

Fetches a node by `NodePath<class_NodePath>`. Similar to
`get_node<class_Node_method_get_node>`, but does not generate an error
if `path` does not point to a valid node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **get\_parent**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_parent>`

Returns this node's parent node, or `null` if the node doesn't have a
parent.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **get\_path**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_path>`

Returns the node's absolute path, relative to the
`SceneTree.root<class_SceneTree_property_root>`. If the node is not
inside the scene tree, this method fails and returns an empty
`NodePath<class_NodePath>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **get\_path\_to**(node: `Node<class_Node>`,
use\_unique\_path: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_path_to>`

Returns the relative `NodePath<class_NodePath>` from this node to the
specified `node`. Both nodes must be in the same
`SceneTree<class_SceneTree>` or scene hierarchy, otherwise this method
fails and returns an empty `NodePath<class_NodePath>`.

If `use_unique_path` is `true`, returns the shortest path accounting for
this node's unique name (see
`unique_name_in_owner<class_Node_property_unique_name_in_owner>`).

\*\*Note:\*\* If you get a relative path which starts from a unique
node, the path may be longer than a normal relative path, due to the
addition of the unique node's name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_physics\_process\_delta\_time**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_physics_process_delta_time>`

Returns the time elapsed (in seconds) since the last physics callback.
This value is identical to
`_physics_process<class_Node_private_method__physics_process>`'s `delta`
parameter, and is often consistent at run-time, unless
`Engine.physics_ticks_per_second<class_Engine_property_physics_ticks_per_second>`
is changed. See also
`NOTIFICATION_PHYSICS_PROCESS<class_Node_constant_NOTIFICATION_PHYSICS_PROCESS>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_process\_delta\_time**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_process_delta_time>`

Returns the time elapsed (in seconds) since the last process callback.
This value is identical to
`_process<class_Node_private_method__process>`'s `delta` parameter, and
may vary from frame to frame. See also
`NOTIFICATION_PROCESS<class_Node_constant_NOTIFICATION_PROCESS>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_rpc\_config**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_rpc_config>`

Returns a `Dictionary<class_Dictionary>` mapping method names to their
RPC configuration defined for this node using
`rpc_config<class_Node_method_rpc_config>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_scene\_instance\_load\_placeholder**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_scene_instance_load_placeholder>`

Returns `true` if this node is an instance load placeholder. See
`InstancePlaceholder<class_InstancePlaceholder>` and
`set_scene_instance_load_placeholder<class_Node_method_set_scene_instance_load_placeholder>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`SceneTree<class_SceneTree>` **get\_tree**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_tree>`

Returns the `SceneTree<class_SceneTree>` that contains this node. If
this node is not inside the tree, generates an error and returns `null`.
See also `is_inside_tree<class_Node_method_is_inside_tree>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_tree\_string**()
`🔗<class_Node_method_get_tree_string>`

Returns the tree as a `String<class_String>`. Used mainly for debugging
purposes. This version displays the path relative to the current node,
and is good for copy/pasting into the
`get_node<class_Node_method_get_node>` function. It also can be used in
game UI/UX.

May print, for example:

    TheGame
    TheGame/Menu
    TheGame/Menu/Label
    TheGame/Menu/Camera2D
    TheGame/SplashScreen
    TheGame/SplashScreen/Camera2D

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_tree\_string\_pretty**()
`🔗<class_Node_method_get_tree_string_pretty>`

Similar to `get_tree_string<class_Node_method_get_tree_string>`, this
returns the tree as a `String<class_String>`. This version displays a
more graphical representation similar to what is displayed in the Scene
Dock. It is useful for inspecting larger trees.

May print, for example:

    ┖╴TheGame
       ┠╴Menu
       ┃  ┠╴Label
       ┃  ┖╴Camera2D
       ┖╴SplashScreen
          ┖╴Camera2D

classref-item-separator

------------------------------------------------------------------------

classref-method

`Viewport<class_Viewport>` **get\_viewport**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_viewport>`

Returns the node's closest `Viewport<class_Viewport>` ancestor, if the
node is inside the tree. Otherwise, returns `null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Window<class_Window>` **get\_window**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_get_window>`

Returns the `Window<class_Window>` that contains this node. If the node
is in the main window, this is equivalent to getting the root node
(`get_tree().get_root()`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_node**(path: `NodePath<class_NodePath>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_has_node>`

Returns `true` if the `path` points to a valid node. See also
`get_node<class_Node_method_get_node>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_node\_and\_resource**(path:
`NodePath<class_NodePath>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_has_node_and_resource>`

Returns `true` if `path` points to a valid node and its subnames point
to a valid `Resource<class_Resource>`, e.g.
`Area2D/CollisionShape2D:shape`. Properties that are not
`Resource<class_Resource>` types (such as nodes or other
`Variant<class_Variant>` types) are not considered. See also
`get_node_and_resource<class_Node_method_get_node_and_resource>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_ancestor\_of**(node: `Node<class_Node>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_ancestor_of>`

Returns `true` if the given `node` is a direct or indirect child of this
node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_displayed\_folded**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_displayed_folded>`

Returns `true` if the node is folded (collapsed) in the Scene dock. This
method is intended to be used in editor plugins and tools. See also
`set_display_folded<class_Node_method_set_display_folded>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_editable\_instance**(node: `Node<class_Node>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_editable_instance>`

Returns `true` if `node` has editable children enabled relative to this
node. This method is intended to be used in editor plugins and tools.
See also
`set_editable_instance<class_Node_method_set_editable_instance>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_greater\_than**(node: `Node<class_Node>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_greater_than>`

Returns `true` if the given `node` occurs later in the scene hierarchy
than this node. A node occurring later is usually processed last.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_in\_group**(group:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_in_group>`

Returns `true` if this node has been added to the given `group`. See
`add_to_group<class_Node_method_add_to_group>` and
`remove_from_group<class_Node_method_remove_from_group>`. See also notes
in the description, and the `SceneTree<class_SceneTree>`'s group
methods.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_inside\_tree**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_inside_tree>`

Returns `true` if this node is currently inside a
`SceneTree<class_SceneTree>`. See also
`get_tree<class_Node_method_get_tree>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_multiplayer\_authority**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_multiplayer_authority>`

Returns `true` if the local system is the multiplayer authority of this
node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_node\_ready**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_node_ready>`

Returns `true` if the node is ready, i.e. it's inside scene tree and all
its children are initialized.

`request_ready<class_Node_method_request_ready>` resets it back to
`false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_part\_of\_edited\_scene**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_part_of_edited_scene>`

Returns `true` if the node is part of the scene currently opened in the
editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_physics\_interpolated**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_physics_interpolated>`

Returns `true` if physics interpolation is enabled for this node (see
`physics_interpolation_mode<class_Node_property_physics_interpolation_mode>`).

\*\*Note:\*\* Interpolation will only be active if both the flag is set
**and** physics interpolation is enabled within the
`SceneTree<class_SceneTree>`. This can be tested using
`is_physics_interpolated_and_enabled<class_Node_method_is_physics_interpolated_and_enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_physics\_interpolated\_and\_enabled**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_physics_interpolated_and_enabled>`

Returns `true` if physics interpolation is enabled (see
`physics_interpolation_mode<class_Node_property_physics_interpolation_mode>`)
**and** enabled in the `SceneTree<class_SceneTree>`.

This is a convenience version of
`is_physics_interpolated<class_Node_method_is_physics_interpolated>`
that also checks whether physics interpolation is enabled globally.

See
`SceneTree.physics_interpolation<class_SceneTree_property_physics_interpolation>`
and
`ProjectSettings.physics/common/physics_interpolation<class_ProjectSettings_property_physics/common/physics_interpolation>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_physics\_processing**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_physics_processing>`

Returns `true` if physics processing is enabled (see
`set_physics_process<class_Node_method_set_physics_process>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_physics\_processing\_internal**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_physics_processing_internal>`

Returns `true` if internal physics processing is enabled (see
`set_physics_process_internal<class_Node_method_set_physics_process_internal>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_processing**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_processing>`

Returns `true` if processing is enabled (see
`set_process<class_Node_method_set_process>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_processing\_input**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_processing_input>`

Returns `true` if the node is processing input (see
`set_process_input<class_Node_method_set_process_input>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_processing\_internal**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_processing_internal>`

Returns `true` if internal processing is enabled (see
`set_process_internal<class_Node_method_set_process_internal>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_processing\_shortcut\_input**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_processing_shortcut_input>`

Returns `true` if the node is processing shortcuts (see
`set_process_shortcut_input<class_Node_method_set_process_shortcut_input>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_processing\_unhandled\_input**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_processing_unhandled_input>`

Returns `true` if the node is processing unhandled input (see
`set_process_unhandled_input<class_Node_method_set_process_unhandled_input>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_processing\_unhandled\_key\_input**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node_method_is_processing_unhandled_key_input>`

Returns `true` if the node is processing unhandled key input (see
`set_process_unhandled_key_input<class_Node_method_set_process_unhandled_key_input>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_child**(child\_node:
`Node<class_Node>`, to\_index: `int<class_int>`)
`🔗<class_Node_method_move_child>`

Moves `child_node` to the given index. A node's index is the order among
its siblings. If `to_index` is negative, the index is counted from the
end of the list. See also `get_child<class_Node_method_get_child>` and
`get_index<class_Node_method_get_index>`.

\*\*Note:\*\* The processing order of several engine callbacks
(`_ready<class_Node_private_method__ready>`,
`_process<class_Node_private_method__process>`, etc.) and notifications
sent through
`propagate_notification<class_Node_method_propagate_notification>` is
affected by tree order. `CanvasItem<class_CanvasItem>` nodes are also
rendered in tree order. See also
`process_priority<class_Node_property_process_priority>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **notify\_deferred\_thread\_group**(what:
`int<class_int>`) `🔗<class_Node_method_notify_deferred_thread_group>`

Similar to
`call_deferred_thread_group<class_Node_method_call_deferred_thread_group>`,
but for notifications.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **notify\_thread\_safe**(what:
`int<class_int>`) `🔗<class_Node_method_notify_thread_safe>`

Similar to `call_thread_safe<class_Node_method_call_thread_safe>`, but
for notifications.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **print\_orphan\_nodes**()
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_Node_method_print_orphan_nodes>`

Prints all orphan nodes (nodes outside the
`SceneTree<class_SceneTree>`). Useful for debugging.

\*\*Note:\*\* This method only works in debug builds. Does nothing in a
project exported in release mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **print\_tree**()
`🔗<class_Node_method_print_tree>`

Prints the node and its children to the console, recursively. The node
does not have to be inside the tree. This method outputs
`NodePath<class_NodePath>`s relative to this node, and is good for
copy/pasting into `get_node<class_Node_method_get_node>`. See also
`print_tree_pretty<class_Node_method_print_tree_pretty>`.

May print, for example:

    .
    Menu
    Menu/Label
    Menu/Camera2D
    SplashScreen
    SplashScreen/Camera2D

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **print\_tree\_pretty**()
`🔗<class_Node_method_print_tree_pretty>`

Prints the node and its children to the console, recursively. The node
does not have to be inside the tree. Similar to
`print_tree<class_Node_method_print_tree>`, but the graphical
representation looks like what is displayed in the editor's Scene dock.
It is useful for inspecting larger trees.

May print, for example:

    ┖╴TheGame
       ┠╴Menu
       ┃  ┠╴Label
       ┃  ┖╴Camera2D
       ┖╴SplashScreen
          ┖╴Camera2D

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **propagate\_call**(method:
`StringName<class_StringName>`, args: `Array<class_Array>` = \[\],
parent\_first: `bool<class_bool>` = false)
`🔗<class_Node_method_propagate_call>`

Calls the given `method` name, passing `args` as arguments, on this node
and all of its children, recursively.

If `parent_first` is `true`, the method is called on this node first,
then on all of its children. If `false`, the children's methods are
called first.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **propagate\_notification**(what:
`int<class_int>`) `🔗<class_Node_method_propagate_notification>`

Calls `Object.notification<class_Object_method_notification>` with
`what` on this node and all of its children, recursively.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **queue\_free**()
`🔗<class_Node_method_queue_free>`

Queues this node to be deleted at the end of the current frame. When
deleted, all of its children are deleted as well, and all references to
the node and its children become invalid.

Unlike with `Object.free<class_Object_method_free>`, the node is not
deleted instantly, and it can still be accessed before deletion. It is
also safe to call `queue_free<class_Node_method_queue_free>` multiple
times. Use
`Object.is_queued_for_deletion<class_Object_method_is_queued_for_deletion>`
to check if the node will be deleted at the end of the frame.

\*\*Note:\*\* The node will only be freed after all other deferred calls
are finished. Using this method is not always the same as calling
`Object.free<class_Object_method_free>` through
`Object.call_deferred<class_Object_method_call_deferred>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_child**(node: `Node<class_Node>`)
`🔗<class_Node_method_remove_child>`

Removes a child `node`. The `node`, along with its children, are **not**
deleted. To delete a node, see
`queue_free<class_Node_method_queue_free>`.

\*\*Note:\*\* When this node is inside the tree, this method sets the
`owner<class_Node_property_owner>` of the removed `node` (or its
descendants) to `null`, if their `owner<class_Node_property_owner>` is
no longer an ancestor (see
`is_ancestor_of<class_Node_method_is_ancestor_of>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_from\_group**(group:
`StringName<class_StringName>`)
`🔗<class_Node_method_remove_from_group>`

Removes the node from the given `group`. Does nothing if the node is not
in the `group`. See also notes in the description, and the
`SceneTree<class_SceneTree>`'s group methods.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reparent**(new\_parent: `Node<class_Node>`,
keep\_global\_transform: `bool<class_bool>` = true)
`🔗<class_Node_method_reparent>`

Changes the parent of this **Node** to the `new_parent`. The node needs
to already have a parent. The node's `owner<class_Node_property_owner>`
is preserved if its owner is still reachable from the new location
(i.e., the node is still a descendant of the new parent after the
operation).

If `keep_global_transform` is `true`, the node's global transform will
be preserved if supported. `Node2D<class_Node2D>`,
`Node3D<class_Node3D>` and `Control<class_Control>` support this
argument (but `Control<class_Control>` keeps only position).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **replace\_by**(node: `Node<class_Node>`,
keep\_groups: `bool<class_bool>` = false)
`🔗<class_Node_method_replace_by>`

Replaces this node by the given `node`. All children of this node are
moved to `node`.

If `keep_groups` is `true`, the `node` is added to the same groups that
the replaced node is in (see
`add_to_group<class_Node_method_add_to_group>`).

\*\*Warning:\*\* The replaced node is removed from the tree, but it is
**not** deleted. To prevent memory leaks, store a reference to the node
in a variable, or use `Object.free<class_Object_method_free>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **request\_ready**()
`🔗<class_Node_method_request_ready>`

Requests `_ready<class_Node_private_method__ready>` to be called again
the next time the node enters the tree. Does **not** immediately call
`_ready<class_Node_private_method__ready>`.

\*\*Note:\*\* This method only affects the current node. If the node's
children also need to request ready, this method needs to be called for
each one of them. When the node and its children enter the tree again,
the order of `_ready<class_Node_private_method__ready>` callbacks will
be the same as normal.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reset\_physics\_interpolation**()
`🔗<class_Node_method_reset_physics_interpolation>`

When physics interpolation is active, moving a node to a radically
different transform (such as placement within a level) can result in a
visible glitch as the object is rendered moving from the old to new
position over the physics tick.

That glitch can be prevented by calling this method, which temporarily
disables interpolation until the physics tick is complete.

The notification
`NOTIFICATION_RESET_PHYSICS_INTERPOLATION<class_Node_constant_NOTIFICATION_RESET_PHYSICS_INTERPOLATION>`
will be received by the node and all children recursively.

\*\*Note:\*\* This function should be called **after** moving the node,
rather than before.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **rpc**(method:
`StringName<class_StringName>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_Node_method_rpc>`

Sends a remote procedure call request for the given `method` to peers on
the network (and locally), sending additional arguments to the method
called by the RPC. The call request will only be received by nodes with
the same `NodePath<class_NodePath>`, including the exact same
`name<class_Node_property_name>`. Behavior depends on the RPC
configuration for the given `method` (see
`rpc_config<class_Node_method_rpc_config>` and
`@GDScript.@rpc<class_@GDScript_annotation_@rpc>`). By default, methods
are not exposed to RPCs.

May return `@GlobalScope.OK<class_@GlobalScope_constant_OK>` if the call
is successful,
`@GlobalScope.ERR_INVALID_PARAMETER<class_@GlobalScope_constant_ERR_INVALID_PARAMETER>`
if the arguments passed in the `method` do not match,
`@GlobalScope.ERR_UNCONFIGURED<class_@GlobalScope_constant_ERR_UNCONFIGURED>`
if the node's `multiplayer<class_Node_property_multiplayer>` cannot be
fetched (such as when the node is not inside the tree),
`@GlobalScope.ERR_CONNECTION_ERROR<class_@GlobalScope_constant_ERR_CONNECTION_ERROR>`
if `multiplayer<class_Node_property_multiplayer>`'s connection is not
available.

\*\*Note:\*\* You can only safely use RPCs on clients after you received
the
`MultiplayerAPI.connected_to_server<class_MultiplayerAPI_signal_connected_to_server>`
signal from the `MultiplayerAPI<class_MultiplayerAPI>`. You also need to
keep track of the connection state, either by the
`MultiplayerAPI<class_MultiplayerAPI>` signals like
`MultiplayerAPI.server_disconnected<class_MultiplayerAPI_signal_server_disconnected>`
or by checking
(`get_multiplayer().peer.get_connection_status() == CONNECTION_CONNECTED`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **rpc\_config**(method:
`StringName<class_StringName>`, config: `Variant<class_Variant>`)
`🔗<class_Node_method_rpc_config>`

Changes the RPC configuration for the given `method`. `config` should
either be `null` to disable the feature (as by default), or a
`Dictionary<class_Dictionary>` containing the following entries:

-   `rpc_mode`: see `RPCMode<enum_MultiplayerAPI_RPCMode>`;
-   `transfer_mode`: see
    `TransferMode<enum_MultiplayerPeer_TransferMode>`;
-   `call_local`: if `true`, the method will also be called locally;
-   `channel`: an `int<class_int>` representing the channel to send the
    RPC on.

\*\*Note:\*\* In GDScript, this method corresponds to the
`@GDScript.@rpc<class_@GDScript_annotation_@rpc>` annotation, with
various parameters passed (`@rpc(any)`, `@rpc(authority)`...). See also
the
`high-level multiplayer <../tutorials/networking/high_level_multiplayer>`
tutorial.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **rpc\_id**(peer\_id: `int<class_int>`,
method: `StringName<class_StringName>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_Node_method_rpc_id>`

Sends a `rpc<class_Node_method_rpc>` to a specific peer identified by
`peer_id` (see
`MultiplayerPeer.set_target_peer<class_MultiplayerPeer_method_set_target_peer>`).

May return `@GlobalScope.OK<class_@GlobalScope_constant_OK>` if the call
is successful,
`@GlobalScope.ERR_INVALID_PARAMETER<class_@GlobalScope_constant_ERR_INVALID_PARAMETER>`
if the arguments passed in the `method` do not match,
`@GlobalScope.ERR_UNCONFIGURED<class_@GlobalScope_constant_ERR_UNCONFIGURED>`
if the node's `multiplayer<class_Node_property_multiplayer>` cannot be
fetched (such as when the node is not inside the tree),
`@GlobalScope.ERR_CONNECTION_ERROR<class_@GlobalScope_constant_ERR_CONNECTION_ERROR>`
if `multiplayer<class_Node_property_multiplayer>`'s connection is not
available.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_deferred\_thread\_group**(property:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`🔗<class_Node_method_set_deferred_thread_group>`

Similar to
`call_deferred_thread_group<class_Node_method_call_deferred_thread_group>`,
but for setting properties.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_display\_folded**(fold:
`bool<class_bool>`) `🔗<class_Node_method_set_display_folded>`

If set to `true`, the node appears folded in the Scene dock. As a
result, all of its children are hidden. This method is intended to be
used in editor plugins and tools, but it also works in release builds.
See also `is_displayed_folded<class_Node_method_is_displayed_folded>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_editable\_instance**(node:
`Node<class_Node>`, is\_editable: `bool<class_bool>`)
`🔗<class_Node_method_set_editable_instance>`

Set to `true` to allow all nodes owned by `node` to be available, and
editable, in the Scene dock, even if their
`owner<class_Node_property_owner>` is not the scene root. This method is
intended to be used in editor plugins and tools, but it also works in
release builds. See also
`is_editable_instance<class_Node_method_is_editable_instance>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_multiplayer\_authority**(id:
`int<class_int>`, recursive: `bool<class_bool>` = true)
`🔗<class_Node_method_set_multiplayer_authority>`

Sets the node's multiplayer authority to the peer with the given peer
`id`. The multiplayer authority is the peer that has authority over the
node on the network. Defaults to peer ID 1 (the server). Useful in
conjunction with `rpc_config<class_Node_method_rpc_config>` and the
`MultiplayerAPI<class_MultiplayerAPI>`.

If `recursive` is `true`, the given peer is recursively set as the
authority for all children of this node.

\*\*Warning:\*\* This does **not** automatically replicate the new
authority to other peers. It is the developer's responsibility to do so.
You may replicate the new authority's information using
`MultiplayerSpawner.spawn_function<class_MultiplayerSpawner_property_spawn_function>`,
an RPC, or a `MultiplayerSynchronizer<class_MultiplayerSynchronizer>`.
Furthermore, the parent's authority does **not** propagate to newly
added children.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_physics\_process**(enable:
`bool<class_bool>`) `🔗<class_Node_method_set_physics_process>`

If set to `true`, enables physics (fixed framerate) processing. When a
node is being processed, it will receive a
`NOTIFICATION_PHYSICS_PROCESS<class_Node_constant_NOTIFICATION_PHYSICS_PROCESS>`
at a fixed (usually 60 FPS, see
`Engine.physics_ticks_per_second<class_Engine_property_physics_ticks_per_second>`
to change) interval (and the
`_physics_process<class_Node_private_method__physics_process>` callback
will be called if it exists).

\*\*Note:\*\* If
`_physics_process<class_Node_private_method__physics_process>` is
overridden, this will be automatically enabled before
`_ready<class_Node_private_method__ready>` is called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_physics\_process\_internal**(enable:
`bool<class_bool>`) `🔗<class_Node_method_set_physics_process_internal>`

If set to `true`, enables internal physics for this node. Internal
physics processing happens in isolation from the normal
`_physics_process<class_Node_private_method__physics_process>` calls and
is used by some nodes internally to guarantee proper functioning even if
the node is paused or physics processing is disabled for scripting
(`set_physics_process<class_Node_method_set_physics_process>`).

\*\*Warning:\*\* Built-in nodes rely on internal processing for their
internal logic. Disabling it is unsafe and may lead to unexpected
behavior. Use this method if you know what you are doing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_process**(enable: `bool<class_bool>`)
`🔗<class_Node_method_set_process>`

If set to `true`, enables processing. When a node is being processed, it
will receive a
`NOTIFICATION_PROCESS<class_Node_constant_NOTIFICATION_PROCESS>` on
every drawn frame (and the
`_process<class_Node_private_method__process>` callback will be called
if it exists).

\*\*Note:\*\* If `_process<class_Node_private_method__process>` is
overridden, this will be automatically enabled before
`_ready<class_Node_private_method__ready>` is called.

\*\*Note:\*\* This method only affects the
`_process<class_Node_private_method__process>` callback, i.e. it has no
effect on other callbacks like
`_physics_process<class_Node_private_method__physics_process>`. If you
want to disable all processing for the node, set
`process_mode<class_Node_property_process_mode>` to
`PROCESS_MODE_DISABLED<class_Node_constant_PROCESS_MODE_DISABLED>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_process\_input**(enable:
`bool<class_bool>`) `🔗<class_Node_method_set_process_input>`

If set to `true`, enables input processing.

\*\*Note:\*\* If `_input<class_Node_private_method__input>` is
overridden, this will be automatically enabled before
`_ready<class_Node_private_method__ready>` is called. Input processing
is also already enabled for GUI controls, such as `Button<class_Button>`
and `TextEdit<class_TextEdit>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_process\_internal**(enable:
`bool<class_bool>`) `🔗<class_Node_method_set_process_internal>`

If set to `true`, enables internal processing for this node. Internal
processing happens in isolation from the normal
`_process<class_Node_private_method__process>` calls and is used by some
nodes internally to guarantee proper functioning even if the node is
paused or processing is disabled for scripting
(`set_process<class_Node_method_set_process>`).

\*\*Warning:\*\* Built-in nodes rely on internal processing for their
internal logic. Disabling it is unsafe and may lead to unexpected
behavior. Use this method if you know what you are doing.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_process\_shortcut\_input**(enable:
`bool<class_bool>`) `🔗<class_Node_method_set_process_shortcut_input>`

If set to `true`, enables shortcut processing for this node.

\*\*Note:\*\* If
`_shortcut_input<class_Node_private_method__shortcut_input>` is
overridden, this will be automatically enabled before
`_ready<class_Node_private_method__ready>` is called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_process\_unhandled\_input**(enable:
`bool<class_bool>`) `🔗<class_Node_method_set_process_unhandled_input>`

If set to `true`, enables unhandled input processing. It enables the
node to receive all input that was not previously handled (usually by a
`Control<class_Control>`).

\*\*Note:\*\* If
`_unhandled_input<class_Node_private_method__unhandled_input>` is
overridden, this will be automatically enabled before
`_ready<class_Node_private_method__ready>` is called. Unhandled input
processing is also already enabled for GUI controls, such as
`Button<class_Button>` and `TextEdit<class_TextEdit>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_process\_unhandled\_key\_input**(enable: `bool<class_bool>`)
`🔗<class_Node_method_set_process_unhandled_key_input>`

If set to `true`, enables unhandled key input processing.

\*\*Note:\*\* If
`_unhandled_key_input<class_Node_private_method__unhandled_key_input>`
is overridden, this will be automatically enabled before
`_ready<class_Node_private_method__ready>` is called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_scene\_instance\_load\_placeholder**(load\_placeholder:
`bool<class_bool>`)
`🔗<class_Node_method_set_scene_instance_load_placeholder>`

If set to `true`, the node becomes a
`InstancePlaceholder<class_InstancePlaceholder>` when packed and
instantiated from a `PackedScene<class_PackedScene>`. See also
`get_scene_instance_load_placeholder<class_Node_method_get_scene_instance_load_placeholder>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_thread\_safe**(property:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`🔗<class_Node_method_set_thread_safe>`

Similar to `call_thread_safe<class_Node_method_call_thread_safe>`, but
for setting properties.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_translation\_domain\_inherited**()
`🔗<class_Node_method_set_translation_domain_inherited>`

Makes this node inherit the translation domain from its parent node. If
this node has no parent, the main translation domain will be used.

This is the default behavior for all nodes. Calling
`Object.set_translation_domain<class_Object_method_set_translation_domain>`
disables this behavior.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update\_configuration\_warnings**()
`🔗<class_Node_method_update_configuration_warnings>`

Refreshes the warnings displayed for this node in the Scene dock. Use
`_get_configuration_warnings<class_Node_private_method__get_configuration_warnings>`
to customize the warning messages to display.
