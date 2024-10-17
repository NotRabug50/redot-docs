github\_url  
hide

# AnimationNodeBlendSpace1D

**Inherits:** `AnimationRootNode<class_AnimationRootNode>` **&lt;**
`AnimationNode<class_AnimationNode>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A set of `AnimationRootNode<class_AnimationRootNode>`s placed on a
virtual axis, crossfading between the two adjacent ones. Used by
`AnimationTree<class_AnimationTree>`.

classref-introduction-group

## Description

A resource used by
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`.

\*\*AnimationNodeBlendSpace1D\*\* represents a virtual axis on which any
type of `AnimationRootNode<class_AnimationRootNode>`s can be added using
`add_blend_point<class_AnimationNodeBlendSpace1D_method_add_blend_point>`.
Outputs the linear blend of the two
`AnimationRootNode<class_AnimationRootNode>`s adjacent to the current
value.

You can set the extents of the axis with
`min_space<class_AnimationNodeBlendSpace1D_property_min_space>` and
`max_space<class_AnimationNodeBlendSpace1D_property_max_space>`.

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **BlendMode**: `🔗<enum_AnimationNodeBlendSpace1D_BlendMode>`

classref-enumeration-constant

`BlendMode<enum_AnimationNodeBlendSpace1D_BlendMode>`
**BLEND\_MODE\_INTERPOLATED** = `0`

The interpolation between animations is linear.

classref-enumeration-constant

`BlendMode<enum_AnimationNodeBlendSpace1D_BlendMode>`
**BLEND\_MODE\_DISCRETE** = `1`

The blend space plays the animation of the animation node which blending
position is closest to. Useful for frame-by-frame 2D animations.

classref-enumeration-constant

`BlendMode<enum_AnimationNodeBlendSpace1D_BlendMode>`
**BLEND\_MODE\_DISCRETE\_CARRY** = `2`

Similar to
`BLEND_MODE_DISCRETE<class_AnimationNodeBlendSpace1D_constant_BLEND_MODE_DISCRETE>`,
but starts the new animation at the last animation's playback position.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`BlendMode<enum_AnimationNodeBlendSpace1D_BlendMode>` **blend\_mode** =
`0` `🔗<class_AnimationNodeBlendSpace1D_property_blend_mode>`

classref-property-setget

-   `void (No return value.)` **set\_blend\_mode**(value:
    `BlendMode<enum_AnimationNodeBlendSpace1D_BlendMode>`)
-   `BlendMode<enum_AnimationNodeBlendSpace1D_BlendMode>`
    **get\_blend\_mode**()

Controls the interpolation between animations. See
`BlendMode<enum_AnimationNodeBlendSpace1D_BlendMode>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **max\_space** = `1.0`
`🔗<class_AnimationNodeBlendSpace1D_property_max_space>`

classref-property-setget

-   `void (No return value.)` **set\_max\_space**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_max\_space**()

The blend space's axis's upper limit for the points' position. See
`add_blend_point<class_AnimationNodeBlendSpace1D_method_add_blend_point>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **min\_space** = `-1.0`
`🔗<class_AnimationNodeBlendSpace1D_property_min_space>`

classref-property-setget

-   `void (No return value.)` **set\_min\_space**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_min\_space**()

The blend space's axis's lower limit for the points' position. See
`add_blend_point<class_AnimationNodeBlendSpace1D_method_add_blend_point>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **snap** = `0.1`
`🔗<class_AnimationNodeBlendSpace1D_property_snap>`

classref-property-setget

-   `void (No return value.)` **set\_snap**(value: `float<class_float>`)
-   `float<class_float>` **get\_snap**()

Position increment to snap to when moving a point on the axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **sync** = `false`
`🔗<class_AnimationNodeBlendSpace1D_property_sync>`

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

`String<class_String>` **value\_label** = `"value"`
`🔗<class_AnimationNodeBlendSpace1D_property_value_label>`

classref-property-setget

-   `void (No return value.)` **set\_value\_label**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_value\_label**()

Label of the virtual axis of the blend space.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_blend\_point**(node:
`AnimationRootNode<class_AnimationRootNode>`, pos: `float<class_float>`,
at\_index: `int<class_int>` = -1)
`🔗<class_AnimationNodeBlendSpace1D_method_add_blend_point>`

Adds a new point that represents a `node` on the virtual axis at a given
position set by `pos`. You can insert it at a specific index using the
`at_index` argument. If you use the default value for `at_index`, the
point is inserted at the end of the blend points array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_blend\_point\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeBlendSpace1D_method_get_blend_point_count>`

Returns the number of points on the blend axis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AnimationRootNode<class_AnimationRootNode>`
**get\_blend\_point\_node**(point: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeBlendSpace1D_method_get_blend_point_node>`

Returns the `AnimationNode<class_AnimationNode>` referenced by the point
at index `point`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_blend\_point\_position**(point:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeBlendSpace1D_method_get_blend_point_position>`

Returns the position of the point at index `point`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_blend\_point**(point:
`int<class_int>`)
`🔗<class_AnimationNodeBlendSpace1D_method_remove_blend_point>`

Removes the point at index `point` from the blend axis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_blend\_point\_node**(point:
`int<class_int>`, node: `AnimationRootNode<class_AnimationRootNode>`)
`🔗<class_AnimationNodeBlendSpace1D_method_set_blend_point_node>`

Changes the `AnimationNode<class_AnimationNode>` referenced by the point
at index `point`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_blend\_point\_position**(point:
`int<class_int>`, pos: `float<class_float>`)
`🔗<class_AnimationNodeBlendSpace1D_method_set_blend_point_position>`

Updates the position of the point at index `point` on the blend axis.
