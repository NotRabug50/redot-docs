github\_url  
hide

# SceneTree

**Inherits:** `MainLoop<class_MainLoop>` **&lt;** `Object<class_Object>`

Manages the game loop via a hierarchy of nodes.

classref-introduction-group

## Description

As one of the most important classes, the **SceneTree** manages the
hierarchy of nodes in a scene, as well as scenes themselves. Nodes can
be added, fetched and removed. The whole scene tree (and thus the
current scene) can be paused. Scenes can be loaded, switched and
reloaded.

You can also use the **SceneTree** to organize your nodes into
**groups**: every node can be added to as many groups as you want to
create, e.g. an "enemy" group. You can then iterate these groups or even
call methods and set properties on all the nodes belonging to any given
group.

\*\*SceneTree\*\* is the default `MainLoop<class_MainLoop>`
implementation used by the engine, and is thus in charge of the game
loop.

classref-introduction-group

## Tutorials

-   `SceneTree <../tutorials/scripting/scene_tree>`
-   `Multiple resolutions <../tutorials/rendering/multiple_resolutions>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**node\_added**(node: `Node<class_Node>`)
`🔗<class_SceneTree_signal_node_added>`

Emitted when the `node` enters this tree.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**node\_configuration\_warning\_changed**(node: `Node<class_Node>`)
`🔗<class_SceneTree_signal_node_configuration_warning_changed>`

Emitted when the `node`'s
`Node.update_configuration_warnings<class_Node_method_update_configuration_warnings>`
is called. Only emitted in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**node\_removed**(node: `Node<class_Node>`)
`🔗<class_SceneTree_signal_node_removed>`

Emitted when the `node` exits this tree.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**node\_renamed**(node: `Node<class_Node>`)
`🔗<class_SceneTree_signal_node_renamed>`

Emitted when the `node`'s `Node.name<class_Node_property_name>` is
changed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**physics\_frame**() `🔗<class_SceneTree_signal_physics_frame>`

Emitted immediately before
`Node._physics_process<class_Node_private_method__physics_process>` is
called on every node in this tree.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**process\_frame**() `🔗<class_SceneTree_signal_process_frame>`

Emitted immediately before
`Node._process<class_Node_private_method__process>` is called on every
node in this tree.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tree\_changed**() `🔗<class_SceneTree_signal_tree_changed>`

Emitted any time the tree's hierarchy changes (nodes being moved,
renamed, etc.).

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tree\_process\_mode\_changed**()
`🔗<class_SceneTree_signal_tree_process_mode_changed>`

Emitted when the `Node.process_mode<class_Node_property_process_mode>`
of any node inside the tree is changed. Only emitted in the editor, to
update the visibility of disabled nodes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **GroupCallFlags**: `🔗<enum_SceneTree_GroupCallFlags>`

classref-enumeration-constant

`GroupCallFlags<enum_SceneTree_GroupCallFlags>` **GROUP\_CALL\_DEFAULT**
= `0`

Call nodes within a group with no special behavior (default).

classref-enumeration-constant

`GroupCallFlags<enum_SceneTree_GroupCallFlags>` **GROUP\_CALL\_REVERSE**
= `1`

Call nodes within a group in reverse tree hierarchy order (all nested
children are called before their respective parent nodes).

classref-enumeration-constant

`GroupCallFlags<enum_SceneTree_GroupCallFlags>`
**GROUP\_CALL\_DEFERRED** = `2`

Call nodes within a group at the end of the current frame (can be either
process or physics frame), similar to
`Object.call_deferred<class_Object_method_call_deferred>`.

classref-enumeration-constant

`GroupCallFlags<enum_SceneTree_GroupCallFlags>` **GROUP\_CALL\_UNIQUE**
= `4`

Call nodes within a group only once, even if the call is executed many
times in the same frame. Must be combined with
`GROUP_CALL_DEFERRED<class_SceneTree_constant_GROUP_CALL_DEFERRED>` to
work.

\*\*Note:\*\* Different arguments are not taken into account. Therefore,
when the same call is executed with different arguments, only the first
call will be performed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **auto\_accept\_quit** = `true`
`🔗<class_SceneTree_property_auto_accept_quit>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_accept\_quit**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_auto\_accept\_quit**()

