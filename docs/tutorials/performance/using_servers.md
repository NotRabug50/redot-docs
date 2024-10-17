article\_outdated  
True

# Optimization using Servers

Engines like Godot provide increased ease of use thanks to their high
level constructs and features. Most of them are accessed and used via
the `Scene System<doc_scene_tree>`. Using nodes and resources simplifies
project organization and asset management in complex games.

There are, of course, always drawbacks:

-   There is an extra layer of complexity.
-   Performance is lower than when using simple APIs directly.
-   It is not possible to use multiple threads to control them.
-   More memory is needed.

In many cases, this is not really a problem (Godot is very optimized,
and most operations are handled with signals, so no polling is
required). Still, sometimes it can be. For example, dealing with tens of
thousands of instances for something that needs to be processed every
frame can be a bottleneck.

This type of situation makes programmers regret they are using a game
engine and wish they could go back to a more handcrafted, low level
implementation of game code.

Still, Godot is designed to work around this problem.

You can see how using low-level servers works in action using the
[Bullet Shower demo
project](https://github.com/godotengine/godot-demo-projects/tree/master/2d/bullet_shower)

## Servers

One of the most interesting design decisions for Godot is the fact that
the whole scene system is *optional*. While it is not currently possible
to compile it out, it can be completely bypassed.

At the core, Godot uses the concept of Servers. They are very low-level
APIs to control rendering, physics, sound, etc. The scene system is
built on top of them and uses them directly. The most common servers
are:

-   `RenderingServer <class_RenderingServer>`: handles everything
    related to graphics.
-   `PhysicsServer3D <class_PhysicsServer3D>`: handles everything
    related to 3D physics.
-   `PhysicsServer2D <class_PhysicsServer2D>`: handles everything
    related to 2D physics.
-   `AudioServer <class_AudioServer>`: handles everything related to
    audio.

Explore their APIs and you will realize that all the functions provided
are low-level implementations of everything Godot allows you to do.

## RIDs

The key to using servers is understanding Resource ID
(`RID <class_RID>`) objects. These are opaque handles to the server
implementation. They are allocated and freed manually. Almost every
function in the servers requires RIDs to access the actual resource.

Most Godot nodes and resources contain these RIDs from the servers
internally, and they can be obtained with different functions. In fact,
anything that inherits `Resource <class_Resource>` can be directly
casted to an RID. Not all resources contain an RID, though: in such
cases, the RID will be empty. The resource can then be passed to server
APIs as an RID.

Warning

Resources are reference-counted (see `RefCounted <class_RefCounted>`),
and references to a resource's RID are *not* counted when determining
whether the resource is still in use. Make sure to keep a reference to
the resource outside the server, or else both it and its RID will be
erased.

For nodes, there are many functions available:

-   For CanvasItem, the
    `CanvasItem.get_canvas_item() <class_CanvasItem_method_get_canvas_item>`
    method will return the canvas item RID in the server.
-   For CanvasLayer, the
    `CanvasLayer.get_canvas() <class_CanvasLayer_method_get_canvas>`
    method will return the canvas RID in the server.
-   For Viewport, the
    `Viewport.get_viewport_rid() <class_Viewport_method_get_viewport_rid>`
    method will return the viewport RID in the server.
-   For 3D, the `World3D <class_World3D>` resource (obtainable in the
    `Viewport <class_Viewport>` and `Node3D <class_Node3D>` nodes)
    contains functions to get the *RenderingServer Scenario*, and the
    *PhysicsServer Space*. This allows creating 3D objects directly with
    the server API and using them.
-   For 2D, the `World2D <class_World2D>` resource (obtainable in the
    `Viewport <class_Viewport>` and `CanvasItem <class_CanvasItem>`
    nodes) contains functions to get the *RenderingServer Canvas*, and
    the *Physics2DServer Space*. This allows creating 2D objects
    directly with the server API and using them.
-   The `VisualInstance3D<class_VisualInstance3D>` class, allows getting
    the scenario *instance* and *instance base* via the
    `VisualInstance3D.get_instance() <class_VisualInstance3D_method_get_instance>`
    and
    `VisualInstance3D.get_base() <class_VisualInstance3D_method_get_base>`
    respectively.

Try exploring the nodes and resources you are familiar with and find the
functions to obtain the server *RIDs*.

It is not advised to control RIDs from objects that already have a node
associated. Instead, server functions should always be used for creating
and controlling new ones and interacting with the existing ones.

## Creating a sprite

This is an example of how to create a sprite from code and move it using
the low-level `CanvasItem <class_CanvasItem>` API.

.. code-tab:: gdscript GDScript

extends Node2D

\# RenderingServer expects references to be kept around. var texture

func \_ready():  
\# Create a canvas item, child of this node. var ci\_rid =
RenderingServer.canvas\_item\_create() \# Make this node the parent.
RenderingServer.canvas\_item\_set\_parent(ci\_rid, get\_canvas\_item())
\# Draw a texture on it. \# Remember, keep this reference. texture =
load("<res://my_texture.png>") \# Add it, centered.
RenderingServer.canvas\_item\_add\_texture\_rect(ci\_rid,
Rect2(-texture.get\_size() / 2, texture.get\_size()), texture) \# Add
the item, rotated 45 degrees and translated. var xform =
Transform2D().rotated(deg\_to\_rad(45)).translated(Vector2(20, 30))
RenderingServer.canvas\_item\_set\_transform(ci\_rid, xform)

csharp

public partial class MyNode2D : Node2D { // RenderingServer expects
references to be kept around. private Texture2D \_texture;

> public override void \_Ready() { // Create a canvas item, child of
> this node. Rid ciRid = RenderingServer.CanvasItemCreate(); // Make
> this node the parent. RenderingServer.CanvasItemSetParent(ciRid,
> GetCanvasItem()); // Draw a texture on it. // Remember, keep this
> reference. \_texture =
> ResourceLoader.Load&lt;Texture2D&gt;("<res://MyTexture.png>"); // Add
> it, centered. RenderingServer.CanvasItemAddTextureRect(ciRid, new
> Rect2(-\_texture.GetSize() / 2, \_texture.GetSize()),
> \_texture.GetRid()); // Add the item, rotated 45 degrees and
> translated. Transform2D xform =
> Transform2D.Identity.Rotated(Mathf.DegToRad(45)).Translated(new
> Vector2(20, 30)); RenderingServer.CanvasItemSetTransform(ciRid,
> xform); }

}

The Canvas Item API in the server allows you to add draw primitives to
it. Once added, they can't be modified. The Item needs to be cleared and
the primitives re-added (this is not the case for setting the transform,
which can be done as many times as desired).

Primitives are cleared this way:

.. code-tab:: gdscript GDScript

RenderingServer.canvas\_item\_clear(ci\_rid)

csharp

RenderingServer.CanvasItemClear(ciRid);

## Instantiating a Mesh into 3D space

The 3D APIs are different from the 2D ones, so the instantiation API
must be used.

.. code-tab:: gdscript GDScript

extends Node3D

\# RenderingServer expects references to be kept around. var mesh

func \_ready():  
\# Create a visual instance (for 3D). var instance =
RenderingServer.instance\_create() \# Set the scenario from the world,
this ensures it \# appears with the same objects as the scene. var
scenario = get\_world\_3d().scenario
RenderingServer.instance\_set\_scenario(instance, scenario) \# Add a
mesh to it. \# Remember, keep the reference. mesh =
load("<res://mymesh.obj>") RenderingServer.instance\_set\_base(instance,
mesh) \# Move the mesh around. var xform = Transform3D(Basis(),
Vector3(20, 100, 0)) RenderingServer.instance\_set\_transform(instance,
xform)

