github\_url  
hide

# GDScript

**Inherits:** `Script<class_Script>` **&lt;** `Resource<class_Resource>`
**&lt;** `RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

A script implemented in the GDScript programming language.

classref-introduction-group

## Description

A script implemented in the GDScript programming language, saved with
the `.gd` extension. The script extends the functionality of all objects
that instantiate it.

Calling `new<class_GDScript_method_new>` creates a new instance of the
script. `Object.set_script<class_Object_method_set_script>` extends an
existing object, if that object's class matches one of the script's base
classes.

If you are looking for GDScript's built-in functions, see
`@GDScript<class_@GDScript>` instead.

classref-introduction-group

## Tutorials

-   `GDScript documentation index <../tutorials/scripting/gdscript/index>`

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

`Variant<class_Variant>` **new**(...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_GDScript_method_new>`

Returns a new instance of the script.

For example:

    var MyClass = load("myclass.gd")
    var instance = MyClass.new()
    assert(instance.get_script() == MyClass)
