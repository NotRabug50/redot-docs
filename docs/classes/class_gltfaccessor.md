github\_url  
hide

# GLTFAccessor

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Represents a glTF accessor.

classref-introduction-group

## Description

GLTFAccessor is a data structure representing a glTF `accessor` that
would be found in the `"accessors"` array. A buffer is a blob of binary
data. A buffer view is a slice of a buffer. An accessor is a typed
interpretation of the data in a buffer view.

Most custom data stored in glTF does not need accessors, only buffer
views (see `GLTFBufferView<class_GLTFBufferView>`). Accessors are for
more advanced use cases such as interleaved mesh data encoded for the
GPU.

classref-introduction-group

## Tutorials

-   [Buffers, BufferViews, and Accessors in Khronos glTF
    specification](https://github.com/KhronosGroup/glTF-Tutorials/blob/master/gltfTutorial/gltfTutorial_005_BuffersBufferViewsAccessors.md)
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

## Enumerations

classref-enumeration

enum **GLTFAccessorType**: `🔗<enum_GLTFAccessor_GLTFAccessorType>`

classref-enumeration-constant

`GLTFAccessorType<enum_GLTFAccessor_GLTFAccessorType>` **TYPE\_SCALAR**
= `0`

Accessor type "SCALAR". For the glTF object model, this can be used to
map to a single float, int, or bool value, or a float array.

classref-enumeration-constant

`GLTFAccessorType<enum_GLTFAccessor_GLTFAccessorType>` **TYPE\_VEC2** =
`1`

Accessor type "VEC2". For the glTF object model, this maps to "float2",
represented in the glTF JSON as an array of two floats.

classref-enumeration-constant

`GLTFAccessorType<enum_GLTFAccessor_GLTFAccessorType>` **TYPE\_VEC3** =
`2`

Accessor type "VEC3". For the glTF object model, this maps to "float3",
represented in the glTF JSON as an array of three floats.

classref-enumeration-constant

`GLTFAccessorType<enum_GLTFAccessor_GLTFAccessorType>` **TYPE\_VEC4** =
`3`

Accessor type "VEC4". For the glTF object model, this maps to "float4",
represented in the glTF JSON as an array of four floats.

classref-enumeration-constant

`GLTFAccessorType<enum_GLTFAccessor_GLTFAccessorType>` **TYPE\_MAT2** =
`4`

Accessor type "MAT2". For the glTF object model, this maps to
"float2x2", represented in the glTF JSON as an array of four floats.

classref-enumeration-constant

`GLTFAccessorType<enum_GLTFAccessor_GLTFAccessorType>` **TYPE\_MAT3** =
`5`

Accessor type "MAT3". For the glTF object model, this maps to
"float3x3", represented in the glTF JSON as an array of nine floats.

classref-enumeration-constant

`GLTFAccessorType<enum_GLTFAccessor_GLTFAccessorType>` **TYPE\_MAT4** =
`6`

Accessor type "MAT4". For the glTF object model, this maps to
"float4x4", represented in the glTF JSON as an array of sixteen floats.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`GLTFAccessorType<enum_GLTFAccessor_GLTFAccessorType>`
**accessor\_type** = `0` `🔗<class_GLTFAccessor_property_accessor_type>`

classref-property-setget

-   `void (No return value.)` **set\_accessor\_type**(value:
    `GLTFAccessorType<enum_GLTFAccessor_GLTFAccessorType>`)
-   `GLTFAccessorType<enum_GLTFAccessor_GLTFAccessorType>`
    **get\_accessor\_type**()

The glTF accessor type as an enum. Possible values are 0 for "SCALAR", 1
for "VEC2", 2 for "VEC3", 3 for "VEC4", 4 for "MAT2", 5 for "MAT3", and
6 for "MAT4".

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **buffer\_view** = `-1`
`🔗<class_GLTFAccessor_property_buffer_view>`

classref-property-setget

-   `void (No return value.)` **set\_buffer\_view**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_buffer\_view**()

The index of the buffer view this accessor is referencing. If `-1`, this
accessor is not referencing any buffer view.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **byte\_offset** = `0`
`🔗<class_GLTFAccessor_property_byte_offset>`

classref-property-setget

-   `void (No return value.)` **set\_byte\_offset**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_byte\_offset**()

The offset relative to the start of the buffer view in bytes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **component\_type** = `0`
`🔗<class_GLTFAccessor_property_component_type>`

classref-property-setget

-   `void (No return value.)` **set\_component\_type**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_component\_type**()

The glTF component type as an enum. Possible values are 5120 for "BYTE",
5121 for "UNSIGNED\_BYTE", 5122 for "SHORT", 5123 for "UNSIGNED\_SHORT",
5125 for "UNSIGNED\_INT", and 5126 for "FLOAT". A value of 5125 or
"UNSIGNED\_INT" must not be used for any accessor that is not referenced
by mesh.primitive.indices.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **count** = `0` `🔗<class_GLTFAccessor_property_count>`

classref-property-setget

-   `void (No return value.)` **set\_count**(value: `int<class_int>`)
-   `int<class_int>` **get\_count**()

The number of elements referenced by this accessor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedFloat64Array<class_PackedFloat64Array>` **max** =
`PackedFloat64Array()` `🔗<class_GLTFAccessor_property_max>`

classref-property-setget

-   `void (No return value.)` **set\_max**(value:
    `PackedFloat64Array<class_PackedFloat64Array>`)
-   `PackedFloat64Array<class_PackedFloat64Array>` **get\_max**()

Maximum value of each component in this accessor.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedFloat64Array<class_PackedFloat64Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`PackedFloat64Array<class_PackedFloat64Array>` **min** =
`PackedFloat64Array()` `🔗<class_GLTFAccessor_property_min>`

classref-property-setget

-   `void (No return value.)` **set\_min**(value:
    `PackedFloat64Array<class_PackedFloat64Array>`)
-   `PackedFloat64Array<class_PackedFloat64Array>` **get\_min**()

Minimum value of each component in this accessor.

**Note:** The returned array is *copied* and any changes to it will not
update the original property value. See
`PackedFloat64Array<class_PackedFloat64Array>` for more details.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **normalized** = `false`
`🔗<class_GLTFAccessor_property_normalized>`

classref-property-setget

-   `void (No return value.)` **set\_normalized**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_normalized**()

Specifies whether integer data values are normalized before usage.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sparse\_count** = `0`
`🔗<class_GLTFAccessor_property_sparse_count>`

classref-property-setget

-   `void (No return value.)` **set\_sparse\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_sparse\_count**()

Number of deviating accessor values stored in the sparse array.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sparse\_indices\_buffer\_view** = `0`
`🔗<class_GLTFAccessor_property_sparse_indices_buffer_view>`

classref-property-setget

-   `void (No return value.)`
    **set\_sparse\_indices\_buffer\_view**(value: `int<class_int>`)
-   `int<class_int>` **get\_sparse\_indices\_buffer\_view**()

The index of the buffer view with sparse indices. The referenced buffer
view MUST NOT have its target or byteStride properties defined. The
buffer view and the optional byteOffset MUST be aligned to the
componentType byte length.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sparse\_indices\_byte\_offset** = `0`
`🔗<class_GLTFAccessor_property_sparse_indices_byte_offset>`

classref-property-setget

-   `void (No return value.)`
    **set\_sparse\_indices\_byte\_offset**(value: `int<class_int>`)
-   `int<class_int>` **get\_sparse\_indices\_byte\_offset**()

The offset relative to the start of the buffer view in bytes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sparse\_indices\_component\_type** = `0`
`🔗<class_GLTFAccessor_property_sparse_indices_component_type>`

classref-property-setget

-   `void (No return value.)`
    **set\_sparse\_indices\_component\_type**(value: `int<class_int>`)
-   `int<class_int>` **get\_sparse\_indices\_component\_type**()

The indices component data type as an enum. Possible values are 5121 for
"UNSIGNED\_BYTE", 5123 for "UNSIGNED\_SHORT", and 5125 for
"UNSIGNED\_INT".

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sparse\_values\_buffer\_view** = `0`
`🔗<class_GLTFAccessor_property_sparse_values_buffer_view>`

classref-property-setget

-   `void (No return value.)`
    **set\_sparse\_values\_buffer\_view**(value: `int<class_int>`)
-   `int<class_int>` **get\_sparse\_values\_buffer\_view**()

The index of the bufferView with sparse values. The referenced buffer
view MUST NOT have its target or byteStride properties defined.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sparse\_values\_byte\_offset** = `0`
`🔗<class_GLTFAccessor_property_sparse_values_byte_offset>`

classref-property-setget

-   `void (No return value.)`
    **set\_sparse\_values\_byte\_offset**(value: `int<class_int>`)
-   `int<class_int>` **get\_sparse\_values\_byte\_offset**()

The offset relative to the start of the bufferView in bytes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **type** `🔗<class_GLTFAccessor_property_type>`

classref-property-setget

-   `void (No return value.)` **set\_type**(value: `int<class_int>`)
-   `int<class_int>` **get\_type**()

**Deprecated:** Use
`accessor_type<class_GLTFAccessor_property_accessor_type>` instead.

The glTF accessor type as an enum. Use
`accessor_type<class_GLTFAccessor_property_accessor_type>` instead.
