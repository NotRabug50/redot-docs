github\_url  
hide

# UPNP

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Universal Plug and Play (UPnP) functions for network device discovery,
querying and port forwarding.

classref-introduction-group

## Description

This class can be used to discover compatible
`UPNPDevice<class_UPNPDevice>`s on the local network and execute
commands on them, like managing port mappings (for port forwarding/NAT
traversal) and querying the local and remote network IP address. Note
that methods on this class are synchronous and block the calling thread.

To forward a specific port (here `7777`, note both
`discover<class_UPNP_method_discover>` and
`add_port_mapping<class_UPNP_method_add_port_mapping>` can return errors
that should be checked):

    var upnp = UPNP.new()
    upnp.discover()
    upnp.add_port_mapping(7777)

To close a specific port (e.g. after you have finished using it):

    upnp.delete_port_mapping(port)

\*\*Note:\*\* UPnP discovery blocks the current thread. To perform
discovery without blocking the main thread, use `Thread<class_Thread>`s
like this:

    # Emitted when UPnP port mapping setup is completed (regardless of success or failure).
    signal upnp_completed(error)

    # Replace this with your own server port number between 1024 and 65535.
    const SERVER_PORT = 3928
    var thread = null

    func _upnp_setup(server_port):
        # UPNP queries take some time.
        var upnp = UPNP.new()
        var err = upnp.discover()

        if err != OK:
            push_error(str(err))
            upnp_completed.emit(err)
            return

        if upnp.get_gateway() and upnp.get_gateway().is_valid_gateway():
            upnp.add_port_mapping(server_port, server_port, ProjectSettings.get_setting("application/config/name"), "UDP")
            upnp.add_port_mapping(server_port, server_port, ProjectSettings.get_setting("application/config/name"), "TCP")
            upnp_completed.emit(OK)

    func _ready():
        thread = Thread.new()
        thread.start(_upnp_setup.bind(SERVER_PORT))

    func _exit_tree():
        # Wait for thread finish here to handle game exit while the thread is running.
        thread.wait_to_finish()

