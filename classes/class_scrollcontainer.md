github\_url  
hide

# ScrollContainer

**Inherits:** `Container<class_Container>` **&lt;**
`Control<class_Control>` **&lt;** `CanvasItem<class_CanvasItem>`
**&lt;** `Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `EditorInspector<class_EditorInspector>`

A container used to provide scrollbars to a child control when needed.

classref-introduction-group

## Description

A container used to provide a child control with scrollbars when needed.
Scrollbars will automatically be drawn at the right (for vertical) or
bottom (for horizontal) and will enable dragging to move the viewable
Control (and its children) within the ScrollContainer. Scrollbars will
also automatically resize the grabber based on the
`Control.custom_minimum_size<class_Control_property_custom_minimum_size>`
of the Control relative to the ScrollContainer.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**scroll\_ended**() `🔗<class_ScrollContainer_signal_scroll_ended>`

Emitted when scrolling stops when dragging the scrollable area *with a
touch event*. This signal is *not* emitted when scrolling by dragging
the scrollbar, scrolling with the mouse wheel or scrolling with
keyboard/gamepad events.

\*\*Note:\*\* This signal is only emitted on Android or iOS, or on
desktop/web platforms when
`ProjectSettings.input_devices/pointing/emulate_touch_from_mouse<class_ProjectSettings_property_input_devices/pointing/emulate_touch_from_mouse>`
is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**scroll\_started**() `🔗<class_ScrollContainer_signal_scroll_started>`

Emitted when scrolling starts when dragging the scrollable area w\*ith a
touch event\*. This signal is *not* emitted when scrolling by dragging
the scrollbar, scrolling with the mouse wheel or scrolling with
keyboard/gamepad events.

\*\*Note:\*\* This signal is only emitted on Android or iOS, or on
desktop/web platforms when
`ProjectSettings.input_devices/pointing/emulate_touch_from_mouse<class_ProjectSettings_property_input_devices/pointing/emulate_touch_from_mouse>`
is enabled.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ScrollMode**: `🔗<enum_ScrollContainer_ScrollMode>`

classref-enumeration-constant

`ScrollMode<enum_ScrollContainer_ScrollMode>` **SCROLL\_MODE\_DISABLED**
= `0`

Scrolling disabled, scrollbar will be invisible.

classref-enumeration-constant

`ScrollMode<enum_ScrollContainer_ScrollMode>` **SCROLL\_MODE\_AUTO** =
`1`

Scrolling enabled, scrollbar will be visible only if necessary, i.e.
container's content is bigger than the container.

classref-enumeration-constant

`ScrollMode<enum_ScrollContainer_ScrollMode>`
**SCROLL\_MODE\_SHOW\_ALWAYS** = `2`

Scrolling enabled, scrollbar will be always visible.

classref-enumeration-constant

`ScrollMode<enum_ScrollContainer_ScrollMode>`
**SCROLL\_MODE\_SHOW\_NEVER** = `3`

Scrolling enabled, scrollbar will be hidden.

classref-enumeration-constant

`ScrollMode<enum_ScrollContainer_ScrollMode>` **SCROLL\_MODE\_RESERVE**
= `4`

Combines
`SCROLL_MODE_AUTO<class_ScrollContainer_constant_SCROLL_MODE_AUTO>` and
`SCROLL_MODE_SHOW_ALWAYS<class_ScrollContainer_constant_SCROLL_MODE_SHOW_ALWAYS>`.
The scrollbar is only visible if necessary, but the content size is
adjusted as if it was always visible. It's useful for ensuring that
content size stays the same regardless if the scrollbar is visible.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **follow\_focus** = `false`
`🔗<class_ScrollContainer_property_follow_focus>`

classref-property-setget

-   `void (No return value.)` **set\_follow\_focus**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_following\_focus**()

If `true`, the ScrollContainer will automatically scroll to focused
children (including indirect children) to make sure they are fully
visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ScrollMode<enum_ScrollContainer_ScrollMode>`
**horizontal\_scroll\_mode** = `1`
`🔗<class_ScrollContainer_property_horizontal_scroll_mode>`

classref-property-setget

-   `void (No return value.)` **set\_horizontal\_scroll\_mode**(value:
    `ScrollMode<enum_ScrollContainer_ScrollMode>`)
-   `ScrollMode<enum_ScrollContainer_ScrollMode>`
    **get\_horizontal\_scroll\_mode**()

