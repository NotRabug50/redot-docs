github\_url  
hide

# AnimationNode

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `AnimationNodeOutput<class_AnimationNodeOutput>`,
`AnimationNodeSync<class_AnimationNodeSync>`,
`AnimationNodeTimeScale<class_AnimationNodeTimeScale>`,
`AnimationNodeTimeSeek<class_AnimationNodeTimeSeek>`,
`AnimationRootNode<class_AnimationRootNode>`

Base class for `AnimationTree<class_AnimationTree>` nodes. Not related
to scene nodes.

classref-introduction-group

## Description

Base resource for `AnimationTree<class_AnimationTree>` nodes. In
general, it's not used directly, but you can create custom ones with
custom blending formulas.

Inherit this when creating animation nodes mainly for use in
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`, otherwise
`AnimationRootNode<class_AnimationRootNode>` should be used instead.

You can access the time information as read-only parameter which is
processed and stored in the previous frame for all nodes except
`AnimationNodeOutput<class_AnimationNodeOutput>`.

\*\*Note:\*\* If multiple inputs exist in the **AnimationNode**, which
time information takes precedence depends on the type of
**AnimationNode**.

    var current_length = $AnimationTree[parameters/AnimationNodeName/current_length]
    var current_position = $AnimationTree[parameters/AnimationNodeName/current_position]
    var current_delta = $AnimationTree[parameters/AnimationNodeName/current_delta]

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

## Signals

classref-signal

**animation\_node\_removed**(object\_id: `int<class_int>`, name:
`String<class_String>`)
`🔗<class_AnimationNode_signal_animation_node_removed>`

Emitted by nodes that inherit from this class and that have an internal
tree when one of their animation nodes removes. The animation nodes that
emit this signal are
`AnimationNodeBlendSpace1D<class_AnimationNodeBlendSpace1D>`,
`AnimationNodeBlendSpace2D<class_AnimationNodeBlendSpace2D>`,
`AnimationNodeStateMachine<class_AnimationNodeStateMachine>`, and
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**animation\_node\_renamed**(object\_id: `int<class_int>`, old\_name:
`String<class_String>`, new\_name: `String<class_String>`)
`🔗<class_AnimationNode_signal_animation_node_renamed>`

Emitted by nodes that inherit from this class and that have an internal
tree when one of their animation node names changes. The animation nodes
that emit this signal are
`AnimationNodeBlendSpace1D<class_AnimationNodeBlendSpace1D>`,
`AnimationNodeBlendSpace2D<class_AnimationNodeBlendSpace2D>`,
`AnimationNodeStateMachine<class_AnimationNodeStateMachine>`, and
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tree\_changed**() `🔗<class_AnimationNode_signal_tree_changed>`

Emitted by nodes that inherit from this class and that have an internal
tree when one of their animation nodes changes. The animation nodes that
emit this signal are
`AnimationNodeBlendSpace1D<class_AnimationNodeBlendSpace1D>`,
`AnimationNodeBlendSpace2D<class_AnimationNodeBlendSpace2D>`,
`AnimationNodeStateMachine<class_AnimationNodeStateMachine>`,
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>` and
`AnimationNodeTransition<class_AnimationNodeTransition>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **FilterAction**: `🔗<enum_AnimationNode_FilterAction>`

classref-enumeration-constant

`FilterAction<enum_AnimationNode_FilterAction>` **FILTER\_IGNORE** = `0`

Do not use filtering.

classref-enumeration-constant

`FilterAction<enum_AnimationNode_FilterAction>` **FILTER\_PASS** = `1`

Paths matching the filter will be allowed to pass.

classref-enumeration-constant

`FilterAction<enum_AnimationNode_FilterAction>` **FILTER\_STOP** = `2`

Paths matching the filter will be discarded.

classref-enumeration-constant

`FilterAction<enum_AnimationNode_FilterAction>` **FILTER\_BLEND** = `3`

Paths matching the filter will be blended (by the blend value).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **filter\_enabled**
`🔗<class_AnimationNode_property_filter_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_filter\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_filter\_enabled**()

