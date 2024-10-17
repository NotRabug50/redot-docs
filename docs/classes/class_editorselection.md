github\_url  
hide

# EditorSelection

**Inherits:** `Object<class_Object>`

Manages the SceneTree selection in the editor.

classref-introduction-group

## Description

This object manages the SceneTree selection in the editor.

\*\*Note:\*\* This class shouldn't be instantiated directly. Instead,
access the singleton using
`EditorInterface.get_selection<class_EditorInterface_method_get_selection>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**selection\_changed**()
`🔗<class_EditorSelection_signal_selection_changed>`

Emitted when the selection changes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_node**(node: `Node<class_Node>`)
`🔗<class_EditorSelection_method_add_node>`

Adds a node to the selection.

\*\*Note:\*\* The newly selected node will not be automatically edited
in the inspector. If you want to edit a node, use
`EditorInterface.edit_node<class_EditorInterface_method_edit_node>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_EditorSelection_method_clear>`

Clear the selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Node<class_Node>`\] **get\_selected\_nodes**()
`🔗<class_EditorSelection_method_get_selected_nodes>`

Returns the list of selected nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Node<class_Node>`\]
**get\_transformable\_selected\_nodes**()
`🔗<class_EditorSelection_method_get_transformable_selected_nodes>`

Returns the list of selected nodes, optimized for transform operations
(i.e. moving them, rotating, etc.). This list can be used to avoid
situations where a node is selected and is also a child/grandchild.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_node**(node: `Node<class_Node>`)
`🔗<class_EditorSelection_method_remove_node>`

Removes a node from the selection.
