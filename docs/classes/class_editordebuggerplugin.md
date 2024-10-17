github\_url  
hide

# EditorDebuggerPlugin

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

A base class to implement debugger plugins.

classref-introduction-group

## Description

**EditorDebuggerPlugin** provides functions related to the editor side
of the debugger.

To interact with the debugger, an instance of this class must be added
to the editor via
`EditorPlugin.add_debugger_plugin<class_EditorPlugin_method_add_debugger_plugin>`.

Once added, the
`_setup_session<class_EditorDebuggerPlugin_private_method__setup_session>`
callback will be called for every
`EditorDebuggerSession<class_EditorDebuggerSession>` available to the
plugin, and when new ones are created (the sessions may be inactive
during this stage).

You can retrieve the available
`EditorDebuggerSession<class_EditorDebuggerSession>`s via
`get_sessions<class_EditorDebuggerPlugin_method_get_sessions>` or get a
specific one via
`get_session<class_EditorDebuggerPlugin_method_get_session>`.

gdscript

@tool extends EditorPlugin

class ExampleEditorDebugger extends EditorDebuggerPlugin:

> func \_has\_capture(prefix):  
> \# Return true if you wish to handle message with this prefix. return
> prefix == "my\_plugin"
>
> func \_capture(message, data, session\_id):  
> if message == "my\_plugin:ping":  
> get\_session(session\_id).send\_message("my\_plugin:echo", data)
>
> func \_setup\_session(session\_id):  
> \# Add a new tab in the debugger session UI containing a label. var
> label = Label.new() label.name = "Example plugin" label.text =
> "Example plugin" var session = get\_session(session\_id) \# Listens to
> the session started and stopped signals. session.started.connect(func
> (): print("Session started")) session.stopped.connect(func ():
> print("Session stopped")) session.add\_session\_tab(label)

var debugger = ExampleEditorDebugger.new()

func \_enter\_tree():  
add\_debugger\_plugin(debugger)

func \_exit\_tree():  
remove\_debugger\_plugin(debugger)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_breakpoint\_set\_in\_tree**(script:
`Script<class_Script>`, line: `int<class_int>`, enabled:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorDebuggerPlugin_private_method__breakpoint_set_in_tree>`

Override this method to be notified when a breakpoint is set in the
editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_breakpoints\_cleared\_in\_tree**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorDebuggerPlugin_private_method__breakpoints_cleared_in_tree>`

Override this method to be notified when all breakpoints are cleared in
the editor.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_capture**(message: `String<class_String>`, data:
`Array<class_Array>`, session\_id: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorDebuggerPlugin_private_method__capture>`

Override this method to process incoming messages. The `session_id` is
the ID of the `EditorDebuggerSession<class_EditorDebuggerSession>` that
received the message (which you can retrieve via
`get_session<class_EditorDebuggerPlugin_method_get_session>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_goto\_script\_line**(script:
`Script<class_Script>`, line: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorDebuggerPlugin_private_method__goto_script_line>`

Override this method to be notified when a breakpoint line has been
clicked in the debugger breakpoint panel.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_has\_capture**(capture: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorDebuggerPlugin_private_method__has_capture>`

Override this method to enable receiving messages from the debugger. If
`capture` is "my\_message" then messages starting with "my\_message:"
will be passes to the
`_capture<class_EditorDebuggerPlugin_private_method__capture>` method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_setup\_session**(session\_id:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorDebuggerPlugin_private_method__setup_session>`

Override this method to be notified whenever a new
`EditorDebuggerSession<class_EditorDebuggerSession>` is created (the
session may be inactive during this stage).

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorDebuggerSession<class_EditorDebuggerSession>`
**get\_session**(id: `int<class_int>`)
`🔗<class_EditorDebuggerPlugin_method_get_session>`

Returns the `EditorDebuggerSession<class_EditorDebuggerSession>` with
the given `id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_sessions**()
`🔗<class_EditorDebuggerPlugin_method_get_sessions>`

Returns an array of `EditorDebuggerSession<class_EditorDebuggerSession>`
currently available to this debugger plugin.

\*\*Note:\*\* Sessions in the array may be inactive, check their state
via
`EditorDebuggerSession.is_active<class_EditorDebuggerSession_method_is_active>`.
