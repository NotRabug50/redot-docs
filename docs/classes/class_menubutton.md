github\_url  
hide

# MenuButton

**Inherits:** `Button<class_Button>` **&lt;**
`BaseButton<class_BaseButton>` **&lt;** `Control<class_Control>`
**&lt;** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A button that brings up a `PopupMenu<class_PopupMenu>` when clicked.

classref-introduction-group

## Description

A button that brings up a `PopupMenu<class_PopupMenu>` when clicked. To
create new items inside this `PopupMenu<class_PopupMenu>`, use
`get_popup().add_item("My Item Name")`. You can also create them
directly from Godot editor's inspector.

See also `BaseButton<class_BaseButton>` which contains common properties
and methods associated with this node.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**about\_to\_popup**() `🔗<class_MenuButton_signal_about_to_popup>`

Emitted when the `PopupMenu<class_PopupMenu>` of this MenuButton is
about to show.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **item\_count** = `0`
`🔗<class_MenuButton_property_item_count>`

classref-property-setget

-   `void (No return value.)` **set\_item\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_item\_count**()

The number of items currently in the list.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **switch\_on\_hover** = `false`
`🔗<class_MenuButton_property_switch_on_hover>`

classref-property-setget

-   `void (No return value.)` **set\_switch\_on\_hover**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_switch\_on\_hover**()

If `true`, when the cursor hovers above another **MenuButton** within
the same parent which also has
`switch_on_hover<class_MenuButton_property_switch_on_hover>` enabled, it
will close the current **MenuButton** and open the other one.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`PopupMenu<class_PopupMenu>` **get\_popup**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MenuButton_method_get_popup>`

Returns the `PopupMenu<class_PopupMenu>` contained in this button.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to hide it or any of its children, use
their `Window.visible<class_Window_property_visible>` property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_disable\_shortcuts**(disabled:
`bool<class_bool>`) `🔗<class_MenuButton_method_set_disable_shortcuts>`

If `true`, shortcuts are disabled and cannot be used to trigger the
button.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **show\_popup**()
`🔗<class_MenuButton_method_show_popup>`

Adjusts popup position and sizing for the **MenuButton**, then shows the
`PopupMenu<class_PopupMenu>`. Prefer this over using
`get_popup().popup()`.
