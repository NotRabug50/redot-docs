github\_url  
hide

# VisualShader

**Inherits:** `Shader<class_Shader>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A custom shader program with a visual editor.

classref-introduction-group

## Description

This class provides a graph-like visual editor for creating a
`Shader<class_Shader>`. Although **VisualShader**s do not require
coding, they share the same logic with script shaders. They use
`VisualShaderNode<class_VisualShaderNode>`s that can be connected to
each other to control the flow of the shader. The visual shader graph is
converted to a script shader behind the scenes.

classref-introduction-group

## Tutorials

-   `Using VisualShaders <../tutorials/shaders/visual_shaders>`

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

## Enumerations

classref-enumeration

enum **Type**: `🔗<enum_VisualShader_Type>`

classref-enumeration-constant

`Type<enum_VisualShader_Type>` **TYPE\_VERTEX** = `0`

A vertex shader, operating on vertices.

classref-enumeration-constant

`Type<enum_VisualShader_Type>` **TYPE\_FRAGMENT** = `1`

A fragment shader, operating on fragments (pixels).

classref-enumeration-constant

`Type<enum_VisualShader_Type>` **TYPE\_LIGHT** = `2`

A shader for light calculations.

classref-enumeration-constant

`Type<enum_VisualShader_Type>` **TYPE\_START** = `3`

A function for the "start" stage of particle shader.

classref-enumeration-constant

`Type<enum_VisualShader_Type>` **TYPE\_PROCESS** = `4`

A function for the "process" stage of particle shader.

classref-enumeration-constant

`Type<enum_VisualShader_Type>` **TYPE\_COLLIDE** = `5`

A function for the "collide" stage (particle collision handler) of
particle shader.

classref-enumeration-constant

`Type<enum_VisualShader_Type>` **TYPE\_START\_CUSTOM** = `6`

A function for the "start" stage of particle shader, with customized
output.

classref-enumeration-constant

`Type<enum_VisualShader_Type>` **TYPE\_PROCESS\_CUSTOM** = `7`

A function for the "process" stage of particle shader, with customized
output.

classref-enumeration-constant

`Type<enum_VisualShader_Type>` **TYPE\_SKY** = `8`

A shader for 3D environment's sky.

classref-enumeration-constant

`Type<enum_VisualShader_Type>` **TYPE\_FOG** = `9`

A compute shader that runs for each froxel of the volumetric fog map.

classref-enumeration-constant

`Type<enum_VisualShader_Type>` **TYPE\_MAX** = `10`

Represents the size of the `Type<enum_VisualShader_Type>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **VaryingMode**: `🔗<enum_VisualShader_VaryingMode>`

classref-enumeration-constant

`VaryingMode<enum_VisualShader_VaryingMode>`
**VARYING\_MODE\_VERTEX\_TO\_FRAG\_LIGHT** = `0`

Varying is passed from `Vertex` function to `Fragment` and `Light`
functions.

classref-enumeration-constant

`VaryingMode<enum_VisualShader_VaryingMode>`
**VARYING\_MODE\_FRAG\_TO\_LIGHT** = `1`

Varying is passed from `Fragment` function to `Light` function.

classref-enumeration-constant

`VaryingMode<enum_VisualShader_VaryingMode>` **VARYING\_MODE\_MAX** =
`2`

Represents the size of the `VaryingMode<enum_VisualShader_VaryingMode>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **VaryingType**: `🔗<enum_VisualShader_VaryingType>`

classref-enumeration-constant

`VaryingType<enum_VisualShader_VaryingType>` **VARYING\_TYPE\_FLOAT** =
`0`

Varying is of type `float<class_float>`.

classref-enumeration-constant

`VaryingType<enum_VisualShader_VaryingType>` **VARYING\_TYPE\_INT** =
`1`

Varying is of type `int<class_int>`.

classref-enumeration-constant

`VaryingType<enum_VisualShader_VaryingType>` **VARYING\_TYPE\_UINT** =
`2`

Varying is of type unsigned `int<class_int>`.

classref-enumeration-constant

`VaryingType<enum_VisualShader_VaryingType>`
**VARYING\_TYPE\_VECTOR\_2D** = `3`

Varying is of type `Vector2<class_Vector2>`.

classref-enumeration-constant

`VaryingType<enum_VisualShader_VaryingType>`
**VARYING\_TYPE\_VECTOR\_3D** = `4`

Varying is of type `Vector3<class_Vector3>`.

classref-enumeration-constant

`VaryingType<enum_VisualShader_VaryingType>`
**VARYING\_TYPE\_VECTOR\_4D** = `5`

Varying is of type `Vector4<class_Vector4>`.

classref-enumeration-constant

`VaryingType<enum_VisualShader_VaryingType>` **VARYING\_TYPE\_BOOLEAN**
= `6`

Varying is of type `bool<class_bool>`.

classref-enumeration-constant

`VaryingType<enum_VisualShader_VaryingType>`
**VARYING\_TYPE\_TRANSFORM** = `7`

Varying is of type `Transform3D<class_Transform3D>`.

classref-enumeration-constant

`VaryingType<enum_VisualShader_VaryingType>` **VARYING\_TYPE\_MAX** =
`8`

Represents the size of the `VaryingType<enum_VisualShader_VaryingType>`
enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NODE\_ID\_INVALID** = `-1`
`🔗<class_VisualShader_constant_NODE_ID_INVALID>`

Indicates an invalid **VisualShader** node.

classref-constant

**NODE\_ID\_OUTPUT** = `0`
`🔗<class_VisualShader_constant_NODE_ID_OUTPUT>`

Indicates an output node of **VisualShader**.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Vector2<class_Vector2>` **graph\_offset** = `Vector2(0, 0)`
`🔗<class_VisualShader_property_graph_offset>`

