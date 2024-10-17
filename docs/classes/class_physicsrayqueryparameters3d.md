github\_url  
hide

# PhysicsRayQueryParameters3D

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides parameters for
`PhysicsDirectSpaceState3D.intersect_ray<class_PhysicsDirectSpaceState3D_method_intersect_ray>`.

classref-introduction-group

## Description

By changing various properties of this object, such as the ray position,
you can configure the parameters for
`PhysicsDirectSpaceState3D.intersect_ray<class_PhysicsDirectSpaceState3D_method_intersect_ray>`.

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
</tbody>
</table>

classref-reftable-group

## Methods

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

`bool<class_bool>` **collide\_with\_areas** = `false`
`🔗<class_PhysicsRayQueryParameters3D_property_collide_with_areas>`

classref-property-setget

-   `void (No return value.)` **set\_collide\_with\_areas**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_collide\_with\_areas\_enabled**()

If `true`, the query will take `Area3D<class_Area3D>`s into account.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **collide\_with\_bodies** = `true`
`🔗<class_PhysicsRayQueryParameters3D_property_collide_with_bodies>`

classref-property-setget

-   `void (No return value.)` **set\_collide\_with\_bodies**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_collide\_with\_bodies\_enabled**()

If `true`, the query will take `PhysicsBody3D<class_PhysicsBody3D>`s
into account.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **collision\_mask** = `4294967295`
`🔗<class_PhysicsRayQueryParameters3D_property_collision_mask>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_collision\_mask**()

The physics layers the query will detect (as a bitmask). By default, all
collision layers are detected. See [Collision layers and
masks](../tutorials/physics/physics_introduction.html#collision-layers-and-masks)
in the documentation for more information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`RID<class_RID>`\] **exclude** = `[]`
`🔗<class_PhysicsRayQueryParameters3D_property_exclude>`

classref-property-setget

-   `void (No return value.)` **set\_exclude**(value:
    `Array<class_Array>`\[`RID<class_RID>`\])
-   `Array<class_Array>`\[`RID<class_RID>`\] **get\_exclude**()

The list of object `RID<class_RID>`s that will be excluded from
collisions. Use
`CollisionObject3D.get_rid<class_CollisionObject3D_method_get_rid>` to
get the `RID<class_RID>` associated with a
`CollisionObject3D<class_CollisionObject3D>`-derived node.

\*\*Note:\*\* The returned array is copied and any changes to it will
not update the original property value. To update the value you need to
modify the returned array, and then assign it to the property again.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **from** = `Vector3(0, 0, 0)`
`🔗<class_PhysicsRayQueryParameters3D_property_from>`

classref-property-setget

-   `void (No return value.)` **set\_from**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_from**()

The starting point of the ray being queried for, in global coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **hit\_back\_faces** = `true`
`🔗<class_PhysicsRayQueryParameters3D_property_hit_back_faces>`

classref-property-setget

-   `void (No return value.)` **set\_hit\_back\_faces**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_hit\_back\_faces\_enabled**()

If `true`, the query will hit back faces with concave polygon shapes
with back face enabled or heightmap shapes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **hit\_from\_inside** = `false`
`🔗<class_PhysicsRayQueryParameters3D_property_hit_from_inside>`

classref-property-setget

-   `void (No return value.)` **set\_hit\_from\_inside**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_hit\_from\_inside\_enabled**()

If `true`, the query will detect a hit when starting inside shapes. In
this case the collision normal will be `Vector3(0, 0, 0)`. Does not
affect concave polygon shapes or heightmap shapes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **to** = `Vector3(0, 0, 0)`
`🔗<class_PhysicsRayQueryParameters3D_property_to>`

classref-property-setget

-   `void (No return value.)` **set\_to**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_to**()

The ending point of the ray being queried for, in global coordinates.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`PhysicsRayQueryParameters3D<class_PhysicsRayQueryParameters3D>`
**create**(from: `Vector3<class_Vector3>`, to: `Vector3<class_Vector3>`,
collision\_mask: `int<class_int>` = 4294967295, exclude:
`Array<class_Array>`\[`RID<class_RID>`\] = \[\])
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_PhysicsRayQueryParameters3D_method_create>`

Returns a new, pre-configured **PhysicsRayQueryParameters3D** object.
Use it to quickly create query parameters using the most common options.

    var query = PhysicsRayQueryParameters3D.create(position, position + Vector3(0, -10, 0))
    var collision = get_world_3d().direct_space_state.intersect_ray(query)
