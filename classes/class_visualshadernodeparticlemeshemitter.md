github\_url  
hide

# VisualShaderNodeParticleMeshEmitter

**Inherits:**
`VisualShaderNodeParticleEmitter<class_VisualShaderNodeParticleEmitter>`
**&lt;** `VisualShaderNode<class_VisualShaderNode>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A visual shader node that makes particles emitted in a shape defined by
a `Mesh<class_Mesh>`.

classref-introduction-group

## Description

`VisualShaderNodeParticleEmitter<class_VisualShaderNodeParticleEmitter>`
that makes the particles emitted in a shape of the assigned
`mesh<class_VisualShaderNodeParticleMeshEmitter_property_mesh>`. It will
emit from the mesh's surfaces, either all or only the specified one.

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Mesh<class_Mesh>` **mesh**
`🔗<class_VisualShaderNodeParticleMeshEmitter_property_mesh>`

classref-property-setget

-   `void (No return value.)` **set\_mesh**(value: `Mesh<class_Mesh>`)
-   `Mesh<class_Mesh>` **get\_mesh**()

The `Mesh<class_Mesh>` that defines emission shape.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **surface\_index** = `0`
`🔗<class_VisualShaderNodeParticleMeshEmitter_property_surface_index>`

classref-property-setget

-   `void (No return value.)` **set\_surface\_index**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_surface\_index**()

Index of the surface that emits particles.
`use_all_surfaces<class_VisualShaderNodeParticleMeshEmitter_property_use_all_surfaces>`
must be `false` for this to take effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **use\_all\_surfaces** = `true`
`🔗<class_VisualShaderNodeParticleMeshEmitter_property_use_all_surfaces>`

classref-property-setget

-   `void (No return value.)` **set\_use\_all\_surfaces**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_use\_all\_surfaces**()

If `true`, the particles will emit from all surfaces of the mesh.
