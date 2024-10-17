github\_url  
hide

# GPUParticlesAttractorSphere3D

**Inherits:** `GPUParticlesAttractor3D<class_GPUParticlesAttractor3D>`
**&lt;** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A spheroid-shaped attractor that influences particles from
`GPUParticles3D<class_GPUParticles3D>` nodes.

classref-introduction-group

## Description

A spheroid-shaped attractor that influences particles from
`GPUParticles3D<class_GPUParticles3D>` nodes. Can be used to attract
particles towards its origin, or to push them away from its origin.

Particle attractors work in real-time and can be moved, rotated and
scaled during gameplay. Unlike collision shapes, non-uniform scaling of
attractors is also supported.

\*\*Note:\*\* Particle attractors only affect
`GPUParticles3D<class_GPUParticles3D>`, not
`CPUParticles3D<class_CPUParticles3D>`.

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

`float<class_float>` **radius** = `1.0`
`🔗<class_GPUParticlesAttractorSphere3D_property_radius>`

classref-property-setget

-   `void (No return value.)` **set\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_radius**()

The attractor sphere's radius in 3D units.

\*\*Note:\*\* Stretched ellipses can be obtained by using non-uniform
scaling on the **GPUParticlesAttractorSphere3D** node.
