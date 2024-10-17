github\_url  
hide

# PhysicsPointQueryParameters3D

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides parameters for
`PhysicsDirectSpaceState3D.intersect_point<class_PhysicsDirectSpaceState3D_method_intersect_point>`.

classref-introduction-group

## Description

By changing various properties of this object, such as the point
position, you can configure the parameters for
`PhysicsDirectSpaceState3D.intersect_point<class_PhysicsDirectSpaceState3D_method_intersect_point>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **collide\_with\_areas** = `false`
`🔗<class_PhysicsPointQueryParameters3D_property_collide_with_areas>`

classref-property-setget

-   `void (No return value.)` **set\_collide\_with\_areas**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_collide\_with\_areas\_enabled**()

If `true`, the query will take `Area3D<class_Area3D>`s into account.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **collide\_with\_bodies** = `true`
`🔗<class_PhysicsPointQueryParameters3D_property_collide_with_bodies>`

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
`🔗<class_PhysicsPointQueryParameters3D_property_collision_mask>`

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
`🔗<class_PhysicsPointQueryParameters3D_property_exclude>`

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

`Vector3<class_Vector3>` **position** = `Vector3(0, 0, 0)`
`🔗<class_PhysicsPointQueryParameters3D_property_position>`

classref-property-setget

-   `void (No return value.)` **set\_position**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_position**()

The position being queried for, in global coordinates.
