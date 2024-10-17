github\_url  
hide

# StaticBody2D

**Inherits:** `PhysicsBody2D<class_PhysicsBody2D>` **&lt;**
`CollisionObject2D<class_CollisionObject2D>` **&lt;**
`Node2D<class_Node2D>` **&lt;** `CanvasItem<class_CanvasItem>` **&lt;**
`Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `AnimatableBody2D<class_AnimatableBody2D>`

A 2D physics body that can't be moved by external forces. When moved
manually, it doesn't affect other bodies in its path.

classref-introduction-group

## Description

A static 2D physics body. It can't be moved by external forces or
contacts, but can be moved manually by other means such as code,
`AnimationMixer<class_AnimationMixer>`s (with
`AnimationMixer.callback_mode_process<class_AnimationMixer_property_callback_mode_process>`
set to
`AnimationMixer.ANIMATION_CALLBACK_MODE_PROCESS_PHYSICS<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_PROCESS_PHYSICS>`),
and `RemoteTransform2D<class_RemoteTransform2D>`.

When **StaticBody2D** is moved, it is teleported to its new position
without affecting other physics bodies in its path. If this is not
desired, use `AnimatableBody2D<class_AnimatableBody2D>` instead.

\*\*StaticBody2D\*\* is useful for completely static objects like floors
and walls, as well as moving surfaces like conveyor belts and circular
revolving platforms (by using
`constant_linear_velocity<class_StaticBody2D_property_constant_linear_velocity>`
and
`constant_angular_velocity<class_StaticBody2D_property_constant_angular_velocity>`).

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **constant\_angular\_velocity** = `0.0`
`🔗<class_StaticBody2D_property_constant_angular_velocity>`

classref-property-setget

-   `void (No return value.)`
    **set\_constant\_angular\_velocity**(value: `float<class_float>`)
-   `float<class_float>` **get\_constant\_angular\_velocity**()

The body's constant angular velocity. This does not rotate the body, but
affects touching bodies, as if it were rotating.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **constant\_linear\_velocity** =
`Vector2(0, 0)`
`🔗<class_StaticBody2D_property_constant_linear_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_constant\_linear\_velocity**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_constant\_linear\_velocity**()

The body's constant linear velocity. This does not move the body, but
affects touching bodies, as if it were moving.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PhysicsMaterial<class_PhysicsMaterial>` **physics\_material\_override**
`🔗<class_StaticBody2D_property_physics_material_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_physics\_material\_override**(value:
    `PhysicsMaterial<class_PhysicsMaterial>`)
-   `PhysicsMaterial<class_PhysicsMaterial>`
    **get\_physics\_material\_override**()

The physics material override for the body.

If a material is assigned to this property, it will be used instead of
any other physics material, such as an inherited one.
