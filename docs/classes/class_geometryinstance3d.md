github\_url  
hide

# GeometryInstance3D

**Inherits:** `VisualInstance3D<class_VisualInstance3D>` **&lt;**
`Node3D<class_Node3D>` **&lt;** `Node<class_Node>` **&lt;**
`Object<class_Object>`

**Inherited By:** `CPUParticles3D<class_CPUParticles3D>`,
`CSGShape3D<class_CSGShape3D>`, `GPUParticles3D<class_GPUParticles3D>`,
`Label3D<class_Label3D>`, `MeshInstance3D<class_MeshInstance3D>`,
`MultiMeshInstance3D<class_MultiMeshInstance3D>`,
`SpriteBase3D<class_SpriteBase3D>`

Base node for geometry-based visual instances.

classref-introduction-group

## Description

Base node for geometry-based visual instances. Shares some common
functionality like visibility and custom materials.

classref-introduction-group

## Tutorials

-   `Visibility ranges (HLOD) <../tutorials/3d/visibility_ranges>`

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
</tbody>
</table>

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Enumerations

classref-enumeration

enum **ShadowCastingSetting**:
`🔗<enum_GeometryInstance3D_ShadowCastingSetting>`

classref-enumeration-constant

`ShadowCastingSetting<enum_GeometryInstance3D_ShadowCastingSetting>`
**SHADOW\_CASTING\_SETTING\_OFF** = `0`

Will not cast any shadows. Use this to improve performance for small
geometry that is unlikely to cast noticeable shadows (such as debris).

classref-enumeration-constant

`ShadowCastingSetting<enum_GeometryInstance3D_ShadowCastingSetting>`
**SHADOW\_CASTING\_SETTING\_ON** = `1`

Will cast shadows from all visible faces in the GeometryInstance3D.

Will take culling into account, so faces not being rendered will not be
taken into account when shadow casting.

classref-enumeration-constant

`ShadowCastingSetting<enum_GeometryInstance3D_ShadowCastingSetting>`
**SHADOW\_CASTING\_SETTING\_DOUBLE\_SIDED** = `2`

Will cast shadows from all visible faces in the GeometryInstance3D.

Will not take culling into account, so all faces will be taken into
account when shadow casting.

classref-enumeration-constant

`ShadowCastingSetting<enum_GeometryInstance3D_ShadowCastingSetting>`
**SHADOW\_CASTING\_SETTING\_SHADOWS\_ONLY** = `3`

Will only show the shadows casted from this object.

In other words, the actual mesh will not be visible, only the shadows
casted from the mesh will be.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **GIMode**: `🔗<enum_GeometryInstance3D_GIMode>`

classref-enumeration-constant

`GIMode<enum_GeometryInstance3D_GIMode>` **GI\_MODE\_DISABLED** = `0`

Disabled global illumination mode. Use for dynamic objects that do not
contribute to global illumination (such as characters). When using
`VoxelGI<class_VoxelGI>` and SDFGI, the geometry will *receive* indirect
lighting and reflections but the geometry will not be considered in GI
baking.

classref-enumeration-constant

`GIMode<enum_GeometryInstance3D_GIMode>` **GI\_MODE\_STATIC** = `1`

Baked global illumination mode. Use for static objects that contribute
to global illumination (such as level geometry). This GI mode is
effective when using `VoxelGI<class_VoxelGI>`, SDFGI and
`LightmapGI<class_LightmapGI>`.

classref-enumeration-constant

`GIMode<enum_GeometryInstance3D_GIMode>` **GI\_MODE\_DYNAMIC** = `2`

Dynamic global illumination mode. Use for dynamic objects that
contribute to global illumination. This GI mode is only effective when
using `VoxelGI<class_VoxelGI>`, but it has a higher performance impact
than `GI_MODE_STATIC<class_GeometryInstance3D_constant_GI_MODE_STATIC>`.
When using other GI methods, this will act the same as
`GI_MODE_DISABLED<class_GeometryInstance3D_constant_GI_MODE_DISABLED>`.
When using `LightmapGI<class_LightmapGI>`, the object will receive
indirect lighting using lightmap probes instead of using the baked
lightmap texture.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **LightmapScale**: `🔗<enum_GeometryInstance3D_LightmapScale>`

classref-enumeration-constant

`LightmapScale<enum_GeometryInstance3D_LightmapScale>`
**LIGHTMAP\_SCALE\_1X** = `0`

The standard texel density for lightmapping with
`LightmapGI<class_LightmapGI>`.

classref-enumeration-constant

