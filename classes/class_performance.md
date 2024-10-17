github\_url  
hide

# Performance

**Inherits:** `Object<class_Object>`

Exposes performance-related data.

classref-introduction-group

## Description

This class provides access to a number of different monitors related to
performance, such as memory usage, draw calls, and FPS. These are the
same as the values displayed in the **Monitor** tab in the editor's
**Debugger** panel. By using the
`get_monitor<class_Performance_method_get_monitor>` method of this
class, you can access this data from your code.

You can add custom monitors using the
`add_custom_monitor<class_Performance_method_add_custom_monitor>`
method. Custom monitors are available in **Monitor** tab in the editor's
**Debugger** panel together with built-in monitors.

\*\*Note:\*\* Some of the built-in monitors are only available in debug
mode and will always return `0` when used in a project exported in
release mode.

\*\*Note:\*\* Some of the built-in monitors are not updated in real-time
for performance reasons, so there may be a delay of up to 1 second
between changes.

\*\*Note:\*\* Custom monitors do not support negative values. Negative
values are clamped to 0.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Monitor**: `🔗<enum_Performance_Monitor>`

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **TIME\_FPS** = `0`

The number of frames rendered in the last second. This metric is only
updated once per second, even if queried more often. *Higher is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **TIME\_PROCESS** = `1`

Time it took to complete one frame, in seconds. *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **TIME\_PHYSICS\_PROCESS** = `2`

Time it took to complete one physics frame, in seconds. *Lower is
better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **TIME\_NAVIGATION\_PROCESS** = `3`

Time it took to complete one navigation step, in seconds. This includes
navigation map updates as well as agent avoidance calculations. *Lower
is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **MEMORY\_STATIC** = `4`

Static memory currently used, in bytes. Not available in release builds.
*Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **MEMORY\_STATIC\_MAX** = `5`

Available static memory. Not available in release builds. *Lower is
better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **MEMORY\_MESSAGE\_BUFFER\_MAX** =
`6`

Largest amount of memory the message queue buffer has used, in bytes.
The message queue is used for deferred functions calls and
notifications. *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **OBJECT\_COUNT** = `7`

Number of objects currently instantiated (including nodes). *Lower is
better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **OBJECT\_RESOURCE\_COUNT** = `8`

Number of resources currently used. *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **OBJECT\_NODE\_COUNT** = `9`

Number of nodes currently instantiated in the scene tree. This also
includes the root node. *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **OBJECT\_ORPHAN\_NODE\_COUNT** =
`10`

Number of orphan nodes, i.e. nodes which are not parented to a node of
the scene tree. *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>`
**RENDER\_TOTAL\_OBJECTS\_IN\_FRAME** = `11`

The total number of objects in the last rendered frame. This metric
doesn't include culled objects (either via hiding nodes, frustum culling
or occlusion culling). *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>`
**RENDER\_TOTAL\_PRIMITIVES\_IN\_FRAME** = `12`

