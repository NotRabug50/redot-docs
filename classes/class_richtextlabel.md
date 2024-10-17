github\_url  
hide

# RichTextLabel

**Inherits:** `Control<class_Control>` **&lt;**
`CanvasItem<class_CanvasItem>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A control for displaying text that can contain different font styles,
images, and basic formatting.

classref-introduction-group

## Description

A control for displaying text that can contain custom fonts, images, and
basic formatting. **RichTextLabel** manages these as an internal tag
stack. It also adapts itself to given width/heights.

\*\*Note:\*\* Assignments to `text<class_RichTextLabel_property_text>`
clear the tag stack and reconstruct it from the property's contents. Any
edits made to `text<class_RichTextLabel_property_text>` will erase
previous edits made from other manual sources such as
`append_text<class_RichTextLabel_method_append_text>` and the `push_*` /
`pop<class_RichTextLabel_method_pop>` methods.

\*\*Note:\*\* RichTextLabel doesn't support entangled BBCode tags. For
example, instead of using `[b]bold[i]bold italic[/b]italic[/i]`, use
`[b]bold[i]bold italic[/i][/b][i]italic[/i]`.

\*\*Note:\*\* `push_*/pop_*` functions won't affect BBCode.

\*\*Note:\*\* Unlike `Label<class_Label>`, **RichTextLabel** doesn't
have a *property* to horizontally align text to the center. Instead,
enable `bbcode_enabled<class_RichTextLabel_property_bbcode_enabled>` and
surround the text in a `[center]` tag as follows:
`[center]Example[/center]`. There is currently no built-in way to
vertically align text either, but this can be emulated by relying on
anchors/containers and the
`fit_content<class_RichTextLabel_property_fit_content>` property.

classref-introduction-group

## Tutorials

-   `BBCode in RichTextLabel <../tutorials/ui/bbcode_in_richtextlabel>`
-   [Rich Text Label with BBCode
    Demo](https://godotengine.org/asset-library/asset/2774)
-   [Operating System Testing
    Demo](https://godotengine.org/asset-library/asset/2789)

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

**finished**() `🔗<class_RichTextLabel_signal_finished>`

Triggered when the document is fully loaded.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**meta\_clicked**(meta: `Variant<class_Variant>`)
`🔗<class_RichTextLabel_signal_meta_clicked>`

Triggered when the user clicks on content between meta (URL) tags. If
the meta is defined in BBCode, e.g. `[url={"key": "value"}]Text[/url]`,
then the parameter for this signal will always be a
`String<class_String>` type. If a particular type or an object is
desired, the `push_meta<class_RichTextLabel_method_push_meta>` method
must be used to manually insert the data into the tag stack.
Alternatively, you can convert the `String<class_String>` input to the
desired type based on its contents (such as calling
`JSON.parse<class_JSON_method_parse>` on it).

For example, the following method can be connected to
`meta_clicked<class_RichTextLabel_signal_meta_clicked>` to open clicked
URLs using the user's default web browser:

gdscript

\# This assumes RichTextLabel's
<span class="title-ref">meta\_clicked</span> signal was connected to \#
the function below using the signal connection dialog. func
\_richtextlabel\_on\_meta\_clicked(meta): \#
<span class="title-ref">meta</span> is of Variant type, so convert it to
a String to avoid script errors at run-time. OS.shell\_open(str(meta))

classref-item-separator

------------------------------------------------------------------------

classref-signal

**meta\_hover\_ended**(meta: `Variant<class_Variant>`)
`🔗<class_RichTextLabel_signal_meta_hover_ended>`

Triggers when the mouse exits a meta tag.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**meta\_hover\_started**(meta: `Variant<class_Variant>`)
`🔗<class_RichTextLabel_signal_meta_hover_started>`

Triggers when the mouse enters a meta tag.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ListType**: `🔗<enum_RichTextLabel_ListType>`

classref-enumeration-constant

`ListType<enum_RichTextLabel_ListType>` **LIST\_NUMBERS** = `0`

Each list item has a number marker.

classref-enumeration-constant

`ListType<enum_RichTextLabel_ListType>` **LIST\_LETTERS** = `1`

Each list item has a letter marker.

classref-enumeration-constant

`ListType<enum_RichTextLabel_ListType>` **LIST\_ROMAN** = `2`

Each list item has a roman number marker.

classref-enumeration-constant

`ListType<enum_RichTextLabel_ListType>` **LIST\_DOTS** = `3`

Each list item has a filled circle marker.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **MenuItems**: `🔗<enum_RichTextLabel_MenuItems>`

classref-enumeration-constant

`MenuItems<enum_RichTextLabel_MenuItems>` **MENU\_COPY** = `0`

Copies the selected text.

classref-enumeration-constant

`MenuItems<enum_RichTextLabel_MenuItems>` **MENU\_SELECT\_ALL** = `1`

Selects the whole **RichTextLabel** text.

classref-enumeration-constant

`MenuItems<enum_RichTextLabel_MenuItems>` **MENU\_MAX** = `2`

Represents the size of the `MenuItems<enum_RichTextLabel_MenuItems>`
enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **MetaUnderline**: `🔗<enum_RichTextLabel_MetaUnderline>`

classref-enumeration-constant

`MetaUnderline<enum_RichTextLabel_MetaUnderline>`
**META\_UNDERLINE\_NEVER** = `0`

Meta tag does not display an underline, even if
`meta_underlined<class_RichTextLabel_property_meta_underlined>` is
`true`.

classref-enumeration-constant

`MetaUnderline<enum_RichTextLabel_MetaUnderline>`
**META\_UNDERLINE\_ALWAYS** = `1`

If `meta_underlined<class_RichTextLabel_property_meta_underlined>` is
`true`, meta tag always display an underline.

classref-enumeration-constant

`MetaUnderline<enum_RichTextLabel_MetaUnderline>`
**META\_UNDERLINE\_ON\_HOVER** = `2`

If `meta_underlined<class_RichTextLabel_property_meta_underlined>` is
`true`, meta tag display an underline when the mouse cursor is over it.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

flags **ImageUpdateMask**: `🔗<enum_RichTextLabel_ImageUpdateMask>`

classref-enumeration-constant

`ImageUpdateMask<enum_RichTextLabel_ImageUpdateMask>`
**UPDATE\_TEXTURE** = `1`

If this bit is set,
`update_image<class_RichTextLabel_method_update_image>` changes image
texture.

classref-enumeration-constant

`ImageUpdateMask<enum_RichTextLabel_ImageUpdateMask>` **UPDATE\_SIZE** =
`2`

If this bit is set,
`update_image<class_RichTextLabel_method_update_image>` changes image
size.

classref-enumeration-constant

`ImageUpdateMask<enum_RichTextLabel_ImageUpdateMask>` **UPDATE\_COLOR**
= `4`

If this bit is set,
`update_image<class_RichTextLabel_method_update_image>` changes image
color.

classref-enumeration-constant

`ImageUpdateMask<enum_RichTextLabel_ImageUpdateMask>`
**UPDATE\_ALIGNMENT** = `8`

If this bit is set,
`update_image<class_RichTextLabel_method_update_image>` changes image
inline alignment.

classref-enumeration-constant

`ImageUpdateMask<enum_RichTextLabel_ImageUpdateMask>` **UPDATE\_REGION**
= `16`

If this bit is set,
`update_image<class_RichTextLabel_method_update_image>` changes image
texture region.

classref-enumeration-constant

`ImageUpdateMask<enum_RichTextLabel_ImageUpdateMask>` **UPDATE\_PAD** =
`32`

If this bit is set,
`update_image<class_RichTextLabel_method_update_image>` changes image
padding.

classref-enumeration-constant

`ImageUpdateMask<enum_RichTextLabel_ImageUpdateMask>`
**UPDATE\_TOOLTIP** = `64`

If this bit is set,
`update_image<class_RichTextLabel_method_update_image>` changes image
tooltip.

classref-enumeration-constant

`ImageUpdateMask<enum_RichTextLabel_ImageUpdateMask>`
**UPDATE\_WIDTH\_IN\_PERCENT** = `128`

If this bit is set,
`update_image<class_RichTextLabel_method_update_image>` changes image
width from/to percents.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`AutowrapMode<enum_TextServer_AutowrapMode>` **autowrap\_mode** = `3`
`🔗<class_RichTextLabel_property_autowrap_mode>`

classref-property-setget

-   `void (No return value.)` **set\_autowrap\_mode**(value:
    `AutowrapMode<enum_TextServer_AutowrapMode>`)
-   `AutowrapMode<enum_TextServer_AutowrapMode>`
    **get\_autowrap\_mode**()

If set to something other than
`TextServer.AUTOWRAP_OFF<class_TextServer_constant_AUTOWRAP_OFF>`, the
text gets wrapped inside the node's bounding rectangle. To see how each
mode behaves, see `AutowrapMode<enum_TextServer_AutowrapMode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **bbcode\_enabled** = `false`
`🔗<class_RichTextLabel_property_bbcode_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_use\_bbcode**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_bbcode**()

If `true`, the label uses BBCode formatting.

\*\*Note:\*\* This only affects the contents of
`text<class_RichTextLabel_property_text>`, not the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **context\_menu\_enabled** = `false`
`🔗<class_RichTextLabel_property_context_menu_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_context\_menu\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_context\_menu\_enabled**()

