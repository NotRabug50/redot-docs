github\_url  
hide

# OpenXRInterface

**Inherits:** `XRInterface<class_XRInterface>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Our OpenXR interface.

classref-introduction-group

## Description

The OpenXR interface allows Godot to interact with OpenXR runtimes and
make it possible to create XR experiences and games.

Due to the needs of OpenXR this interface works slightly different than
other plugin based XR interfaces. It needs to be initialized when Godot
starts. You need to enable OpenXR, settings for this can be found in
your games project settings under the XR heading. You do need to mark a
viewport for use with XR in order for Godot to know which render result
should be output to the headset.

classref-introduction-group

## Tutorials

-   `Setting up XR <../tutorials/xr/setting_up_xr>`

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

**instance\_exiting**()
`🔗<class_OpenXRInterface_signal_instance_exiting>`

Informs our OpenXR instance is exiting.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**pose\_recentered**()
`🔗<class_OpenXRInterface_signal_pose_recentered>`

Informs the user queued a recenter of the player position.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**refresh\_rate\_changed**(refresh\_rate: `float<class_float>`)
`🔗<class_OpenXRInterface_signal_refresh_rate_changed>`

Informs the user the HMD refresh rate has changed.

\*\*Note:\*\* Only emitted if XR runtime supports the refresh rate
extension.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**session\_begun**() `🔗<class_OpenXRInterface_signal_session_begun>`

Informs our OpenXR session has been started.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**session\_focussed**()
`🔗<class_OpenXRInterface_signal_session_focussed>`

Informs our OpenXR session now has focus.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**session\_loss\_pending**()
`🔗<class_OpenXRInterface_signal_session_loss_pending>`

Informs our OpenXR session is in the process of being lost.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**session\_stopping**()
`🔗<class_OpenXRInterface_signal_session_stopping>`

Informs our OpenXR session is stopping.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**session\_visible**()
`🔗<class_OpenXRInterface_signal_session_visible>`

Informs our OpenXR session is now visible (output is being sent to the
HMD).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Hand**: `🔗<enum_OpenXRInterface_Hand>`

classref-enumeration-constant

`Hand<enum_OpenXRInterface_Hand>` **HAND\_LEFT** = `0`

Left hand.

classref-enumeration-constant

`Hand<enum_OpenXRInterface_Hand>` **HAND\_RIGHT** = `1`

Right hand.

classref-enumeration-constant

`Hand<enum_OpenXRInterface_Hand>` **HAND\_MAX** = `2`

Maximum value for the hand enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **HandMotionRange**: `🔗<enum_OpenXRInterface_HandMotionRange>`

classref-enumeration-constant

`HandMotionRange<enum_OpenXRInterface_HandMotionRange>`
**HAND\_MOTION\_RANGE\_UNOBSTRUCTED** = `0`

Full hand range, if user closes their hands, we make a full fist.

classref-enumeration-constant

`HandMotionRange<enum_OpenXRInterface_HandMotionRange>`
**HAND\_MOTION\_RANGE\_CONFORM\_TO\_CONTROLLER** = `1`

Conform to controller, if user closes their hands, the tracked data
conforms to the shape of the controller.

classref-enumeration-constant

`HandMotionRange<enum_OpenXRInterface_HandMotionRange>`
**HAND\_MOTION\_RANGE\_MAX** = `2`

Maximum value for the motion range enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **HandTrackedSource**: `🔗<enum_OpenXRInterface_HandTrackedSource>`

classref-enumeration-constant

`HandTrackedSource<enum_OpenXRInterface_HandTrackedSource>`
**HAND\_TRACKED\_SOURCE\_UNKNOWN** = `0`

The source of hand tracking data is unknown (the extension is likely
unsupported).

classref-enumeration-constant

`HandTrackedSource<enum_OpenXRInterface_HandTrackedSource>`
**HAND\_TRACKED\_SOURCE\_UNOBSTRUCTED** = `1`

The source of hand tracking is unobstructed, this means that an accurate
method of hand tracking is used, e.g. optical hand tracking, data
gloves, etc.

classref-enumeration-constant

`HandTrackedSource<enum_OpenXRInterface_HandTrackedSource>`
**HAND\_TRACKED\_SOURCE\_CONTROLLER** = `2`

The source of hand tracking is a controller, bone positions are inferred
from controller inputs.

classref-enumeration-constant

`HandTrackedSource<enum_OpenXRInterface_HandTrackedSource>`
**HAND\_TRACKED\_SOURCE\_MAX** = `3`

Maximum value for the hand tracked source enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **HandJoints**: `🔗<enum_OpenXRInterface_HandJoints>`

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>` **HAND\_JOINT\_PALM** =
`0`

