github\_url  
hide

# Transform2D

A 2×3 matrix representing a 2D transformation.

classref-introduction-group

## Description

The **Transform2D** built-in `Variant<class_Variant>` type is a 2×3
[matrix](https://en.wikipedia.org/wiki/Matrix_(mathematics))
representing a transformation in 2D space. It contains three
`Vector2<class_Vector2>` values: `x<class_Transform2D_property_x>`,
`y<class_Transform2D_property_y>`, and
`origin<class_Transform2D_property_origin>`. Together, they can
represent translation, rotation, scale, and skew.

The `x<class_Transform2D_property_x>` and
`y<class_Transform2D_property_y>` axes form a 2×2 matrix, known as the
transform's **basis**. The length of each axis
(`Vector2.length<class_Vector2_method_length>`) influences the
transform's scale, while the direction of all axes influence the
rotation. Usually, both axes are perpendicular to one another. However,
when you rotate one axis individually, the transform becomes skewed.
Applying a skewed transform to a 2D sprite will make the sprite appear
distorted.

For a general introduction, see the
`Matrices and transforms <../tutorials/math/matrices_and_transforms>`
tutorial.

\*\*Note:\*\* Unlike `Transform3D<class_Transform3D>`, there is no 2D
equivalent to the `Basis<class_Basis>` type. All mentions of "basis"
refer to the `x<class_Transform2D_property_x>` and
`y<class_Transform2D_property_y>` components of **Transform2D**.

Note

There are notable differences when using this API with C#. See
`doc_c_sharp_differences` for more information.

classref-introduction-group

## Tutorials

-   `Math documentation index <../tutorials/math/index>`
-   `Matrices and transforms <../tutorials/math/matrices_and_transforms>`
-   [Matrix Transform
    Demo](https://godotengine.org/asset-library/asset/2787)
-   [2.5D Game Demo](https://godotengine.org/asset-library/asset/2783)

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

**IDENTITY** = `Transform2D(1, 0, 0, 1, 0, 0)`
`🔗<class_Transform2D_constant_IDENTITY>`

The identity **Transform2D**. A transform with no translation, no
rotation, and its scale being `1`. When multiplied by another
`Variant<class_Variant>` such as `Rect2<class_Rect2>` or another
**Transform2D**, no transformation occurs. This means that:

-   The `x<class_Transform2D_property_x>` points right
    (`Vector2.RIGHT<class_Vector2_constant_RIGHT>`);
-   The `y<class_Transform2D_property_y>` points up
    (`Vector2.UP<class_Vector2_constant_UP>`).

<!-- -->

    var transform = Transform2D.IDENTITY
    print("| X | Y | Origin")
    print("| %s | %s | %s" % [transform.x.x, transform.y.x, transform.origin.x])
    print("| %s | %s | %s" % [transform.x.y, transform.y.y, transform.origin.y])
    # Prints:
    # | X | Y | Origin
    # | 1 | 0 | 0
    # | 0 | 1 | 0

This is identical to creating
`Transform2D<class_Transform2D_constructor_Transform2D>` without any
parameters. This constant can be used to make your code clearer, and for
consistency with C#.

classref-constant

**FLIP\_X** = `Transform2D(-1, 0, 0, 1, 0, 0)`
`🔗<class_Transform2D_constant_FLIP_X>`

When any transform is multiplied by
`FLIP_X<class_Transform2D_constant_FLIP_X>`, it negates all components
of the `x<class_Transform2D_property_x>` axis (the X column).

When `FLIP_X<class_Transform2D_constant_FLIP_X>` is multiplied by any
basis, it negates the `Vector2.x<class_Vector2_property_x>` component of
all axes (the X row).

classref-constant

**FLIP\_Y** = `Transform2D(1, 0, 0, -1, 0, 0)`
`🔗<class_Transform2D_constant_FLIP_Y>`

When any transform is multiplied by
`FLIP_Y<class_Transform2D_constant_FLIP_Y>`, it negates all components
of the `y<class_Transform2D_property_y>` axis (the Y column).

When `FLIP_Y<class_Transform2D_constant_FLIP_Y>` is multiplied by any
basis, it negates the `Vector2.y<class_Vector2_property_y>` component of
all axes (the Y row).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Vector2<class_Vector2>` **origin** = `Vector2(0, 0)`
`🔗<class_Transform2D_property_origin>`

The translation offset of this transform, and the column `2` of the
matrix. In 2D space, this can be seen as the position.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **x** = `Vector2(1, 0)`
`🔗<class_Transform2D_property_x>`

The transform basis's X axis, and the column `0` of the matrix. Combined
with `y<class_Transform2D_property_y>`, this represents the transform's
rotation, scale, and skew.

On the identity transform, this vector points right
(`Vector2.RIGHT<class_Vector2_constant_RIGHT>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector2<class_Vector2>` **y** = `Vector2(0, 1)`
`🔗<class_Transform2D_property_y>`

The transform basis's Y axis, and the column `1` of the matrix. Combined
with `x<class_Transform2D_property_x>`, this represents the transform's
rotation, scale, and skew.

On the identity transform, this vector points up
(`Vector2.UP<class_Vector2_constant_UP>`).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constructor Descriptions

classref-constructor

`Transform2D<class_Transform2D>` **Transform2D**()
`🔗<class_Transform2D_constructor_Transform2D>`

Constructs a **Transform2D** identical to
`IDENTITY<class_Transform2D_constant_IDENTITY>`.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Transform2D<class_Transform2D>` **Transform2D**(from:
`Transform2D<class_Transform2D>`)

Constructs a **Transform2D** as a copy of the given **Transform2D**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Transform2D<class_Transform2D>` **Transform2D**(rotation:
`float<class_float>`, position: `Vector2<class_Vector2>`)

Constructs a **Transform2D** from a given angle (in radians) and
position.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Transform2D<class_Transform2D>` **Transform2D**(rotation:
`float<class_float>`, scale: `Vector2<class_Vector2>`, skew:
`float<class_float>`, position: `Vector2<class_Vector2>`)

Constructs a **Transform2D** from a given angle (in radians), scale,
skew (in radians), and position.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Transform2D<class_Transform2D>` **Transform2D**(x\_axis:
`Vector2<class_Vector2>`, y\_axis: `Vector2<class_Vector2>`, origin:
`Vector2<class_Vector2>`)

Constructs a **Transform2D** from 3 `Vector2<class_Vector2>` values
representing `x<class_Transform2D_property_x>`,
`y<class_Transform2D_property_y>`, and the
`origin<class_Transform2D_property_origin>` (the three matrix columns).

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Transform2D<class_Transform2D>` **affine\_inverse**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_affine_inverse>`

Returns the inverted version of this transform. Unlike
`inverse<class_Transform2D_method_inverse>`, this method works with
almost any basis, including non-uniform ones, but is slower. See also
`inverse<class_Transform2D_method_inverse>`.

\*\*Note:\*\* For this method to return correctly, the transform's basis
needs to have a determinant that is not exactly `0` (see
`determinant<class_Transform2D_method_determinant>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **basis\_xform**(v: `Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_basis_xform>`

Returns a copy of the `v` vector, transformed (multiplied) by the
transform basis's matrix. Unlike the multiplication operator (`*`), this
method ignores the `origin<class_Transform2D_property_origin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **basis\_xform\_inv**(v:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_basis_xform_inv>`

Returns a copy of the `v` vector, transformed (multiplied) by the
inverse transform basis's matrix (see
`inverse<class_Transform2D_method_inverse>`). This method ignores the
`origin<class_Transform2D_property_origin>`.

\*\*Note:\*\* This method assumes that this transform's basis is
*orthonormal* (see
`orthonormalized<class_Transform2D_method_orthonormalized>`). If the
basis is not orthonormal,
`transform.affine_inverse().basis_xform(vector)` should be used instead
(see `affine_inverse<class_Transform2D_method_affine_inverse>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **determinant**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_determinant>`

Returns the [determinant](https://en.wikipedia.org/wiki/Determinant) of
this transform basis's matrix. For advanced math, this number can be
used to determine a few attributes:

-   If the determinant is exactly `0`, the basis is not invertible (see
    `inverse<class_Transform2D_method_inverse>`).
-   If the determinant is a negative number, the basis represents a
    negative scale.

\*\*Note:\*\* If the basis's scale is the same for every axis, its
determinant is always that scale by the power of 2.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_origin**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_get_origin>`

Returns this transform's translation. Equivalent to
`origin<class_Transform2D_property_origin>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_rotation**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_get_rotation>`

Returns this transform's rotation (in radians). This is equivalent to
`x<class_Transform2D_property_x>`'s angle (see
`Vector2.angle<class_Vector2_method_angle>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Vector2<class_Vector2>` **get\_scale**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_get_scale>`

Returns the length of both `x<class_Transform2D_property_x>` and
`y<class_Transform2D_property_y>`, as a `Vector2<class_Vector2>`. If
this transform's basis is not skewed, this value is the scaling factor.
It is not affected by rotation.

gdscript

var my\_transform = Transform2D(  
Vector2(2, 0), Vector2(0, 4), Vector2(0, 0)

) \# Rotating the Transform2D in any way preserves its scale.
my\_transform = my\_transform.rotated(TAU / 2)

print(my\_transform.get\_scale()) \# Prints (2, 4).

csharp

var myTransform = new Transform2D(  
Vector3(2.0f, 0.0f), Vector3(0.0f, 4.0f), Vector3(0.0f, 0.0f)

); // Rotating the Transform2D in any way preserves its scale.
myTransform = myTransform.Rotated(Mathf.Tau / 2.0f);

GD.Print(myTransform.GetScale()); // Prints (2, 4, 8).

\*\*Note:\*\* If the value returned by
`determinant<class_Transform2D_method_determinant>` is negative, the
scale is also negative.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_skew**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_get_skew>`

Returns this transform's skew (in radians).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **interpolate\_with**(xform:
`Transform2D<class_Transform2D>`, weight: `float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_interpolate_with>`

Returns the result of the linear interpolation between this transform
and `xform` by the given `weight`.

The `weight` should be between `0.0` and `1.0` (inclusive). Values
outside this range are allowed and can be used to perform
*extrapolation* instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **inverse**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_inverse>`

Returns the [inverted version of this
transform](https://en.wikipedia.org/wiki/Invertible_matrix).

\*\*Note:\*\* For this method to return correctly, the transform's basis
needs to be *orthonormal* (see
`orthonormalized<class_Transform2D_method_orthonormalized>`). That
means, the basis should only represent a rotation. If it does not, use
`affine_inverse<class_Transform2D_method_affine_inverse>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_conformal**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_is_conformal>`

Returns `true` if this transform's basis is conformal. A conformal basis
is both *orthogonal* (the axes are perpendicular to each other) and
*uniform* (the axes share the same length). This method can be
especially useful during physics calculations.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_equal\_approx**(xform:
`Transform2D<class_Transform2D>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_is_equal_approx>`

Returns `true` if this transform and `xform` are approximately equal, by
running
`@GlobalScope.is_equal_approx<class_@GlobalScope_method_is_equal_approx>`
on each component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_finite**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_is_finite>`

Returns `true` if this transform is finite, by calling
`@GlobalScope.is_finite<class_@GlobalScope_method_is_finite>` on each
component.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **looking\_at**(target:
`Vector2<class_Vector2>` = Vector2(0, 0))
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_looking_at>`

Returns a copy of the transform rotated such that the rotated X-axis
points towards the `target` position, in global space.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **orthonormalized**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_orthonormalized>`

Returns a copy of this transform with its basis orthonormalized. An
orthonormal basis is both *orthogonal* (the axes are perpendicular to
each other) and *normalized* (the axes have a length of `1`), which also
means it can only represent rotation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **rotated**(angle:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_rotated>`

Returns a copy of the transform rotated by the given `angle` (in
radians).

This method is an optimized version of multiplying the given transform
`X` with a corresponding rotation transform `R` from the left, i.e.,
`R * X`.

This can be seen as transforming with respect to the global/parent
frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **rotated\_local**(angle:
`float<class_float>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_rotated_local>`

Returns a copy of the transform rotated by the given `angle` (in
radians).

This method is an optimized version of multiplying the given transform
`X` with a corresponding rotation transform `R` from the right, i.e.,
`X * R`.

This can be seen as transforming with respect to the local frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **scaled**(scale:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_scaled>`

Returns a copy of the transform scaled by the given `scale` factor.

This method is an optimized version of multiplying the given transform
`X` with a corresponding scaling transform `S` from the left, i.e.,
`S * X`.

This can be seen as transforming with respect to the global/parent
frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **scaled\_local**(scale:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_scaled_local>`

Returns a copy of the transform scaled by the given `scale` factor.

This method is an optimized version of multiplying the given transform
`X` with a corresponding scaling transform `S` from the right, i.e.,
`X * S`.

This can be seen as transforming with respect to the local frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **translated**(offset:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_translated>`

Returns a copy of the transform translated by the given `offset`.

This method is an optimized version of multiplying the given transform
`X` with a corresponding translation transform `T` from the left, i.e.,
`T * X`.

This can be seen as transforming with respect to the global/parent
frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Transform2D<class_Transform2D>` **translated\_local**(offset:
`Vector2<class_Vector2>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Transform2D_method_translated_local>`

Returns a copy of the transform translated by the given `offset`.

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
`Transform2D<class_Transform2D>`)
`🔗<class_Transform2D_operator_neq_Transform2D>`

Returns `true` if the components of both transforms are not equal.

\*\*Note:\*\* Due to floating-point precision errors, consider using
`is_equal_approx<class_Transform2D_method_is_equal_approx>` instead,
which is more reliable.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`PackedVector2Array<class_PackedVector2Array>` **operator**\*(right:
`PackedVector2Array<class_PackedVector2Array>`)
`🔗<class_Transform2D_operator_mul_PackedVector2Array>`

Transforms (multiplies) every `Vector2<class_Vector2>` element of the
given `PackedVector2Array<class_PackedVector2Array>` by this
transformation matrix.

On larger arrays, this operation is much faster than transforming each
`Vector2<class_Vector2>` individually.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Rect2<class_Rect2>` **operator**\*(right: `Rect2<class_Rect2>`)
`🔗<class_Transform2D_operator_mul_Rect2>`

Transforms (multiplies) the `Rect2<class_Rect2>` by this transformation
matrix.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Transform2D<class_Transform2D>` **operator**\*(right:
`Transform2D<class_Transform2D>`)
`🔗<class_Transform2D_operator_mul_Transform2D>`

Transforms (multiplies) this transform by the `right` transform.

This is the operation performed between parent and child
`CanvasItem<class_CanvasItem>` nodes.

\*\*Note:\*\* If you need to only modify one attribute of this
transform, consider using one of the following methods, instead:

-   For translation, see
    `translated<class_Transform2D_method_translated>` or
    `translated_local<class_Transform2D_method_translated_local>`.
-   For rotation, see `rotated<class_Transform2D_method_rotated>` or
    `rotated_local<class_Transform2D_method_rotated_local>`.
-   For scale, see `scaled<class_Transform2D_method_scaled>` or
    `scaled_local<class_Transform2D_method_scaled_local>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator**\*(right: `Vector2<class_Vector2>`)
`🔗<class_Transform2D_operator_mul_Vector2>`

Transforms (multiplies) the `Vector2<class_Vector2>` by this
transformation matrix.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Transform2D<class_Transform2D>` **operator**\*(right:
`float<class_float>`) `🔗<class_Transform2D_operator_mul_float>`

Multiplies all components of the **Transform2D** by the given
`float<class_float>`, including the
`origin<class_Transform2D_property_origin>`. This affects the
transform's scale uniformly.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Transform2D<class_Transform2D>` **operator**\*(right: `int<class_int>`)
`🔗<class_Transform2D_operator_mul_int>`

Multiplies all components of the **Transform2D** by the given
`int<class_int>`, including the
`origin<class_Transform2D_property_origin>`. This affects the
transform's scale uniformly.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Transform2D<class_Transform2D>` **operator /**(right:
`float<class_float>`) `🔗<class_Transform2D_operator_div_float>`

Divides all components of the **Transform2D** by the given
`float<class_float>`, including the
`origin<class_Transform2D_property_origin>`. This affects the
transform's scale uniformly.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Transform2D<class_Transform2D>` **operator /**(right: `int<class_int>`)
`🔗<class_Transform2D_operator_div_int>`

Divides all components of the **Transform2D** by the given
`int<class_int>`, including the
`origin<class_Transform2D_property_origin>`. This affects the
transform's scale uniformly.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right:
`Transform2D<class_Transform2D>`)
`🔗<class_Transform2D_operator_eq_Transform2D>`

Returns `true` if the components of both transforms are exactly equal.

\*\*Note:\*\* Due to floating-point precision errors, consider using
`is_equal_approx<class_Transform2D_method_is_equal_approx>` instead,
which is more reliable.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Vector2<class_Vector2>` **operator \[\]**(index: `int<class_int>`)
`🔗<class_Transform2D_operator_idx_int>`

Accesses each axis (column) of this transform by their index. Index `0`
is the same as `x<class_Transform2D_property_x>`, index `1` is the same
as `y<class_Transform2D_property_y>`, and index `2` is the same as
`origin<class_Transform2D_property_origin>`.