If `true`, the application automatically accepts quitting requests.

For mobile platforms, see
`quit_on_go_back<class_SceneTree_property_quit_on_go_back>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Node<class_Node>` **current\_scene**
`🔗<class_SceneTree_property_current_scene>`

classref-property-setget

-   `void (No return value.)` **set\_current\_scene**(value:
    `Node<class_Node>`)
-   `Node<class_Node>` **get\_current\_scene**()

The root node of the currently loaded main scene, usually as a direct
child of `root<class_SceneTree_property_root>`. See also
`change_scene_to_file<class_SceneTree_method_change_scene_to_file>`,
`change_scene_to_packed<class_SceneTree_method_change_scene_to_packed>`,
and `reload_current_scene<class_SceneTree_method_reload_current_scene>`.

\*\*Warning:\*\* Setting this property directly may not work as
expected, as it does *not* add or remove any nodes from this tree.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **debug\_collisions\_hint** = `false`
`🔗<class_SceneTree_property_debug_collisions_hint>`

classref-property-setget

-   `void (No return value.)` **set\_debug\_collisions\_hint**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_debugging\_collisions\_hint**()

If `true`, collision shapes will be visible when running the game from
the editor for debugging purposes.

\*\*Note:\*\* This property is not designed to be changed at run-time.
Changing the value of
`debug_collisions_hint<class_SceneTree_property_debug_collisions_hint>`
while the project is running will not have the desired effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **debug\_navigation\_hint** = `false`
`🔗<class_SceneTree_property_debug_navigation_hint>`

classref-property-setget

-   `void (No return value.)` **set\_debug\_navigation\_hint**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_debugging\_navigation\_hint**()

If `true`, navigation polygons will be visible when running the game
from the editor for debugging purposes.

\*\*Note:\*\* This property is not designed to be changed at run-time.
Changing the value of
`debug_navigation_hint<class_SceneTree_property_debug_navigation_hint>`
while the project is running will not have the desired effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **debug\_paths\_hint** = `false`
`🔗<class_SceneTree_property_debug_paths_hint>`

classref-property-setget

-   `void (No return value.)` **set\_debug\_paths\_hint**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_debugging\_paths\_hint**()

If `true`, curves from `Path2D<class_Path2D>` and `Path3D<class_Path3D>`
nodes will be visible when running the game from the editor for
debugging purposes.

