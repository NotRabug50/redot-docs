github\_url  
hide

# Sprite2D

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

General-purpose sprite node.

classref-introduction-group

## Description

A node that displays a 2D texture. The texture displayed can be a region
from a larger atlas texture, or a frame from a sprite sheet animation.

classref-introduction-group

## Tutorials

-   [Instancing Demo](https://godotengine.org/asset-library/asset/2716)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**frame\_changed**() `🔗<class_Sprite2D_signal_frame_changed>`

Emitted when the `frame<class_Sprite2D_property_frame>` changes.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**texture\_changed**() `🔗<class_Sprite2D_signal_texture_changed>`

Emitted when the `texture<class_Sprite2D_property_texture>` changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **centered** = `true`
`🔗<class_Sprite2D_property_centered>`

classref-property-setget

-   `void (No return value.)` **set\_centered**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_centered**()

If `true`, texture is centered.

\*\*Note:\*\* For games with a pixel art aesthetic, textures may appear
deformed when centered. This is caused by their position being between
pixels. To prevent this, set this property to `false`, or consider
enabling
`ProjectSettings.rendering/2d/snap/snap_2d_vertices_to_pixel<class_ProjectSettings_property_rendering/2d/snap/snap_2d_vertices_to_pixel>`
and
`ProjectSettings.rendering/2d/snap/snap_2d_transforms_to_pixel<class_ProjectSettings_property_rendering/2d/snap/snap_2d_transforms_to_pixel>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **flip\_h** = `false`
`🔗<class_Sprite2D_property_flip_h>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_h**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_flipped\_h**()

If `true`, texture is flipped horizontally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **flip\_v** = `false`
`🔗<class_Sprite2D_property_flip_v>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_v**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_flipped\_v**()

If `true`, texture is flipped vertically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **frame** = `0` `🔗<class_Sprite2D_property_frame>`

classref-property-setget

-   `void (No return value.)` **set\_frame**(value: `int<class_int>`)
-   `int<class_int>` **get\_frame**()

Current frame to display from sprite sheet.
`hframes<class_Sprite2D_property_hframes>` or
`vframes<class_Sprite2D_property_vframes>` must be greater than 1. This
property is automatically adjusted when
`hframes<class_Sprite2D_property_hframes>` or
`vframes<class_Sprite2D_property_vframes>` are changed to keep pointing
to the same visual frame (same column and row). If that's impossible,
this value is reset to `0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **frame\_coords** = `Vector2i(0, 0)`
`🔗<class_Sprite2D_property_frame_coords>`

classref-property-setget

-   `void (No return value.)` **set\_frame\_coords**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_frame\_coords**()

Coordinates of the frame to display from sprite sheet. This is as an
alias for the `frame<class_Sprite2D_property_frame>` property.
`hframes<class_Sprite2D_property_hframes>` or
`vframes<class_Sprite2D_property_vframes>` must be greater than 1.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **hframes** = `1` `🔗<class_Sprite2D_property_hframes>`

classref-property-setget

-   `void (No return value.)` **set\_hframes**(value: `int<class_int>`)
-   `int<class_int>` **get\_hframes**()

The number of columns in the sprite sheet. When this property is
changed, `frame<class_Sprite2D_property_frame>` is adjusted so that the
same visual frame is maintained (same row and column). If that's
impossible, `frame<class_Sprite2D_property_frame>` is reset to `0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **offset** = `Vector2(0, 0)`
`🔗<class_Sprite2D_property_offset>`

classref-property-setget

-   `void (No return value.)` **set\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_offset**()

The texture's drawing offset.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **region\_enabled** = `false`
`🔗<class_Sprite2D_property_region_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_region\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_region\_enabled**()

If `true`, texture is cut from a larger atlas texture. See
`region_rect<class_Sprite2D_property_region_rect>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **region\_filter\_clip\_enabled** = `false`
`🔗<class_Sprite2D_property_region_filter_clip_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_region\_filter\_clip\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_region\_filter\_clip\_enabled**()

If `true`, the area outside of the
`region_rect<class_Sprite2D_property_region_rect>` is clipped to avoid
bleeding of the surrounding texture pixels.
`region_enabled<class_Sprite2D_property_region_enabled>` must be `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Rect2<class_Rect2>` **region\_rect** = `Rect2(0, 0, 0, 0)`
`🔗<class_Sprite2D_property_region_rect>`

classref-property-setget

-   `void (No return value.)` **set\_region\_rect**(value:
    `Rect2<class_Rect2>`)
-   `Rect2<class_Rect2>` **get\_region\_rect**()

The region of the atlas texture to display.
`region_enabled<class_Sprite2D_property_region_enabled>` must be `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture**
`🔗<class_Sprite2D_property_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**()

`Texture2D<class_Texture2D>` object to draw.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **vframes** = `1` `🔗<class_Sprite2D_property_vframes>`

classref-property-setget

-   `void (No return value.)` **set\_vframes**(value: `int<class_int>`)
-   `int<class_int>` **get\_vframes**()

The number of rows in the sprite sheet. When this property is changed,
`frame<class_Sprite2D_property_frame>` is adjusted so that the same
visual frame is maintained (same row and column). If that's impossible,
`frame<class_Sprite2D_property_frame>` is reset to `0`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Rect2<class_Rect2>` **get\_rect**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Sprite2D_method_get_rect>`

Returns a `Rect2<class_Rect2>` representing the Sprite2D's boundary in
local coordinates.

\*\*Example:\*\* Detect if the Sprite2D was clicked:

gdscript

func \_input(event):  
if event is InputEventMouseButton and event.pressed and event.button\_index == MOUSE\_BUTTON\_LEFT:  
if get\_rect().has\_point(to\_local(event.position)):  
print("A click!")

csharp

public override void \_Input(InputEvent @event) { if (@event is
InputEventMouseButton inputEventMouse) { if (inputEventMouse.Pressed &&
inputEventMouse.ButtonIndex == MouseButton.Left) { if
(GetRect().HasPoint(ToLocal(inputEventMouse.Position))) { GD.Print("A
click!"); } } } }

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_pixel\_opaque**(pos: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Sprite2D_method_is_pixel_opaque>`

Returns `true`, if the pixel at the given position is opaque and `false`
in other case. The position is in local coordinates.

\*\*Note:\*\* It also returns `false`, if the sprite's texture is `null`
or if the given position is invalid.
