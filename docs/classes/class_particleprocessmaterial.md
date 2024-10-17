github\_url  
hide

# ParticleProcessMaterial

**Inherits:** `Material<class_Material>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

Holds a particle configuration for
`GPUParticles2D<class_GPUParticles2D>` or
`GPUParticles3D<class_GPUParticles3D>` nodes.

classref-introduction-group

## Description

**ParticleProcessMaterial** defines particle properties and behavior. It
is used in the `process_material` of the
`GPUParticles2D<class_GPUParticles2D>` and
`GPUParticles3D<class_GPUParticles3D>` nodes. Some of this material's
properties are applied to each particle when emitted, while others can
have a `CurveTexture<class_CurveTexture>` or a
`GradientTexture1D<class_GradientTexture1D>` applied to vary numerical
or color values over the lifetime of the particle.

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
<tr>
</tr>
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **Parameter**: `🔗<enum_ParticleProcessMaterial_Parameter>`

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_INITIAL\_LINEAR\_VELOCITY** = `0`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set initial velocity properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_ANGULAR\_VELOCITY** = `1`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set angular velocity properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_ORBIT\_VELOCITY** = `2`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set orbital velocity properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_LINEAR\_ACCEL** = `3`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set linear acceleration properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_RADIAL\_ACCEL** = `4`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set radial acceleration properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_TANGENTIAL\_ACCEL** = `5`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set tangential acceleration properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>` **PARAM\_DAMPING** =
`6`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set damping properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>` **PARAM\_ANGLE** =
`7`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set angle properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>` **PARAM\_SCALE** =
`8`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set scale properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_HUE\_VARIATION** = `9`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set hue variation properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_ANIM\_SPEED** = `10`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set animation speed properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_ANIM\_OFFSET** = `11`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set animation offset properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_RADIAL\_VELOCITY** = `15`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set radial velocity properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_DIRECTIONAL\_VELOCITY** = `16`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set directional velocity properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_SCALE\_OVER\_VELOCITY** = `17`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>`,
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>`, and
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set scale over velocity properties.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>` **PARAM\_MAX** =
`18`

Represents the size of the
`Parameter<enum_ParticleProcessMaterial_Parameter>` enum.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_TURB\_VEL\_INFLUENCE** = `13`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>` and
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>` to
set the turbulence minimum und maximum influence on each particles
velocity.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_TURB\_INIT\_DISPLACEMENT** = `14`

Use with
`set_param_min<class_ParticleProcessMaterial_method_set_param_min>` and
`set_param_max<class_ParticleProcessMaterial_method_set_param_max>` to
set the turbulence minimum and maximum displacement of the particles
spawn position.

classref-enumeration-constant

`Parameter<enum_ParticleProcessMaterial_Parameter>`
**PARAM\_TURB\_INFLUENCE\_OVER\_LIFE** = `12`

Use with
`set_param_texture<class_ParticleProcessMaterial_method_set_param_texture>`
to set the turbulence influence over the particles life time.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **ParticleFlags**: `🔗<enum_ParticleProcessMaterial_ParticleFlags>`

classref-enumeration-constant

`ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`
**PARTICLE\_FLAG\_ALIGN\_Y\_TO\_VELOCITY** = `0`

Use with
`set_particle_flag<class_ParticleProcessMaterial_method_set_particle_flag>`
to set
`particle_flag_align_y<class_ParticleProcessMaterial_property_particle_flag_align_y>`.

classref-enumeration-constant

`ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`
**PARTICLE\_FLAG\_ROTATE\_Y** = `1`

Use with
`set_particle_flag<class_ParticleProcessMaterial_method_set_particle_flag>`
to set
`particle_flag_rotate_y<class_ParticleProcessMaterial_property_particle_flag_rotate_y>`.

classref-enumeration-constant

`ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`
**PARTICLE\_FLAG\_DISABLE\_Z** = `2`

Use with
`set_particle_flag<class_ParticleProcessMaterial_method_set_particle_flag>`
to set
`particle_flag_disable_z<class_ParticleProcessMaterial_property_particle_flag_disable_z>`.

classref-enumeration-constant

`ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`
**PARTICLE\_FLAG\_DAMPING\_AS\_FRICTION** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`
**PARTICLE\_FLAG\_MAX** = `4`

Represents the size of the
`ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EmissionShape**: `🔗<enum_ParticleProcessMaterial_EmissionShape>`

classref-enumeration-constant

`EmissionShape<enum_ParticleProcessMaterial_EmissionShape>`
**EMISSION\_SHAPE\_POINT** = `0`

All particles will be emitted from a single point.

classref-enumeration-constant

`EmissionShape<enum_ParticleProcessMaterial_EmissionShape>`
**EMISSION\_SHAPE\_SPHERE** = `1`

Particles will be emitted in the volume of a sphere.

classref-enumeration-constant

`EmissionShape<enum_ParticleProcessMaterial_EmissionShape>`
**EMISSION\_SHAPE\_SPHERE\_SURFACE** = `2`

Particles will be emitted on the surface of a sphere.

classref-enumeration-constant

`EmissionShape<enum_ParticleProcessMaterial_EmissionShape>`
**EMISSION\_SHAPE\_BOX** = `3`

Particles will be emitted in the volume of a box.

classref-enumeration-constant

`EmissionShape<enum_ParticleProcessMaterial_EmissionShape>`
**EMISSION\_SHAPE\_POINTS** = `4`

Particles will be emitted at a position determined by sampling a random
point on the
`emission_point_texture<class_ParticleProcessMaterial_property_emission_point_texture>`.
Particle color will be modulated by
`emission_color_texture<class_ParticleProcessMaterial_property_emission_color_texture>`.

classref-enumeration-constant

`EmissionShape<enum_ParticleProcessMaterial_EmissionShape>`
**EMISSION\_SHAPE\_DIRECTED\_POINTS** = `5`

Particles will be emitted at a position determined by sampling a random
point on the
`emission_point_texture<class_ParticleProcessMaterial_property_emission_point_texture>`.
Particle velocity and rotation will be set based on
`emission_normal_texture<class_ParticleProcessMaterial_property_emission_normal_texture>`.
Particle color will be modulated by
`emission_color_texture<class_ParticleProcessMaterial_property_emission_color_texture>`.

classref-enumeration-constant

`EmissionShape<enum_ParticleProcessMaterial_EmissionShape>`
**EMISSION\_SHAPE\_RING** = `6`

Particles will be emitted in a ring or cylinder.

classref-enumeration-constant

`EmissionShape<enum_ParticleProcessMaterial_EmissionShape>`
**EMISSION\_SHAPE\_MAX** = `7`

Represents the size of the
`EmissionShape<enum_ParticleProcessMaterial_EmissionShape>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **SubEmitterMode**:
`🔗<enum_ParticleProcessMaterial_SubEmitterMode>`

