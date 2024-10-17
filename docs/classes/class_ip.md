github\_url  
hide

# IP

**Inherits:** `Object<class_Object>`

Internet protocol (IP) support functions such as DNS resolution.

classref-introduction-group

## Description

IP contains support functions for the Internet Protocol (IP). TCP/IP
support is in different classes (see
`StreamPeerTCP<class_StreamPeerTCP>` and `TCPServer<class_TCPServer>`).
IP provides DNS hostname resolution support, both blocking and threaded.

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

## Enumerations

classref-enumeration

enum **ResolverStatus**: `🔗<enum_IP_ResolverStatus>`

classref-enumeration-constant

`ResolverStatus<enum_IP_ResolverStatus>` **RESOLVER\_STATUS\_NONE** =
`0`

DNS hostname resolver status: No status.

classref-enumeration-constant

`ResolverStatus<enum_IP_ResolverStatus>` **RESOLVER\_STATUS\_WAITING** =
`1`

DNS hostname resolver status: Waiting.

classref-enumeration-constant

`ResolverStatus<enum_IP_ResolverStatus>` **RESOLVER\_STATUS\_DONE** =
`2`

DNS hostname resolver status: Done.

classref-enumeration-constant

`ResolverStatus<enum_IP_ResolverStatus>` **RESOLVER\_STATUS\_ERROR** =
`3`

DNS hostname resolver status: Error.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **Type**: `🔗<enum_IP_Type>`

classref-enumeration-constant

`Type<enum_IP_Type>` **TYPE\_NONE** = `0`

Address type: None.

classref-enumeration-constant

`Type<enum_IP_Type>` **TYPE\_IPV4** = `1`

Address type: Internet protocol version 4 (IPv4).

classref-enumeration-constant

`Type<enum_IP_Type>` **TYPE\_IPV6** = `2`

Address type: Internet protocol version 6 (IPv6).

classref-enumeration-constant

`Type<enum_IP_Type>` **TYPE\_ANY** = `3`

Address type: Any.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**RESOLVER\_MAX\_QUERIES** = `256`
`🔗<class_IP_constant_RESOLVER_MAX_QUERIES>`

Maximum number of concurrent DNS resolver queries allowed,
`RESOLVER_INVALID_ID<class_IP_constant_RESOLVER_INVALID_ID>` is returned
if exceeded.

classref-constant

**RESOLVER\_INVALID\_ID** = `-1`
`🔗<class_IP_constant_RESOLVER_INVALID_ID>`

Invalid ID constant. Returned if
`RESOLVER_MAX_QUERIES<class_IP_constant_RESOLVER_MAX_QUERIES>` is
exceeded.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **clear\_cache**(hostname:
`String<class_String>` = "") `🔗<class_IP_method_clear_cache>`

Removes all of a `hostname`'s cached references. If no `hostname` is
given, all cached IP addresses are removed.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **erase\_resolve\_item**(id: `int<class_int>`)
`🔗<class_IP_method_erase_resolve_item>`

Removes a given item `id` from the queue. This should be used to free a
queue after it has completed to enable more queries to happen.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>` **get\_local\_addresses**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_IP_method_get_local_addresses>`

Returns all the user's current IPv4 and IPv6 addresses as an array.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>`\[`Dictionary<class_Dictionary>`\]
**get\_local\_interfaces**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_IP_method_get_local_interfaces>`

Returns all network adapters as an array.

Each adapter is a dictionary of the form:

    {
        "index": "1", # Interface index.
        "name": "eth0", # Interface name.
        "friendly": "Ethernet One", # A friendly name (might be empty).
        "addresses": ["192.168.1.101"], # An array of IP addresses associated to this interface.
    }

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_resolve\_item\_address**(id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_IP_method_get_resolve_item_address>`

Returns a queued hostname's IP address, given its queue `id`. Returns an
empty string on error or if resolution hasn't happened yet (see
`get_resolve_item_status<class_IP_method_get_resolve_item_status>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Array<class_Array>` **get\_resolve\_item\_addresses**(id:
`int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_IP_method_get_resolve_item_addresses>`

Returns resolved addresses, or an empty array if an error happened or
resolution didn't happen yet (see
`get_resolve_item_status<class_IP_method_get_resolve_item_status>`).

classref-item-separator

------------------------------------------------------------------------

classref-method

`ResolverStatus<enum_IP_ResolverStatus>`
**get\_resolve\_item\_status**(id: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_IP_method_get_resolve_item_status>`

Returns a queued hostname's status as a
`ResolverStatus<enum_IP_ResolverStatus>` constant, given its queue `id`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **resolve\_hostname**(host:
`String<class_String>`, ip\_type: `Type<enum_IP_Type>` = 3)
`🔗<class_IP_method_resolve_hostname>`

Returns a given hostname's IPv4 or IPv6 address when resolved
(blocking-type method). The address type returned depends on the
`Type<enum_IP_Type>` constant given as `ip_type`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedStringArray<class_PackedStringArray>`
**resolve\_hostname\_addresses**(host: `String<class_String>`, ip\_type:
`Type<enum_IP_Type>` = 3)
`🔗<class_IP_method_resolve_hostname_addresses>`

Resolves a given hostname in a blocking way. Addresses are returned as
an `Array<class_Array>` of IPv4 or IPv6 addresses depending on
`ip_type`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **resolve\_hostname\_queue\_item**(host:
`String<class_String>`, ip\_type: `Type<enum_IP_Type>` = 3)
`🔗<class_IP_method_resolve_hostname_queue_item>`

Creates a queue item to resolve a hostname to an IPv4 or IPv6 address
depending on the `Type<enum_IP_Type>` constant given as `ip_type`.
Returns the queue ID if successful, or
`RESOLVER_INVALID_ID<class_IP_constant_RESOLVER_INVALID_ID>` on error.
