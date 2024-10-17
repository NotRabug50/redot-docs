github\_url  
hide

# World3D

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A resource that holds all components of a 3D world, such as a visual
scenario and a physics space.

classref-introduction-group

## Description

Class that has everything pertaining to a world: A physics space, a
visual scenario, and a sound space. 3D nodes register their resources
into the current 3D world.

classref-introduction-group

## Tutorials

-   `Ray-casting <../tutorials/physics/ray-casting>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`CameraAttributes<class_CameraAttributes>` **camera\_attributes**
`🔗<class_World3D_property_camera_attributes>`

classref-property-setget

-   `void (No return value.)` **set\_camera\_attributes**(value:
    `CameraAttributes<class_CameraAttributes>`)
-   `CameraAttributes<class_CameraAttributes>`
    **get\_camera\_attributes**()

The default `CameraAttributes<class_CameraAttributes>` resource to use
if none set on the `Camera3D<class_Camera3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PhysicsDirectSpaceState3D<class_PhysicsDirectSpaceState3D>`
**direct\_space\_state** `🔗<class_World3D_property_direct_space_state>`

classref-property-setget

-   `PhysicsDirectSpaceState3D<class_PhysicsDirectSpaceState3D>`
    **get\_direct\_space\_state**()

Direct access to the world's physics 3D space state. Used for querying
current and potential collisions. When using multi-threaded physics,
access is limited to
`Node._physics_process<class_Node_private_method__physics_process>` in
the main thread.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Environment<class_Environment>` **environment**
`🔗<class_World3D_property_environment>`

classref-property-setget

-   `void (No return value.)` **set\_environment**(value:
    `Environment<class_Environment>`)
-   `Environment<class_Environment>` **get\_environment**()

The World3D's `Environment<class_Environment>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Environment<class_Environment>` **fallback\_environment**
`🔗<class_World3D_property_fallback_environment>`

classref-property-setget

-   `void (No return value.)` **set\_fallback\_environment**(value:
    `Environment<class_Environment>`)
-   `Environment<class_Environment>` **get\_fallback\_environment**()

The World3D's fallback environment will be used if
`environment<class_World3D_property_environment>` fails or is missing.

classref-item-separator

------------------------------------------------------------------------

classref-property

`RID<class_RID>` **navigation\_map**
`🔗<class_World3D_property_navigation_map>`

classref-property-setget

-   `RID<class_RID>` **get\_navigation\_map**()

The `RID<class_RID>` of this world's navigation map. Used by the
`NavigationServer3D<class_NavigationServer3D>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`RID<class_RID>` **scenario** `🔗<class_World3D_property_scenario>`

classref-property-setget

-   `RID<class_RID>` **get\_scenario**()

The World3D's visual scenario.

classref-item-separator

------------------------------------------------------------------------

classref-property

`RID<class_RID>` **space** `🔗<class_World3D_property_space>`

classref-property-setget

-   `RID<class_RID>` **get\_space**()

The World3D's physics space.