csharp

public partial class MyNode3D : Node3D { // RenderingServer expects
references to be kept around. private Mesh \_mesh;

> public override void \_Ready() { // Create a visual instance (for 3D).
> Rid instance = RenderingServer.InstanceCreate(); // Set the scenario
> from the world, this ensures it // appears with the same objects as
> the scene. Rid scenario = GetWorld3D().Scenario;
> RenderingServer.InstanceSetScenario(instance, scenario); // Add a mesh
> to it. // Remember, keep the reference. \_mesh =
> ResourceLoader.Load&lt;Mesh&gt;("<res://MyMesh.obj>");
> RenderingServer.InstanceSetBase(instance, \_mesh.GetRid()); // Move
> the mesh around. Transform3D xform = new Transform3D(Basis.Identity,
> new Vector3(20, 100, 0));
> RenderingServer.InstanceSetTransform(instance, xform); }

}

## Creating a 2D RigidBody and moving a sprite with it

This creates a `RigidBody2D <class_RigidBody2D>` using the
`PhysicsServer2D <class_PhysicsServer2D>` API, and moves a
`CanvasItem <class_CanvasItem>` when the body moves.

.. code-tab:: gdscript GDScript

\# Physics2DServer expects references to be kept around. var body var
shape

func \_body\_moved(state, index):  
\# Created your own canvas item, use it here.
RenderingServer.canvas\_item\_set\_transform(canvas\_item,
state.transform)