classref-enumeration-constant

`SubEmitterMode<enum_ParticleProcessMaterial_SubEmitterMode>`
**SUB\_EMITTER\_DISABLED** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`SubEmitterMode<enum_ParticleProcessMaterial_SubEmitterMode>`
**SUB\_EMITTER\_CONSTANT** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`SubEmitterMode<enum_ParticleProcessMaterial_SubEmitterMode>`
**SUB\_EMITTER\_AT\_END** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`SubEmitterMode<enum_ParticleProcessMaterial_SubEmitterMode>`
**SUB\_EMITTER\_AT\_COLLISION** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`SubEmitterMode<enum_ParticleProcessMaterial_SubEmitterMode>`
**SUB\_EMITTER\_MAX** = `4`

Represents the size of the
`SubEmitterMode<enum_ParticleProcessMaterial_SubEmitterMode>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **CollisionMode**: `🔗<enum_ParticleProcessMaterial_CollisionMode>`

classref-enumeration-constant

`CollisionMode<enum_ParticleProcessMaterial_CollisionMode>`
**COLLISION\_DISABLED** = `0`

No collision for particles. Particles will go through
`GPUParticlesCollision3D<class_GPUParticlesCollision3D>` nodes.

classref-enumeration-constant

`CollisionMode<enum_ParticleProcessMaterial_CollisionMode>`
**COLLISION\_RIGID** = `1`

`RigidBody3D<class_RigidBody3D>`-style collision for particles using
`GPUParticlesCollision3D<class_GPUParticlesCollision3D>` nodes.

classref-enumeration-constant

`CollisionMode<enum_ParticleProcessMaterial_CollisionMode>`
**COLLISION\_HIDE\_ON\_CONTACT** = `2`

Hide particles instantly when colliding with a
`GPUParticlesCollision3D<class_GPUParticlesCollision3D>` node. This can
be combined with a subemitter that uses the
`COLLISION_RIGID<class_ParticleProcessMaterial_constant_COLLISION_RIGID>`
collision mode to "replace" the parent particle with the subemitter on
impact.

classref-enumeration-constant

`CollisionMode<enum_ParticleProcessMaterial_CollisionMode>`
**COLLISION\_MAX** = `3`

Represents the size of the
`CollisionMode<enum_ParticleProcessMaterial_CollisionMode>` enum.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`Texture2D<class_Texture2D>` **alpha\_curve**
`🔗<class_ParticleProcessMaterial_property_alpha_curve>`

classref-property-setget

-   `void (No return value.)` **set\_alpha\_curve**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_alpha\_curve**()

The alpha value of each particle's color will be multiplied by this
`CurveTexture<class_CurveTexture>` over its lifetime.

\*\*Note:\*\*
`alpha_curve<class_ParticleProcessMaterial_property_alpha_curve>`
multiplies the particle mesh's vertex colors. To have a visible effect
on a `BaseMaterial3D<class_BaseMaterial3D>`,
`BaseMaterial3D.vertex_color_use_as_albedo<class_BaseMaterial3D_property_vertex_color_use_as_albedo>`
*must* be `true`. For a `ShaderMaterial<class_ShaderMaterial>`,
`ALBEDO *= COLOR.rgb;` must be inserted in the shader's `fragment()`
function. Otherwise,
`alpha_curve<class_ParticleProcessMaterial_property_alpha_curve>` will
have no visible effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **angle\_curve**
`🔗<class_ParticleProcessMaterial_property_angle_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Each particle's rotation will be animated along this
`CurveTexture<class_CurveTexture>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angle\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_angle_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum initial rotation applied to each particle, in degrees.

Only applied when
`particle_flag_disable_z<class_ParticleProcessMaterial_property_particle_flag_disable_z>`
or
`particle_flag_rotate_y<class_ParticleProcessMaterial_property_particle_flag_rotate_y>`
are `true` or the `BaseMaterial3D<class_BaseMaterial3D>` being used to
draw the particle is using
`BaseMaterial3D.BILLBOARD_PARTICLES<class_BaseMaterial3D_constant_BILLBOARD_PARTICLES>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angle\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_angle_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`angle_max<class_ParticleProcessMaterial_property_angle_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **angular\_velocity\_curve**
`🔗<class_ParticleProcessMaterial_property_angular_velocity_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Each particle's angular velocity (rotation speed) will vary along this
`CurveTexture<class_CurveTexture>` over its lifetime.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_velocity\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_angular_velocity_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum initial angular velocity (rotation speed) applied to each
particle in *degrees* per second.

Only applied when
`particle_flag_disable_z<class_ParticleProcessMaterial_property_particle_flag_disable_z>`
or
`particle_flag_rotate_y<class_ParticleProcessMaterial_property_particle_flag_rotate_y>`
are `true` or the `BaseMaterial3D<class_BaseMaterial3D>` being used to
draw the particle is using
`BaseMaterial3D.BILLBOARD_PARTICLES<class_BaseMaterial3D_constant_BILLBOARD_PARTICLES>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **angular\_velocity\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_angular_velocity_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`angular_velocity_max<class_ParticleProcessMaterial_property_angular_velocity_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **anim\_offset\_curve**
`🔗<class_ParticleProcessMaterial_property_anim_offset_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Each particle's animation offset will vary along this
`CurveTexture<class_CurveTexture>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **anim\_offset\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_anim_offset_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum animation offset that corresponds to frame index in the texture.
`0` is the first frame, `1` is the last one. See
`CanvasItemMaterial.particles_animation<class_CanvasItemMaterial_property_particles_animation>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **anim\_offset\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_anim_offset_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`anim_offset_max<class_ParticleProcessMaterial_property_anim_offset_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **anim\_speed\_curve**
`🔗<class_ParticleProcessMaterial_property_anim_speed_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Each particle's animation speed will vary along this
`CurveTexture<class_CurveTexture>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **anim\_speed\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_anim_speed_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum particle animation speed. Animation speed of `1` means that the
particles will make full `0` to `1` offset cycle during lifetime, `2`
means `2` cycles etc.