The total number of vertices or indices rendered in the last rendered
frame. This metric doesn't include primitives from culled objects
(either via hiding nodes, frustum culling or occlusion culling). Due to
the depth prepass and shadow passes, the number of primitives is always
higher than the actual number of vertices in the scene (typically double
or triple the original vertex count). *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>`
**RENDER\_TOTAL\_DRAW\_CALLS\_IN\_FRAME** = `13`

The total number of draw calls performed in the last rendered frame.
This metric doesn't include culled objects (either via hiding nodes,
frustum culling or occlusion culling), since they do not result in draw
calls. *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **RENDER\_VIDEO\_MEM\_USED** = `14`

The amount of video memory used (texture and vertex memory combined, in
bytes). Since this metric also includes miscellaneous allocations, this
value is always greater than the sum of
`RENDER_TEXTURE_MEM_USED<class_Performance_constant_RENDER_TEXTURE_MEM_USED>`
and
`RENDER_BUFFER_MEM_USED<class_Performance_constant_RENDER_BUFFER_MEM_USED>`.
*Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **RENDER\_TEXTURE\_MEM\_USED** =
`15`

The amount of texture memory used (in bytes). *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **RENDER\_BUFFER\_MEM\_USED** = `16`

The amount of render buffer memory used (in bytes). *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **PHYSICS\_2D\_ACTIVE\_OBJECTS** =
`17`

Number of active `RigidBody2D<class_RigidBody2D>` nodes in the game.
*Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **PHYSICS\_2D\_COLLISION\_PAIRS** =
`18`

Number of collision pairs in the 2D physics engine. *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **PHYSICS\_2D\_ISLAND\_COUNT** =
`19`

Number of islands in the 2D physics engine. *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **PHYSICS\_3D\_ACTIVE\_OBJECTS** =
`20`

Number of active `RigidBody3D<class_RigidBody3D>` and
`VehicleBody3D<class_VehicleBody3D>` nodes in the game. *Lower is
better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **PHYSICS\_3D\_COLLISION\_PAIRS** =
`21`

Number of collision pairs in the 3D physics engine. *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **PHYSICS\_3D\_ISLAND\_COUNT** =
`22`

Number of islands in the 3D physics engine. *Lower is better.*

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **AUDIO\_OUTPUT\_LATENCY** = `23`

Output latency of the `AudioServer<class_AudioServer>`. Equivalent to
calling
`AudioServer.get_output_latency<class_AudioServer_method_get_output_latency>`,
it is not recommended to call this every frame.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **NAVIGATION\_ACTIVE\_MAPS** = `24`

Number of active navigation maps in the
`NavigationServer3D<class_NavigationServer3D>`. This also includes the
two empty default navigation maps created by World2D and World3D.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **NAVIGATION\_REGION\_COUNT** = `25`

Number of active navigation regions in the
`NavigationServer3D<class_NavigationServer3D>`.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **NAVIGATION\_AGENT\_COUNT** = `26`

Number of active navigation agents processing avoidance in the
`NavigationServer3D<class_NavigationServer3D>`.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **NAVIGATION\_LINK\_COUNT** = `27`

Number of active navigation links in the
`NavigationServer3D<class_NavigationServer3D>`.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **NAVIGATION\_POLYGON\_COUNT** =
`28`

Number of navigation mesh polygons in the
`NavigationServer3D<class_NavigationServer3D>`.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **NAVIGATION\_EDGE\_COUNT** = `29`

Number of navigation mesh polygon edges in the
`NavigationServer3D<class_NavigationServer3D>`.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **NAVIGATION\_EDGE\_MERGE\_COUNT** =
`30`

Number of navigation mesh polygon edges that were merged due to edge key
overlap in the `NavigationServer3D<class_NavigationServer3D>`.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>`
**NAVIGATION\_EDGE\_CONNECTION\_COUNT** = `31`

Number of polygon edges that are considered connected by edge proximity
`NavigationServer3D<class_NavigationServer3D>`.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **NAVIGATION\_EDGE\_FREE\_COUNT** =
`32`

Number of navigation mesh polygon edges that could not be merged in the
`NavigationServer3D<class_NavigationServer3D>`. The edges still may be
connected by edge proximity or with links.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **NAVIGATION\_OBSTACLE\_COUNT** =
`33`

Number of active navigation obstacles in the
`NavigationServer3D<class_NavigationServer3D>`.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **PIPELINE\_COMPILATIONS\_CANVAS** =
`34`

Number of pipeline compilations that were triggered by the 2D canvas
renderer.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **PIPELINE\_COMPILATIONS\_MESH** =
`35`

Number of pipeline compilations that were triggered by loading meshes.
These compilations will show up as longer loading times the first time a
user runs the game and the pipeline is required.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **PIPELINE\_COMPILATIONS\_SURFACE**
= `36`

Number of pipeline compilations that were triggered by building the
surface cache before rendering the scene. These compilations will show
up as a stutter when loading an scene the first time a user runs the
game and the pipeline is required.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **PIPELINE\_COMPILATIONS\_DRAW** =
`37`

Number of pipeline compilations that were triggered while drawing the
scene. These compilations will show up as stutters during gameplay the
first time a user runs the game and the pipeline is required.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>`
**PIPELINE\_COMPILATIONS\_SPECIALIZATION** = `38`

Number of pipeline compilations that were triggered to optimize the
current scene. These compilations are done in the background and should
not cause any stutters whatsoever.

classref-enumeration-constant

`Monitor<enum_Performance_Monitor>` **MONITOR\_MAX** = `39`

Represents the size of the `Monitor<enum_Performance_Monitor>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_custom\_monitor**(id:
`StringName<class_StringName>`, callable: `Callable<class_Callable>`,
arguments: `Array<class_Array>` = \[\])
`🔗<class_Performance_method_add_custom_monitor>`

