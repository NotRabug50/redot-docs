github\_url  
hide

# GLTFBufferView

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Represents a glTF buffer view.

classref-introduction-group

## Description

GLTFBufferView is a data structure representing a glTF `bufferView` that
would be found in the `"bufferViews"` array. A buffer is a blob of
binary data. A buffer view is a slice of a buffer that can be used to
identify and extract data from the buffer.

Most custom uses of buffers only need to use the
`buffer<class_GLTFBufferView_property_buffer>`,
`byte_length<class_GLTFBufferView_property_byte_length>`, and
`byte_offset<class_GLTFBufferView_property_byte_offset>`. The
`byte_stride<class_GLTFBufferView_property_byte_stride>` and
`indices<class_GLTFBufferView_property_indices>` properties are for more
advanced use cases such as interleaved mesh data encoded for the GPU.

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

`int<class_int>` **buffer** = `-1`
`🔗<class_GLTFBufferView_property_buffer>`

classref-property-setget

-   `void (No return value.)` **set\_buffer**(value: `int<class_int>`)
-   `int<class_int>` **get\_buffer**()

The index of the buffer this buffer view is referencing. If `-1`, this
buffer view is not referencing any buffer.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **byte\_length** = `0`
`🔗<class_GLTFBufferView_property_byte_length>`

classref-property-setget

-   `void (No return value.)` **set\_byte\_length**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_byte\_length**()

The length, in bytes, of this buffer view. If `0`, this buffer view is
empty.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **byte\_offset** = `0`
`🔗<class_GLTFBufferView_property_byte_offset>`

classref-property-setget

-   `void (No return value.)` **set\_byte\_offset**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_byte\_offset**()

The offset, in bytes, from the start of the buffer to the start of this
buffer view.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **byte\_stride** = `-1`
`🔗<class_GLTFBufferView_property_byte_stride>`

classref-property-setget

-   `void (No return value.)` **set\_byte\_stride**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_byte\_stride**()

The stride, in bytes, between interleaved data. If `-1`, this buffer
view is not interleaved.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **indices** = `false`
`🔗<class_GLTFBufferView_property_indices>`

classref-property-setget

-   `void (No return value.)` **set\_indices**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_indices**()

True if the GLTFBufferView's OpenGL GPU buffer type is an
`ELEMENT_ARRAY_BUFFER` used for vertex indices (integer constant
`34963`). False if the buffer type is any other value. See [Buffers,
BufferViews, and
Accessors](https://github.com/KhronosGroup/glTF-Tutorials/blob/master/gltfTutorial/gltfTutorial_005_BuffersBufferViewsAccessors.md)
for possible values. This property is set on import and used on export.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **vertex\_attributes** = `false`
`🔗<class_GLTFBufferView_property_vertex_attributes>`

classref-property-setget

-   `void (No return value.)` **set\_vertex\_attributes**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_vertex\_attributes**()

True if the GLTFBufferView's OpenGL GPU buffer type is an `ARRAY_BUFFER`
used for vertex attributes (integer constant `34962`). False if the
buffer type is any other value. See [Buffers, BufferViews, and
Accessors](https://github.com/KhronosGroup/glTF-Tutorials/blob/master/gltfTutorial/gltfTutorial_005_BuffersBufferViewsAccessors.md)
for possible values. This property is set on import and used on export.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`PackedByteArray<class_PackedByteArray>`
**load\_buffer\_view\_data**(state: `GLTFState<class_GLTFState>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GLTFBufferView_method_load_buffer_view_data>`

Loads the buffer view data from the buffer referenced by this buffer
view in the given `GLTFState<class_GLTFState>`. Interleaved data with a
byte stride is not yet supported by this method. The data is returned as
a `PackedByteArray<class_PackedByteArray>`.
