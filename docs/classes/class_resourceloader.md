github\_url  
hide

# ResourceLoader

**Inherits:** `Object<class_Object>`

A singleton for loading resource files.

classref-introduction-group

## Description

A singleton used to load resource files from the filesystem.

It uses the many `ResourceFormatLoader<class_ResourceFormatLoader>`
classes registered in the engine (either built-in or from a plugin) to
load files into memory and convert them to a format that can be used by
the engine.

\*\*Note:\*\* You have to import the files into the engine first to load
them using `load<class_ResourceLoader_method_load>`. If you want to load
`Image<class_Image>`s at run-time, you may use
`Image.load<class_Image_method_load>`. If you want to import audio
files, you can use the snippet described in
`AudioStreamMP3.data<class_AudioStreamMP3_property_data>`.

classref-introduction-group

## Tutorials

-   [Operating System Testing
    Demo](https://godotengine.org/asset-library/asset/2789)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ThreadLoadStatus**: `🔗<enum_ResourceLoader_ThreadLoadStatus>`

classref-enumeration-constant

`ThreadLoadStatus<enum_ResourceLoader_ThreadLoadStatus>`
**THREAD\_LOAD\_INVALID\_RESOURCE** = `0`

The resource is invalid, or has not been loaded with
`load_threaded_request<class_ResourceLoader_method_load_threaded_request>`.

classref-enumeration-constant

`ThreadLoadStatus<enum_ResourceLoader_ThreadLoadStatus>`
**THREAD\_LOAD\_IN\_PROGRESS** = `1`

The resource is still being loaded.

classref-enumeration-constant

`ThreadLoadStatus<enum_ResourceLoader_ThreadLoadStatus>`
**THREAD\_LOAD\_FAILED** = `2`

Some error occurred during loading and it failed.

classref-enumeration-constant

`ThreadLoadStatus<enum_ResourceLoader_ThreadLoadStatus>`
**THREAD\_LOAD\_LOADED** = `3`

The resource was loaded successfully and can be accessed via
`load_threaded_get<class_ResourceLoader_method_load_threaded_get>`.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CacheMode**: `🔗<enum_ResourceLoader_CacheMode>`

classref-enumeration-constant

`CacheMode<enum_ResourceLoader_CacheMode>` **CACHE\_MODE\_IGNORE** = `0`

Neither the main resource (the one requested to be loaded) nor any of
its subresources are retrieved from cache nor stored into it.
Dependencies (external resources) are loaded with
`CACHE_MODE_REUSE<class_ResourceLoader_constant_CACHE_MODE_REUSE>`.

classref-enumeration-constant

`CacheMode<enum_ResourceLoader_CacheMode>` **CACHE\_MODE\_REUSE** = `1`

The main resource (the one requested to be loaded), its subresources,
and its dependencies (external resources) are retrieved from cache if
present, instead of loaded. Those not cached are loaded and then stored
into the cache. The same rules are propagated recursively down the tree
of dependencies (external resources).

classref-enumeration-constant

`CacheMode<enum_ResourceLoader_CacheMode>` **CACHE\_MODE\_REPLACE** =
`2`

Like `CACHE_MODE_REUSE<class_ResourceLoader_constant_CACHE_MODE_REUSE>`,
but the cache is checked for the main resource (the one requested to be
loaded) as well as for each of its subresources. Those already in the
cache, as long as the loaded and cached types match, have their data
refreshed from storage into the already existing instances. Otherwise,
they are recreated as completely new objects.

classref-enumeration-constant

`CacheMode<enum_ResourceLoader_CacheMode>` **CACHE\_MODE\_IGNORE\_DEEP**
= `3`

Like
`CACHE_MODE_IGNORE<class_ResourceLoader_constant_CACHE_MODE_IGNORE>`,
but propagated recursively down the tree of dependencies (external
resources).

classref-enumeration-constant

`CacheMode<enum_ResourceLoader_CacheMode>`
**CACHE\_MODE\_REPLACE\_DEEP** = `4`

Like
`CACHE_MODE_REPLACE<class_ResourceLoader_constant_CACHE_MODE_REPLACE>`,
but propagated recursively down the tree of dependencies (external
resources).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)`
**add\_resource\_format\_loader**(format\_loader:
`ResourceFormatLoader<class_ResourceFormatLoader>`, at\_front:
`bool<class_bool>` = false)
`🔗<class_ResourceLoader_method_add_resource_format_loader>`

Registers a new `ResourceFormatLoader<class_ResourceFormatLoader>`. The
ResourceLoader will use the ResourceFormatLoader as described in
`load<class_ResourceLoader_method_load>`.

This method is performed implicitly for ResourceFormatLoaders written in
GDScript (see `ResourceFormatLoader<class_ResourceFormatLoader>` for
more information).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **exists**(path: `String<class_String>`, type\_hint:
`String<class_String>` = "") `🔗<class_ResourceLoader_method_exists>`

Returns whether a recognized resource exists for the given `path`.

An optional `type_hint` can be used to further specify the
`Resource<class_Resource>` type that should be handled by the
`ResourceFormatLoader<class_ResourceFormatLoader>`. Anything that
inherits from `Resource<class_Resource>` can be used as a type hint, for
example `Image<class_Image>`.

\*\*Note:\*\* If you use
`Resource.take_over_path<class_Resource_method_take_over_path>`, this
method will return `true` for the taken path even if the resource wasn't
saved (i.e. exists only in resource cache).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Resource<class_Resource>` **get\_cached\_ref**(path:
`String<class_String>`) `🔗<class_ResourceLoader_method_get_cached_ref>`

