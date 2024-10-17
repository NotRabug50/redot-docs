github\_url  
hide

# ConfirmationDialog

**Inherits:** `AcceptDialog<class_AcceptDialog>` **&lt;**
`Window<class_Window>` **&lt;** `Viewport<class_Viewport>` **&lt;**
`Node<class_Node>` **&lt;** `Object<class_Object>`

**Inherited By:** `EditorCommandPalette<class_EditorCommandPalette>`,
`EditorFileDialog<class_EditorFileDialog>`,
`FileDialog<class_FileDialog>`,
`ScriptCreateDialog<class_ScriptCreateDialog>`

A dialog used for confirmation of actions.

classref-introduction-group

## Description

A dialog used for confirmation of actions. This window is similar to
`AcceptDialog<class_AcceptDialog>`, but pressing its Cancel button can
have a different outcome from pressing the OK button. The order of the
two buttons varies depending on the host OS.

To get cancel action, you can use:

gdscript

get\_cancel\_button().pressed.connect(\_on\_canceled)

csharp

GetCancelButton().Pressed += OnCanceled;

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **cancel\_button\_text** = `"Cancel"`
`🔗<class_ConfirmationDialog_property_cancel_button_text>`

classref-property-setget

-   `void (No return value.)` **set\_cancel\_button\_text**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_cancel\_button\_text**()

The text displayed by the cancel button (see
`get_cancel_button<class_ConfirmationDialog_method_get_cancel_button>`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Button<class_Button>` **get\_cancel\_button**()
`🔗<class_ConfirmationDialog_method_get_cancel_button>`

Returns the cancel button.

\*\*Warning:\*\* This is a required internal node, removing and freeing
it may cause a crash. If you wish to hide it or any of its children, use
their `CanvasItem.visible<class_CanvasItem_property_visible>` property.
