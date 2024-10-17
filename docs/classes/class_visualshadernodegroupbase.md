github\_url  
hide

# VisualShaderNodeGroupBase

**Inherits:**
`VisualShaderNodeResizableBase<class_VisualShaderNodeResizableBase>`
**&lt;** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`VisualShaderNodeExpression<class_VisualShaderNodeExpression>`

Base class for a family of nodes with variable number of input and
output ports within the visual shader graph.

classref-introduction-group

## Description

Currently, has no direct usage, use the derived classes instead.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_input\_port**(id: `int<class_int>`,
type: `int<class_int>`, name: `String<class_String>`)
`🔗<class_VisualShaderNodeGroupBase_method_add_input_port>`

Adds an input port with the specified `type` (see
`PortType<enum_VisualShaderNode_PortType>`) and `name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_output\_port**(id: `int<class_int>`,
type: `int<class_int>`, name: `String<class_String>`)
`🔗<class_VisualShaderNodeGroupBase_method_add_output_port>`

Adds an output port with the specified `type` (see
`PortType<enum_VisualShaderNode_PortType>`) and `name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_input\_ports**()
`🔗<class_VisualShaderNodeGroupBase_method_clear_input_ports>`

Removes all previously specified input ports.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_output\_ports**()
`🔗<class_VisualShaderNodeGroupBase_method_clear_output_ports>`

Removes all previously specified output ports.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_free\_input\_port\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNodeGroupBase_method_get_free_input_port_id>`

Returns a free input port ID which can be used in
`add_input_port<class_VisualShaderNodeGroupBase_method_add_input_port>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_free\_output\_port\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNodeGroupBase_method_get_free_output_port_id>`

Returns a free output port ID which can be used in
`add_output_port<class_VisualShaderNodeGroupBase_method_add_output_port>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_input\_port\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNodeGroupBase_method_get_input_port_count>`

Returns the number of input ports in use. Alternative for
`get_free_input_port_id<class_VisualShaderNodeGroupBase_method_get_free_input_port_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_inputs**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNodeGroupBase_method_get_inputs>`

Returns a `String<class_String>` description of the input ports as a
colon-separated list using the format `id,type,name;` (see
`add_input_port<class_VisualShaderNodeGroupBase_method_add_input_port>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_output\_port\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNodeGroupBase_method_get_output_port_count>`

Returns the number of output ports in use. Alternative for
`get_free_output_port_id<class_VisualShaderNodeGroupBase_method_get_free_output_port_id>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_outputs**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNodeGroupBase_method_get_outputs>`

Returns a `String<class_String>` description of the output ports as a
colon-separated list using the format `id,type,name;` (see
`add_output_port<class_VisualShaderNodeGroupBase_method_add_output_port>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_input\_port**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNodeGroupBase_method_has_input_port>`

Returns `true` if the specified input port exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_output\_port**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNodeGroupBase_method_has_output_port>`

Returns `true` if the specified output port exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_port\_name**(name:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShaderNodeGroupBase_method_is_valid_port_name>`

Returns `true` if the specified port name does not override an existed
port name and is valid within the shader.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_input\_port**(id: `int<class_int>`)
`🔗<class_VisualShaderNodeGroupBase_method_remove_input_port>`

Removes the specified input port.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_output\_port**(id: `int<class_int>`)
`🔗<class_VisualShaderNodeGroupBase_method_remove_output_port>`

Removes the specified output port.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_input\_port\_name**(id:
`int<class_int>`, name: `String<class_String>`)
`🔗<class_VisualShaderNodeGroupBase_method_set_input_port_name>`

Renames the specified input port.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_input\_port\_type**(id:
`int<class_int>`, type: `int<class_int>`)
`🔗<class_VisualShaderNodeGroupBase_method_set_input_port_type>`

Sets the specified input port's type (see
`PortType<enum_VisualShaderNode_PortType>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_inputs**(inputs:
`String<class_String>`)
`🔗<class_VisualShaderNodeGroupBase_method_set_inputs>`

Defines all input ports using a `String<class_String>` formatted as a
colon-separated list: `id,type,name;` (see
`add_input_port<class_VisualShaderNodeGroupBase_method_add_input_port>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_output\_port\_name**(id:
`int<class_int>`, name: `String<class_String>`)
`🔗<class_VisualShaderNodeGroupBase_method_set_output_port_name>`

Renames the specified output port.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_output\_port\_type**(id:
`int<class_int>`, type: `int<class_int>`)
`🔗<class_VisualShaderNodeGroupBase_method_set_output_port_type>`

Sets the specified output port's type (see
`PortType<enum_VisualShaderNode_PortType>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_outputs**(outputs:
`String<class_String>`)
`🔗<class_VisualShaderNodeGroupBase_method_set_outputs>`

Defines all output ports using a `String<class_String>` formatted as a
colon-separated list: `id,type,name;` (see
`add_output_port<class_VisualShaderNodeGroupBase_method_add_output_port>`).
