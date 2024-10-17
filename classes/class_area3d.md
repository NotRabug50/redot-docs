github\_url  
hide

# Area3D

**Inherits:** `CollisionObject3D<class_CollisionObject3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A region of 3D space that detects other
`CollisionObject3D<class_CollisionObject3D>`s entering or exiting it.

classref-introduction-group

## Description

**Area3D** is a region of 3D space defined by one or multiple
`CollisionShape3D<class_CollisionShape3D>` or
`CollisionPolygon3D<class_CollisionPolygon3D>` child nodes. It detects
when other `CollisionObject3D<class_CollisionObject3D>`s enter or exit
it, and it also keeps track of which collision objects haven't exited it
yet (i.e. which one are overlapping it).

This node can also locally alter or override physics parameters
(gravity, damping) and route audio to custom audio buses.

\*\*Note:\*\* Areas and bodies created with
`PhysicsServer3D<class_PhysicsServer3D>` might not interact as expected
with **Area3D**s, and might not emit signals or track objects correctly.

\*\*Warning:\*\* Using a
`ConcavePolygonShape3D<class_ConcavePolygonShape3D>` inside a
`CollisionShape3D<class_CollisionShape3D>` child of this node (created
e.g. by using the **Create Trimesh Collision Sibling** option in the
**Mesh** menu that appears when selecting a
`MeshInstance3D<class_MeshInstance3D>` node) may give unexpected
results, since this collision shape is hollow. If this is not desired,
it has to be split into multiple
`ConvexPolygonShape3D<class_ConvexPolygonShape3D>`s or primitive shapes
like `BoxShape3D<class_BoxShape3D>`, or in some cases it may be
replaceable by a `CollisionPolygon3D<class_CollisionPolygon3D>`.

classref-introduction-group

## Tutorials

-   `Using Area2D <../tutorials/physics/using_area_2d>`
-   [3D Platformer
    Demo](https://godotengine.org/asset-library/asset/2748)
-   [GUI in 3D Viewport
    Demo](https://godotengine.org/asset-library/asset/2807)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**area\_entered**(area: `Area3D<class_Area3D>`)
`🔗<class_Area3D_signal_area_entered>`

Emitted when the received `area` enters this area. Requires
`monitoring<class_Area3D_property_monitoring>` to be set to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**area\_exited**(area: `Area3D<class_Area3D>`)
`🔗<class_Area3D_signal_area_exited>`

Emitted when the received `area` exits this area. Requires
`monitoring<class_Area3D_property_monitoring>` to be set to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**area\_shape\_entered**(area\_rid: `RID<class_RID>`, area:
`Area3D<class_Area3D>`, area\_shape\_index: `int<class_int>`,
local\_shape\_index: `int<class_int>`)
`🔗<class_Area3D_signal_area_shape_entered>`

Emitted when a `Shape3D<class_Shape3D>` of the received `area` enters a
shape of this area. Requires
`monitoring<class_Area3D_property_monitoring>` to be set to `true`.

`local_shape_index` and `area_shape_index` contain indices of the
interacting shapes from this area and the other area, respectively.
`area_rid` contains the `RID<class_RID>` of the other area. These values
can be used with the `PhysicsServer3D<class_PhysicsServer3D>`.

\*\*Example of getting the\*\*
`CollisionShape3D<class_CollisionShape3D>` **node from the shape
index:**

gdscript

var other\_shape\_owner = area.shape\_find\_owner(area\_shape\_index)
var other\_shape\_node =
area.shape\_owner\_get\_owner(other\_shape\_owner)

var local\_shape\_owner = shape\_find\_owner(local\_shape\_index) var
local\_shape\_node = shape\_owner\_get\_owner(local\_shape\_owner)

classref-item-separator

------------------------------------------------------------------------

classref-signal

**area\_shape\_exited**(area\_rid: `RID<class_RID>`, area:
`Area3D<class_Area3D>`, area\_shape\_index: `int<class_int>`,
local\_shape\_index: `int<class_int>`)
`🔗<class_Area3D_signal_area_shape_exited>`

Emitted when a `Shape3D<class_Shape3D>` of the received `area` exits a
shape of this area. Requires
`monitoring<class_Area3D_property_monitoring>` to be set to `true`.

See also `area_shape_entered<class_Area3D_signal_area_shape_entered>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**body\_entered**(body: `Node3D<class_Node3D>`)
`🔗<class_Area3D_signal_body_entered>`

