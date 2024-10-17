github\_url  
hide

# SpriteBase3D

**Inherits:** `GeometryInstance3D<class_GeometryInstance3D>` **&lt;**
`VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `AnimatedSprite3D<class_AnimatedSprite3D>`,
`Sprite3D<class_Sprite3D>`

2D sprite node in 3D environment.

classref-introduction-group

## Description

A node that displays 2D texture information in a 3D environment. See
also `Sprite3D<class_Sprite3D>` where many other properties are defined.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **DrawFlags**: `🔗<enum_SpriteBase3D_DrawFlags>`

classref-enumeration-constant

`DrawFlags<enum_SpriteBase3D_DrawFlags>` **FLAG\_TRANSPARENT** = `0`

If set, the texture's transparency and the opacity are used to make
those parts of the sprite invisible.

classref-enumeration-constant

`DrawFlags<enum_SpriteBase3D_DrawFlags>` **FLAG\_SHADED** = `1`

If set, lights in the environment affect the sprite.

classref-enumeration-constant

`DrawFlags<enum_SpriteBase3D_DrawFlags>` **FLAG\_DOUBLE\_SIDED** = `2`

If set, texture can be seen from the back as well. If not, the texture
is invisible when looking at it from behind.

classref-enumeration-constant

`DrawFlags<enum_SpriteBase3D_DrawFlags>` **FLAG\_DISABLE\_DEPTH\_TEST**
= `3`

Disables the depth test, so this object is drawn on top of all others.
However, objects drawn after it in the draw order may cover it.

classref-enumeration-constant

`DrawFlags<enum_SpriteBase3D_DrawFlags>` **FLAG\_FIXED\_SIZE** = `4`

Label is scaled by depth so that it always appears the same size on
screen.

classref-enumeration-constant

`DrawFlags<enum_SpriteBase3D_DrawFlags>` **FLAG\_MAX** = `5`

Represents the size of the `DrawFlags<enum_SpriteBase3D_DrawFlags>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AlphaCutMode**: `🔗<enum_SpriteBase3D_AlphaCutMode>`

classref-enumeration-constant

`AlphaCutMode<enum_SpriteBase3D_AlphaCutMode>` **ALPHA\_CUT\_DISABLED**
= `0`

This mode performs standard alpha blending. It can display translucent
areas, but transparency sorting issues may be visible when multiple
transparent materials are overlapping.

classref-enumeration-constant

`AlphaCutMode<enum_SpriteBase3D_AlphaCutMode>` **ALPHA\_CUT\_DISCARD** =
`1`

This mode only allows fully transparent or fully opaque pixels. Harsh
edges will be visible unless some form of screen-space antialiasing is
enabled (see
`ProjectSettings.rendering/anti_aliasing/quality/screen_space_aa<class_ProjectSettings_property_rendering/anti_aliasing/quality/screen_space_aa>`).
On the bright side, this mode doesn't suffer from transparency sorting
issues when multiple transparent materials are overlapping. This mode is
also known as *alpha testing* or *1-bit transparency*.

classref-enumeration-constant

`AlphaCutMode<enum_SpriteBase3D_AlphaCutMode>`
**ALPHA\_CUT\_OPAQUE\_PREPASS** = `2`

This mode draws fully opaque pixels in the depth prepass. This is slower
than
`ALPHA_CUT_DISABLED<class_SpriteBase3D_constant_ALPHA_CUT_DISABLED>` or
`ALPHA_CUT_DISCARD<class_SpriteBase3D_constant_ALPHA_CUT_DISCARD>`, but
it allows displaying translucent areas and smooth edges while using
proper sorting.

classref-enumeration-constant

`AlphaCutMode<enum_SpriteBase3D_AlphaCutMode>` **ALPHA\_CUT\_HASH** =
`3`

This mode draws cuts off all values below a spatially-deterministic
threshold, the rest will remain opaque.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **alpha\_antialiasing\_edge** = `0.0`
`🔗<class_SpriteBase3D_property_alpha_antialiasing_edge>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_antialiasing\_edge**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_alpha\_antialiasing\_edge**()

Threshold at which antialiasing will be applied on the alpha channel.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`
**alpha\_antialiasing\_mode** = `0`
`🔗<class_SpriteBase3D_property_alpha_antialiasing_mode>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_antialiasing**(value:
    `AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`)
-   `AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`
    **get\_alpha\_antialiasing**()

The type of alpha antialiasing to apply. See
`AlphaAntiAliasing<enum_BaseMaterial3D_AlphaAntiAliasing>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AlphaCutMode<enum_SpriteBase3D_AlphaCutMode>` **alpha\_cut** = `0`
`🔗<class_SpriteBase3D_property_alpha_cut>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_cut\_mode**(value:
    `AlphaCutMode<enum_SpriteBase3D_AlphaCutMode>`)
