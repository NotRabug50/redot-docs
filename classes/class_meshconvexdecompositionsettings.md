github\_url  
hide

# MeshConvexDecompositionSettings

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Parameters to be used with a `Mesh<class_Mesh>` convex decomposition
operation.

classref-introduction-group

## Description

Parameters to be used with a `Mesh<class_Mesh>` convex decomposition
operation.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Mode**: `🔗<enum_MeshConvexDecompositionSettings_Mode>`

classref-enumeration-constant

`Mode<enum_MeshConvexDecompositionSettings_Mode>`
**CONVEX\_DECOMPOSITION\_MODE\_VOXEL** = `0`

Constant for voxel-based approximate convex decomposition.

classref-enumeration-constant

`Mode<enum_MeshConvexDecompositionSettings_Mode>`
**CONVEX\_DECOMPOSITION\_MODE\_TETRAHEDRON** = `1`

Constant for tetrahedron-based approximate convex decomposition.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **convex\_hull\_approximation** = `true`
`🔗<class_MeshConvexDecompositionSettings_property_convex_hull_approximation>`

classref-property-setget

-   `void (No return value.)`
    **set\_convex\_hull\_approximation**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_convex\_hull\_approximation**()

If `true`, uses approximation for computing convex hulls.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **convex\_hull\_downsampling** = `4`
`🔗<class_MeshConvexDecompositionSettings_property_convex_hull_downsampling>`

classref-property-setget

-   `void (No return value.)` **set\_convex\_hull\_downsampling**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_convex\_hull\_downsampling**()

Controls the precision of the convex-hull generation process during the
clipping plane selection stage. Ranges from `1` to `16`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **max\_concavity** = `1.0`
`🔗<class_MeshConvexDecompositionSettings_property_max_concavity>`

classref-property-setget

-   `void (No return value.)` **set\_max\_concavity**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_max\_concavity**()

Maximum concavity. Ranges from `0.0` to `1.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_convex\_hulls** = `1`
`🔗<class_MeshConvexDecompositionSettings_property_max_convex_hulls>`

classref-property-setget

-   `void (No return value.)` **set\_max\_convex\_hulls**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_convex\_hulls**()

The maximum number of convex hulls to produce from the merge operation.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_num\_vertices\_per\_convex\_hull** = `32`
`🔗<class_MeshConvexDecompositionSettings_property_max_num_vertices_per_convex_hull>`

classref-property-setget

-   `void (No return value.)`
    **set\_max\_num\_vertices\_per\_convex\_hull**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_num\_vertices\_per\_convex\_hull**()

Controls the maximum number of triangles per convex-hull. Ranges from
`4` to `1024`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **min\_volume\_per\_convex\_hull** = `0.0001`
`🔗<class_MeshConvexDecompositionSettings_property_min_volume_per_convex_hull>`

classref-property-setget

-   `void (No return value.)`
    **set\_min\_volume\_per\_convex\_hull**(value: `float<class_float>`)
-   `float<class_float>` **get\_min\_volume\_per\_convex\_hull**()

Controls the adaptive sampling of the generated convex-hulls. Ranges
from `0.0` to `0.01`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Mode<enum_MeshConvexDecompositionSettings_Mode>` **mode** = `0`
`🔗<class_MeshConvexDecompositionSettings_property_mode>`

classref-property-setget

-   `void (No return value.)` **set\_mode**(value:
    `Mode<enum_MeshConvexDecompositionSettings_Mode>`)
-   `Mode<enum_MeshConvexDecompositionSettings_Mode>` **get\_mode**()

Mode for the approximate convex decomposition.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **normalize\_mesh** = `false`
`🔗<class_MeshConvexDecompositionSettings_property_normalize_mesh>`

classref-property-setget

-   `void (No return value.)` **set\_normalize\_mesh**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_normalize\_mesh**()

If `true`, normalizes the mesh before applying the convex decomposition.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **plane\_downsampling** = `4`
`🔗<class_MeshConvexDecompositionSettings_property_plane_downsampling>`

classref-property-setget

-   `void (No return value.)` **set\_plane\_downsampling**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_plane\_downsampling**()

Controls the granularity of the search for the "best" clipping plane.
Ranges from `1` to `16`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **project\_hull\_vertices** = `true`
`🔗<class_MeshConvexDecompositionSettings_property_project_hull_vertices>`

classref-property-setget

-   `void (No return value.)` **set\_project\_hull\_vertices**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_project\_hull\_vertices**()

If `true`, projects output convex hull vertices onto the original source
mesh to increase floating-point accuracy of the results.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **resolution** = `10000`
`🔗<class_MeshConvexDecompositionSettings_property_resolution>`

classref-property-setget

-   `void (No return value.)` **set\_resolution**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_resolution**()

Maximum number of voxels generated during the voxelization stage.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **revolution\_axes\_clipping\_bias** = `0.05`
`🔗<class_MeshConvexDecompositionSettings_property_revolution_axes_clipping_bias>`

classref-property-setget

-   `void (No return value.)`
    **set\_revolution\_axes\_clipping\_bias**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_revolution\_axes\_clipping\_bias**()

Controls the bias toward clipping along revolution axes. Ranges from
`0.0` to `1.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **symmetry\_planes\_clipping\_bias** = `0.05`
`🔗<class_MeshConvexDecompositionSettings_property_symmetry_planes_clipping_bias>`

classref-property-setget

-   `void (No return value.)`
    **set\_symmetry\_planes\_clipping\_bias**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_symmetry\_planes\_clipping\_bias**()

Controls the bias toward clipping along symmetry planes. Ranges from
`0.0` to `1.0`.
