github\_url  
hide

# Shortcut

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A shortcut for binding input.

classref-introduction-group

## Description

Shortcuts are commonly used for interacting with a
`Control<class_Control>` element from an `InputEvent<class_InputEvent>`
(also known as hotkeys).

One shortcut can contain multiple `InputEvent<class_InputEvent>`'s,
allowing the possibility of triggering one action with multiple
different inputs.

classref-reftable-group

## Properties

<table>
<tbody>
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

`Array<class_Array>` **events** = `[]`
`🔗<class_Shortcut_property_events>`

classref-property-setget

-   `void (No return value.)` **set\_events**(value:
    `Array<class_Array>`)
-   `Array<class_Array>` **get\_events**()

The shortcut's `InputEvent<class_InputEvent>` array.

Generally the `InputEvent<class_InputEvent>` used is an
`InputEventKey<class_InputEventKey>`, though it can be any
`InputEvent<class_InputEvent>`, including an
`InputEventAction<class_InputEventAction>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`String<class_String>` **get\_as\_text**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Shortcut_method_get_as_text>`

Returns the shortcut's first valid `InputEvent<class_InputEvent>` as a
`String<class_String>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_valid\_event**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Shortcut_method_has_valid_event>`

Returns whether `events<class_Shortcut_property_events>` contains an
`InputEvent<class_InputEvent>` which is valid.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **matches\_event**(event:
`InputEvent<class_InputEvent>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Shortcut_method_matches_event>`

Returns whether any `InputEvent<class_InputEvent>` in
`events<class_Shortcut_property_events>` equals `event`. This uses
`InputEvent.is_match<class_InputEvent_method_is_match>` to compare
events.
