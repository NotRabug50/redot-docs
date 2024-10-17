github\_url  
hide

# GLTFDocument

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `FBXDocument<class_FBXDocument>`

Class for importing and exporting glTF files in and out of Godot.

classref-introduction-group

## Description

GLTFDocument supports reading data from a glTF file, buffer, or Godot
scene. This data can then be written to the filesystem, buffer, or used
to create a Godot scene.

All of the data in a glTF scene is stored in the
`GLTFState<class_GLTFState>` class. GLTFDocument processes state
objects, but does not contain any scene data itself. GLTFDocument has
member variables to store export configuration settings such as the
image format, but is otherwise stateless. Multiple scenes can be
processed with the same settings using the same GLTFDocument object and
different `GLTFState<class_GLTFState>` objects.

GLTFDocument can be extended with arbitrary functionality by extending
the `GLTFDocumentExtension<class_GLTFDocumentExtension>` class and
registering it with GLTFDocument via
`register_gltf_document_extension<class_GLTFDocument_method_register_gltf_document_extension>`.
This allows for custom data to be imported and exported.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`
-   [glTF 'What the duck?'
    guide](https://www.khronos.org/files/gltf20-reference-guide.pdf)
-   [Khronos glTF specification](https://registry.khronos.org/glTF/)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **RootNodeMode**: `🔗<enum_GLTFDocument_RootNodeMode>`

classref-enumeration-constant

`RootNodeMode<enum_GLTFDocument_RootNodeMode>`
**ROOT\_NODE\_MODE\_SINGLE\_ROOT** = `0`

Treat the Godot scene's root node as the root node of the glTF file, and
mark it as the single root node via the `GODOT_single_root` glTF
extension. This will be parsed the same as
`ROOT_NODE_MODE_KEEP_ROOT<class_GLTFDocument_constant_ROOT_NODE_MODE_KEEP_ROOT>`
if the implementation does not support `GODOT_single_root`.

classref-enumeration-constant

`RootNodeMode<enum_GLTFDocument_RootNodeMode>`
**ROOT\_NODE\_MODE\_KEEP\_ROOT** = `1`

Treat the Godot scene's root node as the root node of the glTF file, but
do not mark it as anything special. An extra root node will be generated
when importing into Godot. This uses only vanilla glTF features. This is
equivalent to the behavior in Godot 4.1 and earlier.

classref-enumeration-constant

`RootNodeMode<enum_GLTFDocument_RootNodeMode>`
**ROOT\_NODE\_MODE\_MULTI\_ROOT** = `2`

Treat the Godot scene's root node as the name of the glTF scene, and add
all of its children as root nodes of the glTF file. This uses only
vanilla glTF features. This avoids an extra root node, but only the name
of the Godot scene's root node will be preserved, as it will not be
saved as a node.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **image\_format** = `"PNG"`
`🔗<class_GLTFDocument_property_image_format>`

classref-property-setget

-   `void (No return value.)` **set\_image\_format**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_image\_format**()

The user-friendly name of the export image format. This is used when
exporting the glTF file, including writing to a file and writing to a
byte array.

By default, Godot allows the following options: "None", "PNG", "JPEG",
"Lossless WebP", and "Lossy WebP". Support for more image formats can be
added in `GLTFDocumentExtension<class_GLTFDocumentExtension>` classes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **lossy\_quality** = `0.75`
`🔗<class_GLTFDocument_property_lossy_quality>`

classref-property-setget

-   `void (No return value.)` **set\_lossy\_quality**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_lossy\_quality**()

If `image_format<class_GLTFDocument_property_image_format>` is a lossy
image format, this determines the lossy quality of the image. On a range
of `0.0` to `1.0`, where `0.0` is the lowest quality and `1.0` is the
highest quality. A lossy quality of `1.0` is not the same as lossless.

classref-item-separator

------------------------------------------------------------------------

classref-property

`RootNodeMode<enum_GLTFDocument_RootNodeMode>` **root\_node\_mode** =
`0` `🔗<class_GLTFDocument_property_root_node_mode>`

classref-property-setget

-   `void (No return value.)` **set\_root\_node\_mode**(value:
    `RootNodeMode<enum_GLTFDocument_RootNodeMode>`)
-   `RootNodeMode<enum_GLTFDocument_RootNodeMode>`
    **get\_root\_node\_mode**()

How to process the root node during export. See
`RootNodeMode<enum_GLTFDocument_RootNodeMode>` for details. The default
and recommended value is
`ROOT_NODE_MODE_SINGLE_ROOT<class_GLTFDocument_constant_ROOT_NODE_MODE_SINGLE_ROOT>`.

\*\*Note:\*\* Regardless of how the glTF file is exported, when
importing, the root node type and name can be overridden in the scene
import settings tab.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Error<enum_@GlobalScope_Error>` **append\_from\_buffer**(bytes:
`PackedByteArray<class_PackedByteArray>`, base\_path:
`String<class_String>`, state: `GLTFState<class_GLTFState>`, flags:
`int<class_int>` = 0) `🔗<class_GLTFDocument_method_append_from_buffer>`