-   `AlphaCutMode<enum_SpriteBase3D_AlphaCutMode>`
    **get\_alpha\_cut\_mode**()

The alpha cutting mode to use for the sprite. See
`AlphaCutMode<enum_SpriteBase3D_AlphaCutMode>` for possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **alpha\_hash\_scale** = `1.0`
`🔗<class_SpriteBase3D_property_alpha_hash_scale>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_hash\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_alpha\_hash\_scale**()

The hashing scale for Alpha Hash. Recommended values between `0` and
`2`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **alpha\_scissor\_threshold** = `0.5`
`🔗<class_SpriteBase3D_property_alpha_scissor_threshold>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_scissor\_threshold**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_alpha\_scissor\_threshold**()

Threshold at which the alpha scissor will discard values.

classref-item-separator

------------------------------------------------------------------------

classref-property

Vector3.Axis **axis** = `2` `🔗<class_SpriteBase3D_property_axis>`

classref-property-setget

-   `void (No return value.)` **set\_axis**(value: Vector3.Axis)
-   Vector3.Axis **get\_axis**()

The direction in which the front of the texture faces.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BillboardMode<enum_BaseMaterial3D_BillboardMode>` **billboard** = `0`
`🔗<class_SpriteBase3D_property_billboard>`

classref-property-setget

-   `void (No return value.)` **set\_billboard\_mode**(value:
    `BillboardMode<enum_BaseMaterial3D_BillboardMode>`)
-   `BillboardMode<enum_BaseMaterial3D_BillboardMode>`
    **get\_billboard\_mode**()

The billboard mode to use for the sprite. See
`BillboardMode<enum_BaseMaterial3D_BillboardMode>` for possible values.

\*\*Note:\*\* When billboarding is enabled and the material also casts
shadows, billboards will face **the** camera in the scene when rendering
shadows. In scenes with multiple cameras, the intended shadow cannot be
determined and this will result in undefined behavior. See [GitHub Pull
Request \#72638](https://github.com/godotengine/godot/pull/72638) for
details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **centered** = `true`
`🔗<class_SpriteBase3D_property_centered>`

classref-property-setget

-   `void (No return value.)` **set\_centered**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_centered**()

If `true`, texture will be centered.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **double\_sided** = `true`
`🔗<class_SpriteBase3D_property_double_sided>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_flag**(flag:
    `DrawFlags<enum_SpriteBase3D_DrawFlags>`, enabled:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_draw\_flag**(flag:
    `DrawFlags<enum_SpriteBase3D_DrawFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, texture can be seen from the back as well, if `false`, it is
invisible when looking at it from behind.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **fixed\_size** = `false`
`🔗<class_SpriteBase3D_property_fixed_size>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_flag**(flag:
    `DrawFlags<enum_SpriteBase3D_DrawFlags>`, enabled:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_draw\_flag**(flag:
    `DrawFlags<enum_SpriteBase3D_DrawFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the label is rendered at the same size regardless of
distance.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **flip\_h** = `false`
`🔗<class_SpriteBase3D_property_flip_h>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_h**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_flipped\_h**()

If `true`, texture is flipped horizontally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **flip\_v** = `false`
`🔗<class_SpriteBase3D_property_flip_v>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_v**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_flipped\_v**()

If `true`, texture is flipped vertically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **modulate** = `Color(1, 1, 1, 1)`
`🔗<class_SpriteBase3D_property_modulate>`

classref-property-setget

-   `void (No return value.)` **set\_modulate**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_modulate**()

A color value used to *multiply* the texture's colors. Can be used for
mood-coloring or to simulate the color of ambient light.

\*\*Note:\*\* Unlike
`CanvasItem.modulate<class_CanvasItem_property_modulate>` for 2D, colors
with values above `1.0` (overbright) are not supported.

\*\*Note:\*\* If a
`GeometryInstance3D.material_override<class_GeometryInstance3D_property_material_override>`
is defined on the **SpriteBase3D**, the material override must be
configured to take vertex colors into account for albedo. Otherwise, the
color defined in `modulate<class_SpriteBase3D_property_modulate>` will
be ignored. For a `BaseMaterial3D<class_BaseMaterial3D>`,
`BaseMaterial3D.vertex_color_use_as_albedo<class_BaseMaterial3D_property_vertex_color_use_as_albedo>`
must be `true`. For a `ShaderMaterial<class_ShaderMaterial>`,
`ALBEDO *= COLOR.rgb;` must be inserted in the shader's `fragment()`
function.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **no\_depth\_test** = `false`
`🔗<class_SpriteBase3D_property_no_depth_test>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_flag**(flag:
    `DrawFlags<enum_SpriteBase3D_DrawFlags>`, enabled:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_draw\_flag**(flag:
    `DrawFlags<enum_SpriteBase3D_DrawFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, depth testing is disabled and the object will be drawn in
render order.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **offset** = `Vector2(0, 0)`
`🔗<class_SpriteBase3D_property_offset>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_offset**()

The texture's drawing offset.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pixel\_size** = `0.01`
`🔗<class_SpriteBase3D_property_pixel_size>`

classref-property-setget

-   `void (No return value.)` **set\_pixel\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pixel\_size**()

The size of one pixel's width on the sprite to scale it in 3D.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **render\_priority** = `0`
`🔗<class_SpriteBase3D_property_render_priority>`

classref-property-setget

-   `void (No return value.)` **set\_render\_priority**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_render\_priority**()

Sets the render priority for the sprite. Higher priority objects will be
sorted in front of lower priority objects.

\*\*Note:\*\* This only applies if
`alpha_cut<class_SpriteBase3D_property_alpha_cut>` is set to
`ALPHA_CUT_DISABLED<class_SpriteBase3D_constant_ALPHA_CUT_DISABLED>`
(default value).

\*\*Note:\*\* This only applies to sorting of transparent objects. This
will not impact how transparent objects are sorted relative to opaque
objects. This is because opaque objects are not sorted, while
transparent objects are sorted from back to front (subject to priority).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shaded** = `false`
`🔗<class_SpriteBase3D_property_shaded>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_flag**(flag:
    `DrawFlags<enum_SpriteBase3D_DrawFlags>`, enabled:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_draw\_flag**(flag:
    `DrawFlags<enum_SpriteBase3D_DrawFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the `Light3D<class_Light3D>` in the
`Environment<class_Environment>` has effects on the sprite.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextureFilter<enum_BaseMaterial3D_TextureFilter>` **texture\_filter** =
`3` `🔗<class_SpriteBase3D_property_texture_filter>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_filter**(value:
    `TextureFilter<enum_BaseMaterial3D_TextureFilter>`)
-   `TextureFilter<enum_BaseMaterial3D_TextureFilter>`
    **get\_texture\_filter**()

Filter flags for the texture. See
`TextureFilter<enum_BaseMaterial3D_TextureFilter>` for options.

\*\*Note:\*\* Linear filtering may cause artifacts around the edges,
which are especially noticeable on opaque textures. To prevent this, use
textures with transparent or identical colors around the edges.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **transparent** = `true`
`🔗<class_SpriteBase3D_property_transparent>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_flag**(flag:
    `DrawFlags<enum_SpriteBase3D_DrawFlags>`, enabled:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_draw\_flag**(flag:
    `DrawFlags<enum_SpriteBase3D_DrawFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, the texture's transparency and the opacity are used to make
those parts of the sprite invisible.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`TriangleMesh<class_TriangleMesh>` **generate\_triangle\_mesh**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SpriteBase3D_method_generate_triangle_mesh>`

Returns a `TriangleMesh<class_TriangleMesh>` with the sprite's vertices
following its current configuration (such as its
`axis<class_SpriteBase3D_property_axis>` and
`pixel_size<class_SpriteBase3D_property_pixel_size>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_draw\_flag**(flag:
`DrawFlags<enum_SpriteBase3D_DrawFlags>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SpriteBase3D_method_get_draw_flag>`

Returns the value of the specified flag.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_item\_rect**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_SpriteBase3D_method_get_item_rect>`

Returns the rectangle representing this sprite.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_draw\_flag**(flag:
`DrawFlags<enum_SpriteBase3D_DrawFlags>`, enabled: `bool<class_bool>`)
`🔗<class_SpriteBase3D_method_set_draw_flag>`

If `true`, the specified flag will be enabled. See
`DrawFlags<enum_SpriteBase3D_DrawFlags>` for a list of flags.