If `true`, a right-click displays the context menu.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>` **custom\_effects** = `[]`
`🔗<class_RichTextLabel_property_custom_effects>`

classref-property-setget

-   `void (No return value.)` **set\_effects**(value:
    `Array<class_Array>`)
-   `Array<class_Array>` **get\_effects**()

The currently installed custom effects. This is an array of
`RichTextEffect<class_RichTextEffect>`s.

To add a custom effect, it's more convenient to use
`install_effect<class_RichTextLabel_method_install_effect>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **deselect\_on\_focus\_loss\_enabled** = `true`
`🔗<class_RichTextLabel_property_deselect_on_focus_loss_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_deselect\_on\_focus\_loss\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_deselect\_on\_focus\_loss\_enabled**()

If `true`, the selected text will be deselected when focus is lost.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **drag\_and\_drop\_selection\_enabled** = `true`
`🔗<class_RichTextLabel_property_drag_and_drop_selection_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_drag\_and\_drop\_selection\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_drag\_and\_drop\_selection\_enabled**()

If `true`, allow drag and drop of selected text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **fit\_content** = `false`
`🔗<class_RichTextLabel_property_fit_content>`

classref-property-setget

-   `void (No return value.)` **set\_fit\_content**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_fit\_content\_enabled**()

If `true`, the label's minimum size will be automatically updated to fit
its content, matching the behavior of `Label<class_Label>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **hint\_underlined** = `true`
`🔗<class_RichTextLabel_property_hint_underlined>`

classref-property-setget

-   `void (No return value.)` **set\_hint\_underline**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_hint\_underlined**()

If `true`, the label underlines hint tags such as
`[hint=description]{text}[/hint]`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
**horizontal\_alignment** = `0`
`🔗<class_RichTextLabel_property_horizontal_alignment>`

classref-property-setget

-   `void (No return value.)` **set\_horizontal\_alignment**(value:
    `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`)
-   `HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`
    **get\_horizontal\_alignment**()

Controls the text's horizontal alignment. Supports left, center, right,
and fill, or justify. Set it to one of the
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>` constants.

classref-item-separator

------------------------------------------------------------------------

classref-property

`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
**justification\_flags** = `163`
`🔗<class_RichTextLabel_property_justification_flags>`

classref-property-setget

-   `void (No return value.)` **set\_justification\_flags**(value:
    `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\])
