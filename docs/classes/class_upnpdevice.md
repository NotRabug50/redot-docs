github\_url  
hide

# UPNPDevice

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Universal Plug and Play (UPnP) device.

classref-introduction-group

## Description

Universal Plug and Play (UPnP) device. See `UPNP<class_UPNP>` for UPnP
discovery and utility functions. Provides low-level access to UPNP
control commands. Allows to manage port mappings (port forwarding) and
to query network information of the device (like local and external IP
address and status). Note that methods on this class are synchronous and
block the calling thread.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **IGDStatus**: `🔗<enum_UPNPDevice_IGDStatus>`

classref-enumeration-constant

`IGDStatus<enum_UPNPDevice_IGDStatus>` **IGD\_STATUS\_OK** = `0`

OK.

classref-enumeration-constant

`IGDStatus<enum_UPNPDevice_IGDStatus>` **IGD\_STATUS\_HTTP\_ERROR** =
`1`

HTTP error.

classref-enumeration-constant

`IGDStatus<enum_UPNPDevice_IGDStatus>` **IGD\_STATUS\_HTTP\_EMPTY** =
`2`

Empty HTTP response.

classref-enumeration-constant

`IGDStatus<enum_UPNPDevice_IGDStatus>` **IGD\_STATUS\_NO\_URLS** = `3`

**Deprecated:** This value is no longer used.

Returned response contained no URLs.

classref-enumeration-constant

`IGDStatus<enum_UPNPDevice_IGDStatus>` **IGD\_STATUS\_NO\_IGD** = `4`

Not a valid IGD.

classref-enumeration-constant

`IGDStatus<enum_UPNPDevice_IGDStatus>` **IGD\_STATUS\_DISCONNECTED** =
`5`

Disconnected.

classref-enumeration-constant

`IGDStatus<enum_UPNPDevice_IGDStatus>` **IGD\_STATUS\_UNKNOWN\_DEVICE**
= `6`

Unknown device.

classref-enumeration-constant

`IGDStatus<enum_UPNPDevice_IGDStatus>` **IGD\_STATUS\_INVALID\_CONTROL**
= `7`

Invalid control.

classref-enumeration-constant

`IGDStatus<enum_UPNPDevice_IGDStatus>` **IGD\_STATUS\_MALLOC\_ERROR** =
`8`

**Deprecated:** This value is no longer used.

Memory allocation error.

classref-enumeration-constant

`IGDStatus<enum_UPNPDevice_IGDStatus>` **IGD\_STATUS\_UNKNOWN\_ERROR** =
`9`

Unknown error.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`String<class_String>` **description\_url** = `""`
`🔗<class_UPNPDevice_property_description_url>`

classref-property-setget

-   `void (No return value.)` **set\_description\_url**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_description\_url**()

URL to the device description.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **igd\_control\_url** = `""`
`🔗<class_UPNPDevice_property_igd_control_url>`

classref-property-setget

-   `void (No return value.)` **set\_igd\_control\_url**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_igd\_control\_url**()

IDG control URL.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **igd\_our\_addr** = `""`
`🔗<class_UPNPDevice_property_igd_our_addr>`

classref-property-setget

-   `void (No return value.)` **set\_igd\_our\_addr**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_igd\_our\_addr**()

Address of the local machine in the network connecting it to this
**UPNPDevice**.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **igd\_service\_type** = `""`
`🔗<class_UPNPDevice_property_igd_service_type>`

classref-property-setget

-   `void (No return value.)` **set\_igd\_service\_type**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_igd\_service\_type**()

IGD service type.

classref-item-separator

------------------------------------------------------------------------

classref-property

`IGDStatus<enum_UPNPDevice_IGDStatus>` **igd\_status** = `9`
`🔗<class_UPNPDevice_property_igd_status>`

classref-property-setget

-   `void (No return value.)` **set\_igd\_status**(value:
    `IGDStatus<enum_UPNPDevice_IGDStatus>`)
-   `IGDStatus<enum_UPNPDevice_IGDStatus>` **get\_igd\_status**()

IGD status. See `IGDStatus<enum_UPNPDevice_IGDStatus>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`String<class_String>` **service\_type** = `""`
`🔗<class_UPNPDevice_property_service_type>`

classref-property-setget

-   `void (No return value.)` **set\_service\_type**(value:
    `String<class_String>`)
-   `String<class_String>` **get\_service\_type**()

Service type.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`int<class_int>` **add\_port\_mapping**(port: `int<class_int>`,
port\_internal: `int<class_int>` = 0, desc: `String<class_String>` = "",
proto: `String<class_String>` = "UDP", duration: `int<class_int>` = 0)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UPNPDevice_method_add_port_mapping>`

Adds a port mapping to forward the given external port on this
**UPNPDevice** for the given protocol to the local machine. See
`UPNP.add_port_mapping<class_UPNP_method_add_port_mapping>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`int<class_int>` **delete\_port\_mapping**(port: `int<class_int>`,
proto: `String<class_String>` = "UDP")
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UPNPDevice_method_delete_port_mapping>`

Deletes the port mapping identified by the given port and protocol
combination on this device. See
`UPNP.delete_port_mapping<class_UPNP_method_delete_port_mapping>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_valid\_gateway**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UPNPDevice_method_is_valid_gateway>`

Returns `true` if this is a valid IGD (InternetGatewayDevice) which
potentially supports port forwarding.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **query\_external\_address**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_UPNPDevice_method_query_external_address>`

Returns the external IP address of this **UPNPDevice** or an empty
string.
