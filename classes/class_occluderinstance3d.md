github\_url  
hide

# OccluderInstance3D

**Inherits:** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Provides occlusion culling for 3D nodes, which improves performance in
closed areas.

classref-introduction-group

## Description

Occlusion culling can improve rendering performance in closed/semi-open
areas by hiding geometry that is occluded by other objects.

The occlusion culling system is mostly static. **OccluderInstance3D**s
can be moved or hidden at run-time, but doing so will trigger a
background recomputation that can take several frames. It is recommended
to only move **OccluderInstance3D**s sporadically (e.g. for procedural
generation purposes), rather than doing so every frame.

The occlusion culling system works by rendering the occluders on the CPU
in parallel using [Embree](https://www.embree.org/), drawing the result
to a low-resolution buffer then using this to cull 3D nodes
individually. In the 3D editor, you can preview the occlusion culling
buffer by choosing **Perspective &gt; Debug Advanced... &gt; Occlusion
Culling Buffer** in the top-left corner of the 3D viewport. The
occlusion culling buffer quality can be adjusted in the Project
Settings.

\*\*Baking:\*\* Select an **OccluderInstance3D** node, then use the
**Bake Occluders** button at the top of the 3D editor. Only opaque
materials will be taken into account; transparent materials
(alpha-blended or alpha-tested) will be ignored by the occluder
generation.

\*\*Note:\*\* Occlusion culling is only effective if
`ProjectSettings.rendering/occlusion_culling/use_occlusion_culling<class_ProjectSettings_property_rendering/occlusion_culling/use_occlusion_culling>`
is `true`. Enabling occlusion culling has a cost on the CPU. Only enable
occlusion culling if you actually plan to use it. Large open scenes with
few or no objects blocking the view will generally not benefit much from
occlusion culling. Large open scenes generally benefit more from mesh
LOD and visibility ranges
(`GeometryInstance3D.visibility_range_begin<class_GeometryInstance3D_property_visibility_range_begin>`
and
`GeometryInstance3D.visibility_range_end<class_GeometryInstance3D_property_visibility_range_end>`)
compared to occlusion culling.

\*\*Note:\*\* Due to memory constraints, occlusion culling is not
supported by default in Web export templates. It can be enabled by
compiling custom Web export templates with `module_raycast_enabled=yes`.

classref-introduction-group

## Tutorials

-   `Occlusion culling <../tutorials/3d/occlusion_culling>`

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

## Property Descriptions

classref-property

`int<class_int>` **bake\_mask** = `4294967295`
`🔗<class_OccluderInstance3D_property_bake_mask>`

classref-property-setget

-   `void (No return value.)` **set\_bake\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_bake\_mask**()

The visual layers to account for when baking for occluders. Only
`MeshInstance3D<class_MeshInstance3D>`s whose
`VisualInstance3D.layers<class_VisualInstance3D_property_layers>` match
with this `bake_mask<class_OccluderInstance3D_property_bake_mask>` will
be included in the generated occluder mesh. By default, all objects with
*opaque* materials are taken into account for the occluder baking.

To improve performance and avoid artifacts, it is recommended to exclude
dynamic objects, small objects and fixtures from the baking process by
moving them to a separate visual layer and excluding this layer in
`bake_mask<class_OccluderInstance3D_property_bake_mask>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **bake\_simplification\_distance** = `0.1`
`🔗<class_OccluderInstance3D_property_bake_simplification_distance>`

classref-property-setget

-   `void (No return value.)`
    **set\_bake\_simplification\_distance**(value: `float<class_float>`)
-   `float<class_float>` **get\_bake\_simplification\_distance**()

The simplification distance to use for simplifying the generated
occluder polygon (in 3D units). Higher values result in a less detailed
occluder mesh, which improves performance but reduces culling accuracy.

The occluder geometry is rendered on the CPU, so it is important to keep
its geometry as simple as possible. Since the buffer is rendered at a
low resolution, less detailed occluder meshes generally still work well.
The default value is fairly aggressive, so you may have to decrease it
if you run into false negatives (objects being occluded even though they
are visible by the camera). A value of `0.01` will act conservatively,
and will keep geometry *perceptually* unaffected in the occlusion
culling buffer. Depending on the scene, a value of `0.01` may still
simplify the mesh noticeably compared to disabling simplification
entirely.

Setting this to `0.0` disables simplification entirely, but vertices in
the exact same position will still be merged. The mesh will also be
re-indexed to reduce both the number of vertices and indices.

\*\*Note:\*\* This uses the [meshoptimizer](https://meshoptimizer.org/)
library under the hood, similar to LOD generation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Occluder3D<class_Occluder3D>` **occluder**
`🔗<class_OccluderInstance3D_property_occluder>`

classref-property-setget

-   `void (No return value.)` **set\_occluder**(value:
    `Occluder3D<class_Occluder3D>`)
-   `Occluder3D<class_Occluder3D>` **get\_occluder**()

The occluder resource for this **OccluderInstance3D**. You can generate
an occluder resource by selecting an **OccluderInstance3D** node then
using the **Bake Occluders** button at the top of the editor.

You can also draw your own 2D occluder polygon by adding a new
`PolygonOccluder3D<class_PolygonOccluder3D>` resource to the
`occluder<class_OccluderInstance3D_property_occluder>` property in the
Inspector.

Alternatively, you can select a primitive occluder to use:
`QuadOccluder3D<class_QuadOccluder3D>`,
`BoxOccluder3D<class_BoxOccluder3D>` or
`SphereOccluder3D<class_SphereOccluder3D>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **get\_bake\_mask\_value**(layer\_number:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OccluderInstance3D_method_get_bake_mask_value>`

Returns whether or not the specified layer of the
`bake_mask<class_OccluderInstance3D_property_bake_mask>` is enabled,
given a `layer_number` between 1 and 32.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bake\_mask\_value**(layer\_number:
`int<class_int>`, value: `bool<class_bool>`)
`🔗<class_OccluderInstance3D_method_set_bake_mask_value>`

Based on `value`, enables or disables the specified layer in the
`bake_mask<class_OccluderInstance3D_property_bake_mask>`, given a
`layer_number` between 1 and 32.
