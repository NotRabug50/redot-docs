github\_url  
hide

# InputEventMouseMotion

**Inherits:** `InputEventMouse<class_InputEventMouse>` **&lt;**
`InputEventWithModifiers<class_InputEventWithModifiers>` **&lt;**
`InputEventFromWindow<class_InputEventFromWindow>` **&lt;**
`InputEvent<class_InputEvent>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Represents a mouse or a pen movement.

classref-introduction-group

## Description

Stores information about a mouse or a pen motion. This includes relative
position, absolute position, and velocity. See
`Node._input<class_Node_private_method__input>`.

\*\*Note:\*\* By default, this event is only emitted once per frame
rendered at most. If you need more precise input reporting, set
`Input.use_accumulated_input<class_Input_property_use_accumulated_input>`
to `false` to make events emitted as often as possible. If you use
InputEventMouseMotion to draw lines, consider implementing [Bresenham's
line
algorithm](https://en.wikipedia.org/wiki/Bresenham%27s_line_algorithm)
as well to avoid visible gaps in lines if the user is moving the mouse
quickly.

\*\*Note:\*\* This event may be emitted even when the mouse hasn't
moved, either by the operating system or by Godot itself. If you really
need to know if the mouse has moved (e.g. to suppress displaying a
tooltip), you should check that `relative.is_zero_approx()` is `false`.

classref-introduction-group

## Tutorials

-   `Using InputEvent <../tutorials/inputs/inputevent>`
-   `Mouse and input coordinates <../tutorials/inputs/mouse_and_input_coordinates>`
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **pen\_inverted** = `false`
`🔗<class_InputEventMouseMotion_property_pen_inverted>`

classref-property-setget

-   `void (No return value.)` **set\_pen\_inverted**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_pen\_inverted**()

Returns `true` when using the eraser end of a stylus pen.

\*\*Note:\*\* This property is implemented on Linux, macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **pressure** = `0.0`
`🔗<class_InputEventMouseMotion_property_pressure>`

classref-property-setget

-   `void (No return value.)` **set\_pressure**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pressure**()

Represents the pressure the user puts on the pen. Ranges from `0.0` to
`1.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **relative** = `Vector2(0, 0)`
`🔗<class_InputEventMouseMotion_property_relative>`

classref-property-setget

-   `void (No return value.)` **set\_relative**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_relative**()

The mouse position relative to the previous position (position at the
last frame).

\*\*Note:\*\* Since **InputEventMouseMotion** may only be emitted when
the mouse moves, it is not possible to reliably detect when the mouse
has stopped moving by checking this property. A separate, short timer
may be necessary.

\*\*Note:\*\* `relative<class_InputEventMouseMotion_property_relative>`
is automatically scaled according to the content scale factor, which is
defined by the project's stretch mode settings. This means mouse
sensitivity will appear different depending on resolution when using
`relative<class_InputEventMouseMotion_property_relative>` in a script
that handles mouse aiming with the
`Input.MOUSE_MODE_CAPTURED<class_Input_constant_MOUSE_MODE_CAPTURED>`
mouse mode. To avoid this, use
`screen_relative<class_InputEventMouseMotion_property_screen_relative>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **screen\_relative** = `Vector2(0, 0)`
`🔗<class_InputEventMouseMotion_property_screen_relative>`

classref-property-setget

-   `void (No return value.)` **set\_screen\_relative**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_screen\_relative**()

The unscaled mouse position relative to the previous position in the
coordinate system of the screen (position at the last frame).

\*\*Note:\*\* Since **InputEventMouseMotion** may only be emitted when
the mouse moves, it is not possible to reliably detect when the mouse
has stopped moving by checking this property. A separate, short timer
may be necessary.

\*\*Note:\*\* This coordinate is *not* scaled according to the content
scale factor or calls to
`InputEvent.xformed_by<class_InputEvent_method_xformed_by>`. This should
be preferred over
`relative<class_InputEventMouseMotion_property_relative>` for mouse
aiming when using the
`Input.MOUSE_MODE_CAPTURED<class_Input_constant_MOUSE_MODE_CAPTURED>`
mouse mode, regardless of the project's stretch mode.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **screen\_velocity** = `Vector2(0, 0)`
`🔗<class_InputEventMouseMotion_property_screen_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_screen\_velocity**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_screen\_velocity**()

The unscaled mouse velocity in pixels per second in screen coordinates.
This velocity is *not* scaled according to the content scale factor or
calls to `InputEvent.xformed_by<class_InputEvent_method_xformed_by>`.
This should be preferred over
`velocity<class_InputEventMouseMotion_property_velocity>` for mouse
aiming when using the
`Input.MOUSE_MODE_CAPTURED<class_Input_constant_MOUSE_MODE_CAPTURED>`
mouse mode, regardless of the project's stretch mode.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **tilt** = `Vector2(0, 0)`
`🔗<class_InputEventMouseMotion_property_tilt>`

classref-property-setget

-   `void (No return value.)` **set\_tilt**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_tilt**()

Represents the angles of tilt of the pen. Positive X-coordinate value
indicates a tilt to the right. Positive Y-coordinate value indicates a
tilt toward the user. Ranges from `-1.0` to `1.0` for both axes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **velocity** = `Vector2(0, 0)`
`🔗<class_InputEventMouseMotion_property_velocity>`

classref-property-setget

-   `void (No return value.)` **set\_velocity**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_velocity**()

The mouse velocity in pixels per second.

\*\*Note:\*\* `velocity<class_InputEventMouseMotion_property_velocity>`
is automatically scaled according to the content scale factor, which is
defined by the project's stretch mode settings. This means mouse
sensitivity will appear different depending on resolution when using
`velocity<class_InputEventMouseMotion_property_velocity>` in a script
that handles mouse aiming with the
`Input.MOUSE_MODE_CAPTURED<class_Input_constant_MOUSE_MODE_CAPTURED>`
mouse mode. To avoid this, use
`screen_velocity<class_InputEventMouseMotion_property_screen_velocity>`
instead.
