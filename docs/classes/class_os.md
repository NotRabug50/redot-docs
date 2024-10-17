github\_url  
hide

# OS

**Inherits:** `Object<class_Object>`

Provides access to common operating system functionalities.

classref-introduction-group

## Description

The **OS** class wraps the most common functionalities for communicating
with the host operating system, such as the video driver, delays,
environment variables, execution of binaries, command line, etc.

\*\*Note:\*\* In Godot 4, **OS** functions related to window management,
clipboard, and TTS were moved to the
`DisplayServer<class_DisplayServer>` singleton (and the
`Window<class_Window>` class). Functions related to time were removed
and are only available in the `Time<class_Time>` class.

classref-introduction-group

## Tutorials

-   [Operating System Testing
    Demo](https://godotengine.org/asset-library/asset/2789)

classref-reftable-group

## Properties

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

## Enumerations

classref-enumeration

enum **RenderingDriver**: `🔗<enum_OS_RenderingDriver>`

classref-enumeration-constant

`RenderingDriver<enum_OS_RenderingDriver>` **RENDERING\_DRIVER\_VULKAN**
= `0`

The Vulkan rendering driver. It requires Vulkan 1.0 support and
automatically uses features from Vulkan 1.1 and 1.2 if available.

classref-enumeration-constant

`RenderingDriver<enum_OS_RenderingDriver>`
**RENDERING\_DRIVER\_OPENGL3** = `1`

The OpenGL 3 rendering driver. It uses OpenGL 3.3 Core Profile on
desktop platforms, OpenGL ES 3.0 on mobile devices, and WebGL 2.0 on
Web.

classref-enumeration-constant

`RenderingDriver<enum_OS_RenderingDriver>` **RENDERING\_DRIVER\_D3D12**
= `2`

The Direct3D 12 rendering driver.

classref-enumeration-constant

`RenderingDriver<enum_OS_RenderingDriver>` **RENDERING\_DRIVER\_METAL**
= `3`

The Metal rendering driver.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SystemDir**: `🔗<enum_OS_SystemDir>`

classref-enumeration-constant

`SystemDir<enum_OS_SystemDir>` **SYSTEM\_DIR\_DESKTOP** = `0`

Refers to the Desktop directory path.

classref-enumeration-constant

`SystemDir<enum_OS_SystemDir>` **SYSTEM\_DIR\_DCIM** = `1`

Refers to the DCIM (Digital Camera Images) directory path.

classref-enumeration-constant

`SystemDir<enum_OS_SystemDir>` **SYSTEM\_DIR\_DOCUMENTS** = `2`

Refers to the Documents directory path.

classref-enumeration-constant

`SystemDir<enum_OS_SystemDir>` **SYSTEM\_DIR\_DOWNLOADS** = `3`

Refers to the Downloads directory path.

classref-enumeration-constant

`SystemDir<enum_OS_SystemDir>` **SYSTEM\_DIR\_MOVIES** = `4`

Refers to the Movies (or Videos) directory path.

classref-enumeration-constant

`SystemDir<enum_OS_SystemDir>` **SYSTEM\_DIR\_MUSIC** = `5`

Refers to the Music directory path.

classref-enumeration-constant

`SystemDir<enum_OS_SystemDir>` **SYSTEM\_DIR\_PICTURES** = `6`

Refers to the Pictures directory path.

classref-enumeration-constant

`SystemDir<enum_OS_SystemDir>` **SYSTEM\_DIR\_RINGTONES** = `7`

Refers to the Ringtones directory path.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **delta\_smoothing** = `true`
`🔗<class_OS_property_delta_smoothing>`

classref-property-setget

-   `void (No return value.)` **set\_delta\_smoothing**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_delta\_smoothing\_enabled**()

If `true`, the engine filters the time delta measured between each
frame, and attempts to compensate for random variation. This only works
on systems where V-Sync is active.

\*\*Note:\*\* On start-up, this is the same as
`ProjectSettings.application/run/delta_smoothing<class_ProjectSettings_property_application/run/delta_smoothing>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **low\_processor\_usage\_mode** = `false`
`🔗<class_OS_property_low_processor_usage_mode>`

classref-property-setget

-   `void (No return value.)`
    **set\_low\_processor\_usage\_mode**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_in\_low\_processor\_usage\_mode**()

If `true`, the engine optimizes for low processor usage by only
refreshing the screen if needed. Can improve battery consumption on
mobile.

\*\*Note:\*\* On start-up, this is the same as
`ProjectSettings.application/run/low_processor_mode<class_ProjectSettings_property_application/run/low_processor_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **low\_processor\_usage\_mode\_sleep\_usec** = `6900`
`🔗<class_OS_property_low_processor_usage_mode_sleep_usec>`

classref-property-setget

-   `void (No return value.)`
    **set\_low\_processor\_usage\_mode\_sleep\_usec**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_low\_processor\_usage\_mode\_sleep\_usec**()

The amount of sleeping between frames when the low-processor usage mode
is enabled, in microseconds. Higher values will result in lower CPU
usage. See also
`low_processor_usage_mode<class_OS_property_low_processor_usage_mode>`.

\*\*Note:\*\* On start-up, this is the same as
`ProjectSettings.application/run/low_processor_mode_sleep_usec<class_ProjectSettings_property_application/run/low_processor_mode_sleep_usec>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **alert**(text: `String<class_String>`, title:
`String<class_String>` = "Alert!") `🔗<class_OS_method_alert>`

Displays a modal dialog box using the host platform's implementation.
The engine execution is blocked until the dialog is closed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **close\_midi\_inputs**()
`🔗<class_OS_method_close_midi_inputs>`

Shuts down the system MIDI driver. Godot will no longer receive
`InputEventMIDI<class_InputEventMIDI>`. See also
`open_midi_inputs<class_OS_method_open_midi_inputs>` and
`get_connected_midi_inputs<class_OS_method_get_connected_midi_inputs>`.

\*\*Note:\*\* This method is implemented on Linux, macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **crash**(message: `String<class_String>`)
`🔗<class_OS_method_crash>`

Crashes the engine (or the editor if called within a `@tool` script).
See also `kill<class_OS_method_kill>`.

\*\*Note:\*\* This method should *only* be used for testing the system's
crash handler, not for any other purpose. For general error reporting,
use (in order of preference)
`@GDScript.assert<class_@GDScript_method_assert>`,
`@GlobalScope.push_error<class_@GlobalScope_method_push_error>`, or
`alert<class_OS_method_alert>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **create\_instance**(arguments:
`PackedStringArray<class_PackedStringArray>`)
`🔗<class_OS_method_create_instance>`

Creates a new instance of Godot that runs independently. The `arguments`
are used in the given order and separated by a space.

If the process is successfully created, this method returns the new
process' ID, which you can use to monitor the process (and potentially
terminate it with `kill<class_OS_method_kill>`). If the process cannot
be created, this method returns `-1`.

