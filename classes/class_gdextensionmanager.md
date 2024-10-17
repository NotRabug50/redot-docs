github\_url  
hide

# GDExtensionManager

**Inherits:** `Object<class_Object>`

Provides access to GDExtension functionality.

classref-introduction-group

## Description

The GDExtensionManager loads, initializes, and keeps track of all
available `GDExtension<class_GDExtension>` libraries in the project.

\*\*Note:\*\* Do not worry about GDExtension unless you know what you
are doing.

classref-introduction-group

## Tutorials

-   `GDExtension overview <../tutorials/scripting/gdextension/what_is_gdextension>`
-   `GDExtension example in C++ <../tutorials/scripting/gdextension/gdextension_cpp_example>`

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

## Signals

classref-signal

**extension\_loaded**(extension: `GDExtension<class_GDExtension>`)
`🔗<class_GDExtensionManager_signal_extension_loaded>`

Emitted after the editor has finished loading a new extension.

\*\*Note:\*\* This signal is only emitted in editor builds.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**extension\_unloading**(extension: `GDExtension<class_GDExtension>`)
`🔗<class_GDExtensionManager_signal_extension_unloading>`

Emitted before the editor starts unloading an extension.

\*\*Note:\*\* This signal is only emitted in editor builds.

classref-item-separator

------------------------------------------------------------------------

classref-signal

**extensions\_reloaded**()
`🔗<class_GDExtensionManager_signal_extensions_reloaded>`

Emitted after the editor has finished reloading one or more extensions.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **LoadStatus**: `🔗<enum_GDExtensionManager_LoadStatus>`

classref-enumeration-constant

`LoadStatus<enum_GDExtensionManager_LoadStatus>` **LOAD\_STATUS\_OK** =
`0`

The extension has loaded successfully.

classref-enumeration-constant

`LoadStatus<enum_GDExtensionManager_LoadStatus>`
**LOAD\_STATUS\_FAILED** = `1`

The extension has failed to load, possibly because it does not exist or
has missing dependencies.

classref-enumeration-constant

`LoadStatus<enum_GDExtensionManager_LoadStatus>`
**LOAD\_STATUS\_ALREADY\_LOADED** = `2`

The extension has already been loaded.

classref-enumeration-constant

`LoadStatus<enum_GDExtensionManager_LoadStatus>`
**LOAD\_STATUS\_NOT\_LOADED** = `3`

The extension has not been loaded.

classref-enumeration-constant

`LoadStatus<enum_GDExtensionManager_LoadStatus>`
**LOAD\_STATUS\_NEEDS\_RESTART** = `4`

The extension requires the application to restart to fully load.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`GDExtension<class_GDExtension>` **get\_extension**(path:
`String<class_String>`)
`🔗<class_GDExtensionManager_method_get_extension>`

Returns the `GDExtension<class_GDExtension>` at the given file `path`,
or `null` if it has not been loaded or does not exist.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_loaded\_extensions**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GDExtensionManager_method_get_loaded_extensions>`

Returns the file paths of all currently loaded extensions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_extension\_loaded**(path:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GDExtensionManager_method_is_extension_loaded>`

Returns `true` if the extension at the given file `path` has already
been loaded successfully. See also
`get_loaded_extensions<class_GDExtensionManager_method_get_loaded_extensions>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`LoadStatus<enum_GDExtensionManager_LoadStatus>`
**load\_extension**(path: `String<class_String>`)
`🔗<class_GDExtensionManager_method_load_extension>`

Loads an extension by absolute file path. The `path` needs to point to a
valid `GDExtension<class_GDExtension>`. Returns
`LOAD_STATUS_OK<class_GDExtensionManager_constant_LOAD_STATUS_OK>` if
successful.

classref-item-separator

------------------------------------------------------------------------

classref-method

`LoadStatus<enum_GDExtensionManager_LoadStatus>`
**reload\_extension**(path: `String<class_String>`)
`🔗<class_GDExtensionManager_method_reload_extension>`

Reloads the extension at the given file path. The `path` needs to point
to a valid `GDExtension<class_GDExtension>`, otherwise this method may
return either
`LOAD_STATUS_NOT_LOADED<class_GDExtensionManager_constant_LOAD_STATUS_NOT_LOADED>`
or
`LOAD_STATUS_FAILED<class_GDExtensionManager_constant_LOAD_STATUS_FAILED>`.

\*\*Note:\*\* You can only reload extensions in the editor. In release
builds, this method always fails and returns
`LOAD_STATUS_FAILED<class_GDExtensionManager_constant_LOAD_STATUS_FAILED>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`LoadStatus<enum_GDExtensionManager_LoadStatus>`
**unload\_extension**(path: `String<class_String>`)
`🔗<class_GDExtensionManager_method_unload_extension>`

Unloads an extension by file path. The `path` needs to point to an
already loaded `GDExtension<class_GDExtension>`, otherwise this method
returns
`LOAD_STATUS_NOT_LOADED<class_GDExtensionManager_constant_LOAD_STATUS_NOT_LOADED>`.
