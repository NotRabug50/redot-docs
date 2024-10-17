github\_url  
hide

# SubViewport

**Inherits:** `Viewport<class_Viewport>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

An interface to a game world that doesn't create a window or draw to the
screen directly.

classref-introduction-group

## Description

**SubViewport** Isolates a rectangular region of a scene to be displayed
independently. This can be used, for example, to display UI in 3D space.

\*\*Note:\*\* **SubViewport** is a `Viewport<class_Viewport>` that isn't
a `Window<class_Window>`, i.e. it doesn't draw anything by itself. To
display anything, **SubViewport** must have a non-zero size and be
either put inside a `SubViewportContainer<class_SubViewportContainer>`
or assigned to a `ViewportTexture<class_ViewportTexture>`.

classref-introduction-group

## Tutorials

-   `Using Viewports <../tutorials/rendering/viewports>`
-   `Viewport and canvas transforms <../tutorials/2d/2d_transforms>`
-   [GUI in 3D Viewport
    Demo](https://godotengine.org/asset-library/asset/2807)
-   [3D in 2D Viewport
    Demo](https://godotengine.org/asset-library/asset/2804)
-   [2D in 3D Viewport
    Demo](https://godotengine.org/asset-library/asset/2803)
-   [Screen Capture
    Demo](https://godotengine.org/asset-library/asset/2808)
-   [Dynamic Split Screen
    Demo](https://godotengine.org/asset-library/asset/2806)
-   [3D Resolution Scaling
    Demo](https://godotengine.org/asset-library/asset/2805)

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

## Enumerations

classref-enumeration

enum **ClearMode**: `🔗<enum_SubViewport_ClearMode>`

classref-enumeration-constant

`ClearMode<enum_SubViewport_ClearMode>` **CLEAR\_MODE\_ALWAYS** = `0`

Always clear the render target before drawing.

classref-enumeration-constant

`ClearMode<enum_SubViewport_ClearMode>` **CLEAR\_MODE\_NEVER** = `1`

Never clear the render target.

classref-enumeration-constant

`ClearMode<enum_SubViewport_ClearMode>` **CLEAR\_MODE\_ONCE** = `2`

Clear the render target on the next frame, then switch to
`CLEAR_MODE_NEVER<class_SubViewport_constant_CLEAR_MODE_NEVER>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **UpdateMode**: `🔗<enum_SubViewport_UpdateMode>`

classref-enumeration-constant

`UpdateMode<enum_SubViewport_UpdateMode>` **UPDATE\_DISABLED** = `0`

Do not update the render target.

classref-enumeration-constant

`UpdateMode<enum_SubViewport_UpdateMode>` **UPDATE\_ONCE** = `1`

Update the render target once, then switch to
`UPDATE_DISABLED<class_SubViewport_constant_UPDATE_DISABLED>`.

classref-enumeration-constant

`UpdateMode<enum_SubViewport_UpdateMode>` **UPDATE\_WHEN\_VISIBLE** =
`2`

Update the render target only when it is visible. This is the default
value.

classref-enumeration-constant

`UpdateMode<enum_SubViewport_UpdateMode>`
**UPDATE\_WHEN\_PARENT\_VISIBLE** = `3`

Update the render target only when its parent is visible.

classref-enumeration-constant

`UpdateMode<enum_SubViewport_UpdateMode>` **UPDATE\_ALWAYS** = `4`

Always update the render target.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`ClearMode<enum_SubViewport_ClearMode>` **render\_target\_clear\_mode**
= `0` `🔗<class_SubViewport_property_render_target_clear_mode>`

classref-property-setget

-   `void (No return value.)` **set\_clear\_mode**(value:
    `ClearMode<enum_SubViewport_ClearMode>`)
-   `ClearMode<enum_SubViewport_ClearMode>` **get\_clear\_mode**()

The clear mode when the sub-viewport is used as a render target.

\*\*Note:\*\* This property is intended for 2D usage.

classref-item-separator

------------------------------------------------------------------------

classref-property

`UpdateMode<enum_SubViewport_UpdateMode>`
**render\_target\_update\_mode** = `2`
`🔗<class_SubViewport_property_render_target_update_mode>`

classref-property-setget

-   `void (No return value.)` **set\_update\_mode**(value:
    `UpdateMode<enum_SubViewport_UpdateMode>`)
-   `UpdateMode<enum_SubViewport_UpdateMode>` **get\_update\_mode**()

The update mode when the sub-viewport is used as a render target.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **size** = `Vector2i(512, 512)`
`🔗<class_SubViewport_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_size**()

The width and height of the sub-viewport. Must be set to a value greater
than or equal to 2 pixels on both dimensions. Otherwise, nothing will be
displayed.

\*\*Note:\*\* If the parent node is a
`SubViewportContainer<class_SubViewportContainer>` and its
`SubViewportContainer.stretch<class_SubViewportContainer_property_stretch>`
is `true`, the viewport size cannot be changed manually.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2i<class_Vector2i>` **size\_2d\_override** = `Vector2i(0, 0)`
`🔗<class_SubViewport_property_size_2d_override>`

classref-property-setget

-   `void (No return value.)` **set\_size\_2d\_override**(value:
    `Vector2i<class_Vector2i>`)
-   `Vector2i<class_Vector2i>` **get\_size\_2d\_override**()

The 2D size override of the sub-viewport. If either the width or height
is `0`, the override is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **size\_2d\_override\_stretch** = `false`
`🔗<class_SubViewport_property_size_2d_override_stretch>`

classref-property-setget

-   `void (No return value.)`
    **set\_size\_2d\_override\_stretch**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_size\_2d\_override\_stretch\_enabled**()

If `true`, the 2D size override affects stretch as well.
