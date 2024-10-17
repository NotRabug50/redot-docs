github\_url  
hide

# XRInterface

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

**Inherited By:** `MobileVRInterface<class_MobileVRInterface>`,
`OpenXRInterface<class_OpenXRInterface>`,
`WebXRInterface<class_WebXRInterface>`,
`XRInterfaceExtension<class_XRInterfaceExtension>`

Base class for an XR interface implementation.

classref-introduction-group

## Description

This class needs to be implemented to make an AR or VR platform
available to Godot and these should be implemented as C++ modules or
GDExtension modules. Part of the interface is exposed to GDScript so you
can detect, enable and configure an AR or VR platform.

Interfaces should be written in such a way that simply enabling them
will give us a working setup. You can query the available interfaces
through `XRServer<class_XRServer>`.

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

**play\_area\_changed**(mode: `int<class_int>`)
`🔗<class_XRInterface_signal_play_area_changed>`

Emitted when the play area is changed. This can be a result of the
player resetting the boundary or entering a new play area, the player
changing the play area mode, the world scale changing or the player
resetting their headset orientation.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Capabilities**: `🔗<enum_XRInterface_Capabilities>`

classref-enumeration-constant

`Capabilities<enum_XRInterface_Capabilities>` **XR\_NONE** = `0`

No XR capabilities.

classref-enumeration-constant

`Capabilities<enum_XRInterface_Capabilities>` **XR\_MONO** = `1`

This interface can work with normal rendering output (non-HMD based AR).

classref-enumeration-constant

`Capabilities<enum_XRInterface_Capabilities>` **XR\_STEREO** = `2`

This interface supports stereoscopic rendering.

classref-enumeration-constant

`Capabilities<enum_XRInterface_Capabilities>` **XR\_QUAD** = `4`

This interface supports quad rendering (not yet supported by Godot).

classref-enumeration-constant

`Capabilities<enum_XRInterface_Capabilities>` **XR\_VR** = `8`

This interface supports VR.

classref-enumeration-constant

`Capabilities<enum_XRInterface_Capabilities>` **XR\_AR** = `16`

This interface supports AR (video background and real world tracking).

classref-enumeration-constant

`Capabilities<enum_XRInterface_Capabilities>` **XR\_EXTERNAL** = `32`

This interface outputs to an external device. If the main viewport is
used, the on screen output is an unmodified buffer of either the left or
right eye (stretched if the viewport size is not changed to the same
aspect ratio of
`get_render_target_size<class_XRInterface_method_get_render_target_size>`).
Using a separate viewport node frees up the main viewport for other
purposes.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TrackingStatus**: `🔗<enum_XRInterface_TrackingStatus>`

classref-enumeration-constant

`TrackingStatus<enum_XRInterface_TrackingStatus>`
**XR\_NORMAL\_TRACKING** = `0`

Tracking is behaving as expected.

classref-enumeration-constant

`TrackingStatus<enum_XRInterface_TrackingStatus>`
**XR\_EXCESSIVE\_MOTION** = `1`

Tracking is hindered by excessive motion (the player is moving faster
than tracking can keep up).

classref-enumeration-constant

`TrackingStatus<enum_XRInterface_TrackingStatus>`
**XR\_INSUFFICIENT\_FEATURES** = `2`

Tracking is hindered by insufficient features, it's too dark (for
camera-based tracking), player is blocked, etc.

classref-enumeration-constant

`TrackingStatus<enum_XRInterface_TrackingStatus>`
**XR\_UNKNOWN\_TRACKING** = `3`

We don't know the status of the tracking or this interface does not
provide feedback.

classref-enumeration-constant

`TrackingStatus<enum_XRInterface_TrackingStatus>` **XR\_NOT\_TRACKING**
= `4`

Tracking is not functional (camera not plugged in or obscured,
lighthouses turned off, etc.).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **PlayAreaMode**: `🔗<enum_XRInterface_PlayAreaMode>`

classref-enumeration-constant

`PlayAreaMode<enum_XRInterface_PlayAreaMode>`
**XR\_PLAY\_AREA\_UNKNOWN** = `0`

Play area mode not set or not available.

classref-enumeration-constant

