github\_url  
hide

# GraphElement

**Experimental:** This class may be changed or removed in future
versions.

**Inherits:** `Container<class_Container>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `GraphFrame<class_GraphFrame>`,
`GraphNode<class_GraphNode>`

A container that represents a basic element that can be placed inside a
`GraphEdit<class_GraphEdit>` control.

classref-introduction-group

## Description

**GraphElement** allows to create custom elements for a
`GraphEdit<class_GraphEdit>` graph. By default such elements can be
selected, resized, and repositioned, but they cannot be connected. For a
graph element that allows for connections see
`GraphNode<class_GraphNode>`.

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

## Theme Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**delete\_request**() `🔗<class_GraphElement_signal_delete_request>`

Emitted when removing the GraphElement is requested.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**dragged**(from: `Vector2<class_Vector2>`, to:
`Vector2<class_Vector2>`) `🔗<class_GraphElement_signal_dragged>`

Emitted when the GraphElement is dragged.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**node\_deselected**() `🔗<class_GraphElement_signal_node_deselected>`

Emitted when the GraphElement is deselected.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**node\_selected**() `🔗<class_GraphElement_signal_node_selected>`

Emitted when the GraphElement is selected.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**position\_offset\_changed**()
`🔗<class_GraphElement_signal_position_offset_changed>`

Emitted when the GraphElement is moved.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**raise\_request**() `🔗<class_GraphElement_signal_raise_request>`

Emitted when displaying the GraphElement over other ones is requested.
Happens on focusing (clicking into) the GraphElement.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**resize\_end**(new\_size: `Vector2<class_Vector2>`)
`🔗<class_GraphElement_signal_resize_end>`

Emitted when releasing the mouse button after dragging the resizer
handle (see `resizable<class_GraphElement_property_resizable>`).

classref-item-separator

------------------------------------------------------------------------

classref-signal

**resize\_request**(new\_size: `Vector2<class_Vector2>`)
`🔗<class_GraphElement_signal_resize_request>`

Emitted when resizing the GraphElement is requested. Happens on dragging
the resizer handle (see
`resizable<class_GraphElement_property_resizable>`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **draggable** = `true`
`🔗<class_GraphElement_property_draggable>`

classref-property-setget

-   `void (No return value.)` **set\_draggable**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_draggable**()

If `true`, the user can drag the GraphElement.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **position\_offset** = `Vector2(0, 0)`
`🔗<class_GraphElement_property_position_offset>`

classref-property-setget

-   `void (No return value.)` **set\_position\_offset**(value:
    `Vector2<class_Vector2>`)
-   `Vector2<class_Vector2>` **get\_position\_offset**()

The offset of the GraphElement, relative to the scroll offset of the
`GraphEdit<class_GraphEdit>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **resizable** = `false`
`🔗<class_GraphElement_property_resizable>`

classref-property-setget

-   `void (No return value.)` **set\_resizable**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_resizable**()

If `true`, the user can resize the GraphElement.

\*\*Note:\*\* Dragging the handle will only emit the
`resize_request<class_GraphElement_signal_resize_request>` and
`resize_end<class_GraphElement_signal_resize_end>` signals, the
GraphElement needs to be resized manually.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **selectable** = `true`
`🔗<class_GraphElement_property_selectable>`

classref-property-setget

-   `void (No return value.)` **set\_selectable**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_selectable**()

If `true`, the user can select the GraphElement.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **selected** = `false`
`🔗<class_GraphElement_property_selected>`

classref-property-setget

-   `void (No return value.)` **set\_selected**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_selected**()

If `true`, the GraphElement is selected.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Texture2D<class_Texture2D>` **resizer**
`🔗<class_GraphElement_theme_icon_resizer>`

The icon used for the resizer, visible when
`resizable<class_GraphElement_property_resizable>` is enabled.
