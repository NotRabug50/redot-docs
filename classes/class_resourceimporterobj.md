github\_url  
hide

# ResourceImporterOBJ

**Inherits:** `ResourceImporter<class_ResourceImporter>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Imports an OBJ 3D model as an independent `Mesh<class_Mesh>` or scene.

classref-introduction-group

## Description

Unlike `ResourceImporterScene<class_ResourceImporterScene>`,
**ResourceImporterOBJ** will import a single `Mesh<class_Mesh>` resource
by default instead of importing a `PackedScene<class_PackedScene>`. This
makes it easier to use the `Mesh<class_Mesh>` resource in nodes that
expect direct `Mesh<class_Mesh>` resources, such as
`GridMap<class_GridMap>`, `GPUParticles3D<class_GPUParticles3D>` or
`CPUParticles3D<class_CPUParticles3D>`. Note that it is still possible
to save mesh resources from 3D scenes using the **Advanced Import
Settings** dialog, regardless of the source format.

See also `ResourceImporterScene<class_ResourceImporterScene>`, which is
used for more advanced 3D formats such as glTF.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **force\_disable\_mesh\_compression** = `false`
`🔗<class_ResourceImporterOBJ_property_force_disable_mesh_compression>`

If `true`, mesh compression will not be used. Consider enabling if you
notice blocky artifacts in your mesh normals or UVs, or if you have
meshes that are larger than a few thousand meters in each direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **generate\_tangents** = `true`
`🔗<class_ResourceImporterOBJ_property_generate_tangents>`

If `true`, generate vertex tangents using
[Mikktspace](http://www.mikktspace.com/) if the source mesh doesn't have
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

`Vector3<class_Vector3>` **offset\_mesh** = `Vector3(0, 0, 0)`
`🔗<class_ResourceImporterOBJ_property_offset_mesh>`

Offsets the mesh's data by the specified value. This can be used to work
around misaligned meshes without having to modify the source file.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **scale\_mesh** = `Vector3(1, 1, 1)`
`🔗<class_ResourceImporterOBJ_property_scale_mesh>`

Scales the mesh's data by the specified value. This can be used to work
around misscaled meshes without having to modify the source file.
