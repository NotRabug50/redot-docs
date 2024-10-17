github\_url  
hide

# PhysicsServer2DExtension

**Inherits:** `PhysicsServer2D<class_PhysicsServer2D>` **&lt;**
`Object<class_Object>`

Provides virtual methods that can be overridden to create custom
`PhysicsServer2D<class_PhysicsServer2D>` implementations.

classref-introduction-group

## Description

This class extends `PhysicsServer2D<class_PhysicsServer2D>` by providing
additional virtual methods that can be overridden. When these methods
are overridden, they will be called instead of the internal methods of
the physics server.

Intended for use with GDExtension to create custom implementations of
`PhysicsServer2D<class_PhysicsServer2D>`.

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

`void (No return value.)` **\_area\_add\_shape**(area: `RID<class_RID>`,
shape: `RID<class_RID>`, transform: `Transform2D<class_Transform2D>`,
disabled: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_add_shape>`

Overridable version of
`PhysicsServer2D.area_add_shape<class_PhysicsServer2D_method_area_add_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_attach\_canvas\_instance\_id**(area:
`RID<class_RID>`, id: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_attach_canvas_instance_id>`

Overridable version of
`PhysicsServer2D.area_attach_canvas_instance_id<class_PhysicsServer2D_method_area_attach_canvas_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_attach\_object\_instance\_id**(area:
`RID<class_RID>`, id: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_attach_object_instance_id>`

Overridable version of
`PhysicsServer2D.area_attach_object_instance_id<class_PhysicsServer2D_method_area_attach_object_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_clear\_shapes**(area:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_clear_shapes>`

Overridable version of
`PhysicsServer2D.area_clear_shapes<class_PhysicsServer2D_method_area_clear_shapes>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_area\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_create>`

Overridable version of
`PhysicsServer2D.area_create<class_PhysicsServer2D_method_area_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_area\_get\_canvas\_instance\_id**(area:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_get_canvas_instance_id>`

Overridable version of
`PhysicsServer2D.area_get_canvas_instance_id<class_PhysicsServer2D_method_area_get_canvas_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_area\_get\_collision\_layer**(area:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_get_collision_layer>`

Overridable version of
`PhysicsServer2D.area_get_collision_layer<class_PhysicsServer2D_method_area_get_collision_layer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_area\_get\_collision\_mask**(area:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_get_collision_mask>`

Overridable version of
`PhysicsServer2D.area_get_collision_mask<class_PhysicsServer2D_method_area_get_collision_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_area\_get\_object\_instance\_id**(area:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_get_object_instance_id>`

Overridable version of
`PhysicsServer2D.area_get_object_instance_id<class_PhysicsServer2D_method_area_get_object_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_area\_get\_param**(area: `RID<class_RID>`,
param: `AreaParameter<enum_PhysicsServer2D_AreaParameter>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_get_param>`

Overridable version of
`PhysicsServer2D.area_get_param<class_PhysicsServer2D_method_area_get_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_area\_get\_shape**(area: `RID<class_RID>`,
shape\_idx: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_get_shape>`

Overridable version of
`PhysicsServer2D.area_get_shape<class_PhysicsServer2D_method_area_get_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_area\_get\_shape\_count**(area: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_get_shape_count>`

Overridable version of
`PhysicsServer2D.area_get_shape_count<class_PhysicsServer2D_method_area_get_shape_count>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **\_area\_get\_shape\_transform**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_get_shape_transform>`

Overridable version of
`PhysicsServer2D.area_get_shape_transform<class_PhysicsServer2D_method_area_get_shape_transform>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_area\_get\_space**(area: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_get_space>`

Overridable version of
`PhysicsServer2D.area_get_space<class_PhysicsServer2D_method_area_get_space>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **\_area\_get\_transform**(area:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_get_transform>`

Overridable version of
`PhysicsServer2D.area_get_transform<class_PhysicsServer2D_method_area_get_transform>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_remove\_shape**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_remove_shape>`

Overridable version of
`PhysicsServer2D.area_remove_shape<class_PhysicsServer2D_method_area_remove_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_area\_monitor\_callback**(area:
`RID<class_RID>`, callback: `Callable<class_Callable>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_area_monitor_callback>`

Overridable version of
`PhysicsServer2D.area_set_area_monitor_callback<class_PhysicsServer2D_method_area_set_area_monitor_callback>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_collision\_layer**(area:
`RID<class_RID>`, layer: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_collision_layer>`

Overridable version of
`PhysicsServer2D.area_set_collision_layer<class_PhysicsServer2D_method_area_set_collision_layer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_collision\_mask**(area:
`RID<class_RID>`, mask: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_collision_mask>`

Overridable version of
`PhysicsServer2D.area_set_collision_mask<class_PhysicsServer2D_method_area_set_collision_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_monitor\_callback**(area:
`RID<class_RID>`, callback: `Callable<class_Callable>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_monitor_callback>`

Overridable version of
`PhysicsServer2D.area_set_monitor_callback<class_PhysicsServer2D_method_area_set_monitor_callback>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_monitorable**(area:
`RID<class_RID>`, monitorable: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_monitorable>`

Overridable version of
`PhysicsServer2D.area_set_monitorable<class_PhysicsServer2D_method_area_set_monitorable>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_param**(area: `RID<class_RID>`,
param: `AreaParameter<enum_PhysicsServer2D_AreaParameter>`, value:
`Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_param>`

Overridable version of
`PhysicsServer2D.area_set_param<class_PhysicsServer2D_method_area_set_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_pickable**(area:
`RID<class_RID>`, pickable: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_pickable>`

If set to `true`, allows the area with the given `RID<class_RID>` to
detect mouse inputs when the mouse cursor is hovering on it.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `area_set_pickable` method. Corresponds to
`CollisionObject2D.input_pickable<class_CollisionObject2D_property_input_pickable>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_shape**(area: `RID<class_RID>`,
shape\_idx: `int<class_int>`, shape: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_shape>`

Overridable version of
`PhysicsServer2D.area_set_shape<class_PhysicsServer2D_method_area_set_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_shape\_disabled**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`, disabled:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_shape_disabled>`

Overridable version of
`PhysicsServer2D.area_set_shape_disabled<class_PhysicsServer2D_method_area_set_shape_disabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_shape\_transform**(area:
`RID<class_RID>`, shape\_idx: `int<class_int>`, transform:
`Transform2D<class_Transform2D>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_shape_transform>`

Overridable version of
`PhysicsServer2D.area_set_shape_transform<class_PhysicsServer2D_method_area_set_shape_transform>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_space**(area: `RID<class_RID>`,
space: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_space>`

Overridable version of
`PhysicsServer2D.area_set_space<class_PhysicsServer2D_method_area_set_space>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_area\_set\_transform**(area:
`RID<class_RID>`, transform: `Transform2D<class_Transform2D>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__area_set_transform>`

Overridable version of
`PhysicsServer2D.area_set_transform<class_PhysicsServer2D_method_area_set_transform>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_add\_collision\_exception**(body:
`RID<class_RID>`, excepted\_body: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_add_collision_exception>`

Overridable version of
`PhysicsServer2D.body_add_collision_exception<class_PhysicsServer2D_method_body_add_collision_exception>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_body\_add\_constant\_central\_force**(body: `RID<class_RID>`, force:
`Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_add_constant_central_force>`

Overridable version of
`PhysicsServer2D.body_add_constant_central_force<class_PhysicsServer2D_method_body_add_constant_central_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_add\_constant\_force**(body:
`RID<class_RID>`, force: `Vector2<class_Vector2>`, position:
`Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_add_constant_force>`

Overridable version of
`PhysicsServer2D.body_add_constant_force<class_PhysicsServer2D_method_body_add_constant_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_add\_constant\_torque**(body:
`RID<class_RID>`, torque: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_add_constant_torque>`

Overridable version of
`PhysicsServer2D.body_add_constant_torque<class_PhysicsServer2D_method_body_add_constant_torque>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_add\_shape**(body: `RID<class_RID>`,
shape: `RID<class_RID>`, transform: `Transform2D<class_Transform2D>`,
disabled: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_add_shape>`

Overridable version of
`PhysicsServer2D.body_add_shape<class_PhysicsServer2D_method_body_add_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_apply\_central\_force**(body:
`RID<class_RID>`, force: `Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_apply_central_force>`

Overridable version of
`PhysicsServer2D.body_apply_central_force<class_PhysicsServer2D_method_body_apply_central_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_apply\_central\_impulse**(body:
`RID<class_RID>`, impulse: `Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_apply_central_impulse>`

Overridable version of
`PhysicsServer2D.body_apply_central_impulse<class_PhysicsServer2D_method_body_apply_central_impulse>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_apply\_force**(body:
`RID<class_RID>`, force: `Vector2<class_Vector2>`, position:
`Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_apply_force>`

Overridable version of
`PhysicsServer2D.body_apply_force<class_PhysicsServer2D_method_body_apply_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_apply\_impulse**(body:
`RID<class_RID>`, impulse: `Vector2<class_Vector2>`, position:
`Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_apply_impulse>`

Overridable version of
`PhysicsServer2D.body_apply_impulse<class_PhysicsServer2D_method_body_apply_impulse>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_apply\_torque**(body:
`RID<class_RID>`, torque: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_apply_torque>`

Overridable version of
`PhysicsServer2D.body_apply_torque<class_PhysicsServer2D_method_body_apply_torque>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_apply\_torque\_impulse**(body:
`RID<class_RID>`, impulse: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_apply_torque_impulse>`

Overridable version of
`PhysicsServer2D.body_apply_torque_impulse<class_PhysicsServer2D_method_body_apply_torque_impulse>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_attach\_canvas\_instance\_id**(body:
`RID<class_RID>`, id: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_attach_canvas_instance_id>`

Overridable version of
`PhysicsServer2D.body_attach_canvas_instance_id<class_PhysicsServer2D_method_body_attach_canvas_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_attach\_object\_instance\_id**(body:
`RID<class_RID>`, id: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_attach_object_instance_id>`

Overridable version of
`PhysicsServer2D.body_attach_object_instance_id<class_PhysicsServer2D_method_body_attach_object_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_clear\_shapes**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_clear_shapes>`

Overridable version of
`PhysicsServer2D.body_clear_shapes<class_PhysicsServer2D_method_body_clear_shapes>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_body\_collide\_shape**(body: `RID<class_RID>`,
body\_shape: `int<class_int>`, shape: `RID<class_RID>`, shape\_xform:
`Transform2D<class_Transform2D>`, motion: `Vector2<class_Vector2>`,
results: `void*`, result\_max: `int<class_int>`, result\_count:
`int32_t*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_collide_shape>`

Given a `body`, a `shape`, and their respective parameters, this method
should return `true` if a collision between the two would occur, with
additional details passed in `results`.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `shape_collide` method. Corresponds to
`PhysicsDirectSpaceState2D.collide_shape<class_PhysicsDirectSpaceState2D_method_collide_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_body\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_create>`

Overridable version of
`PhysicsServer2D.body_create<class_PhysicsServer2D_method_body_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_body\_get\_canvas\_instance\_id**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_canvas_instance_id>`

Overridable version of
`PhysicsServer2D.body_get_canvas_instance_id<class_PhysicsServer2D_method_body_get_canvas_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`RID<class_RID>`\]
**\_body\_get\_collision\_exceptions**(body: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_collision_exceptions>`

Returns the `RID<class_RID>`s of all bodies added as collision
exceptions for the given `body`. See also
`_body_add_collision_exception<class_PhysicsServer2DExtension_private_method__body_add_collision_exception>`
and
`_body_remove_collision_exception<class_PhysicsServer2DExtension_private_method__body_remove_collision_exception>`.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `body_get_collision_exceptions` method. Corresponds to
`PhysicsBody2D.get_collision_exceptions<class_PhysicsBody2D_method_get_collision_exceptions>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_body\_get\_collision\_layer**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_collision_layer>`

Overridable version of
`PhysicsServer2D.body_get_collision_layer<class_PhysicsServer2D_method_body_get_collision_layer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_body\_get\_collision\_mask**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_collision_mask>`

Overridable version of
`PhysicsServer2D.body_get_collision_mask<class_PhysicsServer2D_method_body_get_collision_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_body\_get\_collision\_priority**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_collision_priority>`

Overridable version of
`PhysicsServer2D.body_get_collision_priority<class_PhysicsServer2D_method_body_get_collision_priority>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **\_body\_get\_constant\_force**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_constant_force>`

Overridable version of
`PhysicsServer2D.body_get_constant_force<class_PhysicsServer2D_method_body_get_constant_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_body\_get\_constant\_torque**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_constant_torque>`

Overridable version of
`PhysicsServer2D.body_get_constant_torque<class_PhysicsServer2D_method_body_get_constant_torque>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>`
**\_body\_get\_contacts\_reported\_depth\_threshold**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_contacts_reported_depth_threshold>`

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `body_get_contacts_reported_depth_threshold` method.

\*\*Note:\*\* This method is currently unused by Godot's default physics
implementation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CCDMode<enum_PhysicsServer2D_CCDMode>`
**\_body\_get\_continuous\_collision\_detection\_mode**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_continuous_collision_detection_mode>`

Overridable version of
`PhysicsServer2D.body_get_continuous_collision_detection_mode<class_PhysicsServer2D_method_body_get_continuous_collision_detection_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PhysicsDirectBodyState2D<class_PhysicsDirectBodyState2D>`
**\_body\_get\_direct\_state**(body: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_direct_state>`

Overridable version of
`PhysicsServer2D.body_get_direct_state<class_PhysicsServer2D_method_body_get_direct_state>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_body\_get\_max\_contacts\_reported**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_max_contacts_reported>`

Overridable version of
`PhysicsServer2D.body_get_max_contacts_reported<class_PhysicsServer2D_method_body_get_max_contacts_reported>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`BodyMode<enum_PhysicsServer2D_BodyMode>` **\_body\_get\_mode**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_mode>`

Overridable version of
`PhysicsServer2D.body_get_mode<class_PhysicsServer2D_method_body_get_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_body\_get\_object\_instance\_id**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_object_instance_id>`

Overridable version of
`PhysicsServer2D.body_get_object_instance_id<class_PhysicsServer2D_method_body_get_object_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_body\_get\_param**(body: `RID<class_RID>`,
param: `BodyParameter<enum_PhysicsServer2D_BodyParameter>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_param>`

Overridable version of
`PhysicsServer2D.body_get_param<class_PhysicsServer2D_method_body_get_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_body\_get\_shape**(body: `RID<class_RID>`,
shape\_idx: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_shape>`

Overridable version of
`PhysicsServer2D.body_get_shape<class_PhysicsServer2D_method_body_get_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_body\_get\_shape\_count**(body: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_shape_count>`

Overridable version of
`PhysicsServer2D.body_get_shape_count<class_PhysicsServer2D_method_body_get_shape_count>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **\_body\_get\_shape\_transform**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_shape_transform>`

Overridable version of
`PhysicsServer2D.body_get_shape_transform<class_PhysicsServer2D_method_body_get_shape_transform>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_body\_get\_space**(body: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_space>`

Overridable version of
`PhysicsServer2D.body_get_space<class_PhysicsServer2D_method_body_get_space>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_body\_get\_state**(body: `RID<class_RID>`,
state: `BodyState<enum_PhysicsServer2D_BodyState>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_get_state>`

Overridable version of
`PhysicsServer2D.body_get_state<class_PhysicsServer2D_method_body_get_state>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_body\_is\_omitting\_force\_integration**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_is_omitting_force_integration>`

Overridable version of
`PhysicsServer2D.body_is_omitting_force_integration<class_PhysicsServer2D_method_body_is_omitting_force_integration>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_remove\_collision\_exception**(body:
`RID<class_RID>`, excepted\_body: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_remove_collision_exception>`

Overridable version of
`PhysicsServer2D.body_remove_collision_exception<class_PhysicsServer2D_method_body_remove_collision_exception>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_remove\_shape**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_remove_shape>`

Overridable version of
`PhysicsServer2D.body_remove_shape<class_PhysicsServer2D_method_body_remove_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_reset\_mass\_properties**(body:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_reset_mass_properties>`

Overridable version of
`PhysicsServer2D.body_reset_mass_properties<class_PhysicsServer2D_method_body_reset_mass_properties>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_axis\_velocity**(body:
`RID<class_RID>`, axis\_velocity: `Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_axis_velocity>`

Overridable version of
`PhysicsServer2D.body_set_axis_velocity<class_PhysicsServer2D_method_body_set_axis_velocity>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_collision\_layer**(body:
`RID<class_RID>`, layer: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_collision_layer>`

Overridable version of
`PhysicsServer2D.body_set_collision_layer<class_PhysicsServer2D_method_body_set_collision_layer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_collision\_mask**(body:
`RID<class_RID>`, mask: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_collision_mask>`

Overridable version of
`PhysicsServer2D.body_set_collision_mask<class_PhysicsServer2D_method_body_set_collision_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_collision\_priority**(body:
`RID<class_RID>`, priority: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_collision_priority>`

Overridable version of
`PhysicsServer2D.body_set_collision_priority<class_PhysicsServer2D_method_body_set_collision_priority>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_constant\_force**(body:
`RID<class_RID>`, force: `Vector2<class_Vector2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_constant_force>`

Overridable version of
`PhysicsServer2D.body_set_constant_force<class_PhysicsServer2D_method_body_set_constant_force>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_constant\_torque**(body:
`RID<class_RID>`, torque: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_constant_torque>`

Overridable version of
`PhysicsServer2D.body_set_constant_torque<class_PhysicsServer2D_method_body_set_constant_torque>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_body\_set\_contacts\_reported\_depth\_threshold**(body:
`RID<class_RID>`, threshold: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_contacts_reported_depth_threshold>`

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `body_set_contacts_reported_depth_threshold` method.

\*\*Note:\*\* This method is currently unused by Godot's default physics
implementation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_body\_set\_continuous\_collision\_detection\_mode**(body:
`RID<class_RID>`, mode: `CCDMode<enum_PhysicsServer2D_CCDMode>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_continuous_collision_detection_mode>`

Overridable version of
`PhysicsServer2D.body_set_continuous_collision_detection_mode<class_PhysicsServer2D_method_body_set_continuous_collision_detection_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_body\_set\_force\_integration\_callback**(body: `RID<class_RID>`,
callable: `Callable<class_Callable>`, userdata:
`Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_force_integration_callback>`

Overridable version of
`PhysicsServer2D.body_set_force_integration_callback<class_PhysicsServer2D_method_body_set_force_integration_callback>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_max\_contacts\_reported**(body:
`RID<class_RID>`, amount: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_max_contacts_reported>`

Overridable version of
`PhysicsServer2D.body_set_max_contacts_reported<class_PhysicsServer2D_method_body_set_max_contacts_reported>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_mode**(body: `RID<class_RID>`,
mode: `BodyMode<enum_PhysicsServer2D_BodyMode>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_mode>`

Overridable version of
`PhysicsServer2D.body_set_mode<class_PhysicsServer2D_method_body_set_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_body\_set\_omit\_force\_integration**(body: `RID<class_RID>`,
enable: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_omit_force_integration>`

Overridable version of
`PhysicsServer2D.body_set_omit_force_integration<class_PhysicsServer2D_method_body_set_omit_force_integration>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_param**(body: `RID<class_RID>`,
param: `BodyParameter<enum_PhysicsServer2D_BodyParameter>`, value:
`Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_param>`

Overridable version of
`PhysicsServer2D.body_set_param<class_PhysicsServer2D_method_body_set_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_pickable**(body:
`RID<class_RID>`, pickable: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_pickable>`

If set to `true`, allows the body with the given `RID<class_RID>` to
detect mouse inputs when the mouse cursor is hovering on it.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `body_set_pickable` method. Corresponds to
`CollisionObject2D.input_pickable<class_CollisionObject2D_property_input_pickable>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_shape**(body: `RID<class_RID>`,
shape\_idx: `int<class_int>`, shape: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_shape>`

Overridable version of
`PhysicsServer2D.body_set_shape<class_PhysicsServer2D_method_body_set_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_body\_set\_shape\_as\_one\_way\_collision**(body: `RID<class_RID>`,
shape\_idx: `int<class_int>`, enable: `bool<class_bool>`, margin:
`float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_shape_as_one_way_collision>`

Overridable version of
`PhysicsServer2D.body_set_shape_as_one_way_collision<class_PhysicsServer2D_method_body_set_shape_as_one_way_collision>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_shape\_disabled**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`, disabled:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_shape_disabled>`

Overridable version of
`PhysicsServer2D.body_set_shape_disabled<class_PhysicsServer2D_method_body_set_shape_disabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_shape\_transform**(body:
`RID<class_RID>`, shape\_idx: `int<class_int>`, transform:
`Transform2D<class_Transform2D>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_shape_transform>`

Overridable version of
`PhysicsServer2D.body_set_shape_transform<class_PhysicsServer2D_method_body_set_shape_transform>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_space**(body: `RID<class_RID>`,
space: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_space>`

Overridable version of
`PhysicsServer2D.body_set_space<class_PhysicsServer2D_method_body_set_space>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_state**(body: `RID<class_RID>`,
state: `BodyState<enum_PhysicsServer2D_BodyState>`, value:
`Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_state>`

Overridable version of
`PhysicsServer2D.body_set_state<class_PhysicsServer2D_method_body_set_state>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_body\_set\_state\_sync\_callback**(body:
`RID<class_RID>`, callable: `Callable<class_Callable>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_set_state_sync_callback>`

Assigns the `body` to call the given `callable` during the
synchronization phase of the loop, before
`_step<class_PhysicsServer2DExtension_private_method__step>` is called.
See also `_sync<class_PhysicsServer2DExtension_private_method__sync>`.

Overridable version of
`PhysicsServer2D.body_set_state_sync_callback<class_PhysicsServer2D_method_body_set_state_sync_callback>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_body\_test\_motion**(body: `RID<class_RID>`,
from: `Transform2D<class_Transform2D>`, motion:
`Vector2<class_Vector2>`, margin: `float<class_float>`,
collide\_separation\_ray: `bool<class_bool>`, recovery\_as\_collision:
`bool<class_bool>`, result: `PhysicsServer2DExtensionMotionResult*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__body_test_motion>`

Overridable version of
`PhysicsServer2D.body_test_motion<class_PhysicsServer2D_method_body_test_motion>`.
Unlike the exposed implementation, this method does not receive all of
the arguments inside a
`PhysicsTestMotionParameters2D<class_PhysicsTestMotionParameters2D>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_capsule\_shape\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__capsule_shape_create>`

Overridable version of
`PhysicsServer2D.capsule_shape_create<class_PhysicsServer2D_method_capsule_shape_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_circle\_shape\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__circle_shape_create>`

Overridable version of
`PhysicsServer2D.circle_shape_create<class_PhysicsServer2D_method_circle_shape_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_concave\_polygon\_shape\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__concave_polygon_shape_create>`

Overridable version of
`PhysicsServer2D.concave_polygon_shape_create<class_PhysicsServer2D_method_concave_polygon_shape_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_convex\_polygon\_shape\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__convex_polygon_shape_create>`

Overridable version of
`PhysicsServer2D.convex_polygon_shape_create<class_PhysicsServer2D_method_convex_polygon_shape_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_damped\_spring\_joint\_get\_param**(joint:
`RID<class_RID>`, param:
`DampedSpringParam<enum_PhysicsServer2D_DampedSpringParam>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__damped_spring_joint_get_param>`

Overridable version of
`PhysicsServer2D.damped_spring_joint_get_param<class_PhysicsServer2D_method_damped_spring_joint_get_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_damped\_spring\_joint\_set\_param**(joint:
`RID<class_RID>`, param:
`DampedSpringParam<enum_PhysicsServer2D_DampedSpringParam>`, value:
`float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__damped_spring_joint_set_param>`

Overridable version of
`PhysicsServer2D.damped_spring_joint_set_param<class_PhysicsServer2D_method_damped_spring_joint_set_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_end\_sync**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__end_sync>`

Called to indicate that the physics server has stopped synchronizing. It
is in the loop's iteration/physics phase, and can access physics objects
even if running on a separate thread. See also
`_sync<class_PhysicsServer2DExtension_private_method__sync>`.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `end_sync` method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_finish**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__finish>`

Called when the main loop finalizes to shut down the physics server. See
also `MainLoop._finalize<class_MainLoop_private_method__finalize>` and
`_init<class_PhysicsServer2DExtension_private_method__init>`.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `finish` method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_flush\_queries**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__flush_queries>`

Called every physics step before
`_step<class_PhysicsServer2DExtension_private_method__step>` to process
all remaining queries.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `flush_queries` method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_free\_rid**(rid: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__free_rid>`

Overridable version of
`PhysicsServer2D.free_rid<class_PhysicsServer2D_method_free_rid>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_process\_info**(process\_info:
`ProcessInfo<enum_PhysicsServer2D_ProcessInfo>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__get_process_info>`

Overridable version of
`PhysicsServer2D.get_process_info<class_PhysicsServer2D_method_get_process_info>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_init**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__init>`

Called when the main loop is initialized and creates a new instance of
this physics server. See also
`MainLoop._initialize<class_MainLoop_private_method__initialize>` and
`_finish<class_PhysicsServer2DExtension_private_method__finish>`.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `init` method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_flushing\_queries**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__is_flushing_queries>`

Overridable method that should return `true` when the physics server is
processing queries. See also
`_flush_queries<class_PhysicsServer2DExtension_private_method__flush_queries>`.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `is_flushing_queries` method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_joint\_clear**(joint: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__joint_clear>`

Overridable version of
`PhysicsServer2D.joint_clear<class_PhysicsServer2D_method_joint_clear>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_joint\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__joint_create>`

Overridable version of
`PhysicsServer2D.joint_create<class_PhysicsServer2D_method_joint_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_joint\_disable\_collisions\_between\_bodies**(joint:
`RID<class_RID>`, disable: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__joint_disable_collisions_between_bodies>`

Overridable version of
`PhysicsServer2D.joint_disable_collisions_between_bodies<class_PhysicsServer2D_method_joint_disable_collisions_between_bodies>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_joint\_get\_param**(joint: `RID<class_RID>`,
param: `JointParam<enum_PhysicsServer2D_JointParam>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__joint_get_param>`

Overridable version of
`PhysicsServer2D.joint_get_param<class_PhysicsServer2D_method_joint_get_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`JointType<enum_PhysicsServer2D_JointType>`
**\_joint\_get\_type**(joint: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__joint_get_type>`

Overridable version of
`PhysicsServer2D.joint_get_type<class_PhysicsServer2D_method_joint_get_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>`
**\_joint\_is\_disabled\_collisions\_between\_bodies**(joint:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__joint_is_disabled_collisions_between_bodies>`

Overridable version of
`PhysicsServer2D.joint_is_disabled_collisions_between_bodies<class_PhysicsServer2D_method_joint_is_disabled_collisions_between_bodies>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_joint\_make\_damped\_spring**(joint:
`RID<class_RID>`, anchor\_a: `Vector2<class_Vector2>`, anchor\_b:
`Vector2<class_Vector2>`, body\_a: `RID<class_RID>`, body\_b:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__joint_make_damped_spring>`

Overridable version of
`PhysicsServer2D.joint_make_damped_spring<class_PhysicsServer2D_method_joint_make_damped_spring>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_joint\_make\_groove**(joint:
`RID<class_RID>`, a\_groove1: `Vector2<class_Vector2>`, a\_groove2:
`Vector2<class_Vector2>`, b\_anchor: `Vector2<class_Vector2>`, body\_a:
`RID<class_RID>`, body\_b: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__joint_make_groove>`

Overridable version of
`PhysicsServer2D.joint_make_groove<class_PhysicsServer2D_method_joint_make_groove>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_joint\_make\_pin**(joint:
`RID<class_RID>`, anchor: `Vector2<class_Vector2>`, body\_a:
`RID<class_RID>`, body\_b: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__joint_make_pin>`

Overridable version of
`PhysicsServer2D.joint_make_pin<class_PhysicsServer2D_method_joint_make_pin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_joint\_set\_param**(joint:
`RID<class_RID>`, param: `JointParam<enum_PhysicsServer2D_JointParam>`,
value: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__joint_set_param>`

Overridable version of
`PhysicsServer2D.joint_set_param<class_PhysicsServer2D_method_joint_set_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_pin\_joint\_get\_flag**(joint: `RID<class_RID>`,
flag: `PinJointFlag<enum_PhysicsServer2D_PinJointFlag>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__pin_joint_get_flag>`

Overridable version of
`PhysicsServer2D.pin_joint_get_flag<class_PhysicsServer2D_method_pin_joint_get_flag>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_pin\_joint\_get\_param**(joint:
`RID<class_RID>`, param:
`PinJointParam<enum_PhysicsServer2D_PinJointParam>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__pin_joint_get_param>`

Overridable version of
`PhysicsServer2D.pin_joint_get_param<class_PhysicsServer2D_method_pin_joint_get_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_pin\_joint\_set\_flag**(joint:
`RID<class_RID>`, flag:
`PinJointFlag<enum_PhysicsServer2D_PinJointFlag>`, enabled:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__pin_joint_set_flag>`

Overridable version of
`PhysicsServer2D.pin_joint_set_flag<class_PhysicsServer2D_method_pin_joint_set_flag>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_pin\_joint\_set\_param**(joint:
`RID<class_RID>`, param:
`PinJointParam<enum_PhysicsServer2D_PinJointParam>`, value:
`float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__pin_joint_set_param>`

Overridable version of
`PhysicsServer2D.pin_joint_set_param<class_PhysicsServer2D_method_pin_joint_set_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_rectangle\_shape\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__rectangle_shape_create>`

Overridable version of
`PhysicsServer2D.rectangle_shape_create<class_PhysicsServer2D_method_rectangle_shape_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_segment\_shape\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__segment_shape_create>`

Overridable version of
`PhysicsServer2D.segment_shape_create<class_PhysicsServer2D_method_segment_shape_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_separation\_ray\_shape\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__separation_ray_shape_create>`

Overridable version of
`PhysicsServer2D.separation_ray_shape_create<class_PhysicsServer2D_method_separation_ray_shape_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_set\_active**(active: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__set_active>`

Overridable version of
`PhysicsServer2D.set_active<class_PhysicsServer2D_method_set_active>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_shape\_collide**(shape\_A: `RID<class_RID>`,
xform\_A: `Transform2D<class_Transform2D>`, motion\_A:
`Vector2<class_Vector2>`, shape\_B: `RID<class_RID>`, xform\_B:
`Transform2D<class_Transform2D>`, motion\_B: `Vector2<class_Vector2>`,
results: `void*`, result\_max: `int<class_int>`, result\_count:
`int32_t*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__shape_collide>`

Given two shapes and their parameters, should return `true` if a
collision between the two would occur, with additional details passed in
`results`.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `shape_collide` method. Corresponds to
`PhysicsDirectSpaceState2D.collide_shape<class_PhysicsDirectSpaceState2D_method_collide_shape>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_shape\_get\_custom\_solver\_bias**(shape:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__shape_get_custom_solver_bias>`

Should return the custom solver bias of the given `shape`, which defines
how much bodies are forced to separate on contact when this shape is
involved.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `shape_get_custom_solver_bias` method. Corresponds to
`Shape2D.custom_solver_bias<class_Shape2D_property_custom_solver_bias>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_shape\_get\_data**(shape: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__shape_get_data>`

Overridable version of
`PhysicsServer2D.shape_get_data<class_PhysicsServer2D_method_shape_get_data>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ShapeType<enum_PhysicsServer2D_ShapeType>`
**\_shape\_get\_type**(shape: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__shape_get_type>`

Overridable version of
`PhysicsServer2D.shape_get_type<class_PhysicsServer2D_method_shape_get_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_shape\_set\_custom\_solver\_bias**(shape:
`RID<class_RID>`, bias: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__shape_set_custom_solver_bias>`

Should set the custom solver bias for the given `shape`. It defines how
much bodies are forced to separate on contact.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `shape_get_custom_solver_bias` method. Corresponds to
`Shape2D.custom_solver_bias<class_Shape2D_property_custom_solver_bias>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_shape\_set\_data**(shape:
`RID<class_RID>`, data: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__shape_set_data>`

Overridable version of
`PhysicsServer2D.shape_set_data<class_PhysicsServer2D_method_shape_set_data>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_space\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__space_create>`

Overridable version of
`PhysicsServer2D.space_create<class_PhysicsServer2D_method_space_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_space\_get\_contact\_count**(space:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__space_get_contact_count>`

Should return how many contacts have occurred during the last physics
step in the given `space`. See also
`_space_get_contacts<class_PhysicsServer2DExtension_private_method__space_get_contacts>`
and
`_space_set_debug_contacts<class_PhysicsServer2DExtension_private_method__space_set_debug_contacts>`.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `space_get_contact_count` method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector2Array<class_PackedVector2Array>`
**\_space\_get\_contacts**(space: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__space_get_contacts>`

Should return the positions of all contacts that have occurred during
the last physics step in the given `space`. See also
`_space_get_contact_count<class_PhysicsServer2DExtension_private_method__space_get_contact_count>`
and
`_space_set_debug_contacts<class_PhysicsServer2DExtension_private_method__space_set_debug_contacts>`.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `space_get_contacts` method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PhysicsDirectSpaceState2D<class_PhysicsDirectSpaceState2D>`
**\_space\_get\_direct\_state**(space: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__space_get_direct_state>`

Overridable version of
`PhysicsServer2D.space_get_direct_state<class_PhysicsServer2D_method_space_get_direct_state>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_space\_get\_param**(space: `RID<class_RID>`,
param: `SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__space_get_param>`

Overridable version of
`PhysicsServer2D.space_get_param<class_PhysicsServer2D_method_space_get_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_space\_is\_active**(space: `RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_private_method__space_is_active>`

Overridable version of
`PhysicsServer2D.space_is_active<class_PhysicsServer2D_method_space_is_active>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_space\_set\_active**(space:
`RID<class_RID>`, active: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__space_set_active>`

Overridable version of
`PhysicsServer2D.space_set_active<class_PhysicsServer2D_method_space_set_active>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_space\_set\_debug\_contacts**(space:
`RID<class_RID>`, max\_contacts: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__space_set_debug_contacts>`

Used internally to allow the given `space` to store contact points, up
to `max_contacts`. This is automatically set for the main
`World2D<class_World2D>`'s space when
`SceneTree.debug_collisions_hint<class_SceneTree_property_debug_collisions_hint>`
is `true`, or by checking "Visible Collision Shapes" in the editor. Only
works in debug builds.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `space_set_debug_contacts` method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_space\_set\_param**(space:
`RID<class_RID>`, param:
`SpaceParameter<enum_PhysicsServer2D_SpaceParameter>`, value:
`float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__space_set_param>`

Overridable version of
`PhysicsServer2D.space_set_param<class_PhysicsServer2D_method_space_set_param>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_step**(step: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__step>`

Called every physics step to process the physics simulation. `step` is
the time elapsed since the last physics step, in seconds. It is usually
the same as
`Node.get_physics_process_delta_time<class_Node_method_get_physics_process_delta_time>`.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `step` method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_sync**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__sync>`

Called to indicate that the physics server is synchronizing and cannot
access physics states if running on a separate thread. See also
`_end_sync<class_PhysicsServer2DExtension_private_method__end_sync>`.

Overridable version of `PhysicsServer2D<class_PhysicsServer2D>`'s
internal `sync` method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_world\_boundary\_shape\_create**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_PhysicsServer2DExtension_private_method__world_boundary_shape_create>`

Overridable version of
`PhysicsServer2D.world_boundary_shape_create<class_PhysicsServer2D_method_world_boundary_shape_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **body\_test\_motion\_is\_excluding\_body**(body:
`RID<class_RID>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_method_body_test_motion_is_excluding_body>`

Returns `true` if the body with the given `RID<class_RID>` is being
excluded from
`_body_test_motion<class_PhysicsServer2DExtension_private_method__body_test_motion>`.
See also `Object.get_instance_id<class_Object_method_get_instance_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **body\_test\_motion\_is\_excluding\_object**(object:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PhysicsServer2DExtension_method_body_test_motion_is_excluding_object>`

Returns `true` if the object with the given instance ID is being
excluded from
`_body_test_motion<class_PhysicsServer2DExtension_private_method__body_test_motion>`.
See also `Object.get_instance_id<class_Object_method_get_instance_id>`.
