github\_url  
hide

# ResourceFormatLoader

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Loads a specific resource type from a file.

classref-introduction-group

## Description

Godot loads resources in the editor or in exported games using
ResourceFormatLoaders. They are queried automatically via the
`ResourceLoader<class_ResourceLoader>` singleton, or when a resource
with internal dependencies is loaded. Each file type may load as a
different resource type, so multiple ResourceFormatLoaders are
registered in the engine.

Extending this class allows you to define your own loader. Be sure to
respect the documented return types and values. You should give it a
global class name with `class_name` for it to be registered. Like
built-in ResourceFormatLoaders, it will be called automatically when
loading resources of its handled type(s). You may also implement a
`ResourceFormatSaver<class_ResourceFormatSaver>`.

\*\*Note:\*\* You can also extend
`EditorImportPlugin<class_EditorImportPlugin>` if the resource type you
need exists but Godot is unable to load its format. Choosing one way
over another depends on if the format is suitable or not for the final
exported game. For example, it's better to import `.png` textures as
`.ctex` (`CompressedTexture2D<class_CompressedTexture2D>`) first, so
they can be loaded with better efficiency on the graphics card.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **CacheMode**: `🔗<enum_ResourceFormatLoader_CacheMode>`

classref-enumeration-constant

`CacheMode<enum_ResourceFormatLoader_CacheMode>` **CACHE\_MODE\_IGNORE**
= `0`

Neither the main resource (the one requested to be loaded) nor any of
its subresources are retrieved from cache nor stored into it.
Dependencies (external resources) are loaded with
`CACHE_MODE_REUSE<class_ResourceFormatLoader_constant_CACHE_MODE_REUSE>`.

classref-enumeration-constant

`CacheMode<enum_ResourceFormatLoader_CacheMode>` **CACHE\_MODE\_REUSE**
= `1`

The main resource (the one requested to be loaded), its subresources,
and its dependencies (external resources) are retrieved from cache if
present, instead of loaded. Those not cached are loaded and then stored
into the cache. The same rules are propagated recursively down the tree
of dependencies (external resources).

classref-enumeration-constant

`CacheMode<enum_ResourceFormatLoader_CacheMode>`
**CACHE\_MODE\_REPLACE** = `2`

Like
`CACHE_MODE_REUSE<class_ResourceFormatLoader_constant_CACHE_MODE_REUSE>`,
but the cache is checked for the main resource (the one requested to be
loaded) as well as for each of its subresources. Those already in the
cache, as long as the loaded and cached types match, have their data
refreshed from storage into the already existing instances. Otherwise,
they are recreated as completely new objects.

classref-enumeration-constant

`CacheMode<enum_ResourceFormatLoader_CacheMode>`
**CACHE\_MODE\_IGNORE\_DEEP** = `3`

Like
`CACHE_MODE_IGNORE<class_ResourceFormatLoader_constant_CACHE_MODE_IGNORE>`,
but propagated recursively down the tree of dependencies (external
resources).

classref-enumeration-constant

`CacheMode<enum_ResourceFormatLoader_CacheMode>`
**CACHE\_MODE\_REPLACE\_DEEP** = `4`

Like
`CACHE_MODE_REPLACE<class_ResourceFormatLoader_constant_CACHE_MODE_REPLACE>`,
but propagated recursively down the tree of dependencies (external
resources).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **\_exists**(path: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceFormatLoader_private_method__exists>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_classes\_used**(path: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceFormatLoader_private_method__get_classes_used>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_dependencies**(path: `String<class_String>`, add\_types:
`bool<class_bool>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceFormatLoader_private_method__get_dependencies>`

If implemented, gets the dependencies of a given resource. If
`add_types` is `true`, paths should be appended `::TypeName`, where
`TypeName` is the class name of the dependency.

\*\*Note:\*\* Custom resource types defined by scripts aren't known by
the `ClassDB<class_ClassDB>`, so you might just return `"Resource"` for
them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_recognized\_extensions**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceFormatLoader_private_method__get_recognized_extensions>`

Gets the list of extensions for files this loader is able to read.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_resource\_script\_class**(path:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceFormatLoader_private_method__get_resource_script_class>`

Returns the script class name associated with the
`Resource<class_Resource>` under the given `path`. If the resource has
no script or the script isn't a named class, it should return `""`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_resource\_type**(path:
`String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceFormatLoader_private_method__get_resource_type>`

Gets the class name of the resource associated with the given path. If
the loader cannot handle it, it should return `""`.

\*\*Note:\*\* Custom resource types defined by scripts aren't known by
the `ClassDB<class_ClassDB>`, so you might just return `"Resource"` for
them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **\_get\_resource\_uid**(path: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceFormatLoader_private_method__get_resource_uid>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_handles\_type**(type:
`StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceFormatLoader_private_method__handles_type>`

Tells which resource class this loader can load.

\*\*Note:\*\* Custom resource types defined by scripts aren't known by
the `ClassDB<class_ClassDB>`, so you might just handle `"Resource"` for
them.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **\_load**(path: `String<class_String>`,
original\_path: `String<class_String>`, use\_sub\_threads:
`bool<class_bool>`, cache\_mode: `int<class_int>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceFormatLoader_private_method__load>`

Loads a resource when the engine finds this loader to be compatible. If
the loaded resource is the result of an import, `original_path` will
target the source file. Returns a `Resource<class_Resource>` object on
success, or an `Error<enum_@GlobalScope_Error>` constant in case of
failure.

The `cache_mode` property defines whether and how the cache should be
used or updated when loading the resource. See
`CacheMode<enum_ResourceFormatLoader_CacheMode>` for details.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **\_recognize\_path**(path: `String<class_String>`,
type: `StringName<class_StringName>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceFormatLoader_private_method__recognize_path>`

Tells whether or not this loader should load a resource from its
resource path for a given type.

If it is not implemented, the default behavior returns whether the
path's extension is within the ones provided by
`_get_recognized_extensions<class_ResourceFormatLoader_private_method__get_recognized_extensions>`,
and if the type is within the ones provided by
`_get_resource_type<class_ResourceFormatLoader_private_method__get_resource_type>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_rename\_dependencies**(path:
`String<class_String>`, renames: `Dictionary<class_Dictionary>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ResourceFormatLoader_private_method__rename_dependencies>`

If implemented, renames dependencies within the given resource and saves
it. `renames` is a dictionary `{ String => String }` mapping old
dependency paths to new paths.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success, or
an `Error<enum_@GlobalScope_Error>` constant in case of failure.
