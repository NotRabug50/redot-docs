github\_url  
hide

# VisibleOnScreenNotifier3D

**Inherits:** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:**
`VisibleOnScreenEnabler3D<class_VisibleOnScreenEnabler3D>`

A box-shaped region of 3D space that detects whether it is visible on
screen.

classref-introduction-group

## Description

**VisibleOnScreenNotifier3D** represents a box-shaped region of 3D
space. When any part of this region becomes visible on screen or in a
`Camera3D<class_Camera3D>`'s view, it will emit a
`screen_entered<class_VisibleOnScreenNotifier3D_signal_screen_entered>`
signal, and likewise it will emit a
`screen_exited<class_VisibleOnScreenNotifier3D_signal_screen_exited>`
signal when no part of it remains visible.

If you want a node to be enabled automatically when this region is
visible on screen, use
`VisibleOnScreenEnabler3D<class_VisibleOnScreenEnabler3D>`.

\*\*Note:\*\* **VisibleOnScreenNotifier3D** uses an approximate
heuristic that doesn't take walls and other occlusion into account,
unless occlusion culling is used. It also won't function unless
`Node3D.visible<class_Node3D_property_visible>` is set to `true`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**screen\_entered**()
`🔗<class_VisibleOnScreenNotifier3D_signal_screen_entered>`

Emitted when the **VisibleOnScreenNotifier3D** enters the screen.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**screen\_exited**()
`🔗<class_VisibleOnScreenNotifier3D_signal_screen_exited>`

Emitted when the **VisibleOnScreenNotifier3D** exits the screen.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`AABB<class_AABB>` **aabb** = `AABB(-1, -1, -1, 2, 2, 2)`
`🔗<class_VisibleOnScreenNotifier3D_property_aabb>`

classref-property-setget

-   `void (No return value.)` **set\_aabb**(value: `AABB<class_AABB>`)
-   `AABB<class_AABB>` **get\_aabb**()

The **VisibleOnScreenNotifier3D**'s bounding box.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **is\_on\_screen**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VisibleOnScreenNotifier3D_method_is_on_screen>`

Returns `true` if the bounding box is on the screen.

\*\*Note:\*\* It takes one frame for the **VisibleOnScreenNotifier3D**'s
visibility to be assessed once added to the scene tree, so this method
will always return `false` right after it is instantiated.
