github\_url  
hide

# StringName

A built-in type for unique strings.

classref-introduction-group

## Description

**StringName**s are immutable strings designed for general-purpose
representation of unique names (also called "string interning"). Two
**StringName**s with the same value are the same object. Comparing them
is extremely fast compared to regular `String<class_String>`s.

You will usually pass a `String<class_String>` to methods expecting a
**StringName** and it will be automatically converted (often at compile
time), but in rare cases you can construct a **StringName** ahead of
time with the **StringName** constructor or, in GDScript, the literal
syntax `&"example"`. Manually constructing a **StringName** allows you
to control when the conversion from `String<class_String>` occurs or to
use the literal and prevent conversions entirely.

See also `NodePath<class_NodePath>`, which is a similar concept
specifically designed to store pre-parsed scene tree paths.

All of `String<class_String>`'s methods are available in this class too.
They convert the **StringName** into a string, and they also return a
string. This is highly inefficient and should only be used if the string
is desired.

\*\*Note:\*\* In C#, an explicit conversion to `System.String` is
required to use the methods listed on this page. Use the `ToString()`
method to cast a **StringName** to a string, and then use the equivalent
methods in `System.String` or `StringExtensions`.

\*\*Note:\*\* In a boolean context, a **StringName** will evaluate to
`false` if it is empty (`StringName("")`). Otherwise, a **StringName**
will always evaluate to `true`.

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

## Constructor Descriptions

classref-constructor

`StringName<class_StringName>` **StringName**()
`🔗<class_StringName_constructor_StringName>`

Constructs an empty **StringName**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`StringName<class_StringName>` **StringName**(from:
`StringName<class_StringName>`)

Constructs a **StringName** as a copy of the given **StringName**.

classref-item-separator

------------------------------------------------------------------------

classref-constructor

`StringName<class_StringName>` **StringName**(from:
`String<class_String>`)

