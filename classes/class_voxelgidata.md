github\_url  
hide

# VoxelGIData

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Contains baked voxel global illumination data for use in a
`VoxelGI<class_VoxelGI>` node.

classref-introduction-group

## Description

**VoxelGIData** contains baked voxel global illumination for use in a
`VoxelGI<class_VoxelGI>` node. **VoxelGIData** also offers several
properties to adjust the final appearance of the global illumination.
These properties can be adjusted at run-time without having to bake the
`VoxelGI<class_VoxelGI>` node again.

\*\*Note:\*\* To prevent text-based scene files (`.tscn`) from growing
too much and becoming slow to load and save, always save **VoxelGIData**
to an external binary resource file (`.res`) instead of embedding it
within the scene. This can be done by clicking the dropdown arrow next
to the **VoxelGIData** resource, choosing **Edit**, clicking the floppy
disk icon at the top of the Inspector then choosing **Save As...**.

classref-introduction-group

## Tutorials

-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`float<class_float>` **bias** = `1.5`
`🔗<class_VoxelGIData_property_bias>`

classref-property-setget

-   `void (No return value.)` **set\_bias**(value: `float<class_float>`)
-   `float<class_float>` **get\_bias**()

The normal bias to use for indirect lighting and reflections. Higher
values reduce self-reflections visible in non-rough materials, at the
cost of more visible light leaking and flatter-looking indirect
lighting. To prioritize hiding self-reflections over lighting quality,
set `bias<class_VoxelGIData_property_bias>` to `0.0` and
`normal_bias<class_VoxelGIData_property_normal_bias>` to a value between
`1.0` and `2.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **dynamic\_range** = `2.0`
`🔗<class_VoxelGIData_property_dynamic_range>`

classref-property-setget

-   `void (No return value.)` **set\_dynamic\_range**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_dynamic\_range**()

The dynamic range to use (`1.0` represents a low dynamic range scene
brightness). Higher values can be used to provide brighter indirect
lighting, at the cost of more visible color banding in dark areas (both
in indirect lighting and reflections). To avoid color banding, it's
recommended to use the lowest value that does not result in visible
light clipping.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **energy** = `1.0`
`🔗<class_VoxelGIData_property_energy>`

classref-property-setget

-   `void (No return value.)` **set\_energy**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_energy**()

The energy of the indirect lighting and reflections produced by the
`VoxelGI<class_VoxelGI>` node. Higher values result in brighter indirect
lighting. If indirect lighting looks too flat, try decreasing
`propagation<class_VoxelGIData_property_propagation>` while increasing
`energy<class_VoxelGIData_property_energy>` at the same time. See also
`use_two_bounces<class_VoxelGIData_property_use_two_bounces>` which
influences the indirect lighting's effective brightness.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interior** = `false`
`🔗<class_VoxelGIData_property_interior>`

classref-property-setget

-   `void (No return value.)` **set\_interior**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_interior**()

If `true`, `Environment<class_Environment>` lighting is ignored by the
`VoxelGI<class_VoxelGI>` node. If `false`,
`Environment<class_Environment>` lighting is taken into account by the
`VoxelGI<class_VoxelGI>` node. `Environment<class_Environment>` lighting
updates in real-time, which means it can be changed without having to
bake the `VoxelGI<class_VoxelGI>` node again.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **normal\_bias** = `0.0`
`🔗<class_VoxelGIData_property_normal_bias>`

classref-property-setget

-   `void (No return value.)` **set\_normal\_bias**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_normal\_bias**()

The normal bias to use for indirect lighting and reflections. Higher
values reduce self-reflections visible in non-rough materials, at the
cost of more visible light leaking and flatter-looking indirect
lighting. See also `bias<class_VoxelGIData_property_bias>`. To
prioritize hiding self-reflections over lighting quality, set
`bias<class_VoxelGIData_property_bias>` to `0.0` and
`normal_bias<class_VoxelGIData_property_normal_bias>` to a value between
`1.0` and `2.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **propagation** = `0.5`
`🔗<class_VoxelGIData_property_propagation>`

classref-property-setget

-   `void (No return value.)` **set\_propagation**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_propagation**()

The multiplier to use when light bounces off a surface. Higher values
result in brighter indirect lighting. If indirect lighting looks too
flat, try decreasing
`propagation<class_VoxelGIData_property_propagation>` while increasing
`energy<class_VoxelGIData_property_energy>` at the same time. See also
`use_two_bounces<class_VoxelGIData_property_use_two_bounces>` which
influences the indirect lighting's effective brightness.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_two\_bounces** = `true`
`🔗<class_VoxelGIData_property_use_two_bounces>`

classref-property-setget

-   `void (No return value.)` **set\_use\_two\_bounces**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_using\_two\_bounces**()

If `true`, performs two bounces of indirect lighting instead of one.
This makes indirect lighting look more natural and brighter at a small
performance cost. The second bounce is also visible in reflections. If
the scene appears too bright after enabling
`use_two_bounces<class_VoxelGIData_property_use_two_bounces>`, adjust
`propagation<class_VoxelGIData_property_propagation>` and
`energy<class_VoxelGIData_property_energy>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **allocate**(to\_cell\_xform:
`Transform3D<class_Transform3D>`, aabb: `AABB<class_AABB>`,
octree\_size: `Vector3<class_Vector3>`, octree\_cells:
`PackedByteArray<class_PackedByteArray>`, data\_cells:
`PackedByteArray<class_PackedByteArray>`, distance\_field:
`PackedByteArray<class_PackedByteArray>`, level\_counts:
`PackedInt32Array<class_PackedInt32Array>`)
`🔗<class_VoxelGIData_method_allocate>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`AABB<class_AABB>` **get\_bounds**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VoxelGIData_method_get_bounds>`

Returns the bounds of the baked voxel data as an `AABB<class_AABB>`,
which should match `VoxelGI.size<class_VoxelGI_property_size>` after
being baked (which only contains the size as a
`Vector3<class_Vector3>`).

\*\*Note:\*\* If the size was modified without baking the VoxelGI data,
then the value of `get_bounds<class_VoxelGIData_method_get_bounds>` and
`VoxelGI.size<class_VoxelGI_property_size>` will not match.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **get\_data\_cells**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VoxelGIData_method_get_data_cells>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>` **get\_level\_counts**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VoxelGIData_method_get_level_counts>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **get\_octree\_cells**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VoxelGIData_method_get_octree_cells>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector3<class_Vector3>` **get\_octree\_size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VoxelGIData_method_get_octree_size>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **get\_to\_cell\_xform**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_VoxelGIData_method_get_to_cell_xform>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
