github\_url  
hide

# AspectRatioContainer

**Inherits:** `Container<class_Container>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

A container that preserves the proportions of its child controls.

classref-introduction-group

## Description

A container type that arranges its child controls in a way that
preserves their proportions automatically when the container is resized.
Useful when a container has a dynamic size and the child nodes must
adjust their sizes accordingly without losing their aspect ratios.

classref-introduction-group

## Tutorials

-   `Using Containers <../tutorials/ui/gui_containers>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **StretchMode**: `🔗<enum_AspectRatioContainer_StretchMode>`

classref-enumeration-constant

`StretchMode<enum_AspectRatioContainer_StretchMode>`
**STRETCH\_WIDTH\_CONTROLS\_HEIGHT** = `0`

The height of child controls is automatically adjusted based on the
width of the container.

classref-enumeration-constant

`StretchMode<enum_AspectRatioContainer_StretchMode>`
**STRETCH\_HEIGHT\_CONTROLS\_WIDTH** = `1`

The width of child controls is automatically adjusted based on the
height of the container.

classref-enumeration-constant

`StretchMode<enum_AspectRatioContainer_StretchMode>` **STRETCH\_FIT** =
`2`

The bounding rectangle of child controls is automatically adjusted to
fit inside the container while keeping the aspect ratio.

classref-enumeration-constant

`StretchMode<enum_AspectRatioContainer_StretchMode>` **STRETCH\_COVER**
= `3`

The width and height of child controls is automatically adjusted to make
their bounding rectangle cover the entire area of the container while
keeping the aspect ratio.

When the bounding rectangle of child controls exceed the container's
size and `Control.clip_contents<class_Control_property_clip_contents>`
is enabled, this allows to show only the container's area restricted by
its own bounding rectangle.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **AlignmentMode**: `🔗<enum_AspectRatioContainer_AlignmentMode>`

classref-enumeration-constant

`AlignmentMode<enum_AspectRatioContainer_AlignmentMode>`
**ALIGNMENT\_BEGIN** = `0`

Aligns child controls with the beginning (left or top) of the container.

classref-enumeration-constant

`AlignmentMode<enum_AspectRatioContainer_AlignmentMode>`
**ALIGNMENT\_CENTER** = `1`

Aligns child controls with the center of the container.

classref-enumeration-constant

`AlignmentMode<enum_AspectRatioContainer_AlignmentMode>`
**ALIGNMENT\_END** = `2`

Aligns child controls with the end (right or bottom) of the container.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`AlignmentMode<enum_AspectRatioContainer_AlignmentMode>`
**alignment\_horizontal** = `1`
`🔗<class_AspectRatioContainer_property_alignment_horizontal>`

classref-property-setget

-   `void (No return value.)` **set\_alignment\_horizontal**(value:
    `AlignmentMode<enum_AspectRatioContainer_AlignmentMode>`)
-   `AlignmentMode<enum_AspectRatioContainer_AlignmentMode>`
    **get\_alignment\_horizontal**()

Specifies the horizontal relative position of child controls.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AlignmentMode<enum_AspectRatioContainer_AlignmentMode>`
**alignment\_vertical** = `1`
`🔗<class_AspectRatioContainer_property_alignment_vertical>`

classref-property-setget

-   `void (No return value.)` **set\_alignment\_vertical**(value:
    `AlignmentMode<enum_AspectRatioContainer_AlignmentMode>`)
-   `AlignmentMode<enum_AspectRatioContainer_AlignmentMode>`
    **get\_alignment\_vertical**()

Specifies the vertical relative position of child controls.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **ratio** = `1.0`
`🔗<class_AspectRatioContainer_property_ratio>`

classref-property-setget

-   `void (No return value.)` **set\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_ratio**()

The aspect ratio to enforce on child controls. This is the width divided
by the height. The ratio depends on the
`stretch_mode<class_AspectRatioContainer_property_stretch_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StretchMode<enum_AspectRatioContainer_StretchMode>` **stretch\_mode** =
`2` `🔗<class_AspectRatioContainer_property_stretch_mode>`

classref-property-setget

-   `void (No return value.)` **set\_stretch\_mode**(value:
    `StretchMode<enum_AspectRatioContainer_StretchMode>`)
-   `StretchMode<enum_AspectRatioContainer_StretchMode>`
    **get\_stretch\_mode**()

The stretch mode used to align child controls.