With animation speed greater than `1`, remember to enable
`CanvasItemMaterial.particles_anim_loop<class_CanvasItemMaterial_property_particles_anim_loop>`
property if you want the animation to repeat.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **anim\_speed\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_anim_speed_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`anim_speed_max<class_ParticleProcessMaterial_property_anim_speed_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **attractor\_interaction\_enabled** = `true`
`🔗<class_ParticleProcessMaterial_property_attractor_interaction_enabled>`

classref-property-setget

-   `void (No return value.)`
    **set\_attractor\_interaction\_enabled**(value: `bool<class_bool>`)
-   `bool<class_bool>` **is\_attractor\_interaction\_enabled**()

If `true`, interaction with particle attractors is enabled. In 3D,
attraction only occurs within the area defined by the
`GPUParticles3D<class_GPUParticles3D>` node's
`GPUParticles3D.visibility_aabb<class_GPUParticles3D_property_visibility_aabb>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **collision\_bounce**
`🔗<class_ParticleProcessMaterial_property_collision_bounce>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_bounce**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_collision\_bounce**()

The particles' bounciness. Values range from `0` (no bounce) to `1`
(full bounciness). Only effective if
`collision_mode<class_ParticleProcessMaterial_property_collision_mode>`
is
`COLLISION_RIGID<class_ParticleProcessMaterial_constant_COLLISION_RIGID>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **collision\_friction**
`🔗<class_ParticleProcessMaterial_property_collision_friction>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_friction**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_collision\_friction**()

The particles' friction. Values range from `0` (frictionless) to `1`
(maximum friction). Only effective if
`collision_mode<class_ParticleProcessMaterial_property_collision_mode>`
is
`COLLISION_RIGID<class_ParticleProcessMaterial_constant_COLLISION_RIGID>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`CollisionMode<enum_ParticleProcessMaterial_CollisionMode>`
**collision\_mode** = `0`
`🔗<class_ParticleProcessMaterial_property_collision_mode>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_mode**(value:
    `CollisionMode<enum_ParticleProcessMaterial_CollisionMode>`)
-   `CollisionMode<enum_ParticleProcessMaterial_CollisionMode>`
    **get\_collision\_mode**()

The particles' collision mode.

\*\*Note:\*\* 3D Particles can only collide with
`GPUParticlesCollision3D<class_GPUParticlesCollision3D>` nodes, not
`PhysicsBody3D<class_PhysicsBody3D>` nodes. To make particles collide
with various objects, you can add
`GPUParticlesCollision3D<class_GPUParticlesCollision3D>` nodes as
children of `PhysicsBody3D<class_PhysicsBody3D>` nodes. In 3D,
collisions only occur within the area defined by the
`GPUParticles3D<class_GPUParticles3D>` node's
`GPUParticles3D.visibility_aabb<class_GPUParticles3D_property_visibility_aabb>`.

\*\*Note:\*\* 2D Particles can only collide with
`LightOccluder2D<class_LightOccluder2D>` nodes, not
`PhysicsBody2D<class_PhysicsBody2D>` nodes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **collision\_use\_scale** = `false`
`🔗<class_ParticleProcessMaterial_property_collision_use_scale>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_use\_scale**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_collision\_using\_scale**()

If `true`,
`GPUParticles3D.collision_base_size<class_GPUParticles3D_property_collision_base_size>`
is multiplied by the particle's effective scale (see
`scale_min<class_ParticleProcessMaterial_property_scale_min>`,
`scale_max<class_ParticleProcessMaterial_property_scale_max>`,
`scale_curve<class_ParticleProcessMaterial_property_scale_curve>`, and
`scale_over_velocity_curve<class_ParticleProcessMaterial_property_scale_over_velocity_curve>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Color<class_Color>` **color** = `Color(1, 1, 1, 1)`
`🔗<class_ParticleProcessMaterial_property_color>`

classref-property-setget

-   `void (No return value.)` **set\_color**(value:
    `Color<class_Color>`)
-   `Color<class_Color>` **get\_color**()

Each particle's initial color. If the
`GPUParticles2D<class_GPUParticles2D>`'s `texture` is defined, it will
be multiplied by this color.

\*\*Note:\*\* `color<class_ParticleProcessMaterial_property_color>`
multiplies the particle mesh's vertex colors. To have a visible effect
on a `BaseMaterial3D<class_BaseMaterial3D>`,
`BaseMaterial3D.vertex_color_use_as_albedo<class_BaseMaterial3D_property_vertex_color_use_as_albedo>`
*must* be `true`. For a `ShaderMaterial<class_ShaderMaterial>`,
`ALBEDO *= COLOR.rgb;` must be inserted in the shader's `fragment()`
function. Otherwise,
`color<class_ParticleProcessMaterial_property_color>` will have no
visible effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **color\_initial\_ramp**
`🔗<class_ParticleProcessMaterial_property_color_initial_ramp>`

classref-property-setget

-   `void (No return value.)` **set\_color\_initial\_ramp**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_color\_initial\_ramp**()

Each particle's initial color will vary along this
`GradientTexture1D<class_GradientTexture1D>` (multiplied with
`color<class_ParticleProcessMaterial_property_color>`).

\*\*Note:\*\*
`color_initial_ramp<class_ParticleProcessMaterial_property_color_initial_ramp>`
multiplies the particle mesh's vertex colors. To have a visible effect
on a `BaseMaterial3D<class_BaseMaterial3D>`,
`BaseMaterial3D.vertex_color_use_as_albedo<class_BaseMaterial3D_property_vertex_color_use_as_albedo>`
*must* be `true`. For a `ShaderMaterial<class_ShaderMaterial>`,
`ALBEDO *= COLOR.rgb;` must be inserted in the shader's `fragment()`
function. Otherwise,
`color_initial_ramp<class_ParticleProcessMaterial_property_color_initial_ramp>`
will have no visible effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **color\_ramp**
`🔗<class_ParticleProcessMaterial_property_color_ramp>`

classref-property-setget

-   `void (No return value.)` **set\_color\_ramp**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_color\_ramp**()

Each particle's color will vary along this
`GradientTexture1D<class_GradientTexture1D>` over its lifetime
(multiplied with `color<class_ParticleProcessMaterial_property_color>`).

