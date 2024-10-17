github\_url  
hide

# Object

**Inherited By:** `AudioServer<class_AudioServer>`,
`CameraServer<class_CameraServer>`, `ClassDB<class_ClassDB>`,
`DisplayServer<class_DisplayServer>`,
`EditorFileSystemDirectory<class_EditorFileSystemDirectory>`,
`EditorInterface<class_EditorInterface>`,
`EditorPaths<class_EditorPaths>`,
`EditorSelection<class_EditorSelection>`,
`EditorUndoRedoManager<class_EditorUndoRedoManager>`,
`EditorVCSInterface<class_EditorVCSInterface>`, `Engine<class_Engine>`,
`EngineDebugger<class_EngineDebugger>`,
`FramebufferCacheRD<class_FramebufferCacheRD>`,
`GDExtensionManager<class_GDExtensionManager>`,
`Geometry2D<class_Geometry2D>`, `Geometry3D<class_Geometry3D>`,
`Input<class_Input>`, `InputMap<class_InputMap>`, `IP<class_IP>`,
`JavaClassWrapper<class_JavaClassWrapper>`,
`JavaScriptBridge<class_JavaScriptBridge>`,
`JNISingleton<class_JNISingleton>`, `JSONRPC<class_JSONRPC>`,
`MainLoop<class_MainLoop>`, `Marshalls<class_Marshalls>`,
`MovieWriter<class_MovieWriter>`, `NativeMenu<class_NativeMenu>`,
`NavigationMeshGenerator<class_NavigationMeshGenerator>`,
`NavigationServer2D<class_NavigationServer2D>`,
`NavigationServer3D<class_NavigationServer3D>`, `Node<class_Node>`,
`OpenXRExtensionWrapperExtension<class_OpenXRExtensionWrapperExtension>`,
`OpenXRInteractionProfileMetadata<class_OpenXRInteractionProfileMetadata>`,
`OS<class_OS>`, `Performance<class_Performance>`,
`PhysicsDirectBodyState2D<class_PhysicsDirectBodyState2D>`,
`PhysicsDirectBodyState3D<class_PhysicsDirectBodyState3D>`,
`PhysicsDirectSpaceState2D<class_PhysicsDirectSpaceState2D>`,
`PhysicsDirectSpaceState3D<class_PhysicsDirectSpaceState3D>`,
`PhysicsServer2D<class_PhysicsServer2D>`,
`PhysicsServer2DManager<class_PhysicsServer2DManager>`,
`PhysicsServer3D<class_PhysicsServer3D>`,
`PhysicsServer3DManager<class_PhysicsServer3DManager>`,
`PhysicsServer3DRenderingServerHandler<class_PhysicsServer3DRenderingServerHandler>`,
`ProjectSettings<class_ProjectSettings>`,
`RefCounted<class_RefCounted>`, `RenderData<class_RenderData>`,
`RenderingDevice<class_RenderingDevice>`,
`RenderingServer<class_RenderingServer>`,
`RenderSceneData<class_RenderSceneData>`,
`ResourceLoader<class_ResourceLoader>`,
`ResourceSaver<class_ResourceSaver>`, `ResourceUID<class_ResourceUID>`,
`ScriptLanguage<class_ScriptLanguage>`,
`TextServerManager<class_TextServerManager>`, `ThemeDB<class_ThemeDB>`,
`TileData<class_TileData>`, `Time<class_Time>`,
`TranslationServer<class_TranslationServer>`,
`TreeItem<class_TreeItem>`, `UndoRedo<class_UndoRedo>`,
`UniformSetCacheRD<class_UniformSetCacheRD>`,
`WorkerThreadPool<class_WorkerThreadPool>`, `XRServer<class_XRServer>`,
`XRVRS<class_XRVRS>`

Base class for all other classes in the engine.

classref-introduction-group

## Description

An advanced `Variant<class_Variant>` type. All classes in the engine
inherit from Object. Each class may define new properties, methods or
signals, which are available to all inheriting classes. For example, a
`Sprite2D<class_Sprite2D>` instance is able to call
`Node.add_child<class_Node_method_add_child>` because it inherits from
`Node<class_Node>`.

You can create new instances, using `Object.new()` in GDScript, or
`new GodotObject` in C#.

To delete an Object instance, call `free<class_Object_method_free>`.
This is necessary for most classes inheriting Object, because they do
not manage memory on their own, and will otherwise cause memory leaks
when no longer in use. There are a few classes that perform memory
management. For example, `RefCounted<class_RefCounted>` (and by
extension `Resource<class_Resource>`) deletes itself when no longer
referenced, and `Node<class_Node>` deletes its children when freed.

Objects can have a `Script<class_Script>` attached to them. Once the
`Script<class_Script>` is instantiated, it effectively acts as an
extension to the base class, allowing it to define and inherit new
properties, methods and signals.

Inside a `Script<class_Script>`,
`_get_property_list<class_Object_private_method__get_property_list>` may
be overridden to customize properties in several ways. This allows them
to be available to the editor, display as lists of options, sub-divide
into groups, save on disk, etc. Scripting languages offer easier ways to
customize properties, such as with the
`@GDScript.@export<class_@GDScript_annotation_@export>` annotation.

Godot is very dynamic. An object's script, and therefore its properties,
methods and signals, can be changed at run-time. Because of this, there
can be occasions where, for example, a property required by a method may
not exist. To prevent run-time errors, see methods such as
`set<class_Object_method_set>`, `get<class_Object_method_get>`,
`call<class_Object_method_call>`,
`has_method<class_Object_method_has_method>`,
`has_signal<class_Object_method_has_signal>`, etc. Note that these
methods are **much** slower than direct references.

In GDScript, you can also check if a given property, method, or signal
name exists in an object with the `in` operator:

    var node = Node.new()
    print("name" in node)         # Prints true
    print("get_parent" in node)   # Prints true
    print("tree_entered" in node) # Prints true
    print("unknown" in node)      # Prints false

Notifications are `int<class_int>` constants commonly sent and received
by objects. For example, on every rendered frame, the
`SceneTree<class_SceneTree>` notifies nodes inside the tree with a
`Node.NOTIFICATION_PROCESS<class_Node_constant_NOTIFICATION_PROCESS>`.
The nodes receive it and may call
`Node._process<class_Node_private_method__process>` to update. To make
use of notifications, see
`notification<class_Object_method_notification>` and
`_notification<class_Object_private_method__notification>`.

Lastly, every object can also contain metadata (data about data).
`set_meta<class_Object_method_set_meta>` can be useful to store
information that the object itself does not depend on. To keep your code
clean, making excessive use of metadata is discouraged.

\*\*Note:\*\* Unlike references to a `RefCounted<class_RefCounted>`,
references to an object stored in a variable can become invalid without
being set to `null`. To check if an object has been deleted, do *not*
compare it against `null`. Instead, use
`@GlobalScope.is_instance_valid<class_@GlobalScope_method_is_instance_valid>`.
It's also recommended to inherit from `RefCounted<class_RefCounted>` for
classes storing data instead of **Object**.