-   `BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
    **get\_justification\_flags**()

Line fill alignment rules. See
`JustificationFlag<enum_TextServer_JustificationFlag>` for more
information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **language** = `""`
`🔗<class_RichTextLabel_property_language>`

classref-property-setget

-   `void (No return value.)` **set\_language**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_language**()

Language code used for line-breaking and text shaping algorithms, if
left empty current locale is used instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **meta\_underlined** = `true`
`🔗<class_RichTextLabel_property_meta_underlined>`

classref-property-setget

-   `void (No return value.)` **set\_meta\_underline**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_meta\_underlined**()

If `true`, the label underlines meta tags such as `[url]{text}[/url]`.
These tags can call a function when clicked if
`meta_clicked<class_RichTextLabel_signal_meta_clicked>` is connected to
a function.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **progress\_bar\_delay** = `1000`
`🔗<class_RichTextLabel_property_progress_bar_delay>`

classref-property-setget

-   `void (No return value.)` **set\_progress\_bar\_delay**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_progress\_bar\_delay**()

The delay after which the loading progress bar is displayed, in
milliseconds. Set to `-1` to disable progress bar entirely.

\*\*Note:\*\* Progress bar is displayed only if
`threaded<class_RichTextLabel_property_threaded>` is enabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **scroll\_active** = `true`
`🔗<class_RichTextLabel_property_scroll_active>`

classref-property-setget

-   `void (No return value.)` **set\_scroll\_active**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_scroll\_active**()

If `true`, the scrollbar is visible. Setting this to `false` does not
block scrolling completely. See
`scroll_to_line<class_RichTextLabel_method_scroll_to_line>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **scroll\_following** = `false`
`🔗<class_RichTextLabel_property_scroll_following>`

classref-property-setget

-   `void (No return value.)` **set\_scroll\_follow**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_scroll\_following**()

If `true`, the window scrolls down to display new content automatically.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **selection\_enabled** = `false`
`🔗<class_RichTextLabel_property_selection_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_selection\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_selection\_enabled**()

If `true`, the label allows text selection.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **shortcut\_keys\_enabled** = `true`
`🔗<class_RichTextLabel_property_shortcut_keys_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_shortcut\_keys\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_shortcut\_keys\_enabled**()

If `true`, shortcut keys for context menu items are enabled, even if the
context menu is disabled.

classref-item-separator

------------------------------------------------------------------------

classref-property

`StructuredTextParser<enum_TextServer_StructuredTextParser>`
**structured\_text\_bidi\_override** = `0`
`🔗<class_RichTextLabel_property_structured_text_bidi_override>`

classref-property-setget

-   `void (No return value.)`
    **set\_structured\_text\_bidi\_override**(value:
    `StructuredTextParser<enum_TextServer_StructuredTextParser>`)
-   `StructuredTextParser<enum_TextServer_StructuredTextParser>`
    **get\_structured\_text\_bidi\_override**()

Set BiDi algorithm override for the structured text.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>` **structured\_text\_bidi\_override\_options** =
`[]`
`🔗<class_RichTextLabel_property_structured_text_bidi_override_options>`

classref-property-setget

-   `void (No return value.)`
    **set\_structured\_text\_bidi\_override\_options**(value:
    `Array<class_Array>`)
-   `Array<class_Array>`
    **get\_structured\_text\_bidi\_override\_options**()

Set additional options for BiDi override.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **tab\_size** = `4`
`🔗<class_RichTextLabel_property_tab_size>`

classref-property-setget

-   `void (No return value.)` **set\_tab\_size**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_tab\_size**()

The number of spaces associated with a single tab length. Does not
affect `\t` in text tags, only indent tags.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedFloat32Array<class_PackedFloat32Array>` **tab\_stops** =
`PackedFloat32Array()` `🔗<class_RichTextLabel_property_tab_stops>`

classref-property-setget

-   `void (No return value.)` **set\_tab\_stops**(value:
    `PackedFloat32Array<class_PackedFloat32Array>`)
-   `PackedFloat32Array<class_PackedFloat32Array>` **get\_tab\_stops**()

Aligns text to the given tab-stops.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedFloat32Array<class_PackedFloat32Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **text** = `""`
`🔗<class_RichTextLabel_property_text>`

classref-property-setget

-   `void (No return value.)` **set\_text**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_text**()

The label's text in BBCode format. Is not representative of manual
modifications to the internal tag stack. Erases changes made by other
methods when edited.

\*\*Note:\*\* If
`bbcode_enabled<class_RichTextLabel_property_bbcode_enabled>` is `true`,
it is unadvised to use the `+=` operator with
`text<class_RichTextLabel_property_text>` (e.g. `text += "some string"`)
as it replaces the whole text and can cause slowdowns. It will also
erase all BBCode that was added to stack using `push_*` methods. Use
`append_text<class_RichTextLabel_method_append_text>` for adding text
instead, unless you absolutely need to close a tag that was opened in an
earlier method call.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TextDirection<enum_Control_TextDirection>` **text\_direction** = `0`
`🔗<class_RichTextLabel_property_text_direction>`

classref-property-setget

-   `void (No return value.)` **set\_text\_direction**(value:
    `TextDirection<enum_Control_TextDirection>`)
-   `TextDirection<enum_Control_TextDirection>`
    **get\_text\_direction**()

Base text writing direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **threaded** = `false`
`🔗<class_RichTextLabel_property_threaded>`

classref-property-setget

-   `void (No return value.)` **set\_threaded**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_threaded**()

If `true`, text processing is done in a background thread.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **visible\_characters** = `-1`
`🔗<class_RichTextLabel_property_visible_characters>`

classref-property-setget

-   `void (No return value.)` **set\_visible\_characters**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_visible\_characters**()

The number of characters to display. If set to `-1`, all characters are
displayed. This can be useful when animating the text appearing in a
dialog box.

\*\*Note:\*\* Setting this property updates
`visible_ratio<class_RichTextLabel_property_visible_ratio>` accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VisibleCharactersBehavior<enum_TextServer_VisibleCharactersBehavior>`
**visible\_characters\_behavior** = `0`
`🔗<class_RichTextLabel_property_visible_characters_behavior>`

classref-property-setget

