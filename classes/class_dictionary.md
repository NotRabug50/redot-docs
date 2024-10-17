github\_url  
hide

# Dictionary

A built-in data structure that holds key-value pairs.

classref-introduction-group

## Description

Dictionaries are associative containers that contain values referenced
by unique keys. Dictionaries will preserve the insertion order when
adding new entries. In other programming languages, this data structure
is often referred to as a hash map or an associative array.

You can define a dictionary by placing a comma-separated list of
`key: value` pairs inside curly braces `{}`.

Creating a dictionary:

gdscript

var my\_dict = {} \# Creates an empty dictionary.

var dict\_variable\_key = "Another key name" var dict\_variable\_value =
"value2" var another\_dict = { "Some key name": "value1",
dict\_variable\_key: dict\_variable\_value, }

var points\_dict = {"White": 50, "Yellow": 75, "Orange": 100}

\# Alternative Lua-style syntax. \# Doesn't require quotes around keys,
but only string constants can be used as key names. \# Additionally, key
names must start with a letter or an underscore. \# Here,
<span class="title-ref">some\_key</span> is a string literal, not a
variable! another\_dict = { some\_key = 42, }

csharp

var myDict = new Godot.Collections.Dictionary(); // Creates an empty
dictionary. var pointsDict = new Godot.Collections.Dictionary {
{"White", 50}, {"Yellow", 75}, {"Orange", 100} };

You can access a dictionary's value by referencing its corresponding
key. In the above example, `points_dict["White"]` will return `50`. You
can also write `points_dict.White`, which is equivalent. However, you'll
have to use the bracket syntax if the key you're accessing the
dictionary with isn't a fixed string (such as a number or variable).

gdscript

@export\_enum("White", "Yellow", "Orange") var my\_color: String var
points\_dict = {"White": 50, "Yellow": 75, "Orange": 100} func
\_ready(): \# We can't use dot syntax here as
<span class="title-ref">my\_color</span> is a variable. var points =
points\_dict\[my\_color\]

csharp

\[Export(PropertyHint.Enum, "White,Yellow,Orange")\] public string
MyColor { get; set; } private Godot.Collections.Dictionary \_pointsDict
= new Godot.Collections.Dictionary { {"White", 50}, {"Yellow", 75},
{"Orange", 100} };

public override void \_Ready() { int points =
(int)\_pointsDict\[MyColor\]; }

In the above code, `points` will be assigned the value that is paired
with the appropriate color selected in `my_color`.

Dictionaries can contain more complex data:

gdscript

var my\_dict = {  
"First Array": \[1, 2, 3, 4\] \# Assigns an Array to a String key.

}

csharp

var myDict = new Godot.Collections.Dictionary { {"First Array", new
Godot.Collections.Array{1, 2, 3, 4}} };

To add a key to an existing dictionary, access it like an existing key
and assign to it:

gdscript

var points\_dict = {"White": 50, "Yellow": 75, "Orange": 100}
points\_dict\["Blue"\] = 150 \# Add "Blue" as a key and assign 150 as
its value.

csharp

var pointsDict = new Godot.Collections.Dictionary { {"White", 50},
{"Yellow", 75}, {"Orange", 100} }; pointsDict\["Blue"\] = 150; // Add
"Blue" as a key and assign 150 as its value.

Finally, dictionaries can contain different types of keys and values in
the same dictionary:

gdscript

\# This is a valid dictionary. \# To access the string "Nested value"
below, use <span class="title-ref">my\_dict.sub\_dict.sub\_key</span> or
<span class="title-ref">my\_dict\["sub\_dict"\]\["sub\_key"\]</span>. \#
Indexing styles can be mixed and matched depending on your needs. var
my\_dict = { "String Key": 5, 4: \[1, 2, 3\], 7: "Hello", "sub\_dict":
{"sub\_key": "Nested value"}, }

csharp

// This is a valid dictionary. // To access the string "Nested value"
below, use
<span class="title-ref">((Godot.Collections.Dictionary)myDict\["sub\_dict"\])\["sub\_key"\]</span>.
var myDict = new Godot.Collections.Dictionary { {"String Key", 5}, {4,
new Godot.Collections.Array{1,2,3}}, {7, "Hello"}, {"sub\_dict", new
Godot.Collections.Dictionary{{"sub\_key", "Nested value"}}} };

The keys of a dictionary can be iterated with the `for` keyword:

gdscript

var groceries = {"Orange": 20, "Apple": 2, "Banana": 4} for fruit in
groceries: var amount = groceries\[fruit\]

csharp

var groceries = new Godot.Collections.Dictionary{{"Orange", 20},
{"Apple", 2}, {"Banana", 4}}; foreach (var (fruit, amount) in groceries)
{ // <span class="title-ref">fruit</span> is the key,
<span class="title-ref">amount</span> is the value. }

