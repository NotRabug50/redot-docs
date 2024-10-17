github\_url  
hide

# Node2D

**Inherits:** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

**Inherited By:** `AnimatedSprite2D<class_AnimatedSprite2D>`,
`AudioListener2D<class_AudioListener2D>`,
`AudioStreamPlayer2D<class_AudioStreamPlayer2D>`,
`BackBufferCopy<class_BackBufferCopy>`, `Bone2D<class_Bone2D>`,
`Camera2D<class_Camera2D>`, `CanvasGroup<class_CanvasGroup>`,
`CanvasModulate<class_CanvasModulate>`,
`CollisionObject2D<class_CollisionObject2D>`,
`CollisionPolygon2D<class_CollisionPolygon2D>`,
`CollisionShape2D<class_CollisionShape2D>`,
`CPUParticles2D<class_CPUParticles2D>`,
`GPUParticles2D<class_GPUParticles2D>`, `Joint2D<class_Joint2D>`,
`Light2D<class_Light2D>`, `LightOccluder2D<class_LightOccluder2D>`,
`Line2D<class_Line2D>`, `Marker2D<class_Marker2D>`,
`MeshInstance2D<class_MeshInstance2D>`,
`MultiMeshInstance2D<class_MultiMeshInstance2D>`,
`NavigationLink2D<class_NavigationLink2D>`,
`NavigationObstacle2D<class_NavigationObstacle2D>`,
`NavigationRegion2D<class_NavigationRegion2D>`,
`Parallax2D<class_Parallax2D>`, `ParallaxLayer<class_ParallaxLayer>`,
`Path2D<class_Path2D>`, `PathFollow2D<class_PathFollow2D>`,
`Polygon2D<class_Polygon2D>`, `RayCast2D<class_RayCast2D>`,
`RemoteTransform2D<class_RemoteTransform2D>`,
`ShapeCast2D<class_ShapeCast2D>`, `Skeleton2D<class_Skeleton2D>`,
`Sprite2D<class_Sprite2D>`, `TileMap<class_TileMap>`,
`TileMapLayer<class_TileMapLayer>`,
`TouchScreenButton<class_TouchScreenButton>`,
`VisibleOnScreenNotifier2D<class_VisibleOnScreenNotifier2D>`

A 2D game object, inherited by all 2D-related nodes. Has a position,
rotation, scale, and Z index.

classref-introduction-group

## Description

A 2D game object, with a transform (position, rotation, and scale). All
2D nodes, including physics objects and sprites, inherit from Node2D.
Use Node2D as a parent node to move, scale and rotate children in a 2D
project. Also gives control of the node's render order.

classref-introduction-group

## Tutorials

