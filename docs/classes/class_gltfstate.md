github\_url  
hide

# GLTFState

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `FBXState<class_FBXState>`

Represents all data of a glTF file.

classref-introduction-group

## Description

Contains all nodes and resources of a glTF file. This is used by
`GLTFDocument<class_GLTFDocument>` as data storage, which allows
`GLTFDocument<class_GLTFDocument>` and all
`GLTFDocumentExtension<class_GLTFDocumentExtension>` classes to remain
stateless.

GLTFState can be populated by `GLTFDocument<class_GLTFDocument>` reading
a file or by converting a Godot scene. Then the data can either be used
to create a Godot scene or save to a glTF file. The code that converts
to/from a Godot scene can be intercepted at arbitrary points by
`GLTFDocumentExtension<class_GLTFDocumentExtension>` classes. This
allows for custom data to be stored in the glTF file or for custom data
to be converted to/from Godot nodes.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`
-   [glTF asset header
    schema](https://github.com/KhronosGroup/glTF/blob/main/specification/2.0/schema/asset.schema.json%22)

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

## Constants

classref-constant

**HANDLE\_BINARY\_DISCARD\_TEXTURES** = `0`
`🔗<class_GLTFState_constant_HANDLE_BINARY_DISCARD_TEXTURES>`

Discards all embedded textures and uses untextured materials.

classref-constant

**HANDLE\_BINARY\_EXTRACT\_TEXTURES** = `1`
`🔗<class_GLTFState_constant_HANDLE_BINARY_EXTRACT_TEXTURES>`

Extracts embedded textures to be reimported and compressed. Editor only.
Acts as uncompressed at runtime.

classref-constant

**HANDLE\_BINARY\_EMBED\_AS\_BASISU** = `2`
`🔗<class_GLTFState_constant_HANDLE_BINARY_EMBED_AS_BASISU>`

Embeds textures VRAM compressed with Basis Universal into the generated
scene.

classref-constant

**HANDLE\_BINARY\_EMBED\_AS\_UNCOMPRESSED** = `3`
`🔗<class_GLTFState_constant_HANDLE_BINARY_EMBED_AS_UNCOMPRESSED>`

Embeds textures compressed losslessly into the generated scene, matching
old behavior.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **bake\_fps** = `30.0`
`🔗<class_GLTFState_property_bake_fps>`

classref-property-setget

-   `void (No return value.)` **set\_bake\_fps**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_bake\_fps**()

The baking fps of the animation for either import or export.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **base\_path** = `""`
`🔗<class_GLTFState_property_base_path>`

classref-property-setget

-   `void (No return value.)` **set\_base\_path**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_base\_path**()

The folder path associated with this glTF data. This is used to find
other files the glTF file references, like images or binary buffers.
This will be set during import when appending from a file, and will be
set during export when writing to a file.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`PackedByteArray<class_PackedByteArray>`\]
**buffers** = `[]` `🔗<class_GLTFState_property_buffers>`

classref-property-setget

-   `void (No return value.)` **set\_buffers**(value:
    `Array<class_Array>`\[`PackedByteArray<class_PackedByteArray>`\])
-   `Array<class_Array>`\[`PackedByteArray<class_PackedByteArray>`\]
    **get\_buffers**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **copyright** = `""`
`🔗<class_GLTFState_property_copyright>`

classref-property-setget

-   `void (No return value.)` **set\_copyright**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_copyright**()

The copyright string in the asset header of the glTF file. This is set
during import if present and export if non-empty. See the glTF asset
header documentation for more information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **create\_animations** = `true`
`🔗<class_GLTFState_property_create_animations>`

classref-property-setget

-   `void (No return value.)` **set\_create\_animations**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_create\_animations**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **filename** = `""`
`🔗<class_GLTFState_property_filename>`

classref-property-setget

-   `void (No return value.)` **set\_filename**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_filename**()

The file name associated with this glTF data. If it ends with `.gltf`,
this is text-based glTF, otherwise this is binary GLB. This will be set
during import when appending from a file, and will be set during export
when writing to a file. If writing to a buffer, this will be an empty
string.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedByteArray<class_PackedByteArray>` **glb\_data** =
`PackedByteArray()` `🔗<class_GLTFState_property_glb_data>`

