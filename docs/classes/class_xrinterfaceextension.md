github\_url  
hide

# XRInterfaceExtension

**Inherits:** `XRInterface<class_XRInterface>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Base class for XR interface extensions (plugins).

classref-introduction-group

## Description

External XR interface plugins should inherit from this class.

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

## Method Descriptions

classref-method

`void (No return value.)` **\_end\_frame**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__end_frame>`

Called if interface is active and queues have been submitted.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_get\_anchor\_detection\_is\_enabled**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__get_anchor_detection_is_enabled>`

Return `true` if anchor detection is enabled for this interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_camera\_feed\_id**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__get_camera_feed_id>`

Returns the camera feed ID for the `CameraFeed<class_CameraFeed>`
registered with the `CameraServer<class_CameraServer>` that should be
presented as the background on an AR capable device (if applicable).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **\_get\_camera\_transform**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__get_camera_transform>`

Returns the `Transform3D<class_Transform3D>` that positions the
`XRCamera3D<class_XRCamera3D>` in the world.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_capabilities**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__get_capabilities>`

Returns the capabilities of this interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_get\_color\_texture**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__get_color_texture>`

Return color texture into which to render (if applicable).

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_get\_depth\_texture**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__get_depth_texture>`

Return depth texture into which to render (if applicable).

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **\_get\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__get_name>`

Returns the name of this interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>` **\_get\_play\_area**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__get_play_area>`

Returns a `PackedVector3Array<class_PackedVector3Array>` that represents
the play areas boundaries (if applicable).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PlayAreaMode<enum_XRInterface_PlayAreaMode>`
**\_get\_play\_area\_mode**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__get_play_area_mode>`

Returns the play area mode that sets up our play area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedFloat64Array<class_PackedFloat64Array>`
**\_get\_projection\_for\_view**(view: `int<class_int>`, aspect:
`float<class_float>`, z\_near: `float<class_float>`, z\_far:
`float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__get_projection_for_view>`

Returns the projection matrix for the given view as a
`PackedFloat64Array<class_PackedFloat64Array>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **\_get\_render\_target\_size**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__get_render_target_size>`

Returns the size of our render target for this interface, this overrides
the size of the `Viewport<class_Viewport>` marked as the xr viewport.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_suggested\_pose\_names**(tracker\_name:
`StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__get_suggested_pose_names>`

Returns a `PackedStringArray<class_PackedStringArray>` with pose names
configured by this interface. Note that user configuration can override
this list.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_suggested\_tracker\_names**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__get_suggested_tracker_names>`

Returns a `PackedStringArray<class_PackedStringArray>` with tracker
names configured by this interface. Note that user configuration can
override this list.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **\_get\_system\_info**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__get_system_info>`

Returns a `Dictionary<class_Dictionary>` with system information related
to this interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TrackingStatus<enum_XRInterface_TrackingStatus>`
**\_get\_tracking\_status**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__get_tracking_status>`

Returns a `TrackingStatus<enum_XRInterface_TrackingStatus>` specifying
the current status of our tracking.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **\_get\_transform\_for\_view**(view:
`int<class_int>`, cam\_transform: `Transform3D<class_Transform3D>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__get_transform_for_view>`

Returns a `Transform3D<class_Transform3D>` for a given view.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_get\_velocity\_texture**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__get_velocity_texture>`

Return velocity texture into which to render (if applicable).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_view\_count**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__get_view_count>`

Returns the number of views this interface requires, 1 for mono, 2 for
stereoscopic.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **\_get\_vrs\_texture**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__get_vrs_texture>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_initialize**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__initialize>`

Initializes the interface, returns `true` on success.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_initialized**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__is_initialized>`

Returns `true` if this interface has been initialized.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_post\_draw\_viewport**(render\_target:
`RID<class_RID>`, screen\_rect: `Rect2<class_Rect2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__post_draw_viewport>`

Called after the XR `Viewport<class_Viewport>` draw logic has completed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_pre\_draw\_viewport**(render\_target:
`RID<class_RID>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__pre_draw_viewport>`

Called if this is our primary **XRInterfaceExtension** before we start
processing a `Viewport<class_Viewport>` for every active XR
`Viewport<class_Viewport>`, returns `true` if that viewport should be
rendered. An XR interface may return `false` if the user has taken off
their headset and we can pause rendering.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_pre\_render**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__pre_render>`

Called if this **XRInterfaceExtension** is active before rendering
starts. Most XR interfaces will sync tracking at this point in time.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_process**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__process>`

Called if this **XRInterfaceExtension** is active before our physics and
game process is called. Most XR interfaces will update its
`XRPositionalTracker<class_XRPositionalTracker>`s at this point in time.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_set\_anchor\_detection\_is\_enabled**(enabled: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__set_anchor_detection_is_enabled>`

Enables anchor detection on this interface if supported.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_set\_play\_area\_mode**(mode:
`PlayAreaMode<enum_XRInterface_PlayAreaMode>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__set_play_area_mode>`

Set the play area mode for this interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_supports\_play\_area\_mode**(mode:
`PlayAreaMode<enum_XRInterface_PlayAreaMode>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_XRInterfaceExtension_private_method__supports_play_area_mode>`

Returns `true` if this interface supports this play area mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_trigger\_haptic\_pulse**(action\_name:
`String<class_String>`, tracker\_name: `StringName<class_StringName>`,
frequency: `float<class_float>`, amplitude: `float<class_float>`,
duration\_sec: `float<class_float>`, delay\_sec: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__trigger_haptic_pulse>`

Triggers a haptic pulse to be emitted on the specified tracker.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_uninitialize**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_XRInterfaceExtension_private_method__uninitialize>`

Uninitialize the interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_blit**(render\_target:
`RID<class_RID>`, src\_rect: `Rect2<class_Rect2>`, dst\_rect:
`Rect2i<class_Rect2i>`, use\_layer: `bool<class_bool>`, layer:
`int<class_int>`, apply\_lens\_distortion: `bool<class_bool>`,
eye\_center: `Vector2<class_Vector2>`, k1: `float<class_float>`, k2:
`float<class_float>`, upscale: `float<class_float>`, aspect\_ratio:
`float<class_float>`) `🔗<class_XRInterfaceExtension_method_add_blit>`

Blits our render results to screen optionally applying lens distortion.
This can only be called while processing `_commit_views`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_color\_texture**()
`🔗<class_XRInterfaceExtension_method_get_color_texture>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_depth\_texture**()
`🔗<class_XRInterfaceExtension_method_get_depth_texture>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_render\_target\_texture**(render\_target:
`RID<class_RID>`)
`🔗<class_XRInterfaceExtension_method_get_render_target_texture>`

Returns a valid `RID<class_RID>` for a texture to which we should render
the current frame if supported by the interface.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RID<class_RID>` **get\_velocity\_texture**()
`🔗<class_XRInterfaceExtension_method_get_velocity_texture>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
