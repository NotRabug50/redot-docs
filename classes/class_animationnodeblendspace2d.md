github\_url  
hide

# AnimationNodeBlendSpace2D

**Inherits:** `AnimationRootNode<class_AnimationRootNode>` **&lt;**
`AnimationNode<class_AnimationNode>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A set of `AnimationRootNode<class_AnimationRootNode>`s placed on 2D
coordinates, crossfading between the three adjacent ones. Used by
`AnimationTree<class_AnimationTree>`.

classref-introduction-group

## Description

A resource used by
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`.

\*\*AnimationNodeBlendSpace2D\*\* represents a virtual 2D space on which
`AnimationRootNode<class_AnimationRootNode>`s are placed. Outputs the
linear blend of the three adjacent animations using a
`Vector2<class_Vector2>` weight. Adjacent in this context means the
three `AnimationRootNode<class_AnimationRootNode>`s making up the
triangle that contains the current value.

You can add vertices to the blend space with
`add_blend_point<class_AnimationNodeBlendSpace2D_method_add_blend_point>`
and automatically triangulate it by setting
`auto_triangles<class_AnimationNodeBlendSpace2D_property_auto_triangles>`
to `true`. Otherwise, use
`add_triangle<class_AnimationNodeBlendSpace2D_method_add_triangle>` and
`remove_triangle<class_AnimationNodeBlendSpace2D_method_remove_triangle>`
to triangulate the blend space by hand.

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`
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

## Signals

classref-signal

**triangles\_updated**()
`🔗<class_AnimationNodeBlendSpace2D_signal_triangles_updated>`

Emitted every time the blend space's triangles are created, removed, or
when one of their vertices changes position.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **BlendMode**: `🔗<enum_AnimationNodeBlendSpace2D_BlendMode>`

classref-enumeration-constant

`BlendMode<enum_AnimationNodeBlendSpace2D_BlendMode>`
**BLEND\_MODE\_INTERPOLATED** = `0`

The interpolation between animations is linear.

classref-enumeration-constant

`BlendMode<enum_AnimationNodeBlendSpace2D_BlendMode>`
**BLEND\_MODE\_DISCRETE** = `1`

The blend space plays the animation of the animation node which blending
position is closest to. Useful for frame-by-frame 2D animations.

classref-enumeration-constant

`BlendMode<enum_AnimationNodeBlendSpace2D_BlendMode>`
**BLEND\_MODE\_DISCRETE\_CARRY** = `2`

Similar to
`BLEND_MODE_DISCRETE<class_AnimationNodeBlendSpace2D_constant_BLEND_MODE_DISCRETE>`,
but starts the new animation at the last animation's playback position.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **auto\_triangles** = `true`
`🔗<class_AnimationNodeBlendSpace2D_property_auto_triangles>`

classref-property-setget

-   `void (No return value.)` **set\_auto\_triangles**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_auto\_triangles**()

If `true`, the blend space is triangulated automatically. The mesh
updates every time you add or remove points with
`add_blend_point<class_AnimationNodeBlendSpace2D_method_add_blend_point>`
and
`remove_blend_point<class_AnimationNodeBlendSpace2D_method_remove_blend_point>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BlendMode<enum_AnimationNodeBlendSpace2D_BlendMode>` **blend\_mode** =
`0` `🔗<class_AnimationNodeBlendSpace2D_property_blend_mode>`

classref-property-setget

-   `void (No return value.)` **set\_blend\_mode**(value:
    `BlendMode<enum_AnimationNodeBlendSpace2D_BlendMode>`)
-   `BlendMode<enum_AnimationNodeBlendSpace2D_BlendMode>`
    **get\_blend\_mode**()

Controls the interpolation between animations. See
`BlendMode<enum_AnimationNodeBlendSpace2D_BlendMode>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **max\_space** = `Vector2(1, 1)`
`🔗<class_AnimationNodeBlendSpace2D_property_max_space>`

classref-property-setget

-   `void (No return value.)` **set\_max\_space**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_max\_space**()

