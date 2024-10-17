github\_url  
hide

# PhysicsBody2D

**Inherits:** `CollisionObject2D<class_CollisionObject2D>` **&lt;**
`Node2D<class_Node2D>` **&lt;** `CanvasItem<class_CanvasItem>` **&lt;**
`Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `CharacterBody2D<class_CharacterBody2D>`,
`RigidBody2D<class_RigidBody2D>`, `StaticBody2D<class_StaticBody2D>`

Abstract base class for 2D game objects affected by physics.

classref-introduction-group

## Description

**PhysicsBody2D** is an abstract base class for 2D game objects affected
by physics. All 2D physics bodies inherit from it.

classref-introduction-group

## Tutorials

-   `Physics introduction <../tutorials/physics/physics_introduction>`

classref-reftable-group

## Properties

<table>
<tbody>
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

## Method Descriptions

classref-method

`void (No return value.)` **add\_collision\_exception\_with**(body:
`Node<class_Node>`)
`🔗<class_PhysicsBody2D_method_add_collision_exception_with>`

Adds a body to the list of bodies that this body can't collide with.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PhysicsBody2D<class_PhysicsBody2D>`\]
**get\_collision\_exceptions**()
`🔗<class_PhysicsBody2D_method_get_collision_exceptions>`

Returns an array of nodes that were added as collision exceptions for
this body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_gravity**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsBody2D_method_get_gravity>`

Returns the gravity vector computed from all sources that can affect the
body, including all gravity overrides from `Area2D<class_Area2D>` nodes
and the global world gravity.

classref-item-separator

------------------------------------------------------------------------

classref-method

`KinematicCollision2D<class_KinematicCollision2D>`
**move\_and\_collide**(motion: `Vector2<class_Vector2>`, test\_only:
`bool<class_bool>` = false, safe\_margin: `float<class_float>` = 0.08,
recovery\_as\_collision: `bool<class_bool>` = false)
`🔗<class_PhysicsBody2D_method_move_and_collide>`

Moves the body along the vector `motion`. In order to be frame rate
independent in
`Node._physics_process<class_Node_private_method__physics_process>` or
`Node._process<class_Node_private_method__process>`, `motion` should be
computed using `delta`.

Returns a `KinematicCollision2D<class_KinematicCollision2D>`, which
contains information about the collision when stopped, or when touching
another body along the motion.

If `test_only` is `true`, the body does not move but the would-be
collision information is given.

`safe_margin` is the extra margin used for collision recovery (see
`CharacterBody2D.safe_margin<class_CharacterBody2D_property_safe_margin>`
for more details).

If `recovery_as_collision` is `true`, any depenetration from the
recovery phase is also reported as a collision; this is used e.g. by
`CharacterBody2D<class_CharacterBody2D>` for improving floor detection
during floor snapping.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_collision\_exception\_with**(body:
`Node<class_Node>`)
`🔗<class_PhysicsBody2D_method_remove_collision_exception_with>`

Removes a body from the list of bodies that this body can't collide
with.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **test\_move**(from:
`Transform2D<class_Transform2D>`, motion: `Vector2<class_Vector2>`,
collision: `KinematicCollision2D<class_KinematicCollision2D>` = null,
safe\_margin: `float<class_float>` = 0.08, recovery\_as\_collision:
`bool<class_bool>` = false) `🔗<class_PhysicsBody2D_method_test_move>`

Checks for collisions without moving the body. In order to be frame rate
independent in
`Node._physics_process<class_Node_private_method__physics_process>` or
`Node._process<class_Node_private_method__process>`, `motion` should be
computed using `delta`.

Virtually sets the node's position, scale and rotation to that of the
given `Transform2D<class_Transform2D>`, then tries to move the body
along the vector `motion`. Returns `true` if a collision would stop the
body from moving along the whole path.

`collision` is an optional object of type
`KinematicCollision2D<class_KinematicCollision2D>`, which contains
additional information about the collision when stopped, or when
touching another body along the motion.

`safe_margin` is the extra margin used for collision recovery (see
`CharacterBody2D.safe_margin<class_CharacterBody2D_property_safe_margin>`
for more details).

If `recovery_as_collision` is `true`, any depenetration from the
recovery phase is also reported as a collision; this is useful for
checking whether the body would *touch* any other bodies.
