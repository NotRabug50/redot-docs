github\_url  
hide

# ScriptCreateDialog

**Inherits:** `ConfirmationDialog<class_ConfirmationDialog>` **&lt;**
`AcceptDialog<class_AcceptDialog>` **&lt;** `Window<class_Window>`
**&lt;** `Viewport<class_Viewport>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Godot editor's popup dialog for creating new `Script<class_Script>`
files.

classref-introduction-group

## Description

The **ScriptCreateDialog** creates script files according to a given
template for a given scripting language. The standard use is to
configure its fields prior to calling one of the
`Window.popup<class_Window_method_popup>` methods.

gdscript

func \_ready():  
var dialog = ScriptCreateDialog.new(); dialog.config("Node",
"<res://new_node.gd>") \# For in-engine types.
dialog.config(""[res://base\_node.gd\\](res://base_node.gd\)"",
"<res://derived_node.gd>") \# For script types. dialog.popup\_centered()

csharp

public override void \_Ready() { var dialog = new ScriptCreateDialog();
dialog.Config("Node", "<res://NewNode.cs>"); // For in-engine types.
dialog.Config(""[res://BaseNode.cs\\](res://BaseNode.cs\)"",
"<res://DerivedNode.cs>"); // For script types. dialog.PopupCentered();
}

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

## Signals

classref-signal

**script\_created**(script: `Script<class_Script>`)
`🔗<class_ScriptCreateDialog_signal_script_created>`

Emitted when the user clicks the OK button.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **config**(inherits: `String<class_String>`,
path: `String<class_String>`, built\_in\_enabled: `bool<class_bool>` =
true, load\_enabled: `bool<class_bool>` = true)
`🔗<class_ScriptCreateDialog_method_config>`

Prefills required fields to configure the ScriptCreateDialog for use.
