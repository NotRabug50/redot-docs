github\_url  
hide

# OpenXRExtensionWrapperExtension

**Inherits:** `Object<class_Object>`

Allows clients to implement OpenXR extensions with GDExtension.

classref-introduction-group

## Description

**OpenXRExtensionWrapperExtension** allows clients to implement OpenXR
extensions with GDExtension. The extension should be registered with
`register_extension_wrapper<class_OpenXRExtensionWrapperExtension_method_register_extension_wrapper>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **\_get\_composition\_layer**(index: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__get_composition_layer>`

Returns a pointer to an `XrCompositionLayerBaseHeader` struct to provide
the given composition layer.

This will only be called if the extension previously registered itself
with
`OpenXRAPIExtension.register_composition_layer_provider<class_OpenXRAPIExtension_method_register_composition_layer_provider>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_composition\_layer\_count**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__get_composition_layer_count>`

Returns the number of composition layers this extension wrapper provides
via
`_get_composition_layer<class_OpenXRExtensionWrapperExtension_private_method__get_composition_layer>`.

This will only be called if the extension previously registered itself
with
`OpenXRAPIExtension.register_composition_layer_provider<class_OpenXRAPIExtension_method_register_composition_layer_provider>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_composition\_layer\_order**(index:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__get_composition_layer_order>`

Returns an integer that will be used to sort the given composition layer
provided via
`_get_composition_layer<class_OpenXRExtensionWrapperExtension_private_method__get_composition_layer>`.
Lower numbers will move the layer to the front of the list, and higher
numbers to the end. The default projection layer has an order of `0`, so
layers provided by this method should probably be above or below (but
not exactly) `0`.

This will only be called if the extension previously registered itself
with
`OpenXRAPIExtension.register_composition_layer_provider<class_OpenXRAPIExtension_method_register_composition_layer_provider>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **\_get\_requested\_extensions**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__get_requested_extensions>`

Returns a `Dictionary<class_Dictionary>` of OpenXR extensions related to
this extension. The `Dictionary<class_Dictionary>` should contain the
name of the extension, mapped to a `bool *` cast to an integer:

-   If the `bool *` is a `nullptr` this extension is mandatory.
-   If the `bool *` points to a boolean, the boolean will be updated to
    `true` if the extension is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_suggested\_tracker\_names**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__get_suggested_tracker_names>`

Returns a `PackedStringArray<class_PackedStringArray>` of positional
tracker names that are used within the extension wrapper.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_viewport\_composition\_layer\_extension\_properties**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__get_viewport_composition_layer_extension_properties>`

Gets an array of `Dictionary<class_Dictionary>`s that represent
properties, just like
`Object._get_property_list<class_Object_private_method__get_property_list>`,
that will be added to
`OpenXRCompositionLayer<class_OpenXRCompositionLayer>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**\_get\_viewport\_composition\_layer\_extension\_property\_defaults**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__get_viewport_composition_layer_extension_property_defaults>`

Gets a `Dictionary<class_Dictionary>` containing the default values for
the properties returned by
`_get_viewport_composition_layer_extension_properties<class_OpenXRExtensionWrapperExtension_private_method__get_viewport_composition_layer_extension_properties>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_before\_instance\_created**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_before_instance_created>`

