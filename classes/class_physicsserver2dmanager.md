github\_url  
hide

# PhysicsServer2DManager

**Inherits:** `Object<class_Object>`

A singleton for managing `PhysicsServer2D<class_PhysicsServer2D>`
implementations.

classref-introduction-group

## Description

**PhysicsServer2DManager** is the API for registering
`PhysicsServer2D<class_PhysicsServer2D>` implementations and for setting
the default implementation.

\*\*Note:\*\* It is not possible to switch physics servers at runtime.
This class is only used on startup at the server initialization level,
by Godot itself and possibly by GDExtensions.

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

`void (No return value.)` **register\_server**(name:
`String<class_String>`, create\_callback: `Callable<class_Callable>`)
`🔗<class_PhysicsServer2DManager_method_register_server>`

Register a `PhysicsServer2D<class_PhysicsServer2D>` implementation by
passing a `name` and a `Callable<class_Callable>` that returns a
`PhysicsServer2D<class_PhysicsServer2D>` object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_default\_server**(name:
`String<class_String>`, priority: `int<class_int>`)
`🔗<class_PhysicsServer2DManager_method_set_default_server>`

Set the default `PhysicsServer2D<class_PhysicsServer2D>` implementation
to the one identified by `name`, if `priority` is greater than the
priority of the current default implementation.
