github\_url  
hide

# StreamPeer

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

**Inherited By:** `StreamPeerBuffer<class_StreamPeerBuffer>`,
`StreamPeerExtension<class_StreamPeerExtension>`,
`StreamPeerGZIP<class_StreamPeerGZIP>`,
`StreamPeerTCP<class_StreamPeerTCP>`,
`StreamPeerTLS<class_StreamPeerTLS>`

Abstract base class for interacting with streams.

classref-introduction-group

## Description

StreamPeer is an abstract base class mostly used for stream-based
protocols (such as TCP). It provides an API for sending and receiving
data through streams as raw data or strings.

\*\*Note:\*\* When exporting to Android, make sure to enable the
`INTERNET` permission in the Android export preset before exporting the
project or using one-click deploy. Otherwise, network communication of
any kind will be blocked by Android.

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

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **big\_endian** = `false`
`🔗<class_StreamPeer_property_big_endian>`

classref-property-setget

-   `void (No return value.)` **set\_big\_endian**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_big\_endian\_enabled**()

If `true`, this **StreamPeer** will using big-endian format for encoding
and decoding.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_8**() `🔗<class_StreamPeer_method_get_8>`

Gets a signed byte from the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_16**() `🔗<class_StreamPeer_method_get_16>`

Gets a signed 16-bit value from the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_32**() `🔗<class_StreamPeer_method_get_32>`

Gets a signed 32-bit value from the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_64**() `🔗<class_StreamPeer_method_get_64>`

Gets a signed 64-bit value from the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_available\_bytes**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_StreamPeer_method_get_available_bytes>`

Returns the number of bytes this **StreamPeer** has available.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_data**(bytes: `int<class_int>`)
`🔗<class_StreamPeer_method_get_data>`

Returns a chunk data with the received bytes. The number of bytes to be
received can be requested in the `bytes` argument. If not enough bytes
are available, the function will block until the desired amount is
received. This function returns two values, an
`Error<enum_@GlobalScope_Error>` code and a data array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_double**()
`🔗<class_StreamPeer_method_get_double>`

Gets a double-precision float from the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_float**()
`🔗<class_StreamPeer_method_get_float>`

Gets a single-precision float from the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_partial\_data**(bytes: `int<class_int>`)
`🔗<class_StreamPeer_method_get_partial_data>`

Returns a chunk data with the received bytes. The number of bytes to be
received can be requested in the "bytes" argument. If not enough bytes
are available, the function will return how many were actually received.
This function returns two values, an `Error<enum_@GlobalScope_Error>`
code, and a data array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_string**(bytes: `int<class_int>` = -1)
`🔗<class_StreamPeer_method_get_string>`

Gets an ASCII string with byte-length `bytes` from the stream. If
`bytes` is negative (default) the length will be read from the stream
using the reverse process of
`put_string<class_StreamPeer_method_put_string>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_u8**() `🔗<class_StreamPeer_method_get_u8>`

Gets an unsigned byte from the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_u16**() `🔗<class_StreamPeer_method_get_u16>`

Gets an unsigned 16-bit value from the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_u32**() `🔗<class_StreamPeer_method_get_u32>`

Gets an unsigned 32-bit value from the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_u64**() `🔗<class_StreamPeer_method_get_u64>`

Gets an unsigned 64-bit value from the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_utf8\_string**(bytes: `int<class_int>` =
-1) `🔗<class_StreamPeer_method_get_utf8_string>`

Gets a UTF-8 string with byte-length `bytes` from the stream (this
decodes the string sent as UTF-8). If `bytes` is negative (default) the
length will be read from the stream using the reverse process of
`put_utf8_string<class_StreamPeer_method_put_utf8_string>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Variant<class_Variant>` **get\_var**(allow\_objects: `bool<class_bool>`
= false) `🔗<class_StreamPeer_method_get_var>`

Gets a Variant from the stream. If `allow_objects` is `true`, decoding
objects is allowed.

Internally, this uses the same decoding mechanism as the
`@GlobalScope.bytes_to_var<class_@GlobalScope_method_bytes_to_var>`
method.

\*\*Warning:\*\* Deserialized objects can contain code which gets
executed. Do not use this option if the serialized object comes from
untrusted sources to avoid potential security threats such as remote
code execution.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_8**(value: `int<class_int>`)
`🔗<class_StreamPeer_method_put_8>`

Puts a signed byte into the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_16**(value: `int<class_int>`)
`🔗<class_StreamPeer_method_put_16>`

Puts a signed 16-bit value into the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_32**(value: `int<class_int>`)
`🔗<class_StreamPeer_method_put_32>`

Puts a signed 32-bit value into the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_64**(value: `int<class_int>`)
`🔗<class_StreamPeer_method_put_64>`

Puts a signed 64-bit value into the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **put\_data**(data:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_StreamPeer_method_put_data>`

Sends a chunk of data through the connection, blocking if necessary
until the data is done sending. This function returns an
`Error<enum_@GlobalScope_Error>` code.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_double**(value: `float<class_float>`)
`🔗<class_StreamPeer_method_put_double>`

Puts a double-precision float into the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_float**(value: `float<class_float>`)
`🔗<class_StreamPeer_method_put_float>`

Puts a single-precision float into the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **put\_partial\_data**(data:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_StreamPeer_method_put_partial_data>`

Sends a chunk of data through the connection. If all the data could not
be sent at once, only part of it will. This function returns two values,
an `Error<enum_@GlobalScope_Error>` code and an integer, describing how
much data was actually sent.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_string**(value: `String<class_String>`)
`🔗<class_StreamPeer_method_put_string>`

Puts a zero-terminated ASCII string into the stream prepended by a
32-bit unsigned integer representing its size.

\*\*Note:\*\* To put an ASCII string without prepending its size, you
can use `put_data<class_StreamPeer_method_put_data>`:

gdscript

put\_data("Hello world".to\_ascii\_buffer())

csharp

PutData("Hello World".ToAsciiBuffer());

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_u8**(value: `int<class_int>`)
`🔗<class_StreamPeer_method_put_u8>`

Puts an unsigned byte into the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_u16**(value: `int<class_int>`)
`🔗<class_StreamPeer_method_put_u16>`

Puts an unsigned 16-bit value into the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_u32**(value: `int<class_int>`)
`🔗<class_StreamPeer_method_put_u32>`

Puts an unsigned 32-bit value into the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_u64**(value: `int<class_int>`)
`🔗<class_StreamPeer_method_put_u64>`

Puts an unsigned 64-bit value into the stream.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_utf8\_string**(value:
`String<class_String>`) `🔗<class_StreamPeer_method_put_utf8_string>`

Puts a zero-terminated UTF-8 string into the stream prepended by a 32
bits unsigned integer representing its size.

\*\*Note:\*\* To put a UTF-8 string without prepending its size, you can
use `put_data<class_StreamPeer_method_put_data>`:

gdscript

put\_data("Hello world".to\_utf8\_buffer())

csharp

PutData("Hello World".ToUtf8Buffer());

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **put\_var**(value: `Variant<class_Variant>`,
full\_objects: `bool<class_bool>` = false)
`🔗<class_StreamPeer_method_put_var>`

Puts a Variant into the stream. If `full_objects` is `true` encoding
objects is allowed (and can potentially include code).

Internally, this uses the same encoding mechanism as the
`@GlobalScope.var_to_bytes<class_@GlobalScope_method_var_to_bytes>`
method.
