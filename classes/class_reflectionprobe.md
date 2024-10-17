github\_url  
hide

# ReflectionProbe

**Inherits:** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Captures its surroundings to create fast, accurate reflections from a
given point.

classref-introduction-group

## Description

Captures its surroundings as a cubemap, and stores versions of it with
increasing levels of blur to simulate different material roughnesses.

The **ReflectionProbe** is used to create high-quality reflections at a
low performance cost (when
`update_mode<class_ReflectionProbe_property_update_mode>` is
`UPDATE_ONCE<class_ReflectionProbe_constant_UPDATE_ONCE>`).
**ReflectionProbe**s can be blended together and with the rest of the
scene smoothly. **ReflectionProbe**s can also be combined with
`VoxelGI<class_VoxelGI>`, SDFGI
(`Environment.sdfgi_enabled<class_Environment_property_sdfgi_enabled>`)
and screen-space reflections
(`Environment.ssr_enabled<class_Environment_property_ssr_enabled>`) to
get more accurate reflections in specific areas. **ReflectionProbe**s
render all objects within their
`cull_mask<class_ReflectionProbe_property_cull_mask>`, so updating them
can be quite expensive. It is best to update them once with the
important static objects and then leave them as-is.

\*\*Note:\*\* Unlike `VoxelGI<class_VoxelGI>` and SDFGI,
**ReflectionProbe**s only source their environment from a
`WorldEnvironment<class_WorldEnvironment>` node. If you specify an
`Environment<class_Environment>` resource within a
`Camera3D<class_Camera3D>` node, it will be ignored by the
**ReflectionProbe**. This can lead to incorrect lighting within the
**ReflectionProbe**.

\*\*Note:\*\* Reflection probes are only supported in the Forward+ and
Mobile rendering methods, not Compatibility. When using the Mobile
rendering method, only 8 reflection probes can be displayed on each mesh
resource. Attempting to display more than 8 reflection probes on a
single mesh resource will result in reflection probes flickering in and
out as the camera moves.

\*\*Note:\*\* When using the Mobile rendering method, reflection probes
will only correctly affect meshes whose visibility AABB intersects with
the reflection probe's AABB. If using a shader to deform the mesh in a
way that makes it go outside its AABB,
`GeometryInstance3D.extra_cull_margin<class_GeometryInstance3D_property_extra_cull_margin>`
must be increased on the mesh. Otherwise, the reflection probe may not
be visible on the mesh.

classref-introduction-group

## Tutorials

-   `Reflection probes <../tutorials/3d/global_illumination/reflection_probes>`

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

enum **UpdateMode**: `🔗<enum_ReflectionProbe_UpdateMode>`

classref-enumeration-constant

`UpdateMode<enum_ReflectionProbe_UpdateMode>` **UPDATE\_ONCE** = `0`

Update the probe once on the next frame (recommended for most objects).
The corresponding radiance map will be generated over the following six
frames. This takes more time to update than
`UPDATE_ALWAYS<class_ReflectionProbe_constant_UPDATE_ALWAYS>`, but it
has a lower performance cost and can result in higher-quality
reflections. The ReflectionProbe is updated when its transform changes,
but not when nearby geometry changes. You can force a
**ReflectionProbe** update by moving the **ReflectionProbe** slightly in
any direction.

classref-enumeration-constant

`UpdateMode<enum_ReflectionProbe_UpdateMode>` **UPDATE\_ALWAYS** = `1`

