github\_url  
hide

# Container

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `AspectRatioContainer<class_AspectRatioContainer>`,
`BoxContainer<class_BoxContainer>`,
`CenterContainer<class_CenterContainer>`,
`EditorProperty<class_EditorProperty>`,
`FlowContainer<class_FlowContainer>`,
`GraphElement<class_GraphElement>`,
`GridContainer<class_GridContainer>`,
`MarginContainer<class_MarginContainer>`,
`PanelContainer<class_PanelContainer>`,
`ScrollContainer<class_ScrollContainer>`,
`SplitContainer<class_SplitContainer>`,
`SubViewportContainer<class_SubViewportContainer>`,
`TabContainer<class_TabContainer>`

Base class for all GUI containers.

classref-introduction-group

## Description

Base class for all GUI containers. A **Container** automatically
arranges its child controls in a certain way. This class can be
inherited to make custom container types.

classref-introduction-group

## Tutorials

-   `Using Containers <../tutorials/ui/gui_containers>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**pre\_sort\_children**() `🔗<class_Container_signal_pre_sort_children>`

Emitted when children are going to be sorted.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**sort\_children**() `🔗<class_Container_signal_sort_children>`

Emitted when sorting the children is needed.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NOTIFICATION\_PRE\_SORT\_CHILDREN** = `50`
`🔗<class_Container_constant_NOTIFICATION_PRE_SORT_CHILDREN>`

Notification just before children are going to be sorted, in case
there's something to process beforehand.

classref-constant

**NOTIFICATION\_SORT\_CHILDREN** = `51`
`🔗<class_Container_constant_NOTIFICATION_SORT_CHILDREN>`

Notification for when sorting the children, it must be obeyed
immediately.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**\_get\_allowed\_size\_flags\_horizontal**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Container_private_method__get_allowed_size_flags_horizontal>`

Implement to return a list of allowed horizontal
`SizeFlags<enum_Control_SizeFlags>` for child nodes. This doesn't
technically prevent the usages of any other size flags, if your
implementation requires that. This only limits the options available to
the user in the Inspector dock.

\*\*Note:\*\* Having no size flags is equal to having
`Control.SIZE_SHRINK_BEGIN<class_Control_constant_SIZE_SHRINK_BEGIN>`.
As such, this value is always implicitly allowed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>`
**\_get\_allowed\_size\_flags\_vertical**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Container_private_method__get_allowed_size_flags_vertical>`

Implement to return a list of allowed vertical
`SizeFlags<enum_Control_SizeFlags>` for child nodes. This doesn't
technically prevent the usages of any other size flags, if your
implementation requires that. This only limits the options available to
the user in the Inspector dock.

\*\*Note:\*\* Having no size flags is equal to having
`Control.SIZE_SHRINK_BEGIN<class_Control_constant_SIZE_SHRINK_BEGIN>`.
As such, this value is always implicitly allowed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fit\_child\_in\_rect**(child:
`Control<class_Control>`, rect: `Rect2<class_Rect2>`)
`🔗<class_Container_method_fit_child_in_rect>`

Fit a child control in a given rect. This is mainly a helper for
creating custom container classes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **queue\_sort**()
`🔗<class_Container_method_queue_sort>`

Queue resort of the contained children. This is called automatically
anyway, but can be called upon request.
