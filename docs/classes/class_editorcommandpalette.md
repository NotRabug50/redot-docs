github\_url  
hide

# EditorCommandPalette

**Inherits:** `ConfirmationDialog<class_ConfirmationDialog>` **&lt;**
`AcceptDialog<class_AcceptDialog>` **&lt;** `Window<class_Window>`
**&lt;** `Viewport<class_Viewport>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

Godot editor's command palette.

classref-introduction-group

## Description

Object that holds all the available Commands and their shortcuts text.
These Commands can be accessed through **Editor &gt; Command Palette**
menu.

Command key names use slash delimiters to distinguish sections, for
example: `"example/command1"` then `example` will be the section name.

gdscript

var command\_palette = EditorInterface.get\_command\_palette() \#
external\_command is a function that will be called with the command is
executed. var command\_callable = Callable(self,
"external\_command").bind(arguments)
command\_palette.add\_command("command",
"test/command",command\_callable)

csharp

EditorCommandPalette commandPalette =
EditorInterface.Singleton.GetCommandPalette(); // ExternalCommand is a
function that will be called with the command is executed. Callable
commandCallable = new Callable(this, MethodName.ExternalCommand);
commandPalette.AddCommand("command", "test/command", commandCallable)

\*\*Note:\*\* This class shouldn't be instantiated directly. Instead,
access the singleton using
`EditorInterface.get_command_palette<class_EditorInterface_method_get_command_palette>`.

classref-reftable-group

## Properties

<table>
<tbody>
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

## Method Descriptions

classref-method

`void (No return value.)` **add\_command**(command\_name:
`String<class_String>`, key\_name: `String<class_String>`,
binded\_callable: `Callable<class_Callable>`, shortcut\_text:
`String<class_String>` = "None")
`🔗<class_EditorCommandPalette_method_add_command>`

Adds a custom command to EditorCommandPalette.

-   `command_name`: `String<class_String>` (Name of the **Command**.
    This is displayed to the user.)
-   `key_name`: `String<class_String>` (Name of the key for a particular
    **Command**. This is used to uniquely identify the **Command**.)
-   `binded_callable`: `Callable<class_Callable>` (Callable of the
    **Command**. This will be executed when the **Command** is
    selected.)
-   `shortcut_text`: `String<class_String>` (Shortcut text of the
    **Command** if available.)

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_command**(key\_name:
`String<class_String>`)
`🔗<class_EditorCommandPalette_method_remove_command>`

Removes the custom command from EditorCommandPalette.

-   `key_name`: `String<class_String>` (Name of the key for a particular
    **Command**.)
