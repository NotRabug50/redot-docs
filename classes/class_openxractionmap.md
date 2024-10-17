github\_url  
hide

# OpenXRActionMap

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Collection of `OpenXRActionSet<class_OpenXRActionSet>` and
`OpenXRInteractionProfile<class_OpenXRInteractionProfile>` resources for
the OpenXR module.

classref-introduction-group

## Description

OpenXR uses an action system similar to Godots Input map system to bind
inputs and outputs on various types of XR controllers to named actions.
OpenXR specifies more detail on these inputs and outputs than Godot
supports.

Another important distinction is that OpenXR offers no control over
these bindings. The bindings we register are suggestions, it is up to
the XR runtime to offer users the ability to change these bindings. This
allows the XR runtime to fill in the gaps if new hardware becomes
available.

The action map therefore needs to be loaded at startup and can't be
changed afterwards. This resource is a container for the entire action
map.

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

`Array<class_Array>` **action\_sets** = `[]`
`🔗<class_OpenXRActionMap_property_action_sets>`

classref-property-setget

-   `void (No return value.)` **set\_action\_sets**(value:
    `Array<class_Array>`)
-   `Array<class_Array>` **get\_action\_sets**()

Collection of `OpenXRActionSet<class_OpenXRActionSet>`s that are part of
this action map.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>` **interaction\_profiles** = `[]`
`🔗<class_OpenXRActionMap_property_interaction_profiles>`

classref-property-setget

-   `void (No return value.)` **set\_interaction\_profiles**(value:
    `Array<class_Array>`)
-   `Array<class_Array>` **get\_interaction\_profiles**()

Collection of
`OpenXRInteractionProfile<class_OpenXRInteractionProfile>`s that are
part of this action map.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_action\_set**(action\_set:
`OpenXRActionSet<class_OpenXRActionSet>`)
`🔗<class_OpenXRActionMap_method_add_action_set>`

Add an action set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**add\_interaction\_profile**(interaction\_profile:
`OpenXRInteractionProfile<class_OpenXRInteractionProfile>`)
`🔗<class_OpenXRActionMap_method_add_interaction_profile>`

Add an interaction profile.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **create\_default\_action\_sets**()
`🔗<class_OpenXRActionMap_method_create_default_action_sets>`

Setup this action set with our default actions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`OpenXRActionSet<class_OpenXRActionSet>` **find\_action\_set**(name:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRActionMap_method_find_action_set>`

Retrieve an action set by name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`OpenXRInteractionProfile<class_OpenXRInteractionProfile>`
**find\_interaction\_profile**(name: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRActionMap_method_find_interaction_profile>`

Find an interaction profile by its name (path).

classref-item-separator

------------------------------------------------------------------------

classref-method

`OpenXRActionSet<class_OpenXRActionSet>` **get\_action\_set**(idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRActionMap_method_get_action_set>`

Retrieve the action set at this index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_action\_set\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRActionMap_method_get_action_set_count>`

Retrieve the number of actions sets in our action map.

classref-item-separator

------------------------------------------------------------------------

classref-method

`OpenXRInteractionProfile<class_OpenXRInteractionProfile>`
**get\_interaction\_profile**(idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRActionMap_method_get_interaction_profile>`

Get the interaction profile at this index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_interaction\_profile\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRActionMap_method_get_interaction_profile_count>`

Retrieve the number of interaction profiles in our action map.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_action\_set**(action\_set:
`OpenXRActionSet<class_OpenXRActionSet>`)
`🔗<class_OpenXRActionMap_method_remove_action_set>`

Remove an action set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_interaction\_profile**(interaction\_profile:
`OpenXRInteractionProfile<class_OpenXRInteractionProfile>`)
`🔗<class_OpenXRActionMap_method_remove_interaction_profile>`

Remove an interaction profile.
