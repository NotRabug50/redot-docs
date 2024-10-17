github\_url  
hide

# EngineDebugger

**Inherits:** `Object<class_Object>`

Exposes the internal debugger.

classref-introduction-group

## Description

**EngineDebugger** handles the communication between the editor and the
running game. It is active in the running game. Messages can be
sent/received through it. It also manages the profilers.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **clear\_breakpoints**()
`🔗<class_EngineDebugger_method_clear_breakpoints>`

Clears all breakpoints.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **debug**(can\_continue: `bool<class_bool>` =
true, is\_error\_breakpoint: `bool<class_bool>` = false)
`🔗<class_EngineDebugger_method_debug>`

Starts a debug break in script execution, optionally specifying whether
the program can continue based on `can_continue` and whether the break
was due to a breakpoint.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_depth**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EngineDebugger_method_get_depth>`

**Experimental:** This method may be changed or removed in future
versions.

Returns the current debug depth.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_lines\_left**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EngineDebugger_method_get_lines_left>`

**Experimental:** This method may be changed or removed in future
versions.

Returns the number of lines that remain.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_capture**(name:
`StringName<class_StringName>`)
`🔗<class_EngineDebugger_method_has_capture>`

Returns `true` if a capture with the given name is present otherwise
`false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_profiler**(name:
`StringName<class_StringName>`)
`🔗<class_EngineDebugger_method_has_profiler>`

Returns `true` if a profiler with the given name is present otherwise
`false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **insert\_breakpoint**(line: `int<class_int>`,
source: `StringName<class_StringName>`)
`🔗<class_EngineDebugger_method_insert_breakpoint>`

Inserts a new breakpoint with the given `source` and `line`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_active**()
`🔗<class_EngineDebugger_method_is_active>`

Returns `true` if the debugger is active otherwise `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_breakpoint**(line: `int<class_int>`, source:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EngineDebugger_method_is_breakpoint>`

Returns `true` if the given `source` and `line` represent an existing
breakpoint.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_profiling**(name:
`StringName<class_StringName>`)
`🔗<class_EngineDebugger_method_is_profiling>`

Returns `true` if a profiler with the given name is present and active
otherwise `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_skipping\_breakpoints**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EngineDebugger_method_is_skipping_breakpoints>`

Returns `true` if the debugger is skipping breakpoints otherwise
`false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **line\_poll**()
`🔗<class_EngineDebugger_method_line_poll>`

Forces a processing loop of debugger events. The purpose of this method
is just processing events every now and then when the script might get
too busy, so that bugs like infinite loops can be caught.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **profiler\_add\_frame\_data**(name:
`StringName<class_StringName>`, data: `Array<class_Array>`)
`🔗<class_EngineDebugger_method_profiler_add_frame_data>`

Calls the `add` callable of the profiler with given `name` and `data`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **profiler\_enable**(name:
`StringName<class_StringName>`, enable: `bool<class_bool>`, arguments:
`Array<class_Array>` = \[\])
`🔗<class_EngineDebugger_method_profiler_enable>`

Calls the `toggle` callable of the profiler with given `name` and
`arguments`. Enables/Disables the same profiler depending on `enable`
argument.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **register\_message\_capture**(name:
`StringName<class_StringName>`, callable: `Callable<class_Callable>`)
`🔗<class_EngineDebugger_method_register_message_capture>`

Registers a message capture with given `name`. If `name` is
"my\_message" then messages starting with "my\_message:" will be called
with the given callable.

Callable must accept a message string and a data array as argument. If
the message and data are valid then callable must return `true`
otherwise `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **register\_profiler**(name:
`StringName<class_StringName>`, profiler:
`EngineProfiler<class_EngineProfiler>`)
`🔗<class_EngineDebugger_method_register_profiler>`

Registers a profiler with the given `name`. See
`EngineProfiler<class_EngineProfiler>` for more information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_breakpoint**(line: `int<class_int>`,
source: `StringName<class_StringName>`)
`🔗<class_EngineDebugger_method_remove_breakpoint>`

Removes a breakpoint with the given `source` and `line`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **script\_debug**(language:
`ScriptLanguage<class_ScriptLanguage>`, can\_continue:
`bool<class_bool>` = true, is\_error\_breakpoint: `bool<class_bool>` =
false) `🔗<class_EngineDebugger_method_script_debug>`

Starts a debug break in script execution, optionally specifying whether
the program can continue based on `can_continue` and whether the break
was due to a breakpoint.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **send\_message**(message:
`String<class_String>`, data: `Array<class_Array>`)
`🔗<class_EngineDebugger_method_send_message>`

Sends a message with given `message` and `data` array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_depth**(depth: `int<class_int>`)
`🔗<class_EngineDebugger_method_set_depth>`

**Experimental:** This method may be changed or removed in future
versions.

Sets the current debugging depth.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_lines\_left**(lines: `int<class_int>`)
`🔗<class_EngineDebugger_method_set_lines_left>`

**Experimental:** This method may be changed or removed in future
versions.

Sets the current debugging lines that remain.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unregister\_message\_capture**(name:
`StringName<class_StringName>`)
`🔗<class_EngineDebugger_method_unregister_message_capture>`

Unregisters the message capture with given `name`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unregister\_profiler**(name:
`StringName<class_StringName>`)
`🔗<class_EngineDebugger_method_unregister_profiler>`

Unregisters a profiler with given `name`.
