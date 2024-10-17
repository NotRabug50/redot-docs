github\_url  
hide

# GLTFDocumentExtension

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:**
`GLTFDocumentExtensionConvertImporterMesh<class_GLTFDocumentExtensionConvertImporterMesh>`

`GLTFDocument<class_GLTFDocument>` extension class.

classref-introduction-group

## Description

Extends the functionality of the `GLTFDocument<class_GLTFDocument>`
class by allowing you to run arbitrary code at various stages of glTF
import or export.

To use, make a new class extending GLTFDocumentExtension, override any
methods you need, make an instance of your class, and register it using
`GLTFDocument.register_gltf_document_extension<class_GLTFDocument_method_register_gltf_document_extension>`.

\*\*Note:\*\* Like GLTFDocument itself, all GLTFDocumentExtension
classes must be stateless in order to function properly. If you need to
store data, use the `set_additional_data` and `get_additional_data`
methods in `GLTFState<class_GLTFState>` or `GLTFNode<class_GLTFNode>`.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **\_convert\_scene\_node**(state:
`GLTFState<class_GLTFState>`, gltf\_node: `GLTFNode<class_GLTFNode>`,
scene\_node: `Node<class_Node>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__convert_scene_node>`

Part of the export process. This method is run after
`_export_preflight<class_GLTFDocumentExtension_private_method__export_preflight>`
and before
`_export_post_convert<class_GLTFDocumentExtension_private_method__export_post_convert>`.

Runs when converting the data from a Godot scene node. This method can
be used to process the Godot scene node data into a format that can be
used by
`_export_node<class_GLTFDocumentExtension_private_method__export_node>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_export\_node**(state:
`GLTFState<class_GLTFState>`, gltf\_node: `GLTFNode<class_GLTFNode>`,
json: `Dictionary<class_Dictionary>`, node: `Node<class_Node>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__export_node>`

Part of the export process. This method is run after
`_get_saveable_image_formats<class_GLTFDocumentExtension_private_method__get_saveable_image_formats>`
and before
`_export_post<class_GLTFDocumentExtension_private_method__export_post>`.
If this **GLTFDocumentExtension** is used for exporting images, this
runs after
`_serialize_texture_json<class_GLTFDocumentExtension_private_method__serialize_texture_json>`.

This method can be used to modify the final JSON of each node. Data
should be primarily stored in `gltf_node` prior to serializing the JSON,
but the original Godot `node` is also provided if available. The node
may be null if not available, such as when exporting glTF data not
generated from a Godot scene.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_export\_post**(state:
`GLTFState<class_GLTFState>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__export_post>`

Part of the export process. This method is run last, after all other
parts of the export process.

This method can be used to modify the final JSON of the generated glTF
file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_export\_post\_convert**(state:
`GLTFState<class_GLTFState>`, root: `Node<class_Node>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__export_post_convert>`

Part of the export process. This method is run after
`_convert_scene_node<class_GLTFDocumentExtension_private_method__convert_scene_node>`
and before
`_export_preserialize<class_GLTFDocumentExtension_private_method__export_preserialize>`.

This method can be used to modify the converted node data structures
before serialization with any additional data from the scene tree.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_export\_preflight**(state:
`GLTFState<class_GLTFState>`, root: `Node<class_Node>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__export_preflight>`

Part of the export process. This method is run first, before all other
parts of the export process.

The return value is used to determine if this **GLTFDocumentExtension**
instance should be used for exporting a given glTF file. If
`@GlobalScope.OK<class_@GlobalScope_constant_OK>`, the export will use
this **GLTFDocumentExtension** instance. If not overridden,
`@GlobalScope.OK<class_@GlobalScope_constant_OK>` is returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_export\_preserialize**(state:
`GLTFState<class_GLTFState>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__export_preserialize>`

Part of the export process. This method is run after
`_export_post_convert<class_GLTFDocumentExtension_private_method__export_post_convert>`
and before
`_get_saveable_image_formats<class_GLTFDocumentExtension_private_method__get_saveable_image_formats>`.

This method can be used to alter the state before performing
serialization. It runs every time when generating a buffer with
`GLTFDocument.generate_buffer<class_GLTFDocument_method_generate_buffer>`
or writing to the file system with
`GLTFDocument.write_to_filesystem<class_GLTFDocument_method_write_to_filesystem>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node3D<class_Node3D>` **\_generate\_scene\_node**(state:
`GLTFState<class_GLTFState>`, gltf\_node: `GLTFNode<class_GLTFNode>`,
scene\_parent: `Node<class_Node>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__generate_scene_node>`

Part of the import process. This method is run after
`_import_pre_generate<class_GLTFDocumentExtension_private_method__import_pre_generate>`
and before
`_import_node<class_GLTFDocumentExtension_private_method__import_node>`.

Runs when generating a Godot scene node from a GLTFNode. The returned
node will be added to the scene tree. Multiple nodes can be generated in
this step if they are added as a child of the returned node.

\*\*Note:\*\* The `scene_parent` parameter may be null if this is the
single root node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **\_get\_image\_file\_extension**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__get_image_file_extension>`

Returns the file extension to use for saving image data into, for
example, `".png"`. If defined, when this extension is used to handle
images, and the images are saved to a separate file, the image bytes
will be copied to a file with this extension. If this is set, there
should be a `ResourceImporter<class_ResourceImporter>` class able to
import the file. If not defined or empty, Godot will save the image into
a PNG file.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_saveable\_image\_formats**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__get_saveable_image_formats>`

Part of the export process. This method is run after
`_convert_scene_node<class_GLTFDocumentExtension_private_method__convert_scene_node>`
and before
`_export_node<class_GLTFDocumentExtension_private_method__export_node>`.

Returns an array of the image formats that can be saved/exported by this
extension. This extension will only be selected as the image exporter if
the `GLTFDocument<class_GLTFDocument>`'s
`GLTFDocument.image_format<class_GLTFDocument_property_image_format>` is
in this array. If this **GLTFDocumentExtension** is selected as the
image exporter, one of the
`_save_image_at_path<class_GLTFDocumentExtension_private_method__save_image_at_path>`
or
`_serialize_image_to_bytes<class_GLTFDocumentExtension_private_method__serialize_image_to_bytes>`
methods will run next, otherwise
`_export_node<class_GLTFDocumentExtension_private_method__export_node>`
will run next. If the format name contains `"Lossy"`, the lossy quality
slider will be displayed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**\_get\_supported\_extensions**()
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__get_supported_extensions>`

Part of the import process. This method is run after
`_import_preflight<class_GLTFDocumentExtension_private_method__import_preflight>`
and before
`_parse_node_extensions<class_GLTFDocumentExtension_private_method__parse_node_extensions>`.

Returns an array of the glTF extensions supported by this
GLTFDocumentExtension class. This is used to validate if a glTF file
with required extensions can be loaded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_import\_node**(state:
`GLTFState<class_GLTFState>`, gltf\_node: `GLTFNode<class_GLTFNode>`,
json: `Dictionary<class_Dictionary>`, node: `Node<class_Node>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__import_node>`

Part of the import process. This method is run after
`_generate_scene_node<class_GLTFDocumentExtension_private_method__generate_scene_node>`
and before
`_import_post<class_GLTFDocumentExtension_private_method__import_post>`.

This method can be used to make modifications to each of the generated
Godot scene nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_import\_post**(state:
`GLTFState<class_GLTFState>`, root: `Node<class_Node>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__import_post>`

Part of the import process. This method is run last, after all other
parts of the import process.

This method can be used to modify the final Godot scene generated by the
import process.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_import\_post\_parse**(state:
`GLTFState<class_GLTFState>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__import_post_parse>`

Part of the import process. This method is run after
`_parse_node_extensions<class_GLTFDocumentExtension_private_method__parse_node_extensions>`
and before
`_import_pre_generate<class_GLTFDocumentExtension_private_method__import_pre_generate>`.

This method can be used to modify any of the data imported so far after
parsing each node, but before generating the scene or any of its nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_import\_pre\_generate**(state:
`GLTFState<class_GLTFState>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__import_pre_generate>`

Part of the import process. This method is run after
`_import_post_parse<class_GLTFDocumentExtension_private_method__import_post_parse>`
and before
`_generate_scene_node<class_GLTFDocumentExtension_private_method__generate_scene_node>`.

This method can be used to modify or read from any of the processed data
structures, before generating the nodes and then running the final
per-node import step.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_import\_preflight**(state:
`GLTFState<class_GLTFState>`, extensions:
`PackedStringArray<class_PackedStringArray>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__import_preflight>`

Part of the import process. This method is run first, before all other
parts of the import process.

The return value is used to determine if this **GLTFDocumentExtension**
instance should be used for importing a given glTF file. If
`@GlobalScope.OK<class_@GlobalScope_constant_OK>`, the import will use
this **GLTFDocumentExtension** instance. If not overridden,
`@GlobalScope.OK<class_@GlobalScope_constant_OK>` is returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_parse\_image\_data**(state:
`GLTFState<class_GLTFState>`, image\_data:
`PackedByteArray<class_PackedByteArray>`, mime\_type:
`String<class_String>`, ret\_image: `Image<class_Image>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__parse_image_data>`

Part of the import process. This method is run after
`_parse_node_extensions<class_GLTFDocumentExtension_private_method__parse_node_extensions>`
and before
`_parse_texture_json<class_GLTFDocumentExtension_private_method__parse_texture_json>`.

Runs when parsing image data from a glTF file. The data could be sourced
from a separate file, a URI, or a buffer, and then is passed as a byte
array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_parse\_node\_extensions**(state:
`GLTFState<class_GLTFState>`, gltf\_node: `GLTFNode<class_GLTFNode>`,
extensions: `Dictionary<class_Dictionary>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__parse_node_extensions>`

Part of the import process. This method is run after
`_get_supported_extensions<class_GLTFDocumentExtension_private_method__get_supported_extensions>`
and before
`_import_post_parse<class_GLTFDocumentExtension_private_method__import_post_parse>`.

Runs when parsing the node extensions of a GLTFNode. This method can be
used to process the extension JSON data into a format that can be used
by
`_generate_scene_node<class_GLTFDocumentExtension_private_method__generate_scene_node>`.
The return value should be a member of the
`Error<enum_@GlobalScope_Error>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_parse\_texture\_json**(state:
`GLTFState<class_GLTFState>`, texture\_json:
`Dictionary<class_Dictionary>`, ret\_gltf\_texture:
`GLTFTexture<class_GLTFTexture>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__parse_texture_json>`

Part of the import process. This method is run after
`_parse_image_data<class_GLTFDocumentExtension_private_method__parse_image_data>`
and before
`_generate_scene_node<class_GLTFDocumentExtension_private_method__generate_scene_node>`.

Runs when parsing the texture JSON from the glTF textures array. This
can be used to set the source image index to use as the texture.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_save\_image\_at\_path**(state:
`GLTFState<class_GLTFState>`, image: `Image<class_Image>`, file\_path:
`String<class_String>`, image\_format: `String<class_String>`,
lossy\_quality: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__save_image_at_path>`

Part of the export process. This method is run after
`_get_saveable_image_formats<class_GLTFDocumentExtension_private_method__get_saveable_image_formats>`
and before
`_serialize_texture_json<class_GLTFDocumentExtension_private_method__serialize_texture_json>`.

This method is run when saving images separately from the glTF file.
When images are embedded,
`_serialize_image_to_bytes<class_GLTFDocumentExtension_private_method__serialize_image_to_bytes>`
runs instead. Note that these methods only run when this
**GLTFDocumentExtension** is selected as the image exporter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>`
**\_serialize\_image\_to\_bytes**(state: `GLTFState<class_GLTFState>`,
image: `Image<class_Image>`, image\_dict:
`Dictionary<class_Dictionary>`, image\_format: `String<class_String>`,
lossy\_quality: `float<class_float>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__serialize_image_to_bytes>`

Part of the export process. This method is run after
`_get_saveable_image_formats<class_GLTFDocumentExtension_private_method__get_saveable_image_formats>`
and before
`_serialize_texture_json<class_GLTFDocumentExtension_private_method__serialize_texture_json>`.

This method is run when embedding images in the glTF file. When images
are saved separately,
`_save_image_at_path<class_GLTFDocumentExtension_private_method__save_image_at_path>`
runs instead. Note that these methods only run when this
**GLTFDocumentExtension** is selected as the image exporter.

This method must set the image MIME type in the `image_dict` with the
`"mimeType"` key. For example, for a PNG image, it would be set to
`"image/png"`. The return value must be a
`PackedByteArray<class_PackedByteArray>` containing the image data.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **\_serialize\_texture\_json**(state:
`GLTFState<class_GLTFState>`, texture\_json:
`Dictionary<class_Dictionary>`, gltf\_texture:
`GLTFTexture<class_GLTFTexture>`, image\_format: `String<class_String>`)
`virtual (This method should typically be overridden by the user to have any effect.)`
`🔗<class_GLTFDocumentExtension_private_method__serialize_texture_json>`

Part of the export process. This method is run after
`_save_image_at_path<class_GLTFDocumentExtension_private_method__save_image_at_path>`
or
`_serialize_image_to_bytes<class_GLTFDocumentExtension_private_method__serialize_image_to_bytes>`,
and before
`_export_node<class_GLTFDocumentExtension_private_method__export_node>`.
Note that this method only runs when this **GLTFDocumentExtension** is
selected as the image exporter.

This method can be used to set up the extensions for the texture JSON by
editing `texture_json`. The extension must also be added as used
extension with
`GLTFState.add_used_extension<class_GLTFState_method_add_used_extension>`,
be sure to set `required` to `true` if you are not providing a fallback.