-   `void (No return value.)`
    **set\_visible\_characters\_behavior**(value:
    `VisibleCharactersBehavior<enum_TextServer_VisibleCharactersBehavior>`)
-   `VisibleCharactersBehavior<enum_TextServer_VisibleCharactersBehavior>`
    **get\_visible\_characters\_behavior**()

Sets the clipping behavior when
`visible_characters<class_RichTextLabel_property_visible_characters>` or
`visible_ratio<class_RichTextLabel_property_visible_ratio>` is set. See
`VisibleCharactersBehavior<enum_TextServer_VisibleCharactersBehavior>`
for more info.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **visible\_ratio** = `1.0`
`🔗<class_RichTextLabel_property_visible_ratio>`

classref-property-setget

-   `void (No return value.)` **set\_visible\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_visible\_ratio**()

The fraction of characters to display, relative to the total number of
characters (see
`get_total_character_count<class_RichTextLabel_method_get_total_character_count>`).
If set to `1.0`, all characters are displayed. If set to `0.5`, only
half of the characters will be displayed. This can be useful when
animating the text appearing in a dialog box.

\*\*Note:\*\* Setting this property updates
`visible_characters<class_RichTextLabel_property_visible_characters>`
accordingly.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_image**(image:
`Texture2D<class_Texture2D>`, width: `int<class_int>` = 0, height:
`int<class_int>` = 0, color: `Color<class_Color>` = Color(1, 1, 1, 1),
inline\_align: `InlineAlignment<enum_@GlobalScope_InlineAlignment>` = 5,
region: `Rect2<class_Rect2>` = Rect2(0, 0, 0, 0), key:
`Variant<class_Variant>` = null, pad: `bool<class_bool>` = false,
tooltip: `String<class_String>` = "", size\_in\_percent:
`bool<class_bool>` = false) `🔗<class_RichTextLabel_method_add_image>`

Adds an image's opening and closing tags to the tag stack, optionally
providing a `width` and `height` to resize the image, a `color` to tint
the image and a `region` to only use parts of the image.

If `width` or `height` is set to 0, the image size will be adjusted in
order to keep the original aspect ratio.

If `width` and `height` are not set, but `region` is, the region's rect
will be used.

`key` is an optional identifier, that can be used to modify the image
via `update_image<class_RichTextLabel_method_update_image>`.

If `pad` is set, and the image is smaller than the size specified by
`width` and `height`, the image padding is added to match the size
instead of upscaling.

If `size_in_percent` is set, `width` and `height` values are percentages
of the control width instead of pixels.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_text**(text: `String<class_String>`)
`🔗<class_RichTextLabel_method_add_text>`

Adds raw non-BBCode-parsed text to the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **append\_text**(bbcode:
`String<class_String>`) `🔗<class_RichTextLabel_method_append_text>`

Parses `bbcode` and adds tags to the tag stack as needed.

\*\*Note:\*\* Using this method, you can't close a tag that was opened
in a previous `append_text<class_RichTextLabel_method_append_text>`
call. This is done to improve performance, especially when updating
large RichTextLabels since rebuilding the whole BBCode every time would
be slower. If you absolutely need to close a tag in a future method
call, append the `text<class_RichTextLabel_property_text>` instead of
using `append_text<class_RichTextLabel_method_append_text>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_RichTextLabel_method_clear>`

Clears the tag stack, causing the label to display nothing.

\*\*Note:\*\* This method does not affect
`text<class_RichTextLabel_property_text>`, and its contents will show
again if the label is redrawn. However, setting
`text<class_RichTextLabel_property_text>` to an empty
`String<class_String>` also clears the stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **deselect**()
`🔗<class_RichTextLabel_method_deselect>`

Clears the current selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_character\_line**(character: `int<class_int>`)
`🔗<class_RichTextLabel_method_get_character_line>`

Returns the line number of the character position provided. Line and
character numbers are both zero-indexed.

\*\*Note:\*\* If `threaded<class_RichTextLabel_property_threaded>` is
enabled, this method returns a value for the loaded part of the
document. Use `is_finished<class_RichTextLabel_method_is_finished>` or
`finished<class_RichTextLabel_signal_finished>` to determine whether
document is fully loaded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_character\_paragraph**(character:
`int<class_int>`)
`🔗<class_RichTextLabel_method_get_character_paragraph>`

Returns the paragraph number of the character position provided.
Paragraph and character numbers are both zero-indexed.

\*\*Note:\*\* If `threaded<class_RichTextLabel_property_threaded>` is
enabled, this method returns a value for the loaded part of the
document. Use `is_finished<class_RichTextLabel_method_is_finished>` or
`finished<class_RichTextLabel_signal_finished>` to determine whether
document is fully loaded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_content\_height**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_content_height>`

Returns the height of the content.

\*\*Note:\*\* If `threaded<class_RichTextLabel_property_threaded>` is
enabled, this method returns a value for the loaded part of the
document. Use `is_finished<class_RichTextLabel_method_is_finished>` or
`finished<class_RichTextLabel_signal_finished>` to determine whether
document is fully loaded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_content\_width**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_content_width>`

Returns the width of the content.

