github\_url  
hide

# Transform3D

A 3×4 matrix representing a 3D transformation.

classref-introduction-group

## Description

The **Transform3D** built-in `Variant<class_Variant>` type is a 3×4
matrix representing a transformation in 3D space. It contains a
`Basis<class_Basis>`, which on its own can represent rotation, scale,
and shear. Additionally, combined with its own
`origin<class_Transform3D_property_origin>`, the transform can also
represent a translation.

For a general introduction, see the
`Matrices and transforms <../tutorials/math/matrices_and_transforms>`
tutorial.

\*\*Note:\*\* Godot uses a [right-handed coordinate
system](https://en.wikipedia.org/wiki/Right-hand_rule), which is a
common standard. For directions, the convention for built-in types like
`Camera3D<class_Camera3D>` is for -Z to point forward (+X is right, +Y
is up, and +Z is back). Other objects may use different direction
conventions. For more information, see the [3D asset direction
conventions](../tutorials/assets_pipeline/importing_3d_scenes/model_export_considerations.html#d-asset-direction-conventions)
tutorial.

Note

There are notable differences when using this API with C#. See
`doc_c_sharp_differences` for more information.

classref-introduction-group

## Tutorials

-   `Math documentation index <../tutorials/math/index>`
-   `Matrices and transforms <../tutorials/math/matrices_and_transforms>`
-   `Using 3D transforms <../tutorials/3d/using_transforms>`
-   [Matrix Transform
    Demo](https://godotengine.org/asset-library/asset/2787)
-   [3D Platformer
    Demo](https://godotengine.org/asset-library/asset/2748)
-   [2.5D Game Demo](https://godotengine.org/asset-library/asset/2783)

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

## Constructors

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

## Constants

classref-constant

**IDENTITY** = `Transform3D(1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0)`
`🔗<class_Transform3D_constant_IDENTITY>`

A transform with no translation, no rotation, and its scale being `1`.
Its `basis<class_Transform3D_property_basis>` is equal to
`Basis.IDENTITY<class_Basis_constant_IDENTITY>`.

When multiplied by another `Variant<class_Variant>` such as
`AABB<class_AABB>` or another **Transform3D**, no transformation occurs.

classref-constant

**FLIP\_X** = `Transform3D(-1, 0, 0, 0, 1, 0, 0, 0, 1, 0, 0, 0)`
`🔗<class_Transform3D_constant_FLIP_X>`

**Transform3D** with mirroring applied perpendicular to the YZ plane.
Its `basis<class_Transform3D_property_basis>` is equal to
`Basis.FLIP_X<class_Basis_constant_FLIP_X>`.

classref-constant

**FLIP\_Y** = `Transform3D(1, 0, 0, 0, -1, 0, 0, 0, 1, 0, 0, 0)`
`🔗<class_Transform3D_constant_FLIP_Y>`

**Transform3D** with mirroring applied perpendicular to the XZ plane.
Its `basis<class_Transform3D_property_basis>` is equal to
`Basis.FLIP_Y<class_Basis_constant_FLIP_Y>`.

classref-constant

**FLIP\_Z** = `Transform3D(1, 0, 0, 0, 1, 0, 0, 0, -1, 0, 0, 0)`
`🔗<class_Transform3D_constant_FLIP_Z>`

**Transform3D** with mirroring applied perpendicular to the XY plane.
Its `basis<class_Transform3D_property_basis>` is equal to
`Basis.FLIP_Z<class_Basis_constant_FLIP_Z>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Basis<class_Basis>` **basis** = `Basis(1, 0, 0, 0, 1, 0, 0, 0, 1)`
`🔗<class_Transform3D_property_basis>`

The `Basis<class_Basis>` of this transform. It is composed by 3 axes
(`Basis.x<class_Basis_property_x>`, `Basis.y<class_Basis_property_y>`,
and `Basis.z<class_Basis_property_z>`). Together, these represent the
transform's rotation, scale, and shear.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **origin** = `Vector3(0, 0, 0)`
`🔗<class_Transform3D_property_origin>`

The translation offset of this transform. In 3D space, this can be seen
as the position.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constructor Descriptions

classref-constructor

`Transform3D<class_Transform3D>` **Transform3D**()
`🔗<class_Transform3D_constructor_Transform3D>`

Constructs a **Transform3D** identical to the
`IDENTITY<class_Transform3D_constant_IDENTITY>`.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Transform3D<class_Transform3D>` **Transform3D**(from:
`Transform3D<class_Transform3D>`)

Constructs a **Transform3D** as a copy of the given **Transform3D**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Transform3D<class_Transform3D>` **Transform3D**(basis:
`Basis<class_Basis>`, origin: `Vector3<class_Vector3>`)

Constructs a **Transform3D** from a `Basis<class_Basis>` and
`Vector3<class_Vector3>`.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Transform3D<class_Transform3D>` **Transform3D**(from:
`Projection<class_Projection>`)

Constructs a **Transform3D** from a `Projection<class_Projection>`.
Because **Transform3D** is a 3×4 matrix and
`Projection<class_Projection>` is a 4×4 matrix, this operation trims the
last row of the projection matrix (`from.x.w`, `from.y.w`, `from.z.w`,
and `from.w.w` are not included in the new transform).

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Transform3D<class_Transform3D>` **Transform3D**(x\_axis:
`Vector3<class_Vector3>`, y\_axis: `Vector3<class_Vector3>`, z\_axis:
`Vector3<class_Vector3>`, origin: `Vector3<class_Vector3>`)

Constructs a **Transform3D** from four `Vector3<class_Vector3>` values
(also called matrix columns).

The first three arguments are the
`basis<class_Transform3D_property_basis>`'s axes
(`Basis.x<class_Basis_property_x>`, `Basis.y<class_Basis_property_y>`,
and `Basis.z<class_Basis_property_z>`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Transform3D<class_Transform3D>` **affine\_inverse**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_affine_inverse>`

Returns the inverted version of this transform. Unlike
`inverse<class_Transform3D_method_inverse>`, this method works with
almost any `basis<class_Transform3D_property_basis>`, including
non-uniform ones, but is slower. See also
`Basis.inverse<class_Basis_method_inverse>`.

\*\*Note:\*\* For this method to return correctly, the transform's
`basis<class_Transform3D_property_basis>` needs to have a determinant
that is not exactly `0` (see
`Basis.determinant<class_Basis_method_determinant>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **interpolate\_with**(xform:
`Transform3D<class_Transform3D>`, weight: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_interpolate_with>`

Returns the result of the linear interpolation between this transform
and `xform` by the given `weight`.

The `weight` should be between `0.0` and `1.0` (inclusive). Values
outside this range are allowed and can be used to perform
*extrapolation* instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **inverse**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_inverse>`

Returns the inverted version of this transform. See also
`Basis.inverse<class_Basis_method_inverse>`.

\*\*Note:\*\* For this method to return correctly, the transform's
`basis<class_Transform3D_property_basis>` needs to be *orthonormal* (see
`Basis.orthonormalized<class_Basis_method_orthonormalized>`). That
means, the basis should only represent a rotation. If it does not, use
`affine_inverse<class_Transform3D_method_affine_inverse>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_equal\_approx**(xform:
`Transform3D<class_Transform3D>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_is_equal_approx>`

Returns `true` if this transform and `xform` are approximately equal, by
running
`@GlobalScope.is_equal_approx<class_@GlobalScope_method_is_equal_approx>`
on each component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_finite**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_is_finite>`

Returns `true` if this transform is finite, by calling
`@GlobalScope.is_finite<class_@GlobalScope_method_is_finite>` on each
component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **looking\_at**(target:
`Vector3<class_Vector3>`, up: `Vector3<class_Vector3>` = Vector3(0, 1,
0), use\_model\_front: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_looking_at>`

Returns a copy of this transform rotated so that the forward axis (-Z)
points towards the `target` position.

The up axis (+Y) points as close to the `up` vector as possible while
staying perpendicular to the forward axis. The resulting transform is
orthonormalized. The existing rotation, scale, and skew information from
the original transform is discarded. The `target` and `up` vectors
cannot be zero, cannot be parallel to each other, and are defined in
global/parent space.

If `use_model_front` is `true`, the +Z axis (asset front) is treated as
forward (implies +X is left) and points toward the `target` position. By
default, the -Z axis (camera forward) is treated as forward (implies +X
is right).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **orthonormalized**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_orthonormalized>`

Returns a copy of this transform with its
`basis<class_Transform3D_property_basis>` orthonormalized. An
orthonormal basis is both *orthogonal* (the axes are perpendicular to
each other) and *normalized* (the axes have a length of `1`), which also
means it can only represent rotation. See also
`Basis.orthonormalized<class_Basis_method_orthonormalized>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **rotated**(axis:
`Vector3<class_Vector3>`, angle: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_rotated>`

Returns a copy of this transform rotated around the given `axis` by the
given `angle` (in radians).

The `axis` must be a normalized vector.

This method is an optimized version of multiplying the given transform
`X` with a corresponding rotation transform `R` from the left, i.e.,
`R * X`.

This can be seen as transforming with respect to the global/parent
frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **rotated\_local**(axis:
`Vector3<class_Vector3>`, angle: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_rotated_local>`

Returns a copy of this transform rotated around the given `axis` by the
given `angle` (in radians).

The `axis` must be a normalized vector.

This method is an optimized version of multiplying the given transform
`X` with a corresponding rotation transform `R` from the right, i.e.,
`X * R`.

This can be seen as transforming with respect to the local frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **scaled**(scale:
`Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_scaled>`

Returns a copy of this transform scaled by the given `scale` factor.

This method is an optimized version of multiplying the given transform
`X` with a corresponding scaling transform `S` from the left, i.e.,
`S * X`.

This can be seen as transforming with respect to the global/parent
frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **scaled\_local**(scale:
`Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_scaled_local>`

Returns a copy of this transform scaled by the given `scale` factor.

This method is an optimized version of multiplying the given transform
`X` with a corresponding scaling transform `S` from the right, i.e.,
`X * S`.

This can be seen as transforming with respect to the local frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **translated**(offset:
`Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_translated>`

Returns a copy of this transform translated by the given `offset`.

This method is an optimized version of multiplying the given transform
`X` with a corresponding translation transform `T` from the left, i.e.,
`T * X`.

This can be seen as transforming with respect to the global/parent
frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform3D<class_Transform3D>` **translated\_local**(offset:
`Vector3<class_Vector3>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform3D_method_translated_local>`

Returns a copy of this transform translated by the given `offset`.

This method is an optimized version of multiplying the given transform
`X` with a corresponding translation transform `T` from the right, i.e.,
`X * T`.

This can be seen as transforming with respect to the local frame.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Operator Descriptions

classref-operator

`bool<class_bool>` **operator !=**(right:
`Transform3D<class_Transform3D>`)
`🔗<class_Transform3D_operator_neq_Transform3D>`

Returns `true` if the components of both transforms are not equal.

\*\*Note:\*\* Due to floating-point precision errors, consider using
`is_equal_approx<class_Transform3D_method_is_equal_approx>` instead,
which is more reliable.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`AABB<class_AABB>` **operator**\*(right: `AABB<class_AABB>`)
`🔗<class_Transform3D_operator_mul_AABB>`

Transforms (multiplies) the `AABB<class_AABB>` by this transformation
matrix.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`PackedVector3Array<class_PackedVector3Array>` **operator**\*(right:
`PackedVector3Array<class_PackedVector3Array>`)
`🔗<class_Transform3D_operator_mul_PackedVector3Array>`

Transforms (multiplies) every `Vector3<class_Vector3>` element of the
given `PackedVector3Array<class_PackedVector3Array>` by this
transformation matrix.

On larger arrays, this operation is much faster than transforming each
`Vector3<class_Vector3>` individually.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Plane<class_Plane>` **operator**\*(right: `Plane<class_Plane>`)
`🔗<class_Transform3D_operator_mul_Plane>`

Transforms (multiplies) the `Plane<class_Plane>` by this transformation
matrix.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Transform3D<class_Transform3D>` **operator**\*(right:
`Transform3D<class_Transform3D>`)
`🔗<class_Transform3D_operator_mul_Transform3D>`

Transforms (multiplies) this transform by the `right` transform.

This is the operation performed between parent and child
`Node3D<class_Node3D>`s.

\*\*Note:\*\* If you need to only modify one attribute of this
transform, consider using one of the following methods, instead:

-   For translation, see
    `translated<class_Transform3D_method_translated>` or
    `translated_local<class_Transform3D_method_translated_local>`.
-   For rotation, see `rotated<class_Transform3D_method_rotated>` or
    `rotated_local<class_Transform3D_method_rotated_local>`.
-   For scale, see `scaled<class_Transform3D_method_scaled>` or
    `scaled_local<class_Transform3D_method_scaled_local>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector3<class_Vector3>` **operator**\*(right: `Vector3<class_Vector3>`)
`🔗<class_Transform3D_operator_mul_Vector3>`

Transforms (multiplies) the `Vector3<class_Vector3>` by this
transformation matrix.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Transform3D<class_Transform3D>` **operator**\*(right:
`float<class_float>`) `🔗<class_Transform3D_operator_mul_float>`

Multiplies all components of the **Transform3D** by the given
`float<class_float>`, including the
`origin<class_Transform3D_property_origin>`. This affects the
transform's scale uniformly, scaling the
`basis<class_Transform3D_property_basis>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Transform3D<class_Transform3D>` **operator**\*(right: `int<class_int>`)
`🔗<class_Transform3D_operator_mul_int>`

Multiplies all components of the **Transform3D** by the given
`int<class_int>`, including the
`origin<class_Transform3D_property_origin>`. This affects the
transform's scale uniformly, scaling the
`basis<class_Transform3D_property_basis>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Transform3D<class_Transform3D>` **operator /**(right:
`float<class_float>`) `🔗<class_Transform3D_operator_div_float>`

Divides all components of the **Transform3D** by the given
`float<class_float>`, including the
`origin<class_Transform3D_property_origin>`. This affects the
transform's scale uniformly, scaling the
`basis<class_Transform3D_property_basis>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Transform3D<class_Transform3D>` **operator /**(right: `int<class_int>`)
`🔗<class_Transform3D_operator_div_int>`

Divides all components of the **Transform3D** by the given
`int<class_int>`, including the
`origin<class_Transform3D_property_origin>`. This affects the
transform's scale uniformly, scaling the
`basis<class_Transform3D_property_basis>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right:
`Transform3D<class_Transform3D>`)
`🔗<class_Transform3D_operator_eq_Transform3D>`

Returns `true` if the components of both transforms are exactly equal.

\*\*Note:\*\* Due to floating-point precision errors, consider using
`is_equal_approx<class_Transform3D_method_is_equal_approx>` instead,
which is more reliable.
