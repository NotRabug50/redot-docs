github\_url  
hide

# TouchScreenButton

**Inherits:** `Node2D<class_Node2D>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Button for touch screen devices for gameplay use.

classref-introduction-group

## Description

TouchScreenButton allows you to create on-screen buttons for touch
devices. It's intended for gameplay use, such as a unit you have to
touch to move. Unlike `Button<class_Button>`, TouchScreenButton supports
multitouch out of the box. Several TouchScreenButtons can be pressed at
the same time with touch input.

This node inherits from `Node2D<class_Node2D>`. Unlike with
`Control<class_Control>` nodes, you cannot set anchors on it. If you
want to create menus or user interfaces, you may want to use
`Button<class_Button>` nodes instead. To make button nodes react to
touch events, you can enable the Emulate Mouse option in the Project
Settings.

You can configure TouchScreenButton to be visible only on touch devices,
helping you develop your game both for desktop and mobile devices.

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
</tbody>
</table>

classref-reftable-group

## Methods

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**pressed**() `🔗<class_TouchScreenButton_signal_pressed>`

Emitted when the button is pressed (down).

classref-item-separator

------------------------------------------------------------------------

classref-signal

**released**() `🔗<class_TouchScreenButton_signal_released>`

Emitted when the button is released (up).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **VisibilityMode**: `🔗<enum_TouchScreenButton_VisibilityMode>`

classref-enumeration-constant

`VisibilityMode<enum_TouchScreenButton_VisibilityMode>`
**VISIBILITY\_ALWAYS** = `0`

Always visible.

classref-enumeration-constant

`VisibilityMode<enum_TouchScreenButton_VisibilityMode>`
**VISIBILITY\_TOUCHSCREEN\_ONLY** = `1`

Visible on touch screens only.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **action** = `""`
`🔗<class_TouchScreenButton_property_action>`

classref-property-setget

-   `void (No return value.)` **set\_action**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_action**()

The button's action. Actions can be handled with
`InputEventAction<class_InputEventAction>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitMap<class_BitMap>` **bitmask**
`🔗<class_TouchScreenButton_property_bitmask>`

classref-property-setget

-   `void (No return value.)` **set\_bitmask**(value:
    `BitMap<class_BitMap>`)
-   `BitMap<class_BitMap>` **get\_bitmask**()

The button's bitmask.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **passby\_press** = `false`
`🔗<class_TouchScreenButton_property_passby_press>`

classref-property-setget

-   `void (No return value.)` **set\_passby\_press**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_passby\_press\_enabled**()

If `true`, the `pressed<class_TouchScreenButton_signal_pressed>` and
`released<class_TouchScreenButton_signal_released>` signals are emitted
whenever a pressed finger goes in and out of the button, even if the
pressure started outside the active area of the button.

\*\*Note:\*\* This is a "pass-by" (not "bypass") press mode.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Shape2D<class_Shape2D>` **shape**
`🔗<class_TouchScreenButton_property_shape>`

classref-property-setget

-   `void (No return value.)` **set\_shape**(value:
    `Shape2D<class_Shape2D>`)
-   `Shape2D<class_Shape2D>` **get\_shape**()

The button's shape.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shape\_centered** = `true`
`🔗<class_TouchScreenButton_property_shape_centered>`

classref-property-setget

-   `void (No return value.)` **set\_shape\_centered**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_shape\_centered**()

If `true`, the button's shape is centered in the provided texture. If no
texture is used, this property has no effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shape\_visible** = `true`
`🔗<class_TouchScreenButton_property_shape_visible>`

classref-property-setget

-   `void (No return value.)` **set\_shape\_visible**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_shape\_visible**()

If `true`, the button's shape is visible in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture\_normal**
`🔗<class_TouchScreenButton_property_texture_normal>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_normal**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture\_normal**()

The button's texture for the normal state.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **texture\_pressed**
`🔗<class_TouchScreenButton_property_texture_pressed>`

classref-property-setget

-   `void (No return value.)` **set\_texture\_pressed**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_texture\_pressed**()

The button's texture for the pressed state.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VisibilityMode<enum_TouchScreenButton_VisibilityMode>`
**visibility\_mode** = `0`
`🔗<class_TouchScreenButton_property_visibility_mode>`

classref-property-setget

-   `void (No return value.)` **set\_visibility\_mode**(value:
    `VisibilityMode<enum_TouchScreenButton_VisibilityMode>`)
-   `VisibilityMode<enum_TouchScreenButton_VisibilityMode>`
    **get\_visibility\_mode**()

The button's visibility mode. See
`VisibilityMode<enum_TouchScreenButton_VisibilityMode>` for possible
values.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **is\_pressed**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TouchScreenButton_method_is_pressed>`

Returns `true` if this button is currently pressed.
