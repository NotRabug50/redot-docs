github\_url  
hide

# Shape3D

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `BoxShape3D<class_BoxShape3D>`,
`CapsuleShape3D<class_CapsuleShape3D>`,
`ConcavePolygonShape3D<class_ConcavePolygonShape3D>`,
`ConvexPolygonShape3D<class_ConvexPolygonShape3D>`,
`CylinderShape3D<class_CylinderShape3D>`,
`HeightMapShape3D<class_HeightMapShape3D>`,
`SeparationRayShape3D<class_SeparationRayShape3D>`,
`SphereShape3D<class_SphereShape3D>`,
`WorldBoundaryShape3D<class_WorldBoundaryShape3D>`

Abstract base class for 3D shapes used for physics collision.

classref-introduction-group

## Description

Abstract base class for all 3D shapes, intended for use in physics.

\*\*Performance:\*\* Primitive shapes, especially
`SphereShape3D<class_SphereShape3D>`, are fast to check collisions
against. `ConvexPolygonShape3D<class_ConvexPolygonShape3D>` and
`HeightMapShape3D<class_HeightMapShape3D>` are slower, and
`ConcavePolygonShape3D<class_ConcavePolygonShape3D>` is the slowest.

classref-introduction-group

## Tutorials

-   `Physics introduction <../tutorials/physics/physics_introduction>`

classref-reftable-group

## Properties

<table>
<tbody>
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

`float<class_float>` **custom\_solver\_bias** = `0.0`
`🔗<class_Shape3D_property_custom_solver_bias>`

classref-property-setget

-   `void (No return value.)` **set\_custom\_solver\_bias**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_custom\_solver\_bias**()

The shape's custom solver bias. Defines how much bodies react to enforce
contact separation when this shape is involved.

When set to `0`, the default value from
`ProjectSettings.physics/3d/solver/default_contact_bias<class_ProjectSettings_property_physics/3d/solver/default_contact_bias>`
is used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **margin** = `0.04`
`🔗<class_Shape3D_property_margin>`

classref-property-setget

-   `void (No return value.)` **set\_margin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_margin**()

The collision margin for the shape. This is not used in Godot Physics.

Collision margins allow collision detection to be more efficient by
adding an extra shell around shapes. Collision algorithms are more
expensive when objects overlap by more than their margin, so a higher
value for margins is better for performance, at the cost of accuracy
around edges as it makes them less sharp.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`ArrayMesh<class_ArrayMesh>` **get\_debug\_mesh**()
`🔗<class_Shape3D_method_get_debug_mesh>`

Returns the `ArrayMesh<class_ArrayMesh>` used to draw the debug
collision for this **Shape3D**.
