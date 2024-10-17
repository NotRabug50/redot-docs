github\_url  
hide

# ResourceSaver

**Inherits:** `Object<class_Object>`

A singleton for saving `Resource<class_Resource>`s to the filesystem.

classref-introduction-group

## Description

A singleton for saving resource types to the filesystem.

It uses the many `ResourceFormatSaver<class_ResourceFormatSaver>`
classes registered in the engine (either built-in or from a plugin) to
save resource data to text-based (e.g. `.tres` or `.tscn`) or binary
files (e.g. `.res` or `.scn`).

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

flags **SaverFlags**: `🔗<enum_ResourceSaver_SaverFlags>`

classref-enumeration-constant

`SaverFlags<enum_ResourceSaver_SaverFlags>` **FLAG\_NONE** = `0`

No resource saving option.

classref-enumeration-constant

`SaverFlags<enum_ResourceSaver_SaverFlags>` **FLAG\_RELATIVE\_PATHS** =
`1`

Save the resource with a path relative to the scene which uses it.

classref-enumeration-constant

`SaverFlags<enum_ResourceSaver_SaverFlags>` **FLAG\_BUNDLE\_RESOURCES**
= `2`

Bundles external resources.

classref-enumeration-constant

`SaverFlags<enum_ResourceSaver_SaverFlags>` **FLAG\_CHANGE\_PATH** = `4`

Changes the
`Resource.resource_path<class_Resource_property_resource_path>` of the
saved resource to match its new location.

classref-enumeration-constant

`SaverFlags<enum_ResourceSaver_SaverFlags>`
**FLAG\_OMIT\_EDITOR\_PROPERTIES** = `8`

Do not save editor-specific metadata (identified by their `__editor`
prefix).

classref-enumeration-constant

`SaverFlags<enum_ResourceSaver_SaverFlags>` **FLAG\_SAVE\_BIG\_ENDIAN**
= `16`

Save as big endian (see
`FileAccess.big_endian<class_FileAccess_property_big_endian>`).

classref-enumeration-constant

`SaverFlags<enum_ResourceSaver_SaverFlags>` **FLAG\_COMPRESS** = `32`

Compress the resource on save using
`FileAccess.COMPRESSION_ZSTD<class_FileAccess_constant_COMPRESSION_ZSTD>`.
Only available for binary resource types.

classref-enumeration-constant

`SaverFlags<enum_ResourceSaver_SaverFlags>`
**FLAG\_REPLACE\_SUBRESOURCE\_PATHS** = `64`

Take over the paths of the saved subresources (see
`Resource.take_over_path<class_Resource_method_take_over_path>`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)`
**add\_resource\_format\_saver**(format\_saver:
`ResourceFormatSaver<class_ResourceFormatSaver>`, at\_front:
`bool<class_bool>` = false)
`🔗<class_ResourceSaver_method_add_resource_format_saver>`

Registers a new `ResourceFormatSaver<class_ResourceFormatSaver>`. The
ResourceSaver will use the ResourceFormatSaver as described in
`save<class_ResourceSaver_method_save>`.

This method is performed implicitly for ResourceFormatSavers written in
GDScript (see `ResourceFormatSaver<class_ResourceFormatSaver>` for more
information).

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_recognized\_extensions**(type: `Resource<class_Resource>`)
`🔗<class_ResourceSaver_method_get_recognized_extensions>`

Returns the list of extensions available for saving a resource of a
given type.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_resource\_id\_for\_path**(path:
`String<class_String>`, generate: `bool<class_bool>` = false)
`🔗<class_ResourceSaver_method_get_resource_id_for_path>`

Returns the resource ID for the given path. If `generate` is `true`, a
new resource ID will be generated if one for the path is not found. If
`generate` is `false` and the path is not found,
`ResourceUID.INVALID_ID<class_ResourceUID_constant_INVALID_ID>` is
returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_resource\_format\_saver**(format\_saver:
`ResourceFormatSaver<class_ResourceFormatSaver>`)
`🔗<class_ResourceSaver_method_remove_resource_format_saver>`

Unregisters the given `ResourceFormatSaver<class_ResourceFormatSaver>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **save**(resource:
`Resource<class_Resource>`, path: `String<class_String>` = "", flags:
`BitField (This value is an integer composed as a bitmask of the following flags.)`\[`SaverFlags<enum_ResourceSaver_SaverFlags>`\]
= 0) `🔗<class_ResourceSaver_method_save>`

Saves a resource to disk to the given path, using a
`ResourceFormatSaver<class_ResourceFormatSaver>` that recognizes the
resource object. If `path` is empty, **ResourceSaver** will try to use
`Resource.resource_path<class_Resource_property_resource_path>`.

The `flags` bitmask can be specified to customize the save behavior
using `SaverFlags<enum_ResourceSaver_SaverFlags>` flags.

Returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>` on success.

\*\*Note:\*\* When the project is running, any generated UID associated
with the resource will not be saved as the required code is only
executed in editor mode.
