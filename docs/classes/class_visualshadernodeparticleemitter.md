github\_url  
hide

# VisualShaderNodeParticleEmitter

**Inherits:** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

**Inherited By:**
`VisualShaderNodeParticleBoxEmitter<class_VisualShaderNodeParticleBoxEmitter>`,
`VisualShaderNodeParticleMeshEmitter<class_VisualShaderNodeParticleMeshEmitter>`,
`VisualShaderNodeParticleRingEmitter<class_VisualShaderNodeParticleRingEmitter>`,
`VisualShaderNodeParticleSphereEmitter<class_VisualShaderNodeParticleSphereEmitter>`

A base class for particle emitters.

classref-introduction-group

## Description

Particle emitter nodes can be used in "start" step of particle shaders
and they define the starting position of the particles. Connect them to
the Position output port.

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

## Property Descriptions

classref-property

`bool<class_bool>` **mode\_2d** = `false`
`🔗<class_VisualShaderNodeParticleEmitter_property_mode_2d>`

classref-property-setget

-   `void (No return value.)` **set\_mode\_2d**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_mode\_2d**()

If `true`, the result of this emitter is projected to 2D space. By
default it is `false` and meant for use in 3D space.