classref-property-setget

-   `void (No return value.)` **set\_glb\_data**(value:
    `PackedByteArray<class_PackedByteArray>`)
-   `PackedByteArray<class_PackedByteArray>` **get\_glb\_data**()

The binary buffer attached to a .glb file.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedByteArray<class_PackedByteArray>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **import\_as\_skeleton\_bones** = `false`
`🔗<class_GLTFState_property_import_as_skeleton_bones>`

classref-property-setget

-   `void (No return value.)`
    **set\_import\_as\_skeleton\_bones**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_import\_as\_skeleton\_bones**()

True to force all GLTFNodes in the document to be bones of a single
Skeleton3D godot node.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Dictionary<class_Dictionary>` **json** = `{}`
`🔗<class_GLTFState_property_json>`

classref-property-setget

-   `void (No return value.)` **set\_json**(value:
    `Dictionary<class_Dictionary>`)
-   `Dictionary<class_Dictionary>` **get\_json**()

The original raw JSON document corresponding to this GLTFState.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **major\_version** = `0`
`🔗<class_GLTFState_property_major_version>`

classref-property-setget

-   `void (No return value.)` **set\_major\_version**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_major\_version**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **minor\_version** = `0`
`🔗<class_GLTFState_property_minor_version>`

classref-property-setget

-   `void (No return value.)` **set\_minor\_version**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_minor\_version**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedInt32Array<class_PackedInt32Array>` **root\_nodes** =
`PackedInt32Array()` `🔗<class_GLTFState_property_root_nodes>`

classref-property-setget

-   `void (No return value.)` **set\_root\_nodes**(value:
    `PackedInt32Array<class_PackedInt32Array>`)
-   `PackedInt32Array<class_PackedInt32Array>` **get\_root\_nodes**()

The root nodes of the glTF file. Typically, a glTF file will only have
one scene, and therefore one root node. However, a glTF file may have
multiple scenes and therefore multiple root nodes, which will be
generated as siblings of each other and as children of the root node of
the generated Godot scene.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedInt32Array<class_PackedInt32Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **scene\_name** = `""`
`🔗<class_GLTFState_property_scene_name>`

classref-property-setget

-   `void (No return value.)` **set\_scene\_name**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_scene\_name**()

The name of the scene. When importing, if not specified, this will be
the file name. When exporting, if specified, the scene name will be
saved to the glTF file.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_named\_skin\_binds** = `false`
`🔗<class_GLTFState_property_use_named_skin_binds>`

classref-property-setget

-   `void (No return value.)` **set\_use\_named\_skin\_binds**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_use\_named\_skin\_binds**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_used\_extension**(extension\_name:
`String<class_String>`, required: `bool<class_bool>`)
`🔗<class_GLTFState_method_add_used_extension>`

Appends an extension to the list of extensions used by this glTF file
during serialization. If `required` is true, the extension will also be
added to the list of required extensions. Do not run this in
`GLTFDocumentExtension._export_post<class_GLTFDocumentExtension_private_method__export_post>`,
as that stage is too late to add extensions. The final list is sorted
alphabetically.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **append\_data\_to\_buffers**(data:
`PackedByteArray<class_PackedByteArray>`, deduplication:
`bool<class_bool>`) `🔗<class_GLTFState_method_append_data_to_buffers>`

Appends the given byte array data to the buffers and creates a
`GLTFBufferView<class_GLTFBufferView>` for it. The index of the
destination `GLTFBufferView<class_GLTFBufferView>` is returned. If
`deduplication` is true, the buffers will first be searched for
duplicate data, otherwise new bytes will always be appended.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **append\_gltf\_node**(gltf\_node:
`GLTFNode<class_GLTFNode>`, godot\_scene\_node: `Node<class_Node>`,
parent\_node\_index: `int<class_int>`)
`🔗<class_GLTFState_method_append_gltf_node>`

Append the given `GLTFNode<class_GLTFNode>` to the state, and return its
new index. This can be used to export one Godot node as multiple glTF
nodes, or inject new glTF nodes at import time. On import, this must be
called before
`GLTFDocumentExtension._generate_scene_node<class_GLTFDocumentExtension_private_method__generate_scene_node>`
finishes for the parent node. On export, this must be called before
`GLTFDocumentExtension._export_node<class_GLTFDocumentExtension_private_method__export_node>`
runs for the parent node.

