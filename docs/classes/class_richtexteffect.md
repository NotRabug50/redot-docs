github\_url  
hide

# RichTextEffect

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A custom effect for a `RichTextLabel<class_RichTextLabel>`.

classref-introduction-group

## Description

A custom effect for a `RichTextLabel<class_RichTextLabel>`, which can be
loaded in the `RichTextLabel<class_RichTextLabel>` inspector or using
`RichTextLabel.install_effect<class_RichTextLabel_method_install_effect>`.

\*\*Note:\*\* For a **RichTextEffect** to be usable, a BBCode tag must
be defined as a member variable called `bbcode` in the script.

gdscript

\# The RichTextEffect will be usable like this:
<span class="title-ref">\[example\]Some text\[/example\]</span> var
bbcode = "example"

csharp

// The RichTextEffect will be usable like this:
<span class="title-ref">\[example\]Some text\[/example\]</span> string
bbcode = "example";

\*\*Note:\*\* As soon as a `RichTextLabel<class_RichTextLabel>` contains
at least one **RichTextEffect**, it will continuously process the effect
unless the project is paused. This may impact battery life negatively.

classref-introduction-group

## Tutorials

-   `BBCode in RichTextLabel <../tutorials/ui/bbcode_in_richtextlabel>`
-   [RichTextEffect test project
    (third-party)](https://github.com/Eoin-ONeill-Yokai/Godot-Rich-Text-Effect-Test-Project)

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

## Method Descriptions

classref-method

`bool<class_bool>` **\_process\_custom\_fx**(char\_fx:
`CharFXTransform<class_CharFXTransform>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RichTextEffect_private_method__process_custom_fx>`

Override this method to modify properties in `char_fx`. The method must
return `true` if the character could be transformed successfully. If the
method returns `false`, it will skip transformation to avoid displaying
broken text.