\*\*Note:\*\* Dictionaries are always passed by reference. To get a copy
of a dictionary which can be modified independently of the original
dictionary, use `duplicate<class_Dictionary_method_duplicate>`.

\*\*Note:\*\* Erasing elements while iterating over dictionaries is
**not** supported and will result in unpredictable behavior.

Note

There are notable differences when using this API with C#. See
`doc_c_sharp_differences` for more information.

classref-introduction-group

## Tutorials

-   [GDScript basics:
    Dictionary](../tutorials/scripting/gdscript/gdscript_basics.html#dictionary)
-   [3D Voxel Demo](https://godotengine.org/asset-library/asset/2755)
-   [Operating System Testing
    Demo](https://godotengine.org/asset-library/asset/2789)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constructor Descriptions

classref-constructor

`Dictionary<class_Dictionary>` **Dictionary**()
`🔗<class_Dictionary_constructor_Dictionary>`

Constructs an empty **Dictionary**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Dictionary<class_Dictionary>` **Dictionary**(base:
`Dictionary<class_Dictionary>`, key\_type: `int<class_int>`,
key\_class\_name: `StringName<class_StringName>`, key\_script:
`Variant<class_Variant>`, value\_type: `int<class_int>`,
value\_class\_name: `StringName<class_StringName>`, value\_script:
`Variant<class_Variant>`)

Creates a typed dictionary from the `base` dictionary. A typed
dictionary can only contain keys and values of the given types, or that
inherit from the given classes, as described by this constructor's
parameters.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`Dictionary<class_Dictionary>` **Dictionary**(from:
`Dictionary<class_Dictionary>`)

Returns the same dictionary as `from`. If you need a copy of the
dictionary, use `duplicate<class_Dictionary_method_duplicate>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **assign**(dictionary:
`Dictionary<class_Dictionary>`) `🔗<class_Dictionary_method_assign>`

Assigns elements of another `dictionary` into the dictionary. Resizes
the dictionary to match `dictionary`. Performs type conversions if the
dictionary is typed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear**()
`🔗<class_Dictionary_method_clear>`

Clears the dictionary, removing all entries from it.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **duplicate**(deep: `bool<class_bool>` =
false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_duplicate>`

Creates and returns a new copy of the dictionary. If `deep` is `true`,
inner **Dictionary** and `Array<class_Array>` keys and values are also
copied, recursively.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **erase**(key: `Variant<class_Variant>`)
`🔗<class_Dictionary_method_erase>`

Removes the dictionary entry by key, if it exists. Returns `true` if the
given `key` existed in the dictionary, otherwise `false`.

\*\*Note:\*\* Do not erase entries while iterating over the dictionary.
You can iterate over the `keys<class_Dictionary_method_keys>` array
instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **find\_key**(value: `Variant<class_Variant>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_find_key>`

Finds and returns the first key whose associated value is equal to
`value`, or `null` if it is not found.

\*\*Note:\*\* `null` is also a valid key. If inside the dictionary,
`find_key<class_Dictionary_method_find_key>` may give misleading
results.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get**(key: `Variant<class_Variant>`, default:
`Variant<class_Variant>` = null)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_get>`

Returns the corresponding value for the given `key` in the dictionary.
If the `key` does not exist, returns `default`, or `null` if the
parameter is omitted.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_or\_add**(key: `Variant<class_Variant>`,
default: `Variant<class_Variant>` = null)
`🔗<class_Dictionary_method_get_or_add>`

Gets a value and ensures the key is set. If the `key` exists in the
dictionary, this behaves like `get<class_Dictionary_method_get>`.
Otherwise, the `default` value is inserted into the dictionary and
returned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_typed\_key\_builtin**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_get_typed_key_builtin>`

Returns the built-in `Variant<class_Variant>` type of the typed
dictionary's keys as a `Variant.Type<enum_@GlobalScope_Variant.Type>`
constant. If the keys are not typed, returns
`@GlobalScope.TYPE_NIL<class_@GlobalScope_constant_TYPE_NIL>`. See also
`is_typed_key<class_Dictionary_method_is_typed_key>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_typed\_key\_class\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_get_typed_key_class_name>`

Returns the **built-in** class name of the typed dictionary's keys, if
the built-in `Variant<class_Variant>` type is
`@GlobalScope.TYPE_OBJECT<class_@GlobalScope_constant_TYPE_OBJECT>`.
Otherwise, returns an empty `StringName<class_StringName>`. See also
`is_typed_key<class_Dictionary_method_is_typed_key>` and
`Object.get_class<class_Object_method_get_class>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_typed\_key\_script**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_get_typed_key_script>`

Returns the `Script<class_Script>` instance associated with this typed
dictionary's keys, or `null` if it does not exist. See also
`is_typed_key<class_Dictionary_method_is_typed_key>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_typed\_value\_builtin**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_get_typed_value_builtin>`

Returns the built-in `Variant<class_Variant>` type of the typed
dictionary's values as a `Variant.Type<enum_@GlobalScope_Variant.Type>`
constant. If the values are not typed, returns
`@GlobalScope.TYPE_NIL<class_@GlobalScope_constant_TYPE_NIL>`. See also
`is_typed_value<class_Dictionary_method_is_typed_value>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StringName<class_StringName>` **get\_typed\_value\_class\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_get_typed_value_class_name>`

Returns the **built-in** class name of the typed dictionary's values, if
the built-in `Variant<class_Variant>` type is
`@GlobalScope.TYPE_OBJECT<class_@GlobalScope_constant_TYPE_OBJECT>`.
Otherwise, returns an empty `StringName<class_StringName>`. See also
`is_typed_value<class_Dictionary_method_is_typed_value>` and
`Object.get_class<class_Object_method_get_class>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_typed\_value\_script**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_get_typed_value_script>`

Returns the `Script<class_Script>` instance associated with this typed
dictionary's values, or `null` if it does not exist. See also
`is_typed_value<class_Dictionary_method_is_typed_value>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has**(key: `Variant<class_Variant>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_has>`

Returns `true` if the dictionary contains an entry with the given `key`.

gdscript

var my\_dict = {  
"Godot" : 4, 210 : null,

}

print(my\_dict.has("Godot")) \# Prints true print(my\_dict.has(210)) \#
Prints true print(my\_dict.has(4)) \# Prints false

csharp

var myDict = new Godot.Collections.Dictionary { { "Godot", 4 }, { 210,
default }, };

GD.Print(myDict.ContainsKey("Godot")); // Prints true
GD.Print(myDict.ContainsKey(210)); // Prints true
GD.Print(myDict.ContainsKey(4)); // Prints false

In GDScript, this is equivalent to the `in` operator:

    if "Godot" in {"Godot": 4}:
        print("The key is here!") # Will be printed.

\*\*Note:\*\* This method returns `true` as long as the `key` exists,
even if its corresponding value is `null`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_all**(keys: `Array<class_Array>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_has_all>`

Returns `true` if the dictionary contains all keys in the given `keys`
array.

    var data = {"width" : 10, "height" : 20}
    data.has_all(["height", "width"]) # Returns true

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **hash**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_hash>`

Returns a hashed 32-bit integer value representing the dictionary
contents.

gdscript

var dict1 = {"A": 10, "B": 2} var dict2 = {"A": 10, "B": 2}

print(dict1.hash() == dict2.hash()) \# Prints true

csharp

var dict1 = new Godot.Collections.Dictionary{{"A", 10}, {"B", 2}}; var
dict2 = new Godot.Collections.Dictionary{{"A", 10}, {"B", 2}};

// Godot.Collections.Dictionary has no Hash() method. Use GD.Hash()
instead. GD.Print(GD.Hash(dict1) == GD.Hash(dict2)); // Prints true

\*\*Note:\*\* Dictionaries with the same entries but in a different
order will not have the same hash.

\*\*Note:\*\* Dictionaries with equal hash values are *not* guaranteed
to be the same, because of hash collisions. On the contrary,
dictionaries with different hash values are guaranteed to be different.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_empty**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_is_empty>`

Returns `true` if the dictionary is empty (its size is `0`). See also
`size<class_Dictionary_method_size>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_read\_only**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_is_read_only>`

Returns `true` if the dictionary is read-only. See
`make_read_only<class_Dictionary_method_make_read_only>`. Dictionaries
are automatically read-only if declared with `const` keyword.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_same\_typed**(dictionary:
`Dictionary<class_Dictionary>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_is_same_typed>`

Returns `true` if the dictionary is typed the same as `dictionary`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_same\_typed\_key**(dictionary:
`Dictionary<class_Dictionary>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_is_same_typed_key>`

Returns `true` if the dictionary's keys are typed the same as
`dictionary`'s keys.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_same\_typed\_value**(dictionary:
`Dictionary<class_Dictionary>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_is_same_typed_value>`

Returns `true` if the dictionary's values are typed the same as
`dictionary`'s values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_typed**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_is_typed>`

Returns `true` if the dictionary is typed. Typed dictionaries can only
store keys/values of their associated type and provide type safety for
the `[]` operator. Methods of typed dictionary still return
`Variant<class_Variant>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_typed\_key**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_is_typed_key>`

Returns `true` if the dictionary's keys are typed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_typed\_value**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_is_typed_value>`

Returns `true` if the dictionary's values are typed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **keys**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_keys>`

Returns the list of keys in the dictionary.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **make\_read\_only**()
`🔗<class_Dictionary_method_make_read_only>`

Makes the dictionary read-only, i.e. disables modification of the
dictionary's contents. Does not apply to nested content, e.g. content of
nested dictionaries.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **merge**(dictionary:
`Dictionary<class_Dictionary>`, overwrite: `bool<class_bool>` = false)
`🔗<class_Dictionary_method_merge>`

Adds entries from `dictionary` to this dictionary. By default, duplicate
keys are not copied over, unless `overwrite` is `true`.

gdscript

var dict = { "item": "sword", "quantity": 2 } var other\_dict = {
"quantity": 15, "color": "silver" }

\# Overwriting of existing keys is disabled by default.
dict.merge(other\_dict) print(dict) \# { "item": "sword", "quantity": 2,
"color": "silver" }

\# With overwriting of existing keys enabled. dict.merge(other\_dict,
true) print(dict) \# { "item": "sword", "quantity": 15, "color":
"silver" }

csharp

var dict = new Godot.Collections.Dictionary { \["item"\] = "sword",
\["quantity"\] = 2, };

var otherDict = new Godot.Collections.Dictionary { \["quantity"\] = 15,
\["color"\] = "silver", };

// Overwriting of existing keys is disabled by default.
dict.Merge(otherDict); GD.Print(dict); // { "item": "sword", "quantity":
2, "color": "silver" }