The `godot_scene_node` parameter is the Godot scene node that
corresponds to this glTF node. This is highly recommended to be set to a
valid node, but may be null if there is no corresponding Godot scene
node. One Godot scene node may be used for multiple glTF nodes, so if
exporting multiple glTF nodes for one Godot scene node, use the same
Godot scene node for each.

The `parent_node_index` parameter is the index of the parent
`GLTFNode<class_GLTFNode>` in the state. If `-1`, the node will be a
root node, otherwise the new node will be added to the parent's list of
children. The index will also be written to the
`GLTFNode.parent<class_GLTFNode_property_parent>` property of the new
node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`GLTFAccessor<class_GLTFAccessor>`\]
**get\_accessors**() `🔗<class_GLTFState_method_get_accessors>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_additional\_data**(extension\_name:
`StringName<class_StringName>`)
`🔗<class_GLTFState_method_get_additional_data>`

Gets additional arbitrary data in this **GLTFState** instance. This can
be used to keep per-file state data in
`GLTFDocumentExtension<class_GLTFDocumentExtension>` classes, which is
important because they are stateless.

The argument should be the
`GLTFDocumentExtension<class_GLTFDocumentExtension>` name (does not have
to match the extension name in the glTF file), and the return value can
be anything you set. If nothing was set, the return value is null.

classref-item-separator

------------------------------------------------------------------------

classref-method

`AnimationPlayer<class_AnimationPlayer>` **get\_animation\_player**(idx:
`int<class_int>`) `🔗<class_GLTFState_method_get_animation_player>`

Returns the `AnimationPlayer<class_AnimationPlayer>` node with the given
index. These nodes are only used during the export process when
converting Godot `AnimationPlayer<class_AnimationPlayer>` nodes to glTF
animations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_animation\_players\_count**(idx:
`int<class_int>`)
`🔗<class_GLTFState_method_get_animation_players_count>`

Returns the number of `AnimationPlayer<class_AnimationPlayer>` nodes in
this **GLTFState**. These nodes are only used during the export process
when converting Godot `AnimationPlayer<class_AnimationPlayer>` nodes to
glTF animations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`GLTFAnimation<class_GLTFAnimation>`\]
**get\_animations**() `🔗<class_GLTFState_method_get_animations>`

Returns an array of all `GLTFAnimation<class_GLTFAnimation>`s in the
glTF file. When importing, these will be generated as animations in an
`AnimationPlayer<class_AnimationPlayer>` node. When exporting, these
will be generated from Godot `AnimationPlayer<class_AnimationPlayer>`
nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`GLTFBufferView<class_GLTFBufferView>`\]
**get\_buffer\_views**() `🔗<class_GLTFState_method_get_buffer_views>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`GLTFCamera<class_GLTFCamera>`\]
**get\_cameras**() `🔗<class_GLTFState_method_get_cameras>`

Returns an array of all `GLTFCamera<class_GLTFCamera>`s in the glTF
file. These are the cameras that the
`GLTFNode.camera<class_GLTFNode_property_camera>` index refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_handle\_binary\_image**()
`🔗<class_GLTFState_method_get_handle_binary_image>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Texture2D<class_Texture2D>`\] **get\_images**()
`🔗<class_GLTFState_method_get_images>`

Gets the images of the glTF file as an array of
`Texture2D<class_Texture2D>`s. These are the images that the
`GLTFTexture.src_image<class_GLTFTexture_property_src_image>` index
refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`GLTFLight<class_GLTFLight>`\] **get\_lights**()
`🔗<class_GLTFState_method_get_lights>`

Returns an array of all `GLTFLight<class_GLTFLight>`s in the glTF file.
These are the lights that the
`GLTFNode.light<class_GLTFNode_property_light>` index refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Material<class_Material>`\] **get\_materials**()
`🔗<class_GLTFState_method_get_materials>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`GLTFMesh<class_GLTFMesh>`\] **get\_meshes**()
`🔗<class_GLTFState_method_get_meshes>`

