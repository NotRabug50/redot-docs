github\_url  
hide

# TLSOptions

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

TLS configuration for clients and servers.

classref-introduction-group

## Description

TLSOptions abstracts the configuration options for the
`StreamPeerTLS<class_StreamPeerTLS>` and
`PacketPeerDTLS<class_PacketPeerDTLS>` classes.

Objects of this class cannot be instantiated directly, and one of the
static methods `client<class_TLSOptions_method_client>`,
`client_unsafe<class_TLSOptions_method_client_unsafe>`, or
`server<class_TLSOptions_method_server>` should be used instead.

gdscript

\# Create a TLS client configuration which uses our custom trusted CA
chain. var client\_trusted\_cas = load("<res://my_trusted_cas.crt>") var
client\_tls\_options = TLSOptions.client(client\_trusted\_cas)

\# Create a TLS server configuration. var server\_certs =
load("<res://my_server_cas.crt>") var server\_key =
load("<res://my_server_key.key>") var server\_tls\_options =
TLSOptions.server(server\_key, server\_certs)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`TLSOptions<class_TLSOptions>` **client**(trusted\_chain:
`X509Certificate<class_X509Certificate>` = null, common\_name\_override:
`String<class_String>` = "")
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_TLSOptions_method_client>`

Creates a TLS client configuration which validates certificates and
their common names (fully qualified domain names).

You can specify a custom `trusted_chain` of certification authorities
(the default CA list will be used if `null`), and optionally provide a
`common_name_override` if you expect the certificate to have a common
name other than the server FQDN.

\*\*Note:\*\* On the Web platform, TLS verification is always enforced
against the CA list of the web browser. This is considered a security
feature.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TLSOptions<class_TLSOptions>` **client\_unsafe**(trusted\_chain:
`X509Certificate<class_X509Certificate>` = null)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_TLSOptions_method_client_unsafe>`

Creates an **unsafe** TLS client configuration where certificate
validation is optional. You can optionally provide a valid
`trusted_chain`, but the common name of the certificates will never be
checked. Using this configuration for purposes other than testing **is
not recommended**.

\*\*Note:\*\* On the Web platform, TLS verification is always enforced
against the CA list of the web browser. This is considered a security
feature.

classref-item-separator

------------------------------------------------------------------------

classref-method

`String<class_String>` **get\_common\_name\_override**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TLSOptions_method_get_common_name_override>`

Returns the common name (domain name) override specified when creating
with `client<class_TLSOptions_method_client>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`X509Certificate<class_X509Certificate>` **get\_own\_certificate**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TLSOptions_method_get_own_certificate>`

Returns the `X509Certificate<class_X509Certificate>` specified when
creating with `server<class_TLSOptions_method_server>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CryptoKey<class_CryptoKey>` **get\_private\_key**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TLSOptions_method_get_private_key>`

Returns the `CryptoKey<class_CryptoKey>` specified when creating with
`server<class_TLSOptions_method_server>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`X509Certificate<class_X509Certificate>` **get\_trusted\_ca\_chain**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TLSOptions_method_get_trusted_ca_chain>`

Returns the CA `X509Certificate<class_X509Certificate>` chain specified
when creating with `client<class_TLSOptions_method_client>` or
`client_unsafe<class_TLSOptions_method_client_unsafe>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_server**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TLSOptions_method_is_server>`

Returns `true` if created with `server<class_TLSOptions_method_server>`,
`false` otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **is\_unsafe\_client**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_TLSOptions_method_is_unsafe_client>`

Returns `true` if created with
`client_unsafe<class_TLSOptions_method_client_unsafe>`, `false`
otherwise.

classref-item-separator

------------------------------------------------------------------------

classref-method

`TLSOptions<class_TLSOptions>` **server**(key:
`CryptoKey<class_CryptoKey>`, certificate:
`X509Certificate<class_X509Certificate>`)
`static (This method doesn't need an instance to be called, so it can be called directly using the class name.)`
`🔗<class_TLSOptions_method_server>`

Creates a TLS server configuration using the provided `key` and
`certificate`.

\*\*Note:\*\* The `certificate` should include the full certificate
chain up to the signing CA (certificates file can be concatenated using
a general purpose text editor).