\*\*Note:\*\* This property is not designed to be changed at run-time.
Changing the value of
`debug_paths_hint<class_SceneTree_property_debug_paths_hint>` while the
project is running will not have the desired effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Node<class_Node>` **edited\_scene\_root**
`🔗<class_SceneTree_property_edited_scene_root>`

classref-property-setget

-   `void (No return value.)` **set\_edited\_scene\_root**(value:
    `Node<class_Node>`)
-   `Node<class_Node>` **get\_edited\_scene\_root**()

The root of the scene currently being edited in the editor. This is
usually a direct child of `root<class_SceneTree_property_root>`.

\*\*Note:\*\* This property does nothing in release builds.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **multiplayer\_poll** = `true`
`🔗<class_SceneTree_property_multiplayer_poll>`

classref-property-setget

-   `void (No return value.)` **set\_multiplayer\_poll\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_multiplayer\_poll\_enabled**()

If `true` (default value), enables automatic polling of the
`MultiplayerAPI<class_MultiplayerAPI>` for this SceneTree during
`process_frame<class_SceneTree_signal_process_frame>`.

If `false`, you need to manually call
`MultiplayerAPI.poll<class_MultiplayerAPI_method_poll>` to process
network packets and deliver RPCs. This allows running RPCs in a
different loop (e.g. physics, thread, specific time step) and for manual
`Mutex<class_Mutex>` protection when accessing the
`MultiplayerAPI<class_MultiplayerAPI>` from threads.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **paused** = `false`
`🔗<class_SceneTree_property_paused>`

classref-property-setget

-   `void (No return value.)` **set\_pause**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_paused**()

If `true`, the scene tree is considered paused. This causes the
following behavior:

-   2D and 3D physics will be stopped, as well as collision detection
    and related signals.
-   Depending on each node's
    `Node.process_mode<class_Node_property_process_mode>`, their
    `Node._process<class_Node_private_method__process>`,
    `Node._physics_process<class_Node_private_method__physics_process>`
    and `Node._input<class_Node_private_method__input>` callback methods
    may not called anymore.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **physics\_interpolation** = `false`
`🔗<class_SceneTree_property_physics_interpolation>`

classref-property-setget

-   `void (No return value.)`
    **set\_physics\_interpolation\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_physics\_interpolation\_enabled**()

If `true`, the renderer will interpolate the transforms of physics
objects between the last two transforms, so that smooth motion is seen
even when physics ticks do not coincide with rendered frames.

The default value of this property is controlled by
`ProjectSettings.physics/common/physics_interpolation<class_ProjectSettings_property_physics/common/physics_interpolation>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **quit\_on\_go\_back** = `true`
`🔗<class_SceneTree_property_quit_on_go_back>`

classref-property-setget

-   `void (No return value.)` **set\_quit\_on\_go\_back**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_quit\_on\_go\_back**()

If `true`, the application quits automatically when navigating back
(e.g. using the system "Back" button on Android).

To handle 'Go Back' button when this option is disabled, use
`DisplayServer.WINDOW_EVENT_GO_BACK_REQUEST<class_DisplayServer_constant_WINDOW_EVENT_GO_BACK_REQUEST>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Window<class_Window>` **root** `🔗<class_SceneTree_property_root>`

classref-property-setget

-   `Window<class_Window>` **get\_root**()

The tree's root `Window<class_Window>`. This is top-most
`Node<class_Node>` of the scene tree, and is always present. An absolute
`NodePath<class_NodePath>` always starts from this node. Children of the
root node may include the loaded
`current_scene<class_SceneTree_property_current_scene>`, as well as any
`AutoLoad <../tutorials/scripting/singletons_autoload>` configured in
the Project Settings.

