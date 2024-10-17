github\_url  
hide

# CanvasItem

**Inherits:** `Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `Control<class_Control>`, `Node2D<class_Node2D>`

Abstract base class for everything in 2D space.

classref-introduction-group

## Description

Abstract base class for everything in 2D space. Canvas items are laid
out in a tree; children inherit and extend their parent's transform.
**CanvasItem** is extended by `Control<class_Control>` for GUI-related
nodes, and by `Node2D<class_Node2D>` for 2D game objects.

Any **CanvasItem** can draw. For this,
`queue_redraw<class_CanvasItem_method_queue_redraw>` is called by the
engine, then
`NOTIFICATION_DRAW<class_CanvasItem_constant_NOTIFICATION_DRAW>` will be
received on idle time to request a redraw. Because of this, canvas items
don't need to be redrawn on every frame, improving the performance
significantly. Several functions for drawing on the **CanvasItem** are
provided (see `draw_*` functions). However, they can only be used inside
`_draw<class_CanvasItem_private_method__draw>`, its corresponding
`Object._notification<class_Object_private_method__notification>` or
methods connected to the `draw<class_CanvasItem_signal_draw>` signal.

Canvas items are drawn in tree order on their canvas layer. By default,
children are on top of their parents, so a root **CanvasItem** will be
drawn behind everything. This behavior can be changed on a per-item
basis.

A **CanvasItem** can be hidden, which will also hide its children. By
adjusting various other properties of a **CanvasItem**, you can also
modulate its color (via `modulate<class_CanvasItem_property_modulate>`
or `self_modulate<class_CanvasItem_property_self_modulate>`), change its
Z-index, blend mode, and more.

Note that properties like transform, modulation, and visibility are only
propagated to *direct* **CanvasItem** child nodes. If there is a
non-**CanvasItem** node in between, like `Node<class_Node>` or
`AnimationPlayer<class_AnimationPlayer>`, the **CanvasItem** nodes below
will have an independent position and
`modulate<class_CanvasItem_property_modulate>` chain. See also
`top_level<class_CanvasItem_property_top_level>`.

classref-introduction-group

## Tutorials

-   `Viewport and canvas transforms <../tutorials/2d/2d_transforms>`
-   `Custom drawing in 2D <../tutorials/2d/custom_drawing_in_2d>`
-   [Audio Spectrum Visualizer
    Demo](https://godotengine.org/asset-library/asset/2762)

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

**draw**() `🔗<class_CanvasItem_signal_draw>`

Emitted when the **CanvasItem** must redraw, *after* the related
`NOTIFICATION_DRAW<class_CanvasItem_constant_NOTIFICATION_DRAW>`
notification, and *before*
`_draw<class_CanvasItem_private_method__draw>` is called.

\*\*Note:\*\* Deferred connections do not allow drawing through the
`draw_*` methods.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**hidden**() `🔗<class_CanvasItem_signal_hidden>`

Emitted when the **CanvasItem** is hidden, i.e. it's no longer visible
in the tree (see
`is_visible_in_tree<class_CanvasItem_method_is_visible_in_tree>`).

classref-item-separator

------------------------------------------------------------------------

classref-signal

**item\_rect\_changed**()
`🔗<class_CanvasItem_signal_item_rect_changed>`

Emitted when the **CanvasItem**'s boundaries (position or size) change,
or when an action took place that may have affected these boundaries
(e.g. changing `Sprite2D.texture<class_Sprite2D_property_texture>`).

classref-item-separator

------------------------------------------------------------------------

classref-signal

**visibility\_changed**()
`🔗<class_CanvasItem_signal_visibility_changed>`

Emitted when the **CanvasItem**'s visibility changes, either because its
own `visible<class_CanvasItem_property_visible>` property changed or
because its visibility in the tree changed (see
`is_visible_in_tree<class_CanvasItem_method_is_visible_in_tree>`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **TextureFilter**: `🔗<enum_CanvasItem_TextureFilter>`

classref-enumeration-constant

`TextureFilter<enum_CanvasItem_TextureFilter>`
**TEXTURE\_FILTER\_PARENT\_NODE** = `0`

The **CanvasItem** will inherit the filter from its parent.

classref-enumeration-constant

`TextureFilter<enum_CanvasItem_TextureFilter>`
**TEXTURE\_FILTER\_NEAREST** = `1`

The texture filter reads from the nearest pixel only. This makes the
texture look pixelated from up close, and grainy from a distance (due to
mipmaps not being sampled).

classref-enumeration-constant

`TextureFilter<enum_CanvasItem_TextureFilter>`
**TEXTURE\_FILTER\_LINEAR** = `2`

The texture filter blends between the nearest 4 pixels. This makes the
texture look smooth from up close, and grainy from a distance (due to
mipmaps not being sampled).

classref-enumeration-constant

`TextureFilter<enum_CanvasItem_TextureFilter>`
**TEXTURE\_FILTER\_NEAREST\_WITH\_MIPMAPS** = `3`

The texture filter reads from the nearest pixel and blends between the
nearest 2 mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`). This makes the texture look pixelated from up close, and
smooth from a distance.

Use this for non-pixel art textures that may be viewed at a low scale
(e.g. due to `Camera2D<class_Camera2D>` zoom or sprite scaling), as
mipmaps are important to smooth out pixels that are smaller than
on-screen pixels.

classref-enumeration-constant

`TextureFilter<enum_CanvasItem_TextureFilter>`
**TEXTURE\_FILTER\_LINEAR\_WITH\_MIPMAPS** = `4`

The texture filter blends between the nearest 4 pixels and between the
nearest 2 mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`). This makes the texture look smooth from up close, and smooth
from a distance.

Use this for non-pixel art textures that may be viewed at a low scale
(e.g. due to `Camera2D<class_Camera2D>` zoom or sprite scaling), as
mipmaps are important to smooth out pixels that are smaller than
on-screen pixels.

classref-enumeration-constant

`TextureFilter<enum_CanvasItem_TextureFilter>`
**TEXTURE\_FILTER\_NEAREST\_WITH\_MIPMAPS\_ANISOTROPIC** = `5`

The texture filter reads from the nearest pixel and blends between 2
mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`) based on the angle between the surface and the camera view.
This makes the texture look pixelated from up close, and smooth from a
distance. Anisotropic filtering improves texture quality on surfaces
that are almost in line with the camera, but is slightly slower. The
anisotropic filtering level can be changed by adjusting
`ProjectSettings.rendering/textures/default_filters/anisotropic_filtering_level<class_ProjectSettings_property_rendering/textures/default_filters/anisotropic_filtering_level>`.

