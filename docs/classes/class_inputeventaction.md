github\_url  
hide

# InputEventAction

**Inherits:** `InputEvent<class_InputEvent>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

An input event type for actions.

classref-introduction-group

## Description

Contains a generic action which can be targeted from several types of
inputs. Actions and their events can be set in the **Input Map** tab in
**Project &gt; Project Settings**, or with the
`InputMap<class_InputMap>` class.

\*\*Note:\*\* Unlike the other `InputEvent<class_InputEvent>` subclasses
which map to unique physical events, this virtual one is not emitted by
the engine. This class is useful to emit actions manually with
`Input.parse_input_event<class_Input_method_parse_input_event>`, which
are then received in `Node._input<class_Node_private_method__input>`. To
check if a physical event matches an action from the Input Map, use
`InputEvent.is_action<class_InputEvent_method_is_action>` and
`InputEvent.is_action_pressed<class_InputEvent_method_is_action_pressed>`.

classref-introduction-group

## Tutorials

-   [Using InputEvent:
    Actions](../tutorials/inputs/inputevent.html#actions)
-   [2D Dodge The Creeps
    Demo](https://godotengine.org/asset-library/asset/2712)
-   [3D Voxel Demo](https://godotengine.org/asset-library/asset/2755)

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`StringName<class_StringName>` **action** = `&""`
`🔗<class_InputEventAction_property_action>`

classref-property-setget

-   `void (No return value.)` **set\_action**(value:
    `StringName<class_StringName>`)
-   `StringName<class_StringName>` **get\_action**()

The action's name. Actions are accessed via this `String<class_String>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **event\_index** = `-1`
`🔗<class_InputEventAction_property_event_index>`

classref-property-setget

-   `void (No return value.)` **set\_event\_index**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_event\_index**()

The real event index in action this event corresponds to (from events
defined for this action in the `InputMap<class_InputMap>`). If `-1`, a
unique ID will be used and actions pressed with this ID will need to be
released with another **InputEventAction**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **pressed** = `false`
`🔗<class_InputEventAction_property_pressed>`

classref-property-setget

-   `void (No return value.)` **set\_pressed**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_pressed**()

If `true`, the action's state is pressed. If `false`, the action's state
is released.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **strength** = `1.0`
`🔗<class_InputEventAction_property_strength>`

classref-property-setget

-   `void (No return value.)` **set\_strength**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_strength**()

The action's strength between 0 and 1. This value is considered as equal
to 0 if pressed is `false`. The event strength allows faking analog
joypad motion events, by specifying how strongly the joypad axis is bent
or pressed.