Update the probe every frame. This provides better results for
fast-moving dynamic objects (such as cars). However, it has a
significant performance cost. Due to the cost, it's recommended to only
use one ReflectionProbe with
`UPDATE_ALWAYS<class_ReflectionProbe_constant_UPDATE_ALWAYS>` at most
per scene. For all other use cases, use
`UPDATE_ONCE<class_ReflectionProbe_constant_UPDATE_ONCE>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AmbientMode**: `🔗<enum_ReflectionProbe_AmbientMode>`

classref-enumeration-constant

`AmbientMode<enum_ReflectionProbe_AmbientMode>` **AMBIENT\_DISABLED** =
`0`

Do not apply any ambient lighting inside the **ReflectionProbe**'s box
defined by its `size<class_ReflectionProbe_property_size>`.

classref-enumeration-constant

`AmbientMode<enum_ReflectionProbe_AmbientMode>` **AMBIENT\_ENVIRONMENT**
= `1`

Apply automatically-sourced environment lighting inside the
**ReflectionProbe**'s box defined by its
`size<class_ReflectionProbe_property_size>`.

classref-enumeration-constant

`AmbientMode<enum_ReflectionProbe_AmbientMode>` **AMBIENT\_COLOR** = `2`

Apply custom ambient lighting inside the **ReflectionProbe**'s box
defined by its `size<class_ReflectionProbe_property_size>`. See
`ambient_color<class_ReflectionProbe_property_ambient_color>` and
`ambient_color_energy<class_ReflectionProbe_property_ambient_color_energy>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Color<class_Color>` **ambient\_color** = `Color(0, 0, 0, 1)`
`🔗<class_ReflectionProbe_property_ambient_color>`

classref-property-setget

-   `void (No return value.)` **set\_ambient\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_ambient\_color**()

The custom ambient color to use within the **ReflectionProbe**'s box
defined by its `size<class_ReflectionProbe_property_size>`. Only
effective if `ambient_mode<class_ReflectionProbe_property_ambient_mode>`
is `AMBIENT_COLOR<class_ReflectionProbe_constant_AMBIENT_COLOR>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ambient\_color\_energy** = `1.0`
`🔗<class_ReflectionProbe_property_ambient_color_energy>`

classref-property-setget

-   `void (No return value.)` **set\_ambient\_color\_energy**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ambient\_color\_energy**()

The custom ambient color energy to use within the **ReflectionProbe**'s
box defined by its `size<class_ReflectionProbe_property_size>`. Only
effective if `ambient_mode<class_ReflectionProbe_property_ambient_mode>`
is `AMBIENT_COLOR<class_ReflectionProbe_constant_AMBIENT_COLOR>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AmbientMode<enum_ReflectionProbe_AmbientMode>` **ambient\_mode** = `1`
`🔗<class_ReflectionProbe_property_ambient_mode>`

classref-property-setget

-   `void (No return value.)` **set\_ambient\_mode**(value:
    `AmbientMode<enum_ReflectionProbe_AmbientMode>`)
-   `AmbientMode<enum_ReflectionProbe_AmbientMode>`
    **get\_ambient\_mode**()

