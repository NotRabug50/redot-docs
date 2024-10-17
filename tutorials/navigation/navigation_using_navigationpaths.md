# Using NavigationPaths

## Obtaining a NavigationPath

Navigation paths can be directly queried from the NavigationServer and
do not require any additional nodes or objects as long as the navigation
map has a navigation mesh to work with.

To obtain a 2D path, use
`NavigationServer2D.map_get_path(map, from, to, optimize, navigation_layers)`.

To obtain a 3D path, use
`NavigationServer3D.map_get_path(map, from, to, optimize, navigation_layers)`.

For more customizable navigation path queries that require additional
setup see `doc_navigation_using_navigationpathqueryobjects`.

One of the required parameters for the query is the RID of the
navigation map. Each game world has a default navigation map
automatically created. The default navigation maps can be retrieved with
`get_world_2d().get_navigation_map()` from any Node2D inheriting node or
`get_world_3d().get_navigation_map()` from any Node3D inheriting node.
The second and third parameters are the starting position and the target
position as Vector2 for 2D or Vector3 for 3D.

If the `optimized` parameter is `true`, path positions will be shortened
along polygon corners with an additional funnel algorithm pass. This
works well for free movement on navigation meshes with unequally sized
polygons as the path will hug around corners along the polygon corridor
found by the A\* algorithm. With small cells the A\* algorithm creates a
very narrow funnel corridor that can create ugly corner paths when used
with grids.

If the `optimized` parameter is `false`, path positions will be placed
at the center of each polygon edge. This works well for pure grid
movement on navigation meshes with equally sized polygons as the path
will go through the center of the grid cells. Outside of grids due to
polygons often covering large open areas with a single, long edge this
can create paths with unnecessary long detours.

.. code-tab:: gdscript 2D GDScript

extends Node2D

\# Basic query for a navigation path using the default navigation map.

func get\_navigation\_path(p\_start\_position: Vector2, p\_target\_position: Vector2) -&gt; PackedVector2Array:  
if not is\_inside\_tree():  
return PackedVector2Array()

var default\_map\_rid: RID = get\_world\_2d().get\_navigation\_map() var
path: PackedVector2Array = NavigationServer2D.map\_get\_path(
default\_map\_rid, p\_start\_position, p\_target\_position, true )
return path

csharp 2D C#

using Godot; using System;

public partial class MyNode2D : Node2D { // Basic query for a navigation
path using the default navigation map.

> private Vector2\[\] GetNavigationPath(Vector2 startPosition, Vector2
> targetPosition) { if (!IsInsideTree()) { return
> Array.Empty&lt;Vector2&gt;(); }
>
> > Rid defaultMapRid = GetWorld2D().NavigationMap; Vector2\[\] path =
> > NavigationServer2D.MapGetPath( defaultMapRid, startPosition,
> > targetPosition, true ); return path;
>
> }

}

gdscript 3D GDScript

extends Node3D

\# Basic query for a navigation path using the default navigation map.

func get\_navigation\_path(p\_start\_position: Vector3, p\_target\_position: Vector3) -&gt; PackedVector3Array:  
if not is\_inside\_tree():  
return PackedVector3Array()

var default\_map\_rid: RID = get\_world\_3d().get\_navigation\_map() var
path: PackedVector3Array = NavigationServer3D.map\_get\_path(
default\_map\_rid, p\_start\_position, p\_target\_position, true )
return path

csharp 3D C#

using Godot; using System;

public partial class MyNode3D : Node3D { // Basic query for a navigation
path using the default navigation map.

> private Vector3\[\] GetNavigationPath(Vector3 startPosition, Vector3
> targetPosition) { if (!IsInsideTree()) { return
> Array.Empty&lt;Vector3&gt;(); }
>
> > Rid defaultMapRid = GetWorld3D().NavigationMap; Vector3\[\] path =
> > NavigationServer3D.MapGetPath( defaultMapRid, startPosition,
> > targetPosition, true ); return path;
>
> }

}

