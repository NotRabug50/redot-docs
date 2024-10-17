github\_url  
hide

# StyleBox

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `StyleBoxEmpty<class_StyleBoxEmpty>`,
`StyleBoxFlat<class_StyleBoxFlat>`, `StyleBoxLine<class_StyleBoxLine>`,
`StyleBoxTexture<class_StyleBoxTexture>`

Abstract base class for defining stylized boxes for UI elements.

classref-introduction-group

## Description

**StyleBox** is an abstract base class for drawing stylized boxes for UI
elements. It is used for panels, buttons, `LineEdit<class_LineEdit>`
backgrounds, `Tree<class_Tree>` backgrounds, etc. and also for testing a
transparency mask for pointer signals. If mask test fails on a
**StyleBox** assigned as mask to a control, clicks and motion signals
will go through it to the one below.

\*\*Note:\*\* For control nodes that have *Theme Properties*, the
`focus` **StyleBox** is displayed over the `normal`, `hover` or
`pressed` **StyleBox**. This makes the `focus` **StyleBox** more
reusable across different nodes.

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

`float<class_float>` **content\_margin\_bottom** = `-1.0`
`🔗<class_StyleBox_property_content_margin_bottom>`

classref-property-setget

-   `void (No return value.)` **set\_content\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, offset: `float<class_float>`)
-   `float<class_float>` **get\_content\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The bottom margin for the contents of this style box. Increasing this
value reduces the space available to the contents from the bottom.

If this value is negative, it is ignored and a child-specific margin is
used instead. For example, for `StyleBoxFlat<class_StyleBoxFlat>`, the
border thickness (if any) is used instead.

It is up to the code using this style box to decide what these contents
are: for example, a `Button<class_Button>` respects this content margin
for the textual contents of the button.

`get_margin<class_StyleBox_method_get_margin>` should be used to fetch
this value as consumer instead of reading these properties directly.
This is because it correctly respects negative values and the fallback
mentioned above.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **content\_margin\_left** = `-1.0`
`🔗<class_StyleBox_property_content_margin_left>`

classref-property-setget

-   `void (No return value.)` **set\_content\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, offset: `float<class_float>`)
-   `float<class_float>` **get\_content\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The left margin for the contents of this style box. Increasing this
value reduces the space available to the contents from the left.

Refer to
`content_margin_bottom<class_StyleBox_property_content_margin_bottom>`
for extra considerations.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **content\_margin\_right** = `-1.0`
`🔗<class_StyleBox_property_content_margin_right>`

classref-property-setget

-   `void (No return value.)` **set\_content\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, offset: `float<class_float>`)
-   `float<class_float>` **get\_content\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The right margin for the contents of this style box. Increasing this
value reduces the space available to the contents from the right.

Refer to
`content_margin_bottom<class_StyleBox_property_content_margin_bottom>`
for extra considerations.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **content\_margin\_top** = `-1.0`
`🔗<class_StyleBox_property_content_margin_top>`

classref-property-setget

-   `void (No return value.)` **set\_content\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`, offset: `float<class_float>`)
-   `float<class_float>` **get\_content\_margin**(margin:
    `Side<enum_@GlobalScope_Side>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The top margin for the contents of this style box. Increasing this value
reduces the space available to the contents from the top.

Refer to
`content_margin_bottom<class_StyleBox_property_content_margin_bottom>`
for extra considerations.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_draw**(to\_canvas\_item: `RID<class_RID>`,
rect: `Rect2<class_Rect2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBox_private_method__draw>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **\_get\_draw\_rect**(rect: `Rect2<class_Rect2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBox_private_method__get_draw_rect>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **\_get\_minimum\_size**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBox_private_method__get_minimum_size>`

Virtual method to be implemented by the user. Returns a custom minimum
size that the stylebox must respect when drawing. By default
`get_minimum_size<class_StyleBox_method_get_minimum_size>` only takes
content margins into account. This method can be overridden to add
another size restriction. A combination of the default behavior and the
output of this method will be used, to account for both sizes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_test\_mask**(point: `Vector2<class_Vector2>`,
rect: `Rect2<class_Rect2>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBox_private_method__test_mask>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **draw**(canvas\_item: `RID<class_RID>`, rect:
`Rect2<class_Rect2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBox_method_draw>`

Draws this stylebox using a canvas item identified by the given
`RID<class_RID>`.

The `RID<class_RID>` value can either be the result of
`CanvasItem.get_canvas_item<class_CanvasItem_method_get_canvas_item>`
called on an existing `CanvasItem<class_CanvasItem>`-derived node, or
directly from creating a canvas item in the
`RenderingServer<class_RenderingServer>` with
`RenderingServer.canvas_item_create<class_RenderingServer_method_canvas_item_create>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_content\_margin**(margin:
`Side<enum_@GlobalScope_Side>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBox_method_get_content_margin>`

Returns the default margin of the specified
`Side<enum_@GlobalScope_Side>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CanvasItem<class_CanvasItem>` **get\_current\_item\_drawn**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBox_method_get_current_item_drawn>`

Returns the `CanvasItem<class_CanvasItem>` that handles its
`CanvasItem.NOTIFICATION_DRAW<class_CanvasItem_constant_NOTIFICATION_DRAW>`
or `CanvasItem._draw<class_CanvasItem_private_method__draw>` callback at
this moment.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_margin**(margin:
`Side<enum_@GlobalScope_Side>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBox_method_get_margin>`

Returns the content margin offset for the specified
`Side<enum_@GlobalScope_Side>`.

Positive values reduce size inwards, unlike `Control<class_Control>`'s
margin values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_minimum\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBox_method_get_minimum_size>`

Returns the minimum size that this stylebox can be shrunk to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_offset**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBox_method_get_offset>`

Returns the "offset" of a stylebox. This helper function returns a value
equivalent to
`Vector2(style.get_margin(MARGIN_LEFT), style.get_margin(MARGIN_TOP))`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_content\_margin**(margin:
`Side<enum_@GlobalScope_Side>`, offset: `float<class_float>`)
`🔗<class_StyleBox_method_set_content_margin>`

Sets the default value of the specified `Side<enum_@GlobalScope_Side>`
to `offset` pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_content\_margin\_all**(offset:
`float<class_float>`) `🔗<class_StyleBox_method_set_content_margin_all>`

Sets the default margin to `offset` pixels for all sides.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **test\_mask**(point: `Vector2<class_Vector2>`, rect:
`Rect2<class_Rect2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StyleBox_method_test_mask>`

Test a position in a rectangle, return whether it passes the mask test.