Adds a custom monitor with the name `id`. You can specify the category
of the monitor using slash delimiters in `id` (for example:
`"Game/NumberOfNPCs"`). If there is more than one slash delimiter, then
the default category is used. The default category is `"Custom"`. Prints
an error if given `id` is already present.

gdscript

func \_ready():  
var monitor\_value = Callable(self, "get\_monitor\_value")

\# Adds monitor with name "MyName" to category "MyCategory".
Performance.add\_custom\_monitor("MyCategory/MyMonitor", monitor\_value)

\# Adds monitor with name "MyName" to category "Custom". \# Note:
"MyCategory/MyMonitor" and "MyMonitor" have same name but different IDs,
so the code is valid. Performance.add\_custom\_monitor("MyMonitor",
monitor\_value)

\# Adds monitor with name "MyName" to category "Custom". \# Note:
"MyMonitor" and "Custom/MyMonitor" have same name and same category but
different IDs, so the code is valid.
Performance.add\_custom\_monitor("Custom/MyMonitor", monitor\_value)

\# Adds monitor with name "MyCategoryOne/MyCategoryTwo/MyMonitor" to
category "Custom".
Performance.add\_custom\_monitor("MyCategoryOne/MyCategoryTwo/MyMonitor",
monitor\_value)

func get\_monitor\_value():  
return randi() % 25

csharp

public override void \_Ready() { var monitorValue = new Callable(this,
MethodName.GetMonitorValue);

> // Adds monitor with name "MyName" to category "MyCategory".
> Performance.AddCustomMonitor("MyCategory/MyMonitor", monitorValue); //
> Adds monitor with name "MyName" to category "Custom". // Note:
> "MyCategory/MyMonitor" and "MyMonitor" have same name but different
> ids so the code is valid. Performance.AddCustomMonitor("MyMonitor",
> monitorValue);
>
> // Adds monitor with name "MyName" to category "Custom". // Note:
> "MyMonitor" and "Custom/MyMonitor" have same name and same category
> but different ids so the code is valid.
> Performance.AddCustomMonitor("Custom/MyMonitor", monitorValue);
>
> // Adds monitor with name "MyCategoryOne/MyCategoryTwo/MyMonitor" to
> category "Custom".
> Performance.AddCustomMonitor("MyCategoryOne/MyCategoryTwo/MyMonitor",
> monitorValue);

}

public int GetMonitorValue() { return GD.Randi() % 25; }

The debugger calls the callable to get the value of custom monitor. The
callable must return a zero or positive integer or floating-point
number.

Callables are called with arguments supplied in argument array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_custom\_monitor**(id:
`StringName<class_StringName>`)
`🔗<class_Performance_method_get_custom_monitor>`

Returns the value of custom monitor with given `id`. The callable is
called to get the value of custom monitor. See also
`has_custom_monitor<class_Performance_method_has_custom_monitor>`.
Prints an error if the given `id` is absent.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`StringName<class_StringName>`\]
**get\_custom\_monitor\_names**()
`🔗<class_Performance_method_get_custom_monitor_names>`

Returns the names of active custom monitors in an `Array<class_Array>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_monitor**(monitor:
`Monitor<enum_Performance_Monitor>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Performance_method_get_monitor>`

Returns the value of one of the available built-in monitors. You should
provide one of the `Monitor<enum_Performance_Monitor>` constants as the
argument, like this:

gdscript

print(Performance.get\_monitor(Performance.TIME\_FPS)) \# Prints the FPS
to the console.

csharp

GD.Print(Performance.GetMonitor(Performance.Monitor.TimeFps)); // Prints
the FPS to the console.

See `get_custom_monitor<class_Performance_method_get_custom_monitor>` to
query custom performance monitors' values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_monitor\_modification\_time**()
`🔗<class_Performance_method_get_monitor_modification_time>`

Returns the last tick in which custom monitor was added/removed (in
microseconds since the engine started). This is set to
`Time.get_ticks_usec<class_Time_method_get_ticks_usec>` when the monitor
is updated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_custom\_monitor**(id:
`StringName<class_StringName>`)
`🔗<class_Performance_method_has_custom_monitor>`

Returns `true` if custom monitor with the given `id` is present, `false`
otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_custom\_monitor**(id:
`StringName<class_StringName>`)
`🔗<class_Performance_method_remove_custom_monitor>`

Removes the custom monitor with given `id`. Prints an error if the given
`id` is already absent.