A returned `path` by the NavigationServer will be a `PackedVector2Array`
for 2D or a `PackedVector3Array` for 3D. These are just a
memory-optimized `Array` of vector positions. All position vectors
inside the array are guaranteed to be inside a NavigationPolygon or
NavigationMesh. The path array, if not empty, has the navigation mesh
position closest to the starting position at the first index `path[0]`
position. The closest available navigation mesh position to the target
position is the last index `path[path.size()-1]` position. All indexes
between are the path points that an actor should follow to reach the
target without leaving the navigation mesh.

Note

If the target position is on a different navigation mesh that is not
merged or connected the navigation path will lead to the closest
possible position on the starting position navigation mesh.

The following script moves a Node3D inheriting node along a navigation
path using the default navigation map by setting the target position
with `set_movement_target()`.

.. code-tab:: gdscript GDScript

@onready var default\_3d\_map\_rid: RID =
get\_world\_3d().get\_navigation\_map()

var movement\_speed: float = 4.0 var movement\_delta: float var
path\_point\_margin: float = 0.5

var current\_path\_index: int = 0 var current\_path\_point: Vector3 var
current\_path: PackedVector3Array

func set\_movement\_target(target\_position: Vector3):

> var start\_position: Vector3 = global\_transform.origin
>
> current\_path = NavigationServer3D.map\_get\_path(  
> default\_3d\_map\_rid, start\_position, target\_position, true
>
> )
>
> if not current\_path.is\_empty():  
> current\_path\_index = 0 current\_path\_point = current\_path\[0\]

func \_physics\_process(delta):

> if current\_path.is\_empty():  
> return
>
> movement\_delta = movement\_speed \* delta
>
> if global\_transform.origin.distance\_to(current\_path\_point) &lt;= path\_point\_margin:  
> current\_path\_index += 1 if current\_path\_index &gt;=
> current\_path.size(): current\_path = \[\] current\_path\_index = 0
> current\_path\_point = global\_transform.origin return
>
> current\_path\_point = current\_path\[current\_path\_index\]
>
> var new\_velocity: Vector3 =
> global\_transform.origin.direction\_to(current\_path\_point) \*
> movement\_delta
>
> global\_transform.origin =
> global\_transform.origin.move\_toward(global\_transform.origin +
> new\_velocity, movement\_delta)

csharp

using Godot;

public partial class MyNode3D : Node3D { private Rid \_default3DMapRid;

> private float \_movementSpeed = 4.0f; private float \_movementDelta;
> private float \_pathPointMargin = 0.5f;
>
> private int \_currentPathIndex = 0; private Vector3
> \_currentPathPoint; private Vector3\[\] \_currentPath;
>
> public override void \_Ready() { \_default3DMapRid =
> GetWorld3D().NavigationMap; }
>
> private void SetMovementTarget(Vector3 targetPosition) { Vector3
> startPosition = GlobalTransform.Origin;
>
> > \_currentPath = NavigationServer3D.MapGetPath(\_default3DMapRid,
> > startPosition, targetPosition, true);
> >
> > if (!\_currentPath.IsEmpty()) { \_currentPathIndex = 0;
> > \_currentPathPoint = \_currentPath\[0\]; }
>
> }
>
> public override void \_PhysicsProcess(double delta) { if
> (\_currentPath.IsEmpty()) { return; }
>
> > \_movementDelta = \_movementSpeed \* (float)delta;
> >
> > if (GlobalTransform.Origin.DistanceTo(\_currentPathPoint) &lt;=
> > \_pathPointMargin) { \_currentPathIndex += 1; if (\_currentPathIndex
> > &gt;= \_currentPath.Length) { \_currentPath =
> > Array.Empty&lt;Vector3&gt;(); \_currentPathIndex = 0;
> > \_currentPathPoint = GlobalTransform.Origin; return; } }
> >
> > \_currentPathPoint = \_currentPath\[\_currentPathIndex\];
> >
> > Vector3 newVelocity =
> > GlobalTransform.Origin.DirectionTo(\_currentPathPoint) \*
> > \_movementDelta; var globalTransform = GlobalTransform;
> > globalTransform.Origin =
> > globalTransform.Origin.MoveToward(globalTransform.Origin +
> > newVelocity, \_movementDelta); GlobalTransform = globalTransform;
>
> }

}
