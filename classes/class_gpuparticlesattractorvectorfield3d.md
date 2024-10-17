github\_url  
hide

# GPUParticlesAttractorVectorField3D

**Inherits:** `GPUParticlesAttractor3D<class_GPUParticlesAttractor3D>`
**&lt;** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A box-shaped attractor with varying directions and strengths defined in
it that influences particles from `GPUParticles3D<class_GPUParticles3D>`
nodes.

classref-introduction-group

## Description

A box-shaped attractor with varying directions and strengths defined in
it that influences particles from `GPUParticles3D<class_GPUParticles3D>`
nodes.

Unlike `GPUParticlesAttractorBox3D<class_GPUParticlesAttractorBox3D>`,
**GPUParticlesAttractorVectorField3D** uses a
`texture<class_GPUParticlesAttractorVectorField3D_property_texture>` to
affect attraction strength within the box. This can be used to create
complex attraction scenarios where particles travel in different
directions depending on their location. This can be useful for weather
effects such as sandstorms.

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Vector3<class_Vector3>` **size** = `Vector3(2, 2, 2)`
`🔗<class_GPUParticlesAttractorVectorField3D_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_size**()

The size of the vector field box in 3D units.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture3D<class_Texture3D>` **texture**
`🔗<class_GPUParticlesAttractorVectorField3D_property_texture>`

classref-property-setget

-   `void (No return value.)` **set\_texture**(value:
    `Texture3D<class_Texture3D>`)
-   `Texture3D<class_Texture3D>` **get\_texture**()

The 3D texture to be used. Values are linearly interpolated between the
texture's pixels.

\*\*Note:\*\* To get better performance, the 3D texture's resolution
should reflect the
`size<class_GPUParticlesAttractorVectorField3D_property_size>` of the
attractor. Since particle attraction is usually low-frequency data, the
texture can be kept at a low resolution such as 64×64×64.
