github\_url  
hide

# EditorDebuggerSession

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

A class to interact with the editor debugger.

classref-introduction-group

## Description

This class cannot be directly instantiated and must be retrieved via a
`EditorDebuggerPlugin<class_EditorDebuggerPlugin>`.

You can add tabs to the session UI via
`add_session_tab<class_EditorDebuggerSession_method_add_session_tab>`,
send messages via
`send_message<class_EditorDebuggerSession_method_send_message>`, and
toggle `EngineProfiler<class_EngineProfiler>`s via
`toggle_profiler<class_EditorDebuggerSession_method_toggle_profiler>`.

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

## Signals

classref-signal

**breaked**(can\_debug: `bool<class_bool>`)
`🔗<class_EditorDebuggerSession_signal_breaked>`

Emitted when the attached remote instance enters a break state. If
`can_debug` is `true`, the remote instance will enter the debug loop.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**continued**() `🔗<class_EditorDebuggerSession_signal_continued>`

Emitted when the attached remote instance exits a break state.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**started**() `🔗<class_EditorDebuggerSession_signal_started>`

Emitted when a remote instance is attached to this session (i.e. the
session becomes active).

classref-item-separator

------------------------------------------------------------------------

classref-signal

**stopped**() `🔗<class_EditorDebuggerSession_signal_stopped>`

Emitted when a remote instance is detached from this session (i.e. the
session becomes inactive).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_session\_tab**(control:
`Control<class_Control>`)
`🔗<class_EditorDebuggerSession_method_add_session_tab>`

Adds the given `control` to the debug session UI in the debugger bottom
panel.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_active**()
`🔗<class_EditorDebuggerSession_method_is_active>`

Returns `true` if the debug session is currently attached to a remote
instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_breaked**()
`🔗<class_EditorDebuggerSession_method_is_breaked>`

Returns `true` if the attached remote instance is currently in the debug
loop.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_debuggable**()
`🔗<class_EditorDebuggerSession_method_is_debuggable>`

Returns `true` if the attached remote instance can be debugged.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_session\_tab**(control:
`Control<class_Control>`)
`🔗<class_EditorDebuggerSession_method_remove_session_tab>`

Removes the given `control` from the debug session UI in the debugger
bottom panel.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **send\_message**(message:
`String<class_String>`, data: `Array<class_Array>` = \[\])
`🔗<class_EditorDebuggerSession_method_send_message>`

Sends the given `message` to the attached remote instance, optionally
passing additionally `data`. See `EngineDebugger<class_EngineDebugger>`
for how to retrieve those messages.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_breakpoint**(path:
`String<class_String>`, line: `int<class_int>`, enabled:
`bool<class_bool>`)
`🔗<class_EditorDebuggerSession_method_set_breakpoint>`

Enables or disables a specific breakpoint based on `enabled`, updating
the Editor Breakpoint Panel accordingly.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **toggle\_profiler**(profiler:
`String<class_String>`, enable: `bool<class_bool>`, data:
`Array<class_Array>` = \[\])
`🔗<class_EditorDebuggerSession_method_toggle_profiler>`

Toggle the given `profiler` on the attached remote instance, optionally
passing additionally `data`. See `EngineProfiler<class_EngineProfiler>`
for more details.