\*\*Note:\*\* This texture filter is rarely useful in 2D projects.
`TEXTURE_FILTER_NEAREST_WITH_MIPMAPS<class_CanvasItem_constant_TEXTURE_FILTER_NEAREST_WITH_MIPMAPS>`
is usually more appropriate in this case.

classref-enumeration-constant

`TextureFilter<enum_CanvasItem_TextureFilter>`
**TEXTURE\_FILTER\_LINEAR\_WITH\_MIPMAPS\_ANISOTROPIC** = `6`

The texture filter blends between the nearest 4 pixels and blends
between 2 mipmaps (or uses the nearest mipmap if
`ProjectSettings.rendering/textures/default_filters/use_nearest_mipmap_filter<class_ProjectSettings_property_rendering/textures/default_filters/use_nearest_mipmap_filter>`
is `true`) based on the angle between the surface and the camera view.
This makes the texture look smooth from up close, and smooth from a
distance. Anisotropic filtering improves texture quality on surfaces
that are almost in line with the camera, but is slightly slower. The
anisotropic filtering level can be changed by adjusting
`ProjectSettings.rendering/textures/default_filters/anisotropic_filtering_level<class_ProjectSettings_property_rendering/textures/default_filters/anisotropic_filtering_level>`.

\*\*Note:\*\* This texture filter is rarely useful in 2D projects.
`TEXTURE_FILTER_LINEAR_WITH_MIPMAPS<class_CanvasItem_constant_TEXTURE_FILTER_LINEAR_WITH_MIPMAPS>`
is usually more appropriate in this case.

classref-enumeration-constant

`TextureFilter<enum_CanvasItem_TextureFilter>` **TEXTURE\_FILTER\_MAX**
= `7`

Represents the size of the
`TextureFilter<enum_CanvasItem_TextureFilter>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TextureRepeat**: `🔗<enum_CanvasItem_TextureRepeat>`

classref-enumeration-constant

`TextureRepeat<enum_CanvasItem_TextureRepeat>`
**TEXTURE\_REPEAT\_PARENT\_NODE** = `0`

The **CanvasItem** will inherit the filter from its parent.

classref-enumeration-constant

`TextureRepeat<enum_CanvasItem_TextureRepeat>`
**TEXTURE\_REPEAT\_DISABLED** = `1`

Texture will not repeat.

classref-enumeration-constant

`TextureRepeat<enum_CanvasItem_TextureRepeat>`
**TEXTURE\_REPEAT\_ENABLED** = `2`

Texture will repeat normally.

classref-enumeration-constant

`TextureRepeat<enum_CanvasItem_TextureRepeat>`
**TEXTURE\_REPEAT\_MIRROR** = `3`

Texture will repeat in a 2×2 tiled mode, where elements at even
positions are mirrored.

classref-enumeration-constant

`TextureRepeat<enum_CanvasItem_TextureRepeat>` **TEXTURE\_REPEAT\_MAX**
= `4`

Represents the size of the
`TextureRepeat<enum_CanvasItem_TextureRepeat>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ClipChildrenMode**: `🔗<enum_CanvasItem_ClipChildrenMode>`

classref-enumeration-constant

`ClipChildrenMode<enum_CanvasItem_ClipChildrenMode>`
**CLIP\_CHILDREN\_DISABLED** = `0`

Child draws over parent and is not clipped.

classref-enumeration-constant

`ClipChildrenMode<enum_CanvasItem_ClipChildrenMode>`
**CLIP\_CHILDREN\_ONLY** = `1`

Parent is used for the purposes of clipping only. Child is clipped to
the parent's visible area, parent is not drawn.

classref-enumeration-constant

`ClipChildrenMode<enum_CanvasItem_ClipChildrenMode>`
**CLIP\_CHILDREN\_AND\_DRAW** = `2`

Parent is used for clipping child, but parent is also drawn underneath
child as normal before clipping child to its visible area.

classref-enumeration-constant

`ClipChildrenMode<enum_CanvasItem_ClipChildrenMode>`
**CLIP\_CHILDREN\_MAX** = `3`

Represents the size of the
`ClipChildrenMode<enum_CanvasItem_ClipChildrenMode>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NOTIFICATION\_TRANSFORM\_CHANGED** = `2000`
`🔗<class_CanvasItem_constant_NOTIFICATION_TRANSFORM_CHANGED>`

The **CanvasItem**'s global transform has changed. This notification is
only received if enabled by
`set_notify_transform<class_CanvasItem_method_set_notify_transform>`.

classref-constant

**NOTIFICATION\_LOCAL\_TRANSFORM\_CHANGED** = `35`
`🔗<class_CanvasItem_constant_NOTIFICATION_LOCAL_TRANSFORM_CHANGED>`

The **CanvasItem**'s local transform has changed. This notification is
only received if enabled by
`set_notify_local_transform<class_CanvasItem_method_set_notify_local_transform>`.

classref-constant

**NOTIFICATION\_DRAW** = `30`
`🔗<class_CanvasItem_constant_NOTIFICATION_DRAW>`

The **CanvasItem** is requested to draw (see
`_draw<class_CanvasItem_private_method__draw>`).

classref-constant

**NOTIFICATION\_VISIBILITY\_CHANGED** = `31`
`🔗<class_CanvasItem_constant_NOTIFICATION_VISIBILITY_CHANGED>`

The **CanvasItem**'s visibility has changed.

classref-constant

**NOTIFICATION\_ENTER\_CANVAS** = `32`
`🔗<class_CanvasItem_constant_NOTIFICATION_ENTER_CANVAS>`

The **CanvasItem** has entered the canvas.

classref-constant

**NOTIFICATION\_EXIT\_CANVAS** = `33`
`🔗<class_CanvasItem_constant_NOTIFICATION_EXIT_CANVAS>`

The **CanvasItem** has exited the canvas.

classref-constant

**NOTIFICATION\_WORLD\_2D\_CHANGED** = `36`
`🔗<class_CanvasItem_constant_NOTIFICATION_WORLD_2D_CHANGED>`

The **CanvasItem**'s active `World2D<class_World2D>` changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`ClipChildrenMode<enum_CanvasItem_ClipChildrenMode>` **clip\_children**
= `0` `🔗<class_CanvasItem_property_clip_children>`

classref-property-setget

-   `void (No return value.)` **set\_clip\_children\_mode**(value:
    `ClipChildrenMode<enum_CanvasItem_ClipChildrenMode>`)
-   `ClipChildrenMode<enum_CanvasItem_ClipChildrenMode>`
    **get\_clip\_children\_mode**()

Allows the current node to clip child nodes, essentially acting as a
mask.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **light\_mask** = `1`
`🔗<class_CanvasItem_property_light_mask>`

classref-property-setget

-   `void (No return value.)` **set\_light\_mask**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_light\_mask**()

The rendering layers in which this **CanvasItem** responds to
`Light2D<class_Light2D>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Material<class_Material>` **material**
`🔗<class_CanvasItem_property_material>`

classref-property-setget

-   `void (No return value.)` **set\_material**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_material**()

The material applied to this **CanvasItem**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **modulate** = `Color(1, 1, 1, 1)`
`🔗<class_CanvasItem_property_modulate>`

classref-property-setget

-   `void (No return value.)` **set\_modulate**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_modulate**()

The color applied to this **CanvasItem**. This property does affect
child **CanvasItem**s, unlike
`self_modulate<class_CanvasItem_property_self_modulate>` which only
affects the node itself.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **self\_modulate** = `Color(1, 1, 1, 1)`
`🔗<class_CanvasItem_property_self_modulate>`

classref-property-setget

-   `void (No return value.)` **set\_self\_modulate**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_self\_modulate**()

The color applied to this **CanvasItem**. This property does **not**
affect child **CanvasItem**s, unlike
`modulate<class_CanvasItem_property_modulate>` which affects both the
node itself and its children.

\*\*Note:\*\* Internal children (e.g. sliders in
`ColorPicker<class_ColorPicker>` or tab bar in
`TabContainer<class_TabContainer>`) are also not affected by this
property (see `include_internal` parameter of
`Node.get_child<class_Node_method_get_child>` and other similar
methods).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_behind\_parent** = `false`
`🔗<class_CanvasItem_property_show_behind_parent>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_behind\_parent**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_draw\_behind\_parent\_enabled**()

