github\_url  
hide

# OpenXRAPIExtension

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Makes the OpenXR API available for GDExtension.

classref-introduction-group

## Description

**OpenXRAPIExtension** makes OpenXR available for GDExtension. It
provides the OpenXR API to GDExtension through the
`get_instance_proc_addr<class_OpenXRAPIExtension_method_get_instance_proc_addr>`
method, and the OpenXR instance through
`get_instance<class_OpenXRAPIExtension_method_get_instance>`.

It also provides methods for querying the status of OpenXR
initialization, and helper methods for ease of use of the API with
GDExtension.

classref-introduction-group

## Tutorials

-   [XrResult
    documentation](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrResult.html)
-   [XrInstance
    documentation](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrInstance.html)
-   [XrSpace
    documentation](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrSpace.html)
-   [XrSession
    documentation](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrSession.html)
-   [XrSystemId
    documentation](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrSystemId.html)
-   [xrBeginSession
    documentation](https://registry.khronos.org/OpenXR/specs/1.0/man/html/xrBeginSession.html)
-   [XrPosef
    documentation](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrPosef.html)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **OpenXRAlphaBlendModeSupport**:
`🔗<enum_OpenXRAPIExtension_OpenXRAlphaBlendModeSupport>`

classref-enumeration-constant

`OpenXRAlphaBlendModeSupport<enum_OpenXRAPIExtension_OpenXRAlphaBlendModeSupport>`
**OPENXR\_ALPHA\_BLEND\_MODE\_SUPPORT\_NONE** = `0`

Means that
`XRInterface.XR_ENV_BLEND_MODE_ALPHA_BLEND<class_XRInterface_constant_XR_ENV_BLEND_MODE_ALPHA_BLEND>`
isn't supported at all.

classref-enumeration-constant

`OpenXRAlphaBlendModeSupport<enum_OpenXRAPIExtension_OpenXRAlphaBlendModeSupport>`
**OPENXR\_ALPHA\_BLEND\_MODE\_SUPPORT\_REAL** = `1`

Means that
`XRInterface.XR_ENV_BLEND_MODE_ALPHA_BLEND<class_XRInterface_constant_XR_ENV_BLEND_MODE_ALPHA_BLEND>`
is really supported.

classref-enumeration-constant

`OpenXRAlphaBlendModeSupport<enum_OpenXRAPIExtension_OpenXRAlphaBlendModeSupport>`
**OPENXR\_ALPHA\_BLEND\_MODE\_SUPPORT\_EMULATING** = `2`

Means that
`XRInterface.XR_ENV_BLEND_MODE_ALPHA_BLEND<class_XRInterface_constant_XR_ENV_BLEND_MODE_ALPHA_BLEND>`
is emulated.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **begin\_debug\_label\_region**(label\_name:
`String<class_String>`)
`🔗<class_OpenXRAPIExtension_method_begin_debug_label_region>`

Begins a new debug label region, this label will be reported in debug
messages for any calls following this until
`end_debug_label_region<class_OpenXRAPIExtension_method_end_debug_label_region>`
is called. Debug labels can be stacked.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **can\_render**()
`🔗<class_OpenXRAPIExtension_method_can_render>`

Returns `true` if OpenXR is initialized for rendering with an XR
viewport.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **end\_debug\_label\_region**()
`🔗<class_OpenXRAPIExtension_method_end_debug_label_region>`

Marks the end of a debug label region. Removes the latest debug label
region added by calling
`begin_debug_label_region<class_OpenXRAPIExtension_method_begin_debug_label_region>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_error\_string**(result: `int<class_int>`)
`🔗<class_OpenXRAPIExtension_method_get_error_string>`

Returns an error string for the given
[XrResult](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrResult.html).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_hand\_tracker**(hand\_index: `int<class_int>`)
`🔗<class_OpenXRAPIExtension_method_get_hand_tracker>`

Returns the corresponding `XRHandTrackerEXT` handle for the given hand
index value.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_instance**()
`🔗<class_OpenXRAPIExtension_method_get_instance>`

Returns the
[XrInstance](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrInstance.html)
created during the initialization of the OpenXR API.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_instance\_proc\_addr**(name:
`String<class_String>`)
`🔗<class_OpenXRAPIExtension_method_get_instance_proc_addr>`

Returns the function pointer of the OpenXR function with the specified
name, cast to an integer. If the function with the given name does not
exist, the method returns `0`.

\*\*Note:\*\* `openxr/util.h` contains utility macros for acquiring
OpenXR functions, e.g. `GDEXTENSION_INIT_XR_FUNC_V(xrCreateAction)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_next\_frame\_time**()
`🔗<class_OpenXRAPIExtension_method_get_next_frame_time>`

Returns the predicted display timing for the next frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_play\_space**()
`🔗<class_OpenXRAPIExtension_method_get_play_space>`

Returns the play space, which is an
[XrSpace](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrSpace.html)
cast to an integer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_predicted\_display\_time**()
`🔗<class_OpenXRAPIExtension_method_get_predicted_display_time>`

Returns the predicted display timing for the current frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_session**()
`🔗<class_OpenXRAPIExtension_method_get_session>`

Returns the OpenXR session, which is an
[XrSession](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrSession.html)
cast to an integer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>`
**get\_swapchain\_format\_name**(swapchain\_format: `int<class_int>`)
`🔗<class_OpenXRAPIExtension_method_get_swapchain_format_name>`

Returns the name of the specified swapchain format.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_system\_id**()
`🔗<class_OpenXRAPIExtension_method_get_system_id>`

Returns the id of the system, which is a
[XrSystemId](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrSystemId.html)
cast to an integer.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **insert\_debug\_label**(label\_name:
`String<class_String>`)
`🔗<class_OpenXRAPIExtension_method_insert_debug_label>`

Inserts a debug label, this label is reported in any debug message
resulting from the OpenXR calls that follows, until any of
`begin_debug_label_region<class_OpenXRAPIExtension_method_begin_debug_label_region>`,
`end_debug_label_region<class_OpenXRAPIExtension_method_end_debug_label_region>`,
or
`insert_debug_label<class_OpenXRAPIExtension_method_insert_debug_label>`
is called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`OpenXRAlphaBlendModeSupport<enum_OpenXRAPIExtension_OpenXRAlphaBlendModeSupport>`
**is\_environment\_blend\_mode\_alpha\_supported**()
`🔗<class_OpenXRAPIExtension_method_is_environment_blend_mode_alpha_supported>`

Returns
`OpenXRAlphaBlendModeSupport<enum_OpenXRAPIExtension_OpenXRAlphaBlendModeSupport>`
denoting if
`XRInterface.XR_ENV_BLEND_MODE_ALPHA_BLEND<class_XRInterface_constant_XR_ENV_BLEND_MODE_ALPHA_BLEND>`
is really supported, emulated or not supported at all.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_initialized**()
`🔗<class_OpenXRAPIExtension_method_is_initialized>`

Returns `true` if OpenXR is initialized.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_running**()
`🔗<class_OpenXRAPIExtension_method_is_running>`

Returns `true` if OpenXR is running
([xrBeginSession](https://registry.khronos.org/OpenXR/specs/1.0/man/html/xrBeginSession.html)
was successfully called and the swapchains were created).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **openxr\_is\_enabled**(check\_run\_in\_editor:
`bool<class_bool>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_OpenXRAPIExtension_method_openxr_is_enabled>`

Returns `true` if OpenXR is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**register\_composition\_layer\_provider**(extension:
`OpenXRExtensionWrapperExtension<class_OpenXRExtensionWrapperExtension>`)
`🔗<class_OpenXRAPIExtension_method_register_composition_layer_provider>`

Registers the given extension as a composition layer provider.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_emulate\_environment\_blend\_mode\_alpha\_blend**(enabled:
`bool<class_bool>`)
`🔗<class_OpenXRAPIExtension_method_set_emulate_environment_blend_mode_alpha_blend>`

If set to `true`, an OpenXR extension is loaded which is capable of
emulating the
`XRInterface.XR_ENV_BLEND_MODE_ALPHA_BLEND<class_XRInterface_constant_XR_ENV_BLEND_MODE_ALPHA_BLEND>`
blend mode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_object\_name**(object\_type:
`int<class_int>`, object\_handle: `int<class_int>`, object\_name:
`String<class_String>`)
`🔗<class_OpenXRAPIExtension_method_set_object_name>`

Set the object name of an OpenXR object, used for debug output.
`object_type` must be a valid OpenXR `XrObjectType` enum and
`object_handle` must be a valid OpenXR object handle.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **transform\_from\_pose**(pose:
`const void*`) `🔗<class_OpenXRAPIExtension_method_transform_from_pose>`

Creates a `Transform3D<class_Transform3D>` from an
[XrPosef](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrPosef.html).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**unregister\_composition\_layer\_provider**(extension:
`OpenXRExtensionWrapperExtension<class_OpenXRExtensionWrapperExtension>`)
`🔗<class_OpenXRAPIExtension_method_unregister_composition_layer_provider>`

Unregisters the given extension as a composition layer provider.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **xr\_result**(result: `int<class_int>`, format:
`String<class_String>`, args: `Array<class_Array>`)
`🔗<class_OpenXRAPIExtension_method_xr_result>`

Returns `true` if the provided
[XrResult](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrResult.html)
(cast to an integer) is successful. Otherwise returns `false` and prints
the
[XrResult](https://registry.khronos.org/OpenXR/specs/1.0/man/html/XrResult.html)
converted to a string, with the specified additional information.