Palm joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>` **HAND\_JOINT\_WRIST** =
`1`

Wrist joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_THUMB\_METACARPAL** = `2`

Thumb metacarpal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_THUMB\_PROXIMAL** = `3`

Thumb proximal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_THUMB\_DISTAL** = `4`

Thumb distal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_THUMB\_TIP** = `5`

Thumb tip joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_INDEX\_METACARPAL** = `6`

Index metacarpal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_INDEX\_PROXIMAL** = `7`

Index proximal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_INDEX\_INTERMEDIATE** = `8`

Index intermediate joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_INDEX\_DISTAL** = `9`

Index distal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_INDEX\_TIP** = `10`

Index tip joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_MIDDLE\_METACARPAL** = `11`

Middle metacarpal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_MIDDLE\_PROXIMAL** = `12`

Middle proximal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_MIDDLE\_INTERMEDIATE** = `13`

Middle intermediate joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_MIDDLE\_DISTAL** = `14`

Middle distal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_MIDDLE\_TIP** = `15`

Middle tip joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_RING\_METACARPAL** = `16`

Ring metacarpal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_RING\_PROXIMAL** = `17`

Ring proximal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_RING\_INTERMEDIATE** = `18`

Ring intermediate joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_RING\_DISTAL** = `19`

Ring distal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>` **HAND\_JOINT\_RING\_TIP**
= `20`

Ring tip joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_LITTLE\_METACARPAL** = `21`

Little metacarpal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_LITTLE\_PROXIMAL** = `22`

Little proximal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_LITTLE\_INTERMEDIATE** = `23`

Little intermediate joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_LITTLE\_DISTAL** = `24`

Little distal joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>`
**HAND\_JOINT\_LITTLE\_TIP** = `25`

Little tip joint.

classref-enumeration-constant

`HandJoints<enum_OpenXRInterface_HandJoints>` **HAND\_JOINT\_MAX** =
`26`

Maximum value for the hand joint enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **HandJointFlags**: `🔗<enum_OpenXRInterface_HandJointFlags>`

classref-enumeration-constant

`HandJointFlags<enum_OpenXRInterface_HandJointFlags>`
**HAND\_JOINT\_NONE** = `0`

No flags are set.

classref-enumeration-constant

`HandJointFlags<enum_OpenXRInterface_HandJointFlags>`
**HAND\_JOINT\_ORIENTATION\_VALID** = `1`

If set, the orientation data is valid, otherwise, the orientation data
is unreliable and should not be used.

classref-enumeration-constant

`HandJointFlags<enum_OpenXRInterface_HandJointFlags>`
**HAND\_JOINT\_ORIENTATION\_TRACKED** = `2`

If set, the orientation data comes from tracking data, otherwise, the
orientation data contains predicted data.

classref-enumeration-constant

`HandJointFlags<enum_OpenXRInterface_HandJointFlags>`
**HAND\_JOINT\_POSITION\_VALID** = `4`

If set, the positional data is valid, otherwise, the positional data is
unreliable and should not be used.

classref-enumeration-constant

`HandJointFlags<enum_OpenXRInterface_HandJointFlags>`
**HAND\_JOINT\_POSITION\_TRACKED** = `8`

If set, the positional data comes from tracking data, otherwise, the
positional data contains predicted data.

classref-enumeration-constant

`HandJointFlags<enum_OpenXRInterface_HandJointFlags>`
**HAND\_JOINT\_LINEAR\_VELOCITY\_VALID** = `16`

If set, our linear velocity data is valid, otherwise, the linear
velocity data is unreliable and should not be used.

classref-enumeration-constant

`HandJointFlags<enum_OpenXRInterface_HandJointFlags>`
**HAND\_JOINT\_ANGULAR\_VELOCITY\_VALID** = `32`

If set, our angular velocity data is valid, otherwise, the angular
velocity data is unreliable and should not be used.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **display\_refresh\_rate** = `0.0`
`🔗<class_OpenXRInterface_property_display_refresh_rate>`

classref-property-setget

-   `void (No return value.)` **set\_display\_refresh\_rate**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_display\_refresh\_rate**()

The display refresh rate for the current HMD. Only functional if this
feature is supported by the OpenXR runtime and after the interface has
been initialized.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **foveation\_dynamic** = `false`
`🔗<class_OpenXRInterface_property_foveation_dynamic>`

classref-property-setget

-   `void (No return value.)` **set\_foveation\_dynamic**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_foveation\_dynamic**()

Enable dynamic foveation adjustment, the interface must be initialized
before this is accessible. If enabled foveation will automatically
adjusted between low and
`foveation_level<class_OpenXRInterface_property_foveation_level>`.

\*\*Note:\*\* Only works on compatibility renderer.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **foveation\_level** = `0`
`🔗<class_OpenXRInterface_property_foveation_level>`

classref-property-setget

-   `void (No return value.)` **set\_foveation\_level**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_foveation\_level**()

Set foveation level from 0 (off) to 3 (high), the interface must be
initialized before this is accessible.

\*\*Note:\*\* Only works on compatibility renderer.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **render\_target\_size\_multiplier** = `1.0`
`🔗<class_OpenXRInterface_property_render_target_size_multiplier>`

classref-property-setget

-   `void (No return value.)`
    **set\_render\_target\_size\_multiplier**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_render\_target\_size\_multiplier**()

The render size multiplier for the current HMD. Must be set before the
interface has been initialized.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **vrs\_min\_radius** = `20.0`
`🔗<class_OpenXRInterface_property_vrs_min_radius>`

classref-property-setget

-   `void (No return value.)` **set\_vrs\_min\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_vrs\_min\_radius**()

The minimum radius around the focal point where full quality is
guaranteed if VRS is used as a percentage of screen size.

\*\*Note:\*\* Mobile and Forward+ renderers only. Requires
`Viewport.vrs_mode<class_Viewport_property_vrs_mode>` to be set to
`Viewport.VRS_XR<class_Viewport_constant_VRS_XR>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **vrs\_strength** = `1.0`
`🔗<class_OpenXRInterface_property_vrs_strength>`