If `true`, the object draws behind its parent.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureFilter<enum_CanvasItem_TextureFilter>` **texture\_filter** = `0`
`🔗<class_CanvasItem_property_texture_filter>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_filter**(value:
    `TextureFilter<enum_CanvasItem_TextureFilter>`)
-   `TextureFilter<enum_CanvasItem_TextureFilter>`
    **get\_texture\_filter**()

The texture filtering mode to use on this **CanvasItem**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureRepeat<enum_CanvasItem_TextureRepeat>` **texture\_repeat** = `0`
`🔗<class_CanvasItem_property_texture_repeat>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_repeat**(value:
    `TextureRepeat<enum_CanvasItem_TextureRepeat>`)
-   `TextureRepeat<enum_CanvasItem_TextureRepeat>`
    **get\_texture\_repeat**()

The texture repeating mode to use on this **CanvasItem**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **top\_level** = `false`
`🔗<class_CanvasItem_property_top_level>`

classref-property-setget

-   `void (No return value.)` **set\_as\_top\_level**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_set\_as\_top\_level**()

If `true`, this **CanvasItem** will *not* inherit its transform from
parent **CanvasItem**s. Its draw order will also be changed to make it
draw on top of other **CanvasItem**s that do not have
`top_level<class_CanvasItem_property_top_level>` set to `true`. The
**CanvasItem** will effectively act as if it was placed as a child of a
bare `Node<class_Node>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_parent\_material** = `false`
`🔗<class_CanvasItem_property_use_parent_material>`

classref-property-setget

-   `void (No return value.)` **set\_use\_parent\_material**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_use\_parent\_material**()

If `true`, the parent **CanvasItem**'s
`material<class_CanvasItem_property_material>` property is used as this
one's material.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **visibility\_layer** = `1`
`🔗<class_CanvasItem_property_visibility_layer>`

classref-property-setget

-   `void (No return value.)` **set\_visibility\_layer**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_visibility\_layer**()

The rendering layer in which this **CanvasItem** is rendered by
`Viewport<class_Viewport>` nodes. A `Viewport<class_Viewport>` will
render a **CanvasItem** if it and all its parents share a layer with the
`Viewport<class_Viewport>`'s canvas cull mask.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **visible** = `true`
`🔗<class_CanvasItem_property_visible>`

classref-property-setget

-   `void (No return value.)` **set\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_visible**()

If `true`, this **CanvasItem** may be drawn. Whether this **CanvasItem**
is actually drawn depends on the visibility of all of its **CanvasItem**
ancestors. In other words: this **CanvasItem** will be drawn when
`is_visible_in_tree<class_CanvasItem_method_is_visible_in_tree>` returns
`true` and all **CanvasItem** ancestors share at least one
`visibility_layer<class_CanvasItem_property_visibility_layer>` with this
**CanvasItem**.

\*\*Note:\*\* For controls that inherit `Popup<class_Popup>`, the
correct way to make them visible is to call one of the multiple
`popup*()` functions instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **y\_sort\_enabled** = `false`
`🔗<class_CanvasItem_property_y_sort_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_y\_sort\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_y\_sort\_enabled**()

If `true`, this and child **CanvasItem** nodes with a higher Y position
are rendered in front of nodes with a lower Y position. If `false`, this
and child **CanvasItem** nodes are rendered normally in scene tree
order.

With Y-sorting enabled on a parent node ('A') but disabled on a child
node ('B'), the child node ('B') is sorted but its children ('C1', 'C2',
etc) render together on the same Y position as the child node ('B').
This allows you to organize the render order of a scene without changing
the scene tree.

Nodes sort relative to each other only if they are on the same
`z_index<class_CanvasItem_property_z_index>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **z\_as\_relative** = `true`
`🔗<class_CanvasItem_property_z_as_relative>`

classref-property-setget

-   `void (No return value.)` **set\_z\_as\_relative**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_z\_relative**()

If `true`, the node's Z index is relative to its parent's Z index. If
this node's Z index is 2 and its parent's effective Z index is 3, then
this node's effective Z index will be 2 + 3 = 5.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **z\_index** = `0`
`🔗<class_CanvasItem_property_z_index>`

classref-property-setget

-   `void (No return value.)` **set\_z\_index**(value: `int<class_int>`)
-   `int<class_int>` **get\_z\_index**()

Controls the order in which the nodes render. A node with a higher Z
index will display in front of others. Must be between
`RenderingServer.CANVAS_ITEM_Z_MIN<class_RenderingServer_constant_CANVAS_ITEM_Z_MIN>`
and
`RenderingServer.CANVAS_ITEM_Z_MAX<class_RenderingServer_constant_CANVAS_ITEM_Z_MAX>`
(inclusive).

\*\*Note:\*\* Changing the Z index of a `Control<class_Control>` only
affects the drawing order, not the order in which input events are
handled. This can be useful to implement certain UI animations, e.g. a
menu where hovered items are scaled and should overlap others.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_draw**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_CanvasItem_private_method__draw>`

