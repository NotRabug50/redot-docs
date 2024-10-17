github\_url  
hide

# Crypto

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides access to advanced cryptographic functionalities.

classref-introduction-group

## Description

The Crypto class provides access to advanced cryptographic
functionalities.

Currently, this includes asymmetric key encryption/decryption,
signing/verification, and generating cryptographically secure random
bytes, RSA keys, HMAC digests, and self-signed
`X509Certificate<class_X509Certificate>`s.

gdscript

var crypto = Crypto.new()

\# Generate new RSA key. var key = crypto.generate\_rsa(4096)

\# Generate new self-signed certificate with the given key. var cert =
crypto.generate\_self\_signed\_certificate(key, "CN=mydomain.com,O=My
Game Company,C=IT")

\# Save key and certificate in the user folder.
key.save("user://generated.key") cert.save("user://generated.crt")

\# Encryption var data = "Some data" var encrypted = crypto.encrypt(key,
data.to\_utf8\_buffer())

\# Decryption var decrypted = crypto.decrypt(key, encrypted)

\# Signing var signature = crypto.sign(HashingContext.HASH\_SHA256,
data.sha256\_buffer(), key)

\# Verifying var verified = crypto.verify(HashingContext.HASH\_SHA256,
data.sha256\_buffer(), signature, key)

\# Checks assert(verified) assert(data.to\_utf8\_buffer() == decrypted)

csharp

using Godot; using System.Diagnostics;

Crypto crypto = new Crypto();

// Generate new RSA key. CryptoKey key = crypto.GenerateRsa(4096);

// Generate new self-signed certificate with the given key.
X509Certificate cert = crypto.GenerateSelfSignedCertificate(key,
"CN=mydomain.com,O=My Game Company,C=IT");

// Save key and certificate in the user folder.
key.Save("user://generated.key"); cert.Save("user://generated.crt");

// Encryption string data = "Some data"; byte\[\] encrypted =
crypto.Encrypt(key, data.ToUtf8Buffer());

// Decryption byte\[\] decrypted = crypto.Decrypt(key, encrypted);

// Signing byte\[\] signature =
crypto.Sign(HashingContext.HashType.Sha256, Data.Sha256Buffer(), key);

// Verifying bool verified =
crypto.Verify(HashingContext.HashType.Sha256, Data.Sha256Buffer(),
signature, key);

// Checks Debug.Assert(verified); Debug.Assert(data.ToUtf8Buffer() ==
decrypted);

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

`bool<class_bool>` **constant\_time\_compare**(trusted:
`PackedByteArray<class_PackedByteArray>`, received:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_Crypto_method_constant_time_compare>`

Compares two `PackedByteArray<class_PackedByteArray>`s for equality
without leaking timing information in order to prevent timing attacks.

See [this blog
post](https://paragonie.com/blog/2015/11/preventing-timing-attacks-on-string-comparison-with-double-hmac-strategy)
for more information.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **decrypt**(key:
`CryptoKey<class_CryptoKey>`, ciphertext:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_Crypto_method_decrypt>`

Decrypt the given `ciphertext` with the provided private `key`.

\*\*Note:\*\* The maximum size of accepted ciphertext is limited by the
key size.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **encrypt**(key:
`CryptoKey<class_CryptoKey>`, plaintext:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_Crypto_method_encrypt>`

Encrypt the given `plaintext` with the provided public `key`.

\*\*Note:\*\* The maximum size of accepted plaintext is limited by the
key size.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>`
**generate\_random\_bytes**(size: `int<class_int>`)
`🔗<class_Crypto_method_generate_random_bytes>`

Generates a `PackedByteArray<class_PackedByteArray>` of
cryptographically secure random bytes with given `size`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`CryptoKey<class_CryptoKey>` **generate\_rsa**(size: `int<class_int>`)
`🔗<class_Crypto_method_generate_rsa>`

Generates an RSA `CryptoKey<class_CryptoKey>` that can be used for
creating self-signed certificates and passed to
`StreamPeerTLS.accept_stream<class_StreamPeerTLS_method_accept_stream>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`X509Certificate<class_X509Certificate>`
**generate\_self\_signed\_certificate**(key:
`CryptoKey<class_CryptoKey>`, issuer\_name: `String<class_String>` =
"CN=myserver,O=myorganisation,C=IT", not\_before: `String<class_String>`
= "20140101000000", not\_after: `String<class_String>` =
"20340101000000")
`🔗<class_Crypto_method_generate_self_signed_certificate>`

Generates a self-signed `X509Certificate<class_X509Certificate>` from
the given `CryptoKey<class_CryptoKey>` and `issuer_name`. The
certificate validity will be defined by `not_before` and `not_after`
(first valid date and last valid date). The `issuer_name` must contain
at least "CN=" (common name, i.e. the domain name), "O=" (organization,
i.e. your company name), "C=" (country, i.e. 2 lettered ISO-3166 code of
the country the organization is based in).

A small example to generate an RSA key and an X509 self-signed
certificate.

gdscript

var crypto = Crypto.new() \# Generate 4096 bits RSA key. var key =
crypto.generate\_rsa(4096) \# Generate self-signed certificate using the
given key. var cert = crypto.generate\_self\_signed\_certificate(key,
"CN=example.com,O=A Game Company,C=IT")

csharp

var crypto = new Crypto(); // Generate 4096 bits RSA key. CryptoKey key
= crypto.GenerateRsa(4096); // Generate self-signed certificate using
the given key. X509Certificate cert =
crypto.GenerateSelfSignedCertificate(key, "CN=mydomain.com,O=My Game
Company,C=IT");

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **hmac\_digest**(hash\_type:
`HashType<enum_HashingContext_HashType>`, key:
`PackedByteArray<class_PackedByteArray>`, msg:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_Crypto_method_hmac_digest>`

Generates an [HMAC](https://en.wikipedia.org/wiki/HMAC) digest of `msg`
using `key`. The `hash_type` parameter is the hashing algorithm that is
used for the inner and outer hashes.

Currently, only
`HashingContext.HASH_SHA256<class_HashingContext_constant_HASH_SHA256>`
and `HashingContext.HASH_SHA1<class_HashingContext_constant_HASH_SHA1>`
are supported.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **sign**(hash\_type:
`HashType<enum_HashingContext_HashType>`, hash:
`PackedByteArray<class_PackedByteArray>`, key:
`CryptoKey<class_CryptoKey>`) `🔗<class_Crypto_method_sign>`

Sign a given `hash` of type `hash_type` with the provided private `key`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **verify**(hash\_type:
`HashType<enum_HashingContext_HashType>`, hash:
`PackedByteArray<class_PackedByteArray>`, signature:
`PackedByteArray<class_PackedByteArray>`, key:
`CryptoKey<class_CryptoKey>`) `🔗<class_Crypto_method_verify>`

Verify that a given `signature` for `hash` of type `hash_type` against
the provided public `key`.