// With overwriting of existing keys enabled. dict.Merge(otherDict,
true); GD.Print(dict); // { "item": "sword", "quantity": 15, "color":
"silver" }

\*\*Note:\*\* `merge<class_Dictionary_method_merge>` is *not* recursive.
Nested dictionaries are considered as keys that can be overwritten or
not depending on the value of `overwrite`, but they will never be merged
together.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **merged**(dictionary:
`Dictionary<class_Dictionary>`, overwrite: `bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_merged>`

Returns a copy of this dictionary merged with the other `dictionary`. By
default, duplicate keys are not copied over, unless `overwrite` is
`true`. See also `merge<class_Dictionary_method_merge>`.

This method is useful for quickly making dictionaries with default
values:

    var base = { "fruit": "apple", "vegetable": "potato" }
    var extra = { "fruit": "orange", "dressing": "vinegar" }
    # Prints { "fruit": "orange", "vegetable": "potato", "dressing": "vinegar" }
    print(extra.merged(base))
    # Prints { "fruit": "apple", "vegetable": "potato", "dressing": "vinegar" }
    print(extra.merged(base, true))

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **recursive\_equal**(dictionary:
`Dictionary<class_Dictionary>`, recursion\_count: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_recursive_equal>`

Returns `true` if the two dictionaries contain the same keys and values,
inner **Dictionary** and `Array<class_Array>` keys and values are
compared recursively.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **set**(key: `Variant<class_Variant>`, value:
`Variant<class_Variant>`) `🔗<class_Dictionary_method_set>`

Sets the value of the element at the given `key` to the given `value`.
This is the same as using the `[]` operator (`array[index] = value`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **size**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_size>`

Returns the number of entries in the dictionary. Empty dictionaries
(`{ }`) always return `0`. See also
`is_empty<class_Dictionary_method_is_empty>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **sort**() `🔗<class_Dictionary_method_sort>`

Sorts the dictionary in-place by key. This can be used to ensure
dictionaries with the same contents produce equivalent results when
getting the `keys<class_Dictionary_method_keys>`, getting the
`values<class_Dictionary_method_values>`, and converting to a string.
This is also useful when wanting a JSON representation consistent with
what is in memory, and useful for storing on a database that requires
dictionaries to be sorted.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **values**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_Dictionary_method_values>`

Returns the list of values in this dictionary.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Operator Descriptions

classref-operator

`bool<class_bool>` **operator !=**(right:
`Dictionary<class_Dictionary>`)
`🔗<class_Dictionary_operator_neq_Dictionary>`

Returns `true` if the two dictionaries do not contain the same keys and
values.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right:
`Dictionary<class_Dictionary>`)
`🔗<class_Dictionary_operator_eq_Dictionary>`

Returns `true` if the two dictionaries contain the same keys and values.
The order of the entries does not matter.

\*\*Note:\*\* In C#, by convention, this operator compares by
**reference**. If you need to compare by value, iterate over both
dictionaries.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`Variant<class_Variant>` **operator \[\]**(key:
`Variant<class_Variant>`) `🔗<class_Dictionary_operator_idx_Variant>`

Returns the corresponding value for the given `key` in the dictionary.
If the entry does not exist, fails and returns `null`. For safe access,
use `get<class_Dictionary_method_get>` or
`has<class_Dictionary_method_has>`.