\*\*Note:\*\*
`color_ramp<class_ParticleProcessMaterial_property_color_ramp>`
multiplies the particle mesh's vertex colors. To have a visible effect
on a `BaseMaterial3D<class_BaseMaterial3D>`,
`BaseMaterial3D.vertex_color_use_as_albedo<class_BaseMaterial3D_property_vertex_color_use_as_albedo>`
*must* be `true`. For a `ShaderMaterial<class_ShaderMaterial>`,
`ALBEDO *= COLOR.rgb;` must be inserted in the shader's `fragment()`
function. Otherwise,
`color_ramp<class_ParticleProcessMaterial_property_color_ramp>` will
have no visible effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **damping\_curve**
`🔗<class_ParticleProcessMaterial_property_damping_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Damping will vary along this `CurveTexture<class_CurveTexture>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **damping\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_damping_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

The maximum rate at which particles lose velocity. For example value of
`100` means that the particle will go from `100` velocity to `0` in `1`
second.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **damping\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_damping_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`damping_max<class_ParticleProcessMaterial_property_damping_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **direction** = `Vector3(1, 0, 0)`
`🔗<class_ParticleProcessMaterial_property_direction>`

classref-property-setget

-   `void (No return value.)` **set\_direction**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_direction**()

Unit vector specifying the particles' emission direction.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **directional\_velocity\_curve**
`🔗<class_ParticleProcessMaterial_property_directional_velocity_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

A curve that specifies the velocity along each of the axes of the
particle system along its lifetime.

\*\*Note:\*\* Animated velocities will not be affected by damping, use
`velocity_limit_curve<class_ParticleProcessMaterial_property_velocity_limit_curve>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **directional\_velocity\_max**
`🔗<class_ParticleProcessMaterial_property_directional_velocity_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum directional velocity value, which is multiplied by
`directional_velocity_curve<class_ParticleProcessMaterial_property_directional_velocity_curve>`.

\*\*Note:\*\* Animated velocities will not be affected by damping, use
`velocity_limit_curve<class_ParticleProcessMaterial_property_velocity_limit_curve>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **directional\_velocity\_min**
`🔗<class_ParticleProcessMaterial_property_directional_velocity_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum directional velocity value, which is multiplied by
`directional_velocity_curve<class_ParticleProcessMaterial_property_directional_velocity_curve>`.

\*\*Note:\*\* Animated velocities will not be affected by damping, use
`velocity_limit_curve<class_ParticleProcessMaterial_property_velocity_limit_curve>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **emission\_box\_extents**
`🔗<class_ParticleProcessMaterial_property_emission_box_extents>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_box\_extents**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_emission\_box\_extents**()

The box's extents if
`emission_shape<class_ParticleProcessMaterial_property_emission_shape>`
is set to
`EMISSION_SHAPE_BOX<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_BOX>`.

\*\*Note:\*\*
`emission_box_extents<class_ParticleProcessMaterial_property_emission_box_extents>`
starts from the center point and applies the X, Y, and Z values in both
directions. The size is twice the area of the extents.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **emission\_color\_texture**
`🔗<class_ParticleProcessMaterial_property_emission_color_texture>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_color\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_emission\_color\_texture**()

Particle color will be modulated by color determined by sampling this
texture at the same point as the
`emission_point_texture<class_ParticleProcessMaterial_property_emission_point_texture>`.

\*\*Note:\*\*
`emission_color_texture<class_ParticleProcessMaterial_property_emission_color_texture>`
multiplies the particle mesh's vertex colors. To have a visible effect
on a `BaseMaterial3D<class_BaseMaterial3D>`,
`BaseMaterial3D.vertex_color_use_as_albedo<class_BaseMaterial3D_property_vertex_color_use_as_albedo>`
*must* be `true`. For a `ShaderMaterial<class_ShaderMaterial>`,
`ALBEDO *= COLOR.rgb;` must be inserted in the shader's `fragment()`
function. Otherwise,
`emission_color_texture<class_ParticleProcessMaterial_property_emission_color_texture>`
will have no visible effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **emission\_curve**
`🔗<class_ParticleProcessMaterial_property_emission_curve>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_curve**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_emission\_curve**()

Each particle's color will be multiplied by this
`CurveTexture<class_CurveTexture>` over its lifetime.

\*\*Note:\*\*
`emission_curve<class_ParticleProcessMaterial_property_emission_curve>`
multiplies the particle mesh's vertex colors. To have a visible effect
on a `BaseMaterial3D<class_BaseMaterial3D>`,
`BaseMaterial3D.vertex_color_use_as_albedo<class_BaseMaterial3D_property_vertex_color_use_as_albedo>`
*must* be `true`. For a `ShaderMaterial<class_ShaderMaterial>`,
`ALBEDO *= COLOR.rgb;` must be inserted in the shader's `fragment()`
function. Otherwise,
`emission_curve<class_ParticleProcessMaterial_property_emission_curve>`
will have no visible effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **emission\_normal\_texture**
`🔗<class_ParticleProcessMaterial_property_emission_normal_texture>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_normal\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_emission\_normal\_texture**()

Particle velocity and rotation will be set by sampling this texture at
the same point as the
`emission_point_texture<class_ParticleProcessMaterial_property_emission_point_texture>`.
Used only in
`EMISSION_SHAPE_DIRECTED_POINTS<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_DIRECTED_POINTS>`.
Can be created automatically from mesh or node by selecting "Create
Emission Points from Mesh/Node" under the "Particles" tool in the
toolbar.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **emission\_point\_count**
`🔗<class_ParticleProcessMaterial_property_emission_point_count>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_point\_count**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_emission\_point\_count**()

The number of emission points if
`emission_shape<class_ParticleProcessMaterial_property_emission_shape>`
is set to
`EMISSION_SHAPE_POINTS<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_POINTS>`
or
`EMISSION_SHAPE_DIRECTED_POINTS<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_DIRECTED_POINTS>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **emission\_point\_texture**
`🔗<class_ParticleProcessMaterial_property_emission_point_texture>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_point\_texture**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_emission\_point\_texture**()

Particles will be emitted at positions determined by sampling this
texture at a random position. Used with
`EMISSION_SHAPE_POINTS<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_POINTS>`
and
`EMISSION_SHAPE_DIRECTED_POINTS<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_DIRECTED_POINTS>`.
Can be created automatically from mesh or node by selecting "Create
Emission Points from Mesh/Node" under the "Particles" tool in the
toolbar.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **emission\_ring\_axis**
`🔗<class_ParticleProcessMaterial_property_emission_ring_axis>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_ring\_axis**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_emission\_ring\_axis**()

The axis of the ring when using the emitter
`EMISSION_SHAPE_RING<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_RING>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **emission\_ring\_cone\_angle**
`🔗<class_ParticleProcessMaterial_property_emission_ring_cone_angle>`