`LightmapScale<enum_GeometryInstance3D_LightmapScale>`
**LIGHTMAP\_SCALE\_2X** = `1`

Multiplies texel density by 2× for lightmapping with
`LightmapGI<class_LightmapGI>`. To ensure consistency in texel density,
use this when scaling a mesh by a factor between 1.5 and 3.0.

classref-enumeration-constant

`LightmapScale<enum_GeometryInstance3D_LightmapScale>`
**LIGHTMAP\_SCALE\_4X** = `2`

Multiplies texel density by 4× for lightmapping with
`LightmapGI<class_LightmapGI>`. To ensure consistency in texel density,
use this when scaling a mesh by a factor between 3.0 and 6.0.

classref-enumeration-constant

`LightmapScale<enum_GeometryInstance3D_LightmapScale>`
**LIGHTMAP\_SCALE\_8X** = `3`

Multiplies texel density by 8× for lightmapping with
`LightmapGI<class_LightmapGI>`. To ensure consistency in texel density,
use this when scaling a mesh by a factor greater than 6.0.

classref-enumeration-constant

`LightmapScale<enum_GeometryInstance3D_LightmapScale>`
**LIGHTMAP\_SCALE\_MAX** = `4`

Represents the size of the
`LightmapScale<enum_GeometryInstance3D_LightmapScale>` enum.

classref-item-separator

------------------------------------------------------------------------

classref-enumeration

enum **VisibilityRangeFadeMode**:
`🔗<enum_GeometryInstance3D_VisibilityRangeFadeMode>`

classref-enumeration-constant

`VisibilityRangeFadeMode<enum_GeometryInstance3D_VisibilityRangeFadeMode>`
**VISIBILITY\_RANGE\_FADE\_DISABLED** = `0`

Will not fade itself nor its visibility dependencies, hysteresis will be
used instead. This is the fastest approach to manual LOD, but it can
result in noticeable LOD transitions depending on how the LOD meshes are
authored. See
`visibility_range_begin<class_GeometryInstance3D_property_visibility_range_begin>`
and `Node3D.visibility_parent<class_Node3D_property_visibility_parent>`
for more information.

classref-enumeration-constant

`VisibilityRangeFadeMode<enum_GeometryInstance3D_VisibilityRangeFadeMode>`
**VISIBILITY\_RANGE\_FADE\_SELF** = `1`

Will fade-out itself when reaching the limits of its own visibility
range. This is slower than
`VISIBILITY_RANGE_FADE_DISABLED<class_GeometryInstance3D_constant_VISIBILITY_RANGE_FADE_DISABLED>`,
but it can provide smoother transitions. The fading range is determined
by
`visibility_range_begin_margin<class_GeometryInstance3D_property_visibility_range_begin_margin>`
and
`visibility_range_end_margin<class_GeometryInstance3D_property_visibility_range_end_margin>`.

\*\*Note:\*\* Only supported when using the Forward+ rendering method.
When using the Mobile or Compatibility rendering method, this mode acts
like
`VISIBILITY_RANGE_FADE_DISABLED<class_GeometryInstance3D_constant_VISIBILITY_RANGE_FADE_DISABLED>`
but with hysteresis disabled.

classref-enumeration-constant

`VisibilityRangeFadeMode<enum_GeometryInstance3D_VisibilityRangeFadeMode>`
**VISIBILITY\_RANGE\_FADE\_DEPENDENCIES** = `2`

Will fade-in its visibility dependencies (see
`Node3D.visibility_parent<class_Node3D_property_visibility_parent>`)
when reaching the limits of its own visibility range. This is slower
than
`VISIBILITY_RANGE_FADE_DISABLED<class_GeometryInstance3D_constant_VISIBILITY_RANGE_FADE_DISABLED>`,
but it can provide smoother transitions. The fading range is determined
by
`visibility_range_begin_margin<class_GeometryInstance3D_property_visibility_range_begin_margin>`
and
`visibility_range_end_margin<class_GeometryInstance3D_property_visibility_range_end_margin>`.

\*\*Note:\*\* Only supported when using the Forward+ rendering method.
When using the Mobile or Compatibility rendering method, this mode acts
like
`VISIBILITY_RANGE_FADE_DISABLED<class_GeometryInstance3D_constant_VISIBILITY_RANGE_FADE_DISABLED>`
but with hysteresis disabled.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Property Descriptions

classref-property

`ShadowCastingSetting<enum_GeometryInstance3D_ShadowCastingSetting>`
**cast\_shadow** = `1`
`🔗<class_GeometryInstance3D_property_cast_shadow>`

classref-property-setget

