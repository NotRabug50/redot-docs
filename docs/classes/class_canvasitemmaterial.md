github\_url  
hide

# CanvasItemMaterial

**Inherits:** `Material<class_Material>` **&lt;**
`Resource<class_Resource>` **&lt;** `RefCounted<class_RefCounted>`
**&lt;** `Object<class_Object>`

A material for `CanvasItem<class_CanvasItem>`s.

classref-introduction-group

## Description

**CanvasItemMaterial**s provide a means of modifying the textures
associated with a CanvasItem. They specialize in describing blend and
lighting behaviors for textures. Use a
`ShaderMaterial<class_ShaderMaterial>` to more fully customize a
material's interactions with a `CanvasItem<class_CanvasItem>`.

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

## Enumerations

classref-enumeration

enum **BlendMode**: `🔗<enum_CanvasItemMaterial_BlendMode>`

classref-enumeration-constant

`BlendMode<enum_CanvasItemMaterial_BlendMode>` **BLEND\_MODE\_MIX** =
`0`

Mix blending mode. Colors are assumed to be independent of the alpha
(opacity) value.

classref-enumeration-constant

`BlendMode<enum_CanvasItemMaterial_BlendMode>` **BLEND\_MODE\_ADD** =
`1`

Additive blending mode.

classref-enumeration-constant

`BlendMode<enum_CanvasItemMaterial_BlendMode>` **BLEND\_MODE\_SUB** =
`2`

Subtractive blending mode.

classref-enumeration-constant

`BlendMode<enum_CanvasItemMaterial_BlendMode>` **BLEND\_MODE\_MUL** =
`3`

Multiplicative blending mode.

classref-enumeration-constant

`BlendMode<enum_CanvasItemMaterial_BlendMode>`
**BLEND\_MODE\_PREMULT\_ALPHA** = `4`

Mix blending mode. Colors are assumed to be premultiplied by the alpha
(opacity) value.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LightMode**: `🔗<enum_CanvasItemMaterial_LightMode>`

classref-enumeration-constant

`LightMode<enum_CanvasItemMaterial_LightMode>` **LIGHT\_MODE\_NORMAL** =
`0`

Render the material using both light and non-light sensitive material
properties.

classref-enumeration-constant

`LightMode<enum_CanvasItemMaterial_LightMode>` **LIGHT\_MODE\_UNSHADED**
= `1`

Render the material as if there were no light.

classref-enumeration-constant

`LightMode<enum_CanvasItemMaterial_LightMode>`
**LIGHT\_MODE\_LIGHT\_ONLY** = `2`

Render the material as if there were only light.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`BlendMode<enum_CanvasItemMaterial_BlendMode>` **blend\_mode** = `0`
`🔗<class_CanvasItemMaterial_property_blend_mode>`

classref-property-setget

-   `void (No return value.)` **set\_blend\_mode**(value:
    `BlendMode<enum_CanvasItemMaterial_BlendMode>`)
-   `BlendMode<enum_CanvasItemMaterial_BlendMode>`
    **get\_blend\_mode**()

The manner in which a material's rendering is applied to underlying
textures.

classref-item-separator

------------------------------------------------------------------------

classref-property

`LightMode<enum_CanvasItemMaterial_LightMode>` **light\_mode** = `0`
`🔗<class_CanvasItemMaterial_property_light_mode>`

classref-property-setget

-   `void (No return value.)` **set\_light\_mode**(value:
    `LightMode<enum_CanvasItemMaterial_LightMode>`)
-   `LightMode<enum_CanvasItemMaterial_LightMode>`
    **get\_light\_mode**()

The manner in which material reacts to lighting.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **particles\_anim\_h\_frames**
`🔗<class_CanvasItemMaterial_property_particles_anim_h_frames>`

classref-property-setget

-   `void (No return value.)` **set\_particles\_anim\_h\_frames**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_particles\_anim\_h\_frames**()

The number of columns in the spritesheet assigned as
`Texture2D<class_Texture2D>` for a
`GPUParticles2D<class_GPUParticles2D>` or
`CPUParticles2D<class_CPUParticles2D>`.

\*\*Note:\*\* This property is only used and visible in the editor if
`particles_animation<class_CanvasItemMaterial_property_particles_animation>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **particles\_anim\_loop**
`🔗<class_CanvasItemMaterial_property_particles_anim_loop>`

classref-property-setget

-   `void (No return value.)` **set\_particles\_anim\_loop**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_particles\_anim\_loop**()

If `true`, the particles animation will loop.

\*\*Note:\*\* This property is only used and visible in the editor if
`particles_animation<class_CanvasItemMaterial_property_particles_animation>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`int<class_int>` **particles\_anim\_v\_frames**
`🔗<class_CanvasItemMaterial_property_particles_anim_v_frames>`

classref-property-setget

-   `void (No return value.)` **set\_particles\_anim\_v\_frames**(value:
    `int<class_int>`)
-   `int<class_int>` **get\_particles\_anim\_v\_frames**()

The number of rows in the spritesheet assigned as
`Texture2D<class_Texture2D>` for a
`GPUParticles2D<class_GPUParticles2D>` or
`CPUParticles2D<class_CPUParticles2D>`.

\*\*Note:\*\* This property is only used and visible in the editor if
`particles_animation<class_CanvasItemMaterial_property_particles_animation>`
is `true`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **particles\_animation** = `false`
`🔗<class_CanvasItemMaterial_property_particles_animation>`

classref-property-setget

-   `void (No return value.)` **set\_particles\_animation**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **get\_particles\_animation**()

If `true`, enable spritesheet-based animation features when assigned to
`GPUParticles2D<class_GPUParticles2D>` and
`CPUParticles2D<class_CPUParticles2D>` nodes. The
`ParticleProcessMaterial.anim_speed_max<class_ParticleProcessMaterial_property_anim_speed_max>`
or
`CPUParticles2D.anim_speed_max<class_CPUParticles2D_property_anim_speed_max>`
should also be set to a positive value for the animation to play.

This property (and other `particles_anim_*` properties that depend on
it) has no effect on other types of nodes.
