github\_url  
hide

# TabBar

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A control that provides a horizontal bar with tabs.

classref-introduction-group

## Description

A control that provides a horizontal bar with tabs. Similar to
`TabContainer<class_TabContainer>` but is only in charge of drawing
tabs, not interacting with children.

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

**active\_tab\_rearranged**(idx\_to: `int<class_int>`)
`🔗<class_TabBar_signal_active_tab_rearranged>`

Emitted when the active tab is rearranged via mouse drag. See
`drag_to_rearrange_enabled<class_TabBar_property_drag_to_rearrange_enabled>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tab\_button\_pressed**(tab: `int<class_int>`)
`🔗<class_TabBar_signal_tab_button_pressed>`

Emitted when a tab's right button is pressed. See
`set_tab_button_icon<class_TabBar_method_set_tab_button_icon>`.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tab\_changed**(tab: `int<class_int>`)
`🔗<class_TabBar_signal_tab_changed>`

Emitted when switching to another tab.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tab\_clicked**(tab: `int<class_int>`)
`🔗<class_TabBar_signal_tab_clicked>`

Emitted when a tab is clicked, even if it is the current tab.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tab\_close\_pressed**(tab: `int<class_int>`)
`🔗<class_TabBar_signal_tab_close_pressed>`

Emitted when a tab's close button is pressed.

\*\*Note:\*\* Tabs are not removed automatically once the close button
is pressed, this behavior needs to be programmed manually. For example:

gdscript

$TabBar.tab\_close\_pressed.connect($TabBar.remove\_tab)

csharp

GetNode&lt;TabBar&gt;("TabBar").TabClosePressed +=
GetNode&lt;TabBar&gt;("TabBar").RemoveTab;

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tab\_hovered**(tab: `int<class_int>`)
`🔗<class_TabBar_signal_tab_hovered>`

Emitted when a tab is hovered by the mouse.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tab\_rmb\_clicked**(tab: `int<class_int>`)
`🔗<class_TabBar_signal_tab_rmb_clicked>`

Emitted when a tab is right-clicked.
`select_with_rmb<class_TabBar_property_select_with_rmb>` must be
enabled.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**tab\_selected**(tab: `int<class_int>`)
`🔗<class_TabBar_signal_tab_selected>`

Emitted when a tab is selected via click, directional input, or script,
even if it is the current tab.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **AlignmentMode**: `🔗<enum_TabBar_AlignmentMode>`

classref-enumeration-constant

`AlignmentMode<enum_TabBar_AlignmentMode>` **ALIGNMENT\_LEFT** = `0`

Places tabs to the left.

classref-enumeration-constant

`AlignmentMode<enum_TabBar_AlignmentMode>` **ALIGNMENT\_CENTER** = `1`

Places tabs in the middle.

classref-enumeration-constant

`AlignmentMode<enum_TabBar_AlignmentMode>` **ALIGNMENT\_RIGHT** = `2`

Places tabs to the right.

classref-enumeration-constant

`AlignmentMode<enum_TabBar_AlignmentMode>` **ALIGNMENT\_MAX** = `3`

Represents the size of the `AlignmentMode<enum_TabBar_AlignmentMode>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CloseButtonDisplayPolicy**:
`🔗<enum_TabBar_CloseButtonDisplayPolicy>`

classref-enumeration-constant

`CloseButtonDisplayPolicy<enum_TabBar_CloseButtonDisplayPolicy>`
**CLOSE\_BUTTON\_SHOW\_NEVER** = `0`

Never show the close buttons.

classref-enumeration-constant

`CloseButtonDisplayPolicy<enum_TabBar_CloseButtonDisplayPolicy>`
**CLOSE\_BUTTON\_SHOW\_ACTIVE\_ONLY** = `1`

Only show the close button on the currently active tab.

classref-enumeration-constant

`CloseButtonDisplayPolicy<enum_TabBar_CloseButtonDisplayPolicy>`
**CLOSE\_BUTTON\_SHOW\_ALWAYS** = `2`

Show the close button on all tabs.

classref-enumeration-constant

