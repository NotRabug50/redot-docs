github\_url  
hide

# PackedScene

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

An abstraction of a serialized scene.

classref-introduction-group

## Description

A simplified interface to a scene file. Provides access to operations
and checks that can be performed on the scene resource itself.

Can be used to save a node to a file. When saving, the node as well as
all the nodes it owns get saved (see
`Node.owner<class_Node_property_owner>` property).

\*\*Note:\*\* The node doesn't need to own itself.

\*\*Example of loading a saved scene:\*\*

gdscript

\# Use load() instead of preload() if the path isn't known at
compile-time. var scene = preload("<res://scene.tscn>").instantiate() \#
Add the node as a child of the node the script is attached to.
add\_child(scene)

csharp

// C# has no preload, so you have to always use
ResourceLoader.Load&lt;PackedScene&gt;(). var scene =
ResourceLoader.Load&lt;PackedScene&gt;("<res://scene.tscn>").Instantiate();
// Add the node as a child of the node the script is attached to.
AddChild(scene);

\*\*Example of saving a node with different owners:\*\* The following
example creates 3 objects: `Node2D<class_Node2D>` (`node`),
`RigidBody2D<class_RigidBody2D>` (`body`) and
`CollisionObject2D<class_CollisionObject2D>` (`collision`). `collision`
is a child of `body` which is a child of `node`. Only `body` is owned by
`node` and `pack<class_PackedScene_method_pack>` will therefore only
save those two nodes, but not `collision`.

gdscript

\# Create the objects. var node = Node2D.new() var body =
RigidBody2D.new() var collision = CollisionShape2D.new()

\# Create the object hierarchy. body.add\_child(collision)
node.add\_child(body)

\# Change owner of <span class="title-ref">body</span>, but not of
<span class="title-ref">collision</span>. body.owner = node var scene =
PackedScene.new()

\# Only <span class="title-ref">node</span> and
<span class="title-ref">body</span> are now packed. var result =
scene.pack(node) if result == OK: var error = ResourceSaver.save(scene,
"<res://path/name.tscn>") \# Or "user://..." if error != OK:
push\_error("An error occurred while saving the scene to disk.")

csharp

// Create the objects. var node = new Node2D(); var body = new
RigidBody2D(); var collision = new CollisionShape2D();

// Create the object hierarchy. body.AddChild(collision);
node.AddChild(body);

// Change owner of <span class="title-ref">body</span>, but not of
<span class="title-ref">collision</span>. body.Owner = node; var scene =
new PackedScene();

// Only <span class="title-ref">node</span> and
<span class="title-ref">body</span> are now packed. Error result =
scene.Pack(node); if (result == Error.Ok) { Error error =
ResourceSaver.Save(scene, "<res://path/name.tscn>"); // Or "user://..."
if (error != Error.Ok) { GD.PushError("An error occurred while saving
the scene to disk."); } }

classref-introduction-group

## Tutorials

-   [2D Role Playing Game (RPG)
    Demo](https://godotengine.org/asset-library/asset/2729)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **GenEditState**: `🔗<enum_PackedScene_GenEditState>`

classref-enumeration-constant

`GenEditState<enum_PackedScene_GenEditState>`
**GEN\_EDIT\_STATE\_DISABLED** = `0`

If passed to `instantiate<class_PackedScene_method_instantiate>`, blocks
edits to the scene state.

classref-enumeration-constant

`GenEditState<enum_PackedScene_GenEditState>`
**GEN\_EDIT\_STATE\_INSTANCE** = `1`

If passed to `instantiate<class_PackedScene_method_instantiate>`,
provides local scene resources to the local scene.

\*\*Note:\*\* Only available in editor builds.

classref-enumeration-constant

`GenEditState<enum_PackedScene_GenEditState>` **GEN\_EDIT\_STATE\_MAIN**
= `2`

If passed to `instantiate<class_PackedScene_method_instantiate>`,
provides local scene resources to the local scene. Only the main scene
should receive the main edit state.

\*\*Note:\*\* Only available in editor builds.

classref-enumeration-constant

`GenEditState<enum_PackedScene_GenEditState>`
**GEN\_EDIT\_STATE\_MAIN\_INHERITED** = `3`

It's similar to
`GEN_EDIT_STATE_MAIN<class_PackedScene_constant_GEN_EDIT_STATE_MAIN>`,
but for the case where the scene is being instantiated to be the base of
another one.

\*\*Note:\*\* Only available in editor builds.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **can\_instantiate**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedScene_method_can_instantiate>`

Returns `true` if the scene file has nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`SceneState<class_SceneState>` **get\_state**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedScene_method_get_state>`

Returns the `SceneState<class_SceneState>` representing the scene file
contents.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **instantiate**(edit\_state:
`GenEditState<enum_PackedScene_GenEditState>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedScene_method_instantiate>`

Instantiates the scene's node hierarchy. Triggers child scene
instantiation(s). Triggers a
`Node.NOTIFICATION_SCENE_INSTANTIATED<class_Node_constant_NOTIFICATION_SCENE_INSTANTIATED>`
notification on the root node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **pack**(path: `Node<class_Node>`)
`🔗<class_PackedScene_method_pack>`

Packs the `path` node, and all owned sub-nodes, into this
**PackedScene**. Any existing data will be cleared. See
`Node.owner<class_Node_property_owner>`.
