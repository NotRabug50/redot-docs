github\_url  
hide

# Engine

**Inherits:** `Object<class_Object>`

Provides access to engine properties.

classref-introduction-group

## Description

The **Engine** singleton allows you to query and modify the project's
run-time parameters, such as frames per second, time scale, and others.
It also stores information about the current build of Godot, such as the
current version.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **max\_fps** = `0` `🔗<class_Engine_property_max_fps>`

classref-property-setget

-   `void (No return value.)` **set\_max\_fps**(value: `int<class_int>`)
-   `int<class_int>` **get\_max\_fps**()

The maximum number of frames that can be rendered every second (FPS). A
value of `0` means the framerate is uncapped.

Limiting the FPS can be useful to reduce the host machine's power
consumption, which reduces heat, noise emissions, and improves battery
life.

If
`ProjectSettings.display/window/vsync/vsync_mode<class_ProjectSettings_property_display/window/vsync/vsync_mode>`
is **Enabled** or **Adaptive**, the setting takes precedence and the max
FPS number cannot exceed the monitor's refresh rate.

If
`ProjectSettings.display/window/vsync/vsync_mode<class_ProjectSettings_property_display/window/vsync/vsync_mode>`
is **Enabled**, on monitors with variable refresh rate enabled
(G-Sync/FreeSync), using an FPS limit a few frames lower than the
monitor's refresh rate will [reduce input lag while avoiding
tearing](https://blurbusters.com/howto-low-lag-vsync-on/).

See also
`physics_ticks_per_second<class_Engine_property_physics_ticks_per_second>`
and
`ProjectSettings.application/run/max_fps<class_ProjectSettings_property_application/run/max_fps>`.

\*\*Note:\*\* The actual number of frames per second may still be below
this value if the CPU or GPU cannot keep up with the project's logic and
rendering.

\*\*Note:\*\* If
`ProjectSettings.display/window/vsync/vsync_mode<class_ProjectSettings_property_display/window/vsync/vsync_mode>`
is **Disabled**, limiting the FPS to a high value that can be
consistently reached on the system can reduce input lag compared to an
uncapped framerate. Since this works by ensuring the GPU load is lower
than 100%, this latency reduction is only effective in GPU-bottlenecked
scenarios, not CPU-bottlenecked scenarios.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **max\_physics\_steps\_per\_frame** = `8`
`🔗<class_Engine_property_max_physics_steps_per_frame>`

classref-property-setget

-   `void (No return value.)`
    **set\_max\_physics\_steps\_per\_frame**(value: `int<class_int>`)
-   `int<class_int>` **get\_max\_physics\_steps\_per\_frame**()

The maximum number of physics steps that can be simulated each rendered
frame.

\*\*Note:\*\* The default value is tuned to prevent expensive physics
simulations from triggering even more expensive simulations
indefinitely. However, the game will appear to slow down if the
rendering FPS is less than `1 / max_physics_steps_per_frame` of
`physics_ticks_per_second<class_Engine_property_physics_ticks_per_second>`.
This occurs even if `delta` is consistently used in physics
calculations. To avoid this, increase
`max_physics_steps_per_frame<class_Engine_property_max_physics_steps_per_frame>`
if you have increased
`physics_ticks_per_second<class_Engine_property_physics_ticks_per_second>`
significantly above its default value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **physics\_jitter\_fix** = `0.5`
`🔗<class_Engine_property_physics_jitter_fix>`

classref-property-setget

-   `void (No return value.)` **set\_physics\_jitter\_fix**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_physics\_jitter\_fix**()

How much physics ticks are synchronized with real time. If `0` or less,
the ticks are fully synchronized. Higher values cause the in-game clock
to deviate more from the real clock, but they smooth out framerate
jitters.

\*\*Note:\*\* The default value of `0.5` should be good enough for most
cases; values above `2` could cause the game to react to dropped frames
with a noticeable delay and are not recommended.

\*\*Note:\*\* When using a custom physics interpolation solution, or
within a network game, it's recommended to disable the physics jitter
fix by setting this property to `0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **physics\_ticks\_per\_second** = `60`
`🔗<class_Engine_property_physics_ticks_per_second>`

classref-property-setget

-   `void (No return value.)`
    **set\_physics\_ticks\_per\_second**(value: `int<class_int>`)
-   `int<class_int>` **get\_physics\_ticks\_per\_second**()

The number of fixed iterations per second. This controls how often
physics simulation and
`Node._physics_process<class_Node_private_method__physics_process>`
methods are run. This value should generally always be set to `60` or
above, as Godot doesn't interpolate the physics step. As a result,
values lower than `60` will look stuttery. This value can be increased
to make input more reactive or work around collision tunneling issues,
but keep in mind doing so will increase CPU usage. See also
`max_fps<class_Engine_property_max_fps>` and
`ProjectSettings.physics/common/physics_ticks_per_second<class_ProjectSettings_property_physics/common/physics_ticks_per_second>`.

\*\*Note:\*\* Only
`max_physics_steps_per_frame<class_Engine_property_max_physics_steps_per_frame>`
physics ticks may be simulated per rendered frame at most. If more
physics ticks have to be simulated per rendered frame to keep up with
rendering, the project will appear to slow down (even if `delta` is used
consistently in physics calculations). Therefore, it is recommended to
also increase
`max_physics_steps_per_frame<class_Engine_property_max_physics_steps_per_frame>`
if increasing
`physics_ticks_per_second<class_Engine_property_physics_ticks_per_second>`
significantly above its default value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **print\_error\_messages** = `true`
`🔗<class_Engine_property_print_error_messages>`

classref-property-setget

-   `void (No return value.)` **set\_print\_error\_messages**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_printing\_error\_messages**()

If `false`, stops printing error and warning messages to the console and
editor Output log. This can be used to hide error and warning messages
during unit test suite runs. This property is equivalent to the
`ProjectSettings.application/run/disable_stderr<class_ProjectSettings_property_application/run/disable_stderr>`
project setting.

\*\*Note:\*\* This property does not impact the editor's Errors tab when
running a project from the editor.

\*\*Warning:\*\* If set to `false` anywhere in the project, important
error messages may be hidden even if they are emitted from other
scripts. In a `@tool` script, this will also impact the editor itself.
Do *not* report bugs before ensuring error messages are enabled (as they
are by default).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **print\_to\_stdout** = `true`
`🔗<class_Engine_property_print_to_stdout>`

classref-property-setget

-   `void (No return value.)` **set\_print\_to\_stdout**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_printing\_to\_stdout**()

If `false`, stops printing messages (for example using
`@GlobalScope.print<class_@GlobalScope_method_print>`) to the console,
log files, and editor Output log. This property is equivalent to the
`ProjectSettings.application/run/disable_stdout<class_ProjectSettings_property_application/run/disable_stdout>`
project setting.

\*\*Note:\*\* This does not stop printing errors or warnings produced by
scripts to the console or log files, for more details see
`print_error_messages<class_Engine_property_print_error_messages>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **time\_scale** = `1.0`
`🔗<class_Engine_property_time_scale>`

classref-property-setget

-   `void (No return value.)` **set\_time\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_time\_scale**()

The speed multiplier at which the in-game clock updates, compared to
real time. For example, if set to `2.0` the game runs twice as fast, and
if set to `0.5` the game runs half as fast.

This value affects `Timer<class_Timer>`,
`SceneTreeTimer<class_SceneTreeTimer>`, and all other simulations that
make use of `delta` time (such as
`Node._process<class_Node_private_method__process>` and
`Node._physics_process<class_Node_private_method__physics_process>`).

\*\*Note:\*\* It's recommended to keep this property above `0.0`, as the
game may behave unexpectedly otherwise.

\*\*Note:\*\* This does not affect audio playback speed. Use
`AudioServer.playback_speed_scale<class_AudioServer_property_playback_speed_scale>`
to adjust audio playback speed independently of
`time_scale<class_Engine_property_time_scale>`.

\*\*Note:\*\* This does not automatically adjust
`physics_ticks_per_second<class_Engine_property_physics_ticks_per_second>`.
With values above `1.0` physics simulation may become less precise, as
each physics tick will stretch over a larger period of engine time. If
you're modifying `time_scale<class_Engine_property_time_scale>` to speed
up simulation by a large factor, consider also increasing
`physics_ticks_per_second<class_Engine_property_physics_ticks_per_second>`
to make the simulation more reliable.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`String<class_String>` **get\_architecture\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_architecture_name>`

Returns the name of the CPU architecture the Godot binary was built for.
Possible return values include `"x86_64"`, `"x86_32"`, `"arm64"`,
`"arm32"`, `"rv64"`, `"riscv"`, `"ppc64"`, `"ppc"`, `"wasm64"`, and
`"wasm32"`.

To detect whether the current build is 64-bit, you can use the fact that
all 64-bit architecture names contain `64` in their name:

gdscript

if "64" in Engine.get\_architecture\_name():  
print("Running a 64-bit build of Godot.")

else:  
print("Running a 32-bit build of Godot.")

csharp

if (Engine.GetArchitectureName().Contains("64"))  
GD.Print("Running a 64-bit build of Godot.");

else  
GD.Print("Running a 32-bit build of Godot.");

\*\*Note:\*\* This method does *not* return the name of the system's CPU
architecture (like
`OS.get_processor_name<class_OS_method_get_processor_name>`). For
example, when running an `x86_32` Godot binary on an `x86_64` system,
the returned value will still be `"x86_32"`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_author\_info**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_author_info>`

Returns the engine author information as a
`Dictionary<class_Dictionary>`, where each entry is an
`Array<class_Array>` of strings with the names of notable contributors
to the Godot Engine: `lead_developers`, `founders`, `project_managers`,
and `developers`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_copyright\_info**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_copyright_info>`

Returns an `Array<class_Array>` of dictionaries with copyright
information for every component of Godot's source code.

Every `Dictionary<class_Dictionary>` contains a `name` identifier, and a
`parts` array of dictionaries. It describes the component in detail with
the following entries:

-   `files` - `Array<class_Array>` of file paths from the source code
    affected by this component;
-   `copyright` - `Array<class_Array>` of owners of this component;
-   `license` - The license applied to this component (such as
    "[Expat](https://en.wikipedia.org/wiki/MIT_License#Ambiguity_and_variants)"
    or "[CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/)").

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_donor\_info**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_donor_info>`

Returns a `Dictionary<class_Dictionary>` of categorized donor names.
Each entry is an `Array<class_Array>` of strings:

{`platinum_sponsors`, `gold_sponsors`, `silver_sponsors`,
`bronze_sponsors`, `mini_sponsors`, `gold_donors`, `silver_donors`,
`bronze_donors`}

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_frames\_drawn**()
`🔗<class_Engine_method_get_frames_drawn>`

Returns the total number of frames drawn since the engine started.

\*\*Note:\*\* On headless platforms, or if rendering is disabled with
`--disable-render-loop` via command line, this method always returns
`0`. See also
`get_process_frames<class_Engine_method_get_process_frames>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_frames\_per\_second**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_frames_per_second>`

Returns the average frames rendered every second (FPS), also known as
the framerate.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_license\_info**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_license_info>`

Returns a `Dictionary<class_Dictionary>` of licenses used by Godot and
included third party components. Each entry is a license name (such as
"[Expat](https://en.wikipedia.org/wiki/MIT_License#Ambiguity_and_variants)")
and its associated text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_license\_text**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_license_text>`

Returns the full Godot license text.

classref-item-separator

------------------------------------------------------------------------

classref-method

`MainLoop<class_MainLoop>` **get\_main\_loop**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_main_loop>`

Returns the instance of the `MainLoop<class_MainLoop>`. This is usually
the main `SceneTree<class_SceneTree>` and is the same as
`Node.get_tree<class_Node_method_get_tree>`.

\*\*Note:\*\* The type instantiated as the main loop can changed with
`ProjectSettings.application/run/main_loop_type<class_ProjectSettings_property_application/run/main_loop_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_physics\_frames**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_physics_frames>`

Returns the total number of frames passed since the engine started. This
number is increased every **physics frame**. See also
`get_process_frames<class_Engine_method_get_process_frames>`.

This method can be used to run expensive logic less often without
relying on a `Timer<class_Timer>`:

gdscript

func \_physics\_process(\_delta):  
if Engine.get\_physics\_frames() % 2 == 0:  
pass \# Run expensive logic only once every 2 physics frames here.

csharp

public override void \_PhysicsProcess(double delta) {
base.\_PhysicsProcess(delta);

> if (Engine.GetPhysicsFrames() % 2 == 0) { // Run expensive logic only
> once every 2 physics frames here. }

}

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_physics\_interpolation\_fraction**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_physics_interpolation_fraction>`

Returns the fraction through the current physics tick we are at the time
of rendering the frame. This can be used to implement fixed timestep
interpolation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_process\_frames**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_process_frames>`

Returns the total number of frames passed since the engine started. This
number is increased every **process frame**, regardless of whether the
render loop is enabled. See also
`get_frames_drawn<class_Engine_method_get_frames_drawn>` and
`get_physics_frames<class_Engine_method_get_physics_frames>`.

This method can be used to run expensive logic less often without
relying on a `Timer<class_Timer>`:

gdscript

func \_process(\_delta):  
if Engine.get\_process\_frames() % 5 == 0:  
pass \# Run expensive logic only once every 5 process (render) frames
here.

csharp

public override void \_Process(double delta) { base.\_Process(delta);

> if (Engine.GetProcessFrames() % 5 == 0) { // Run expensive logic only
> once every 5 process (render) frames here. }

}

classref-item-separator

------------------------------------------------------------------------

classref-method

`ScriptLanguage<class_ScriptLanguage>` **get\_script\_language**(index:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_script_language>`

Returns an instance of a `ScriptLanguage<class_ScriptLanguage>` with the
given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_script\_language\_count**()
`🔗<class_Engine_method_get_script_language_count>`

Returns the number of available script languages. Use with
`get_script_language<class_Engine_method_get_script_language>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Object<class_Object>` **get\_singleton**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_singleton>`

Returns the global singleton with the given `name`, or `null` if it does
not exist. Often used for plugins. See also
`has_singleton<class_Engine_method_has_singleton>` and
`get_singleton_list<class_Engine_method_get_singleton_list>`.

\*\*Note:\*\* Global singletons are not the same as autoloaded nodes,
which are configurable in the project settings.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_singleton\_list**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_singleton_list>`

Returns a list of names of all available global singletons. See also
`get_singleton<class_Engine_method_get_singleton>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **get\_version\_info**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_version_info>`

Returns the current engine version information as a
`Dictionary<class_Dictionary>` containing the following entries:

-   `major` - Major version number as an int;
-   `minor` - Minor version number as an int;
-   `patch` - Patch version number as an int;
-   `hex` - Full version encoded as a hexadecimal int with one byte (2
    hex digits) per number (see example below);
-   `status` - Status (such as "beta", "rc1", "rc2", "stable", etc.) as
    a String;
-   `build` - Build name (e.g. "custom\_build") as a String;
-   `hash` - Full Git commit hash as a String;
-   `timestamp` - Holds the Git commit date UNIX timestamp in seconds as
    an int, or `0` if unavailable;
-   `string` - `major`, `minor`, `patch`, `status`, and `build` in a
    single String.

The `hex` value is encoded as follows, from left to right: one byte for
the major, one byte for the minor, one byte for the patch version. For
example, "3.1.12" would be `0x03010C`.

\*\*Note:\*\* The `hex` value is still an `int<class_int>` internally,
and printing it will give you its decimal representation, which is not
particularly meaningful. Use hexadecimal literals for quick version
comparisons from code:

gdscript

if Engine.get\_version\_info().hex &gt;= 0x040100:  
pass \# Do things specific to version 4.1 or later.

else:  
pass \# Do things specific to versions before 4.1.

csharp

if ((int)Engine.GetVersionInfo()\["hex"\] &gt;= 0x040100) { // Do things
specific to version 4.1 or later. } else { // Do things specific to
versions before 4.1. }

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_write\_movie\_path**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_get_write_movie_path>`

Returns the path to the `MovieWriter<class_MovieWriter>`'s output file,
or an empty string if the engine wasn't started in Movie Maker mode. The
default path can be changed in
`ProjectSettings.editor/movie_writer/movie_file<class_ProjectSettings_property_editor/movie_writer/movie_file>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_singleton**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_has_singleton>`

Returns `true` if a singleton with the given `name` exists in the global
scope. See also `get_singleton<class_Engine_method_get_singleton>`.

gdscript

print(Engine.has\_singleton("OS")) \# Prints true
print(Engine.has\_singleton("Engine")) \# Prints true
print(Engine.has\_singleton("AudioServer")) \# Prints true
print(Engine.has\_singleton("Unknown")) \# Prints false

csharp

GD.Print(Engine.HasSingleton("OS")); // Prints true
GD.Print(Engine.HasSingleton("Engine")); // Prints true
GD.Print(Engine.HasSingleton("AudioServer")); // Prints true
GD.Print(Engine.HasSingleton("Unknown")); // Prints false

\*\*Note:\*\* Global singletons are not the same as autoloaded nodes,
which are configurable in the project settings.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_editor\_hint**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_is_editor_hint>`

Returns `true` if the script is currently running inside the editor,
otherwise returns `false`. This is useful for `@tool` scripts to
conditionally draw editor helpers, or prevent accidentally running
"game" code that would affect the scene state while in the editor:

gdscript

if Engine.is\_editor\_hint():  
draw\_gizmos()

else:  
simulate\_physics()

csharp

if (Engine.IsEditorHint())  
DrawGizmos();

else  
SimulatePhysics();

See
`Running code in the editor <../tutorials/plugins/running_code_in_the_editor>`
in the documentation for more information.

\*\*Note:\*\* To detect whether the script is running on an editor
*build* (such as when pressing `F5`), use
`OS.has_feature<class_OS_method_has_feature>` with the `"editor"`
argument instead. `OS.has_feature("editor")` evaluate to `true` both
when the script is running in the editor and when running the project
from the editor, but returns `false` when run from an exported project.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_in\_physics\_frame**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Engine_method_is_in_physics_frame>`

Returns `true` if the engine is inside the fixed physics process step of
the main loop.

    func _enter_tree():
        # Depending on when the node is added to the tree,
        # prints either "true" or "false".
        print(Engine.is_in_physics_frame())

    func _process(delta):
        print(Engine.is_in_physics_frame()) # Prints false

    func _physics_process(delta):
        print(Engine.is_in_physics_frame()) # Prints true

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**register\_script\_language**(language:
`ScriptLanguage<class_ScriptLanguage>`)
`🔗<class_Engine_method_register_script_language>`

Registers a `ScriptLanguage<class_ScriptLanguage>` instance to be
available with `ScriptServer`.

Returns:

-   `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success;
-   `@GlobalScope.ERR_UNAVAILABLE<class_@GlobalScope_constant_ERR_UNAVAILABLE>`
    if `ScriptServer` has reached the limit and cannot register any new
    language;
-   `@GlobalScope.ERR_ALREADY_EXISTS<class_@GlobalScope_constant_ERR_ALREADY_EXISTS>`
    if `ScriptServer` already contains a language with similar
    extension/name/type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **register\_singleton**(name:
`StringName<class_StringName>`, instance: `Object<class_Object>`)
`🔗<class_Engine_method_register_singleton>`

Registers the given `Object<class_Object>` `instance` as a singleton,
available globally under `name`. Useful for plugins.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>`
**unregister\_script\_language**(language:
`ScriptLanguage<class_ScriptLanguage>`)
`🔗<class_Engine_method_unregister_script_language>`

Unregisters the `ScriptLanguage<class_ScriptLanguage>` instance from
`ScriptServer`.

Returns:

-   `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success;
-   `@GlobalScope.ERR_DOES_NOT_EXIST<class_@GlobalScope_constant_ERR_DOES_NOT_EXIST>`
    if the language is not registered in `ScriptServer`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **unregister\_singleton**(name:
`StringName<class_StringName>`)
`🔗<class_Engine_method_unregister_singleton>`

Removes the singleton registered under `name`. The singleton object is
*not* freed. Only works with user-defined singletons registered with
`register_singleton<class_Engine_method_register_singleton>`.
