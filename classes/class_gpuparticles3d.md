github\_url  
hide

# GPUParticles3D

**Inherits:** `GeometryInstance3D<class_GeometryInstance3D>` **&lt;**
`VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

A 3D particle emitter.

classref-introduction-group

## Description

3D particle node used to create a variety of particle systems and
effects. **GPUParticles3D** features an emitter that generates some
number of particles at a given rate.

Use `process_material<class_GPUParticles3D_property_process_material>`
to add a `ParticleProcessMaterial<class_ParticleProcessMaterial>` to
configure particle appearance and behavior. Alternatively, you can add a
`ShaderMaterial<class_ShaderMaterial>` which will be applied to all
particles.

classref-introduction-group

## Tutorials

-   `Particle systems (3D) <../tutorials/3d/particles/index>`
-   `Controlling thousands of fish with Particles <../tutorials/performance/vertex_animation/controlling_thousands_of_fish>`
-   [Third Person Shooter (TPS)
    Demo](https://godotengine.org/asset-library/asset/2710)

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Signals

classref-signal

**finished**() `🔗<class_GPUParticles3D_signal_finished>`

Emitted when all active particles have finished processing. To
immediately emit new particles, call
`restart<class_GPUParticles3D_method_restart>`.

Never emitted when `one_shot<class_GPUParticles3D_property_one_shot>` is
disabled, as particles will be emitted and processed continuously.

\*\*Note:\*\* For `one_shot<class_GPUParticles3D_property_one_shot>`
emitters, due to the particles being computed on the GPU, there may be a
short period after receiving the signal during which setting
`emitting<class_GPUParticles3D_property_emitting>` to `true` will not
restart the emission cycle. This delay is avoided by instead calling
`restart<class_GPUParticles3D_method_restart>`.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **DrawOrder**: `🔗<enum_GPUParticles3D_DrawOrder>`

classref-enumeration-constant

`DrawOrder<enum_GPUParticles3D_DrawOrder>` **DRAW\_ORDER\_INDEX** = `0`

Particles are drawn in the order emitted.

classref-enumeration-constant

`DrawOrder<enum_GPUParticles3D_DrawOrder>` **DRAW\_ORDER\_LIFETIME** =
`1`

Particles are drawn in order of remaining lifetime. In other words, the
particle with the highest lifetime is drawn at the front.

classref-enumeration-constant

`DrawOrder<enum_GPUParticles3D_DrawOrder>`
**DRAW\_ORDER\_REVERSE\_LIFETIME** = `2`

Particles are drawn in reverse order of remaining lifetime. In other
words, the particle with the lowest lifetime is drawn at the front.

classref-enumeration-constant

`DrawOrder<enum_GPUParticles3D_DrawOrder>` **DRAW\_ORDER\_VIEW\_DEPTH**
= `3`

Particles are drawn in order of depth.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **EmitFlags**: `🔗<enum_GPUParticles3D_EmitFlags>`

classref-enumeration-constant

`EmitFlags<enum_GPUParticles3D_EmitFlags>` **EMIT\_FLAG\_POSITION** =
`1`

Particle starts at the specified position.

classref-enumeration-constant

`EmitFlags<enum_GPUParticles3D_EmitFlags>`
**EMIT\_FLAG\_ROTATION\_SCALE** = `2`

Particle starts with specified rotation and scale.

classref-enumeration-constant

`EmitFlags<enum_GPUParticles3D_EmitFlags>` **EMIT\_FLAG\_VELOCITY** =
`4`

Particle starts with the specified velocity vector, which defines the
emission direction and speed.

classref-enumeration-constant

`EmitFlags<enum_GPUParticles3D_EmitFlags>` **EMIT\_FLAG\_COLOR** = `8`

Particle starts with specified color.

classref-enumeration-constant

`EmitFlags<enum_GPUParticles3D_EmitFlags>` **EMIT\_FLAG\_CUSTOM** = `16`

Particle starts with specified `CUSTOM` data.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **TransformAlign**: `🔗<enum_GPUParticles3D_TransformAlign>`

classref-enumeration-constant

`TransformAlign<enum_GPUParticles3D_TransformAlign>`
**TRANSFORM\_ALIGN\_DISABLED** = `0`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`TransformAlign<enum_GPUParticles3D_TransformAlign>`
**TRANSFORM\_ALIGN\_Z\_BILLBOARD** = `1`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`TransformAlign<enum_GPUParticles3D_TransformAlign>`
**TRANSFORM\_ALIGN\_Y\_TO\_VELOCITY** = `2`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-enumeration-constant

`TransformAlign<enum_GPUParticles3D_TransformAlign>`
**TRANSFORM\_ALIGN\_Z\_BILLBOARD\_Y\_TO\_VELOCITY** = `3`

There is currently no description for this enum. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Constants

classref-constant

**MAX\_DRAW\_PASSES** = `4`
`🔗<class_GPUParticles3D_constant_MAX_DRAW_PASSES>`

Maximum number of draw passes supported.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`int<class_int>` **amount** = `8`
`🔗<class_GPUParticles3D_property_amount>`

classref-property-setget

-   `void (No return value.)` **set\_amount**(value: `int<class_int>`)
-   `int<class_int>` **get\_amount**()

The number of particles to emit in one emission cycle. The effective
emission rate is `(amount * amount_ratio) / lifetime` particles per
second. Higher values will increase GPU requirements, even if not all
particles are visible at a given time or if
`amount_ratio<class_GPUParticles3D_property_amount_ratio>` is decreased.

\*\*Note:\*\* Changing this value will cause the particle system to
restart. To avoid this, change
`amount_ratio<class_GPUParticles3D_property_amount_ratio>` instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **amount\_ratio** = `1.0`
`🔗<class_GPUParticles3D_property_amount_ratio>`

classref-property-setget

-   `void (No return value.)` **set\_amount\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_amount\_ratio**()

The ratio of particles that should actually be emitted. If set to a
value lower than `1.0`, this will set the amount of emitted particles
throughout the lifetime to `amount * amount_ratio`. Unlike changing
`amount<class_GPUParticles3D_property_amount>`, changing
`amount_ratio<class_GPUParticles3D_property_amount_ratio>` while
emitting does not affect already-emitted particles and doesn't cause the
particle system to restart.
`amount_ratio<class_GPUParticles3D_property_amount_ratio>` can be used
to create effects that make the number of emitted particles vary over
time.

\*\*Note:\*\* Reducing the
`amount_ratio<class_GPUParticles3D_property_amount_ratio>` has no
performance benefit, since resources need to be allocated and processed
for the total `amount<class_GPUParticles3D_property_amount>` of
particles regardless of the
`amount_ratio<class_GPUParticles3D_property_amount_ratio>`. If you don't
intend to change the number of particles emitted while the particles are
emitting, make sure
`amount_ratio<class_GPUParticles3D_property_amount_ratio>` is set to `1`
and change `amount<class_GPUParticles3D_property_amount>` to your liking
instead.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **collision\_base\_size** = `0.01`
`🔗<class_GPUParticles3D_property_collision_base_size>`

classref-property-setget

-   `void (No return value.)` **set\_collision\_base\_size**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_collision\_base\_size**()

The base diameter for particle collision in meters. If particles appear
to sink into the ground when colliding, increase this value. If
particles appear to float when colliding, decrease this value. Only
effective if
`ParticleProcessMaterial.collision_mode<class_ParticleProcessMaterial_property_collision_mode>`
is
`ParticleProcessMaterial.COLLISION_RIGID<class_ParticleProcessMaterial_constant_COLLISION_RIGID>`
or
`ParticleProcessMaterial.COLLISION_HIDE_ON_CONTACT<class_ParticleProcessMaterial_constant_COLLISION_HIDE_ON_CONTACT>`.

\*\*Note:\*\* Particles always have a spherical collision shape.

classref-item-separator

------------------------------------------------------------------------

classref-property

`DrawOrder<enum_GPUParticles3D_DrawOrder>` **draw\_order** = `0`
`🔗<class_GPUParticles3D_property_draw_order>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_order**(value:
    `DrawOrder<enum_GPUParticles3D_DrawOrder>`)
