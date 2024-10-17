github\_url  
hide

# MenuBar

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A horizontal menu bar that creates a menu for each
`PopupMenu<class_PopupMenu>` child.

classref-introduction-group

## Description

A horizontal menu bar that creates a menu for each
`PopupMenu<class_PopupMenu>` child. New items are created by adding
`PopupMenu<class_PopupMenu>`s to this node.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **flat** = `false` `🔗<class_MenuBar_property_flat>`

classref-property-setget

-   `void (No return value.)` **set\_flat**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_flat**()

Flat **MenuBar** don't display item decoration.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **language** = `""`
`🔗<class_MenuBar_property_language>`

classref-property-setget

-   `void (No return value.)` **set\_language**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_language**()

Language code used for line-breaking and text shaping algorithms, if
left empty current locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **prefer\_global\_menu** = `true`
`🔗<class_MenuBar_property_prefer_global_menu>`

classref-property-setget

-   `void (No return value.)` **set\_prefer\_global\_menu**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_prefer\_global\_menu**()

If `true`, **MenuBar** will use system global menu when supported.

\*\*Note:\*\* If `true` and global menu is supported, this node is not
displayed, has zero size, and all its child nodes except
`PopupMenu<class_PopupMenu>`s are inaccessible.

\*\*Note:\*\* This property overrides the value of the
`PopupMenu.prefer_native_menu<class_PopupMenu_property_prefer_native_menu>`
property of the child nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **start\_index** = `-1`
`🔗<class_MenuBar_property_start_index>`

classref-property-setget

-   `void (No return value.)` **set\_start\_index**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_start\_index**()

Position order in the global menu to insert **MenuBar** items at. All
menu items in the **MenuBar** are always inserted as a continuous range.
Menus with lower `start_index<class_MenuBar_property_start_index>` are
inserted first. Menus with
`start_index<class_MenuBar_property_start_index>` equal to `-1` are
inserted last.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **switch\_on\_hover** = `true`
`🔗<class_MenuBar_property_switch_on_hover>`

classref-property-setget

-   `void (No return value.)` **set\_switch\_on\_hover**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_switch\_on\_hover**()

If `true`, when the cursor hovers above menu item, it will close the
current `PopupMenu<class_PopupMenu>` and open the other one.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextDirection<enum_Control_TextDirection>` **text\_direction** = `0`
`🔗<class_MenuBar_property_text_direction>`

classref-property-setget

-   `void (No return value.)` **set\_text\_direction**(value:
    `TextDirection<enum_Control_TextDirection>`)
-   `TextDirection<enum_Control_TextDirection>`
    **get\_text\_direction**()

Base text writing direction.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_menu\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MenuBar_method_get_menu_count>`

Returns number of menu items.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PopupMenu<class_PopupMenu>` **get\_menu\_popup**(menu:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MenuBar_method_get_menu_popup>`

