github\_url  
hide

# InputMap

**Inherits:** `Object<class_Object>`

A singleton that manages all
`InputEventAction<class_InputEventAction>`s.

classref-introduction-group

## Description

Manages all `InputEventAction<class_InputEventAction>` which can be
created/modified from the project settings menu **Project &gt; Project
Settings &gt; Input Map** or in code with
`add_action<class_InputMap_method_add_action>` and
`action_add_event<class_InputMap_method_action_add_event>`. See
`Node._input<class_Node_private_method__input>`.

classref-introduction-group

## Tutorials

-   [Using InputEvent:
    InputMap](../tutorials/inputs/inputevent.html#inputmap)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **action\_add\_event**(action:
`StringName<class_StringName>`, event: `InputEvent<class_InputEvent>`)
`🔗<class_InputMap_method_action_add_event>`

Adds an `InputEvent<class_InputEvent>` to an action. This
`InputEvent<class_InputEvent>` will trigger the action.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **action\_erase\_event**(action:
`StringName<class_StringName>`, event: `InputEvent<class_InputEvent>`)
`🔗<class_InputMap_method_action_erase_event>`

Removes an `InputEvent<class_InputEvent>` from an action.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **action\_erase\_events**(action:
`StringName<class_StringName>`)
`🔗<class_InputMap_method_action_erase_events>`

Removes all events from an action.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **action\_get\_deadzone**(action:
`StringName<class_StringName>`)
`🔗<class_InputMap_method_action_get_deadzone>`

Returns a deadzone value for the action.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`InputEvent<class_InputEvent>`\]
**action\_get\_events**(action: `StringName<class_StringName>`)
`🔗<class_InputMap_method_action_get_events>`

Returns an array of `InputEvent<class_InputEvent>`s associated with a
given action.

\*\*Note:\*\* When used in the editor (e.g. a tool script or
`EditorPlugin<class_EditorPlugin>`), this method will return events for
the editor action. If you want to access your project's input binds from
the editor, read the `input/*` settings from
`ProjectSettings<class_ProjectSettings>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **action\_has\_event**(action:
`StringName<class_StringName>`, event: `InputEvent<class_InputEvent>`)
`🔗<class_InputMap_method_action_has_event>`

Returns `true` if the action has the given
`InputEvent<class_InputEvent>` associated with it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **action\_set\_deadzone**(action:
`StringName<class_StringName>`, deadzone: `float<class_float>`)
`🔗<class_InputMap_method_action_set_deadzone>`

Sets a deadzone value for the action.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_action**(action:
`StringName<class_StringName>`, deadzone: `float<class_float>` = 0.2)
`🔗<class_InputMap_method_add_action>`

Adds an empty action to the **InputMap** with a configurable `deadzone`.

An `InputEvent<class_InputEvent>` can then be added to this action with
`action_add_event<class_InputMap_method_action_add_event>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase\_action**(action:
`StringName<class_StringName>`) `🔗<class_InputMap_method_erase_action>`

Removes an action from the **InputMap**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **event\_is\_action**(event:
`InputEvent<class_InputEvent>`, action: `StringName<class_StringName>`,
exact\_match: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InputMap_method_event_is_action>`

Returns `true` if the given event is part of an existing action. This
method ignores keyboard modifiers if the given
`InputEvent<class_InputEvent>` is not pressed (for proper release
detection). See
`action_has_event<class_InputMap_method_action_has_event>` if you don't
want this behavior.

If `exact_match` is `false`, it ignores additional input modifiers for
`InputEventKey<class_InputEventKey>` and
`InputEventMouseButton<class_InputEventMouseButton>` events, and the
direction for `InputEventJoypadMotion<class_InputEventJoypadMotion>`
events.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`StringName<class_StringName>`\]
**get\_actions**() `🔗<class_InputMap_method_get_actions>`

Returns an array of all actions in the **InputMap**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_action**(action:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_InputMap_method_has_action>`

Returns `true` if the **InputMap** has a registered action with the
given name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **load\_from\_project\_settings**()
`🔗<class_InputMap_method_load_from_project_settings>`

Clears all `InputEventAction<class_InputEventAction>` in the
**InputMap** and load it anew from
`ProjectSettings<class_ProjectSettings>`.
