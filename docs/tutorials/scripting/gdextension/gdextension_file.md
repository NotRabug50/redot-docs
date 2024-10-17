# The .gdextension file

## Introduction

The `.gdextension` file in your project contains the instructions for
how to load the GDExtension. The instructions are separated into
specific sections. This page should give you a quick overview of the
different options available to you. For an introduction how to get
started with GDExtensions take a look at the
`GDExtension C++ Example <doc_gdextension_cpp_example>`.

## Configuration section

<table style="width:99%;">
<colgroup>
<col style="width: 21%" />
<col style="width: 8%" />
<col style="width: 69%" />
</colgroup>
<thead>
<tr>
<th>Property</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>entry_symbol</strong></td>
<td>String</td>
<td>Name of the entry function for initializing the GDExtension. This
function should be defined in the <code>register_types.cpp</code> file
when using godot-cpp. Adding this is necessary for the extension to
work.</td>
</tr>
<tr>
<td><strong>compatibility_minimum</strong></td>
<td>String</td>
<td>Minimum compatible version. This prevents older versions of Godot
from loading extensions that depend on features from newer versions of
Godot. <strong>Only supported in Godot 4.1 or later</strong></td>
</tr>
<tr>
<td><strong>compatibility_maximum</strong></td>
<td>String</td>
<td>Maximum compatible version. This prevents newer versions of Godot
from loading the extension. <strong>Only supported in Godot 4.3 or
later</strong></td>
</tr>
<tr>
<td><strong>reloadable</strong></td>
<td>Boolean</td>
<td>Reloads the extension upon recompilation. Reloading is supported for
the godot-cpp binding in Godot 4.2 or later. Other language bindings may
or may not support it as well. This flag should be mainly used for
developing or debugging an extension.</td>
</tr>
<tr>
<td><strong>android_aar_plugin</strong></td>
<td>Boolean</td>
<td>The GDExtension is part of a <code class="interpreted-text"
role="ref">v2 Android plugin &lt;doc_android_plugin&gt;</code>. During
export this flag will indicate to the editor that the GDExtension native
shared libraries are exported by the Android plugin AAR binaries.</td>
</tr>
</tbody>
</table>

## Libraries section

In this section you can set the paths to the compiled binaries of your
GDExtension libraries. By specifying feature flags you can filter which
version should be loaded and exported with your game depending on which
feature flags are active. Every feature flag must match to Godot's
feature flags or your custom export flags to be loaded in an exported
game. For instance `macos.debug` means that it will be loaded if Godot
has both the `macos` and `debug` flag active. Each line of the section
is evaluated from top to bottom.

Here is an example of what that can look like:

    [libraries]

    macos.debug = "res://bin/libgdexample.macos.template_debug.framework"
    macos.release = "res://bin/libgdexample.macos.template_release.framework"
    windows.debug.x86_32 = "res://bin/libgdexample.windows.template_debug.x86_32.dll"
    windows.release.x86_32 = "res://bin/libgdexample.windows.template_release.x86_32.dll"
    windows.debug.x86_64 = "res://bin/libgdexample.windows.template_debug.x86_64.dll"
    windows.release.x86_64 = "res://bin/libgdexample.windows.template_release.x86_64.dll"
    linux.debug.x86_64 = "res://bin/libgdexample.linux.template_debug.x86_64.so"
    linux.release.x86_64 = "res://bin/libgdexample.linux.template_release.x86_64.so"
    linux.debug.arm64 = "res://bin/libgdexample.linux.template_debug.arm64.so"
    linux.release.arm64 = "res://bin/libgdexample.linux.template_release.arm64.so"
    linux.debug.rv64 = "res://bin/libgdexample.linux.template_debug.rv64.so"
    linux.release.rv64 = "res://bin/libgdexample.linux.template_release.rv64.so"

Here are lists of some of the available built-in options (for more look
at the `feature tags <doc_feature_tags>`):

