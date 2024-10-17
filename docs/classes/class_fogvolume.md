github\_url  
hide

# FogVolume

**Inherits:** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A region that contributes to the default volumetric fog from the world
environment.

classref-introduction-group

## Description

**FogVolume**s are used to add localized fog into the global volumetric
fog effect. **FogVolume**s can also remove volumetric fog from specific
areas if using a `FogMaterial<class_FogMaterial>` with a negative
`FogMaterial.density<class_FogMaterial_property_density>`.

Performance of **FogVolume**s is directly related to their relative size
on the screen and the complexity of their attached
`FogMaterial<class_FogMaterial>`. It is best to keep **FogVolume**s
relatively small and simple where possible.

\*\*Note:\*\* **FogVolume**s only have a visible effect if
`Environment.volumetric_fog_enabled<class_Environment_property_volumetric_fog_enabled>`
is `true`. If you don't want fog to be globally visible (but only within
**FogVolume** nodes), set
`Environment.volumetric_fog_density<class_Environment_property_volumetric_fog_density>`
to `0.0`.

classref-introduction-group

## Tutorials

-   `Volumetric fog and fog volumes <../tutorials/3d/volumetric_fog>`

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

`Material<class_Material>` **material**
`🔗<class_FogVolume_property_material>`

classref-property-setget

-   `void (No return value.)` **set\_material**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_material**()

The `Material<class_Material>` used by the **FogVolume**. Can be either
a built-in `FogMaterial<class_FogMaterial>` or a custom
`ShaderMaterial<class_ShaderMaterial>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`FogVolumeShape<enum_RenderingServer_FogVolumeShape>` **shape** = `3`
`🔗<class_FogVolume_property_shape>`

classref-property-setget

-   `void (No return value.)` **set\_shape**(value:
    `FogVolumeShape<enum_RenderingServer_FogVolumeShape>`)
-   `FogVolumeShape<enum_RenderingServer_FogVolumeShape>`
    **get\_shape**()

The shape of the **FogVolume**. This can be set to either
`RenderingServer.FOG_VOLUME_SHAPE_ELLIPSOID<class_RenderingServer_constant_FOG_VOLUME_SHAPE_ELLIPSOID>`,
`RenderingServer.FOG_VOLUME_SHAPE_CONE<class_RenderingServer_constant_FOG_VOLUME_SHAPE_CONE>`,
`RenderingServer.FOG_VOLUME_SHAPE_CYLINDER<class_RenderingServer_constant_FOG_VOLUME_SHAPE_CYLINDER>`,
`RenderingServer.FOG_VOLUME_SHAPE_BOX<class_RenderingServer_constant_FOG_VOLUME_SHAPE_BOX>`
or
`RenderingServer.FOG_VOLUME_SHAPE_WORLD<class_RenderingServer_constant_FOG_VOLUME_SHAPE_WORLD>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **size** = `Vector3(2, 2, 2)`
`🔗<class_FogVolume_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_size**()

The size of the **FogVolume** when
`shape<class_FogVolume_property_shape>` is
`RenderingServer.FOG_VOLUME_SHAPE_ELLIPSOID<class_RenderingServer_constant_FOG_VOLUME_SHAPE_ELLIPSOID>`,
`RenderingServer.FOG_VOLUME_SHAPE_CONE<class_RenderingServer_constant_FOG_VOLUME_SHAPE_CONE>`,
`RenderingServer.FOG_VOLUME_SHAPE_CYLINDER<class_RenderingServer_constant_FOG_VOLUME_SHAPE_CYLINDER>`
or
`RenderingServer.FOG_VOLUME_SHAPE_BOX<class_RenderingServer_constant_FOG_VOLUME_SHAPE_BOX>`.

\*\*Note:\*\* Thin fog volumes may appear to flicker when the camera
moves or rotates. This can be alleviated by increasing
`ProjectSettings.rendering/environment/volumetric_fog/volume_depth<class_ProjectSettings_property_rendering/environment/volumetric_fog/volume_depth>`
(at a performance cost) or by decreasing
`Environment.volumetric_fog_length<class_Environment_property_volumetric_fog_length>`
(at no performance cost, but at the cost of lower fog range).
Alternatively, the **FogVolume** can be made thicker and use a lower
density in the `material<class_FogVolume_property_material>`.

\*\*Note:\*\* If `shape<class_FogVolume_property_shape>` is
`RenderingServer.FOG_VOLUME_SHAPE_CONE<class_RenderingServer_constant_FOG_VOLUME_SHAPE_CONE>`
or
`RenderingServer.FOG_VOLUME_SHAPE_CYLINDER<class_RenderingServer_constant_FOG_VOLUME_SHAPE_CYLINDER>`,
the cone/cylinder will be adjusted to fit within the size. Non-uniform
scaling of cone/cylinder shapes via the
`size<class_FogVolume_property_size>` property is not supported, but you
can scale the **FogVolume** node instead.
