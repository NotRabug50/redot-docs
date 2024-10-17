github\_url  
hide

# InputEventMagnifyGesture

**Inherits:** `InputEventGesture<class_InputEventGesture>` **&lt;**
`InputEventWithModifiers<class_InputEventWithModifiers>` **&lt;**
`InputEventFromWindow<class_InputEventFromWindow>` **&lt;**
`InputEvent<class_InputEvent>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Represents a magnifying touch gesture.

classref-introduction-group

## Description

Stores the factor of a magnifying touch gesture. This is usually
performed when the user pinches the touch screen and used for zooming
in/out.

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

`float<class_float>` **factor** = `1.0`
`🔗<class_InputEventMagnifyGesture_property_factor>`

classref-property-setget

-   `void (No return value.)` **set\_factor**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_factor**()

The amount (or delta) of the event. This value is closer to `1.0` the
slower the gesture is performed.