Returns an array of all `GLTFMesh<class_GLTFMesh>`es in the glTF file.
These are the meshes that the
`GLTFNode.mesh<class_GLTFNode_property_mesh>` index refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_node\_index**(scene\_node: `Node<class_Node>`)
`🔗<class_GLTFState_method_get_node_index>`

Returns the index of the `GLTFNode<class_GLTFNode>` corresponding to
this Godot scene node. This is the inverse of
`get_scene_node<class_GLTFState_method_get_scene_node>`. Useful during
the export process.

\*\*Note:\*\* Not every Godot scene node will have a corresponding
`GLTFNode<class_GLTFNode>`, and not every `GLTFNode<class_GLTFNode>`
will have a scene node generated. If there is no
`GLTFNode<class_GLTFNode>` index for this scene node, `-1` is returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`GLTFNode<class_GLTFNode>`\] **get\_nodes**()
`🔗<class_GLTFState_method_get_nodes>`

Returns an array of all `GLTFNode<class_GLTFNode>`s in the glTF file.
These are the nodes that
`GLTFNode.children<class_GLTFNode_property_children>` and
`root_nodes<class_GLTFState_property_root_nodes>` refer to. This
includes nodes that may not be generated in the Godot scene, or nodes
that may generate multiple Godot scene nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Node<class_Node>` **get\_scene\_node**(idx: `int<class_int>`)
`🔗<class_GLTFState_method_get_scene_node>`

Returns the Godot scene node that corresponds to the same index as the
`GLTFNode<class_GLTFNode>` it was generated from. This is the inverse of
`get_node_index<class_GLTFState_method_get_node_index>`. Useful during
the import process.

\*\*Note:\*\* Not every `GLTFNode<class_GLTFNode>` will have a scene
node generated, and not every generated scene node will have a
corresponding `GLTFNode<class_GLTFNode>`. If there is no scene node for
this `GLTFNode<class_GLTFNode>` index, `null` is returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`GLTFSkeleton<class_GLTFSkeleton>`\]
**get\_skeletons**() `🔗<class_GLTFState_method_get_skeletons>`

Returns an array of all `GLTFSkeleton<class_GLTFSkeleton>`s in the glTF
file. These are the skeletons that the
`GLTFNode.skeleton<class_GLTFNode_property_skeleton>` index refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`GLTFSkin<class_GLTFSkin>`\] **get\_skins**()
`🔗<class_GLTFState_method_get_skins>`

Returns an array of all `GLTFSkin<class_GLTFSkin>`s in the glTF file.
These are the skins that the
`GLTFNode.skin<class_GLTFNode_property_skin>` index refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`GLTFTextureSampler<class_GLTFTextureSampler>`\]
**get\_texture\_samplers**()
`🔗<class_GLTFState_method_get_texture_samplers>`

Retrieves the array of texture samplers that are used by the textures
contained in the glTF.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`GLTFTexture<class_GLTFTexture>`\]
**get\_textures**() `🔗<class_GLTFState_method_get_textures>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`String<class_String>`\]
**get\_unique\_animation\_names**()
`🔗<class_GLTFState_method_get_unique_animation_names>`

Returns an array of unique animation names. This is only used during the
import process.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`String<class_String>`\] **get\_unique\_names**()
`🔗<class_GLTFState_method_get_unique_names>`

Returns an array of unique node names. This is used in both the import
process and export process.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_accessors**(accessors:
`Array<class_Array>`\[`GLTFAccessor<class_GLTFAccessor>`\])
`🔗<class_GLTFState_method_set_accessors>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_additional\_data**(extension\_name:
`StringName<class_StringName>`, additional\_data:
`Variant<class_Variant>`)
`🔗<class_GLTFState_method_set_additional_data>`

Sets additional arbitrary data in this **GLTFState** instance. This can
be used to keep per-file state data in
`GLTFDocumentExtension<class_GLTFDocumentExtension>` classes, which is
important because they are stateless.

The first argument should be the
`GLTFDocumentExtension<class_GLTFDocumentExtension>` name (does not have
to match the extension name in the glTF file), and the second argument
can be anything you want.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_animations**(animations:
`Array<class_Array>`\[`GLTFAnimation<class_GLTFAnimation>`\])
`🔗<class_GLTFState_method_set_animations>`

Sets the `GLTFAnimation<class_GLTFAnimation>`s in the state. When
importing, these will be generated as animations in an
`AnimationPlayer<class_AnimationPlayer>` node. When exporting, these
will be generated from Godot `AnimationPlayer<class_AnimationPlayer>`
nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_buffer\_views**(buffer\_views:
`Array<class_Array>`\[`GLTFBufferView<class_GLTFBufferView>`\])
`🔗<class_GLTFState_method_set_buffer_views>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_cameras**(cameras:
`Array<class_Array>`\[`GLTFCamera<class_GLTFCamera>`\])
`🔗<class_GLTFState_method_set_cameras>`

