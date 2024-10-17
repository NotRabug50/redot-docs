github\_url  
hide

# EditorResourcePicker

**Inherits:** `HBoxContainer<class_HBoxContainer>` **&lt;**
`BoxContainer<class_BoxContainer>` **&lt;** `Container<class_Container>`
**&lt;** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `EditorScriptPicker<class_EditorScriptPicker>`

Godot editor's control for selecting `Resource<class_Resource>` type
properties.

classref-introduction-group

## Description

This `Control<class_Control>` node is used in the editor's Inspector
dock to allow editing of `Resource<class_Resource>` type properties. It
provides options for creating, loading, saving and converting resources.
Can be used with `EditorInspectorPlugin<class_EditorInspectorPlugin>` to
recreate the same behavior.

\*\*Note:\*\* This `Control<class_Control>` does not include any editor
for the resource, as editing is controlled by the Inspector dock itself
or sub-Inspectors.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**resource\_changed**(resource: `Resource<class_Resource>`)
`🔗<class_EditorResourcePicker_signal_resource_changed>`

Emitted when the value of the edited resource was changed.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**resource\_selected**(resource: `Resource<class_Resource>`, inspect:
`bool<class_bool>`)
`🔗<class_EditorResourcePicker_signal_resource_selected>`

Emitted when the resource value was set and user clicked to edit it.
When `inspect` is `true`, the signal was caused by the context menu
"Edit" or "Inspect" option.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **base\_type** = `""`
`🔗<class_EditorResourcePicker_property_base_type>`

classref-property-setget

-   `void (No return value.)` **set\_base\_type**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_base\_type**()

The base type of allowed resource types. Can be a comma-separated list
of several options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editable** = `true`
`🔗<class_EditorResourcePicker_property_editable>`

classref-property-setget

-   `void (No return value.)` **set\_editable**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_editable**()

If `true`, the value can be selected and edited.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Resource<class_Resource>` **edited\_resource**
`🔗<class_EditorResourcePicker_property_edited_resource>`

classref-property-setget

-   `void (No return value.)` **set\_edited\_resource**(value:
    `Resource<class_Resource>`)
-   `Resource<class_Resource>` **get\_edited\_resource**()

The edited resource value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **toggle\_mode** = `false`
`🔗<class_EditorResourcePicker_property_toggle_mode>`

classref-property-setget

-   `void (No return value.)` **set\_toggle\_mode**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_toggle\_mode**()

If `true`, the main button with the resource preview works in the toggle
mode. Use
`set_toggle_pressed<class_EditorResourcePicker_method_set_toggle_pressed>`
to manually set the state.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **\_handle\_menu\_selected**(id: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorResourcePicker_private_method__handle_menu_selected>`

This virtual method can be implemented to handle context menu items not
handled by default. See
`_set_create_options<class_EditorResourcePicker_private_method__set_create_options>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_set\_create\_options**(menu\_node:
`Object<class_Object>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorResourcePicker_private_method__set_create_options>`

This virtual method is called when updating the context menu of
**EditorResourcePicker**. Implement this method to override the "New
..." items with your own options. `menu_node` is a reference to the
`PopupMenu<class_PopupMenu>` node.

\*\*Note:\*\* Implement
`_handle_menu_selected<class_EditorResourcePicker_private_method__handle_menu_selected>`
to handle these custom items.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_allowed\_types**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorResourcePicker_method_get_allowed_types>`

Returns a list of all allowed types and subtypes corresponding to the
`base_type<class_EditorResourcePicker_property_base_type>`. If the
`base_type<class_EditorResourcePicker_property_base_type>` is empty, an
empty list is returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_toggle\_pressed**(pressed:
`bool<class_bool>`)
`🔗<class_EditorResourcePicker_method_set_toggle_pressed>`

Sets the toggle mode state for the main button. Works only if
`toggle_mode<class_EditorResourcePicker_property_toggle_mode>` is set to
`true`.
