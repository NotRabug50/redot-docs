github\_url  
hide

# CodeHighlighter

**Inherits:** `SyntaxHighlighter<class_SyntaxHighlighter>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A syntax highlighter intended for code.

classref-introduction-group

## Description

By adjusting various properties of this resource, you can change the
colors of strings, comments, numbers, and other text patterns inside a
`TextEdit<class_TextEdit>` control.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Dictionary<class_Dictionary>` **color\_regions** = `{}`
`🔗<class_CodeHighlighter_property_color_regions>`

classref-property-setget

-   `void (No return value.)` **set\_color\_regions**(value:
    `Dictionary<class_Dictionary>`)
-   `Dictionary<class_Dictionary>` **get\_color\_regions**()

Sets the color regions. All existing regions will be removed. The
`Dictionary<class_Dictionary>` key is the region start and end key,
separated by a space. The value is the region color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **function\_color** = `Color(0, 0, 0, 1)`
`🔗<class_CodeHighlighter_property_function_color>`

classref-property-setget

-   `void (No return value.)` **set\_function\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_function\_color**()

Sets color for functions. A function is a non-keyword string followed by
a '('.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Dictionary<class_Dictionary>` **keyword\_colors** = `{}`
`🔗<class_CodeHighlighter_property_keyword_colors>`

classref-property-setget

-   `void (No return value.)` **set\_keyword\_colors**(value:
    `Dictionary<class_Dictionary>`)
-   `Dictionary<class_Dictionary>` **get\_keyword\_colors**()

Sets the keyword colors. All existing keywords will be removed. The
`Dictionary<class_Dictionary>` key is the keyword. The value is the
keyword color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Dictionary<class_Dictionary>` **member\_keyword\_colors** = `{}`
`🔗<class_CodeHighlighter_property_member_keyword_colors>`

classref-property-setget

-   `void (No return value.)` **set\_member\_keyword\_colors**(value:
    `Dictionary<class_Dictionary>`)
-   `Dictionary<class_Dictionary>` **get\_member\_keyword\_colors**()

Sets the member keyword colors. All existing member keyword will be
removed. The `Dictionary<class_Dictionary>` key is the member keyword.
The value is the member keyword color.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **member\_variable\_color** = `Color(0, 0, 0, 1)`
`🔗<class_CodeHighlighter_property_member_variable_color>`

classref-property-setget

-   `void (No return value.)` **set\_member\_variable\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_member\_variable\_color**()

Sets color for member variables. A member variable is non-keyword,
non-function string proceeded with a '.'.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **number\_color** = `Color(0, 0, 0, 1)`
`🔗<class_CodeHighlighter_property_number_color>`

classref-property-setget

-   `void (No return value.)` **set\_number\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_number\_color**()

Sets the color for numbers.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **symbol\_color** = `Color(0, 0, 0, 1)`
`🔗<class_CodeHighlighter_property_symbol_color>`

classref-property-setget

-   `void (No return value.)` **set\_symbol\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_symbol\_color**()

Sets the color for symbols.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_color\_region**(start\_key:
`String<class_String>`, end\_key: `String<class_String>`, color:
`Color<class_Color>`, line\_only: `bool<class_bool>` = false)
`🔗<class_CodeHighlighter_method_add_color_region>`

Adds a color region (such as for comments or strings) from `start_key`
to `end_key`. Both keys should be symbols, and `start_key` must not be
shared with other delimiters.

If `line_only` is `true` or `end_key` is an empty
`String<class_String>`, the region does not carry over to the next line.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **add\_keyword\_color**(keyword:
`String<class_String>`, color: `Color<class_Color>`)
`🔗<class_CodeHighlighter_method_add_keyword_color>`

Sets the color for a keyword.

The keyword cannot contain any symbols except '\_'.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**add\_member\_keyword\_color**(member\_keyword: `String<class_String>`,
color: `Color<class_Color>`)
`🔗<class_CodeHighlighter_method_add_member_keyword_color>`

Sets the color for a member keyword.

The member keyword cannot contain any symbols except '\_'.

It will not be highlighted if preceded by a '.'.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_color\_regions**()
`🔗<class_CodeHighlighter_method_clear_color_regions>`

Removes all color regions.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_keyword\_colors**()
`🔗<class_CodeHighlighter_method_clear_keyword_colors>`

Removes all keywords.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_member\_keyword\_colors**()
`🔗<class_CodeHighlighter_method_clear_member_keyword_colors>`

Removes all member keywords.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_keyword\_color**(keyword:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeHighlighter_method_get_keyword_color>`

Returns the color for a keyword.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Color<class_Color>` **get\_member\_keyword\_color**(member\_keyword:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeHighlighter_method_get_member_keyword_color>`

Returns the color for a member keyword.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_color\_region**(start\_key:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeHighlighter_method_has_color_region>`

Returns `true` if the start key exists, else `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_keyword\_color**(keyword:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeHighlighter_method_has_keyword_color>`

Returns `true` if the keyword exists, else `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **has\_member\_keyword\_color**(member\_keyword:
`String<class_String>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_CodeHighlighter_method_has_member_keyword_color>`

Returns `true` if the member keyword exists, else `false`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_color\_region**(start\_key:
`String<class_String>`)
`🔗<class_CodeHighlighter_method_remove_color_region>`

Removes the color region that uses that start key.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_keyword\_color**(keyword:
`String<class_String>`)
`🔗<class_CodeHighlighter_method_remove_keyword_color>`

Removes the keyword.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)`
**remove\_member\_keyword\_color**(member\_keyword:
`String<class_String>`)
`🔗<class_CodeHighlighter_method_remove_member_keyword_color>`

Removes the member keyword.