`PlayAreaMode<enum_XRInterface_PlayAreaMode>` **XR\_PLAY\_AREA\_3DOF** =
`1`

Play area only supports orientation tracking, no positional tracking,
area will center around player.

classref-enumeration-constant

`PlayAreaMode<enum_XRInterface_PlayAreaMode>`
**XR\_PLAY\_AREA\_SITTING** = `2`

Player is in seated position, limited positional tracking, fixed
guardian around player.

classref-enumeration-constant

`PlayAreaMode<enum_XRInterface_PlayAreaMode>`
**XR\_PLAY\_AREA\_ROOMSCALE** = `3`

Player is free to move around, full positional tracking.

classref-enumeration-constant

`PlayAreaMode<enum_XRInterface_PlayAreaMode>` **XR\_PLAY\_AREA\_STAGE**
= `4`

Same as
`XR_PLAY_AREA_ROOMSCALE<class_XRInterface_constant_XR_PLAY_AREA_ROOMSCALE>`
but origin point is fixed to the center of the physical space. In this
mode, system-level recentering may be disabled, requiring the use of
`XRServer.center_on_hmd<class_XRServer_method_center_on_hmd>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EnvironmentBlendMode**:
`🔗<enum_XRInterface_EnvironmentBlendMode>`

classref-enumeration-constant

`EnvironmentBlendMode<enum_XRInterface_EnvironmentBlendMode>`
**XR\_ENV\_BLEND\_MODE\_OPAQUE** = `0`

Opaque blend mode. This is typically used for VR devices.

classref-enumeration-constant

`EnvironmentBlendMode<enum_XRInterface_EnvironmentBlendMode>`
**XR\_ENV\_BLEND\_MODE\_ADDITIVE** = `1`

Additive blend mode. This is typically used for AR devices or VR devices
with passthrough.

classref-enumeration-constant

`EnvironmentBlendMode<enum_XRInterface_EnvironmentBlendMode>`
**XR\_ENV\_BLEND\_MODE\_ALPHA\_BLEND** = `2`

Alpha blend mode. This is typically used for AR or VR devices with
passthrough capabilities. The alpha channel controls how much of the
passthrough is visible. Alpha of 0.0 means the passthrough is visible
and this pixel works in ADDITIVE mode. Alpha of 1.0 means that the
passthrough is not visible and this pixel works in OPAQUE mode.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **ar\_is\_anchor\_detection\_enabled** = `false`
`🔗<class_XRInterface_property_ar_is_anchor_detection_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_anchor\_detection\_is\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_anchor\_detection\_is\_enabled**()

On an AR interface, `true` if anchor detection is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`EnvironmentBlendMode<enum_XRInterface_EnvironmentBlendMode>`
**environment\_blend\_mode** = `0`
`🔗<class_XRInterface_property_environment_blend_mode>`

classref-property-setget

-   `bool<class_bool>` **set\_environment\_blend\_mode**(mode:
    `EnvironmentBlendMode<enum_XRInterface_EnvironmentBlendMode>`)
-   `EnvironmentBlendMode<enum_XRInterface_EnvironmentBlendMode>`
    **get\_environment\_blend\_mode**()

Specify how XR should blend in the environment. This is specific to
certain AR and passthrough devices where camera images are blended in by
the XR compositor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interface\_is\_primary** = `false`
`🔗<class_XRInterface_property_interface_is_primary>`

classref-property-setget

-   `void (No return value.)` **set\_primary**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_primary**()

`true` if this is the primary interface.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PlayAreaMode<enum_XRInterface_PlayAreaMode>` **xr\_play\_area\_mode** =
`0` `🔗<class_XRInterface_property_xr_play_area_mode>`

classref-property-setget

-   `bool<class_bool>` **set\_play\_area\_mode**(mode:
    `PlayAreaMode<enum_XRInterface_PlayAreaMode>`)
-   `PlayAreaMode<enum_XRInterface_PlayAreaMode>`
    **get\_play\_area\_mode**()

The play area mode for this interface.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_camera\_feed\_id**()
`🔗<class_XRInterface_method_get_camera_feed_id>`

If this is an AR interface that requires displaying a camera feed as the
background, this method returns the feed ID in the
`CameraServer<class_CameraServer>` for this interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_capabilities**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterface_method_get_capabilities>`

