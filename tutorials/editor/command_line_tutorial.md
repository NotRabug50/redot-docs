# Command line tutorial

Some developers like using the command line extensively. Godot is
designed to be friendly to them, so here are the steps for working
entirely from the command line. Given the engine relies on almost no
external libraries, initialization times are pretty fast, making it
suitable for this workflow.

Note

On Windows and Linux, you can run a Godot binary in a terminal by
specifying its relative or absolute path.

On macOS, the process is different due to Godot being contained within
an `.app` bundle (which is a *folder*, not a file). To run a Godot
binary from a terminal on macOS, you have to `cd` to the folder where
the Godot application bundle is located, then run
`Godot.app/Contents/MacOS/Godot` followed by any command line arguments.
If you've renamed the application bundle from `Godot` to another name,
make sure to edit this command line accordingly.

## Command line reference

**Legend**

-   ![release](img/template_release.svg) Available in editor builds,
    debug export templates and release export templates.
-   ![debug](img/template_debug.svg) Available in editor builds and
    debug export templates only.
-   ![editor](img/editor.svg) Only available in editor builds.

Note that unknown command line arguments have no effect whatsoever. The
engine will **not** warn you when using a command line argument that
doesn't exist with a given build type.

**General options**

<table>
<colgroup>
<col style="width: 27%" />
<col style="width: 72%" />
</colgroup>
<tbody>
<tr>
<td>Command</td>
<td>Description</td>
</tr>
<tr>
<td><code>-h</code>, <code>--help</code></td>
<td><img src="img/template_release.svg" alt="release" /> Display the
list of command line options.</td>
</tr>
<tr>
<td><code>--version</code></td>
<td><img src="img/template_release.svg" alt="release" /> Display the
version string.</td>
</tr>
<tr>
<td><code>-v</code>, <code>--verbose</code></td>
<td><img src="img/template_release.svg" alt="release" /> Use verbose
stdout mode.</td>
</tr>
<tr>
<td><code>-q</code>, <code>--quiet</code></td>
<td><img src="img/template_release.svg" alt="release" /> Quiet mode,
silences stdout messages. Errors are still displayed.</td>
</tr>
</tbody>
</table>

**Run options**

