github\_url  
hide

# GridContainer

**Inherits:** `Container<class_Container>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

A container that arranges its child controls in a grid layout.

classref-introduction-group

## Description

**GridContainer** arranges its child controls in a grid layout. The
number of columns is specified by the
`columns<class_GridContainer_property_columns>` property, whereas the
number of rows depends on how many are needed for the child controls.
The number of rows and columns is preserved for every size of the
container.

\*\*Note:\*\* **GridContainer** only works with child nodes inheriting
from `Control<class_Control>`. It won't rearrange child nodes inheriting
from `Node2D<class_Node2D>`.

classref-introduction-group

## Tutorials

-   `Using Containers <../tutorials/ui/gui_containers>`
-   [Operating System Testing
    Demo](https://godotengine.org/asset-library/asset/2789)

classref-reftable-group

## Properties

<table>
<tbody>
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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **columns** = `1`
`🔗<class_GridContainer_property_columns>`

classref-property-setget

-   `void (No return value.)` **set\_columns**(value: `int<class_int>`)
-   `int<class_int>` **get\_columns**()

The number of columns in the **GridContainer**. If modified,
**GridContainer** reorders its Control-derived children to accommodate
the new layout.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`int<class_int>` **h\_separation** = `4`
`🔗<class_GridContainer_theme_constant_h_separation>`

The horizontal separation of child nodes.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **v\_separation** = `4`
`🔗<class_GridContainer_theme_constant_v_separation>`

The vertical separation of child nodes.
