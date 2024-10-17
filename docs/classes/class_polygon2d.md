github\_url  
hide

# Polygon2D

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A 2D polygon.

classref-introduction-group

## Description

A Polygon2D is defined by a set of points. Each point is connected to
the next, with the final point being connected to the first, resulting
in a closed polygon. Polygon2Ds can be filled with color (solid or
gradient) or filled with a given texture.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **antialiased** = `false`
`🔗<class_Polygon2D_property_antialiased>`

classref-property-setget

-   `void (No return value.)` **set\_antialiased**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_antialiased**()

If `true`, polygon edges will be anti-aliased.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **color** = `Color(1, 1, 1, 1)`
`🔗<class_Polygon2D_property_color>`

classref-property-setget

-   `void (No return value.)` **set\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_color**()

The polygon's fill color. If `texture<class_Polygon2D_property_texture>`
is set, it will be multiplied by this color. It will also be the default
color for vertices not set in
`vertex_colors<class_Polygon2D_property_vertex_colors>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **internal\_vertex\_count** = `0`
`🔗<class_Polygon2D_property_internal_vertex_count>`

classref-property-setget

-   `void (No return value.)` **set\_internal\_vertex\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_internal\_vertex\_count**()

Number of internal vertices, used for UV mapping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **invert\_border** = `100.0`
`🔗<class_Polygon2D_property_invert_border>`

classref-property-setget

-   `void (No return value.)` **set\_invert\_border**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_invert\_border**()

Added padding applied to the bounding box when
`invert_enabled<class_Polygon2D_property_invert_enabled>` is set to
`true`. Setting this value too small may result in a "Bad Polygon"
error.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **invert\_enabled** = `false`
`🔗<class_Polygon2D_property_invert_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_invert\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_invert\_enabled**()

If `true`, the polygon will be inverted, containing the area outside the
defined points and extending to the
`invert_border<class_Polygon2D_property_invert_border>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **offset** = `Vector2(0, 0)`
`🔗<class_Polygon2D_property_offset>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_offset**()

The offset applied to each vertex.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedVector2Array<class_PackedVector2Array>` **polygon** =
`PackedVector2Array()` `🔗<class_Polygon2D_property_polygon>`

classref-property-setget

-   `void (No return value.)` **set\_polygon**(value:
    `PackedVector2Array<class_PackedVector2Array>`)
-   `PackedVector2Array<class_PackedVector2Array>` **get\_polygon**()

The polygon's list of vertices. The final point will be connected to the
first.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedVector2Array<class_PackedVector2Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>` **polygons** = `[]`
`🔗<class_Polygon2D_property_polygons>`

classref-property-setget

-   `void (No return value.)` **set\_polygons**(value:
    `Array<class_Array>`)
-   `Array<class_Array>` **get\_polygons**()

The list of polygons, in case more than one is being represented. Every
individual polygon is stored as a
`PackedInt32Array<class_PackedInt32Array>` where each `int<class_int>`
is an index to a point in `polygon<class_Polygon2D_property_polygon>`.
If empty, this property will be ignored, and the resulting single
polygon will be composed of all points in
`polygon<class_Polygon2D_property_polygon>`, using the order they are
stored in.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **skeleton** = `NodePath("")`
`🔗<class_Polygon2D_property_skeleton>`

classref-property-setget

-   `void (No return value.)` **set\_skeleton**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_skeleton**()

Path to a `Skeleton2D<class_Skeleton2D>` node used for skeleton-based
deformations of this polygon. If empty or invalid, skeletal deformations
will not be used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture**
`🔗<class_Polygon2D_property_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**()

The polygon's fill texture. Use `uv<class_Polygon2D_property_uv>` to set
texture coordinates.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **texture\_offset** = `Vector2(0, 0)`
`🔗<class_Polygon2D_property_texture_offset>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_texture\_offset**()

Amount to offset the polygon's
`texture<class_Polygon2D_property_texture>`. If set to `Vector2(0, 0)`,
the texture's origin (its top-left corner) will be placed at the
polygon's position.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **texture\_rotation** = `0.0`
`🔗<class_Polygon2D_property_texture_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_rotation**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_texture\_rotation**()

The texture's rotation in radians.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **texture\_scale** = `Vector2(1, 1)`
`🔗<class_Polygon2D_property_texture_scale>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_scale**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_texture\_scale**()

Amount to multiply the `uv<class_Polygon2D_property_uv>` coordinates
when using `texture<class_Polygon2D_property_texture>`. Larger values
make the texture smaller, and vice versa.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedVector2Array<class_PackedVector2Array>` **uv** =
`PackedVector2Array()` `🔗<class_Polygon2D_property_uv>`

classref-property-setget

-   `void (No return value.)` **set\_uv**(value:
    `PackedVector2Array<class_PackedVector2Array>`)
-   `PackedVector2Array<class_PackedVector2Array>` **get\_uv**()

Texture coordinates for each vertex of the polygon. There should be one
UV value per polygon vertex. If there are fewer, undefined vertices will
use `Vector2(0, 0)`.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedVector2Array<class_PackedVector2Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedColorArray<class_PackedColorArray>` **vertex\_colors** =
`PackedColorArray()` `🔗<class_Polygon2D_property_vertex_colors>`

classref-property-setget

-   `void (No return value.)` **set\_vertex\_colors**(value:
    `PackedColorArray<class_PackedColorArray>`)
-   `PackedColorArray<class_PackedColorArray>` **get\_vertex\_colors**()

Color for each vertex. Colors are interpolated between vertices,
resulting in smooth gradients. There should be one per polygon vertex.
If there are fewer, undefined vertices will use
`color<class_Polygon2D_property_color>`.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedColorArray<class_PackedColorArray>` for more details.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_bone**(path:
`NodePath<class_NodePath>`, weights:
`PackedFloat32Array<class_PackedFloat32Array>`)
`🔗<class_Polygon2D_method_add_bone>`

Adds a bone with the specified `path` and `weights`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_bones**()
`🔗<class_Polygon2D_method_clear_bones>`

Removes all bones from this **Polygon2D**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase\_bone**(index: `int<class_int>`)
`🔗<class_Polygon2D_method_erase_bone>`

Removes the specified bone from this **Polygon2D**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_bone\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Polygon2D_method_get_bone_count>`

Returns the number of bones in this **Polygon2D**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`NodePath<class_NodePath>` **get\_bone\_path**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Polygon2D_method_get_bone_path>`

Returns the path to the node associated with the specified bone.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedFloat32Array<class_PackedFloat32Array>`
**get\_bone\_weights**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Polygon2D_method_get_bone_weights>`

Returns the weight values of the specified bone.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_path**(index: `int<class_int>`,
path: `NodePath<class_NodePath>`)
`🔗<class_Polygon2D_method_set_bone_path>`

Sets the path to the node associated with the specified bone.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_bone\_weights**(index:
`int<class_int>`, weights:
`PackedFloat32Array<class_PackedFloat32Array>`)
`🔗<class_Polygon2D_method_set_bone_weights>`

Sets the weight values for the specified bone.
