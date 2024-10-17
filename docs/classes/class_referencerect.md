github\_url  
hide

# ReferenceRect

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A rectangle hint for designing UIs.

classref-introduction-group

## Description

A rectangle box that displays only a colored border around its
rectangle. It is used to visualize the extents of a
`Control<class_Control>`.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Color<class_Color>` **border\_color** = `Color(1, 0, 0, 1)`
`🔗<class_ReferenceRect_property_border_color>`

classref-property-setget

-   `void (No return value.)` **set\_border\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_border\_color**()

Sets the border color of the **ReferenceRect**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **border\_width** = `1.0`
`🔗<class_ReferenceRect_property_border_width>`

classref-property-setget

-   `void (No return value.)` **set\_border\_width**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_border\_width**()

Sets the border width of the **ReferenceRect**. The border grows both
inwards and outwards with respect to the rectangle box.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **editor\_only** = `true`
`🔗<class_ReferenceRect_property_editor_only>`

classref-property-setget

-   `void (No return value.)` **set\_editor\_only**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_editor\_only**()

If `true`, the **ReferenceRect** will only be visible while in editor.
Otherwise, **ReferenceRect** will be visible in the running project.
