github\_url  
hide

# PackedByteArray

A packed array of bytes.

classref-introduction-group

## Description

An array specifically designed to hold bytes. Packs data tightly, so it
saves memory for large array sizes.

\*\*PackedByteArray\*\* also provides methods to encode/decode various
types to/from bytes. The way values are encoded is an implementation
detail and shouldn't be relied upon when interacting with external apps.

\*\*Note:\*\* Packed arrays are always passed by reference. To get a
copy of an array that can be modified independently of the original
array, use `duplicate<class_PackedByteArray_method_duplicate>`. This is
*not* the case for built-in properties and methods. The returned packed
array of these are a copies, and changing it will *not* affect the
original value. To update a built-in property you need to modify the
returned array, and then assign it to the property again.

Note

There are notable differences when using this API with C#. See
`doc_c_sharp_differences` for more information.

classref-reftable-group

## Constructors

<table>
<tbody>
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

classref-reftable-group

## Operators

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

## Constructor Descriptions

classref-constructor

`PackedByteArray<class_PackedByteArray>` **PackedByteArray**()
`🔗<class_PackedByteArray_constructor_PackedByteArray>`

Constructs an empty **PackedByteArray**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`PackedByteArray<class_PackedByteArray>` **PackedByteArray**(from:
`PackedByteArray<class_PackedByteArray>`)

Constructs a **PackedByteArray** as a copy of the given
**PackedByteArray**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`PackedByteArray<class_PackedByteArray>` **PackedByteArray**(from:
`Array<class_Array>`)

Constructs a new **PackedByteArray**. Optionally, you can pass in a
generic `Array<class_Array>` that will be converted.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **append**(value: `int<class_int>`)
`🔗<class_PackedByteArray_method_append>`

