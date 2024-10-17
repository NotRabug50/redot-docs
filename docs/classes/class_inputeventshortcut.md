github\_url  
hide

# InputEventShortcut

**Inherits:** `InputEvent<class_InputEvent>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Represents a triggered keyboard `Shortcut<class_Shortcut>`.

classref-introduction-group

## Description

InputEventShortcut is a special event that can be received in
`Node._input<class_Node_private_method__input>`,
`Node._shortcut_input<class_Node_private_method__shortcut_input>`, and
`Node._unhandled_input<class_Node_private_method__unhandled_input>`. It
is typically sent by the editor's Command Palette to trigger actions,
but can also be sent manually using
`Viewport.push_input<class_Viewport_method_push_input>`.

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Shortcut<class_Shortcut>` **shortcut**
`🔗<class_InputEventShortcut_property_shortcut>`

classref-property-setget

-   `void (No return value.)` **set\_shortcut**(value:
    `Shortcut<class_Shortcut>`)
-   `Shortcut<class_Shortcut>` **get\_shortcut**()

The `Shortcut<class_Shortcut>` represented by this event. Its
`Shortcut.matches_event<class_Shortcut_method_matches_event>` method
will always return `true` for this event.