### Running system

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 76%" />
</colgroup>
<thead>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>windows</strong></td>
<td>Windows operating system</td>
</tr>
<tr>
<td><strong>macos</strong></td>
<td>Mac operating system</td>
</tr>
<tr>
<td><strong>linux</strong></td>
<td>Linux operating system</td>
</tr>
<tr>
<td><strong>bsd</strong></td>
<td>BSD operating system</td>
</tr>
<tr>
<td><strong>linuxbsd</strong></td>
<td>Linux or BSD operating system</td>
</tr>
<tr>
<td><strong>android</strong></td>
<td>Android operating system</td>
</tr>
<tr>
<td><strong>ios</strong></td>
<td>iOS operating system</td>
</tr>
<tr>
<td><strong>web</strong></td>
<td>Web browser</td>
</tr>
</tbody>
</table>

### Build

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 76%" />
</colgroup>
<thead>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>debug</strong></td>
<td>Build with debug symbols</td>
</tr>
<tr>
<td><strong>release</strong></td>
<td>Optimized build without debug symbols</td>
</tr>
<tr>
<td><strong>editor</strong></td>
<td>Editor build</td>
</tr>
</tbody>
</table>

### Architecture

<table>
<colgroup>
<col style="width: 23%" />
<col style="width: 76%" />
</colgroup>
<thead>
<tr>
<th>Flag</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>double</strong></td>
<td>double-precision build</td>
</tr>
<tr>
<td><strong>single</strong></td>
<td>single-precision build</td>
</tr>
<tr>
<td><strong>x86_64</strong></td>
<td>64-bit x86 build</td>
</tr>
<tr>
<td><strong>arm64</strong></td>
<td>64-bit ARM build</td>
</tr>
<tr>
<td><strong>rv64</strong></td>
<td>64-bit RISC-V build</td>
</tr>
<tr>
<td><strong>riscv</strong></td>
<td>RISC-V build (any bitness)</td>
</tr>
<tr>
<td><strong>wasm32</strong></td>
<td>32-bit WebAssembly build</td>
</tr>
</tbody>
</table>

## Icons section

By default, Godot uses the Node icon in the scene dock for GDExtension
nodes. A custom icon can be set by reference to its name and resource
path of an SVG file.

For example:

    [icons]

    GDExample = "res://icons/gd_example.svg"

The path should point to a 16 by 16 pixel SVG image. Read the guide for
`creating icons <doc_editor_icons>` for more information.

## Dependencies section

In this section you set the paths of the GDExtension dependencies. This
is used internally to export the dependencies when exporting your game
executable. You are able to set which dependency is loaded depending on
the feature flags of the exported executable. In addition, you are able
to set an optional subdirectory to move your dependencies into. If no
path is supplied Godot will move the libraries into the same directory
as your game executable.

Warning

In MacOS it is necessary to have shared libraries inside a folder called
`Frameworks` with a directory structure like this:
`Game.app/Contents/Frameworks`.

    [dependencies]

    macos.debug = {
        "res://bin/libdependency.macos.template_debug.framework" : "Contents/Frameworks"
    }
    macos.release = {
        "res://bin/libdependency.macos.template_release.framework" : "Contents/Frameworks"
    }
    windows.debug = {
        "res://bin/libdependency.windows.template_debug.x86_64.dll" : "",
        "res://bin/libdependency.windows.template_debug.x86_32.dll" : ""
    }
    windows.release = {
        "res://bin/libdependency.windows.template_release.x86_64.dll" : "",
        "res://bin/libdependency.windows.template_release.x86_32.dll" : ""
    }
    linux.debug = {
        "res://bin/libdependency.linux.template_debug.x86_64.so" : "",
        "res://bin/libdependency.linux.template_debug.arm64.so" : "",
        "res://bin/libdependency.linux.template_debug.rv64.so" : ""
    }
    linux.release = {
        "res://bin/libdependency.linux.template_release.x86_64.so" : "",
        "res://bin/libdependency.linux.template_release.arm64.so" : "",
        "res://bin/libdependency.linux.template_release.rv64.so" : ""
    }
