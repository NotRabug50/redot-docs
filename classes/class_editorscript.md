github\_url  
hide

# EditorScript

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Base script that can be used to add extension functions to the editor.

classref-introduction-group

## Description

Scripts extending this class and implementing its
`_run<class_EditorScript_private_method__run>` method can be executed
from the Script Editor's **File &gt; Run** menu option (or by pressing
`Ctrl + Shift + X`) while the editor is running. This is useful for
adding custom in-editor functionality to Godot. For more complex
additions, consider using `EditorPlugin<class_EditorPlugin>`s instead.

\*\*Note:\*\* Extending scripts need to have `tool` mode enabled.

\*\*Example script:\*\*

gdscript

@tool extends EditorScript

func \_run():  
print("Hello from the Godot Editor!")

csharp

using Godot;

\[Tool\] public partial class HelloEditor : EditorScript { public
override void \_Run() { GD.Print("Hello from the Godot Editor!"); } }

\*\*Note:\*\* The script is run in the Editor context, which means the
output is visible in the console window started with the Editor (stdout)
instead of the usual Godot **Output** dock.

\*\*Note:\*\* EditorScript is `RefCounted<class_RefCounted>`, meaning it
is destroyed when nothing references it. This can cause errors during
asynchronous operations if there are no references to the script.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_run**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorScript_private_method__run>`

This method is executed by the Editor when **File &gt; Run** is used.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_root\_node**(node: `Node<class_Node>`)
`🔗<class_EditorScript_method_add_root_node>`

Makes `node` root of the currently opened scene. Only works if the scene
is empty. If the `node` is a scene instance, an inheriting scene will be
created.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorInterface<class_EditorInterface>` **get\_editor\_interface**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorScript_method_get_editor_interface>`

**Deprecated:** `EditorInterface<class_EditorInterface>` is a global
singleton and can be accessed directly by its name.

Returns the `EditorInterface<class_EditorInterface>` singleton instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **get\_scene**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorScript_method_get_scene>`

Returns the edited (current) scene's root `Node<class_Node>`. Equivalent
of
`EditorInterface.get_edited_scene_root<class_EditorInterface_method_get_edited_scene_root>`.
