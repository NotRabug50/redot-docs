github\_url  
hide

# VisibleOnScreenEnabler2D

**Inherits:**
`VisibleOnScreenNotifier2D<class_VisibleOnScreenNotifier2D>` **&lt;**
`Node2D<class_Node2D>` **&lt;** `CanvasItem<class_CanvasItem>` **&lt;**
`Node<class_Node>` **&lt;** `Object<class_Object>`

A rectangular region of 2D space that, when visible on screen, enables a
target node.

classref-introduction-group

## Description

**VisibleOnScreenEnabler2D** contains a rectangular region of 2D space
and a target node. The target node will be automatically enabled (via
its `Node.process_mode<class_Node_property_process_mode>` property) when
any part of this region becomes visible on the screen, and automatically
disabled otherwise. This can for example be used to activate enemies
only when the player approaches them.

See `VisibleOnScreenNotifier2D<class_VisibleOnScreenNotifier2D>` if you
only want to be notified when the region is visible on screen.

\*\*Note:\*\* **VisibleOnScreenEnabler2D** uses the render culling code
to determine whether it's visible on screen, so it won't function unless
`CanvasItem.visible<class_CanvasItem_property_visible>` is set to
`true`.

classref-reftable-group

## Properties

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

## Enumerations

classref-enumeration

enum **EnableMode**: `🔗<enum_VisibleOnScreenEnabler2D_EnableMode>`

classref-enumeration-constant

`EnableMode<enum_VisibleOnScreenEnabler2D_EnableMode>`
**ENABLE\_MODE\_INHERIT** = `0`

Corresponds to
`Node.PROCESS_MODE_INHERIT<class_Node_constant_PROCESS_MODE_INHERIT>`.

classref-enumeration-constant

`EnableMode<enum_VisibleOnScreenEnabler2D_EnableMode>`
**ENABLE\_MODE\_ALWAYS** = `1`

Corresponds to
`Node.PROCESS_MODE_ALWAYS<class_Node_constant_PROCESS_MODE_ALWAYS>`.

classref-enumeration-constant

`EnableMode<enum_VisibleOnScreenEnabler2D_EnableMode>`
**ENABLE\_MODE\_WHEN\_PAUSED** = `2`

Corresponds to
`Node.PROCESS_MODE_WHEN_PAUSED<class_Node_constant_PROCESS_MODE_WHEN_PAUSED>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`EnableMode<enum_VisibleOnScreenEnabler2D_EnableMode>` **enable\_mode**
= `0` `🔗<class_VisibleOnScreenEnabler2D_property_enable_mode>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_mode**(value:
    `EnableMode<enum_VisibleOnScreenEnabler2D_EnableMode>`)
-   `EnableMode<enum_VisibleOnScreenEnabler2D_EnableMode>`
    **get\_enable\_mode**()

Determines how the target node is enabled. Corresponds to
`ProcessMode<enum_Node_ProcessMode>`. When the node is disabled, it
always uses
`Node.PROCESS_MODE_DISABLED<class_Node_constant_PROCESS_MODE_DISABLED>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **enable\_node\_path** = `NodePath("..")`
`🔗<class_VisibleOnScreenEnabler2D_property_enable_node_path>`

classref-property-setget

-   `void (No return value.)` **set\_enable\_node\_path**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_enable\_node\_path**()

The path to the target node, relative to the
**VisibleOnScreenEnabler2D**. The target node is cached; it's only
assigned when setting this property (if the **VisibleOnScreenEnabler2D**
is inside the scene tree) and every time the
**VisibleOnScreenEnabler2D** enters the scene tree. If the path is
empty, no node will be affected. If the path is invalid, an error is
also generated.
