github\_url  
hide

# Signal

A built-in type representing a signal of an `Object<class_Object>`.

classref-introduction-group

## Description

**Signal** is a built-in `Variant<class_Variant>` type that represents a
signal of an `Object<class_Object>` instance. Like all
`Variant<class_Variant>` types, it can be stored in variables and passed
to functions. Signals allow all connected `Callable<class_Callable>`s
(and by extension their respective objects) to listen and react to
events, without directly referencing one another. This keeps the code
flexible and easier to manage. You can check whether an
`Object<class_Object>` has a given signal name using
`Object.has_signal<class_Object_method_has_signal>`.

In GDScript, signals can be declared with the `signal` keyword. In C#,
you may use the `[Signal]` attribute on a delegate.

gdscript

signal attacked

\# Additional arguments may be declared. \# These arguments must be
passed when the signal is emitted. signal item\_dropped(item\_name,
amount)

csharp

\[Signal\] delegate void AttackedEventHandler();

// Additional arguments may be declared. // These arguments must be
passed when the signal is emitted. \[Signal\] delegate void
ItemDroppedEventHandler(string itemName, int amount);

Note

There are notable differences when using this API with C#. See
`doc_c_sharp_differences` for more information.

classref-introduction-group

## Tutorials

-   `Using Signals <../getting_started/step_by_step/signals>`
-   [GDScript
    Basics](../tutorials/scripting/gdscript/gdscript_basics.html#signals)

classref-reftable-group

## Constructors

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

## Operators

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

## Constructor Descriptions

classref-constructor

`Signal<class_Signal>` **Signal**()
`🔗<class_Signal_constructor_Signal>`

Constructs an empty **Signal** with no object nor signal name bound.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Signal<class_Signal>` **Signal**(from: `Signal<class_Signal>`)

Constructs a **Signal** as a copy of the given **Signal**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Signal<class_Signal>` **Signal**(object: `Object<class_Object>`,
signal: `StringName<class_StringName>`)

Creates a **Signal** object referencing a signal named `signal` in the
specified `object`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **connect**(callable: `Callable<class_Callable>`,
flags: `int<class_int>` = 0) `🔗<class_Signal_method_connect>`

Connects this signal to the specified `callable`. Optional `flags` can
be also added to configure the connection's behavior (see
`ConnectFlags<enum_Object_ConnectFlags>` constants). You can provide
additional arguments to the connected `callable` by using
`Callable.bind<class_Callable_method_bind>`.

A signal can only be connected once to the same
`Callable<class_Callable>`. If the signal is already connected, returns
`@GlobalScope.ERR_INVALID_PARAMETER<class_@GlobalScope_constant_ERR_INVALID_PARAMETER>`
and pushes an error message, unless the signal is connected with
`Object.CONNECT_REFERENCE_COUNTED<class_Object_constant_CONNECT_REFERENCE_COUNTED>`.
To prevent this, use `is_connected<class_Signal_method_is_connected>`
first to check for existing connections.

    for button in $Buttons.get_children():
        button.pressed.connect(_on_pressed.bind(button))

    func _on_pressed(button):
        print(button.name, " was pressed")

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **disconnect**(callable:
`Callable<class_Callable>`) `🔗<class_Signal_method_disconnect>`

Disconnects this signal from the specified `Callable<class_Callable>`.
If the connection does not exist, generates an error. Use
`is_connected<class_Signal_method_is_connected>` to make sure that the
connection exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **emit**(...)
`vararg (This method accepts any number of arguments after the ones described here.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Signal_method_emit>`

Emits this signal. All `Callable<class_Callable>`s connected to this
signal will be triggered. This method supports a variable number of
arguments, so parameters can be passed as a comma separated list.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_connections**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Signal_method_get_connections>`

Returns an `Array<class_Array>` of connections for this signal. Each
connection is represented as a `Dictionary<class_Dictionary>` that
contains three entries:

-   `signal` is a reference to this signal;
-   `callable` is a reference to the connected
    `Callable<class_Callable>`;
-   `flags` is a combination of
    `ConnectFlags<enum_Object_ConnectFlags>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Signal_method_get_name>`

Returns the name of this signal.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Object<class_Object>` **get\_object**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Signal_method_get_object>`

Returns the object emitting this signal.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_object\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Signal_method_get_object_id>`

Returns the ID of the object emitting this signal (see
`Object.get_instance_id<class_Object_method_get_instance_id>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_connections**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Signal_method_has_connections>`

Returns `true` if any `Callable<class_Callable>` is connected to this
signal.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_connected**(callable:
`Callable<class_Callable>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Signal_method_is_connected>`

Returns `true` if the specified `Callable<class_Callable>` is connected
to this signal.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_null**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Signal_method_is_null>`

Returns `true` if this **Signal** has no object and the signal name is
empty. Equivalent to `signal == Signal()`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Operator Descriptions

classref-operator

`bool<class_bool>` **operator !=**(right: `Signal<class_Signal>`)
`🔗<class_Signal_operator_neq_Signal>`

Returns `true` if the signals do not share the same object and name.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right: `Signal<class_Signal>`)
`🔗<class_Signal_operator_eq_Signal>`

Returns `true` if both signals share the same object and name.