Called when **CanvasItem** has been requested to redraw (after
`queue_redraw<class_CanvasItem_method_queue_redraw>` is called, either
manually or by the engine).

Corresponds to the
`NOTIFICATION_DRAW<class_CanvasItem_constant_NOTIFICATION_DRAW>`
notification in
`Object._notification<class_Object_private_method__notification>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_animation\_slice**(animation\_length:
`float<class_float>`, slice\_begin: `float<class_float>`, slice\_end:
`float<class_float>`, offset: `float<class_float>` = 0.0)
`🔗<class_CanvasItem_method_draw_animation_slice>`

Subsequent drawing commands will be ignored unless they fall within the
specified animation slice. This is a faster way to implement animations
that loop on background rather than redrawing constantly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_arc**(center:
`Vector2<class_Vector2>`, radius: `float<class_float>`, start\_angle:
`float<class_float>`, end\_angle: `float<class_float>`, point\_count:
`int<class_int>`, color: `Color<class_Color>`, width:
`float<class_float>` = -1.0, antialiased: `bool<class_bool>` = false)
`🔗<class_CanvasItem_method_draw_arc>`

Draws an unfilled arc between the given angles with a uniform `color`
and `width` and optional antialiasing (supported only for positive
`width`). The larger the value of `point_count`, the smoother the curve.
See also `draw_circle<class_CanvasItem_method_draw_circle>`.

If `width` is negative, it will be ignored and the arc will be drawn
using
`RenderingServer.PRIMITIVE_LINE_STRIP<class_RenderingServer_constant_PRIMITIVE_LINE_STRIP>`.
This means that when the CanvasItem is scaled, the arc will remain thin.
If this behavior is not desired, then pass a positive `width` like
`1.0`.

The arc is drawn from `start_angle` towards the value of `end_angle` so
in clockwise direction if `start_angle < end_angle` and
counter-clockwise otherwise. Passing the same angles but in reversed
order will produce the same arc. If absolute difference of `start_angle`
and `end_angle` is greater than
`@GDScript.TAU<class_@GDScript_constant_TAU>` radians, then a full
circle arc is drawn (i.e. arc will not overlap itself).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_char**(font: `Font<class_Font>`, pos:
`Vector2<class_Vector2>`, char: `String<class_String>`, font\_size:
`int<class_int>` = 16, modulate: `Color<class_Color>` = Color(1, 1, 1,
1))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_draw_char>`

Draws a string first character using a custom font.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_char\_outline**(font:
`Font<class_Font>`, pos: `Vector2<class_Vector2>`, char:
`String<class_String>`, font\_size: `int<class_int>` = 16, size:
`int<class_int>` = -1, modulate: `Color<class_Color>` = Color(1, 1, 1,
1))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_draw_char_outline>`

Draws a string first character outline using a custom font.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_circle**(position:
`Vector2<class_Vector2>`, radius: `float<class_float>`, color:
`Color<class_Color>`, filled: `bool<class_bool>` = true, width:
`float<class_float>` = -1.0, antialiased: `bool<class_bool>` = false)
`🔗<class_CanvasItem_method_draw_circle>`

Draws a circle. See also `draw_arc<class_CanvasItem_method_draw_arc>`,
`draw_polyline<class_CanvasItem_method_draw_polyline>`, and
`draw_polygon<class_CanvasItem_method_draw_polygon>`.

If `filled` is `true`, the circle will be filled with the `color`
specified. If `filled` is `false`, the circle will be drawn as a stroke
with the `color` and `width` specified.

If `width` is negative, then two-point primitives will be drawn instead
of a four-point ones. This means that when the CanvasItem is scaled, the
lines will remain thin. If this behavior is not desired, then pass a
positive `width` like `1.0`.

If `antialiased` is `true`, half transparent "feathers" will be attached
to the boundary, making outlines smooth.

\*\*Note:\*\* `width` is only effective if `filled` is `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_colored\_polygon**(points:
`PackedVector2Array<class_PackedVector2Array>`, color:
`Color<class_Color>`, uvs:
`PackedVector2Array<class_PackedVector2Array>` = PackedVector2Array(),
texture: `Texture2D<class_Texture2D>` = null)
`🔗<class_CanvasItem_method_draw_colored_polygon>`

Draws a colored polygon of any number of points, convex or concave.
Unlike `draw_polygon<class_CanvasItem_method_draw_polygon>`, a single
color must be specified for the whole polygon.

\*\*Note:\*\* If you frequently redraw the same polygon with a large
number of vertices, consider pre-calculating the triangulation with
`Geometry2D.triangulate_polygon<class_Geometry2D_method_triangulate_polygon>`
and using `draw_mesh<class_CanvasItem_method_draw_mesh>`,
`draw_multimesh<class_CanvasItem_method_draw_multimesh>`, or
`RenderingServer.canvas_item_add_triangle_array<class_RenderingServer_method_canvas_item_add_triangle_array>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_dashed\_line**(from:
`Vector2<class_Vector2>`, to: `Vector2<class_Vector2>`, color:
`Color<class_Color>`, width: `float<class_float>` = -1.0, dash:
`float<class_float>` = 2.0, aligned: `bool<class_bool>` = true,
antialiased: `bool<class_bool>` = false)
`🔗<class_CanvasItem_method_draw_dashed_line>`

Draws a dashed line from a 2D point to another, with a given color and
width. See also `draw_multiline<class_CanvasItem_method_draw_multiline>`
and `draw_polyline<class_CanvasItem_method_draw_polyline>`.

If `width` is negative, then a two-point primitives will be drawn
instead of a four-point ones. This means that when the CanvasItem is
scaled, the line parts will remain thin. If this behavior is not
desired, then pass a positive `width` like `1.0`.

If `antialiased` is `true`, half transparent "feathers" will be attached
to the boundary, making outlines smooth.

\*\*Note:\*\* `antialiased` is only effective if `width` is greater than
`0.0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_end\_animation**()
`🔗<class_CanvasItem_method_draw_end_animation>`

