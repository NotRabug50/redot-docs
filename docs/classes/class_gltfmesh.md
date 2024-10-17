github\_url  
hide

# GLTFMesh

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

GLTFMesh represents a glTF mesh.

classref-introduction-group

## Description

GLTFMesh handles 3D mesh data imported from glTF files. It includes
properties for blend channels, blend weights, instance materials, and
the mesh itself.

classref-introduction-group

## Tutorials

-   `Runtime file loading and saving <../tutorials/io/runtime_file_loading_and_saving>`

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

classref-reftable-group

## Methods

<table>
<tbody>
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

`PackedFloat32Array<class_PackedFloat32Array>` **blend\_weights** =
`PackedFloat32Array()` `🔗<class_GLTFMesh_property_blend_weights>`

classref-property-setget

-   `void (No return value.)` **set\_blend\_weights**(value:
    `PackedFloat32Array<class_PackedFloat32Array>`)
-   `PackedFloat32Array<class_PackedFloat32Array>`
    **get\_blend\_weights**()

An array of floats representing the blend weights of the mesh.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedFloat32Array<class_PackedFloat32Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Array<class_Array>`\[`Material<class_Material>`\]
**instance\_materials** = `[]`
`🔗<class_GLTFMesh_property_instance_materials>`

classref-property-setget

-   `void (No return value.)` **set\_instance\_materials**(value:
    `Array<class_Array>`\[`Material<class_Material>`\])
-   `Array<class_Array>`\[`Material<class_Material>`\]
    **get\_instance\_materials**()

An array of Material objects representing the materials used in the
mesh.

classref-item-separator

------------------------------------------------------------------------

classref-property

`ImporterMesh<class_ImporterMesh>` **mesh**
`🔗<class_GLTFMesh_property_mesh>`

classref-property-setget

-   `void (No return value.)` **set\_mesh**(value:
    `ImporterMesh<class_ImporterMesh>`)
-   `ImporterMesh<class_ImporterMesh>` **get\_mesh**()

The `ImporterMesh<class_ImporterMesh>` object representing the mesh
itself.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **original\_name** = `""`
`🔗<class_GLTFMesh_property_original_name>`

classref-property-setget

-   `void (No return value.)` **set\_original\_name**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_original\_name**()

The original name of the mesh.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Variant<class_Variant>` **get\_additional\_data**(extension\_name:
`StringName<class_StringName>`)
`🔗<class_GLTFMesh_method_get_additional_data>`

Gets additional arbitrary data in this **GLTFMesh** instance. This can
be used to keep per-node state data in
`GLTFDocumentExtension<class_GLTFDocumentExtension>` classes, which is
important because they are stateless.

The argument should be the
`GLTFDocumentExtension<class_GLTFDocumentExtension>` name (does not have
to match the extension name in the glTF file), and the return value can
be anything you set. If nothing was set, the return value is null.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_additional\_data**(extension\_name:
`StringName<class_StringName>`, additional\_data:
`Variant<class_Variant>`)
`🔗<class_GLTFMesh_method_set_additional_data>`

Sets additional arbitrary data in this **GLTFMesh** instance. This can
be used to keep per-node state data in
`GLTFDocumentExtension<class_GLTFDocumentExtension>` classes, which is
important because they are stateless.

The first argument should be the
`GLTFDocumentExtension<class_GLTFDocumentExtension>` name (does not have
to match the extension name in the glTF file), and the second argument
can be anything you want.