Emitted when the received `body` enters this area. `body` can be a
`PhysicsBody3D<class_PhysicsBody3D>` or a `GridMap<class_GridMap>`.
`GridMap<class_GridMap>`s are detected if their
`MeshLibrary<class_MeshLibrary>` has collision shapes configured.
Requires `monitoring<class_Area3D_property_monitoring>` to be set to
`true`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**body\_exited**(body: `Node3D<class_Node3D>`)
`🔗<class_Area3D_signal_body_exited>`

Emitted when the received `body` exits this area. `body` can be a
`PhysicsBody3D<class_PhysicsBody3D>` or a `GridMap<class_GridMap>`.
`GridMap<class_GridMap>`s are detected if their
`MeshLibrary<class_MeshLibrary>` has collision shapes configured.
Requires `monitoring<class_Area3D_property_monitoring>` to be set to
`true`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**body\_shape\_entered**(body\_rid: `RID<class_RID>`, body:
`Node3D<class_Node3D>`, body\_shape\_index: `int<class_int>`,
local\_shape\_index: `int<class_int>`)
`🔗<class_Area3D_signal_body_shape_entered>`

Emitted when a `Shape3D<class_Shape3D>` of the received `body` enters a
shape of this area. `body` can be a `PhysicsBody3D<class_PhysicsBody3D>`
or a `GridMap<class_GridMap>`. `GridMap<class_GridMap>`s are detected if
their `MeshLibrary<class_MeshLibrary>` has collision shapes configured.
Requires `monitoring<class_Area3D_property_monitoring>` to be set to
`true`.

`local_shape_index` and `body_shape_index` contain indices of the
interacting shapes from this area and the interacting body,
respectively. `body_rid` contains the `RID<class_RID>` of the body.
These values can be used with the
`PhysicsServer3D<class_PhysicsServer3D>`.

\*\*Example of getting the\*\*
`CollisionShape3D<class_CollisionShape3D>` **node from the shape
index:**

gdscript

var body\_shape\_owner = body.shape\_find\_owner(body\_shape\_index) var
body\_shape\_node = body.shape\_owner\_get\_owner(body\_shape\_owner)

var local\_shape\_owner = shape\_find\_owner(local\_shape\_index) var
local\_shape\_node = shape\_owner\_get\_owner(local\_shape\_owner)

classref-item-separator

------------------------------------------------------------------------

classref-signal

**body\_shape\_exited**(body\_rid: `RID<class_RID>`, body:
`Node3D<class_Node3D>`, body\_shape\_index: `int<class_int>`,
local\_shape\_index: `int<class_int>`)
`🔗<class_Area3D_signal_body_shape_exited>`

Emitted when a `Shape3D<class_Shape3D>` of the received `body` exits a
shape of this area. `body` can be a `PhysicsBody3D<class_PhysicsBody3D>`
or a `GridMap<class_GridMap>`. `GridMap<class_GridMap>`s are detected if
their `MeshLibrary<class_MeshLibrary>` has collision shapes configured.
Requires `monitoring<class_Area3D_property_monitoring>` to be set to
`true`.

See also `body_shape_entered<class_Area3D_signal_body_shape_entered>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **SpaceOverride**: `🔗<enum_Area3D_SpaceOverride>`

classref-enumeration-constant

`SpaceOverride<enum_Area3D_SpaceOverride>` **SPACE\_OVERRIDE\_DISABLED**
= `0`

This area does not affect gravity/damping.

classref-enumeration-constant

`SpaceOverride<enum_Area3D_SpaceOverride>` **SPACE\_OVERRIDE\_COMBINE**
= `1`

This area adds its gravity/damping values to whatever has been
calculated so far (in `priority<class_Area3D_property_priority>` order).

classref-enumeration-constant

`SpaceOverride<enum_Area3D_SpaceOverride>`
**SPACE\_OVERRIDE\_COMBINE\_REPLACE** = `2`

This area adds its gravity/damping values to whatever has been
calculated so far (in `priority<class_Area3D_property_priority>` order),
ignoring any lower priority areas.

classref-enumeration-constant

`SpaceOverride<enum_Area3D_SpaceOverride>` **SPACE\_OVERRIDE\_REPLACE**
= `3`

This area replaces any gravity/damping, even the defaults, ignoring any
lower priority areas.

classref-enumeration-constant

`SpaceOverride<enum_Area3D_SpaceOverride>`
**SPACE\_OVERRIDE\_REPLACE\_COMBINE** = `4`

This area replaces any gravity/damping calculated so far (in
`priority<class_Area3D_property_priority>` order), but keeps calculating
the rest of the areas.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **angular\_damp** = `0.1`
`🔗<class_Area3D_property_angular_damp>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_damp**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_angular\_damp**()

