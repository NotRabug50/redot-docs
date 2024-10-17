github\_url  
hide

# PhysicsDirectSpaceState3DExtension

**Inherits:**
`PhysicsDirectSpaceState3D<class_PhysicsDirectSpaceState3D>` **&lt;**
`Object<class_Object>`

Provides virtual methods that can be overridden to create custom
`PhysicsDirectSpaceState3D<class_PhysicsDirectSpaceState3D>`
implementations.

classref-introduction-group

## Description

This class extends
`PhysicsDirectSpaceState3D<class_PhysicsDirectSpaceState3D>` by
providing additional virtual methods that can be overridden. When these
methods are overridden, they will be called instead of the internal
methods of the physics server.

Intended for use with GDExtension to create custom implementations of
`PhysicsDirectSpaceState3D<class_PhysicsDirectSpaceState3D>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **\_cast\_motion**(shape\_rid: `RID<class_RID>`,
transform: `Transform3D<class_Transform3D>`, motion:
`Vector3<class_Vector3>`, margin: `float<class_float>`, collision\_mask:
`int<class_int>`, collide\_with\_bodies: `bool<class_bool>`,
collide\_with\_areas: `bool<class_bool>`, closest\_safe: `float*`,
closest\_unsafe: `float*`, info:
`PhysicsServer3DExtensionShapeRestInfo*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState3DExtension_private_method__cast_motion>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_collide\_shape**(shape\_rid: `RID<class_RID>`,
transform: `Transform3D<class_Transform3D>`, motion:
`Vector3<class_Vector3>`, margin: `float<class_float>`, collision\_mask:
`int<class_int>`, collide\_with\_bodies: `bool<class_bool>`,
collide\_with\_areas: `bool<class_bool>`, results: `void*`,
max\_results: `int<class_int>`, result\_count: `int32_t*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState3DExtension_private_method__collide_shape>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>`
**\_get\_closest\_point\_to\_object\_volume**(object: `RID<class_RID>`,
point: `Vector3<class_Vector3>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectSpaceState3DExtension_private_method__get_closest_point_to_object_volume>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_intersect\_point**(position:
`Vector3<class_Vector3>`, collision\_mask: `int<class_int>`,
collide\_with\_bodies: `bool<class_bool>`, collide\_with\_areas:
`bool<class_bool>`, results: `PhysicsServer3DExtensionShapeResult*`,
max\_results: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState3DExtension_private_method__intersect_point>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_intersect\_ray**(from: `Vector3<class_Vector3>`,
to: `Vector3<class_Vector3>`, collision\_mask: `int<class_int>`,
collide\_with\_bodies: `bool<class_bool>`, collide\_with\_areas:
`bool<class_bool>`, hit\_from\_inside: `bool<class_bool>`,
hit\_back\_faces: `bool<class_bool>`, pick\_ray: `bool<class_bool>`,
result: `PhysicsServer3DExtensionRayResult*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState3DExtension_private_method__intersect_ray>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_intersect\_shape**(shape\_rid: `RID<class_RID>`,
transform: `Transform3D<class_Transform3D>`, motion:
`Vector3<class_Vector3>`, margin: `float<class_float>`, collision\_mask:
`int<class_int>`, collide\_with\_bodies: `bool<class_bool>`,
collide\_with\_areas: `bool<class_bool>`, result\_count:
`PhysicsServer3DExtensionShapeResult*`, max\_results: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState3DExtension_private_method__intersect_shape>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_rest\_info**(shape\_rid: `RID<class_RID>`,
transform: `Transform3D<class_Transform3D>`, motion:
`Vector3<class_Vector3>`, margin: `float<class_float>`, collision\_mask:
`int<class_int>`, collide\_with\_bodies: `bool<class_bool>`,
collide\_with\_areas: `bool<class_bool>`, rest\_info:
`PhysicsServer3DExtensionShapeRestInfo*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState3DExtension_private_method__rest_info>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_body\_excluded\_from\_query**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectSpaceState3DExtension_method_is_body_excluded_from_query>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
