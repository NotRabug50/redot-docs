github\_url  
hide

# JSON

**Inherits:** `Resource<class_Resource>` **&lt;**
`RefCounted<class_RefCounted>` **&lt;** `Object<class_Object>`

Helper class for creating and parsing JSON data.

classref-introduction-group

## Description

The **JSON** class enables all data types to be converted to and from a
JSON string. This is useful for serializing data, e.g. to save to a file
or send over the network.

`stringify<class_JSON_method_stringify>` is used to convert any data
type into a JSON string.

`parse<class_JSON_method_parse>` is used to convert any existing JSON
data into a `Variant<class_Variant>` that can be used within Godot. If
successfully parsed, use `data<class_JSON_property_data>` to retrieve
the `Variant<class_Variant>`, and use
`@GlobalScope.typeof<class_@GlobalScope_method_typeof>` to check if the
Variant's type is what you expect. JSON Objects are converted into a
`Dictionary<class_Dictionary>`, but JSON data can be used to store
`Array<class_Array>`s, numbers, `String<class_String>`s and even just a
boolean.

    var data_to_send = ["a", "b", "c"]
    var json_string = JSON.stringify(data_to_send)
    # Save data
    # ...
    # Retrieve data
    var json = JSON.new()
    var error = json.parse(json_string)
    if error == OK:
        var data_received = json.data
        if typeof(data_received) == TYPE_ARRAY:
            print(data_received) # Prints array
        else:
            print("Unexpected data")
    else:
        print("JSON Parse Error: ", json.get_error_message(), " in ", json_string, " at line ", json.get_error_line())

Alternatively, you can parse strings using the static
`parse_string<class_JSON_method_parse_string>` method, but it doesn't
handle errors.

    var data = JSON.parse_string(json_string) # Returns null if parsing failed.

\*\*Note:\*\* Both parse methods do not fully comply with the JSON
specification:

-   Trailing commas in arrays or objects are ignored, instead of causing
    a parser error.
-   New line and tab characters are accepted in string literals, and are
    treated like their corresponding escape sequences `\n` and `\t`.
-   Numbers are parsed using
    `String.to_float<class_String_method_to_float>` which is generally
    more lax than the JSON specification.
-   Certain errors, such as invalid Unicode sequences, do not cause a
    parser error. Instead, the string is cleaned up and an error is
    logged to the console.

classref-reftable-group

## Properties

<table>
<tbody>
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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Variant<class_Variant>` **data** = `null`
`🔗<class_JSON_property_data>`

classref-property-setget

-   `void (No return value.)` **set\_data**(value:
    `Variant<class_Variant>`)
-   `Variant<class_Variant>` **get\_data**()

Contains the parsed JSON data in `Variant<class_Variant>` form.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Variant<class_Variant>` **from\_native**(variant:
`Variant<class_Variant>`, allow\_classes: `bool<class_bool>` = false,
allow\_scripts: `bool<class_bool>` = false)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_JSON_method_from_native>`

Converts a native engine type to a JSON-compliant dictionary.

By default, classes and scripts are ignored for security reasons, unless
`allow_classes` or `allow_scripts` are specified.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_error\_line**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_JSON_method_get_error_line>`

Returns `0` if the last call to `parse<class_JSON_method_parse>` was
successful, or the line number where the parse failed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_error\_message**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_JSON_method_get_error_message>`

Returns an empty string if the last call to
`parse<class_JSON_method_parse>` was successful, or the error message if
it failed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_parsed\_text**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_JSON_method_get_parsed_text>`

Return the text parsed by `parse<class_JSON_method_parse>` (requires
passing `keep_text` to `parse<class_JSON_method_parse>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **parse**(json\_text:
`String<class_String>`, keep\_text: `bool<class_bool>` = false)
`🔗<class_JSON_method_parse>`

Attempts to parse the `json_text` provided.

Returns an `Error<enum_@GlobalScope_Error>`. If the parse was
successful, it returns `@GlobalScope.OK<class_@GlobalScope_constant_OK>`
and the result can be retrieved using `data<class_JSON_property_data>`.
If unsuccessful, use `get_error_line<class_JSON_method_get_error_line>`
and `get_error_message<class_JSON_method_get_error_message>` to identify
the source of the failure.

Non-static variant of `parse_string<class_JSON_method_parse_string>`, if
you want custom error handling.

The optional `keep_text` argument instructs the parser to keep a copy of
the original text. This text can be obtained later by using the
`get_parsed_text<class_JSON_method_get_parsed_text>` function and is
used when saving the resource (instead of generating new text from
`data<class_JSON_property_data>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **parse\_string**(json\_string:
`String<class_String>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_JSON_method_parse_string>`

Attempts to parse the `json_string` provided and returns the parsed
data. Returns `null` if parse failed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **stringify**(data: `Variant<class_Variant>`,
indent: `String<class_String>` = "", sort\_keys: `bool<class_bool>` =
true, full\_precision: `bool<class_bool>` = false)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_JSON_method_stringify>`

Converts a `Variant<class_Variant>` var to JSON text and returns the
result. Useful for serializing data to store or send over the network.

\*\*Note:\*\* The JSON specification does not define integer or float
types, but only a *number* type. Therefore, converting a Variant to JSON
text will convert all numerical values to `float<class_float>` types.

\*\*Note:\*\* If `full_precision` is `true`, when stringifying floats,
the unreliable digits are stringified in addition to the reliable digits
to guarantee exact decoding.

The `indent` parameter controls if and how something is indented; its
contents will be used where there should be an indent in the output.
Even spaces like `"   "` will work. `\t` and `\n` can also be used for a
tab indent, or to make a newline for each indent respectively.

\*\*Example output:\*\*

    ## JSON.stringify(my_dictionary)
    {"name":"my_dictionary","version":"1.0.0","entities":[{"name":"entity_0","value":"value_0"},{"name":"entity_1","value":"value_1"}]}

    ## JSON.stringify(my_dictionary, "\t")
    {
        "name": "my_dictionary",
        "version": "1.0.0",
        "entities": [
            {
                "name": "entity_0",
                "value": "value_0"
            },
            {
                "name": "entity_1",
                "value": "value_1"
            }
        ]
    }

    ## JSON.stringify(my_dictionary, "...")
    {
    ..."name": "my_dictionary",
    ..."version": "1.0.0",
    ..."entities": [
    ......{
    ........."name": "entity_0",
    ........."value": "value_0"
    ......},
    ......{
    ........."name": "entity_1",
    ........."value": "value_1"
    ......}
    ...]
    }

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **to\_native**(json: `Variant<class_Variant>`,
allow\_classes: `bool<class_bool>` = false, allow\_scripts:
`bool<class_bool>` = false)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_JSON_method_to_native>`

Converts a JSON-compliant dictionary that was created with
`from_native<class_JSON_method_from_native>` back to native engine
types.

By default, classes and scripts are ignored for security reasons, unless
`allow_classes` or `allow_scripts` are specified.
