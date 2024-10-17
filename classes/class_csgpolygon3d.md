github\_url  
hide

# CSGPolygon3D

**Inherits:** `CSGPrimitive3D<class_CSGPrimitive3D>` **&lt;**
`CSGShape3D<class_CSGShape3D>` **&lt;**
`GeometryInstance3D<class_GeometryInstance3D>` **&lt;**
`VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Extrudes a 2D polygon shape to create a 3D mesh.

classref-introduction-group

## Description

An array of 2D points is extruded to quickly and easily create a variety
of 3D meshes. See also `CSGMesh3D<class_CSGMesh3D>` for using 3D meshes
as CSG nodes.

\*\*Note:\*\* CSG nodes are intended to be used for level prototyping.
Creating CSG nodes has a significant CPU cost compared to creating a
`MeshInstance3D<class_MeshInstance3D>` with a
`PrimitiveMesh<class_PrimitiveMesh>`. Moving a CSG node within another
CSG node also has a significant CPU cost, so it should be avoided during
gameplay.

classref-introduction-group

## Tutorials

-   `Prototyping levels with CSG <../tutorials/3d/csg_tools>`

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

enum **Mode**: `🔗<enum_CSGPolygon3D_Mode>`

classref-enumeration-constant

`Mode<enum_CSGPolygon3D_Mode>` **MODE\_DEPTH** = `0`

The `polygon<class_CSGPolygon3D_property_polygon>` shape is extruded
along the negative Z axis.

classref-enumeration-constant

`Mode<enum_CSGPolygon3D_Mode>` **MODE\_SPIN** = `1`

The `polygon<class_CSGPolygon3D_property_polygon>` shape is extruded by
rotating it around the Y axis.

classref-enumeration-constant

`Mode<enum_CSGPolygon3D_Mode>` **MODE\_PATH** = `2`

The `polygon<class_CSGPolygon3D_property_polygon>` shape is extruded
along the `Path3D<class_Path3D>` specified in
`path_node<class_CSGPolygon3D_property_path_node>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PathRotation**: `🔗<enum_CSGPolygon3D_PathRotation>`

classref-enumeration-constant

`PathRotation<enum_CSGPolygon3D_PathRotation>`
**PATH\_ROTATION\_POLYGON** = `0`

The `polygon<class_CSGPolygon3D_property_polygon>` shape is not rotated.

\*\*Note:\*\* Requires the path Z coordinates to continually decrease to
ensure viable shapes.

classref-enumeration-constant

`PathRotation<enum_CSGPolygon3D_PathRotation>` **PATH\_ROTATION\_PATH**
= `1`

The `polygon<class_CSGPolygon3D_property_polygon>` shape is rotated
along the path, but it is not rotated around the path axis.

\*\*Note:\*\* Requires the path Z coordinates to continually decrease to
ensure viable shapes.

classref-enumeration-constant

`PathRotation<enum_CSGPolygon3D_PathRotation>`
**PATH\_ROTATION\_PATH\_FOLLOW** = `2`

The `polygon<class_CSGPolygon3D_property_polygon>` shape follows the
path and its rotations around the path axis.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PathIntervalType**: `🔗<enum_CSGPolygon3D_PathIntervalType>`

classref-enumeration-constant

`PathIntervalType<enum_CSGPolygon3D_PathIntervalType>`
**PATH\_INTERVAL\_DISTANCE** = `0`

When `mode<class_CSGPolygon3D_property_mode>` is set to
`MODE_PATH<class_CSGPolygon3D_constant_MODE_PATH>`,
`path_interval<class_CSGPolygon3D_property_path_interval>` will
determine the distance, in meters, each interval of the path will
extrude.

classref-enumeration-constant

`PathIntervalType<enum_CSGPolygon3D_PathIntervalType>`
**PATH\_INTERVAL\_SUBDIVIDE** = `1`

When `mode<class_CSGPolygon3D_property_mode>` is set to
`MODE_PATH<class_CSGPolygon3D_constant_MODE_PATH>`,
`path_interval<class_CSGPolygon3D_property_path_interval>` will
subdivide the polygons along the path.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **depth** = `1.0`
`🔗<class_CSGPolygon3D_property_depth>`

classref-property-setget

-   `void (No return value.)` **set\_depth**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_depth**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_DEPTH<class_CSGPolygon3D_constant_MODE_DEPTH>`, the depth of the
extrusion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Material<class_Material>` **material**
`🔗<class_CSGPolygon3D_property_material>`

classref-property-setget

-   `void (No return value.)` **set\_material**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_material**()

Material to use for the resulting mesh. The UV maps the top half of the
material to the extruded shape (U along the length of the extrusions and
V around the outline of the
`polygon<class_CSGPolygon3D_property_polygon>`), the bottom-left quarter
to the front end face, and the bottom-right quarter to the back end
face.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Mode<enum_CSGPolygon3D_Mode>` **mode** = `0`
`🔗<class_CSGPolygon3D_property_mode>`

classref-property-setget

-   `void (No return value.)` **set\_mode**(value:
    `Mode<enum_CSGPolygon3D_Mode>`)
-   `Mode<enum_CSGPolygon3D_Mode>` **get\_mode**()

The `mode<class_CSGPolygon3D_property_mode>` used to extrude the
`polygon<class_CSGPolygon3D_property_polygon>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **path\_continuous\_u**
`🔗<class_CSGPolygon3D_property_path_continuous_u>`

classref-property-setget