`CloseButtonDisplayPolicy<enum_TabBar_CloseButtonDisplayPolicy>`
**CLOSE\_BUTTON\_MAX** = `3`

Represents the size of the
`CloseButtonDisplayPolicy<enum_TabBar_CloseButtonDisplayPolicy>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **clip\_tabs** = `true`
`🔗<class_TabBar_property_clip_tabs>`

classref-property-setget

-   `void (No return value.)` **set\_clip\_tabs**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_clip\_tabs**()

If `true`, tabs overflowing this node's width will be hidden, displaying
two navigation buttons instead. Otherwise, this node's minimum size is
updated so that all tabs are visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **current\_tab** = `-1`
`🔗<class_TabBar_property_current_tab>`

classref-property-setget

-   `void (No return value.)` **set\_current\_tab**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_current\_tab**()

The index of the current selected tab. A value of `-1` means that no tab
is selected and can only be set when
`deselect_enabled<class_TabBar_property_deselect_enabled>` is `true` or
if all tabs are hidden or disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **deselect\_enabled** = `false`
`🔗<class_TabBar_property_deselect_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_deselect\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_deselect\_enabled**()

If `true`, all tabs can be deselected so that no tab is selected. Click
on the current tab to deselect it.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **drag\_to\_rearrange\_enabled** = `false`
`🔗<class_TabBar_property_drag_to_rearrange_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_drag\_to\_rearrange\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_drag\_to\_rearrange\_enabled**()

If `true`, tabs can be rearranged with mouse drag.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_tab\_width** = `0`
`🔗<class_TabBar_property_max_tab_width>`

classref-property-setget

-   `void (No return value.)` **set\_max\_tab\_width**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_max\_tab\_width**()

Sets the maximum width which all tabs should be limited to. Unlimited if
set to `0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **scroll\_to\_selected** = `true`
`🔗<class_TabBar_property_scroll_to_selected>`

classref-property-setget

-   `void (No return value.)` **set\_scroll\_to\_selected**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_scroll\_to\_selected**()

If `true`, the tab offset will be changed to keep the currently selected
tab visible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **scrolling\_enabled** = `true`
`🔗<class_TabBar_property_scrolling_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_scrolling\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_scrolling\_enabled**()

if `true`, the mouse's scroll wheel can be used to navigate the scroll
view.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **select\_with\_rmb** = `false`
`🔗<class_TabBar_property_select_with_rmb>`

classref-property-setget

-   `void (No return value.)` **set\_select\_with\_rmb**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_select\_with\_rmb**()

If `true`, enables selecting a tab with the right mouse button.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AlignmentMode<enum_TabBar_AlignmentMode>` **tab\_alignment** = `0`
`🔗<class_TabBar_property_tab_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_tab\_alignment**(value:
    `AlignmentMode<enum_TabBar_AlignmentMode>`)
-   `AlignmentMode<enum_TabBar_AlignmentMode>` **get\_tab\_alignment**()

Sets the position at which tabs will be placed. See
`AlignmentMode<enum_TabBar_AlignmentMode>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CloseButtonDisplayPolicy<enum_TabBar_CloseButtonDisplayPolicy>`
**tab\_close\_display\_policy** = `0`
`🔗<class_TabBar_property_tab_close_display_policy>`

classref-property-setget

-   `void (No return value.)`
    **set\_tab\_close\_display\_policy**(value:
    `CloseButtonDisplayPolicy<enum_TabBar_CloseButtonDisplayPolicy>`)
-   `CloseButtonDisplayPolicy<enum_TabBar_CloseButtonDisplayPolicy>`
    **get\_tab\_close\_display\_policy**()

Sets when the close button will appear on the tabs. See
`CloseButtonDisplayPolicy<enum_TabBar_CloseButtonDisplayPolicy>` for
details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **tab\_count** = `0`
`🔗<class_TabBar_property_tab_count>`

classref-property-setget

-   `void (No return value.)` **set\_tab\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_tab\_count**()

The number of tabs currently in the bar.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **tabs\_rearrange\_group** = `-1`
`🔗<class_TabBar_property_tabs_rearrange_group>`

classref-property-setget

-   `void (No return value.)` **set\_tabs\_rearrange\_group**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_tabs\_rearrange\_group**()

**TabBar**s with the same rearrange group ID will allow dragging the
tabs between them. Enable drag with
`drag_to_rearrange_enabled<class_TabBar_property_drag_to_rearrange_enabled>`.

Setting this to `-1` will disable rearranging between **TabBar**s.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_tab**(title: `String<class_String>` =
"", icon: `Texture2D<class_Texture2D>` = null)
`🔗<class_TabBar_method_add_tab>`

Adds a new tab.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_tabs**()
`🔗<class_TabBar_method_clear_tabs>`

Clears all tabs.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **ensure\_tab\_visible**(idx:
`int<class_int>`) `🔗<class_TabBar_method_ensure_tab_visible>`

Moves the scroll view to make the tab visible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_offset\_buttons\_visible**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_offset_buttons_visible>`

