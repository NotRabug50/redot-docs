github\_url  
hide

# PhysicsShapeQueryParameters3D

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides parameters for
`PhysicsDirectSpaceState3D.intersect_shape<class_PhysicsDirectSpaceState3D_method_intersect_shape>`.

classref-introduction-group

## Description

By changing various properties of this object, such as the shape, you
can configure the parameters for
`PhysicsDirectSpaceState3D.intersect_shape<class_PhysicsDirectSpaceState3D_method_intersect_shape>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **collide\_with\_areas** = `false`
`🔗<class_PhysicsShapeQueryParameters3D_property_collide_with_areas>`

classref-property-setget

-   `void (No return value.)` **set\_collide\_with\_areas**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_collide\_with\_areas\_enabled**()

If `true`, the query will take `Area3D<class_Area3D>`s into account.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **collide\_with\_bodies** = `true`
`🔗<class_PhysicsShapeQueryParameters3D_property_collide_with_bodies>`

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
`🔗<class_PhysicsShapeQueryParameters3D_property_collision_mask>`

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
`🔗<class_PhysicsShapeQueryParameters3D_property_exclude>`

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

`float<class_float>` **margin** = `0.0`
`🔗<class_PhysicsShapeQueryParameters3D_property_margin>`

classref-property-setget

-   `void (No return value.)` **set\_margin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_margin**()

The collision margin for the shape.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **motion** = `Vector3(0, 0, 0)`
`🔗<class_PhysicsShapeQueryParameters3D_property_motion>`

classref-property-setget

-   `void (No return value.)` **set\_motion**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_motion**()

The motion of the shape being queried for.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Resource<class_Resource>` **shape**
`🔗<class_PhysicsShapeQueryParameters3D_property_shape>`

classref-property-setget

-   `void (No return value.)` **set\_shape**(value:
    `Resource<class_Resource>`)
-   `Resource<class_Resource>` **get\_shape**()

The `Shape3D<class_Shape3D>` that will be used for
collision/intersection queries. This stores the actual reference which
avoids the shape to be released while being used for queries, so always
prefer using this over
`shape_rid<class_PhysicsShapeQueryParameters3D_property_shape_rid>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`RID<class_RID>` **shape\_rid** = `RID()`
`🔗<class_PhysicsShapeQueryParameters3D_property_shape_rid>`

classref-property-setget

-   `void (No return value.)` **set\_shape\_rid**(value:
    `RID<class_RID>`)
-   `RID<class_RID>` **get\_shape\_rid**()

The queried shape's `RID<class_RID>` that will be used for
collision/intersection queries. Use this over
`shape<class_PhysicsShapeQueryParameters3D_property_shape>` if you want
to optimize for performance using the Servers API:

gdscript

var shape\_rid =
PhysicsServer3D.shape\_create(PhysicsServer3D.SHAPE\_SPHERE) var radius
= 2.0 PhysicsServer3D.shape\_set\_data(shape\_rid, radius)

var params = PhysicsShapeQueryParameters3D.new() params.shape\_rid =
shape\_rid

\# Execute physics queries here...

\# Release the shape when done with physics queries.
PhysicsServer3D.free\_rid(shape\_rid)

csharp

RID shapeRid =
PhysicsServer3D.ShapeCreate(PhysicsServer3D.ShapeType.Sphere); float
radius = 2.0f; PhysicsServer3D.ShapeSetData(shapeRid, radius);

var params = new PhysicsShapeQueryParameters3D(); params.ShapeRid =
shapeRid;

// Execute physics queries here...

// Release the shape when done with physics queries.
PhysicsServer3D.FreeRid(shapeRid);

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform3D<class_Transform3D>` **transform** =
`Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0)`
`🔗<class_PhysicsShapeQueryParameters3D_property_transform>`

classref-property-setget

-   `void (No return value.)` **set\_transform**(value:
    `Transform3D<class_Transform3D>`)
-   `Transform3D<class_Transform3D>` **get\_transform**()

The queried shape's transform matrix.