\*\*Note:\*\* If `threaded<class_RichTextLabel_property_threaded>` is
enabled, this method returns a value for the loaded part of the
document. Use `is_finished<class_RichTextLabel_method_is_finished>` or
`finished<class_RichTextLabel_signal_finished>` to determine whether
document is fully loaded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_line\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_line_count>`

Returns the total number of lines in the text. Wrapped text is counted
as multiple lines.

\*\*Note:\*\* If `threaded<class_RichTextLabel_property_threaded>` is
enabled, this method returns a value for the loaded part of the
document. Use `is_finished<class_RichTextLabel_method_is_finished>` or
`finished<class_RichTextLabel_signal_finished>` to determine whether
document is fully loaded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_line\_offset**(line: `int<class_int>`)
`🔗<class_RichTextLabel_method_get_line_offset>`

Returns the vertical offset of the line found at the provided index.

\*\*Note:\*\* If `threaded<class_RichTextLabel_property_threaded>` is
enabled, this method returns a value for the loaded part of the
document. Use `is_finished<class_RichTextLabel_method_is_finished>` or
`finished<class_RichTextLabel_signal_finished>` to determine whether
document is fully loaded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PopupMenu<class_PopupMenu>` **get\_menu**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_menu>`

Returns the `PopupMenu<class_PopupMenu>` of this **RichTextLabel**. By
default, this menu is displayed when right-clicking on the
**RichTextLabel**.

You can add custom menu items or remove standard ones. Make sure your
IDs don't conflict with the standard ones (see
`MenuItems<enum_RichTextLabel_MenuItems>`). For example:

gdscript

func \_ready():  
var menu = get\_menu() \# Remove "Select All" item.
menu.remove\_item(MENU\_SELECT\_ALL) \# Add custom items.
menu.add\_separator() menu.add\_item("Duplicate Text", MENU\_MAX + 1) \#
Connect callback. menu.id\_pressed.connect(\_on\_item\_pressed)

func \_on\_item\_pressed(id):  
if id == MENU\_MAX + 1:  
add\_text("n" + get\_parsed\_text())

csharp

public override void \_Ready() { var menu = GetMenu(); // Remove "Select
All" item. menu.RemoveItem(RichTextLabel.MenuItems.SelectAll); // Add
custom items. menu.AddSeparator(); menu.AddItem("Duplicate Text",
RichTextLabel.MenuItems.Max + 1); // Add event handler. menu.IdPressed
+= OnItemPressed; }

public void OnItemPressed(int id) { if (id ==
TextEdit.MenuItems.Max + 1) { AddText("n" + GetParsedText()); } }

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to hide it or any of its children, use
their `Window.visible<class_Window_property_visible>` property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_paragraph\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_paragraph_count>`

Returns the total number of paragraphs (newlines or `p` tags in the tag
stack's text tags). Considers wrapped text as one paragraph.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_paragraph\_offset**(paragraph:
`int<class_int>`) `🔗<class_RichTextLabel_method_get_paragraph_offset>`

Returns the vertical offset of the paragraph found at the provided
index.

\*\*Note:\*\* If `threaded<class_RichTextLabel_property_threaded>` is
enabled, this method returns a value for the loaded part of the
document. Use `is_finished<class_RichTextLabel_method_is_finished>` or
`finished<class_RichTextLabel_signal_finished>` to determine whether
document is fully loaded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_parsed\_text**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_parsed_text>`

Returns the text without BBCode mark-up.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_selected\_text**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_selected_text>`

Returns the current selection text. Does not include BBCodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selection\_from**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_selection_from>`

Returns the current selection first character index if a selection is
active, `-1` otherwise. Does not include BBCodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_selection\_to**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_selection_to>`

Returns the current selection last character index if a selection is
active, `-1` otherwise. Does not include BBCodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_total\_character\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_total_character_count>`

Returns the total number of characters from text tags. Does not include
BBCodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`VScrollBar<class_VScrollBar>` **get\_v\_scroll\_bar**()
`🔗<class_RichTextLabel_method_get_v_scroll_bar>`

Returns the vertical scrollbar.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to hide it or any of its children, use
their `CanvasItem.visible<class_CanvasItem_property_visible>` property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_visible\_line\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_visible_line_count>`

Returns the number of visible lines.

\*\*Note:\*\* If `threaded<class_RichTextLabel_property_threaded>` is
enabled, this method returns a value for the loaded part of the
document. Use `is_finished<class_RichTextLabel_method_is_finished>` or
`finished<class_RichTextLabel_signal_finished>` to determine whether
document is fully loaded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_visible\_paragraph\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_get_visible_paragraph_count>`

Returns the number of visible paragraphs. A paragraph is considered
visible if at least one of its lines is visible.

\*\*Note:\*\* If `threaded<class_RichTextLabel_property_threaded>` is
enabled, this method returns a value for the loaded part of the
document. Use `is_finished<class_RichTextLabel_method_is_finished>` or
`finished<class_RichTextLabel_signal_finished>` to determine whether
document is fully loaded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **install\_effect**(effect:
`Variant<class_Variant>`)
`🔗<class_RichTextLabel_method_install_effect>`

Installs a custom effect. This can also be done in the RichTextLabel
inspector using the
`custom_effects<class_RichTextLabel_property_custom_effects>` property.
`effect` should be a valid `RichTextEffect<class_RichTextEffect>`.

Example RichTextEffect:

    # effect.gd
    class_name MyCustomEffect
    extends RichTextEffect

    var bbcode = "my_custom_effect"

    # ...

Registering the above effect in RichTextLabel from script:

    # rich_text_label.gd
    extends RichTextLabel

    func _ready():
        install_effect(MyCustomEffect.new())

        # Alternatively, if not using `class_name` in the script that extends RichTextEffect:
        install_effect(preload("res://effect.gd").new())

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **invalidate\_paragraph**(paragraph:
`int<class_int>`) `🔗<class_RichTextLabel_method_invalidate_paragraph>`

Invalidates `paragraph` and all subsequent paragraphs cache.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_finished**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_is_finished>`

If `threaded<class_RichTextLabel_property_threaded>` is enabled, returns
`true` if the background thread has finished text processing, otherwise
always return `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_menu\_visible**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_is_menu_visible>`

Returns whether the menu is visible. Use this instead of
`get_menu().visible` to improve performance (so the creation of the menu
is avoided).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_ready**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextLabel_method_is_ready>`

**Deprecated:** Use
`is_finished<class_RichTextLabel_method_is_finished>` instead.

If `threaded<class_RichTextLabel_property_threaded>` is enabled, returns
`true` if the background thread has finished text processing, otherwise
always return `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **menu\_option**(option: `int<class_int>`)
`🔗<class_RichTextLabel_method_menu_option>`

