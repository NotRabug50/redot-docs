github\_url  
hide

# VisualShaderNodeParticleEmit

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A visual shader node that forces to emit a particle from a sub-emitter.

classref-introduction-group

## Description

This node internally calls `emit_subparticle` shader method. It will
emit a particle from the configured sub-emitter and also allows to
customize how its emitted. Requires a sub-emitter assigned to the
particles node with this shader.

classref-reftable-group

## Properties

<table>
<tbody>
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **EmitFlags**: `🔗<enum_VisualShaderNodeParticleEmit_EmitFlags>`

classref-enumeration-constant

`EmitFlags<enum_VisualShaderNodeParticleEmit_EmitFlags>`
**EMIT\_FLAG\_POSITION** = `1`

If enabled, the particle starts with the position defined by this node.

classref-enumeration-constant

`EmitFlags<enum_VisualShaderNodeParticleEmit_EmitFlags>`
**EMIT\_FLAG\_ROT\_SCALE** = `2`

If enabled, the particle starts with the rotation and scale defined by
this node.

classref-enumeration-constant

`EmitFlags<enum_VisualShaderNodeParticleEmit_EmitFlags>`
**EMIT\_FLAG\_VELOCITY** = `4`

If enabled,the particle starts with the velocity defined by this node.

classref-enumeration-constant

`EmitFlags<enum_VisualShaderNodeParticleEmit_EmitFlags>`
**EMIT\_FLAG\_COLOR** = `8`

If enabled, the particle starts with the color defined by this node.

classref-enumeration-constant

`EmitFlags<enum_VisualShaderNodeParticleEmit_EmitFlags>`
**EMIT\_FLAG\_CUSTOM** = `16`

If enabled, the particle starts with the `CUSTOM` data defined by this
node.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`EmitFlags<enum_VisualShaderNodeParticleEmit_EmitFlags>` **flags** =
`31` `🔗<class_VisualShaderNodeParticleEmit_property_flags>`

classref-property-setget

-   `void (No return value.)` **set\_flags**(value:
    `EmitFlags<enum_VisualShaderNodeParticleEmit_EmitFlags>`)
-   `EmitFlags<enum_VisualShaderNodeParticleEmit_EmitFlags>`
    **get\_flags**()

Flags used to override the properties defined in the sub-emitter's
process material.