Returns a combination of `Capabilities<enum_XRInterface_Capabilities>`
flags providing information about the capabilities of this interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterface_method_get_name>`

Returns the name of this interface (`"OpenXR"`, `"OpenVR"`, `"OpenHMD"`,
`"ARKit"`, etc.).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>` **get\_play\_area**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterface_method_get_play_area>`

Returns an array of vectors that represent the physical play area mapped
to the virtual space around the `XROrigin3D<class_XROrigin3D>` point.
The points form a convex polygon that can be used to react to or
visualize the play area. This returns an empty array if this feature is
not supported or if the information is not yet available.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Projection<class_Projection>` **get\_projection\_for\_view**(view:
`int<class_int>`, aspect: `float<class_float>`, near:
`float<class_float>`, far: `float<class_float>`)
`🔗<class_XRInterface_method_get_projection_for_view>`

Returns the projection matrix for a view/eye.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_render\_target\_size**()
`🔗<class_XRInterface_method_get_render_target_size>`

Returns the resolution at which we should render our intermediate
results before things like lens distortion are applied by the VR
platform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_supported\_environment\_blend\_modes**()
`🔗<class_XRInterface_method_get_supported_environment_blend_modes>`

Returns the an array of supported environment blend modes, see
`EnvironmentBlendMode<enum_XRInterface_EnvironmentBlendMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_system\_info**()
`🔗<class_XRInterface_method_get_system_info>`

Returns a `Dictionary<class_Dictionary>` with extra system info.
Interfaces are expected to return `XRRuntimeName` and `XRRuntimeVersion`
providing info about the used XR runtime. Additional entries may be
provided specific to an interface.

\*\*Note:\*\*This information may only be available after
`initialize<class_XRInterface_method_initialize>` was successfully
called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TrackingStatus<enum_XRInterface_TrackingStatus>`
**get\_tracking\_status**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterface_method_get_tracking_status>`

If supported, returns the status of our tracking. This will allow you to
provide feedback to the user whether there are issues with positional
tracking.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **get\_transform\_for\_view**(view:
`int<class_int>`, cam\_transform: `Transform3D<class_Transform3D>`)
`🔗<class_XRInterface_method_get_transform_for_view>`

Returns the transform for a view/eye.

`view` is the view/eye index.

`cam_transform` is the transform that maps device coordinates to scene
coordinates, typically the
`Node3D.global_transform<class_Node3D_property_global_transform>` of the
current XROrigin3D.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_view\_count**()
`🔗<class_XRInterface_method_get_view_count>`

Returns the number of views that need to be rendered for this device. 1
for Monoscopic, 2 for Stereoscopic.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **initialize**()
`🔗<class_XRInterface_method_initialize>`

Call this to initialize this interface. The first interface that is
initialized is identified as the primary interface and it will be used
for rendering output.

After initializing the interface you want to use you then need to enable
the AR/VR mode of a viewport and rendering should commence.

\*\*Note:\*\* You must enable the XR mode on the main viewport for any
device that uses the main output of Godot, such as for mobile VR.

If you do this for a platform that handles its own output (such as
OpenVR) Godot will show just one eye without distortion on screen.
Alternatively, you can add a separate viewport node to your scene and
enable AR/VR on that viewport. It will be used to output to the HMD,
leaving you free to do anything you like in the main window, such as
using a separate camera as a spectator camera or rendering something
completely different.

While currently not used, you can activate additional interfaces. You
may wish to do this if you want to track controllers from other
platforms. However, at this point in time only one interface can render
to an HMD.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_initialized**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterface_method_is_initialized>`

Returns `true` if this interface has been initialized.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_passthrough\_enabled**()
`🔗<class_XRInterface_method_is_passthrough_enabled>`

**Deprecated:** Check if
`environment_blend_mode<class_XRInterface_property_environment_blend_mode>`
is
`XR_ENV_BLEND_MODE_ALPHA_BLEND<class_XRInterface_constant_XR_ENV_BLEND_MODE_ALPHA_BLEND>`,
instead.

Returns `true` if passthrough is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_passthrough\_supported**()
`🔗<class_XRInterface_method_is_passthrough_supported>`

