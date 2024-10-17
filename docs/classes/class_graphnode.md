github\_url  
hide

# GraphNode

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `GraphElement<class_GraphElement>` **&lt;**
`Container<class_Container>` **&lt;** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A container with connection ports, representing a node in a
`GraphEdit<class_GraphEdit>`.

classref-introduction-group

## Description

**GraphNode** allows to create nodes for a `GraphEdit<class_GraphEdit>`
graph with customizable content based on its child controls.
**GraphNode** is derived from `Container<class_Container>` and it is
responsible for placing its children on screen. This works similar to
`VBoxContainer<class_VBoxContainer>`. Children, in turn, provide
**GraphNode** with so-called slots, each of which can have a connection
port on either side.

Each **GraphNode** slot is defined by its index and can provide the node
with up to two ports: one on the left, and one on the right. By
convention the left port is also referred to as the **input port** and
the right port is referred to as the **output port**. Each port can be
enabled and configured individually, using different type and color. The
type is an arbitrary value that you can define using your own
considerations. The parent `GraphEdit<class_GraphEdit>` will receive
this information on each connect and disconnect request.

Slots can be configured in the Inspector dock once you add at least one
child `Control<class_Control>`. The properties are grouped by each
slot's index in the "Slot" section.

\*\*Note:\*\* While GraphNode is set up using slots and slot indices,
connections are made between the ports which are enabled. Because of
that `GraphEdit<class_GraphEdit>` uses the port's index and not the
slot's index. You can use
`get_input_port_slot<class_GraphNode_method_get_input_port_slot>` and
`get_output_port_slot<class_GraphNode_method_get_output_port_slot>` to
get the slot index from the port index.

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

classref-reftable-group

## Theme Properties

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**slot\_updated**(slot\_index: `int<class_int>`)
`🔗<class_GraphNode_signal_slot_updated>`

Emitted when any GraphNode's slot is updated.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **ignore\_invalid\_connection\_type** = `false`
`🔗<class_GraphNode_property_ignore_invalid_connection_type>`

classref-property-setget

-   `void (No return value.)`
    **set\_ignore\_invalid\_connection\_type**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_ignoring\_valid\_connection\_type**()

If `true`, you can connect ports with different types, even if the
connection was not explicitly allowed in the parent
`GraphEdit<class_GraphEdit>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **title** = `""`
`🔗<class_GraphNode_property_title>`

classref-property-setget

-   `void (No return value.)` **set\_title**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_title**()

The text displayed in the GraphNode's title bar.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_draw\_port**(slot\_index:
`int<class_int>`, position: `Vector2i<class_Vector2i>`, left:
`bool<class_bool>`, color: `Color<class_Color>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GraphNode_private_method__draw_port>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_all\_slots**()
`🔗<class_GraphNode_method_clear_all_slots>`

Disables all slots of the GraphNode. This will remove all input/output
ports from the GraphNode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_slot**(slot\_index: `int<class_int>`)
`🔗<class_GraphNode_method_clear_slot>`

Disables the slot with the given `slot_index`. This will remove the
corresponding input and output port from the GraphNode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_input\_port\_color**(port\_idx:
`int<class_int>`) `🔗<class_GraphNode_method_get_input_port_color>`

Returns the `Color<class_Color>` of the input port with the given
`port_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_input\_port\_count**()
`🔗<class_GraphNode_method_get_input_port_count>`

Returns the number of slots with an enabled input port.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_input\_port\_position**(port\_idx:
`int<class_int>`) `🔗<class_GraphNode_method_get_input_port_position>`

Returns the position of the input port with the given `port_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_input\_port\_slot**(port\_idx: `int<class_int>`)
`🔗<class_GraphNode_method_get_input_port_slot>`

Returns the corresponding slot index of the input port with the given
`port_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_input\_port\_type**(port\_idx: `int<class_int>`)
`🔗<class_GraphNode_method_get_input_port_type>`

Returns the type of the input port with the given `port_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_output\_port\_color**(port\_idx:
`int<class_int>`) `🔗<class_GraphNode_method_get_output_port_color>`