-   `Custom drawing in 2D <../tutorials/2d/custom_drawing_in_2d>`
-   [All 2D
    Demos](https://github.com/godotengine/godot-demo-projects/tree/master/2d)

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

## Property Descriptions

classref-property

`Vector2<class_Vector2>` **global\_position**
`🔗<class_Node2D_property_global_position>`

classref-property-setget

-   `void (No return value.)` **set\_global\_position**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_global\_position**()

Global position. See also `position<class_Node2D_property_position>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **global\_rotation**
`🔗<class_Node2D_property_global_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_global\_rotation**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_global\_rotation**()

Global rotation in radians. See also
`rotation<class_Node2D_property_rotation>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **global\_rotation\_degrees**
`🔗<class_Node2D_property_global_rotation_degrees>`

classref-property-setget

-   `void (No return value.)` **set\_global\_rotation\_degrees**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_global\_rotation\_degrees**()

Helper property to access
`global_rotation<class_Node2D_property_global_rotation>` in degrees
instead of radians. See also
`rotation_degrees<class_Node2D_property_rotation_degrees>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **global\_scale**
`🔗<class_Node2D_property_global_scale>`

classref-property-setget

-   `void (No return value.)` **set\_global\_scale**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_global\_scale**()

Global scale. See also `scale<class_Node2D_property_scale>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **global\_skew**
`🔗<class_Node2D_property_global_skew>`

classref-property-setget

-   `void (No return value.)` **set\_global\_skew**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_global\_skew**()

Global skew in radians. See also `skew<class_Node2D_property_skew>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform2D<class_Transform2D>` **global\_transform**
`🔗<class_Node2D_property_global_transform>`

classref-property-setget

-   `void (No return value.)` **set\_global\_transform**(value:
    `Transform2D<class_Transform2D>`)
-   `Transform2D<class_Transform2D>` **get\_global\_transform**()

Global `Transform2D<class_Transform2D>`. See also
`transform<class_Node2D_property_transform>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **position** = `Vector2(0, 0)`
`🔗<class_Node2D_property_position>`

classref-property-setget

-   `void (No return value.)` **set\_position**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_position**()

Position, relative to the node's parent. See also
`global_position<class_Node2D_property_global_position>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **rotation** = `0.0`
`🔗<class_Node2D_property_rotation>`

classref-property-setget

-   `void (No return value.)` **set\_rotation**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_rotation**()

Rotation in radians, relative to the node's parent. See also
`global_rotation<class_Node2D_property_global_rotation>`.

\*\*Note:\*\* This property is edited in the inspector in degrees. If
you want to use degrees in a script, use
`rotation_degrees<class_Node2D_property_rotation_degrees>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **rotation\_degrees**
`🔗<class_Node2D_property_rotation_degrees>`

classref-property-setget

-   `void (No return value.)` **set\_rotation\_degrees**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_rotation\_degrees**()

Helper property to access `rotation<class_Node2D_property_rotation>` in
degrees instead of radians. See also
`global_rotation_degrees<class_Node2D_property_global_rotation_degrees>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **scale** = `Vector2(1, 1)`
`🔗<class_Node2D_property_scale>`

classref-property-setget

-   `void (No return value.)` **set\_scale**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_scale**()

The node's scale, relative to the node's parent. Unscaled value:
`(1, 1)`. See also `global_scale<class_Node2D_property_global_scale>`.

\*\*Note:\*\* Negative X scales in 2D are not decomposable from the
transformation matrix. Due to the way scale is represented with
transformation matrices in Godot, negative scales on the X axis will be
changed to negative scales on the Y axis and a rotation of 180 degrees
when decomposed.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **skew** = `0.0` `🔗<class_Node2D_property_skew>`

classref-property-setget

-   `void (No return value.)` **set\_skew**(value: `float<class_float>`)
-   `float<class_float>` **get\_skew**()

If set to a non-zero value, slants the node in one direction or another.
This can be used for pseudo-3D effects. See also
`global_skew<class_Node2D_property_global_skew>`.

\*\*Note:\*\* Skew is performed on the X axis only, and *between*
rotation and scaling.

\*\*Note:\*\* This property is edited in the inspector in degrees. If
you want to use degrees in a script, use
`skew = deg_to_rad(value_in_degrees)`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Transform2D<class_Transform2D>` **transform**
`🔗<class_Node2D_property_transform>`

classref-property-setget

-   `void (No return value.)` **set\_transform**(value:
    `Transform2D<class_Transform2D>`)
-   `Transform2D<class_Transform2D>` **get\_transform**()

The node's `Transform2D<class_Transform2D>`, relative to the node's
parent. See also
`global_transform<class_Node2D_property_global_transform>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **apply\_scale**(ratio:
`Vector2<class_Vector2>`) `🔗<class_Node2D_method_apply_scale>`

Multiplies the current scale by the `ratio` vector.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_angle\_to**(point: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node2D_method_get_angle_to>`

Returns the angle between the node and the `point` in radians.

[Illustration of the returned
angle.](https://raw.githubusercontent.com/godotengine/godot-docs/master/img/node2d_get_angle_to.png)

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>`
**get\_relative\_transform\_to\_parent**(parent: `Node<class_Node>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node2D_method_get_relative_transform_to_parent>`

Returns the `Transform2D<class_Transform2D>` relative to this node's
parent.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **global\_translate**(offset:
`Vector2<class_Vector2>`) `🔗<class_Node2D_method_global_translate>`

Adds the `offset` vector to the node's global position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **look\_at**(point: `Vector2<class_Vector2>`)
`🔗<class_Node2D_method_look_at>`

Rotates the node so that its local +X axis points towards the `point`,
which is expected to use global coordinates.

`point` should not be the same as the node's position, otherwise the
node always looks to the right.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_local\_x**(delta:
`float<class_float>`, scaled: `bool<class_bool>` = false)
`🔗<class_Node2D_method_move_local_x>`

Applies a local translation on the node's X axis based on the
`Node._process<class_Node_private_method__process>`'s `delta`. If
`scaled` is `false`, normalizes the movement.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_local\_y**(delta:
`float<class_float>`, scaled: `bool<class_bool>` = false)
`🔗<class_Node2D_method_move_local_y>`

Applies a local translation on the node's Y axis based on the
`Node._process<class_Node_private_method__process>`'s `delta`. If
`scaled` is `false`, normalizes the movement.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **rotate**(radians: `float<class_float>`)
`🔗<class_Node2D_method_rotate>`

Applies a rotation to the node, in radians, starting from its current
rotation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **to\_global**(local\_point:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node2D_method_to_global>`

Transforms the provided local position into a position in global
coordinate space. The input is expected to be local relative to the
**Node2D** it is called on. e.g. Applying this method to the positions
of child nodes will correctly transform their positions into the global
coordinate space, but applying it to a node's own position will give an
incorrect result, as it will incorporate the node's own transformation
into its global position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **to\_local**(global\_point:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Node2D_method_to_local>`

Transforms the provided global position into a position in local
coordinate space. The output will be local relative to the **Node2D** it
is called on. e.g. It is appropriate for determining the positions of
child nodes, but it is not appropriate for determining its own position
relative to its parent.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **translate**(offset:
`Vector2<class_Vector2>`) `🔗<class_Node2D_method_translate>`

Translates the node by the given `offset` in local coordinates.