classref-property-setget

-   `void (No return value.)` **set\_vrs\_strength**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_vrs\_strength**()

The strength used to calculate the VRS density map. The greater this
value, the more noticeable VRS is. This improves performance at the cost
of quality.

\*\*Note:\*\* Mobile and Forward+ renderers only. Requires
`Viewport.vrs_mode<class_Viewport_property_vrs_mode>` to be set to
`Viewport.VRS_XR<class_Viewport_constant_VRS_XR>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Array<class_Array>` **get\_action\_sets**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_get_action_sets>`

Returns a list of action sets registered with Godot (loaded from the
action map at runtime).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_available\_display\_refresh\_rates**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_get_available_display_refresh_rates>`

Returns display refresh rates supported by the current HMD. Only
returned if this feature is supported by the OpenXR runtime and after
the interface has been initialized.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_hand\_joint\_angular\_velocity**(hand:
`Hand<enum_OpenXRInterface_Hand>`, joint:
`HandJoints<enum_OpenXRInterface_HandJoints>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_get_hand_joint_angular_velocity>`

**Deprecated:** Use
`XRHandTracker.get_hand_joint_angular_velocity<class_XRHandTracker_method_get_hand_joint_angular_velocity>`
obtained from `XRServer.get_tracker<class_XRServer_method_get_tracker>`
instead.

If handtracking is enabled, returns the angular velocity of a joint
(`joint`) of a hand (`hand`) as provided by OpenXR. This is relative to
`XROrigin3D<class_XROrigin3D>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`HandJointFlags<enum_OpenXRInterface_HandJointFlags>`\]
**get\_hand\_joint\_flags**(hand: `Hand<enum_OpenXRInterface_Hand>`,
joint: `HandJoints<enum_OpenXRInterface_HandJoints>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_get_hand_joint_flags>`

**Deprecated:** Use
`XRHandTracker.get_hand_joint_flags<class_XRHandTracker_method_get_hand_joint_flags>`
obtained from `XRServer.get_tracker<class_XRServer_method_get_tracker>`
instead.

If handtracking is enabled, returns flags that inform us of the validity
of the tracking data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_hand\_joint\_linear\_velocity**(hand:
`Hand<enum_OpenXRInterface_Hand>`, joint:
`HandJoints<enum_OpenXRInterface_HandJoints>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_get_hand_joint_linear_velocity>`

**Deprecated:** Use
`XRHandTracker.get_hand_joint_linear_velocity<class_XRHandTracker_method_get_hand_joint_linear_velocity>`
obtained from `XRServer.get_tracker<class_XRServer_method_get_tracker>`
instead.

If handtracking is enabled, returns the linear velocity of a joint
(`joint`) of a hand (`hand`) as provided by OpenXR. This is relative to
`XROrigin3D<class_XROrigin3D>` without worldscale applied!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_hand\_joint\_position**(hand:
`Hand<enum_OpenXRInterface_Hand>`, joint:
`HandJoints<enum_OpenXRInterface_HandJoints>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_get_hand_joint_position>`

**Deprecated:** Use
`XRHandTracker.get_hand_joint_transform<class_XRHandTracker_method_get_hand_joint_transform>`
obtained from `XRServer.get_tracker<class_XRServer_method_get_tracker>`
instead.

If handtracking is enabled, returns the position of a joint (`joint`) of
a hand (`hand`) as provided by OpenXR. This is relative to
`XROrigin3D<class_XROrigin3D>` without worldscale applied!

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_hand\_joint\_radius**(hand:
`Hand<enum_OpenXRInterface_Hand>`, joint:
`HandJoints<enum_OpenXRInterface_HandJoints>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_get_hand_joint_radius>`

**Deprecated:** Use
`XRHandTracker.get_hand_joint_radius<class_XRHandTracker_method_get_hand_joint_radius>`
obtained from `XRServer.get_tracker<class_XRServer_method_get_tracker>`
instead.

If handtracking is enabled, returns the radius of a joint (`joint`) of a
hand (`hand`) as provided by OpenXR. This is without worldscale applied!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Quaternion<class_Quaternion>` **get\_hand\_joint\_rotation**(hand:
`Hand<enum_OpenXRInterface_Hand>`, joint:
`HandJoints<enum_OpenXRInterface_HandJoints>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_get_hand_joint_rotation>`

**Deprecated:** Use
`XRHandTracker.get_hand_joint_transform<class_XRHandTracker_method_get_hand_joint_transform>`
obtained from `XRServer.get_tracker<class_XRServer_method_get_tracker>`
instead.

If handtracking is enabled, returns the rotation of a joint (`joint`) of
a hand (`hand`) as provided by OpenXR.

classref-item-separator

------------------------------------------------------------------------

classref-method

`HandTrackedSource<enum_OpenXRInterface_HandTrackedSource>`
**get\_hand\_tracking\_source**(hand: `Hand<enum_OpenXRInterface_Hand>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_get_hand_tracking_source>`

**Deprecated:** Use
`XRHandTracker.hand_tracking_source<class_XRHandTracker_property_hand_tracking_source>`
obtained from `XRServer.get_tracker<class_XRServer_method_get_tracker>`
instead.

If handtracking is enabled and hand tracking source is supported, gets
the source of the hand tracking data for `hand`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`HandMotionRange<enum_OpenXRInterface_HandMotionRange>`
**get\_motion\_range**(hand: `Hand<enum_OpenXRInterface_Hand>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_get_motion_range>`

If handtracking is enabled and motion range is supported, gets the
currently configured motion range for `hand`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_action\_set\_active**(name:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_is_action_set_active>`

Returns `true` if the given action set is active.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_eye\_gaze\_interaction\_supported**()
`🔗<class_OpenXRInterface_method_is_eye_gaze_interaction_supported>`

Returns the capabilities of the eye gaze interaction extension.

\*\*Note:\*\* This only returns a valid value after OpenXR has been
initialized.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_foveation\_supported**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_is_foveation_supported>`

Returns `true` if OpenXR's foveation extension is supported, the
interface must be initialized before this returns a valid value.

\*\*Note:\*\* This feature is only available on the compatibility
renderer and currently only available on some stand alone headsets. For
Vulkan set `Viewport.vrs_mode<class_Viewport_property_vrs_mode>` to
`VRS_XR` on desktop.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_hand\_interaction\_supported**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRInterface_method_is_hand_interaction_supported>`

Returns `true` if OpenXR's hand interaction profile is supported and
enabled.

\*\*Note:\*\* This only returns a valid value after OpenXR has been
initialized.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_hand\_tracking\_supported**()
`🔗<class_OpenXRInterface_method_is_hand_tracking_supported>`

Returns `true` if OpenXR's hand tracking is supported and enabled.

\*\*Note:\*\* This only returns a valid value after OpenXR has been
initialized.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_action\_set\_active**(name:
`String<class_String>`, active: `bool<class_bool>`)
`🔗<class_OpenXRInterface_method_set_action_set_active>`

Sets the given action set as active or inactive.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_motion\_range**(hand:
`Hand<enum_OpenXRInterface_Hand>`, motion\_range:
`HandMotionRange<enum_OpenXRInterface_HandMotionRange>`)
`🔗<class_OpenXRInterface_method_set_motion_range>`

If handtracking is enabled and motion range is supported, sets the
currently configured motion range for `hand` to `motion_range`.
