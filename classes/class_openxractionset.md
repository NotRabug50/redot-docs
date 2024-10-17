github\_url  
hide

# OpenXRActionSet

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Collection of `OpenXRAction<class_OpenXRAction>` resources that make up
an action set.

classref-introduction-group

## Description

Action sets in OpenXR define a collection of actions that can be
activated in unison. This allows games to easily change between
different states that require different inputs or need to reinterpret
inputs. For instance we could have an action set that is active when a
menu is open, an action set that is active when the player is freely
walking around and an action set that is active when the player is
controlling a vehicle.

Action sets can contain the same action with the same name, if such
action sets are active at the same time the action set with the highest
priority defines which binding is active.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Array<class_Array>` **actions** = `[]`
`🔗<class_OpenXRActionSet_property_actions>`

classref-property-setget

-   `void (No return value.)` **set\_actions**(value:
    `Array<class_Array>`)
-   `Array<class_Array>` **get\_actions**()

Collection of actions for this action set.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **localized\_name** = `""`
`🔗<class_OpenXRActionSet_property_localized_name>`

classref-property-setget

-   `void (No return value.)` **set\_localized\_name**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_localized\_name**()

The localized name of this action set.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **priority** = `0`
`🔗<class_OpenXRActionSet_property_priority>`

classref-property-setget

-   `void (No return value.)` **set\_priority**(value: `int<class_int>`)
-   `int<class_int>` **get\_priority**()

The priority for this action set.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_action**(action:
`OpenXRAction<class_OpenXRAction>`)
`🔗<class_OpenXRActionSet_method_add_action>`

Add an action to this action set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_action\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OpenXRActionSet_method_get_action_count>`

Retrieve the number of actions in our action set.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_action**(action:
`OpenXRAction<class_OpenXRAction>`)
`🔗<class_OpenXRActionSet_method_remove_action>`

Remove an action from this action set.
