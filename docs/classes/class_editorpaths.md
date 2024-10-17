github\_url  
hide

# EditorPaths

**Inherits:** `Object<class_Object>`

Editor-only singleton that returns paths to various OS-specific data
folders and files.

classref-introduction-group

## Description

This editor-only singleton returns OS-specific paths to various data
folders and files. It can be used in editor plugins to ensure files are
saved in the correct location on each operating system.

\*\*Note:\*\* This singleton is not accessible in exported projects.
Attempting to access it in an exported project will result in a script
error as the singleton won't be declared. To prevent script errors in
exported projects, use
`Engine.has_singleton<class_Engine_method_has_singleton>` to check
whether the singleton is available before using it.

\*\*Note:\*\* On the Linux/BSD platform, Godot complies with the [XDG
Base Directory
Specification](https://specifications.freedesktop.org/basedir-spec/basedir-spec-latest.html).
You can override environment variables following the specification to
change the editor and project data paths.

classref-introduction-group

## Tutorials

-   `File paths in Godot projects <../tutorials/io/data_paths>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`String<class_String>` **get\_cache\_dir**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPaths_method_get_cache_dir>`

Returns the absolute path to the user's cache folder. This folder should
be used for temporary data that can be removed safely whenever the
editor is closed (such as generated resource thumbnails).

\*\*Default paths per platform:\*\*

    - Windows: %LOCALAPPDATA%\Godot\
    - macOS: ~/Library/Caches/Godot/
    - Linux: ~/.cache/godot/

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_config\_dir**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPaths_method_get_config_dir>`

Returns the absolute path to the user's configuration folder. This
folder should be used for *persistent* user configuration files.

\*\*Default paths per platform:\*\*

    - Windows: %APPDATA%\Godot\                    (same as `get_data_dir()`)
    - macOS: ~/Library/Application Support/Godot/  (same as `get_data_dir()`)
    - Linux: ~/.config/godot/

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_data\_dir**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPaths_method_get_data_dir>`

Returns the absolute path to the user's data folder. This folder should
be used for *persistent* user data files such as installed export
templates.

\*\*Default paths per platform:\*\*

    - Windows: %APPDATA%\Godot\                    (same as `get_config_dir()`)
    - macOS: ~/Library/Application Support/Godot/  (same as `get_config_dir()`)
    - Linux: ~/.local/share/godot/

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_project\_settings\_dir**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPaths_method_get_project_settings_dir>`

Returns the project-specific editor settings path. Projects all have a
unique subdirectory inside the settings path where project-specific
editor settings are saved.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_self\_contained\_file**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPaths_method_get_self_contained_file>`

Returns the absolute path to the self-contained file that makes the
current Godot editor instance be considered as self-contained. Returns
an empty string if the current Godot editor instance isn't
self-contained. See also
`is_self_contained<class_EditorPaths_method_is_self_contained>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_self\_contained**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorPaths_method_is_self_contained>`

Returns `true` if the editor is marked as self-contained, `false`
otherwise. When self-contained mode is enabled, user configuration, data
and cache files are saved in an `editor_data/` folder next to the editor
binary. This makes portable usage easier and ensures the Godot editor
minimizes file writes outside its own folder. Self-contained mode is not
available for exported projects.

Self-contained mode can be enabled by creating a file named `._sc_` or
`_sc_` in the same folder as the editor binary or macOS .app bundle
while the editor is not running. See also
`get_self_contained_file<class_EditorPaths_method_get_self_contained_file>`.

\*\*Note:\*\* On macOS, quarantine flag should be manually removed
before using self-contained mode, see [Running on
macOS](https://docs.godotengine.org/en/stable/tutorials/export/running_on_macos.html).

\*\*Note:\*\* On macOS, placing `_sc_` or any other file inside .app
bundle will break digital signature and make it non-portable, consider
placing it in the same folder as the .app bundle instead.

\*\*Note:\*\* The Steam release of Godot uses self-contained mode by
default.