Executes a given action as defined in the
`MenuItems<enum_RichTextLabel_MenuItems>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **newline**()
`🔗<class_RichTextLabel_method_newline>`

Adds a newline tag to the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **parse\_bbcode**(bbcode:
`String<class_String>`) `🔗<class_RichTextLabel_method_parse_bbcode>`

The assignment version of
`append_text<class_RichTextLabel_method_append_text>`. Clears the tag
stack and inserts the new content.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**parse\_expressions\_for\_values**(expressions:
`PackedStringArray<class_PackedStringArray>`)
`🔗<class_RichTextLabel_method_parse_expressions_for_values>`

Parses BBCode parameter `expressions` into a dictionary.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **pop**() `🔗<class_RichTextLabel_method_pop>`

Terminates the current tag. Use after `push_*` methods to close BBCodes
manually. Does not need to follow `add_*` methods.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **pop\_all**()
`🔗<class_RichTextLabel_method_pop_all>`

Terminates all tags opened by `push_*` methods.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **pop\_context**()
`🔗<class_RichTextLabel_method_pop_context>`

Terminates tags opened after the last
`push_context<class_RichTextLabel_method_push_context>` call (including
context marker), or all tags if there's no context marker on the stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_bgcolor**(bgcolor:
`Color<class_Color>`) `🔗<class_RichTextLabel_method_push_bgcolor>`

Adds a `[bgcolor]` tag to the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_bold**()
`🔗<class_RichTextLabel_method_push_bold>`

Adds a `[font]` tag with a bold font to the tag stack. This is the same
as adding a `[b]` tag if not currently in a `[i]` tag.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_bold\_italics**()
`🔗<class_RichTextLabel_method_push_bold_italics>`

Adds a `[font]` tag with a bold italics font to the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_cell**()
`🔗<class_RichTextLabel_method_push_cell>`

Adds a `[cell]` tag to the tag stack. Must be inside a `[table]` tag.
See `push_table<class_RichTextLabel_method_push_table>` for details. Use
`set_table_column_expand<class_RichTextLabel_method_set_table_column_expand>`
to set column expansion ratio,
`set_cell_border_color<class_RichTextLabel_method_set_cell_border_color>`
to set cell border,
`set_cell_row_background_color<class_RichTextLabel_method_set_cell_row_background_color>`
to set cell background,
`set_cell_size_override<class_RichTextLabel_method_set_cell_size_override>`
to override cell size, and
`set_cell_padding<class_RichTextLabel_method_set_cell_padding>` to set
padding.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_color**(color: `Color<class_Color>`)
`🔗<class_RichTextLabel_method_push_color>`

Adds a `[color]` tag to the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_context**()
`🔗<class_RichTextLabel_method_push_context>`

Adds a context marker to the tag stack. See
`pop_context<class_RichTextLabel_method_pop_context>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_customfx**(effect:
`RichTextEffect<class_RichTextEffect>`, env:
`Dictionary<class_Dictionary>`)
`🔗<class_RichTextLabel_method_push_customfx>`

Adds a custom effect tag to the tag stack. The effect does not need to
be in `custom_effects<class_RichTextLabel_property_custom_effects>`. The
environment is directly passed to the effect.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_dropcap**(string:
`String<class_String>`, font: `Font<class_Font>`, size:
`int<class_int>`, dropcap\_margins: `Rect2<class_Rect2>` = Rect2(0, 0,
0, 0), color: `Color<class_Color>` = Color(1, 1, 1, 1), outline\_size:
`int<class_int>` = 0, outline\_color: `Color<class_Color>` = Color(0, 0,
0, 0)) `🔗<class_RichTextLabel_method_push_dropcap>`

Adds a `[dropcap]` tag to the tag stack. Drop cap (dropped capital) is a
decorative element at the beginning of a paragraph that is larger than
the rest of the text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_fgcolor**(fgcolor:
`Color<class_Color>`) `🔗<class_RichTextLabel_method_push_fgcolor>`

Adds a `[fgcolor]` tag to the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_font**(font: `Font<class_Font>`,
font\_size: `int<class_int>` = 0)
`🔗<class_RichTextLabel_method_push_font>`

Adds a `[font]` tag to the tag stack. Overrides default fonts for its
duration.

Passing `0` to `font_size` will use the existing default font size.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_font\_size**(font\_size:
`int<class_int>`) `🔗<class_RichTextLabel_method_push_font_size>`

Adds a `[font_size]` tag to the tag stack. Overrides default font size
for its duration.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_hint**(description:
`String<class_String>`) `🔗<class_RichTextLabel_method_push_hint>`

Adds a `[hint]` tag to the tag stack. Same as BBCode
`[hint=something]{text}[/hint]`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_indent**(level: `int<class_int>`)
`🔗<class_RichTextLabel_method_push_indent>`

Adds an `[indent]` tag to the tag stack. Multiplies `level` by current
`tab_size<class_RichTextLabel_property_tab_size>` to determine new
margin length.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_italics**()
`🔗<class_RichTextLabel_method_push_italics>`

Adds a `[font]` tag with an italics font to the tag stack. This is the
same as adding an `[i]` tag if not currently in a `[b]` tag.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_language**(language:
`String<class_String>`) `🔗<class_RichTextLabel_method_push_language>`

Adds language code used for text shaping algorithm and Open-Type font
features.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_list**(level: `int<class_int>`, type:
`ListType<enum_RichTextLabel_ListType>`, capitalize: `bool<class_bool>`,
bullet: `String<class_String>` = "•")
`🔗<class_RichTextLabel_method_push_list>`

Adds `[ol]` or `[ul]` tag to the tag stack. Multiplies `level` by
current `tab_size<class_RichTextLabel_property_tab_size>` to determine
new margin length.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_meta**(data: `Variant<class_Variant>`,
underline\_mode: `MetaUnderline<enum_RichTextLabel_MetaUnderline>` = 1)
`🔗<class_RichTextLabel_method_push_meta>`

Adds a meta tag to the tag stack. Similar to the BBCode
`[url=something]{text}[/url]`, but supports non-`String<class_String>`
metadata types.

