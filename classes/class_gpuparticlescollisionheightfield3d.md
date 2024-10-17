github\_url  
hide

# GPUParticlesCollisionHeightField3D

**Inherits:** `GPUParticlesCollision3D<class_GPUParticlesCollision3D>`
**&lt;** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A real-time heightmap-shaped 3D particle collision shape affecting
`GPUParticles3D<class_GPUParticles3D>` nodes.

classref-introduction-group

## Description

A real-time heightmap-shaped 3D particle collision shape affecting
`GPUParticles3D<class_GPUParticles3D>` nodes.

Heightmap shapes allow for efficiently representing collisions for
convex and concave objects with a single "floor" (such as terrain). This
is less flexible than
`GPUParticlesCollisionSDF3D<class_GPUParticlesCollisionSDF3D>`, but it
doesn't require a baking step.

\*\*GPUParticlesCollisionHeightField3D\*\* can also be regenerated in
real-time when it is moved, when the camera moves, or even continuously.
This makes **GPUParticlesCollisionHeightField3D** a good choice for
weather effects such as rain and snow and games with highly dynamic
geometry. However, this class is limited since heightmaps cannot
represent overhangs (e.g. indoors or caves).

\*\*Note:\*\*
`ParticleProcessMaterial.collision_mode<class_ParticleProcessMaterial_property_collision_mode>`
must be `true` on the `GPUParticles3D<class_GPUParticles3D>`'s process
material for collision to work.

\*\*Note:\*\* Particle collision only affects
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

enum **Resolution**:
`🔗<enum_GPUParticlesCollisionHeightField3D_Resolution>`

classref-enumeration-constant

`Resolution<enum_GPUParticlesCollisionHeightField3D_Resolution>`
**RESOLUTION\_256** = `0`

Generate a 256×256 heightmap. Intended for small-scale scenes, or larger
scenes with no distant particles.

classref-enumeration-constant

`Resolution<enum_GPUParticlesCollisionHeightField3D_Resolution>`
**RESOLUTION\_512** = `1`

Generate a 512×512 heightmap. Intended for medium-scale scenes, or
larger scenes with no distant particles.

classref-enumeration-constant

`Resolution<enum_GPUParticlesCollisionHeightField3D_Resolution>`
**RESOLUTION\_1024** = `2`

Generate a 1024×1024 heightmap. Intended for large scenes with distant
particles.

classref-enumeration-constant

`Resolution<enum_GPUParticlesCollisionHeightField3D_Resolution>`
**RESOLUTION\_2048** = `3`

Generate a 2048×2048 heightmap. Intended for very large scenes with
distant particles.

classref-enumeration-constant

`Resolution<enum_GPUParticlesCollisionHeightField3D_Resolution>`
**RESOLUTION\_4096** = `4`

Generate a 4096×4096 heightmap. Intended for huge scenes with distant
particles.

classref-enumeration-constant

`Resolution<enum_GPUParticlesCollisionHeightField3D_Resolution>`
**RESOLUTION\_8192** = `5`

Generate a 8192×8192 heightmap. Intended for gigantic scenes with
distant particles.

classref-enumeration-constant

`Resolution<enum_GPUParticlesCollisionHeightField3D_Resolution>`
**RESOLUTION\_MAX** = `6`

Represents the size of the
`Resolution<enum_GPUParticlesCollisionHeightField3D_Resolution>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **UpdateMode**:
`🔗<enum_GPUParticlesCollisionHeightField3D_UpdateMode>`

classref-enumeration-constant

`UpdateMode<enum_GPUParticlesCollisionHeightField3D_UpdateMode>`
**UPDATE\_MODE\_WHEN\_MOVED** = `0`

Only update the heightmap when the
**GPUParticlesCollisionHeightField3D** node is moved, or when the camera
moves if
`follow_camera_enabled<class_GPUParticlesCollisionHeightField3D_property_follow_camera_enabled>`
is `true`. An update can be forced by slightly moving the
**GPUParticlesCollisionHeightField3D** in any direction, or by calling
`RenderingServer.particles_collision_height_field_update<class_RenderingServer_method_particles_collision_height_field_update>`.

classref-enumeration-constant

`UpdateMode<enum_GPUParticlesCollisionHeightField3D_UpdateMode>`
**UPDATE\_MODE\_ALWAYS** = `1`

Update the heightmap every frame. This has a significant performance
cost. This update should only be used when geometry that particles can
collide with changes significantly during gameplay.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`bool<class_bool>` **follow\_camera\_enabled** = `false`
`🔗<class_GPUParticlesCollisionHeightField3D_property_follow_camera_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_follow\_camera\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_follow\_camera\_enabled**()

If `true`, the **GPUParticlesCollisionHeightField3D** will follow the
current camera in global space. The
**GPUParticlesCollisionHeightField3D** does not need to be a child of
the `Camera3D<class_Camera3D>` node for this to work.

Following the camera has a performance cost, as it will force the
heightmap to update whenever the camera moves. Consider lowering
`resolution<class_GPUParticlesCollisionHeightField3D_property_resolution>`
to improve performance if
`follow_camera_enabled<class_GPUParticlesCollisionHeightField3D_property_follow_camera_enabled>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Resolution<enum_GPUParticlesCollisionHeightField3D_Resolution>`
**resolution** = `2`
`🔗<class_GPUParticlesCollisionHeightField3D_property_resolution>`

classref-property-setget

-   `void (No return value.)` **set\_resolution**(value:
    `Resolution<enum_GPUParticlesCollisionHeightField3D_Resolution>`)
-   `Resolution<enum_GPUParticlesCollisionHeightField3D_Resolution>`
    **get\_resolution**()

Higher resolutions can represent small details more accurately in large
scenes, at the cost of lower performance. If
`update_mode<class_GPUParticlesCollisionHeightField3D_property_update_mode>`
is
`UPDATE_MODE_ALWAYS<class_GPUParticlesCollisionHeightField3D_constant_UPDATE_MODE_ALWAYS>`,
consider using the lowest resolution possible.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **size** = `Vector3(2, 2, 2)`
`🔗<class_GPUParticlesCollisionHeightField3D_property_size>`

classref-property-setget

-   `void (No return value.)` **set\_size**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_size**()

The collision heightmap's size in 3D units. To improve heightmap
quality, `size<class_GPUParticlesCollisionHeightField3D_property_size>`
should be set as small as possible while covering the parts of the scene
you need.

classref-item-separator

------------------------------------------------------------------------

classref-property

`UpdateMode<enum_GPUParticlesCollisionHeightField3D_UpdateMode>`
**update\_mode** = `0`
`🔗<class_GPUParticlesCollisionHeightField3D_property_update_mode>`

classref-property-setget

-   `void (No return value.)` **set\_update\_mode**(value:
    `UpdateMode<enum_GPUParticlesCollisionHeightField3D_UpdateMode>`)
-   `UpdateMode<enum_GPUParticlesCollisionHeightField3D_UpdateMode>`
    **get\_update\_mode**()

The update policy to use for the generated heightmap.
