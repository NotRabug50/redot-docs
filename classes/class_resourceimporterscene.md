github\_url  
hide

# ResourceImporterScene

**Inherits:** `ResourceImporter<class_ResourceImporter>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Imports a glTF, FBX, Collada or Blender 3D scene.

classref-introduction-group

## Description

See also `ResourceImporterOBJ<class_ResourceImporterOBJ>`, which is used
for OBJ models that can be imported as an independent `Mesh<class_Mesh>`
or a scene.

Additional options (such as extracting individual meshes or materials to
files) are available in the **Advanced Import Settings** dialog. This
dialog can be accessed by double-clicking a 3D scene in the FileSystem
dock or by selecting a 3D scene in the FileSystem dock, going to the
Import dock and choosing **Advanced**.

\*\*Note:\*\* **ResourceImporterScene** is *not* used for
`PackedScene<class_PackedScene>`s, such as `.tscn` and `.scn` files.

classref-introduction-group

## Tutorials

-   `Importing 3D scenes <../tutorials/assets_pipeline/importing_3d_scenes/index>`

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

## Property Descriptions

classref-property

`Dictionary<class_Dictionary>` **\_subresources** = `{}`
`🔗<class_ResourceImporterScene_property__subresources>`

Contains properties for the scene's subresources. This is an internal
option which is not visible in the Import dock.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **animation/fps** = `30`
`🔗<class_ResourceImporterScene_property_animation/fps>`

The number of frames per second to use for baking animation curves to a
series of points with linear interpolation. It's recommended to
configure this value to match the value you're using as a baseline in
your 3D modeling software. Higher values result in more precise
animation with fast movement changes, at the cost of higher file sizes
and memory usage. Thanks to interpolation, there is usually not much
benefit in going above 30 FPS (as the animation will still appear smooth
at higher rendering framerates).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **animation/import** = `true`
`🔗<class_ResourceImporterScene_property_animation/import>`

If `true`, import animations from the 3D scene.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **animation/import\_rest\_as\_RESET** = `false`
`🔗<class_ResourceImporterScene_property_animation/import_rest_as_RESET>`

If `true`, adds an `Animation<class_Animation>` named `RESET`,
containing the
`Skeleton3D.get_bone_rest<class_Skeleton3D_method_get_bone_rest>` from
`Skeleton3D<class_Skeleton3D>` nodes. This can be useful to extract an
animation in the reference pose.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **animation/remove\_immutable\_tracks** = `true`
`🔗<class_ResourceImporterScene_property_animation/remove_immutable_tracks>`

If `true`, remove animation tracks that only contain default values.
This can reduce output file size and memory usage with certain 3D
scenes, depending on the contents of their animation tracks.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **animation/trimming** = `false`
`🔗<class_ResourceImporterScene_property_animation/trimming>`

If `true`, trim the beginning and end of animations if there are no
keyframe changes. This can reduce output file size and memory usage with
certain 3D scenes, depending on the contents of their animation tracks.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **import\_script/path** = `""`
`🔗<class_ResourceImporterScene_property_import_script/path>`

Path to an import script, which can run code after the import process
has completed for custom processing. See [Using import scripts for
automation](../tutorials/assets_pipeline/importing_3d_scenes/import_configuration.html#using-import-scripts-for-automation)
for more information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **meshes/create\_shadow\_meshes** = `true`
`🔗<class_ResourceImporterScene_property_meshes/create_shadow_meshes>`

If `true`, enables the generation of shadow meshes on import. This
optimizes shadow rendering without reducing quality by welding vertices
together when possible. This in turn reduces the memory bandwidth
required to render shadows. Shadow mesh generation currently doesn't
support using a lower detail level than the source mesh (but shadow
rendering will make use of LODs when relevant).

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **meshes/ensure\_tangents** = `true`
`🔗<class_ResourceImporterScene_property_meshes/ensure_tangents>`

If `true`, generate vertex tangents using
[Mikktspace](http://www.mikktspace.com/) if the input meshes don't have
tangent data. When possible, it's recommended to let the 3D modeling
software generate tangents on export instead on relying on this option.
Tangents are required for correct display of normal and height maps,
along with any material/shader features that require tangents.

If you don't need material features that require tangents, disabling
this can reduce output file size and speed up importing if the source 3D
file doesn't contain tangents.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **meshes/force\_disable\_compression** = `false`
`🔗<class_ResourceImporterScene_property_meshes/force_disable_compression>`

If `true`, mesh compression will not be used. Consider enabling if you
notice blocky artifacts in your mesh normals or UVs, or if you have
meshes that are larger than a few thousand meters in each direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **meshes/generate\_lods** = `true`
`🔗<class_ResourceImporterScene_property_meshes/generate_lods>`

If `true`, generates lower detail variants of the mesh which will be
displayed in the distance to improve rendering performance. Not all
meshes benefit from LOD, especially if they are never rendered from far
away. Disabling this can reduce output file size and speed up importing.
See [Mesh level of detail
(LOD)](../tutorials/3d/mesh_lod.html#doc-mesh-lod) for more information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **meshes/light\_baking** = `1`
`🔗<class_ResourceImporterScene_property_meshes/light_baking>`

Configures the meshes'
`GeometryInstance3D.gi_mode<class_GeometryInstance3D_property_gi_mode>`
in the 3D scene. If set to **Static Lightmaps**, sets the meshes' GI
mode to Static and generates UV2 on import for
`LightmapGI<class_LightmapGI>` baking.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **meshes/lightmap\_texel\_size** = `0.2`
`🔗<class_ResourceImporterScene_property_meshes/lightmap_texel_size>`

Controls the size of each texel on the baked lightmap. A smaller value
results in more precise lightmaps, at the cost of larger lightmap sizes
and longer bake times.

\*\*Note:\*\* Only effective if
`meshes/light_baking<class_ResourceImporterScene_property_meshes/light_baking>`
is set to **Static Lightmaps**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **nodes/apply\_root\_scale** = `true`
`🔗<class_ResourceImporterScene_property_nodes/apply_root_scale>`

If `true`,
`nodes/root_scale<class_ResourceImporterScene_property_nodes/root_scale>`
will be applied to the descendant nodes, meshes, animations, bones, etc.
This means that if you add a child node later on within the imported
scene, it won't be scaled. If `false`,
`nodes/root_scale<class_ResourceImporterScene_property_nodes/root_scale>`
will multiply the scale of the root node instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **nodes/import\_as\_skeleton\_bones** = `false`
`🔗<class_ResourceImporterScene_property_nodes/import_as_skeleton_bones>`

Treat all nodes in the imported scene as if they are bones within a
single `Skeleton3D<class_Skeleton3D>`. Can be used to guarantee that
imported animations target skeleton bones rather than nodes. May also be
used to assign the `"Root"` bone in a `BoneMap<class_BoneMap>`. See
`Retargeting 3D Skeletons <../tutorials/assets_pipeline/retargeting_3d_skeletons>`
for more information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **nodes/root\_name** = `""`
`🔗<class_ResourceImporterScene_property_nodes/root_name>`

Override for the root node name. If empty, the root node will use what
the scene specifies, or the file name if the scene does not specify a
root name.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **nodes/root\_scale** = `1.0`
`🔗<class_ResourceImporterScene_property_nodes/root_scale>`

The uniform scale to use for the scene root. The default value of `1.0`
will not perform any rescaling. See
`nodes/apply_root_scale<class_ResourceImporterScene_property_nodes/apply_root_scale>`
for details of how this scale is applied.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **nodes/root\_type** = `""`
`🔗<class_ResourceImporterScene_property_nodes/root_type>`

Override for the root node type. If empty, the root node will use what
the scene specifies, or `Node3D<class_Node3D>` if the scene does not
specify a root type. Using a node type that inherits from
`Node3D<class_Node3D>` is recommended. Otherwise, you'll lose the
ability to position the node directly in the 3D editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **nodes/use\_node\_type\_suffixes** = `true`
`🔗<class_ResourceImporterScene_property_nodes/use_node_type_suffixes>`

If `true`, use suffixes in the node names to determine the node type,
such as `-col` for collision shapes. Disabling this makes
editor-imported files more similar to the original files, and more
similar to importing files at runtime. See
`Node type customization using name suffixes <../tutorials/assets_pipeline/importing_3d_scenes/node_type_customization>`
for more information.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **skins/use\_named\_skins** = `true`
`🔗<class_ResourceImporterScene_property_skins/use_named_skins>`

If checked, use named `Skin<class_Skin>`s for animation. The
`MeshInstance3D<class_MeshInstance3D>` node contains 3 properties of
relevance here: a skeleton `NodePath<class_NodePath>` pointing to the
`Skeleton3D<class_Skeleton3D>` node (usually `..`), a mesh, and a skin:

-   The `Skeleton3D<class_Skeleton3D>` node contains a list of bones
    with names, their pose and rest, a name and a parent bone.
-   The mesh is all of the raw vertex data needed to display a mesh. In
    terms of the mesh, it knows how vertices are weight-painted and uses
    some internal numbering often imported from 3D modeling software.
-   The skin contains the information necessary to bind this mesh onto
    this Skeleton3D. For every one of the internal bone IDs chosen by
    the 3D modeling software, it contains two things. Firstly, a matrix
    known as the Bind Pose Matrix, Inverse Bind Matrix, or IBM for
    short. Secondly, the `Skin<class_Skin>` contains each bone's name
    (if
    `skins/use_named_skins<class_ResourceImporterScene_property_skins/use_named_skins>`
    is `true`), or the bone's index within the
    `Skeleton3D<class_Skeleton3D>` list (if
    `skins/use_named_skins<class_ResourceImporterScene_property_skins/use_named_skins>`
    is `false`).

Together, this information is enough to tell Godot how to use the bone
poses in the `Skeleton3D<class_Skeleton3D>` node to render the mesh from
each `MeshInstance3D<class_MeshInstance3D>`. Note that each
`MeshInstance3D<class_MeshInstance3D>` may share binds, as is common in
models exported from Blender, or each
`MeshInstance3D<class_MeshInstance3D>` may use a separate
`Skin<class_Skin>` object, as is common in models exported from other
tools such as Maya.
