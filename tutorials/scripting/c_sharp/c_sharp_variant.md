# C# Variant

For a detailed explanation of Variant in general, see the
`Variant <class_Variant>` documentation page.

`Godot.Variant` is used to represent Godot's native
`Variant <class_Variant>` type. Any
`Variant-compatible type <c_sharp_variant_compatible_types>` can be
converted from/to it. We recommend avoiding `Godot.Variant` unless it is
necessary to interact with untyped engine APIs. Take advantage of C#'s
type safety when possible.

Converting from a Variant-compatible C# type to `Godot.Variant` can be
done using implicit conversions. There are also `CreateFrom` method
overloads and the generic `Variant.From<T>` methods. Only the syntax is
different: the behavior is the same.

    int x = 42;
    Variant numberVariant = x;
    Variant helloVariant = "Hello, World!";

    Variant numberVariant2 = Variant.CreateFrom(x);
    Variant numberVariant3 = Variant.From(x);

Implicit conversions to `Godot.Variant` make passing variants as method
arguments very convenient. For example, the third argument of
`tween_property<class_Tween_method_tween_property>` specifying the final
color of the tween is a `Godot.Variant`.

    Tween tween = CreateTween();
    tween.TweenProperty(GetNode("Sprite"), "modulate", Colors.Red, 1.0f);

Converting from `Godot.Variant` to a C# type can be done using explicit
conversions. There are also `Variant.As{TYPE}` methods and the generic
`Variant.As<T>` method. All of these behave the same.

    int number = (int)numberVariant;
    string hello = (string)helloVariant;

    int number2 = numberVariant.As<int>();
    int number3 = numberVariant.AsInt32();

Note

The `Variant.As{TYPE}` methods are typically named after C# types
(`Int32`), not C# keywords (`int`).

If the Variant type doesn't match the conversion target type, the
consequences vary depending on the source and target values.

-   The conversion may examine the value and return a similar but
    potentially unexpected value of the target type. For example, the
    string `"42a"` may be converted to the integer `42`.
-   The default value of the target type may be returned.
-   An empty array may be returned.
-   An exception may be thrown.

Converting to the correct type avoids complicated behavior and should be
preferred.

The `Variant.Obj` property returns a C# `object` with the correct value
for any variant. This may be useful when the type of Variant is
completely unknown. However, when possible, prefer more specific
conversions. `Variant.Obj` evaluates a `switch` on `Variant.VariantType`
and it may not be necessary. Also, if the result is a value type, it is
boxed.

For example, if the potential for `Variant.As<MyNode>()` to throw an
invalid cast exception isn't acceptable, consider using a
`Variant.As<GodotObject>() is MyNode n` type pattern instead.

Note

Since the Variant type in C# is a struct, it can't be null. To create a
"null" Variant, use the `default` keyword or the `Godot.Variant`
parameterless constructor.

## Variant-compatible types

A Variant-compatible type can be converted to and from a
`Godot.Variant`. These C# types are Variant-compatible:

-   All the [built-in value
    types](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/built-in-types-table),
    except `decimal`, `nint` and `nuint`.
-   `string`.
-   Classes derived from `GodotObject <class_Object>`.
-   Collections types defined in the `Godot.Collections` namespace.

Full list of Variant types and their equivalent C# type:

<table>
<thead>
<tr>
<th>Variant.Type</th>
<th>C# Type</th>
</tr>
</thead>
<tbody>
<tr>
<td><code>Nil</code></td>
<td><code>null</code> (Not a type)</td>
</tr>
<tr>
<td><code>Bool</code></td>
<td><code>bool</code></td>
</tr>
<tr>
<td><code>Int</code></td>
<td><code>long</code> (Godot stores 64-bit integers in Variant)</td>
</tr>
<tr>
<td><code>Float</code></td>
<td><code>double</code> (Godot stores 64-bit floats in Variant)</td>
</tr>
<tr>
<td><code>String</code></td>
<td><code>string</code></td>
</tr>
<tr>
<td><code>Vector2</code></td>
<td><code>Godot.Vector2</code></td>
</tr>
<tr>
<td><code>Vector2I</code></td>
<td><code>Godot.Vector2I</code></td>
</tr>
<tr>
<td><code>Rect2</code></td>
<td><code>Godot.Rect2</code></td>
</tr>
<tr>
<td><code>Rect2I</code></td>
<td><code>Godot.Rect2I</code></td>
</tr>
<tr>
<td><code>Vector3</code></td>
<td><code>Godot.Vector3</code></td>
</tr>
<tr>
<td><code>Vector3I</code></td>
<td><code>Godot.Vector3I</code></td>
</tr>
<tr>
<td><code>Transform2D</code></td>
<td><code>Godot.Transform2D</code></td>
</tr>
<tr>
<td><code>Vector4</code></td>
<td><code>Godot.Vector4</code></td>
</tr>
<tr>
<td><code>Vector4I</code></td>
<td><code>Godot.Vector4I</code></td>
</tr>
<tr>
<td><code>Plane</code></td>
<td><code>Godot.Plane</code></td>
</tr>
<tr>
<td><code>Quaternion</code></td>
<td><code>Godot.Quaternion</code></td>
</tr>
<tr>
<td><code>Aabb</code></td>
<td><code>Godot.Aabb</code></td>
</tr>
<tr>
<td><code>Basis</code></td>
<td><code>Godot.Basis</code></td>
</tr>
<tr>
<td><code>Transform3D</code></td>
<td><code>Godot.Transform3D</code></td>
</tr>
<tr>
<td><code>Projection</code></td>
<td><code>Godot.Projection</code></td>
</tr>
<tr>
<td><code>Color</code></td>
<td><code>Godot.Color</code></td>
</tr>
<tr>
<td><code>StringName</code></td>
<td><code>Godot.StringName</code></td>
</tr>
<tr>
<td><code>NodePath</code></td>
<td><code>Godot.NodePath</code></td>
</tr>
<tr>
<td><code>Rid</code></td>
<td><code>Godot.Rid</code></td>
</tr>
<tr>
<td><code>Object</code></td>
<td><code>Godot.GodotObject</code> or any derived type.</td>
</tr>
<tr>
<td><code>Callable</code></td>
<td><code>Godot.Callable</code></td>
</tr>
<tr>
<td><code>Signal</code></td>
<td><code>Godot.Signal</code></td>
</tr>
<tr>
<td><code>Dictionary</code></td>
<td><code>Godot.Collections.Dictionary</code></td>
</tr>
<tr>
<td><code>Array</code></td>
<td><code>Godot.Collections.Array</code></td>
</tr>
<tr>
<td><code>PackedByteArray</code></td>
<td><code>byte[]</code></td>
</tr>
<tr>
<td><code>PackedInt32Array</code></td>
<td><code>int[]</code></td>
</tr>
<tr>
<td><code>PackedInt64Array</code></td>
<td><code>long[]</code></td>
</tr>
<tr>
<td><code>PackedFloat32Array</code></td>
<td><code>float[]</code></td>
</tr>
<tr>
<td><code>PackedFloat64Array</code></td>
<td><code>double[]</code></td>
</tr>
<tr>
<td><code>PackedStringArray</code></td>
<td><code>string[]</code></td>
</tr>
<tr>
<td><code>PackedVector2Array</code></td>
<td><code>Godot.Vector2[]</code></td>
</tr>
<tr>
<td><code>PackedVector3Array</code></td>
<td><code>Godot.Vector3[]</code></td>
</tr>
<tr>
<td><code>PackedVector4Array</code></td>
<td><code>Godot.Vector4[]</code></td>
</tr>
<tr>
<td><code>PackedColorArray</code></td>
<td><code>Godot.Color[]</code></td>
</tr>
</tbody>
</table>

Warning

Godot uses 64-bit integers and floats in Variant. Smaller integer and
float types such as `int`, `short` and `float` are supported since they
can fit in the bigger type. Be aware that when a conversion is
performed, using the wrong type will result in potential precision loss.

Warning

Enums are supported by `Godot.Variant` since their underlying type is an
integer type which are all compatible. However, implicit conversions
don't exist, enums must be manually converted to their underlying
integer type before they can converted to/from `Godot.Variant` or use
the generic `Variant.As<T>` and `Variant.From<T>` methods to convert
them.

    enum MyEnum { A, B, C }

    Variant variant1 = (int)MyEnum.A;
    MyEnum enum1 = (MyEnum)(int)variant1;

    Variant variant2 = Variant.From(MyEnum.A);
    MyEnum enum2 = variant2.As<MyEnum>();

## Using Variant in a generic context

When using generics, you may be interested in restricting the generic
`T` type to be only one of the Variant-compatible types. This can be
achieved using the `[MustBeVariant]` attribute.

    public void MethodThatOnlySupportsVariants<[MustBeVariant] T>(T onlyVariant)
    {
        // Do something with the Variant-compatible value.
    }

Combined with the generic `Variant.From<T>` allows you to obtain an
instance of `Godot.Variant` from an instance of a generic `T` type. Then
it can be used in any API that only supports the `Godot.Variant` struct.

    public void Method1<[MustBeVariant] T>(T variantCompatible)
    {
        Variant variant = Variant.From(variantCompatible);
        Method2(variant);
    }

    public void Method2(Variant variant)
    {
        // Do something with variant.
    }

In order to invoke a method with a generic parameter annotated with the
`[MustBeVariant]` attribute, the value must be a Variant-compatible type
or a generic `T` type annotated with the `[MustBeVariant]` attribute as
well.

    public class ObjectDerivedClass : GodotObject { }

    public class NonObjectDerivedClass { }

    public void Main<[MustBeVariant] T1, T2>(T1 someGeneric1, T2 someGeneric2)
    {
        MyMethod(42); // Works because `int` is a Variant-compatible type.
        MyMethod(new ObjectDerivedClass()); // Works because any type that derives from `GodotObject` is a Variant-compatible type.
        MyMethod(new NonObjectDerivedClass()); // Does NOT work because the type is not Variant-compatible.
        MyMethod(someGeneric1); // Works because `T1` is annotated with the `[MustBeVariant]` attribute.
        MyMethod(someGeneric2); // Does NOT work because `T2` is NOT annotated with the `[MustBeVariant]` attribute.
    }

    public void MyMethod<[MustBeVariant] T>(T variant)
    {
        // Do something with variant.
    }