If `meta_underlined<class_RichTextLabel_property_meta_underlined>` is
`true`, meta tags display an underline. This behavior can be customized
with `underline_mode`.

\*\*Note:\*\* Meta tags do nothing by default when clicked. To assign
behavior when clicked, connect
`meta_clicked<class_RichTextLabel_signal_meta_clicked>` to a function
that is called when the meta tag is clicked.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_mono**()
`🔗<class_RichTextLabel_method_push_mono>`

Adds a `[font]` tag with a monospace font to the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_normal**()
`🔗<class_RichTextLabel_method_push_normal>`

Adds a `[font]` tag with a normal font to the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_outline\_color**(color:
`Color<class_Color>`)
`🔗<class_RichTextLabel_method_push_outline_color>`

Adds a `[outline_color]` tag to the tag stack. Adds text outline for its
duration.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_outline\_size**(outline\_size:
`int<class_int>`) `🔗<class_RichTextLabel_method_push_outline_size>`

Adds a `[outline_size]` tag to the tag stack. Overrides default text
outline size for its duration.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_paragraph**(alignment:
`HorizontalAlignment<enum_@GlobalScope_HorizontalAlignment>`,
base\_direction: `TextDirection<enum_Control_TextDirection>` = 0,
language: `String<class_String>` = "", st\_parser:
`StructuredTextParser<enum_TextServer_StructuredTextParser>` = 0,
justification\_flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`JustificationFlag<enum_TextServer_JustificationFlag>`\]
= 163, tab\_stops: `PackedFloat32Array<class_PackedFloat32Array>` =
PackedFloat32Array()) `🔗<class_RichTextLabel_method_push_paragraph>`

Adds a `[p]` tag to the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_strikethrough**()
`🔗<class_RichTextLabel_method_push_strikethrough>`

Adds a `[s]` tag to the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_table**(columns: `int<class_int>`,
inline\_align: `InlineAlignment<enum_@GlobalScope_InlineAlignment>` = 0,
align\_to\_row: `int<class_int>` = -1)
`🔗<class_RichTextLabel_method_push_table>`

Adds a `[table=columns,inline_align]` tag to the tag stack. Use
`set_table_column_expand<class_RichTextLabel_method_set_table_column_expand>`
to set column expansion ratio. Use
`push_cell<class_RichTextLabel_method_push_cell>` to add cells.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **push\_underline**()
`🔗<class_RichTextLabel_method_push_underline>`

Adds a `[u]` tag to the tag stack.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **remove\_paragraph**(paragraph: `int<class_int>`,
no\_invalidate: `bool<class_bool>` = false)
`🔗<class_RichTextLabel_method_remove_paragraph>`

Removes a paragraph of content from the label. Returns `true` if the
paragraph exists.

The `paragraph` argument is the index of the paragraph to remove, it can
take values in the interval `[0, get_paragraph_count() - 1]`.

If `no_invalidate` is set to `true`, cache for the subsequent paragraphs
is not invalidated. Use it for faster updates if deleted paragraph is
fully self-contained (have no unclosed tags), or this call is part of
the complex edit operation and
`invalidate_paragraph<class_RichTextLabel_method_invalidate_paragraph>`
will be called at the end of operation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **scroll\_to\_line**(line: `int<class_int>`)
`🔗<class_RichTextLabel_method_scroll_to_line>`

Scrolls the window's top line to match `line`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **scroll\_to\_paragraph**(paragraph:
`int<class_int>`) `🔗<class_RichTextLabel_method_scroll_to_paragraph>`

Scrolls the window's top line to match first line of the `paragraph`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **scroll\_to\_selection**()
`🔗<class_RichTextLabel_method_scroll_to_selection>`

Scrolls to the beginning of the current selection.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **select\_all**()
`🔗<class_RichTextLabel_method_select_all>`

Select all the text.

If `selection_enabled<class_RichTextLabel_property_selection_enabled>`
is `false`, no selection will occur.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_cell\_border\_color**(color:
`Color<class_Color>`)
`🔗<class_RichTextLabel_method_set_cell_border_color>`

Sets color of a table cell border.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_cell\_padding**(padding:
`Rect2<class_Rect2>`) `🔗<class_RichTextLabel_method_set_cell_padding>`

Sets inner padding of a table cell.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_cell\_row\_background\_color**(odd\_row\_bg:
`Color<class_Color>`, even\_row\_bg: `Color<class_Color>`)
`🔗<class_RichTextLabel_method_set_cell_row_background_color>`

Sets color of a table cell. Separate colors for alternating rows can be
specified.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_cell\_size\_override**(min\_size:
`Vector2<class_Vector2>`, max\_size: `Vector2<class_Vector2>`)
`🔗<class_RichTextLabel_method_set_cell_size_override>`

Sets minimum and maximum size overrides for a table cell.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_table\_column\_expand**(column:
`int<class_int>`, expand: `bool<class_bool>`, ratio: `int<class_int>`
= 1) `🔗<class_RichTextLabel_method_set_table_column_expand>`

Edits the selected column's expansion options. If `expand` is `true`,
the column expands in proportion to its expansion ratio versus the other
columns' ratios.

For example, 2 columns with ratios 3 and 4 plus 70 pixels in available
width would expand 30 and 40 pixels, respectively.

If `expand` is `false`, the column will not contribute to the total
ratio.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **update\_image**(key:
`Variant<class_Variant>`, mask:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`ImageUpdateMask<enum_RichTextLabel_ImageUpdateMask>`\],
image: `Texture2D<class_Texture2D>`, width: `int<class_int>` = 0,
height: `int<class_int>` = 0, color: `Color<class_Color>` = Color(1, 1,
1, 1), inline\_align:
`InlineAlignment<enum_@GlobalScope_InlineAlignment>` = 5, region:
`Rect2<class_Rect2>` = Rect2(0, 0, 0, 0), pad: `bool<class_bool>` =
false, tooltip: `String<class_String>` = "", size\_in\_percent:
`bool<class_bool>` = false)
`🔗<class_RichTextLabel_method_update_image>`

