github\_url  
hide

# Script

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `CSharpScript<class_CSharpScript>`,
`GDScript<class_GDScript>`, `ScriptExtension<class_ScriptExtension>`

A class stored as a resource.

classref-introduction-group

## Description

A class stored as a resource. A script extends the functionality of all
objects that instantiate it.

This is the base class for all scripts and should not be used directly.
Trying to create a new script with this class will result in an error.

The `new` method of a script subclass creates a new instance.
`Object.set_script<class_Object_method_set_script>` extends an existing
object, if that object's class matches one of the script's base classes.

classref-introduction-group

## Tutorials

-   `Scripting documentation index <../tutorials/scripting/index>`

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

`String<class_String>` **source\_code**
`🔗<class_Script_property_source_code>`

classref-property-setget

-   `void (No return value.)` **set\_source\_code**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_source\_code**()

The script source code or an empty string if source code is not
available. When set, does not reload the class implementation
automatically.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **can\_instantiate**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Script_method_can_instantiate>`

Returns `true` if the script can be instantiated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Script<class_Script>` **get\_base\_script**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Script_method_get_base_script>`

Returns the script directly inherited by this script.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_global\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Script_method_get_global_name>`

Returns the class name associated with the script, if there is one.
Returns an empty string otherwise.

To give the script a global name, you can use the `class_name` keyword
in GDScript and the `[GlobalClass]` attribute in C#.

gdscript

class\_name MyNode extends Node

csharp

using Godot;

\[GlobalClass\] public partial class MyNode : Node { }

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_instance\_base\_type**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Script_method_get_instance_base_type>`

Returns the script's base type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_property\_default\_value**(property:
`StringName<class_StringName>`)
`🔗<class_Script_method_get_property_default_value>`

Returns the default value of the specified property.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_rpc\_config**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Script_method_get_rpc_config>`

Returns a `Dictionary<class_Dictionary>` mapping method names to their
RPC configuration defined by this script.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_script\_constant\_map**()
`🔗<class_Script_method_get_script_constant_map>`

Returns a dictionary containing constant names and their values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_script\_method\_list**()
`🔗<class_Script_method_get_script_method_list>`

Returns the list of methods in this **Script**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_script\_property\_list**()
`🔗<class_Script_method_get_script_property_list>`

Returns the list of properties in this **Script**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_script\_signal\_list**()
`🔗<class_Script_method_get_script_signal_list>`

Returns the list of user signals defined in this **Script**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_script\_signal**(signal\_name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Script_method_has_script_signal>`

Returns `true` if the script, or a base class, defines a signal with the
given name.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_source\_code**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Script_method_has_source_code>`

Returns `true` if the script contains non-empty source code.

\*\*Note:\*\* If a script does not have source code, this does not mean
that it is invalid or unusable. For example, a
`GDScript<class_GDScript>` that was exported with binary tokenization
has no source code, but still behaves as expected and could be
instantiated. This can be checked with
`can_instantiate<class_Script_method_can_instantiate>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **instance\_has**(base\_object:
`Object<class_Object>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Script_method_instance_has>`

Returns `true` if `base_object` is an instance of this script.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_abstract**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Script_method_is_abstract>`

Returns `true` if the script is an abstract script. An abstract script
does not have a constructor and cannot be instantiated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_tool**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Script_method_is_tool>`

Returns `true` if the script is a tool script. A tool script can run in
the editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **reload**(keep\_state:
`bool<class_bool>` = false) `🔗<class_Script_method_reload>`

Reloads the script's class implementation. Returns an error code.
