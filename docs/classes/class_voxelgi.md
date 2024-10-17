github\_url  
hide

# VoxelGI

**Inherits:** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Real-time global illumination (GI) probe.

classref-introduction-group

## Description

**VoxelGI**s are used to provide high-quality real-time indirect light
and reflections to scenes. They precompute the effect of objects that
emit light and the effect of static geometry to simulate the behavior of
complex light in real-time. **VoxelGI**s need to be baked before having
a visible effect. However, once baked, dynamic objects will receive
light from them. Furthermore, lights can be fully dynamic or baked.

\*\*Note:\*\* **VoxelGI** is only supported in the Forward+ rendering
method, not Mobile or Compatibility.

\*\*Procedural generation:\*\* **VoxelGI** can be baked in an exported
project, which makes it suitable for procedurally generated or
user-built levels as long as all the geometry is generated in advance.
For games where geometry is generated at any time during gameplay, SDFGI
is more suitable (see
`Environment.sdfgi_enabled<class_Environment_property_sdfgi_enabled>`).

\*\*Performance:\*\* **VoxelGI** is relatively demanding on the GPU and
is not suited to low-end hardware such as integrated graphics (consider
`LightmapGI<class_LightmapGI>` instead). To improve performance, adjust
`ProjectSettings.rendering/global_illumination/voxel_gi/quality<class_ProjectSettings_property_rendering/global_illumination/voxel_gi/quality>`
and enable
`ProjectSettings.rendering/global_illumination/gi/use_half_resolution<class_ProjectSettings_property_rendering/global_illumination/gi/use_half_resolution>`
in the Project Settings. To provide a fallback for low-end hardware,
consider adding an option to disable **VoxelGI** in your project's
options menus. A **VoxelGI** node can be disabled by hiding it.

\*\*Note:\*\* Meshes should have sufficiently thick walls to avoid light
leaks (avoid one-sided walls). For interior levels, enclose your level
geometry in a sufficiently large box and bridge the loops to close the
mesh. To further prevent light leaks, you can also strategically place
temporary `MeshInstance3D<class_MeshInstance3D>` nodes with their
`GeometryInstance3D.gi_mode<class_GeometryInstance3D_property_gi_mode>`
set to
`GeometryInstance3D.GI_MODE_STATIC<class_GeometryInstance3D_constant_GI_MODE_STATIC>`.
These temporary nodes can then be hidden after baking the **VoxelGI**
node.

classref-introduction-group

## Tutorials

-   `Using Voxel global illumination <../tutorials/3d/global_illumination/using_voxel_gi>`
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Subdiv**: `🔗<enum_VoxelGI_Subdiv>`

classref-enumeration-constant

`Subdiv<enum_VoxelGI_Subdiv>` **SUBDIV\_64** = `0`

Use 64 subdivisions. This is the lowest quality setting, but the
fastest. Use it if you can, but especially use it on lower-end hardware.

classref-enumeration-constant

`Subdiv<enum_VoxelGI_Subdiv>` **SUBDIV\_128** = `1`

Use 128 subdivisions. This is the default quality setting.

classref-enumeration-constant

`Subdiv<enum_VoxelGI_Subdiv>` **SUBDIV\_256** = `2`

Use 256 subdivisions.

classref-enumeration-constant

`Subdiv<enum_VoxelGI_Subdiv>` **SUBDIV\_512** = `3`

Use 512 subdivisions. This is the highest quality setting, but the
slowest. On lower-end hardware, this could cause the GPU to stall.

classref-enumeration-constant

`Subdiv<enum_VoxelGI_Subdiv>` **SUBDIV\_MAX** = `4`

Represents the size of the `Subdiv<enum_VoxelGI_Subdiv>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`CameraAttributes<class_CameraAttributes>` **camera\_attributes**
`🔗<class_VoxelGI_property_camera_attributes>`

classref-property-setget

-   `void (No return value.)` **set\_camera\_attributes**(value:
    `CameraAttributes<class_CameraAttributes>`)
-   `CameraAttributes<class_CameraAttributes>`
    **get\_camera\_attributes**()

The `CameraAttributes<class_CameraAttributes>` resource that specifies
exposure levels to bake at. Auto-exposure and non exposure properties
will be ignored. Exposure settings should be used to reduce the dynamic
range present when baking. If exposure is too high, the **VoxelGI** will
have banding artifacts or may have over-exposure artifacts.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VoxelGIData<class_VoxelGIData>` **data**
`🔗<class_VoxelGI_property_data>`

classref-property-setget

-   `void (No return value.)` **set\_probe\_data**(value:
    `VoxelGIData<class_VoxelGIData>`)
-   `VoxelGIData<class_VoxelGIData>` **get\_probe\_data**()

The `VoxelGIData<class_VoxelGIData>` resource that holds the data for
this **VoxelGI**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **size** = `Vector3(20, 20, 20)`
`🔗<class_VoxelGI_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_size**()

The size of the area covered by the **VoxelGI**. If you make the size
larger without increasing the subdivisions with
`subdiv<class_VoxelGI_property_subdiv>`, the size of each cell will
increase and result in lower detailed lighting.

\*\*Note:\*\* Size is clamped to 1.0 unit or more on each axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Subdiv<enum_VoxelGI_Subdiv>` **subdiv** = `1`
`🔗<class_VoxelGI_property_subdiv>`

classref-property-setget

-   `void (No return value.)` **set\_subdiv**(value:
    `Subdiv<enum_VoxelGI_Subdiv>`)
-   `Subdiv<enum_VoxelGI_Subdiv>` **get\_subdiv**()

Number of times to subdivide the grid that the **VoxelGI** operates on.
A higher number results in finer detail and thus higher visual quality,
while lower numbers result in better performance.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **bake**(from\_node: `Node<class_Node>` =
null, create\_visual\_debug: `bool<class_bool>` = false)
`🔗<class_VoxelGI_method_bake>`

Bakes the effect from all
`GeometryInstance3D<class_GeometryInstance3D>`s marked with
`GeometryInstance3D.GI_MODE_STATIC<class_GeometryInstance3D_constant_GI_MODE_STATIC>`
and `Light3D<class_Light3D>`s marked with either
`Light3D.BAKE_STATIC<class_Light3D_constant_BAKE_STATIC>` or
`Light3D.BAKE_DYNAMIC<class_Light3D_constant_BAKE_DYNAMIC>`. If
`create_visual_debug` is `true`, after baking the light, this will
generate a `MultiMesh<class_MultiMesh>` that has a cube representing
each solid cell with each cube colored to the cell's albedo color. This
can be used to visualize the **VoxelGI**'s data and debug any issues
that may be occurring.

\*\*Note:\*\* `bake<class_VoxelGI_method_bake>` works from the editor
and in exported projects. This makes it suitable for procedurally
generated or user-built levels. Baking a **VoxelGI** node generally
takes from 5 to 20 seconds in most scenes. Reducing
`subdiv<class_VoxelGI_property_subdiv>` can speed up baking.

\*\*Note:\*\* `GeometryInstance3D<class_GeometryInstance3D>`s and
`Light3D<class_Light3D>`s must be fully ready before
`bake<class_VoxelGI_method_bake>` is called. If you are procedurally
creating those and some meshes or lights are missing from your baked
**VoxelGI**, use `call_deferred("bake")` instead of calling
`bake<class_VoxelGI_method_bake>` directly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **debug\_bake**()
`🔗<class_VoxelGI_method_debug_bake>`

Calls `bake<class_VoxelGI_method_bake>` with `create_visual_debug`
enabled.