-   `DrawOrder<enum_GPUParticles3D_DrawOrder>` **get\_draw\_order**()

Particle draw order. Uses `DrawOrder<enum_GPUParticles3D_DrawOrder>`
values.

\*\*Note:\*\*
`DRAW_ORDER_INDEX<class_GPUParticles3D_constant_DRAW_ORDER_INDEX>` is
the only option that supports motion vectors for effects like TAA. It is
suggested to use this draw order if the particles are opaque to fix
ghosting artifacts.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Mesh<class_Mesh>` **draw\_pass\_1**
`🔗<class_GPUParticles3D_property_draw_pass_1>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_pass\_mesh**(pass:
    `int<class_int>`, mesh: `Mesh<class_Mesh>`)
-   `Mesh<class_Mesh>` **get\_draw\_pass\_mesh**(pass: `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

`Mesh<class_Mesh>` that is drawn for the first draw pass.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Mesh<class_Mesh>` **draw\_pass\_2**
`🔗<class_GPUParticles3D_property_draw_pass_2>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_pass\_mesh**(pass:
    `int<class_int>`, mesh: `Mesh<class_Mesh>`)
-   `Mesh<class_Mesh>` **get\_draw\_pass\_mesh**(pass: `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

`Mesh<class_Mesh>` that is drawn for the second draw pass.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Mesh<class_Mesh>` **draw\_pass\_3**
`🔗<class_GPUParticles3D_property_draw_pass_3>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_pass\_mesh**(pass:
    `int<class_int>`, mesh: `Mesh<class_Mesh>`)
-   `Mesh<class_Mesh>` **get\_draw\_pass\_mesh**(pass: `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

`Mesh<class_Mesh>` that is drawn for the third draw pass.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Mesh<class_Mesh>` **draw\_pass\_4**
`🔗<class_GPUParticles3D_property_draw_pass_4>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_pass\_mesh**(pass:
    `int<class_int>`, mesh: `Mesh<class_Mesh>`)
-   `Mesh<class_Mesh>` **get\_draw\_pass\_mesh**(pass: `int<class_int>`)
    `const (This method has no side effects. It doesn't modify any of the instance's member variables.)`

`Mesh<class_Mesh>` that is drawn for the fourth draw pass.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **draw\_passes** = `1`
`🔗<class_GPUParticles3D_property_draw_passes>`

classref-property-setget

-   `void (No return value.)` **set\_draw\_passes**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_draw\_passes**()

The number of draw passes when rendering particles.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Skin<class_Skin>` **draw\_skin**
`🔗<class_GPUParticles3D_property_draw_skin>`

classref-property-setget

-   `void (No return value.)` **set\_skin**(value: `Skin<class_Skin>`)
-   `Skin<class_Skin>` **get\_skin**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **emitting** = `true`
`🔗<class_GPUParticles3D_property_emitting>`

classref-property-setget

-   `void (No return value.)` **set\_emitting**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_emitting**()

If `true`, particles are being emitted.
`emitting<class_GPUParticles3D_property_emitting>` can be used to start
and stop particles from emitting. However, if
`one_shot<class_GPUParticles3D_property_one_shot>` is `true` setting
`emitting<class_GPUParticles3D_property_emitting>` to `true` will not
restart the emission cycle unless all active particles have finished
processing. Use the `finished<class_GPUParticles3D_signal_finished>`
signal to be notified once all active particles finish processing.

\*\*Note:\*\* For `one_shot<class_GPUParticles3D_property_one_shot>`
emitters, due to the particles being computed on the GPU, there may be a
short period after receiving the
`finished<class_GPUParticles3D_signal_finished>` signal during which
setting this to `true` will not restart the emission cycle.

\*\*Tip:\*\* If your `one_shot<class_GPUParticles3D_property_one_shot>`
emitter needs to immediately restart emitting particles once
`finished<class_GPUParticles3D_signal_finished>` signal is received,
consider calling `restart<class_GPUParticles3D_method_restart>` instead
of setting `emitting<class_GPUParticles3D_property_emitting>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **explosiveness** = `0.0`
`🔗<class_GPUParticles3D_property_explosiveness>`

classref-property-setget

-   `void (No return value.)` **set\_explosiveness\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_explosiveness\_ratio**()

Time ratio between each emission. If `0`, particles are emitted
continuously. If `1`, all particles are emitted simultaneously.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **fixed\_fps** = `30`
`🔗<class_GPUParticles3D_property_fixed_fps>`

classref-property-setget

-   `void (No return value.)` **set\_fixed\_fps**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_fixed\_fps**()

The particle system's frame rate is fixed to a value. For example,
changing the value to 2 will make the particles render at 2 frames per
second. Note this does not slow down the simulation of the particle
system itself.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **fract\_delta** = `true`
`🔗<class_GPUParticles3D_property_fract_delta>`

classref-property-setget

-   `void (No return value.)` **set\_fractional\_delta**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_fractional\_delta**()

If `true`, results in fractional delta calculation which has a smoother
particles display effect.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **interp\_to\_end** = `0.0`
`🔗<class_GPUParticles3D_property_interp_to_end>`

classref-property-setget

-   `void (No return value.)` **set\_interp\_to\_end**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_interp\_to\_end**()

Causes all the particles in this node to interpolate towards the end of
their lifetime.

\*\*Note:\*\* This only works when used with a
`ParticleProcessMaterial<class_ParticleProcessMaterial>`. It needs to be
manually implemented for custom process shaders.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **interpolate** = `true`
`🔗<class_GPUParticles3D_property_interpolate>`

classref-property-setget

-   `void (No return value.)` **set\_interpolate**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_interpolate**()

Enables particle interpolation, which makes the particle movement
smoother when their `fixed_fps<class_GPUParticles3D_property_fixed_fps>`
is lower than the screen refresh rate.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **lifetime** = `1.0`
`🔗<class_GPUParticles3D_property_lifetime>`

classref-property-setget

-   `void (No return value.)` **set\_lifetime**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_lifetime**()

The amount of time each particle will exist (in seconds). The effective
emission rate is `(amount * amount_ratio) / lifetime` particles per
second.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **local\_coords** = `false`
`🔗<class_GPUParticles3D_property_local_coords>`

classref-property-setget

-   `void (No return value.)` **set\_use\_local\_coordinates**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_use\_local\_coordinates**()

If `true`, particles use the parent node's coordinate space (known as
local coordinates). This will cause particles to move and rotate along
the **GPUParticles3D** node (and its parents) when it is moved or
rotated. If `false`, particles use global coordinates; they will not
move or rotate along the **GPUParticles3D** node (and its parents) when
it is moved or rotated.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **one\_shot** = `false`
`🔗<class_GPUParticles3D_property_one_shot>`

classref-property-setget

-   `void (No return value.)` **set\_one\_shot**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_one\_shot**()

If `true`, only the number of particles equal to
`amount<class_GPUParticles3D_property_amount>` will be emitted.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **preprocess** = `0.0`
`🔗<class_GPUParticles3D_property_preprocess>`

classref-property-setget

-   `void (No return value.)` **set\_pre\_process\_time**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_pre\_process\_time**()

Amount of time to preprocess the particles before animation starts. Lets
you start the animation some time after particles have started emitting.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Material<class_Material>` **process\_material**
`🔗<class_GPUParticles3D_property_process_material>`

classref-property-setget

-   `void (No return value.)` **set\_process\_material**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_process\_material**()

`Material<class_Material>` for processing particles. Can be a
`ParticleProcessMaterial<class_ParticleProcessMaterial>` or a
`ShaderMaterial<class_ShaderMaterial>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **randomness** = `0.0`
`🔗<class_GPUParticles3D_property_randomness>`

classref-property-setget

-   `void (No return value.)` **set\_randomness\_ratio**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_randomness\_ratio**()

Emission randomness ratio.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **speed\_scale** = `1.0`
`🔗<class_GPUParticles3D_property_speed_scale>`

classref-property-setget

-   `void (No return value.)` **set\_speed\_scale**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_speed\_scale**()

Speed scaling ratio. A value of `0` can be used to pause the particles.

classref-item-separator

------------------------------------------------------------------------

classref-property

`NodePath<class_NodePath>` **sub\_emitter** = `NodePath("")`
`🔗<class_GPUParticles3D_property_sub_emitter>`

classref-property-setget

-   `void (No return value.)` **set\_sub\_emitter**(value:
    `NodePath<class_NodePath>`)
-   `NodePath<class_NodePath>` **get\_sub\_emitter**()

Path to another **GPUParticles3D** node that will be used as a
subemitter (see
`ParticleProcessMaterial.sub_emitter_mode<class_ParticleProcessMaterial_property_sub_emitter_mode>`).
Subemitters can be used to achieve effects such as fireworks, sparks on
collision, bubbles popping into water drops, and more.

\*\*Note:\*\* When
`sub_emitter<class_GPUParticles3D_property_sub_emitter>` is set, the
target **GPUParticles3D** node will no longer emit particles on its own.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **trail\_enabled** = `false`
`🔗<class_GPUParticles3D_property_trail_enabled>`

classref-property-setget

-   `void (No return value.)` **set\_trail\_enabled**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_trail\_enabled**()

If `true`, enables particle trails using a mesh skinning system.
Designed to work with `RibbonTrailMesh<class_RibbonTrailMesh>` and
`TubeTrailMesh<class_TubeTrailMesh>`.

\*\*Note:\*\*
`BaseMaterial3D.use_particle_trails<class_BaseMaterial3D_property_use_particle_trails>`
must also be enabled on the particle mesh's material. Otherwise, setting
`trail_enabled<class_GPUParticles3D_property_trail_enabled>` to `true`
will have no effect.

\*\*Note:\*\* Unlike `GPUParticles2D<class_GPUParticles2D>`, the number
of trail sections and subdivisions is set in the
`RibbonTrailMesh<class_RibbonTrailMesh>` or the
`TubeTrailMesh<class_TubeTrailMesh>`'s properties.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **trail\_lifetime** = `0.3`
`🔗<class_GPUParticles3D_property_trail_lifetime>`

classref-property-setget

-   `void (No return value.)` **set\_trail\_lifetime**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_trail\_lifetime**()

The amount of time the particle's trail should represent (in seconds).
Only effective if
`trail_enabled<class_GPUParticles3D_property_trail_enabled>` is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`TransformAlign<enum_GPUParticles3D_TransformAlign>`
**transform\_align** = `0`
`🔗<class_GPUParticles3D_property_transform_align>`

classref-property-setget

-   `void (No return value.)` **set\_transform\_align**(value:
    `TransformAlign<enum_GPUParticles3D_TransformAlign>`)
-   `TransformAlign<enum_GPUParticles3D_TransformAlign>`
    **get\_transform\_align**()

There is currently no description for this property. Please help us by
`contributing one <doc_updating_the_class_reference>`!

classref-item-separator

------------------------------------------------------------------------

classref-property

`AABB<class_AABB>` **visibility\_aabb** = `AABB(-4, -4, -4, 8, 8, 8)`
`🔗<class_GPUParticles3D_property_visibility_aabb>`

classref-property-setget

-   `void (No return value.)` **set\_visibility\_aabb**(value:
    `AABB<class_AABB>`)
-   `AABB<class_AABB>` **get\_visibility\_aabb**()

The `AABB<class_AABB>` that determines the node's region which needs to
be visible on screen for the particle system to be active.
`GeometryInstance3D.extra_cull_margin<class_GeometryInstance3D_property_extra_cull_margin>`
is added on each of the AABB's axes. Particle collisions and attraction
will only occur within this area.

Grow the box if particles suddenly appear/disappear when the node
enters/exits the screen. The `AABB<class_AABB>` can be grown via code or
with the **Particles → Generate AABB** editor tool.

\*\*Note:\*\*
`visibility_aabb<class_GPUParticles3D_property_visibility_aabb>` is
overridden by
`GeometryInstance3D.custom_aabb<class_GeometryInstance3D_property_custom_aabb>`
if that property is set to a non-default value.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`AABB<class_AABB>` **capture\_aabb**()
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GPUParticles3D_method_capture_aabb>`

Returns the axis-aligned bounding box that contains all the particles
that are active in the current frame.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **convert\_from\_particles**(particles:
`Node<class_Node>`)
`🔗<class_GPUParticles3D_method_convert_from_particles>`

Sets this node's properties to match a given
`CPUParticles3D<class_CPUParticles3D>` node.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **emit\_particle**(xform:
`Transform3D<class_Transform3D>`, velocity: `Vector3<class_Vector3>`,
color: `Color<class_Color>`, custom: `Color<class_Color>`, flags:
`int<class_int>`) `🔗<class_GPUParticles3D_method_emit_particle>`

Emits a single particle. Whether `xform`, `velocity`, `color` and
`custom` are applied depends on the value of `flags`. See
`EmitFlags<enum_GPUParticles3D_EmitFlags>`.

The default ParticleProcessMaterial will overwrite `color` and use the
contents of `custom` as `(rotation, age, animation, lifetime)`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`Mesh<class_Mesh>` **get\_draw\_pass\_mesh**(pass: `int<class_int>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GPUParticles3D_method_get_draw_pass_mesh>`

Returns the `Mesh<class_Mesh>` that is drawn at index `pass`.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **restart**()
`🔗<class_GPUParticles3D_method_restart>`

Restarts the particle emission cycle, clearing existing particles. To
avoid particles vanishing from the viewport, wait for the
`finished<class_GPUParticles3D_signal_finished>` signal before calling.

\*\*Note:\*\* The `finished<class_GPUParticles3D_signal_finished>`
signal is only emitted by
`one_shot<class_GPUParticles3D_property_one_shot>` emitters.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_draw\_pass\_mesh**(pass:
`int<class_int>`, mesh: `Mesh<class_Mesh>`)
`🔗<class_GPUParticles3D_method_set_draw_pass_mesh>`

Sets the `Mesh<class_Mesh>` that is drawn at index `pass`.