-   `void (No return value.)` **set\_cast\_shadows\_setting**(value:
    `ShadowCastingSetting<enum_GeometryInstance3D_ShadowCastingSetting>`)
-   `ShadowCastingSetting<enum_GeometryInstance3D_ShadowCastingSetting>`
    **get\_cast\_shadows\_setting**()

The selected shadow casting flag. See
`ShadowCastingSetting<enum_GeometryInstance3D_ShadowCastingSetting>` for
possible values.

classref-item-separator

------------------------------------------------------------------------

classref-property

`AABB<class_AABB>` **custom\_aabb** = `AABB(0, 0, 0, 0, 0, 0)`
`🔗<class_GeometryInstance3D_property_custom_aabb>`

classref-property-setget

-   `void (No return value.)` **set\_custom\_aabb**(value:
    `AABB<class_AABB>`)
-   `AABB<class_AABB>` **get\_custom\_aabb**()

Overrides the bounding box of this node with a custom one. This can be
used to avoid the expensive `AABB<class_AABB>` recalculation that
happens when a skeleton is used with a
`MeshInstance3D<class_MeshInstance3D>` or to have precise control over
the `MeshInstance3D<class_MeshInstance3D>`'s bounding box. To use the
default AABB, set value to an `AABB<class_AABB>` with all fields set to
`0.0`. To avoid frustum culling, set
`custom_aabb<class_GeometryInstance3D_property_custom_aabb>` to a very
large AABB that covers your entire game world such as
`AABB(-10000, -10000, -10000, 20000, 20000, 20000)`. To disable all
forms of culling (including occlusion culling), call
`RenderingServer.instance_set_ignore_culling<class_RenderingServer_method_instance_set_ignore_culling>`
on the **GeometryInstance3D**'s `RID<class_RID>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **extra\_cull\_margin** = `0.0`
`🔗<class_GeometryInstance3D_property_extra_cull_margin>`

classref-property-setget

-   `void (No return value.)` **set\_extra\_cull\_margin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_extra\_cull\_margin**()

The extra distance added to the GeometryInstance3D's bounding box
(`AABB<class_AABB>`) to increase its cull box.

classref-item-separator

------------------------------------------------------------------------

classref-property

`LightmapScale<enum_GeometryInstance3D_LightmapScale>`
**gi\_lightmap\_scale** = `0`
`🔗<class_GeometryInstance3D_property_gi_lightmap_scale>`

classref-property-setget

-   `void (No return value.)` **set\_lightmap\_scale**(value:
    `LightmapScale<enum_GeometryInstance3D_LightmapScale>`)
-   `LightmapScale<enum_GeometryInstance3D_LightmapScale>`
    **get\_lightmap\_scale**()

The texel density to use for lightmapping in
`LightmapGI<class_LightmapGI>`. Greater scale values provide higher
resolution in the lightmap, which can result in sharper shadows for
lights that have both direct and indirect light baked. However, greater
scale values will also increase the space taken by the mesh in the
lightmap texture, which increases the memory, storage, and bake time
requirements. When using a single mesh at different scales, consider
adjusting this value to keep the lightmap texel density consistent
across meshes.

classref-item-separator

------------------------------------------------------------------------

classref-property

`GIMode<enum_GeometryInstance3D_GIMode>` **gi\_mode** = `1`
`🔗<class_GeometryInstance3D_property_gi_mode>`

classref-property-setget

-   `void (No return value.)` **set\_gi\_mode**(value:
    `GIMode<enum_GeometryInstance3D_GIMode>`)
-   `GIMode<enum_GeometryInstance3D_GIMode>` **get\_gi\_mode**()

The global illumination mode to use for the whole geometry. To avoid
inconsistent results, use a mode that matches the purpose of the mesh
during gameplay (static/dynamic).

\*\*Note:\*\* Lights' bake mode will also affect the global illumination
rendering. See
`Light3D.light_bake_mode<class_Light3D_property_light_bake_mode>`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`bool<class_bool>` **ignore\_occlusion\_culling** = `false`
`🔗<class_GeometryInstance3D_property_ignore_occlusion_culling>`

classref-property-setget

-   `void (No return value.)` **set\_ignore\_occlusion\_culling**(value:
    `bool<class_bool>`)
-   `bool<class_bool>` **is\_ignoring\_occlusion\_culling**()

If `true`, disables occlusion culling for this instance. Useful for
gizmos that must be rendered even when occlusion culling is in use.

