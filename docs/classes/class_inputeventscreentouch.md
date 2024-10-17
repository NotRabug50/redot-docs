github\_url  
hide

# InputEventScreenTouch

**Inherits:** `InputEventFromWindow<class_InputEventFromWindow>`
**&lt;** `InputEvent<class_InputEvent>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Represents a screen touch event.

classref-introduction-group

## Description

Stores information about multi-touch press/release input events.
Supports touch press, touch release and
`index<class_InputEventScreenTouch_property_index>` for multi-touch
count and order.

classref-introduction-group

## Tutorials

-   `Using InputEvent <../tutorials/inputs/inputevent>`

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

## Property Descriptions

classref-property

`bool<class_bool>` **canceled** = `false`
`🔗<class_InputEventScreenTouch_property_canceled>`

classref-property-setget

-   `void (No return value.)` **set\_canceled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_canceled**()

If `true`, the touch event has been canceled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **double\_tap** = `false`
`🔗<class_InputEventScreenTouch_property_double_tap>`

classref-property-setget

-   `void (No return value.)` **set\_double\_tap**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_double\_tap**()

If `true`, the touch's state is a double tap.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **index** = `0`
`🔗<class_InputEventScreenTouch_property_index>`

classref-property-setget

-   `void (No return value.)` **set\_index**(value: `int<class_int>`)
-   `int<class_int>` **get\_index**()

The touch index in the case of a multi-touch event. One index = one
finger.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **position** = `Vector2(0, 0)`
`🔗<class_InputEventScreenTouch_property_position>`

classref-property-setget

-   `void (No return value.)` **set\_position**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_position**()

The touch position in the viewport the node is in, using the coordinate
system of this viewport.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **pressed** = `false`
`🔗<class_InputEventScreenTouch_property_pressed>`

classref-property-setget

-   `void (No return value.)` **set\_pressed**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_pressed**()

If `true`, the touch's state is pressed. If `false`, the touch's state
is released.