Sets the `GLTFCamera<class_GLTFCamera>`s in the state. These are the
cameras that the `GLTFNode.camera<class_GLTFNode_property_camera>` index
refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_handle\_binary\_image**(method:
`int<class_int>`) `🔗<class_GLTFState_method_set_handle_binary_image>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_images**(images:
`Array<class_Array>`\[`Texture2D<class_Texture2D>`\])
`🔗<class_GLTFState_method_set_images>`

Sets the images in the state stored as an array of
`Texture2D<class_Texture2D>`s. This can be used during export. These are
the images that the
`GLTFTexture.src_image<class_GLTFTexture_property_src_image>` index
refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_lights**(lights:
`Array<class_Array>`\[`GLTFLight<class_GLTFLight>`\])
`🔗<class_GLTFState_method_set_lights>`

Sets the `GLTFLight<class_GLTFLight>`s in the state. These are the
lights that the `GLTFNode.light<class_GLTFNode_property_light>` index
refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_materials**(materials:
`Array<class_Array>`\[`Material<class_Material>`\])
`🔗<class_GLTFState_method_set_materials>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_meshes**(meshes:
`Array<class_Array>`\[`GLTFMesh<class_GLTFMesh>`\])
`🔗<class_GLTFState_method_set_meshes>`

Sets the `GLTFMesh<class_GLTFMesh>`es in the state. These are the meshes
that the `GLTFNode.mesh<class_GLTFNode_property_mesh>` index refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_nodes**(nodes:
`Array<class_Array>`\[`GLTFNode<class_GLTFNode>`\])
`🔗<class_GLTFState_method_set_nodes>`

Sets the `GLTFNode<class_GLTFNode>`s in the state. These are the nodes
that `GLTFNode.children<class_GLTFNode_property_children>` and
`root_nodes<class_GLTFState_property_root_nodes>` refer to. Some of the
nodes set here may not be generated in the Godot scene, or may generate
multiple Godot scene nodes.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_skeletons**(skeletons:
`Array<class_Array>`\[`GLTFSkeleton<class_GLTFSkeleton>`\])
`🔗<class_GLTFState_method_set_skeletons>`

Sets the `GLTFSkeleton<class_GLTFSkeleton>`s in the state. These are the
skeletons that the `GLTFNode.skeleton<class_GLTFNode_property_skeleton>`
index refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_skins**(skins:
`Array<class_Array>`\[`GLTFSkin<class_GLTFSkin>`\])
`🔗<class_GLTFState_method_set_skins>`

Sets the `GLTFSkin<class_GLTFSkin>`s in the state. These are the skins
that the `GLTFNode.skin<class_GLTFNode_property_skin>` index refers to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_texture\_samplers**(texture\_samplers:
`Array<class_Array>`\[`GLTFTextureSampler<class_GLTFTextureSampler>`\])
`🔗<class_GLTFState_method_set_texture_samplers>`

Sets the array of texture samplers that are used by the textures
contained in the glTF.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_textures**(textures:
`Array<class_Array>`\[`GLTFTexture<class_GLTFTexture>`\])
`🔗<class_GLTFState_method_set_textures>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**set\_unique\_animation\_names**(unique\_animation\_names:
`Array<class_Array>`\[`String<class_String>`\])
`🔗<class_GLTFState_method_set_unique_animation_names>`

Sets the unique animation names in the state. This is only used during
the import process.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_unique\_names**(unique\_names:
`Array<class_Array>`\[`String<class_String>`\])
`🔗<class_GLTFState_method_set_unique_names>`

Sets the unique node names in the state. This is used in both the import
process and export process.