Takes a `PackedByteArray<class_PackedByteArray>` defining a glTF and
imports the data to the given `GLTFState<class_GLTFState>` object
through the `state` parameter.

\*\*Note:\*\* The `base_path` tells
`append_from_buffer<class_GLTFDocument_method_append_from_buffer>` where
to find dependencies and can be empty.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **append\_from\_file**(path:
`String<class_String>`, state: `GLTFState<class_GLTFState>`, flags:
`int<class_int>` = 0, base\_path: `String<class_String>` = "")
`🔗<class_GLTFDocument_method_append_from_file>`

Takes a path to a glTF file and imports the data at that file path to
the given `GLTFState<class_GLTFState>` object through the `state`
parameter.

\*\*Note:\*\* The `base_path` tells
`append_from_file<class_GLTFDocument_method_append_from_file>` where to
find dependencies and can be empty.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **append\_from\_scene**(node:
`Node<class_Node>`, state: `GLTFState<class_GLTFState>`, flags:
`int<class_int>` = 0) `🔗<class_GLTFDocument_method_append_from_scene>`

Takes a Godot Engine scene node and exports it and its descendants to
the given `GLTFState<class_GLTFState>` object through the `state`
parameter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **generate\_buffer**(state:
`GLTFState<class_GLTFState>`)
`🔗<class_GLTFDocument_method_generate_buffer>`

Takes a `GLTFState<class_GLTFState>` object through the `state`
parameter and returns a glTF `PackedByteArray<class_PackedByteArray>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **generate\_scene**(state:
`GLTFState<class_GLTFState>`, bake\_fps: `float<class_float>` = 30,
trimming: `bool<class_bool>` = false, remove\_immutable\_tracks:
`bool<class_bool>` = true)
`🔗<class_GLTFDocument_method_generate_scene>`

Takes a `GLTFState<class_GLTFState>` object through the `state`
parameter and returns a Godot Engine scene node.

The `bake_fps` parameter overrides the bake\_fps in `state`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**get\_supported\_gltf\_extensions**()
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFDocument_method_get_supported_gltf_extensions>`

Returns a list of all support glTF extensions, including extensions
supported directly by the engine, and extensions supported by user
plugins registering `GLTFDocumentExtension<class_GLTFDocumentExtension>`
classes.

\*\*Note:\*\* If this method is run before a GLTFDocumentExtension is
registered, its extensions won't be included in the list. Be sure to
only run this method after all extensions are registered. If you run
this when the engine starts, consider waiting a frame before calling
this method to ensure all extensions are registered.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**register\_gltf\_document\_extension**(extension:
`GLTFDocumentExtension<class_GLTFDocumentExtension>`, first\_priority:
`bool<class_bool>` = false)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFDocument_method_register_gltf_document_extension>`

Registers the given `GLTFDocumentExtension<class_GLTFDocumentExtension>`
instance with GLTFDocument. If `first_priority` is true, this extension
will be run first. Otherwise, it will be run last.

\*\*Note:\*\* Like GLTFDocument itself, all GLTFDocumentExtension
classes must be stateless in order to function properly. If you need to
store data, use the `set_additional_data` and `get_additional_data`
methods in `GLTFState<class_GLTFState>` or `GLTFNode<class_GLTFNode>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**unregister\_gltf\_document\_extension**(extension:
`GLTFDocumentExtension<class_GLTFDocumentExtension>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_GLTFDocument_method_unregister_gltf_document_extension>`

Unregisters the given
`GLTFDocumentExtension<class_GLTFDocumentExtension>` instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **write\_to\_filesystem**(state:
`GLTFState<class_GLTFState>`, path: `String<class_String>`)
`🔗<class_GLTFDocument_method_write_to_filesystem>`

Takes a `GLTFState<class_GLTFState>` object through the `state`
parameter and writes a glTF file to the filesystem.

\*\*Note:\*\* The extension of the glTF file determines if it is a .glb
binary file or a .gltf text file.
