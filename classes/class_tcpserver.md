github\_url  
hide

# TCPServer

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

A TCP server.

classref-introduction-group

## Description

A TCP server. Listens to connections on a port and returns a
`StreamPeerTCP<class_StreamPeerTCP>` when it gets an incoming
connection.

\*\*Note:\*\* When exporting to Android, make sure to enable the
`INTERNET` permission in the Android export preset before exporting the
project or using one-click deploy. Otherwise, network communication of
any kind will be blocked by Android.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **get\_local\_port**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TCPServer_method_get_local_port>`

Returns the local port this server is listening to.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_connection\_available**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TCPServer_method_is_connection_available>`

Returns `true` if a connection is available for taking.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_listening**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TCPServer_method_is_listening>`

Returns `true` if the server is currently listening for connections.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **listen**(port: `int<class_int>`,
bind\_address: `String<class_String>` = "\*")
`🔗<class_TCPServer_method_listen>`

Listen on the `port` binding to `bind_address`.

If `bind_address` is set as `"*"` (default), the server will listen on
all available addresses (both IPv4 and IPv6).

If `bind_address` is set as `"0.0.0.0"` (for IPv4) or `"::"` (for IPv6),
the server will listen on all available addresses matching that IP type.

If `bind_address` is set to any valid address (e.g. `"192.168.1.101"`,
`"::1"`, etc.), the server will only listen on the interface with that
address (or fail if no interface with the given address exists).

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **stop**() `🔗<class_TCPServer_method_stop>`

Stops listening.

classref-item-separator

------------------------------------------------------------------------

classref-method

`StreamPeerTCP<class_StreamPeerTCP>` **take\_connection**()
`🔗<class_TCPServer_method_take_connection>`

If a connection is available, returns a StreamPeerTCP with the
connection.
