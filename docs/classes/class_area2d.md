github\_url  
hide

# Area2D

**Inherits:** `CollisionObject2D<class_CollisionObject2D>` **&lt;**
`Node2D<class_Node2D>` **&lt;** `CanvasItem<class_CanvasItem>` **&lt;**
`Node<class_Node>` **&lt;** `Object<class_Object>`

A region of 2D space that detects other
`CollisionObject2D<class_CollisionObject2D>`s entering or exiting it.

classref-introduction-group

## Description

**Area2D** is a region of 2D space defined by one or multiple
`CollisionShape2D<class_CollisionShape2D>` or
`CollisionPolygon2D<class_CollisionPolygon2D>` child nodes. It detects
when other `CollisionObject2D<class_CollisionObject2D>`s enter or exit
it, and it also keeps track of which collision objects haven't exited it
yet (i.e. which one are overlapping it).

This node can also locally alter or override physics parameters
(gravity, damping) and route audio to custom audio buses.

\*\*Note:\*\* Areas and bodies created with
`PhysicsServer2D<class_PhysicsServer2D>` might not interact as expected
with **Area2D**s, and might not emit signals or track objects correctly.

classref-introduction-group

## Tutorials

-   `Using Area2D <../tutorials/physics/using_area_2d>`
-   [2D Dodge The Creeps
    Demo](https://godotengine.org/asset-library/asset/2712)
-   [2D Pong Demo](https://godotengine.org/asset-library/asset/2728)
-   [2D Platformer
    Demo](https://godotengine.org/asset-library/asset/2727)

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

**area\_entered**(area: `Area2D<class_Area2D>`)
`🔗<class_Area2D_signal_area_entered>`

Emitted when the received `area` enters this area. Requires
`monitoring<class_Area2D_property_monitoring>` to be set to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**area\_exited**(area: `Area2D<class_Area2D>`)
`🔗<class_Area2D_signal_area_exited>`

Emitted when the received `area` exits this area. Requires
`monitoring<class_Area2D_property_monitoring>` to be set to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**area\_shape\_entered**(area\_rid: `RID<class_RID>`, area:
`Area2D<class_Area2D>`, area\_shape\_index: `int<class_int>`,
local\_shape\_index: `int<class_int>`)
`🔗<class_Area2D_signal_area_shape_entered>`

Emitted when a `Shape2D<class_Shape2D>` of the received `area` enters a
shape of this area. Requires
`monitoring<class_Area2D_property_monitoring>` to be set to `true`.

`local_shape_index` and `area_shape_index` contain indices of the
interacting shapes from this area and the other area, respectively.
`area_rid` contains the `RID<class_RID>` of the other area. These values
can be used with the `PhysicsServer2D<class_PhysicsServer2D>`.

\*\*Example of getting the\*\*
`CollisionShape2D<class_CollisionShape2D>` **node from the shape
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
`Area2D<class_Area2D>`, area\_shape\_index: `int<class_int>`,
local\_shape\_index: `int<class_int>`)
`🔗<class_Area2D_signal_area_shape_exited>`

Emitted when a `Shape2D<class_Shape2D>` of the received `area` exits a
shape of this area. Requires
`monitoring<class_Area2D_property_monitoring>` to be set to `true`.

See also `area_shape_entered<class_Area2D_signal_area_shape_entered>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**body\_entered**(body: `Node2D<class_Node2D>`)
`🔗<class_Area2D_signal_body_entered>`

Emitted when the received `body` enters this area. `body` can be a
`PhysicsBody2D<class_PhysicsBody2D>` or a `TileMap<class_TileMap>`.
`TileMap<class_TileMap>`s are detected if their `TileSet<class_TileSet>`
has collision shapes configured. Requires
`monitoring<class_Area2D_property_monitoring>` to be set to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**body\_exited**(body: `Node2D<class_Node2D>`)
`🔗<class_Area2D_signal_body_exited>`

Emitted when the received `body` exits this area. `body` can be a
`PhysicsBody2D<class_PhysicsBody2D>` or a `TileMap<class_TileMap>`.
`TileMap<class_TileMap>`s are detected if their `TileSet<class_TileSet>`
has collision shapes configured. Requires
`monitoring<class_Area2D_property_monitoring>` to be set to `true`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**body\_shape\_entered**(body\_rid: `RID<class_RID>`, body:
`Node2D<class_Node2D>`, body\_shape\_index: `int<class_int>`,
local\_shape\_index: `int<class_int>`)
`🔗<class_Area2D_signal_body_shape_entered>`

Emitted when a `Shape2D<class_Shape2D>` of the received `body` enters a
shape of this area. `body` can be a `PhysicsBody2D<class_PhysicsBody2D>`
or a `TileMap<class_TileMap>`. `TileMap<class_TileMap>`s are detected if
their `TileSet<class_TileSet>` has collision shapes configured. Requires
`monitoring<class_Area2D_property_monitoring>` to be set to `true`.

`local_shape_index` and `body_shape_index` contain indices of the
interacting shapes from this area and the interacting body,
respectively. `body_rid` contains the `RID<class_RID>` of the body.
These values can be used with the
`PhysicsServer2D<class_PhysicsServer2D>`.

\*\*Example of getting the\*\*
`CollisionShape2D<class_CollisionShape2D>` **node from the shape
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
`Node2D<class_Node2D>`, body\_shape\_index: `int<class_int>`,
local\_shape\_index: `int<class_int>`)
`🔗<class_Area2D_signal_body_shape_exited>`

Emitted when a `Shape2D<class_Shape2D>` of the received `body` exits a
shape of this area. `body` can be a `PhysicsBody2D<class_PhysicsBody2D>`
or a `TileMap<class_TileMap>`. `TileMap<class_TileMap>`s are detected if
their `TileSet<class_TileSet>` has collision shapes configured. Requires
`monitoring<class_Area2D_property_monitoring>` to be set to `true`.

See also `body_shape_entered<class_Area2D_signal_body_shape_entered>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **SpaceOverride**: `🔗<enum_Area2D_SpaceOverride>`

classref-enumeration-constant

`SpaceOverride<enum_Area2D_SpaceOverride>` **SPACE\_OVERRIDE\_DISABLED**
= `0`

This area does not affect gravity/damping.

classref-enumeration-constant

`SpaceOverride<enum_Area2D_SpaceOverride>` **SPACE\_OVERRIDE\_COMBINE**
= `1`

This area adds its gravity/damping values to whatever has been
calculated so far (in `priority<class_Area2D_property_priority>` order).

classref-enumeration-constant

`SpaceOverride<enum_Area2D_SpaceOverride>`
**SPACE\_OVERRIDE\_COMBINE\_REPLACE** = `2`

This area adds its gravity/damping values to whatever has been
calculated so far (in `priority<class_Area2D_property_priority>` order),
ignoring any lower priority areas.

classref-enumeration-constant

`SpaceOverride<enum_Area2D_SpaceOverride>` **SPACE\_OVERRIDE\_REPLACE**
= `3`

This area replaces any gravity/damping, even the defaults, ignoring any
lower priority areas.

classref-enumeration-constant

`SpaceOverride<enum_Area2D_SpaceOverride>`
**SPACE\_OVERRIDE\_REPLACE\_COMBINE** = `4`

This area replaces any gravity/damping calculated so far (in
`priority<class_Area2D_property_priority>` order), but keeps calculating
the rest of the areas.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **angular\_damp** = `1.0`
`🔗<class_Area2D_property_angular_damp>`

classref-property-setget

-   `void (No return value.)` **set\_angular\_damp**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_angular\_damp**()

The rate at which objects stop spinning in this area. Represents the
angular velocity lost per second.

See
`ProjectSettings.physics/2d/default_angular_damp<class_ProjectSettings_property_physics/2d/default_angular_damp>`
for more details about damping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SpaceOverride<enum_Area2D_SpaceOverride>`
**angular\_damp\_space\_override** = `0`
`🔗<class_Area2D_property_angular_damp_space_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_angular\_damp\_space\_override\_mode**(value:
    `SpaceOverride<enum_Area2D_SpaceOverride>`)
-   `SpaceOverride<enum_Area2D_SpaceOverride>`
    **get\_angular\_damp\_space\_override\_mode**()

Override mode for angular damping calculations within this area. See
`SpaceOverride<enum_Area2D_SpaceOverride>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **audio\_bus\_name** = `&"Master"`
`🔗<class_Area2D_property_audio_bus_name>`

classref-property-setget

-   `void (No return value.)` **set\_audio\_bus\_name**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_audio\_bus\_name**()

The name of the area's audio bus.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **audio\_bus\_override** = `false`
`🔗<class_Area2D_property_audio_bus_override>`

classref-property-setget

-   `void (No return value.)` **set\_audio\_bus\_override**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_overriding\_audio\_bus**()

If `true`, the area's audio bus overrides the default audio bus.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **gravity** = `980.0`
`🔗<class_Area2D_property_gravity>`

classref-property-setget

-   `void (No return value.)` **set\_gravity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_gravity**()

The area's gravity intensity (in pixels per second squared). This value
multiplies the gravity direction. This is useful to alter the force of
gravity without altering its direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **gravity\_direction** = `Vector2(0, 1)`
`🔗<class_Area2D_property_gravity_direction>`

classref-property-setget

-   `void (No return value.)` **set\_gravity\_direction**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_gravity\_direction**()

The area's gravity vector (not normalized).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **gravity\_point** = `false`
`🔗<class_Area2D_property_gravity_point>`

classref-property-setget

-   `void (No return value.)` **set\_gravity\_is\_point**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_gravity\_a\_point**()

If `true`, gravity is calculated from a point (set via
`gravity_point_center<class_Area2D_property_gravity_point_center>`). See
also
`gravity_space_override<class_Area2D_property_gravity_space_override>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **gravity\_point\_center** = `Vector2(0, 1)`
`🔗<class_Area2D_property_gravity_point_center>`

classref-property-setget

-   `void (No return value.)` **set\_gravity\_point\_center**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_gravity\_point\_center**()

If gravity is a point (see
`gravity_point<class_Area2D_property_gravity_point>`), this will be the
point of attraction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **gravity\_point\_unit\_distance** = `0.0`
`🔗<class_Area2D_property_gravity_point_unit_distance>`

classref-property-setget

-   `void (No return value.)`
    **set\_gravity\_point\_unit\_distance**(value: `float<class_float>`)
-   `float<class_float>` **get\_gravity\_point\_unit\_distance**()

The distance at which the gravity strength is equal to
`gravity<class_Area2D_property_gravity>`. For example, on a planet 100
pixels in radius with a surface gravity of 4.0 px/s², set the
`gravity<class_Area2D_property_gravity>` to 4.0 and the unit distance to
100.0. The gravity will have falloff according to the inverse square
law, so in the example, at 200 pixels from the center the gravity will
be 1.0 px/s² (twice the distance, 1/4th the gravity), at 50 pixels it
will be 16.0 px/s² (half the distance, 4x the gravity), and so on.

The above is true only when the unit distance is a positive number. When
this is set to 0.0, the gravity will be constant regardless of distance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SpaceOverride<enum_Area2D_SpaceOverride>` **gravity\_space\_override**
= `0` `🔗<class_Area2D_property_gravity_space_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_gravity\_space\_override\_mode**(value:
    `SpaceOverride<enum_Area2D_SpaceOverride>`)
-   `SpaceOverride<enum_Area2D_SpaceOverride>`
    **get\_gravity\_space\_override\_mode**()

Override mode for gravity calculations within this area. See
`SpaceOverride<enum_Area2D_SpaceOverride>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_damp** = `0.1`
`🔗<class_Area2D_property_linear_damp>`

classref-property-setget

-   `void (No return value.)` **set\_linear\_damp**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_linear\_damp**()

The rate at which objects stop moving in this area. Represents the
linear velocity lost per second.

See
`ProjectSettings.physics/2d/default_linear_damp<class_ProjectSettings_property_physics/2d/default_linear_damp>`
for more details about damping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SpaceOverride<enum_Area2D_SpaceOverride>`
**linear\_damp\_space\_override** = `0`
`🔗<class_Area2D_property_linear_damp_space_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_linear\_damp\_space\_override\_mode**(value:
    `SpaceOverride<enum_Area2D_SpaceOverride>`)
-   `SpaceOverride<enum_Area2D_SpaceOverride>`
    **get\_linear\_damp\_space\_override\_mode**()

Override mode for linear damping calculations within this area. See
`SpaceOverride<enum_Area2D_SpaceOverride>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **monitorable** = `true`
`🔗<class_Area2D_property_monitorable>`

classref-property-setget

-   `void (No return value.)` **set\_monitorable**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_monitorable**()

If `true`, other monitoring areas can detect this area.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **monitoring** = `true`
`🔗<class_Area2D_property_monitoring>`

classref-property-setget

-   `void (No return value.)` **set\_monitoring**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_monitoring**()

If `true`, the area detects bodies or areas entering and exiting it.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **priority** = `0` `🔗<class_Area2D_property_priority>`

classref-property-setget

-   `void (No return value.)` **set\_priority**(value: `int<class_int>`)
-   `int<class_int>` **get\_priority**()

The area's priority. Higher priority areas are processed first. The
`World2D<class_World2D>`'s physics is always processed last, after all
areas.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Array<class_Array>`\[`Area2D<class_Area2D>`\]
**get\_overlapping\_areas**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area2D_method_get_overlapping_areas>`

Returns a list of intersecting **Area2D**s. The overlapping area's
`CollisionObject2D.collision_layer<class_CollisionObject2D_property_collision_layer>`
must be part of this area's
`CollisionObject2D.collision_mask<class_CollisionObject2D_property_collision_mask>`
in order to be detected.

For performance reasons (collisions are all processed at the same time)
this list is modified once during the physics step, not immediately
after objects are moved. Consider using signals instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Node2D<class_Node2D>`\]
**get\_overlapping\_bodies**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area2D_method_get_overlapping_bodies>`

Returns a list of intersecting `PhysicsBody2D<class_PhysicsBody2D>`s and
`TileMap<class_TileMap>`s. The overlapping body's
`CollisionObject2D.collision_layer<class_CollisionObject2D_property_collision_layer>`
must be part of this area's
`CollisionObject2D.collision_mask<class_CollisionObject2D_property_collision_mask>`
in order to be detected.

For performance reasons (collisions are all processed at the same time)
this list is modified once during the physics step, not immediately
after objects are moved. Consider using signals instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_overlapping\_areas**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area2D_method_has_overlapping_areas>`

Returns `true` if intersecting any **Area2D**s, otherwise returns
`false`. The overlapping area's
`CollisionObject2D.collision_layer<class_CollisionObject2D_property_collision_layer>`
must be part of this area's
`CollisionObject2D.collision_mask<class_CollisionObject2D_property_collision_mask>`
in order to be detected.

For performance reasons (collisions are all processed at the same time)
the list of overlapping areas is modified once during the physics step,
not immediately after objects are moved. Consider using signals instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_overlapping\_bodies**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area2D_method_has_overlapping_bodies>`

Returns `true` if intersecting any `PhysicsBody2D<class_PhysicsBody2D>`s
or `TileMap<class_TileMap>`s, otherwise returns `false`. The overlapping
body's
`CollisionObject2D.collision_layer<class_CollisionObject2D_property_collision_layer>`
must be part of this area's
`CollisionObject2D.collision_mask<class_CollisionObject2D_property_collision_mask>`
in order to be detected.

For performance reasons (collisions are all processed at the same time)
the list of overlapping bodies is modified once during the physics step,
not immediately after objects are moved. Consider using signals instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **overlaps\_area**(area: `Node<class_Node>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area2D_method_overlaps_area>`

Returns `true` if the given **Area2D** intersects or overlaps this
**Area2D**, `false` otherwise.

\*\*Note:\*\* The result of this test is not immediate after moving
objects. For performance, the list of overlaps is updated once per frame
and before the physics step. Consider using signals instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **overlaps\_body**(body: `Node<class_Node>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Area2D_method_overlaps_body>`

Returns `true` if the given physics body intersects or overlaps this
**Area2D**, `false` otherwise.

\*\*Note:\*\* The result of this test is not immediate after moving
objects. For performance, list of overlaps is updated once per frame and
before the physics step. Consider using signals instead.

The `body` argument can either be a `PhysicsBody2D<class_PhysicsBody2D>`
or a `TileMap<class_TileMap>` instance. While TileMaps are not physics
bodies themselves, they register their tiles with collision shapes as a
virtual physics body.