**Deprecated:** Check that
`XR_ENV_BLEND_MODE_ALPHA_BLEND<class_XRInterface_constant_XR_ENV_BLEND_MODE_ALPHA_BLEND>`
is supported using
`get_supported_environment_blend_modes<class_XRInterface_method_get_supported_environment_blend_modes>`,
instead.

Returns `true` if this interface supports passthrough.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **set\_environment\_blend\_mode**(mode:
`EnvironmentBlendMode<enum_XRInterface_EnvironmentBlendMode>`)
`🔗<class_XRInterface_method_set_environment_blend_mode>`

Sets the active environment blend mode.

`mode` is the environment blend mode starting with the next frame.

\*\*Note:\*\* Not all runtimes support all environment blend modes, so
it is important to check this at startup. For example:

    func _ready():
        var xr_interface: XRInterface = XRServer.find_interface("OpenXR")
        if xr_interface and xr_interface.is_initialized():
            var vp: Viewport = get_viewport()
            vp.use_xr = true
            var acceptable_modes = [XRInterface.XR_ENV_BLEND_MODE_OPAQUE, XRInterface.XR_ENV_BLEND_MODE_ADDITIVE]
            var modes = xr_interface.get_supported_environment_blend_modes()
            for mode in acceptable_modes:
                if mode in modes:
                    xr_interface.set_environment_blend_mode(mode)
                    break

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **set\_play\_area\_mode**(mode:
`PlayAreaMode<enum_XRInterface_PlayAreaMode>`)
`🔗<class_XRInterface_method_set_play_area_mode>`

Sets the active play area mode, will return `false` if the mode can't be
used with this interface.

\*\*Note:\*\* Changing this after the interface has already been
initialized can be jarring for the player, so it's recommended to
recenter on the HMD with
`XRServer.center_on_hmd<class_XRServer_method_center_on_hmd>` (if
switching to
`XR_PLAY_AREA_STAGE<class_XRInterface_constant_XR_PLAY_AREA_STAGE>`) or
make the switch during a scene change.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **start\_passthrough**()
`🔗<class_XRInterface_method_start_passthrough>`

**Deprecated:** Set the
`environment_blend_mode<class_XRInterface_property_environment_blend_mode>`
to
`XR_ENV_BLEND_MODE_ALPHA_BLEND<class_XRInterface_constant_XR_ENV_BLEND_MODE_ALPHA_BLEND>`,
instead.

Starts passthrough, will return `false` if passthrough couldn't be
started.

\*\*Note:\*\* The viewport used for XR must have a transparent
background, otherwise passthrough may not properly render.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop\_passthrough**()
`🔗<class_XRInterface_method_stop_passthrough>`

**Deprecated:** Set the
`environment_blend_mode<class_XRInterface_property_environment_blend_mode>`
to
`XR_ENV_BLEND_MODE_OPAQUE<class_XRInterface_constant_XR_ENV_BLEND_MODE_OPAQUE>`,
instead.

Stops passthrough.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **supports\_play\_area\_mode**(mode:
`PlayAreaMode<enum_XRInterface_PlayAreaMode>`)
`🔗<class_XRInterface_method_supports_play_area_mode>`

Call this to find out if a given play area mode is supported by this
interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **trigger\_haptic\_pulse**(action\_name:
`String<class_String>`, tracker\_name: `StringName<class_StringName>`,
frequency: `float<class_float>`, amplitude: `float<class_float>`,
duration\_sec: `float<class_float>`, delay\_sec: `float<class_float>`)
`🔗<class_XRInterface_method_trigger_haptic_pulse>`

Triggers a haptic pulse on a device associated with this interface.

`action_name` is the name of the action for this pulse.

`tracker_name` is optional and can be used to direct the pulse to a
specific device provided that device is bound to this haptic.

`frequency` is the frequency of the pulse, set to `0.0` to have the
system use a default frequency.

`amplitude` is the amplitude of the pulse between `0.0` and `1.0`.

`duration_sec` is the duration of the pulse in seconds.

`delay_sec` is a delay in seconds before the pulse is given.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **uninitialize**()
`🔗<class_XRInterface_method_uninitialize>`

Turns the interface off.