If `true`, filtering is enabled.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`String<class_String>` **\_get\_caption**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_private_method__get_caption>`

When inheriting from `AnimationRootNode<class_AnimationRootNode>`,
implement this virtual method to override the text caption for this
animation node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AnimationNode<class_AnimationNode>` **\_get\_child\_by\_name**(name:
`StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_private_method__get_child_by_name>`

When inheriting from `AnimationRootNode<class_AnimationRootNode>`,
implement this virtual method to return a child animation node by its
`name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **\_get\_child\_nodes**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_private_method__get_child_nodes>`

When inheriting from `AnimationRootNode<class_AnimationRootNode>`,
implement this virtual method to return all child animation nodes in
order as a `name: node` dictionary.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_get\_parameter\_default\_value**(parameter:
`StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_private_method__get_parameter_default_value>`

When inheriting from `AnimationRootNode<class_AnimationRootNode>`,
implement this virtual method to return the default value of a
`parameter`. Parameters are custom local memory used for your animation
nodes, given a resource can be reused in multiple trees.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **\_get\_parameter\_list**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_private_method__get_parameter_list>`

When inheriting from `AnimationRootNode<class_AnimationRootNode>`,
implement this virtual method to return a list of the properties on this
animation node. Parameters are custom local memory used for your
animation nodes, given a resource can be reused in multiple trees.
Format is similar to
`Object.get_property_list<class_Object_method_get_property_list>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_has\_filter**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_private_method__has_filter>`

When inheriting from `AnimationRootNode<class_AnimationRootNode>`,
implement this virtual method to return whether the blend tree editor
should display filter editing on this animation node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_is\_parameter\_read\_only**(parameter:
`StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_private_method__is_parameter_read_only>`

When inheriting from `AnimationRootNode<class_AnimationRootNode>`,
implement this virtual method to return whether the `parameter` is
read-only. Parameters are custom local memory used for your animation
nodes, given a resource can be reused in multiple trees.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **\_process**(time: `float<class_float>`, seek:
`bool<class_bool>`, is\_external\_seeking: `bool<class_bool>`,
test\_only: `bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_private_method__process>`

**Deprecated:** Currently this is mostly useless as there is a lack of
many APIs to extend AnimationNode by GDScript. It is planned that a more
flexible API using structures will be provided in the future.

When inheriting from `AnimationRootNode<class_AnimationRootNode>`,
implement this virtual method to run some code when this animation node
is processed. The `time` parameter is a relative delta, unless `seek` is
`true`, in which case it is absolute.

Here, call the `blend_input<class_AnimationNode_method_blend_input>`,
`blend_node<class_AnimationNode_method_blend_node>` or
`blend_animation<class_AnimationNode_method_blend_animation>` functions.
You can also use
`get_parameter<class_AnimationNode_method_get_parameter>` and
`set_parameter<class_AnimationNode_method_set_parameter>` to modify
local memory.

This function should return the delta.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **add\_input**(name: `String<class_String>`)
`🔗<class_AnimationNode_method_add_input>`

Adds an input to the animation node. This is only useful for animation
nodes created for use in an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`. If the addition
fails, returns `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **blend\_animation**(animation:
`StringName<class_StringName>`, time: `float<class_float>`, delta:
`float<class_float>`, seeked: `bool<class_bool>`, is\_external\_seeking:
`bool<class_bool>`, blend: `float<class_float>`, looped\_flag:
`LoopedFlag<enum_Animation_LoopedFlag>` = 0)
`🔗<class_AnimationNode_method_blend_animation>`

Blend an animation by `blend` amount (name must be valid in the linked
`AnimationPlayer<class_AnimationPlayer>`). A `time` and `delta` may be
passed, as well as whether `seeked` happened.

A `looped_flag` is used by internal processing immediately after the
loop. See also `LoopedFlag<enum_Animation_LoopedFlag>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **blend\_input**(input\_index: `int<class_int>`,
time: `float<class_float>`, seek: `bool<class_bool>`,
is\_external\_seeking: `bool<class_bool>`, blend: `float<class_float>`,
filter: `FilterAction<enum_AnimationNode_FilterAction>` = 0, sync:
`bool<class_bool>` = true, test\_only: `bool<class_bool>` = false)
`🔗<class_AnimationNode_method_blend_input>`

Blend an input. This is only useful for animation nodes created for an
`AnimationNodeBlendTree<class_AnimationNodeBlendTree>`. The `time`
parameter is a relative delta, unless `seek` is `true`, in which case it
is absolute. A filter mode may be optionally passed (see
`FilterAction<enum_AnimationNode_FilterAction>` for options).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **blend\_node**(name:
`StringName<class_StringName>`, node:
`AnimationNode<class_AnimationNode>`, time: `float<class_float>`, seek:
`bool<class_bool>`, is\_external\_seeking: `bool<class_bool>`, blend:
`float<class_float>`, filter:
`FilterAction<enum_AnimationNode_FilterAction>` = 0, sync:
`bool<class_bool>` = true, test\_only: `bool<class_bool>` = false)
`🔗<class_AnimationNode_method_blend_node>`

Blend another animation node (in case this animation node contains child
animation nodes). This function is only useful if you inherit from
`AnimationRootNode<class_AnimationRootNode>` instead, otherwise editors
will not display your animation node for addition.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **find\_input**(name: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_method_find_input>`

Returns the input index which corresponds to `name`. If not found,
returns `-1`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_input\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_method_get_input_count>`

Amount of inputs in this animation node, only useful for animation nodes
that go into `AnimationNodeBlendTree<class_AnimationNodeBlendTree>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_input\_name**(input: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_method_get_input_name>`

Gets the name of an input by index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_parameter**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_method_get_parameter>`

Gets the value of a parameter. Parameters are custom local memory used
for your animation nodes, given a resource can be reused in multiple
trees.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_path\_filtered**(path:
`NodePath<class_NodePath>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationNode_method_is_path_filtered>`

Returns whether the given path is filtered.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_input**(index: `int<class_int>`)
`🔗<class_AnimationNode_method_remove_input>`

Removes an input, call this only when inactive.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_filter\_path**(path:
`NodePath<class_NodePath>`, enable: `bool<class_bool>`)
`🔗<class_AnimationNode_method_set_filter_path>`

Adds or removes a path for the filter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **set\_input\_name**(input: `int<class_int>`, name:
`String<class_String>`) `🔗<class_AnimationNode_method_set_input_name>`

Sets the name of the input at the given `input` index. If the setting
fails, returns `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_parameter**(name:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`🔗<class_AnimationNode_method_set_parameter>`

Sets a custom parameter. These are used as local memory, because
resources can be reused across the tree or scenes.
