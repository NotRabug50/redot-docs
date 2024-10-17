github\_url  
hide

# SplitContainer

**Inherits:** `Container<class_Container>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `HSplitContainer<class_HSplitContainer>`,
`VSplitContainer<class_VSplitContainer>`

A container that splits two child controls horizontally or vertically
and provides a grabber for adjusting the split ratio.

classref-introduction-group

## Description

A container that accepts only two child controls, then arranges them
horizontally or vertically and creates a divisor between them. The
divisor can be dragged around to change the size relation between the
child controls.

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**drag\_ended**() `🔗<class_SplitContainer_signal_drag_ended>`

Emitted when the user ends dragging.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**drag\_started**() `🔗<class_SplitContainer_signal_drag_started>`

Emitted when the user starts dragging.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**dragged**(offset: `int<class_int>`)
`🔗<class_SplitContainer_signal_dragged>`

Emitted when the dragger is dragged by user.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **DraggerVisibility**: `🔗<enum_SplitContainer_DraggerVisibility>`

classref-enumeration-constant

`DraggerVisibility<enum_SplitContainer_DraggerVisibility>`
**DRAGGER\_VISIBLE** = `0`

The split dragger icon is always visible when
`autohide<class_SplitContainer_theme_constant_autohide>` is `false`,
otherwise visible only when the cursor hovers it.

The size of the grabber icon determines the minimum
`separation<class_SplitContainer_theme_constant_separation>`.

The dragger icon is automatically hidden if the length of the grabber
icon is longer than the split bar.

classref-enumeration-constant

`DraggerVisibility<enum_SplitContainer_DraggerVisibility>`
**DRAGGER\_HIDDEN** = `1`

The split dragger icon is never visible regardless of the value of
`autohide<class_SplitContainer_theme_constant_autohide>`.

The size of the grabber icon determines the minimum
`separation<class_SplitContainer_theme_constant_separation>`.

classref-enumeration-constant

`DraggerVisibility<enum_SplitContainer_DraggerVisibility>`
**DRAGGER\_HIDDEN\_COLLAPSED** = `2`

The split dragger icon is not visible, and the split bar is collapsed to
zero thickness.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **collapsed** = `false`
`🔗<class_SplitContainer_property_collapsed>`

classref-property-setget

-   `void (No return value.)` **set\_collapsed**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_collapsed**()

If `true`, the area of the first `Control<class_Control>` will be
collapsed and the dragger will be disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **drag\_area\_highlight\_in\_editor** = `false`
`🔗<class_SplitContainer_property_drag_area_highlight_in_editor>`

classref-property-setget

-   `void (No return value.)`
    **set\_drag\_area\_highlight\_in\_editor**(value:
    `bool<class_bool>`)
-   `bool<class_bool>`
    **is\_drag\_area\_highlight\_in\_editor\_enabled**()

Highlights the drag area `Rect2<class_Rect2>` so you can see where it is
during development. The drag area is gold if
`dragging_enabled<class_SplitContainer_property_dragging_enabled>` is
`true`, and red if `false`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **drag\_area\_margin\_begin** = `0`
`🔗<class_SplitContainer_property_drag_area_margin_begin>`

classref-property-setget

-   `void (No return value.)` **set\_drag\_area\_margin\_begin**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_drag\_area\_margin\_begin**()

Reduces the size of the drag area and split bar
`split_bar_background<class_SplitContainer_theme_style_split_bar_background>`
at the beginning of the container.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **drag\_area\_margin\_end** = `0`
`🔗<class_SplitContainer_property_drag_area_margin_end>`

classref-property-setget

-   `void (No return value.)` **set\_drag\_area\_margin\_end**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_drag\_area\_margin\_end**()

Reduces the size of the drag area and split bar
`split_bar_background<class_SplitContainer_theme_style_split_bar_background>`
at the end of the container.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **drag\_area\_offset** = `0`
`🔗<class_SplitContainer_property_drag_area_offset>`

classref-property-setget

-   `void (No return value.)` **set\_drag\_area\_offset**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_drag\_area\_offset**()

Shifts the drag area in the axis of the container to prevent the drag
area from overlapping the `ScrollBar<class_ScrollBar>` or other
selectable `Control<class_Control>` of a child node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DraggerVisibility<enum_SplitContainer_DraggerVisibility>`
**dragger\_visibility** = `0`
`🔗<class_SplitContainer_property_dragger_visibility>`

classref-property-setget

-   `void (No return value.)` **set\_dragger\_visibility**(value:
    `DraggerVisibility<enum_SplitContainer_DraggerVisibility>`)
-   `DraggerVisibility<enum_SplitContainer_DraggerVisibility>`
    **get\_dragger\_visibility**()

