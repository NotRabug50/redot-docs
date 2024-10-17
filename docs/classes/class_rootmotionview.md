github\_url  
hide

# RootMotionView

**Inherits:** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Editor-only helper for setting up root motion in
`AnimationMixer<class_AnimationMixer>`.

classref-introduction-group

## Description

*Root motion* refers to an animation technique where a mesh's skeleton
is used to give impulse to a character. When working with 3D animations,
a popular technique is for animators to use the root skeleton bone to
give motion to the rest of the skeleton. This allows animating
characters in a way where steps actually match the floor below. It also
allows precise interaction with objects during cinematics. See also
`AnimationMixer<class_AnimationMixer>`.

\*\*Note:\*\* **RootMotionView** is only visible in the editor. It will
be hidden automatically in the running project.

classref-introduction-group

## Tutorials

-   [Using AnimationTree - Root
    motion](../tutorials/animation/animation_tree.html#root-motion)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`NodePath<class_NodePath>` **animation\_path** = `NodePath("")`
`🔗<class_RootMotionView_property_animation_path>`

classref-property-setget

-   `void (No return value.)` **set\_animation\_path**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_animation\_path**()

Path to an `AnimationMixer<class_AnimationMixer>` node to use as a basis
for root motion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **cell\_size** = `1.0`
`🔗<class_RootMotionView_property_cell_size>`

classref-property-setget

-   `void (No return value.)` **set\_cell\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_cell\_size**()

The grid's cell size in 3D units.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **color** = `Color(0.5, 0.5, 1, 1)`
`🔗<class_RootMotionView_property_color>`

classref-property-setget

-   `void (No return value.)` **set\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_color**()

The grid's color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radius** = `10.0`
`🔗<class_RootMotionView_property_radius>`

classref-property-setget

-   `void (No return value.)` **set\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_radius**()

The grid's radius in 3D units. The grid's opacity will fade gradually as
the distance from the origin increases until this
`radius<class_RootMotionView_property_radius>` is reached.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **zero\_y** = `true`
`🔗<class_RootMotionView_property_zero_y>`

classref-property-setget

-   `void (No return value.)` **set\_zero\_y**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_zero\_y**()

If `true`, the grid's points will all be on the same Y coordinate
(*local* Y = 0). If `false`, the points' original Y coordinate is
preserved.