Creates a new **StringName** from the given `String<class_String>`. In
GDScript, `StringName("example")` is equivalent to `&"example"`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`bool<class_bool>` **begins\_with**(text: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_begins_with>`

Returns `true` if the string begins with the given `text`. See also
`ends_with<class_StringName_method_ends_with>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **bigrams**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_bigrams>`

Returns an array containing the bigrams (pairs of consecutive
characters) of this string.

    print("Get up!".bigrams()) # Prints ["Ge", "et", "t ", " u", "up", "p!"]

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **bin\_to\_int**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_bin_to_int>`

Converts the string representing a binary number into an
`int<class_int>`. The string may optionally be prefixed with `"0b"`, and
an additional `-` prefix for negative numbers.

gdscript

print("101".bin\_to\_int()) \# Prints 5 print("0b101".bin\_to\_int()) \#
Prints 5 print("-0b10".bin\_to\_int()) \# Prints -2

csharp

GD.Print("101".BinToInt()); // Prints 5 GD.Print("0b101".BinToInt()); //
Prints 5 GD.Print("-0b10".BinToInt()); // Prints -2

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **c\_escape**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_c_escape>`

Returns a copy of the string with special characters escaped using the C
language standard.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **c\_unescape**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_c_unescape>`

Returns a copy of the string with escaped characters replaced by their
meanings. Supported escape sequences are `\'`, `\"`, `\\`, `\a`, `\b`,
`\f`, `\n`, `\r`, `\t`, `\v`.

\*\*Note:\*\* Unlike the GDScript parser, this method doesn't support
the `\uXXXX` escape sequence.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **capitalize**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_capitalize>`

Changes the appearance of the string: replaces underscores (`_`) with
spaces, adds spaces before uppercase letters in the middle of a word,
converts all letters to lowercase, then converts the first one and each
one following a space to uppercase.

gdscript

"move\_local\_x".capitalize() \# Returns "Move Local X"
"sceneFile\_path".capitalize() \# Returns "Scene File Path" "2D, FPS,
PNG".capitalize() \# Returns "2d, Fps, Png"

csharp

"move\_local\_x".Capitalize(); // Returns "Move Local X"
"sceneFile\_path".Capitalize(); // Returns "Scene File Path" "2D, FPS,
PNG".Capitalize(); // Returns "2d, Fps, Png"

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **casecmp\_to**(to: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_casecmp_to>`

Performs a case-sensitive comparison to another string. Returns `-1` if
less than, `1` if greater than, or `0` if equal. "Less than" and
"greater than" are determined by the [Unicode code
points](https://en.wikipedia.org/wiki/List_of_Unicode_characters) of
each string, which roughly matches the alphabetical order.

With different string lengths, returns `1` if this string is longer than
the `to` string, or `-1` if shorter. Note that the length of empty
strings is *always* `0`.

To get a `bool<class_bool>` result from a string comparison, use the
`==` operator instead. See also
`nocasecmp_to<class_StringName_method_nocasecmp_to>`,
`filecasecmp_to<class_StringName_method_filecasecmp_to>`, and
`naturalcasecmp_to<class_StringName_method_naturalcasecmp_to>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **contains**(what: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_contains>`

Returns `true` if the string contains `what`. In GDScript, this
corresponds to the `in` operator.

gdscript

print("Node".contains("de")) \# Prints true print("team".contains("I"))
\# Prints false print("I" in "team") \# Prints false

csharp

GD.Print("Node".Contains("de")); // Prints true
GD.Print("team".Contains("I")); // Prints false

If you need to know where `what` is within the string, use
`find<class_StringName_method_find>`. See also
`containsn<class_StringName_method_containsn>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **containsn**(what: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_containsn>`

Returns `true` if the string contains `what`, **ignoring case**.

If you need to know where `what` is within the string, use
`findn<class_StringName_method_findn>`. See also
`contains<class_StringName_method_contains>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **count**(what: `String<class_String>`, from:
`int<class_int>` = 0, to: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_count>`

Returns the number of occurrences of the substring `what` between `from`
and `to` positions. If `to` is 0, the search continues until the end of
the string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **countn**(what: `String<class_String>`, from:
`int<class_int>` = 0, to: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_countn>`

Returns the number of occurrences of the substring `what` between `from`
and `to` positions, **ignoring case**. If `to` is 0, the search
continues until the end of the string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **dedent**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_dedent>`

Returns a copy of the string with indentation (leading tabs and spaces)
removed. See also `indent<class_StringName_method_indent>` to add
indentation.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **ends\_with**(text: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_ends_with>`

Returns `true` if the string ends with the given `text`. See also
`begins_with<class_StringName_method_begins_with>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **erase**(position: `int<class_int>`, chars:
`int<class_int>` = 1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_erase>`

Returns a string with `chars` characters erased starting from
`position`. If `chars` goes beyond the string's length given the
specified `position`, fewer characters will be erased from the returned
string. Returns an empty string if either `position` or `chars` is
negative. Returns the original string unmodified if `chars` is `0`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **filecasecmp\_to**(to: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_filecasecmp_to>`

Like `naturalcasecmp_to<class_StringName_method_naturalcasecmp_to>` but
prioritizes strings that begin with periods (`.`) and underscores (`_`)
before any other character. Useful when sorting folders or file names.

To get a `bool<class_bool>` result from a string comparison, use the
`==` operator instead. See also
`filenocasecmp_to<class_StringName_method_filenocasecmp_to>`,
`naturalcasecmp_to<class_StringName_method_naturalcasecmp_to>`, and
`casecmp_to<class_StringName_method_casecmp_to>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **filenocasecmp\_to**(to: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_filenocasecmp_to>`

Like `naturalnocasecmp_to<class_StringName_method_naturalnocasecmp_to>`
but prioritizes strings that begin with periods (`.`) and underscores
(`_`) before any other character. Useful when sorting folders or file
names.

To get a `bool<class_bool>` result from a string comparison, use the
`==` operator instead. See also
`filecasecmp_to<class_StringName_method_filecasecmp_to>`,
`naturalnocasecmp_to<class_StringName_method_naturalnocasecmp_to>`, and
`nocasecmp_to<class_StringName_method_nocasecmp_to>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **find**(what: `String<class_String>`, from:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_find>`

Returns the index of the **first** occurrence of `what` in this string,
or `-1` if there are none. The search's start can be specified with
`from`, continuing to the end of the string.

gdscript

print("Team".find("I")) \# Prints -1

print("Potato".find("t")) \# Prints 2 print("Potato".find("t", 3)) \#
Prints 4 print("Potato".find("t", 5)) \# Prints -1

csharp

GD.Print("Team".Find("I")); // Prints -1

GD.Print("Potato".Find("t")); // Prints 2 GD.Print("Potato".Find("t",
3)); // Prints 4 GD.Print("Potato".Find("t", 5)); // Prints -1

\*\*Note:\*\* If you just want to know whether the string contains
`what`, use `contains<class_StringName_method_contains>`. In GDScript,
you may also use the `in` operator.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **findn**(what: `String<class_String>`, from:
`int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_findn>`

Returns the index of the **first** **case-insensitive** occurrence of
`what` in this string, or `-1` if there are none. The starting search
index can be specified with `from`, continuing to the end of the string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **format**(values: `Variant<class_Variant>`,
placeholder: `String<class_String>` = "{\_}")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_format>`

Formats the string by replacing all occurrences of `placeholder` with
the elements of `values`.

`values` can be a `Dictionary<class_Dictionary>` or an
`Array<class_Array>`. Any underscores in `placeholder` will be replaced
with the corresponding keys in advance. Array elements use their index
as keys.

    # Prints "Waiting for Godot is a play by Samuel Beckett, and Godot Engine is named after it."
    var use_array_values = "Waiting for {0} is a play by {1}, and {0} Engine is named after it."
    print(use_array_values.format(["Godot", "Samuel Beckett"]))

    # Prints "User 42 is Godot."
    print("User {id} is {name}.".format({"id": 42, "name": "Godot"}))

Some additional handling is performed when `values` is an
`Array<class_Array>`. If `placeholder` does not contain an underscore,
the elements of the `values` array will be used to replace one
occurrence of the placeholder in order; If an element of `values` is
another 2-element array, it'll be interpreted as a key-value pair.

    # Prints "User 42 is Godot."
    print("User {} is {}.".format([42, "Godot"], "{}"))
    print("User {id} is {name}.".format([["id", 42], ["name", "Godot"]]))

See also the
`GDScript format string <../tutorials/scripting/gdscript/gdscript_format_string>`
tutorial.

\*\*Note:\*\* In C#, it's recommended to [interpolate strings with
"$"](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/interpolated),
instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_base\_dir**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_get_base_dir>`

If the string is a valid file path, returns the base directory name.

    var dir_path = "/path/to/file.txt".get_base_dir() # dir_path is "/path/to"

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_basename**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_get_basename>`

If the string is a valid file path, returns the full file path, without
the extension.

    var base = "/path/to/file.txt".get_basename() # base is "/path/to/file"

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_extension**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_get_extension>`

If the string is a valid file name or path, returns the file extension
without the leading period (`.`). Otherwise, returns an empty string.

    var a = "/path/to/file.txt".get_extension() # a is "txt"
    var b = "cool.txt".get_extension()          # b is "txt"
    var c = "cool.font.tres".get_extension()    # c is "tres"
    var d = ".pack1".get_extension()            # d is "pack1"

    var e = "file.txt.".get_extension()  # e is ""
    var f = "file.txt..".get_extension() # f is ""
    var g = "txt".get_extension()        # g is ""
    var h = "".get_extension()           # h is ""

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_file**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_get_file>`

If the string is a valid file path, returns the file name, including the
extension.

    var file = "/path/to/icon.png".get_file() # file is "icon.png"

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_slice**(delimiter: `String<class_String>`,
slice: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_get_slice>`

Splits the string using a `delimiter` and returns the substring at index
`slice`. Returns an empty string if the `slice` does not exist.

This is faster than `split<class_StringName_method_split>`, if you only
need one substring.

    print("i/am/example/hi".get_slice("/", 2)) # Prints "example"

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_slice\_count**(delimiter:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_get_slice_count>`

Returns the total number of slices when the string is split with the
given `delimiter` (see `split<class_StringName_method_split>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_slicec**(delimiter: `int<class_int>`,
slice: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_get_slicec>`

Splits the string using a Unicode character with code `delimiter` and
returns the substring at index `slice`. Returns an empty string if the
`slice` does not exist.

This is faster than `split<class_StringName_method_split>`, if you only
need one substring.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **hash**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_hash>`

Returns the 32-bit hash value representing the string's contents.

\*\*Note:\*\* Strings with equal hash values are *not* guaranteed to be
the same, as a result of hash collisions. On the contrary, strings with
different hash values are guaranteed to be different.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **hex\_decode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_hex_decode>`

Decodes a hexadecimal string as a
`PackedByteArray<class_PackedByteArray>`.

gdscript

var text = "hello world" var encoded =
text.to\_utf8\_buffer().hex\_encode() \# outputs
"68656c6c6f20776f726c64"
print(buf.hex\_decode().get\_string\_from\_utf8())

csharp

var text = "hello world"; var encoded = text.ToUtf8Buffer().HexEncode();
// outputs "68656c6c6f20776f726c64"
GD.Print(buf.HexDecode().GetStringFromUtf8());

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **hex\_to\_int**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_hex_to_int>`

Converts the string representing a hexadecimal number into an
`int<class_int>`. The string may be optionally prefixed with `"0x"`, and
an additional `-` prefix for negative numbers.

gdscript

print("0xff".hex\_to\_int()) \# Prints 255 print("ab".hex\_to\_int()) \#
Prints 171

csharp

GD.Print("0xff".HexToInt()); // Prints 255 GD.Print("ab".HexToInt()); //
Prints 171

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **indent**(prefix: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_indent>`

Indents every line of the string with the given `prefix`. Empty lines
are not indented. See also `dedent<class_StringName_method_dedent>` to
remove indentation.

For example, the string can be indented with two tabulations using
`"\t\t"`, or four spaces using `"    "`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **insert**(position: `int<class_int>`, what:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_insert>`

Inserts `what` at the given `position` in the string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_absolute\_path**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_absolute_path>`

Returns `true` if the string is a path to a file or directory, and its
starting point is explicitly defined. This method is the opposite of
`is_relative_path<class_StringName_method_is_relative_path>`.

This includes all paths starting with `"res://"`, `"user://"`, `"C:\"`,
`"/"`, etc.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_empty**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_empty>`

Returns `true` if the string's length is `0` (`""`). See also
`length<class_StringName_method_length>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_relative\_path**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_relative_path>`

Returns `true` if the string is a path, and its starting point is
dependent on context. The path could begin from the current directory,
or the current `Node<class_Node>` (if the string is derived from a
`NodePath<class_NodePath>`), and may sometimes be prefixed with `"./"`.
This method is the opposite of
`is_absolute_path<class_StringName_method_is_absolute_path>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_subsequence\_of**(text: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_subsequence_of>`

Returns `true` if all characters of this string can be found in `text`
in their original order.

    var text = "Wow, incredible!"

    print("inedible".is_subsequence_of(text)) # Prints true
    print("Word!".is_subsequence_of(text))    # Prints true
    print("Window".is_subsequence_of(text))   # Prints false
    print("".is_subsequence_of(text))         # Prints true

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_subsequence\_ofn**(text:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_subsequence_ofn>`

Returns `true` if all characters of this string can be found in `text`
in their original order, **ignoring case**.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_ascii\_identifier**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_valid_ascii_identifier>`

Returns `true` if this string is a valid ASCII identifier. A valid ASCII
identifier may contain only letters, digits, and underscores (`_`), and
the first character may not be a digit.

    print("node_2d".is_valid_ascii_identifier())    # Prints true
    print("TYPE_FLOAT".is_valid_ascii_identifier()) # Prints true
    print("1st_method".is_valid_ascii_identifier()) # Prints false
    print("MyMethod#2".is_valid_ascii_identifier()) # Prints false

See also
`is_valid_unicode_identifier<class_StringName_method_is_valid_unicode_identifier>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_filename**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_valid_filename>`

Returns `true` if this string does not contain characters that are not
allowed in file names (`:` `/` `\` `?` `*` `"` `|` `%` `<` `>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_float**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_valid_float>`

Returns `true` if this string represents a valid floating-point number.
A valid float may contain only digits, one decimal point (`.`), and the
exponent letter (`e`). It may also be prefixed with a positive (`+`) or
negative (`-`) sign. Any valid integer is also a valid float (see
`is_valid_int<class_StringName_method_is_valid_int>`). See also
`to_float<class_StringName_method_to_float>`.

    print("1.7".is_valid_float())   # Prints true
    print("24".is_valid_float())    # Prints true
    print("7e3".is_valid_float())   # Prints true
    print("Hello".is_valid_float()) # Prints false

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_hex\_number**(with\_prefix:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_valid_hex_number>`

Returns `true` if this string is a valid hexadecimal number. A valid
hexadecimal number only contains digits or letters `A` to `F` (either
uppercase or lowercase), and may be prefixed with a positive (`+`) or
negative (`-`) sign.

If `with_prefix` is `true`, the hexadecimal number needs to prefixed by
`"0x"` to be considered valid.

    print("A08E".is_valid_hex_number())    # Prints true
    print("-AbCdEf".is_valid_hex_number()) # Prints true
    print("2.5".is_valid_hex_number())     # Prints false

    print("0xDEADC0DE".is_valid_hex_number(true)) # Prints true

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_html\_color**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_valid_html_color>`

Returns `true` if this string is a valid color in hexadecimal HTML
notation. The string must be a hexadecimal value (see
`is_valid_hex_number<class_StringName_method_is_valid_hex_number>`) of
either 3, 4, 6 or 8 digits, and may be prefixed by a hash sign (`#`).
Other HTML notations for colors, such as names or `hsl()`, are not
considered valid. See also `Color.html<class_Color_method_html>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_identifier**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_valid_identifier>`

**Deprecated:** Use
`is_valid_ascii_identifier<class_StringName_method_is_valid_ascii_identifier>`
instead.

Returns `true` if this string is a valid identifier. A valid identifier
may contain only letters, digits and underscores (`_`), and the first
character may not be a digit.

    print("node_2d".is_valid_identifier())    # Prints true
    print("TYPE_FLOAT".is_valid_identifier()) # Prints true
    print("1st_method".is_valid_identifier()) # Prints false
    print("MyMethod#2".is_valid_identifier()) # Prints false

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_int**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_valid_int>`

Returns `true` if this string represents a valid integer. A valid
integer only contains digits, and may be prefixed with a positive (`+`)
or negative (`-`) sign. See also
`to_int<class_StringName_method_to_int>`.

    print("7".is_valid_int())    # Prints true
    print("1.65".is_valid_int()) # Prints false
    print("Hi".is_valid_int())   # Prints false
    print("+3".is_valid_int())   # Prints true
    print("-12".is_valid_int())  # Prints true

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_ip\_address**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_valid_ip_address>`

Returns `true` if this string represents a well-formatted IPv4 or IPv6
address. This method considers [reserved IP
addresses](https://en.wikipedia.org/wiki/Reserved_IP_addresses) such as
`"0.0.0.0"` and `"ffff:ffff:ffff:ffff:ffff:ffff:ffff:ffff"` as valid.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_unicode\_identifier**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_is_valid_unicode_identifier>`

Returns `true` if this string is a valid Unicode identifier.

A valid Unicode identifier must begin with a Unicode character of class
`XID_Start` or `"_"`, and may contain Unicode characters of class
`XID_Continue` in the other positions.

    print("node_2d".is_valid_unicode_identifier())      # Prints true
    print("1st_method".is_valid_unicode_identifier())   # Prints false
    print("MyMethod#2".is_valid_unicode_identifier())   # Prints false
    print("állóképesség".is_valid_unicode_identifier()) # Prints true
    print("выносливость".is_valid_unicode_identifier()) # Prints true
    print("体力".is_valid_unicode_identifier())         # Prints true

See also
`is_valid_ascii_identifier<class_StringName_method_is_valid_ascii_identifier>`.

\*\*Note:\*\* This method checks identifiers the same way as GDScript.
See
`TextServer.is_valid_identifier<class_TextServer_method_is_valid_identifier>`
for more advanced checks.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **join**(parts:
`PackedStringArray<class_PackedStringArray>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_join>`

Returns the concatenation of `parts`' elements, with each element
separated by the string calling this method. This method is the opposite
of `split<class_StringName_method_split>`.

gdscript

var fruits = \["Apple", "Orange", "Pear", "Kiwi"\]

print(", ".join(fruits)) \# Prints "Apple, Orange, Pear, Kiwi"
print("---".join(fruits)) \# Prints "Apple---Orange---Pear---Kiwi"

csharp

var fruits = new string\[\] {"Apple", "Orange", "Pear", "Kiwi"};

// In C#, this method is static. GD.Print(string.Join(", ", fruits)); //
Prints "Apple, Orange, Pear, Kiwi" GD.Print(string.Join("---", fruits));
// Prints "Apple---Orange---Pear---Kiwi"

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **json\_escape**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_json_escape>`

Returns a copy of the string with special characters escaped using the
JSON standard. Because it closely matches the C standard, it is possible
to use `c_unescape<class_StringName_method_c_unescape>` to unescape the
string, if necessary.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **left**(length: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_left>`

Returns the first `length` characters from the beginning of the string.
If `length` is negative, strips the last `length` characters from the
string's end.

    print("Hello World!".left(3))  # Prints "Hel"
    print("Hello World!".left(-4)) # Prints "Hello Wo"

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **length**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_length>`

Returns the number of characters in the string. Empty strings (`""`)
always return `0`. See also
`is_empty<class_StringName_method_is_empty>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **lpad**(min\_length: `int<class_int>`,
character: `String<class_String>` = " ")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_lpad>`

Formats the string to be at least `min_length` long by adding
`character`s to the left of the string, if necessary. See also
`rpad<class_StringName_method_rpad>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **lstrip**(chars: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_lstrip>`

Removes a set of characters defined in `chars` from the string's
beginning. See also `rstrip<class_StringName_method_rstrip>`.

\*\*Note:\*\* `chars` is not a prefix. Use
`trim_prefix<class_StringName_method_trim_prefix>` to remove a single
prefix, rather than a set of characters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **match**(expr: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_match>`

Does a simple expression match (also called "glob" or "globbing"), where
`*` matches zero or more arbitrary characters and `?` matches any single
character except a period (`.`). An empty string or empty expression
always evaluates to `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **matchn**(expr: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_matchn>`

Does a simple **case-insensitive** expression match, where `*` matches
zero or more arbitrary characters and `?` matches any single character
except a period (`.`). An empty string or empty expression always
evaluates to `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **md5\_buffer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_md5_buffer>`

Returns the [MD5 hash](https://en.wikipedia.org/wiki/MD5) of the string
as a `PackedByteArray<class_PackedByteArray>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **md5\_text**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_md5_text>`

Returns the [MD5 hash](https://en.wikipedia.org/wiki/MD5) of the string
as another `String<class_String>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **naturalcasecmp\_to**(to: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_naturalcasecmp_to>`

Performs a **case-sensitive**, *natural order* comparison to another
string. Returns `-1` if less than, `1` if greater than, or `0` if equal.
"Less than" or "greater than" are determined by the [Unicode code
points](https://en.wikipedia.org/wiki/List_of_Unicode_characters) of
each string, which roughly matches the alphabetical order.

When used for sorting, natural order comparison orders sequences of
numbers by the combined value of each digit as is often expected,
instead of the single digit's value. A sorted sequence of numbered
strings will be `["1", "2", "3", ...]`, not
`["1", "10", "2", "3", ...]`.

With different string lengths, returns `1` if this string is longer than
the `to` string, or `-1` if shorter. Note that the length of empty
strings is *always* `0`.

To get a `bool<class_bool>` result from a string comparison, use the
`==` operator instead. See also
`naturalnocasecmp_to<class_StringName_method_naturalnocasecmp_to>`,
`filecasecmp_to<class_StringName_method_filecasecmp_to>`, and
`nocasecmp_to<class_StringName_method_nocasecmp_to>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **naturalnocasecmp\_to**(to: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_naturalnocasecmp_to>`

Performs a **case-insensitive**, *natural order* comparison to another
string. Returns `-1` if less than, `1` if greater than, or `0` if equal.
"Less than" or "greater than" are determined by the [Unicode code
points](https://en.wikipedia.org/wiki/List_of_Unicode_characters) of
each string, which roughly matches the alphabetical order. Internally,
lowercase characters are converted to uppercase for the comparison.

When used for sorting, natural order comparison orders sequences of
numbers by the combined value of each digit as is often expected,
instead of the single digit's value. A sorted sequence of numbered
strings will be `["1", "2", "3", ...]`, not
`["1", "10", "2", "3", ...]`.

With different string lengths, returns `1` if this string is longer than
the `to` string, or `-1` if shorter. Note that the length of empty
strings is *always* `0`.

To get a `bool<class_bool>` result from a string comparison, use the
`==` operator instead. See also
`naturalcasecmp_to<class_StringName_method_naturalcasecmp_to>`,
`filenocasecmp_to<class_StringName_method_filenocasecmp_to>`, and
`casecmp_to<class_StringName_method_casecmp_to>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **nocasecmp\_to**(to: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_nocasecmp_to>`

Performs a **case-insensitive** comparison to another string. Returns
`-1` if less than, `1` if greater than, or `0` if equal. "Less than" or
"greater than" are determined by the [Unicode code
points](https://en.wikipedia.org/wiki/List_of_Unicode_characters) of
each string, which roughly matches the alphabetical order. Internally,
lowercase characters are converted to uppercase for the comparison.

With different string lengths, returns `1` if this string is longer than
the `to` string, or `-1` if shorter. Note that the length of empty
strings is *always* `0`.

To get a `bool<class_bool>` result from a string comparison, use the
`==` operator instead. See also
`casecmp_to<class_StringName_method_casecmp_to>`,
`filenocasecmp_to<class_StringName_method_filenocasecmp_to>`, and
`naturalnocasecmp_to<class_StringName_method_naturalnocasecmp_to>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **pad\_decimals**(digits: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_pad_decimals>`

Formats the string representing a number to have an exact number of
`digits` *after* the decimal point.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **pad\_zeros**(digits: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_pad_zeros>`

Formats the string representing a number to have an exact number of
`digits` *before* the decimal point.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **path\_join**(file: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_path_join>`

Concatenates `file` at the end of the string as a subpath, adding `/` if
necessary.

\*\*Example:\*\* `"this/is".path_join("path") == "this/is/path"`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **repeat**(count: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_repeat>`

Repeats this string a number of times. `count` needs to be greater than
`0`. Otherwise, returns an empty string.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **replace**(what: `String<class_String>`,
forwhat: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_replace>`

Replaces all occurrences of `what` inside the string with the given
`forwhat`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **replacen**(what: `String<class_String>`,
forwhat: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_replacen>`

Replaces all **case-insensitive** occurrences of `what` inside the
string with the given `forwhat`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **reverse**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_reverse>`

Returns the copy of this string in reverse order. This operation works
on unicode codepoints, rather than sequences of codepoints, and may
break things like compound letters or emojis.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **rfind**(what: `String<class_String>`, from:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_rfind>`

Returns the index of the **last** occurrence of `what` in this string,
or `-1` if there are none. The search's start can be specified with
`from`, continuing to the beginning of the string. This method is the
reverse of `find<class_StringName_method_find>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **rfindn**(what: `String<class_String>`, from:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_rfindn>`

Returns the index of the **last** **case-insensitive** occurrence of
`what` in this string, or `-1` if there are none. The starting search
index can be specified with `from`, continuing to the beginning of the
string. This method is the reverse of
`findn<class_StringName_method_findn>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **right**(length: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_right>`

Returns the last `length` characters from the end of the string. If
`length` is negative, strips the first `length` characters from the
string's beginning.

    print("Hello World!".right(3))  # Prints "ld!"
    print("Hello World!".right(-4)) # Prints "o World!"

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **rpad**(min\_length: `int<class_int>`,
character: `String<class_String>` = " ")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_rpad>`

Formats the string to be at least `min_length` long, by adding
`character`s to the right of the string, if necessary. See also
`lpad<class_StringName_method_lpad>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **rsplit**(delimiter:
`String<class_String>` = "", allow\_empty: `bool<class_bool>` = true,
maxsplit: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_rsplit>`

Splits the string using a `delimiter` and returns an array of the
substrings, starting from the end of the string. The splits in the
returned array appear in the same order as the original string. If
`delimiter` is an empty string, each substring will be a single
character.

If `allow_empty` is `false`, empty strings between adjacent delimiters
are excluded from the array.

If `maxsplit` is greater than `0`, the number of splits may not exceed
`maxsplit`. By default, the entire string is split, which is mostly
identical to `split<class_StringName_method_split>`.

gdscript

var some\_string = "One,Two,Three,Four" var some\_array =
some\_string.rsplit(",", true, 1)

print(some\_array.size()) \# Prints 2 print(some\_array\[0\]) \# Prints
"One,Two,Three" print(some\_array\[1\]) \# Prints "Four"

csharp

// In C#, there is no String.RSplit() method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **rstrip**(chars: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_rstrip>`

Removes a set of characters defined in `chars` from the string's end.
See also `lstrip<class_StringName_method_lstrip>`.

\*\*Note:\*\* `chars` is not a suffix. Use
`trim_suffix<class_StringName_method_trim_suffix>` to remove a single
suffix, rather than a set of characters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **sha1\_buffer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_sha1_buffer>`

Returns the [SHA-1](https://en.wikipedia.org/wiki/SHA-1) hash of the
string as a `PackedByteArray<class_PackedByteArray>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **sha1\_text**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_sha1_text>`

Returns the [SHA-1](https://en.wikipedia.org/wiki/SHA-1) hash of the
string as another `String<class_String>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **sha256\_buffer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_sha256_buffer>`

Returns the [SHA-256](https://en.wikipedia.org/wiki/SHA-2) hash of the
string as a `PackedByteArray<class_PackedByteArray>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **sha256\_text**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_sha256_text>`

Returns the [SHA-256](https://en.wikipedia.org/wiki/SHA-2) hash of the
string as another `String<class_String>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **similarity**(text: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_similarity>`

Returns the similarity index ([Sorensen-Dice
coefficient](https://en.wikipedia.org/wiki/S%C3%B8rensen%E2%80%93Dice_coefficient))
of this string compared to another. A result of `1.0` means totally
similar, while `0.0` means totally dissimilar.

    print("ABC123".similarity("ABC123")) # Prints 1.0
    print("ABC123".similarity("XYZ456")) # Prints 0.0
    print("ABC123".similarity("123ABC")) # Prints 0.8
    print("ABC123".similarity("abc123")) # Prints 0.4

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **simplify\_path**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_simplify_path>`

If the string is a valid file path, converts the string into a canonical
path. This is the shortest possible path, without `"./"`, and all the
unnecessary `".."` and `"/"`.

    var simple_path = "./path/to///../file".simplify_path()
    print(simple_path) # Prints "path/file"

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **split**(delimiter:
`String<class_String>` = "", allow\_empty: `bool<class_bool>` = true,
maxsplit: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_split>`

Splits the string using a `delimiter` and returns an array of the
substrings. If `delimiter` is an empty string, each substring will be a
single character. This method is the opposite of
`join<class_StringName_method_join>`.

If `allow_empty` is `false`, empty strings between adjacent delimiters
are excluded from the array.

If `maxsplit` is greater than `0`, the number of splits may not exceed
`maxsplit`. By default, the entire string is split.

gdscript

var some\_array = "One,Two,Three,Four".split(",", true, 2)

print(some\_array.size()) \# Prints 3 print(some\_array\[0\]) \# Prints
"One" print(some\_array\[1\]) \# Prints "Two" print(some\_array\[2\]) \#
Prints "Three,Four"

csharp

// C#'s <span class="title-ref">Split()</span> does not support the
<span class="title-ref">maxsplit</span> parameter. var someArray =
"One,Two,Three".Split(",");

GD.Print(someArray\[0\]); // Prints "One" GD.Print(someArray\[1\]); //
Prints "Two" GD.Print(someArray\[2\]); // Prints "Three"

\*\*Note:\*\* If you only need one substring from the array, consider
using `get_slice<class_StringName_method_get_slice>` which is faster. If
you need to split strings with more complex rules, use the
`RegEx<class_RegEx>` class instead.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedFloat64Array<class_PackedFloat64Array>`
**split\_floats**(delimiter: `String<class_String>`, allow\_empty:
`bool<class_bool>` = true)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_split_floats>`

Splits the string into floats by using a `delimiter` and returns a
`PackedFloat64Array<class_PackedFloat64Array>`.

If `allow_empty` is `false`, empty or invalid `float<class_float>`
conversions between adjacent delimiters are excluded.

    var a = "1,2,4.5".split_floats(",")         # a is [1.0, 2.0, 4.5]
    var c = "1| ||4.5".split_floats("|")        # c is [1.0, 0.0, 0.0, 4.5]
    var b = "1| ||4.5".split_floats("|", false) # b is [1.0, 4.5]

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **strip\_edges**(left: `bool<class_bool>` = true,
right: `bool<class_bool>` = true)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_strip_edges>`

Strips all non-printable characters from the beginning and the end of
the string. These include spaces, tabulations (`\t`), and newlines (`\n`
`\r`).

If `left` is `false`, ignores the string's beginning. Likewise, if
`right` is `false`, ignores the string's end.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **strip\_escapes**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_strip_escapes>`

Strips all escape characters from the string. These include all
non-printable control characters of the first page of the ASCII table
(values from 0 to 31), such as tabulation (`\t`) and newline (`\n`,
`\r`) characters, but *not* spaces.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **substr**(from: `int<class_int>`, len:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_substr>`

Returns part of the string from the position `from` with length `len`.
If `len` is `-1` (as by default), returns the rest of the string
starting from the given position.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **to\_ascii\_buffer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_ascii_buffer>`

Converts the string to an
[ASCII](https://en.wikipedia.org/wiki/ASCII)/Latin-1 encoded
`PackedByteArray<class_PackedByteArray>`. This method is slightly faster
than `to_utf8_buffer<class_StringName_method_to_utf8_buffer>`, but
replaces all unsupported characters with spaces.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **to\_camel\_case**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_camel_case>`

Returns the string converted to `camelCase`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **to\_float**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_float>`

Converts the string representing a decimal number into a
`float<class_float>`. This method stops on the first non-number
character, except the first decimal point (`.`) and the exponent letter
(`e`). See also
`is_valid_float<class_StringName_method_is_valid_float>`.

    var a = "12.35".to_float() # a is 12.35
    var b = "1.2.3".to_float() # b is 1.2
    var c = "12xy3".to_float() # c is 12.0
    var d = "1e3".to_float()   # d is 1000.0
    var e = "Hello!".to_int()  # e is 0.0

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **to\_int**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_int>`

Converts the string representing an integer number into an
`int<class_int>`. This method removes any non-number character and stops
at the first decimal point (`.`). See also
`is_valid_int<class_StringName_method_is_valid_int>`.

    var a = "123".to_int()    # a is 123
    var b = "x1y2z3".to_int() # b is 123
    var c = "-1.2.3".to_int() # c is -1
    var d = "Hello!".to_int() # d is 0

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **to\_lower**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_lower>`

Returns the string converted to `lowercase`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **to\_pascal\_case**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_pascal_case>`

Returns the string converted to `PascalCase`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **to\_snake\_case**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_snake_case>`

Returns the string converted to `snake_case`.

\*\*Note:\*\* Numbers followed by a *single* letter are not separated in
the conversion to keep some words (such as "2D") together.

gdscript

"Node2D".to\_snake\_case() \# Returns "node\_2d" "2nd
place".to\_snake\_case() \# Returns "2\_nd\_place"
"Texture3DAssetFolder".to\_snake\_case() \# Returns
"texture\_3d\_asset\_folder"

csharp

"Node2D".ToSnakeCase(); // Returns "node\_2d" "2nd place".ToSnakeCase();
// Returns "2\_nd\_place" "Texture3DAssetFolder".ToSnakeCase(); //
Returns "texture\_3d\_asset\_folder"

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **to\_upper**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_upper>`

Returns the string converted to `UPPERCASE`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **to\_utf8\_buffer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_utf8_buffer>`

Converts the string to a [UTF-8](https://en.wikipedia.org/wiki/UTF-8)
encoded `PackedByteArray<class_PackedByteArray>`. This method is
slightly slower than
`to_ascii_buffer<class_StringName_method_to_ascii_buffer>`, but supports
all UTF-8 characters. For most cases, prefer using this method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **to\_utf16\_buffer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_utf16_buffer>`

Converts the string to a [UTF-16](https://en.wikipedia.org/wiki/UTF-16)
encoded `PackedByteArray<class_PackedByteArray>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **to\_utf32\_buffer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_utf32_buffer>`

Converts the string to a [UTF-32](https://en.wikipedia.org/wiki/UTF-32)
encoded `PackedByteArray<class_PackedByteArray>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **to\_wchar\_buffer**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_to_wchar_buffer>`

Converts the string to a [wide
character](https://en.wikipedia.org/wiki/Wide_character) (`wchar_t`,
UTF-16 on Windows, UTF-32 on other platforms) encoded
`PackedByteArray<class_PackedByteArray>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **trim\_prefix**(prefix: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_trim_prefix>`

Removes the given `prefix` from the start of the string, or returns the
string unchanged.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **trim\_suffix**(suffix: `String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_trim_suffix>`

Removes the given `suffix` from the end of the string, or returns the
string unchanged.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **unicode\_at**(at: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_unicode_at>`

Returns the character code at position `at`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **uri\_decode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_uri_decode>`

Decodes the string from its URL-encoded format. This method is meant to
properly decode the parameters in a URL when receiving an HTTP request.

gdscript

var url = "$DOCS\_URL/?highlight=Godot%20Engine%3%docs"
print(url.uri\_decode()) \# Prints "$DOCS\_URL/?highlight=Godot
Engine:docs"

csharp

var url = "$DOCS\_URL/?highlight=Godot%20Engine%3%docs"
GD.Print(url.URIDecode()) // Prints "$DOCS\_URL/?highlight=Godot
Engine:docs"

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **uri\_encode**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_uri_encode>`

Encodes the string to URL-friendly format. This method is meant to
properly encode the parameters in a URL when sending an HTTP request.

gdscript

var prefix = "$DOCS\_URL/?highlight=" var url = prefix + "Godot
Engine:docs".uri\_encode()

print(url) \# Prints "$DOCS\_URL/?highlight=Godot%20Engine%3%docs"

csharp

var prefix = "$DOCS\_URL/?highlight="; var url = prefix + "Godot
Engine:docs".URIEncode();

GD.Print(url); // Prints "$DOCS\_URL/?highlight=Godot%20Engine%3%docs"

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **validate\_filename**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_validate_filename>`

Returns a copy of the string with all characters that are not allowed in
`is_valid_filename<class_StringName_method_is_valid_filename>` replaced
with underscores.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **validate\_node\_name**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_validate_node_name>`

Returns a copy of the string with all characters that are not allowed in
`Node.name<class_Node_property_name>` (`.` `:` `@` `/` `"` `%`) replaced
with underscores.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **xml\_escape**(escape\_quotes:
`bool<class_bool>` = false)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_xml_escape>`

Returns a copy of the string with special characters escaped using the
XML standard. If `escape_quotes` is `true`, the single quote (`'`) and
double quote (`"`) characters are also escaped.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **xml\_unescape**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StringName_method_xml_unescape>`

Returns a copy of the string with escaped characters replaced by their
meanings according to the XML standard.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Operator Descriptions

classref-operator

`bool<class_bool>` **operator !=**(right: `String<class_String>`)
`🔗<class_StringName_operator_neq_String>`

Returns `true` if this **StringName** is not equivalent to the given
`String<class_String>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator !=**(right:
`StringName<class_StringName>`)
`🔗<class_StringName_operator_neq_StringName>`

Returns `true` if the **StringName** and `right` do not refer to the
same name. Comparisons between **StringName**s are much faster than
regular `String<class_String>` comparisons.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`String<class_String>` **operator %**(right: `Variant<class_Variant>`)
`🔗<class_StringName_operator_mod_Variant>`

Formats the **StringName**, replacing the placeholders with one or more
parameters, returning a `String<class_String>`. To pass multiple
parameters, `right` needs to be an `Array<class_Array>`.

For more information, see the
`GDScript format strings <../tutorials/scripting/gdscript/gdscript_format_string>`
tutorial.

\*\*Note:\*\* In C#, this operator is not available. Instead, see [how
to interpolate strings with
"$"](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/tokens/interpolated).

classref-item-separator

------------------------------------------------------------------------

classref-operator

`String<class_String>` **operator +**(right: `String<class_String>`)
`🔗<class_StringName_operator_sum_String>`

Appends `right` at the end of this **StringName**, returning a
`String<class_String>`. This is also known as a string concatenation.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`String<class_String>` **operator +**(right:
`StringName<class_StringName>`)
`🔗<class_StringName_operator_sum_StringName>`

Appends `right` at the end of this **StringName**, returning a
`String<class_String>`. This is also known as a string concatenation.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &lt;**(right:
`StringName<class_StringName>`)
`🔗<class_StringName_operator_lt_StringName>`

Returns `true` if the left **StringName**'s pointer comes before
`right`. Note that this will not match their [Unicode
order](https://en.wikipedia.org/wiki/List_of_Unicode_characters).

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &lt;=**(right:
`StringName<class_StringName>`)
`🔗<class_StringName_operator_lte_StringName>`

Returns `true` if the left **StringName**'s pointer comes before `right`
or if they are the same. Note that this will not match their [Unicode
order](https://en.wikipedia.org/wiki/List_of_Unicode_characters).

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right: `String<class_String>`)
`🔗<class_StringName_operator_eq_String>`

Returns `true` if this **StringName** is equivalent to the given
`String<class_String>`.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator ==**(right:
`StringName<class_StringName>`)
`🔗<class_StringName_operator_eq_StringName>`

Returns `true` if the **StringName** and `right` refer to the same name.
Comparisons between **StringName**s are much faster than regular
`String<class_String>` comparisons.

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &gt;**(right:
`StringName<class_StringName>`)
`🔗<class_StringName_operator_gt_StringName>`

Returns `true` if the left **StringName**'s pointer comes after `right`.
Note that this will not match their [Unicode
order](https://en.wikipedia.org/wiki/List_of_Unicode_characters).

classref-item-separator

------------------------------------------------------------------------

classref-operator

`bool<class_bool>` **operator &gt;=**(right:
`StringName<class_StringName>`)
`🔗<class_StringName_operator_gte_StringName>`

Returns `true` if the left **StringName**'s pointer comes after `right`
or if they are the same. Note that this will not match their [Unicode
order](https://en.wikipedia.org/wiki/List_of_Unicode_characters).