Returns the `Color<class_Color>` of the output port with the given
`port_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_output\_port\_count**()
`🔗<class_GraphNode_method_get_output_port_count>`

Returns the number of slots with an enabled output port.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_output\_port\_position**(port\_idx:
`int<class_int>`) `🔗<class_GraphNode_method_get_output_port_position>`

Returns the position of the output port with the given `port_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_output\_port\_slot**(port\_idx:
`int<class_int>`) `🔗<class_GraphNode_method_get_output_port_slot>`

Returns the corresponding slot index of the output port with the given
`port_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_output\_port\_type**(port\_idx:
`int<class_int>`) `🔗<class_GraphNode_method_get_output_port_type>`

Returns the type of the output port with the given `port_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_slot\_color\_left**(slot\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphNode_method_get_slot_color_left>`

Returns the left (input) `Color<class_Color>` of the slot with the given
`slot_index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_slot\_color\_right**(slot\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphNode_method_get_slot_color_right>`

Returns the right (output) `Color<class_Color>` of the slot with the
given `slot_index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>`
**get\_slot\_custom\_icon\_left**(slot\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphNode_method_get_slot_custom_icon_left>`

Returns the left (input) custom `Texture2D<class_Texture2D>` of the slot
with the given `slot_index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>`
**get\_slot\_custom\_icon\_right**(slot\_index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphNode_method_get_slot_custom_icon_right>`

Returns the right (output) custom `Texture2D<class_Texture2D>` of the
slot with the given `slot_index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_slot\_type\_left**(slot\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphNode_method_get_slot_type_left>`

Returns the left (input) type of the slot with the given `slot_index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_slot\_type\_right**(slot\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphNode_method_get_slot_type_right>`

Returns the right (output) type of the slot with the given `slot_index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`HBoxContainer<class_HBoxContainer>` **get\_titlebar\_hbox**()
`🔗<class_GraphNode_method_get_titlebar_hbox>`

Returns the `HBoxContainer<class_HBoxContainer>` used for the title bar,
only containing a `Label<class_Label>` for displaying the title by
default. This can be used to add custom controls to the title bar such
as option or close buttons.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_slot\_draw\_stylebox**(slot\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphNode_method_is_slot_draw_stylebox>`

Returns true if the background `StyleBox<class_StyleBox>` of the slot
with the given `slot_index` is drawn.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_slot\_enabled\_left**(slot\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphNode_method_is_slot_enabled_left>`

Returns `true` if left (input) side of the slot with the given
`slot_index` is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_slot\_enabled\_right**(slot\_index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GraphNode_method_is_slot_enabled_right>`

Returns `true` if right (output) side of the slot with the given
`slot_index` is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_slot**(slot\_index: `int<class_int>`,
enable\_left\_port: `bool<class_bool>`, type\_left: `int<class_int>`,
color\_left: `Color<class_Color>`, enable\_right\_port:
`bool<class_bool>`, type\_right: `int<class_int>`, color\_right:
`Color<class_Color>`, custom\_icon\_left: `Texture2D<class_Texture2D>` =
null, custom\_icon\_right: `Texture2D<class_Texture2D>` = null,
draw\_stylebox: `bool<class_bool>` = true)
`🔗<class_GraphNode_method_set_slot>`

Sets properties of the slot with the given `slot_index`.

If `enable_left_port`/`enable_right_port` is `true`, a port will appear
and the slot will be able to be connected from this side.

With `type_left`/`type_right` an arbitrary type can be assigned to each
port. Two ports can be connected if they share the same type, or if the
connection between their types is allowed in the parent
`GraphEdit<class_GraphEdit>` (see
`GraphEdit.add_valid_connection_type<class_GraphEdit_method_add_valid_connection_type>`).
Keep in mind that the `GraphEdit<class_GraphEdit>` has the final say in
accepting the connection. Type compatibility simply allows the
`GraphEdit.connection_request<class_GraphEdit_signal_connection_request>`
signal to be emitted.

Ports can be further customized using `color_left`/`color_right` and
`custom_icon_left`/`custom_icon_right`. The color parameter adds a tint
to the icon. The custom icon can be used to override the default port
dot.

Additionally, `draw_stylebox` can be used to enable or disable drawing
of the background stylebox for each slot. See
`slot<class_GraphNode_theme_style_slot>`.

Individual properties can also be set using one of the `set_slot_*`
methods.

\*\*Note:\*\* This method only sets properties of the slot. To create
the slot itself, add a `Control<class_Control>`-derived child to the
GraphNode.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_slot\_color\_left**(slot\_index:
`int<class_int>`, color: `Color<class_Color>`)
`🔗<class_GraphNode_method_set_slot_color_left>`

Sets the `Color<class_Color>` of the left (input) side of the slot with
the given `slot_index` to `color`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_slot\_color\_right**(slot\_index:
`int<class_int>`, color: `Color<class_Color>`)
`🔗<class_GraphNode_method_set_slot_color_right>`

Sets the `Color<class_Color>` of the right (output) side of the slot
with the given `slot_index` to `color`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_slot\_custom\_icon\_left**(slot\_index:
`int<class_int>`, custom\_icon: `Texture2D<class_Texture2D>`)
`🔗<class_GraphNode_method_set_slot_custom_icon_left>`

Sets the custom `Texture2D<class_Texture2D>` of the left (input) side of
the slot with the given `slot_index` to `custom_icon`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_slot\_custom\_icon\_right**(slot\_index: `int<class_int>`,
custom\_icon: `Texture2D<class_Texture2D>`)
`🔗<class_GraphNode_method_set_slot_custom_icon_right>`

Sets the custom `Texture2D<class_Texture2D>` of the right (output) side
of the slot with the given `slot_index` to `custom_icon`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_slot\_draw\_stylebox**(slot\_index:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_GraphNode_method_set_slot_draw_stylebox>`

Toggles the background `StyleBox<class_StyleBox>` of the slot with the
given `slot_index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_slot\_enabled\_left**(slot\_index:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_GraphNode_method_set_slot_enabled_left>`

Toggles the left (input) side of the slot with the given `slot_index`.
If `enable` is `true`, a port will appear on the left side and the slot
will be able to be connected from this side.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_slot\_enabled\_right**(slot\_index:
`int<class_int>`, enable: `bool<class_bool>`)
`🔗<class_GraphNode_method_set_slot_enabled_right>`

Toggles the right (output) side of the slot with the given `slot_index`.
If `enable` is `true`, a port will appear on the right side and the slot
will be able to be connected from this side.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_slot\_type\_left**(slot\_index:
`int<class_int>`, type: `int<class_int>`)
`🔗<class_GraphNode_method_set_slot_type_left>`

Sets the left (input) type of the slot with the given `slot_index` to
`type`. If the value is negative, all connections will be disallowed to
be created via user inputs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_slot\_type\_right**(slot\_index:
`int<class_int>`, type: `int<class_int>`)
`🔗<class_GraphNode_method_set_slot_type_right>`

Sets the right (output) type of the slot with the given `slot_index` to
`type`. If the value is negative, all connections will be disallowed to
be created via user inputs.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **resizer\_color** =
`Color(0.875, 0.875, 0.875, 1)`
`🔗<class_GraphNode_theme_color_resizer_color>`

The color modulation applied to the resizer icon.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **port\_h\_offset** = `0`
`🔗<class_GraphNode_theme_constant_port_h_offset>`

Horizontal offset for the ports.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **separation** = `2`
`🔗<class_GraphNode_theme_constant_separation>`

The vertical distance between ports.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **port**
`🔗<class_GraphNode_theme_icon_port>`

The icon used for representing ports.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **panel**
`🔗<class_GraphNode_theme_style_panel>`

The default background for the slot area of the **GraphNode**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **panel\_selected**
`🔗<class_GraphNode_theme_style_panel_selected>`

The `StyleBox<class_StyleBox>` used for the slot area when selected.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **slot**
`🔗<class_GraphNode_theme_style_slot>`

The `StyleBox<class_StyleBox>` used for each slot of the **GraphNode**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **titlebar**
`🔗<class_GraphNode_theme_style_titlebar>`

The `StyleBox<class_StyleBox>` used for the title bar of the
**GraphNode**.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **titlebar\_selected**
`🔗<class_GraphNode_theme_style_titlebar_selected>`

The `StyleBox<class_StyleBox>` used for the title bar of the
**GraphNode** when it is selected.
