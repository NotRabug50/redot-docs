github\_url  
hide

# MarginContainer

**Inherits:** `Container<class_Container>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

A container that keeps a margin around its child controls.

classref-introduction-group

## Description

**MarginContainer** adds an adjustable margin on each side of its child
controls. The margins are added around all children, not around each
individual one. To control the **MarginContainer**'s margins, use the
`margin_*` theme properties listed below.

\*\*Note:\*\* The margin sizes are theme overrides, not normal
properties. This is an example of how to change them in code:

gdscript

\# This code sample assumes the current script is extending
MarginContainer. var margin\_value = 100
add\_theme\_constant\_override("margin\_top", margin\_value)
add\_theme\_constant\_override("margin\_left", margin\_value)
add\_theme\_constant\_override("margin\_bottom", margin\_value)
add\_theme\_constant\_override("margin\_right", margin\_value)

csharp

// This code sample assumes the current script is extending
MarginContainer. int marginValue = 100;
AddThemeConstantOverride("margin\_top", marginValue);
AddThemeConstantOverride("margin\_left", marginValue);
AddThemeConstantOverride("margin\_bottom", marginValue);
AddThemeConstantOverride("margin\_right", marginValue);

classref-introduction-group

## Tutorials

-   `Using Containers <../tutorials/ui/gui_containers>`

classref-reftable-group

## Theme Properties

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

## Theme Property Descriptions

classref-themeproperty

`int<class_int>` **margin\_bottom** = `0`
`🔗<class_MarginContainer_theme_constant_margin_bottom>`

Offsets towards the inside direct children of the container by this
amount of pixels from the bottom.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **margin\_left** = `0`
`🔗<class_MarginContainer_theme_constant_margin_left>`

Offsets towards the inside direct children of the container by this
amount of pixels from the left.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **margin\_right** = `0`
`🔗<class_MarginContainer_theme_constant_margin_right>`

Offsets towards the inside direct children of the container by this
amount of pixels from the right.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **margin\_top** = `0`
`🔗<class_MarginContainer_theme_constant_margin_top>`

Offsets towards the inside direct children of the container by this
amount of pixels from the top.
