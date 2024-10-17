github\_url  
hide

# Sprite3D

**Inherits:** `SpriteBase3D<class_SpriteBase3D>` **&lt;**
`GeometryInstance3D<class_GeometryInstance3D>` **&lt;**
`VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

2D sprite node in a 3D world.

classref-introduction-group

## Description

A node that displays a 2D texture in a 3D environment. The texture
displayed can be a region from a larger atlas texture, or a frame from a
sprite sheet animation. See also `SpriteBase3D<class_SpriteBase3D>`
where properties such as the billboard mode are defined.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**frame\_changed**() `🔗<class_Sprite3D_signal_frame_changed>`

Emitted when the `frame<class_Sprite3D_property_frame>` changes.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**texture\_changed**() `🔗<class_Sprite3D_signal_texture_changed>`

Emitted when the `texture<class_Sprite3D_property_texture>` changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **frame** = `0` `🔗<class_Sprite3D_property_frame>`

classref-property-setget

-   `void (No return value.)` **set\_frame**(value: `int<class_int>`)
-   `int<class_int>` **get\_frame**()

Current frame to display from sprite sheet.
`hframes<class_Sprite3D_property_hframes>` or
`vframes<class_Sprite3D_property_vframes>` must be greater than 1. This
property is automatically adjusted when
`hframes<class_Sprite3D_property_hframes>` or
`vframes<class_Sprite3D_property_vframes>` are changed to keep pointing
to the same visual frame (same column and row). If that's impossible,
this value is reset to `0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **frame\_coords** = `Vector2i(0, 0)`
`🔗<class_Sprite3D_property_frame_coords>`

classref-property-setget

-   `void (No return value.)` **set\_frame\_coords**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_frame\_coords**()

Coordinates of the frame to display from sprite sheet. This is as an
alias for the `frame<class_Sprite3D_property_frame>` property.
`hframes<class_Sprite3D_property_hframes>` or
`vframes<class_Sprite3D_property_vframes>` must be greater than 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **hframes** = `1` `🔗<class_Sprite3D_property_hframes>`

classref-property-setget

-   `void (No return value.)` **set\_hframes**(value: `int<class_int>`)
-   `int<class_int>` **get\_hframes**()

The number of columns in the sprite sheet. When this property is
changed, `frame<class_Sprite3D_property_frame>` is adjusted so that the
same visual frame is maintained (same row and column). If that's
impossible, `frame<class_Sprite3D_property_frame>` is reset to `0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **region\_enabled** = `false`
`🔗<class_Sprite3D_property_region_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_region\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_region\_enabled**()

If `true`, the sprite will use
`region_rect<class_Sprite3D_property_region_rect>` and display only the
specified part of its texture.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Rect2<class_Rect2>` **region\_rect** = `Rect2(0, 0, 0, 0)`
`🔗<class_Sprite3D_property_region_rect>`

classref-property-setget

-   `void (No return value.)` **set\_region\_rect**(value:
    `Rect2<class_Rect2>`)
-   `Rect2<class_Rect2>` **get\_region\_rect**()

The region of the atlas texture to display.
`region_enabled<class_Sprite3D_property_region_enabled>` must be `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture**
`🔗<class_Sprite3D_property_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**()

`Texture2D<class_Texture2D>` object to draw. If
`GeometryInstance3D.material_override<class_GeometryInstance3D_property_material_override>`
is used, this will be overridden. The size information is still used.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **vframes** = `1` `🔗<class_Sprite3D_property_vframes>`

classref-property-setget

-   `void (No return value.)` **set\_vframes**(value: `int<class_int>`)
-   `int<class_int>` **get\_vframes**()

The number of rows in the sprite sheet. When this property is changed,
`frame<class_Sprite3D_property_frame>` is adjusted so that the same
visual frame is maintained (same row and column). If that's impossible,
`frame<class_Sprite3D_property_frame>` is reset to `0`.
