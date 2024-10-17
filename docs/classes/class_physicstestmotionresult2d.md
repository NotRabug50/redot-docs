github\_url  
hide

# PhysicsTestMotionResult2D

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Describes the motion and collision result from
`PhysicsServer2D.body_test_motion<class_PhysicsServer2D_method_body_test_motion>`.

classref-introduction-group

## Description

Describes the motion and collision result from
`PhysicsServer2D.body_test_motion<class_PhysicsServer2D_method_body_test_motion>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Object<class_Object>` **get\_collider**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_collider>`

Returns the colliding body's attached `Object<class_Object>`, if a
collision occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_collider\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_collider_id>`

Returns the unique instance ID of the colliding body's attached
`Object<class_Object>`, if a collision occurred. See
`Object.get_instance_id<class_Object_method_get_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_collider\_rid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_collider_rid>`

Returns the colliding body's `RID<class_RID>` used by the
`PhysicsServer2D<class_PhysicsServer2D>`, if a collision occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_collider\_shape**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_collider_shape>`

Returns the colliding body's shape index, if a collision occurred. See
`CollisionObject2D<class_CollisionObject2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_collider\_velocity**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_collider_velocity>`

Returns the colliding body's velocity, if a collision occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_collision\_depth**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_collision_depth>`

Returns the length of overlap along the collision normal, if a collision
occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_collision\_local\_shape**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_collision_local_shape>`

Returns the moving object's colliding shape, if a collision occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_collision\_normal**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_collision_normal>`

Returns the colliding body's shape's normal at the point of collision,
if a collision occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_collision\_point**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_collision_point>`

Returns the point of collision in global coordinates, if a collision
occurred.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_collision\_safe\_fraction**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_collision_safe_fraction>`

Returns the maximum fraction of the motion that can occur without a
collision, between `0` and `1`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_collision\_unsafe\_fraction**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_collision_unsafe_fraction>`

Returns the minimum fraction of the motion needed to collide, if a
collision occurred, between `0` and `1`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_remainder**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_remainder>`

Returns the moving object's remaining movement vector.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_travel**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsTestMotionResult2D_method_get_travel>`

Returns the moving object's travel before collision.
