github\_url  
hide

# PackedVector4Array

A packed array of `Vector4<class_Vector4>`s.

classref-introduction-group

## Description

An array specifically designed to hold `Vector4<class_Vector4>`. Packs
data tightly, so it saves memory for large array sizes.

\*\*Note:\*\* Packed arrays are always passed by reference. To get a
copy of an array that can be modified independently of the original
array, use `duplicate<class_PackedVector4Array_method_duplicate>`. This
is *not* the case for built-in properties and methods. The returned
packed array of these are a copies, and changing it will *not* affect
the original value. To update a built-in property you need to modify the
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

`PackedVector4Array<class_PackedVector4Array>` **PackedVector4Array**()
`🔗<class_PackedVector4Array_constructor_PackedVector4Array>`

Constructs an empty **PackedVector4Array**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`PackedVector4Array<class_PackedVector4Array>`
**PackedVector4Array**(from:
`PackedVector4Array<class_PackedVector4Array>`)

Constructs a **PackedVector4Array** as a copy of the given
**PackedVector4Array**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`PackedVector4Array<class_PackedVector4Array>`
**PackedVector4Array**(from: `Array<class_Array>`)

Constructs a new **PackedVector4Array**. Optionally, you can pass in a
generic `Array<class_Array>` that will be converted.

\*\*Note:\*\* When initializing a **PackedVector4Array** with elements,
it must be initialized with an `Array<class_Array>` of
`Vector4<class_Vector4>` values:

    var array = PackedVector4Array([Vector4(12, 34, 56, 78), Vector4(90, 12, 34, 56)])

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **append**(value: `Vector4<class_Vector4>`)
`🔗<class_PackedVector4Array_method_append>`

Appends an element at the end of the array (alias of
`push_back<class_PackedVector4Array_method_push_back>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **append\_array**(array:
`PackedVector4Array<class_PackedVector4Array>`)
`🔗<class_PackedVector4Array_method_append_array>`

Appends a **PackedVector4Array** at the end of this array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **bsearch**(value: `Vector4<class_Vector4>`, before:
`bool<class_bool>` = true) `🔗<class_PackedVector4Array_method_bsearch>`

Finds the index of an existing value (or the insertion index that
maintains sorting order, if the value is not yet present in the array)
using binary search. Optionally, a `before` specifier can be passed. If
`false`, the returned index comes after all existing entries of the
value in the array.

\*\*Note:\*\* Calling `bsearch<class_PackedVector4Array_method_bsearch>`
on an unsorted array results in unexpected behavior.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this method may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_PackedVector4Array_method_clear>`

Clears the array. This is equivalent to using
`resize<class_PackedVector4Array_method_resize>` with a size of `0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **count**(value: `Vector4<class_Vector4>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedVector4Array_method_count>`

Returns the number of times an element is in the array.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this method may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector4Array<class_PackedVector4Array>` **duplicate**()
`🔗<class_PackedVector4Array_method_duplicate>`

Creates a copy of the array, and returns it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **fill**(value: `Vector4<class_Vector4>`)
`🔗<class_PackedVector4Array_method_fill>`

Assigns the given value to all elements in the array. This can typically
be used together with `resize<class_PackedVector4Array_method_resize>`
to create an array with a given size and initialized elements.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **find**(value: `Vector4<class_Vector4>`, from:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedVector4Array_method_find>`

Searches the array for a value and returns its index or `-1` if not
found. Optionally, the initial search index can be passed.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this method may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector4<class_Vector4>` **get**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedVector4Array_method_get>`

Returns the `Vector4<class_Vector4>` at the given `index` in the array.
This is the same as using the `[]` operator (`array[index]`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has**(value: `Vector4<class_Vector4>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedVector4Array_method_has>`

Returns `true` if the array contains `value`.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this method may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **insert**(at\_index: `int<class_int>`, value:
`Vector4<class_Vector4>`) `🔗<class_PackedVector4Array_method_insert>`

Inserts a new element at a given position in the array. The position
must be valid, or at the end of the array (`idx == size()`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_empty**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedVector4Array_method_is_empty>`

Returns `true` if the array is empty.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **push\_back**(value: `Vector4<class_Vector4>`)
`🔗<class_PackedVector4Array_method_push_back>`

Inserts a `Vector4<class_Vector4>` at the end.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_at**(index: `int<class_int>`)
`🔗<class_PackedVector4Array_method_remove_at>`

Removes an element from the array by index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **resize**(new\_size: `int<class_int>`)
`🔗<class_PackedVector4Array_method_resize>`

Sets the size of the array. If the array is grown, reserves elements at
the end of the array. If the array is shrunk, truncates the array to the
new size.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **reverse**()
`🔗<class_PackedVector4Array_method_reverse>`

Reverses the order of the elements in the array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **rfind**(value: `Vector4<class_Vector4>`, from:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedVector4Array_method_rfind>`

Searches the array in reverse order. Optionally, a start search index
can be passed. If negative, the start index is considered relative to
the end of the array.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this method may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set**(index: `int<class_int>`, value:
`Vector4<class_Vector4>`) `🔗<class_PackedVector4Array_method_set>`

Changes the `Vector4<class_Vector4>` at the given index.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedVector4Array_method_size>`

Returns the number of elements in the array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedVector4Array<class_PackedVector4Array>` **slice**(begin:
`int<class_int>`, end: `int<class_int>` = 2147483647)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedVector4Array_method_slice>`

Returns the slice of the **PackedVector4Array**, from `begin`
(inclusive) to `end` (exclusive), as a new **PackedVector4Array**.

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
`🔗<class_PackedVector4Array_method_sort>`

Sorts the elements of the array in ascending order.

\*\*Note:\*\* Vectors with `@GDScript.NAN<class_@GDScript_constant_NAN>`
elements don't behave the same as other vectors. Therefore, the results
from this method may not be accurate if NaNs are included.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **to\_byte\_array**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_PackedVector4Array_method_to_byte_array>`

Returns a `PackedByteArray<class_PackedByteArray>` with each vector
encoded as bytes.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Operator Descriptions

classref-operator

`bool<class_bool>` **operator !=**(right:
`PackedVector4Array<class_PackedVector4Array>`)
`🔗<class_PackedVector4Array_operator_neq_PackedVector4Array>`

Returns `true` if contents of the arrays differ.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`PackedVector4Array<class_PackedVector4Array>` **operator +**(right:
`PackedVector4Array<class_PackedVector4Array>`)
`🔗<class_PackedVector4Array_operator_sum_PackedVector4Array>`

Returns a new **PackedVector4Array** with contents of `right` added at
the end of this array. For better performance, consider using
`append_array<class_PackedVector4Array_method_append_array>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right:
`PackedVector4Array<class_PackedVector4Array>`)
`🔗<class_PackedVector4Array_operator_eq_PackedVector4Array>`

Returns `true` if contents of both arrays are the same, i.e. they have
all equal `Vector4<class_Vector4>`s at the corresponding indices.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector4<class_Vector4>` **operator \[\]**(index: `int<class_int>`)
`🔗<class_PackedVector4Array_operator_idx_int>`

Returns the `Vector4<class_Vector4>` at index `index`. Negative indices
can be used to access the elements starting from the end. Using index
out of array's bounds will result in an error.