classref-property-setget

-   `void (No return value.)` **set\_graph\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_graph\_offset**()

The offset vector of the whole graph.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_node**(type:
`Type<enum_VisualShader_Type>`, node:
`VisualShaderNode<class_VisualShaderNode>`, position:
`Vector2<class_Vector2>`, id: `int<class_int>`)
`🔗<class_VisualShader_method_add_node>`

Adds the specified `node` to the shader.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_varying**(name: `String<class_String>`,
mode: `VaryingMode<enum_VisualShader_VaryingMode>`, type:
`VaryingType<enum_VisualShader_VaryingType>`)
`🔗<class_VisualShader_method_add_varying>`

Adds a new varying value node to the shader.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **attach\_node\_to\_frame**(type:
`Type<enum_VisualShader_Type>`, id: `int<class_int>`, frame:
`int<class_int>`) `🔗<class_VisualShader_method_attach_node_to_frame>`

Attaches the given node to the given frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **can\_connect\_nodes**(type:
`Type<enum_VisualShader_Type>`, from\_node: `int<class_int>`,
from\_port: `int<class_int>`, to\_node: `int<class_int>`, to\_port:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShader_method_can_connect_nodes>`

Returns `true` if the specified nodes and ports can be connected
together.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **connect\_nodes**(type:
`Type<enum_VisualShader_Type>`, from\_node: `int<class_int>`,
from\_port: `int<class_int>`, to\_node: `int<class_int>`, to\_port:
`int<class_int>`) `🔗<class_VisualShader_method_connect_nodes>`

Connects the specified nodes and ports.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **connect\_nodes\_forced**(type:
`Type<enum_VisualShader_Type>`, from\_node: `int<class_int>`,
from\_port: `int<class_int>`, to\_node: `int<class_int>`, to\_port:
`int<class_int>`) `🔗<class_VisualShader_method_connect_nodes_forced>`

Connects the specified nodes and ports, even if they can't be connected.
Such connection is invalid and will not function properly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **detach\_node\_from\_frame**(type:
`Type<enum_VisualShader_Type>`, id: `int<class_int>`)
`🔗<class_VisualShader_method_detach_node_from_frame>`

Detaches the given node from the frame it is attached to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **disconnect\_nodes**(type:
`Type<enum_VisualShader_Type>`, from\_node: `int<class_int>`,
from\_port: `int<class_int>`, to\_node: `int<class_int>`, to\_port:
`int<class_int>`) `🔗<class_VisualShader_method_disconnect_nodes>`

Connects the specified nodes and ports.

classref-item-separator

------------------------------------------------------------------------

classref-method

`VisualShaderNode<class_VisualShaderNode>` **get\_node**(type:
`Type<enum_VisualShader_Type>`, id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShader_method_get_node>`

Returns the shader node instance with specified `type` and `id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_node\_connections**(type: `Type<enum_VisualShader_Type>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShader_method_get_node_connections>`

Returns the list of connected nodes with the specified type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>` **get\_node\_list**(type:
`Type<enum_VisualShader_Type>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShader_method_get_node_list>`

Returns the list of all nodes in the shader with the specified type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_node\_position**(type:
`Type<enum_VisualShader_Type>`, id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShader_method_get_node_position>`

Returns the position of the specified node within the shader graph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_valid\_node\_id**(type:
`Type<enum_VisualShader_Type>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShader_method_get_valid_node_id>`

Returns next valid node ID that can be added to the shader graph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_varying**(name: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShader_method_has_varying>`

Returns `true` if the shader has a varying with the given `name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_node\_connection**(type:
`Type<enum_VisualShader_Type>`, from\_node: `int<class_int>`,
from\_port: `int<class_int>`, to\_node: `int<class_int>`, to\_port:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisualShader_method_is_node_connection>`

Returns `true` if the specified node and port connection exist.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_node**(type:
`Type<enum_VisualShader_Type>`, id: `int<class_int>`)
`🔗<class_VisualShader_method_remove_node>`

Removes the specified node from the shader.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_varying**(name:
`String<class_String>`) `🔗<class_VisualShader_method_remove_varying>`

Removes a varying value node with the given `name`. Prints an error if a
node with this name is not found.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **replace\_node**(type:
`Type<enum_VisualShader_Type>`, id: `int<class_int>`, new\_class:
`StringName<class_StringName>`)
`🔗<class_VisualShader_method_replace_node>`

Replaces the specified node with a node of new class type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_mode**(mode: `Mode<enum_Shader_Mode>`)
`🔗<class_VisualShader_method_set_mode>`

Sets the mode of this shader.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_node\_position**(type:
`Type<enum_VisualShader_Type>`, id: `int<class_int>`, position:
`Vector2<class_Vector2>`)
`🔗<class_VisualShader_method_set_node_position>`

Sets the position of the specified node.
