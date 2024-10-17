github\_url  
hide

# AESContext

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides access to AES encryption/decryption of raw data.

classref-introduction-group

## Description

This class holds the context information required for encryption and
decryption operations with AES (Advanced Encryption Standard). Both
AES-ECB and AES-CBC modes are supported.

gdscript

extends Node

var aes = AESContext.new()

func \_ready():  
var key = "My secret key!!!" \# Key must be either 16 or 32 bytes. var
data = "My secret text!!" \# Data size must be multiple of 16 bytes,
apply padding if needed. \# Encrypt ECB
aes.start(AESContext.MODE\_ECB\_ENCRYPT, key.to\_utf8\_buffer()) var
encrypted = aes.update(data.to\_utf8\_buffer()) aes.finish() \# Decrypt
ECB aes.start(AESContext.MODE\_ECB\_DECRYPT, key.to\_utf8\_buffer()) var
decrypted = aes.update(encrypted) aes.finish() \# Check ECB
assert(decrypted == data.to\_utf8\_buffer())

var iv = "My secret iv!!!!" \# IV must be of exactly 16 bytes. \#
Encrypt CBC aes.start(AESContext.MODE\_CBC\_ENCRYPT,
key.to\_utf8\_buffer(), iv.to\_utf8\_buffer()) encrypted =
aes.update(data.to\_utf8\_buffer()) aes.finish() \# Decrypt CBC
aes.start(AESContext.MODE\_CBC\_DECRYPT, key.to\_utf8\_buffer(),
iv.to\_utf8\_buffer()) decrypted = aes.update(encrypted) aes.finish() \#
Check CBC assert(decrypted == data.to\_utf8\_buffer())

csharp

using Godot; using System.Diagnostics;

public partial class MyNode : Node { private AesContext \_aes = new
AesContext();

> public override void \_Ready() { string key = "My secret key!!!"; //
> Key must be either 16 or 32 bytes. string data = "My secret text!!";
> // Data size must be multiple of 16 bytes, apply padding if needed. //
> Encrypt ECB \_aes.Start(AesContext.Mode.EcbEncrypt,
> key.ToUtf8Buffer()); byte\[\] encrypted =
> \_aes.Update(data.ToUtf8Buffer()); \_aes.Finish(); // Decrypt ECB
> \_aes.Start(AesContext.Mode.EcbDecrypt, key.ToUtf8Buffer()); byte\[\]
> decrypted = \_aes.Update(encrypted); \_aes.Finish(); // Check ECB
> Debug.Assert(decrypted == data.ToUtf8Buffer());
>
> > string iv = "My secret iv!!!!"; // IV must be of exactly 16 bytes.
> > // Encrypt CBC \_aes.Start(AesContext.Mode.EcbEncrypt,
> > key.ToUtf8Buffer(), iv.ToUtf8Buffer()); encrypted =
> > \_aes.Update(data.ToUtf8Buffer()); \_aes.Finish(); // Decrypt CBC
> > \_aes.Start(AesContext.Mode.EcbDecrypt, key.ToUtf8Buffer(),
> > iv.ToUtf8Buffer()); decrypted = \_aes.Update(encrypted);
> > \_aes.Finish(); // Check CBC Debug.Assert(decrypted ==
> > data.ToUtf8Buffer());
>
> }

}

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

enum **Mode**: `🔗<enum_AESContext_Mode>`

classref-enumeration-constant

`Mode<enum_AESContext_Mode>` **MODE\_ECB\_ENCRYPT** = `0`

AES electronic codebook encryption mode.

classref-enumeration-constant

`Mode<enum_AESContext_Mode>` **MODE\_ECB\_DECRYPT** = `1`

AES electronic codebook decryption mode.

classref-enumeration-constant

`Mode<enum_AESContext_Mode>` **MODE\_CBC\_ENCRYPT** = `2`

AES cipher blocker chaining encryption mode.

classref-enumeration-constant

`Mode<enum_AESContext_Mode>` **MODE\_CBC\_DECRYPT** = `3`

AES cipher blocker chaining decryption mode.

classref-enumeration-constant

`Mode<enum_AESContext_Mode>` **MODE\_MAX** = `4`

Maximum value for the mode enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`void (No return value.)` **finish**()
`🔗<class_AESContext_method_finish>`

Close this AES context so it can be started again. See
`start<class_AESContext_method_start>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **get\_iv\_state**()
`🔗<class_AESContext_method_get_iv_state>`

Get the current IV state for this context (IV gets updated when calling
`update<class_AESContext_method_update>`). You normally don't need this
function.

\*\*Note:\*\* This function only makes sense when the context is started
with `MODE_CBC_ENCRYPT<class_AESContext_constant_MODE_CBC_ENCRYPT>` or
`MODE_CBC_DECRYPT<class_AESContext_constant_MODE_CBC_DECRYPT>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **start**(mode:
`Mode<enum_AESContext_Mode>`, key:
`PackedByteArray<class_PackedByteArray>`, iv:
`PackedByteArray<class_PackedByteArray>` = PackedByteArray())
`🔗<class_AESContext_method_start>`

Start the AES context in the given `mode`. A `key` of either 16 or 32
bytes must always be provided, while an `iv` (initialization vector) of
exactly 16 bytes, is only needed when `mode` is either
`MODE_CBC_ENCRYPT<class_AESContext_constant_MODE_CBC_ENCRYPT>` or
`MODE_CBC_DECRYPT<class_AESContext_constant_MODE_CBC_DECRYPT>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`PackedByteArray<class_PackedByteArray>` **update**(src:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_AESContext_method_update>`

Run the desired operation for this AES context. Will return a
`PackedByteArray<class_PackedByteArray>` containing the result of
encrypting (or decrypting) the given `src`. See
`start<class_AESContext_method_start>` for mode of operation.

\*\*Note:\*\* The size of `src` must be a multiple of 16. Apply some
padding if needed.