-   `void (No return value.)` **set\_path\_continuous\_u**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_path\_continuous\_u**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_PATH<class_CSGPolygon3D_constant_MODE_PATH>`, by default, the top
half of the `material<class_CSGPolygon3D_property_material>` is
stretched along the entire length of the extruded shape. If `false` the
top half of the material is repeated every step of the extrusion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **path\_interval**
`🔗<class_CSGPolygon3D_property_path_interval>`

classref-property-setget

-   `void (No return value.)` **set\_path\_interval**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_path\_interval**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_PATH<class_CSGPolygon3D_constant_MODE_PATH>`, the path interval or
ratio of path points to extrusions.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PathIntervalType<enum_CSGPolygon3D_PathIntervalType>`
**path\_interval\_type**
`🔗<class_CSGPolygon3D_property_path_interval_type>`

classref-property-setget

-   `void (No return value.)` **set\_path\_interval\_type**(value:
    `PathIntervalType<enum_CSGPolygon3D_PathIntervalType>`)
-   `PathIntervalType<enum_CSGPolygon3D_PathIntervalType>`
    **get\_path\_interval\_type**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_PATH<class_CSGPolygon3D_constant_MODE_PATH>`, this will determine
if the interval should be by distance
(`PATH_INTERVAL_DISTANCE<class_CSGPolygon3D_constant_PATH_INTERVAL_DISTANCE>`)
or subdivision fractions
(`PATH_INTERVAL_SUBDIVIDE<class_CSGPolygon3D_constant_PATH_INTERVAL_SUBDIVIDE>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **path\_joined**
`🔗<class_CSGPolygon3D_property_path_joined>`

classref-property-setget

-   `void (No return value.)` **set\_path\_joined**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_path\_joined**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_PATH<class_CSGPolygon3D_constant_MODE_PATH>`, if `true` the ends
of the path are joined, by adding an extrusion between the last and
first points of the path.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **path\_local**
`🔗<class_CSGPolygon3D_property_path_local>`

classref-property-setget

-   `void (No return value.)` **set\_path\_local**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_path\_local**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_PATH<class_CSGPolygon3D_constant_MODE_PATH>`, if `true` the
`Transform3D<class_Transform3D>` of the **CSGPolygon3D** is used as the
starting point for the extrusions, not the
`Transform3D<class_Transform3D>` of the
`path_node<class_CSGPolygon3D_property_path_node>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **path\_node**
`🔗<class_CSGPolygon3D_property_path_node>`

classref-property-setget

-   `void (No return value.)` **set\_path\_node**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_path\_node**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_PATH<class_CSGPolygon3D_constant_MODE_PATH>`, the location of the
`Path3D<class_Path3D>` object used to extrude the
`polygon<class_CSGPolygon3D_property_polygon>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PathRotation<enum_CSGPolygon3D_PathRotation>` **path\_rotation**
`🔗<class_CSGPolygon3D_property_path_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_path\_rotation**(value:
    `PathRotation<enum_CSGPolygon3D_PathRotation>`)
-   `PathRotation<enum_CSGPolygon3D_PathRotation>`
    **get\_path\_rotation**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_PATH<class_CSGPolygon3D_constant_MODE_PATH>`, the path rotation
method used to rotate the `polygon<class_CSGPolygon3D_property_polygon>`
as it is extruded.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **path\_simplify\_angle**
`🔗<class_CSGPolygon3D_property_path_simplify_angle>`

classref-property-setget

-   `void (No return value.)` **set\_path\_simplify\_angle**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_path\_simplify\_angle**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_PATH<class_CSGPolygon3D_constant_MODE_PATH>`, extrusions that are
less than this angle, will be merged together to reduce polygon count.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **path\_u\_distance**
`🔗<class_CSGPolygon3D_property_path_u_distance>`

classref-property-setget

-   `void (No return value.)` **set\_path\_u\_distance**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_path\_u\_distance**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_PATH<class_CSGPolygon3D_constant_MODE_PATH>`, this is the distance
along the path, in meters, the texture coordinates will tile. When set
to 0, texture coordinates will match geometry exactly with no tiling.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedVector2Array<class_PackedVector2Array>` **polygon** =
`PackedVector2Array(0, 0, 0, 1, 1, 1, 1, 0)`
`🔗<class_CSGPolygon3D_property_polygon>`

classref-property-setget

-   `void (No return value.)` **set\_polygon**(value:
    `PackedVector2Array<class_PackedVector2Array>`)
-   `PackedVector2Array<class_PackedVector2Array>` **get\_polygon**()

The point array that defines the 2D polygon that is extruded. This can
be a convex or concave polygon with 3 or more points. The polygon must
*not* have any intersecting edges. Otherwise, triangulation will fail
and no mesh will be generated.

\*\*Note:\*\* If only 1 or 2 points are defined in
`polygon<class_CSGPolygon3D_property_polygon>`, no mesh will be
generated.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedVector2Array<class_PackedVector2Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **smooth\_faces** = `false`
`🔗<class_CSGPolygon3D_property_smooth_faces>`

classref-property-setget

-   `void (No return value.)` **set\_smooth\_faces**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_smooth\_faces**()

If `true`, applies smooth shading to the extrusions.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **spin\_degrees**
`🔗<class_CSGPolygon3D_property_spin_degrees>`

classref-property-setget

-   `void (No return value.)` **set\_spin\_degrees**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_spin\_degrees**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_SPIN<class_CSGPolygon3D_constant_MODE_SPIN>`, the total number of
degrees the `polygon<class_CSGPolygon3D_property_polygon>` is rotated
when extruding.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **spin\_sides**
`🔗<class_CSGPolygon3D_property_spin_sides>`

classref-property-setget

-   `void (No return value.)` **set\_spin\_sides**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_spin\_sides**()

When `mode<class_CSGPolygon3D_property_mode>` is
`MODE_SPIN<class_CSGPolygon3D_constant_MODE_SPIN>`, the number of
extrusions made.