The rate at which objects stop spinning in this area. Represents the
angular velocity lost per second.

See
`ProjectSettings.physics/3d/default_angular_damp<class_ProjectSettings_property_physics/3d/default_angular_damp>`
for more details about damping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SpaceOverride<enum_Area3D_SpaceOverride>`
**angular\_damp\_space\_override** = `0`
`🔗<class_Area3D_property_angular_damp_space_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_angular\_damp\_space\_override\_mode**(value:
    `SpaceOverride<enum_Area3D_SpaceOverride>`)
-   `SpaceOverride<enum_Area3D_SpaceOverride>`
    **get\_angular\_damp\_space\_override\_mode**()

Override mode for angular damping calculations within this area. See
`SpaceOverride<enum_Area3D_SpaceOverride>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **audio\_bus\_name** = `&"Master"`
`🔗<class_Area3D_property_audio_bus_name>`

classref-property-setget

-   `void (No return value.)` **set\_audio\_bus\_name**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_audio\_bus\_name**()

The name of the area's audio bus.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **audio\_bus\_override** = `false`
`🔗<class_Area3D_property_audio_bus_override>`

classref-property-setget

-   `void (No return value.)` **set\_audio\_bus\_override**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_overriding\_audio\_bus**()

If `true`, the area's audio bus overrides the default audio bus.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **gravity** = `9.8`
`🔗<class_Area3D_property_gravity>`

classref-property-setget

-   `void (No return value.)` **set\_gravity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_gravity**()

The area's gravity intensity (in meters per second squared). This value
multiplies the gravity direction. This is useful to alter the force of
gravity without altering its direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **gravity\_direction** = `Vector3(0, -1, 0)`
`🔗<class_Area3D_property_gravity_direction>`

classref-property-setget

-   `void (No return value.)` **set\_gravity\_direction**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_gravity\_direction**()

The area's gravity vector (not normalized).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gravity\_point** = `false`
`🔗<class_Area3D_property_gravity_point>`

classref-property-setget

-   `void (No return value.)` **set\_gravity\_is\_point**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_gravity\_a\_point**()

If `true`, gravity is calculated from a point (set via
`gravity_point_center<class_Area3D_property_gravity_point_center>`). See
also
`gravity_space_override<class_Area3D_property_gravity_space_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **gravity\_point\_center** =
`Vector3(0, -1, 0)` `🔗<class_Area3D_property_gravity_point_center>`

classref-property-setget

-   `void (No return value.)` **set\_gravity\_point\_center**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_gravity\_point\_center**()

If gravity is a point (see
`gravity_point<class_Area3D_property_gravity_point>`), this will be the
point of attraction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **gravity\_point\_unit\_distance** = `0.0`
`🔗<class_Area3D_property_gravity_point_unit_distance>`

classref-property-setget

-   `void (No return value.)`
    **set\_gravity\_point\_unit\_distance**(value: `float<class_float>`)
-   `float<class_float>` **get\_gravity\_point\_unit\_distance**()

The distance at which the gravity strength is equal to
`gravity<class_Area3D_property_gravity>`. For example, on a planet 100
meters in radius with a surface gravity of 4.0 m/s², set the
`gravity<class_Area3D_property_gravity>` to 4.0 and the unit distance to
100.0. The gravity will have falloff according to the inverse square
law, so in the example, at 200 meters from the center the gravity will
be 1.0 m/s² (twice the distance, 1/4th the gravity), at 50 meters it
will be 16.0 m/s² (half the distance, 4x the gravity), and so on.

