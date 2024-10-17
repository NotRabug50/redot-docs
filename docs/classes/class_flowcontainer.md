github\_url  
hide

# FlowContainer

**Inherits:** `Container<class_Container>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `HFlowContainer<class_HFlowContainer>`,
`VFlowContainer<class_VFlowContainer>`

A container that arranges its child controls horizontally or vertically
and wraps them around at the borders.

classref-introduction-group

## Description

A container that arranges its child controls horizontally or vertically
and wraps them around at the borders. This is similar to how text in a
book wraps around when no more words can fit on a line.

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

classref-reftable-group

## Methods

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

## Enumerations

classref-enumeration

enum **AlignmentMode**: `🔗<enum_FlowContainer_AlignmentMode>`

classref-enumeration-constant

`AlignmentMode<enum_FlowContainer_AlignmentMode>` **ALIGNMENT\_BEGIN** =
`0`

The child controls will be arranged at the beginning of the container,
i.e. top if orientation is vertical, left if orientation is horizontal
(right for RTL layout).

classref-enumeration-constant

`AlignmentMode<enum_FlowContainer_AlignmentMode>` **ALIGNMENT\_CENTER**
= `1`

The child controls will be centered in the container.

classref-enumeration-constant

`AlignmentMode<enum_FlowContainer_AlignmentMode>` **ALIGNMENT\_END** =
`2`

The child controls will be arranged at the end of the container, i.e.
bottom if orientation is vertical, right if orientation is horizontal
(left for RTL layout).

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LastWrapAlignmentMode**:
`🔗<enum_FlowContainer_LastWrapAlignmentMode>`

classref-enumeration-constant

`LastWrapAlignmentMode<enum_FlowContainer_LastWrapAlignmentMode>`
**LAST\_WRAP\_ALIGNMENT\_INHERIT** = `0`

The last partially filled row or column will wrap aligned to the
previous row or column in accordance with
`alignment<class_FlowContainer_property_alignment>`.

classref-enumeration-constant

`LastWrapAlignmentMode<enum_FlowContainer_LastWrapAlignmentMode>`
**LAST\_WRAP\_ALIGNMENT\_BEGIN** = `1`

The last partially filled row or column will wrap aligned to the
beginning of the previous row or column.

classref-enumeration-constant

`LastWrapAlignmentMode<enum_FlowContainer_LastWrapAlignmentMode>`
**LAST\_WRAP\_ALIGNMENT\_CENTER** = `2`

The last partially filled row or column will wrap aligned to the center
of the previous row or column.

classref-enumeration-constant

`LastWrapAlignmentMode<enum_FlowContainer_LastWrapAlignmentMode>`
**LAST\_WRAP\_ALIGNMENT\_END** = `3`

The last partially filled row or column will wrap aligned to the end of
the previous row or column.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`AlignmentMode<enum_FlowContainer_AlignmentMode>` **alignment** = `0`
`🔗<class_FlowContainer_property_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_alignment**(value:
    `AlignmentMode<enum_FlowContainer_AlignmentMode>`)
-   `AlignmentMode<enum_FlowContainer_AlignmentMode>`
    **get\_alignment**()

The alignment of the container's children (must be one of
`ALIGNMENT_BEGIN<class_FlowContainer_constant_ALIGNMENT_BEGIN>`,
`ALIGNMENT_CENTER<class_FlowContainer_constant_ALIGNMENT_CENTER>`, or
`ALIGNMENT_END<class_FlowContainer_constant_ALIGNMENT_END>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`LastWrapAlignmentMode<enum_FlowContainer_LastWrapAlignmentMode>`
**last\_wrap\_alignment** = `0`
`🔗<class_FlowContainer_property_last_wrap_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_last\_wrap\_alignment**(value:
    `LastWrapAlignmentMode<enum_FlowContainer_LastWrapAlignmentMode>`)
-   `LastWrapAlignmentMode<enum_FlowContainer_LastWrapAlignmentMode>`
    **get\_last\_wrap\_alignment**()

The wrap behavior of the last, partially filled row or column (must be
one of
`LAST_WRAP_ALIGNMENT_INHERIT<class_FlowContainer_constant_LAST_WRAP_ALIGNMENT_INHERIT>`,
`LAST_WRAP_ALIGNMENT_BEGIN<class_FlowContainer_constant_LAST_WRAP_ALIGNMENT_BEGIN>`,
`LAST_WRAP_ALIGNMENT_CENTER<class_FlowContainer_constant_LAST_WRAP_ALIGNMENT_CENTER>`,
or
`LAST_WRAP_ALIGNMENT_END<class_FlowContainer_constant_LAST_WRAP_ALIGNMENT_END>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **reverse\_fill** = `false`
`🔗<class_FlowContainer_property_reverse_fill>`

classref-property-setget

-   `void (No return value.)` **set\_reverse\_fill**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_reverse\_fill**()

If `true`, reverses fill direction. Horizontal **FlowContainer**s will
fill rows bottom to top, vertical **FlowContainer**s will fill columns
right to left.

When using a vertical **FlowContainer** with a right to left
`Control.layout_direction<class_Control_property_layout_direction>`,
columns will fill left to right instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **vertical** = `false`
`🔗<class_FlowContainer_property_vertical>`

classref-property-setget

-   `void (No return value.)` **set\_vertical**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_vertical**()

If `true`, the **FlowContainer** will arrange its children vertically,
rather than horizontally.

Can't be changed when using `HFlowContainer<class_HFlowContainer>` and
`VFlowContainer<class_VFlowContainer>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_line\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_FlowContainer_method_get_line_count>`

Returns the current line count.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`int<class_int>` **h\_separation** = `4`
`🔗<class_FlowContainer_theme_constant_h_separation>`

The horizontal separation of child nodes.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **v\_separation** = `4`
`🔗<class_FlowContainer_theme_constant_v_separation>`

The vertical separation of child nodes.