\*\*Warning:\*\* Do not delete this node. This will result in unstable
behavior, followed by a crash.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **call\_group**(group:
`StringName<class_StringName>`, method: `StringName<class_StringName>`,
...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_SceneTree_method_call_group>`

Calls `method` on each node inside this tree added to the given `group`.
You can pass arguments to `method` by specifying them at the end of this
method call. Nodes that cannot call `method` (either because the method
doesn't exist or the arguments do not match) are ignored. See also
`set_group<class_SceneTree_method_set_group>` and
`notify_group<class_SceneTree_method_notify_group>`.

\*\*Note:\*\* This method acts immediately on all selected nodes at
once, which may cause stuttering in some performance-intensive
situations.

\*\*Note:\*\* In C#, `method` must be in snake\_case when referring to
built-in Godot methods. Prefer using the names exposed in the
`MethodName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **call\_group\_flags**(flags:
`int<class_int>`, group: `StringName<class_StringName>`, method:
`StringName<class_StringName>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_SceneTree_method_call_group_flags>`

Calls the given `method` on each node inside this tree added to the
given `group`. Use `flags` to customize this method's behavior (see
`GroupCallFlags<enum_SceneTree_GroupCallFlags>`). Additional arguments
for `method` can be passed at the end of this method. Nodes that cannot
call `method` (either because the method doesn't exist or the arguments
do not match) are ignored.

    # Calls "hide" to all nodes of the "enemies" group, at the end of the frame and in reverse tree order.
    get_tree().call_group_flags(
            SceneTree.GROUP_CALL_DEFERRED | SceneTree.GROUP_CALL_REVERSE,
            "enemies", "hide")

\*\*Note:\*\* In C#, `method` must be in snake\_case when referring to
built-in Godot methods. Prefer using the names exposed in the
`MethodName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **change\_scene\_to\_file**(path:
`String<class_String>`)
`🔗<class_SceneTree_method_change_scene_to_file>`

Changes the running scene to the one at the given `path`, after loading
it into a `PackedScene<class_PackedScene>` and creating a new instance.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success,
`@GlobalScope.ERR_CANT_OPEN<class_@GlobalScope_constant_ERR_CANT_OPEN>`
if the `path` cannot be loaded into a `PackedScene<class_PackedScene>`,
or
`@GlobalScope.ERR_CANT_CREATE<class_@GlobalScope_constant_ERR_CANT_CREATE>`
if that scene cannot be instantiated.

\*\*Note:\*\* See
`change_scene_to_packed<class_SceneTree_method_change_scene_to_packed>`
for details on the order of operations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**change\_scene\_to\_packed**(packed\_scene:
`PackedScene<class_PackedScene>`)
`🔗<class_SceneTree_method_change_scene_to_packed>`

Changes the running scene to a new instance of the given
`PackedScene<class_PackedScene>` (which must be valid).

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success,
`@GlobalScope.ERR_CANT_CREATE<class_@GlobalScope_constant_ERR_CANT_CREATE>`
if the scene cannot be instantiated, or
`@GlobalScope.ERR_INVALID_PARAMETER<class_@GlobalScope_constant_ERR_INVALID_PARAMETER>`
if the scene is invalid.

\*\*Note:\*\* Operations happen in the following order when
`change_scene_to_packed<class_SceneTree_method_change_scene_to_packed>`
is called:

1.  The current scene node is immediately removed from the tree. From
    that point, `Node.get_tree<class_Node_method_get_tree>` called on
    the current (outgoing) scene will return `null`.
    `current_scene<class_SceneTree_property_current_scene>` will be
    `null`, too, because the new scene is not available yet.
2.  At the end of the frame, the formerly current scene, already removed
    from the tree, will be deleted (freed from memory) and then the new
    scene will be instantiated and added to the tree.
    `Node.get_tree<class_Node_method_get_tree>` and
    `current_scene<class_SceneTree_property_current_scene>` will be back
    to working as usual.

This ensures that both scenes aren't running at the same time, while
still freeing the previous scene in a safe way similar to
`Node.queue_free<class_Node_method_queue_free>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`SceneTreeTimer<class_SceneTreeTimer>` **create\_timer**(time\_sec:
`float<class_float>`, process\_always: `bool<class_bool>` = true,
process\_in\_physics: `bool<class_bool>` = false, ignore\_time\_scale:
`bool<class_bool>` = false) `🔗<class_SceneTree_method_create_timer>`

Returns a new `SceneTreeTimer<class_SceneTreeTimer>`. After `time_sec`
in seconds have passed, the timer will emit
`SceneTreeTimer.timeout<class_SceneTreeTimer_signal_timeout>` and will
be automatically freed.

If `process_always` is `false`, the timer will be paused when setting
`paused<class_SceneTree_property_paused>` to `true`.

If `process_in_physics` is `true`, the timer will update at the end of
the physics frame, instead of the process frame.

If `ignore_time_scale` is `true`, the timer will ignore
`Engine.time_scale<class_Engine_property_time_scale>` and update with
the real, elapsed time.

This method is commonly used to create a one-shot delay timer, as in the
following example:

gdscript

func some\_function():  
print("start") await get\_tree().create\_timer(1.0).timeout print("end")

csharp

public async Task SomeFunction() { GD.Print("start"); await
ToSignal(GetTree().CreateTimer(1.0f),
SceneTreeTimer.SignalName.Timeout); GD.Print("end"); }

\*\*Note:\*\* The timer is always updated *after* all of the nodes in
the tree. A node's `Node._process<class_Node_private_method__process>`
method would be called before the timer updates (or
`Node._physics_process<class_Node_private_method__physics_process>` if
`process_in_physics` is set to `true`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Tween<class_Tween>` **create\_tween**()
`🔗<class_SceneTree_method_create_tween>`

Creates and returns a new `Tween<class_Tween>` processed in this tree.
The Tween will start automatically on the next process frame or physics
frame (depending on its
`TweenProcessMode<enum_Tween_TweenProcessMode>`).

\*\*Note:\*\* A `Tween<class_Tween>` created using this method is not
bound to any `Node<class_Node>`. It may keep working until there is
nothing left to animate. If you want the `Tween<class_Tween>` to be
automatically killed when the `Node<class_Node>` is freed, use
`Node.create_tween<class_Node_method_create_tween>` or
`Tween.bind_node<class_Tween_method_bind_node>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **get\_first\_node\_in\_group**(group:
`StringName<class_StringName>`)
`🔗<class_SceneTree_method_get_first_node_in_group>`

Returns the first `Node<class_Node>` found inside the tree, that has
been added to the given `group`, in scene hierarchy order. Returns
`null` if no match is found. See also
`get_nodes_in_group<class_SceneTree_method_get_nodes_in_group>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_frame**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneTree_method_get_frame>`

Returns how many frames have been processed, since the application
started. This is *not* a measurement of elapsed time.

classref-item-separator

------------------------------------------------------------------------

classref-method

`MultiplayerAPI<class_MultiplayerAPI>` **get\_multiplayer**(for\_path:
`NodePath<class_NodePath>` = NodePath(""))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneTree_method_get_multiplayer>`

Searches for the `MultiplayerAPI<class_MultiplayerAPI>` configured for
the given path, if one does not exist it searches the parent paths until
one is found. If the path is empty, or none is found, the default one is
returned. See `set_multiplayer<class_SceneTree_method_set_multiplayer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_node\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneTree_method_get_node_count>`

Returns the number of nodes inside this tree.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_node\_count\_in\_group**(group:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneTree_method_get_node_count_in_group>`

Returns the number of nodes assigned to the given group.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Node<class_Node>`\]
**get\_nodes\_in\_group**(group: `StringName<class_StringName>`)
`🔗<class_SceneTree_method_get_nodes_in_group>`

Returns an `Array<class_Array>` containing all nodes inside this tree,
that have been added to the given `group`, in scene hierarchy order.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Tween<class_Tween>`\]
**get\_processed\_tweens**()
`🔗<class_SceneTree_method_get_processed_tweens>`

Returns an `Array<class_Array>` of currently existing
`Tween<class_Tween>`s in the tree, including paused tweens.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_group**(name: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SceneTree_method_has_group>`

Returns `true` if a node added to the given group `name` exists in the
tree.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **notify\_group**(group:
`StringName<class_StringName>`, notification: `int<class_int>`)
`🔗<class_SceneTree_method_notify_group>`

Calls `Object.notification<class_Object_method_notification>` with the
given `notification` to all nodes inside this tree added to the `group`.
See also
`Godot notifications <../tutorials/best_practices/godot_notifications>`
and `call_group<class_SceneTree_method_call_group>` and
`set_group<class_SceneTree_method_set_group>`.

\*\*Note:\*\* This method acts immediately on all selected nodes at
once, which may cause stuttering in some performance-intensive
situations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **notify\_group\_flags**(call\_flags:
`int<class_int>`, group: `StringName<class_StringName>`, notification:
`int<class_int>`) `🔗<class_SceneTree_method_notify_group_flags>`

Calls `Object.notification<class_Object_method_notification>` with the
given `notification` to all nodes inside this tree added to the `group`.
Use `call_flags` to customize this method's behavior (see
`GroupCallFlags<enum_SceneTree_GroupCallFlags>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **queue\_delete**(obj: `Object<class_Object>`)
`🔗<class_SceneTree_method_queue_delete>`

Queues the given `obj` to be deleted, calling its
`Object.free<class_Object_method_free>` at the end of the current frame.
This method is similar to
`Node.queue_free<class_Node_method_queue_free>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **quit**(exit\_code: `int<class_int>` = 0)
`🔗<class_SceneTree_method_quit>`

Quits the application at the end of the current iteration, with the
given `exit_code`.

By convention, an exit code of `0` indicates success, whereas any other
exit code indicates an error. For portability reasons, it should be
between `0` and `125` (inclusive).

\*\*Note:\*\* On iOS this method doesn't work. Instead, as recommended
by the [iOS Human Interface
Guidelines](https://developer.apple.com/library/archive/qa/qa1561/_index.html),
the user is expected to close apps via the Home button.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **reload\_current\_scene**()
`🔗<class_SceneTree_method_reload_current_scene>`

Reloads the currently active scene, replacing
`current_scene<class_SceneTree_property_current_scene>` with a new
instance of its original `PackedScene<class_PackedScene>`.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success,
`@GlobalScope.ERR_UNCONFIGURED<class_@GlobalScope_constant_ERR_UNCONFIGURED>`
if no `current_scene<class_SceneTree_property_current_scene>` is
defined,
`@GlobalScope.ERR_CANT_OPEN<class_@GlobalScope_constant_ERR_CANT_OPEN>`
if `current_scene<class_SceneTree_property_current_scene>` cannot be
loaded into a `PackedScene<class_PackedScene>`, or
`@GlobalScope.ERR_CANT_CREATE<class_@GlobalScope_constant_ERR_CANT_CREATE>`
if the scene cannot be instantiated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_group**(group:
`StringName<class_StringName>`, property: `String<class_String>`, value:
`Variant<class_Variant>`) `🔗<class_SceneTree_method_set_group>`

Sets the given `property` to `value` on all nodes inside this tree added
to the given `group`. Nodes that do not have the `property` are ignored.
See also `call_group<class_SceneTree_method_call_group>` and
`notify_group<class_SceneTree_method_notify_group>`.

\*\*Note:\*\* This method acts immediately on all selected nodes at
once, which may cause stuttering in some performance-intensive
situations.

\*\*Note:\*\* In C#, `property` must be in snake\_case when referring to
built-in Godot properties. Prefer using the names exposed in the
`PropertyName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_group\_flags**(call\_flags:
`int<class_int>`, group: `StringName<class_StringName>`, property:
`String<class_String>`, value: `Variant<class_Variant>`)
`🔗<class_SceneTree_method_set_group_flags>`

Sets the given `property` to `value` on all nodes inside this tree added
to the given `group`. Nodes that do not have the `property` are ignored.
Use `call_flags` to customize this method's behavior (see
`GroupCallFlags<enum_SceneTree_GroupCallFlags>`).

\*\*Note:\*\* In C#, `property` must be in snake\_case when referring to
built-in Godot properties. Prefer using the names exposed in the
`PropertyName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_multiplayer**(multiplayer:
`MultiplayerAPI<class_MultiplayerAPI>`, root\_path:
`NodePath<class_NodePath>` = NodePath(""))
`🔗<class_SceneTree_method_set_multiplayer>`

Sets a custom `MultiplayerAPI<class_MultiplayerAPI>` with the given
`root_path` (controlling also the relative subpaths), or override the
default one if `root_path` is empty.

\*\*Note:\*\* No `MultiplayerAPI<class_MultiplayerAPI>` must be
configured for the subpath containing `root_path`, nested custom
multiplayers are not allowed. I.e. if one is configured for
`"/root/Foo"` setting one for `"/root/Foo/Bar"` will cause an error.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unload\_current\_scene**()
`🔗<class_SceneTree_method_unload_current_scene>`

If a current scene is loaded, calling this method will unload it.
