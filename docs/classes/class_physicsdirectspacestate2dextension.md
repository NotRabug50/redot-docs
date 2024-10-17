github\_url  
hide

# PhysicsDirectSpaceState2DExtension

**Inherits:**
`PhysicsDirectSpaceState2D<class_PhysicsDirectSpaceState2D>` **&lt;**
`Object<class_Object>`

Provides virtual methods that can be overridden to create custom
`PhysicsDirectSpaceState2D<class_PhysicsDirectSpaceState2D>`
implementations.

classref-introduction-group

## Description

This class extends
`PhysicsDirectSpaceState2D<class_PhysicsDirectSpaceState2D>` by
providing additional virtual methods that can be overridden. When these
methods are overridden, they will be called instead of the internal
methods of the physics server.

Intended for use with GDExtension to create custom implementations of
`PhysicsDirectSpaceState2D<class_PhysicsDirectSpaceState2D>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **\_cast\_motion**(shape\_rid: `RID<class_RID>`,
transform: `Transform2D<class_Transform2D>`, motion:
`Vector2<class_Vector2>`, margin: `float<class_float>`, collision\_mask:
`int<class_int>`, collide\_with\_bodies: `bool<class_bool>`,
collide\_with\_areas: `bool<class_bool>`, closest\_safe: `float*`,
closest\_unsafe: `float*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState2DExtension_private_method__cast_motion>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_collide\_shape**(shape\_rid: `RID<class_RID>`,
transform: `Transform2D<class_Transform2D>`, motion:
`Vector2<class_Vector2>`, margin: `float<class_float>`, collision\_mask:
`int<class_int>`, collide\_with\_bodies: `bool<class_bool>`,
collide\_with\_areas: `bool<class_bool>`, results: `void*`,
max\_results: `int<class_int>`, result\_count: `int32_t*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState2DExtension_private_method__collide_shape>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_intersect\_point**(position:
`Vector2<class_Vector2>`, canvas\_instance\_id: `int<class_int>`,
collision\_mask: `int<class_int>`, collide\_with\_bodies:
`bool<class_bool>`, collide\_with\_areas: `bool<class_bool>`, results:
`PhysicsServer2DExtensionShapeResult*`, max\_results: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState2DExtension_private_method__intersect_point>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_intersect\_ray**(from: `Vector2<class_Vector2>`,
to: `Vector2<class_Vector2>`, collision\_mask: `int<class_int>`,
collide\_with\_bodies: `bool<class_bool>`, collide\_with\_areas:
`bool<class_bool>`, hit\_from\_inside: `bool<class_bool>`, result:
`PhysicsServer2DExtensionRayResult*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState2DExtension_private_method__intersect_ray>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_intersect\_shape**(shape\_rid: `RID<class_RID>`,
transform: `Transform2D<class_Transform2D>`, motion:
`Vector2<class_Vector2>`, margin: `float<class_float>`, collision\_mask:
`int<class_int>`, collide\_with\_bodies: `bool<class_bool>`,
collide\_with\_areas: `bool<class_bool>`, result:
`PhysicsServer2DExtensionShapeResult*`, max\_results: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState2DExtension_private_method__intersect_shape>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_rest\_info**(shape\_rid: `RID<class_RID>`,
transform: `Transform2D<class_Transform2D>`, motion:
`Vector2<class_Vector2>`, margin: `float<class_float>`, collision\_mask:
`int<class_int>`, collide\_with\_bodies: `bool<class_bool>`,
collide\_with\_areas: `bool<class_bool>`, rest\_info:
`PhysicsServer2DExtensionShapeRestInfo*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsDirectSpaceState2DExtension_private_method__rest_info>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_body\_excluded\_from\_query**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsDirectSpaceState2DExtension_method_is_body_excluded_from_query>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