Returns `PopupMenu<class_PopupMenu>` associated with menu item.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_menu\_title**(menu: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MenuBar_method_get_menu_title>`

Returns menu item title.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_menu\_tooltip**(menu: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MenuBar_method_get_menu_tooltip>`

Returns menu item tooltip.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_menu\_disabled**(menu: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MenuBar_method_is_menu_disabled>`

Returns `true`, if menu item is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_menu\_hidden**(menu: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MenuBar_method_is_menu_hidden>`

Returns `true`, if menu item is hidden.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_native\_menu**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_MenuBar_method_is_native_menu>`

Returns `true`, if system global menu is supported and used by this
**MenuBar**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_disable\_shortcuts**(disabled:
`bool<class_bool>`) `🔗<class_MenuBar_method_set_disable_shortcuts>`

If `true`, shortcuts are disabled and cannot be used to trigger the
button.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_menu\_disabled**(menu:
`int<class_int>`, disabled: `bool<class_bool>`)
`🔗<class_MenuBar_method_set_menu_disabled>`

If `true`, menu item is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_menu\_hidden**(menu: `int<class_int>`,
hidden: `bool<class_bool>`) `🔗<class_MenuBar_method_set_menu_hidden>`

If `true`, menu item is hidden.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_menu\_title**(menu: `int<class_int>`,
title: `String<class_String>`) `🔗<class_MenuBar_method_set_menu_title>`

Sets menu item title.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_menu\_tooltip**(menu: `int<class_int>`,
tooltip: `String<class_String>`)
`🔗<class_MenuBar_method_set_menu_tooltip>`

Sets menu item tooltip.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **font\_color** = `Color(0.875, 0.875, 0.875, 1)`
`🔗<class_MenuBar_theme_color_font_color>`

Default text `Color<class_Color>` of the menu item.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_disabled\_color** =
`Color(0.875, 0.875, 0.875, 0.5)`
`🔗<class_MenuBar_theme_color_font_disabled_color>`

Text `Color<class_Color>` used when the menu item is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_focus\_color** =
`Color(0.95, 0.95, 0.95, 1)`
`🔗<class_MenuBar_theme_color_font_focus_color>`

Text `Color<class_Color>` used when the menu item is focused. Only
replaces the normal text color of the menu item. Disabled, hovered, and
pressed states take precedence over this color.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_hover\_color** =
`Color(0.95, 0.95, 0.95, 1)`
`🔗<class_MenuBar_theme_color_font_hover_color>`

Text `Color<class_Color>` used when the menu item is being hovered.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_hover\_pressed\_color** =
`Color(1, 1, 1, 1)`
`🔗<class_MenuBar_theme_color_font_hover_pressed_color>`

Text `Color<class_Color>` used when the menu item is being hovered and
pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_outline\_color** = `Color(0, 0, 0, 1)`
`🔗<class_MenuBar_theme_color_font_outline_color>`

The tint of text outline of the menu item.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_pressed\_color** = `Color(1, 1, 1, 1)`
`🔗<class_MenuBar_theme_color_font_pressed_color>`

Text `Color<class_Color>` used when the menu item is being pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **h\_separation** = `4`
`🔗<class_MenuBar_theme_constant_h_separation>`

The horizontal space between menu items.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **outline\_size** = `0`
`🔗<class_MenuBar_theme_constant_outline_size>`

The size of the text outline.

\*\*Note:\*\* If using a font with
`FontFile.multichannel_signed_distance_field<class_FontFile_property_multichannel_signed_distance_field>`
enabled, its
`FontFile.msdf_pixel_range<class_FontFile_property_msdf_pixel_range>`
must be set to at least *twice* the value of
`outline_size<class_MenuBar_theme_constant_outline_size>` for outline
rendering to look correct. Otherwise, the outline may appear to be cut
off earlier than intended.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **font** `🔗<class_MenuBar_theme_font_font>`

`Font<class_Font>` of the menu item's text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **font\_size**
`🔗<class_MenuBar_theme_font_size_font_size>`

Font size of the menu item's text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **disabled**
`🔗<class_MenuBar_theme_style_disabled>`

`StyleBox<class_StyleBox>` used when the menu item is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **disabled\_mirrored**
`🔗<class_MenuBar_theme_style_disabled_mirrored>`

`StyleBox<class_StyleBox>` used when the menu item is disabled (for
right-to-left layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **hover**
`🔗<class_MenuBar_theme_style_hover>`

`StyleBox<class_StyleBox>` used when the menu item is being hovered.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **hover\_mirrored**
`🔗<class_MenuBar_theme_style_hover_mirrored>`

`StyleBox<class_StyleBox>` used when the menu item is being hovered (for
right-to-left layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **hover\_pressed**
`🔗<class_MenuBar_theme_style_hover_pressed>`

`StyleBox<class_StyleBox>` used when the menu item is being pressed and
hovered at the same time.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **hover\_pressed\_mirrored**
`🔗<class_MenuBar_theme_style_hover_pressed_mirrored>`

`StyleBox<class_StyleBox>` used when the menu item is being pressed and
hovered at the same time (for right-to-left layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **normal**
`🔗<class_MenuBar_theme_style_normal>`

Default `StyleBox<class_StyleBox>` for the menu item.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **normal\_mirrored**
`🔗<class_MenuBar_theme_style_normal_mirrored>`

Default `StyleBox<class_StyleBox>` for the menu item (for right-to-left
layouts).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **pressed**
`🔗<class_MenuBar_theme_style_pressed>`

`StyleBox<class_StyleBox>` used when the menu item is being pressed.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **pressed\_mirrored**
`🔗<class_MenuBar_theme_style_pressed_mirrored>`

`StyleBox<class_StyleBox>` used when the menu item is being pressed (for
right-to-left layouts).
