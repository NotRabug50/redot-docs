github\_url  
hide

# InputEventGesture

**Inherits:** `InputEventWithModifiers<class_InputEventWithModifiers>`
**&lt;** `InputEventFromWindow<class_InputEventFromWindow>` **&lt;**
`InputEvent<class_InputEvent>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:**
`InputEventMagnifyGesture<class_InputEventMagnifyGesture>`,
`InputEventPanGesture<class_InputEventPanGesture>`

Abstract base class for touch gestures.

classref-introduction-group

## Description

InputEventGestures are sent when a user performs a supported gesture on
a touch screen. Gestures can't be emulated using mouse, because they
typically require multi-touch.

classref-introduction-group

## Tutorials

-   `Using InputEvent <../tutorials/inputs/inputevent>`

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Vector2<class_Vector2>` **position** = `Vector2(0, 0)`
`🔗<class_InputEventGesture_property_position>`

classref-property-setget

-   `void (No return value.)` **set\_position**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_position**()

The local gesture position relative to the `Viewport<class_Viewport>`.
If used in
`Control._gui_input<class_Control_private_method__gui_input>`, the
position is relative to the current `Control<class_Control>` that
received this gesture.