The blend space's X and Y axes' upper limit for the points' position.
See
`add_blend_point<class_AnimationNodeBlendSpace2D_method_add_blend_point>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **min\_space** = `Vector2(-1, -1)`
`🔗<class_AnimationNodeBlendSpace2D_property_min_space>`

classref-property-setget

-   `void (No return value.)` **set\_min\_space**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_min\_space**()

The blend space's X and Y axes' lower limit for the points' position.
See
`add_blend_point<class_AnimationNodeBlendSpace2D_method_add_blend_point>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **snap** = `Vector2(0.1, 0.1)`
`🔗<class_AnimationNodeBlendSpace2D_property_snap>`

classref-property-setget

-   `void (No return value.)` **set\_snap**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_snap**()

Position increment to snap to when moving a point.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **sync** = `false`
`🔗<class_AnimationNodeBlendSpace2D_property_sync>`

classref-property-setget

-   `void (No return value.)` **set\_use\_sync**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_sync**()

If `false`, the blended animations' frame are stopped when the blend
value is `0`.

If `true`, forcing the blended animations to advance frame.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **x\_label** = `"x"`
`🔗<class_AnimationNodeBlendSpace2D_property_x_label>`

classref-property-setget

-   `void (No return value.)` **set\_x\_label**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_x\_label**()

Name of the blend space's X axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **y\_label** = `"y"`
`🔗<class_AnimationNodeBlendSpace2D_property_y_label>`

classref-property-setget

-   `void (No return value.)` **set\_y\_label**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_y\_label**()

Name of the blend space's Y axis.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_blend\_point**(node:
`AnimationRootNode<class_AnimationRootNode>`, pos:
`Vector2<class_Vector2>`, at\_index: `int<class_int>` = -1)
`🔗<class_AnimationNodeBlendSpace2D_method_add_blend_point>`

Adds a new point that represents a `node` at the position set by `pos`.
You can insert it at a specific index using the `at_index` argument. If
you use the default value for `at_index`, the point is inserted at the
end of the blend points array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_triangle**(x: `int<class_int>`, y:
`int<class_int>`, z: `int<class_int>`, at\_index: `int<class_int>` = -1)
`🔗<class_AnimationNodeBlendSpace2D_method_add_triangle>`

Creates a new triangle using three points `x`, `y`, and `z`. Triangles
can overlap. You can insert the triangle at a specific index using the
`at_index` argument. If you use the default value for `at_index`, the
point is inserted at the end of the blend points array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_blend\_point\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeBlendSpace2D_method_get_blend_point_count>`

Returns the number of points in the blend space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AnimationRootNode<class_AnimationRootNode>`
**get\_blend\_point\_node**(point: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeBlendSpace2D_method_get_blend_point_node>`

Returns the `AnimationRootNode<class_AnimationRootNode>` referenced by
the point at index `point`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_blend\_point\_position**(point:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeBlendSpace2D_method_get_blend_point_position>`

Returns the position of the point at index `point`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_triangle\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeBlendSpace2D_method_get_triangle_count>`

Returns the number of triangles in the blend space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_triangle\_point**(triangle: `int<class_int>`,
point: `int<class_int>`)
`🔗<class_AnimationNodeBlendSpace2D_method_get_triangle_point>`

Returns the position of the point at index `point` in the triangle of
index `triangle`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_blend\_point**(point:
`int<class_int>`)
`🔗<class_AnimationNodeBlendSpace2D_method_remove_blend_point>`

Removes the point at index `point` from the blend space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_triangle**(triangle:
`int<class_int>`)
`🔗<class_AnimationNodeBlendSpace2D_method_remove_triangle>`

Removes the triangle at index `triangle` from the blend space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_blend\_point\_node**(point:
`int<class_int>`, node: `AnimationRootNode<class_AnimationRootNode>`)
`🔗<class_AnimationNodeBlendSpace2D_method_set_blend_point_node>`

Changes the `AnimationNode<class_AnimationNode>` referenced by the point
at index `point`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_blend\_point\_position**(point:
`int<class_int>`, pos: `Vector2<class_Vector2>`)
`🔗<class_AnimationNodeBlendSpace2D_method_set_blend_point_position>`

Updates the position of the point at index `point` in the blend space.
