github\_url  
hide

# SoftBody3D

**Inherits:** `MeshInstance3D<class_MeshInstance3D>` **&lt;**
`GeometryInstance3D<class_GeometryInstance3D>` **&lt;**
`VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A deformable 3D physics mesh.

classref-introduction-group

## Description

A deformable 3D physics mesh. Used to create elastic or deformable
objects such as cloth, rubber, or other flexible materials.

Additionally, **SoftBody3D** is subject to wind forces defined in
`Area3D<class_Area3D>` (see
`Area3D.wind_source_path<class_Area3D_property_wind_source_path>`,
`Area3D.wind_force_magnitude<class_Area3D_property_wind_force_magnitude>`,
and
`Area3D.wind_attenuation_factor<class_Area3D_property_wind_attenuation_factor>`).

\*\*Note:\*\* There are many known bugs in **SoftBody3D**. Therefore,
it's not recommended to use them for things that can affect gameplay
(such as trampolines).

classref-introduction-group

## Tutorials

-   `SoftBody <../tutorials/physics/soft_body>`

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

## Enumerations

classref-enumeration

enum **DisableMode**: `🔗<enum_SoftBody3D_DisableMode>`

classref-enumeration-constant

`DisableMode<enum_SoftBody3D_DisableMode>` **DISABLE\_MODE\_REMOVE** =
`0`

When `Node.process_mode<class_Node_property_process_mode>` is set to
`Node.PROCESS_MODE_DISABLED<class_Node_constant_PROCESS_MODE_DISABLED>`,
remove from the physics simulation to stop all physics interactions with
this **SoftBody3D**.

Automatically re-added to the physics simulation when the
`Node<class_Node>` is processed again.

classref-enumeration-constant

`DisableMode<enum_SoftBody3D_DisableMode>`
**DISABLE\_MODE\_KEEP\_ACTIVE** = `1`

When `Node.process_mode<class_Node_property_process_mode>` is set to
`Node.PROCESS_MODE_DISABLED<class_Node_constant_PROCESS_MODE_DISABLED>`,
do not affect the physics simulation.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **collision\_layer** = `1`
`🔗<class_SoftBody3D_property_collision_layer>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_layer**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_collision\_layer**()

The physics layers this SoftBody3D **is in**. Collision objects can
exist in one or more of 32 different layers. See also
`collision_mask<class_SoftBody3D_property_collision_mask>`.

\*\*Note:\*\* Object A can detect a contact with object B only if object
B is in any of the layers that object A scans. See [Collision layers and
masks](../tutorials/physics/physics_introduction.html#collision-layers-and-masks)
in the documentation for more information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **collision\_mask** = `1`
`🔗<class_SoftBody3D_property_collision_mask>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_collision\_mask**()

The physics layers this SoftBody3D **scans**. Collision objects can scan
one or more of 32 different layers. See also
`collision_layer<class_SoftBody3D_property_collision_layer>`.

\*\*Note:\*\* Object A can detect a contact with object B only if object
B is in any of the layers that object A scans. See [Collision layers and
masks](../tutorials/physics/physics_introduction.html#collision-layers-and-masks)
in the documentation for more information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **damping\_coefficient** = `0.01`
`🔗<class_SoftBody3D_property_damping_coefficient>`

classref-property-setget

-   `void (No return value.)` **set\_damping\_coefficient**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_damping\_coefficient**()

The body's damping coefficient. Higher values will slow down the body
more noticeably when forces are applied.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DisableMode<enum_SoftBody3D_DisableMode>` **disable\_mode** = `0`
`🔗<class_SoftBody3D_property_disable_mode>`

classref-property-setget

-   `void (No return value.)` **set\_disable\_mode**(value:
    `DisableMode<enum_SoftBody3D_DisableMode>`)
-   `DisableMode<enum_SoftBody3D_DisableMode>` **get\_disable\_mode**()

Defines the behavior in physics when
`Node.process_mode<class_Node_property_process_mode>` is set to
`Node.PROCESS_MODE_DISABLED<class_Node_constant_PROCESS_MODE_DISABLED>`.
See `DisableMode<enum_SoftBody3D_DisableMode>` for more details about
the different modes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **drag\_coefficient** = `0.0`
`🔗<class_SoftBody3D_property_drag_coefficient>`

classref-property-setget

-   `void (No return value.)` **set\_drag\_coefficient**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_drag\_coefficient**()

The body's drag coefficient. Higher values increase this body's air
resistance.

\*\*Note:\*\* This value is currently unused by Godot's default physics
implementation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_stiffness** = `0.5`
`🔗<class_SoftBody3D_property_linear_stiffness>`

classref-property-setget

-   `void (No return value.)` **set\_linear\_stiffness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_linear\_stiffness**()

Higher values will result in a stiffer body, while lower values will
increase the body's ability to bend. The value can be between `0.0` and
`1.0` (inclusive).

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **parent\_collision\_ignore** =
`NodePath("")` `🔗<class_SoftBody3D_property_parent_collision_ignore>`

classref-property-setget

-   `void (No return value.)` **set\_parent\_collision\_ignore**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_parent\_collision\_ignore**()

`NodePath<class_NodePath>` to a
`CollisionObject3D<class_CollisionObject3D>` this SoftBody3D should
avoid clipping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pressure\_coefficient** = `0.0`
`🔗<class_SoftBody3D_property_pressure_coefficient>`

classref-property-setget

-   `void (No return value.)` **set\_pressure\_coefficient**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pressure\_coefficient**()

The pressure coefficient of this soft body. Simulate pressure build-up
from inside this body. Higher values increase the strength of this
effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ray\_pickable** = `true`
`🔗<class_SoftBody3D_property_ray_pickable>`

classref-property-setget

-   `void (No return value.)` **set\_ray\_pickable**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_ray\_pickable**()

If `true`, the **SoftBody3D** will respond to
`RayCast3D<class_RayCast3D>`s.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **simulation\_precision** = `5`
`🔗<class_SoftBody3D_property_simulation_precision>`

classref-property-setget

-   `void (No return value.)` **set\_simulation\_precision**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_simulation\_precision**()

Increasing this value will improve the resulting simulation, but can
affect performance. Use with care.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **total\_mass** = `1.0`
`🔗<class_SoftBody3D_property_total_mass>`

classref-property-setget

-   `void (No return value.)` **set\_total\_mass**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_total\_mass**()

The SoftBody3D's mass.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_collision\_exception\_with**(body:
`Node<class_Node>`)
`🔗<class_SoftBody3D_method_add_collision_exception_with>`

