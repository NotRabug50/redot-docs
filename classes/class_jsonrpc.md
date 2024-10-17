github\_url  
hide

# JSONRPC

**Inherits:** `Object<class_Object>`

A helper to handle dictionaries which look like JSONRPC documents.

classref-introduction-group

## Description

[JSON-RPC](https://www.jsonrpc.org/) is a standard which wraps a method
call in a `JSON<class_JSON>` object. The object has a particular
structure and identifies which method is called, the parameters to that
function, and carries an ID to keep track of responses. This class
implements that standard on top of `Dictionary<class_Dictionary>`; you
will have to convert between a `Dictionary<class_Dictionary>` and
`JSON<class_JSON>` with other functions.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ErrorCode**: `🔗<enum_JSONRPC_ErrorCode>`

classref-enumeration-constant

`ErrorCode<enum_JSONRPC_ErrorCode>` **PARSE\_ERROR** = `-32700`

The request could not be parsed as it was not valid by JSON standard
(`JSON.parse<class_JSON_method_parse>` failed).

classref-enumeration-constant

`ErrorCode<enum_JSONRPC_ErrorCode>` **INVALID\_REQUEST** = `-32600`

A method call was requested but the request's format is not valid.

classref-enumeration-constant

`ErrorCode<enum_JSONRPC_ErrorCode>` **METHOD\_NOT\_FOUND** = `-32601`

A method call was requested but no function of that name existed in the
JSONRPC subclass.

classref-enumeration-constant

`ErrorCode<enum_JSONRPC_ErrorCode>` **INVALID\_PARAMS** = `-32602`

A method call was requested but the given method parameters are not
valid. Not used by the built-in JSONRPC.

classref-enumeration-constant

`ErrorCode<enum_JSONRPC_ErrorCode>` **INTERNAL\_ERROR** = `-32603`

An internal error occurred while processing the request. Not used by the
built-in JSONRPC.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Dictionary<class_Dictionary>` **make\_notification**(method:
`String<class_String>`, params: `Variant<class_Variant>`)
`🔗<class_JSONRPC_method_make_notification>`

Returns a dictionary in the form of a JSON-RPC notification.
Notifications are one-shot messages which do not expect a response.

-   `method`: Name of the method being called.
-   `params`: An array or dictionary of parameters being passed to the
    method.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **make\_request**(method:
`String<class_String>`, params: `Variant<class_Variant>`, id:
`Variant<class_Variant>`) `🔗<class_JSONRPC_method_make_request>`

Returns a dictionary in the form of a JSON-RPC request. Requests are
sent to a server with the expectation of a response. The ID field is
used for the server to specify which exact request it is responding to.

-   `method`: Name of the method being called.
-   `params`: An array or dictionary of parameters being passed to the
    method.
-   `id`: Uniquely identifies this request. The server is expected to
    send a response with the same ID.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **make\_response**(result:
`Variant<class_Variant>`, id: `Variant<class_Variant>`)
`🔗<class_JSONRPC_method_make_response>`

When a server has received and processed a request, it is expected to
send a response. If you did not want a response then you need to have
sent a Notification instead.

-   `result`: The return value of the function which was called.
-   `id`: The ID of the request this response is targeted to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Dictionary<class_Dictionary>` **make\_response\_error**(code:
`int<class_int>`, message: `String<class_String>`, id:
`Variant<class_Variant>` = null)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_JSONRPC_method_make_response_error>`

Creates a response which indicates a previous reply has failed in some
way.

-   `code`: The error code corresponding to what kind of error this is.
    See the `ErrorCode<enum_JSONRPC_ErrorCode>` constants.
-   `message`: A custom message about this error.
-   `id`: The request this error is a response to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **process\_action**(action:
`Variant<class_Variant>`, recurse: `bool<class_bool>` = false)
`🔗<class_JSONRPC_method_process_action>`

Given a Dictionary which takes the form of a JSON-RPC request: unpack
the request and run it. Methods are resolved by looking at the field
called "method" and looking for an equivalently named function in the
JSONRPC object. If one is found that method is called.

To add new supported methods extend the JSONRPC class and call
`process_action<class_JSONRPC_method_process_action>` on your subclass.

`action`: The action to be run, as a Dictionary in the form of a
JSON-RPC request or notification.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **process\_string**(action:
`String<class_String>`) `🔗<class_JSONRPC_method_process_string>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_scope**(scope: `String<class_String>`,
target: `Object<class_Object>`) `🔗<class_JSONRPC_method_set_scope>`

There is currently no description for this method. Please help us by
`contributing one <doc_updating_the_class_reference>`!
