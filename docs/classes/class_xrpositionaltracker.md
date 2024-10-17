github\_url  
hide

# XRPositionalTracker

**Inherits:** `XRTracker<class_XRTracker>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `XRBodyTracker<class_XRBodyTracker>`,
`XRControllerTracker<class_XRControllerTracker>`,
`XRHandTracker<class_XRHandTracker>`

A tracked object.

classref-introduction-group

## Description

An instance of this object represents a device that is tracked, such as
a controller or anchor point. HMDs aren't represented here as they are
handled internally.

As controllers are turned on and the `XRInterface<class_XRInterface>`
detects them, instances of this object are automatically added to this
list of active tracking objects accessible through the
`XRServer<class_XRServer>`.

The `XRNode3D<class_XRNode3D>` and `XRAnchor3D<class_XRAnchor3D>` both
consume objects of this type and should be used in your project. The
positional trackers are just under-the-hood objects that make this all
work. These are mostly exposed so that GDExtension-based interfaces can
interact with them.

classref-introduction-group

## Tutorials

-   `XR documentation index <../tutorials/xr/index>`

classref-reftable-group

## Properties

<table>
<tbody>
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
`🔗<class_XRPositionalTracker_signal_button_pressed>`

Emitted when a button on this tracker is pressed. Note that many XR
runtimes allow other inputs to be mapped to buttons.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**button\_released**(name: `String<class_String>`)
`🔗<class_XRPositionalTracker_signal_button_released>`

Emitted when a button on this tracker is released.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**input\_float\_changed**(name: `String<class_String>`, value:
`float<class_float>`)
`🔗<class_XRPositionalTracker_signal_input_float_changed>`

Emitted when a trigger or similar input on this tracker changes value.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**input\_vector2\_changed**(name: `String<class_String>`, vector:
`Vector2<class_Vector2>`)
`🔗<class_XRPositionalTracker_signal_input_vector2_changed>`

Emitted when a thumbstick or thumbpad on this tracker moves.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**pose\_changed**(pose: `XRPose<class_XRPose>`)
`🔗<class_XRPositionalTracker_signal_pose_changed>`

Emitted when the state of a pose tracked by this tracker changes.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**pose\_lost\_tracking**(pose: `XRPose<class_XRPose>`)
`🔗<class_XRPositionalTracker_signal_pose_lost_tracking>`

Emitted when a pose tracked by this tracker stops getting updated
tracking data.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**profile\_changed**(role: `String<class_String>`)
`🔗<class_XRPositionalTracker_signal_profile_changed>`

Emitted when the profile of our tracker changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **TrackerHand**: `🔗<enum_XRPositionalTracker_TrackerHand>`

classref-enumeration-constant

`TrackerHand<enum_XRPositionalTracker_TrackerHand>`
**TRACKER\_HAND\_UNKNOWN** = `0`

The hand this tracker is held in is unknown or not applicable.

classref-enumeration-constant

`TrackerHand<enum_XRPositionalTracker_TrackerHand>`
**TRACKER\_HAND\_LEFT** = `1`

This tracker is the left hand controller.

classref-enumeration-constant

`TrackerHand<enum_XRPositionalTracker_TrackerHand>`
**TRACKER\_HAND\_RIGHT** = `2`

This tracker is the right hand controller.

classref-enumeration-constant

`TrackerHand<enum_XRPositionalTracker_TrackerHand>`
**TRACKER\_HAND\_MAX** = `3`

Represents the size of the
`TrackerHand<enum_XRPositionalTracker_TrackerHand>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`TrackerHand<enum_XRPositionalTracker_TrackerHand>` **hand** = `0`
`🔗<class_XRPositionalTracker_property_hand>`

classref-property-setget

-   `void (No return value.)` **set\_tracker\_hand**(value:
    `TrackerHand<enum_XRPositionalTracker_TrackerHand>`)
-   `TrackerHand<enum_XRPositionalTracker_TrackerHand>`
    **get\_tracker\_hand**()

Defines which hand this tracker relates to.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **profile** = `""`
`🔗<class_XRPositionalTracker_property_profile>`

classref-property-setget

-   `void (No return value.)` **set\_tracker\_profile**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_tracker\_profile**()

The profile associated with this tracker, interface dependent but will
indicate the type of controller being tracked.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Variant<class_Variant>` **get\_input**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRPositionalTracker_method_get_input>`

**Deprecated:** Use through
`XRControllerTracker<class_XRControllerTracker>`.

Returns an input for this tracker. It can return a boolean, float or
`Vector2<class_Vector2>` value depending on whether the input is a
button, trigger or thumbstick/thumbpad.

classref-item-separator

------------------------------------------------------------------------

classref-method

`XRPose<class_XRPose>` **get\_pose**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRPositionalTracker_method_get_pose>`

Returns the current `XRPose<class_XRPose>` state object for the bound
`name` pose.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_pose**(name: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRPositionalTracker_method_has_pose>`

Returns `true` if the tracker is available and is currently tracking the
bound `name` pose.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **invalidate\_pose**(name:
`StringName<class_StringName>`)
`🔗<class_XRPositionalTracker_method_invalidate_pose>`

Marks this pose as invalid, we don't clear the last reported state but
it allows users to decide if trackers need to be hidden if we lose
tracking or just remain at their last known position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_input**(name:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`🔗<class_XRPositionalTracker_method_set_input>`

**Deprecated:** Use through
`XRControllerTracker<class_XRControllerTracker>`.

Changes the value for the given input. This method is called by a
`XRInterface<class_XRInterface>` implementation and should not be used
directly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_pose**(name:
`StringName<class_StringName>`, transform:
`Transform3D<class_Transform3D>`, linear\_velocity:
`Vector3<class_Vector3>`, angular\_velocity: `Vector3<class_Vector3>`,
tracking\_confidence:
`TrackingConfidence<enum_XRPose_TrackingConfidence>`)
`🔗<class_XRPositionalTracker_method_set_pose>`

Sets the transform, linear velocity, angular velocity and tracking
confidence for the given pose. This method is called by a
`XRInterface<class_XRInterface>` implementation and should not be used
directly.
