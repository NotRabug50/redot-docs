github\_url  
hide

# AnimationNodeBlendTree

**Inherits:** `AnimationRootNode<class_AnimationRootNode>` **&lt;**
`AnimationNode<class_AnimationNode>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A sub-tree of many type `AnimationNode<class_AnimationNode>`s used for
complex animations. Used by `AnimationTree<class_AnimationTree>`.

classref-introduction-group

## Description

This animation node may contain a sub-tree of any other type animation
nodes, such as `AnimationNodeTransition<class_AnimationNodeTransition>`,
`AnimationNodeBlend2<class_AnimationNodeBlend2>`,
`AnimationNodeBlend3<class_AnimationNodeBlend3>`,
`AnimationNodeOneShot<class_AnimationNodeOneShot>`, etc. This is one of
the most commonly used animation node roots.

An `AnimationNodeOutput<class_AnimationNodeOutput>` node named `output`
is created by default.

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**node\_changed**(node\_name: `StringName<class_StringName>`)
`🔗<class_AnimationNodeBlendTree_signal_node_changed>`

Emitted when the input port information is changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**CONNECTION\_OK** = `0`
`🔗<class_AnimationNodeBlendTree_constant_CONNECTION_OK>`

The connection was successful.

classref-constant

**CONNECTION\_ERROR\_NO\_INPUT** = `1`
`🔗<class_AnimationNodeBlendTree_constant_CONNECTION_ERROR_NO_INPUT>`

The input node is `null`.

classref-constant

**CONNECTION\_ERROR\_NO\_INPUT\_INDEX** = `2`
`🔗<class_AnimationNodeBlendTree_constant_CONNECTION_ERROR_NO_INPUT_INDEX>`

The specified input port is out of range.

classref-constant

**CONNECTION\_ERROR\_NO\_OUTPUT** = `3`
`🔗<class_AnimationNodeBlendTree_constant_CONNECTION_ERROR_NO_OUTPUT>`

The output node is `null`.

classref-constant

**CONNECTION\_ERROR\_SAME\_NODE** = `4`
`🔗<class_AnimationNodeBlendTree_constant_CONNECTION_ERROR_SAME_NODE>`

Input and output nodes are the same.

classref-constant

**CONNECTION\_ERROR\_CONNECTION\_EXISTS** = `5`
`🔗<class_AnimationNodeBlendTree_constant_CONNECTION_ERROR_CONNECTION_EXISTS>`

The specified connection already exists.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Vector2<class_Vector2>` **graph\_offset** = `Vector2(0, 0)`
`🔗<class_AnimationNodeBlendTree_property_graph_offset>`

classref-property-setget

-   `void (No return value.)` **set\_graph\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_graph\_offset**()

The global offset of all sub animation nodes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_node**(name:
`StringName<class_StringName>`, node:
`AnimationNode<class_AnimationNode>`, position: `Vector2<class_Vector2>`
= Vector2(0, 0)) `🔗<class_AnimationNodeBlendTree_method_add_node>`

Adds an `AnimationNode<class_AnimationNode>` at the given `position`.
The `name` is used to identify the created sub animation node later.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **connect\_node**(input\_node:
`StringName<class_StringName>`, input\_index: `int<class_int>`,
output\_node: `StringName<class_StringName>`)
`🔗<class_AnimationNodeBlendTree_method_connect_node>`

Connects the output of an `AnimationNode<class_AnimationNode>` as input
for another `AnimationNode<class_AnimationNode>`, at the input port
specified by `input_index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **disconnect\_node**(input\_node:
`StringName<class_StringName>`, input\_index: `int<class_int>`)
`🔗<class_AnimationNodeBlendTree_method_disconnect_node>`

Disconnects the animation node connected to the specified input.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AnimationNode<class_AnimationNode>` **get\_node**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeBlendTree_method_get_node>`

Returns the sub animation node with the specified `name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_node\_position**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeBlendTree_method_get_node_position>`

Returns the position of the sub animation node with the specified
`name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_node**(name: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNodeBlendTree_method_has_node>`

Returns `true` if a sub animation node with specified `name` exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_node**(name:
`StringName<class_StringName>`)
`🔗<class_AnimationNodeBlendTree_method_remove_node>`

Removes a sub animation node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **rename\_node**(name:
`StringName<class_StringName>`, new\_name:
`StringName<class_StringName>`)
`🔗<class_AnimationNodeBlendTree_method_rename_node>`

Changes the name of a sub animation node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_node\_position**(name:
`StringName<class_StringName>`, position: `Vector2<class_Vector2>`)
`🔗<class_AnimationNodeBlendTree_method_set_node_position>`

Modifies the position of a sub animation node.
