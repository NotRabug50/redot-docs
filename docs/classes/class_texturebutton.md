github\_url  
hide

# TextureButton

**Inherits:** `BaseButton<class_BaseButton>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

Texture-based button. Supports Pressed, Hover, Disabled and Focused
states.

classref-introduction-group

## Description

**TextureButton** has the same functionality as `Button<class_Button>`,
except it uses sprites instead of Godot's `Theme<class_Theme>` resource.
It is faster to create, but it doesn't support localization like more
complex `Control<class_Control>`s.

The "normal" state must contain a texture
(`texture_normal<class_TextureButton_property_texture_normal>`); other
textures are optional.

See also `BaseButton<class_BaseButton>` which contains common properties
and methods associated with this node.

classref-introduction-group

## Tutorials

-   [3D Voxel Demo](https://godotengine.org/asset-library/asset/2755)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **StretchMode**: `🔗<enum_TextureButton_StretchMode>`

classref-enumeration-constant

`StretchMode<enum_TextureButton_StretchMode>` **STRETCH\_SCALE** = `0`

Scale to fit the node's bounding rectangle.

classref-enumeration-constant

`StretchMode<enum_TextureButton_StretchMode>` **STRETCH\_TILE** = `1`

Tile inside the node's bounding rectangle.

classref-enumeration-constant

`StretchMode<enum_TextureButton_StretchMode>` **STRETCH\_KEEP** = `2`

The texture keeps its original size and stays in the bounding
rectangle's top-left corner.

classref-enumeration-constant

`StretchMode<enum_TextureButton_StretchMode>`
**STRETCH\_KEEP\_CENTERED** = `3`

The texture keeps its original size and stays centered in the node's
bounding rectangle.

classref-enumeration-constant

`StretchMode<enum_TextureButton_StretchMode>` **STRETCH\_KEEP\_ASPECT**
= `4`

Scale the texture to fit the node's bounding rectangle, but maintain the
texture's aspect ratio.

classref-enumeration-constant

`StretchMode<enum_TextureButton_StretchMode>`
**STRETCH\_KEEP\_ASPECT\_CENTERED** = `5`

Scale the texture to fit the node's bounding rectangle, center it, and
maintain its aspect ratio.

classref-enumeration-constant

`StretchMode<enum_TextureButton_StretchMode>`
**STRETCH\_KEEP\_ASPECT\_COVERED** = `6`

Scale the texture so that the shorter side fits the bounding rectangle.
The other side clips to the node's limits.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **flip\_h** = `false`
`🔗<class_TextureButton_property_flip_h>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_h**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_flipped\_h**()

If `true`, texture is flipped horizontally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **flip\_v** = `false`
`🔗<class_TextureButton_property_flip_v>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_v**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_flipped\_v**()

If `true`, texture is flipped vertically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ignore\_texture\_size** = `false`
`🔗<class_TextureButton_property_ignore_texture_size>`

classref-property-setget

-   `void (No return value.)` **set\_ignore\_texture\_size**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_ignore\_texture\_size**()

If `true`, the size of the texture won't be considered for minimum size
calculation, so the **TextureButton** can be shrunk down past the
texture size.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StretchMode<enum_TextureButton_StretchMode>` **stretch\_mode** = `2`
`🔗<class_TextureButton_property_stretch_mode>`

classref-property-setget

-   `void (No return value.)` **set\_stretch\_mode**(value:
    `StretchMode<enum_TextureButton_StretchMode>`)
-   `StretchMode<enum_TextureButton_StretchMode>`
    **get\_stretch\_mode**()

Controls the texture's behavior when you resize the node's bounding
rectangle. See the `StretchMode<enum_TextureButton_StretchMode>`
constants for available options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitMap<class_BitMap>` **texture\_click\_mask**
`🔗<class_TextureButton_property_texture_click_mask>`

classref-property-setget

-   `void (No return value.)` **set\_click\_mask**(value:
    `BitMap<class_BitMap>`)
-   `BitMap<class_BitMap>` **get\_click\_mask**()

Pure black and white `BitMap<class_BitMap>` image to use for click
detection. On the mask, white pixels represent the button's clickable
area. Use it to create buttons with curved shapes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture\_disabled**
`🔗<class_TextureButton_property_texture_disabled>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_disabled**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture\_disabled**()

Texture to display when the node is disabled. See
`BaseButton.disabled<class_BaseButton_property_disabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture\_focused**
`🔗<class_TextureButton_property_texture_focused>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_focused**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture\_focused**()

Texture to display when the node has mouse or keyboard focus.
`texture_focused<class_TextureButton_property_texture_focused>` is
displayed *over* the base texture, so a partially transparent texture
should be used to ensure the base texture remains visible. A texture
that represents an outline or an underline works well for this purpose.
To disable the focus visual effect, assign a fully transparent texture
of any size. Note that disabling the focus visual effect will harm
keyboard/controller navigation usability, so this is not recommended for
accessibility reasons.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture\_hover**
`🔗<class_TextureButton_property_texture_hover>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_hover**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture\_hover**()

Texture to display when the mouse hovers the node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture\_normal**
`🔗<class_TextureButton_property_texture_normal>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_normal**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture\_normal**()

Texture to display by default, when the node is **not** in the disabled,
hover or pressed state. This texture is still displayed in the focused
state, with
`texture_focused<class_TextureButton_property_texture_focused>` drawn on
top.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture\_pressed**
`🔗<class_TextureButton_property_texture_pressed>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_pressed**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture\_pressed**()

Texture to display on mouse down over the node, if the node has keyboard
focus and the player presses the Enter key or if the player presses the
`BaseButton.shortcut<class_BaseButton_property_shortcut>` key.
