github\_url  
hide

# HashingContext

**Inherits:** `RefCounted<class_RefCounted>` **&lt;**
`Object<class_Object>`

Provides functionality for computing cryptographic hashes chunk by
chunk.

classref-introduction-group

## Description

The HashingContext class provides an interface for computing
cryptographic hashes over multiple iterations. Useful for computing
hashes of big files (so you don't have to load them all in memory),
network streams, and data streams in general (so you don't have to hold
buffers).

The `HashType<enum_HashingContext_HashType>` enum shows the supported
hashing algorithms.

gdscript

const CHUNK\_SIZE = 1024

func hash\_file(path):  
\# Check that file exists. if not FileAccess.file\_exists(path): return
\# Start an SHA-256 context. var ctx = HashingContext.new()
ctx.start(HashingContext.HASH\_SHA256) \# Open the file to hash. var
file = FileAccess.open(path, FileAccess.READ) \# Update the context
after reading each chunk. while file.get\_position() &lt;
file.get\_length(): var remaining = file.get\_length() -
file.get\_position() ctx.update(file.get\_buffer(min(remaining,
CHUNK\_SIZE))) \# Get the computed hash. var res = ctx.finish() \# Print
the result as hex string and array. printt(res.hex\_encode(),
Array(res))

csharp

public const int ChunkSize = 1024;

public void HashFile(string path) { // Check that file exists. if
(!FileAccess.FileExists(path)) { return; } // Start an SHA-256 context.
var ctx = new HashingContext();
ctx.Start(HashingContext.HashType.Sha256); // Open the file to hash.
using var file = FileAccess.Open(path, FileAccess.ModeFlags.Read); //
Update the context after reading each chunk. while (file.GetPosition()
&lt; file.GetLength()) { int remaining = (int)(file.GetLength() -
file.GetPosition()); ctx.Update(file.GetBuffer(Mathf.Min(remaining,
ChunkSize))); } // Get the computed hash. byte\[\] res = ctx.Finish();
// Print the result as hex string and array. GD.PrintT(res.HexEncode(),
(Variant)res); }

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **HashType**: `🔗<enum_HashingContext_HashType>`

classref-enumeration-constant

`HashType<enum_HashingContext_HashType>` **HASH\_MD5** = `0`

Hashing algorithm: MD5.

classref-enumeration-constant

`HashType<enum_HashingContext_HashType>` **HASH\_SHA1** = `1`

Hashing algorithm: SHA-1.

classref-enumeration-constant

`HashType<enum_HashingContext_HashType>` **HASH\_SHA256** = `2`

Hashing algorithm: SHA-256.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`PackedByteArray<class_PackedByteArray>` **finish**()
`🔗<class_HashingContext_method_finish>`

Closes the current context, and return the computed hash.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **start**(type:
`HashType<enum_HashingContext_HashType>`)
`🔗<class_HashingContext_method_start>`

Starts a new hash computation of the given `type` (e.g.
`HASH_SHA256<class_HashingContext_constant_HASH_SHA256>` to start
computation of an SHA-256).

classref-item-separator

------------------------------------------------------------------------

classref-method

`Error<enum_@GlobalScope_Error>` **update**(chunk:
`PackedByteArray<class_PackedByteArray>`)
`🔗<class_HashingContext_method_update>`

Updates the computation with the given `chunk` of data.
