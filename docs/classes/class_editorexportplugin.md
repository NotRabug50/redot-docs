github\_url  
hide

# EditorExportPlugin

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

A script that is executed when exporting the project.

classref-introduction-group

## Description

**EditorExportPlugin**s are automatically invoked whenever the user
exports the project. Their most common use is to determine what files
are being included in the exported project. For each plugin,
`_export_begin<class_EditorExportPlugin_private_method__export_begin>`
is called at the beginning of the export process and then
`_export_file<class_EditorExportPlugin_private_method__export_file>` is
called for each exported file.

To use **EditorExportPlugin**, register it using the
`EditorPlugin.add_export_plugin<class_EditorPlugin_method_add_export_plugin>`
method first.

classref-introduction-group

## Tutorials

-   `Export Android plugins <../tutorials/platform/android/android_plugin>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **\_begin\_customize\_resources**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`, features:
`PackedStringArray<class_PackedStringArray>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__begin_customize_resources>`

Return `true` if this plugin will customize resources based on the
platform and features used.

When enabled,
`_get_customization_configuration_hash<class_EditorExportPlugin_private_method__get_customization_configuration_hash>`
and
`_customize_resource<class_EditorExportPlugin_private_method__customize_resource>`
will be called and must be implemented.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_begin\_customize\_scenes**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`, features:
`PackedStringArray<class_PackedStringArray>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__begin_customize_scenes>`

Return `true` if this plugin will customize scenes based on the platform
and features used.

When enabled,
`_get_customization_configuration_hash<class_EditorExportPlugin_private_method__get_customization_configuration_hash>`
and
`_customize_scene<class_EditorExportPlugin_private_method__customize_scene>`
will be called and must be implemented.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Resource<class_Resource>` **\_customize\_resource**(resource:
`Resource<class_Resource>`, path: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlugin_private_method__customize_resource>`

Customize a resource. If changes are made to it, return the same or a
new resource. Otherwise, return `null`.

The *path* argument is only used when customizing an actual file,
otherwise this means that this resource is part of another one and it
will be empty.

Implementing this method is required if
`_begin_customize_resources<class_EditorExportPlugin_private_method__begin_customize_resources>`
returns `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **\_customize\_scene**(scene: `Node<class_Node>`,
path: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlugin_private_method__customize_scene>`

Customize a scene. If changes are made to it, return the same or a new
scene. Otherwise, return `null`. If a new scene is returned, it is up to
you to dispose of the old one.

Implementing this method is required if
`_begin_customize_scenes<class_EditorExportPlugin_private_method__begin_customize_scenes>`
returns `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_end\_customize\_resources**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlugin_private_method__end_customize_resources>`

This is called when the customization process for resources ends.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_end\_customize\_scenes**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlugin_private_method__end_customize_scenes>`

This is called when the customization process for scenes ends.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_export\_begin**(features:
`PackedStringArray<class_PackedStringArray>`, is\_debug:
`bool<class_bool>`, path: `String<class_String>`, flags:
`int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlugin_private_method__export_begin>`

Virtual method to be overridden by the user. It is called when the
export starts and provides all information about the export. `features`
is the list of features for the export, `is_debug` is `true` for debug
builds, `path` is the target path for the exported project. `flags` is
only used when running a runnable profile, e.g. when using native run on
Android.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_export\_end**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlugin_private_method__export_end>`

Virtual method to be overridden by the user. Called when the export is
finished.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **\_export\_file**(path:
`String<class_String>`, type: `String<class_String>`, features:
`PackedStringArray<class_PackedStringArray>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_EditorExportPlugin_private_method__export_file>`

Virtual method to be overridden by the user. Called for each exported
file before
`_customize_resource<class_EditorExportPlugin_private_method__customize_resource>`
and
`_customize_scene<class_EditorExportPlugin_private_method__customize_scene>`.
The arguments can be used to identify the file. `path` is the path of
the file, `type` is the `Resource<class_Resource>` represented by the
file (e.g. `PackedScene<class_PackedScene>`), and `features` is the list
of features for the export.

Calling `skip<class_EditorExportPlugin_method_skip>` inside this
callback will make the file not included in the export.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_android\_dependencies**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`, debug:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_android_dependencies>`

Virtual method to be overridden by the user. This is called to retrieve
the set of Android dependencies provided by this plugin. Each returned
Android dependency should have the format of an Android remote binary
dependency: `org.godot.example:my-plugin:0.0.0`

For more information see [Android documentation on
dependencies](https://developer.android.com/build/dependencies?agpversion=4.1#dependency-types).

\*\*Note:\*\* Only supported on Android and requires
`EditorExportPlatformAndroid.gradle_build/use_gradle_build<class_EditorExportPlatformAndroid_property_gradle_build/use_gradle_build>`
to be enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_android\_dependencies\_maven\_repos**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`, debug:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_android_dependencies_maven_repos>`

Virtual method to be overridden by the user. This is called to retrieve
the URLs of Maven repositories for the set of Android dependencies
provided by this plugin.

For more information see [Gradle documentation on dependency
management](https://docs.gradle.org/current/userguide/dependency_management.html#sec:maven_repo).

\*\*Note:\*\* Google's Maven repo and the Maven Central repo are already
included by default.

\*\*Note:\*\* Only supported on Android and requires
`EditorExportPlatformAndroid.gradle_build/use_gradle_build<class_EditorExportPlatformAndroid_property_gradle_build/use_gradle_build>`
to be enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_android\_libraries**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`, debug:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_android_libraries>`

Virtual method to be overridden by the user. This is called to retrieve
the local paths of the Android libraries archive (AAR) files provided by
this plugin.

\*\*Note:\*\* Relative paths **must** be relative to Godot's
`res://addons/` directory. For example, an AAR file located under
`res://addons/hello_world_plugin/HelloWorld.release.aar` can be returned
as an absolute path using
`res://addons/hello_world_plugin/HelloWorld.release.aar` or a relative
path using `hello_world_plugin/HelloWorld.release.aar`.

\*\*Note:\*\* Only supported on Android and requires
`EditorExportPlatformAndroid.gradle_build/use_gradle_build<class_EditorExportPlatformAndroid_property_gradle_build/use_gradle_build>`
to be enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>`
**\_get\_android\_manifest\_activity\_element\_contents**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`, debug:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_android_manifest_activity_element_contents>`

Virtual method to be overridden by the user. This is used at export time
to update the contents of the `activity` element in the generated
Android manifest.

\*\*Note:\*\* Only supported on Android and requires
`EditorExportPlatformAndroid.gradle_build/use_gradle_build<class_EditorExportPlatformAndroid_property_gradle_build/use_gradle_build>`
to be enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>`
**\_get\_android\_manifest\_application\_element\_contents**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`, debug:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_android_manifest_application_element_contents>`

Virtual method to be overridden by the user. This is used at export time
to update the contents of the `application` element in the generated
Android manifest.

\*\*Note:\*\* Only supported on Android and requires
`EditorExportPlatformAndroid.gradle_build/use_gradle_build<class_EditorExportPlatformAndroid_property_gradle_build/use_gradle_build>`
to be enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>`
**\_get\_android\_manifest\_element\_contents**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`, debug:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_android_manifest_element_contents>`

Virtual method to be overridden by the user. This is used at export time
to update the contents of the `manifest` element in the generated
Android manifest.

\*\*Note:\*\* Only supported on Android and requires
`EditorExportPlatformAndroid.gradle_build/use_gradle_build<class_EditorExportPlatformAndroid_property_gradle_build/use_gradle_build>`
to be enabled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_customization\_configuration\_hash**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_customization_configuration_hash>`

Return a hash based on the configuration passed (for both scenes and
resources). This helps keep separate caches for separate export
configurations.

Implementing this method is required if
`_begin_customize_resources<class_EditorExportPlugin_private_method__begin_customize_resources>`
returns `true`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_export\_features**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`, debug:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_export_features>`

Return a `PackedStringArray<class_PackedStringArray>` of additional
features this preset, for the given `platform`, should have.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_get\_export\_option\_visibility**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`, option:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_export_option_visibility>`

**Optional.**

Validates `option` and returns the visibility for the specified
`platform`. The default implementation returns `true` for all options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_export\_option\_warning**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`, option:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_export_option_warning>`

Check the requirements for the given `option` and return a non-empty
warning string if they are not met.

\*\*Note:\*\* Use
`get_option<class_EditorExportPlugin_method_get_option>` to check the
value of the export options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**\_get\_export\_options**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_export_options>`

Return a list of export options that can be configured for this export
plugin.

Each element in the return value is a `Dictionary<class_Dictionary>`
with the following keys:

-   `option`: A dictionary with the structure documented by
    `Object.get_property_list<class_Object_method_get_property_list>`,
    but all keys are optional.
-   `default_value`: The default value for this option.
-   `update_visibility`: An optional boolean value. If set to `true`,
    the preset will emit
    `Object.property_list_changed<class_Object_signal_property_list_changed>`
    when the option is changed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>`
**\_get\_export\_options\_overrides**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_export_options_overrides>`

Return a `Dictionary<class_Dictionary>` of override values for export
options, that will be used instead of user-provided values. Overridden
options will be hidden from the user interface.

    class MyExportPlugin extends EditorExportPlugin:
        func _get_name() -> String:
            return "MyExportPlugin"

        func _supports_platform(platform) -> bool:
            if platform is EditorExportPlatformPC:
                # Run on all desktop platforms including Windows, MacOS and Linux.
                return true
            return false

        func _get_export_options_overrides(platform) -> Dictionary:
            # Override "Embed PCK" to always be enabled.
            return {
                "binary_format/embed_pck": true,
            }

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_name**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__get_name>`

Return the name identifier of this plugin (for future identification by
the exporter). The plugins are sorted by name before exporting.

Implementing this method is required.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_should\_update\_export\_options**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__should_update_export_options>`

Return `true`, if the result of
`_get_export_options<class_EditorExportPlugin_private_method__get_export_options>`
has changed and the export options of preset corresponding to `platform`
should be updated.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_supports\_platform**(platform:
`EditorExportPlatform<class_EditorExportPlatform>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_private_method__supports_platform>`

Return `true` if the plugin supports the given `platform`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_file**(path: `String<class_String>`,
file: `PackedByteArray<class_PackedByteArray>`, remap:
`bool<class_bool>`) `🔗<class_EditorExportPlugin_method_add_file>`

Adds a custom file to be exported. `path` is the virtual path that can
be used to load the file, `file` is the binary data of the file.

When called inside
`_export_file<class_EditorExportPlugin_private_method__export_file>` and
`remap` is `true`, the current file will not be exported, but instead
remapped to this custom file. `remap` is ignored when called in other
places.

`file` will not be imported, so consider using
`_customize_resource<class_EditorExportPlugin_private_method__customize_resource>`
to remap imported resources.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_ios\_bundle\_file**(path:
`String<class_String>`)
`🔗<class_EditorExportPlugin_method_add_ios_bundle_file>`

Adds an iOS bundle file from the given `path` to the exported project.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_ios\_cpp\_code**(code:
`String<class_String>`)
`🔗<class_EditorExportPlugin_method_add_ios_cpp_code>`

Adds a C++ code to the iOS export. The final code is created from the
code appended by each active export plugin.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_ios\_embedded\_framework**(path:
`String<class_String>`)
`🔗<class_EditorExportPlugin_method_add_ios_embedded_framework>`

Adds a dynamic library (\*.dylib, \*.framework) to Linking Phase in
iOS's Xcode project and embeds it into resulting binary.

\*\*Note:\*\* For static libraries (\*.a) works in same way as
`add_ios_framework<class_EditorExportPlugin_method_add_ios_framework>`.

\*\*Note:\*\* This method should not be used for System libraries as
they are already present on the device.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_ios\_framework**(path:
`String<class_String>`)
`🔗<class_EditorExportPlugin_method_add_ios_framework>`

Adds a static library (\*.a) or dynamic library (\*.dylib, \*.framework)
to Linking Phase in iOS's Xcode project.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_ios\_linker\_flags**(flags:
`String<class_String>`)
`🔗<class_EditorExportPlugin_method_add_ios_linker_flags>`

Adds linker flags for the iOS export.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_ios\_plist\_content**(plist\_content:
`String<class_String>`)
`🔗<class_EditorExportPlugin_method_add_ios_plist_content>`

Adds content for iOS Property List files.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_ios\_project\_static\_lib**(path:
`String<class_String>`)
`🔗<class_EditorExportPlugin_method_add_ios_project_static_lib>`

Adds a static lib from the given `path` to the iOS project.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_macos\_plugin\_file**(path:
`String<class_String>`)
`🔗<class_EditorExportPlugin_method_add_macos_plugin_file>`

Adds file or directory matching `path` to `PlugIns` directory of macOS
app bundle.

\*\*Note:\*\* This is useful only for macOS exports.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_shared\_object**(path:
`String<class_String>`, tags:
`PackedStringArray<class_PackedStringArray>`, target:
`String<class_String>`)
`🔗<class_EditorExportPlugin_method_add_shared_object>`

Adds a shared object or a directory containing only shared objects with
the given `tags` and destination `path`.

\*\*Note:\*\* In case of macOS exports, those shared objects will be
added to `Frameworks` directory of app bundle.

In case of a directory code-sign will error if you place non code object
in directory.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorExportPlatform<class_EditorExportPlatform>`
**get\_export\_platform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_method_get_export_platform>`

Returns currently used export platform.

classref-item-separator

------------------------------------------------------------------------

classref-method

`EditorExportPreset<class_EditorExportPreset>` **get\_export\_preset**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_method_get_export_preset>`

Returns currently used export preset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_option**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_EditorExportPlugin_method_get_option>`

Returns the current value of an export option supplied by
`_get_export_options<class_EditorExportPlugin_private_method__get_export_options>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **skip**()
`🔗<class_EditorExportPlugin_method_skip>`

To be called inside
`_export_file<class_EditorExportPlugin_private_method__export_file>`.
Skips the current file, so it's not included in the export.
