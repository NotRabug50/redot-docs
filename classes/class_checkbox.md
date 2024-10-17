github\_url  
hide

# CheckBox

**Inherits:** `Button<class_Button>` **&lt;**
`BaseButton<class_BaseButton>` **&lt;** `Control<class_Control>`
**&lt;** `CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>`
**&lt;** `Object<class_Object>`

A button that represents a binary choice.

classref-introduction-group

## Description

**CheckBox** allows the user to choose one of only two possible options.
It's similar to `CheckButton<class_CheckButton>` in functionality, but
it has a different appearance. To follow established UX patterns, it's
recommended to use **CheckBox** when toggling it has **no** immediate
effect on something. For example, it could be used when toggling it will
only do something once a confirmation button is pressed.

See also `BaseButton<class_BaseButton>` which contains common properties
and methods associated with this node.

When `BaseButton.button_group<class_BaseButton_property_button_group>`
specifies a `ButtonGroup<class_ButtonGroup>`, **CheckBox** changes its
appearance to that of a radio button and uses the various `radio_*`
theme properties.

classref-reftable-group

## Properties

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

`int<class_int>` **check\_v\_offset** = `0`
`🔗<class_CheckBox_theme_constant_check_v_offset>`

The vertical offset used when rendering the check icons (in pixels).

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **checked**
`🔗<class_CheckBox_theme_icon_checked>`

The check icon to display when the **CheckBox** is checked.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **checked\_disabled**
`🔗<class_CheckBox_theme_icon_checked_disabled>`

The check icon to display when the **CheckBox** is checked and is
disabled.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **radio\_checked**
`🔗<class_CheckBox_theme_icon_radio_checked>`

The check icon to display when the **CheckBox** is configured as a radio
button and is checked.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **radio\_checked\_disabled**
`🔗<class_CheckBox_theme_icon_radio_checked_disabled>`

The check icon to display when the **CheckBox** is configured as a radio
button, is disabled, and is unchecked.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **radio\_unchecked**
`🔗<class_CheckBox_theme_icon_radio_unchecked>`

The check icon to display when the **CheckBox** is configured as a radio
button and is unchecked.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **radio\_unchecked\_disabled**
`🔗<class_CheckBox_theme_icon_radio_unchecked_disabled>`

The check icon to display when the **CheckBox** is configured as a radio
button, is disabled, and is unchecked.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **unchecked**
`🔗<class_CheckBox_theme_icon_unchecked>`

The check icon to display when the **CheckBox** is unchecked.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Texture2D<class_Texture2D>` **unchecked\_disabled**
`🔗<class_CheckBox_theme_icon_unchecked_disabled>`

The check icon to display when the **CheckBox** is unchecked and is
disabled.
