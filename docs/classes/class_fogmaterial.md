github\_url  
hide

# FogMaterial

**Inherits:** `Material<class_Material>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A material that controls how volumetric fog is rendered, to be assigned
to a `FogVolume<class_FogVolume>`.

classref-introduction-group

## Description

A `Material<class_Material>` resource that can be used by
`FogVolume<class_FogVolume>`s to draw volumetric effects.

If you need more advanced effects, use a custom
`fog shader <../tutorials/shaders/shader_reference/fog_shader>`.

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

`Color<class_Color>` **albedo** = `Color(1, 1, 1, 1)`
`🔗<class_FogMaterial_property_albedo>`

classref-property-setget

-   `void (No return value.)` **set\_albedo**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_albedo**()

The single-scattering `Color<class_Color>` of the
`FogVolume<class_FogVolume>`. Internally,
`albedo<class_FogMaterial_property_albedo>` is converted into
single-scattering, which is additively blended with other
`FogVolume<class_FogVolume>`s and the
`Environment.volumetric_fog_albedo<class_Environment_property_volumetric_fog_albedo>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **density** = `1.0`
`🔗<class_FogMaterial_property_density>`

classref-property-setget

-   `void (No return value.)` **set\_density**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_density**()

The density of the `FogVolume<class_FogVolume>`. Denser objects are more
opaque, but may suffer from under-sampling artifacts that look like
stripes. Negative values can be used to subtract fog from other
`FogVolume<class_FogVolume>`s or global volumetric fog.

\*\*Note:\*\* Due to limited precision,
`density<class_FogMaterial_property_density>` values between `-0.001`
and `0.001` (exclusive) act like `0.0`. This does not apply to
`Environment.volumetric_fog_density<class_Environment_property_volumetric_fog_density>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture3D<class_Texture3D>` **density\_texture**
`🔗<class_FogMaterial_property_density_texture>`

classref-property-setget

-   `void (No return value.)` **set\_density\_texture**(value:
    `Texture3D<class_Texture3D>`)
-   `Texture3D<class_Texture3D>` **get\_density\_texture**()

The 3D texture that is used to scale the
`density<class_FogMaterial_property_density>` of the
`FogVolume<class_FogVolume>`. This can be used to vary fog density
within the `FogVolume<class_FogVolume>` with any kind of static pattern.
For animated effects, consider using a custom
`fog shader <../tutorials/shaders/shader_reference/fog_shader>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **edge\_fade** = `0.1`
`🔗<class_FogMaterial_property_edge_fade>`

classref-property-setget

-   `void (No return value.)` **set\_edge\_fade**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_edge\_fade**()

The hardness of the edges of the `FogVolume<class_FogVolume>`. A higher
value will result in softer edges, while a lower value will result in
harder edges.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **emission** = `Color(0, 0, 0, 1)`
`🔗<class_FogMaterial_property_emission>`

classref-property-setget

-   `void (No return value.)` **set\_emission**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_emission**()

The `Color<class_Color>` of the light emitted by the
`FogVolume<class_FogVolume>`. Emitted light will not cast light or
shadows on other objects, but can be useful for modulating the
`Color<class_Color>` of the `FogVolume<class_FogVolume>` independently
from light sources.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **height\_falloff** = `0.0`
`🔗<class_FogMaterial_property_height_falloff>`

classref-property-setget

-   `void (No return value.)` **set\_height\_falloff**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_height\_falloff**()

The rate by which the height-based fog decreases in density as height
increases in world space. A high falloff will result in a sharp
transition, while a low falloff will result in a smoother transition. A
value of `0.0` results in uniform-density fog. The height threshold is
determined by the height of the associated `FogVolume<class_FogVolume>`.
