github\_url  
hide

# XRNode3D

**Inherits:** `Node3D<class_Node3D>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

**Inherited By:** `XRAnchor3D<class_XRAnchor3D>`,
`XRController3D<class_XRController3D>`

A spatial node that has its position automatically updated by the
`XRServer<class_XRServer>`.

classref-introduction-group

## Description

This node can be bound to a specific pose of a
`XRPositionalTracker<class_XRPositionalTracker>` and will automatically
have its `Node3D.transform<class_Node3D_property_transform>` updated by
the `XRServer<class_XRServer>`. Nodes of this type must be added as
children of the `XROrigin3D<class_XROrigin3D>` node.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**tracking\_changed**(tracking: `bool<class_bool>`)
`🔗<class_XRNode3D_signal_tracking_changed>`

Emitted when the `tracker<class_XRNode3D_property_tracker>` starts or
stops receiving updated tracking data for the
`pose<class_XRNode3D_property_pose>` being tracked. The `tracking`
argument indicates whether the tracker is getting updated tracking data.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`StringName<class_StringName>` **pose** = `&"default"`
`🔗<class_XRNode3D_property_pose>`

classref-property-setget

-   `void (No return value.)` **set\_pose\_name**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_pose\_name**()

The name of the pose we're bound to. Which poses a tracker supports is
not known during design time.

Godot defines number of standard pose names such as `aim` and `grip` but
other may be configured within a given `XRInterface<class_XRInterface>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **show\_when\_tracked** = `false`
`🔗<class_XRNode3D_property_show_when_tracked>`

classref-property-setget

-   `void (No return value.)` **set\_show\_when\_tracked**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_show\_when\_tracked**()

Enables showing the node when tracking starts, and hiding the node when
tracking is lost.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StringName<class_StringName>` **tracker** = `&""`
`🔗<class_XRNode3D_property_tracker>`

classref-property-setget

-   `void (No return value.)` **set\_tracker**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_tracker**()

The name of the tracker we're bound to. Which trackers are available is
not known during design time.

Godot defines a number of standard trackers such as `left_hand` and
`right_hand` but others may be configured within a given
`XRInterface<class_XRInterface>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **get\_has\_tracking\_data**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRNode3D_method_get_has_tracking_data>`

Returns `true` if the `tracker<class_XRNode3D_property_tracker>` has
current tracking data for the `pose<class_XRNode3D_property_pose>` being
tracked.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_is\_active**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRNode3D_method_get_is_active>`

Returns `true` if the `tracker<class_XRNode3D_property_tracker>` has
been registered and the `pose<class_XRNode3D_property_pose>` is being
tracked.

classref-item-separator

------------------------------------------------------------------------

classref-method

`XRPose<class_XRPose>` **get\_pose**()
`🔗<class_XRNode3D_method_get_pose>`

Returns the `XRPose<class_XRPose>` containing the current state of the
pose being tracked. This gives access to additional properties of this
pose.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **trigger\_haptic\_pulse**(action\_name:
`String<class_String>`, frequency: `float<class_float>`, amplitude:
`float<class_float>`, duration\_sec: `float<class_float>`, delay\_sec:
`float<class_float>`) `🔗<class_XRNode3D_method_trigger_haptic_pulse>`

Triggers a haptic pulse on a device associated with this interface.

`action_name` is the name of the action for this pulse.

`frequency` is the frequency of the pulse, set to `0.0` to have the
system use a default frequency.

`amplitude` is the amplitude of the pulse between `0.0` and `1.0`.

`duration_sec` is the duration of the pulse in seconds.

`delay_sec` is a delay in seconds before the pulse is given.
