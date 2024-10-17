github\_url  
hide

# AnimatableBody3D

**Inherits:** `StaticBody3D<class_StaticBody3D>` **&lt;**
`PhysicsBody3D<class_PhysicsBody3D>` **&lt;**
`CollisionObject3D<class_CollisionObject3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A 3D physics body that can't be moved by external forces. When moved
manually, it affects other bodies in its path.

classref-introduction-group

## Description

An animatable 3D physics body. It can't be moved by external forces or
contacts, but can be moved manually by other means such as code,
`AnimationMixer<class_AnimationMixer>`s (with
`AnimationMixer.callback_mode_process<class_AnimationMixer_property_callback_mode_process>`
set to
`AnimationMixer.ANIMATION_CALLBACK_MODE_PROCESS_PHYSICS<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_PROCESS_PHYSICS>`),
and `RemoteTransform3D<class_RemoteTransform3D>`.

When **AnimatableBody3D** is moved, its linear and angular velocity are
estimated and used to affect other physics bodies in its path. This
makes it useful for moving platforms, doors, and other moving objects.

classref-introduction-group

## Tutorials

-   [3D Physics Tests
    Demo](https://godotengine.org/asset-library/asset/2747)
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)
-   [3D Voxel Demo](https://godotengine.org/asset-library/asset/2755)

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **sync\_to\_physics** = `true`
`🔗<class_AnimatableBody3D_property_sync_to_physics>`

classref-property-setget

-   `void (No return value.)` **set\_sync\_to\_physics**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_sync\_to\_physics\_enabled**()

If `true`, the body's movement will be synchronized to the physics
frame. This is useful when animating movement via
`AnimationPlayer<class_AnimationPlayer>`, for example on moving
platforms. Do **not** use together with
`PhysicsBody3D.move_and_collide<class_PhysicsBody3D_method_move_and_collide>`.