Returns the cached resource reference for the given `path`.

\*\*Note:\*\* If the resource is not cached, the returned
`Resource<class_Resource>` will be invalid.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_dependencies**(path:
`String<class_String>`)
`🔗<class_ResourceLoader_method_get_dependencies>`

Returns the dependencies for the resource at the given `path`.

\*\*Note:\*\* The dependencies are returned with slices separated by
`::`. You can use `String.get_slice<class_String_method_get_slice>` to
get their components.

    for dep in ResourceLoader.get_dependencies(path):
        print(dep.get_slice("::", 0)) # Prints UID.
        print(dep.get_slice("::", 2)) # Prints path.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_recognized\_extensions\_for\_type**(type: `String<class_String>`)
`🔗<class_ResourceLoader_method_get_recognized_extensions_for_type>`

Returns the list of recognized extensions for a resource type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_resource\_uid**(path: `String<class_String>`)
`🔗<class_ResourceLoader_method_get_resource_uid>`

Returns the ID associated with a given resource path, or `-1` when no
such ID exists.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_cached**(path: `String<class_String>`)
`🔗<class_ResourceLoader_method_has_cached>`

Returns whether a cached resource is available for the given `path`.

Once a resource has been loaded by the engine, it is cached in memory
for faster access, and future calls to the
`load<class_ResourceLoader_method_load>` method will use the cached
version. The cached resource can be overridden by using
`Resource.take_over_path<class_Resource_method_take_over_path>` on a new
resource for that same path.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Resource<class_Resource>` **load**(path: `String<class_String>`,
type\_hint: `String<class_String>` = "", cache\_mode:
`CacheMode<enum_ResourceLoader_CacheMode>` = 1)
`🔗<class_ResourceLoader_method_load>`

Loads a resource at the given `path`, caching the result for further
access.

The registered `ResourceFormatLoader<class_ResourceFormatLoader>`s are
queried sequentially to find the first one which can handle the file's
extension, and then attempt loading. If loading fails, the remaining
ResourceFormatLoaders are also attempted.

An optional `type_hint` can be used to further specify the
`Resource<class_Resource>` type that should be handled by the
`ResourceFormatLoader<class_ResourceFormatLoader>`. Anything that
inherits from `Resource<class_Resource>` can be used as a type hint, for
example `Image<class_Image>`.

The `cache_mode` property defines whether and how the cache should be
used or updated when loading the resource. See
`CacheMode<enum_ResourceLoader_CacheMode>` for details.

Returns an empty resource if no
`ResourceFormatLoader<class_ResourceFormatLoader>` could handle the
file, and prints an error if no file is found at the specified path.

GDScript has a simplified `@GDScript.load<class_@GDScript_method_load>`
built-in method which can be used in most situations, leaving the use of
**ResourceLoader** for more advanced scenarios.

\*\*Note:\*\* If
`ProjectSettings.editor/export/convert_text_resources_to_binary<class_ProjectSettings_property_editor/export/convert_text_resources_to_binary>`
is `true`, `@GDScript.load<class_@GDScript_method_load>` will not be
able to read converted files in an exported project. If you rely on
run-time loading of files present within the PCK, set
`ProjectSettings.editor/export/convert_text_resources_to_binary<class_ProjectSettings_property_editor/export/convert_text_resources_to_binary>`
to `false`.

\*\*Note:\*\* Relative paths will be prefixed with `"res://"` before
loading, to avoid unexpected results make sure your paths are absolute.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Resource<class_Resource>` **load\_threaded\_get**(path:
`String<class_String>`)
`🔗<class_ResourceLoader_method_load_threaded_get>`