func \_ready():  
\# Create the body. body = Physics2DServer.body\_create()
Physics2DServer.body\_set\_mode(body, Physics2DServer.BODY\_MODE\_RIGID)
\# Add a shape. shape = Physics2DServer.rectangle\_shape\_create() \#
Set rectangle extents. Physics2DServer.shape\_set\_data(shape,
Vector2(10, 10)) \# Make sure to keep the shape reference!
Physics2DServer.body\_add\_shape(body, shape) \# Set space, so it
collides in the same space as current scene.
Physics2DServer.body\_set\_space(body, get\_world\_2d().space) \# Move
initial position. Physics2DServer.body\_set\_state(body,
Physics2DServer.BODY\_STATE\_TRANSFORM, Transform2D(0, Vector2(10, 20)))
\# Add the transform callback, when body moves \# The last parameter is
optional, can be used as index \# if you have many bodies and a single
callback. Physics2DServer.body\_set\_force\_integration\_callback(body,
self, "\_body\_moved", 0)

csharp

using Godot;

public partial class MyNode2D : Node2D { private Rid \_canvasItem;

> private void BodyMoved(PhysicsDirectBodyState2D state, int index) {
> RenderingServer.CanvasItemSetTransform(\_canvasItem, state.Transform);
> }
>
> public override void \_Ready() { // Create the body. var body =
> PhysicsServer2D.BodyCreate(); PhysicsServer2D.BodySetMode(body,
> PhysicsServer2D.BodyMode.Rigid); // Add a shape. var shape =
> PhysicsServer2D.RectangleShapeCreate(); // Set rectangle extents.
> PhysicsServer2D.ShapeSetData(shape, new Vector2(10, 10)); // Make sure
> to keep the shape reference! PhysicsServer2D.BodyAddShape(body,
> shape); // Set space, so it collides in the same space as current
> scene. PhysicsServer2D.BodySetSpace(body, GetWorld2D().Space); // Move
> initial position. PhysicsServer2D.BodySetState(body,
> PhysicsServer2D.BodyState.Transform, new Transform2D(0, new
> Vector2(10, 20))); // Add the transform callback, when body moves //
> The last parameter is optional, can be used as index // if you have
> many bodies and a single callback.
> PhysicsServer2D.BodySetForceIntegrationCallback(body, new
> Callable(this, MethodName.BodyMoved), 0); }

}

The 3D version should be very similar, as 2D and 3D physics servers are
identical (using `RigidBody3D <class_RigidBody3D>` and
`PhysicsServer3D <class_PhysicsServer3D>` respectively).

## Getting data from the servers

Try to **never** request any information from `RenderingServer`,
`PhysicsServer2D` or `PhysicsServer3D` by calling functions unless you
know what you are doing. These servers will often run asynchronously for
performance and calling any function that returns a value will stall
them and force them to process anything pending until the function is
actually called. This will severely decrease performance if you call
them every frame (and it won't be obvious why).

Because of this, most APIs in such servers are designed so it's not even
possible to request information back, until it's actual data that can be
saved.
