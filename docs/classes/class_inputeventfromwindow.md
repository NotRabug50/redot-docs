github\_url  
hide

# InputEventFromWindow

**Inherits:** `InputEvent<class_InputEvent>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:** `InputEventScreenDrag<class_InputEventScreenDrag>`,
`InputEventScreenTouch<class_InputEventScreenTouch>`,
`InputEventWithModifiers<class_InputEventWithModifiers>`

Abstract base class for `Viewport<class_Viewport>`-based input events.

classref-introduction-group

## Description

InputEventFromWindow represents events specifically received by windows.
This includes mouse events, keyboard events in focused windows or touch
screen actions.

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

`int<class_int>` **window\_id** = `0`
`🔗<class_InputEventFromWindow_property_window_id>`

classref-property-setget

-   `void (No return value.)` **set\_window\_id**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_window\_id**()

The ID of a `Window<class_Window>` that received this event.