Adds a body to the list of bodies that this body can't collide with.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`PhysicsBody3D<class_PhysicsBody3D>`\]
**get\_collision\_exceptions**()
`🔗<class_SoftBody3D_method_get_collision_exceptions>`

Returns an array of nodes that were added as collision exceptions for
this body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_collision\_layer\_value**(layer\_number:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SoftBody3D_method_get_collision_layer_value>`

Returns whether or not the specified layer of the
`collision_layer<class_SoftBody3D_property_collision_layer>` is enabled,
given a `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_collision\_mask\_value**(layer\_number:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SoftBody3D_method_get_collision_mask_value>`

Returns whether or not the specified layer of the
`collision_mask<class_SoftBody3D_property_collision_mask>` is enabled,
given a `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_physics\_rid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SoftBody3D_method_get_physics_rid>`

Returns the internal `RID<class_RID>` used by the
`PhysicsServer3D<class_PhysicsServer3D>` for this body.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_point\_transform**(point\_index:
`int<class_int>`) `🔗<class_SoftBody3D_method_get_point_transform>`

Returns local translation of a vertex in the surface array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_point\_pinned**(point\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SoftBody3D_method_is_point_pinned>`

Returns `true` if vertex is set to pinned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_collision\_exception\_with**(body:
`Node<class_Node>`)
`🔗<class_SoftBody3D_method_remove_collision_exception_with>`

Removes a body from the list of bodies that this body can't collide
with.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_collision\_layer\_value**(layer\_number: `int<class_int>`, value:
`bool<class_bool>`)
`🔗<class_SoftBody3D_method_set_collision_layer_value>`

Based on `value`, enables or disables the specified layer in the
`collision_layer<class_SoftBody3D_property_collision_layer>`, given a
`layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_collision\_mask\_value**(layer\_number:
`int<class_int>`, value: `bool<class_bool>`)
`🔗<class_SoftBody3D_method_set_collision_mask_value>`

Based on `value`, enables or disables the specified layer in the
`collision_mask<class_SoftBody3D_property_collision_mask>`, given a
`layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_point\_pinned**(point\_index:
`int<class_int>`, pinned: `bool<class_bool>`, attachment\_path:
`NodePath<class_NodePath>` = NodePath(""), insert\_at: `int<class_int>`
= -1) `🔗<class_SoftBody3D_method_set_point_pinned>`

Sets the pinned state of a surface vertex. When set to `true`, the
optional `attachment_path` can define a `Node3D<class_Node3D>` the
pinned vertex will be attached to.