Called before the OpenXR instance is created.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_on\_event\_polled**(event: `const void*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_event_polled>`

Called when there is an OpenXR event to process. When implementing,
return `true` if the event was handled, return `false` otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_instance\_created**(instance:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_instance_created>`

Called right after the OpenXR instance is created.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_instance\_destroyed**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_instance_destroyed>`

Called right before the OpenXR instance is destroyed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_main\_swapchains\_created**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_main_swapchains_created>`

Called right after the main swapchains are (re)created.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_pre\_render**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_pre_render>`

Called right before the XR viewports begin their rendering step.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_process**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_process>`

Called as part of the OpenXR process handling. This happens right before
general and physics processing steps of the main loop. During this step
controller data is queried and made available to game logic.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_register\_metadata**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_register_metadata>`

Allows extensions to register additional controller metadata. This
function is called even when the OpenXR API is not constructed as the
metadata needs to be available to the editor.

Extensions should also provide metadata regardless of whether they are
supported on the host system. The controller data is used to setup
action maps for users who may have access to the relevant hardware.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_session\_created**(session:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_session_created>`

Called right after the OpenXR session is created.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_session\_destroyed**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_session_destroyed>`

Called right before the OpenXR session is destroyed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_state\_exiting**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_state_exiting>`

Called when the OpenXR session state is changed to exiting.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_state\_focused**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_state_focused>`

Called when the OpenXR session state is changed to focused. This state
is the active state when the game runs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_state\_idle**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_state_idle>`

Called when the OpenXR session state is changed to idle.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_state\_loss\_pending**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_state_loss_pending>`

Called when the OpenXR session state is changed to loss pending.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_state\_ready**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_state_ready>`

Called when the OpenXR session state is changed to ready. This means
OpenXR is ready to set up the session.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_state\_stopping**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_state_stopping>`

Called when the OpenXR session state is changed to stopping.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_state\_synchronized**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_state_synchronized>`

Called when the OpenXR session state is changed to synchronized. OpenXR
also returns to this state when the application loses focus.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_on\_state\_visible**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_state_visible>`

Called when the OpenXR session state is changed to visible. This means
OpenXR is now ready to receive frames.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**\_on\_viewport\_composition\_layer\_destroyed**(layer: `const void*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__on_viewport_composition_layer_destroyed>`

Called when a composition layer created via
`OpenXRCompositionLayer<class_OpenXRCompositionLayer>` is destroyed.

`layer` is a pointer to an `XrCompositionLayerBaseHeader` struct.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**\_set\_android\_surface\_swapchain\_create\_info\_and\_get\_next\_pointer**(property\_values:
`Dictionary<class_Dictionary>`, next\_pointer: `void*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__set_android_surface_swapchain_create_info_and_get_next_pointer>`

Adds additional data structures to Android surface swapchains created by
`OpenXRCompositionLayer<class_OpenXRCompositionLayer>`.

`property_values` contains the values of the properties returned by
`_get_viewport_composition_layer_extension_properties<class_OpenXRExtensionWrapperExtension_private_method__get_viewport_composition_layer_extension_properties>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**\_set\_hand\_joint\_locations\_and\_get\_next\_pointer**(hand\_index:
`int<class_int>`, next\_pointer: `void*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__set_hand_joint_locations_and_get_next_pointer>`

Adds additional data structures when each hand tracker is created.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**\_set\_instance\_create\_info\_and\_get\_next\_pointer**(next\_pointer:
`void*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__set_instance_create_info_and_get_next_pointer>`

Adds additional data structures when the OpenXR instance is created.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**\_set\_session\_create\_and\_get\_next\_pointer**(next\_pointer:
`void*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__set_session_create_and_get_next_pointer>`

Adds additional data structures when the OpenXR session is created.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**\_set\_swapchain\_create\_info\_and\_get\_next\_pointer**(next\_pointer:
`void*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__set_swapchain_create_info_and_get_next_pointer>`

Adds additional data structures when creating OpenXR swapchains.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**\_set\_system\_properties\_and\_get\_next\_pointer**(next\_pointer:
`void*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__set_system_properties_and_get_next_pointer>`

Adds additional data structures when interogating OpenXR system
abilities.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>`
**\_set\_viewport\_composition\_layer\_and\_get\_next\_pointer**(layer:
`const void*`, property\_values: `Dictionary<class_Dictionary>`,
next\_pointer: `void*`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_OpenXRExtensionWrapperExtension_private_method__set_viewport_composition_layer_and_get_next_pointer>`

Adds additional data structures to composition layers created by
`OpenXRCompositionLayer<class_OpenXRCompositionLayer>`.

`property_values` contains the values of the properties returned by
`_get_viewport_composition_layer_extension_properties<class_OpenXRExtensionWrapperExtension_private_method__get_viewport_composition_layer_extension_properties>`.

`layer` is a pointer to an `XrCompositionLayerBaseHeader` struct.

classref-item-separator

------------------------------------------------------------------------

classref-method

`OpenXRAPIExtension<class_OpenXRAPIExtension>` **get\_openxr\_api**()
`🔗<class_OpenXRExtensionWrapperExtension_method_get_openxr_api>`

Returns the created `OpenXRAPIExtension<class_OpenXRAPIExtension>`,
which can be used to access the OpenXR API.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **register\_extension\_wrapper**()
`🔗<class_OpenXRExtensionWrapperExtension_method_register_extension_wrapper>`

Registers the extension. This should happen at core module
initialization level.
