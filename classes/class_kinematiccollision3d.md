github\_url  
hide

# KinematicCollision3D

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Holds collision data from the movement of a
`PhysicsBody3D<class_PhysicsBody3D>`.

classref-introduction-group

## Description

Holds collision data from the movement of a
`PhysicsBody3D<class_PhysicsBody3D>`, usually from
`PhysicsBody3D.move_and_collide<class_PhysicsBody3D_method_move_and_collide>`.
When a `PhysicsBody3D<class_PhysicsBody3D>` is moved, it stops if it
detects a collision with another body. If a collision is detected, a
**KinematicCollision3D** object is returned.

The collision data includes the colliding object, the remaining motion,
and the collision position. This data can be used to determine a custom
response to the collision.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_angle**(collision\_index: `int<class_int>` =
0, up\_direction: `Vector3<class_Vector3>` = Vector3(0, 1, 0))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_angle>`

Returns the collision angle according to `up_direction`, which is
`Vector3.UP<class_Vector3_constant_UP>` by default. This value is always
positive.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Object<class_Object>` **get\_collider**(collision\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_collider>`

Returns the colliding body's attached `Object<class_Object>` given a
collision index (the deepest collision by default).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_collider\_id**(collision\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_collider_id>`

Returns the unique instance ID of the colliding body's attached
`Object<class_Object>` given a collision index (the deepest collision by
default). See
`Object.get_instance_id<class_Object_method_get_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_collider\_rid**(collision\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_collider_rid>`

Returns the colliding body's `RID<class_RID>` used by the
`PhysicsServer3D<class_PhysicsServer3D>` given a collision index (the
deepest collision by default).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Object<class_Object>` **get\_collider\_shape**(collision\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_collider_shape>`

Returns the colliding body's shape given a collision index (the deepest
collision by default).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_collider\_shape\_index**(collision\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_collider_shape_index>`

Returns the colliding body's shape index given a collision index (the
deepest collision by default). See
`CollisionObject3D<class_CollisionObject3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_collider\_velocity**(collision\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_collider_velocity>`

Returns the colliding body's velocity given a collision index (the
deepest collision by default).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_collision\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_collision_count>`

Returns the number of detected collisions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_depth**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_depth>`

Returns the colliding body's length of overlap along the collision
normal.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Object<class_Object>` **get\_local\_shape**(collision\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_local_shape>`

Returns the moving object's colliding shape given a collision index (the
deepest collision by default).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_normal**(collision\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_normal>`

Returns the colliding body's shape's normal at the point of collision
given a collision index (the deepest collision by default).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_position**(collision\_index:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_position>`

Returns the point of collision in global coordinates given a collision
index (the deepest collision by default).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_remainder**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_remainder>`

Returns the moving object's remaining movement vector.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_travel**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_KinematicCollision3D_method_get_travel>`

Returns the moving object's travel before collision.