The ambient color to use within the **ReflectionProbe**'s box defined by
its `size<class_ReflectionProbe_property_size>`. The ambient color will
smoothly blend with other **ReflectionProbe**s and the rest of the scene
(outside the **ReflectionProbe**'s box defined by its
`size<class_ReflectionProbe_property_size>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **box\_projection** = `false`
`🔗<class_ReflectionProbe_property_box_projection>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_box\_projection**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_box\_projection\_enabled**()

If `true`, enables box projection. This makes reflections look more
correct in rectangle-shaped rooms by offsetting the reflection center
depending on the camera's location.

\*\*Note:\*\* To better fit rectangle-shaped rooms that are not aligned
to the grid, you can rotate the **ReflectionProbe** node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **cull\_mask** = `1048575`
`🔗<class_ReflectionProbe_property_cull_mask>`

classref-property-setget

-   `void (No return value.)` **set\_cull\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_cull\_mask**()

Sets the cull mask which determines what objects are drawn by this
probe. Every `VisualInstance3D<class_VisualInstance3D>` with a layer
included in this cull mask will be rendered by the probe. It is best to
only include large objects which are likely to take up a lot of space in
the reflection in order to save on rendering cost.

This can also be used to prevent an object from reflecting upon itself
(for instance, a **ReflectionProbe** centered on a vehicle).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **enable\_shadows** = `false`
`🔗<class_ReflectionProbe_property_enable_shadows>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_shadows**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **are\_shadows\_enabled**()

If `true`, computes shadows in the reflection probe. This makes the
reflection probe slower to render; you may want to disable this if using
the `UPDATE_ALWAYS<class_ReflectionProbe_constant_UPDATE_ALWAYS>`
`update_mode<class_ReflectionProbe_property_update_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **intensity** = `1.0`
`🔗<class_ReflectionProbe_property_intensity>`

classref-property-setget

-   `void (No return value.)` **set\_intensity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_intensity**()

Defines the reflection intensity. Intensity modulates the strength of
the reflection.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interior** = `false`
`🔗<class_ReflectionProbe_property_interior>`

classref-property-setget

-   `void (No return value.)` **set\_as\_interior**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_set\_as\_interior**()

If `true`, reflections will ignore sky contribution.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **max\_distance** = `0.0`
`🔗<class_ReflectionProbe_property_max_distance>`

classref-property-setget

-   `void (No return value.)` **set\_max\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_max\_distance**()

The maximum distance away from the **ReflectionProbe** an object can be
before it is culled. Decrease this to improve performance, especially
when using the
`UPDATE_ALWAYS<class_ReflectionProbe_constant_UPDATE_ALWAYS>`
`update_mode<class_ReflectionProbe_property_update_mode>`.

\*\*Note:\*\* The maximum reflection distance is always at least equal
to the probe's extents. This means that decreasing
`max_distance<class_ReflectionProbe_property_max_distance>` will not
always cull objects from reflections, especially if the reflection
probe's box defined by its `size<class_ReflectionProbe_property_size>`
is already large.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **mesh\_lod\_threshold** = `1.0`
`🔗<class_ReflectionProbe_property_mesh_lod_threshold>`

classref-property-setget

-   `void (No return value.)` **set\_mesh\_lod\_threshold**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_mesh\_lod\_threshold**()

The automatic LOD bias to use for meshes rendered within the
**ReflectionProbe** (this is analog to
`Viewport.mesh_lod_threshold<class_Viewport_property_mesh_lod_threshold>`).
Higher values will use less detailed versions of meshes that have LOD
variations generated. If set to `0.0`, automatic LOD is disabled.
Increase
`mesh_lod_threshold<class_ReflectionProbe_property_mesh_lod_threshold>`
to improve performance at the cost of geometry detail, especially when
using the `UPDATE_ALWAYS<class_ReflectionProbe_constant_UPDATE_ALWAYS>`
`update_mode<class_ReflectionProbe_property_update_mode>`.

\*\*Note:\*\*
`mesh_lod_threshold<class_ReflectionProbe_property_mesh_lod_threshold>`
does not affect `GeometryInstance3D<class_GeometryInstance3D>`
visibility ranges (also known as "manual" LOD or hierarchical LOD).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **origin\_offset** = `Vector3(0, 0, 0)`
`🔗<class_ReflectionProbe_property_origin_offset>`

classref-property-setget

-   `void (No return value.)` **set\_origin\_offset**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_origin\_offset**()

Sets the origin offset to be used when this **ReflectionProbe** is in
`box_projection<class_ReflectionProbe_property_box_projection>` mode.
This can be set to a non-zero value to ensure a reflection fits a
rectangle-shaped room, while reducing the number of objects that "get in
the way" of the reflection.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **reflection\_mask** = `1048575`
`🔗<class_ReflectionProbe_property_reflection_mask>`

classref-property-setget

-   `void (No return value.)` **set\_reflection\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_reflection\_mask**()

Sets the reflection mask which determines what objects have reflections
applied from this probe. Every
`VisualInstance3D<class_VisualInstance3D>` with a layer included in this
reflection mask will have reflections applied from this probe. See also
`cull_mask<class_ReflectionProbe_property_cull_mask>`, which can be used
to exclude objects from appearing in the reflection while still making
them affected by the **ReflectionProbe**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **size** = `Vector3(20, 20, 20)`
`🔗<class_ReflectionProbe_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_size**()

The size of the reflection probe. The larger the size, the more space
covered by the probe, which will lower the perceived resolution. It is
best to keep the size only as large as you need it.

\*\*Note:\*\* To better fit areas that are not aligned to the grid, you
can rotate the **ReflectionProbe** node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`UpdateMode<enum_ReflectionProbe_UpdateMode>` **update\_mode** = `0`
`🔗<class_ReflectionProbe_property_update_mode>`

classref-property-setget

-   `void (No return value.)` **set\_update\_mode**(value:
    `UpdateMode<enum_ReflectionProbe_UpdateMode>`)
-   `UpdateMode<enum_ReflectionProbe_UpdateMode>`
    **get\_update\_mode**()

Sets how frequently the **ReflectionProbe** is updated. Can be
`UPDATE_ONCE<class_ReflectionProbe_constant_UPDATE_ONCE>` or
`UPDATE_ALWAYS<class_ReflectionProbe_constant_UPDATE_ALWAYS>`.
