github\_url  
hide

# TextureRect

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A control that displays a texture.

classref-introduction-group

## Description

A control that displays a texture, for example an icon inside a GUI. The
texture's placement can be controlled with the
`stretch_mode<class_TextureRect_property_stretch_mode>` property. It can
scale, tile, or stay centered inside its bounding rectangle.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ExpandMode**: `🔗<enum_TextureRect_ExpandMode>`

classref-enumeration-constant

`ExpandMode<enum_TextureRect_ExpandMode>` **EXPAND\_KEEP\_SIZE** = `0`

The minimum size will be equal to texture size, i.e. **TextureRect**
can't be smaller than the texture.

classref-enumeration-constant

`ExpandMode<enum_TextureRect_ExpandMode>` **EXPAND\_IGNORE\_SIZE** = `1`

The size of the texture won't be considered for minimum size
calculation, so the **TextureRect** can be shrunk down past the texture
size.

classref-enumeration-constant

`ExpandMode<enum_TextureRect_ExpandMode>` **EXPAND\_FIT\_WIDTH** = `2`

The height of the texture will be ignored. Minimum width will be equal
to the current height. Useful for horizontal layouts, e.g. inside
`HBoxContainer<class_HBoxContainer>`.

classref-enumeration-constant

`ExpandMode<enum_TextureRect_ExpandMode>`
**EXPAND\_FIT\_WIDTH\_PROPORTIONAL** = `3`

Same as `EXPAND_FIT_WIDTH<class_TextureRect_constant_EXPAND_FIT_WIDTH>`,
but keeps texture's aspect ratio.

classref-enumeration-constant

`ExpandMode<enum_TextureRect_ExpandMode>` **EXPAND\_FIT\_HEIGHT** = `4`

The width of the texture will be ignored. Minimum height will be equal
to the current width. Useful for vertical layouts, e.g. inside
`VBoxContainer<class_VBoxContainer>`.

classref-enumeration-constant

`ExpandMode<enum_TextureRect_ExpandMode>`
**EXPAND\_FIT\_HEIGHT\_PROPORTIONAL** = `5`

Same as
`EXPAND_FIT_HEIGHT<class_TextureRect_constant_EXPAND_FIT_HEIGHT>`, but
keeps texture's aspect ratio.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **StretchMode**: `🔗<enum_TextureRect_StretchMode>`

classref-enumeration-constant

`StretchMode<enum_TextureRect_StretchMode>` **STRETCH\_SCALE** = `0`

Scale to fit the node's bounding rectangle.

classref-enumeration-constant

`StretchMode<enum_TextureRect_StretchMode>` **STRETCH\_TILE** = `1`

Tile inside the node's bounding rectangle.

classref-enumeration-constant

`StretchMode<enum_TextureRect_StretchMode>` **STRETCH\_KEEP** = `2`

The texture keeps its original size and stays in the bounding
rectangle's top-left corner.

classref-enumeration-constant

`StretchMode<enum_TextureRect_StretchMode>` **STRETCH\_KEEP\_CENTERED**
= `3`

The texture keeps its original size and stays centered in the node's
bounding rectangle.

classref-enumeration-constant

`StretchMode<enum_TextureRect_StretchMode>` **STRETCH\_KEEP\_ASPECT** =
`4`

Scale the texture to fit the node's bounding rectangle, but maintain the
texture's aspect ratio.

classref-enumeration-constant

`StretchMode<enum_TextureRect_StretchMode>`
**STRETCH\_KEEP\_ASPECT\_CENTERED** = `5`

Scale the texture to fit the node's bounding rectangle, center it and
maintain its aspect ratio.

classref-enumeration-constant

`StretchMode<enum_TextureRect_StretchMode>`
**STRETCH\_KEEP\_ASPECT\_COVERED** = `6`

Scale the texture so that the shorter side fits the bounding rectangle.
The other side clips to the node's limits.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`ExpandMode<enum_TextureRect_ExpandMode>` **expand\_mode** = `0`
`🔗<class_TextureRect_property_expand_mode>`

classref-property-setget

-   `void (No return value.)` **set\_expand\_mode**(value:
    `ExpandMode<enum_TextureRect_ExpandMode>`)
-   `ExpandMode<enum_TextureRect_ExpandMode>` **get\_expand\_mode**()

**Experimental:** Using
`EXPAND_FIT_WIDTH<class_TextureRect_constant_EXPAND_FIT_WIDTH>`,
`EXPAND_FIT_WIDTH_PROPORTIONAL<class_TextureRect_constant_EXPAND_FIT_WIDTH_PROPORTIONAL>`,
`EXPAND_FIT_HEIGHT<class_TextureRect_constant_EXPAND_FIT_HEIGHT>`, or
`EXPAND_FIT_HEIGHT_PROPORTIONAL<class_TextureRect_constant_EXPAND_FIT_HEIGHT_PROPORTIONAL>`
may result in unstable behavior in some `Container<class_Container>`
controls. This behavior may be re-evaluated and changed in the future.

Defines how minimum size is determined based on the texture's size. See
`ExpandMode<enum_TextureRect_ExpandMode>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **flip\_h** = `false`
`🔗<class_TextureRect_property_flip_h>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_h**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_flipped\_h**()

If `true`, texture is flipped horizontally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **flip\_v** = `false`
`🔗<class_TextureRect_property_flip_v>`

classref-property-setget

-   `void (No return value.)` **set\_flip\_v**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_flipped\_v**()

If `true`, texture is flipped vertically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StretchMode<enum_TextureRect_StretchMode>` **stretch\_mode** = `0`
`🔗<class_TextureRect_property_stretch_mode>`

classref-property-setget

-   `void (No return value.)` **set\_stretch\_mode**(value:
    `StretchMode<enum_TextureRect_StretchMode>`)
-   `StretchMode<enum_TextureRect_StretchMode>` **get\_stretch\_mode**()

Controls the texture's behavior when resizing the node's bounding
rectangle. See `StretchMode<enum_TextureRect_StretchMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture**
`🔗<class_TextureRect_property_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture**()

The node's `Texture2D<class_Texture2D>` resource.