The above is true only when the unit distance is a positive number. When
this is set to 0.0, the gravity will be constant regardless of distance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SpaceOverride<enum_Area3D_SpaceOverride>` **gravity\_space\_override**
= `0` `🔗<class_Area3D_property_gravity_space_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_gravity\_space\_override\_mode**(value:
    `SpaceOverride<enum_Area3D_SpaceOverride>`)
-   `SpaceOverride<enum_Area3D_SpaceOverride>`
    **get\_gravity\_space\_override\_mode**()

Override mode for gravity calculations within this area. See
`SpaceOverride<enum_Area3D_SpaceOverride>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_damp** = `0.1`
`🔗<class_Area3D_property_linear_damp>`

classref-property-setget

-   `void (No return value.)` **set\_linear\_damp**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_linear\_damp**()

The rate at which objects stop moving in this area. Represents the
linear velocity lost per second.

See
`ProjectSettings.physics/3d/default_linear_damp<class_ProjectSettings_property_physics/3d/default_linear_damp>`
for more details about damping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SpaceOverride<enum_Area3D_SpaceOverride>`
**linear\_damp\_space\_override** = `0`
`🔗<class_Area3D_property_linear_damp_space_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_linear\_damp\_space\_override\_mode**(value:
    `SpaceOverride<enum_Area3D_SpaceOverride>`)
-   `SpaceOverride<enum_Area3D_SpaceOverride>`
    **get\_linear\_damp\_space\_override\_mode**()

Override mode for linear damping calculations within this area. See
`SpaceOverride<enum_Area3D_SpaceOverride>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **monitorable** = `true`
`🔗<class_Area3D_property_monitorable>`

classref-property-setget

-   `void (No return value.)` **set\_monitorable**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_monitorable**()

If `true`, other monitoring areas can detect this area.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **monitoring** = `true`
`🔗<class_Area3D_property_monitoring>`

classref-property-setget

-   `void (No return value.)` **set\_monitoring**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_monitoring**()

If `true`, the area detects bodies or areas entering and exiting it.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **priority** = `0` `🔗<class_Area3D_property_priority>`

classref-property-setget

-   `void (No return value.)` **set\_priority**(value: `int<class_int>`)
-   `int<class_int>` **get\_priority**()

The area's priority. Higher priority areas are processed first. The
`World3D<class_World3D>`'s physics is always processed last, after all
areas.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **reverb\_bus\_amount** = `0.0`
`🔗<class_Area3D_property_reverb_bus_amount>`

classref-property-setget

-   `void (No return value.)` **set\_reverb\_amount**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_reverb\_amount**()