classref-property-setget

-   `void (No return value.)`
    **set\_emission\_ring\_cone\_angle**(value: `float<class_float>`)
-   `float<class_float>` **get\_emission\_ring\_cone\_angle**()

The angle of the cone when using the emitter
`EMISSION_SHAPE_RING<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_RING>`.
The default angle of 90 degrees results in a ring, while an angle of 0
degrees results in a cone. Intermediate values will result in a ring
where one end is larger than the other.

\*\*Note:\*\* Depending on
`emission_ring_height<class_ParticleProcessMaterial_property_emission_ring_height>`,
the angle may be clamped if the ring's end is reached to form a perfect
cone.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **emission\_ring\_height**
`🔗<class_ParticleProcessMaterial_property_emission_ring_height>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_ring\_height**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_emission\_ring\_height**()

The height of the ring when using the emitter
`EMISSION_SHAPE_RING<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_RING>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **emission\_ring\_inner\_radius**
`🔗<class_ParticleProcessMaterial_property_emission_ring_inner_radius>`

classref-property-setget

-   `void (No return value.)`
    **set\_emission\_ring\_inner\_radius**(value: `float<class_float>`)
-   `float<class_float>` **get\_emission\_ring\_inner\_radius**()

The inner radius of the ring when using the emitter
`EMISSION_SHAPE_RING<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_RING>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **emission\_ring\_radius**
`🔗<class_ParticleProcessMaterial_property_emission_ring_radius>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_ring\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_emission\_ring\_radius**()

The radius of the ring when using the emitter
`EMISSION_SHAPE_RING<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_RING>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`EmissionShape<enum_ParticleProcessMaterial_EmissionShape>`
**emission\_shape** = `0`
`🔗<class_ParticleProcessMaterial_property_emission_shape>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_shape**(value:
    `EmissionShape<enum_ParticleProcessMaterial_EmissionShape>`)
-   `EmissionShape<enum_ParticleProcessMaterial_EmissionShape>`
    **get\_emission\_shape**()

Particles will be emitted inside this region. Use
`EmissionShape<enum_ParticleProcessMaterial_EmissionShape>` constants
for values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **emission\_shape\_offset** =
`Vector3(0, 0, 0)`
`🔗<class_ParticleProcessMaterial_property_emission_shape_offset>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_shape\_offset**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_emission\_shape\_offset**()

The offset for the
`emission_shape<class_ParticleProcessMaterial_property_emission_shape>`,
in local space.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **emission\_shape\_scale** = `Vector3(1, 1, 1)`
`🔗<class_ParticleProcessMaterial_property_emission_shape_scale>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_shape\_scale**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_emission\_shape\_scale**()

The scale of the
`emission_shape<class_ParticleProcessMaterial_property_emission_shape>`,
in local space.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **emission\_sphere\_radius**
`🔗<class_ParticleProcessMaterial_property_emission_sphere_radius>`

classref-property-setget

-   `void (No return value.)` **set\_emission\_sphere\_radius**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_emission\_sphere\_radius**()

The sphere's radius if
`emission_shape<class_ParticleProcessMaterial_property_emission_shape>`
is set to
`EMISSION_SHAPE_SPHERE<class_ParticleProcessMaterial_constant_EMISSION_SHAPE_SPHERE>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **flatness** = `0.0`
`🔗<class_ParticleProcessMaterial_property_flatness>`

classref-property-setget

-   `void (No return value.)` **set\_flatness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_flatness**()

Amount of `spread<class_ParticleProcessMaterial_property_spread>` along
the Y axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **gravity** = `Vector3(0, -9.8, 0)`
`🔗<class_ParticleProcessMaterial_property_gravity>`

classref-property-setget

-   `void (No return value.)` **set\_gravity**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_gravity**()

Gravity applied to every particle.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **hue\_variation\_curve**
`🔗<class_ParticleProcessMaterial_property_hue_variation_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Each particle's hue will vary along this
`CurveTexture<class_CurveTexture>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **hue\_variation\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_hue_variation_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum initial hue variation applied to each particle. It will shift
the particle color's hue.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **hue\_variation\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_hue_variation_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`hue_variation_max<class_ParticleProcessMaterial_property_hue_variation_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **inherit\_velocity\_ratio** = `0.0`
`🔗<class_ParticleProcessMaterial_property_inherit_velocity_ratio>`

classref-property-setget

-   `void (No return value.)` **set\_inherit\_velocity\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_inherit\_velocity\_ratio**()

Percentage of the velocity of the respective
`GPUParticles2D<class_GPUParticles2D>` or
`GPUParticles3D<class_GPUParticles3D>` inherited by each particle when
spawning.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **initial\_velocity\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_initial_velocity_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum initial velocity magnitude for each particle. Direction comes
from `direction<class_ParticleProcessMaterial_property_direction>` and
`spread<class_ParticleProcessMaterial_property_spread>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **initial\_velocity\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_initial_velocity_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`initial_velocity_max<class_ParticleProcessMaterial_property_initial_velocity_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **lifetime\_randomness** = `0.0`
`🔗<class_ParticleProcessMaterial_property_lifetime_randomness>`

classref-property-setget

-   `void (No return value.)` **set\_lifetime\_randomness**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_lifetime\_randomness**()

Particle lifetime randomness ratio. The equation for the lifetime of a
particle is `lifetime * (1.0 - randf() * lifetime_randomness)`. For
example, a
`lifetime_randomness<class_ParticleProcessMaterial_property_lifetime_randomness>`
of `0.4` scales the lifetime between `0.6` to `1.0` of its original
value.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **linear\_accel\_curve**
`🔗<class_ParticleProcessMaterial_property_linear_accel_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Each particle's linear acceleration will vary along this
`CurveTexture<class_CurveTexture>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_accel\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_linear_accel_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum linear acceleration applied to each particle in the direction of
motion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **linear\_accel\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_linear_accel_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`linear_accel_max<class_ParticleProcessMaterial_property_linear_accel_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **orbit\_velocity\_curve**
`🔗<class_ParticleProcessMaterial_property_orbit_velocity_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Each particle's orbital velocity will vary along this
`CurveTexture<class_CurveTexture>`.

\*\*Note:\*\* For 3D orbital velocity, use a
`CurveXYZTexture<class_CurveXYZTexture>`.

