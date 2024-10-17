github\_url  
hide

# VisualShaderNodeParticleOutput

**Inherits:** `VisualShaderNodeOutput<class_VisualShaderNodeOutput>`
**&lt;** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Visual shader node that defines output values for particle emitting.

classref-introduction-group

## Description

This node defines how particles are emitted. It allows to customize e.g.
position and velocity. Available ports are different depending on which
function this node is inside (start, process, collision) and whether
custom data is enabled.