<table>
<colgroup>
<col style="width: 21%" />
<col style="width: 78%" />
</colgroup>
<tbody>
<tr>
<td>Command</td>
<td>Description</td>
</tr>
<tr>
<td><code>--</code>, <code>++</code></td>
<td><img src="img/template_release.svg" alt="release" /> Separator for
user-provided arguments. Following arguments are not used by the engine,
but can be read from <code>OS.get_cmdline_user_args()</code>.</td>
</tr>
<tr>
<td><code>-e</code>, <code>--editor</code></td>
<td><img src="img/editor.svg" alt="editor" /> Start the editor instead
of running the scene.</td>
</tr>
<tr>
<td><code>-p</code>, <code>--project-manager</code></td>
<td><img src="img/editor.svg" alt="editor" /> Start the Project Manager,
even if a project is auto-detected.</td>
</tr>
<tr>
<td><code>--debug-server &lt;uri&gt;</code></td>
<td><img src="img/editor.svg" alt="editor" /> Start the editor debug
server (<code>&lt;protocol&gt;://&lt;host/IP&gt;[:&lt;port&gt;]</code>,
e.g. <code>tcp://127.0.0.1:6007</code>)</td>
</tr>
<tr>
<td><code>--quit</code></td>
<td><img src="img/template_release.svg" alt="release" /> Quit after the
first iteration.</td>
</tr>
<tr>
<td><code>--quit-after</code></td>
<td><img src="img/template_release.svg" alt="release" /> Quit after the
given number of iterations. Set to 0 to disable.</td>
</tr>
<tr>
<td><code>-l</code>, <code>--language &lt;locale&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Use a specific
locale. <code>&lt;locale&gt;</code> follows the format
<code>language_Script_COUNTRY_VARIANT</code> where language is a 2 or
3-letter language code in lowercase and the rest is optional. See <code
class="interpreted-text" role="ref">doc_locales</code> for more
details.</td>
</tr>
<tr>
<td><code>--path &lt;directory&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Path to a
project (<code>&lt;directory&gt;</code> must contain a 'project.godot'
file).</td>
</tr>
<tr>
<td><code>-u</code>, <code>--upwards</code></td>
<td><img src="img/template_release.svg" alt="release" /> Scan folders
upwards for 'project.godot' file.</td>
</tr>
<tr>
<td><code>--main-pack &lt;file&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Path to a pack
(.pck) file to load.</td>
</tr>
<tr>
<td><code>--render-thread &lt;mode&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Render thread
mode ('unsafe', 'safe', 'separate'). See <code class="interpreted-text"
role="ref">Thread Model &lt;class_ProjectSettings_property_rendering/driver/threads/thread_model&gt;</code>
for more details.</td>
</tr>
<tr>
<td><code>--remote-fs &lt;address&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Remote
filesystem (<code>&lt;host/IP&gt;[:&lt;port&gt;]</code> address).</td>
</tr>
<tr>
<td><code>--remote-fs-password &lt;password&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Password for
remote filesystem.</td>
</tr>
<tr>
<td><code>--audio-driver &lt;driver&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Audio driver.
Use <code>--help</code> first to display the list of available
drivers.</td>
</tr>
<tr>
<td><code>--display-driver &lt;driver&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Display driver
(and rendering driver). Use <code>--help</code> first to display the
list of available drivers.</td>
</tr>
<tr>
<td><code>--rendering-method &lt;renderer&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Renderer name.
Requires driver support.</td>
</tr>
<tr>
<td><code>--rendering-driver &lt;driver&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Rendering
driver (depends on display driver). Use <code>--help</code> first to
display the list of available drivers.</td>
</tr>
<tr>
<td><code>--gpu-index &lt;device_index&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Use a specific
GPU (run with <code>--verbose</code> to get available device list).</td>
</tr>
<tr>
<td><code>--text-driver &lt;driver&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Text driver
(Fonts, BiDi, shaping).</td>
</tr>
<tr>
<td><code>--tablet-driver &lt;driver&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Pen tablet
input driver.</td>
</tr>
<tr>
<td><code>--headless</code></td>
<td><img src="img/template_release.svg" alt="release" /> Enable headless
mode (<code>--display-driver headless --audio-driver Dummy</code>).
Useful for servers and with <code>--script</code>.</td>
</tr>
<tr>
<td><code>--write-movie &lt;file&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Run the engine
in a way that a movie is written (usually with .avi or .png extension).
<code>--fixed-fps</code> is forced when enabled, but can be used to
change movie FPS. <code>--disable-vsync</code> can speed up movie
writing but makes interaction more difficult. <code>--quit-after</code>
can be used to specify the number of frames to write.</td>
</tr>
</tbody>
</table>

**Display options**

<table>
<colgroup>
<col style="width: 32%" />
<col style="width: 67%" />
</colgroup>
<tbody>
<tr>
<td>Command</td>
<td>Description</td>
</tr>
<tr>
<td><code>-f</code>, <code>--fullscreen</code></td>
<td><img src="img/template_release.svg" alt="release" /> Request
fullscreen mode.</td>
</tr>
<tr>
<td><code>-m</code>, <code>--maximized</code></td>
<td><img src="img/template_release.svg" alt="release" /> Request a
maximized window.</td>
</tr>
<tr>
<td><code>-w</code>, <code>--windowed</code></td>
<td><img src="img/template_release.svg" alt="release" /> Request
windowed mode.</td>
</tr>
<tr>
<td><code>-t</code>, <code>--always-on-top</code></td>
<td><img src="img/template_release.svg" alt="release" /> Request an
always-on-top window.</td>
</tr>
<tr>
<td><code>--resolution &lt;W&gt;x&lt;H&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Request window
resolution.</td>
</tr>
<tr>
<td><code>--position &lt;X&gt;,&lt;Y&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Request window
position.</td>
</tr>
<tr>
<td><code>--screen &lt;N&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Request window
screen.</td>
</tr>
<tr>
<td><code>--single-window</code></td>
<td><img src="img/template_release.svg" alt="release" /> Use a single
window (no separate subwindows).</td>
</tr>
<tr>
<td><code>--xr-mode &lt;mode&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Select XR mode
('default', 'off', 'on').</td>
</tr>
</tbody>
</table>

**Debug options**

<table>
<colgroup>
<col style="width: 22%" />
<col style="width: 77%" />
</colgroup>
<tbody>
<tr>
<td>Command</td>
<td>Description</td>
</tr>
<tr>
<td><code>-d</code>, <code>--debug</code></td>
<td><img src="img/template_release.svg" alt="release" /> Debug (local
stdout debugger).</td>
</tr>
<tr>
<td><code>-b</code>, <code>--breakpoints</code></td>
<td><img src="img/template_release.svg" alt="release" /> Breakpoint list
as source::line comma-separated pairs, no spaces (use <code>%20</code>
instead).</td>
</tr>
<tr>
<td><code>--profiling</code></td>
<td><img src="img/template_release.svg" alt="release" /> Enable
profiling in the script debugger.</td>
</tr>
<tr>
<td><code>--gpu-profile</code></td>
<td><img src="img/template_release.svg" alt="release" /> Show a GPU
profile of the tasks that took the most time during frame
rendering.</td>
</tr>
<tr>
<td><code>--gpu-validation</code></td>
<td><img src="img/template_release.svg" alt="release" /> Enable graphics
API <code class="interpreted-text"
role="ref">validation layers &lt;doc_vulkan_validation_layers&gt;</code>
for debugging.</td>
</tr>
<tr>
<td><code>--gpu-abort</code></td>
<td><img src="img/template_debug.svg" alt="debug" /> Abort on GPU errors
(usually validation layer errors), may help see the problem if your
system freezes.</td>
</tr>
<tr>
<td><code>--remote-debug &lt;uri&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Remote debug
(<code>&lt;protocol&gt;://&lt;host/IP&gt;[:&lt;port&gt;]</code>, e.g.
<code>tcp://127.0.0.1:6007</code>).</td>
</tr>
<tr>
<td><code>--single-threaded-scene</code></td>
<td><img src="img/template_release.svg" alt="release" /> Scene tree runs
in single-threaded mode. Sub-thread groups are disabled and run on the
main thread.</td>
</tr>
<tr>
<td><code>--debug-collisions</code></td>
<td><img src="img/template_debug.svg" alt="debug" /> Show collision
shapes when running the scene.</td>
</tr>
<tr>
<td><code>--debug-paths</code></td>
<td><img src="img/template_debug.svg" alt="debug" /> Show path lines
when running the scene.</td>
</tr>
<tr>
<td><code>--debug-navigation</code></td>
<td><img src="img/template_debug.svg" alt="debug" /> Show navigation
polygons when running the scene.</td>
</tr>
<tr>
<td><code>--debug-avoidance</code></td>
<td><img src="img/template_debug.svg" alt="debug" /> Show navigation
avoidance debug visuals when running the scene.</td>
</tr>
<tr>
<td><code>--debug-stringnames</code></td>
<td><img src="img/template_debug.svg" alt="debug" /> Print all
StringName allocations to stdout when the engine quits.</td>
</tr>
<tr>
<td><code>--frame-delay &lt;ms&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Simulate high
CPU load (delay each frame by &lt;ms&gt; milliseconds).</td>
</tr>
<tr>
<td><code>--time-scale &lt;scale&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Force time
scale (higher values are faster, 1.0 is normal speed).</td>
</tr>
<tr>
<td><code>--disable-vsync</code></td>
<td><img src="img/template_release.svg" alt="release" /> Forces
disabling of vertical synchronization, even if enabled in the project
settings. Does not override driver-level V-Sync enforcement.</td>
</tr>
<tr>
<td><code>--disable-render-loop</code></td>
<td><img src="img/template_release.svg" alt="release" /> Disable render
loop so rendering only occurs when called explicitly from script.</td>
</tr>
<tr>
<td><code>--disable-crash-handler</code></td>
<td><img src="img/template_release.svg" alt="release" /> Disable crash
handler when supported by the platform code.</td>
</tr>
<tr>
<td><code>--fixed-fps &lt;fps&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Force a fixed
number of frames per second. This setting disables real-time
synchronization.</td>
</tr>
<tr>
<td><code>--delta-smoothing &lt;enable&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Enable or
disable frame delta smoothing ('enable', 'disable').</td>
</tr>
<tr>
<td><code>--print-fps</code></td>
<td><img src="img/template_release.svg" alt="release" /> Print the
frames per second to the stdout.</td>
</tr>
</tbody>
</table>

**Standalone tools**

<table>
<colgroup>
<col style="width: 30%" />
<col style="width: 69%" />
</colgroup>
<tbody>
<tr>
<td>Command</td>
<td>Description</td>
</tr>
<tr>
<td><code>-s</code>, <code>--script &lt;script&gt;</code></td>
<td><img src="img/template_release.svg" alt="release" /> Run a
script.</td>
</tr>
<tr>
<td><code>--check-only</code></td>
<td><img src="img/template_release.svg" alt="release" /> Only parse for
errors and quit (use with <code>--script</code>).</td>
</tr>
<tr>
<td><code>--import</code></td>
<td><img src="img/editor.svg" alt="editor" /> Starts the editor, waits
for any resources to be imported, and then quits. Implies
<code>--editor</code> and <code>--quit</code>.</td>
</tr>
<tr>
<td><code>--export-release &lt;preset&gt; &lt;path&gt;</code></td>
<td><img src="img/editor.svg" alt="editor" /> Export the project using
the given preset and matching release template. The preset name should
match one defined in export_presets.cfg. <code>&lt;path&gt;</code>
should be absolute or relative to the project directory, and include the
filename for the binary (e.g. 'builds/game.exe'). The target directory
should exist. Implies <code>--import</code>.</td>
</tr>
<tr>
<td><code>--export-debug &lt;preset&gt; &lt;path&gt;</code></td>
<td><img src="img/editor.svg" alt="editor" /> Like
<code>--export-release</code>, but use debug template. Implies
<code>--import</code>.</td>
</tr>
<tr>
<td><code>--export-pack &lt;preset&gt; &lt;path&gt;</code></td>
<td><img src="img/editor.svg" alt="editor" /> Like
<code>--export-release</code>, but only export the game pack for the
given preset. The <code>&lt;path&gt;</code> extension determines whether
it will be in PCK or ZIP format. Implies <code>--import</code>.</td>
</tr>
<tr>
<td><code>--convert-3to4 [&lt;max_file_kb&gt;] [&lt;max_line_size&gt;]</code></td>
<td><img src="img/editor.svg" alt="editor" /> Convert project from Godot
3.x to Godot 4.x.</td>
</tr>
<tr>
<td><code>--validate-conversion-3to4 [&lt;max_file_kb&gt;] [&lt;max_line_size&gt;]</code></td>
<td><img src="img/editor.svg" alt="editor" /> Show what elements will be
renamed when converting project from Godot 3.x to Godot 4.x.</td>
</tr>
<tr>
<td><code>--doctool [&lt;path&gt;]</code></td>
<td><img src="img/editor.svg" alt="editor" /> Dump the engine API
reference to the given <code>&lt;path&gt;</code> in XML format, merging
if existing files are found.</td>
</tr>
<tr>
<td><code>--no-docbase</code></td>
<td><img src="img/editor.svg" alt="editor" /> Disallow dumping the base
types (used with <code>--doctool</code>).</td>
</tr>
<tr>
<td><code>--gdscript-docs &lt;path&gt;</code></td>
<td><img src="img/editor.svg" alt="editor" /> Rather than dumping the
engine API, generate API reference from the inline documentation in the
GDScript files found in &lt;path&gt; (used with
<code>--doctool</code>).</td>
</tr>
<tr>
<td><code>--build-solutions</code></td>
<td><img src="img/editor.svg" alt="editor" /> Build the scripting
solutions (e.g. for C# projects). Implies <code>--editor</code> and
requires a valid project to edit.</td>
</tr>
<tr>
<td><code>--dump-gdextension-interface</code></td>
<td><img src="img/editor.svg" alt="editor" /> Generate GDExtension
header file 'gdnative_interface.h' in the current folder. This file is
the base file required to implement a GDExtension.</td>
</tr>
<tr>
<td><code>--dump-extension-api</code></td>
<td><img src="img/editor.svg" alt="editor" /> Generate JSON dump of the
Godot API for GDExtension bindings named 'extension_api.json' in the
current folder.</td>
</tr>
<tr>
<td><code>--validate-extension-api &lt;path&gt;</code></td>
<td><img src="img/editor.svg" alt="editor" /> Validate an extension API
file dumped (with the option above) from a previous version of the
engine to ensure API compatibility. If incompatibilities or errors are
detected, the return code will be non-zero.</td>
</tr>
<tr>
<td><code>--benchmark</code></td>
<td><img src="img/editor.svg" alt="editor" /> Benchmark the run time and
print it to console.</td>
</tr>
<tr>
<td><code>--benchmark-file &lt;path&gt;</code></td>
<td><img src="img/editor.svg" alt="editor" /> Benchmark the run time and
save it to a given file in JSON format. The path should be
absolute.</td>
</tr>
</tbody>
</table>

## Path

It is recommended to place your Godot editor binary in your `PATH`
environment variable, so it can be executed easily from any place by
typing `godot`. You can do so on Linux by placing the Godot binary in
`/usr/local/bin` and making sure it is called `godot` (case-sensitive).

To achieve this on Windows or macOS easily, you can install Godot using
[Scoop](https://scoop.sh) (on Windows) or [Homebrew](https://brew.sh)
(on macOS). This will automatically make the copy of Godot installed
available in the `PATH`:

sh Windows

\# Add "Extras" bucket scoop bucket add extras

\# Standard editor: scoop install godot

\# Editor with C# support (will be available as
<span class="title-ref">godot-mono</span> in
<span class="title-ref">PATH</span>): scoop install godot-mono

sh macOS

\# Standard editor: brew install godot

\# Editor with C# support (will be available as
<span class="title-ref">godot-mono</span> in
<span class="title-ref">PATH</span>): brew install godot-mono

## Setting the project path

Depending on where your Godot binary is located and what your current
working directory is, you may need to set the path to your project for
any of the following commands to work correctly.

When running the editor, this can be done by giving the path to the
`project.godot` file of your project as either the first argument, like
this:

    godot path_to_your_project/project.godot [other] [commands] [and] [args]

For all commands, this can be done by using the `--path` argument:

    godot --path path_to_your_project [other] [commands] [and] [args]

For example, the full command for exporting your game (as explained
below) might look like this:

    godot --headless --path path_to_your_project --export-release my_export_preset_name game.exe

When starting from a subdirectory of your project, use the `--upwards`
argument for Godot to automatically find the `project.godot` file by
recursively searching the parent directories.

For example, running a scene (as explained below) nested in a
subdirectory might look like this when your working directory is in the
same path:

    godot --upwards nested_scene.tscn 

## Creating a project

Creating a project from the command line can be done by navigating the
shell to the desired place and making a `project.godot` file.

    mkdir newgame
    cd newgame
    touch project.godot

The project can now be opened with Godot.

## Running the editor

Running the editor is done by executing Godot with the `-e` flag. This
must be done from within the project directory or by setting the project
path as explained above, otherwise the command is ignored and the
Project Manager appears.

    godot -e

When passing in the full path to the `project.godot` file, the `-e` flag
may be omitted.

If a scene has been created and saved, it can be edited later by running
the same code with that scene as argument.

    godot -e scene.tscn

## Erasing a scene

Godot is friends with your filesystem and will not create extra metadata
files. Use `rm` to erase a scene file. Make sure nothing references that
scene. Otherwise, an error will be thrown upon opening the project.

    rm scene.tscn

## Running the game

To run the game, execute Godot within the project directory or with the
project path as explained above.

    godot

Note that passing in the `project.godot` file will always run the editor
instead of running the game.

When a specific scene needs to be tested, pass that scene to the command
line.

    godot scene.tscn

## Debugging

Catching errors in the command line can be a difficult task because they
scroll quickly. For this, a command line debugger is provided by adding
`-d`. It works for running either the game or a single scene.

    godot -d

    godot -d scene.tscn

## Exporting

Exporting the project from the command line is also supported. This is
especially useful for continuous integration setups.

Note

Using the `--headless` command line argument is **required** on
platforms that do not have GPU access (such as continuous integration).
On platforms with GPU access, `--headless` prevents a window from
spawning while the project is exporting.

    # `godot` must be a Godot editor binary, not an export template.
    # Also, export templates must be installed for the editor
    # (or a valid custom export template must be defined in the export preset).
    godot --headless --export-release "Linux/X11" /var/builds/project
    godot --headless --export-release Android /var/builds/project.apk

The preset name must match the name of an export preset defined in the
project's `export_presets.cfg` file. If the preset name contains spaces
or special characters (such as "Windows Desktop"), it must be surrounded
with quotes.

To export a debug version of the game, use the `--export-debug` switch
instead of `--export-release`. Their parameters and usage are the same.

To export only a PCK file, use the `--export-pack` option followed by
the preset name and output path, with the file extension, instead of
`--export-release` or `--export-debug`. The output path extension
determines the package's format, either PCK or ZIP.

Warning

When specifying a relative path as the path for `--export-release`,
`--export-debug` or `--export-pack`, the path will be relative to the
directory containing the `project.godot` file, **not** relative to the
current working directory.

## Running a script

It is possible to run a `.gd` script from the command line. This feature
is especially useful in large projects, e.g. for batch conversion of
assets or custom import/export.

The script must inherit from `SceneTree` or `MainLoop`.

Here is an example `sayhello.gd`, showing how it works:

    #!/usr/bin/env -S godot -s
    extends SceneTree

    func _init():
        print("Hello!")
        quit()

And how to run it:

    # Prints "Hello!" to standard output.
    godot -s sayhello.gd

If no `project.godot` exists at the path, current path is assumed to be
the current working directory (unless `--path` is specified).

The first line of `sayhello.gd` above is commonly referred to as a
*shebang*. If the Godot binary is in your `PATH` as `godot`, it allows
you to run the script as follows in modern Linux distributions, as well
as macOS:

    # Mark script as executable.
    chmod +x sayhello.gd
    # Prints "Hello!" to standard output.
    ./sayhello.gd

If the above doesn't work in your current version of Linux or macOS, you
can always have the shebang run Godot straight from where it is located
as follows:

    #!/usr/bin/godot -s
