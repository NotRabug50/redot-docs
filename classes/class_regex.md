github\_url  
hide

# RegEx

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Class for searching text for patterns using regular expressions.

classref-introduction-group

## Description

A regular expression (or regex) is a compact language that can be used
to recognize strings that follow a specific pattern, such as URLs, email
addresses, complete sentences, etc. For example, a regex of `ab[0-9]`
would find any string that is `ab` followed by any number from `0` to
`9`. For a more in-depth look, you can easily find various tutorials and
detailed explanations on the Internet.

To begin, the RegEx object needs to be compiled with the search pattern
using `compile<class_RegEx_method_compile>` before it can be used.

    var regex = RegEx.new()
    regex.compile("\\w-(\\d+)")

The search pattern must be escaped first for GDScript before it is
escaped for the expression. For example, `compile("\\d+")` would be read
by RegEx as `\d+`. Similarly, `compile("\"(?:\\\\.|[^\"])*\"")` would be
read as `"(?:\\.|[^"])*"`. In GDScript, you can also use raw string
literals (r-strings). For example, `compile(r'"(?:\\.|[^"])*"')` would
be read the same.

Using `search<class_RegEx_method_search>`, you can find the pattern
within the given text. If a pattern is found,
`RegExMatch<class_RegExMatch>` is returned and you can retrieve details
of the results using methods such as
`RegExMatch.get_string<class_RegExMatch_method_get_string>` and
`RegExMatch.get_start<class_RegExMatch_method_get_start>`.

    var regex = RegEx.new()
    regex.compile("\\w-(\\d+)")
    var result = regex.search("abc n-0123")
    if result:
        print(result.get_string()) # Would print n-0123

The results of capturing groups `()` can be retrieved by passing the
group number to the various methods in `RegExMatch<class_RegExMatch>`.
Group 0 is the default and will always refer to the entire pattern. In
the above example, calling `result.get_string(1)` would give you `0123`.

This version of RegEx also supports named capturing groups, and the
names can be used to retrieve the results. If two or more groups have
the same name, the name would only refer to the first one with a match.

    var regex = RegEx.new()
    regex.compile("d(?<digit>[0-9]+)|x(?<digit>[0-9a-f]+)")
    var result = regex.search("the number is x2f")
    if result:
        print(result.get_string("digit")) # Would print 2f

If you need to process multiple results,
`search_all<class_RegEx_method_search_all>` generates a list of all
non-overlapping results. This can be combined with a `for` loop for
convenience.

    for result in regex.search_all("d01, d03, d0c, x3f and x42"):
        print(result.get_string("digit"))
    # Would print 01 03 0 3f 42

\*\*Example of splitting a string using a RegEx:\*\*

    var regex = RegEx.new()
    regex.compile("\\S+") # Negated whitespace character class.
    var results = []
    for result in regex.search_all("One  Two \n\tThree"):
        results.push_back(result.get_string())
    # The `results` array now contains "One", "Two", "Three".

\*\*Note:\*\* Godot's regex implementation is based on the
[PCRE2](https://www.pcre.org/) library. You can view the full pattern
reference
[here](https://www.pcre.org/current/doc/html/pcre2pattern.html).

\*\*Tip:\*\* You can use [Regexr](https://regexr.com/) to test regular
expressions online.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **clear**() `🔗<class_RegEx_method_clear>`

This method resets the state of the object, as if it was freshly
created. Namely, it unassigns the regular expression of this object.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **compile**(pattern:
`String<class_String>`, show\_error: `bool<class_bool>` = true)
`🔗<class_RegEx_method_compile>`

Compiles and assign the search pattern to use. Returns
`@GlobalScope.OK<class_@GlobalScope_constant_OK>` if the compilation is
successful. If compilation fails, returns
`@GlobalScope.FAILED<class_@GlobalScope_constant_FAILED>` and when
`show_error` is `true`, details are printed to standard output.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RegEx<class_RegEx>` **create\_from\_string**(pattern:
`String<class_String>`, show\_error: `bool<class_bool>` = true)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_RegEx_method_create_from_string>`

Creates and compiles a new **RegEx** object. See also
`compile<class_RegEx_method_compile>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_group\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RegEx_method_get_group_count>`

Returns the number of capturing groups in compiled pattern.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_names**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RegEx_method_get_names>`

Returns an array of names of named capturing groups in the compiled
pattern. They are ordered by appearance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_pattern**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RegEx_method_get_pattern>`

Returns the original search pattern that was compiled.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RegEx_method_is_valid>`

Returns whether this object has a valid search pattern assigned.

classref-item-separator

------------------------------------------------------------------------

classref-method

`RegExMatch<class_RegExMatch>` **search**(subject:
`String<class_String>`, offset: `int<class_int>` = 0, end:
`int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RegEx_method_search>`

Searches the text for the compiled pattern. Returns a
`RegExMatch<class_RegExMatch>` container of the first matching result if
found, otherwise `null`.

The region to search within can be specified with `offset` and `end`.
This is useful when searching for another match in the same `subject` by
calling this method again after a previous success. Note that setting
these parameters differs from passing over a shortened string. For
example, the start anchor `^` is not affected by `offset`, and the
character before `offset` will be checked for the word boundary `\b`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`RegExMatch<class_RegExMatch>`\]
**search\_all**(subject: `String<class_String>`, offset:
`int<class_int>` = 0, end: `int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RegEx_method_search_all>`

Searches the text for the compiled pattern. Returns an array of
`RegExMatch<class_RegExMatch>` containers for each non-overlapping
result. If no results were found, an empty array is returned instead.

The region to search within can be specified with `offset` and `end`.
This is useful when searching for another match in the same `subject` by
calling this method again after a previous success. Note that setting
these parameters differs from passing over a shortened string. For
example, the start anchor `^` is not affected by `offset`, and the
character before `offset` will be checked for the word boundary `\b`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **sub**(subject: `String<class_String>`,
replacement: `String<class_String>`, all: `bool<class_bool>` = false,
offset: `int<class_int>` = 0, end: `int<class_int>` = -1)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_RegEx_method_sub>`

Searches the text for the compiled pattern and replaces it with the
specified string. Escapes and backreferences such as `$1` and `$name`
are expanded and resolved. By default, only the first instance is
replaced, but it can be changed for all instances (global replacement).

The region to search within can be specified with `offset` and `end`.
This is useful when searching for another match in the same `subject` by
calling this method again after a previous success. Note that setting
these parameters differs from passing over a shortened string. For
example, the start anchor `^` is not affected by `offset`, and the
character before `offset` will be checked for the word boundary `\b`.