After submitting all animations slices via
`draw_animation_slice<class_CanvasItem_method_draw_animation_slice>`,
this function can be used to revert drawing to its default state (all
subsequent drawing commands will be visible). If you don't care about
this particular use case, usage of this function after submitting the
slices is not required.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_lcd\_texture\_rect\_region**(texture:
`Texture2D<class_Texture2D>`, rect: `Rect2<class_Rect2>`, src\_rect:
`Rect2<class_Rect2>`, modulate: `Color<class_Color>` = Color(1, 1, 1,
1)) `🔗<class_CanvasItem_method_draw_lcd_texture_rect_region>`

Draws a textured rectangle region of the font texture with LCD subpixel
anti-aliasing at a given position, optionally modulated by a color.

Texture is drawn using the following blend operation, blend mode of the
`CanvasItemMaterial<class_CanvasItemMaterial>` is ignored:

    dst.r = texture.r * modulate.r * modulate.a + dst.r * (1.0 - texture.r * modulate.a);
    dst.g = texture.g * modulate.g * modulate.a + dst.g * (1.0 - texture.g * modulate.a);
    dst.b = texture.b * modulate.b * modulate.a + dst.b * (1.0 - texture.b * modulate.a);
    dst.a = modulate.a + dst.a * (1.0 - modulate.a);

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_line**(from: `Vector2<class_Vector2>`,
to: `Vector2<class_Vector2>`, color: `Color<class_Color>`, width:
`float<class_float>` = -1.0, antialiased: `bool<class_bool>` = false)
`🔗<class_CanvasItem_method_draw_line>`

Draws a line from a 2D point to another, with a given color and width.
It can be optionally antialiased. See also
`draw_multiline<class_CanvasItem_method_draw_multiline>` and
`draw_polyline<class_CanvasItem_method_draw_polyline>`.

If `width` is negative, then a two-point primitive will be drawn instead
of a four-point one. This means that when the CanvasItem is scaled, the
line will remain thin. If this behavior is not desired, then pass a
positive `width` like `1.0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_mesh**(mesh: `Mesh<class_Mesh>`,
texture: `Texture2D<class_Texture2D>`, transform:
`Transform2D<class_Transform2D>` = Transform2D(1, 0, 0, 1, 0, 0),
modulate: `Color<class_Color>` = Color(1, 1, 1, 1))
`🔗<class_CanvasItem_method_draw_mesh>`

Draws a `Mesh<class_Mesh>` in 2D, using the provided texture. See
`MeshInstance2D<class_MeshInstance2D>` for related documentation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_msdf\_texture\_rect\_region**(texture:
`Texture2D<class_Texture2D>`, rect: `Rect2<class_Rect2>`, src\_rect:
`Rect2<class_Rect2>`, modulate: `Color<class_Color>` = Color(1, 1, 1,
1), outline: `float<class_float>` = 0.0, pixel\_range:
`float<class_float>` = 4.0, scale: `float<class_float>` = 1.0)
`🔗<class_CanvasItem_method_draw_msdf_texture_rect_region>`

Draws a textured rectangle region of the multi-channel signed distance
field texture at a given position, optionally modulated by a color. See
`FontFile.multichannel_signed_distance_field<class_FontFile_property_multichannel_signed_distance_field>`
for more information and caveats about MSDF font rendering.

If `outline` is positive, each alpha channel value of pixel in region is
set to maximum value of true distance in the `outline` radius.

Value of the `pixel_range` should the same that was used during distance
field texture generation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_multiline**(points:
`PackedVector2Array<class_PackedVector2Array>`, color:
`Color<class_Color>`, width: `float<class_float>` = -1.0, antialiased:
`bool<class_bool>` = false) `🔗<class_CanvasItem_method_draw_multiline>`

Draws multiple disconnected lines with a uniform `width` and `color`.
Each line is defined by two consecutive points from `points` array, i.e.
i-th segment consists of `points[2 * i]`, `points[2 * i + 1]` endpoints.
When drawing large amounts of lines, this is faster than using
individual `draw_line<class_CanvasItem_method_draw_line>` calls. To draw
interconnected lines, use
`draw_polyline<class_CanvasItem_method_draw_polyline>` instead.

If `width` is negative, then two-point primitives will be drawn instead
of a four-point ones. This means that when the CanvasItem is scaled, the
lines will remain thin. If this behavior is not desired, then pass a
positive `width` like `1.0`.

\*\*Note:\*\* `antialiased` is only effective if `width` is greater than
`0.0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_multiline\_colors**(points:
`PackedVector2Array<class_PackedVector2Array>`, colors:
`PackedColorArray<class_PackedColorArray>`, width: `float<class_float>`
= -1.0, antialiased: `bool<class_bool>` = false)
`🔗<class_CanvasItem_method_draw_multiline_colors>`

Draws multiple disconnected lines with a uniform `width` and
segment-by-segment coloring. Each segment is defined by two consecutive
points from `points` array and a corresponding color from `colors`
array, i.e. i-th segment consists of `points[2 * i]`,
`points[2 * i + 1]` endpoints and has `colors[i]` color. When drawing
large amounts of lines, this is faster than using individual
`draw_line<class_CanvasItem_method_draw_line>` calls. To draw
interconnected lines, use
`draw_polyline_colors<class_CanvasItem_method_draw_polyline_colors>`
instead.

If `width` is negative, then two-point primitives will be drawn instead
of a four-point ones. This means that when the CanvasItem is scaled, the
lines will remain thin. If this behavior is not desired, then pass a
positive `width` like `1.0`.

\*\*Note:\*\* `antialiased` is only effective if `width` is greater than
`0.0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_multiline\_string**(font:
`Font<class_Font>`, pos: `Vector2<class_Vector2>`, text:
`String<class_String>`, alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` = 0, width:
`float<class_float>` = -1, font\_size: `int<class_int>` = 16,
max\_lines: `int<class_int>` = -1, modulate: `Color<class_Color>` =
Color(1, 1, 1, 1), brk\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`LineBreakFlag<enum_TextServer_LineBreakFlag>`\]
= 3, justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
= 3, direction: `Direction<enum_TextServer_Direction>` = 0, orientation:
`Orientation<enum_TextServer_Orientation>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_draw_multiline_string>`

