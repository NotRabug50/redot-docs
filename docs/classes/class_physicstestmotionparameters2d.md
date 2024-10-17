github\_url  
hide

# PhysicsTestMotionParameters2D

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides parameters for
`PhysicsServer2D.body_test_motion<class_PhysicsServer2D_method_body_test_motion>`.

classref-introduction-group

## Description

By changing various properties of this object, such as the motion, you
can configure the parameters for
`PhysicsServer2D.body_test_motion<class_PhysicsServer2D_method_body_test_motion>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **collide\_separation\_ray** = `false`
`🔗<class_PhysicsTestMotionParameters2D_property_collide_separation_ray>`

classref-property-setget

-   `void (No return value.)`
    **set\_collide\_separation\_ray\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_collide\_separation\_ray\_enabled**()

If set to `true`, shapes of type
`PhysicsServer2D.SHAPE_SEPARATION_RAY<class_PhysicsServer2D_constant_SHAPE_SEPARATION_RAY>`
are used to detect collisions and can stop the motion. Can be useful
when snapping to the ground.

If set to `false`, shapes of type
`PhysicsServer2D.SHAPE_SEPARATION_RAY<class_PhysicsServer2D_constant_SHAPE_SEPARATION_RAY>`
are only used for separation when overlapping with other bodies. That's
the main use for separation ray shapes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`RID<class_RID>`\] **exclude\_bodies** = `[]`
`🔗<class_PhysicsTestMotionParameters2D_property_exclude_bodies>`

classref-property-setget

-   `void (No return value.)` **set\_exclude\_bodies**(value:
    `Array<class_Array>`\[`RID<class_RID>`\])
-   `Array<class_Array>`\[`RID<class_RID>`\] **get\_exclude\_bodies**()

Optional array of body `RID<class_RID>` to exclude from collision. Use
`CollisionObject2D.get_rid<class_CollisionObject2D_method_get_rid>` to
get the `RID<class_RID>` associated with a
`CollisionObject2D<class_CollisionObject2D>`-derived node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`int<class_int>`\] **exclude\_objects** = `[]`
`🔗<class_PhysicsTestMotionParameters2D_property_exclude_objects>`

classref-property-setget

-   `void (No return value.)` **set\_exclude\_objects**(value:
    `Array<class_Array>`\[`int<class_int>`\])
-   `Array<class_Array>`\[`int<class_int>`\] **get\_exclude\_objects**()

Optional array of object unique instance ID to exclude from collision.
See `Object.get_instance_id<class_Object_method_get_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform2D<class_Transform2D>` **from** =
`Transform2D(1, 0, 0, 1, 0, 0)`
`🔗<class_PhysicsTestMotionParameters2D_property_from>`

classref-property-setget

-   `void (No return value.)` **set\_from**(value:
    `Transform2D<class_Transform2D>`)
-   `Transform2D<class_Transform2D>` **get\_from**()

Transform in global space where the motion should start. Usually set to
`Node2D.global_transform<class_Node2D_property_global_transform>` for
the current body's transform.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **margin** = `0.08`
`🔗<class_PhysicsTestMotionParameters2D_property_margin>`

classref-property-setget

-   `void (No return value.)` **set\_margin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_margin**()

Increases the size of the shapes involved in the collision detection.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **motion** = `Vector2(0, 0)`
`🔗<class_PhysicsTestMotionParameters2D_property_motion>`

classref-property-setget

-   `void (No return value.)` **set\_motion**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_motion**()

Motion vector to define the length and direction of the motion to test.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **recovery\_as\_collision** = `false`
`🔗<class_PhysicsTestMotionParameters2D_property_recovery_as_collision>`

classref-property-setget

-   `void (No return value.)`
    **set\_recovery\_as\_collision\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_recovery\_as\_collision\_enabled**()

If set to `true`, any depenetration from the recovery phase is reported
as a collision; this is used e.g. by
`CharacterBody2D<class_CharacterBody2D>` for improving floor detection
during floor snapping.

If set to `false`, only collisions resulting from the motion are
reported, which is generally the desired behavior.