The degree to which this area applies reverb to its associated audio.
Ranges from `0` to `1` with `0.1` precision.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **reverb\_bus\_enabled** = `false`
`🔗<class_Area3D_property_reverb_bus_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_use\_reverb\_bus**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_reverb\_bus**()

If `true`, the area applies reverb to its associated audio.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **reverb\_bus\_name** = `&"Master"`
`🔗<class_Area3D_property_reverb_bus_name>`

classref-property-setget

-   `void (No return value.)` **set\_reverb\_bus\_name**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_reverb\_bus\_name**()

The name of the reverb bus to use for this area's associated audio.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **reverb\_bus\_uniformity** = `0.0`
`🔗<class_Area3D_property_reverb_bus_uniformity>`

classref-property-setget

-   `void (No return value.)` **set\_reverb\_uniformity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_reverb\_uniformity**()

The degree to which this area's reverb is a uniform effect. Ranges from
`0` to `1` with `0.1` precision.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **wind\_attenuation\_factor** = `0.0`
`🔗<class_Area3D_property_wind_attenuation_factor>`

classref-property-setget

-   `void (No return value.)` **set\_wind\_attenuation\_factor**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_wind\_attenuation\_factor**()

The exponential rate at which wind force decreases with distance from
its origin.

\*\*Note:\*\* This wind force only applies to
`SoftBody3D<class_SoftBody3D>` nodes. Other physics bodies are currently
not affected by wind.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **wind\_force\_magnitude** = `0.0`
`🔗<class_Area3D_property_wind_force_magnitude>`

classref-property-setget

-   `void (No return value.)` **set\_wind\_force\_magnitude**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_wind\_force\_magnitude**()

The magnitude of area-specific wind force.

\*\*Note:\*\* This wind force only applies to
`SoftBody3D<class_SoftBody3D>` nodes. Other physics bodies are currently
not affected by wind.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **wind\_source\_path** = `NodePath("")`
`🔗<class_Area3D_property_wind_source_path>`

classref-property-setget

-   `void (No return value.)` **set\_wind\_source\_path**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_wind\_source\_path**()

The `Node3D<class_Node3D>` which is used to specify the direction and
origin of an area-specific wind force. The direction is opposite to the
z-axis of the `Node3D<class_Node3D>`'s local transform, and its origin
is the origin of the `Node3D<class_Node3D>`'s local transform.

\*\*Note:\*\* This wind force only applies to
`SoftBody3D<class_SoftBody3D>` nodes. Other physics bodies are currently
not affected by wind.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Array<class_Array>`\[`Area3D<class_Area3D>`\]
**get\_overlapping\_areas**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area3D_method_get_overlapping_areas>`

Returns a list of intersecting **Area3D**s. The overlapping area's
`CollisionObject3D.collision_layer<class_CollisionObject3D_property_collision_layer>`
must be part of this area's
`CollisionObject3D.collision_mask<class_CollisionObject3D_property_collision_mask>`
in order to be detected.

For performance reasons (collisions are all processed at the same time)
this list is modified once during the physics step, not immediately
after objects are moved. Consider using signals instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Node3D<class_Node3D>`\]
**get\_overlapping\_bodies**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area3D_method_get_overlapping_bodies>`

Returns a list of intersecting `PhysicsBody3D<class_PhysicsBody3D>`s and
`GridMap<class_GridMap>`s. The overlapping body's
`CollisionObject3D.collision_layer<class_CollisionObject3D_property_collision_layer>`
must be part of this area's
`CollisionObject3D.collision_mask<class_CollisionObject3D_property_collision_mask>`
in order to be detected.

For performance reasons (collisions are all processed at the same time)
this list is modified once during the physics step, not immediately
after objects are moved. Consider using signals instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_overlapping\_areas**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area3D_method_has_overlapping_areas>`

Returns `true` if intersecting any **Area3D**s, otherwise returns
`false`. The overlapping area's
`CollisionObject3D.collision_layer<class_CollisionObject3D_property_collision_layer>`
must be part of this area's
`CollisionObject3D.collision_mask<class_CollisionObject3D_property_collision_mask>`
in order to be detected.

For performance reasons (collisions are all processed at the same time)
the list of overlapping areas is modified once during the physics step,
not immediately after objects are moved. Consider using signals instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_overlapping\_bodies**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area3D_method_has_overlapping_bodies>`

Returns `true` if intersecting any `PhysicsBody3D<class_PhysicsBody3D>`s
or `GridMap<class_GridMap>`s, otherwise returns `false`. The overlapping
body's
`CollisionObject3D.collision_layer<class_CollisionObject3D_property_collision_layer>`
must be part of this area's
`CollisionObject3D.collision_mask<class_CollisionObject3D_property_collision_mask>`
in order to be detected.

For performance reasons (collisions are all processed at the same time)
the list of overlapping bodies is modified once during the physics step,
not immediately after objects are moved. Consider using signals instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **overlaps\_area**(area: `Node<class_Node>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area3D_method_overlaps_area>`

Returns `true` if the given **Area3D** intersects or overlaps this
**Area3D**, `false` otherwise.

\*\*Note:\*\* The result of this test is not immediate after moving
objects. For performance, list of overlaps is updated once per frame and
before the physics step. Consider using signals instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **overlaps\_body**(body: `Node<class_Node>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area3D_method_overlaps_body>`

Returns `true` if the given physics body intersects or overlaps this
**Area3D**, `false` otherwise.

\*\*Note:\*\* The result of this test is not immediate after moving
objects. For performance, list of overlaps is updated once per frame and
before the physics step. Consider using signals instead.

The `body` argument can either be a `PhysicsBody3D<class_PhysicsBody3D>`
or a `GridMap<class_GridMap>` instance. While GridMaps are not physics
body themselves, they register their tiles with collision shapes as a
virtual physics body.
