github\_url  
hide

# EditorScriptPicker

**Inherits:** `EditorResourcePicker<class_EditorResourcePicker>`
**&lt;** `HBoxContainer<class_HBoxContainer>` **&lt;**
`BoxContainer<class_BoxContainer>` **&lt;** `Container<class_Container>`
**&lt;** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Godot editor's control for selecting the `script` property of a
`Node<class_Node>`.

classref-introduction-group

## Description

Similar to `EditorResourcePicker<class_EditorResourcePicker>` this
`Control<class_Control>` node is used in the editor's Inspector dock,
but only to edit the `script` property of a `Node<class_Node>`. Default
options for creating new resources of all possible subtypes are replaced
with dedicated buttons that open the "Attach Node Script" dialog. Can be
used with `EditorInspectorPlugin<class_EditorInspectorPlugin>` to
recreate the same behavior.

\*\*Note:\*\* You must set the
`script_owner<class_EditorScriptPicker_property_script_owner>` for the
custom context menu items to work.

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

`Node<class_Node>` **script\_owner**
`🔗<class_EditorScriptPicker_property_script_owner>`

classref-property-setget

-   `void (No return value.)` **set\_script\_owner**(value:
    `Node<class_Node>`)
-   `Node<class_Node>` **get\_script\_owner**()

The owner `Node<class_Node>` of the script property that holds the
edited resource.