Returns the resource loaded by
`load_threaded_request<class_ResourceLoader_method_load_threaded_request>`.

If this is called before the loading thread is done (i.e.
`load_threaded_get_status<class_ResourceLoader_method_load_threaded_get_status>`
is not
`THREAD_LOAD_LOADED<class_ResourceLoader_constant_THREAD_LOAD_LOADED>`),
the calling thread will be blocked until the resource has finished
loading. However, it's recommended to use
`load_threaded_get_status<class_ResourceLoader_method_load_threaded_get_status>`
to known when the load has actually completed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`ThreadLoadStatus<enum_ResourceLoader_ThreadLoadStatus>`
**load\_threaded\_get\_status**(path: `String<class_String>`, progress:
`Array<class_Array>` = \[\])
`🔗<class_ResourceLoader_method_load_threaded_get_status>`

Returns the status of a threaded loading operation started with
`load_threaded_request<class_ResourceLoader_method_load_threaded_request>`
for the resource at `path`. See
`ThreadLoadStatus<enum_ResourceLoader_ThreadLoadStatus>` for possible
return values.

An array variable can optionally be passed via `progress`, and will
return a one-element array containing the percentage of completion of
the threaded loading.

\*\*Note:\*\* The recommended way of using this method is to call it
during different frames (e.g., in
`Node._process<class_Node_private_method__process>`, instead of a loop).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **load\_threaded\_request**(path:
`String<class_String>`, type\_hint: `String<class_String>` = "",
use\_sub\_threads: `bool<class_bool>` = false, cache\_mode:
`CacheMode<enum_ResourceLoader_CacheMode>` = 1)
`🔗<class_ResourceLoader_method_load_threaded_request>`

Loads the resource using threads. If `use_sub_threads` is `true`,
multiple threads will be used to load the resource, which makes loading
faster, but may affect the main thread (and thus cause game slowdowns).

The `cache_mode` property defines whether and how the cache should be
used or updated when loading the resource. See
`CacheMode<enum_ResourceLoader_CacheMode>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_resource\_format\_loader**(format\_loader:
`ResourceFormatLoader<class_ResourceFormatLoader>`)
`🔗<class_ResourceLoader_method_remove_resource_format_loader>`

Unregisters the given
`ResourceFormatLoader<class_ResourceFormatLoader>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_abort\_on\_missing\_resources**(abort:
`bool<class_bool>`)
`🔗<class_ResourceLoader_method_set_abort_on_missing_resources>`

Changes the behavior on missing sub-resources. The default behavior is
to abort loading.