Breaks `text` into lines and draws it using the specified `font` at the
`pos` (top-left corner). The text will have its color multiplied by
`modulate`. If `width` is greater than or equal to 0, the text will be
clipped if it exceeds the specified width.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_multiline\_string\_outline**(font:
`Font<class_Font>`, pos: `Vector2<class_Vector2>`, text:
`String<class_String>`, alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` = 0, width:
`float<class_float>` = -1, font\_size: `int<class_int>` = 16,
max\_lines: `int<class_int>` = -1, size: `int<class_int>` = 1, modulate:
`Color<class_Color>` = Color(1, 1, 1, 1), brk\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`LineBreakFlag<enum_TextServer_LineBreakFlag>`\]
= 3, justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
= 3, direction: `Direction<enum_TextServer_Direction>` = 0, orientation:
`Orientation<enum_TextServer_Orientation>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_draw_multiline_string_outline>`

Breaks `text` to the lines and draws text outline using the specified
`font` at the `pos` (top-left corner). The text will have its color
multiplied by `modulate`. If `width` is greater than or equal to 0, the
text will be clipped if it exceeds the specified width.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_multimesh**(multimesh:
`MultiMesh<class_MultiMesh>`, texture: `Texture2D<class_Texture2D>`)
`🔗<class_CanvasItem_method_draw_multimesh>`

Draws a `MultiMesh<class_MultiMesh>` in 2D with the provided texture.
See `MultiMeshInstance2D<class_MultiMeshInstance2D>` for related
documentation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_polygon**(points:
`PackedVector2Array<class_PackedVector2Array>`, colors:
`PackedColorArray<class_PackedColorArray>`, uvs:
`PackedVector2Array<class_PackedVector2Array>` = PackedVector2Array(),
texture: `Texture2D<class_Texture2D>` = null)
`🔗<class_CanvasItem_method_draw_polygon>`

Draws a solid polygon of any number of points, convex or concave. Unlike
`draw_colored_polygon<class_CanvasItem_method_draw_colored_polygon>`,
each point's color can be changed individually. See also
`draw_polyline<class_CanvasItem_method_draw_polyline>` and
`draw_polyline_colors<class_CanvasItem_method_draw_polyline_colors>`. If
you need more flexibility (such as being able to use bones), use
`RenderingServer.canvas_item_add_triangle_array<class_RenderingServer_method_canvas_item_add_triangle_array>`
instead.

\*\*Note:\*\* If you frequently redraw the same polygon with a large
number of vertices, consider pre-calculating the triangulation with
`Geometry2D.triangulate_polygon<class_Geometry2D_method_triangulate_polygon>`
and using `draw_mesh<class_CanvasItem_method_draw_mesh>`,
`draw_multimesh<class_CanvasItem_method_draw_multimesh>`, or
`RenderingServer.canvas_item_add_triangle_array<class_RenderingServer_method_canvas_item_add_triangle_array>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_polyline**(points:
`PackedVector2Array<class_PackedVector2Array>`, color:
`Color<class_Color>`, width: `float<class_float>` = -1.0, antialiased:
`bool<class_bool>` = false) `🔗<class_CanvasItem_method_draw_polyline>`

Draws interconnected line segments with a uniform `color` and `width`
and optional antialiasing (supported only for positive `width`). When
drawing large amounts of lines, this is faster than using individual
`draw_line<class_CanvasItem_method_draw_line>` calls. To draw
disconnected lines, use
`draw_multiline<class_CanvasItem_method_draw_multiline>` instead. See
also `draw_polygon<class_CanvasItem_method_draw_polygon>`.

If `width` is negative, it will be ignored and the polyline will be
drawn using
`RenderingServer.PRIMITIVE_LINE_STRIP<class_RenderingServer_constant_PRIMITIVE_LINE_STRIP>`.
This means that when the CanvasItem is scaled, the polyline will remain
thin. If this behavior is not desired, then pass a positive `width` like
`1.0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_polyline\_colors**(points:
`PackedVector2Array<class_PackedVector2Array>`, colors:
`PackedColorArray<class_PackedColorArray>`, width: `float<class_float>`
= -1.0, antialiased: `bool<class_bool>` = false)
`🔗<class_CanvasItem_method_draw_polyline_colors>`

Draws interconnected line segments with a uniform `width`,
point-by-point coloring, and optional antialiasing (supported only for
positive `width`). Colors assigned to line points match by index between
`points` and `colors`, i.e. each line segment is filled with a gradient
between the colors of the endpoints. When drawing large amounts of
lines, this is faster than using individual
`draw_line<class_CanvasItem_method_draw_line>` calls. To draw
disconnected lines, use
`draw_multiline_colors<class_CanvasItem_method_draw_multiline_colors>`
instead. See also `draw_polygon<class_CanvasItem_method_draw_polygon>`.

If `width` is negative, it will be ignored and the polyline will be
drawn using
`RenderingServer.PRIMITIVE_LINE_STRIP<class_RenderingServer_constant_PRIMITIVE_LINE_STRIP>`.
This means that when the CanvasItem is scaled, the polyline will remain
thin. If this behavior is not desired, then pass a positive `width` like
`1.0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_primitive**(points:
`PackedVector2Array<class_PackedVector2Array>`, colors:
`PackedColorArray<class_PackedColorArray>`, uvs:
`PackedVector2Array<class_PackedVector2Array>`, texture:
`Texture2D<class_Texture2D>` = null)
`🔗<class_CanvasItem_method_draw_primitive>`

Draws a custom primitive. 1 point for a point, 2 points for a line, 3
points for a triangle, and 4 points for a quad. If 0 points or more than
4 points are specified, nothing will be drawn and an error message will
be printed. See also `draw_line<class_CanvasItem_method_draw_line>`,
`draw_polyline<class_CanvasItem_method_draw_polyline>`,
`draw_polygon<class_CanvasItem_method_draw_polygon>`, and
`draw_rect<class_CanvasItem_method_draw_rect>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_rect**(rect: `Rect2<class_Rect2>`,
color: `Color<class_Color>`, filled: `bool<class_bool>` = true, width:
`float<class_float>` = -1.0, antialiased: `bool<class_bool>` = false)
`🔗<class_CanvasItem_method_draw_rect>`

Draws a rectangle. If `filled` is `true`, the rectangle will be filled
with the `color` specified. If `filled` is `false`, the rectangle will
be drawn as a stroke with the `color` and `width` specified. See also
`draw_texture_rect<class_CanvasItem_method_draw_texture_rect>`.

If `width` is negative, then two-point primitives will be drawn instead
of a four-point ones. This means that when the CanvasItem is scaled, the
lines will remain thin. If this behavior is not desired, then pass a
positive `width` like `1.0`.

If `antialiased` is `true`, half transparent "feathers" will be attached
to the boundary, making outlines smooth.

\*\*Note:\*\* `width` is only effective if `filled` is `false`.

\*\*Note:\*\* Unfilled rectangles drawn with a negative `width` may not
display perfectly. For example, corners may be missing or brighter due
to overlapping lines (for a translucent `color`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_set\_transform**(position:
`Vector2<class_Vector2>`, rotation: `float<class_float>` = 0.0, scale:
`Vector2<class_Vector2>` = Vector2(1, 1))
`🔗<class_CanvasItem_method_draw_set_transform>`

Sets a custom transform for drawing via components. Anything drawn
afterwards will be transformed by this.

\*\*Note:\*\*
`FontFile.oversampling<class_FontFile_property_oversampling>` does *not*
take `scale` into account. This means that scaling up/down will cause
bitmap fonts and rasterized (non-MSDF) dynamic fonts to appear blurry or
pixelated. To ensure text remains crisp regardless of scale, you can
enable MSDF font rendering by enabling
`ProjectSettings.gui/theme/default_font_multichannel_signed_distance_field<class_ProjectSettings_property_gui/theme/default_font_multichannel_signed_distance_field>`
(applies to the default project font only), or enabling **Multichannel
Signed Distance Field** in the import options of a DynamicFont for
custom fonts. On system fonts,
`SystemFont.multichannel_signed_distance_field<class_SystemFont_property_multichannel_signed_distance_field>`
can be enabled in the inspector.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_set\_transform\_matrix**(xform:
`Transform2D<class_Transform2D>`)
`🔗<class_CanvasItem_method_draw_set_transform_matrix>`

Sets a custom transform for drawing via matrix. Anything drawn
afterwards will be transformed by this.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_string**(font: `Font<class_Font>`,
pos: `Vector2<class_Vector2>`, text: `String<class_String>`, alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` = 0, width:
`float<class_float>` = -1, font\_size: `int<class_int>` = 16, modulate:
`Color<class_Color>` = Color(1, 1, 1, 1), justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
= 3, direction: `Direction<enum_TextServer_Direction>` = 0, orientation:
`Orientation<enum_TextServer_Orientation>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_draw_string>`

Draws `text` using the specified `font` at the `pos` (bottom-left corner
using the baseline of the font). The text will have its color multiplied
by `modulate`. If `width` is greater than or equal to 0, the text will
be clipped if it exceeds the specified width.

\*\*Example using the default project font:\*\*

gdscript

\# If using this method in a script that redraws constantly, move the \#
<span class="title-ref">default\_font</span> declaration to a member
variable assigned in <span class="title-ref">\_ready()</span> \# so the
Control is only created once. var default\_font = ThemeDB.fallback\_font
var default\_font\_size = ThemeDB.fallback\_font\_size
draw\_string(default\_font, Vector2(64, 64), "Hello world",
HORIZONTAL\_ALIGNMENT\_LEFT, -1, default\_font\_size)

csharp

// If using this method in a script that redraws constantly, move the //
<span class="title-ref">default\_font</span> declaration to a member
variable assigned in <span class="title-ref">\_Ready()</span> // so the
Control is only created once. Font defaultFont = ThemeDB.FallbackFont;
int defaultFontSize = ThemeDB.FallbackFontSize; DrawString(defaultFont,
new Vector2(64, 64), "Hello world", HORIZONTAL\_ALIGNMENT\_LEFT, -1,
defaultFontSize);

See also `Font.draw_string<class_Font_method_draw_string>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_string\_outline**(font:
`Font<class_Font>`, pos: `Vector2<class_Vector2>`, text:
`String<class_String>`, alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` = 0, width:
`float<class_float>` = -1, font\_size: `int<class_int>` = 16, size:
`int<class_int>` = 1, modulate: `Color<class_Color>` = Color(1, 1, 1,
1), justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
= 3, direction: `Direction<enum_TextServer_Direction>` = 0, orientation:
`Orientation<enum_TextServer_Orientation>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_draw_string_outline>`

Draws `text` outline using the specified `font` at the `pos`
(bottom-left corner using the baseline of the font). The text will have
its color multiplied by `modulate`. If `width` is greater than or equal
to 0, the text will be clipped if it exceeds the specified width.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_style\_box**(style\_box:
`StyleBox<class_StyleBox>`, rect: `Rect2<class_Rect2>`)
`🔗<class_CanvasItem_method_draw_style_box>`

Draws a styled rectangle.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_texture**(texture:
`Texture2D<class_Texture2D>`, position: `Vector2<class_Vector2>`,
modulate: `Color<class_Color>` = Color(1, 1, 1, 1))
`🔗<class_CanvasItem_method_draw_texture>`

Draws a texture at a given position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_texture\_rect**(texture:
`Texture2D<class_Texture2D>`, rect: `Rect2<class_Rect2>`, tile:
`bool<class_bool>`, modulate: `Color<class_Color>` = Color(1, 1, 1, 1),
transpose: `bool<class_bool>` = false)
`🔗<class_CanvasItem_method_draw_texture_rect>`

Draws a textured rectangle at a given position, optionally modulated by
a color. If `transpose` is `true`, the texture will have its X and Y
coordinates swapped. See also
`draw_rect<class_CanvasItem_method_draw_rect>` and
`draw_texture_rect_region<class_CanvasItem_method_draw_texture_rect_region>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw\_texture\_rect\_region**(texture:
`Texture2D<class_Texture2D>`, rect: `Rect2<class_Rect2>`, src\_rect:
`Rect2<class_Rect2>`, modulate: `Color<class_Color>` = Color(1, 1, 1,
1), transpose: `bool<class_bool>` = false, clip\_uv: `bool<class_bool>`
= true) `🔗<class_CanvasItem_method_draw_texture_rect_region>`

Draws a textured rectangle from a texture's region (specified by
`src_rect`) at a given position, optionally modulated by a color. If
`transpose` is `true`, the texture will have its X and Y coordinates
swapped. See also
`draw_texture_rect<class_CanvasItem_method_draw_texture_rect>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **force\_update\_transform**()
`🔗<class_CanvasItem_method_force_update_transform>`

Forces the transform to update. Transform changes in physics are not
instant for performance reasons. Transforms are accumulated and then
set. Use this if you need an up-to-date transform when doing physics
operations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_canvas**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_canvas>`

Returns the `RID<class_RID>` of the `World2D<class_World2D>` canvas
where this item is in.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_canvas\_item**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_canvas_item>`

Returns the canvas item RID used by
`RenderingServer<class_RenderingServer>` for this item.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CanvasLayer<class_CanvasLayer>` **get\_canvas\_layer\_node**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_canvas_layer_node>`

Returns the `CanvasLayer<class_CanvasLayer>` that contains this node, or
`null` if the node is not in any `CanvasLayer<class_CanvasLayer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **get\_canvas\_transform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_canvas_transform>`

Returns the transform from the coordinate system of the canvas, this
item is in, to the `Viewport<class_Viewport>`s coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_global\_mouse\_position**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_global_mouse_position>`

Returns the mouse's position in the `CanvasLayer<class_CanvasLayer>`
that this **CanvasItem** is in using the coordinate system of the
`CanvasLayer<class_CanvasLayer>`.

\*\*Note:\*\* For screen-space coordinates (e.g. when using a
non-embedded `Popup<class_Popup>`), you can use
`DisplayServer.mouse_get_position<class_DisplayServer_method_mouse_get_position>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **get\_global\_transform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_global_transform>`

Returns the global transform matrix of this item, i.e. the combined
transform up to the topmost **CanvasItem** node. The topmost item is a
**CanvasItem** that either has no parent, has non-**CanvasItem** parent
or it has `top_level<class_CanvasItem_property_top_level>` enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>`
**get\_global\_transform\_with\_canvas**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_global_transform_with_canvas>`

Returns the transform from the local coordinate system of this
**CanvasItem** to the `Viewport<class_Viewport>`s coordinate system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_local\_mouse\_position**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_local_mouse_position>`

Returns the mouse's position in this **CanvasItem** using the local
coordinate system of this **CanvasItem**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **get\_screen\_transform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_screen_transform>`

Returns the transform of this **CanvasItem** in global screen
coordinates (i.e. taking window position into account). Mostly useful
for editor plugins.

Equals to
`get_global_transform<class_CanvasItem_method_get_global_transform>` if
the window is embedded (see
`Viewport.gui_embed_subwindows<class_Viewport_property_gui_embed_subwindows>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **get\_transform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_transform>`

Returns the transform matrix of this item.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_viewport\_rect**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_viewport_rect>`

Returns the viewport's boundaries as a `Rect2<class_Rect2>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **get\_viewport\_transform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_viewport_transform>`

Returns the transform from the coordinate system of the canvas, this
item is in, to the `Viewport<class_Viewport>`s embedders coordinate
system.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_visibility\_layer\_bit**(layer:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_visibility_layer_bit>`

Returns an individual bit on the rendering visibility layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`World2D<class_World2D>` **get\_world\_2d**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_get_world_2d>`

Returns the `World2D<class_World2D>` where this item is in.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **hide**() `🔗<class_CanvasItem_method_hide>`

Hide the **CanvasItem** if it's currently visible. This is equivalent to
setting `visible<class_CanvasItem_property_visible>` to `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_local\_transform\_notification\_enabled**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_is_local_transform_notification_enabled>`

Returns `true` if local transform notifications are communicated to
children.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_transform\_notification\_enabled**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_is_transform_notification_enabled>`

Returns `true` if global transform notifications are communicated to
children.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_visible\_in\_tree**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_is_visible_in_tree>`

Returns `true` if the node is present in the
`SceneTree<class_SceneTree>`, its
`visible<class_CanvasItem_property_visible>` property is `true` and all
its ancestors are also visible. If any ancestor is hidden, this node
will not be visible in the scene tree, and is therefore not drawn (see
`_draw<class_CanvasItem_private_method__draw>`).

Visibility is checked only in parent nodes that inherit from
**CanvasItem**, `CanvasLayer<class_CanvasLayer>`, and
`Window<class_Window>`. If the parent is of any other type (such as
`Node<class_Node>`, `AnimationPlayer<class_AnimationPlayer>`, or
`Node3D<class_Node3D>`), it is assumed to be visible.

\*\*Note:\*\* This method does not take
`visibility_layer<class_CanvasItem_property_visibility_layer>` into
account, so even if this method returns `true` the node might end up not
being rendered.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>`
**make\_canvas\_position\_local**(screen\_point:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_make_canvas_position_local>`

Assigns `screen_point` as this node's new local transform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`InputEvent<class_InputEvent>` **make\_input\_local**(event:
`InputEvent<class_InputEvent>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CanvasItem_method_make_input_local>`

Transformations issued by `event`'s inputs are applied in local space
instead of global space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_to\_front**()
`🔗<class_CanvasItem_method_move_to_front>`

Moves this node to display on top of its siblings.

Internally, the node is moved to the bottom of parent's child list. The
method has no effect on nodes without a parent.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **queue\_redraw**()
`🔗<class_CanvasItem_method_queue_redraw>`

Queues the **CanvasItem** to redraw. During idle time, if **CanvasItem**
is visible,
`NOTIFICATION_DRAW<class_CanvasItem_constant_NOTIFICATION_DRAW>` is sent
and `_draw<class_CanvasItem_private_method__draw>` is called. This only
occurs **once** per frame, even if this method has been called multiple
times.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_notify\_local\_transform**(enable:
`bool<class_bool>`)
`🔗<class_CanvasItem_method_set_notify_local_transform>`

If `enable` is `true`, this node will receive
`NOTIFICATION_LOCAL_TRANSFORM_CHANGED<class_CanvasItem_constant_NOTIFICATION_LOCAL_TRANSFORM_CHANGED>`
when its local transform changes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_notify\_transform**(enable:
`bool<class_bool>`) `🔗<class_CanvasItem_method_set_notify_transform>`

If `enable` is `true`, this node will receive
`NOTIFICATION_TRANSFORM_CHANGED<class_CanvasItem_constant_NOTIFICATION_TRANSFORM_CHANGED>`
when its global transform changes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_visibility\_layer\_bit**(layer:
`int<class_int>`, enabled: `bool<class_bool>`)
`🔗<class_CanvasItem_method_set_visibility_layer_bit>`

Set/clear individual bits on the rendering visibility layer. This
simplifies editing this **CanvasItem**'s visibility layer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **show**() `🔗<class_CanvasItem_method_show>`

Show the **CanvasItem** if it's currently hidden. This is equivalent to
setting `visible<class_CanvasItem_property_visible>` to `true`. For
controls that inherit `Popup<class_Popup>`, the correct way to make them
visible is to call one of the multiple `popup*()` functions instead.
