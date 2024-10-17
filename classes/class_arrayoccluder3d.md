github\_url  
hide

# ArrayOccluder3D

**Inherits:** `Occluder3D<class_Occluder3D>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

3D polygon shape for use with occlusion culling in
`OccluderInstance3D<class_OccluderInstance3D>`.

classref-introduction-group

## Description

**ArrayOccluder3D** stores an arbitrary 3D polygon shape that can be
used by the engine's occlusion culling system. This is analogous to
`ArrayMesh<class_ArrayMesh>`, but for occluders.

See `OccluderInstance3D<class_OccluderInstance3D>`'s documentation for
instructions on setting up occlusion culling.

classref-introduction-group

## Tutorials

-   `Occlusion culling <../tutorials/3d/occlusion_culling>`

classref-reftable-group

## Properties

<table>
<tbody>
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`PackedInt32Array<class_PackedInt32Array>` **indices** =
`PackedInt32Array()` `🔗<class_ArrayOccluder3D_property_indices>`

classref-property-setget

-   `void (No return value.)` **set\_indices**(value:
    `PackedInt32Array<class_PackedInt32Array>`)
-   `PackedInt32Array<class_PackedInt32Array>` **get\_indices**()

The occluder's index position. Indices determine which points from the
`vertices<class_ArrayOccluder3D_property_vertices>` array should be
drawn, and in which order.

\*\*Note:\*\* The occluder is always updated after setting this value.
If creating occluders procedurally, consider using
`set_arrays<class_ArrayOccluder3D_method_set_arrays>` instead to avoid
updating the occluder twice when it's created.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedInt32Array<class_PackedInt32Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedVector3Array<class_PackedVector3Array>` **vertices** =
`PackedVector3Array()` `🔗<class_ArrayOccluder3D_property_vertices>`

classref-property-setget

-   `void (No return value.)` **set\_vertices**(value:
    `PackedVector3Array<class_PackedVector3Array>`)
-   `PackedVector3Array<class_PackedVector3Array>` **get\_vertices**()

The occluder's vertex positions in local 3D coordinates.

\*\*Note:\*\* The occluder is always updated after setting this value.
If creating occluders procedurally, consider using
`set_arrays<class_ArrayOccluder3D_method_set_arrays>` instead to avoid
updating the occluder twice when it's created.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedVector3Array<class_PackedVector3Array>` for more details.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **set\_arrays**(vertices:
`PackedVector3Array<class_PackedVector3Array>`, indices:
`PackedInt32Array<class_PackedInt32Array>`)
`🔗<class_ArrayOccluder3D_method_set_arrays>`

Sets `indices<class_ArrayOccluder3D_property_indices>` and
`vertices<class_ArrayOccluder3D_property_vertices>`, while updating the
final occluder only once after both values are set.
