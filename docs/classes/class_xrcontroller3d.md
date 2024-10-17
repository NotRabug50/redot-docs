github\_url  
hide

# XRController3D

**Inherits:** `XRNode3D<class_XRNode3D>` **&lt;** `Node3D<class_Node3D>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

A spatial node representing a spatially-tracked controller.

classref-introduction-group

## Description

This is a helper spatial node that is linked to the tracking of
controllers. It also offers several handy passthroughs to the state of
buttons and such on the controllers.

Controllers are linked by their ID. You can create controller nodes
before the controllers are available. If your game always uses two
controllers (one for each hand), you can predefine the controllers with
ID 1 and 2; they will become active as soon as the controllers are
identified. If you expect additional controllers to be used, you should
react to the signals and add XRController3D nodes to your scene.

The position of the controller node is automatically updated by the
`XRServer<class_XRServer>`. This makes this node ideal to add child
nodes to visualize the controller.

As many XR runtimes now use a configurable action map all inputs are
named.

classref-introduction-group

## Tutorials

-   `XR documentation index <../tutorials/xr/index>`

classref-reftable-group

## Methods

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

## Signals

classref-signal

**button\_pressed**(name: `String<class_String>`)
`🔗<class_XRController3D_signal_button_pressed>`

Emitted when a button on this controller is pressed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**button\_released**(name: `String<class_String>`)
`🔗<class_XRController3D_signal_button_released>`

Emitted when a button on this controller is released.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**input\_float\_changed**(name: `String<class_String>`, value:
`float<class_float>`)
`🔗<class_XRController3D_signal_input_float_changed>`

Emitted when a trigger or similar input on this controller changes
value.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**input\_vector2\_changed**(name: `String<class_String>`, value:
`Vector2<class_Vector2>`)
`🔗<class_XRController3D_signal_input_vector2_changed>`

Emitted when a thumbstick or thumbpad on this controller is moved.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**profile\_changed**(role: `String<class_String>`)
`🔗<class_XRController3D_signal_profile_changed>`

Emitted when the interaction profile on this controller is changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`float<class_float>` **get\_float**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRController3D_method_get_float>`

Returns a numeric value for the input with the given `name`. This is
used for triggers and grip sensors.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_input**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRController3D_method_get_input>`

Returns a `Variant<class_Variant>` for the input with the given `name`.
This works for any input type, the variant will be typed according to
the actions configuration.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TrackerHand<enum_XRPositionalTracker_TrackerHand>`
**get\_tracker\_hand**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRController3D_method_get_tracker_hand>`

Returns the hand holding this controller, if known. See
`TrackerHand<enum_XRPositionalTracker_TrackerHand>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_vector2**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRController3D_method_get_vector2>`

Returns a `Vector2<class_Vector2>` for the input with the given `name`.
This is used for thumbsticks and thumbpads found on many controllers.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_button\_pressed**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRController3D_method_is_button_pressed>`

Returns `true` if the button with the given `name` is pressed.
