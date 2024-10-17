github\_url  
hide

# InputEventPanGesture

**Inherits:** `InputEventGesture<class_InputEventGesture>` **&lt;**
`InputEventWithModifiers<class_InputEventWithModifiers>` **&lt;**
`InputEventFromWindow<class_InputEventFromWindow>` **&lt;**
`InputEvent<class_InputEvent>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Represents a panning touch gesture.

classref-introduction-group

## Description

Stores information about pan gestures. A pan gesture is performed when
the user swipes the touch screen with two fingers. It's typically used
for panning/scrolling.

\*\*Note:\*\* On Android, this requires the
`ProjectSettings.input_devices/pointing/android/enable_pan_and_scale_gestures<class_ProjectSettings_property_input_devices/pointing/android/enable_pan_and_scale_gestures>`
project setting to be enabled.

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

`Vector2<class_Vector2>` **delta** = `Vector2(0, 0)`
`🔗<class_InputEventPanGesture_property_delta>`

classref-property-setget

-   `void (No return value.)` **set\_delta**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_delta**()

Panning amount since last pan event.