Determines the dragger's visibility. See
`DraggerVisibility<enum_SplitContainer_DraggerVisibility>` for details.
This property does not determine whether dragging is enabled or not. Use
`dragging_enabled<class_SplitContainer_property_dragging_enabled>` for
that.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **dragging\_enabled** = `true`
`🔗<class_SplitContainer_property_dragging_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_dragging\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_dragging\_enabled**()

Enables or disables split dragging.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **split\_offset** = `0`
`🔗<class_SplitContainer_property_split_offset>`

classref-property-setget

-   `void (No return value.)` **set\_split\_offset**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_split\_offset**()

The initial offset of the splitting between the two
`Control<class_Control>`s, with `0` being at the end of the first
`Control<class_Control>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **vertical** = `false`
`🔗<class_SplitContainer_property_vertical>`

classref-property-setget

-   `void (No return value.)` **set\_vertical**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_vertical**()

If `true`, the **SplitContainer** will arrange its children vertically,
rather than horizontally.

Can't be changed when using `HSplitContainer<class_HSplitContainer>` and
`VSplitContainer<class_VSplitContainer>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **clamp\_split\_offset**()
`🔗<class_SplitContainer_method_clamp_split_offset>`

Clamps the `split_offset<class_SplitContainer_property_split_offset>`
value to not go outside the currently possible minimal and maximum
values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Control<class_Control>` **get\_drag\_area\_control**()
`🔗<class_SplitContainer_method_get_drag_area_control>`

Returns the drag area `Control<class_Control>`. For example, you can
move a pre-configured button into the drag area `Control<class_Control>`
so that it rides along with the split bar. Try setting the
`Button<class_Button>` anchors to `center` prior to the `reparent()`
call.

    $BarnacleButton.reparent($SplitContainer.get_drag_area_control())

\*\*Note:\*\* The drag area `Control<class_Control>` is drawn over the
**SplitContainer**'s children, so `CanvasItem<class_CanvasItem>` draw
objects called from the `Control<class_Control>` and children added to
the `Control<class_Control>` will also appear over the
**SplitContainer**'s children. Try setting
`Control.mouse_filter<class_Control_property_mouse_filter>` of custom
children to
`Control.MOUSE_FILTER_IGNORE<class_Control_constant_MOUSE_FILTER_IGNORE>`
to prevent blocking the mouse from dragging if desired.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`int<class_int>` **autohide** = `1`
`🔗<class_SplitContainer_theme_constant_autohide>`

Boolean value. If `1` (`true`), the grabber will hide automatically when
it isn't under the cursor. If `0` (`false`), it's always visible. The
`dragger_visibility<class_SplitContainer_property_dragger_visibility>`
must be
`DRAGGER_VISIBLE<class_SplitContainer_constant_DRAGGER_VISIBLE>`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **minimum\_grab\_thickness** = `6`
`🔗<class_SplitContainer_theme_constant_minimum_grab_thickness>`

The minimum thickness of the area users can click on to grab the split
bar. This ensures that the split bar can still be dragged if
`separation<class_SplitContainer_theme_constant_separation>` or
`h_grabber<class_SplitContainer_theme_icon_h_grabber>` /
`v_grabber<class_SplitContainer_theme_icon_v_grabber>`'s size is too
narrow to easily select.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **separation** = `12`
`🔗<class_SplitContainer_theme_constant_separation>`

The split bar thickness, i.e., the gap between the two children of the
container. This is overridden by the size of the grabber icon if
`dragger_visibility<class_SplitContainer_property_dragger_visibility>`
is set to
`DRAGGER_VISIBLE<class_SplitContainer_constant_DRAGGER_VISIBLE>`, or
`DRAGGER_HIDDEN<class_SplitContainer_constant_DRAGGER_HIDDEN>`, and
`separation<class_SplitContainer_theme_constant_separation>` is smaller
than the size of the grabber icon in the same axis.

\*\*Note:\*\* To obtain
`separation<class_SplitContainer_theme_constant_separation>` values less
than the size of the grabber icon, for example a `1 px` hairline, set
`h_grabber<class_SplitContainer_theme_icon_h_grabber>` or
`v_grabber<class_SplitContainer_theme_icon_v_grabber>` to a new
`ImageTexture<class_ImageTexture>`, which effectively sets the grabber
icon size to `0 px`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **grabber**
`🔗<class_SplitContainer_theme_icon_grabber>`

The icon used for the grabber drawn in the middle area.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **h\_grabber**
`🔗<class_SplitContainer_theme_icon_h_grabber>`

The icon used for the grabber drawn in the middle area when
`vertical<class_SplitContainer_property_vertical>` is `false`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **v\_grabber**
`🔗<class_SplitContainer_theme_icon_v_grabber>`

The icon used for the grabber drawn in the middle area when
`vertical<class_SplitContainer_property_vertical>` is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **split\_bar\_background**
`🔗<class_SplitContainer_theme_style_split_bar_background>`

Determines the background of the split bar if its thickness is greater
than zero.