Appends an element at the end of the array (alias of
`push_back<class_PackedByteArray_method_push_back>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **append\_array**(array:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_PackedByteArray_method_append_array>`

Appends a **PackedByteArray** at the end of this array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **bsearch**(value: `int<class_int>`, before:
`bool<class_bool>` = true) `🔗<class_PackedByteArray_method_bsearch>`

Finds the index of an existing value (or the insertion index that
maintains sorting order, if the value is not yet present in the array)
using binary search. Optionally, a `before` specifier can be passed. If
`false`, the returned index comes after all existing entries of the
value in the array.

\*\*Note:\*\* Calling `bsearch<class_PackedByteArray_method_bsearch>` on
an unsorted array results in unexpected behavior.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_PackedByteArray_method_clear>`

Clears the array. This is equivalent to using
`resize<class_PackedByteArray_method_resize>` with a size of `0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **compress**(compression\_mode:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_compress>`

Returns a new **PackedByteArray** with the data compressed. Set the
compression mode using one of
`CompressionMode<enum_FileAccess_CompressionMode>`'s constants.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **count**(value: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_count>`

Returns the number of times an element is in the array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **decode\_double**(byte\_offset: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_double>`

Decodes a 64-bit floating-point number from the bytes starting at
`byte_offset`. Fails if the byte count is insufficient. Returns `0.0` if
a valid number can't be decoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **decode\_float**(byte\_offset: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_float>`

Decodes a 32-bit floating-point number from the bytes starting at
`byte_offset`. Fails if the byte count is insufficient. Returns `0.0` if
a valid number can't be decoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **decode\_half**(byte\_offset: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_half>`

Decodes a 16-bit floating-point number from the bytes starting at
`byte_offset`. Fails if the byte count is insufficient. Returns `0.0` if
a valid number can't be decoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **decode\_s8**(byte\_offset: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_s8>`

Decodes a 8-bit signed integer number from the bytes starting at
`byte_offset`. Fails if the byte count is insufficient. Returns `0` if a
valid number can't be decoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **decode\_s16**(byte\_offset: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_s16>`

Decodes a 16-bit signed integer number from the bytes starting at
`byte_offset`. Fails if the byte count is insufficient. Returns `0` if a
valid number can't be decoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **decode\_s32**(byte\_offset: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_s32>`

Decodes a 32-bit signed integer number from the bytes starting at
`byte_offset`. Fails if the byte count is insufficient. Returns `0` if a
valid number can't be decoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **decode\_s64**(byte\_offset: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_s64>`

Decodes a 64-bit signed integer number from the bytes starting at
`byte_offset`. Fails if the byte count is insufficient. Returns `0` if a
valid number can't be decoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **decode\_u8**(byte\_offset: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_u8>`

Decodes a 8-bit unsigned integer number from the bytes starting at
`byte_offset`. Fails if the byte count is insufficient. Returns `0` if a
valid number can't be decoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **decode\_u16**(byte\_offset: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_u16>`

Decodes a 16-bit unsigned integer number from the bytes starting at
`byte_offset`. Fails if the byte count is insufficient. Returns `0` if a
valid number can't be decoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **decode\_u32**(byte\_offset: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_u32>`

Decodes a 32-bit unsigned integer number from the bytes starting at
`byte_offset`. Fails if the byte count is insufficient. Returns `0` if a
valid number can't be decoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **decode\_u64**(byte\_offset: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_u64>`

Decodes a 64-bit unsigned integer number from the bytes starting at
`byte_offset`. Fails if the byte count is insufficient. Returns `0` if a
valid number can't be decoded.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **decode\_var**(byte\_offset: `int<class_int>`,
allow\_objects: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_var>`

Decodes a `Variant<class_Variant>` from the bytes starting at
`byte_offset`. Returns `null` if a valid variant can't be decoded or the
value is `Object<class_Object>`-derived and `allow_objects` is `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **decode\_var\_size**(byte\_offset: `int<class_int>`,
allow\_objects: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decode_var_size>`

Decodes a size of a `Variant<class_Variant>` from the bytes starting at
`byte_offset`. Requires at least 4 bytes of data starting at the offset,
otherwise fails.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **decompress**(buffer\_size:
`int<class_int>`, compression\_mode: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decompress>`

Returns a new **PackedByteArray** with the data decompressed. Set
`buffer_size` to the size of the uncompressed data. Set the compression
mode using one of `CompressionMode<enum_FileAccess_CompressionMode>`'s
constants.

\*\*Note:\*\* Decompression is not guaranteed to work with data not
compressed by Godot, for example if data compressed with the deflate
compression mode lacks a checksum or header.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>`
**decompress\_dynamic**(max\_output\_size: `int<class_int>`,
compression\_mode: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_decompress_dynamic>`

Returns a new **PackedByteArray** with the data decompressed. Set the
compression mode using one of
`CompressionMode<enum_FileAccess_CompressionMode>`'s constants. **This
method only accepts brotli, gzip, and deflate compression modes.**

This method is potentially slower than
`decompress<class_PackedByteArray_method_decompress>`, as it may have to
re-allocate its output buffer multiple times while decompressing,
whereas `decompress<class_PackedByteArray_method_decompress>` knows it's
output buffer size from the beginning.

GZIP has a maximal compression ratio of 1032:1, meaning it's very
possible for a small compressed payload to decompress to a potentially
very large output. To guard against this, you may provide a maximum size
this function is allowed to allocate in bytes via `max_output_size`.
Passing -1 will allow for unbounded output. If any positive value is
passed, and the decompression exceeds that amount in bytes, then an
error will be returned.

\*\*Note:\*\* Decompression is not guaranteed to work with data not
compressed by Godot, for example if data compressed with the deflate
compression mode lacks a checksum or header.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **duplicate**()
`🔗<class_PackedByteArray_method_duplicate>`

Creates a copy of the array, and returns it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **encode\_double**(byte\_offset:
`int<class_int>`, value: `float<class_float>`)
`🔗<class_PackedByteArray_method_encode_double>`

Encodes a 64-bit floating-point number as bytes at the index of
`byte_offset` bytes. The array must have at least 8 bytes of allocated
space, starting at the offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **encode\_float**(byte\_offset:
`int<class_int>`, value: `float<class_float>`)
`🔗<class_PackedByteArray_method_encode_float>`

Encodes a 32-bit floating-point number as bytes at the index of
`byte_offset` bytes. The array must have at least 4 bytes of space,
starting at the offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **encode\_half**(byte\_offset:
`int<class_int>`, value: `float<class_float>`)
`🔗<class_PackedByteArray_method_encode_half>`

Encodes a 16-bit floating-point number as bytes at the index of
`byte_offset` bytes. The array must have at least 2 bytes of space,
starting at the offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **encode\_s8**(byte\_offset: `int<class_int>`,
value: `int<class_int>`) `🔗<class_PackedByteArray_method_encode_s8>`

Encodes a 8-bit signed integer number (signed byte) at the index of
`byte_offset` bytes. The array must have at least 1 byte of space,
starting at the offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **encode\_s16**(byte\_offset:
`int<class_int>`, value: `int<class_int>`)
`🔗<class_PackedByteArray_method_encode_s16>`

Encodes a 16-bit signed integer number as bytes at the index of
`byte_offset` bytes. The array must have at least 2 bytes of space,
starting at the offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **encode\_s32**(byte\_offset:
`int<class_int>`, value: `int<class_int>`)
`🔗<class_PackedByteArray_method_encode_s32>`

Encodes a 32-bit signed integer number as bytes at the index of
`byte_offset` bytes. The array must have at least 4 bytes of space,
starting at the offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **encode\_s64**(byte\_offset:
`int<class_int>`, value: `int<class_int>`)
`🔗<class_PackedByteArray_method_encode_s64>`

Encodes a 64-bit signed integer number as bytes at the index of
`byte_offset` bytes. The array must have at least 8 bytes of space,
starting at the offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **encode\_u8**(byte\_offset: `int<class_int>`,
value: `int<class_int>`) `🔗<class_PackedByteArray_method_encode_u8>`

Encodes a 8-bit unsigned integer number (byte) at the index of
`byte_offset` bytes. The array must have at least 1 byte of space,
starting at the offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **encode\_u16**(byte\_offset:
`int<class_int>`, value: `int<class_int>`)
`🔗<class_PackedByteArray_method_encode_u16>`

Encodes a 16-bit unsigned integer number as bytes at the index of
`byte_offset` bytes. The array must have at least 2 bytes of space,
starting at the offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **encode\_u32**(byte\_offset:
`int<class_int>`, value: `int<class_int>`)
`🔗<class_PackedByteArray_method_encode_u32>`

Encodes a 32-bit unsigned integer number as bytes at the index of
`byte_offset` bytes. The array must have at least 4 bytes of space,
starting at the offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **encode\_u64**(byte\_offset:
`int<class_int>`, value: `int<class_int>`)
`🔗<class_PackedByteArray_method_encode_u64>`

Encodes a 64-bit unsigned integer number as bytes at the index of
`byte_offset` bytes. The array must have at least 8 bytes of space,
starting at the offset.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **encode\_var**(byte\_offset: `int<class_int>`, value:
`Variant<class_Variant>`, allow\_objects: `bool<class_bool>` = false)
`🔗<class_PackedByteArray_method_encode_var>`

Encodes a `Variant<class_Variant>` at the index of `byte_offset` bytes.
A sufficient space must be allocated, depending on the encoded variant's
size. If `allow_objects` is `false`, `Object<class_Object>`-derived
values are not permitted and will instead be serialized as ID-only.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fill**(value: `int<class_int>`)
`🔗<class_PackedByteArray_method_fill>`

Assigns the given value to all elements in the array. This can typically
be used together with `resize<class_PackedByteArray_method_resize>` to
create an array with a given size and initialized elements.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **find**(value: `int<class_int>`, from:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_find>`

Searches the array for a value and returns its index or `-1` if not
found. Optionally, the initial search index can be passed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_get>`

Returns the byte at the given `index` in the array. This is the same as
using the `[]` operator (`array[index]`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_string\_from\_ascii**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_get_string_from_ascii>`

Converts ASCII/Latin-1 encoded array to `String<class_String>`. Fast
alternative to
`get_string_from_utf8<class_PackedByteArray_method_get_string_from_utf8>`
if the content is ASCII/Latin-1 only. Unlike the UTF-8 function this
function maps every byte to a character in the array. Multibyte
sequences will not be interpreted correctly. For parsing user input
always use
`get_string_from_utf8<class_PackedByteArray_method_get_string_from_utf8>`.
This is the inverse of
`String.to_ascii_buffer<class_String_method_to_ascii_buffer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_string\_from\_utf8**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_get_string_from_utf8>`

Converts UTF-8 encoded array to `String<class_String>`. Slower than
`get_string_from_ascii<class_PackedByteArray_method_get_string_from_ascii>`
but supports UTF-8 encoded data. Use this function if you are unsure
about the source of the data. For user input this function should always
be preferred. Returns empty string if source array is not valid UTF-8
string. This is the inverse of
`String.to_utf8_buffer<class_String_method_to_utf8_buffer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_string\_from\_utf16**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_get_string_from_utf16>`

Converts UTF-16 encoded array to `String<class_String>`. If the BOM is
missing, system endianness is assumed. Returns empty string if source
array is not valid UTF-16 string. This is the inverse of
`String.to_utf16_buffer<class_String_method_to_utf16_buffer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_string\_from\_utf32**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_get_string_from_utf32>`

Converts UTF-32 encoded array to `String<class_String>`. System
endianness is assumed. Returns empty string if source array is not valid
UTF-32 string. This is the inverse of
`String.to_utf32_buffer<class_String_method_to_utf32_buffer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_string\_from\_wchar**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_get_string_from_wchar>`

Converts wide character (`wchar_t`, UTF-16 on Windows, UTF-32 on other
platforms) encoded array to `String<class_String>`. Returns empty string
if source array is not valid wide string. This is the inverse of
`String.to_wchar_buffer<class_String_method_to_wchar_buffer>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has**(value: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_has>`

Returns `true` if the array contains `value`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_encoded\_var**(byte\_offset: `int<class_int>`,
allow\_objects: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_has_encoded_var>`

Returns `true` if a valid `Variant<class_Variant>` value can be decoded
at the `byte_offset`. Returns `false` otherwise or when the value is
`Object<class_Object>`-derived and `allow_objects` is `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **hex\_encode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_hex_encode>`

Returns a hexadecimal representation of this array as a
`String<class_String>`.

gdscript

var array = PackedByteArray(\[11, 46, 255\]) print(array.hex\_encode())
\# Prints: 0b2eff

csharp

var array = new byte\[\] {11, 46, 255}; GD.Print(array.HexEncode()); //
Prints: 0b2eff

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **insert**(at\_index: `int<class_int>`, value:
`int<class_int>`) `🔗<class_PackedByteArray_method_insert>`

Inserts a new element at a given position in the array. The position
must be valid, or at the end of the array (`idx == size()`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_empty**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_is_empty>`

Returns `true` if the array is empty.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **push\_back**(value: `int<class_int>`)
`🔗<class_PackedByteArray_method_push_back>`

Appends an element at the end of the array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_at**(index: `int<class_int>`)
`🔗<class_PackedByteArray_method_remove_at>`

Removes an element from the array by index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **resize**(new\_size: `int<class_int>`)
`🔗<class_PackedByteArray_method_resize>`

Sets the size of the array. If the array is grown, reserves elements at
the end of the array. If the array is shrunk, truncates the array to the
new size. Calling `resize<class_PackedByteArray_method_resize>` once and
assigning the new values is faster than adding new elements one by one.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reverse**()
`🔗<class_PackedByteArray_method_reverse>`

Reverses the order of the elements in the array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **rfind**(value: `int<class_int>`, from:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_rfind>`

Searches the array in reverse order. Optionally, a start search index
can be passed. If negative, the start index is considered relative to
the end of the array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set**(index: `int<class_int>`, value:
`int<class_int>`) `🔗<class_PackedByteArray_method_set>`

Changes the byte at the given index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_size>`

Returns the number of elements in the array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **slice**(begin:
`int<class_int>`, end: `int<class_int>` = 2147483647)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_slice>`

Returns the slice of the **PackedByteArray**, from `begin` (inclusive)
to `end` (exclusive), as a new **PackedByteArray**.

The absolute value of `begin` and `end` will be clamped to the array
size, so the default value for `end` makes it slice to the size of the
array by default (i.e. `arr.slice(1)` is a shorthand for
`arr.slice(1, arr.size())`).

If either `begin` or `end` are negative, they will be relative to the
end of the array (i.e. `arr.slice(0, -2)` is a shorthand for
`arr.slice(0, arr.size() - 2)`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **sort**()
`🔗<class_PackedByteArray_method_sort>`

Sorts the elements of the array in ascending order.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedFloat32Array<class_PackedFloat32Array>` **to\_float32\_array**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_to_float32_array>`

Returns a copy of the data converted to a
`PackedFloat32Array<class_PackedFloat32Array>`, where each block of 4
bytes has been converted to a 32-bit float (C++ `float`).

The size of the input array must be a multiple of 4 (size of 32-bit
float). The size of the new array will be `byte_array.size() / 4`.

If the original data can't be converted to 32-bit floats, the resulting
data is undefined.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedFloat64Array<class_PackedFloat64Array>` **to\_float64\_array**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_to_float64_array>`

Returns a copy of the data converted to a
`PackedFloat64Array<class_PackedFloat64Array>`, where each block of 8
bytes has been converted to a 64-bit float (C++ `double`, Godot
`float<class_float>`).

The size of the input array must be a multiple of 8 (size of 64-bit
double). The size of the new array will be `byte_array.size() / 8`.

If the original data can't be converted to 64-bit floats, the resulting
data is undefined.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt32Array<class_PackedInt32Array>` **to\_int32\_array**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_to_int32_array>`

Returns a copy of the data converted to a
`PackedInt32Array<class_PackedInt32Array>`, where each block of 4 bytes
has been converted to a signed 32-bit integer (C++ `int32_t`).

The size of the input array must be a multiple of 4 (size of 32-bit
integer). The size of the new array will be `byte_array.size() / 4`.

If the original data can't be converted to signed 32-bit integers, the
resulting data is undefined.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedInt64Array<class_PackedInt64Array>` **to\_int64\_array**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedByteArray_method_to_int64_array>`

Returns a copy of the data converted to a
`PackedInt64Array<class_PackedInt64Array>`, where each block of 8 bytes
has been converted to a signed 64-bit integer (C++ `int64_t`, Godot
`int<class_int>`).

The size of the input array must be a multiple of 8 (size of 64-bit
integer). The size of the new array will be `byte_array.size() / 8`.

If the original data can't be converted to signed 64-bit integers, the
resulting data is undefined.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Operator Descriptions

classref-operator

`bool<class_bool>` **operator !=**(right:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_PackedByteArray_operator_neq_PackedByteArray>`

Returns `true` if contents of the arrays differ.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`PackedByteArray<class_PackedByteArray>` **operator +**(right:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_PackedByteArray_operator_sum_PackedByteArray>`

Returns a new **PackedByteArray** with contents of `right` added at the
end of this array. For better performance, consider using
`append_array<class_PackedByteArray_method_append_array>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_PackedByteArray_operator_eq_PackedByteArray>`

Returns `true` if contents of both arrays are the same, i.e. they have
all equal bytes at the corresponding indices.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`int<class_int>` **operator \[\]**(index: `int<class_int>`)
`🔗<class_PackedByteArray_operator_idx_int>`

Returns the byte at index `index`. Negative indices can be used to
access the elements starting from the end. Using index out of array's
bounds will result in an error.

Note that the byte is returned as a 64-bit `int<class_int>`.
