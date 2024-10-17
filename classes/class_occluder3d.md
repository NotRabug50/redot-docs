github\_url  
hide

# Occluder3D

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

**Inherited By:** `ArrayOccluder3D<class_ArrayOccluder3D>`,
`BoxOccluder3D<class_BoxOccluder3D>`,
`PolygonOccluder3D<class_PolygonOccluder3D>`,
`QuadOccluder3D<class_QuadOccluder3D>`,
`SphereOccluder3D<class_SphereOccluder3D>`

Occluder shape resource for use with occlusion culling in
`OccluderInstance3D<class_OccluderInstance3D>`.

classref-introduction-group

## Description

**Occluder3D** stores an occluder shape that can be used by the engine's
occlusion culling system.

See `OccluderInstance3D<class_OccluderInstance3D>`'s documentation for
instructions on setting up occlusion culling.

classref-introduction-group

## Tutorials

-   `Occlusion culling <../tutorials/3d/occlusion_culling>`

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

## Method Descriptions

classref-method

`PackedInt32Array<class_PackedInt32Array>` **get\_indices**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Occluder3D_method_get_indices>`

Returns the occluder shape's vertex indices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector3Array<class_PackedVector3Array>` **get\_vertices**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Occluder3D_method_get_vertices>`

Returns the occluder shape's vertex positions.
