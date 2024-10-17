github\_url  
hide

# StaticBody3D

**Inherits:** `PhysicsBody3D<class_PhysicsBody3D>` **&lt;**
`CollisionObject3D<class_CollisionObject3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `AnimatableBody3D<class_AnimatableBody3D>`

A 3D physics body that can't be moved by external forces. When moved
manually, it doesn't affect other bodies in its path.

classref-introduction-group

## Description

A static 3D physics body. It can't be moved by external forces or
contacts, but can be moved manually by other means such as code,
`AnimationMixer<class_AnimationMixer>`s (with
`AnimationMixer.callback_mode_process<class_AnimationMixer_property_callback_mode_process>`
set to
`AnimationMixer.ANIMATION_CALLBACK_MODE_PROCESS_PHYSICS<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_PROCESS_PHYSICS>`),
and `RemoteTransform3D<class_RemoteTransform3D>`.

When **StaticBody3D** is moved, it is teleported to its new position
without affecting other physics bodies in its path. If this is not
desired, use `AnimatableBody3D<class_AnimatableBody3D>` instead.

\*\*StaticBody3D\*\* is useful for completely static objects like floors
and walls, as well as moving surfaces like conveyor belts and circular
revolving platforms (by using
`constant_linear_velocity<class_StaticBody3D_property_constant_linear_velocity>`
and
`constant_angular_velocity<class_StaticBody3D_property_constant_angular_velocity>`).

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

`Vector3<class_Vector3>` **constant\_angular\_velocity** =
`Vector3(0, 0, 0)`
`🔗<class_StaticBody3D_property_constant_angular_velocity>`

classref-property-setget

-   `void (No return value.)`
    **set\_constant\_angular\_velocity**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_constant\_angular\_velocity**()

The body's constant angular velocity. This does not rotate the body, but
affects touching bodies, as if it were rotating.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **constant\_linear\_velocity** =
`Vector3(0, 0, 0)`
`🔗<class_StaticBody3D_property_constant_linear_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_constant\_linear\_velocity**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_constant\_linear\_velocity**()

The body's constant linear velocity. This does not move the body, but
affects touching bodies, as if it were moving.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PhysicsMaterial<class_PhysicsMaterial>` **physics\_material\_override**
`🔗<class_StaticBody3D_property_physics_material_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_physics\_material\_override**(value:
    `PhysicsMaterial<class_PhysicsMaterial>`)
-   `PhysicsMaterial<class_PhysicsMaterial>`
    **get\_physics\_material\_override**()

The physics material override for the body.

If a material is assigned to this property, it will be used instead of
any other physics material, such as an inherited one.