\*\*Note:\*\* The `script` is not exposed like most properties. To set
or get an object's `Script<class_Script>` in code, use
`set_script<class_Object_method_set_script>` and
`get_script<class_Object_method_get_script>`, respectively.

classref-introduction-group

## Tutorials

-   `Object class introduction <../contributing/development/core_and_modules/object_class>`
-   `When and how to avoid using nodes for everything <../tutorials/best_practices/node_alternatives>`
-   `Object notifications <../tutorials/best_practices/godot_notifications>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**property\_list\_changed**()
`🔗<class_Object_signal_property_list_changed>`

Emitted when
`notify_property_list_changed<class_Object_method_notify_property_list_changed>`
is called.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**script\_changed**() `🔗<class_Object_signal_script_changed>`

Emitted when the object's script is changed.

\*\*Note:\*\* When this signal is emitted, the new script is not
initialized yet. If you need to access the new script, defer connections
to this signal with
`CONNECT_DEFERRED<class_Object_constant_CONNECT_DEFERRED>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ConnectFlags**: `🔗<enum_Object_ConnectFlags>`

classref-enumeration-constant

`ConnectFlags<enum_Object_ConnectFlags>` **CONNECT\_DEFERRED** = `1`

Deferred connections trigger their `Callable<class_Callable>`s on idle
time (at the end of the frame), rather than instantly.

classref-enumeration-constant

`ConnectFlags<enum_Object_ConnectFlags>` **CONNECT\_PERSIST** = `2`

Persisting connections are stored when the object is serialized (such as
when using `PackedScene.pack<class_PackedScene_method_pack>`). In the
editor, connections created through the Node dock are always persisting.

classref-enumeration-constant

`ConnectFlags<enum_Object_ConnectFlags>` **CONNECT\_ONE\_SHOT** = `4`

One-shot connections disconnect themselves after emission.

classref-enumeration-constant

`ConnectFlags<enum_Object_ConnectFlags>` **CONNECT\_REFERENCE\_COUNTED**
= `8`

Reference-counted connections can be assigned to the same
`Callable<class_Callable>` multiple times. Each disconnection decreases
the internal counter. The signal fully disconnects only when the counter
reaches 0.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**NOTIFICATION\_POSTINITIALIZE** = `0`
`🔗<class_Object_constant_NOTIFICATION_POSTINITIALIZE>`

Notification received when the object is initialized, before its script
is attached. Used internally.

classref-constant

**NOTIFICATION\_PREDELETE** = `1`
`🔗<class_Object_constant_NOTIFICATION_PREDELETE>`

Notification received when the object is about to be deleted. Can be
used like destructors in object-oriented programming languages.

classref-constant

**NOTIFICATION\_EXTENSION\_RELOADED** = `2`
`🔗<class_Object_constant_NOTIFICATION_EXTENSION_RELOADED>`

Notification received when the object finishes hot reloading. This
notification is only sent for extensions classes and derived.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Variant<class_Variant>` **\_get**(property:
`StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__get>`

Override this method to customize the behavior of
`get<class_Object_method_get>`. Should return the given `property`'s
value, or `null` if the `property` should be handled normally.

Combined with `_set<class_Object_private_method__set>` and
`_get_property_list<class_Object_private_method__get_property_list>`,
this method allows defining custom properties, which is particularly
useful for editor plugins. Note that a property must be present in
`get_property_list<class_Object_method_get_property_list>`, otherwise
this method will not be called.

gdscript

func \_get(property):  
if property == "fake\_property":  
print("Getting my property!") return 4

func \_get\_property\_list():  
return \[  
{ "name": "fake\_property", "type": TYPE\_INT }

\]

csharp

public override Variant \_Get(StringName property) { if (property ==
"FakeProperty") { GD.Print("Getting my property!"); return 4; } return
default; }

public override
Godot.Collections.Array&lt;Godot.Collections.Dictionary&gt;
\_GetPropertyList() { return new
Godot.Collections.Array&lt;Godot.Collections.Dictionary&gt;() { new
Godot.Collections.Dictionary() { { "name", "FakeProperty" }, { "type",
(int)Variant.Type.Int } } }; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_property\_list**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__get_property_list>`

Override this method to provide a custom list of additional properties
to handle by the engine.

Should return a property list, as an `Array<class_Array>` of
dictionaries. The result is added to the array of
`get_property_list<class_Object_method_get_property_list>`, and should
be formatted in the same way. Each `Dictionary<class_Dictionary>` must
at least contain the `name` and `type` entries.

You can use
`_property_can_revert<class_Object_private_method__property_can_revert>`
and
`_property_get_revert<class_Object_private_method__property_get_revert>`
to customize the default values of the properties added by this method.

The example below displays a list of numbers shown as words going from
`ZERO` to `FIVE`, with `number_count` controlling the size of the list:

gdscript

@tool extends Node

@export var number\_count = 3:  
set(nc):  
number\_count = nc numbers.resize(number\_count)
notify\_property\_list\_changed()

var numbers = PackedInt32Array(\[0, 0, 0\])

func \_get\_property\_list():  
var properties = \[\]

for i in range(number\_count):  
properties.append({  
"name": "[number]()%d" % i, "type": TYPE\_INT, "hint":
PROPERTY\_HINT\_ENUM, "hint\_string": "ZERO,ONE,TWO,THREE,FOUR,FIVE",

})

return properties

func \_get(property):  
if property.begins\_with("[number]()"):  
var index = property.get\_slice("\_", 1).to\_int() return
numbers\[index\]

func \_set(property, value):  
if property.begins\_with("[number]()"):  
var index = property.get\_slice("\_", 1).to\_int() numbers\[index\] =
value return true

return false

csharp

\[Tool\] public partial class MyNode : Node { private int \_numberCount;

> \[Export\] public int NumberCount { get =&gt; \_numberCount; set {
> \_numberCount = value; \_numbers.Resize(\_numberCount);
> NotifyPropertyListChanged(); } }
>
> private Godot.Collections.Array&lt;int&gt; \_numbers = new();
>
> public override
> Godot.Collections.Array&lt;Godot.Collections.Dictionary&gt;
> \_GetPropertyList() { var properties = new
> Godot.Collections.Array&lt;Godot.Collections.Dictionary&gt;();
>
> > for (int i = 0; i &lt; \_numberCount; i++) { properties.Add(new
> > Godot.Collections.Dictionary() { { "name", $"[number](){i}" }, {
> > "type", (int)Variant.Type.Int }, { "hint", (int)PropertyHint.Enum },
> > { "hint\_string", "Zero,One,Two,Three,Four,Five" }, }); }
> >
> > return properties;
>
> }
>
> public override Variant \_Get(StringName property) { string
> propertyName = property.ToString(); if
> (propertyName.StartsWith("[number]()")) { int index =
> int.Parse(propertyName.Substring("[number]()".Length)); return
> \_numbers\[index\]; } return default; }
>
> public override bool \_Set(StringName property, Variant value) {
> string propertyName = property.ToString(); if
> (propertyName.StartsWith("[number]()")) { int index =
> int.Parse(propertyName.Substring("[number]()".Length));
> \_numbers\[index\] = value.As&lt;int&gt;(); return true; } return
> false; }

}