\*\*Note:\*\* Animated velocities will not be affected by damping, use
`velocity_limit_curve<class_ParticleProcessMaterial_property_velocity_limit_curve>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **orbit\_velocity\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_orbit_velocity_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum orbital velocity applied to each particle. Makes the particles
circle around origin. Specified in number of full rotations around
origin per second.

\*\*Note:\*\* Animated velocities will not be affected by damping, use
`velocity_limit_curve<class_ParticleProcessMaterial_property_velocity_limit_curve>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **orbit\_velocity\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_orbit_velocity_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`orbit_velocity_max<class_ParticleProcessMaterial_property_orbit_velocity_max>`.

\*\*Note:\*\* Animated velocities will not be affected by damping, use
`velocity_limit_curve<class_ParticleProcessMaterial_property_velocity_limit_curve>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **particle\_flag\_align\_y** = `false`
`🔗<class_ParticleProcessMaterial_property_particle_flag_align_y>`

classref-property-setget

-   `void (No return value.)` **set\_particle\_flag**(particle\_flag:
    `ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`, enable:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_particle\_flag**(particle\_flag:
    `ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Align Y axis of particle with the direction of its velocity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **particle\_flag\_damping\_as\_friction** = `false`
`🔗<class_ParticleProcessMaterial_property_particle_flag_damping_as_friction>`

classref-property-setget

