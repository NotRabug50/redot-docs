github\_url  
hide

# ThemeDB

**Inherits:** `Object<class_Object>`

A singleton that provides access to static information about
`Theme<class_Theme>` resources used by the engine and by your project.

classref-introduction-group

## Description

This singleton provides access to static information about
`Theme<class_Theme>` resources used by the engine and by your projects.
You can fetch the default engine theme, as well as your project
configured theme.

\*\*ThemeDB\*\* also contains fallback values for theme properties.

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**fallback\_changed**() `🔗<class_ThemeDB_signal_fallback_changed>`

Emitted when one of the fallback values had been changed. Use it to
refresh the look of controls that may rely on the fallback theme items.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **fallback\_base\_scale** = `1.0`
`🔗<class_ThemeDB_property_fallback_base_scale>`

classref-property-setget

-   `void (No return value.)` **set\_fallback\_base\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_fallback\_base\_scale**()

The fallback base scale factor of every `Control<class_Control>` node
and `Theme<class_Theme>` resource. Used when no other value is available
to the control.

See also
`Theme.default_base_scale<class_Theme_property_default_base_scale>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Font<class_Font>` **fallback\_font**
`🔗<class_ThemeDB_property_fallback_font>`

classref-property-setget

-   `void (No return value.)` **set\_fallback\_font**(value:
    `Font<class_Font>`)
-   `Font<class_Font>` **get\_fallback\_font**()

The fallback font of every `Control<class_Control>` node and
`Theme<class_Theme>` resource. Used when no other value is available to
the control.

See also `Theme.default_font<class_Theme_property_default_font>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **fallback\_font\_size** = `16`
`🔗<class_ThemeDB_property_fallback_font_size>`

classref-property-setget

-   `void (No return value.)` **set\_fallback\_font\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_fallback\_font\_size**()

The fallback font size of every `Control<class_Control>` node and
`Theme<class_Theme>` resource. Used when no other value is available to
the control.

See also
`Theme.default_font_size<class_Theme_property_default_font_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **fallback\_icon**
`🔗<class_ThemeDB_property_fallback_icon>`

classref-property-setget

-   `void (No return value.)` **set\_fallback\_icon**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_fallback\_icon**()

The fallback icon of every `Control<class_Control>` node and
`Theme<class_Theme>` resource. Used when no other value is available to
the control.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StyleBox<class_StyleBox>` **fallback\_stylebox**
`🔗<class_ThemeDB_property_fallback_stylebox>`

classref-property-setget

-   `void (No return value.)` **set\_fallback\_stylebox**(value:
    `StyleBox<class_StyleBox>`)
-   `StyleBox<class_StyleBox>` **get\_fallback\_stylebox**()

The fallback stylebox of every `Control<class_Control>` node and
`Theme<class_Theme>` resource. Used when no other value is available to
the control.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Theme<class_Theme>` **get\_default\_theme**()
`🔗<class_ThemeDB_method_get_default_theme>`

Returns a reference to the default engine `Theme<class_Theme>`. This
theme resource is responsible for the out-of-the-box look of
`Control<class_Control>` nodes and cannot be overridden.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Theme<class_Theme>` **get\_project\_theme**()
`🔗<class_ThemeDB_method_get_project_theme>`

Returns a reference to the custom project `Theme<class_Theme>`. This
theme resources allows to override the default engine theme for every
control node in the project.

To set the project theme, see
`ProjectSettings.gui/theme/custom<class_ProjectSettings_property_gui/theme/custom>`.