Controls whether horizontal scrollbar can be used and when it should be
visible. See `ScrollMode<enum_ScrollContainer_ScrollMode>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **scroll\_deadzone** = `0`
`🔗<class_ScrollContainer_property_scroll_deadzone>`

classref-property-setget

-   `void (No return value.)` **set\_deadzone**(value: `int<class_int>`)
-   `int<class_int>` **get\_deadzone**()

Deadzone for touch scrolling. Lower deadzone makes the scrolling more
sensitive.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **scroll\_horizontal** = `0`
`🔗<class_ScrollContainer_property_scroll_horizontal>`

classref-property-setget

-   `void (No return value.)` **set\_h\_scroll**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_h\_scroll**()

The current horizontal scroll value.

\*\*Note:\*\* If you are setting this value in the
`Node._ready<class_Node_private_method__ready>` function or earlier, it
needs to be wrapped with
`Object.set_deferred<class_Object_method_set_deferred>`, since scroll
bar's `Range.max_value<class_Range_property_max_value>` is not
initialized yet.

    func _ready():
        set_deferred("scroll_horizontal", 600)

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **scroll\_horizontal\_custom\_step** = `-1.0`
`🔗<class_ScrollContainer_property_scroll_horizontal_custom_step>`

classref-property-setget

-   `void (No return value.)` **set\_horizontal\_custom\_step**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_horizontal\_custom\_step**()

Overrides the
`ScrollBar.custom_step<class_ScrollBar_property_custom_step>` used when
clicking the internal scroll bar's horizontal increment and decrement
buttons or when using arrow keys when the `ScrollBar<class_ScrollBar>`
is focused.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **scroll\_vertical** = `0`
`🔗<class_ScrollContainer_property_scroll_vertical>`

classref-property-setget

-   `void (No return value.)` **set\_v\_scroll**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_v\_scroll**()

The current vertical scroll value.

\*\*Note:\*\* Setting it early needs to be deferred, just like in
`scroll_horizontal<class_ScrollContainer_property_scroll_horizontal>`.

    func _ready():
        set_deferred("scroll_vertical", 600)

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **scroll\_vertical\_custom\_step** = `-1.0`
`🔗<class_ScrollContainer_property_scroll_vertical_custom_step>`

classref-property-setget

-   `void (No return value.)` **set\_vertical\_custom\_step**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_vertical\_custom\_step**()

Overrides the
`ScrollBar.custom_step<class_ScrollBar_property_custom_step>` used when
clicking the internal scroll bar's vertical increment and decrement
buttons or when using arrow keys when the `ScrollBar<class_ScrollBar>`
is focused.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ScrollMode<enum_ScrollContainer_ScrollMode>` **vertical\_scroll\_mode**
= `1` `🔗<class_ScrollContainer_property_vertical_scroll_mode>`

classref-property-setget

-   `void (No return value.)` **set\_vertical\_scroll\_mode**(value:
    `ScrollMode<enum_ScrollContainer_ScrollMode>`)
-   `ScrollMode<enum_ScrollContainer_ScrollMode>`
    **get\_vertical\_scroll\_mode**()

Controls whether vertical scrollbar can be used and when it should be
visible. See `ScrollMode<enum_ScrollContainer_ScrollMode>` for options.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **ensure\_control\_visible**(control:
`Control<class_Control>`)
`🔗<class_ScrollContainer_method_ensure_control_visible>`

Ensures the given `control` is visible (must be a direct or indirect
child of the ScrollContainer). Used by
`follow_focus<class_ScrollContainer_property_follow_focus>`.

\*\*Note:\*\* This will not work on a node that was just added during
the same frame. If you want to scroll to a newly added child, you must
wait until the next frame using
`SceneTree.process_frame<class_SceneTree_signal_process_frame>`:

    add_child(child_node)
    await get_tree().process_frame
    ensure_control_visible(child_node)

classref-item-separator

------------------------------------------------------------------------

classref-method

`HScrollBar<class_HScrollBar>` **get\_h\_scroll\_bar**()
`🔗<class_ScrollContainer_method_get_h_scroll_bar>`

Returns the horizontal scrollbar `HScrollBar<class_HScrollBar>` of this
**ScrollContainer**.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to disable or hide a scrollbar, you
can use
`horizontal_scroll_mode<class_ScrollContainer_property_horizontal_scroll_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`VScrollBar<class_VScrollBar>` **get\_v\_scroll\_bar**()
`🔗<class_ScrollContainer_method_get_v_scroll_bar>`

Returns the vertical scrollbar `VScrollBar<class_VScrollBar>` of this
**ScrollContainer**.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to disable or hide a scrollbar, you
can use
`vertical_scroll_mode<class_ScrollContainer_property_vertical_scroll_mode>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`StyleBox<class_StyleBox>` **panel**
`🔗<class_ScrollContainer_theme_style_panel>`

The background `StyleBox<class_StyleBox>` of the **ScrollContainer**.