\*\*Note:\*\*
`ignore_occlusion_culling<class_GeometryInstance3D_property_ignore_occlusion_culling>`
does not affect frustum culling (which is what happens when an object is
not visible given the camera's angle). To avoid frustum culling, set
`custom_aabb<class_GeometryInstance3D_property_custom_aabb>` to a very
large AABB that covers your entire game world such as
`AABB(-10000, -10000, -10000, 20000, 20000, 20000)`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **lod\_bias** = `1.0`
`🔗<class_GeometryInstance3D_property_lod_bias>`

classref-property-setget

-   `void (No return value.)` **set\_lod\_bias**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_lod\_bias**()

Changes how quickly the mesh transitions to a lower level of detail. A
value of 0 will force the mesh to its lowest level of detail, a value of
1 will use the default settings, and larger values will keep the mesh in
a higher level of detail at farther distances.

Useful for testing level of detail transitions in the editor.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Material<class_Material>` **material\_overlay**
`🔗<class_GeometryInstance3D_property_material_overlay>`

classref-property-setget

-   `void (No return value.)` **set\_material\_overlay**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_material\_overlay**()

The material overlay for the whole geometry.

If a material is assigned to this property, it will be rendered on top
of any other active material for all the surfaces.

classref-item-separator

------------------------------------------------------------------------

classref-property

`Material<class_Material>` **material\_override**
`🔗<class_GeometryInstance3D_property_material_override>`

classref-property-setget

-   `void (No return value.)` **set\_material\_override**(value:
    `Material<class_Material>`)
-   `Material<class_Material>` **get\_material\_override**()

The material override for the whole geometry.

If a material is assigned to this property, it will be used instead of
any material set in any material slot of the mesh.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **transparency** = `0.0`
`🔗<class_GeometryInstance3D_property_transparency>`

classref-property-setget

-   `void (No return value.)` **set\_transparency**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_transparency**()

The transparency applied to the whole geometry (as a multiplier of the
materials' existing transparency). `0.0` is fully opaque, while `1.0` is
fully transparent. Values greater than `0.0` (exclusive) will force the
geometry's materials to go through the transparent pipeline, which is
slower to render and can exhibit rendering issues due to incorrect
transparency sorting. However, unlike using a transparent material,
setting `transparency<class_GeometryInstance3D_property_transparency>`
to a value greater than `0.0` (exclusive) will *not* disable shadow
rendering.

In spatial shaders, `1.0 - transparency` is set as the default value of
the `ALPHA` built-in.

\*\*Note:\*\*
`transparency<class_GeometryInstance3D_property_transparency>` is
clamped between `0.0` and `1.0`, so this property cannot be used to make
transparent materials more opaque than they originally are.

\*\*Note:\*\* Only supported when using the Forward+ rendering method.
When using the Mobile or Compatibility rendering method,
`transparency<class_GeometryInstance3D_property_transparency>` is
ignored and is considered as always being `0.0`.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **visibility\_range\_begin** = `0.0`
`🔗<class_GeometryInstance3D_property_visibility_range_begin>`

classref-property-setget

-   `void (No return value.)` **set\_visibility\_range\_begin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_visibility\_range\_begin**()

Starting distance from which the GeometryInstance3D will be visible,
taking
`visibility_range_begin_margin<class_GeometryInstance3D_property_visibility_range_begin_margin>`
into account as well. The default value of 0 is used to disable the
range check.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **visibility\_range\_begin\_margin** = `0.0`
`🔗<class_GeometryInstance3D_property_visibility_range_begin_margin>`

classref-property-setget

-   `void (No return value.)`
    **set\_visibility\_range\_begin\_margin**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_visibility\_range\_begin\_margin**()

Margin for the
`visibility_range_begin<class_GeometryInstance3D_property_visibility_range_begin>`
threshold. The GeometryInstance3D will only change its visibility state
when it goes over or under the
`visibility_range_begin<class_GeometryInstance3D_property_visibility_range_begin>`
threshold by this amount.

If
`visibility_range_fade_mode<class_GeometryInstance3D_property_visibility_range_fade_mode>`
is
`VISIBILITY_RANGE_FADE_DISABLED<class_GeometryInstance3D_constant_VISIBILITY_RANGE_FADE_DISABLED>`,
this acts as a hysteresis distance. If
`visibility_range_fade_mode<class_GeometryInstance3D_property_visibility_range_fade_mode>`
is
`VISIBILITY_RANGE_FADE_SELF<class_GeometryInstance3D_constant_VISIBILITY_RANGE_FADE_SELF>`
or
`VISIBILITY_RANGE_FADE_DEPENDENCIES<class_GeometryInstance3D_constant_VISIBILITY_RANGE_FADE_DEPENDENCIES>`,
this acts as a fade transition distance and must be set to a value
greater than `0.0` for the effect to be noticeable.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **visibility\_range\_end** = `0.0`
`🔗<class_GeometryInstance3D_property_visibility_range_end>`

classref-property-setget

-   `void (No return value.)` **set\_visibility\_range\_end**(value:
    `float<class_float>`)
-   `float<class_float>` **get\_visibility\_range\_end**()

Distance from which the GeometryInstance3D will be hidden, taking
`visibility_range_end_margin<class_GeometryInstance3D_property_visibility_range_end_margin>`
into account as well. The default value of 0 is used to disable the
range check.

classref-item-separator

------------------------------------------------------------------------

classref-property

`float<class_float>` **visibility\_range\_end\_margin** = `0.0`
`🔗<class_GeometryInstance3D_property_visibility_range_end_margin>`

classref-property-setget

-   `void (No return value.)`
    **set\_visibility\_range\_end\_margin**(value: `float<class_float>`)
-   `float<class_float>` **get\_visibility\_range\_end\_margin**()

Margin for the
`visibility_range_end<class_GeometryInstance3D_property_visibility_range_end>`
threshold. The GeometryInstance3D will only change its visibility state
when it goes over or under the
`visibility_range_end<class_GeometryInstance3D_property_visibility_range_end>`
threshold by this amount.

If
`visibility_range_fade_mode<class_GeometryInstance3D_property_visibility_range_fade_mode>`
is
`VISIBILITY_RANGE_FADE_DISABLED<class_GeometryInstance3D_constant_VISIBILITY_RANGE_FADE_DISABLED>`,
this acts as a hysteresis distance. If
`visibility_range_fade_mode<class_GeometryInstance3D_property_visibility_range_fade_mode>`
is
`VISIBILITY_RANGE_FADE_SELF<class_GeometryInstance3D_constant_VISIBILITY_RANGE_FADE_SELF>`
or
`VISIBILITY_RANGE_FADE_DEPENDENCIES<class_GeometryInstance3D_constant_VISIBILITY_RANGE_FADE_DEPENDENCIES>`,
this acts as a fade transition distance and must be set to a value
greater than `0.0` for the effect to be noticeable.

classref-item-separator

------------------------------------------------------------------------

classref-property

`VisibilityRangeFadeMode<enum_GeometryInstance3D_VisibilityRangeFadeMode>`
**visibility\_range\_fade\_mode** = `0`
`🔗<class_GeometryInstance3D_property_visibility_range_fade_mode>`

classref-property-setget

-   `void (No return value.)`
    **set\_visibility\_range\_fade\_mode**(value:
    `VisibilityRangeFadeMode<enum_GeometryInstance3D_VisibilityRangeFadeMode>`)
-   `VisibilityRangeFadeMode<enum_GeometryInstance3D_VisibilityRangeFadeMode>`
    **get\_visibility\_range\_fade\_mode**()

Controls which instances will be faded when approaching the limits of
the visibility range. See
`VisibilityRangeFadeMode<enum_GeometryInstance3D_VisibilityRangeFadeMode>`
for possible values.

classref-section-separator

------------------------------------------------------------------------

classref-descriptions-group

## Method Descriptions

classref-method

`Variant<class_Variant>` **get\_instance\_shader\_parameter**(name:
`StringName<class_StringName>`)
`const (This method has no side effects. It doesn't modify any of the instance's member variables.)`
`🔗<class_GeometryInstance3D_method_get_instance_shader_parameter>`

Get the value of a shader parameter as set on this instance.

classref-item-separator

------------------------------------------------------------------------

classref-method

`void (No return value.)` **set\_instance\_shader\_parameter**(name:
`StringName<class_StringName>`, value: `Variant<class_Variant>`)
`🔗<class_GeometryInstance3D_method_set_instance_shader_parameter>`

Set the value of a shader uniform for this instance only ([per-instance
uniform](../tutorials/shaders/shader_reference/shading_language.html#per-instance-uniforms)).
See also
`ShaderMaterial.set_shader_parameter<class_ShaderMaterial_method_set_shader_parameter>`
to assign a uniform on all instances using the same
`ShaderMaterial<class_ShaderMaterial>`.

\*\*Note:\*\* For a shader uniform to be assignable on a per-instance
basis, it *must* be defined with `instance uniform ...` rather than
`uniform ...` in the shader code.

\*\*Note:\*\* `name` is case-sensitive and must match the name of the
uniform in the code exactly (not the capitalized name in the inspector).

\*\*Note:\*\* Per-instance shader uniforms are currently only available
in 3D, so there is no 2D equivalent of this method.