\*\*Note:\*\* This method is intended for advanced purposes. For most
common use cases, the scripting languages offer easier ways to handle
properties. See `@GDScript.@export<class_@GDScript_annotation_@export>`,
`@GDScript.@export_enum<class_@GDScript_annotation_@export_enum>`,
`@GDScript.@export_group<class_@GDScript_annotation_@export_group>`,
etc. If you want to customize exported properties, use
`_validate_property<class_Object_private_method__validate_property>`.

\*\*Note:\*\* If the object's script is not
`@GDScript.@tool<class_@GDScript_annotation_@tool>`, this method will
not be called in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_init**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__init>`

Called when the object's script is instantiated, oftentimes after the
object is initialized in memory (through `Object.new()` in GDScript, or
`new GodotObject` in C#). It can be also defined to take in parameters.
This method is similar to a constructor in most programming languages.

\*\*Note:\*\* If `_init<class_Object_private_method__init>` is defined
with *required* parameters, the Object with script may only be created
directly. If any other means (such as
`PackedScene.instantiate<class_PackedScene_method_instantiate>` or
`Node.duplicate<class_Node_method_duplicate>`) are used, the script's
initialization will fail.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_iter\_get**(iter: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__iter_get>`

Returns the current iterable value. `iter` stores the iteration state,
but unlike `_iter_init<class_Object_private_method__iter_init>` and
`_iter_next<class_Object_private_method__iter_next>` the state is
supposed to be read-only, so there is no `Array<class_Array>` wrapper.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_iter\_init**(iter: `Array<class_Array>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__iter_init>`

Initializes the iterator. `iter` stores the iteration state. Since
GDScript does not support passing arguments by reference, a
single-element array is used as a wrapper. Returns `true` so long as the
iterator has not reached the end.

Example:

    class MyRange:
        var _from
        var _to

        func _init(from, to):
            assert(from <= to)
            _from = from
            _to = to

        func _iter_init(iter):
            iter[0] = _from
            return iter[0] < _to

        func _iter_next(iter):
            iter[0] += 1
            return iter[0] < _to

        func _iter_get(iter):
            return iter

    func _ready():
        var my_range = MyRange.new(2, 5)
        for x in my_range:
            print(x) # Prints 2, 3, 4.

\*\*Note:\*\* Alternatively, you can ignore `iter` and use the object's
state instead, see [online
docs](../tutorials/scripting/gdscript/gdscript_advanced.html#custom-iterators)
for an example. Note that in this case you will not be able to reuse the
same iterator instance in nested loops. Also, make sure you reset the
iterator state in this method if you want to reuse the same instance
multiple times.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_iter\_next**(iter: `Array<class_Array>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__iter_next>`

Moves the iterator to the next iteration. `iter` stores the iteration
state. Since GDScript does not support passing arguments by reference, a
single-element array is used as a wrapper. Returns `true` so long as the
iterator has not reached the end.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_notification**(what: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__notification>`

Called when the object receives a notification, which can be identified
in `what` by comparing it with a constant. See also
`notification<class_Object_method_notification>`.

gdscript

func \_notification(what):  
if what == NOTIFICATION\_PREDELETE:  
print("Goodbye!")

csharp

public override void \_Notification(int what) { if (what ==
NotificationPredelete) { GD.Print("Goodbye!"); } }

\*\*Note:\*\* The base **Object** defines a few notifications
(`NOTIFICATION_POSTINITIALIZE<class_Object_constant_NOTIFICATION_POSTINITIALIZE>`
and
`NOTIFICATION_PREDELETE<class_Object_constant_NOTIFICATION_PREDELETE>`).
Inheriting classes such as `Node<class_Node>` define a lot more
notifications, which are also received by this method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_property\_can\_revert**(property:
`StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__property_can_revert>`

Override this method to customize the given `property`'s revert
behavior. Should return `true` if the `property` has a custom default
value and is revertible in the Inspector dock. Use
`_property_get_revert<class_Object_private_method__property_get_revert>`
to specify the `property`'s default value.

\*\*Note:\*\* This method must return consistently, regardless of the
current value of the `property`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_property\_get\_revert**(property:
`StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__property_get_revert>`

Override this method to customize the given `property`'s revert
behavior. Should return the default value for the `property`. If the
default value differs from the `property`'s current value, a revert icon
is displayed in the Inspector dock.

\*\*Note:\*\*
`_property_can_revert<class_Object_private_method__property_can_revert>`
must also be overridden for this method to be called.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_set**(property: `StringName<class_StringName>`,
value: `Variant<class_Variant>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__set>`

Override this method to customize the behavior of
`set<class_Object_method_set>`. Should set the `property` to `value` and
return `true`, or `false` if the `property` should be handled normally.
The *exact* way to set the `property` is up to this method's
implementation.

Combined with `_get<class_Object_private_method__get>` and
`_get_property_list<class_Object_private_method__get_property_list>`,
this method allows defining custom properties, which is particularly
useful for editor plugins. Note that a property *must* be present in
`get_property_list<class_Object_method_get_property_list>`, otherwise
this method will not be called.

gdscript

var internal\_data = {}

func \_set(property, value):  
if property == "fake\_property":  
\# Storing the value in the fake property.
internal\_data\["fake\_property"\] = value return true

return false

func \_get\_property\_list():  
return \[  
{ "name": "fake\_property", "type": TYPE\_INT }

\]

csharp

private Godot.Collections.Dictionary \_internalData = new
Godot.Collections.Dictionary();

public override bool \_Set(StringName property, Variant value) { if
(property == "FakeProperty") { // Storing the value in the fake
property. \_internalData\["FakeProperty"\] = value; return true; }

> return false;

}

public override
Godot.Collections.Array&lt;Godot.Collections.Dictionary&gt;
\_GetPropertyList() { return new
Godot.Collections.Array&lt;Godot.Collections.Dictionary&gt;() { new
Godot.Collections.Dictionary() { { "name", "FakeProperty" }, { "type",
(int)Variant.Type.Int } } }; }

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_to\_string**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__to_string>`

Override this method to customize the return value of
`to_string<class_Object_method_to_string>`, and therefore the object's
representation as a `String<class_String>`.

    func _to_string():
        return "Welcome to Godot 4!"

    func _init():
        print(self)       # Prints Welcome to Godot 4!"
        var a = str(self) # a is "Welcome to Godot 4!"

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_validate\_property**(property:
`Dictionary<class_Dictionary>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_Object_private_method__validate_property>`

Override this method to customize existing properties. Every property
info goes through this method, except properties added with
`_get_property_list<class_Object_private_method__get_property_list>`.
The dictionary contents is the same as in
`_get_property_list<class_Object_private_method__get_property_list>`.

gdscript

@tool extends Node

@export var is\_number\_editable: bool:  
set(value):  
is\_number\_editable = value notify\_property\_list\_changed()

@export var number: int

func \_validate\_property(property: Dictionary):  
if property.name == "number" and not is\_number\_editable:  
property.usage |= PROPERTY\_USAGE\_READ\_ONLY

csharp

\[Tool\] public partial class MyNode : Node { private bool
\_isNumberEditable;

> \[Export\] public bool IsNumberEditable { get =&gt;
> \_isNumberEditable; set { \_isNumberEditable = value;
> NotifyPropertyListChanged(); } }
>
> \[Export\] public int Number { get; set; }
>
> public override void \_ValidateProperty(Godot.Collections.Dictionary
> property) { if (property\["name"\].AsStringName() ==
> PropertyName.Number && !IsNumberEditable) { var usage =
> property\["usage"\].As&lt;PropertyUsageFlags&gt;() |
> PropertyUsageFlags.ReadOnly; property\["usage"\] = (int)usage; } }

}

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_user\_signal**(signal:
`String<class_String>`, arguments: `Array<class_Array>` = \[\])
`🔗<class_Object_method_add_user_signal>`

Adds a user-defined `signal`. Optional arguments for the signal can be
added as an `Array<class_Array>` of dictionaries, each defining a `name`
`String<class_String>` and a `type` `int<class_int>` (see
`Variant.Type<enum_@GlobalScope_Variant.Type>`). See also
`has_user_signal<class_Object_method_has_user_signal>` and
`remove_user_signal<class_Object_method_remove_user_signal>`.

gdscript

add\_user\_signal("hurt", \[  
{ "name": "damage", "type": TYPE\_INT }, { "name": "source", "type":
TYPE\_OBJECT }

\])

csharp

AddUserSignal("Hurt", new Godot.Collections.Array() { new
Godot.Collections.Dictionary() { { "name", "damage" }, { "type",
(int)Variant.Type.Int } }, new Godot.Collections.Dictionary() { {
"name", "source" }, { "type", (int)Variant.Type.Object } } });

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **call**(method:
`StringName<class_StringName>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_Object_method_call>`

Calls the `method` on the object and returns the result. This method
supports a variable number of arguments, so parameters can be passed as
a comma separated list.

gdscript

var node = Node3D.new() node.call("rotate", Vector3(1.0, 0.0, 0.0),
1.571)

csharp

var node = new Node3D(); node.Call(Node3D.MethodName.Rotate, new
Vector3(1f, 0f, 0f), 1.571f);

\*\*Note:\*\* In C#, `method` must be in snake\_case when referring to
built-in Godot methods. Prefer using the names exposed in the
`MethodName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **call\_deferred**(method:
`StringName<class_StringName>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_Object_method_call_deferred>`

Calls the `method` on the object during idle time. Always returns null,
**not** the method's result.

Idle time happens mainly at the end of process and physics frames. In
it, deferred calls will be run until there are none left, which means
you can defer calls from other deferred calls and they'll still be run
in the current idle time cycle. This means you should not call a method
deferred from itself (or from a method called by it), as this causes
infinite recursion the same way as if you had called the method
directly.

This method supports a variable number of arguments, so parameters can
be passed as a comma separated list.

gdscript

var node = Node3D.new() node.call\_deferred("rotate", Vector3(1.0, 0.0,
0.0), 1.571)

csharp

var node = new Node3D(); node.CallDeferred(Node3D.MethodName.Rotate, new
Vector3(1f, 0f, 0f), 1.571f);

See also `Callable.call_deferred<class_Callable_method_call_deferred>`.

\*\*Note:\*\* In C#, `method` must be in snake\_case when referring to
built-in Godot methods. Prefer using the names exposed in the
`MethodName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

\*\*Note:\*\* If you're looking to delay the function call by a frame,
refer to the
`SceneTree.process_frame<class_SceneTree_signal_process_frame>` and
`SceneTree.physics_frame<class_SceneTree_signal_physics_frame>` signals.

    var node = Node3D.new()
    # Make a Callable and bind the arguments to the node's rotate() call.
    var callable = node.rotate.bind(Vector3(1.0, 0.0, 0.0), 1.571)
    # Connect the callable to the process_frame signal, so it gets called in the next process frame.
    # CONNECT_ONE_SHOT makes sure it only gets called once instead of every frame.
    get_tree().process_frame.connect(callable, CONNECT_ONE_SHOT)

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **callv**(method:
`StringName<class_StringName>`, arg\_array: `Array<class_Array>`)
`🔗<class_Object_method_callv>`

Calls the `method` on the object and returns the result. Unlike
`call<class_Object_method_call>`, this method expects all parameters to
be contained inside `arg_array`.

gdscript

var node = Node3D.new() node.callv("rotate", \[Vector3(1.0, 0.0, 0.0),
1.571\])

csharp

var node = new Node3D(); node.Callv(Node3D.MethodName.Rotate, new
Godot.Collections.Array { new Vector3(1f, 0f, 0f), 1.571f });

\*\*Note:\*\* In C#, `method` must be in snake\_case when referring to
built-in Godot methods. Prefer using the names exposed in the
`MethodName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **can\_translate\_messages**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_can_translate_messages>`

Returns `true` if the object is allowed to translate messages with
`tr<class_Object_method_tr>` and `tr_n<class_Object_method_tr_n>`. See
also
`set_message_translation<class_Object_method_set_message_translation>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **cancel\_free**()
`🔗<class_Object_method_cancel_free>`

If this method is called during
`NOTIFICATION_PREDELETE<class_Object_constant_NOTIFICATION_PREDELETE>`,
this object will reject being freed and will remain allocated. This is
mostly an internal function used for error handling to avoid the user
from freeing objects when they are not intended to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **connect**(signal:
`StringName<class_StringName>`, callable: `Callable<class_Callable>`,
flags: `int<class_int>` = 0) `🔗<class_Object_method_connect>`

Connects a `signal` by name to a `callable`. Optional `flags` can be
also added to configure the connection's behavior (see
`ConnectFlags<enum_Object_ConnectFlags>` constants).

A signal can only be connected once to the same
`Callable<class_Callable>`. If the signal is already connected, this
method returns
`@GlobalScope.ERR_INVALID_PARAMETER<class_@GlobalScope_constant_ERR_INVALID_PARAMETER>`
and pushes an error message, unless the signal is connected with
`CONNECT_REFERENCE_COUNTED<class_Object_constant_CONNECT_REFERENCE_COUNTED>`.
To prevent this, use `is_connected<class_Object_method_is_connected>`
first to check for existing connections.

If the `callable`'s object is freed, the connection will be lost.

\*\*Examples with recommended syntax:\*\*

Connecting signals is one of the most common operations in Godot and the
API gives many options to do so, which are described further down. The
code block below shows the recommended approach.

gdscript

func \_ready():  
var button = Button.new() \# <span class="title-ref">button\_down</span>
here is a Signal variant type, and we thus call the Signal.connect()
method, not Object.connect(). \# See discussion below for a more
in-depth overview of the API.
button.button\_down.connect(\_on\_button\_down)

\# This assumes that a <span class="title-ref">Player</span> class
exists, which defines a <span class="title-ref">hit</span> signal. var
player = Player.new() \# We use Signal.connect() again, and we also use
the Callable.bind() method, \# which returns a new Callable with the
parameter binds. player.hit.connect(\_on\_player\_hit.bind("sword",
100))

func \_on\_button\_down():  
print("Button down!")

func \_on\_player\_hit(weapon\_type, damage):  
print("Hit with weapon %s for %d damage." % \[weapon\_type, damage\])

csharp

public override void \_Ready() { var button = new Button(); // C#
supports passing signals as events, so we can use this idiomatic
construct: button.ButtonDown += OnButtonDown;

> // This assumes that a <span class="title-ref">Player</span> class
> exists, which defines a <span class="title-ref">Hit</span> signal. var
> player = new Player(); // We can use lambdas when we need to bind
> additional parameters. player.Hit += () =&gt; OnPlayerHit("sword",
> 100);

}

private void OnButtonDown() { GD.Print("Button down!"); }

private void OnPlayerHit(string weaponType, int damage) { GD.Print($"Hit
with weapon {weaponType} for {damage} damage."); }

\*\*`Object.connect()` or `Signal.connect()`?\*\*

As seen above, the recommended method to connect signals is not
`connect<class_Object_method_connect>`. The code block below shows the
four options for connecting signals, using either this legacy method or
the recommended `Signal.connect<class_Signal_method_connect>`, and using
either an implicit `Callable<class_Callable>` or a manually defined one.

gdscript

func \_ready():  
var button = Button.new() \# Option 1: Object.connect() with an implicit
Callable for the defined function. button.connect("button\_down",
\_on\_button\_down) \# Option 2: Object.connect() with a constructed
Callable using a target object and method name.
button.connect("button\_down", Callable(self, "\_on\_button\_down")) \#
Option 3: Signal.connect() with an implicit Callable for the defined
function. button.button\_down.connect(\_on\_button\_down) \# Option 4:
Signal.connect() with a constructed Callable using a target object and
method name. button.button\_down.connect(Callable(self,
"\_on\_button\_down"))

func \_on\_button\_down():  
print("Button down!")

csharp

public override void \_Ready() { var button = new Button(); // Option 1:
In C#, we can use signals as events and connect with this idiomatic
syntax: button.ButtonDown += OnButtonDown; // Option 2:
GodotObject.Connect() with a constructed Callable from a method group.
button.Connect(Button.SignalName.ButtonDown,
Callable.From(OnButtonDown)); // Option 3: GodotObject.Connect() with a
constructed Callable using a target object and method name.
button.Connect(Button.SignalName.ButtonDown, new Callable(this,
MethodName.OnButtonDown)); }

private void OnButtonDown() { GD.Print("Button down!"); }

While all options have the same outcome (`button`'s
`BaseButton.button_down<class_BaseButton_signal_button_down>` signal
will be connected to `_on_button_down`), **option 3** offers the best
validation: it will print a compile-time error if either the
`button_down` `Signal<class_Signal>` or the `_on_button_down`
`Callable<class_Callable>` are not defined. On the other hand, **option
2** only relies on string names and will only be able to validate either
names at runtime: it will print a runtime error if `"button_down"`
doesn't correspond to a signal, or if `"_on_button_down"` is not a
registered method in the object `self`. The main reason for using
options 1, 2, or 4 would be if you actually need to use strings (e.g. to
connect signals programmatically based on strings read from a
configuration file). Otherwise, option 3 is the recommended (and
fastest) method.

\*\*Binding and passing parameters:\*\*

The syntax to bind parameters is through
`Callable.bind<class_Callable_method_bind>`, which returns a copy of the
`Callable<class_Callable>` with its parameters bound.

When calling `emit_signal<class_Object_method_emit_signal>` or
`Signal.emit<class_Signal_method_emit>`, the signal parameters can be
also passed. The examples below show the relationship between these
signal parameters and bound parameters.

gdscript

func \_ready():  
\# This assumes that a <span class="title-ref">Player</span> class
exists, which defines a <span class="title-ref">hit</span> signal. var
player = Player.new() \# Using Callable.bind().
player.hit.connect(\_on\_player\_hit.bind("sword", 100))

\# Parameters added when emitting the signal are passed first.
player.hit.emit("Dark lord", 5)

\# We pass two arguments when emitting
(<span class="title-ref">hit\_by</span>,
<span class="title-ref">level</span>), \# and bind two more arguments
when connecting (<span class="title-ref">weapon\_type</span>,
<span class="title-ref">damage</span>). func \_on\_player\_hit(hit\_by,
level, weapon\_type, damage): print("Hit by %s (level %d) with weapon %s
for %d damage." % \[hit\_by, level, weapon\_type, damage\])

csharp

public override void \_Ready() { // This assumes that a
<span class="title-ref">Player</span> class exists, which defines a
<span class="title-ref">Hit</span> signal. var player = new Player(); //
Using lambda expressions that create a closure that captures the
additional parameters. // The lambda only receives the parameters
defined by the signal's delegate. player.Hit += (hitBy, level) =&gt;
OnPlayerHit(hitBy, level, "sword", 100);

> // Parameters added when emitting the signal are passed first.
> player.EmitSignal(SignalName.Hit, "Dark lord", 5);

}

// We pass two arguments when emitting
(<span class="title-ref">hit\_by</span>,
<span class="title-ref">level</span>), // and bind two more arguments
when connecting (<span class="title-ref">weapon\_type</span>,
<span class="title-ref">damage</span>). private void OnPlayerHit(string
hitBy, int level, string weaponType, int damage) { GD.Print($"Hit by
{hitBy} (level {level}) with weapon {weaponType} for {damage} damage.");
}

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **disconnect**(signal:
`StringName<class_StringName>`, callable: `Callable<class_Callable>`)
`🔗<class_Object_method_disconnect>`

Disconnects a `signal` by name from a given `callable`. If the
connection does not exist, generates an error. Use
`is_connected<class_Object_method_is_connected>` to make sure that the
connection exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **emit\_signal**(signal:
`StringName<class_StringName>`, ...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`🔗<class_Object_method_emit_signal>`

Emits the given `signal` by name. The signal must exist, so it should be
a built-in signal of this class or one of its inherited classes, or a
user-defined signal (see
`add_user_signal<class_Object_method_add_user_signal>`). This method
supports a variable number of arguments, so parameters can be passed as
a comma separated list.

Returns
`@GlobalScope.ERR_UNAVAILABLE<class_@GlobalScope_constant_ERR_UNAVAILABLE>`
if `signal` does not exist or the parameters are invalid.

gdscript

emit\_signal("hit", "sword", 100) emit\_signal("game\_over")

csharp

EmitSignal(SignalName.Hit, "sword", 100);
EmitSignal(SignalName.GameOver);

\*\*Note:\*\* In C#, `signal` must be in snake\_case when referring to
built-in Godot signals. Prefer using the names exposed in the
`SignalName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **free**() `🔗<class_Object_method_free>`

Deletes the object from memory. Pre-existing references to the object
become invalid, and any attempt to access them will result in a run-time
error. Checking the references with
`@GlobalScope.is_instance_valid<class_@GlobalScope_method_is_instance_valid>`
will return `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get**(property:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get>`

Returns the `Variant<class_Variant>` value of the given `property`. If
the `property` does not exist, this method returns `null`.

gdscript

var node = Node2D.new() node.rotation = 1.5 var a = node.get("rotation")
\# a is 1.5

csharp

var node = new Node2D(); node.Rotation = 1.5f; var a =
node.Get(Node2D.PropertyName.Rotation); // a is 1.5

\*\*Note:\*\* In C#, `property` must be in snake\_case when referring to
built-in Godot properties. Prefer using the names exposed in the
`PropertyName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_class**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_class>`

Returns the object's built-in class name, as a `String<class_String>`.
See also `is_class<class_Object_method_is_class>`.

\*\*Note:\*\* This method ignores `class_name` declarations. If this
object's script has defined a `class_name`, the base, built-in class
name is returned instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_incoming\_connections**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_incoming_connections>`

Returns an `Array<class_Array>` of signal connections received by this
object. Each connection is represented as a
`Dictionary<class_Dictionary>` that contains three entries:

-   `signal` is a reference to the `Signal<class_Signal>`;
-   `callable` is a reference to the `Callable<class_Callable>`;
-   `flags` is a combination of
    `ConnectFlags<enum_Object_ConnectFlags>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_indexed**(property\_path:
`NodePath<class_NodePath>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_indexed>`

Gets the object's property indexed by the given `property_path`. The
path should be a `NodePath<class_NodePath>` relative to the current
object and can use the colon character (`:`) to access nested
properties.

\*\*Examples:\*\* `"position:x"` or `"material:next_pass:blend_mode"`.

gdscript

var node = Node2D.new() node.position = Vector2(5, -10) var a =
node.get\_indexed("position") \# a is Vector2(5, -10) var b =
node.get\_indexed("position:y") \# b is -10

csharp

var node = new Node2D(); node.Position = new Vector2(5, -10); var a =
node.GetIndexed("position"); // a is Vector2(5, -10) var b =
node.GetIndexed("position:y"); // b is -10

\*\*Note:\*\* In C#, `property_path` must be in snake\_case when
referring to built-in Godot properties. Prefer using the names exposed
in the `PropertyName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

\*\*Note:\*\* This method does not support actual paths to nodes in the
`SceneTree<class_SceneTree>`, only sub-property paths. In the context of
nodes, use
`Node.get_node_and_resource<class_Node_method_get_node_and_resource>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_instance\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_instance_id>`

Returns the object's unique instance ID. This ID can be saved in
`EncodedObjectAsID<class_EncodedObjectAsID>`, and can be used to
retrieve this object instance with
`@GlobalScope.instance_from_id<class_@GlobalScope_method_instance_from_id>`.

\*\*Note:\*\* This ID is only useful during the current session. It
won't correspond to a similar object if the ID is sent over a network,
or loaded from a file at a later time.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_meta**(name:
`StringName<class_StringName>`, default: `Variant<class_Variant>` =
null)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_meta>`

Returns the object's metadata value for the given entry `name`. If the
entry does not exist, returns `default`. If `default` is `null`, an
error is also generated.

\*\*Note:\*\* A metadata's name must be a valid identifier as per
`StringName.is_valid_identifier<class_StringName_method_is_valid_identifier>`
method.

\*\*Note:\*\* Metadata that has a name starting with an underscore (`_`)
is considered editor-only. Editor-only metadata is not displayed in the
Inspector and should not be edited, although it can still be found by
this method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`StringName<class_StringName>`\]
**get\_meta\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_meta_list>`

Returns the object's metadata entry names as a
`PackedStringArray<class_PackedStringArray>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_method\_argument\_count**(method:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_method_argument_count>`

Returns the number of arguments of the given `method` by name.

\*\*Note:\*\* In C#, `method` must be in snake\_case when referring to
built-in Godot methods. Prefer using the names exposed in the
`MethodName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_method\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_method_list>`

Returns this object's methods and their signatures as an
`Array<class_Array>` of dictionaries. Each
`Dictionary<class_Dictionary>` contains the following entries:

-   `name` is the name of the method, as a `String<class_String>`;
-   `args` is an `Array<class_Array>` of dictionaries representing the
    arguments;
-   `default_args` is the default arguments as an `Array<class_Array>`
    of variants;
-   `flags` is a combination of
    `MethodFlags<enum_@GlobalScope_MethodFlags>`;
-   `id` is the method's internal identifier `int<class_int>`;
-   `return` is the returned value, as a `Dictionary<class_Dictionary>`;

\*\*Note:\*\* The dictionaries of `args` and `return` are formatted
identically to the results of
`get_property_list<class_Object_method_get_property_list>`, although not
all entries are used.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_property\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_property_list>`

Returns the object's property list as an `Array<class_Array>` of
dictionaries. Each `Dictionary<class_Dictionary>` contains the following
entries:

-   `name` is the property's name, as a `String<class_String>`;
-   `class_name` is an empty `StringName<class_StringName>`, unless the
    property is
    `@GlobalScope.TYPE_OBJECT<class_@GlobalScope_constant_TYPE_OBJECT>`
    and it inherits from a class;
-   `type` is the property's type, as an `int<class_int>` (see
    `Variant.Type<enum_@GlobalScope_Variant.Type>`);
-   `hint` is *how* the property is meant to be edited (see
    `PropertyHint<enum_@GlobalScope_PropertyHint>`);
-   `hint_string` depends on the hint (see
    `PropertyHint<enum_@GlobalScope_PropertyHint>`);
-   `usage` is a combination of
    `PropertyUsageFlags<enum_@GlobalScope_PropertyUsageFlags>`.

\*\*Note:\*\* In GDScript, all class members are treated as properties.
In C# and GDExtension, it may be necessary to explicitly mark class
members as Godot properties using decorators or attributes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_script**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_script>`

Returns the object's `Script<class_Script>` instance, or `null` if no
script is attached.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_signal\_connection\_list**(signal:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_signal_connection_list>`

Returns an `Array<class_Array>` of connections for the given `signal`
name. Each connection is represented as a `Dictionary<class_Dictionary>`
that contains three entries:

-   `signal` is a reference to the `Signal<class_Signal>`;
-   `callable` is a reference to the connected
    `Callable<class_Callable>`;
-   `flags` is a combination of
    `ConnectFlags<enum_Object_ConnectFlags>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_signal\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_signal_list>`

Returns the list of existing signals as an `Array<class_Array>` of
dictionaries.

\*\*Note:\*\* Due of the implementation, each
`Dictionary<class_Dictionary>` is formatted very similarly to the
returned values of
`get_method_list<class_Object_method_get_method_list>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_translation\_domain**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_get_translation_domain>`

Returns the name of the translation domain used by
`tr<class_Object_method_tr>` and `tr_n<class_Object_method_tr_n>`. See
also `TranslationServer<class_TranslationServer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_connections**(signal:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_has_connections>`

Returns `true` if any connection exists on the given `signal` name.

\*\*Note:\*\* In C#, `signal` must be in snake\_case when referring to
built-in Godot methods. Prefer using the names exposed in the
`SignalName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_meta**(name: `StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_has_meta>`

Returns `true` if a metadata entry is found with the given `name`. See
also `get_meta<class_Object_method_get_meta>`,
`set_meta<class_Object_method_set_meta>` and
`remove_meta<class_Object_method_remove_meta>`.

\*\*Note:\*\* A metadata's name must be a valid identifier as per
`StringName.is_valid_identifier<class_StringName_method_is_valid_identifier>`
method.

\*\*Note:\*\* Metadata that has a name starting with an underscore (`_`)
is considered editor-only. Editor-only metadata is not displayed in the
Inspector and should not be edited, although it can still be found by
this method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_method**(method:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_has_method>`

Returns `true` if the given `method` name exists in the object.

\*\*Note:\*\* In C#, `method` must be in snake\_case when referring to
built-in Godot methods. Prefer using the names exposed in the
`MethodName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_signal**(signal:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_has_signal>`

Returns `true` if the given `signal` name exists in the object.

\*\*Note:\*\* In C#, `signal` must be in snake\_case when referring to
built-in Godot methods. Prefer using the names exposed in the
`SignalName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_user\_signal**(signal:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_has_user_signal>`

Returns `true` if the given user-defined `signal` name exists. Only
signals added with
`add_user_signal<class_Object_method_add_user_signal>` are included. See
also `remove_user_signal<class_Object_method_remove_user_signal>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_blocking\_signals**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_is_blocking_signals>`

Returns `true` if the object is blocking its signals from being emitted.
See `set_block_signals<class_Object_method_set_block_signals>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_class**(class: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_is_class>`

Returns `true` if the object inherits from the given `class`. See also
`get_class<class_Object_method_get_class>`.

gdscript

var sprite2d = Sprite2D.new() sprite2d.is\_class("Sprite2D") \# Returns
true sprite2d.is\_class("Node") \# Returns true
sprite2d.is\_class("Node3D") \# Returns false

csharp

var sprite2D = new Sprite2D(); sprite2D.IsClass("Sprite2D"); // Returns
true sprite2D.IsClass("Node"); // Returns true
sprite2D.IsClass("Node3D"); // Returns false

\*\*Note:\*\* This method ignores `class_name` declarations in the
object's script.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_connected**(signal:
`StringName<class_StringName>`, callable: `Callable<class_Callable>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_is_connected>`

Returns `true` if a connection exists between the given `signal` name
and `callable`.

\*\*Note:\*\* In C#, `signal` must be in snake\_case when referring to
built-in Godot methods. Prefer using the names exposed in the
`SignalName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_queued\_for\_deletion**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_is_queued_for_deletion>`

Returns `true` if the `Node.queue_free<class_Node_method_queue_free>`
method was called for the object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **notification**(what: `int<class_int>`,
reversed: `bool<class_bool>` = false)
`🔗<class_Object_method_notification>`

Sends the given `what` notification to all classes inherited by the
object, triggering calls to
`_notification<class_Object_private_method__notification>`, starting
from the highest ancestor (the **Object** class) and going down to the
object's script.

If `reversed` is `true`, the call order is reversed.

gdscript

var player = Node2D.new() player.set\_script(load("<res://player.gd>"))

player.notification(NOTIFICATION\_ENTER\_TREE) \# The call order is
Object -&gt; Node -&gt; Node2D -&gt; player.gd.

player.notification(NOTIFICATION\_ENTER\_TREE, true) \# The call order
is player.gd -&gt; Node2D -&gt; Node -&gt; Object.

csharp

var player = new Node2D();
player.SetScript(GD.Load("<res://player.gd>"));

player.Notification(NotificationEnterTree); // The call order is
GodotObject -&gt; Node -&gt; Node2D -&gt; player.gd.

player.Notification(NotificationEnterTree, true); // The call order is
player.gd -&gt; Node2D -&gt; Node -&gt; GodotObject.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **notify\_property\_list\_changed**()
`🔗<class_Object_method_notify_property_list_changed>`

Emits the
`property_list_changed<class_Object_signal_property_list_changed>`
signal. This is mainly used to refresh the editor, so that the Inspector
and editor plugins are properly updated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **property\_can\_revert**(property:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_property_can_revert>`

Returns `true` if the given `property` has a custom default value. Use
`property_get_revert<class_Object_method_property_get_revert>` to get
the `property`'s default value.

\*\*Note:\*\* This method is used by the Inspector dock to display a
revert icon. The object must implement
`_property_can_revert<class_Object_private_method__property_can_revert>`
to customize the default value. If
`_property_can_revert<class_Object_private_method__property_can_revert>`
is not implemented, this method returns `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **property\_get\_revert**(property:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_property_get_revert>`

Returns the custom default value of the given `property`. Use
`property_can_revert<class_Object_method_property_can_revert>` to check
if the `property` has a custom default value.

\*\*Note:\*\* This method is used by the Inspector dock to display a
revert icon. The object must implement
`_property_get_revert<class_Object_private_method__property_get_revert>`
to customize the default value. If
`_property_get_revert<class_Object_private_method__property_get_revert>`
is not implemented, this method returns `null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_meta**(name:
`StringName<class_StringName>`) `🔗<class_Object_method_remove_meta>`

Removes the given entry `name` from the object's metadata. See also
`has_meta<class_Object_method_has_meta>`,
`get_meta<class_Object_method_get_meta>` and
`set_meta<class_Object_method_set_meta>`.

\*\*Note:\*\* A metadata's name must be a valid identifier as per
`StringName.is_valid_identifier<class_StringName_method_is_valid_identifier>`
method.

\*\*Note:\*\* Metadata that has a name starting with an underscore (`_`)
is considered editor-only. Editor-only metadata is not displayed in the
Inspector and should not be edited, although it can still be found by
this method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_user\_signal**(signal:
`StringName<class_StringName>`)
`🔗<class_Object_method_remove_user_signal>`

Removes the given user signal `signal` from the object. See also
`add_user_signal<class_Object_method_add_user_signal>` and
`has_user_signal<class_Object_method_has_user_signal>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set**(property:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`🔗<class_Object_method_set>`

Assigns `value` to the given `property`. If the property does not exist
or the given `value`'s type doesn't match, nothing happens.

gdscript

var node = Node2D.new() node.set("global\_scale", Vector2(8, 2.5))
print(node.global\_scale) \# Prints (8, 2.5)

csharp

var node = new Node2D(); node.Set(Node2D.PropertyName.GlobalScale, new
Vector2(8, 2.5)); GD.Print(node.GlobalScale); // Prints Vector2(8, 2.5)

\*\*Note:\*\* In C#, `property` must be in snake\_case when referring to
built-in Godot properties. Prefer using the names exposed in the
`PropertyName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_block\_signals**(enable:
`bool<class_bool>`) `🔗<class_Object_method_set_block_signals>`

If set to `true`, the object becomes unable to emit signals. As such,
`emit_signal<class_Object_method_emit_signal>` and signal connections
will not work, until it is set to `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_deferred**(property:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`🔗<class_Object_method_set_deferred>`

Assigns `value` to the given `property`, at the end of the current
frame. This is equivalent to calling `set<class_Object_method_set>`
through `call_deferred<class_Object_method_call_deferred>`.

gdscript

var node = Node2D.new() add\_child(node)

node.rotation = 1.5 node.set\_deferred("rotation", 3.0)
print(node.rotation) \# Prints 1.5

await get\_tree().process\_frame print(node.rotation) \# Prints 3.0

csharp

var node = new Node2D(); node.Rotation = 1.5f;
node.SetDeferred(Node2D.PropertyName.Rotation, 3f);
GD.Print(node.Rotation); // Prints 1.5

await ToSignal(GetTree(), SceneTree.SignalName.ProcessFrame);
GD.Print(node.Rotation); // Prints 3.0

\*\*Note:\*\* In C#, `property` must be in snake\_case when referring to
built-in Godot properties. Prefer using the names exposed in the
`PropertyName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_indexed**(property\_path:
`NodePath<class_NodePath>`, value: `Variant<class_Variant>`)
`🔗<class_Object_method_set_indexed>`

Assigns a new `value` to the property identified by the `property_path`.
The path should be a `NodePath<class_NodePath>` relative to this object,
and can use the colon character (`:`) to access nested properties.

gdscript

var node = Node2D.new() node.set\_indexed("position", Vector2(42, 0))
node.set\_indexed("position:y", -10) print(node.position) \# Prints (42,
-10)

csharp

var node = new Node2D(); node.SetIndexed("position", new Vector2(42,
0)); node.SetIndexed("position:y", -10); GD.Print(node.Position); //
Prints (42, -10)

\*\*Note:\*\* In C#, `property_path` must be in snake\_case when
referring to built-in Godot properties. Prefer using the names exposed
in the `PropertyName` class to avoid allocating a new
`StringName<class_StringName>` on each call.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_message\_translation**(enable:
`bool<class_bool>`) `🔗<class_Object_method_set_message_translation>`

If set to `true`, allows the object to translate messages with
`tr<class_Object_method_tr>` and `tr_n<class_Object_method_tr_n>`.
Enabled by default. See also
`can_translate_messages<class_Object_method_can_translate_messages>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_meta**(name:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`🔗<class_Object_method_set_meta>`

Adds or changes the entry `name` inside the object's metadata. The
metadata `value` can be any `Variant<class_Variant>`, although some
types cannot be serialized correctly.

If `value` is `null`, the entry is removed. This is the equivalent of
using `remove_meta<class_Object_method_remove_meta>`. See also
`has_meta<class_Object_method_has_meta>` and
`get_meta<class_Object_method_get_meta>`.

\*\*Note:\*\* A metadata's name must be a valid identifier as per
`StringName.is_valid_identifier<class_StringName_method_is_valid_identifier>`
method.

\*\*Note:\*\* Metadata that has a name starting with an underscore (`_`)
is considered editor-only. Editor-only metadata is not displayed in the
Inspector and should not be edited, although it can still be found by
this method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_script**(script:
`Variant<class_Variant>`) `🔗<class_Object_method_set_script>`

Attaches `script` to the object, and instantiates it. As a result, the
script's `_init<class_Object_private_method__init>` is called. A
`Script<class_Script>` is used to extend the object's functionality.

If a script already exists, its instance is detached, and its property
values and state are lost. Built-in property values are still kept.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_translation\_domain**(domain:
`StringName<class_StringName>`)
`🔗<class_Object_method_set_translation_domain>`

Sets the name of the translation domain used by
`tr<class_Object_method_tr>` and `tr_n<class_Object_method_tr_n>`. See
also `TranslationServer<class_TranslationServer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **to\_string**()
`🔗<class_Object_method_to_string>`

Returns a `String<class_String>` representing the object. Defaults to
`"<ClassName#RID>"`. Override
`_to_string<class_Object_private_method__to_string>` to customize the
string representation of the object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **tr**(message: `StringName<class_StringName>`,
context: `StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_tr>`

Translates a `message`, using the translation catalogs configured in the
Project Settings. Further `context` can be specified to help with the
translation. Note that most `Control<class_Control>` nodes automatically
translate their strings, so this method is mostly useful for formatted
strings or custom drawn text.

If `can_translate_messages<class_Object_method_can_translate_messages>`
is `false`, or no translation is available, this method returns the
`message` without changes. See
`set_message_translation<class_Object_method_set_message_translation>`.

For detailed examples, see
`Internationalizing games <../tutorials/i18n/internationalizing_games>`.

\*\*Note:\*\* This method can't be used without an **Object** instance,
as it requires the
`can_translate_messages<class_Object_method_can_translate_messages>`
method. To translate strings in a static context, use
`TranslationServer.translate<class_TranslationServer_method_translate>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **tr\_n**(message:
`StringName<class_StringName>`, plural\_message:
`StringName<class_StringName>`, n: `int<class_int>`, context:
`StringName<class_StringName>` = &"")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Object_method_tr_n>`

Translates a `message` or `plural_message`, using the translation
catalogs configured in the Project Settings. Further `context` can be
specified to help with the translation.

If `can_translate_messages<class_Object_method_can_translate_messages>`
is `false`, or no translation is available, this method returns
`message` or `plural_message`, without changes. See
`set_message_translation<class_Object_method_set_message_translation>`.

The `n` is the number, or amount, of the message's subject. It is used
by the translation system to fetch the correct plural form for the
current language.

For detailed examples, see
`Localization using gettext <../tutorials/i18n/localization_using_gettext>`.

\*\*Note:\*\* Negative and `float<class_float>` numbers may not properly
apply to some countable subjects. It's recommended to handle these cases
with `tr<class_Object_method_tr>`.

\*\*Note:\*\* This method can't be used without an **Object** instance,
as it requires the
`can_translate_messages<class_Object_method_can_translate_messages>`
method. To translate strings in a static context, use
`TranslationServer.translate_plural<class_TranslationServer_method_translate_plural>`.
