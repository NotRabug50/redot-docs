# C# collections

The .NET base class library contains multiple collection types that can
be used to store and manipulate data. Godot also provide some collection
types that are tightly integrated with the rest of the engine.

## Choose a collection

The main difference between the [.NET
collections](https://learn.microsoft.com/en-us/dotnet/standard/collections/)
and the Godot collections is that the .NET collections are implemented
in C# while the Godot collections are implemented in C++ and the Godot
C# API is a wrapper over it, this is an important distinction since it
means every operation on a Godot collection requires marshaling which
can be expensive especially inside a loop.

Due to the performance implications, using Godot collections is only
recommended when absolutely necessary (such as interacting with the
Godot API). Godot only understands its own collection types, so it's
required to use them when talking to the engine.

If you have a collection of elements that don't need to be passed to a
Godot API, using a .NET collection would be more performant.

Tip

It's also possible to convert between .NET collections and Godot
collections. The Godot collections contain constructors from generic
.NET collection interfaces that copy their elements, and the Godot
collections can be used with the
[LINQ](https://learn.microsoft.com/en-us/dotnet/standard/linq) `ToList`,
`ToArray` and `ToDictionary` methods. But keep in mind this conversion
requires marshaling every element in the collection and copies it to a
new collection so it can be expensive.

Despite this, the Godot collections are optimized to try and avoid
unnecessary marshaling, so methods like `Sort` or `Reverse` are
implemented with a single interop call and don't need to marshal every
element. Keep an eye out for generic APIs that take collection
interfaces like
[LINQ](https://learn.microsoft.com/en-us/dotnet/standard/linq) because
every method requires iterating the collection and, therefore,
marshaling every element. Prefer using the instance methods of the Godot
collections when possible.

To choose which collection type to use for each situation, consider the
following questions:

-   Does your collection need to interact with the Godot engine? (e.g.:
    the type of an exported property, calling a Godot method).

    > -   If yes, since Godot only supports
    >     `c_sharp_variant_compatible_types`, use a Godot collection.
    > -   If not, consider [choosing an appropriate .NET
    >     collection](https://learn.microsoft.com/en-us/dotnet/standard/collections/selecting-a-collection-class).

-   Do you need a Godot collection that represents a list or sequential
    set of data?

    > -   Godot `arrays <doc_c_sharp_collections_array>` are similar to
    >     the C# collection `List<T>`.
    > -   Godot `packed arrays <doc_c_sharp_collections_packedarray>`
    >     are more memory-efficient arrays, in C# use one of the
    >     supported `System.Array` types.

-   Do you need a Godot collection that maps a set of keys to a set of
    values?

    > -   Godot `dictionaries <doc_c_sharp_collections_dictionary>`
    >     store pairs of keys and values and allow easy access to the
    >     values by their associated key.

## Godot collections

### PackedArray

Godot packed arrays are implemented as an array of a specific type,
allowing it to be more tightly packed as each element has the size of
the specific type, not `Variant`.

In C#, packed arrays are replaced by `System.Array`:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
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
<td><code>Vector2[]</code></td>
</tr>
<tr>
<td><code>PackedVector3Array</code></td>
<td><code>Vector3[]</code></td>
</tr>
<tr>
<td><code>PackedVector4Array</code></td>
<td><code>Vector4[]</code></td>
</tr>
<tr>
<td><code>PackedColorArray</code></td>
<td><code>Color[]</code></td>
</tr>
</tbody>
</table>

Other C# arrays are not supported by the Godot C# API since a packed
array equivalent does not exist. See the list of
`c_sharp_variant_compatible_types`.

### Array

Godot arrays are implemented as an array of `Variant` and can contain
several elements of any type. In C#, the equivalent type is
`Godot.Collections.Array`.

The generic `Godot.Collections.Array<T>` type allows restricting the
element type to a
`Variant-compatible type <c_sharp_variant_compatible_types>`.

An untyped `Godot.Collections.Array` can be converted to a typed array
using the `Godot.Collections.Array<T>(Godot.Collections.Array)`
constructor.

Note

Despite the name, Godot arrays are more similar to the C# collection
`List<T>` than `System.Array`. Their size is not fixed and can grow or
shrink as elements are added/removed from the collection.

List of Godot's Array methods and their equivalent in C#:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td>all</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.all">System.Linq.Enumerable.All</a></td>
</tr>
<tr>
<td>any</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.any">System.Linq.Enumerable.Any</a></td>
</tr>
<tr>
<td>append</td>
<td>Add</td>
</tr>
<tr>
<td>append_array</td>
<td>AddRange</td>
</tr>
<tr>
<td>assign</td>
<td>Clear and AddRange</td>
</tr>
<tr>
<td>back</td>
<td><code>Array[^1]</code> or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.last">System.Linq.Enumerable.Last</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.lastordefault">System.Linq.Enumerable.LastOrDefault</a></td>
</tr>
<tr>
<td>bsearch</td>
<td>BinarySearch</td>
</tr>
<tr>
<td>bsearch_custom</td>
<td>N/A</td>
</tr>
<tr>
<td>clear</td>
<td>Clear</td>
</tr>
<tr>
<td>count</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.count">System.Linq.Enumerable.Count</a></td>
</tr>
<tr>
<td>duplicate</td>
<td>Duplicate</td>
</tr>
<tr>
<td>erase</td>
<td>Remove</td>
</tr>
<tr>
<td>fill</td>
<td>Fill</td>
</tr>
<tr>
<td>filter</td>
<td>Use <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.where">System.Linq.Enumerable.Where</a></td>
</tr>
<tr>
<td>find</td>
<td>IndexOf</td>
</tr>
<tr>
<td>front</td>
<td><code>Array[0]</code> or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.first">System.Linq.Enumerable.First</a>
or <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.firstordefault">System.Linq.Enumerable.FirstOrDefault</a></td>
</tr>
<tr>
<td>get_typed_builtin</td>
<td>N/A</td>
</tr>
<tr>
<td>get_typed_class_name</td>
<td>N/A</td>
</tr>
<tr>
<td>get_typed_script</td>
<td>N/A</td>
</tr>
<tr>
<td>has</td>
<td>Contains</td>
</tr>
<tr>
<td>hash</td>
<td>GD.Hash</td>
</tr>
<tr>
<td>insert</td>
<td>Insert</td>
</tr>
<tr>
<td>is_empty</td>
<td>Use <code>Count == 0</code></td>
</tr>
<tr>
<td>is_read_only</td>
<td>IsReadOnly</td>
</tr>
<tr>
<td>is_same_typed</td>
<td>N/A</td>
</tr>
<tr>
<td>is_typed</td>
<td>N/A</td>
</tr>
<tr>
<td>make_read_only</td>
<td>MakeReadOnly</td>
</tr>
<tr>
<td>map</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.select">System.Linq.Enumerable.Select</a></td>
</tr>
<tr>
<td>max</td>
<td>Max</td>
</tr>
<tr>
<td>min</td>
<td>Min</td>
</tr>
<tr>
<td>pick_random</td>
<td>PickRandom (Consider using <a
href="https://learn.microsoft.com/en-us/dotnet/api/system.random">System.Random</a>)</td>
</tr>
<tr>
<td>pop_at</td>
<td><code>Array[i]</code> with <code>RemoveAt(i)</code></td>
</tr>
<tr>
<td>pop_back</td>
<td><code>Array[^1]</code> with <code>RemoveAt(Count - 1)</code></td>
</tr>
<tr>
<td>pop_front</td>
<td><code>Array[0]</code> with <code>RemoveAt(0)</code></td>
</tr>
<tr>
<td>push_back</td>
<td><code>Insert(Count, item)</code></td>
</tr>
<tr>
<td>push_front</td>
<td><code>Insert(0, item)</code></td>
</tr>
<tr>
<td>reduce</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.aggregate">System.Linq.Enumerable.Aggregate</a></td>
</tr>
<tr>
<td>remove_at</td>
<td>RemoveAt</td>
</tr>
<tr>
<td>resize</td>
<td>Resize</td>
</tr>
<tr>
<td>reverse</td>
<td>Reverse</td>
</tr>
<tr>
<td>rfind</td>
<td>LastIndexOf</td>
</tr>
<tr>
<td>shuffle</td>
<td>Shuffle</td>
</tr>
<tr>
<td>size</td>
<td>Count</td>
</tr>
<tr>
<td>slice</td>
<td>Slice</td>
</tr>
<tr>
<td>sort</td>
<td>Sort</td>
</tr>
<tr>
<td>sort_custom</td>
<td><a
href="https://learn.microsoft.com/en-us/dotnet/api/system.linq.enumerable.orderby">System.Linq.Enumerable.OrderBy</a></td>
</tr>
<tr>
<td>operator !=</td>
<td>!RecursiveEqual</td>
</tr>
<tr>
<td>operator +</td>
<td>operator +</td>
</tr>
<tr>
<td>operator &lt;</td>
<td>N/A</td>
</tr>
<tr>
<td>operator &lt;=</td>
<td>N/A</td>
</tr>
<tr>
<td>operator ==</td>
<td>RecursiveEqual</td>
</tr>
<tr>
<td>operator &gt;</td>
<td>N/A</td>
</tr>
<tr>
<td>operator &gt;=</td>
<td>N/A</td>
</tr>
<tr>
<td>operator []</td>
<td>Array[int] indexer</td>
</tr>
</tbody>
</table>

### Dictionary

Godot dictionaries are implemented as a dictionary with `Variant` keys
and values. In C#, the equivalent type is
`Godot.Collections.Dictionary`.

The generic `Godot.Collections.Dictionary<TKey, TValue>` type allows
restricting the key and value types to a
`Variant-compatible type <c_sharp_variant_compatible_types>`.

An untyped `Godot.Collections.Dictionary` can be converted to a typed
dictionary using the
`Godot.Collections.Dictionary<TKey, TValue>(Godot.Collections.Dictionary)`
constructor.

Tip

If you need a dictionary where the key is typed but not the value, use
`Variant` as the `TValue` generic parameter of the typed dictionary.

    // The keys must be string, but the values can be any Variant-compatible type.
    var dictionary = new Godot.Collections.Dictionary<string, Variant>();

List of Godot's Dictionary methods and their equivalent in C#:

<table>
<thead>
<tr>
<th>GDScript</th>
<th>C#</th>
</tr>
</thead>
<tbody>
<tr>
<td>clear</td>
<td>Clear</td>
</tr>
<tr>
<td>duplicate</td>
<td>Duplicate</td>
</tr>
<tr>
<td>erase</td>
<td>Remove</td>
</tr>
<tr>
<td>find_key</td>
<td>N/A</td>
</tr>
<tr>
<td>get</td>
<td>Dictionary[Variant] indexer or TryGetValue</td>
</tr>
<tr>
<td>has</td>
<td>ContainsKey</td>
</tr>
<tr>
<td>has_all</td>
<td>N/A</td>
</tr>
<tr>
<td>hash</td>
<td>GD.Hash</td>
</tr>
<tr>
<td>is_empty</td>
<td>Use <code>Count == 0</code></td>
</tr>
<tr>
<td>is_read_only</td>
<td>IsReadOnly</td>
</tr>
<tr>
<td>keys</td>
<td>Keys</td>
</tr>
<tr>
<td>make_read_only</td>
<td>MakeReadOnly</td>
</tr>
<tr>
<td>merge</td>
<td>Merge</td>
</tr>
<tr>
<td>size</td>
<td>Count</td>
</tr>
<tr>
<td>values</td>
<td>Values</td>
</tr>
<tr>
<td>operator !=</td>
<td>!RecursiveEqual</td>
</tr>
<tr>
<td>operator ==</td>
<td>RecursiveEqual</td>
</tr>
<tr>
<td>operator []</td>
<td>Dictionary[Variant] indexer, Add or TryGetValue</td>
</tr>
</tbody>
</table>