See `create_process<class_OS_method_create_process>` if you wish to run
a different process.

\*\*Note:\*\* This method is implemented on Android, Linux, macOS and
Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **create\_process**(path: `String<class_String>`,
arguments: `PackedStringArray<class_PackedStringArray>`, open\_console:
`bool<class_bool>` = false) `🔗<class_OS_method_create_process>`

Creates a new process that runs independently of Godot. It will not
terminate when Godot terminates. The path specified in `path` must exist
and be an executable file or macOS `.app` bundle. The path is resolved
based on the current platform. The `arguments` are used in the given
order and separated by a space.

On Windows, if `open_console` is `true` and the process is a console
app, a new terminal window will be opened.

If the process is successfully created, this method returns its process
ID, which you can use to monitor the process (and potentially terminate
it with `kill<class_OS_method_kill>`). Otherwise, this method returns
`-1`.

For example, running another instance of the project:

gdscript

var pid = OS.create\_process(OS.get\_executable\_path(), \[\])

csharp

var pid = OS.CreateProcess(OS.GetExecutablePath(), new string\[\] {});

See `execute<class_OS_method_execute>` if you wish to run an external
command and retrieve the results.

\*\*Note:\*\* This method is implemented on Android, Linux, macOS, and
Windows.

\*\*Note:\*\* On macOS, sandboxed applications are limited to run only
embedded helper executables, specified during export or system .app
bundle, system .app bundles will ignore arguments.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **delay\_msec**(msec: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_delay_msec>`

Delays execution of the current thread by `msec` milliseconds. `msec`
must be greater than or equal to `0`. Otherwise,
`delay_msec<class_OS_method_delay_msec>` does nothing and prints an
error message.

\*\*Note:\*\* `delay_msec<class_OS_method_delay_msec>` is a *blocking*
way to delay code execution. To delay code execution in a non-blocking
way, you may use
`SceneTree.create_timer<class_SceneTree_method_create_timer>`. Awaiting
with `SceneTreeTimer<class_SceneTreeTimer>` delays the execution of code
placed below the `await` without affecting the rest of the project (or
editor, for `EditorPlugin<class_EditorPlugin>`s and
`EditorScript<class_EditorScript>`s).

\*\*Note:\*\* When `delay_msec<class_OS_method_delay_msec>` is called on
the main thread, it will freeze the project and will prevent it from
redrawing and registering input until the delay has passed. When using
`delay_msec<class_OS_method_delay_msec>` as part of an
`EditorPlugin<class_EditorPlugin>` or
`EditorScript<class_EditorScript>`, it will freeze the editor but won't
freeze the project if it is currently running (since the project is an
independent child process).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **delay\_usec**(usec: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_delay_usec>`

Delays execution of the current thread by `usec` microseconds. `usec`
must be greater than or equal to `0`. Otherwise,
`delay_usec<class_OS_method_delay_usec>` does nothing and prints an
error message.

\*\*Note:\*\* `delay_usec<class_OS_method_delay_usec>` is a *blocking*
way to delay code execution. To delay code execution in a non-blocking
way, you may use
`SceneTree.create_timer<class_SceneTree_method_create_timer>`. Awaiting
with a `SceneTreeTimer<class_SceneTreeTimer>` delays the execution of
code placed below the `await` without affecting the rest of the project
(or editor, for `EditorPlugin<class_EditorPlugin>`s and
`EditorScript<class_EditorScript>`s).

\*\*Note:\*\* When `delay_usec<class_OS_method_delay_usec>` is called on
the main thread, it will freeze the project and will prevent it from
redrawing and registering input until the delay has passed. When using
`delay_usec<class_OS_method_delay_usec>` as part of an
`EditorPlugin<class_EditorPlugin>` or
`EditorScript<class_EditorScript>`, it will freeze the editor but won't
freeze the project if it is currently running (since the project is an
independent child process).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **execute**(path: `String<class_String>`, arguments:
`PackedStringArray<class_PackedStringArray>`, output:
`Array<class_Array>` = \[\], read\_stderr: `bool<class_bool>` = false,
open\_console: `bool<class_bool>` = false) `🔗<class_OS_method_execute>`

Executes the given process in a *blocking* way. The file specified in
`path` must exist and be executable. The system path resolution will be
used. The `arguments` are used in the given order, separated by spaces,
and wrapped in quotes.

If an `output` array is provided, the complete shell output of the
process is appended to `output` as a single `String<class_String>`
element. If `read_stderr` is `true`, the output to the standard error
stream is also appended to the array.

On Windows, if `open_console` is `true` and the process is a console
app, a new terminal window is opened.

This method returns the exit code of the command, or `-1` if the process
fails to execute.

\*\*Note:\*\* The main thread will be blocked until the executed command
terminates. Use `Thread<class_Thread>` to create a separate thread that
will not block the main thread, or use
`create_process<class_OS_method_create_process>` to create a completely
independent process.

For example, to retrieve a list of the working directory's contents:

gdscript

var output = \[\] var exit\_code = OS.execute("ls", \["-l", "/tmp"\],
output)

csharp

var output = new Godot.Collections.Array(); int exitCode =
OS.Execute("ls", new string\[\] {"-l", "/tmp"}, output);

If you wish to access a shell built-in or execute a composite command, a
platform-specific shell can be invoked. For example:

gdscript

var output = \[\] OS.execute("CMD.exe", \["/C", "cd %TEMP% && dir"\],
output)

csharp

var output = new Godot.Collections.Array(); OS.Execute("CMD.exe", new
string\[\] {"/C", "cd %TEMP% && dir"}, output);

\*\*Note:\*\* This method is implemented on Android, Linux, macOS, and
Windows.

\*\*Note:\*\* To execute a Windows command interpreter built-in command,
specify `cmd.exe` in `path`, `/c` as the first argument, and the desired
command as the second argument.

\*\*Note:\*\* To execute a PowerShell built-in command, specify
`powershell.exe` in `path`, `-Command` as the first argument, and the
desired command as the second argument.

\*\*Note:\*\* To execute a Unix shell built-in command, specify shell
executable name in `path`, `-c` as the first argument, and the desired
command as the second argument.

\*\*Note:\*\* On macOS, sandboxed applications are limited to run only
embedded helper executables, specified during export.

\*\*Note:\*\* On Android, system commands such as `dumpsys` can only be
run on a rooted device.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **execute\_with\_pipe**(path:
`String<class_String>`, arguments:
`PackedStringArray<class_PackedStringArray>`, blocking:
`bool<class_bool>` = true) `🔗<class_OS_method_execute_with_pipe>`

Creates a new process that runs independently of Godot with redirected
IO. It will not terminate when Godot terminates. The path specified in
`path` must exist and be an executable file or macOS `.app` bundle. The
path is resolved based on the current platform. The `arguments` are used
in the given order and separated by a space.

If `blocking` is `false`, created pipes work in non-blocking mode, i.e.
read and write operations will return immediately. Use
`FileAccess.get_error<class_FileAccess_method_get_error>` to check if
the last read/write operation was successful.

If the process cannot be created, this method returns an empty
`Dictionary<class_Dictionary>`. Otherwise, this method returns a
`Dictionary<class_Dictionary>` with the following keys:

-   `"stdio"` - `FileAccess<class_FileAccess>` to access the process
    stdin and stdout pipes (read/write).
-   `"stderr"` - `FileAccess<class_FileAccess>` to access the process
    stderr pipe (read only).
-   `"pid"` - Process ID as an `int<class_int>`, which you can use to
    monitor the process (and potentially terminate it with
    `kill<class_OS_method_kill>`).

\*\*Note:\*\* This method is implemented on Android, Linux, macOS, and
Windows.

\*\*Note:\*\* To execute a Windows command interpreter built-in command,
specify `cmd.exe` in `path`, `/c` as the first argument, and the desired
command as the second argument.

\*\*Note:\*\* To execute a PowerShell built-in command, specify
`powershell.exe` in `path`, `-Command` as the first argument, and the
desired command as the second argument.

\*\*Note:\*\* To execute a Unix shell built-in command, specify shell
executable name in `path`, `-c` as the first argument, and the desired
command as the second argument.

\*\*Note:\*\* On macOS, sandboxed applications are limited to run only
embedded helper executables, specified during export or system .app
bundle, system .app bundles will ignore arguments.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Key<enum_@GlobalScope_Key>` **find\_keycode\_from\_string**(string:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_find_keycode_from_string>`

Finds the keycode for the given string. The returned values are
equivalent to the `Key<enum_@GlobalScope_Key>` constants.

gdscript

print(OS.find\_keycode\_from\_string("C")) \# Prints 67 (KEY\_C)
print(OS.find\_keycode\_from\_string("Escape")) \# Prints 4194305
(KEY\_ESCAPE) print(OS.find\_keycode\_from\_string("Shift+Tab")) \#
Prints 37748738 (KEY\_MASK\_SHIFT | KEY\_TAB)
print(OS.find\_keycode\_from\_string("Unknown")) \# Prints 0 (KEY\_NONE)

csharp

GD.Print(OS.FindKeycodeFromString("C")); // Prints C (Key.C)
GD.Print(OS.FindKeycodeFromString("Escape")); // Prints Escape
(Key.Escape) GD.Print(OS.FindKeycodeFromString("Shift+Tab")); // Prints
37748738 (KeyModifierMask.MaskShift | Key.Tab)
GD.Print(OS.FindKeycodeFromString("Unknown")); // Prints None (Key.None)

See also `get_keycode_string<class_OS_method_get_keycode_string>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_cache\_dir**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_cache_dir>`

Returns the *global* cache data directory according to the operating
system's standards.

On the Linux/BSD platform, this path can be overridden by setting the
`XDG_CACHE_HOME` environment variable before starting the project. See
`File paths in Godot projects <../tutorials/io/data_paths>` in the
documentation for more information. See also
`get_config_dir<class_OS_method_get_config_dir>` and
`get_data_dir<class_OS_method_get_data_dir>`.

Not to be confused with
`get_user_data_dir<class_OS_method_get_user_data_dir>`, which returns
the *project-specific* user data path.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_cmdline\_args**()
`🔗<class_OS_method_get_cmdline_args>`

Returns the command-line arguments passed to the engine.

Command-line arguments can be written in any form, including both
`--key value` and `--key=value` forms so they can be properly parsed, as
long as custom command-line arguments do not conflict with engine
arguments.

You can also incorporate environment variables using the
`get_environment<class_OS_method_get_environment>` method.

You can set
`ProjectSettings.editor/run/main_run_args<class_ProjectSettings_property_editor/run/main_run_args>`
to define command-line arguments to be passed by the editor when running
the project.

Here's a minimal example on how to parse command-line arguments into a
`Dictionary<class_Dictionary>` using the `--key=value` form for
arguments:

gdscript

var arguments = {} for argument in OS.get\_cmdline\_args(): if
argument.contains("="): var key\_value = argument.split("=")
arguments\[key\_value\[0\].trim\_prefix("--")\] = key\_value\[1\] else:
\# Options without an argument will be present in the dictionary, \#
with the value set to an empty string.
arguments\[argument.trim\_prefix("--")\] = ""

csharp

var arguments = new Dictionary&lt;string, string&gt;(); foreach (var
argument in OS.GetCmdlineArgs()) { if (argument.Contains('=')) {
string\[\] keyValue = argument.Split("=");
arguments\[keyValue\[0\].TrimPrefix("--")\] = keyValue\[1\]; } else { //
Options without an argument will be present in the dictionary, // with
the value set to an empty string. arguments\[argument.TrimPrefix("--")\]
= ""; } }

\*\*Note:\*\* Passing custom user arguments directly is not recommended,
as the engine may discard or modify them. Instead, pass the standard
UNIX double dash (`--`) and then the custom arguments, which the engine
will ignore by design. These can be read via
`get_cmdline_user_args<class_OS_method_get_cmdline_user_args>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_cmdline\_user\_args**()
`🔗<class_OS_method_get_cmdline_user_args>`

Returns the command-line user arguments passed to the engine. User
arguments are ignored by the engine and reserved for the user. They are
passed after the double dash `--` argument. `++` may be used when `--`
is intercepted by another program (such as `startx`).

    # Godot has been executed with the following command:
    # godot --fullscreen -- --level=2 --hardcore

    OS.get_cmdline_args()      # Returns ["--fullscreen", "--level=2", "--hardcore"]
    OS.get_cmdline_user_args() # Returns ["--level=2", "--hardcore"]

To get all passed arguments, use
`get_cmdline_args<class_OS_method_get_cmdline_args>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_config\_dir**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_config_dir>`

Returns the *global* user configuration directory according to the
operating system's standards.

On the Linux/BSD platform, this path can be overridden by setting the
`XDG_CONFIG_HOME` environment variable before starting the project. See
`File paths in Godot projects <../tutorials/io/data_paths>` in the
documentation for more information. See also
`get_cache_dir<class_OS_method_get_cache_dir>` and
`get_data_dir<class_OS_method_get_data_dir>`.

Not to be confused with
`get_user_data_dir<class_OS_method_get_user_data_dir>`, which returns
the *project-specific* user data path.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_connected\_midi\_inputs**()
`🔗<class_OS_method_get_connected_midi_inputs>`

Returns an array of connected MIDI device names, if they exist. Returns
an empty array if the system MIDI driver has not previously been
initialized with `open_midi_inputs<class_OS_method_open_midi_inputs>`.
See also `close_midi_inputs<class_OS_method_close_midi_inputs>`.

\*\*Note:\*\* This method is implemented on Linux, macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_data\_dir**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_data_dir>`

Returns the *global* user data directory according to the operating
system's standards.

On the Linux/BSD platform, this path can be overridden by setting the
`XDG_DATA_HOME` environment variable before starting the project. See
`File paths in Godot projects <../tutorials/io/data_paths>` in the
documentation for more information. See also
`get_cache_dir<class_OS_method_get_cache_dir>` and
`get_config_dir<class_OS_method_get_config_dir>`.

Not to be confused with
`get_user_data_dir<class_OS_method_get_user_data_dir>`, which returns
the *project-specific* user data path.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_distribution\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_distribution_name>`

Returns the name of the distribution for Linux and BSD platforms (e.g.
"Ubuntu", "Manjaro", "OpenBSD", etc.).

Returns the same value as `get_name<class_OS_method_get_name>` for stock
Android ROMs, but attempts to return the custom ROM name for popular
Android derivatives such as "LineageOS".

Returns the same value as `get_name<class_OS_method_get_name>` for other
platforms.

\*\*Note:\*\* This method is not supported on the Web platform. It
returns an empty string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **get\_entropy**(size:
`int<class_int>`) `🔗<class_OS_method_get_entropy>`

Generates a `PackedByteArray<class_PackedByteArray>` of
cryptographically secure random bytes with given `size`.

\*\*Note:\*\* Generating large quantities of bytes using this method can
result in locking and entropy of lower quality on most platforms. Using
`Crypto.generate_random_bytes<class_Crypto_method_generate_random_bytes>`
is preferred in most cases.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_environment**(variable:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_environment>`

Returns the value of the given environment variable, or an empty string
if `variable` doesn't exist.

\*\*Note:\*\* Double-check the casing of `variable`. Environment
variable names are case-sensitive on all platforms except Windows.

\*\*Note:\*\* On macOS, applications do not have access to shell
environment variables.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_executable\_path**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_executable_path>`

Returns the file path to the current engine executable.

\*\*Note:\*\* On macOS, if you want to launch another instance of Godot,
always use `create_instance<class_OS_method_create_instance>` instead of
relying on the executable path.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_granted\_permissions**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_granted_permissions>`

On Android devices: Returns the list of dangerous permissions that have
been granted.

On macOS: Returns the list of user selected folders accessible to the
application (sandboxed applications only). Use the native file dialog to
request folder access permission.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_keycode\_string**(code:
`Key<enum_@GlobalScope_Key>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_keycode_string>`

Returns the given keycode as a `String<class_String>`.

gdscript

print(OS.get\_keycode\_string(KEY\_C)) \# Prints "C"
print(OS.get\_keycode\_string(KEY\_ESCAPE)) \# Prints "Escape"
print(OS.get\_keycode\_string(KEY\_MASK\_SHIFT | KEY\_TAB)) \# Prints
"Shift+Tab"

csharp

GD.Print(OS.GetKeycodeString(Key.C)); // Prints "C"
GD.Print(OS.GetKeycodeString(Key.Escape)); // Prints "Escape"
GD.Print(OS.GetKeycodeString((Key)KeyModifierMask.MaskShift | Key.Tab));
// Prints "Shift+Tab"

See also
`find_keycode_from_string<class_OS_method_find_keycode_from_string>`,
`InputEventKey.keycode<class_InputEventKey_property_keycode>`, and
`InputEventKey.get_keycode_with_modifiers<class_InputEventKey_method_get_keycode_with_modifiers>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_locale**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_locale>`

Returns the host OS locale as a `String<class_String>` of the form
`language_Script_COUNTRY_VARIANT@extra`. Every substring after
`language` is optional and may not exist.

-   `language` - 2 or 3-letter [language
    code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes), in
    lower case.
-   `Script` - 4-letter [script
    code](https://en.wikipedia.org/wiki/ISO_15924), in title case.
-   `COUNTRY` - 2 or 3-letter [country
    code](https://en.wikipedia.org/wiki/ISO_3166-1), in upper case.
-   `VARIANT` - language variant, region and sort order. The variant can
    have any number of underscored keywords.
-   `extra` - semicolon separated list of additional key words. This may
    include currency, calendar, sort order and numbering system
    information.

If you want only the language code and not the fully specified locale
from the OS, you can use
`get_locale_language<class_OS_method_get_locale_language>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_locale\_language**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_locale_language>`

Returns the host OS locale's 2 or 3-letter [language
code](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes) as a string
which should be consistent on all platforms. This is equivalent to
extracting the `language` part of the
`get_locale<class_OS_method_get_locale>` string.

This can be used to narrow down fully specified locale strings to only
the "common" language code, when you don't need the additional
information about country code or variants. For example, for a French
Canadian user with `fr_CA` locale, this would return `fr`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_main\_thread\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_main_thread_id>`

Returns the ID of the main thread. See
`get_thread_caller_id<class_OS_method_get_thread_caller_id>`.

\*\*Note:\*\* Thread IDs are not deterministic and may be reused across
application restarts.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_memory\_info**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_memory_info>`

Returns a `Dictionary<class_Dictionary>` containing information about
the current memory with the following entries:

-   `"physical"` - total amount of usable physical memory in bytes. This
    value can be slightly less than the actual physical memory amount,
    since it does not include memory reserved by the kernel and devices.
-   `"free"` - amount of physical memory, that can be immediately
    allocated without disk access or other costly operations, in bytes.
    The process might be able to allocate more physical memory, but this
    action will require moving inactive pages to disk, which can be
    expensive.
-   `"available"` - amount of memory that can be allocated without
    extending the swap file(s), in bytes. This value includes both
    physical memory and swap.
-   `"stack"` - size of the current thread stack in bytes.

\*\*Note:\*\* Each entry's value may be `-1` if it is unknown.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_model\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_model_name>`

Returns the model name of the current device.

\*\*Note:\*\* This method is implemented on Android and iOS. Returns
`"GenericDevice"` on unsupported platforms.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_name>`

Returns the name of the host platform.

-   On Windows, this is `"Windows"`.
-   On macOS, this is `"macOS"`.
-   On Linux-based operating systems, this is `"Linux"`.
-   On BSD-based operating systems, this is `"FreeBSD"`, `"NetBSD"`,
    `"OpenBSD"`, or `"BSD"` as a fallback.
-   On Android, this is `"Android"`.
-   On iOS, this is `"iOS"`.
-   On Web, this is `"Web"`.

\*\*Note:\*\* Custom builds of the engine may support additional
platforms, such as consoles, possibly returning other names.

gdscript

match OS.get\_name():  
"Windows":  
print("Welcome to Windows!")

"macOS":  
print("Welcome to macOS!")

"Linux", "FreeBSD", "NetBSD", "OpenBSD", "BSD":  
print("Welcome to Linux/BSD!")

"Android":  
print("Welcome to Android!")

"iOS":  
print("Welcome to iOS!")

"Web":  
print("Welcome to the Web!")

csharp

switch (OS.GetName()) { case "Windows": GD.Print("Welcome to Windows");
break; case "macOS": GD.Print("Welcome to macOS!"); break; case "Linux":
case "FreeBSD": case "NetBSD": case "OpenBSD": case "BSD":
GD.Print("Welcome to Linux/BSD!"); break; case "Android":
GD.Print("Welcome to Android!"); break; case "iOS": GD.Print("Welcome to
iOS!"); break; case "Web": GD.Print("Welcome to the Web!"); break; }

\*\*Note:\*\* On Web platforms, it is still possible to determine the
host platform's OS with feature tags. See
`has_feature<class_OS_method_has_feature>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_process\_exit\_code**(pid: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_process_exit_code>`

Returns the exit code of a spawned process once it has finished running
(see `is_process_running<class_OS_method_is_process_running>`).

Returns `-1` if the `pid` is not a PID of a spawned child process, the
process is still running, or the method is not implemented for the
current platform.

\*\*Note:\*\* Returns `-1` if the `pid` is a macOS bundled app process.

\*\*Note:\*\* This method is implemented on Android, Linux, macOS and
Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_process\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_process_id>`

Returns the number used by the host machine to uniquely identify this
application.

\*\*Note:\*\* This method is implemented on Android, iOS, Linux, macOS,
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_processor\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_processor_count>`

Returns the number of *logical* CPU cores available on the host machine.
On CPUs with HyperThreading enabled, this number will be greater than
the number of *physical* CPU cores.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_processor\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_processor_name>`

Returns the full name of the CPU model on the host machine (e.g.
`"Intel(R) Core(TM) i7-6700K CPU @ 4.00GHz"`).

\*\*Note:\*\* This method is only implemented on Windows, macOS, Linux
and iOS. On Android and Web,
`get_processor_name<class_OS_method_get_processor_name>` returns an
empty string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_restart\_on\_exit\_arguments**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_restart_on_exit_arguments>`

Returns the list of command line arguments that will be used when the
project automatically restarts using
`set_restart_on_exit<class_OS_method_set_restart_on_exit>`. See also
`is_restart_on_exit_set<class_OS_method_is_restart_on_exit_set>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_static\_memory\_peak\_usage**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_static_memory_peak_usage>`

Returns the maximum amount of static memory used. Only works in debug
builds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_static\_memory\_usage**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_static_memory_usage>`

Returns the amount of static memory being used by the program in bytes.
Only works in debug builds.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_system\_ca\_certificates**()
`🔗<class_OS_method_get_system_ca_certificates>`

Returns the list of certification authorities trusted by the operating
system as a string of concatenated certificates in PEM format.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_system\_dir**(dir:
`SystemDir<enum_OS_SystemDir>`, shared\_storage: `bool<class_bool>` =
true)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_system_dir>`

Returns the path to commonly used folders across different platforms, as
defined by `dir`. See the `SystemDir<enum_OS_SystemDir>` constants for
available locations.

\*\*Note:\*\* This method is implemented on Android, Linux, macOS and
Windows.

\*\*Note:\*\* Shared storage is implemented on Android and allows to
differentiate between app specific and shared directories, if
`shared_storage` is `true`. Shared directories have additional
restrictions on Android.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_system\_font\_path**(font\_name:
`String<class_String>`, weight: `int<class_int>` = 400, stretch:
`int<class_int>` = 100, italic: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_system_font_path>`

Returns the path to the system font file with `font_name` and style.
Returns an empty string if no matching fonts found.

The following aliases can be used to request default fonts:
"sans-serif", "serif", "monospace", "cursive", and "fantasy".

\*\*Note:\*\* Returned font might have different style if the requested
style is not available.

\*\*Note:\*\* This method is implemented on Android, iOS, Linux, macOS
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_system\_font\_path\_for\_text**(font\_name:
`String<class_String>`, text: `String<class_String>`, locale:
`String<class_String>` = "", script: `String<class_String>` = "",
weight: `int<class_int>` = 400, stretch: `int<class_int>` = 100, italic:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_system_font_path_for_text>`

Returns an array of the system substitute font file paths, which are
similar to the font with `font_name` and style for the specified text,
locale, and script. Returns an empty array if no matching fonts found.

The following aliases can be used to request default fonts:
"sans-serif", "serif", "monospace", "cursive", and "fantasy".

\*\*Note:\*\* Depending on OS, it's not guaranteed that any of the
returned fonts will be suitable for rendering specified text. Fonts
should be loaded and checked in the order they are returned, and the
first suitable one used.

\*\*Note:\*\* Returned fonts might have different style if the requested
style is not available or belong to a different font family.

\*\*Note:\*\* This method is implemented on Android, iOS, Linux, macOS
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_system\_fonts**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_system_fonts>`

Returns the list of font family names available.

\*\*Note:\*\* This method is implemented on Android, iOS, Linux, macOS
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_thread\_caller\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_thread_caller_id>`

Returns the ID of the current thread. This can be used in logs to ease
debugging of multi-threaded applications.

\*\*Note:\*\* Thread IDs are not deterministic and may be reused across
application restarts.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_unique\_id**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_unique_id>`

Returns a string that is unique to the device.

\*\*Note:\*\* This string may change without notice if the user
reinstalls their operating system, upgrades it, or modifies their
hardware. This means it should generally not be used to encrypt
persistent data, as the data saved before an unexpected ID change would
become inaccessible. The returned string may also be falsified using
external programs, so do not rely on the string returned by this method
for security purposes.

\*\*Note:\*\* On Web, returns an empty string and generates an error, as
this method cannot be implemented for security reasons.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_user\_data\_dir**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_user_data_dir>`

Returns the absolute directory path where user data is written (the
`user://` directory in Godot). The path depends on the project name and
`ProjectSettings.application/config/use_custom_user_dir<class_ProjectSettings_property_application/config/use_custom_user_dir>`.

-   On Windows, this is `%AppData%\Godot\app_userdata\[project_name]`,
    or `%AppData%\[custom_name]` if `use_custom_user_dir` is set.
    `%AppData%` expands to `%UserProfile%\AppData\Roaming`.
-   On macOS, this is
    `~/Library/Application Support/Godot/app_userdata/[project_name]`,
    or `~/Library/Application Support/[custom_name]` if
    `use_custom_user_dir` is set.
-   On Linux and BSD, this is
    `~/.local/share/godot/app_userdata/[project_name]`, or
    `~/.local/share/[custom_name]` if `use_custom_user_dir` is set.
-   On Android and iOS, this is a sandboxed directory in either internal
    or external storage, depending on the user's configuration.
-   On Web, this is a virtual directory managed by the browser.

If the project name is empty, `[project_name]` falls back to
`[unnamed project]`.

Not to be confused with `get_data_dir<class_OS_method_get_data_dir>`,
which returns the *global* (non-project-specific) user home directory.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_version**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_version>`

Returns the exact production and build version of the operating system.
This is different from the branded version used in marketing. This helps
to distinguish between different releases of operating systems,
including minor versions, and insider and custom builds.

-   For Windows, the major and minor version are returned, as well as
    the build number. For example, the returned string may look like
    `10.0.9926` for a build of Windows 10, and it may look like
    `6.1.7601` for a build of Windows 7 SP1.
-   For rolling distributions, such as Arch Linux, an empty string is
    returned.
-   For macOS and iOS, the major and minor version are returned, as well
    as the patch number.
-   For Android, the SDK version and the incremental build number are
    returned. If it's a custom ROM, it attempts to return its version
    instead.

\*\*Note:\*\* This method is not supported on the Web platform. It
returns an empty string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_video\_adapter\_driver\_info**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_get_video_adapter_driver_info>`

Returns the video adapter driver name and version for the user's
currently active graphics card, as a
`PackedStringArray<class_PackedStringArray>`. See also
`RenderingServer.get_video_adapter_api_version<class_RenderingServer_method_get_video_adapter_api_version>`.

The first element holds the driver name, such as `nvidia`, `amdgpu`,
etc.

The second element holds the driver version. For example, on the
`nvidia` driver on a Linux/BSD platform, the version is in the format
`510.85.02`. For Windows, the driver's format is `31.0.15.1659`.

\*\*Note:\*\* This method is only supported on Linux/BSD and Windows
when not running in headless mode. On other platforms, it returns an
empty array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_environment**(variable:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_has_environment>`

Returns `true` if the environment variable with the name `variable`
exists.

\*\*Note:\*\* Double-check the casing of `variable`. Environment
variable names are case-sensitive on all platforms except Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_feature**(tag\_name: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_has_feature>`

Returns `true` if the feature for the given feature tag is supported in
the currently running instance, depending on the platform, build, etc.
Can be used to check whether you're currently running a debug build, on
a certain platform or arch, etc. Refer to the
`Feature Tags <../tutorials/export/feature_tags>` documentation for more
details.

\*\*Note:\*\* Tag names are case-sensitive.

\*\*Note:\*\* On the Web platform, one of the following additional tags
is defined to indicate the host platform: `web_android`, `web_ios`,
`web_linuxbsd`, `web_macos`, or `web_windows`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_debug\_build**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_is_debug_build>`

Returns `true` if the Godot binary used to run the project is a *debug*
export template, or when running in the editor.

Returns `false` if the Godot binary used to run the project is a
*release* export template.

\*\*Note:\*\* To check whether the Godot binary used to run the project
is an export template (debug or release), use
`OS.has_feature("template")` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_keycode\_unicode**(code: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_is_keycode_unicode>`

Returns `true` if the input keycode corresponds to a Unicode character.
For a list of codes, see the `Key<enum_@GlobalScope_Key>` constants.

gdscript

print(OS.is\_keycode\_unicode(KEY\_G)) \# Prints true
print(OS.is\_keycode\_unicode(KEY\_KP\_4)) \# Prints true
print(OS.is\_keycode\_unicode(KEY\_TAB)) \# Prints false
print(OS.is\_keycode\_unicode(KEY\_ESCAPE)) \# Prints false

csharp

GD.Print(OS.IsKeycodeUnicode((long)Key.G)); // Prints true
GD.Print(OS.IsKeycodeUnicode((long)Key.Kp4)); // Prints true
GD.Print(OS.IsKeycodeUnicode((long)Key.Tab)); // Prints false
GD.Print(OS.IsKeycodeUnicode((long)Key.Escape)); // Prints false

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_process\_running**(pid: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_is_process_running>`

Returns `true` if the child process ID (`pid`) is still running or
`false` if it has terminated. `pid` must be a valid ID generated from
`create_process<class_OS_method_create_process>`.

\*\*Note:\*\* This method is implemented on Android, iOS, Linux, macOS,
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_restart\_on\_exit\_set**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_is_restart_on_exit_set>`

Returns `true` if the project will automatically restart when it exits
for any reason, `false` otherwise. See also
`set_restart_on_exit<class_OS_method_set_restart_on_exit>` and
`get_restart_on_exit_arguments<class_OS_method_get_restart_on_exit_arguments>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_sandboxed**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_is_sandboxed>`

Returns `true` if the application is running in the sandbox.

\*\*Note:\*\* This method is only implemented on macOS and Linux.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_stdout\_verbose**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_is_stdout_verbose>`

Returns `true` if the engine was executed with the `--verbose` or `-v`
command line argument, or if
`ProjectSettings.debug/settings/stdout/verbose_stdout<class_ProjectSettings_property_debug/settings/stdout/verbose_stdout>`
is `true`. See also
`@GlobalScope.print_verbose<class_@GlobalScope_method_print_verbose>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_userfs\_persistent**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_is_userfs_persistent>`

Returns `true` if the `user://` file system is persistent, that is, its
state is the same after a player quits and starts the game again.
Relevant to the Web platform, where this persistence may be unavailable.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **kill**(pid: `int<class_int>`)
`🔗<class_OS_method_kill>`

Kill (terminate) the process identified by the given process ID (`pid`),
such as the ID returned by `execute<class_OS_method_execute>` in
non-blocking mode. See also `crash<class_OS_method_crash>`.

\*\*Note:\*\* This method can also be used to kill processes that were
not spawned by the engine.

\*\*Note:\*\* This method is implemented on Android, iOS, Linux, macOS
and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **move\_to\_trash**(path:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_move_to_trash>`

Moves the file or directory at the given `path` to the system's recycle
bin. See also `DirAccess.remove<class_DirAccess_method_remove>`.

The method takes only global paths, so you may need to use
`ProjectSettings.globalize_path<class_ProjectSettings_method_globalize_path>`.
Do not use it for files in `res://` as it will not work in exported
projects.

Returns `@GlobalScope.FAILED<class_@GlobalScope_constant_FAILED>` if the
file or directory cannot be found, or the system does not support this
method.

gdscript

var file\_to\_remove = "user://slot1.save"
OS.move\_to\_trash(ProjectSettings.globalize\_path(file\_to\_remove))

csharp

var fileToRemove = "user://slot1.save";
OS.MoveToTrash(ProjectSettings.GlobalizePath(fileToRemove));

\*\*Note:\*\* This method is implemented on Android, Linux, macOS and
Windows.

\*\*Note:\*\* If the user has disabled the recycle bin on their system,
the file will be permanently deleted instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **open\_midi\_inputs**()
`🔗<class_OS_method_open_midi_inputs>`

Initializes the singleton for the system MIDI driver, allowing Godot to
receive `InputEventMIDI<class_InputEventMIDI>`. See also
`get_connected_midi_inputs<class_OS_method_get_connected_midi_inputs>`
and `close_midi_inputs<class_OS_method_close_midi_inputs>`.

\*\*Note:\*\* This method is implemented on Linux, macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **read\_string\_from\_stdin**()
`🔗<class_OS_method_read_string_from_stdin>`

Reads a user input string from the standard input (usually the
terminal). This operation is *blocking*, which causes the window to
freeze if
`read_string_from_stdin<class_OS_method_read_string_from_stdin>` is
called on the main thread. The thread calling
`read_string_from_stdin<class_OS_method_read_string_from_stdin>` will
block until the program receives a line break in standard input (usually
by the user pressing `Enter`).

\*\*Note:\*\* This method is implemented on Linux, macOS and Windows.

\*\*Note:\*\* On exported Windows builds, run the console wrapper
executable to access the terminal. Otherwise, the standard input will
not work correctly. If you need a single executable with console
support, use a custom build compiled with the
`windows_subsystem=console` flag.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **request\_permission**(name: `String<class_String>`)
`🔗<class_OS_method_request_permission>`

Requests permission from the OS for the given `name`. Returns `true` if
the permission has been successfully granted.

\*\*Note:\*\* This method is currently only implemented on Android, to
specifically request permission for `"RECORD_AUDIO"` by
`AudioDriverOpenSL`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **request\_permissions**()
`🔗<class_OS_method_request_permissions>`

Requests *dangerous* permissions from the OS. Returns `true` if
permissions have been successfully granted.

\*\*Note:\*\* This method is only implemented on Android. Normal
permissions are automatically granted at install time in Android
applications.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **revoke\_granted\_permissions**()
`🔗<class_OS_method_revoke_granted_permissions>`

On macOS (sandboxed applications only), this function clears list of
user selected folders accessible to the application.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_environment**(variable:
`String<class_String>`, value: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_set_environment>`

Sets the value of the environment variable `variable` to `value`. The
environment variable will be set for the Godot process and any process
executed with `execute<class_OS_method_execute>` after running
`set_environment<class_OS_method_set_environment>`. The environment
variable will *not* persist to processes run after the Godot process was
terminated.

\*\*Note:\*\* Environment variable names are case-sensitive on all
platforms except Windows. The `variable` name cannot be empty or include
the `=` character. On Windows, there is a 32767 characters limit for the
combined length of `variable`, `value`, and the `=` and null terminator
characters that will be registered in the environment block.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_restart\_on\_exit**(restart:
`bool<class_bool>`, arguments:
`PackedStringArray<class_PackedStringArray>` = PackedStringArray())
`🔗<class_OS_method_set_restart_on_exit>`

If `restart` is `true`, restarts the project automatically when it is
exited with `SceneTree.quit<class_SceneTree_method_quit>` or
`Node.NOTIFICATION_WM_CLOSE_REQUEST<class_Node_constant_NOTIFICATION_WM_CLOSE_REQUEST>`.
Command-line `arguments` can be supplied. To restart the project with
the same command line arguments as originally used to run the project,
pass `get_cmdline_args<class_OS_method_get_cmdline_args>` as the value
for `arguments`.

This method can be used to apply setting changes that require a restart.
See also
`is_restart_on_exit_set<class_OS_method_is_restart_on_exit_set>` and
`get_restart_on_exit_arguments<class_OS_method_get_restart_on_exit_arguments>`.

\*\*Note:\*\* This method is only effective on desktop platforms, and
only when the project isn't started from the editor. It will have no
effect on mobile and Web platforms, or when the project is started from
the editor.

\*\*Note:\*\* If the project process crashes or is *killed* by the user
(by sending `SIGKILL` instead of the usual `SIGTERM`), the project won't
restart automatically.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **set\_thread\_name**(name:
`String<class_String>`) `🔗<class_OS_method_set_thread_name>`

Assigns the given name to the current thread. Returns
`@GlobalScope.ERR_UNAVAILABLE<class_@GlobalScope_constant_ERR_UNAVAILABLE>`
if unavailable on the current platform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_use\_file\_access\_save\_and\_swap**(enabled: `bool<class_bool>`)
`🔗<class_OS_method_set_use_file_access_save_and_swap>`

If `enabled` is `true`, when opening a file for writing, a temporary
file is used in its place. When closed, it is automatically applied to
the target file.

This can useful when files may be opened by other applications, such as
antiviruses, text editors, or even the Godot editor itself.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **shell\_open**(uri:
`String<class_String>`) `🔗<class_OS_method_shell_open>`

Requests the OS to open a resource identified by `uri` with the most
appropriate program. For example:

-   `OS.shell_open("C:\\Users\name\Downloads")` on Windows opens the
    file explorer at the user's Downloads folder.
-   `OS.shell_open("https://godotengine.org")` opens the default web
    browser on the official Godot website.
-   `OS.shell_open("mailto:example@example.com")` opens the default
    email client with the "To" field set to `example@example.com`. See
    [RFC 2368 - The \[code\]mailto\[/code\] URL
    scheme](https://datatracker.ietf.org/doc/html/rfc2368) for a list of
    fields that can be added.

Use
`ProjectSettings.globalize_path<class_ProjectSettings_method_globalize_path>`
to convert a `res://` or `user://` project path into a system path for
use with this method.

\*\*Note:\*\* Use `String.uri_encode<class_String_method_uri_encode>` to
encode characters within URLs in a URL-safe, portable way. This is
especially required for line breaks. Otherwise,
`shell_open<class_OS_method_shell_open>` may not work correctly in a
project exported to the Web platform.

\*\*Note:\*\* This method is implemented on Android, iOS, Web, Linux,
macOS and Windows.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**shell\_show\_in\_file\_manager**(file\_or\_dir\_path:
`String<class_String>`, open\_folder: `bool<class_bool>` = true)
`🔗<class_OS_method_shell_show_in_file_manager>`

Requests the OS to open the file manager, navigate to the given
`file_or_dir_path` and select the target file or folder.

If `open_folder` is `true` and `file_or_dir_path` is a valid directory
path, the OS will open the file manager and navigate to the target
folder without selecting anything.

Use
`ProjectSettings.globalize_path<class_ProjectSettings_method_globalize_path>`
to convert a `res://` or `user://` project path into a system path to
use with this method.

\*\*Note:\*\* This method is currently only implemented on Windows and
macOS. On other platforms, it will fallback to
`shell_open<class_OS_method_shell_open>` with a directory path of
`file_or_dir_path` prefixed with `file://`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unset\_environment**(variable:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_OS_method_unset_environment>`

Removes the given environment variable from the current environment, if
it exists. The `variable` name cannot be empty or include the `=`
character. The environment variable will be removed for the Godot
process and any process executed with `execute<class_OS_method_execute>`
after running `unset_environment<class_OS_method_unset_environment>`.
The removal of the environment variable will *not* persist to processes
run after the Godot process was terminated.

\*\*Note:\*\* Environment variable names are case-sensitive on all
platforms except Windows.