\*\*Terminology:\*\* In the context of UPnP networking, "gateway" (or
"internet gateway device", short IGD) refers to network devices that
allow computers in the local network to access the internet ("wide area
network", WAN). These gateways are often also called "routers".

\*\*Pitfalls:\*\*

-   As explained above, these calls are blocking and shouldn't be run on
    the main thread, especially as they can block for multiple seconds
    at a time. Use threading!
-   Networking is physical and messy. Packets get lost in transit or get
    filtered, addresses, free ports and assigned mappings change, and
    devices may leave or join the network at any time. Be mindful of
    this, be diligent when checking and handling errors, and handle
    these gracefully if you can: add clear error UI, timeouts and re-try
    handling.
-   Port mappings may change (and be removed) at any time, and the
    remote/external IP address of the gateway can change likewise. You
    should consider re-querying the external IP and try to
    update/refresh the port mapping periodically (for example, every 5
    minutes and on networking failures).
-   Not all devices support UPnP, and some users disable UPnP support.
    You need to handle this (e.g. documenting and requiring the user to
    manually forward ports, or adding alternative methods of NAT
    traversal, like a relay/mirror server, or NAT hole punching,
    STUN/TURN, etc.).
-   Consider what happens on mapping conflicts. Maybe multiple users on
    the same network would like to play your game at the same time, or
    maybe another application uses the same port. Make the port
    configurable, and optimally choose a port automatically (re-trying
    with a different port on failure).

\*\*Further reading:\*\* If you want to know more about UPnP (and the
Internet Gateway Device (IGD) and Port Control Protocol (PCP)
specifically),
[Wikipedia](https://en.wikipedia.org/wiki/Universal_Plug_and_Play) is a
good first stop, the specification can be found at the [Open
Connectivity
Foundation](https://openconnectivity.org/developer/specifications/upnp-resources/upnp/)
and Godot's implementation is based on the [MiniUPnP
client](https://github.com/miniupnp/miniupnp).

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **UPNPResult**: `🔗<enum_UPNP_UPNPResult>`

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_SUCCESS** = `0`

UPNP command or discovery was successful.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_NOT\_AUTHORIZED** =
`1`

Not authorized to use the command on the `UPNPDevice<class_UPNPDevice>`.
May be returned when the user disabled UPNP on their router.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_PORT\_MAPPING\_NOT\_FOUND** = `2`

No port mapping was found for the given port, protocol combination on
the given `UPNPDevice<class_UPNPDevice>`.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_INCONSISTENT\_PARAMETERS** = `3`

Inconsistent parameters.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_NO\_SUCH\_ENTRY\_IN\_ARRAY** = `4`

No such entry in array. May be returned if a given port, protocol
combination is not found on an `UPNPDevice<class_UPNPDevice>`.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_ACTION\_FAILED** =
`5`

The action failed.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_SRC\_IP\_WILDCARD\_NOT\_PERMITTED** = `6`

The `UPNPDevice<class_UPNPDevice>` does not allow wildcard values for
the source IP address.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_EXT\_PORT\_WILDCARD\_NOT\_PERMITTED** = `7`

The `UPNPDevice<class_UPNPDevice>` does not allow wildcard values for
the external port.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_INT\_PORT\_WILDCARD\_NOT\_PERMITTED** = `8`

The `UPNPDevice<class_UPNPDevice>` does not allow wildcard values for
the internal port.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_REMOTE\_HOST\_MUST\_BE\_WILDCARD** = `9`

The remote host value must be a wildcard.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_EXT\_PORT\_MUST\_BE\_WILDCARD** = `10`

The external port value must be a wildcard.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_NO\_PORT\_MAPS\_AVAILABLE** = `11`

No port maps are available. May also be returned if port mapping
functionality is not available.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_CONFLICT\_WITH\_OTHER\_MECHANISM** = `12`

Conflict with other mechanism. May be returned instead of
`UPNP_RESULT_CONFLICT_WITH_OTHER_MAPPING<class_UPNP_constant_UPNP_RESULT_CONFLICT_WITH_OTHER_MAPPING>`
if a port mapping conflicts with an existing one.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_CONFLICT\_WITH\_OTHER\_MAPPING** = `13`

Conflict with an existing port mapping.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_SAME\_PORT\_VALUES\_REQUIRED** = `14`

External and internal port values must be the same.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>`
**UPNP\_RESULT\_ONLY\_PERMANENT\_LEASE\_SUPPORTED** = `15`

Only permanent leases are supported. Do not use the `duration` parameter
when adding port mappings.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_INVALID\_GATEWAY** =
`16`

Invalid gateway.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_INVALID\_PORT** =
`17`

Invalid port.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_INVALID\_PROTOCOL** =
`18`

Invalid protocol.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_INVALID\_DURATION** =
`19`

Invalid duration.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_INVALID\_ARGS** =
`20`

Invalid arguments.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_INVALID\_RESPONSE** =
`21`

Invalid response.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_INVALID\_PARAM** =
`22`

Invalid parameter.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_HTTP\_ERROR** = `23`

HTTP error.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_SOCKET\_ERROR** =
`24`

Socket error.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_MEM\_ALLOC\_ERROR** =
`25`

Error allocating memory.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_NO\_GATEWAY** = `26`

No gateway available. You may need to call
`discover<class_UPNP_method_discover>` first, or discovery didn't detect
any valid IGDs (InternetGatewayDevices).

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_NO\_DEVICES** = `27`

No devices available. You may need to call
`discover<class_UPNP_method_discover>` first, or discovery didn't detect
any valid `UPNPDevice<class_UPNPDevice>`s.

classref-enumeration-constant

`UPNPResult<enum_UPNP_UPNPResult>` **UPNP\_RESULT\_UNKNOWN\_ERROR** =
`28`

Unknown error.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **discover\_ipv6** = `false`
`🔗<class_UPNP_property_discover_ipv6>`

classref-property-setget

-   `void (No return value.)` **set\_discover\_ipv6**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_discover\_ipv6**()

If `true`, IPv6 is used for `UPNPDevice<class_UPNPDevice>` discovery.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **discover\_local\_port** = `0`
`🔗<class_UPNP_property_discover_local_port>`

classref-property-setget

-   `void (No return value.)` **set\_discover\_local\_port**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_discover\_local\_port**()

If `0`, the local port to use for discovery is chosen automatically by
the system. If `1`, discovery will be done from the source port 1900
(same as destination port). Otherwise, the value will be used as the
port.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **discover\_multicast\_if** = `""`
`🔗<class_UPNP_property_discover_multicast_if>`

classref-property-setget

-   `void (No return value.)` **set\_discover\_multicast\_if**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_discover\_multicast\_if**()

Multicast interface to use for discovery. Uses the default multicast
interface if empty.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **add\_device**(device:
`UPNPDevice<class_UPNPDevice>`) `🔗<class_UPNP_method_add_device>`

Adds the given `UPNPDevice<class_UPNPDevice>` to the list of discovered
devices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **add\_port\_mapping**(port: `int<class_int>`,
port\_internal: `int<class_int>` = 0, desc: `String<class_String>` = "",
proto: `String<class_String>` = "UDP", duration: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UPNP_method_add_port_mapping>`

Adds a mapping to forward the external `port` (between 1 and 65535,
although recommended to use port 1024 or above) on the default gateway
(see `get_gateway<class_UPNP_method_get_gateway>`) to the
`port_internal` on the local machine for the given protocol `proto`
(either `"TCP"` or `"UDP"`, with UDP being the default). If a port
mapping for the given port and protocol combination already exists on
that gateway device, this method tries to overwrite it. If that is not
desired, you can retrieve the gateway manually with
`get_gateway<class_UPNP_method_get_gateway>` and call
`add_port_mapping<class_UPNP_method_add_port_mapping>` on it, if any.
Note that forwarding a well-known port (below 1024) with UPnP may fail
depending on the device.

Depending on the gateway device, if a mapping for that port already
exists, it will either be updated or it will refuse this command due to
that conflict, especially if the existing mapping for that port wasn't
created via UPnP or points to a different network address (or device)
than this one.

If `port_internal` is `0` (the default), the same port number is used
for both the external and the internal port (the `port` value).

The description (`desc`) is shown in some routers management UIs and can
be used to point out which application added the mapping.

The mapping's lease `duration` can be limited by specifying a duration
in seconds. The default of `0` means no duration, i.e. a permanent lease
and notably some devices only support these permanent leases. Note that
whether permanent or not, this is only a request and the gateway may
still decide at any point to remove the mapping (which usually happens
on a reboot of the gateway, when its external IP address changes, or on
some models when it detects a port mapping has become inactive, i.e. had
no traffic for multiple minutes). If not `0` (permanent), the allowed
range according to spec is between `120` (2 minutes) and `86400` seconds
(24 hours).

See `UPNPResult<enum_UPNP_UPNPResult>` for possible return values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **clear\_devices**()
`🔗<class_UPNP_method_clear_devices>`

Clears the list of discovered devices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **delete\_port\_mapping**(port: `int<class_int>`,
proto: `String<class_String>` = "UDP")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UPNP_method_delete_port_mapping>`

Deletes the port mapping for the given port and protocol combination on
the default gateway (see `get_gateway<class_UPNP_method_get_gateway>`)
if one exists. `port` must be a valid port between 1 and 65535, `proto`
can be either `"TCP"` or `"UDP"`. May be refused for mappings pointing
to addresses other than this one, for well-known ports (below 1024), or
for mappings not added via UPnP. See `UPNPResult<enum_UPNP_UPNPResult>`
for possible return values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **discover**(timeout: `int<class_int>` = 2000, ttl:
`int<class_int>` = 2, device\_filter: `String<class_String>` =
"InternetGatewayDevice") `🔗<class_UPNP_method_discover>`

Discovers local `UPNPDevice<class_UPNPDevice>`s. Clears the list of
previously discovered devices.

Filters for IGD (InternetGatewayDevice) type devices by default, as
those manage port forwarding. `timeout` is the time to wait for
responses in milliseconds. `ttl` is the time-to-live; only touch this if
you know what you're doing.

See `UPNPResult<enum_UPNP_UPNPResult>` for possible return values.

classref-item-separator

------------------------------------------------------------------------

classref-method

`UPNPDevice<class_UPNPDevice>` **get\_device**(index: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UPNP_method_get_device>`

Returns the `UPNPDevice<class_UPNPDevice>` at the given `index`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **get\_device\_count**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UPNP_method_get_device_count>`

Returns the number of discovered `UPNPDevice<class_UPNPDevice>`s.

classref-item-separator

------------------------------------------------------------------------

classref-method

`UPNPDevice<class_UPNPDevice>` **get\_gateway**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UPNP_method_get_gateway>`

Returns the default gateway. That is the first discovered
`UPNPDevice<class_UPNPDevice>` that is also a valid IGD
(InternetGatewayDevice).

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **query\_external\_address**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UPNP_method_query_external_address>`

Returns the external `IP<class_IP>` address of the default gateway (see
`get_gateway<class_UPNP_method_get_gateway>`) as string. Returns an
empty string on error.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **remove\_device**(index: `int<class_int>`)
`🔗<class_UPNP_method_remove_device>`

Removes the device at `index` from the list of discovered devices.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_device**(index: `int<class_int>`,
device: `UPNPDevice<class_UPNPDevice>`)
`🔗<class_UPNP_method_set_device>`

Sets the device at `index` from the list of discovered devices to
`device`.