Updates the existing images with the key `key`. Only properties
specified by `mask` bits are updated. See
`add_image<class_RichTextLabel_method_add_image>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Theme Property Descriptions

classref-themeproperty

`Color<class_Color>` **default\_color** = `Color(1, 1, 1, 1)`
`🔗<class_RichTextLabel_theme_color_default_color>`

The default text color.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_outline\_color** = `Color(0, 0, 0, 1)`
`🔗<class_RichTextLabel_theme_color_font_outline_color>`

The default tint of text outline.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_selected\_color** = `Color(0, 0, 0, 0)`
`🔗<class_RichTextLabel_theme_color_font_selected_color>`

The color of selected text, used when
`selection_enabled<class_RichTextLabel_property_selection_enabled>` is
`true`. If equal to `Color(0, 0, 0, 0)`, it will be ignored.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **font\_shadow\_color** = `Color(0, 0, 0, 0)`
`🔗<class_RichTextLabel_theme_color_font_shadow_color>`

The color of the font's shadow.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **selection\_color** = `Color(0.1, 0.1, 1, 0.8)`
`🔗<class_RichTextLabel_theme_color_selection_color>`

The color of the selection box.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **table\_border** = `Color(0, 0, 0, 0)`
`🔗<class_RichTextLabel_theme_color_table_border>`

The default cell border color.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **table\_even\_row\_bg** = `Color(0, 0, 0, 0)`
`🔗<class_RichTextLabel_theme_color_table_even_row_bg>`

The default background color for even rows.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Color<class_Color>` **table\_odd\_row\_bg** = `Color(0, 0, 0, 0)`
`🔗<class_RichTextLabel_theme_color_table_odd_row_bg>`

The default background color for odd rows.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **line\_separation** = `0`
`🔗<class_RichTextLabel_theme_constant_line_separation>`

The vertical space between lines.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **outline\_size** = `0`
`🔗<class_RichTextLabel_theme_constant_outline_size>`

The size of the text outline.

\*\*Note:\*\* If using a font with
`FontFile.multichannel_signed_distance_field<class_FontFile_property_multichannel_signed_distance_field>`
enabled, its
`FontFile.msdf_pixel_range<class_FontFile_property_msdf_pixel_range>`
must be set to at least *twice* the value of
`outline_size<class_RichTextLabel_theme_constant_outline_size>` for
outline rendering to look correct. Otherwise, the outline may appear to
be cut off earlier than intended.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **shadow\_offset\_x** = `1`
`🔗<class_RichTextLabel_theme_constant_shadow_offset_x>`

The horizontal offset of the font's shadow.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **shadow\_offset\_y** = `1`
`🔗<class_RichTextLabel_theme_constant_shadow_offset_y>`

The vertical offset of the font's shadow.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **shadow\_outline\_size** = `1`
`🔗<class_RichTextLabel_theme_constant_shadow_outline_size>`

The size of the shadow outline.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **table\_h\_separation** = `3`
`🔗<class_RichTextLabel_theme_constant_table_h_separation>`

The horizontal separation of elements in a table.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **table\_v\_separation** = `3`
`🔗<class_RichTextLabel_theme_constant_table_v_separation>`

The vertical separation of elements in a table.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **text\_highlight\_h\_padding** = `3`
`🔗<class_RichTextLabel_theme_constant_text_highlight_h_padding>`

The horizontal padding around boxes drawn by the `[fgcolor]` and
`[bgcolor]` tags. This does not affect the appearance of text selection.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **text\_highlight\_v\_padding** = `3`
`🔗<class_RichTextLabel_theme_constant_text_highlight_v_padding>`

The vertical padding around boxes drawn by the `[fgcolor]` and
`[bgcolor]` tags. This does not affect the appearance of text selection.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **bold\_font**
`🔗<class_RichTextLabel_theme_font_bold_font>`

The font used for bold text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **bold\_italics\_font**
`🔗<class_RichTextLabel_theme_font_bold_italics_font>`

The font used for bold italics text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **italics\_font**
`🔗<class_RichTextLabel_theme_font_italics_font>`

The font used for italics text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **mono\_font**
`🔗<class_RichTextLabel_theme_font_mono_font>`

The font used for monospace text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`Font<class_Font>` **normal\_font**
`🔗<class_RichTextLabel_theme_font_normal_font>`

The default text font.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **bold\_font\_size**
`🔗<class_RichTextLabel_theme_font_size_bold_font_size>`

The font size used for bold text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **bold\_italics\_font\_size**
`🔗<class_RichTextLabel_theme_font_size_bold_italics_font_size>`

The font size used for bold italics text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **italics\_font\_size**
`🔗<class_RichTextLabel_theme_font_size_italics_font_size>`

The font size used for italics text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **mono\_font\_size**
`🔗<class_RichTextLabel_theme_font_size_mono_font_size>`

The font size used for monospace text.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`int<class_int>` **normal\_font\_size**
`🔗<class_RichTextLabel_theme_font_size_normal_font_size>`

The default text font size.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **focus**
`🔗<class_RichTextLabel_theme_style_focus>`

The background used when the **RichTextLabel** is focused. The
`focus<class_RichTextLabel_theme_style_focus>`
`StyleBox<class_StyleBox>` is displayed *over* the base
`StyleBox<class_StyleBox>`, so a partially transparent
`StyleBox<class_StyleBox>` should be used to ensure the base
`StyleBox<class_StyleBox>` remains visible. A `StyleBox<class_StyleBox>`
that represents an outline or an underline works well for this purpose.
To disable the focus visual effect, assign a
`StyleBoxEmpty<class_StyleBoxEmpty>` resource. Note that disabling the
focus visual effect will harm keyboard/controller navigation usability,
so this is not recommended for accessibility reasons.

classref-item-separator

------------------------------------------------------------------------

classref-themeproperty

`StyleBox<class_StyleBox>` **normal**
`🔗<class_RichTextLabel_theme_style_normal>`

The normal background for the **RichTextLabel**.