Returns `true` if the offset buttons (the ones that appear when there's
not enough space for all tabs) are visible.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_previous\_tab**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_previous_tab>`

Returns the previously active tab index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_tab\_button\_icon**(tab\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_tab_button_icon>`

Returns the icon for the right button of the tab at index `tab_idx` or
`null` if the right button has no icon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_tab\_icon**(tab\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_tab_icon>`

Returns the icon for the tab at index `tab_idx` or `null` if the tab has
no icon.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_tab\_icon\_max\_width**(tab\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_tab_icon_max_width>`

Returns the maximum allowed width of the icon for the tab at index
`tab_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_tab\_idx\_at\_point**(point:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_tab_idx_at_point>`

Returns the index of the tab at local coordinates `point`. Returns `-1`
if the point is outside the control boundaries or if there's no tab at
the queried position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_tab\_language**(tab\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_tab_language>`

Returns tab title language code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_tab\_metadata**(tab\_idx:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_tab_metadata>`

Returns the metadata value set to the tab at index `tab_idx` using
`set_tab_metadata<class_TabBar_method_set_tab_metadata>`. If no metadata
was previously set, returns `null` by default.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_tab\_offset**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_tab_offset>`

Returns the number of hidden tabs offsetted to the left.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Rect2<class_Rect2>` **get\_tab\_rect**(tab\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_tab_rect>`

Returns tab `Rect2<class_Rect2>` with local position and size.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TextDirection<enum_Control_TextDirection>`
**get\_tab\_text\_direction**(tab\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_tab_text_direction>`

Returns tab title text base writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_tab\_title**(tab\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_tab_title>`

Returns the title of the tab at index `tab_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_tab\_tooltip**(tab\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_get_tab_tooltip>`

Returns the tooltip text of the tab at index `tab_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_tab\_disabled**(tab\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_is_tab_disabled>`

Returns `true` if the tab at index `tab_idx` is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_tab\_hidden**(tab\_idx: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TabBar_method_is_tab_hidden>`

Returns `true` if the tab at index `tab_idx` is hidden.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **move\_tab**(from: `int<class_int>`, to:
`int<class_int>`) `🔗<class_TabBar_method_move_tab>`

Moves a tab from `from` to `to`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_tab**(tab\_idx: `int<class_int>`)
`🔗<class_TabBar_method_remove_tab>`

Removes the tab at index `tab_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **select\_next\_available**()
`🔗<class_TabBar_method_select_next_available>`

Selects the first available tab with greater index than the currently
selected. Returns `true` if tab selection changed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **select\_previous\_available**()
`🔗<class_TabBar_method_select_previous_available>`

Selects the first available tab with lower index than the currently
selected. Returns `true` if tab selection changed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tab\_button\_icon**(tab\_idx:
`int<class_int>`, icon: `Texture2D<class_Texture2D>`)
`🔗<class_TabBar_method_set_tab_button_icon>`

Sets an `icon` for the button of the tab at index `tab_idx` (located to
the right, before the close button), making it visible and clickable
(See `tab_button_pressed<class_TabBar_signal_tab_button_pressed>`).
Giving it a `null` value will hide the button.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tab\_disabled**(tab\_idx:
`int<class_int>`, disabled: `bool<class_bool>`)
`🔗<class_TabBar_method_set_tab_disabled>`

If `disabled` is `true`, disables the tab at index `tab_idx`, making it
non-interactable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tab\_hidden**(tab\_idx:
`int<class_int>`, hidden: `bool<class_bool>`)
`🔗<class_TabBar_method_set_tab_hidden>`

If `hidden` is `true`, hides the tab at index `tab_idx`, making it
disappear from the tab area.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tab\_icon**(tab\_idx: `int<class_int>`,
icon: `Texture2D<class_Texture2D>`)
`🔗<class_TabBar_method_set_tab_icon>`

Sets an `icon` for the tab at index `tab_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tab\_icon\_max\_width**(tab\_idx:
`int<class_int>`, width: `int<class_int>`)
`🔗<class_TabBar_method_set_tab_icon_max_width>`

Sets the maximum allowed width of the icon for the tab at index
`tab_idx`. This limit is applied on top of the default size of the icon
and on top of
`icon_max_width<class_TabBar_theme_constant_icon_max_width>`. The height
is adjusted according to the icon's ratio.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tab\_language**(tab\_idx:
`int<class_int>`, language: `String<class_String>`)
`🔗<class_TabBar_method_set_tab_language>`

Sets language code of tab title used for line-breaking and text shaping
algorithms, if left empty current locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tab\_metadata**(tab\_idx:
`int<class_int>`, metadata: `Variant<class_Variant>`)
`🔗<class_TabBar_method_set_tab_metadata>`

Sets the metadata value for the tab at index `tab_idx`, which can be
retrieved later using
`get_tab_metadata<class_TabBar_method_get_tab_metadata>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tab\_text\_direction**(tab\_idx:
`int<class_int>`, direction:
`TextDirection<enum_Control_TextDirection>`)
`🔗<class_TabBar_method_set_tab_text_direction>`

Sets tab title base writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tab\_title**(tab\_idx:
`int<class_int>`, title: `String<class_String>`)
`🔗<class_TabBar_method_set_tab_title>`

Sets a `title` for the tab at index `tab_idx`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_tab\_tooltip**(tab\_idx:
`int<class_int>`, tooltip: `String<class_String>`)
`🔗<class_TabBar_method_set_tab_tooltip>`

Sets a `tooltip` for tab at index `tab_idx`.

\*\*Note:\*\* By default, if the `tooltip` is empty and the tab text is
truncated (not all characters fit into the tab), the title will be
displayed as a tooltip. To hide the tooltip, assign `" "` as the
`tooltip` text.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **drop\_mark\_color** = `Color(1, 1, 1, 1)`
`🔗<class_TabBar_theme_color_drop_mark_color>`

Modulation color for the `drop_mark<class_TabBar_theme_icon_drop_mark>`
icon.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_disabled\_color** =
`Color(0.875, 0.875, 0.875, 0.5)`
`🔗<class_TabBar_theme_color_font_disabled_color>`

Font color of disabled tabs.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_hovered\_color** =
`Color(0.95, 0.95, 0.95, 1)`
`🔗<class_TabBar_theme_color_font_hovered_color>`

Font color of the currently hovered tab. Does not apply to the selected
tab.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_outline\_color** = `Color(0, 0, 0, 1)`
`🔗<class_TabBar_theme_color_font_outline_color>`

The tint of text outline of the tab name.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_selected\_color** =
`Color(0.95, 0.95, 0.95, 1)`
`🔗<class_TabBar_theme_color_font_selected_color>`

Font color of the currently selected tab.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_unselected\_color** =
`Color(0.7, 0.7, 0.7, 1)`
`🔗<class_TabBar_theme_color_font_unselected_color>`

Font color of the other, unselected tabs.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **h\_separation** = `4`
`🔗<class_TabBar_theme_constant_h_separation>`

The horizontal separation between the elements inside tabs.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **icon\_max\_width** = `0`
`🔗<class_TabBar_theme_constant_icon_max_width>`

The maximum allowed width of the tab's icon. This limit is applied on
top of the default size of the icon, but before the value set with
`set_tab_icon_max_width<class_TabBar_method_set_tab_icon_max_width>`.
The height is adjusted according to the icon's ratio.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **outline\_size** = `0`
`🔗<class_TabBar_theme_constant_outline_size>`

The size of the tab text outline.

\*\*Note:\*\* If using a font with
`FontFile.multichannel_signed_distance_field<class_FontFile_property_multichannel_signed_distance_field>`
enabled, its
`FontFile.msdf_pixel_range<class_FontFile_property_msdf_pixel_range>`
must be set to at least *twice* the value of
`outline_size<class_TabBar_theme_constant_outline_size>` for outline
rendering to look correct. Otherwise, the outline may appear to be cut
off earlier than intended.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **font** `🔗<class_TabBar_theme_font_font>`

The font used to draw tab names.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **font\_size**
`🔗<class_TabBar_theme_font_size_font_size>`

Font size of the tab names.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **close**
`🔗<class_TabBar_theme_icon_close>`

The icon for the close button (see
`tab_close_display_policy<class_TabBar_property_tab_close_display_policy>`).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **decrement**
`🔗<class_TabBar_theme_icon_decrement>`

Icon for the left arrow button that appears when there are too many tabs
to fit in the container width. When the button is disabled (i.e. the
first tab is visible), it appears semi-transparent.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **decrement\_highlight**
`🔗<class_TabBar_theme_icon_decrement_highlight>`

Icon for the left arrow button that appears when there are too many tabs
to fit in the container width. Used when the button is being hovered
with the cursor.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **drop\_mark**
`🔗<class_TabBar_theme_icon_drop_mark>`

Icon shown to indicate where a dragged tab is gonna be dropped (see
`drag_to_rearrange_enabled<class_TabBar_property_drag_to_rearrange_enabled>`).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **increment**
`🔗<class_TabBar_theme_icon_increment>`

Icon for the right arrow button that appears when there are too many
tabs to fit in the container width. When the button is disabled (i.e.
the last tab is visible) it appears semi-transparent.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **increment\_highlight**
`🔗<class_TabBar_theme_icon_increment_highlight>`

Icon for the right arrow button that appears when there are too many
tabs to fit in the container width. Used when the button is being
hovered with the cursor.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **button\_highlight**
`🔗<class_TabBar_theme_style_button_highlight>`

Background of the tab and close buttons when they're being hovered with
the cursor.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **button\_pressed**
`🔗<class_TabBar_theme_style_button_pressed>`

Background of the tab and close buttons when it's being pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **tab\_disabled**
`🔗<class_TabBar_theme_style_tab_disabled>`

The style of disabled tabs.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **tab\_focus**
`🔗<class_TabBar_theme_style_tab_focus>`

`StyleBox<class_StyleBox>` used when the **TabBar** is focused. The
`tab_focus<class_TabBar_theme_style_tab_focus>`
`StyleBox<class_StyleBox>` is displayed *over* the base
`StyleBox<class_StyleBox>` of the selected tab, so a partially
transparent `StyleBox<class_StyleBox>` should be used to ensure the base
`StyleBox<class_StyleBox>` remains visible. A `StyleBox<class_StyleBox>`
that represents an outline or an underline works well for this purpose.
To disable the focus visual effect, assign a
`StyleBoxEmpty<class_StyleBoxEmpty>` resource. Note that disabling the
focus visual effect will harm keyboard/controller navigation usability,
so this is not recommended for accessibility reasons.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **tab\_hovered**
`🔗<class_TabBar_theme_style_tab_hovered>`

The style of the currently hovered tab. Does not apply to the selected
tab.

\*\*Note:\*\* This style will be drawn with the same width as
`tab_unselected<class_TabBar_theme_style_tab_unselected>` at minimum.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **tab\_selected**
`🔗<class_TabBar_theme_style_tab_selected>`

The style of the currently selected tab.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **tab\_unselected**
`🔗<class_TabBar_theme_style_tab_unselected>`

The style of the other, unselected tabs.