-   `void (No return value.)` **set\_particle\_flag**(particle\_flag:
    `ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`, enable:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_particle\_flag**(particle\_flag:
    `ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Changes the behavior of the damping properties from a linear
deceleration to a deceleration based on speed percentage.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **particle\_flag\_disable\_z** = `false`
`🔗<class_ParticleProcessMaterial_property_particle_flag_disable_z>`

classref-property-setget

-   `void (No return value.)` **set\_particle\_flag**(particle\_flag:
    `ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`, enable:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_particle\_flag**(particle\_flag:
    `ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, particles will not move on the z axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **particle\_flag\_rotate\_y** = `false`
`🔗<class_ParticleProcessMaterial_property_particle_flag_rotate_y>`

classref-property-setget

-   `void (No return value.)` **set\_particle\_flag**(particle\_flag:
    `ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`, enable:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_particle\_flag**(particle\_flag:
    `ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

If `true`, particles rotate around Y axis by
`angle_min<class_ParticleProcessMaterial_property_angle_min>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **radial\_accel\_curve**
`🔗<class_ParticleProcessMaterial_property_radial_accel_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Each particle's radial acceleration will vary along this
`CurveTexture<class_CurveTexture>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radial\_accel\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_radial_accel_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum radial acceleration applied to each particle. Makes particle
accelerate away from the origin or towards it if negative.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radial\_accel\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_radial_accel_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`radial_accel_max<class_ParticleProcessMaterial_property_radial_accel_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **radial\_velocity\_curve**
`🔗<class_ParticleProcessMaterial_property_radial_velocity_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

A `CurveTexture<class_CurveTexture>` that defines the velocity over the
particle's lifetime away (or toward) the
`velocity_pivot<class_ParticleProcessMaterial_property_velocity_pivot>`.

\*\*Note:\*\* Animated velocities will not be affected by damping, use
`velocity_limit_curve<class_ParticleProcessMaterial_property_velocity_limit_curve>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radial\_velocity\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_radial_velocity_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum radial velocity applied to each particle. Makes particles move
away from the
`velocity_pivot<class_ParticleProcessMaterial_property_velocity_pivot>`,
or toward it if negative.

\*\*Note:\*\* Animated velocities will not be affected by damping, use
`velocity_limit_curve<class_ParticleProcessMaterial_property_velocity_limit_curve>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **radial\_velocity\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_radial_velocity_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum radial velocity applied to each particle. Makes particles move
away from the
`velocity_pivot<class_ParticleProcessMaterial_property_velocity_pivot>`,
or toward it if negative.

\*\*Note:\*\* Animated velocities will not be affected by damping, use
`velocity_limit_curve<class_ParticleProcessMaterial_property_velocity_limit_curve>`
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **scale\_curve**
`🔗<class_ParticleProcessMaterial_property_scale_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Each particle's scale will vary along this
`CurveTexture<class_CurveTexture>` over its lifetime. If a
`CurveXYZTexture<class_CurveXYZTexture>` is supplied instead, the scale
will be separated per-axis.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **scale\_max** = `1.0`
`🔗<class_ParticleProcessMaterial_property_scale_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum initial scale applied to each particle.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **scale\_min** = `1.0`
`🔗<class_ParticleProcessMaterial_property_scale_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`scale_max<class_ParticleProcessMaterial_property_scale_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **scale\_over\_velocity\_curve**
`🔗<class_ParticleProcessMaterial_property_scale_over_velocity_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Either a `CurveTexture<class_CurveTexture>` or a
`CurveXYZTexture<class_CurveXYZTexture>` that scales each particle based
on its velocity.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **scale\_over\_velocity\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_scale_over_velocity_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum velocity value reference for
`scale_over_velocity_curve<class_ParticleProcessMaterial_property_scale_over_velocity_curve>`.

`scale_over_velocity_curve<class_ParticleProcessMaterial_property_scale_over_velocity_curve>`
will be interpolated between
`scale_over_velocity_min<class_ParticleProcessMaterial_property_scale_over_velocity_min>`
and
`scale_over_velocity_max<class_ParticleProcessMaterial_property_scale_over_velocity_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **scale\_over\_velocity\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_scale_over_velocity_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum velocity value reference for
`scale_over_velocity_curve<class_ParticleProcessMaterial_property_scale_over_velocity_curve>`.

`scale_over_velocity_curve<class_ParticleProcessMaterial_property_scale_over_velocity_curve>`
will be interpolated between
`scale_over_velocity_min<class_ParticleProcessMaterial_property_scale_over_velocity_min>`
and
`scale_over_velocity_max<class_ParticleProcessMaterial_property_scale_over_velocity_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **spread** = `45.0`
`🔗<class_ParticleProcessMaterial_property_spread>`

classref-property-setget

-   `void (No return value.)` **set\_spread**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_spread**()

Each particle's initial direction range from `+spread` to `-spread`
degrees.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sub\_emitter\_amount\_at\_collision**
`🔗<class_ParticleProcessMaterial_property_sub_emitter_amount_at_collision>`

classref-property-setget

-   `void (No return value.)`
    **set\_sub\_emitter\_amount\_at\_collision**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_sub\_emitter\_amount\_at\_collision**()

The amount of particles to spawn from the subemitter node when a
collision occurs. When combined with
`COLLISION_HIDE_ON_CONTACT<class_ParticleProcessMaterial_constant_COLLISION_HIDE_ON_CONTACT>`
on the main particles material, this can be used to achieve effects such
as raindrops hitting the ground.

\*\*Note:\*\* This value shouldn't exceed
`GPUParticles2D.amount<class_GPUParticles2D_property_amount>` or
`GPUParticles3D.amount<class_GPUParticles3D_property_amount>` defined on
the *subemitter node* (not the main node), relative to the subemitter's
particle lifetime. If the number of particles is exceeded, no new
particles will spawn from the subemitter until enough particles have
expired.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **sub\_emitter\_amount\_at\_end**
`🔗<class_ParticleProcessMaterial_property_sub_emitter_amount_at_end>`

classref-property-setget

-   `void (No return value.)`
    **set\_sub\_emitter\_amount\_at\_end**(value: `int<class_int>`)
-   `int<class_int>` **get\_sub\_emitter\_amount\_at\_end**()

The amount of particles to spawn from the subemitter node when the
particle expires.

\*\*Note:\*\* This value shouldn't exceed
`GPUParticles2D.amount<class_GPUParticles2D_property_amount>` or
`GPUParticles3D.amount<class_GPUParticles3D_property_amount>` defined on
the *subemitter node* (not the main node), relative to the subemitter's
particle lifetime. If the number of particles is exceeded, no new
particles will spawn from the subemitter until enough particles have
expired.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **sub\_emitter\_frequency**
`🔗<class_ParticleProcessMaterial_property_sub_emitter_frequency>`

classref-property-setget

-   `void (No return value.)` **set\_sub\_emitter\_frequency**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_sub\_emitter\_frequency**()

The frequency at which particles should be emitted from the subemitter
node. One particle will be spawned every
`sub_emitter_frequency<class_ParticleProcessMaterial_property_sub_emitter_frequency>`
seconds.

\*\*Note:\*\* This value shouldn't exceed
`GPUParticles2D.amount<class_GPUParticles2D_property_amount>` or
`GPUParticles3D.amount<class_GPUParticles3D_property_amount>` defined on
the *subemitter node* (not the main node), relative to the subemitter's
particle lifetime. If the number of particles is exceeded, no new
particles will spawn from the subemitter until enough particles have
expired.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **sub\_emitter\_keep\_velocity** = `false`
`🔗<class_ParticleProcessMaterial_property_sub_emitter_keep_velocity>`

classref-property-setget

-   `void (No return value.)`
    **set\_sub\_emitter\_keep\_velocity**(value: `bool<class_bool>`)
-   `bool<class_bool>` **get\_sub\_emitter\_keep\_velocity**()

If `true`, the subemitter inherits the parent particle's velocity when
it spawns.

classref-item-separator

------------------------------------------------------------------------

classref-property

`SubEmitterMode<enum_ParticleProcessMaterial_SubEmitterMode>`
**sub\_emitter\_mode** = `0`
`🔗<class_ParticleProcessMaterial_property_sub_emitter_mode>`

classref-property-setget

-   `void (No return value.)` **set\_sub\_emitter\_mode**(value:
    `SubEmitterMode<enum_ParticleProcessMaterial_SubEmitterMode>`)
-   `SubEmitterMode<enum_ParticleProcessMaterial_SubEmitterMode>`
    **get\_sub\_emitter\_mode**()

The particle subemitter mode (see
`GPUParticles2D.sub_emitter<class_GPUParticles2D_property_sub_emitter>`
and
`GPUParticles3D.sub_emitter<class_GPUParticles3D_property_sub_emitter>`).

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **tangential\_accel\_curve**
`🔗<class_ParticleProcessMaterial_property_tangential_accel_curve>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Each particle's tangential acceleration will vary along this
`CurveTexture<class_CurveTexture>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **tangential\_accel\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_tangential_accel_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum tangential acceleration applied to each particle. Tangential
acceleration is perpendicular to the particle's velocity giving the
particles a swirling motion.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **tangential\_accel\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_tangential_accel_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum equivalent of
`tangential_accel_max<class_ParticleProcessMaterial_property_tangential_accel_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **turbulence\_enabled** = `false`
`🔗<class_ParticleProcessMaterial_property_turbulence_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_turbulence\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_turbulence\_enabled**()

If `true`, enables turbulence for the particle system. Turbulence can be
used to vary particle movement according to its position (based on a 3D
noise pattern). In 3D,
`GPUParticlesAttractorVectorField3D<class_GPUParticlesAttractorVectorField3D>`
with `NoiseTexture3D<class_NoiseTexture3D>` can be used as an
alternative to turbulence that works in world space and with multiple
particle systems reacting in the same way.

\*\*Note:\*\* Enabling turbulence has a high performance cost on the
GPU. Only enable turbulence on a few particle systems at once at most,
and consider disabling it when targeting mobile/web platforms.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **turbulence\_influence\_max** = `0.1`
`🔗<class_ParticleProcessMaterial_property_turbulence_influence_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum turbulence influence on each particle.

The actual amount of turbulence influence on each particle is calculated
as a random value between
`turbulence_influence_min<class_ParticleProcessMaterial_property_turbulence_influence_min>`
and
`turbulence_influence_max<class_ParticleProcessMaterial_property_turbulence_influence_max>`
and multiplied by the amount of turbulence influence from
`turbulence_influence_over_life<class_ParticleProcessMaterial_property_turbulence_influence_over_life>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **turbulence\_influence\_min** = `0.1`
`🔗<class_ParticleProcessMaterial_property_turbulence_influence_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum turbulence influence on each particle.

The actual amount of turbulence influence on each particle is calculated
as a random value between
`turbulence_influence_min<class_ParticleProcessMaterial_property_turbulence_influence_min>`
and
`turbulence_influence_max<class_ParticleProcessMaterial_property_turbulence_influence_max>`
and multiplied by the amount of turbulence influence from
`turbulence_influence_over_life<class_ParticleProcessMaterial_property_turbulence_influence_over_life>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **turbulence\_influence\_over\_life**
`🔗<class_ParticleProcessMaterial_property_turbulence_influence_over_life>`

classref-property-setget

-   `void (No return value.)` **set\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_param\_texture**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Each particle's amount of turbulence will be influenced along this
`CurveTexture<class_CurveTexture>` over its life time.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **turbulence\_initial\_displacement\_max** = `0.0`
`🔗<class_ParticleProcessMaterial_property_turbulence_initial_displacement_max>`

classref-property-setget

-   `void (No return value.)` **set\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_max**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Maximum displacement of each particle's spawn position by the
turbulence.

The actual amount of displacement will be a factor of the underlying
turbulence multiplied by a random value between
`turbulence_initial_displacement_min<class_ParticleProcessMaterial_property_turbulence_initial_displacement_min>`
and
`turbulence_initial_displacement_max<class_ParticleProcessMaterial_property_turbulence_initial_displacement_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **turbulence\_initial\_displacement\_min** = `0.0`
`🔗<class_ParticleProcessMaterial_property_turbulence_initial_displacement_min>`

classref-property-setget

-   `void (No return value.)` **set\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
    `float<class_float>`)
-   `float<class_float>` **get\_param\_min**(param:
    `Parameter<enum_ParticleProcessMaterial_Parameter>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

Minimum displacement of each particle's spawn position by the
turbulence.

The actual amount of displacement will be a factor of the underlying
turbulence multiplied by a random value between
`turbulence_initial_displacement_min<class_ParticleProcessMaterial_property_turbulence_initial_displacement_min>`
and
`turbulence_initial_displacement_max<class_ParticleProcessMaterial_property_turbulence_initial_displacement_max>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **turbulence\_noise\_scale** = `9.0`
`🔗<class_ParticleProcessMaterial_property_turbulence_noise_scale>`

classref-property-setget

-   `void (No return value.)` **set\_turbulence\_noise\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_turbulence\_noise\_scale**()

This value controls the overall scale/frequency of the turbulence noise
pattern.

A small scale will result in smaller features with more detail while a
high scale will result in smoother noise with larger features.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **turbulence\_noise\_speed** =
`Vector3(0, 0, 0)`
`🔗<class_ParticleProcessMaterial_property_turbulence_noise_speed>`

classref-property-setget

-   `void (No return value.)` **set\_turbulence\_noise\_speed**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_turbulence\_noise\_speed**()

A scrolling velocity for the turbulence field. This sets a directional
trend for the pattern to move in over time.

The default value of `Vector3(0, 0, 0)` turns off the scrolling.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **turbulence\_noise\_speed\_random** = `0.2`
`🔗<class_ParticleProcessMaterial_property_turbulence_noise_speed_random>`

classref-property-setget

-   `void (No return value.)`
    **set\_turbulence\_noise\_speed\_random**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_turbulence\_noise\_speed\_random**()

The in-place rate of change of the turbulence field. This defines how
quickly the noise pattern varies over time.

A value of 0.0 will result in a fixed pattern.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **turbulence\_noise\_strength** = `1.0`
`🔗<class_ParticleProcessMaterial_property_turbulence_noise_strength>`

classref-property-setget

-   `void (No return value.)`
    **set\_turbulence\_noise\_strength**(value: `float<class_float>`)
-   `float<class_float>` **get\_turbulence\_noise\_strength**()

The turbulence noise strength. Increasing this will result in a
stronger, more contrasting, flow pattern.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Texture2D<class_Texture2D>` **velocity\_limit\_curve**
`🔗<class_ParticleProcessMaterial_property_velocity_limit_curve>`

classref-property-setget

-   `void (No return value.)` **set\_velocity\_limit\_curve**(value:
    `Texture2D<class_Texture2D>`)
-   `Texture2D<class_Texture2D>` **get\_velocity\_limit\_curve**()

A `CurveTexture<class_CurveTexture>` that defines the maximum velocity
of a particle during its lifetime.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Vector3<class_Vector3>` **velocity\_pivot** = `Vector3(0, 0, 0)`
`🔗<class_ParticleProcessMaterial_property_velocity_pivot>`

classref-property-setget

-   `void (No return value.)` **set\_velocity\_pivot**(value:
    `Vector3<class_Vector3>`)
-   `Vector3<class_Vector3>` **get\_velocity\_pivot**()

A pivot point used to calculate radial and orbital velocity of
particles.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Vector2<class_Vector2>` **get\_param**(param:
`Parameter<enum_ParticleProcessMaterial_Parameter>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ParticleProcessMaterial_method_get_param>`

Returns the minimum and maximum values of the given `param` as a vector.

The `x` component of the returned vector corresponds to minimum and the
`y` component corresponds to maximum.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_param\_max**(param:
`Parameter<enum_ParticleProcessMaterial_Parameter>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ParticleProcessMaterial_method_get_param_max>`

Returns the maximum value range for the given parameter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`float<class_float>` **get\_param\_min**(param:
`Parameter<enum_ParticleProcessMaterial_Parameter>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ParticleProcessMaterial_method_get_param_min>`

Returns the minimum value range for the given parameter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Texture2D<class_Texture2D>` **get\_param\_texture**(param:
`Parameter<enum_ParticleProcessMaterial_Parameter>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ParticleProcessMaterial_method_get_param_texture>`

Returns the `Texture2D<class_Texture2D>` used by the specified
parameter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`bool<class_bool>` **get\_particle\_flag**(particle\_flag:
`ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_ParticleProcessMaterial_method_get_particle_flag>`

Returns `true` if the specified particle flag is enabled. See
`ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>` for options.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_param**(param:
`Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
`Vector2<class_Vector2>`)
`🔗<class_ParticleProcessMaterial_method_set_param>`

Sets the minimum and maximum values of the given `param`.

The `x` component of the argument vector corresponds to minimum and the
`y` component corresponds to maximum.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_param\_max**(param:
`Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
`float<class_float>`)
`🔗<class_ParticleProcessMaterial_method_set_param_max>`

Sets the maximum value range for the given parameter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_param\_min**(param:
`Parameter<enum_ParticleProcessMaterial_Parameter>`, value:
`float<class_float>`)
`🔗<class_ParticleProcessMaterial_method_set_param_min>`

Sets the minimum value range for the given parameter.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_param\_texture**(param:
`Parameter<enum_ParticleProcessMaterial_Parameter>`, texture:
`Texture2D<class_Texture2D>`)
`🔗<class_ParticleProcessMaterial_method_set_param_texture>`

Sets the `Texture2D<class_Texture2D>` for the specified
`Parameter<enum_ParticleProcessMaterial_Parameter>`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_particle\_flag**(particle\_flag:
`ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>`, enable:
`bool<class_bool>`)
`🔗<class_ParticleProcessMaterial_method_set_particle_flag>`

If `true`, enables the specified particle flag. See
`ParticleFlags<enum_ParticleProcessMaterial_ParticleFlags>` for options.
