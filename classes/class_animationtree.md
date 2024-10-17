github\_url  
hide

# AnimationTree

**Inherits:** `AnimationMixer<class_AnimationMixer>` **&lt;**
`Node<class_Node>` **&lt;** `Object<class_Object>`

A node used for advanced animation transitions in an
`AnimationPlayer<class_AnimationPlayer>`.

classref-introduction-group

## Description

A node used for advanced animation transitions in an
`AnimationPlayer<class_AnimationPlayer>`.

\*\*Note:\*\* When linked with an
`AnimationPlayer<class_AnimationPlayer>`, several properties and methods
of the corresponding `AnimationPlayer<class_AnimationPlayer>` will not
function as expected. Playback and transitions should be handled using
only the **AnimationTree** and its constituent
`AnimationNode<class_AnimationNode>`(s). The
`AnimationPlayer<class_AnimationPlayer>` node should be used solely for
adding, deleting, and editing animations.

classref-introduction-group

## Tutorials

-   `Using AnimationTree <../tutorials/animation/animation_tree>`
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**animation\_player\_changed**()
`🔗<class_AnimationTree_signal_animation_player_changed>`

Emitted when the `anim_player<class_AnimationTree_property_anim_player>`
is changed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **AnimationProcessCallback**:
`🔗<enum_AnimationTree_AnimationProcessCallback>`

classref-enumeration-constant

`AnimationProcessCallback<enum_AnimationTree_AnimationProcessCallback>`
**ANIMATION\_PROCESS\_PHYSICS** = `0`

**Deprecated:** See
`AnimationMixer.ANIMATION_CALLBACK_MODE_PROCESS_PHYSICS<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_PROCESS_PHYSICS>`.

classref-enumeration-constant

`AnimationProcessCallback<enum_AnimationTree_AnimationProcessCallback>`
**ANIMATION\_PROCESS\_IDLE** = `1`

**Deprecated:** See
`AnimationMixer.ANIMATION_CALLBACK_MODE_PROCESS_IDLE<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_PROCESS_IDLE>`.

classref-enumeration-constant

`AnimationProcessCallback<enum_AnimationTree_AnimationProcessCallback>`
**ANIMATION\_PROCESS\_MANUAL** = `2`

**Deprecated:** See
`AnimationMixer.ANIMATION_CALLBACK_MODE_PROCESS_MANUAL<class_AnimationMixer_constant_ANIMATION_CALLBACK_MODE_PROCESS_MANUAL>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`NodePath<class_NodePath>` **advance\_expression\_base\_node** =
`NodePath(".")`
`🔗<class_AnimationTree_property_advance_expression_base_node>`

classref-property-setget

-   `void (No return value.)`
    **set\_advance\_expression\_base\_node**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>`
    **get\_advance\_expression\_base\_node**()

The path to the `Node<class_Node>` used to evaluate the
`AnimationNode<class_AnimationNode>` `Expression<class_Expression>` if
one is not explicitly specified internally.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **anim\_player** = `NodePath("")`
`🔗<class_AnimationTree_property_anim_player>`

classref-property-setget

-   `void (No return value.)` **set\_animation\_player**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_animation\_player**()

The path to the `AnimationPlayer<class_AnimationPlayer>` used for
animating.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AnimationRootNode<class_AnimationRootNode>` **tree\_root**
`🔗<class_AnimationTree_property_tree_root>`

classref-property-setget

-   `void (No return value.)` **set\_tree\_root**(value:
    `AnimationRootNode<class_AnimationRootNode>`)
-   `AnimationRootNode<class_AnimationRootNode>` **get\_tree\_root**()

The root animation node of this **AnimationTree**. See
`AnimationRootNode<class_AnimationRootNode>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`AnimationProcessCallback<enum_AnimationTree_AnimationProcessCallback>`
**get\_process\_callback**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_AnimationTree_method_get_process_callback>`

**Deprecated:** Use
`AnimationMixer.callback_mode_process<class_AnimationMixer_property_callback_mode_process>`
instead.

Returns the process notification in which to update animations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_process\_callback**(mode:
`AnimationProcessCallback<enum_AnimationTree_AnimationProcessCallback>`)
`🔗<class_AnimationTree_method_set_process_callback>`

**Deprecated:** Use
`AnimationMixer.callback_mode_process<class_AnimationMixer_property_callback_mode_process>`
instead.

Sets the process notification in which to update animations.
